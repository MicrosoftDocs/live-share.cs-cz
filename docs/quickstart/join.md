---
title: Připojte se k rychlý start – Visual Studio Live Share | Dokumentace Microsoftu
description: Stručné návod na připojení k vaší první spolupráci relace Visual Studio Live Share.
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
ms.openlocfilehash: ec3c983e91f849c6e966d2e5d0ae688e98b2b3f1
ms.sourcegitcommit: c702aafb65b0fc43cb210e1bb7340cef48b57f35
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/21/2019
ms.locfileid: "67322820"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="quickstart-join-your-first-collaboration-session"></a>Rychlý start: Připojte se k relaci první spolupráce

Vítá vás Visual Studio Live Share! Rozšíření Live Share vám umožňuje upravovat a ladit v reálném čase společně s ostatními bez ohledu na to, jaké programovací jazyky používáte nebo jaké typy aplikací vytváříte. Umožňuje okamžitě a bezpečně připojit k programujete pro aktuální projekt a pak podle potřeby, zadejte do ladicími relacemi, zobrazit a upravit terminálu instance, přečtěte si místního hostitele webové aplikace, připojení k hlasových hovorů a další!

Jste připraveni začít? Týmová spolupráce by měl být tak rychlý a přirozené, že čím dál těžší není k tomu! Z tohoto důvodu Visual Studio Live Share usnadňuje Začínáme, tak, že můžete bez problémů začít sdílení práce a nápady.

> [!TIP]
> Víte, že se můžete *připojit k vlastní relaci spolupráce*? Díky tomu si můžete Live Share vyzkoušet sami nebo můžete rozjet instanci Visual Studia nebo VS Code a vzdáleně se k ní připojit. U obou instancí můžete dokonce používat stejnou identitu. Vyzkoušejte to!

Postupujte podle těchto kroků připojit k relaci spolupráci.

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
        <a href="https://aka.ms/vsls-dl/vscode" alt="Download button"><img src="../media/download.png"></a>
    </td>
</tr>
<tr style="border:none;">
    <td width="128px" style="width: 128px; text-align: center; border:none;"><img src="../media/vs-ide-2019.svg" width="128px" alt="Visual Studio 2019 logo" /></td>
    <td  style="border:none;">
        <strong>Visual Studio 2019 </strong><br />
        1.Nainstalujte sadu <a href="https://visualstudio.microsoft.com/downloads/">Visual Studio 2019</a>.<br/>
        2. Nainstalujte <a href="../reference/platform-support.md">podporované sady funkcí</a> (například ASP.NET, .NET Core, C++, Python a/nebo Node.js).<br />
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

## <a name="2-optional-join-as-a-read-only-guest-in-vs-code"></a>2. [připojení k nepovinné] v roli hosta jen pro čtení v nástroji VS Code

Ve VS Code, po instalaci rozšíření Live Share, restartování a čeká se závislosti pro dokončení instalace můžete přejít v a připojte se k relaci spolupráci jako Host jen pro čtení.

> [!NOTE]
> Pokud chcete provádět úpravy kódu, které se připojujete, musíte se přihlásit.

Otevřete (nebo znovu otevřete) odkaz pozvání v prohlížeči a zobrazí upozornění, že v prohlížeči chce spusťte VS Code. Ten spustit a začneme připojení k relaci spolupráce.

Při spuštění VS Code, zobrazí se informační zpráva s výzvou k přihlášení. Vyberte možnost "Pokračovat jako jen pro čtení hosta" připojení relace.

![Připojit, protože relace jako jen pro čtení hosta oznámení](../media/vscode-read-only-guest.png)

Budete vyzváni k zadání zobrazovaný název, který pomůže účastníky můžete identifikovat v relaci.

![Název hostovaného jen pro čtení](../media/vscode-read-only-guest-name.png)

Potom budete propojována do relace jako jen pro čtení. Budete moct zobrazit a navigaci v kódu, společném ladění a zobrazení sdílené servery a terminály (jen pro čtení).

> [!NOTE]
> Pokud chcete později získat přístup pro čtení a zápis ke kódu, můžete přihlásit. Klikněte na své zobrazované jméno na stav, panelu a vyberte možnost "Sign in".
![Přihlásit jako jen pro čtení Host](../media/vscode-read-only-guest-signin.png) tím se spustí prohlížeč, a můžete použít účet Microsoft nebo GitHub se přihlásit pomocí.

## <a name="3-sign-in"></a>3. Přihlášení

Po instalaci rozšíření Live Share, restartování a čeká se závislosti pro dokončení instalace (VS Code), budete chtít přihlásit, aby ostatní účastníci vědět, kdo jste. Pokud tento krok přeskočíte, se zobrazí výzva k přihlášení během připojení k procesu nebo může připojit k relaci jako Host jen pro čtení. Klikněte na položku stavového řádku (VS Code) "Live Share" / "sign in" tlačítko (nebo), abyste mohli začít.

<table style="border: none;">
<tr style="border: none;">
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vscode-sign-in-button-new.png" width="100%" alt="Visual Studio Code sign in status bar item" />
    </td>
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vs-sign-in-button.png" width="100%" alt="Visual Studio sign in button"/>
    </td>
