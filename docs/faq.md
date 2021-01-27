---
title: NEJČASTĚJŠÍ DOTAZY | Microsoft Docs
description: Nejčastější dotazy týkající se Visual Studio Live Share.
ms.custom: ''
ms.date: 05/05/2018
ms.reviewer: ''
ms.suite: ''
ms.topic: reference
author: lostintangent
ms.author: joncart
manager: AmandaSilver
ms.workload:
- liveshare
ms.openlocfilehash: 3da327261766ea0aea7ed167059c864100d25da0
ms.sourcegitcommit: 9deed590c0876b732c8eb150a9a23498a8243efc
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/27/2021
ms.locfileid: "98870485"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="frequently-asked-questions"></a>Nejčastější dotazy

## <a name="what-is-live-share"></a>Co je Live Share?
Rozšíření Live Share vám umožňuje upravovat a ladit v reálném čase společně s ostatními bez ohledu na to, jaké programovací jazyky používáte nebo jaké typy aplikací vytváříte. Umožňuje okamžitě (a bezpečně) sdílet aktuální projekt a pak podle potřeby sdílet relace ladění, instance terminálu, webové aplikace a další věci. Vývojáři, kteří se připojí k vašim relacím, přijmou ze svého prostředí svůj kontext svého editoru (např. jazykové služby, ladění), které zajistí, že budou moct okamžitě začít spolupracovat přímo, aniž by museli klonovat žádné úložiště nebo instalovat sady SDK.

