---
title: Insider | Microsoft Docs
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
ms.openlocfilehash: a58bf30ad1c6f4c4cecedb1a07ca0482a67f5ec7
ms.sourcegitcommit: 9deed590c0876b732c8eb150a9a23498a8243efc
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/27/2021
ms.locfileid: "98870718"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="insiders"></a>Účastníci programu Insider

Tým Visual Studio Live Share je vše o iteracích rychle, vyzkoušení nových nápadů a naslouchání našim zákazníkům! Insider nabízí našim uživatelům příležitost vyzkoušet si všechny nové funkce jako první a poskytnou jim svůj názor. Naučte se, jak [se stát Insider](#BecomeanInsider) , a požádejte ho o budoucí spolupráci vývojářů. 

## <a name="new-to-insiders"></a>✨ Novinky pro program Insider ✨

### <a name="planned-sessions-vs-code"></a>**Plánované relace (VS Code)**
Opakovaně použitelné relace nyní mají místo v Live Share Viewlet. Plánované relace vám umožní jako hostitele relace Live Share vytvořit propojení Live Share relace předem. 


![Obrázek plánované-Session-CreateLink-VSCode ](../media/planned-session-creation-vscode.png)
 *znázorňující vytvoření nové plánované relace z Viewlet*

Díky tomu můžete tento odkaz sdílet jako součást pravidelně naplánovaných schůzek ve vašich týmech, vašich rozhovorech nebo relacích párování.
Jakmile je relace naplánovaná předem, máte k ní přístup přímo z Live Share Viewlet. 

![Obrázek plánované relace-Session-VSCode ](../media/planned-session-copylink-vscode.png) * znázorňující "plánované relace" ve službě Live Share Viewlet

>[!TIP]
>Zapněte v programu Insider Live Share v VS Code, aby používala možnost plánované >relace. Přečtěte si, jak se stát s buildem Insider níže. 

Možnost plánované relace v aplikaci Visual Studio je momentálně pouze interní funkcí. V případě, že přejdete do fáze Insider, vraťte se prosím na aktualizace. 


# <a name="pushed-to-public"></a>Vloženo na veřejné 

Následující funkce programu Insider byly vloženy na veřejné.

### <a name="reusable-sessions-vs-code"></a>**Opakovaně použitelné relace (VS Code)**

Live Share teď můžou hostovat opakovaně použitelné relace! Opakovaně použitelné relace poskytují možnost znovu použít relaci Live Share pro různé scénáře. To znamená, že můžete naplánovat předem Live Share relaci pro vaše technické rozhovory, týdenní Mob relaci programování, použít stejnou relaci při podávání přítele a spoustu dalšího.

Chcete-li vytvořit opakovaně použitelnou relaci, postupujte následovně:
1. Přejít na adresu `Command Palette` pomocí `Ctrl+Shift+P`
1. Zadejte "živý SHA..." a klikněte na příkaz '**_Live Share: vytvořit opakovaně použitelný odkaz na relaci_**'.

![VSCode – reusablesessioncmd](../media/vscode-cmdpalette-createreusablelink.png)

3. Tím se vytvoří opakovaně použitelná relace a odkaz na ni se zkopíruje do schránky. V pravém dolním rohu editoru se zobrazí místní okno s oznámením.

![VSCode – reusablesessionnotif](../media/vscode-notification-resuablesession.png)

4. Vaše opakovaně použitelná relace se vytvořila! Sdílejte odkaz s vaší relací a použijte ho pokaždé, když budete mít přístup k této relaci.

> [!TIP] 
>Opakovaně použitelná propojení relace je trvalé a trvá po dobu 30 dnů od jejího vytvoření nebo data posledního použití. To znamená, že pokud stále používáte relaci nejméně jednou za 30 dní, nemusíte se o vypršení platnosti této relace starat. Jednoduše uložte odkaz na bezpečné místo, kde k němu máte snadný přístup.
 


## <a name="become-an-insider"></a>Staňte se Insider <a name="BecomeanInsider"></a>

Ve výchozím nastavení platí, že po instalaci rozšíření Visual Studio Live Share používáte `Stable` sadu funkcí, která zahrnuje všechny funkce připravené pro produkční prostředí (např. společné úpravy, sdílené ladění, terminály). Pokud byste ale chtěli získat dřívější přístup k funkci, na které pracujeme, můžete se přihlásit k `Insiders` sadě funkcí změnou následujícího nastavení v integrovaném vývojovém prostředí:

* Visual Studio

    ![sada funkcí – vs](../media/feature-set-vs.png)

* Visual Studio Code 

    ![funkce Set-VSCode](../media/feature-set-vscode.png)

Následující části popisují sadu funkcí, které jsou aktuálně v `Insiders` sadě funkcí, a proto jsou připravené k vyhodnocení po změně výše uvedeného nastavení:



## <a name="see-also"></a>Viz také

- [Podpora jazyků a platforem](platform-support.md)
- [Požadavky na připojení pro Live Share](connectivity.md)
- [Funkce zabezpečení Live Share](security.md)
- [Všechny hlavní chyby, žádosti o funkce a omezení](https://aka.ms/vsls-issues)
- [Všechny požadavky a omezení funkcí](https://aka.ms/vsls-feature-requests)

Máte potíže? Podívejte se na článek o [odstraňování potíží](../troubleshooting.md) nebo nám [pošlete svůj názor](../support.md).
