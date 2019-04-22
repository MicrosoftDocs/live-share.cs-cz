---
title: Běžné případy použití – Visual Studio Live sdílenou složku | Dokumentace Microsoftu
description: Přehled případy použití, které Visual Studio Live Share pro běžně využívají vývojáři.
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
ms.openlocfilehash: 1b6ecafc933c6521f6c21ec0dcd38c25e889a0e2
ms.sourcegitcommit: 1706889dd48377932868a03e88fbd2b4512a3729
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/18/2019
ms.locfileid: "58853570"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="common-use-cases"></a>Běžné případy použití

Je hlavním cílem Visual Studio Live Share umožňuje vývojářům snadněji, spolupracovat s kolegy bez vnášení žádné stanovisko o kdy a jak to udělat (třeba který komunikační nástroj použít, "vpravo" softwaru metodologie nebo správce řízení služeb pracovního postupu). Tímto způsobem své nástroje podporují interakce **přirozeně**a stejně jako **často** podle potřeby, ale způsobem, který **pozdravem** jak již raději pracujete.

Tento dokument zvýrazní některé používají případy, že se už používá pro Visual Studio Live Share a popisuje, jak dobře aktuálně podporujeme a způsoby, máme v plánu je Optimalizujte další (na základě zpětné vazby!). Pokud používáte Live Share k něčemu, pro které neplatí již níže, nebo si myslíte, že můžeme udělat lépe pro podporu prosím případ použití konkrétní [dejte nám vědět](https://github.com/MicrosoftDocs/live-share/issues/new).

- [Rychlá pomoc](#quick-assistance)
    - [Hodiny Office](#office-hours)
- [Pár programování](#pair-programming)
    - [Programování MOB](#mob-programming)
    - [Kódování soutěže / Hack-A-Thons](#coding-competitions--hack-a-thons)
    - [Projekty skupiny školy](#school-group-projects)
    - [Pro vývojáře datových proudů](#developer-streaming)
    - [Vytváření prototypů / Project zahájení](#prototyping--project-inception)
- [Interaktivní vzdělávání](#interactive-education)
    - [Peer Mentorování / registrace](#peer-mentoring--onboarding)
    - [Týmu Hnědý kontejnery objektů a dat](#team-brown-bags)
    - [Přednášky učebny](#classroom-lectures)
- [Revize kódu](#code-reviews)
- [Technické rozhovory](#technical-interviews)

## <a name="quick-assistance"></a>Rychlá pomoc

Pokud narazíte na problém (například pokusu o přeložení chybu, nastavením vašeho prostředí), můžete použít Visual Studio Live Share okamžitě usilovat o pomoc od jiného partnera. V mnoha případech není okamžitě vymazat kontext osoba poskytnutí nápovědy, bude nutné, a proto Live Share umožňuje tak snadno a zajistit tak přístup do celého projektu, a pokud jako potřebné postupně sdílet informace (například místní server, jen pro čtení terminál). Není nutné odesílat fragmenty kódu a/nebo chybové zprávy a zpět!

Kromě toho Live Share umožňuje sdílet aktivní ladicí relace, aniž by "Guest" nainstalujte potřebné platformy sady SDK (například Node.js, Go, .NET Core) nebo nástroje rozšíření, může vám pomoct získat řešení rychleji a zabránit "není situace reprodukovat na mém počítači". Živé sdílené složky umožňuje sdílet s ostatními, stav ladění, pro žádné programovací jazyk nebo modul runtime prostředí (například Kubernetes, React Native app) a to bez ohledu na to že co budete potřebovat pomoc s, můžete ho sdílet!

### <a name="office-hours"></a>Hodiny Office

Mnoha firmám a vzdělávacím institucím (např. školy, online kurzy) poskytují podporu pro jejich zákazníky/zaměstnancům a studentům, kteří jsou předem určit dobu a obvykle na frekvenci opakování (například každý pátek ze 3 – 17: 00). Tímto způsobem jsou "office hours" jednoduše naplánované formou "rychlá pomoc", na rozdíl od se zcela ad-hoc. Živé sdílenou složku usnadňuje rychlé, získejte pomoc od "odbornou" poskytující pomoc může okamžitě připojit k relaci spolupráci a zodpovědět vaše otázky, aniž by bylo potřeba nastavit jejich počítač vůbec.

## <a name="pair-programming"></a>Pár programování

Jedním z nejčastěji používaných scénáře pro Visual Studio Live Share je "pár programování": dva nebo více vývojářů, spolupracují na sdílených úloh s cílem sdílení znalostí, zvýšení týmu soudržnosti a potenciálně, kvalitu produktu. Přesný vzhled a chování pár programování se může výrazně lišit od ostatních týmů i v situacích, v závislosti na následující (mimo jiné):

1. Obor "úloha" se spolupracovali na (například chyby, uživatelský scénář)

1. Očekávané době trvání relace spolupráce (třeba dvě minuty, hodiny, na plný úvazek, jednou týdně, bude doplněno)

1. Počet lidí zahrnuty (například 2, celý tým)

1. Role každý účastník (např. "driver", pozorovatel/revidující, odborník na danou problematiku)

1. Vzdálenost účastníky (například umístěné ve stejné budově, po celém světě)

Živé sdílení bylo navrženo jako nezávislé na všechny výše uvedené otázky a místo toho se snaží podporují pár programování, který je zcela "příležitostné" a catered vaší situaci. Ale nutné dodat, na rozdíl od dvou vývojáři sdílení jedné klávesnice a obrazovky, Live Share umožňuje určitou formu pár programování, které umožňuje vývojářům pracovat na sdílené cíle bez odebrání jejich jednotlivých autonomie nebo předvoleb prostředí. Může pracovat nezávisle, nebo společně, povolení každý účastník zpřístupnit vlastní si mysleli, že proces pro spolupráci.

Pro tento případ použití ještě dál rozdělit, následující položky představují formy pár programování, že uživatelům Live Share pro jsme zjistili jsme:

### <a name="mob-programming"></a>Programování MOB

[MOB programování](https://en.wikipedia.org/wiki/Mob_programming) (nebo programování swarm) je v podstatě pár programování, ale s více než dva uživatele. Proto všechny výhody Live Share pár programování se účtovat stejně také. Kromě toho některé týmy provést "swarming" na základě podle potřeby (například tým rallying kolem fire procházení) na rozdíl od na plný úvazek.

Live Share v současné době podporuje až 30 hostů v relaci.
> [!TIP]
> Pokud chcete povolit 30 hostů v relaci:
> - **VS Code:** přidat "liveshare.increasedGuestLimit":"true" Settings.JSON v nástroji
> - **VS:** Nastavení nástroje > Možnosti > Live Share > Increased hosta omezení na hodnotu "True" 

### <a name="coding-competitions--hack-a-thons"></a>Kódování soutěže / Hack-A-Thons

Kódování soutěží a hack thons jsou účinně krátkodobé, jedné úlohy varianty mob programování. Členové týmu a jejich aktuální roli, jsou také potenciálně dynamické. Protože tento případ použití je obvykle také časově, možnost spolupráce v reálném čase, aniž by bylo potřeba implementovat zcela nový nástroj a možnost spolupráce, bez je omezen na jedné obrazovce nebo klávesnice, můžete přejít tak protokolu ve vzestupném rychlost.

Od účastníků v tomto prostředí nemusí být vždy plně "důvěryhodné", můžete odebrat (a blokovat) hostovaného v relaci v každém okamžiku. To poskytuje "hostitele" plnou kontrolu nad svým prostředím.

### <a name="school-group-projects"></a>Projekty skupiny školy

Skupiny projektů končí vypadá mnohem jako mob programování, kde více studentů spolupracují a může přechod bez problémů mezi soustředit na jednu úlohu, nebo pracovat současně na samostatné úlohy. Spoléhání se pouze na správy verzí ke spolupráci asynchronně, mohou použít Live Share spolupráce reálném čase, které může pomoct sociálních sítí a vzdělávací výhody práce ve skupině.

### <a name="developer-streaming"></a>Pro vývojáře datových proudů

Pro vývojáře datových proudů (prostřednictvím Twitch nebo Mixer) stal poutavé nový formulář vzdělávání. Zatímco Live Share není určena k nahrazení jejich platformách všesměrového vysílání (v případě, že jste dostali jsme požadavek!), poskytuje prostředky pro hostitele na spárování programovat s nejméně hosty a potom Streamovat interakce. Tímto způsobem prohlížeče může potenciálně Další informace zobrazením, přirozené interakce a myšlenkovému dva nebo více vývojářů, kteří může společně fungují i ve zcela samostatném operačních systémů a integrovanými vývojovými prostředími!

### <a name="prototyping--project-inception"></a>Vytváření prototypů / Project zahájení

Při spuštění nového projektu/mikroslužeb nebo nové funkce pro vytváření prototypů/vrcholů tým může často být užitečné spolupráci rychlé pokroku a prozkoumejte nové nápady. Vzhledem k tomu, že nově tvořící základu kódu nemusí ještě potvrzené do sdíleného úložiště, Live Share umožňuje všem uživatelům se účastnit iterativní proces, bez ohledu na to případě, že jsou ve stejné pobočce nebo ne.

## <a name="interactive-education"></a>Interaktivní vzdělávání

Obecně řečeno Live Share cílem je pomoci vývojářům při sdílení znalostí mezi jejich tým. Vzdělávání je základní použití případu pro Live Share, a to podporuje obzvláště dobře tím, že každý účastník k interakci s základu kódu se spolupracovali na, na rozdíl od jednoduše sledovat obrazovku. Každý se učí subtlety různými způsoby, a proto poskytnutím nezávislost na "student" je bylo možné využít výhod instrukce se vzhledem, aniž byste museli obětovat jejich schopnost zkoumat svoje vlastní nápady na cestě.

### <a name="peer-mentoring--onboarding"></a>Peer Mentorování / registrace

Když vývojář představíte novou základu kódu, funkce oblasti, technologie a podobně, Live Share umožňuje provede projektu (pomocí `Follow Mode`), tak, že se můžete postupovat, ale z v rámci své vlastní osobní integrovaného vývojového prostředí. Protože Live Share umožňuje "Guest" nezávisle na sobě přejděte projektu (např. otevření souboru, provádění `Peek Definition`), můžete postupovat podle umožnit, ale také provést rychlé průzkumy podle potřeby (např.) "Hmm, k čemu tato funkce slouží?").

### <a name="team-brown-bags"></a>Týmu Hnědý kontejnery objektů a dat

Tým Hnědý kontejnery objektů a dat jsou efektivně podobné peer mentorování, ale zobrazí na celý tým atd potenciálně, zaměřuje na socializing obecně užitečné poznatky, na rozdíl od zavádění podporu a/nebo pomoc s konkrétním úkolem.

### <a name="classroom-lectures"></a>Přednášky učebny

Instruktoři představujete lekci, mohou použít Live Share sdílet projekt se zúčastnili studenti, namísto jednoduše nabízí ten samý jeho obrazovka. Díky tomu celá třída chcete postupovat podle učitele, při zachování komunikovat s projektem na své vlastní. Kromě toho můžete učitele požádat o jednotlivých studentů při řešení konkrétní části v lekci (např.) "Metoda by měla říkáme zde?"), které vám můžou pomoct na sociálních sítích aspekty třídu, bez nutnosti studentům přímo na začátku místnosti nebo dokonce být fyzicky přítomen ve stejné místnosti (třeba online kurzy).

Pro usnadnění v učebně nastavení, Live Share umožňuje sdílení v režimu jen pro čtení. Instruktoři můžete povolit sdílet svoje projekty s studenty bez nutnosti starat o zbytečné nebo nechtěné změny prováděné režimu jen pro čtení.

Kromě toho Live Share má podporu o povolení až 30 hosté připojení do relace spolupráci. Tímto způsobem Instruktoři může mít své celé třídy připojit do relace a zobrazit kód společně.

Pokud chcete povolit tuto funkci:

- **VS Code:** Přidejte do settings.json "liveshare.increasedGuestLimit":"true".
- **VS:** Nastavení nástroje > Možnosti > Live Share > Increased hosta omezení na hodnotu "True"

Pro tento scénář plně optimalizovat Live Share, musíme Zjednodušte způsob, jak inicializována relace ([#422](https://github.com/MicrosoftDocs/live-share/issues/422)).

## <a name="code-reviews"></a>Revize kódu

Žádosti o přijetí změn se efektivní způsob, jak spolupracovat s ostatními, ale obvykle představují dokončení úlohy (s výjimkou žádostí o přijetí změn "WIP") a že je požadováno sloučí v. V mnoha případech, zpětnou vazbu, která je uvedena v žádost o přijetí změn může snadno získali dříve, a proto není potenciálně hodnotu týmům umožňuje snadno a nepřetržitě vyhledejte pomoc od jejich partnerské uzly, na rozdíl od čekat, než "dokončení" úlohu požádat.

Live Share umožňuje okamžitě sdílí váš projekt s ostatními, je možné povolit "neformální" / ad-hoc revize kódu, kde místo s žádostí o pomoc, můžete se jednoduše hledání vstup zajistit směr nebo přístup v souladu s ostatními. To může pomoct potenciálně následných žádostí o přijetí změn dokončí rychleji a jednoznačně pomáhá socialize znalostí v týmu.

Kromě toho Live Share umožňuje sdílet libovolného adresáře, můžete ji k provedení revize kódu i v případě, že používáte není aktuálně správy verzí (v případě, že byste měli!), nebo pokud váš tým nepoužívá žádosti o přijetí změn (například můžete provádět vývoj založených na páteřní).

Živé sdílené složky nesdílel aktuálně rozdíly zdrojového ovládacího prvku, což je důležitých kontextu při použití na revizi kódu. Toto je do našeho plánu a velmi si vážíme jakoukoli zpětnou vazbu na prioritu ([hlas 👍 tady](https://github.com/MicrosoftDocs/live-share/issues/36)).

## <a name="technical-interviews"></a>Technické rozhovory

Při dotazování kandidáty na pozici pro vývojáře, často je užitečné k jít za hranice Tabule, diskusí a místo toho zachovány řešení kódování problém z v rámci skutečné integrované vývojové prostředí (zejména v případě, že tým nebo organizace má "standardizované" pro nástroj, který Chcete je použít). To zajišťuje jejich výhody pracovat způsobem, který je potenciálně přirozeného/pohodlnější (Většina vývojářů není kód na Tabule!), ale taky jim umožňuje okamžitou zpětnou vazbu nebo pomoc při práci (například chyby intellisense sestavení). V mnoha případech je mnohem důležitější pochopit Release candidate myšlenkovému, na rozdíl od jejich schopnost pamatovat Přesná syntaxe a/nebo názvy rozhraní API. Tímto způsobem, Live Share poskytuje funkce, která se podobá až po provádění pár programování relace, ale umožňuje účastníka a být ve svém vlastním prostředí (včetně nastavení operačního systému, jako je přístupnost) a bude fungovat stejně i pro místní nebo vzdálené rozhovory.

Vývoj skutečných je víc než jen psaní kódu. Protože Live Share také podporuje sdílené ladění, úkoly a terminály, umožňuje tazatelům sledovat kandidáty při diagnostikování problému a poskytují je vhodné nástroje potřebné k vyřešení (například krok ladit, spouštět testy). Vzhledem k tomu, že všechny kontext je vzdálený od počítače hostitele, kandidáty rychle přejít do "rozhovor prostředí" aniž by bylo potřeba nastavit jejich počítače (kromě instalace Live Share). Týmy může potom udržovat úložiště sdílené dotazování aplikace (nebo použijte svůj základ kódu skutečných produktů), který může klonovat a sdílí s kandidáty, stačí poslat mu adresa URL relace před každou rozhovor.

## <a name="see-also"></a>Viz také:

- [Podpora jazyků a platforem](platform-support.md)
- [Požadavky na připojení pro Live Share](connectivity.md)
- [Funkce zabezpečení Live Share](security.md)
- [Hlavní chyby, žádosti o funkce a omezení](https://aka.ms/vsls-issues)
- [Všechny žádosti o funkce a omezení](https://aka.ms/vsls-feature-requests)

Máte potíže? Podívejte se na článek o [odstraňování potíží](../troubleshooting.md) nebo nám [pošlete svůj názor](../support.md).
