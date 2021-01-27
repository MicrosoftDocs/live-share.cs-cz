---
title: Připojení | Microsoft Docs
description: Informace o připojení a režimech připojení pro Visual Studio Live Share.
ms.custom: ''
ms.date: 03/22/2018
ms.reviewer: ''
ms.suite: ''
ms.topic: reference
author: chuxel
ms.author: clantz
manager: AmandaSilver
ms.workload:
- liveshare
ms.openlocfilehash: e1a2567b18e7dbd30d86e49a22950d300fb0a95b
ms.sourcegitcommit: 9deed590c0876b732c8eb150a9a23498a8243efc
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/27/2021
ms.locfileid: "98870523"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="connectivity-requirements-for-live-share"></a>Požadavky na připojení pro Live Share

Tento článek shrnuje požadavky na připojení pro Visual Studio Live Share, dostupné možnosti připojení a známá řešení v případě potřeby.

## <a name="sign-in"></a>Přihlásit se

K Live Share se můžete přihlásit pomocí [Azure Active Directory](https://azure.microsoft.com/en-us/services/active-directory) zálohovaného pracovního nebo školního účtu, [účet Microsoft](https://account.microsoft.com/account)nebo [profilu GitHubu](https://github.com/). Obvykle jsou adresy URL pro přihlášení pro tyto produkty ve většině organizací otevřené, a to s ohledem na počet veřejných produktů, které je používají, ale pokud ne, požádejte správce sítě o otevření `login.microsoftonline.com` a/nebo `github.com` kromě domén [uvedených níže](#requirements-for-connection-modes).

> [!NOTE]
> Účty AD FS (on-Prem AD) a účty na Prem GitHubu na webu nejsou v současné době podporovány [(Hlasujte 👍 )](https://github.com/MicrosoftDocs/live-share/issues/341).

## <a name="connection-modes"></a>Režimy připojení

Aby se zajistil optimální výkon, ve výchozím nastavení Visual Studio Live Share automaticky detekuje, jestli počítač hostitele relace spolupráce a počítač hosta můžou komunikovat přímo přes síť a přenáší se jenom přes Cloud, pokud mezi nimi neexistují žádné trasy. Tento smíšený režim "automatické" je flexibilní a dokonce umožňuje některým hostům přenášet přes Cloud, zatímco ostatní se připojují přímo ke stejné relaci.

Přímá připojení se ověřují prostřednictvím cloudového mechanismu, aby se zajistilo zabezpečení, ale vyžaduje se otevření portu mezi 5990 a 5999, aby bylo možné připojení povolit. V důsledku toho se při prvním sdílení může zobrazit výzva k otevření portu v bráně firewall vaší plochy. Přijetí tohoto požadavku je volitelné, protože ho ignoruje, stačí, když Live Share vždycky používat předávání v automatickém režimu.

Všechna připojení v Visual Studio Live Share jsou zašifrovaná pomocí protokolu SSH nebo SSL a ověřená proti centrální službě, aby se zajistilo, že k obsahu budou mít přístup jenom ty, které jsou v relaci spolupráce. Cloud Relay Live Share navíc neuchovává žádný provoz, který je prostřednictvím něj směrován, a žádným způsobem nepracuje s přenosy "Snoop".

## <a name="changing-the-connection-mode"></a>Změna režimu připojení

Pokud chcete zakázat přímá nebo přepřenosná připojení nebo jednoduše řešit problémy s připojením, můžete vynutit jiné režimy připojení.

| Režim | Chování hostitele | Chování hostů |
|------|----------------|----------------------|
| Auto | Relace spolupráce hostitele přijímá zabezpečená, ověřená přímá připojení nebo připojení v cloudu. | Pokusí se použít přímé připojení a vrátit se k předávání přes Cloud v případě, že dojde k chybě. |
| Direct | Relace spolupráce hostitele přijímá pouze ověřená a zabezpečená přímá připojení. | Pokusí se použít přímé připojení a zastaví se, pokud se nemůže připojit. |
| Propojení | Relace spolupráce hostitele nepovoluje přímá připojení. Na počítači hostitele není otevřený žádný port. | Vždy se připojuje přes Cloud. |

Postup změny režimu:

**INFRASTRUKTURA**

1. V nabídce nástroje > možnosti > Live Share.
2. Vyberte režim v rozevíracím seznamu "režim připojení".
3. Restartujte VS.

**VS Code:**

1. Upravit settings.jszapnuto (Předvolby > souborů > nastavení).
2. Nastavte `"liveshare.connectionMode"` na `"auto"` , `"direct"` nebo `"relay"` v závislosti na vaší předvolbách.
3. Restartujte VS Code.

## <a name="requirements-for-connection-modes"></a>Požadavky na režimy připojení

Režim připojení, ve kterém se nacházíte, určí konkrétní porty a adresy URL, které musí být k dispozici, aby mohla Live Share fungovat.

| Režim | Požadavek na klientský přístup | Řešení potíží |
|------|--------------|-----------------|
| Libovolný | Odchozí přístup k `*.liveshare.vsengsaas.visualstudio.com:443` | Ujistěte se, že vaše firemní nebo osobní síťová brána firewall vám umožní připojit se k této doméně. Zadejte https://insiders.liveshare.vsengsaas.visualstudio.com v prohlížeči a ověřte, že jste na domovské stránce Visual Studio Live Share. Můžete také spustit [problémy proxy](#proxies) , které je třeba vyřešit.|
| Any (VS Code) | Odchozí přístup k `download.microsoft.com:443` | Ujistěte se, že vaše firemní nebo osobní síťová brána firewall vám umožní připojit se k této doméně. Můžete také spustit [problémy proxy](#proxies) , které je třeba vyřešit. |
| Auto | Automatické přepínače. Viz režimy přímých a přenosů. | Přepněte na přímý nebo předávací režim a odstraňte potíže. |
| Direct | Hostitelé: pro příjem příchozích místních síťových připojení je potřeba otevřít port v rozsahu 5990-5999.<br /><br />Hosté: Síťová trasa a odchozí přístup k hostiteli na tomto stejném portu. | Ověřte, jestli váš software brány firewall pro tento rozsah portů neblokoval "vsls-agent" a že můžete provést příkaz k dalšímu příkazu k otestování. I když by se vám systém Windows a jiný desktopový software měl vyzvat k prvnímu spuštění agenta, zjistili jsme instance, které brání zásadám skupiny v tom, aby se to stalo, a budete muset [položku přidat ručně](#manually-adding-a-firewall-entry). Můžete také spustit [problémy proxy](#proxies) , které je třeba vyřešit. |
| Propojení | Odchozí přístup pro `*.servicebus.windows.net:443` . | Ujistěte se, že vaše firemní nebo osobní síťová brána firewall vám umožní připojit se k této doméně. Můžete také spustit [problémy proxy](#proxies) , které je třeba vyřešit.|

## <a name="manually-adding-a-firewall-entry"></a>Ruční přidání položky brány firewall

Jak je uvedeno výše, přímý režim vyžaduje, aby osobní brána firewall povolovala **vsls agenta** pro přijímání připojení v rozsahu portů 5990-5999. Pokud chcete použít přímý režim, ale zjistili jste, že brána firewall nemá položku vsls-agent, můžete ji přidat ručně. Postup se liší podle softwaru brány firewall, ale tady můžete najít informace o **[konfiguraci brány Windows Firewall](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-firewall/create-an-inbound-program-or-service-rule)**.

Pokud nevidíte záznam pro vsls-agent, můžete najít spustitelný soubor agenta v jednom z následujících umístění.

### <a name="vs-code-agent-location"></a>Umístění agenta VS Code

**Nahraďte číslo verze rozšíření** v jedné z následujících cest:

- **macOS, Linux**

    `$HOME/.vscode/extensions/ms-vsliveshare.vsliveshare-VERSION/dotnet_modules/vsls-agent`

- **Windows**

    `%USERPROFILE%\.vscode\extensions\ms-vsliveshare.vsliveshare-VERSION\dotnet_modules\vsls-agent.exe`

### <a name="visual-studio-agent-location"></a>Umístění agenta sady Visual Studio

Umístění sady Visual Studio je dynamičtější, ale pomocí těchto kroků můžete najít spustitelný soubor:

1. Přejděte do umístění instalace sady Visual Studio. Většinou se jedná `C:\Program Files (x86)\Microsoft Visual Studio\EDITION` o **edici** Community, Enterprise atd.

2. Spusťte hledání `vsls-agent.exe` v části pod podsložkou **IDE\Extensions** .

Tento krok možná budete muset udělat při **každé aktualizaci Visual Studio Live Share.**

## <a name="proxies"></a>Proxy

Visual Studio Live Share má v tuto chvíli nějaká omezení týkající se použití proxy serveru. Přestože automatické nastavení proxy serveru by mělo fungovat ve Windows, při použití macOS nebo Linux (a s některými konfiguracemi proxy ve Windows), musí být proměnné prostředí **http_proxy** a **HTTPS_PROXY** nastavené *globálně*.

Pokud to váš proxy server nenastaví automaticky, můžete proměnné nastavit ručně v následujícím tvaru:

`HTTPS_PROXY=http://proxy-ip-address:proxyport`

Pokud máte ověřující proxy server, můžete přidat uživatele a heslo následujícím způsobem:

`HTTPS_PROXY=http://user:password@proxy-ip-address:proxyport`

Pokud tato nastavení problém nevyřeší, [sdělte nám prosím informace](https://github.com/MicrosoftDocs/live-share/issues/86) o nastaveních proxy serveru, abychom se mohli podívat na vylepšení podpory.

## <a name="see-also"></a>Viz také

- [Postupy: spolupráce pomocí Visual Studio Code](../use/vscode.md)
- [Postupy: spolupráce pomocí sady Visual Studio](../use/vs.md)
- [Funkce zabezpečení Live Share](security.md)

Máte potíže? Podívejte se na článek o [odstraňování potíží](../troubleshooting.md) nebo nám [pošlete svůj názor](../support.md).
