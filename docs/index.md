---
title: Přehled – Visual Studio Live Share | Microsoft Docs
description: Přehled rozšíření Visual Studio Live Share a jeho možností
ms.custom: ''
ms.date: 10/30/2019
ms.reviewer: ''
ms.suite: ''
ms.topic: overview
author: fubaduba
ms.author: fubaduba
manager: AmandaSilver
ms.workload:
- liveshare
ms.openlocfilehash: 10679c4ef44e2bdaeb4d8a8f25107b10b5f52243
ms.sourcegitcommit: c2ff6f29393990e91390875bb065bb811c071353
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2020
ms.locfileid: "76978898"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="what-is-visual-studio-live-share"></a>Co je Visual Studio Live Share?

Vítá vás Visual Studio Live Share! Rozšíření Live Share vám umožňuje upravovat a ladit v reálném čase společně s ostatními bez ohledu na to, jaké programovací jazyky používáte nebo jaké typy aplikací vytváříte. Budete moct okamžitě a bezpečně sdílet svůj aktuální projekt a pak podle potřeby zahájit ladicí relaci, sdílet terminálové instance, přesměrovat webové aplikace místního hostitele, uskutečňovat hlasové hovory a využívat i další funkce!

 Visual Studio Live Share (na rozdíl od párového programování) umožňuje vývojářům spolupracovat a přitom si zachovat osobní předvolby editoru (například motiv a klávesové zkratky) a také mít vlastní kurzor. Vývojáři díky tomu můžou hladce přepínat mezi vzájemným sledováním a samostatným zkoumáním nápadů nebo úloh. Tato schopnost pracovat společně a přitom nezávisle přináší možnosti spolupráce, ze které budete mít pocit jako z přímého _osobního_ kontaktu.

Jste připraveni začít? V tomto článku vám seznámíme s některými koncepcemi a ukážeme, jak instalovat potřebná rozšíření. Pokud hledáte zkrácenou verzi, podívejte se na naše články Rychlý start o [sdílení](quickstart/share.md) a [připojení](quickstart/join.md).

> [!TIP]
> Víte, že se můžete *připojit k vlastní relaci spolupráce*? Díky tomu si můžete Live Share vyzkoušet sami nebo můžete rozjet instanci Visual Studia nebo VS Code a vzdáleně se k ní připojit. U obou instancí můžete dokonce používat stejnou identitu. Vyzkoušejte to!

## <a name="install-visual-studio-live-share"></a>Instalace rozšíření Visual Studio Live Share

Než začnete, měli byste zajistit, abyste měli Visual Studio a Visual Studio Code nainstalované ve verzích, které splňují základní požadavky rozšíření Live Share.

