---
title: Podpora rozšíření a ekosystém – Visual Studio Live Share | Dokumentace Microsoftu
description: Přehled rozšíření podpory pro Visual Studio Live share.
ms.custom: ''
ms.date: 04/25/2018
ms.reviewer: ''
ms.suite: ''
ms.technology:
- liveshare
ms.topic: reference
author: lostintangent
ms.author: joncart
manager: AmandaSilver
ms.workload:
- liveshare
ms.openlocfilehash: 5a9787643643c22ca7302528dc794480d09df902
ms.sourcegitcommit: 4f733c9053848f26da03d47050bcb734f6c98b31
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/02/2019
ms.locfileid: "57254851"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="extensions-and-ecosystem-support"></a>Rozšíření a podporu ekosystém

Jedním z primárních cílů Visual Studio Live Share je vývojářům umožňuje spolupracovat s kolegy a z pohodlí jejich oblíbených a [ **vysoce přizpůsobené** ](https://marketplace.visualstudio.com/) nástroje. Tímto způsobem ad-hoc interakce často, může dojít, přitom vizuálně známé a výrazně, bez ohledu na to co vám pomáhají s. Za tím účelem je velmi důležité, že budou moci pokračovat v používání všechna rozšíření, které podporují účastníci v rámci spolupráce relace jejich [osobní preference a pracovních postupů](#user-specific-extensions) (třeba/ikony barevné motivy, klávesové zkratky, editor zvýšení produktivity stimulátory).

Kromě toho provést v rámci připojení k relaci spolupráci jako okamžité nejvíce přitom vysoce produktivní, cílem Visual Studio Live Share je povolit hosté automaticky využívat nástroje specifické pro projekt, který sdílí jeho hostitele. Tímto způsobem můžete jednoduše kliknout na odkaz, spusťte nástroj dle výběru a zahájit spolupráci, bez jakékoliv další nastavení. Za tím účelem je velmi důležité tohoto rozšíření, která power základní [upravovat, vytvářet a ladit pracovní postup](#project-specific-extensions)se transparentně "vzdálený" z hostitele na hosta, tak, aby věci, jako je automatické dokončování, přejít k definici a ladění " prostě fungují".

Tento dokument popisuje aktuální označuje stav pro rozšíření rozsáhlému ekosystému, stejně jako "metrik" pro výše uvedené cíle. Pokud dojde k rozšíření, které nebude tato kritéria splňují a je velmi důležité pro váš osobní pracovní postup, pak prosím [dejte nám vědět!](https://github.com/MicrosoftDocs/live-share/issues/new)

## <a name="user-specific-extensions"></a>Rozšíření specifické pro uživatele

Rozšíření, které podporují vlastní uživatelská nastavení **musí** práce pro hostitele, a **by měl** pro všechny hosté fungují. Pokud rozšíření nebude fungovat správně pro hostitele, který by byl regrese a je pravděpodobně chyba ve Visual Studio Live Share (prosím [založte problém](https://github.com/MicrosoftDocs/live-share/issues/new) Pokud se zobrazí jedna!). Pokud rozšíření nechová podle očekávání pro hosta, můžou vyžadovat [změn v samotné rozšíření](#known-issues), a jsme budete pracovat s ekosystémem partnerů pro adresu/zlepšit tyto scénáře.

### <a name="visual-studio-code"></a>Visual Studio Code

| Kategorie | Příklady () dotazů | Host podporovány? | Spolupráci? |
|-|-|-|-|
| Barevné motivy | [Jeden Pro tmavý](https://marketplace.visualstudio.com/items?itemName=zhuangtongfa.Material-theme), [výstup Colorizer](https://marketplace.visualstudio.com/items?itemName=IBM.output-colorizer), [Rainbow řetězec](https://marketplace.visualstudio.com/items?itemName=wk-j.vscode-rainbow-string), [Vybarvenými oblastech](https://github.com/jmihelcic/colored-regions), [odsazena bloku zvýraznění](https://marketplace.visualstudio.com/items?itemName=byi8220.indented-block-highlighting), [ Zvýraznění todo](https://marketplace.visualstudio.com/items?itemName=wayou.vscode-todo-highlight), [párování Colorizer pár](https://marketplace.visualstudio.com/items?itemName=CoenraadS.bracket-pair-colorizer) | ✅ | *NENÍ K DISPOZICI* |
| Ikona sady | [vscode-icons](https://marketplace.visualstudio.com/items?itemName=robertohuertasm.vscode-icons), [Visual Studio Classic Icons](https://marketplace.visualstudio.com/items?itemName=jez9999.vsclassic-icon-theme) | ✅ | *NENÍ K DISPOZICI* |
| Klávesové zkratky | [VIM](https://marketplace.visualstudio.com/items?itemName=vscodevim.vim), [klávesové zkratky IntelliJ IDEA](https://marketplace.visualstudio.com/items?itemName=k--kato.intellij-idea-keybindings), [Keymap popisný (emacs)](https://marketplace.visualstudio.com/items?itemName=lfs.vscode-emacs-friendly) | ✅ | *NENÍ K DISPOZICI* |
| Fragmenty kódu | [Fragmenty kódu angular v5](https://marketplace.visualstudio.com/items?itemName=johnpapa.Angular2), [fragmentů kódu HTML](https://marketplace.visualstudio.com/items?itemName=abusaidm.html-snippets), [SVG ikony](https://marketplace.visualstudio.com/items?itemName=idleberg.svg-icons), [hlavička souboru](https://marketplace.visualstudio.com/items?itemName=mikey.vscode-fileheader) | ✅ | *NENÍ K DISPOZICI* <sup>1</sup> |
| Organizace | [Synchronizace nastavení](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync), [projektový manažer](https://marketplace.visualstudio.com/items?itemName=alefragnani.project-manager), [Timeit](https://marketplace.visualstudio.com/items?itemName=smulyono.timeit), [kontrolní body](https://marketplace.visualstudio.com/items?itemName=micnil.vscode-checkpoints), [TODO analyzátor](https://marketplace.visualstudio.com/items?itemName=minhthai.vscode-todo-parser), [Oblíbené položky ](https://marketplace.visualstudio.com/items?itemName=kdcro101.favorites) (❌) [záložky](https://marketplace.visualstudio.com/items?itemName=alefragnani.Bookmarks) (❌) | ✅ <sup>2</sup> | *NENÍ K DISPOZICI* <sup>3</sup> |
| Produktivita | [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens), [Automatické přejmenování značky](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag), [kódu osnovy](https://github.com/patrys/vscode-code-outline), [barevné zvýraznění](https://marketplace.visualstudio.com/items?itemName=naumovs.color-highlight), [zvýšit výběr](https://marketplace.visualstudio.com/items?itemName=albymor.increment-selection), [ Bracketeer](https://marketplace.visualstudio.com/items?itemName=pustelto.bracketeer), [náhled obrázku](https://marketplace.visualstudio.com/items?itemName=kisstkondoros.vscode-gutter-preview), [pomocné rutiny JSON](https://marketplace.visualstudio.com/items?itemName=zhoufeng.json-helper) (ukazatel), [výběr barvy](https://marketplace.visualstudio.com/items?itemName=anseki.vscode-color), [kopírování aplikace Word v kurzoru](https://marketplace.visualstudio.com/items?itemName=alefragnani.copy-word), [CodeMetrics](https://marketplace.visualstudio.com/items?itemName=kisstkondoros.vscode-codemetrics) (CodeLens) [Git spoluautoři](https://github.com/rjimenezda/vscode-coauthor), [JavaScript podpůrná](https://marketplace.visualstudio.com/items?itemName=sburg.vscode-javascript-booster) (CodeActions) [protokolu konzoly Turbo](https://marketplace.visualstudio.com/items?itemName=ChakrounAnas.turbo-console-log), [ Goto další/předchozí člen](https://marketplace.visualstudio.com/items?itemName=mishkinf.goto-next-previous-member), [Automatické posunování](https://github.com/PejmanNik/vscode-autoScroll?files=1), [NPM Import verze](https://marketplace.visualstudio.com/items?itemName=axetroy.vscode-npm-import-package-version) (❌) [importovat náklady](https://github.com/wix/import-cost) (❌) | ✅ <sup>2</sup> | ❌ <sup>3</sup> |
| REPLs | [Klient REST](https://marketplace.visualstudio.com/items?itemName=humao.rest-client), [kódu Runner](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner), [Quokka.js](https://marketplace.visualstudio.com/items?itemName=WallabyJs.quokka-vscode), [R](https://marketplace.visualstudio.com/items?itemName=Ikuyadeu.r) | ✅ <sup>4</sup> | ❌ <sup>3</sup>  |
| Správce prostředků | [MSSQL](https://marketplace.visualstudio.com/items?itemName=ms-mssql.mssql), [ftp jednoduchý](https://marketplace.visualstudio.com/items?itemName=humy2833.ftp-simple), [Azure Functions](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-azurefunctions), [Docker](https://marketplace.visualstudio.com/items?itemName=PeterJausovec.vscode-docker), [Brew služby](https://marketplace.visualstudio.com/items?itemName=beauallison.brew-services) | ✅ <sup>5</sup> | ❌ <sup>3</sup>  |

<sup>1</sup> *Pokud byl uživatel již znáte fragment kódu, očekávají by byla k dispozici, a proto, díky kterým sdílené nedává smysl nutně.*

<sup>2</sup> *tyto kategorie rozšíření jsou tak rozdílné, že není možné Řekněme, že fungují. Ale teoreticky by měly a sledujeme budete klíč ty, které ji nemají.*

<sup>3</sup> *tyto kategorie rozšíření můžou mít užitek z prostředí pro spolupráci, a proto potřebujeme vědět, že koncový uživatel zpětnou vazbu!*

<sup>4</sup> *vyžadují hostem a být modulu runtime nainstalovány nástroje (například Node.js) a fungují tak, že spouštění kódu místně.*

<sup>5</sup> *těchto fungují tak, že připojení k serveru určitého druhu a můžete pracovat buď centralizované servery, servery, které sdílí hosta.*

### <a name="visual-studio"></a>Visual Studio

Již brzy.

## <a name="project-specific-extensions"></a>Rozšíření specifické pro projekt

Hostiteli nainstalovaná rozšíření, která podporu základní úpravy, sestavování a ladění aplikace a specifické na jazyk nebo platformu/knihovny/sadu SDK, musí být automaticky dostupná ke hosté, bez nutnosti jejich nutnost nic instalovat. Tímto způsobem hostitele můžete nastavit jejich prostředí pro podporu produktivitu vývoje projektu a povolit jejich hosté k nim, okamžitě bez další předpoklady. Vzhledem k tomu, že rozšíření specifické pro projekt nejsou subjektivní nebo osobní žádným způsobem, nedeterministicky sdíleny z hostitele na hosta, aniž by to ovlivnilo kýmkoli známém prostředí.

Kromě toho za účelem podpory specifické pro projekt rozšíření, která má nainstalovanou hosta, ale hostitel nebude, by v ideálním případě poskytují degradovaný, ještě funkční prostředí (např. načtení jednotlivých souborů intellisense, nebudou moct dokument formátu).

| Kategorie | Příklady () dotazů | Sdílet? | Host podporovány? |
|-------|----------|--------|-----|
| Gramatika / zvýrazňování syntaxe | [Ryb prostředí](https://marketplace.visualstudio.com/items?itemName=TeddyDD.fish), [Nginx](https://marketplace.visualstudio.com/items?itemName=shanoor.vscode-nginx), [Vetur](https://marketplace.visualstudio.com/items?itemName=octref.vetur), [DotEnv](https://marketplace.visualstudio.com/items?itemName=mikestead.dotenv), [ES6 řetězec HTML](https://marketplace.visualstudio.com/items?itemName=hjb2012.vscode-es6-string-html), [Todo +](https://marketplace.visualstudio.com/items?itemName=fabiospampinato.vscode-todo-plus), [Rainbow sdíleného svazku clusteru](https://marketplace.visualstudio.com/items?itemName=mechatroner.rainbow-csv) | ❌ | ✅ |
| Jazykové služby | [YAML](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml), [cesta Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense), [ARM](https://marketplace.visualstudio.com/items?itemName=msazurermtools.azurerm-vscode-tools) | ✅ <sup>1</sup>| ✅ <sup>2</sup> |
| JSON Schemas | [Azure Functions](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-azurefunctions) | ✅ | ✅ |
| Linterů | [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint), [Markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint), [kódu kontrolu pravopisu](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker), [PHPCS](https://marketplace.visualstudio.com/items?itemName=ikappas.phpcs) | ✅ | ✅ <sup>2</sup>  |
| Formátovací moduly | [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode), [Beautify](https://marketplace.visualstudio.com/items?itemName=HookyQR.beautify) | ✅ | ✅ <sup>2</sup> |
| Ladicí programy | [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python), [ladicího programu pro Chrome](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome) | ✅ <sup>3</sup> | ❌ <sup>4</sup> |
| Nástrojům test Runner | [Nástroj Test Runner pro jazyk Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-test), [postranního panelu Mocha](https://marketplace.visualstudio.com/items?itemName=maty.vscode-mocha-sidebar), [Postman Runner](https://marketplace.visualstudio.com/items?itemName=eridem.vscode-postman), [Jest Runner](https://marketplace.visualstudio.com/items?itemName=firsttris.vscode-jest-runner), [Neptun](https://marketplace.visualstudio.com/items?itemName=LambdaFactory.neptune) | ❌ <sup>5</sup> | ✅ <sup>2</sup> |
| Vlastní soubor náhledy | [Ve verzi Preview SVG](https://marketplace.visualstudio.com/items?itemName=cssho.vscode-svgviewer), [GraphViz](https://marketplace.visualstudio.com/items?itemName=joaompinto.vscode-graphviz), [velikost obrázku Markdownu](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-image-size) | ❌ |  ✅ |
| Generátory souboru nebo projektu | [Služba Azure Functions](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-azurefunctions), [generátor projektu jazyka C/C++](https://marketplace.visualstudio.com/items?itemName=danielpinto8zz6.c-cpp-project-generator) | ❌ | ❌<sup>6</sup> |
| Poskytovatelé řízení zdrojů | [SVN](https://marketplace.visualstudio.com/items?itemName=johnstoncode.svn-scm), [Hg](https://marketplace.visualstudio.com/items?itemName=mrcrowl.hg) | ❌ | ❌ |

<sup>1</sup> *momentálně se podporuje jenom C# a jazyka JavaScript/TypeScript s další podporou již brzy.*

<sup>2</sup> *by podporují pouze aktuálně aktivní dokument, protože hosté nemají přístup k místnímu souboru.*

<sup>3</sup> *sdílené základní možnosti ladění, ale nejsou automaticky předávat všechny spuštěné servery.*

<sup>4</sup> *hosté nemají místní kopii aplikace, a proto běžící aplikaci a všechny relace ladění potřeba spustit na počítači hostiteli.*

<sup>5</sup> *výstup testovacího běhu by vyžadovaly všechny výsledné terminály, podokna výstup a chyby byly také sdílet s hosty.*

<sup>6</sup> *téměř všechny z nich byste použili na Node.js `fs` modul přímo k vytváření souborů, které nebude fungovat.*

### <a name="visual-studio"></a>Visual Studio

Již brzy.

## <a name="known-issues"></a>Známé problémy

Toto jsou problémy s aktuálně známé rozšíření, které může bránit funkčním pro hosty v rámci kontextu relace spolupráce (spolu s jejich řešení) a proto může mít vliv na jejich pracovního postupu:

### <a name="visual-studio-code"></a>Visual Studio Code

| Problém | Důvod | Alternativní řešení |
|-|-|-|
| Použití na Node.js `fs` modulu, který chcete detekovat/čtení souborů (například konfigurace souboru), nebo vytvoření výčtu adresářů (a nejste si služba jazyka). | Hosté nemají přístup k místním souborům. | 1. Řádně snížit činnost koncového uživatele *(Pokud je to možné).*<br /><br />2. Použití `openTextDocument` a `findFiles` pracovního prostoru rozhraní API pro čtení a vytvoření výčtu souborů. |
| Použití na Node.js `fs` modulu k vytvoření nebo zápis souborů | *Stejný jako předchozí* | *Není k dispozici* můžete použít `openTextDocument(Uri)` rozhraní API k vytvoření `untitled` soubor, ale nelze uložit přímo do systému souborů do konkrétní cesty. |
| V závislosti na dodávat projektu knihovny nebo nástroj | *Stejný jako předchozí* | 1. Vytvoření balíčku záložní verze závislosti s příponou<br><br> 2. Podporu globální instalace odblokujete hosté, pokud se rozhodnete explicitně ji nainstalovat.<br><br> 3. Vzdálené stavu a akce, pokud je to možné, protože hostitel bude mít správné závislosti, které jsou k dispozici. |
| Použití na Node.js `fs` modulu k vytvoření adresáře | *Stejný jako předchozí* | *NENÍ K DISPOZICI* |
| Omezení funkce na dokumenty, které používají `file` schéma. | Soubory při použití na straně hosta `vsls` schéma. | Přidání podpory pro `vsls` dokumenty ([příklad](https://github.com/CoenraadS/BracketPair/pull/73)) |
| Použití `Uri.file` metoda a/nebo `Uri.fsPath` / `TextDocument.fileName` členy k serializaci/parsování identifikátorů URI | *Stejný jako předchozí* | Použití `Uri.parse` a `Url.toString()` místo, které udržovat a dodržovat schémata souboru ([příklad](https://github.com/micnil/vscode-checkpoints/pull/2)) |
| Použití `workspace.openTextDocument` metodu s cestu k souboru místo `Uri` | *Stejný jako předchozí* | Zadejte `Uri` instanci místo řetězec cesty soubor raw ([příklad](https://github.com/micnil/vscode-checkpoints/pull/2)) |
| Použití `workspace.rootPath` vlastnost pro zjištění přítomnosti tohoto pracovního prostoru | `workspace.rootPath` Vlastnost volání `Uri.fsPath` první `workspaceFolder` v `workspace`, který má stejný problém uvedených výše | Použití `workspace.workspaceFolders` vlastnost pro zjištění přítomnosti tohoto pracovního prostoru místo a v případě potřeby, podívejte se na každý `workspaceFolder`společnosti `Uri.scheme` chcete zjistit, jestli je místní nebo ne |
| Bez zadání schématu dokumentu, při registraci jazykových služeb (buď prostřednictvím `LanguageClient`, nebo `languages.register*` metody) | Hosté příjem výsledků služby jazyka ze svých místních rozšíření i hostitele a proto, pokud obě účastníci mají nainstalované rozšíření služby stejného jazyka, guests uvidí duplicitní položky pro určité informace (například automatické doplňování, kód Akce) | Omezit jazykové služby na pouze `file` a `untitled` schémata ([příklad](https://github.com/vuejs/vetur/pull/756/files)) |
| Nekontrolují se dokumentu `Uri.scheme` před naplnění `DiagnosticCollection` pro něj | *Stejný jako předchozí* | Generovat jenom `Diagnostics` pro `documents` jehož `Uri.scheme`  ===  `file` ([příklad](https://github.com/Huachao/vscode-restclient/pull/196)) |
| Nekontrolují schéma pracovního prostoru se při vrácení `Tasks` z vlastního `TaskProvider`  | Zobrazit všechny úlohy vzdáleném i místním hostů a proto by se zobrazily duplicity po obou účastníci měl stejnou příponu nainstalované  | Vrátit pouze `Tasks` pro `WorkspaceFolder`s jejíž `Uri.scheme`  ===  `file` ([příklad](https://github.com/Microsoft/vscode-eslint/blob/0fdb7c74b093cae9dc08355e7235582a254f24c2/client/src/tasks.ts#L42)) |

### <a name="visual-studio"></a>Visual Studio

Již brzy.

<!--

## Extensibility API

In addition to the core goals outlined in the beginning of this document, Live Share also wants to enable extension authors to enhance the default sharing experience in the following ways:

1. Contributing to the core collaborative feature set, based on behavior that only the extension would know about. In these scenarios, the host could have an extension installed, and potentially allow guests to benefit from it without also needing to have it installed

2. Enhancing their own experiences to be collaborative (e.g. syncing bookmarks between participants), by synchronizing any custom state and UI interactions. In these scenarios, only participants that had the custom extension installed would be able to take advantage of the added collaboratively.

This will require some form of API/SDK, which extensions can use to determine if/when the end-user is within a Live Share session, and if so, light up additional capabilities. The following represents a high-level overview of some of the extension points we've identified, and look forward to getting further feedback on:

| Shared Resource | Extensibility Point(s) |
|------------------|---------------------|
| User status | 1. Retrieving the list of participants within the current Live Share session (e.g. the [Git Co-Authors](https://marketplace.visualstudio.com/items?itemName=drrouman.git-coauthors) extension could use that to populate the host's commit message with)<br /><br /> 2. Updating a participant's location (outside of just editors), as well as allowing other participant's to jump to/pin to them as they move into custom extension UI (e.g. a participant is navigating a MongoDB database using the [Azure Cosmos DB](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-cosmosdb) extension). |
| Workspace | *N/A* - Live Share can transparently share all files, edits, cursors and highlights, without requiring an extension to do anything extra if it modified the file system and/or cursor/highlight position. |
| Language Services | *N/A* - Long-term, Live Share can transparently remote all language services (e.g. go to definition, document formatting, CodeLens) to the guest, including those that are contributed via extensions (e.g. [Path Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense), [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)) |
| Debugging Sessions | *N/A* - Live Share can transparently remote all debugging sessions, including those that are enabled by custom extensions (e.g. [Debugger for Chrome](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome)) |
| Servers | 1. Sharing a server that an extension was responsible for starting, and then optionally specifying whether a browser should be launched on the guest's machine as well (e.g. a debug adapter that launched a web server).  |
| Custom | 1. Synchronizing arbitrary state and/or user interactions (e.g. the [Bookmarks](https://marketplace.visualstudio.com/items?itemName=alefragnani.Bookmarks) extension syncing CRUD operations across participants, the [Maven for Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-maven) extension exposing the project-wide view to guests) |

-->

## <a name="see-also"></a>Viz také:

- [Podpora jazyků a platforem](platform-support.md)
- [Požadavky na připojení pro Live Share](connectivity.md)
- [Funkce zabezpečení Live Share](security.md)
- [Hlavní chyby, žádosti o funkce a omezení](https://aka.ms/vsls-issues)
- [Všechny žádosti o funkce a omezení](https://aka.ms/vsls-feature-requests)

Máte potíže? Podívejte se na článek o [odstraňování potíží](../troubleshooting.md) nebo nám [pošlete svůj názor](../support.md).
