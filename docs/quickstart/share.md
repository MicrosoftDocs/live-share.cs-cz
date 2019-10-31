---
title: Rychlý Start pro sdílení – Visual Studio Live Share | Microsoft Docs
description: Zkrácený návod ke sdílení prvního projektu pomocí Visual Studio Live Share relace spolupráce.
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
ms.openlocfilehash: 32fc12da3b26ccb1f6d5b984915dfd0cc6afd647
ms.sourcegitcommit: c6ef4e5a9aec4f682718819c58efeab599e2781b
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/30/2019
ms.locfileid: "73170008"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="quickstart-share-your-first-project"></a>Rychlý Start: sdílení prvního projektu

Vítá vás Visual Studio Live Share! Rozšíření Live Share vám umožňuje upravovat a ladit v reálném čase společně s ostatními bez ohledu na to, jaké programovací jazyky používáte nebo jaké typy aplikací vytváříte. Umožňuje vám okamžitě a bezpečně sdílet váš aktuální projekt a pak podle potřeby sdílet ladicí relace, terminálové instance, webové aplikace místního hostitele, hlasové hovory a další věci.

Jste připraveni začít?  Týmová spolupráce by měla být tak rychlá a přirozená, takže ji nebudete moct dělat těžší. Z tohoto důvodu je Visual Studio Live Share snadné začít, takže můžete hladce začít sdílet práci a nápady.

> [!TIP]
> Víte, že se můžete *připojit k vlastní relaci spolupráce*? Díky tomu si můžete Live Share vyzkoušet sami nebo můžete rozjet instanci Visual Studia nebo VS Code a vzdáleně se k ní připojit. Stejnou identitu můžete dokonce použít i v obou instancích. Vyzkoušejte to!

Stačí pomocí těchto kroků začít sdílet.
<!--
Change the instructions to Install extension for VS Code and in-tool for VS?
-->
## <a name="1-install-the-extension"></a>1. Instalace rozšíření

Instalace rozšíření je snadná. Stačí postupovat podle těchto kroků:

<table style="width: 100%; border:none;">
<tr>
    <td width="128px" style="width: 128px; text-align: center; border:none;"><img src="../media/vs-code.svg" width="128px" alt="Visual Studio Code logo"/></td>
    <td style="border:none;">
        <strong>Visual Studio Code (1.22.0+)</strong><br />
        1. Nainstalujte <a href="https://code.visualstudio.com/">Visual Studio Code</a> pro Windows (7, 8.1 nebo 10), macOS <b>(Sierra+)</b>, 64bitový Linux <b>(<a href="../how-to-guides/vscode.md#installation">podrobnosti</a>)</b>.<br />
        2. Z marketplace si stáhněte a nainstalujte rozšíření Visual Studio Live Share. <br />
        3. Zvolte Znovu načíst a počkejte, až se stáhnou a nainstalují závislosti (sledujte stavový řádek).<br />
        4. <strong>Linux</strong>: Pokud se zobrazí výzva k <a href="../reference/linux.md#install-linux-prerequisites">instalaci knihoven</a>, klikněte na nainstalovat, zadejte heslo a po dokončení vs Code restartujte.<br />
        <a href="https://aka.ms/vsls-dl/vscode"><img src="../media/download.png" alt="Download button"></a>
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

## <a name="2-sign-in"></a>2. Přihlaste se

<!--
Re-write the grammar here- run on sentence does not make sense. Change screen shots. There is another way of signing in as well- what if a user goes directly to the start collaboration. 
-->
Po instalaci rozšíření Live Share, restartování a čekání na dokončení instalace (VS Code) se budete chtít přihlásit, aby mohli ostatní účastníci informovat o tom, kdo máte. Chcete-li začít, stačí kliknout na položku stavového řádku "Live Share" (VS Code)/"přihlašovat" (a).

<table style="border: none;">
<tr style="border: none;">
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vscode-sign-in-button-new.png" width="100%" alt="Visual Studio Code sign in status bar item"/>
    </td>
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vs-sign-in-button.png" width="100%" alt="Visual Studio sign in button"/>
    </td>
</tr>
</table>

V **vs Code**se prohlížeč spustí, když se zobrazí oznámení o spuštění, které vás vyzve k přihlášení. Dokončete proces přihlášení v prohlížeči a po dokončení jednoduše zavřete prohlížeč.

![Informační zpráva s výzvou k přihlášení pomocí webového prohlížeče](../media/vscode-sign-in-toast.png)