- **Visual Studio Code 1.22.0 nebo vyšší** – Windows 7, 8.1 nebo 10, macOS *(pouze High Sierra 10.13 nebo vyšší)* , 64bitový Linux *(doporučuje se 64bitový Ubuntu Desktop 16.04 nebo vyšší, Fedora 27 nebo vyšší – [podívejte se na podrobnosti](use/vscode.md#installation))*
- **Visual Studio 2019** (libovolná edice) – Windows 7, 8.1 nebo 10
- **Visual Studio 2017 15.6 nebo vyšší** (libovolná edice) – Windows 7, 8.1 nebo 10

Stažení a instalace rozšíření Visual Studio Live Share pak bude hračka:

<table style="width: 100%; border:none;">
<tr>
    <td width="128px" style="width: 128px; text-align: center; border:none;"><img src="media/vs-code.svg" width="128px" alt="Visual Studio Code logo"/></td>
    <td style="border:none;">
        <strong>Visual Studio Code (1.22.0+)</strong><br />
        1. Nainstalujte <a href="https://code.visualstudio.com/">Visual Studio Code</a> pro Windows (7, 8.1 nebo 10), macOS <b>(High Sierra 10.13 nebo vyšší)</b>, 64bitový Linux <b>(<a href="use/vscode.md#installation">podrobnosti</a>)</b>.<br />
        2. Z marketplace si stáhněte a nainstalujte rozšíření Visual Studio Live Share. <br />
        3. Zvolte Znovu načíst a počkejte, až se stáhnou a nainstalují závislosti (sledujte stavový řádek).<br />
        4. <strong>Linux:</strong> Pokud se zobrazí výzva k <a href="reference/linux.md#install-linux-prerequisites">instalaci knihoven</a>, klikněte na Nainstalovat, zadejte heslo, a až budete hotovi, restartujte VS Code.<br />
        <a href="https://aka.ms/vsls-dl/vscode"><img src="media/download.png" alt="Download button"></a>
    </td>
</tr>
<tr style="border:none;">
    <td width="128px" style="width: 128px; text-align: center; border:none;"><img src="media/vs-ide-2019.svg" width="128px" alt="Visual Studio 2019 logo" /></td>
    <td  style="border:none;">
        <strong>Visual Studio 2019 </strong><br />
        1.Nainstalujte sadu <a href="https://visualstudio.microsoft.com/downloads/">Visual Studio 2019</a>.<br/>
        2. Nainstalujte <a href="reference/platform-support.md">podporované sady funkcí</a> (například ASP.NET, .NET Core, C++, Python a/nebo Node.js).<br />
        3. Visual Studio Live Share se standardně instaluje s těmito sadami funkcí. <br />
    </td>
</tr>
<tr style="border:none;">
    <td width="128px" style="width: 128px; text-align: center; border:none;"><img src="media/vs-ide-2017.svg" width="128px" alt="Visual Studio 2017 logo" /></td>
    <td  style="border:none;">
        <strong>Visual Studio 2017 15.6 nebo vyšší</strong><br />
        1. Nainstalujte nejnovější verzi sady <a href="https://visualstudio.microsoft.com/vs/older-downloads/">Visual Studio 2017</a> (15.6+) na Windows (7, 8.1 nebo 10).<br/>
        2. Nainstalujte <a href="reference/platform-support.md">podporované sady funkcí</a> (například ASP.NET, .NET Core, C++ a/nebo Node.js).<br />
        3. Z marketplace si stáhněte a nainstalujte rozšíření Visual Studio Live Share. <br />
        <a href="https://aka.ms/vsls-dl/vs"><img style="padding: 0; spacing: 0;" src="media/download.png" alt="Download button" ></a><br />
    </td>
</tr>
</table>

Stažením a používáním rozšíření Visual Studio Live Share vyjadřujete souhlas s [licenčními podmínkami](https://aka.ms/vsls-license) a [prohlášením o zásadách ochrany osobních údajů](https://www.microsoft.com/en-us/privacystatement/EnterpriseDev/default.aspx). Pokud narazíte na problémy, podívejte se na článek o [odstraňování potíží](troubleshooting.md).

A je to! Teď byste měli ve VS Code vlevo dole vidět přihlašovací stavový řádek a ve Visual Studio vpravo nahoře tlačítko Sdílet. Informace o tom, co dělat dál, najdete ve zbývajících částech dokumentace.


## <a name="see-also"></a>Viz také:

Rychlý start

- [Sdílení prvního projektu](quickstart/share.md)
- [Připojení k první relaci](quickstart/join.md)

Postupy

- [Spolupráce ve Visual Studio Code](use/vscode.md)
- [Spolupráce ve Visual Studiu](use/vs.md)

reference

- [Požadavky na připojení pro Live Share](reference/connectivity.md)
- [Funkce zabezpečení Live Share](reference/security.md)
- [Podpora jazyků a platforem](reference/platform-support.md)
- [Podpora rozšíření](reference/extensions.md)
- [Zpráva k vydání verze](https://aka.ms/vsls-releases)

Máte potíže? Podívejte se na článek o [odstraňování potíží](troubleshooting.md) nebo nám [pošlete svůj názor](support.md).