## <a name="what-are-the-tooling-requirements-for-using-live-share"></a>Jaké jsou požadavky nástrojů na použití Live Share?
[Základní funkce](#what-are-the-core-capabilities-of-live-share) Live Share jsou plně podporované v následujících nástrojích:

* [Visual Studio 2019](https://visualstudio.microsoft.com/vs/)
* [Visual Studio 2017 (15.6 +)](https://visualstudio.microsoft.com/vs/older-downloads/)
* [Visual Studio Code](https://code.visualstudio.com/)

Rychle iterovat na zpětnou vazbu od uživatelů. To vyžaduje, abychom využili výhod funkcí v rámci sady Visual Studio a Visual Studio Code, které jsou k dispozici pouze v příslušných verzích Preview a Insider. Určíme, které funkce budou vyžadovat novější verze VS nebo VS Code v dokumentaci. Například místní Podpora funkce zpět/znovu vyžaduje Visual Studio 2017 15.7 +.

## <a name="what-are-the-core-capabilities-of-live-share"></a>Jaké jsou základní funkce Live Share?
Live Share umožňuje sdílet základ kódu se členy týmu prostřednictvím zabezpečeného připojení. Díky Live Share můžete v pracovním prostoru spolupracovat s více soubory a důležitějším laděním aplikace pomocí ostatními týmu. Během souběžného úprav se vaše úpravy okamžitě projeví v ostatními týmu. Během společného ladění sdílíte stejnou relaci ladění aplikace. To znamená, že vy a váš ostatními týmu můžete řídit provádění programu pomocí zarážek a kroků, ale můžete nezávisle kontrolovat proměnné, hodinky, místní a REPLs (například okamžité okno v aplikaci Visual Studio).

Live Share má širokou škálu případů použití, jako je například: zkoumání chyby společně s problémem, který se reprodukci na počítači jiné osoby, řešení problémů s návrhem, párování programování, provádění pohovorů při psaní kódu, poradenství dalších členů týmu nebo provádění revizí ad hoc kódu.

## <a name="by-using-live-share-is-my-code-stored-on-a-microsoft-server"></a>Pomocí Live Share je můj kód uložený na serveru Microsoftu?
Ne, sdílený kód se nachází výhradně v počítači vývojáře, který zahájil sdílení. Neukládá se ani neukládá do cloudu jakýmkoli způsobem. Místo toho Live Share jednoduše navázat zabezpečené připojení mezi vámi a vaším ostatními týmu (zašifrovaný a komplexní) a nekontroluje ani neshromažďuje žádná data v kódu, který je sdílený.

## <a name="does-this-remote-based-model-work-anywhere-is-it-peer-to-peer"></a>Funguje tento model vzdáleného modelu na libovolném místě? Je to peer-to-peer?
Jediným požadavkem Live Share je, že osoba sdílející a jejich společník mají přístup k Internetu. Zabezpečená komunikace mezi členy týmu během relace spolupráce je usnadněna službou Azure Relay. Váš pracovní prostor (tj. zdrojové soubory) není uložený v cloudu. K omezení latence se nevyžaduje žádné zvláštní připojení peer-to-peer. Další podrobnosti najdete v tématu [Změna režimu připojení](https://aka.ms/vsls-docs/connection-mode) v naší dokumentaci.

## <a name="what-is-shared-during-a-live-share-session"></a>Co se sdílí během Live Share relace?
Live Share nepřenáší všechny vstupy klávesnice a myši. Komunikuje jenom data potřebná pro každou aktivitu spolupráce s počítači s ostatními týmu. Když například sdílíte pracovní prostor, vaše struktura složek je sdílená. Při spolupráci s úpravou souboru se obsah tohoto souboru sdílí. Když spolupracujete na spolupráci, sdílí se akce ladění (například krokování) a stav (například zásobník volání a místní).

## <a name="when-will-live-share-be-released"></a>Kdy se Live Share uvolní?
Live Share je teď všeobecně k dispozici! Můžete začít [s Live Share](https://aka.ms/vsls-start) ještě dnes.

## <a name="how-much-will-it-cost"></a>Kolik to bude stát?
Jsme se zavázali k podstatné bezplatné úrovni Visual Studio Live Share, aby se vývojáři mohli průběžně používat. Vyhodnocujeme zavedení placených úrovní s pokročilými funkcemi, protože lépe rozumíte potřebám komunity.

## <a name="how-is-my-code-shared-with-other-teammates"></a>Jak se sdílí můj kód s jinými ostatními týmuy?
Při použití Live Share vytváříte kód, na kterém pracujete tak, aby k němu ostatními týmu mohl přistupovat přes zabezpečenou cloudovou službu, která z vašeho editoru provádí vzdálené příkazy. Vaše ostatními týmu může soubory otevřít a upravit, aniž by je museli ukládat do cloudu, nebo je trvale uložit na počítač s společník.

Live Share umožňuje okamžitý přístup k funkcím, jako jsou strom projektu, navigace v kódu a hledání. Umožňuje také vašemu ostatními týmuu těžit z vylepšení editoru, jako je například IntelliSense.

## <a name="what-happens-if-a-user-goes-offline-or-stops-sharing"></a>Co se stane, když uživatel přejde do režimu offline nebo zastaví sdílení?
Vzdálený model vyžaduje, aby bylo sdílení pro vývojáře prostřednictvím Live Share a jejich společník online, aby bylo možné je připojit. Pokud se vaše společník pokusí použít Live Share, když jste offline, nebude se moct připojit k relaci, dokud nebudete znovu online. Navíc po zastavení spolupráce (třeba zavřít editor, přejít do offline režimu nebo ukončit sdílení), jsou okamžitě zakázané další akce nebo přístup k souborům v ostatními týmu.

## <a name="what-about-screen-sharing"></a>Co je sdílení obrazovky?
Live Share umožňuje sdílet kód projektu a jeho kontext. To znamená, že váš společník může snadno přejít do základu kódu a pracovat s vámi pomocí jejich známého nástroje. Váš Editor nebo jiné aplikace nejsou sdíleny nebo zobrazitelny vaším společník a nemusíte měnit IT manažery ani používat webovou aplikaci.

Live Share nenahrazuje sdílení obrazovky, kde můžete chtít zobrazit položku nabídky nebo diskutovat o vizuálních aspektech vaší aplikace nebo editoru. Místo toho máte možnost použít Live Share společně s funkcí chat, Voice, video a sdílení obrazovky.

## <a name="what-about-other-collaboration-tools"></a>Co se týká dalších nástrojů pro spolupráci?
Live Share lze použít s technologiemi chat, rychlých zpráv nebo e-mailů. Zjistili jsme, že v těchto nástrojích začíná spousta spolupráce mezi vývojáři. Nicméně pokud je diskuze o kódu, často se dostanete k bodu, kde je jednoduše příliš těžko vysvětlovat problém s textem, fragmenty kódu nebo s jedním soubory. je třeba zadat více kontextu.

Live Share lze použít pro mnoho věcí, jako je například vyhledávání pomocníka při potížích, řešení chyby, spárování programování, vedení pohovoru s psaním kódu nebo provedení ad-hoc kontroly před potvrzením kódu nebo vyžádáním žádosti o přijetí změn.

## <a name="what-about-other-web-editors"></a>Co jsou další webové editory?
Díky webovým editorům musí obě ostatními týmu používat stejnou webovou aplikaci k získání výhod pro spolupráci, které nemusí být jejich hlavním, každodenním editorem. Mnoho webových editorů předpokládá, že sestavíte a nasazujete do virtuálního počítače, který je často hostován v cloudovém prostředí.

I když to může být žádoucí pro mnoho scénářů, vývojáři často chtějí spolupracovat na aplikacích, které nejsou hostované na virtuálním počítači nebo v cloudu.  Díky Live Share můžete vy a váš společník využívat možnosti ekosystému nástrojů kromě stejných možností, které jsou k dispozici v editorech založeném na webu.

Live Share ještě další krok a umožní vám sdílet relaci ladění.  To je užitečné hlavně při zařazování dalších, které vám pomůžou sledovat problémy, ke kterým dochází jenom na vašem počítači, aniž by došlo ke změně vývojového pracovního postupu nebo k tomu, aby se návrh aplikace změnil.

## <a name="which-languages-and-platforms-will-be-supported"></a>Které jazyky a platformy budou podporovány?
Naším cílem je podporovat nejrůznější jazyky a platformy, aby bylo zajištěno, že můžeme povolit bohatou spolupráci bez ohledu na to, jaký typ aplikace se vyvíjí. Podrobnosti o tom, co dnes funguje, najdete v článku [Podpora jazyků a platforem](reference/platform-support.md) .

## <a name="how-many-developers-can-join-a-collaboration-session"></a>Kolik vývojářů se může připojit k relaci spolupráce?
V současné době podporujeme 30 souběžných hostů, kromě vývojářů, kteří sdílejí ("hostování") jejich projektu. 

## <a name="what-is-the-roadmap"></a>Co je plán?
Můžete zobrazit sadu známých problémů [a položky plánu](https://aka.ms/vsls-issues). Pokud byste chtěli zobrazit jenom žádosti o funkce místo všech problémů, přečtěte si [tady](https://aka.ms/vsls-feature-requests). Doporučujeme vám, abyste si vyžádali existující položky, soubory nových funkcí a protokoly chyb, aby bylo možné pořídit směr pohybu produktu směrem k.

## <a name="see-also"></a>Viz také

- [Podpora jazyků a platforem](platform-support.md)
- [Požadavky na připojení pro Live Share](reference/connectivity.md)
- [Funkce zabezpečení Live Share](reference/security.md)
- [Všechny hlavní chyby, žádosti o funkce a omezení](https://aka.ms/vsls-issues)
- [Všechny požadavky a omezení funkcí](https://aka.ms/vsls-feature-requests)

Máte potíže? Podívejte se na článek o [odstraňování potíží](troubleshooting.md) nebo nám [pošlete svůj názor](support.md).
