---
title: Insider – Visual Studio Live sdílenou složku | Dokumentace Microsoftu
description: Popis kanálu "Insiders" v rámci Visual Studio Live Share.
ms.custom: ''
ms.date: 04/02/2019
ms.reviewer: ''
ms.suite: ''
ms.topic: reference
author: lostintangent
ms.author: joncart
manager: AmandaSilver
ms.workload:
- liveshare
ms.openlocfilehash: a79effc25c09851301bb2231511a8a9d8a9f549b
ms.sourcegitcommit: 6e84bf17eedd616417f474551344c2161700c4d3
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/18/2019
ms.locfileid: "67192713"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="insiders"></a>Účastníci programu Insider

Visual Studio Live Share týmu pokusí rychle řešit problémy v pořadí pro zpětnou vazbu uživatelů a jako součást, která nabízíme dvě samostatné funkce "kanály", který umožní se rozhodnout, jak rychle se zobrazí nové funkce. Ve výchozím nastavení, po instalaci rozšíření Visual Studio Live Share, které používáte `Stable` funkci set, která zahrnuje všechny funkce připravené pro produkční prostředí (například společně úpravy, sdílené ladění, terminály). Ale pokud chcete získat dřívější přístup k funkci pořád pracujeme, je můžete vyjádřit výslovný souhlas pro `Insiders` změnou následujících nastavení v prostředí (IDE) sady funkcí:

* Visual Studio

    ![feature-set-vs](../media/feature-set-vs.png)

* Visual Studio Code 

    ![feature-set-vscode](../media/feature-set-vscode.png)

Následující části popisují sadu možností, které jsou v současné době `Insiders` sady funkcí a proto jsou připraveny k vyhodnocení, když změníte nastavení výše uvedené:

## <a name="direct-user-invitations"></a>Pozvání uživatele s přímým přístupem

V současné době poskytuje Visual Studio a Visual Studio Code `Contacts` podokno, které umožňuje dvě klíčové funkce:

1. Zobrazení seznamu `Suggested Contacts`, které jsou vývojáři, kteří přispět k projektu aktuálně otevřené za posledních 30 dnů. V praxi to jsou lidé, které budete pravděpodobně chtít spolupracovat a proto je doporučujeme pro snazší začít pracovat.

2. Poskytuje seznam `Recent Contacts`, které jsou vývojáři jsme dříve spolupracovali pomocí Live Share. V praxi Většina vývojářů často spolupracovat stejné lidí a proto seznamu posledních umožňuje více opakovatelné způsob práce se váš tým/classroom/atd.

Ale `Contacts` seznam aktuálně umožňuje zvaní kontaktů poslední/navrhované prostřednictvím e-mailu, který jsme se naučili není tak účinné jako může být. Pokud nainstalujete nejnovější aktualizaci Live Share a povolit `Insiders` (jak je popsáno výše), které budete teď moct **pozvat vývojáře do relace spolupráci přímo z integrovaného vývojového prostředí**! Poznámka: Pokud používáte Visual Studio Code, budete muset nainstalovat [sestavení Insider](https://code.visualstudio.com/insiders/) v pořadí pro tuto funkci používat.

![Přímé Invitatiosn](https://user-images.githubusercontent.com/116461/59691804-7ece0c00-9198-11e9-94fb-99ec89df91c9.gif)

<em>Live Share hostitele (vlevo) přímo do relace pozvání partnerské zařízení (vpravo)</em>

Jakmile vývojáře ve službě Live Share, jejich stav dostupnosti bude publikován svým spolupracovníkům. V důsledku toho můžete uvidíte, že někdo z vašeho týmu je online a potom hned začít spolupracovat s nimi. Zobrazí se informační zpráva, která jim uděluje možnost připojit k relaci, nebo ne. To eliminuje potřebu zcela exchange relace adresy URL.

Po 5 minutách nečinnosti, bude stav automaticky přepnout na `Away`, a až budete v rámci relace Live Share, stav se automaticky přepne na `Do not disturb` (které suprresses pozvánku informační zprávy). Po své aktivaci opakujte nebo ponechte do relace Live Share, stav se automaticky přepnout zpět do `Available`. Se toto chování nepotřebujete, aby skutečně spravoval stavu Live Share. Je jednoduše došlo k povolení přímé pozvánky a komunikovat se svým kolegům, zda je k dispozici pro spolupráci nebo ne. Pokud dáváte přednost však můžete nastavit vždy ručně svůj stav.

Pokud se chcete odhlásit z této funkce můžete jednoduše zakázat `Presence` nastavení v rámci nastavení Live Share v sadě Visual Studio a Visual Studio Code. Jakmile zakázané, stále budete moci zobrazit stav druhé strany a pozvat je, ale nebudou publikovány stavu a ostatní nelze přímo Pozvěte.

## <a name="see-also"></a>Viz také:

- [Podpora jazyků a platforem](platform-support.md)
- [Požadavky na připojení pro Live Share](connectivity.md)
- [Funkce zabezpečení Live Share](security.md)
- [Hlavní chyby, žádosti o funkce a omezení](https://aka.ms/vsls-issues)
- [Všechny žádosti o funkce a omezení](https://aka.ms/vsls-feature-requests)

Máte potíže? Podívejte se na článek o [odstraňování potíží](../troubleshooting.md) nebo nám [pošlete svůj názor](../support.md).
