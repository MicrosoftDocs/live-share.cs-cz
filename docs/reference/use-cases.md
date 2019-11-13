---
title: Běžné případy použití – Visual Studio Live Share | Microsoft Docs
description: Přehled případů použití, které vývojáři běžně využívají Visual Studio Live Share pro.
ms.custom: ''
ms.date: 05/21/2018
ms.reviewer: ''
ms.suite: ''
ms.topic: reference
author: lostintangent
ms.author: joncart
manager: AmandaSilver
ms.workload:
- liveshare
ms.openlocfilehash: 0d328ad39b35ae1c6338825848857342765418d9
ms.sourcegitcommit: 3a1b22eac528b0f6a241f9fec7ec20264db24cfe
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/13/2019
ms.locfileid: "74019799"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="common-use-cases"></a>Běžné případy použití

Primárním cílem Visual Studio Live Share je umožnit vývojářům vzájemnou spolupráci, aniž byste museli zavádět jakékoli stanovisko k tomu, kdy a jak postupovat (např. který komunikační nástroj použít, "pravé" softwarové metodologie nebo pracovní postup SCM. Tímto způsobem můžou vaše nástroje podporovat interakce, ke kterým dochází **přirozeně**, a **podle potřeby** , ale způsobem **, který si** přeje, aby fungovaly.

V tomto dokumentu se dozvíte o některých případech použití, které Visual Studio Live Share už používá, a popisuje, jak dobře je teď podporujeme, a způsoby, jak je lépe optimalizovat (na základě zpětné vazby!). Pokud používáte Live Share pro něco, co ještě není popsáno níže, nebo si myslíte, že můžeme dělat lepší podporu konkrétního případu použití, [dejte nám prosím jistotu](https://github.com/MicrosoftDocs/live-share/issues/new).

- [Rychlá pomoc](#quick-assistance)
    - [Hodiny kanceláře](#office-hours)
- [Párování programování](#pair-programming)
    - [Programování Mob](#mob-programming)
    - [Kódování soutěží/napadení – A – Thons](#coding-competitions--hack-a-thons)
    - [Projekty školních skupin](#school-group-projects)
    - [Streamování pro vývojáře](#developer-streaming)
    - [Vytváření prototypů/zahájení projektu](#prototyping--project-inception)
- [Interaktivní vzdělávání](#interactive-education)
    - [Partnerský poradce/připojování](#peer-mentoring--onboarding)
    - [Penalty pro Team Brown](#team-brown-bags)
    - [Přednášky učebny](#classroom-lectures)
- [Revize kódu](#code-reviews)
- [Technické rozhovory](#technical-interviews)

## <a name="quick-assistance"></a>Rychlá pomoc

Když narazíte na problém (například při pokusu o vyřešení chyby, nastavením prostředí), můžete použít Visual Studio Live Share k okamžitému vyhledání pomoci od jiného partnera. V mnoha případech není okamžitě jasné, jaký kontext má osoba poskytující podporu, a proto Live Share pomáhá zjednodušit poskytnutí přístupu k celému projektu a pokud je to potřeba, přírůstkové sdílení dalších (např. místní server, jen pro čtení). terminál). Není nutné odesílat fragmenty kódu ani chybové zprávy zpět.

Vzhledem k tomu, že Live Share umožňuje sdílet aktivní relaci ladění, aniž by to vyžadovalo "hostů" k instalaci některého z nezbytných sad SDK pro platformy (např. Node. js, přejít, .NET Core) nebo rozšíření nástrojů, vám může usnadnit získání řešení rychleji a zabránit tomu, že ne reprodukci v mém počítači "situace. Live Share vám umožňuje sdílet stav ladění s ostatními, pro libovolný programovací jazyk nebo běhové prostředí (např. Kubernetes, reagovat na nativní aplikaci), a nezávisle na tom, co potřebujete s tím pomáhat, můžete také sdílet!

### <a name="office-hours"></a>Hodiny kanceláře

Mnohé firmy a vzdělávací instituce (například školy, Online školicí kurzy) poskytují podporu svým zákazníkům/zaměstnancům/studentům v předem stanovených časech a obvykle četnosti opakování (například každý pátek od 3-5./odp.). Tímto způsobem jsou "hodiny v kanceláři" jednoduše naplánovanou podobu "Rychlá pomoc", a to na rozdíl od toho, že je celá ad-hoc. Live Share usnadňuje rychlé získání nápovědy, protože odborník na poskytnutí nápovědy se může okamžitě připojit k relaci spolupráce a odpovědět na vaše otázky, aniž by museli nastavit počítač vůbec.

## <a name="pair-programming"></a>Párování programování

Jedním z nejčastěji používaných scénářů pro Visual Studio Live Share je "párové programování": dva nebo více vývojářů, spolupracuje na sdílené úloze, a to s cílem znalosti o sdílení, zvýšením soudržnosti týmu a potenciálně i s kvalitou produktu. Přesné sečtení a chování páru programování se může výrazně lišit mezi týmy a situaceou v závislosti na tom, které z těchto možností (mimo jiné):

1. Rozsah "úkolu", na kterém se spolupracuje (např. chyba, uživatelský scénář)

1. Očekávaná doba trvání relace spolupráce (například dvě minuty, hodina, celý čas, jednou za týden, TBD)

1. Počet zúčastněných lidí (například dva, celý tým)

1. Role každého účastníka (např. "ovladač", pozorovatelka/kontrolora, odborník na danou problematiku)

1. Blízkost účastníků (např. společně umístěného na celém světě)

Live Share byla navržena tak, aby se nezávislá ke všem uvedeným obavám a místo toho se snaží podporovat párové programování, které je zcela "příležitostné" a zaměřené na vaši situaci. Na rozdíl od dvou vývojářů, kteří sdílejí jednu klávesnici a obrazovku, Live Share umožňuje vytvořit dvojici programování, která vývojářům umožní pracovat na sdíleném cíli, aniž by museli odebírat jejich individuální autonomii nebo preference prostředí. Můžete pracovat nezávisle nebo dohromady a umožnit tak každému účastníkovi přenášet svůj vlastní myšlenkový proces do spolupráce.

Chcete-li tento případ použití přerušit ještě dále, následující položky představuje formy páru programování, které jsme zjistili lidé pomocí Live Share pro:

### <a name="mob-programming"></a>Programování Mob

[Programování Mob](https://en.wikipedia.org/wiki/Mob_programming) (nebo programování v Swarm) je v podstatě spárováno s programováním, ale s více než dvěma lidmi. Proto se všechny výhody Live Share pro párové programování použijí také stejně. Kromě toho některé týmy dělají "swarming" podle potřeby (například tým rallying na základě cvičení), a to na rozdíl od plného času.

V současné době Live Share podporuje až 30 hostů v rámci relace.
> [!TIP]
> Povolení 30 hostů v relaci:
> - **Vs Code:** přidejte "LiveShare. increasedGuestLimit": "true" do Settings. JSON
> - **Vs:** Nastavení nástrojů > možností > Live Share > zvýšil limit počtu hostů na hodnotu "true". 

### <a name="coding-competitions--hack-a-thons"></a>Kódování soutěží/napadení – A – Thons

Kódování soutěží a napadení – a – thons jsou efektivní krátkodobé, proměnlivé variace Mob programování. Členové týmu a jejich stávající role jsou také potenciálně dynamické. Vzhledem k tomu, že tento případ použití je obvykle také časově citlivý, je schopnost spolupracovat v reálném čase, aniž by bylo nutné přijmout zcela nový nástroj a možnost společné spolupráce, aniž by byla omezena na jednu obrazovku nebo klávesnici, může při rostoucím způsobu přicházet k protokolu. rychlostí.

Vzhledem k tomu, že účastníci v tomto prostředí nemusí vždy plně "důvěřovat", můžete z relace kdykoli odebrat (a zablokovat) hosta. To poskytuje "hostitelé" s úplnou kontrolou nad jejich prostředím.

### <a name="school-group-projects"></a>Projekty školních skupin

Seskupení projektů končí hledáním hodně, jako je Mob programování, kde více studentů spolupracuje, a může plynule přecházet mezi zaměřením na jednu úlohu nebo souběžně pracovat na samostatných úlohách. Místo pouhého spoléhání na správu verzí, aby spolupracuje asynchronně, můžou použít Live Share k vzájemné spolupráci v reálném čase, což může přispět k tomu, aby sociální a vzdělávací výhody fungovaly ve skupině.

### <a name="developer-streaming"></a>Streamování pro vývojáře

Streamování pro vývojáře (přes Twitch nebo mixer) se stává přesvědčivou novou formou vzdělávání. I když Live Share nezpůsobí nahrazení svých vysílacích platforem (i když jste si vyzkoušeli žádost!), poskytuje hostiteli způsob, jak spárovat program s jedním nebo více hostů a potom streamovat tuto interakci. Díky tomu mohou čtenáři získat další informace o přirozené interakci a myšlenkných procesech dvou nebo více vývojářů, kteří by dokonce mohli spolupracovat v zcela samostatném operačním systému a v prostředí s více procesory.

### <a name="prototyping--project-inception"></a>Vytváření prototypů/zahájení projektu

Když tým spustí nový projekt nebo mikroslužbu nebo vytvoří prototypy nebo spiking novou funkci, může být často užitečný k vzájemné spolupráci, aby bylo možné rychle začít a prozkoumat nové nápady. Vzhledem k tomu, že nově vydaný základ kódu ještě nemusí být uložen do sdíleného úložiště, Live Share umožňuje všem zapojit se do iteračního procesu bez ohledu na to, jestli jsou ve stejné kanceláři nebo ne.

## <a name="interactive-education"></a>Interaktivní vzdělávání

Obecně řečeno Live Share snaží pomáhat vývojářům při sdílení zkušeností mezi jejich týmem. Vzdělávání je základní případ použití pro Live Share a podporuje to zejména tím, že každému účastníkovi umožní pracovat s tímto základem kódu, a to na rozdíl od pouhého sledování obrazovky. Všichni se učí v Subtlety různých způsobech, a díky tomu poskytují nezávislost studentům, které se dají využít, a to bez nutnosti vzít v úvahu své možnosti prozkoumat jejich vlastní myšlenky.

### <a name="peer-mentoring--onboarding"></a>Partnerský poradce/připojování

Když zadáváte vývojáře k novému základu kódu, oblasti funkcí, technologii, atd. můžete použít Live Share k jeho procházení prostřednictvím projektu (pomocí `Follow Mode`), takže můžou sledovat společně s vámi, ale z vlastního osobního rozhraní IDE. Vzhledem k tomu, že Live Share umožňuje hostům nezávisle na projektu (například otevření souboru, provádění `Peek Definition`), může postupovat podle potřeby, ale také provádět rychlé průzkumy podle potřeby (například "Hmm", co tato funkce dělá? ").

### <a name="team-brown-bags"></a>Penalty pro Team Brown

Týmové hnědé sáčky jsou efektivní jako partnerského přihlašování, ale prezentují se celému týmu a můžou se lépe soustředit na socializing všeobecně užitečnou znalost, a to na rozdíl od podpory podpory a/nebo pomoci s konkrétním úkolem.

### <a name="classroom-lectures"></a>Přednášky učebny

Když instruktori učební lekce, můžou použít Live Share ke sdílení projektu s studenty místo pouhého zobrazení obrazovky. To umožňuje, aby celá třída následovala s učitelem a současně dokázala pracovat s projektem sami. Kromě toho učitel může požádat jednotlivé studenty, aby pomohli řešit určitou část lekce (například metodu, kterou bychom volali? "), která může pomoct v sociálních aspektech třídy, aniž by se museli zabývat na přední straně místnosti. nebo dokonce fyzicky přítomná ve stejné místnosti (např. online kurzy).

Aby bylo možné pomoci v nastavení učebny, Live Share umožňuje sdílení v režimu jen pro čtení. Instruktoři můžou použít režim jen pro čtení, který jim umožní sdílet své projekty s studenty, aniž by museli dělat starosti s zbytečnými nebo náhodnými úpravami.

Kromě toho Live Share podpora umožňuje až 30 hostům připojit se do relace spolupráce. Tímto způsobem mohou instruktori zobrazit celou třídu do relace a zobrazit kód společně.

Povolení této funkce:

- **Vs Code:** Přidejte "LiveShare. increasedGuestLimit": "true" do Settings. JSON.
- **Vs:** Nastavení nástrojů > možností > Live Share > zvýšil limit počtu hostů na hodnotu "true".

Aby bylo možné plně optimalizovat Live Share pro tento scénář, musíme zjednodušit způsob, jakým jsou iniciované relace ([#422](https://github.com/MicrosoftDocs/live-share/issues/422)).

## <a name="code-reviews"></a>Revize kódu

PR představují účinný způsob spolupráce s ostatními, ale obvykle představuje dokončení úlohy (s výjimkou "nedokončená výroba" PR) a přání k jejich sloučení v. Zpětnou vazbu, která je uvedena v žádosti o přijetí změn, je možné snadno předávat dříve, takže týmy můžou snadno a nepřetržitě vyhledávat rady od jejich partnerských uzlů, a to na rozdíl od čekání, dokud je úloha nedokončila.

Vzhledem k tomu, že Live Share umožňuje okamžitě sdílet váš projekt s ostatními, dá se použít k povolení "neformálních"/ad-hoc revizí kódu, kde se nedotazuje na nápovědu, stačí jenom vyhledat vstup, abyste zajistili, že váš směr nebo přístup se bude zarovnávat s ostatními. To může potenciálně pomoci s dalším PR kompletním rychlejším a konečně pomáhá Socialize znalosti v rámci týmu.

Vzhledem k tomu, že Live Share umožňuje sdílet libovolný adresář, můžete ho použít k provádění revizí kódu, i když aktuálně nepoužíváte správu verzí (i když byste to měli!), nebo pokud váš tým nepoužívá PR (např. vývoj na základě šachty

Live Share aktuálně nesdílí rozdílové správy zdrojového kódu, což je kritická část kontextu při použití pro revize kódu. To je v našem plánu a kdykoli se vám na ni povede žádná zpětná vazba, ([hlasujte 👍 tady](https://github.com/MicrosoftDocs/live-share/issues/36)).

## <a name="technical-interviews"></a>Technické rozhovory

Při prohlížení kandidátů na pozici pro vývojáře může být často užitečné jít mimo diskuze v programu Tabule a místo toho sledovat problémy s kódováním z vlastního integrovaného vývojového prostředí (zejména v případě, že váš tým nebo organizace má "standardizované" prostředí pro nástroj, který Chcete je vidět, jak je používat). To nejen přináší výhody práce způsobem, který je potenciálně přirozenější (většina vývojářů nekóduje kód na tabulích), ale také poskytuje okamžitou zpětnou vazbu nebo pomoc při práci (například chyby sestavení, IntelliSense). V mnoha případech je důležitější pochopit postup, který je kandidátný na kandidáta, a to na rozdíl od jejich schopností nepamatují přesná syntaxe nebo názvy rozhraní API. Tímto způsobem Live Share poskytuje prostředí, které je podobné jako relace programování v relaci, ale umožňuje, aby účastník byl ve svém vlastním prostředí (včetně nastavení operačního systému, jako je usnadnění přístupu), a pracoval stejně jako i pro místní nebo vzdálené rozhovory.

Kromě toho je vývoj v reálném světě více než pouhým psaním kódu. Vzhledem k tomu, že Live Share podporuje také sdílené ladění, úlohy a terminály, umožňuje spolupracovníkům sledovat kandidáty při diagnostice problému a poskytnout jim vhodné nástroje potřebné k jejich vyřešení (např. ladění, spuštění testů). Vzhledem k tomu, že je všechny kontexty vzdálené z počítače hostitele, můžou kandidáti rychle přejít do prostředí pro rozhovor, aniž by museli nastavit počítač (po instalaci Live Share). Týmy pak můžou udržovat úložiště sdílených vzájemně se používaných aplikací (nebo použít svůj skutečný základ kódu produktu), který by se mohl klonovat a sdílet s kandidáty, protože jednoduše jim pošle adresu URL relace před každým pohovorem.

## <a name="see-also"></a>Viz také:

- [Podpora jazyků a platforem](../reference/platform-support.md)
- [Požadavky na připojení pro Live Share](../reference/connectivity.md)
- [Funkce zabezpečení Live Share](../reference/security.md)
- [Všechny hlavní chyby, žádosti o funkce a omezení](https://aka.ms/vsls-issues)
- [Všechny požadavky a omezení funkcí](https://aka.ms/vsls-feature-requests)

Máte potíže? Podívejte se na článek o [odstraňování potíží](../troubleshooting.md) nebo nám [pošlete svůj názor](../support.md).
