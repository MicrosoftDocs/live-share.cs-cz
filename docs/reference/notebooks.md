---
title: Poznámkové bloky – Visual Studio Live Share | Microsoft Docs
description: Podrobné informace o použití Live Share pro spolupráci s poznámkovým blokem
ms.date: 01/26/2021
ms.reviewer: ''
ms.suite: ''
ms.topic: reference
author: lostintangent
ms.author: joncart
manager: simoncal
ms.workload:
- liveshare
ms.openlocfilehash: 40e30c77ebf3a1c339e1694c413eb8e744d576b9
ms.sourcegitcommit: 9deed590c0876b732c8eb150a9a23498a8243efc
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/27/2021
ms.locfileid: "98887582"
---
# <a name="-notebooks"></a>📓 Poznámkových bloků

Poznámkové bloky se staly klíčovou součástí mnoha pracovních postupů pro vývojáře a odborníky na data. Díky Visual Studio Code, který nabízí bohatě nativní editor poznámkových bloků, se zajímáme, abychom umožnili prostředí pro spolupráci v reálném čase, které týmům a učebnám umožní používat poznámkové bloky a Live Share společně.

Prostředí Live Share Poznámkový blok je momentálně ve verzi Preview, a proto obsahuje některé z [předběžných požadavků](#pre-requisites) a [známých problémů](#known-issues) , o kterých je potřeba vědět. V této úvodní verzi Preview se rychle provede iterace a proto se neváhajíme, [abychom nám poslali jakékoli otázky a zpětnou vazbu](http://github.com/microsoftdocs/live-share), jak si ji vyhodnocujete. 👍<br />

<img width="800px" src="https://user-images.githubusercontent.com/116461/105928037-0d07a680-5ffa-11eb-8447-23bdb77fee9e.png" title="Spolupráce poznámkového bloku" />

## <a name="pre-requisites"></a>Požadavky

Než budete moct začít s poznámkovým blokům pro spolupráci, musíte jako součást této verze Preview nainstalovat následující požadavky:

| Před požadavky | Hostitel – požadováno? | Host – povinné? |
|-|-|-|
| Visual Studio Insider | ✅ | ✅ |
| Live Share v 1.0.3541 + | ✅ | ✅ |
| Nezbytná rozšíření poznámkových bloků (např. Jupyter) | ✅ | Není _k dispozici_ (Live Share to postará!) |

## <a name="getting-started"></a>Začínáme

Jakmile a vaši účastníci mají správné požadavky, můžete začít používat Live Share a poznámkové bloky pomocí následujících kroků:

1. Otevření poznámkového bloku v Visual Studio Code
1. Spustit relaci Live Share
1. Jakmile se připojíte k hostům, můžete začít společně upravovat buňky a zobrazovat kurzory ostatních a zvýraznit text.
1. Máte zábavné spolupráci na poznámkových blocích! 🎉 

## <a name="known-issues"></a>Známé problémy

Následující seznam představuje sadu známých problémů s Live Share a poznámkami experinece spolu s jejich příslušnými alternativními řešeními. 

| Problém | Alternativní řešení | 
|-|-|
| "Režim sledování" nesleduje posouvání v rámci poznámkového bloku | Pracujeme na řádné podpoře "dodržování" na poznámkových blocích, ale mezitím budete muset ručně přejít k pravé buňce poznámkového bloku, kterou chcete společně upravit s vašimi účastníky. |
| Přidávání, odstraňování a přesouvání buněk není synchronizované mezi účastníky. | Uložte dokument poznámkového bloku a všechny ho znovu otevřete. V budoucnu budeme kompletní synchronizaci operací na úrovni poznámkového bloku v reálném čase. |
| Editory poznámkových bloků nerespektují relace Live Share jen pro čtení | I když jsou hosté schopné upravovat buňky v poznámkovém bloku, nebudou je moct ukládat na disk, takže se zabezpečení zachová v relaci jen pro čtení. |
