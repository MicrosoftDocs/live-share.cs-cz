---
title: Přehled | Microsoft Docs
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
ms.openlocfilehash: fd6c028729c6b376e48995a01c8f625b96d06f85
ms.sourcegitcommit: 9deed590c0876b732c8eb150a9a23498a8243efc
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/27/2021
ms.locfileid: "98870774"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->
# <a name="live-share-features-and-concepts"></a>Live Share funkce a koncepty 

Live Share je sestavená pomocí Revoluční architektury a konceptů, které pro naše uživatele manifestují jako výkonné funkce. Níže najdete všechny charakteristické funkce Live Share a to, co vedoucí v prostoru pro spolupráci způsobuje. 

### <a name="collaboration-sessions"></a>Relace spolupráce

Všechny aktivity spolupráce ve Visual Studiu Live Share zahrnují jednoho **hostitele relace spolupráce** a jednoho nebo více **hostů**. Hostitel je osoba, která spustila relaci spolupráce, a kdokoli, kdo se připojuje, je host.

Hostitelé relace spolupráce můžou používat všechny své nástroje a služby, ale hosté mají přístup jenom k určitým věcem, které s nimi chce hostitel sdílet. K nim patří kód, běžící servery, ladicí relace, terminály a další věci. V současnosti se veškerý sdílený obsah uchovává na počítači hostitele a nesynchronizuje se s cloudem nebo s počítači hostů. To umožňuje _okamžitý přístup_ a _lepší zabezpečení_. Výhodou je, že celé řešení je dostupné v okamžiku, kdy se host připojí, a přestane být k dispozici ve chvíli, kdy hostitel ukončí relaci spolupráce. Kromě toho je výhodné i to, že dočasné soubory vytvořené integrovaným vývojovým prostředím (IDE) nebo editorem za účelem zlepšení výkonu pro hosta se při skončení relace automaticky vyčistí.

#### <a name="sharing"></a>Sdílení

Když „sdílíte“ jako hostitel, zahájíte tím relaci spolupráce, která sdílí obsah projektu, řešení nebo složky. Hosté můžou získat přístup k tomuto obsahu pomocí pozvánky s odkazem, který jim pošlete. „Sdílením“ se sice zkráceně myslí „sdílení projektu“, ale otevírají se jím také dveře pro sdílení dalších schopností, jako je ladění.

