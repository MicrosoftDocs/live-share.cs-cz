---
title: Řešení potíží | Microsoft Docs
description: Tipy a triky pro řešení potíží pro Visual Studio Live Share.
ms.custom: ''
ms.date: 03/22/2018
ms.reviewer: ''
ms.suite: ''
ms.topic: troubleshooting
author: chuxel
ms.author: clantz
manager: AmandaSilver
ms.workload:
- liveshare
ms.openlocfilehash: 692e129252ac92c159660842b62a45fe4f7db864
ms.sourcegitcommit: 9deed590c0876b732c8eb150a9a23498a8243efc
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/27/2021
ms.locfileid: "98870847"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="troubleshooting-visual-studio-live-share"></a>Řešení potíží s Visual Studio Live Share

Tento článek popisuje tipy k odstraňování potíží, alternativní řešení a odpovědi na běžné problémy a otázky. Můžete si také prohlédnout [Nejčastější dotazy](faq.md). 

## <a name="installation--tool-requirements"></a>Požadavky na instalaci/nástroj

Níže najdete tipy k odstraňování potíží souvisejících s instalací Visual Studio Live Share.

| Nástroj | Problém | Řešení/alternativní řešení |
|------|---------|------------|
|VS Code <strong>(MacOS)</strong>| Zobrazí se upozornění s informací o tom, že váš MacOS již není <strong> podporován rozhraním .NET Core. <strong>| Toto upozornění se zobrazí v důsledku nedávné aktualizace, kterou [provedla .NET Core](https://docs.microsoft.com/en-us/dotnet/core/install/dependencies?tabs=netcore31&pivots=os-macos) , která už nepodporuje žádné verze nižší než <strong>Vysoký Sierra (10.13 +).</strong> Pokud chcete povolit rozšíření Live Share, aktualizujte prosím operační systém.
| sada VS | Instalační program rozšíření <strong>nemůže najít verzi sady Visual Studio</strong> , která se má použít při pokusu o instalaci rozšíření Visual Studio Live Share. | Visual Studio Live Share vyžaduje **Visual Studio 2017 verze 15,6** nebo vyšší pro hostitele i hosty. Nainstalujte nejnovější stabilní [aktualizaci sady Visual Studio 2017](https://visualstudio.com/vs/) a zkuste to znovu. |
| VS Code | V případě, že se **nedají nainstalovat závislosti**, se zobrazí chyba při prvním spuštění rozšíření se **dokončí instalace** nebo dojde k chybám **nebo už přítomných souborů**. | Ověřte, že jste připojeni k **síťovému připojení**. Pokud se jedná o, můžete být spuštěni na **proxy serveru nebo na problém s bránou firewall** . Podívejte se na téma [řešení potíží s připojením](#connectivity). <br /><br />|
| VS Code | Instalace rozšíření Visual Studio Live Share z webu Marketplace <strong>ho nainstaluje ve verzi stabilní/insider vs Code</strong> místo verze, kterou chci. | Zahajte VS Code stabilní nebo Insider v závislosti na vaší předvolbách, klikněte na kartu rozšíření, vyhledejte "Visual Studio Live Share" a z něj nainstalujte. |
| VS Code (**Linux**) | Rozšíření Live Share se neaktivuje a po instalaci rozšíření na **Linux** **se nezobrazí žádné položky stavového řádku** . | Visual Studio Live Share závisí na rozhraní .NET Core 2,0, které má řadu požadavků na Linux, které nemusí být ve výchozím nastavení splněné v některých distribucích systému Linux. Podrobnosti o tom, co je potřeba nainstalovat, najdete [tady](reference/linux.md#install-linux-prerequisites) . |

## <a name="sign-in"></a>Přihlásit se

Níže najdete tipy pro řešení problémů s přihlašováním.

| Nástroj | Problém | Řešení/alternativní řešení |
|------|---------|------------|
| sada VS | Musíte se přihlásit k Visual Studio Live Share s <strong>jinou identitou</strong> , než použijete k přihlášení do sady Visual Studio. | V nabídce nástroje > možnosti > Live Share > uživatelský účet vyberte alternativní účet. |
| VS Code | Když se během přihlašování otevře okno prohlížeče a proces na <strong>webové stránce vypadá úspěšně</strong>, stavový řádek <strong>stále říká, "přihlásit"</strong> po zavření prohlížeče. | Po přihlášení klikněte na "máte potíže?" a postupujte podle pokynů a do nástroje zadejte dočasný uživatelský kód.<br /><br />Rádi bychom také viděli, co se může stát, a [zaprotokolovat chybu](https://aka.ms/vsls-problem). |
| Vše | Zobrazuje se <strong>časový limit nebo Chyba připojení</strong>. | Podívejte se na téma [řešení potíží s připojením](#connectivity). |
| Vše | Když se přihlašujete pomocí **pracovní nebo školní e-mailové adresy** Microsoftu, zobrazí se zpráva, že je **potřeba schválit správce**. | Vaše služba Azure AD principem je nastavená tak, aby vyžadovala "souhlas správce" pro nové aplikace, které přistupují k obsahu adresáře. Další podrobnosti najdete [tady](reference/security.md). |
| VS Code (**MacOS**) | Při přihlašování se zobrazí chyba s oznámením, že **SecKeychainAddGenericPassword () selhalo**. | To je téměř vždy kvůli běžnému problému s macOS, kde se změny hesla neprojeví v řetězci přihlašovacích údajů. Zkuste přejít do řetězce "přístup k řetězci klíčů", uzamknout přihlašovací řetězec řetězce a pak ho znovu odemknout. To může být dostačující pro vyřešení problému, ale pokud ho nemůžete odemknout s vaším aktuálním heslem, vyzkoušejte si předchozí. Pokud to funguje, změňte přihlašovací heslo řetězce klíčů na vaše aktuální heslo. Podrobnosti najdete [tady](https://support.apple.com/en-us/HT201609) . |
| VS Code (**Linux**) | Při zadávání v uživatelském kódu po přihlášení přes prohlížeč se zobrazí chyba s oznámením, že **secret_password_store_sync () selhala s kódem chyby XX**. | Obvykle je to způsobeno `gnome-keyring` nebo `libsecret-1-0` /  `libsecret` není nainstalováno. Pomocí `seahorse` aplikace "hesla a klíče" v desktopovém prostředí můžete ověřit, že je služba GNOME-Key Ring správně nakonfigurovaná. Další informace o [požadavcích pro Linux najdete tady](reference/linux.md#install-linux-prerequisites). |
| VS Code (**Linux**) | Zobrazí se <strong>výzva k zadání uživatelského kódu</strong> s Live Share v 0.3.295 nebo níže, ale nezobrazí se žádný prohlížeč, který vám to umožňuje získat ho. | Pracujeme na odstranění požadavku na kód uživatele v systému Linux. Ve středním čase by se měl zobrazit okno prohlížeče, které se používá k přihlášení. V takovém případě může být okno prohlížeče v VS Code skryté. Pokud se nejedná o tento případ, podívejte se na další tip.  |
| VS Code | Po kliknutí na přihlásit (nebo pomocí příkazu "Live Share: Sign in") <strong>se nezobrazí žádné okno prohlížeče, které vám umožní zadat přihlašovací údaje</strong>. | 1. [Přihlaste se sem](https://insiders.liveshare.vsengsaas.visualstudio.com/auth/login) .<br />2. po přihlášení klikněte na "máte potíže?"<br /> 3. postupujte podle pokynů a do nástroje zadejte dočasný uživatelský kód. |
| Vše | Chtěli byste se <strong>připojit</strong> k relaci spolupráce, </strong> ale <strong>nechcete dostávat e-mailové aktualizace</strong>. | Přihlášení k rozšíření Live Share v aplikaci VS/VS Code <strong>neumožňuje přijímat</strong> aktualizace e-mailů.<br /><br />Live Share vyžaduje, aby se hosté přihlásili jako bezpečnostní opatření, takže hostitel bude mít přehled o identitě těch, ke kterým se připojili. [Tuto funkci můžete hlasovat](https://github.com/MicrosoftDocs/live-share/issues/3) , pokud chcete, aby se anonymní uživatelé mohli připojit (například uživatelé bez názvu nebo uživatelem definovaný název). |

## <a name="share-and-join"></a>Sdílet a připojit

Níže najdete tipy pro řešení problémů s přihlašováním.

| Nástroj | Problém | Řešení/alternativní řešení |
|------|----------------|------------|
| Vše | <strong>Sdílet/připojit:</strong> Obdržíte časový limit nebo chybu, se kterou se nemůžete připojit. | Podívejte se na téma [řešení potíží s připojením](#connectivity). |
| VS Code | <strong>Připojit:</strong> Po otevření stránky pro spojení v prohlížeči se vám <strong>nezobrazila výzva/spuštění vs Code</strong> . |  Tipy: <ul><li>Ujistěte se, že jste <i>spustili vs Code aspoň jednou a čekali na dokončení instalace na stavovém řádku.</i></li><li>Pokud to nepomůže, zkuste spustit příkaz Live Share: spuštění instalačního programu.</li><li>**Uživatelé systému Linux**: Pokud se zobrazí výzva k zadání hesla správce (sudo) při spuštění výše uvedeného příkazu, udělejte to prosím.</li><li>Nakonec se podívejte na alternativní řešení v části [připojení ručně](reference/manual-join.md) .</li></ul> Pokud tento problém obdržíte, rádi bychom zjistili, co se děje, a [zaprotokolovat chybu](https://aka.ms/vsls-new-issue). |
| sada VS | <strong>Připojit:</strong> Po otevření stránky pro spojení v prohlížeči jste <strong>nemuseli zobrazit ani </strong> po otevření. |  Podívejte se na téma [ruční připojení](reference/manual-join.md).<br /><br /> Rádi bychom také viděli vaše protokoly, takže si [Zaprotokolujte chybu](https://aka.ms/vsls-problem) pomocí možnosti nahlásit problém pomocí sady Visual Studio. zapnut. |
| Vše | <strong>Připojit:</strong> Doporučuje se <strong>Vložit odkaz spojení přímo do sady Visual Studio nebo vs Code</strong> místo kliknutí na webový odkaz. | Podívejte se na téma [ruční připojení](reference/manual-join.md). |
| Vše | <strong>Připojit:</strong> Zobrazí se zpráva "**vlastník pracovního prostoru vypadá jako offline**," při připojení přes prohlížeč. | Možná alternativní řešení:<br /><ul><li>Zkuste se [připojit ručně](reference/manual-join.md). Zjistili jsme problémy s spojeními mezi oblastí (např. východ a západní USA) z důvodu problémů se službou, které neovlivňují ruční spojení.</li><li>Live Share nemůže být při spuštění v režimu připojení automaticky směrován přímo na hostitele. Vyzkoušejte [Přenosový režim](reference/connectivity.md).</li></ul>Další možnosti najdete v tématu [řešení potíží s připojením](#connectivity) . |
| VS Code | <strong>Připojit:</strong> Připojili jste se přes prohlížeč <strong>před přihlášením</strong>, nebyli vyzváni k přihlášení </strong> a připojení se nikdy nedokončí. |  Jedná se o [známou chybu](https://github.com/MicrosoftDocs/live-share/issues/167). Klikněte na položku Přihlásit se stavovým řádkem a přihlaste se a potom se znovu připojte. |

## <a name="connectivity"></a>Připojení

Následující informace vám můžou pomoct při řešení potíží s připojením nebo vypršením časových limitů při přihlašování, sdílení nebo spojování.

Jak je uvedeno v požadavcích na [připojení Live Share](reference/connectivity.md) článku, různé režimy připojení mají různé požadavky na fungování, takže existuje několik různých potenciálních problémů.

| Nástroj | Problém | Pravděpodobná příčina |
|------|------|----------------|
| Vše | Používáte <strong>proxy server</strong> a zobrazuje se počet problémů s připojením. | Nastavení proxy serveru může být obtížné.  Zkuste nastavit **http_proxy** a proměnné prostředí **HTTPS_PROXY** **globálně** a pak restartujte nástroj. Další podrobnosti najdete v tématu [nastavení proxy serveru](reference/connectivity.md#proxies) . Je možné, že některé konfigurace ještě nepodporujeme, abychom [nás věděli](https://github.com/MicrosoftDocs/live-share/issues/86) , že vám to nevyhovuje. |
| VS Code | Po instalaci rozšíření a spuštění VS Code poprvé dojde k <strong>chybě, když se ve stavovém řádku zobrazí zpráva "dokončí instalaci"</strong>. |  Nemůžete získat přístup k Internetu ani přístup k download.visualstudio.microsoft.com a/nebo download.microsoft.com na portu 443, který vaše osobní nebo podniková brána firewall zablokovala. V [této části najdete informace](https://github.com/MicrosoftDocs/live-share/issues/58) o tom, proč Live Share potřebují stáhnout něco v tomto okamžiku. |
| Vše | <strong>Nemůžete se přihlásit Visual Studio Live Share</strong> | Nemůžete získat přístup k Internetu ani přístup k *. liveshare.vsengsaas.visualstudio.com na portu 80/443 je zablokovaný vaší osobní nebo firemní bránou firewall. Zadejte https://insiders.liveshare.vsengsaas.visualstudio.com v prohlížeči a ověřte, že jste na domovské stránce Visual Studio Live Share. |
| Vše | Pracujete v <strong>automatickém režimu</strong> (výchozí možnost), můžete se přihlásit, ale při sdílení nebo připojení se zobrazí <strong>Chyba s časovým limitem nebo připojením</strong> . | Buď přímé přenosové režimy, nebo došlo k chybě v režimu automatického přenosu. Pokud se budete moci připojit po [Přepnutí do režimu přímého nebo přenosu](reference/connectivity.md#changing-the-connection-mode), [vyvolejte chybu](https://aka.ms/vsls-problem). |
| Vše | Jste v <strong>přímém režimu</strong>, budete se moct přihlásit, ale při sdílení nebo připojení se zobrazí <strong>Chyba s časovým limitem nebo připojením</strong> . | Host a hostitel se nemohou přímo připojit. Vyzkoušejte si [režim automatického nebo přenosu](reference/connectivity.md#changing-the-connection-mode) , abyste viděli, jestli problém nezmizí. Možná budete muset [ručně Live Share přes osobní bránu firewall](reference/connectivity.md#manually-adding-a-firewall-entry) nebo jednoduše použít režim přenosu. |
| Vše | Jste v <strong>režimu přenosu</strong>, máte možnost se přihlásit, ale při sdílení nebo připojení se zobrazí oznámení o <strong>vypršení časového limitu nebo chybě připojení</strong> . | Přístup k *. servicebus.windows.net na portu 80/443 je blokovaný vaší osobní nebo podnikovou bránou firewall. Vyzkoušejte [přímý režim](reference/connectivity.md#changing-the-connection-mode). |

Další informace o požadavcích na připojení najdete v článku [požadavky na připojení pro Live Share](reference/connectivity.md) .

## <a name="see-also"></a>Viz také

Rychlý start

- [Sdílení prvního projektu](quickstart/share.md)
- [Připojení k první relaci](quickstart/join.md)

Postupy

- [Spolupráce ve Visual Studio Code](use/vscode.md)
- [Spolupráce v sadě Visual Studio](use/vs.md)

Reference

- [Všechny hlavní chyby, žádosti o funkce a omezení](https://aka.ms/vsls-issues)
- [Všechny požadavky a omezení funkcí](https://aka.ms/vsls-feature-requests)
- [Požadavky na připojení pro Live Share](reference/connectivity.md)
- [Podrobnosti o instalaci systému Linux](reference/linux.md)
- [Podpora jazyků a platforem](reference/platform-support.md)
- [Podpora rozšíření](reference/extensions.md)

Pořád máte problémy? Můžete [poskytnout zpětnou vazbu](support.md).
