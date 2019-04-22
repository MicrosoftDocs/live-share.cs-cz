---
title: Časté otázky – Visual Studio Live sdílenou složku | Dokumentace Microsoftu
description: Nejčastější dotazy ohledně Visual Studio Live Share.
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
ms.openlocfilehash: 1b68dc90f4bac5e21c04c555ab2d8fc7f59aad55
ms.sourcegitcommit: 1706889dd48377932868a03e88fbd2b4512a3729
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/18/2019
ms.locfileid: "58853596"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="frequently-asked-questions"></a>Nejčastější dotazy

## <a name="what-is-live-share"></a>Co je Live Share?
Rozšíření Live Share vám umožňuje upravovat a ladit v reálném čase společně s ostatními bez ohledu na to, jaké programovací jazyky používáte nebo jaké typy aplikací vytváříte. Umožňuje okamžitě (a bezpečně) sdílet vaše aktuální projekt a pak podle potřeby, sdílet ladicí relace, terminálu instancí, místního hostitele webové aplikace a další! Vývojáři, kteří připojit relací prostředí přijímat všechny jejich kontextu editoru z vašeho prostředí (například jazykových služeb, ladění), což zajistí, že mohou začít produktivně spolupráce okamžitě, aniž by bylo potřeba klonovat jakékoli úložiště nebo instalovat všechny sady SDK.

