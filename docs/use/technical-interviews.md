---
title: Spolupráce pomocí Visual Studio Code-Visual Studio Live Share | Microsoft Docs
description: Sada postupů spolupráce pro Visual Studio Code a Live Share.
ms.custom: ''
ms.date: 09/16/2019
ms.reviewer: ''
ms.suite: ''
ms.topic: conceptual
author: fubaduba
ms.author: fubaduba
manager: JonathanCarter
ms.workload:
- liveshare
ms.openlocfilehash: 810c60754c0be4f11511fb1ccbb0bb612de42e5d
ms.sourcegitcommit: 3a1b22eac528b0f6a241f9fec7ec20264db24cfe
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/13/2019
ms.locfileid: "74019806"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="how-to-do-technical-interviews-using-live-share"></a>Postupy: provádění technických rozhovorů pomocí Live Share

Než začnete používat Live Share k technickým rozhovorům, je nutné provést jeden integrálový krok: **stažení Visual Studio Code a balíček rozšíření Live Share z webu Marketplace** pomocí následujících [kroků.](../use/vscode.md)

Live Share poskytuje možnost hostování opakovaně použitelných relací! To znamená, že můžete naplánovat předem Live Share relaci pro vaše technické pohovory a nemusíte si dělat starosti s vypršením platnosti odkazu.

> [!TIP] 
>Opakovaně použitelná propojení relace je trvalé a trvá po dobu 30 dnů od jejího vytvoření nebo data posledního použití. Při generování opakovaně použitelného odkazu relace pro váš rozhovor se ujistěte, že je pohovor do 30 dnů od data vytvoření odkazu. V případě vypršení platnosti odkazu stačí vytvořit novou opakovaně použitelnou relaci. (K dispozici je způsob, jak zajistit, aby propojení nikdy nevypršelo, ale je to pro rozhovory jen snazší.)

### <a name="what-to-do-as-an-interviewer"></a>**Co dělat jako revidující?**

Jako revidující budete působit jako hostitel relace Live Share. Pokud nejste obeznámeni s Live Share, doporučujeme vám Přečtěte si část " [sdílení projektu](../use/vscode.md) " v našem průvodci.

Teď vytvořte relaci Live Share pro váš technický rozhovor a místo běžné relace pro spolupráci vytvoříte speciální "opakovaně použitelnou relaci". To vám umožní mít Live Shareou relaci, která se dá naplánovat předem a pak ji použít kdykoli.

Chcete-li vytvořit opakovaně použitelnou relaci, postupujte následovně:

1. Přejít na `Command Palette` pomocí `Ctrl+Shift+P`
1. Zadejte "živý SHA..." a klikněte na příkaz ' **_Live Share: vytvořit opakovaně použitelný odkaz na relaci_** '.

![VSCode – reusablesessioncmd](../media/vscode-cmdpalette-createreusablelink.png)

3. Tím se vytvoří opakovaně použitelná relace a odkaz na ni se zkopíruje do schránky. V pravém dolním rohu editoru se zobrazí místní okno s oznámením.

![VSCode – reusablesessionnotif](../media/vscode-notification-resuablesession.png)

4. Vaše opakovaně použitelná relace se vytvořila! Sdílejte odkaz s vaší relací a použijte ho pokaždé, když budete mít přístup k této relaci.

Jakmile budete mít tento odkaz, stačí ho sdílet s interviewee prostřednictvím e-mailu nebo podle vašeho výběru mechanismu plánování. Stačí kliknout na tento odkaz v okamžiku rozhovoru a bude se nacházet v relaci Live Share. 

### <a name="what-to-do-as-the-interviewee"></a>**Co dělat jako Interviewee?**

Pokud očekáváte, že budete provádět technický rozhovor pomocí Live Share, jste na hodně štěstí! Chceme mít jistotu, že jste obeznámeni se základními funkcemi Live Share, abyste se mohli svými pohovorem cítit.

1. Než se podíváte na rozhovor, podrobnější informace si přečtěte [Průvodce postupy](../use/vscode.md) , abyste se seznámili s tím, jak Live Share funguje.

1. Možná budete chtít nainstalovat Visual Studio Code předem, abyste nečekali na dokončení instalace po zahájení rozhovoru.

1. Pokud nemáte čas, nedělejte si starosti. Vše, co potřebujete k úplnému pohovoru, je odkaz na Live Share relaci, kterou váš revidující vám pošle během plánování pohovoru. Pouhým kliknutím na odkaz se vás automaticky provede všemi potřebnými kroky.

1. V okamžiku rozhovoru stačí kliknout na odkaz a postupovat podle kroků, které vás provede. Pokud jste v brzké době nebo jste viděli pozdě, nedělejte si starosti! Jenom přijdete o "předsálí", který se vašemu spolupohledu připojí. Nejsou nutné žádné další kroky a jakmile se provedený revidující připojí k relaci, automaticky spustí.

>[!NOTE]
>Pokud zjistíte, že se relace odpojila před nebo po připojení k prodanému spolupohledu, nedělejte si starosti. Pokud (ještě není uzavřený), stačí ukončit tuto relaci a znovu kliknout na stejný odkaz.

Nyní je vše nastaveno na použití Live Share pro rozhovor. 
