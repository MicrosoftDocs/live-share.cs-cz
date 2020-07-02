---
title: Přehled – Visual Studio Live Share | Microsoft Docs
description: Nové funkce a verze Live Share
ms.custom: ''
ms.reviewer: ''
ms.suite: ''
ms.topic: overview
author: fubaduba
ms.author: fubaduba
ms.workload:
- liveshare
ms.openlocfilehash: 55425a7d57775a4e042e87b8dceb86532e1b966a
ms.sourcegitcommit: 211b17e49e7343786bd6859b65444cedd5e24958
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/01/2020
ms.locfileid: "85796060"
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

>Služba chat je aktuálně odpojena.Zkuste to prosím za chvíli znovu.

Hostitel relace Live Share buď používá sadu Visual Studio, nebo jiné platformy k hostování relace, která ještě nepodporují integrovaný chat Live Share. Můžou být taky nedostupné hned. Může se zobrazit také chybová zpráva 1. uvedená výše.


**Aby bylo možné používat integrovaný chat, musíte mít automatické aktualizace pro vaše Live Share rozšíření na.** 