**Další informace:** [ ![ vs Code](../media/vscode-icon-15x15.png)](../use/vscode.md#share-a-project) [ ![ vs](../media/vs-icon-15x15.png)](../use/vs.md#share-a-project)

#### <a name="joining"></a>Připojení

Když vám hostitel pošle pozvánku s odkazem, můžete na odkaz kliknout a připojit se k relaci spolupráce jako host. Získáte tak přístup k veškerému obsahu a schopnostem, které s vámi chce hostitel sdílet. Tento webový odkaz vám umožňuje rychle se připojit k relaci spolupráce (pokud už máte rozšíření nainstalované) nebo rychle připravit informace (pokud rozšíření ještě nainstalované nemáte).

**Další informace:** [ ![ vs Code](../media/vscode-icon-15x15.png)](../use/vscode.md#join-a-collaboration-session) [ ![ vs](../media/vs-icon-15x15.png)](../use/vs.md#join-a-collaboration-session)

### <a name="features"></a>Funkce

#### <a name="co-editing"></a>Společné úpravy

Když otevřete stejný soubor jako jiný spolupracovník, můžete okamžitě „společně upravovat“ obsah souboru. Uvidíte úpravy jednotlivých spolupracovníků, jejich kurzory a výběry i další věci. A ještě lepší je to, že nemusíte stejný soubor upravovat pořád společně, takže chvíli můžete sobecky pracovat nezávisle, nebo zase spolupracovat – jak se to zrovna hodí.

> [!NOTE]
> Společné upravování má několik omezení. Stav funkcí podle jazyků najdete v článku [o podpoře platforem](../reference/platform-support.md).

**Další informace:** [ ![ vs Code](../media/vscode-icon-15x15.png)](../use/vscode.md#co-editing) [ ![ vs](../media/vs-icon-15x15.png)](../use/vs.md#co-editing)

#### <a name="following-and-focusing"></a>Sledování a zaměření

Někdy potřebujete objasnit problém nebo návrh, který se týká více souborů nebo míst v kódu. V takových situacích může být užitečné dočasně sledovat kolegy, jak se při společných úpravách pohybují v projektu. Z tohoto důvodu to funguje tak, že když se připojíte jako host k relaci spolupráce, automaticky „sledujete“ místo úprav hostitele. Hostitelé a hosté můžou vzájemné sledování zapínat a vypínat jednoduše kliknutím myší. Kromě toho ale můžete chtít, aby vás sledovali všichni účastníci. Live Share vám umožňuje žádat, aby všichni „zaměřili“ svou pozornost na vás – prostřednictvím oznámení, které ostatním usnadní vaše zpětné sledování.

**Další informace:** [ ![ vs Code](../media/vscode-icon-15x15.png)](../use/vscode.md#following) [ ![ vs](../media/vs-icon-15x15.png)](../use/vs.md#following)

#### <a name="co-debugging"></a>Společné ladění

Při ladění obtížných problémů nebo chyb v kódu může být opravdu užitečné mít k tomu pár očí navíc. Jako hostiteli vám Live Share umožňuje automaticky „společné ladění“ – to znamená sdílení ladicí relace se všemi hosty. Každý z vás tak získá funkce společných úprav spolu s možností nezávislého zkoumání během společného krokování.

> [!NOTE]
> Stav funkcí ladění podle jazyků a platforem najdete v článku [o podpoře platforem](../reference/platform-support.md).

**Další informace:** [ ![ vs Code](../media/vscode-icon-15x15.png)](../use/vscode.md#co-debugging) [ ![ vs](../media/vs-icon-15x15.png)](../use/vs.md#co-debugging)

#### <a name="share-server--share-port"></a>Sdílení serveru / sdílení portu

Při společném ladění může být opravdu užitečné mít přístup k různým částem aplikace obsluhované hostitelem pro ladicí relaci. Můžete chtít k aplikaci přistupovat v prohlížeči, mít přístup k místní databázi nebo ke koncovému bodu REST z vašich nástrojů. Live Share umožňuje „sdílení serveru“ – při kterém se místní port na počítači hostitele mapuje na přesně stejný port na počítači každého hosta. Jako host pak můžete s aplikací pracovat stejně, jako by běžela na vašem počítači (hostitel i host mají například přístup k webové aplikaci běžící na http://localhost:3000).

**Další informace:** [ ![ vs Code](../media/vscode-icon-15x15.png)](../use/vscode.md#share-a-server) [ ![ vs](../media/vs-icon-15x15.png)](../use/vs.md#share-a-server)

#### <a name="share-terminals"></a>Sdílení terminálů

Moderní vývojáři často používají celou řadu nástrojů příkazového řádku. Live Share vám jako hostiteli naštěstí umožňuje volitelné „sdílení terminálu“ s hosty. Sdílený terminál může umožňovat jenom čtení, nebo úplnou spolupráci – vy i hosté pak můžete spouštět příkazy a zobrazovat výsledky. Jako hostitel to máte pod kontrolou a můžete rozhodnout, jestli ostatní spolupracovníci můžou sami spouštět příkazy, nebo jenom uvidí výstupy příkazů. Přesněji řečeno je to tak, že cokoli si chcete nechat sami pro sebe, můžete spustit v nesdíleném terminálu.

**Další informace:** [ ![ vs Code](../media/vscode-icon-15x15.png)](../use/vscode.md#share-a-terminal) [ ![ vs](../media/vs-icon-15x15.png)](../use/vs.md#share-a-terminal)

#### <a name="access-controls"></a>Řízení přístupu

Visual Studio Live Share nabízí účastníkům mnoho skvělých způsobů spolupráce. Vzhledem k množství možností a flexibilitě, jakou mají hosté při interakci s hostiteli, můžete chtít hosty, kteří se můžou připojit, explicitně schvalovat, nebo zablokovat přístup k určitým souborům nebo složkám. Live Share nabízí řadu nastavení, která vám můžou pomoct – včetně přístupu jen pro čtení a vyžadování souhlasu s hosty.

**Další informace:** [ ![ vs Code](../media/vscode-icon-15x15.png)](../reference/security.md) [ ![ vs](../media/vs-icon-15x15.png)](../reference/security.md)

#### <a name="flexible-connection-modes"></a>Flexibilní režimy připojení

K zajištění optimálního výkonu podporuje Visual Studio Live Share dva základní „režimy připojení“: „přímý“ a „přenosový“. V přímém režimu se hosté připojují přímo k hostiteli, aniž by procházeli přes web. Přenosový režim umožňuje hostům umístěným v úplně jiné síti připojovat se k hostiteli prostřednictvím internetového přenosu. Připojení jsou vždy šifrovaná protokolem SSH nebo SSL, aby k tomu, co se děje „na drátě“, měli přístup jenom spolupracovníci. Live Share je standardně v „automatickém“ režimu, který nejdříve vyzkouší přímé připojení a až při neúspěšném pokusu přepne na přenosové. Pokud ale chcete, můžete jeden režim uzamknout.

**Další informace:** [ ![ vs Code](../media/vscode-icon-15x15.png)](../reference/connectivity.md#changing-the-connection-mode) [ ![ vs](../media/vs-icon-15x15.png)](../reference/connectivity.md#changing-the-connection-mode)
