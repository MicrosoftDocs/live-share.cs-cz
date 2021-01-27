---
title: Přehled | Microsoft Docs
description: Nové funkce a verze Live Share
ms.custom: ''
ms.reviewer: ''
ms.suite: ''
ms.topic: overview
author: fubaduba
ms.author: fubaduba
ms.workload:
- liveshare
ms.openlocfilehash: 70adacfbb8d5e3b4ca9a7b2652c7c455a977f2f7
ms.sourcegitcommit: 9deed590c0876b732c8eb150a9a23498a8243efc
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/27/2021
ms.locfileid: "98870471"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

## <a name="integrated-chat"></a>Integrovaný chat 
Live Share teď má integrovaný chat pro [Visual Studio Code](..\use\vscode.md) a [Live Share Web.](..\quickstart\browser-join). To znamená, že můžete s partnerskými uzly komunikovat přímo z integrovaného vývojového prostředí (IDE).

>[!TIP]
>Live Share dříve poskytovalo doprovodné rozšíření. To znamenalo, že uživatelé s tímto rozšířením můžou používat chat v rámci Live Share. Toto rozšíření bylo teď odepsáno a všichni uživatelé Live Share v VS Code a webovém klientovi budou mít chatovací službu.

### <a name="common-questions"></a>Časté dotazy

##### <a name="why-am-i-seeing-this-error-message"></a>Proč se mi zobrazuje tato chybová zpráva?

Pokud jste zakázali automatické aktualizace pro rozšíření (včetně Live Share a rozšíření doprovodného chatu Live Share), zobrazí se následující chybové zprávy.

1. Pokud máte hostitele nebo hosta, v případě, že máte nainstalovanou příponu doprovodného chatu Live Share, pokud se zobrazí:

>Aktualizujte prosím `Live Share Chat` doprovodné rozšíření. Nainstalovaná verze již není kompatibilní.

Tato chybová zpráva vyžaduje, abyste v doprovodném chatu Live Share použili nové integrované prostředí chatu.
Navštivte web Marketplace a vyhledejte *chat* a aktualizujte na nejnovější verzi. 

2. Jako host, pokud máte nejnovější verze rozšíření Live Share a pokud vidíte:

>Hostitel této relace spolupráce je aktuálně odpojen od chatu nebo používá verzi _Live Share_ , která tuto funkci nepodporuje. [Další informace] 

Hostitel relace Live Share buď používá sadu Visual Studio, nebo jiné platformy k hostování relace, která ještě nepodporují integrovaný chat Live Share. Může se zobrazit také chybová zpráva 1. uvedená výše.

3. Pokud se zobrazí tato chybová zpráva jako hostitel nebo Host: 

> Osoba, kterou se snažíte kontaktovat, je momentálně nedostupná nebo používá verzi _Live Share_ , která tuto funkci nepodporuje. [Další informace] 

>Služba chat je aktuálně odpojena. Zkuste to prosím za chvíli znovu.

Hostitel relace Live Share buď používá sadu Visual Studio, nebo jiné platformy k hostování relace, která ještě nepodporují integrovaný chat Live Share. Můžou být taky nedostupné hned. Může se zobrazit také chybová zpráva 1. uvedená výše.


**Aby bylo možné používat integrovaný chat, musíte mít automatické aktualizace pro vaše Live Share rozšíření na.** 
