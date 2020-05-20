---
title: Připojení z prohlížeče – Visual Studio Live Share | Microsoft Docs
description: Představujeme připojení z prohlížeče
ms.date: 03/18/2020
ms.reviewer: ''
ms.suite: ''
ms.topic: quickstart
author: fishah
ms.author: fishah
manager: joncart
ms.workload:
- liveshare
ms.openlocfilehash: 5e485397ff23be0fdab8449fad6237d829775c55
ms.sourcegitcommit: d7f923c1bcd0430b48065ea2c0902b470f530987
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/19/2020
ms.locfileid: "83569532"
---
<!--
Copyright &copy; Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="preview-joining-a-live-share-session-from-the-browser"></a>✨ [Preview] ✨ se připojuje k Live Share relaci z prohlížeče

Všechny Live Share relace spolupráce teď mají možnost připojit se z prohlížeče. To znamená, že host pro vaši relaci už není potřeba instalovat VS Code nebo Visual Studio, aby se mohl připojit k vaší relaci. To je užitečné hlavně pro všechny tyto instance, pokud chcete, aby se někdo rychle dostal do vaší relace, nebo pro studenty, kteří na stolních počítačích často nemají nainstalované klienty pro stolní počítače.


# <a name="how-to-join-a-live-share-session-from-the-browser"></a>Jak připojit relaci Live Share z prohlížeče 

### <a name="1-host-starts-session"></a>1. hostitel: spustí relaci. 
Chcete-li začít, hostitel by měl přejít buď do sady Visual Studio, nebo na VS Code a spustit relaci spolupráce. Když hostitel sdílí složku nebo projekt.

![Animace spuštění relace](https://user-images.githubusercontent.com/51928518/76938928-b814e300-68b4-11ea-923e-cefabd4688c6.gif)

### <a name="2-guest-uses-shared-link-to-join-from-browser"></a>2. Host: používá sdílený odkaz pro připojení z prohlížeče. 
Live Share vygeneruje odkaz spojení, který bude možné sdílet s hostem. Host může nyní pomocí tohoto odkazu přejít na webovou stránku, která nyní poskytuje možnost pokračovat v prohlížeči.

![Animace spojování relací](https://user-images.githubusercontent.com/51928518/76941137-b8af7880-68b8-11ea-8228-41fdf4afd3ef.gif)

### <a name="3-guest-enjoys-full-fidelity-collaboration-experience-from-browser"></a>3. Host: požívá kompletní prostředí pro spolupráci s kvalitou z prohlížeče. 
Jakmile se host připojí k relaci, může na stejné úrovni, jako by se jednalo o spolupráci od klientů pro stolní počítače.

![Animace plné přesnosti](https://user-images.githubusercontent.com/51928518/76942009-40e24d80-68ba-11ea-885c-6eb1069ed550.gif)

<!---
# Frequently asked questions 

##### 1. Is there an environment running in the background, that is hosting my session in the browser?
When you join a Live Share session from the browser, there is no new environment spun up. It is a serverless service. 
##### 2. Do I have to pay for the service of joining from the browser?
Joining from the browser is free, much like all of Live Share.

##### 3. How is this different from Visual Studio Online?
When you join from the browser, you only access the VS Code client from the browser during the session. Once the session ends, all the files and folders along with editor capabilities will close. To use an editor in the browser, backed with your own environment to edit your own files, you must use [Visual Studio Online.](aka.ms/vso)

##### 4. Does this work for all browsers?
Yes. This works on all browsers. 
##### 5. Is there a VS client that I can use in the browser?
We do not have this available yet. 

# Feedback and issues 
This is a preview feature, and we hope to get user feedback to improve the experience. Please fill out any feedback or issues you see on our GitHub repo [here.](https://github.com/MicrosoftDocs/live-share/issues/new?template=bug_report.md)

--->
