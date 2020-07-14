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
ms.openlocfilehash: ff5dff3e6a88dba8e0d6f49c5bdcf52d1163ef1a
ms.sourcegitcommit: 6b1c502ba1763527aa69bad2e0c919d60a47153d
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/14/2020
ms.locfileid: "86300269"
---
<!--
Copyright &copy; Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="how-to-do-technical-interviews-using-live-share"></a>Postupy: provádění technických rozhovorů pomocí Live Share

Pomocí Live Share pro rozhovory umožníte, aby si revidující a kandidáti měli rychlou a spolehlivou relaci s pohovorem, a to s využitím integrovaného vývojového prostředí (IDE) s plnou věrností. Tento kurz se zaměřuje na použití ["plánovaných relací"](../reference/insiders.md) a [Live Shareho webového připojení](../quickstart/browser-join.md) pro prostředí s pohovorem. 

## <a name="setup-for-interviewer-vs-code"></a>Nastavení pro revidujícího (VS Code)

Nainstalujte [Visual Studio Code](../use/vscode.md) a stáhněte [Live Share rozšíření balíčku](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare-pack) z webu Marketplace. Balíček rozšíření vám poskytne naši zvukovou podporu pro rozhovory.

>[!TIP]
>Pokud chcete mít v VS Code nejlepší možnosti zobrazení pomocí Live Share, nezapomeňte zapnout příznak funkce Live Share Insiders. *Předvolby: rozšíření UserSettings > > Visual Studio Live Share > sadě funkcí: Insiders*

>[!NOTE]
> Live Share chat v VS Code obsahuje sestavení s rozšířením Live Share.

## <a name="scheduling-an-interview"></a>Plánování pohovoru 

**Live Share v vs Code** poskytuje možnost vytvářet relace Live Share předem. Pomocí následujících kroků můžete vytvořit relaci předem:

### <a name="option-a-insider"></a>Možnost A (Insider)
1. `Planned Sessions`V Viewlet otevřete a vytvořte novou relaci. Nyní teď vytvořila relaci Live Share pro vás, která bude k dispozici z Viewlet po dobu rozhovoru. 

![plánované – Session – CreateLink](../media/planned-session-creation-vscode.PNG)


2. Kopírovat odkaz z Viewlet a odeslat ho kandidátovi. Odkaz, který pošlete na kandidáta, je možné použít v době, kdy se pohovor připojí k relaci.

![plánované – Session – COPYLINK](../media/planned-session-copylink-vscode.PNG)


### <a name="option-b-not-an-insider"></a>Možnost B (nejedná se o program Insider)

1. Přejít na adresu `Command Palette` pomocí`Ctrl+Shift+P`
1. Zadejte "živý SHA..." a klikněte na příkaz '_Live Share: vytvořit opakovaně použitelný odkaz na relaci_'.

![VSCode – reusablesessioncmd](../media/vscode-cmdpalette-createreusablelink.png)

3. Tím se vytvoří opakovaně použitelná relace a odkaz na ni se zkopíruje do schránky. V pravém dolním rohu editoru se zobrazí místní okno s oznámením.

![VSCode – reusablesessionnotif](../media/vscode-notification-resuablesession.png)

4. pošlete odkaz.

Jakmile budete mít tento odkaz, stačí ho sdílet s interviewee prostřednictvím e-mailu nebo podle vašeho výběru mechanismu plánování. Stačí kliknout na tento odkaz v okamžiku rozhovoru a bude se nacházet v relaci Live Share. 
> [!TIP] 
>Opakovaně použitelná propojení relace je trvalé a trvá po dobu 30 dnů od jejího vytvoření nebo data posledního použití. Při generování opakovaně použitelného odkazu relace pro váš rozhovor se ujistěte, že je pohovor do 30 dnů od data vytvoření odkazu. V případě vypršení platnosti odkazu stačí vytvořit novou opakovaně použitelnou relaci. (K dispozici je způsob, jak zajistit, aby propojení nikdy nevypršelo, ale je to pro rozhovory jen snazší.)

**Poznámka:** V současné době není Live Share v aplikaci Visual Studio možné vytvářet relace předem. Pro rozhovory, které provádíte pomocí Live Share v aplikaci Visual Studio, můžete postupovat podle našeho průvodce, jak [spustit relaci okamžité](../quickstart/share.md) Live Share.



## <a name="setup-for-candidate"></a>Nastavení pro kandidáta
I když kandidát může vždycky nainstalovat aplikaci Visual Studio nebo Visual Studio Code, aby se mohla spojit s pohovorem, není potřeba. **K relacím na Live Share rozhovorů se dá přihlásili kandidáti bez předchozího nastavení.** Můžou kliknout na odkaz na rozhovor v době relace a **připojit se z prohlížeče**. Další informace najdete [tady.](../quickstart/browser-join.md)


<!--
### **What to do as an Interviewer?**

As an interviewer you will act as the host of the Live Share session. If you are not familiar with Live Share, we suggest you refer to the [share a project](../use/vscode.md) section of our how-to guide
### **What to do as the Interviewee?**

If you are expecting to do a Technical Interview using Live Share, you are in luck! We want to make sure you are familiar with the basic Live Share features so you feel comfortable during your interview.

1. Before the interview, take some time and look over the [How-to guide](../use/vscode.md) so you understand how Live Share works.

1. You may want to install Visual Studio Code beforehand so that you are not waiting for the installation to complete once you start your interview

1. If you don't have the time, no worries. All you need to have a full interview is the link to a Live Share session your interviewer sends you while scheduling the interview. Just clicking on the link will automatically take you through all the steps needed.

1. At the time of the interview, just click on the link and follow the steps it takes you through. If you are early or your interviewer is late to the interview, don't worry! You will just be in the 'lobby' waiting for your interviewer to join. No other steps are required, and once your interviewer joins the session will automatically start.

>[!NOTE]
>If you find that the session has disconnected before or after the interviewer joined, don't worry. Just exit out of that session if (it isn't already closed) and re-click on the same link!

You are now all set to go with using Live Share for your interview! 
-->