</tr>
</table>

V **VS Code**, zatímco oznámení se zobrazí spuštění s výzvou, abyste se přihlásili, spustí se váš prohlížeč. Dokončete proces v prohlížeči přihlašování a pak jednoduše zavřít prohlížeč, až budete hotovi.

![Informační zpráva s výzvou k přihlášení pomocí webového prohlížeče](../media/vscode-sign-in-toast.png)

> **Uživatelé Linuxu:** Můžete být vyzváni k zadání uživatelského kódu, pokud používáte starší verzi Live Share (v0.3.295 nebo níže). Aktualizovat na nejnovější verzi rozšíření, nebo klikněte "s vlastním?" Chcete-li zobrazit kód odkaz po přihlášení. Zobrazit [zde podrobnosti](../use/vscode.md#sign-in-using-a-user-code).

V **sady Visual Studio**, Live Share automaticky použije vaše [aktivního účtu přizpůsobení](https://docs.microsoft.com/en-us/visualstudio/ide/signing-in-to-visual-studio). V důsledku toho můžete jednoduše přihlásit běžným způsobem. Nicméně pokud chcete raději použít jiný znak než váš účet přizpůsobení sady Visual Studio, přejděte na **nástroje &gt; možnosti &gt; Live Share &gt; uživatelský účet** a vyberte jiné přihlašovací údaje.

Zobrazit [řešení potíží s](../troubleshooting.md#sign-in) Pokud jsou pořád máte problémy.

## <a name="4-openre-open-the-invite-link-in-a-browser"></a>4. Otevřít nebo jejich opakované-open pozvánku na odkaz v prohlížeči

Teď stačí otevřít místní (nebo znovu otevřete) odkaz pozvání v prohlížeči.

> **Poznámka:** Pokud jste ještě nenainstalovali rozšíření Live Share, zobrazí se vám s odkazy na marketplace pro rozšíření. Instalace rozšíření a restartujte nástroj a zkuste to znovu.

Zobrazí se oznámení, spustí se nástroj Live Share povolené vyžaduje prohlížeče. Pokud jste povolili jeho spuštění vybrané nástroje, už budete připojíte k relaci spolupráce po jeho spuštění.

![Připojte se k stránky](../media/join-page.png)

Pokud je hostitel v režimu offline, zobrazí se upozornění v tuto chvíli místo. Potom můžete kontaktovat hostitele a požádejte ho, aby znovu sdílet.

> **Tip Poradce při potížích:** Při použití VS Code, ujistěte se, když jste **alespoň jednou spuštěn nástroj** po instalaci rozšíření a čekalo se na závislosti k dokončení instalace (viz stavový řádek) před levou nebo jejich opakované-opening pozvánku stránce. Stále se nedaří? Zobrazit [ručně připojit](../reference/manual-join.md) podrobnosti.

## <a name="5-collaborate"></a>5. Spolupracujte!

A to je vše! Ve chvíli budete mít připojené k spolupracovníka relace spolupráci. Ve výchozím nastavení, hostitele auto přijímá osoby, které se připojit, ale pokud je nastavena na hostiteli [vyžadovat schválení hosta](../reference/security.md#requiring-guest-approval) bude zobrazen stavový řádek / join zmínka dialogového okna, Live Share čekajícím na hostiteli, aby vaši žádost o připojení.

> **Tip zabezpečení:** V roli hosta připojení k relaci spolupráce je důležité pochopit, že hostitelé může omezit přístup k určité soubory nebo funkce. Chcete si uvědomit důsledky zabezpečení některých funkcích a nastaveních Live Share? Podívejte se [zabezpečení](../reference/security.md) článku.

Tady je pár věcí k vyzkoušení:

1. Nezávisle pohybovat projektu a ujistěte se, některé úpravy
2. Projděte si pracovní intellisense pro JavaScript, TypeScript, a/nebo C# kódu
3. Upravit něco spolu s hostiteli
4. Postupujte podle hostitele a s nimi pohybovat přejděte a proveďte úpravy v různých souborů
5. Spuštění relace ladění společně s hostitelem
6. Požádejte hostitele do sdílené složky serveru, tak si můžete prohlédnout něco jako webová aplikace spuštěná na počítači
7. Požádejte hostitele do sdílené složky terminálu a spusťte některé příkazy

Máte potíže? Podívejte se na článek o [odstraňování potíží](../troubleshooting.md) nebo nám [pošlete svůj názor](../support.md).

## <a name="next-steps"></a>Další kroky

Prohlédněte si tyto další články pro další informace.

- [Rychlý start: Sdílejte svůj první projekt](share.md)
- [Postupy: Spolupráce pomocí Visual Studio Code](../use/vscode.md)
- [Postupy: Spolupráce pomocí sady Visual Studio](../use/vs.md)

Odkaz

- [Požadavky na připojení pro Live Share](../reference/connectivity.md)
- [Funkce zabezpečení Live Share](../reference/security.md)
- [Podpora jazyků a platforem](../reference/platform-support.md)
- [Podpora rozšíření](../reference/extensions.md)
