---
title: Rychlý start – Visual Studio Live Share sdílet | Dokumentace Microsoftu
description: Stručné návod na sdílení svůj první projekt pomocí Visual Studio Live Share spolupráci relace.
ms.custom: ''
ms.date: 03/22/2018
ms.reviewer: ''
ms.suite: ''
ms.topic: quickstart
author: chuxel
ms.author: clantz
manager: AmandaSilver
ms.workload:
- liveshare
ms.openlocfilehash: b25158970f325bbc55618909315a8ed09d6f50a8
ms.sourcegitcommit: 1706889dd48377932868a03e88fbd2b4512a3729
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/18/2019
ms.locfileid: "58853609"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="quickstart-share-your-first-project"></a>Rychlý start: Sdílení prvního projektu

Vítá vás Visual Studio Live Share! Rozšíření Live Share vám umožňuje upravovat a ladit v reálném čase společně s ostatními bez ohledu na to, jaké programovací jazyky používáte nebo jaké typy aplikací vytváříte. Umožňuje vám okamžitě a bezpečně sdílet váš aktuální projekt a pak podle potřeby sdílet ladicí relace, terminálové instance, webové aplikace místního hostitele, hlasové hovory a další věci.

Jste připraveni začít?  Týmová spolupráce by měl být tak rychlý a přirozené, že čím dál těžší není k tomu! Z tohoto důvodu Visual Studio Live Share usnadňuje Začínáme, tak, že můžete bez problémů začít sdílení práce a nápady.

> [!TIP]
> Víte, že se můžete *připojit k vlastní relaci spolupráce*? Díky tomu si můžete Live Share vyzkoušet sami nebo můžete rozjet instanci Visual Studia nebo VS Code a vzdáleně se k ní připojit. V obou případech můžete použít i stejnou identitu. Vyzkoušejte to!

Postupujte podle těchto kroků můžete začít sdílet.

## <a name="1-install-the-extension"></a>1. Instalace rozšíření

Instalaci rozšíření je snadné. Postupujte podle těchto kroků:

<table style="width: 100%; border:none;">
<tr>
    <td width="128px" style="width: 128px; text-align: center; border:none;"><img src="../media/vs-code.svg" width="128px" alt="Visual Studio Code logo"/></td>
    <td style="border:none;">
        <strong>Visual Studio Code (1.22.0+)</strong><br />
        1. Nainstalujte <a href="https://code.visualstudio.com/">Visual Studio Code</a> pro Windows (7, 8.1 nebo 10), macOS <b>(Sierra+)</b>, 64bitový Linux <b>(<a href="../use/vscode.md#installation">podrobnosti</a>)</b>.<br />
        2. Z marketplace si stáhněte a nainstalujte rozšíření Visual Studio Live Share. <br />
        3. Zvolte Znovu načíst a počkejte, až se stáhnou a nainstalují závislosti (sledujte stavový řádek).<br />
        4. <strong>Linux:</strong> Pokud se zobrazí výzva k <a href="../reference/linux.md#install-linux-prerequisites">instalaci knihoven</a>, klikněte na Nainstalovat, zadejte heslo, a až budete hotovi, restartujte VS Code.<br />
        <a href="https://aka.ms/vsls-dl/vscode"><img src="../media/download.png" alt="Download button"></a>
    </td>
</tr>
<tr style="border:none;">
    <td width="128px" style="width: 128px; text-align: center; border:none;"><img src="../media/vs-ide-2019.svg" width="128px" alt="Visual Studio 2019 logo" /></td>
    <td  style="border:none;">
        <strong>Visual Studio 2019 </strong><br />
        1. Nainstalujte <a href="https://visualstudio.microsoft.com/downloads/">Visual Studio 2019</a>.<br/>
        2. Nainstalujte <a href="../reference/platform-support.md">podporované sady funkcí</a> (například ASP.NET, .NET Core, C++ a/nebo Node.js).<br />
        3. Visual Studio Live Share se standardně instaluje s těmito sadami funkcí. <br />
    </td>
</tr>
<tr style="border:none;">
    <td width="128px" style="width: 128px; text-align: center; border:none;"><img src="../media/vs-ide-2017.svg" width="128px" alt="Visual Studio 2017 logo" /></td>
    <td  style="border:none;">
        <strong>Visual Studio 2017 15.6 nebo vyšší</strong><br />
        1. Nainstalujte nejnovější verzi sady <a href="https://visualstudio.microsoft.com/vs/older-downloads/">Visual Studio 2017</a> (15.6+) na Windows (7, 8.1 nebo 10).<br/>
        2. Nainstalujte <a href="../reference/platform-support.md">podporované sady funkcí</a> (například ASP.NET, .NET Core, C++ a/nebo Node.js).<br />
        3. Z marketplace si stáhněte a nainstalujte rozšíření Visual Studio Live Share. <br />
        <a href="https://aka.ms/vsls-dl/vs"><img style="padding: 0; spacing: 0;" src="../media/download.png" alt="Download button" ></a><br />
    </td>
