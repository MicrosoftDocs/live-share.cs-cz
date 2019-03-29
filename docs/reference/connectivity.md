---
title: Připojení – za sdílené složky sady Visual Studio | Dokumentace Microsoftu
description: Informace o připojení a připojení režimy pro Visual Studio Live Share.
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
ms.openlocfilehash: c685df798fc10b449c3e73db678e3b5d34e73ef0
ms.sourcegitcommit: 100fce9b9bbcd7e6f68d40659bd2760e9537de37
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/29/2019
ms.locfileid: "58640078"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="connectivity-requirements-for-live-share"></a>Požadavky na připojení pro Live Share

Tento článek shrnuje požadavky na připojení pro Visual Studio Live Share, možnosti připojení k dispozici a známé alternativní řešení v případě potřeby.

## <a name="sign-in"></a>Přihlášení

Se můžete přihlásit pomocí libovolné Live Share [Azure Active Directory](https://azure.microsoft.com/en-us/services/active-directory) zajištěnou pracovní nebo školní účet [účtu Microsoft](https://account.microsoft.com/account), nebo [profilu Githubu](https://github.com/). Obvykle přihlašovací adresy URL pro tyto jsou otevřené ve většině organizací počet veřejný internetový produkty, které je používají, ale pokud ne, obraťte se na správce sítě o otevírání `login.microsoftonline.com` a/nebo `github.com` kromě domény [níže uvedené](#requirements-for-connection-modes).

> [!NOTE]
> Místní účty AD (AD FS) a účtů GitHub Enterprise v místním prostředí nejsou aktuálně podporované [(nahoru hlas 👍)](https://github.com/MicrosoftDocs/live-share/issues/341).

## <a name="connection-modes"></a>Režimy připojení

K zajištění optimálního výkonu, ve výchozím nastavení Visual Studio Live Share automaticky zjišťuje, zda spolupráci relace hostitelský počítač a hostovaný počítač může komunikovat přímo přes síť a předává pouze přes cloud, pokud neexistuje žádná trasa mezi nimi. Tento režim smíšené "auto" je flexibilní a i umožňuje některé hostům relay přes cloud, zatímco ostatní připojit přímo pro stejnou relaci.

Přímé spojení přes cloudový mechanismus pro zajištění zabezpečení, ale vyžadují otevřít port mezi 5990 a 5999 Pokud chcete umožnit připojení k ověření. V důsledku toho při prvním sdílení plochy brána firewall může vyzvat otevření portu. Přijetí, že toto je volitelné, protože ignoruje ji jednoduše způsobí, že Live Share, vždy používali relay v režimu auto.

Všechna připojení v aplikaci Visual Studio Live Share jsou SSH nebo SSL zašifrované a ověřování proti centrální služby k zajištění, že pouze ty v relaci spolupráce můžou získat přístup k jeho obsahu. Kromě toho relay cloud Live Share nezachová veškerý provoz směrovat přes něj a není "stará" provoz žádným způsobem.

## <a name="changing-the-connection-mode"></a>Změna režimu připojení

Pokud chcete zakázat připojení s přímým přístupem nebo přes předávací službu nebo jednoduše řešíte problémy s připojením, které donutí jiné režimy připojení.

| Režim | Chování hostitele | Chování hosta |
|------|----------------|----------------------|
| Auto | Relaci spolupráce hostitele přijme zabezpečenou, ověřený přímé připojení nebo připojení předávané do cloudu. | Pokusí se použít přímé připojení a spadne zpět na předávání přes cloud, když se to nepovede. |
| S přímým přístupem | Relaci spolupráce hostitele přijímá jenom ověřené a zabezpečené připojení s přímým přístupem. | Pokusí se použít přímé připojení a zastaví, pokud se nelze připojit. |
| Propojení | Spolupráce relace hostiteli neumožňuje přímé připojení. Port se otevírá ve službě hostitelském počítači. | Vždy připojí přes cloud. |

Chcete-li změnit režim:

**VS:**

1. Přejděte na Nástroje > Možnosti > Live sdílené složky.
2. Vyberte režim z rozevíracího seznamu "Režim připojení".
3. Restartujte VS.

**VS Code:**

1. Upravit settings.json (Soubor > Předvolby > Nastavení).
2. Nastavte `"liveshare.connectionMode"` k `"auto"`, `"direct"`, nebo `"relay"` v závislosti na vašich předvoleb.
3. Znovu spusťte VS Code.

## <a name="requirements-for-connection-modes"></a>Požadavky pro režimy připojení

Určuje, ke kterému jste v režimu připojení určité porty a adresy URL, které musí být dostupné pro Live Share funkce.

| Režim | Požadavek na přístup klienta | Poradce při potížích |
|------|--------------|-----------------|
| Jakýkoli | Odchozí přístup k `*.liveshare.vsengsaas.visualstudio.com:443` | Zkontrolujte vaše firemní nebo osobní síťová brána firewall umožňuje připojení k této doméně. Zadejte https://insiders.liveshare.vsengsaas.visualstudio.com v prohlížeči a ověření budete přesměrováni na domovské stránce Visual Studio Live Share. Možná používáte také do [proxy problémy](#proxies) , které je potřeba vyřešit.|
| Žádné (VS Code) | Odchozí přístup k `download.microsoft.com:443` | Zkontrolujte vaše firemní nebo osobní síťová brána firewall umožňuje připojení k této doméně. Možná používáte také do [proxy problémy](#proxies) , které je potřeba vyřešit. |
| Auto | Auto přepínače. Režimy relay a s přímým přístupem najdete v tématu. | Přepněte na přímé nebo předávání režim pro řešení potíží. |
| S přímým přístupem | Hostitelé: Port v rozsahu 5990 5999 potřeba otevřít tak, aby přijímal příchozí místní síťová připojení.<br /><br />Hosté: Síťová trasa a odchozí přístup k hostiteli na tento stejný port. | Ověřte "vsls agent" neblokují brány firewall na klasické pracovní plochy softwaru pro tento rozsah portů a že příkazem ping mezi sebou. Když Windows a jiné desktopového softwaru by se zobrazit výzva při prvním spuštění agenta, jsme viděli instance, kde zásady skupiny tomu nedocházelo, a budete muset [ručně přidejte položku](#manually-adding-a-firewall-entry). Možná používáte také do [proxy problémy](#proxies) , které je potřeba vyřešit. |
| Propojení | Odchozí přístup k `*.servicebus.windows.net:443`. | Zkontrolujte vaše firemní nebo osobní síťová brána firewall umožňuje připojení k této doméně. Možná používáte také do [proxy problémy](#proxies) , které je potřeba vyřešit.|

## <a name="manually-adding-a-firewall-entry"></a>Ruční přidání brány firewall položky

Jak je uvedeno výš, přímý režim vyžaduje, aby osobní bráně firewall povolit **vsls agenta** tak, aby přijímal připojení v portu v rozsahu 5990 5999. Pokud chcete použít režim s přímým přístupem, ale zjistili, že brána firewall nemá zadání vsls agenta, můžete ji přidat ručně. Tento postup se liší podle software brány firewall, ale můžete si projít informace o  **[konfigurace brány Windows Firewall zde](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-firewall/create-an-inbound-program-or-service-rule)**.

Pokud se nezobrazí položka pro vsls agenta, najdete agenta spustitelný soubor v jednom z následujících umístění.

### <a name="vs-code-agent-location"></a>Umístění agenta VS Code

Náhradní **verze** pro číslo verze rozšíření v jednom z následujících možností:

- **macOS, Linux**

    `$HOME/.vscode/extensions/ms-vsliveshare.vsliveshare-VERSION/dotnet_modules/vsls-agent`

- **Windows**

    `%USERPROFILE%\.vscode\extensions\ms-vsliveshare.vsliveshare-VERSION\dotnet_modules\vsls-agent.exe`

### <a name="visual-studio-agent-location"></a>Umístění agenta aplikace Visual Studio

Umístění sady Visual Studio je dynamičtější, ale můžete postupovat podle těchto pokynů vyhledejte spustitelný soubor:

1. Přejděte do umístění instalace sady Visual Studio. Obvykle se jedná `C:\Program Files (x86)\Microsoft Visual Studio\EDITION` kde **EDITION** je komunity, Enterprise atd.

2. Spustit hledání `vsls-agent.exe` v pod **IDE\Extensions** podsložky.

Bohužel se budete muset provést tento krok **pokaždé, když aktualizujete aplikaci Visual Studio Live Share.**

## <a name="proxies"></a>Proxy servery

Visual Studio Live Share aktuálně má určitá omezení kolem proxy serveru využívají. Během automatického nastavení serveru proxy by měl pracovat na Windows, při použití systému macOS nebo Linux (a pomocí některých konfiguracích proxy serveru na Windows) **HTTP_PROXY** a **HTTPS_PROXY** muset proměnné prostředí nastavit *globálně*.

Pokud váš proxy server toto za vás nebude automaticky nastavení, můžete ručně nastavit proměnné v následujícím tvaru:

`HTTPS_PROXY=http://proxy-ip-address:proxyport`

Pokud máte ověřovací proxy server, můžete přidat uživatele a heslo:

`HTTPS_PROXY=http://user:password@proxy-ip-address:proxyport`

Pokud toto nastavení není problém vyřešit, [dejte nám prosím vědět](https://github.com/MicrosoftDocs/live-share/issues/86) specifika vašeho proxy serveru nastavit, aby nám můžete podívejte se na vylepšení podpory.

## <a name="see-also"></a>Viz také:

- [Postupy: Spolupráce pomocí Visual Studio Code](../use/vscode.md)
- [Postupy: Spolupráce pomocí sady Visual Studio](../use/vs.md)
- [Funkce zabezpečení Live Share](security.md)

Máte potíže? Podívejte se na článek o [odstraňování potíží](../troubleshooting.md) nebo nám [pošlete svůj názor](../support.md).
