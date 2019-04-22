---
title: Přehled – Visual Studio Live Share | Microsoft Docs
description: Přehled rozšíření Visual Studio Live Share a jeho možností
ms.custom: ''
ms.date: 04/26/2018
ms.reviewer: ''
ms.suite: ''
ms.topic: overview
author: chuxel
ms.author: clantz
manager: AmandaSilver
ms.workload:
- liveshare
ms.openlocfilehash: 5f67086e9040a477e082cbd3ef27a1789c6406c5
ms.sourcegitcommit: 1706889dd48377932868a03e88fbd2b4512a3729
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/18/2019
ms.locfileid: "58853583"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="what-is-visual-studio-live-share"></a>Co je Visual Studio Live Share?

Vítá vás Visual Studio Live Share! Rozšíření Live Share vám umožňuje upravovat a ladit v reálném čase společně s ostatními bez ohledu na to, jaké programovací jazyky používáte nebo jaké typy aplikací vytváříte. Umožňuje vám okamžitě a bezpečně sdílet váš aktuální projekt a pak podle potřeby sdílet ladicí relace, terminálové instance, webové aplikace místního hostitele, hlasové hovory a další věci.

Visual Studio Live Share navíc (na rozdíl od párového programování) umožňuje vývojářům spolupracovat a přitom si zachovat osobní předvolby editoru (například motiv a klávesové zkratky) a také mít vlastní kurzor. Vývojáři díky tomu můžou hladce přepínat mezi vzájemným sledováním a samostatným zkoumáním nápadů nebo úloh. Tato schopnost pracovat společně _a přitom_ nezávisle přináší v praxi možnosti spolupráce, které jsou pro mnoho běžných případů použití potenciálně přirozenější.

Jste připraveni začít? V tomto článku vám seznámíme s některými koncepcemi a ukážeme, jak instalovat potřebná rozšíření. Pokud hledáte zkrácenou verzi, podívejte se na naše články Rychlý start o [sdílení](quickstart/share.md) a [připojení](quickstart/join.md).

> [!TIP]
> Víte, že se můžete *připojit k vlastní relaci spolupráce*? Díky tomu si můžete Live Share vyzkoušet sami nebo můžete rozjet instanci Visual Studia nebo VS Code a vzdáleně se k ní připojit. U obou instancí můžete dokonce používat stejnou identitu. Vyzkoušejte to!

## <a name="install-visual-studio-live-share"></a>Instalace rozšíření Visual Studio Live Share

Než začnete, měli byste zajistit, abyste měli Visual Studio a Visual Studio Code nainstalované ve verzích, které splňují základní požadavky rozšíření Live Share.