</tr>
</table>

Stažením a používáním rozšíření Visual Studio Live Share vyjadřujete souhlas s [licenčními podmínkami](https://aka.ms/vsls-license) a [prohlášením o zásadách ochrany osobních údajů](https://www.microsoft.com/en-us/privacystatement/EnterpriseDev/default.aspx). Pokud narazíte na problémy, podívejte se na článek o [odstraňování potíží](../troubleshooting.md).

## <a name="2-sign-in"></a>2. Přihlášení

Po instalaci rozšíření Live Share, restartování a čeká se závislosti pro dokončení instalace (VS Code), budete chtít přihlásit, aby ostatní účastníci vědět, kdo jste. Jednoduše klikněte na položku stavového řádku (VS Code) "Live Share" / "Sign in" tlačítko (nebo), abyste mohli začít.

<table style="border: none;">
<tr style="border: none;">
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vscode-sign-in-button.png" width="100%" alt="Visual Studio Code sign in status bar item"/>
    </td>
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vs-sign-in-button.png" width="100%" alt="Visual Studio sign in button"/>
    </td>
</tr>
</table>

V **VS Code**, zatímco oznámení se zobrazí spuštění s výzvou, abyste se přihlásili, spustí se váš prohlížeč. Dokončete proces v prohlížeči přihlašování a pak jednoduše zavřít prohlížeč, až budete hotovi.

![Informační zpráva s výzvou k přihlášení pomocí webového prohlížeče](../media/vscode-sign-in-toast.png)

> **Uživatelé Linuxu:** Můžete být vyzváni k zadání uživatelského kódu, pokud používáte starší verzi Live Share (v0.3.295 nebo níže). Aktualizovat na nejnovější verzi rozšíření, nebo klikněte "s vlastním?" Chcete-li zobrazit kód odkaz po přihlášení. Zobrazit [zde podrobnosti](../use/vscode.md#sign-in-using-a-user-code).

V **sady Visual Studio**, Live Share automaticky použije vaše [aktivního účtu přizpůsobení](https://docs.microsoft.com/en-us/visualstudio/ide/signing-in-to-visual-studio). V důsledku toho můžete jednoduše přihlásit běžným způsobem. Nicméně, pokud chcete použít jiný znak než váš účet přizpůsobení sady Visual Studio, přejděte na **nástroje &gt; možnosti &gt; Live Share &gt; uživatelský účet** a vyberte jiné přihlašovací údaje.

Zobrazit [řešení potíží s](../troubleshooting.md#sign-in) Pokud jsou pořád máte problémy.

## <a name="3-open-a-folder-project-or-solution"></a>3. Otevřete složku, projekt nebo řešení

Otevřít složku, projekt nebo řešení, které chcete sdílet v sadě Visual Studio nebo Visual Studio Code pomocí normálním pracovním postupu.

### <a name="4-optional-update-hidden-or-excluded-files"></a>4. [Update nepovinné] skrytý nebo vyloučit soubory

Ve výchozím nastavení, Live Share **skryje** všech souborů a složek odkazovat v souborech .gitignore ve sdílených složkách hostů. **Skrytí** soubor zabraňuje zobrazování v stromovou strukturu souborů hosta. **S výjimkou** souboru se vztahuje přísnější pravidla, které brání otevření pro hostovaný v situacích, jako jsou přejít k definici nebo pokud přejdete do souboru při ladění nebo "splňovalo" Live Share. Pokud chcete skrýt nebo vyloučit jiné soubory, **. vsls.json** soubor lze přidat do projektu s tímto nastavením. Zobrazit [řízení přístupu k souborům a viditelnost](../reference/security.md#controlling-file-access-and-visibility) podrobnosti.

## <a name="5-start-a-collaboration-session"></a>5. Spustit relaci spolupráce

Dále, jednoduše klikněte na tlačítko "Live Share" v rámci vašeho nástroje a odkaz na pozvánku je automaticky zkopíruje do schránky.

<table style="border: none;">
<tr style="border: none;">
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vscode-share-button.png" width="100%" alt="Visual Studio Code share status bar item" />
    </td>
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vs-share-button.png" width="100%" alt="Visual Studio share button"/>
    </td>
</tr>
</table>

> [!NOTE]
> Můžete být vyzváni softwarem klasické pracovní plochy brány firewall umožňující Live Share agenta pro otevření portu okamžiku, kdy budete sdílet. Přijímá to je naprosto volitelné, ale umožňuje zabezpečené "přímý režim" ke zlepšení výkonu při osoby, že pracujete s je ve stejné síti jako vy. Zobrazit [změnit režim připojení](../reference/connectivity.md#changing-the-connection-mode) podrobnosti.

## <a name="6-optional-enable-read-only-mode"></a>6. [režim jen pro čtení povolit nepovinné]

Po spuštění relace spolupráce, můžete nastavit relace, která má být jen pro čtení pro hosty zabránit v provádění úprav kódu sdílením.

Po sdílení, zobrazí se oznámení, pozvánky odkaz byl zkopírován do schránky. Pak můžete vybrat možnost nastavit relaci jen pro čtení.

<table style="border: none;">
<tr style="border: none;">
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vscode-read-only-toast.png" width="100%" alt="Visual Studio Code read-only option" />
    </td>
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vs-read-only-notification.png" width="100%" alt="Visual Studio read-only option"/>
    </td>
</tr>
</table>

V **VS Code**, relaci jen pro čtení můžete spustit také na Live Share viewlet kartě.

![Informační zpráva s výzvou k přihlášení pomocí webového prohlížeče](../media/vscode-read-only-viewlet.png)

### <a name="7-send-someone-the-invite-link"></a>7. Odeslání pozvánky odkaz

Odkaz na odeslání e-mailu, Slack, Skype, atd. a těch, které chcete pozvat. Odkaz otevřít v prohlížeči umožňující připojte se k relaci spolupráce, který sdílí obsah složky, projekt nebo řešení, které jste otevřeli. Všimněte si, že udělená úroveň přístupu, Live Share relací může poskytovat hosté, **pouze by měly sdílet s lidmi, kterým důvěřujete** a přemýšlení prostřednictvím důsledky sdílení.

> **Tip zabezpečení:** Chcete pochopili důsledky zabezpečení některé funkce Live Share? Podívejte se [zabezpečení](../reference/security.md) článku.

Pokud vás pozvat hosta má otázky, [rychlý start: Připojte se k relaci první](join.md) článek poskytuje některé další informace o zprovoznění jako Host.

## <a name="8-optional-approve-the-guest"></a>8. [Nepovinné] schválit hosta

Ve výchozím nastavení guests automaticky připojí k relaci spolupráci a budete upozorněni, když jsou připraveni spolupracovat s vámi.

<table style="border: none;">
<tr style="border: none;">
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vscode-join-notification.png" width="100%" alt="Visual Studio Code join notification" />
    </td>
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vs-join-notification.png" width="100%" alt="Visual Studio join notification"/>
    </td>
</tr>
</table>

Můžete se rozhodnout vyžadují explicitní "schválení" pro každého, kdo připojení místo. Pokud je toto nastavení zapnuté, oznámení vás vyzve k schválit Host při pokusu o připojení relace.

Zobrazit [vyžadující schválení hosta](../reference/security.md#requiring-guest-approval) podrobnosti o tom, jak tuto funkci zapnout.

## <a name="9-collaborate"></a>9. Spolupracujte!

A to je vše! Tady je pár věcí k vyzkoušení po Host připojil:

1. Nezávisle pohybovat na různé soubory v projektu a ujistěte se, některé úpravy
1. Postupujte podle hosta a sledovat tak, jak posunout, proveďte úpravy a přejděte na různé soubory
1. Spuštění relace ladění společně s nimi
1. Sdílet server, takže si můžete prohlédnout něco jako webová aplikace spuštěná na počítači
1. Sdílet terminálu a spusťte některé příkazy

Podívejte se [Visual Studio Code](../use/vscode.md) a [sady Visual Studio](../use/vs.md) dokumentace rozšíření informace o tom, jak provést tyto akce a další.

Máte potíže? Podívejte se na článek o [odstraňování potíží](../troubleshooting.md) nebo nám [pošlete svůj názor](../support.md).

## <a name="next-steps"></a>Další kroky

Prohlédněte si tyto další články pro další informace.

- [Rychlý start: Připojte se k relaci první spolupráce](join.md)
- [Postupy: Spolupráce pomocí Visual Studio Code](../use/vscode.md)
- [Postupy: Spolupráce pomocí sady Visual Studio](../use/vs.md)

Odkaz

- [Požadavky na připojení pro Live Share](../reference/connectivity.md)
- [Funkce zabezpečení Live Share](../reference/security.md)
- [Podpora jazyků a platforem](../reference/platform-support.md)
- [Podpora rozšíření](../reference/extensions.md)
