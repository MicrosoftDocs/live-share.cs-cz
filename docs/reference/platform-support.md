---
title: Podpora platforem a jazyků | Microsoft Docs
description: Přehled podpory platforem a jazyků pro živé sdílení sady Visual Studio
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
ms.openlocfilehash: f3dbe1c81a9f91b6452185f4089b5d5100582275
ms.sourcegitcommit: 9deed590c0876b732c8eb150a9a23498a8243efc
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/27/2021
ms.locfileid: "98870536"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="language-and-platform-support"></a>Podpora jazyků a platforem

Funkce Visual Studio Live Share jsou určené pro práci napříč různými oblastmi jazyků a platforem aplikací. Avšak s ohledem na Sheer počet variant jsou některé platformy a jazyky více dokončeny, než jiné. Tento dokument popisuje aktuální známý stav řady oblíbených jazyků a platforem pro aktuálně podporované funkce.

Podívejte se na jazyk nebo platformu, kterou potřebujete? Chcete přidat tu, kterou nevidíte? [Hlasujte.](https://github.com/MicrosoftDocs/live-share/issues/12)

## <a name="visual-studio-code"></a>Visual Studio Code

Všechny jazyky a platformy mají stejný soubor IntelliSense (když je nainstalováno příslušné rozšíření), stejně jako podpora zabarvení a souběžné úpravy. Níže uvedené seznamy zahrnují pokročilé funkce, které jsou aktuálně bez dokončení, univerzální podpora:

### <a name="languages"></a>Jazyky

| Jazyk | Sdílené jazykové služby | Sdílené ladění |
|----------|--------------------------------|--------------|
| Ansible | ✅ | *NENÍ K DISPOZICI* |
| Ballerina | ✅ | ✅ |
| Bash | ✅ | ✅ |
| C++ | ✅ | ✅ |
| C# | ✅ | ✅ |
| Clojure | ✅ | Není *k dispozici* <sup>4</sup> |
| [ColdFusion (CFML)](https://marketplace.visualstudio.com/items?itemName=KamasamaK.vscode-cfml) | ✅ | Není *k dispozici* <sup>4</sup> |
| [Crystal](https://marketplace.visualstudio.com/items?itemName=faustinoaq.crystal-lang) | ✅ | Není *k dispozici* <sup>4</sup> |
| CSHTML | Není *k dispozici* <sup>1</sup> | ✅ |
| Šablony stylů CSS | *NENÍ K DISPOZICI* | *NENÍ K DISPOZICI* |
| Dart | ✅ | ✅ |
| Docker | ✅ | *NENÍ K DISPOZICI* |
| Elixir | ✅ | ✅ |
| Elm | ✅ |  Není *k dispozici* <sup>4</sup> |
| Erlang | ✅ | ✅ |
| F# | ✅ |  Není *k dispozici* <sup>4</sup> |
| Tok | ✅ |  Není *k dispozici* <sup>4</sup> |
| Fortran | ✅ | *NENÍ K DISPOZICI* |
| Go | ✅ | ✅ |
| Gradle | ✅ | Není *k dispozici* <sup>4</sup> |
| GraphQL | ✅ | Není *k dispozici* <sup>4</sup> |
| Haskell | ✅ | ✅ |
| HTML | *NENÍ K DISPOZICI* | <sup>2</sup> |
| Java | ✅ | ✅ |
| JavaScript a TypeScript | ✅ | ✅<sup>3</sup> . |
| Julia | ✅ | Není *k dispozici* <sup>4</sup> |
| [Kotlin](https://marketplace.visualstudio.com/items?itemName=mathiasfrohlich.Kotlin) | *NENÍ K DISPOZICI* | Není *k dispozici* <sup>4</sup> |
| Lua | ✅ | ✅ |
| Markdown | ✅ | *NENÍ K DISPOZICI* |
| MATLAB |  ✅ | Není *k dispozici* <sup>4</sup> |
| Objective-C | ✅ | Není *k dispozici* <sup>4</sup> |
| Jazyce | ✅ | Není *k dispozici* <sup>4</sup> |
| Perl | ✅ | ✅ |
| PHP | ✅ | ✅ |
| PowerShell | *NENÍ K DISPOZICI* | ✅ |
| Python |  ✅ | ✅ |
| PureScript | ✅ | Není *k dispozici* <sup>4</sup> |
| R |  ✅ | Není *k dispozici* <sup>4</sup> |
| [Důvod/OCaml](https://marketplace.visualstudio.com/items?itemName=freebroccolo.reasonml) | ✅ | Není *k dispozici* <sup>4</sup> |
| reStructuredText | ✅ | *NENÍ K DISPOZICI* |
| Ruby | ✅ | ✅ |
| Rust | ✅ | Není *k dispozici* <sup>4</sup> |
| [Sass](https://marketplace.visualstudio.com/items?itemName=robinbentley.sass-indented) | ✅ | *NENÍ K DISPOZICI* |
| Scala | ✅ | Není *k dispozici* <sup>4</sup> |
| Solidity | ✅ | Není *k dispozici* <sup>4</sup> |
| SQL / T-SQL | *NENÍ K DISPOZICI* | Není *k dispozici* <sup>4</sup> |
| [Stylus](https://marketplace.visualstudio.com/items?itemName=sysoev.language-stylus) | ✅ | *NENÍ K DISPOZICI* |
| [Svelte](https://marketplace.visualstudio.com/items?itemName=JamesBirtles.svelte-vscode) | ✅ | Není *k dispozici* <sup>4</sup> |
| Swift | ✅ | Není *k dispozici* <sup>4</sup> |
| Terraform | ✅ | Není *k dispozici* <sup>4</sup> |
| XML | ✅ | Není *k dispozici* <sup>4</sup> |
| YAML | ✅ | Není *k dispozici* <sup>4</sup> |

<sup>1</sup> není podporována podpora cshtml v rozšíření C#.<br />
<sup>2</sup> vložený JavaScript ve formátu HTML je při ladění klienta podporován.<br />
<sup>3</sup> ladění JavaScriptu/TypeScript pro uzel nebo prohlížeč<br />
<sup>4</sup> příslušné rozšíření pro vs Code v současné době nepodporuje ladění. Jakmile k tomu dojde, budeme zkoumat, že do ní bude přidána podpora souběžného ladění. <br />

### <a name="platforms"></a>Platformy

| Typ aplikace nebo platformy | Sdílené ladění | Sdílení aplikací |
|-------------------|--------------|-------------|
| Arduino | ✅ | *NENÍ K DISPOZICI* |
| Azure App Service | ✅ | *NENÍ K DISPOZICI* |
| Azure Dev Spaces | ✅ | ✅ <sup>1</sup> |
| Azure Functions (místní a vzdálené) | ✅ | ✅ <sup>1</sup> |
| Blockchain (Ethereem) | ✅ | ✅ <sup>1</sup> |
| Konzola/CLI | ✅ | ✅ <sup>4</sup> |
| Databáze | <sup>5</sup> | ✅ <sup>1</sup> |
| Plocha (elektronická/nativní) | ✅ | <sup>9</sup> |
| Dynamics NAV 2018 | ✅ | ✅ <sup>1</sup> |
| Hry (Unity) | ✅ | <sup>9</sup> |
| Hry (Unreal) | ✅ | <sup>9</sup> |
| Kubernetes (YAML, Helm) | ✅ |  ✅ <sup>1</sup> |
| Markdown | *NENÍ K DISPOZICI* | ✅<sup>6</sup> |
| Mobilní (Cordova) | ✅ | ✅<sup>1, 7</sup> |
| Mobilní (nativní) | ✅ | <sup>9</sup> |
| Mobilní (reakce na nativní) | ✅ | ✅<sup>1, 8</sup> |
| Webová aplikace/rozhraní API (back-end) | ✅ | ✅ <sup>1</sup> |
| Webová aplikace (front-end) | ✅<sup>2</sup> . | ✅<sup>3</sup> . |
| Rozšíření VS Code | | <sup>9</sup> |

<sup>1</sup> prostřednictvím [sdílení místního serveru](../use/vscode.md#share-a-server).<br />
<sup>2</sup> ladění probíhá místo hosta v prohlížeči hostitele.<br />
<sup>3</sup> sdílení back-endu.<br />
<sup>4</sup> podporováno prostřednictvím sdílených terminálů.<br />
<sup>5</sup> uložených procesů databáze ladění není v současné době podporováno. <br />
<sup>6</sup> prostřednictvím "Preview". Obrázky se ale neprojeví kvůli známému problému. [Hlasujte ( 👍 ) zde.](https://github.com/MicrosoftDocs/live-share/issues/61)<br />
aplikace z <sup>7</sup> Cordova se dají sdílet přes platformu "prohlížeč".<br />
<sup>8</sup> reakci nativních aplikací můžete sdílet přes poutavou a [sdílené servery](../use/vscode.md#share-a-server).<br />
<sup>9</sup> Live Share v současné době nepodporuje sdílení oken nebo obrazovek. [Hlasujte ( 👍 ) zde.](https://github.com/MicrosoftDocs/live-share/issues/236)

## <a name="visual-studio"></a>Visual Studio

I když většina jazyků obsahuje určitou podporu jediného souboru, jsou níže uvedené upozornění. Všechny jazyky a platformy podporují společné úpravy. Zbývající část seznamu pokrývá pokročilé funkce, které jsou aktuálně bez dokončení, univerzální podpora:

### <a name="languages"></a>Jazyky

| Jazyk | Jazykové služby založené na jednom souboru | Jazykové služby pro nejrůznější aplikace | Co-Debugging |
|----------|-------------------------------|--------------------------------|--------------|
| C# | ✅ | ✅ | ✅ |
| CSHTML | ✅  <sup>1</sup> | | ✅ |
| ASPX | ✅ <sup>1</sup> |  | ✅ |
| HTML | ✅ | *NENÍ K DISPOZICI* | <sup>2</sup> |
| Šablony stylů CSS | ✅ | *NENÍ K DISPOZICI* | *NENÍ K DISPOZICI* |
| JavaScript a TypeScript | ✅ | ✅ | ✅<sup>3</sup> . |
| C++ | ✅ | ✅ | ✅ |
| Python | ✅ | | ✅ |
| Markdown | ✅ | *NENÍ K DISPOZICI* | *NENÍ K DISPOZICI* |
| PowerShell | ✅ | *NENÍ K DISPOZICI* | ✅ |
| VB.NET | ✅ | | ✅ |
| VBHTML | ✅ <sup>1</sup> | | ✅ |
| XAML | ✅ | *NENÍ K DISPOZICI* | <sup>4</sup> |
| SQL / T-SQL | ✅ | *NENÍ K DISPOZICI* | |
| F# | ✅ | | ✅ |
| R | ❌<sup>5</sup> . | *NENÍ K DISPOZICI* | ✅ |

<sup>1</sup> mezera: cshtml, vbhtml a aspx mají známé problémy s tím, že se podpora vloženého c#/VB souborů s kódem v c#/VB nevyřešila z důvodu neimplementace celé technologie IntelliSense. [Hlasujte ( 👍 ) zde na CSHTML/VBHTML.](https://github.com/MicrosoftDocs/live-share/issues/59) [Hlasujte ( 👍 ) tady na aspx.](https://github.com/MicrosoftDocs/live-share/issues/70)<br />
<sup>2</sup> vložený JavaScript ve formátu HTML je při ladění klienta podporován.<br />
<sup>3</sup> ladění JavaScriptu/TypeScript pro uzel nebo prohlížeč<br />
<sup>4</sup> , přestože samotný ladění XAML je technicky N/a, je podporováno ladění kódu na pozadí.<br />
<sup>5</sup> mezer: chyby služby jazyka R na straně hosta při připojení a po každém řádku. Nepodporováno [Hlasujte ( 👍 ) zde.](https://github.com/MicrosoftDocs/live-share/issues/72)<br />

### <a name="platforms"></a>Platformy

| Typ aplikace nebo platformy | Společné ladění | Sdílení aplikací |
|-------------------|--------------|-------------|
| Webová aplikace/rozhraní API (back-end) | ✅ | ✅ <sup>1</sup> |
| Webová aplikace (front-end) | ✅<sup>2</sup> . | ✅<sup>3</sup> . |
| Azure Functions | ✅  | ✅<sup>5</sup> . |
| Azure Service Fabric | ✅ | ✅<sup>5</sup> . |
| [Azure Dev Spaces](https://aka.ms/devspaces) | ✅ | ✅ <sup>1</sup> |
| Databáze | <sup>4</sup> | ✅<sup>5</sup> . |
| Konzola/CLI | ✅ | ✅<sup>6</sup> |
| Plocha (WinForms) | ✅ | |
| Plocha (WPF) | ✅ | |
| Univerzální platforma Windows | ✅ |  |
| Rozšíření VS | ✅ |  |

<sup>1</sup> prostřednictvím [sdílení místního serveru](../use/vs.md#share-a-server). ASP.NET Web Apps můžou používat taky [automatické sdílení webových aplikací](../use/vs.md#automatic-web-app-sharing).<br />
<sup>2</sup> ladění probíhá místo hosta v prohlížeči hostitele.<br />
<sup>3</sup> sdílení back-endu.<br />
<sup>4</sup> uložená procedura databáze ladění se momentálně nepodporuje. <br />
<sup>5</sup> prostřednictvím [sdílení místního serveru](../use/vs.md#share-a-server). <br />
<sup>6</sup> částečně podporováno prostřednictvím sdílených terminálů.<br />
<sup>?</sup> Dosud Neověřeno.

## <a name="see-also"></a>Viz také

- [Podpora rozšíření](extensions.md)
- [Požadavky na připojení pro Live Share](connectivity.md)
- [Funkce zabezpečení Live Share](security.md)
- [Všechny hlavní chyby, žádosti o funkce a omezení](https://aka.ms/vsls-issues)
- [Všechny požadavky a omezení funkcí](https://aka.ms/vsls-feature-requests)

Máte potíže? Podívejte se na článek o [odstraňování potíží](../troubleshooting.md) nebo nám [pošlete svůj názor](../support.md).
