---
title: Insider – Visual Studio Live Share | Microsoft Docs
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
ms.openlocfilehash: 04bfb314ebae711566a8bab8b0ada8f2fbd2e940
ms.sourcegitcommit: 6b46e300d76eda661ab34c67a3b909d5c162cd9a
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/28/2019
ms.locfileid: "70062270"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="insiders"></a>Účastníci programu Insider

Tým Visual Studio Live Share je vše o iteracích rychle, vyzkoušení nových nápadů a naslouchání našim zákazníkům! Insider nabízí našim uživatelům příležitost vyzkoušet si všechny nové funkce jako první a poskytnou jim svůj názor. Naučte se, jak [se stát Insider](#BecomeanInsider) , a požádejte ho o budoucí spolupráci vývojářů. 

## <a name="new-to-insiders"></a>✨ Novinky pro program Insider ✨


### <a name="reusable-sessions-vs-code"></a>**Opakovaně použitelné relace (VS Code)**

Live Share teď můžou hostovat opakovaně použitelné relace! Opakovaně použitelné relace poskytují možnost znovu použít relaci Live Share pro různé scénáře. To znamená, že můžete naplánovat předem Live Share relaci pro vaše technické rozhovory, týdenní Mob relaci programování, použít stejnou relaci při podávání přítele a spoustu dalšího.

Chcete-li vytvořit opakovaně použitelnou relaci, postupujte následovně:
1. Přejít na `Command Palette` adresu pomocí`Ctrl+Shift+P`
1. Zadejte "živý SHA..." a klikněte na **_Live Share: Příkaz vytvořit opakovaně použitelný odkaz_** na relaci.

![VSCode – reusablesessioncmd](../media/vscode-cmdpalette-createreusablelink.png)

3. Tím se vytvoří opakovaně použitelná relace a odkaz na ni se zkopíruje do schránky. V pravém dolním rohu editoru se zobrazí místní okno s oznámením.

![VSCode – reusablesessionnotif](../media/vscode-notification-resuablesession.png)

4. Vaše opakovaně použitelná relace se vytvořila! Sdílejte odkaz s vaší relací a použijte ho pokaždé, když budete mít přístup k této relaci.

> [!TIP] 
>Opakovaně použitelná propojení relace je trvalé a trvá po dobu 30 dnů od jejího vytvoření nebo data posledního použití. To znamená, že pokud stále používáte relaci nejméně jednou za 30 dní, nemusíte se o vypršení platnosti této relace starat. Jednoduše uložte odkaz na bezpečné místo, kde k němu máte snadný přístup.
 

### <a name="direct-user-invitations"></a>**Pozvání přímých uživatelů**

V současné době aplikace Visual Studio i Visual Studio Code poskytují `Contacts` podokno, které umožňuje dvě klíčové funkce:

1. Zobrazení seznamu `Suggested Contacts`, což jsou vývojáři, kteří během posledních 30 dnů přispěli k vašemu aktuálně otevřenému projektu. V praxi se jedná o lidé, se kterým pravděpodobně budete chtít spolupracovat, a proto je doporučujeme, aby bylo snazší začít.

2. Seznamte se s `Recent Contacts`vývojáři, kteří jste předtím spolupracovali pomocí Live Share. V praxi většina vývojářů často spolupracuje se stejnými lidmi, a proto poslední seznam umožňuje pracovat s týmem, třídou a dalšími možnostmi opakování práce.

V tomto seznamu `Contacts` se ale v tuto chvíli dá pozvat jenom poslední/navrhované kontakty prostřednictvím e-mailu, které jsme se naučili, protože to není tak efektivně. Pokud nainstalujete nejnovější aktualizaci Live Share a povolíte `Insiders` (jak je popsáno výše), budete teď moci **pozvat vývojáře do relace spolupráce přímo z rozhraní IDE**. Všimněte si, že pokud používáte Visual Studio Code, budete muset nainstalovat [buildy Insiders](https://code.visualstudio.com/insiders/) , aby tato funkce fungovala.

![Přímý Invitatiosn](https://user-images.githubusercontent.com/116461/59691804-7ece0c00-9198-11e9-94fb-99ec89df91c9.gif)

<em>Hostitel Live Share (vlevo), který přímo zve partnera (vpravo) do relace</em>

Když se vývojáři přihlásí pomocí Live Share, jejich stav dostupnosti se publikuje do jejich partnerských uzlů. V důsledku toho vidíte, že je někdo v týmu online a že se s nimi hned začne spolupracovat. Obdrží informační zprávu, která jim poskytne možnost připojit se k relaci, nebo ne. Tím se zcela odstraní potřeba adresy URL relací Exchange.

Po 5 minutách nečinnosti se váš stav automaticky přepne na `Away`a když jste v rámci Live Share relace, váš stav se automaticky přepne na `Do not disturb` (které oznámení informační zprávy pozvánky suprresses). Po opětovném zprovoznění nebo opuštění relace Live Share se stav automaticky přepne zpět na `Available`. S tímto chováním nemusíte ve skutečnosti spravovat stav Live Share. Stačí tam, kde můžete povolit přímé pozvánky, a komunikovat s vašimi partnery, ať už máte k dispozici spolupráci nebo ne. Pokud ale dáváte přednost, můžete stav kdykoli nastavit ručně.

Pokud chcete tuto funkci odhlásit, můžete jednoduše zakázat `Presence` nastavení v rámci nastavení Live Share v sadě Visual Studio a Visual Studio Code. Jakmile je tato možnosti zakázaná, bude se vám pořád zobrazovat stav ostatních a zvát, ale váš stav nebude publikovaný a ostatní vás nemůžou přímo pozvat.

 

## Staňte se Insider <a name="BecomeanInsider"></a>

Ve výchozím nastavení platí, že po instalaci rozšíření Visual Studio Live Share používáte sadu `Stable` funkcí, která zahrnuje všechny funkce připravené pro produkční prostředí (např. společné úpravy, sdílené ladění, terminály). Pokud byste ale chtěli získat dřívější přístup k funkci, na které pracujeme, můžete se přihlásit k `Insiders` sadě funkcí změnou následujícího nastavení v integrovaném vývojovém prostředí:

* Visual Studio

    ![feature-set-vs](../media/feature-set-vs.png)

* Visual Studio Code 

    ![feature-set-vscode](../media/feature-set-vscode.png)

Následující části popisují sadu funkcí, které jsou aktuálně v `Insiders` sadě funkcí, a proto jsou připravené k vyhodnocení po změně výše uvedeného nastavení:



## <a name="see-also"></a>Viz také:

- [Podpora jazyků a platforem](platform-support.md)
- [Požadavky na připojení pro Live Share](connectivity.md)
- [Funkce zabezpečení Live Share](security.md)
- [Všechny hlavní chyby, žádosti o funkce a omezení](https://aka.ms/vsls-issues)
- [Všechny požadavky a omezení funkcí](https://aka.ms/vsls-feature-requests)

Máte potíže? Podívejte se na článek o [odstraňování potíží](../troubleshooting.md) nebo nám [pošlete svůj názor](../support.md).
