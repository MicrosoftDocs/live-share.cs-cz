---
title: Podpora platforem a jazyků – Visual Studio Live Share | Dokumentace Microsoftu
description: Přehled o podpoře platforem a jazyků pro Visual Studio Live share.
ms.custom: ''
ms.date: 04/25/2018
ms.reviewer: ''
ms.suite: ''
ms.topic: reference
author: lostintangent
ms.author: joncart
manager: AmandaSilver
ms.workload:
- liveshare
ms.openlocfilehash: 91e80df324a0b2f49fdf37a5270cf7b86fca5c7c
ms.sourcegitcommit: 100fce9b9bbcd7e6f68d40659bd2760e9537de37
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/29/2019
ms.locfileid: "58640221"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="language-and-platform-support"></a>Podpora jazyka a libovolné platformy

Visual Studio Live Share na funkce jsou určeny pro práci napříč různými na šířku jazyky a platformy aplikací. Ale vzhledem k velkému počtu změn, některé platformy a jazyky jsou podrobnější než jiné. Tento dokument popisuje aktuální známé stavu řadu oblíbených jazyků a platforem pro aktuálně podporované funkce.

Zjistit jazyk nebo platformu, kterou budete potřebovat? Chcete přidat jednoho nevidíte? [Hlasujte, zde.](https://github.com/MicrosoftDocs/live-share/issues/12)

## <a name="visual-studio-code"></a>Visual Studio Code

Všechny jazyky / platformy mají stejný soubor intellisense (při instalaci příslušné rozšíření), stejně jako zabarvení a společně podporu pro editaci. Seznamy níže popisuje pokročilé funkce aktuálně bez dokončení, univerzální podpory:

### <a name="languages"></a>Jazyky

| Jazyk | Sdílené jazykových služeb | Sdílené ladění |
|----------|--------------------------------|--------------|
| Ansible | ✅ | *NENÍ K DISPOZICI* |
| Ballerina | ✅ | ✅ |
| Bash | ✅ | ✅ |
| C++ | ✅ | ✅ |
| C# | ✅ | ✅ |
| Clojure | ✅ | *NENÍ K DISPOZICI* <sup>4</sup> |
| [ColdFusion (CFML)](https://marketplace.visualstudio.com/items?itemName=KamasamaK.vscode-cfml) | ✅ | *NENÍ K DISPOZICI* <sup>4</sup> |
| [Crystal](https://marketplace.visualstudio.com/items?itemName=faustinoaq.crystal-lang) | ✅ | *NENÍ K DISPOZICI* <sup>4</sup> |
| CSHTML | *NENÍ K DISPOZICI* <sup>1</sup> | ✅ |
| CSS | *NENÍ K DISPOZICI* | *NENÍ K DISPOZICI* |
| DART | ✅ | ✅ |
| Docker | ✅ | *NENÍ K DISPOZICI* |
| Elixir | ✅ | ✅ |
| Elm | ✅ |  *NENÍ K DISPOZICI* <sup>4</sup> |
| Erlangovo | ✅ | ✅ |
| F# | ✅ |  *NENÍ K DISPOZICI* <sup>4</sup> |
| Tok | ✅ |  *NENÍ K DISPOZICI* <sup>4</sup> |
| Fortran | ✅ | *NENÍ K DISPOZICI* |
| Go | ✅ | ✅ |
| Gradle | ✅ | *NENÍ K DISPOZICI* <sup>4</sup> |
| GraphQL | ✅ | *NENÍ K DISPOZICI* <sup>4</sup> |
| Haskell | ✅ | ✅ |
| HTML | *NENÍ K DISPOZICI* | <sup>2</sup> |
| Java | ✅ | ✅ |
| JavaScript / TypeScript | ✅ | ✅ <sup>3</sup> |
| Helena | ✅ | *NENÍ K DISPOZICI* <sup>4</sup> |
| [Kotlin](https://marketplace.visualstudio.com/items?itemName=mathiasfrohlich.Kotlin) | *NENÍ K DISPOZICI* | *NENÍ K DISPOZICI* <sup>4</sup> |
| Lua | ✅ | ✅ |
| Markdown | ✅ | *NENÍ K DISPOZICI* |
| MATLAB |  ✅ | *NENÍ K DISPOZICI* <sup>4</sup> |
| Objective-C | ✅ | *NENÍ K DISPOZICI* <sup>4</sup> |
| Pascal | ✅ | *NENÍ K DISPOZICI* <sup>4</sup> |
| Perl | ✅ | ✅ |
| PHP | ✅ | ✅ |
| PowerShell | *NENÍ K DISPOZICI* | ✅ |
| Python |  ✅ | ✅ |
| PureScript | ✅ | *NENÍ K DISPOZICI* <sup>4</sup> |
| R |  ✅ | *NENÍ K DISPOZICI* <sup>4</sup> |
| [Z důvodu/OCaml](https://marketplace.visualstudio.com/items?itemName=freebroccolo.reasonml) | ✅ | *NENÍ K DISPOZICI* <sup>4</sup> |
| reStructuredText | ✅ | *NENÍ K DISPOZICI* |
| Ruby | ✅ | ✅ |
| Rust | ✅ | *NENÍ K DISPOZICI* <sup>4</sup> |
| [Sass](https://marketplace.visualstudio.com/items?itemName=robinbentley.sass-indented) | ✅ | *NENÍ K DISPOZICI* |
| Scala | ✅ | *NENÍ K DISPOZICI* <sup>4</sup> |
| Solidity | ✅ | *NENÍ K DISPOZICI* <sup>4</sup> |
| SQL / T-SQL | *NENÍ K DISPOZICI* | *NENÍ K DISPOZICI* <sup>4</sup> |
| [Pera](https://marketplace.visualstudio.com/items?itemName=sysoev.language-stylus) | ✅ | *NENÍ K DISPOZICI* |
| [Svelte](https://marketplace.visualstudio.com/items?itemName=JamesBirtles.svelte-vscode) | ✅ | *NENÍ K DISPOZICI* <sup>4</sup> |
| Kód SWIFT | ✅ | *NENÍ K DISPOZICI* <sup>4</sup> |
| Terraform | ✅ | *NENÍ K DISPOZICI* <sup>4</sup> |
| XML | ✅ | *NENÍ K DISPOZICI* <sup>4</sup> |
| YAML | ✅ | *NENÍ K DISPOZICI* <sup>4</sup> |

<sup>1</sup> CSHTML bez podpory v C# rozšíření.<br />
<sup>2</sup> vložený JavaScript ve formátu HTML se podporuje při ladění klienta.<br />
<sup>3</sup> JavaScript / TypeScript ladění pro uzel nebo prohlížeče.<br />
<sup>4</sup> příslušné rozšíření pro VS Code v současné době nepodporuje ladění. Jakmile ho nemá, bude prozkoumáme přidává podporu společně ladění k němu. <br />

### <a name="platforms"></a>Platformy

| Typ aplikace a platformy | Sdílené ladění | Sdílení aplikací |
|-------------------|--------------|-------------|
| Arduino | ✅ | *NENÍ K DISPOZICI* |
| Azure App Service | ✅ | *NENÍ K DISPOZICI* |
| Azure Dev mezery | ✅ | ✅ <sup>1</sup> |
| Služba Azure Functions (místní a vzdálené) | ✅ | ✅ <sup>1</sup> |
| Blockchain (Etherea) | ✅ | ✅ <sup>1</sup> |
| Konzoly nebo rozhraní příkazového řádku | ✅ | ✅ <sup>4</sup> |
| Databáze | <sup>5</sup> | ✅ <sup>1</sup> |
| Desktop (elektronovým nebo nativní) | ✅ | <sup>9</sup> |
| Dynamics NAV 2018 | ✅ | ✅ <sup>1</sup> |
| Hry (Unity) | ✅ | <sup>9</sup> |
| Hry (Unreal) | ✅ | <sup>9</sup> |
| Kubernetes (YAML, Helm) | ✅ |  ✅ <sup>1</sup> |
| Markdown | *NENÍ K DISPOZICI* | ✅ <sup>6</sup> |
| Mobilní zařízení (Cordova) | ✅ | ✅ <sup>1,7</sup> |
| Mobilní zařízení (nativní) | ✅ | <sup>9</sup> |
| Mobilní zařízení (React Native) | ✅ | ✅ <sup>1,8</sup> |
| Webová aplikace / rozhraní API (Back-end) | ✅ | ✅ <sup>1</sup> |
| Webová aplikace (Front-end) | ✅ <sup>2</sup> | ✅ <sup>3</sup> |
| Rozšíření pro VS Code | | <sup>9</sup> |

<sup>1</sup> prostřednictvím [místní server sdílená složka](../use/vscode.md#share-a-server).<br />
<sup>2</sup> ladění nastane znovu proti hostitele prohlížeče spíše než hosta.<br />
<sup>3</sup> sdílením back-end.<br />
<sup>4</sup> podporované prostřednictvím sdíleného terminály.<br />
<sup>5</sup> ladění procs databáze uloženou v tuto chvíli nepodporuje <br />
<sup>6</sup> prostřednictvím "verze preview". Image se však nezobrazí kvůli známému problému. [Hlas (👍) tady.](https://github.com/MicrosoftDocs/live-share/issues/61)<br />
<sup>7</sup> aplikace Cordova je možné sdílet prostřednictvím platformy "prohlížeč"<br />
<sup>8</sup> react Native aplikace je možné sdílet prostřednictvím Expo a [sdílené servery](../use/vscode.md#share-a-server).<br />
<sup>9</sup> live Share v současné době nepodporuje sdílení systému windows/obrazovky. [Hlas (👍) tady.](https://github.com/MicrosoftDocs/live-share/issues/236)

## <a name="visual-studio"></a>Visual Studio

I když většina jazyků má některé jednoho souboru podporu technologie Intellisense, existují některé upozornění níže. Všechny jazyky a platformy podporují společný úpravy. Zbývající část seznamu vysvětluje pokročilé funkce aktuálně bez dokončení, univerzální podpory:

### <a name="languages"></a>Jazyky

| Jazyk | Jedním souborem jazykových služeb | Celého projektu jazykových služeb | Společně ladění |
|----------|-------------------------------|--------------------------------|--------------|
| C# | ✅ | ✅ | ✅ |
| CSHTML | ✅  <sup>1</sup> | | ✅ |
| ASPX | ✅ <sup>1</sup> |  | ✅ |
| HTML | ✅ | *NENÍ K DISPOZICI* | <sup>2</sup> |
| CSS | ✅ | *NENÍ K DISPOZICI* | *NENÍ K DISPOZICI* |
| JavaScript / TypeScript | ✅ | ✅ | ✅ <sup>3</sup> |
| C++ | ✅ | ✅ | ✅ |
| Python | ✅ | | ✅ |
| Markdown | ✅ | *NENÍ K DISPOZICI* | *NENÍ K DISPOZICI* |
| PowerShell | ✅ | *NENÍ K DISPOZICI* | ✅ |
| VB.NET | ✅ | | ✅ |
| VBHTML | ✅ <sup>1</sup> | | ✅ |
| XAML | ✅ | *NENÍ K DISPOZICI* | <sup>4</sup> |
| SQL / T-SQL | ✅ | *NENÍ K DISPOZICI* | |
| F# | ✅ | | ✅ |
| R | ❌ <sup>5</sup> | *NENÍ K DISPOZICI* | ✅ |

<sup>1</sup> mezery: ASPX, CSHTML a VBHTML mají známé problémy kolem vložené C#/VB podpoře použití modelu code-behind C#/VB soubory nejsou rozpoznat z důvodu plnou podporou technologie intellisense není implementována. [Hlas (👍) si na CSHTML a VBHTML.](https://github.com/MicrosoftDocs/live-share/issues/59) [Hlas (👍) si na ASPX.](https://github.com/MicrosoftDocs/live-share/issues/70)<br />
<sup>2</sup> vložený JavaScript ve formátu HTML se podporuje při ladění klienta.<br />
<sup>3</sup> JavaScript / TypeScript ladění pro uzel nebo prohlížeče.<br />
<sup>4</sup> i když je technicky vzato není k dispozici pro ladění XAML, samotný, je podporováno ladění kódu na pozadí.<br />
<sup>5</sup> mezery: Chyby služby jazyka R na straně hostovaného na spojení a po každé znaku nového řádku. Není podporováno. [Hlas (👍) tady.](https://github.com/MicrosoftDocs/live-share/issues/72)<br />

### <a name="platforms"></a>Platformy

| Typ aplikace a platformy | Společné ladění | Sdílení aplikací |
|-------------------|--------------|-------------|
| Webová aplikace / rozhraní API (Back-End) | ✅ | ✅ <sup>1</sup> |
| Webová aplikace (Front-end) | ✅ <sup>2</sup> | ✅ <sup>3</sup> |
| Azure Functions | ✅  | ✅ <sup>5</sup> |
| Azure Service Fabric | ✅ | ✅ <sup>5</sup> |
| [Azure Dev mezery](https://aka.ms/devspaces) | ✅ | ✅ <sup>1</sup> |
| Databáze | <sup>4</sup> | ✅ <sup>5</sup> |
| Konzoly nebo rozhraní příkazového řádku | ✅ | ✅ <sup>6</sup> |
| Desktop (WinForms) | ✅ | |
| Plochy (WPF) | ✅ | |
| Univerzální platforma pro Windows | ✅ |  |
| Rozšíření VS | ✅ |  |

<sup>1</sup> prostřednictvím [místní server sdílená složka](../use/vs.md#share-a-server). Můžete také použít webové aplikace ASP.NET [automatické webové aplikace sdílení](../use/vs.md#automatic-web-app-sharing).<br />
<sup>2</sup> ladění nastane znovu proti hostitele prohlížeče spíše než hosta.<br />
<sup>3</sup> sdílením back-end.<br />
<sup>4</sup> ladění procs databáze uloženou v tuto chvíli nepodporuje <br />
<sup>5</sup> prostřednictvím [místní server sdílená složka](../use/vs.md#share-a-server). <br />
<sup>6</sup> částečně podporované prostřednictvím sdíleného terminály.<br />
<sup>?</sup> Ještě nebyla ověřena.

## <a name="see-also"></a>Viz také:

- [Podpora rozšíření](extensions.md)
- [Požadavky na připojení pro Live Share](connectivity.md)
- [Funkce zabezpečení Live Share](security.md)
- [Hlavní chyby, žádosti o funkce a omezení](https://aka.ms/vsls-issues)
- [Všechny žádosti o funkce a omezení](https://aka.ms/vsls-feature-requests)

Máte potíže? Podívejte se na článek o [odstraňování potíží](../troubleshooting.md) nebo nám [pošlete svůj názor](../support.md).
