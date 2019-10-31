---
title: Visual Studio Live Share pro přítomnost | Microsoft Docs
description: Informace o službě stavu pro kontakty pro Visual Studio Live Share.
ms.custom: ''
ms.date: 10/08/2019
ms.reviewer: ''
ms.suite: ''
ms.topic: reference
author: fubaduba
ms.author: fubaduba
manager: JonathanCarter
ms.workload:
- liveshare
ms.openlocfilehash: b95e5f837d044b2b069f73478da40461268bdf3d
ms.sourcegitcommit: c6ef4e5a9aec4f682718819c58efeab599e2781b
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/30/2019
ms.locfileid: "73169997"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="contacts-in-live-share"></a>Kontakty v Live Share 

Takže jste používali Live Share a všimnete si, že odesílání odkazů prostřednictvím externí aplikace (například chat nebo e-mail) může být opravdu rychlé? Víme, že pokud chceme podpořit spolupráci, je potřeba, abyste měli k dispozici nejmenší možný objem tření. Proto Live Share nyní má **Kontakty** se **stavem** .

>Kontakty se automaticky povolí pro všechny verze **Live Share v 1.0.950** a vyšší.

Kontakty se zobrazí v okně Live Share jako samostatné podokno, jak je vidět na následujícím obrázku: 

![Složce](../media/vscode-contacts-intro.png)

<em>Zobrazení podokna kontaktů v okně Live Share</em>
## <a name="who-shows-up-in-my-contacts"></a>Kdo zobrazuje kontakty?

Podokno kontaktů obsahuje dva typy kontaktů, které při práci podporují přirozené pracovní postupy pro vývojáře.
### <a name="1-recent-contacts"></a>1. poslední kontakty  
 Jedná se o vývojáře, na kterých jste předtím spolupracovali pomocí Live Share. V praxi většina vývojářů často spolupracuje se stejnými lidmi, a proto poslední seznam umožňuje pracovat s týmem, třídou a dalšími možnostmi opakování práce.
### <a name="2-suggested-contacts"></a>2. navrhované kontakty
Jedná se o vývojáře, kteří během posledních 30 dnů přispěli k vašemu aktuálně otevřenému projektu. V praxi se jedná o lidé, se kterým pravděpodobně budete chtít spolupracovat, a proto je doporučujeme, aby bylo snazší začít.

## <a name="direct-user-invitations"></a>Pozvání přímých uživatelů 
Všechny vaše kontakty lze pozvat přímo do relace Live Share v editoru. Obdrží informační zprávu, která jim poskytne možnost připojit se k relaci, nebo ne. Tím se zcela odstraní potřeba adresy URL relací Exchange.
![DirectInvitationVSCode](https://user-images.githubusercontent.com/51928518/66443914-e59c5d00-e9f5-11e9-957a-b1a92949d660.gif)
<em>Live Shareho hostitele (vlevo), který přímo zve partnerský uzel (vpravo) do relace</em> .

## <a name="how-does-status-for-contacts-work"></a>Jak stav kontaktů funguje?
Když se vývojáři přihlásí pomocí Live Share, **jejich stav dostupnosti se publikuje do jejich partnerských uzlů.** V důsledku toho vidíte, že je někdo v týmu online, a pak hned začít spolupracovat s nimi pomocí přímého pozvání, jak vidíte výše.
Váš stav lze nastavit přímo v editoru, takže můžete k vašemu týmu signalizovat dostupnost, aniž byste museli přepnout kontext. V tuto chvíli má Live Share kontaktů 4 stavy:

**1. k dispozici:** váš výchozí stav bude `Available`, pokud máte rozšíření Live Share a aktivně používáte editor, ale nejste v relaci.

**2. Nerušit:** stav je nastaven na `Do not disturb`, pokud aktuálně používáte aktivní relaci Live Share a všechna oznámení pozvánky jsou potlačena.

**3. pryč:** po 5 minutách nečinnosti se váš stav automaticky přepne na `Away`.

**4. offline:** po delší dobu budete offline, nebo pokud se rozhodnete odhlásit [stav sdílení](##ManagingPresence) .


## Správa stavu<a name="ManagingPresence"> </a> kontaktů a sdílení

Pokud chcete tuto funkci odhlásit, můžete to provést dvěma způsoby.
1. Nastavení stavu můžete zakázat volbou `offline`. Jakmile je tato možnosti zakázaná, bude se vám pořád zobrazovat stav ostatních a zvát, ale váš stav nebude publikovaný a ostatní vás nemůžou přímo pozvat.
Kliknutím na kruhový stav, který se zobrazí v následující rozevírací nabídce, můžete zvolit offline:

![dropdownstatus](../media/vscode-presence-opt-out.png)
<em>znázorňující vyřazení stavů stavu</em>

2. Můžete otevřít `user settings` a přejít na *rozšíření > Visual Studio Live Share > Live Share: přítomnost* a zakázat přítomnost služby. Jakmile je tato možnosti zakázaná, bude se vám pořád zobrazovat stav ostatních a zvát, ale váš stav nebude publikovaný a ostatní vás nemůžou přímo pozvat.

![presencesettings](../media/vscode-presence-setting.png)

## <a name="faqs"></a>Nejčastější dotazy 

###### <a name="1-will-i-be-automatically-opting-into-sharing-status-when-i-use-live-share-v10950-and-above"></a>1. při použití Live Share v 1.0.950 a výše se automaticky zaměří na stav sdílení?

Při prvním výskytu kontaktů se vám zobrazí oznámení se zprávou a možností, jak se odhlásit ze stavu sdílení. Potom budete svůj stav automaticky sdílet s vašimi kontakty, pokud se nerozhodnete, jak je uvedeno výše.

###### <a name="2-can-i-add-my-own-contacts"></a>2. můžu přidat vlastní kontakty?

V současné době služba kontaktů automaticky detekuje tyto spolupracovníky, u kterých často sdílíte kód s nebo pracujete, a neposkytuje možnost přidat vlastní kontakty. 


>Je možné, že budete moct ručně přidat kontakty, které budou užitečné? Požádejte nás o stanovení priorit tím, že na toto [místo](https://github.com/MicrosoftDocs/live-share/issues/new?template=feature_request.md) otevřete žádost o funkci GitHubu.
 

 