> **Uživatelé systému Linux:** Pokud používáte starší verzi Live Share (v 0.3.295 nebo níže), může se zobrazit výzva k zadání kódu uživatele. Aktualizujte na nejnovější verzi rozšíření nebo klikněte na "máte potíže?" odkaz po přihlášení, aby se zobrazil kód [Podrobnosti najdete tady](../how-to-guides/vscode.md#sign-in-using-a-user-code).

V **aplikaci Visual Studio**Live Share automaticky používá váš [účet přizpůsobení](https://docs.microsoft.com/en-us/visualstudio/ide/signing-in-to-visual-studio). V důsledku toho se můžete jednoduše přihlásit stejným způsobem jako normálně. Pokud ale dáváte přednost jinému přihlášení než k vašemu účtu přizpůsobení sady Visual Studio, v nabídce **nástroje &gt; možnosti &gt; Live Share &gt; uživatelský účet** a vyberte jiné přihlašovací údaje.

Pokud stále dochází k potížím, přečtěte si téma [řešení potíží](../troubleshooting.md#sign-in) .

## <a name="3-open-a-folder-project-or-solution"></a>3. Otevřete složku, projekt nebo řešení.

Použijte běžný pracovní postup k otevření složky, projektu nebo řešení, které chcete sdílet v aplikaci Visual Studio nebo Visual Studio Code.

### <a name="4-optional-update-hidden-or-excluded-files"></a>4. [nepovinné] aktualizace skrytých nebo vyloučených souborů

Ve výchozím nastavení Live Share **skrývá** všechny soubory nebo složky, na které se odkazuje ve sdílených složkách z hostů. **Skrytím** souboru znemožníte jeho zobrazení ve stromu souborů hosta. **Vyloučení** souboru platí přísnější pravidlo, které brání Live Share jeho otevření pro hosta v situacích, jako je například definice přejít k definici, nebo pokud se do souboru při ladění nebo při ladění používá "za". Pokud chcete skrýt nebo vyloučit různé soubory, můžete do projektu pomocí těchto nastavení přidat soubor **. vsls. JSON** . Podrobnosti najdete v tématu [řízení přístupu k souborům a viditelnost](../reference/security.md#controlling-file-access-and-visibility) .

## <a name="5-start-a-collaboration-session"></a>5. zahájení relace spolupráce

<!--
-->
Potom jednoduše klikněte v nástroji na "Live Share" a odkaz na pozvánku se automaticky zkopíruje do schránky.

<table style="border: none;">
<tr style="border: none;">
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vscode-share-button-new.png" width="100%" alt="Visual Studio Code share status bar item" />
    </td>
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vs-share-button.png" width="100%" alt="Visual Studio share button"/>
    </td>
</tr>
</table>

> [!NOTE]
> Možná budete požádáni o váš software brány firewall na ploše, aby mohl agent Live Share otevřít port při prvním sdílení. Přijetí je zcela volitelné, ale umožňuje zabezpečený "přímý režim", aby se zlepšil výkon, když osoba, se kterou pracujete, je ve stejné síti jako vy. Podrobnosti najdete v tématu [Změna režimu připojení](../reference/connectivity.md#changing-the-connection-mode) .

## <a name="6-optional-enable-read-only-mode"></a>6. [volitelné] povolit režim jen pro čtení

Po zahájení relace spolupráce můžete nastavit relaci jen pro čtení a zabránit tak hostům v provádění úprav v kódu, který se sdílí.

Po sdílení se dostanete oznámení, že se odkaz na pozvánku zkopíroval do schránky. Pak můžete vybrat možnost nastavit relaci jen pro čtení.

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

V **vs Code**můžete také na kartě Live Share Viewlet spustit relaci jen pro čtení.

![Informační zpráva s výzvou k přihlášení pomocí webového prohlížeče](../media/vscode-read-only-viewlet.png)

### <a name="7-send-someone-the-invite-link"></a>7. poslat někomu pozvánku odkaz

Pošlete odkaz prostřednictvím e-mailu, časové rezervy, Skypu atd. na ty, které chcete pozvat. Otevřením odkazu v prohlížeči umožníte, aby se připojili k relaci spolupráce, která sdílí obsah složky, projektu nebo řešení, které jste otevřeli. Všimněte si, že vzhledem k tomu, že úroveň přístupu Live Share relace může poskytnout hostům, **byste měli sdílet jenom s lidmi, kterým důvěřujete** , a zamyslete se nad důsledky sdílení.

> **Tip zabezpečení:** Chcete pochopit důsledky zabezpečení některých funkcí Live Share? Podívejte se na článek o [zabezpečení](../reference/security.md) .

Pokud má host, kterého jste pozvali, dotazy, [rychlý Start: připojení k první relaci](join.md) obsahuje další informace o tom, jak začít pracovat jako host.

## <a name="8-optional-approve-the-guest"></a>8. [volitelné] schvalte hosta.

Ve výchozím nastavení se hosté připojovat k vaší relaci spolupráce automaticky a vy budete upozorněni, až budou připraveni pracovat s vámi.

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

Místo toho se můžete rozhodnout, že budete vyžadovat explicitní schválení pro kohokoli. Pokud je toto nastavení zapnuté, zobrazí se při pokusu o připojení k vaší relaci výzva k potvrzení uživatele.

Podrobnosti o tom, jak tuto funkci zapnout, najdete v tématu [vyžadování schválení hostů](../reference/security.md#requiring-guest-approval) .

## <a name="9-collaborate"></a>9. spolupráce

A je to! Tady je několik věcí, které si můžete vyzkoušet, jakmile se k hostovi připojíte:

1. Přechod k různým souborům v projektu nezávisle na sobě a provádění některých úprav
1. Sledujte hosta a sledujte, jak se posouvají, proveďte úpravy a přejděte do různých souborů.
1. Spustit relaci spoluladění s nimi
1. Nasdílejte Server, abyste se mohli podívat na něco jako na webové aplikaci běžící na svém počítači.
1. Sdílení terminálu a spuštění některých příkazů

Další informace o tom, jak provádět tyto akce a další, najdete v dokumentaci k rozšířením pro [Visual Studio Code](../how-to-guides/vscode.md) a [Visual Studio](../how-to-guides/vs.md) .

Máte potíže? Podívejte se na článek o [odstraňování potíží](../troubleshooting.md) nebo nám [pošlete svůj názor](../support.md).

## <a name="next-steps"></a>Další kroky

Další informace najdete v těchto dalších článcích.

- [Rychlý Start: připojení první relace spolupráce](join.md)
- [Postupy: spolupráce pomocí Visual Studio Code](../how-to-guides/vscode.md)
- [Postupy: spolupráce pomocí sady Visual Studio](../how-to-guides/vs.md)

Odkaz

- [Požadavky na připojení pro Live Share](../reference/connectivity.md)
- [Funkce zabezpečení Live Share](../reference/security.md)
- [Podpora jazyků a platforem](../reference/platform-support.md)
- [Podpora rozšíření](../reference/extensions.md)
