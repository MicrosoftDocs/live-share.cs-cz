---
title: Řešení potíží – Visual Studio Live sdílenou složku | Dokumentace Microsoftu
description: Řešení potíží s tipy a triky pro Visual Studio Live Share.
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
ms.openlocfilehash: 5fc611714d148a9ba1d5a6848e0399af753d1a37
ms.sourcegitcommit: 100fce9b9bbcd7e6f68d40659bd2760e9537de37
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/29/2019
ms.locfileid: "58640208"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="troubleshooting-visual-studio-live-share"></a>Řešení potíží s Visual Studio za sdílené složky

Tento článek se týká řešení problémů s tipy, řešení a odpovědi na běžné problémy a otázky. Můžete také podívejte se na [nejčastější dotazy k](faq.md). 

## <a name="installation--tool-requirements"></a>Instalace a požadavky na nástroj

Následující jsou řešení potíží, tipy týkající se instalace Visual Studio Live Share.

| Nástroj | Problém | Řešení nebo alternativní řešení |
|------|---------|------------|
| sada VS | Instalační služba rozšíření <strong>nejde najít verzi sady Visual Studio</strong> při pokusu o použití k instalaci rozšíření Visual Studio Live Share. | Vyžaduje Visual Studio Live Share **Visual Studio 2017 verze 15.6** nebo vyšší pro hostitele a hostů. Nainstalujte nejnovější stabilní verze [aktualizace sady Visual Studio 2017](https://visualstudio.com/vs/) a zkuste to znovu.|
| VS Code | Objeví se chyba při pokusu o použití Visual Studio Live Share s VS Code na macOS <strong>El Capitan nebo jeho podadresářem</strong>. | Visual Studio Live Share pro podporu operačního systému je závislé na .NET Core která aktuálně [pouze podporuje macOS Sierra a vyšší.]((https://github.com/dotnet/core/blob/master/release-notes/2.0/2.0-supported-os.md).) |
| VS Code | A "**závislostí se nepodařilo nainstalovat**" se zobrazí chyba while rozšíření je **dokončuje se instalace** na první spuštění nebo dojde k chybám **chybí nebo je již k dispozici soubory**. | Ověření, jste na **dobré síťové připojení**. Pokud jste, může běžet na **proxy nebo brány firewall** problém. Zobrazit [řešení potíží s připojením](#connectivity). <br /><br />|
| VS Code | Instaluje se rozšíření Visual Studio Live Share z marketplace <strong>umisťuje stable/insiders verzi VS Code</strong> místo verze chci. | Spusťte VS Code stabilní nebo programu insider v závislosti na vašich předvoleb, klikněte na kartu "rozšíření", vyhledejte "Visual Studio Live Share" a instalaci z tohoto místa. |
| VS Code (**Linux**) | Rozšíření Live Share neaktivuje a **se neobjeví žádné položky panelu Stav** po instalaci rozšíření na **Linux**. | Visual Studio Live Share závisí na .NET Core 2.0, který má několik požadavky pro Linux, které nemusí být splněny v některých distribucích systému Linux ve výchozím nastavení. Zobrazit [zde podrobnosti](reference/linux.md#install-linux-prerequisites) na co se má nainstalovat. |

## <a name="sign-in"></a>Přihlášení

Následující jsou tipy pro řešení problémů přihlášení problémy.

| Nástroj | Problém | Řešení nebo alternativní řešení |
|------|---------|------------|
| sada VS | Budete potřebovat k přihlášení do aplikace Visual Studio Live Share s <strong>jinou identitou</strong> než používáte k přihlášení do sady Visual Studio. | Přejděte na Nástroje > Možnosti > Live Share > uživatelský účet a vyberte alternativní účet. |
| VS Code | Zatímco POP prohlížeče okna se během přihlašování a proces <strong>se objeví jako úspěšné na webové stránce</strong>, stavový řádek <strong>stále říká "Sign in"</strong> po zavření prohlížeče. | Po přihlášení klikněte na tlačítko "Se nedaří?" a postupujte podle pokynů k zadání dočasného uživatelský kód do nástroje.<br /><br />Budeme rádi také vidět, co může být děje, tak prosím [protokolovat chybu](https://aka.ms/vsls-problem). |
| Všechny | Se zobrazuje <strong>limitu nebo chybě připojení</strong>. | Zobrazit [řešení potíží s připojením](#connectivity). |
| Všechny | Po přihlášení pomocí služby Microsoft zajišťuje **pracovní nebo školní e-mailovou adresu** zobrazí zpráva, **"Vyžaduje schválení správcem"**. | Vaše zásada Azure AD je nastavená tak, aby vyžadovala "souhlas správce" pro přístup k obsahu adresáře nové aplikace. Zobrazit [tady](reference/security.md) další podrobnosti. |
| VS Code (**macOS**) | Až budete přihlášení zobrazí chyba **SecKeychainAddGenericPassword() nepovedlo**. | Příčinou je téměř vždy běžný problém v systému macOS kde heslo změny se neprojeví v řetězci klíčů přihlášení. Vyzkoušejte si přicházející do "Přístup do řetězce klíčů", uzamčení řetězce klíčů přihlášení a odemknutí znovu. To může být dost informací k vyřešení problému, ale pokud se nemůžete ho odemknout pomocí aktuálního hesla, opakujte předchozí. Pokud to funguje, změňte přístupové heslo pro přihlášení na vaše aktuální heslo. Zobrazit [tady](https://support.apple.com/en-us/HT201609) podrobnosti. |
| VS Code (**Linux**) | Při zadávání v uživatelském kódu po přihlášení v prohlížeči se zobrazí chyba **secret_password_store_sync() selhalo s kódem chyby XX**. | To je obvykle způsobena `gnome-keyring` a/nebo `libsecret-1-0` /  `libsecret` není nainstalována. Můžete ověřit gnome Správce klíčů je správně nakonfigurované nainstalováním `seahorse` a pak pomocí hesla a klíčů."aplikace v prostředí plochy. Další informace o [tady požadavky pro Linux](reference/linux.md#install-linux-prerequisites). |
| VS Code (**Linux**) | Jste <strong>výzva k zadání uživatelského kódu</strong> s Live Share v0.3.295 nebo verzi uvedenou níže, ale žádný prohlížeč, zobrazí se k tomu, abyste ho můžete získat. | Pracujeme na odstranění kódu požadavky uživatelů na Linuxu. Ve střední čas by se zobrazit okno prohlížeče můžete použít k přihlášení. V opačném případě okno prohlížeče může být skrytý pod tlačítkem VS Code. Pokud se nejedná o případ, přečtěte si další tip.  |
| VS Code | Po kliknutí na tlačítko "Sign in" (nebo pomocí "živé sdílené složky: Sign in"příkaz), <strong>žádné okno prohlížeče se zobrazí k tomu, abyste k zadání přihlašovacích údajů</strong>. | 1. [Přihlaste se tady](https://insiders.liveshare.vsengsaas.visualstudio.com/auth/login)<br />2. Po přihlášení klikněte na tlačítko "Se nedaří?"<br /> 3. Postupujte podle pokynů k zadání dočasného uživatelský kód do nástroje. |
| Všechny | Chcete <strong>spojení</strong> relaci spolupráce</strong> ale <strong>ne / nechcete dostávat aktualizace e-mailem</strong>. | Přihlášení k rozšíření Live Share v kódu VS/VS neodpovídá <strong>není</strong> přihlašují přijímají aktualizace e-mailem.<br /><br />Sdílené složky za provozu vyžaduje hosté se přihlásit jako bezpečnostní opatření, že hostitel má přehled pro ty, kteří se připojili k identity. [Hlasovat, až tuto funkci](https://github.com/MicrosoftDocs/live-share/issues/3) Pokud chcete tuto možnost a povolíte anonymním uživatelům připojit (třeba uživatelé bez názvu nebo uživatelem definovaný název). |

## <a name="share-and-join"></a>Sdílené složky a spojení

Následující jsou tipy pro řešení problémů přihlášení problémy.

| Nástroj | Problém | Řešení nebo alternativní řešení |
|------|----------------|------------|
| Všechny | <strong>Sdílené složky/spojení:</strong> Získáte vypršení časového limitu nebo chyba týkající se nebude moct připojit. | Zobrazit [řešení potíží s připojením](#connectivity). |
| VS Code | <strong>Připojte se k:</strong> Jste byli <strong>není výzvami / připojit spusťte VS Code</strong> po otevření stránky spojení v prohlížeči. |  Tipy: <ul><li>Ujistěte se, když jste <i>alespoň jednou spustit VS Code a čekání na dokončení ve stavovém řádku instalace.</i></li><li>Pokud to nefunguje, zkuste spustit "živé sdílené složky: Příkaz pro nastavení Spouštěč".</li><li>**Uživatelé Linuxu**: Pokud se zobrazí výzva k zadání hesla správce (sudo) při spuštění výše uvedeného příkazu, proveďte to.</li><li>A konečně, naleznete v tématu [ruční spojování](reference/manual-join.md) jako alternativní řešení.</li></ul> Pokud dosáhnete tento problém, budeme rádi vidět, co může být děje, tak prosím [protokolovat chybu](https://aka.ms/vsls-new-issue). |
| sada VS | <strong>Připojte se k:</strong> Jste byli <strong>není výzvami / připojit k uvedení VS</strong>  po otevření stránky spojení v prohlížeči. |  Zobrazit [ručně připojit](reference/manual-join.md).<br /><br /> Také rádi, pokud chcete zobrazit protokoly, proto prosím [protokolovat chybu](https://aka.ms/vsls-problem) pomocí sady Visual Studio "sestavy problém..." funkce. |
| Všechny | <strong>Připojte se k:</strong> Chcete raději <strong>vložte odkaz spojení přímo do sady Visual Studio / VS Code</strong> místo kliknutí na webový odkaz. | Zobrazit [ručně připojit](reference/manual-join.md). |
| Všechny | <strong>Připojte se k:</strong> Zobrazí se zpráva oznamující, "**vlastník pracovního prostoru se zdá být offline**," při připojování přes prohlížeč. | Možná řešení:<br /><ul><li>Zkuste [ruční spojování](reference/manual-join.md). Jsme viděli problémy s mezi oblastmi (například východní a západní USA) spojení kvůli problémům s služby, které nemají vliv na ruční spojení.</li><li>Živé sdílení možná nebudete moct směrování přímo do hostitele při spuštění v režimu připojení "auto". Zkuste [přenosový režim](reference/connectivity.md).</li></ul>Zobrazit [řešení potíží s připojením](#connectivity) pro víc možností |
| VS Code | <strong>Připojte se k:</strong> Připojený prostřednictvím prohlížeče <strong>před přihlášením</strong>, se zobrazí výzva k přihlášení</strong>a nikdy dokončit připojení. |  Jedná se [známého problému](https://github.com/MicrosoftDocs/live-share/issues/167). Klikněte na znaménko v položky stavového řádku se přihlásit a pak znovu připojit. |

## <a name="connectivity"></a>Připojení

Následující informace můžou pomoct při řešení problémů, pokud máte problémy související s připojením nebo vypršení časového limitu při přihlášení, sdílení nebo připojení.

Jak je uvedeno v [požadavky na připojení pro Live Share](reference/connectivity.md) článku, jiné připojení režimy mají různé požadavky fungovat tak, že existuje několik různých potenciálních problémů děje.

| Nástroj | Problém | Pravděpodobná příčina |
|------|------|----------------|
| Všechny | Použití <strong>proxy</strong> a zobrazují se celou řadou potíží s připojením | Nastavení proxy serveru může být velmi obtížné.  Zkuste **HTTP_PROXY** a **HTTPS_PROXY** proměnné prostředí **globálně** a restartujte nástroj. Zobrazit [nastavení proxy serveru](reference/connectivity.md#proxies) další podrobnosti. Pravděpodobně existují některé konfigurace, které jsme zatím ještě nepodporují, takže [dejte nám vědět](https://github.com/MicrosoftDocs/live-share/issues/86) Pokud to nefunguje pro vás. |
| VS Code | Po instalaci rozšíření a spuštění VS Code poprvé získáte <strong>chybu, když se ve stavovém řádku zobrazí "Dokončení instalace"</strong>. |  Nelze přistupovat k Internetu nebo přístupu k download.visualstudio.microsoft.com a/nebo osobní nebo podniková brána firewall neblokuje download.microsoft.com na portu 443. Zobrazit [tady](https://github.com/MicrosoftDocs/live-share/issues/58) informace o tom, proč je potřeba Live Share něco v tuto chvíli stahovat. |
| Všechny | Jste <strong>nejde se přihlásit do aplikace Visual Studio Live Share</strong> | Nelze přistupovat k Internetu nebo přístupu k *. liveshare.vsengsaas.visualstudio.com na portu 80/443 zablokovaly osobní nebo podniková brána firewall. Zadejte https://insiders.liveshare.vsengsaas.visualstudio.com v prohlížeči a ověření budete přesměrováni na domovské stránce Visual Studio Live Share. |
| Všechny | V <strong>režim automatického</strong> (výchozí), budou moct přihlásit, ale naleznete v tématu <strong>limitu nebo chybě připojení</strong> při sdílení nebo připojení. | Buď přímé i režimy se nedaří připojit nebo je chyba s režimem automatického přenosu. Pokud je to možné se připojit po [přepínání na přímé nebo režim přenosu](reference/connectivity.md#changing-the-connection-mode), prosím [vyvolat chybu](https://aka.ms/vsls-problem). |
| Všechny | Jsou v <strong>přímý režim</strong>, budou moct přihlásit, ale najdete v článku <strong>limitu nebo chybě připojení</strong> při sdílení nebo připojení. | Host i hostitel nemůže připojit přímo. Zkuste [režim automatického nebo předávání](reference/connectivity.md#changing-the-connection-mode) zobrazíte, pokud se problém zmizí. Možná budete muset [ručně přes osobní bráně firewall povolit Live Share](reference/connectivity.md#manually-adding-a-firewall-entry) nebo jednoduše použít režim přenosu. |
| Všechny | Jste v <strong>přenosový režim</strong>, budou moct přihlásit, ale budou upozorněni <strong>limitu nebo chybě připojení</strong> při sdílení nebo připojení. | Přístup k *. servicebus.windows.net na portu 80/443 blokovaný osobní nebo podniková brána firewall neblokuje. Zkuste [přímý režim](reference/connectivity.md#changing-the-connection-mode). |

Zobrazit [požadavky na připojení pro Live Share](reference/connectivity.md) přečtěte si další informace o požadavcích na připojení.

## <a name="see-also"></a>Viz také:

Rychlý start

- [Sdílení prvního projektu](quickstart/share.md)
- [Připojení k první relaci](quickstart/join.md)

Postupy

- [Spolupráce ve Visual Studio Code](use/vscode.md)
- [Spolupráce ve Visual Studiu](use/vs.md)

Odkaz

- [Hlavní chyby, žádosti o funkce a omezení](https://aka.ms/vsls-issues)
- [Všechny žádosti o funkce a omezení](https://aka.ms/vsls-feature-requests)
- [Požadavky na připojení pro Live Share](reference/connectivity.md)
- [Podrobnosti o instalaci systému Linux](reference/linux.md)
- [Podpora jazyků a platforem](reference/platform-support.md)
- [Podpora rozšíření](reference/extensions.md)

Stále máte problémy? Je možné [poskytnout zpětnou vazbu](support.md).