## <a name="what-are-the-tooling-requirements-for-using-live-share"></a>Jaké jsou požadavky nástroje pro použití Live Share?
[Základní možnosti](#what-are-the-core-capabilities-of-live-share) Live Share jsou plně podporované v těchto nástrojů:

* [Visual Studio 2019](https://visualstudio.microsoft.com/vs/)
* [Visual Studio 2017 (verzi 15.6 +)](https://visualstudio.microsoft.com/vs/older-downloads/)
* [Visual Studio Code](https://code.visualstudio.com/)

Rychle iterovat jsme reagovat na zpětnou vazbu uživatelů. To vyžaduje, abychom mohli využít výhod funkcí v sadě Visual Studio a Visual Studio Code, které jsou pouze být k dispozici ve vydáních jejich příslušné verze preview/insider. Ukážeme, funkcí, které vyžadují novější verze sady Visual Studio nebo VS Code v dokumentaci. Například místní zpět/znovu podpora vyžaduje Visual Studio 2017 15.7 +.

## <a name="what-are-the-core-capabilities-of-live-share"></a>Jaké jsou základní funkce Live Share?
Live Share umožňuje sdílet váš kód s členy svého týmu přes zabezpečené připojení. S Live Share budete moci spolupracovat upravit více souborů v pracovním prostoru a další důležité je ladění aplikace s ostatními členy týmu. Při úpravách společně úprav jsou okamžitě vidět členy vašeho týmu. Během ladění společně sdílejí stejné relace ladění vaší aplikace. To znamená, že a ostatními členy týmu můžete řídit spuštění programu pomocí zarážek a kroků, ale nezávisle na sobě můžete kontrolovat proměnné, Watch, místní hodnoty a REPLs (např. příkazové podokno v sadě Visual Studio).

Sdílené složky za provozu, jako má širokou škálu případů použití: zkoumání chybu společně zobrazující problém, který nebude reprodukovat na počítači někoho jiného řešení návrhu vydá, pár programování, provádění kódování rozhovor, mentorování ostatní členy týmu nebo provádění revize kódu ad-hoc.

## <a name="by-using-live-share-is-my-code-stored-on-a-microsoft-server"></a>Pomocí Live Share je můj kód uložené na serveru Microsoft?
Ne, sdílený kód nachází pouze v počítači vývojáře, kteří iniciované sdílenou složku. Ji není uložená nebo při jejich nahrávání do cloudu žádným způsobem. Místo toho Live Share jednoduše vytvoří zabezpečené připojení mezi vámi a s ostatními členy týmu (což je šifrovaná začátku do konce) a nebude kontrolovat ani neshromažďují žádná data do kódu, který se sdílí.

## <a name="does-this-remote-based-model-work-anywhere-is-it-peer-to-peer"></a>Tento model založený na vzdálené funguje kdekoli? Je to peer-to-peer?
Živé sdílenou složku Jediným požadavkem je, že osoby, která sdílí a jejich programujete mají přístup k Internetu. Azure relay usnadňují zabezpečenou komunikaci mezi členy týmu během relace spolupráci. Váš pracovní prostor (tj. zdrojové soubory) nejsou uložená v cloudu. Je nutné žádné speciální připojení peer-to-peer, i když se jeden může použít ke snížení latence. Zobrazit [Změna režimu připojení](https://aka.ms/vsls-docs/connection-mode) v naší dokumentaci pro další podrobnosti.

## <a name="what-is-shared-during-a-live-share-session"></a>Co je sdílet během relace Live Share?
Živé sdílené složky nepřenese všechny vstupy klávesnici a myš. Komunikuje jenom data potřebná pro každou aktivitu spolupráce na počítače s ostatními členy týmu. Například při sdílení pracovního prostoru je sdílet vaše struktura složky. Když upravíte soubor spolupracovat, obsah tohoto souboru se sdílí. Při ladění spolupracovat, jsou sdíleny ladění akce (například krokování) a stavu (např. zásobník volání a místní hodnoty).

## <a name="when-will-live-share-be-released"></a>Kdy Live Share vydáte?
Sdílené složky za provozu je teď obecně dostupná! Je možné [začít pracovat s Live Share](https://aka.ms/vsls-start) ještě dnes.

## <a name="how-much-will-it-cost"></a>Kolik vás to bude stát?
Jsme usilujeme o podstatné úroveň free služby Visual Studio Live Share vývojáři mohou použít průběžně. Jsme bude se hodnocení Úvod placených úrovní pomocí pokročilých funkcí, jako jsme lépe pochopili požadavky komunity.

## <a name="how-is-my-code-shared-with-other-teammates"></a>Sdílení vlastního kódu s ostatní členové týmu
Pokud používáte Live Share, děláte, kterou právě pracujete dostupné tak, aby ostatními členy týmu k němu přístup přes zabezpečenou cloudovou službu této příkazy Vzdálená úložiště z editoru kódu. Ostatními členy týmu můžete otevřít a upravit soubory bez nutnosti je ukládat v cloudu nebo trvale je uložit v počítači, vaše programujete.

Live Share umožňuje okamžitý přístup k funkcím, jako strom projektu, navigace v kódu a hledání. Umožňuje také členy vašeho týmu mít prospěch z vylepšení editoru, jako je například technologie IntelliSense.

## <a name="what-happens-if-a-user-goes-offline-or-stops-sharing"></a>Co se stane, když uživatel přejde do režimu offline nebo ukončí sdílení?
Vzdálené modelu vyžaduje, vývojář sdílení prostřednictvím Live Share a jejich programujete musí být online, připojený k Internetu. Pokud vaše programujete se pokusí použít Live Share, když jste offline, nemohl připojit k relaci, dokud se znovu online. Kromě toho po zastavení spolupráce (třeba vám zavřete editor, přejít do režimu offline nebo zakázání sdílení), pak další akce nebo přístup k souborům členy vašeho týmu jsou okamžitě zakázat.

## <a name="what-about-screen-sharing"></a>Co o sdílení obrazovky?
Sdílené složky za provozu umožňuje sdílet kód vašeho projektu a jeho kontextu. Znamená to, že vaše programujete můžete snadno přejít do vašeho základu kódu a spolupracovat s vámi své zkušenosti s nástrojem. Editor nebo jiným aplikacím nejsou sdílené nebo zobrazitelné ve vaší programujete a není nutné změnit vašemu stylu práce nebo použít webovou aplikaci.

Živé sdílené složky nenahrazuje sdílení obrazovky, kde můžete chtít zobrazit položku nabídky a diskutovat visual aspekty vaší aplikace nebo vašem editoru. Místo toho máte možnost použít Live Share spolu s konverzace, hlasové, videa a sdílení obrazovky.

## <a name="what-about-other-collaboration-tools"></a>A co jiných nástrojů pro spolupráci?
Živé sdílenou složku jde použít s chatu, zasílání rychlých zpráv nebo technologie e-mailu. Jsme zjistili jsme, že v těchto nástrojích spustí mnoha interakcím spolupráci mezi vývojáři. Ale když diskuse o kódu, jsou často dostat k okamžiku, kde je to ale příliš obtížné popisují potíže s textem, fragmenty kódu nebo jednotlivé soubory – je potřeba další kontext.

Sdílené složky za provozu je možné ke spoustě věcí, jako například: hledání nápovědy na problém, řeší chyby, zkontrolovat pár programování, provádění kódování dotazování nebo provádění ad-hoc před potvrzení změn kódu nebo žádost o přijetí změn.

## <a name="what-about-other-web-editors"></a>Jak ostatní editory web?
Pomocí editoru založeného na webu i členové týmu muset použít stejnou webovou aplikaci zobrazíte spolupráci výhody, které nemusí být jejich primárních, každodenní editoru. Mnohé editory založeného na webu se předpokládá, že jsou vytváření a nasazování do virtuálního počítače často hostované v cloudovém prostředí.

To může být žádoucí, aby mnoho scénářů, vývojáři často chtějí spolupracovat na aplikace, které se nehostují ve virtuálním počítači nebo v cloudu.  S Live Share vám a vaší programujete může využívat možnosti ekosystému nástrojů kromě stejné funkce, které jsou k dispozici v editoru založeného na webu.

Živé sdílenou složku přejde o krok dál a umožňuje sdílet ladicí relaci.  Díky tomu je zvláště užitečná v uvedení ostatní, aby vám problémy, které mohlo dojít pouze v počítači bez změny jejich pracovního postupu vývoje nebo by bylo potřeba změnit návrh aplikace pomohla najít.

## <a name="which-languages-and-platforms-will-be-supported"></a>Jaké jazyky a platformy bude podporována?
Naším cílem je podporovat různé prostředí, jazyků a platforem, ujistěte se, že jsme povolili spolupráce, bez ohledu na typ aplikace, a proto produkt. Zobrazit [jazyka a libovolné platformy podporují](reference/platform-support.md) , kde najdete podrobnosti o tom, co funguje už dnes.

## <a name="how-many-developers-can-join-a-collaboration-session"></a>Jak celá řada vývojářů může připojit k relaci spolupráci?
V tuto chvíli podporujeme 30 souběžných hostech. Kromě toho pro vývojáře, který sdílí ("hostování") projekt. Ve výchozím nastavení jsme povolili až 5 hostů v relaci. 

Pokud chcete povolit zvýšené hosta limit: 
- **VS Code:** Přidejte do settings.json "liveshare.increasedGuestLimit":"true".
- **VS:** Nastavení nástroje > Možnosti > Live Share > Increased hosta omezení na hodnotu "True"

## <a name="what-is-the-roadmap"></a>Co je plán?
Můžete zobrazit sadu známé problémy a položky plán [tady](https://aka.ms/vsls-issues). Pokud chcete pouze požadavky na funkce najdete v tématu, ne všechny problémy, přečtěte si téma [tady](https://aka.ms/vsls-feature-requests). Doporučujeme vám nahoru vote existující položky souboru žádostí o nové funkce a protokolování zpráv o chybách, aby bylo možné Pomozte nám tvar směr produktu v budoucnu.

## <a name="see-also"></a>Viz také:

- [Podpora jazyků a platforem](platform-support.md)
- [Požadavky na připojení pro Live Share](reference/connectivity.md)
- [Funkce zabezpečení Live Share](reference/security.md)
- [Hlavní chyby, žádosti o funkce a omezení](https://aka.ms/vsls-issues)
- [Všechny žádosti o funkce a omezení](https://aka.ms/vsls-feature-requests)

Máte potíže? Podívejte se na článek o [odstraňování potíží](troubleshooting.md) nebo nám [pošlete svůj názor](support.md).
