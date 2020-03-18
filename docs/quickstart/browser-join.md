---
title: Připojení z prohlížeče – Visual Studio Live Share | Microsoft Docs
description: Představení připojení z prohlížeče p
ms.date: 03/18/2020
ms.reviewer: ''
ms.suite: ''
ms.topic: quickstart
author: fishah
ms.author: fishah
manager: joncart
ms.workload:
- liveshare
ms.openlocfilehash: 741292a3df8b86a8f7a9484875b352ebe6e8ec10
ms.sourcegitcommit: 382f069abbd81ed258d497a974b30379be36b4f0
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "79510623"
---
<!--
Copyright &copy; Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="preview-joining-a-live-share-session-from-the-browser"></a>✨ [Preview] ✨ se připojuje k Live Share relaci z prohlížeče

Všechny Live Share relace spolupráce teď mají možnost připojit se v prohlížeči. To znamená, že host pro vaši relaci už není potřeba instalovat VS Code nebo Visual Studio, aby se mohl připojit k vaší relaci. To je užitečné hlavně pro všechny tyto instance, pokud chcete, aby se někdo rychle dostal do vaší relace, nebo pro studenty, kteří na stolních počítačích často nemají nainstalované klienty pro stolní počítače.

> [!TIP]
> V části Nejčastější dotazy níže najdete nejčastější dotazy týkající se připojení z prohlížeče.

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
# <a name="frequently-asked-questions"></a>Nejčastější dotazy 

##### <a name="1-is-there-an-environment-running-in-the-background-that-is-hosting-my-session-in-the-browser"></a>1. je prostředí spuštěné na pozadí, které hostuje moji relaci v prohlížeči?
Když se připojíte k Live Share relaci z prohlížeče, nedošlo k žádnému novému pronově prostředí. Jedná se o službu bez serveru. 
##### <a name="2-do-i-have-to-pay-for-the-service-of-joining-from-the-browser"></a>2. musím platit za službu připojení z prohlížeče?
Spojení z prohlížeče je zdarma, podobně jako u všech Live Share.

##### <a name="3-how-is-this-different-from-visual-studio-online"></a>3. jak se to liší od služby Visual Studio Online?
Když se připojíte z prohlížeče, získáte přístup k klientovi VS Code jenom z prohlížeče během relace. Po ukončení relace budou všechny soubory a složky společně s možnostmi editoru zavřeny. Pokud chcete použít Editor v prohlížeči, který je zálohovaný s vlastním prostředím pro úpravy vlastních souborů, musíte použít [Visual Studio Online.](aka.ms/vso)

##### <a name="4-does-this-work-for-all-browsers"></a>4. udělá tuto práci pro všechny prohlížeče?
Ano. To funguje na všech prohlížečích. 
##### <a name="5-is-there-a-vs-client-that-i-can-use-in-the-browser"></a>5. je to klient VS, který můžu v prohlížeči použít?
Ještě nemáte k dispozici. 

# <a name="feedback-and-issues"></a>Názory a problémy 
Toto je funkce ve verzi Preview a doufáme, že získáme zpětnou vazbu od uživatele, abychom mohli vylepšit prostředí. Vyplňte prosím jakékoli názory nebo problémy, které vidíte v našem úložišti GitHub [.](https://github.com/MicrosoftDocs/live-share/issues/new?template=bug_report.md)