- **Visual Studio Code 1.22.0 nebo vyšší** – Windows 7, 8.1 nebo 10, macOS *(pouze Sierra 10.12 nebo vyšší)*, 64bitový Linux *(doporučuje se 64bitový Ubuntu Desktop 16.04+, Fedora 27+ – [podívejte se na podrobnosti](use/vscode.md#installation))*
- **Visual Studio 2019** (libovolná edice) – Windows 7, 8.1 nebo 10
- **Visual Studio 2017 15.6 nebo vyšší** (libovolná edice) – Windows 7, 8.1 nebo 10

Stažení a instalace rozšíření Visual Studio Live Share pak bude hračka:

<table style="width: 100%; border:none;">
<tr>
    <td width="128px" style="width: 128px; text-align: center; border:none;"><img src="media/vs-code.svg" width="128px" alt="Visual Studio Code logo"/></td>
    <td style="border:none;">
        <strong>Visual Studio Code (1.22.0+)</strong><br />
        1. Nainstalujte <a href="https://code.visualstudio.com/">Visual Studio Code</a> pro Windows (7, 8.1 nebo 10), macOS <b>(Sierra+)</b>, 64bitový Linux <b>(<a href="use/vscode.md#installation">podrobnosti</a>)</b>.<br />
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
        2. Nainstalujte <a href="reference/platform-support.md">podporované sady funkcí</a> (například ASP.NET, .NET Core, C++ a/nebo Node.js).<br />
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

## <a name="concepts-and-features"></a>Koncepce a funkce

Podobně jako jiné produkty poskytuje i Visual Studio Live Share sadu výkonných funkcí, které jsou založené na některých základních koncepcích. V této části vás seznámíme s některými koncepcemi a nabídneme stručný přehled funkcí.

### <a name="collaboration-sessions"></a>Relace spolupráce

Všechny aktivity spolupráce ve Visual Studiu Live Share zahrnují jednoho **hostitele relace spolupráce** a jednoho nebo více **hostů**. Hostitel je osoba, která relaci spolupráce zahájila, a host je každý, kdo se k relaci připojí.

Hostitelé relace spolupráce můžou používat všechny své nástroje a služby, ale hosté mají přístup jenom k určitým věcem, které s nimi chce hostitel sdílet. K nim patří kód, běžící servery, ladicí relace, terminály a další věci. V současnosti se veškerý sdílený obsah uchovává na počítači hostitele a nesynchronizuje se s cloudem nebo s počítači hostů. To umožňuje _okamžitý přístup_ a _lepší zabezpečení_. Výhodou je, že celé řešení je dostupné v okamžiku, kdy se host připojí, a přestane být k dispozici ve chvíli, kdy hostitel ukončí relaci spolupráce. Kromě toho je výhodné i to, že dočasné soubory vytvořené integrovaným vývojovým prostředím (IDE) nebo editorem za účelem zlepšení výkonu pro hosta se při skončení relace automaticky vyčistí.

#### <a name="sharing"></a>Sdílení

Když „sdílíte“ jako hostitel, zahájíte tím relaci spolupráce, která sdílí obsah projektu, řešení nebo složky. Hosté můžou získat přístup k tomuto obsahu pomocí pozvánky s odkazem, který jim pošlete. „Sdílením“ se sice zkráceně myslí „sdílení projektu“, ale otevírají se jím také dveře pro sdílení dalších schopností, jako je ladění.

**Další informace:** [![VS Code](media/vscode-icon-15x15.png)](use/vscode.md#share-a-project) [![VS](media/vs-icon-15x15.png)](use/vs.md#share-a-project)

#### <a name="joining"></a>Spojování

Když vám hostitel pošle pozvánku s odkazem, můžete na odkaz kliknout a připojit se k relaci spolupráce jako host. Získáte tak přístup k veškerému obsahu a schopnostem, které s vámi chce hostitel sdílet. Tento webový odkaz vám umožňuje rychle se připojit k relaci spolupráce (pokud už máte rozšíření nainstalované) nebo rychle připravit informace (pokud rozšíření ještě nainstalované nemáte).

**Další informace:** [![VS Code](media/vscode-icon-15x15.png)](use/vscode.md#join-a-collaboration-session) [![VS](media/vs-icon-15x15.png)](use/vs.md#join-a-collaboration-session)

### <a name="features"></a>Funkce

#### <a name="co-editing"></a>Společné úpravy

Když otevřete stejný soubor jako jiný spolupracovník, můžete okamžitě „společně upravovat“ obsah souboru. Uvidíte úpravy jednotlivých spolupracovníků, jejich kurzory a výběry i další věci. A ještě lepší je to, že nemusíte stejný soubor upravovat pořád společně, takže chvíli můžete sobecky pracovat nezávisle, nebo zase spolupracovat – jak se to zrovna hodí.

> [!NOTE]
> Společné upravování má několik omezení. Stav funkcí podle jazyků najdete v článku [o podpoře platforem](reference/platform-support.md).

**Další informace:** [![VS Code](media/vscode-icon-15x15.png)](use/vscode.md#co-editing) [![VS](media/vs-icon-15x15.png)](use/vs.md#co-editing)

#### <a name="following-and-focusing"></a>Sledování a zaměření

Někdy potřebujete objasnit problém nebo návrh, který se týká více souborů nebo míst v kódu. V takových situacích může být užitečné dočasně sledovat kolegy, jak se při společných úpravách pohybují v projektu. Z tohoto důvodu to funguje tak, že když se připojíte jako host k relaci spolupráce, automaticky „sledujete“ místo úprav hostitele. Hostitelé a hosté můžou vzájemné sledování zapínat a vypínat jednoduše kliknutím myší. Kromě toho ale můžete chtít, aby vás sledovali všichni účastníci. Live Share vám umožňuje žádat, aby všichni „zaměřili“ svou pozornost na vás – prostřednictvím oznámení, které ostatním usnadní vaše zpětné sledování.

**Další informace:** [![VS Code](media/vscode-icon-15x15.png)](use/vscode.md#following) [![VS](media/vs-icon-15x15.png)](use/vs.md#following)

#### <a name="co-debugging"></a>Společné ladění

Při ladění obtížných problémů nebo chyb v kódu může být opravdu užitečné mít k tomu pár očí navíc. Jako hostiteli vám Live Share umožňuje automaticky „společné ladění“ – to znamená sdílení ladicí relace se všemi hosty. Každý z vás tak získá funkce společných úprav spolu s možností nezávislého zkoumání během společného krokování.

> [!NOTE]
> Stav funkcí ladění podle jazyků a platforem najdete v článku [o podpoře platforem](reference/platform-support.md).

**Další informace:** [![VS Code](media/vscode-icon-15x15.png)](use/vscode.md#co-debugging) [![VS](media/vs-icon-15x15.png)](use/vs.md#co-debugging)

#### <a name="share-server--share-port"></a>Sdílení serveru / sdílení portu

Při společném ladění může být opravdu užitečné mít přístup k různým částem aplikace obsluhované hostitelem pro ladicí relaci. Můžete chtít k aplikaci přistupovat v prohlížeči, mít přístup k místní databázi nebo ke koncovému bodu REST z vašich nástrojů. Live Share umožňuje „sdílení serveru“ – při kterém se místní port na počítači hostitele mapuje na přesně stejný port na počítači každého hosta. Jako host pak můžete s aplikací pracovat stejně, jako by běžela na vašem počítači (hostitel i host mají například přístup k webové aplikaci běžící na http://localhost:3000).

**Další informace:** [![VS Code](media/vscode-icon-15x15.png)](use/vscode.md#share-a-server) [![VS](media/vs-icon-15x15.png)](use/vs.md#share-a-server)

#### <a name="share-terminals"></a>Sdílení terminálů

Moderní vývojáři často používají celou řadu nástrojů příkazového řádku. Live Share vám jako hostiteli naštěstí umožňuje volitelné „sdílení terminálu“ s hosty. Sdílený terminál může umožňovat jenom čtení, nebo úplnou spolupráci – vy i hosté pak můžete spouštět příkazy a zobrazovat výsledky. Jako hostitel to máte pod kontrolou a můžete rozhodnout, jestli ostatní spolupracovníci můžou sami spouštět příkazy, nebo jenom uvidí výstupy příkazů. Přesněji řečeno je to tak, že cokoli si chcete nechat sami pro sebe, můžete spustit v nesdíleném terminálu.

**Další informace:** [![VS Code](media/vscode-icon-15x15.png)](use/vscode.md#share-a-terminal) [![VS](media/vs-icon-15x15.png)](use/vs.md#share-a-terminal)

#### <a name="access-controls"></a>Řízení přístupu

Visual Studio Live Share nabízí účastníkům mnoho skvělých způsobů spolupráce. Vzhledem k množství možností a flexibilitě, jakou mají hosté při interakci s hostiteli, můžete chtít hosty, kteří se můžou připojit, explicitně schvalovat, nebo zablokovat přístup k určitým souborům nebo složkám. Live Share nabízí řadu nastavení, která vám můžou pomoct – včetně přístupu jen pro čtení a vyžadování souhlasu s hosty.

**Další informace:** [![VS Code](media/vscode-icon-15x15.png)](reference/security.md) [![VS](media/vs-icon-15x15.png)](reference/security.md)

#### <a name="flexible-connection-modes"></a>Flexibilní režimy připojení

K zajištění optimálního výkonu podporuje Visual Studio Live Share dva základní „režimy připojení“: „přímý“ a „přenosový“. V přímém režimu se hosté připojují přímo k hostiteli, aniž by procházeli přes web. Přenosový režim umožňuje hostům umístěným v úplně jiné síti připojovat se k hostiteli prostřednictvím internetového přenosu. Připojení jsou vždy šifrovaná protokolem SSH nebo SSL, aby k tomu, co se děje „na drátě“, měli přístup jenom spolupracovníci. Live Share je standardně v „automatickém“ režimu, který nejdříve vyzkouší přímé připojení a až při neúspěšném pokusu přepne na přenosové. Pokud ale chcete, můžete jeden režim uzamknout.

**Další informace:** [![VS Code](media/vscode-icon-15x15.png)](reference/connectivity.md#changing-the-connection-mode) [![VS](media/vs-icon-15x15.png)](reference/connectivity.md#changing-the-connection-mode)

## <a name="see-also"></a>Viz také:

Rychlý start

- [Sdílení prvního projektu](quickstart/share.md)
- [Připojení k první relaci](quickstart/join.md)

Postupy

- [Spolupráce ve Visual Studio Code](use/vscode.md)
- [Spolupráce ve Visual Studiu](use/vs.md)

Odkaz

- [Požadavky na připojení pro Live Share](reference/connectivity.md)
- [Funkce zabezpečení Live Share](reference/security.md)
- [Podpora jazyků a platforem](reference/platform-support.md)
- [Podpora rozšíření](reference/extensions.md)
- [Zpráva k vydání verze](https://aka.ms/vsls-releases)

Máte potíže? Podívejte se na článek o [odstraňování potíží](troubleshooting.md) nebo nám [pošlete svůj názor](support.md).
