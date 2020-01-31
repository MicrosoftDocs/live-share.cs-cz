---
title: Podrobnosti instalace pro Linux – Visual Studio Live Share | Microsoft Docs
description: Podrobné informace o instalaci Visual Studio Live Share v systému Linux.
ms.custom: ''
ms.date: 10/6/2018
ms.reviewer: ''
ms.suite: ''
ms.topic: reference
author: chuxel
ms.author: clantz
manager: AmandaSilver
ms.workload:
- liveshare
ms.openlocfilehash: 69bc178ebb4052757f984d67482d216335f46dac
ms.sourcegitcommit: 5180aab73c086cbded6aae01aa01f71fb991dee1
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2020
ms.locfileid: "76818073"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="linux-installation-details"></a>Podrobnosti instalace pro Linux

Linux je vysoce proměnlivé prostředí a s sheerm počtem desktopových prostředí a distribucí může být složitější, aby bylo možné pracovat. Pokud jste přistoupili k podporovaným verzím **desktopu Ubuntu Desktop** (16.04 +), **CentOS 7**nebo **Fedora Workstation** (27 +) a používáte pouze **oficiální distribuce vs Code**, měli byste proces rovnou dopředt. V případě, že používáte nestandardní konfiguraci nebo distribuci pro příjem dat, je však možné, že nebudete moci spustit hiccups. V tomto dokumentu najdete některé informace o požadavcích a některých podrobnostech k odstraňování potíží, které vám můžou pomáhat začít, i když je vaše konfigurace podporovaná jenom v komunitě. Upozorňujeme, že Live Share podporuje jenom **64 systému Linux**.

## <a name="install-linux-prerequisites"></a>Nainstalovat požadavky pro Linux

V některých distribucích systému Linux chybí knihovny Live Share musí fungovat. Ve výchozím nastavení se Live Share pokusí zjistit a nainstalovat požadavky systému Linux za vás. Zobrazí se informační zpráva, když Live Share narazí na problém, který může pocházet z chybějících knihoven, které vás požádají o oprávnění k jejich instalaci.

![Informační zprávy ukazující zprávu, že chybí předpoklady pro Linux](../media/vscode-linux-prereq-missing.png)

Po kliknutí na nainstalovat se zobrazí okno terminálu, kde se váš operační systém vyzve k zadání hesla správce/kořene (sudo), aby bylo možné pokračovat. Za předpokladu, že se skript úspěšně dokončí, znovu načtěte Visual Studio Code po zobrazení výzvy byste měli být nastaveni. Můžete také chtít vyzkoušet **[Tipy podle distribuce](#tips-by-distribution)** pro jiné tipy a alternativní řešení, pokud existují.

Pokud se zobrazí zpráva oznamující, že skript nepodporuje vaši distribuci, přečtěte si **[tipy pro distribuce s podporou komunity](#tips-for-unsupported-distros)** pro informace, které komunita sdílí s námi.

Pokud nechcete, **vs Code spustit příkaz**, můžete také kdykoli ručně spustit nejnovější verzi tohoto skriptu pomocí následujícího příkazu v okně terminálu:...

    wget -O ~/vsls-reqs https://aka.ms/vsls-linux-prereq-script && chmod +x ~/vsls-reqs && ~/vsls-reqs

## <a name="tips-by-distribution"></a>Tipy podle distribuce

I když výše uvedený instalační skript zahrnuje celou řadu distribucí, možná vás zajímá, co většinou v instalacích Vanilla chybí. V následujícím seznamu jsou uvedeny knihovny klíčů, které chybí v nové instalaci dané distribuce. V tomto seznamu najdete taky několik tipů, které vám pomůžou začít pracovat, pokud dojde k problému.

| Distribuce | Vanilla instalovat chybějící knihovny | Další kroky |
|--------|-------------------|----|
| Ubuntu Desktop 18,04 (64 bitů) | &lt;žádné&gt;  | &lt;žádné&gt; |
| Ubuntu Desktop 16,04 (64 bitů) | &lt;žádné&gt; | &lt;žádné&gt; |
| Kubuntu 18,04 (64 bitů) | `gnome-keyring desktop-file-utils` | &lt;žádné&gt; |
| Kubuntu 16,04 (64 bitů) | `gnome-keyring desktop-file-utils` | &lt;žádné&gt; |
| Xubuntu 18,04 (64 bitů) |&lt;žádné&gt;  | <ul><li>Zajistěte, aby se na kartě Upřesnit v části relace a spuštění kontrolovala možnost spustit GNOME služby při spuštění.</li><li>Pokud narazíte na potíže s přihlašováním, nainstalujte `seahorse`, spusťte "hesla a klíče", ověřte, že máte k dispozici "přihlašovací" a že ho můžete odemknout.</li></ul> |
| Xubuntu 16,04 (64 bitů) | &lt;žádné&gt; | <ul><li>Zajistěte, aby se na kartě Upřesnit v části relace a spuštění kontrolovala možnost spustit GNOME služby při spuštění.</li><li>Pokud narazíte na potíže s přihlašováním, nainstalujte `seahorse`, spusťte "hesla a klíče", ověřte, že máte k dispozici "přihlašovací" a že ho můžete odemknout.</li></ul> |
| Mentolová 19 Cinnamon (64 bitů) | &lt;žádné&gt;  | &lt;žádné&gt; |
| Mentolová 18,3 Cinnamon (64 bitů) | &lt;žádné&gt;  | &lt;žádné&gt; |
| Testování Debian 10 (Buster) (64 bitů) | Verze není stabilní, proto je neznámá. | <ul><li>Testování Debian a nestabilní (SID) se oficiálně nepodporují.</li><li>V rozhraní .NET Core je [známý problém](https://github.com/dotnet/corefx/issues/33179) , který má vliv na Live Share. </li><li>[Alternativní řešení najdete tady](https://github.com/dotnet/corefx/issues/33179#issuecomment-435118249).</li></ul> |
| Debian 9 desktop GNOME (64 bitů) | &lt;žádné&gt; | <ul><li>Možná budete muset nainstalovat `sudo` a přidat uživatele do skupiny sudo, abyste mohli použít automatizovaný instalační skript.</li>  |
| Fedora Workstation 29 (64 bitů) | `openssl-compat10` | &lt;žádné&gt; |
| Fedora Workstation 28 (64 bitů) | &lt;žádné&gt; | &lt;žádné&gt; |
| Fedora Workstation 27 (64 bitů) | &lt;žádné&gt; | &lt;žádné&gt; |
| CentOS 7 GNOME Desktop (64 bitů) | &lt;žádné&gt; | &lt;žádné&gt; |

V tématu **[tipy pro distribuce podporované komunitou](#tips-for-community-supported-distros)** najdete informace o dalších distribucích, která nejsou Debian/Ubuntu nebo RHL.

Další podrobnosti najdete také [níže](#detailed-library-requirements) v konkrétní knihovně Live Share potřeby.

<a name="tips-for-unsupported-distros"></a>

## <a name="tips-for-community-supported-distros"></a>Tipy pro komunitu podporovanou distribuce

Distribuce mimo Debian/Ubuntu nebo RHL stromy nejsou oficiálně podporovány Visual Studio Code nebo .NET Core. Proto nejsou podle přípony oficiálně podporovány Visual Studio Live Share ani. Komunita ale přispěla k nějakým užitečným informacím o tom, jak se Live Share v řadě dalších distribucí a provozovat.

> **PR Welcome:** Pokud vás zajímá aktualizace těchto informací s vaší oblíbenou distribucí, odešlete žádost o přijetí změn pro [Tento soubor](https://github.com/MicrosoftDocs/live-share/tree/master/docs/reference/linux.md) v úložišti GitHub docs. Ještě lepší, pokud byste chtěli získat instalační program závislosti, který podporuje vaši oblíbenou distribuci, můžete [pro tento soubor](https://github.com/MicrosoftDocs/live-share/blob/master/scripts/linux-prereqs.sh)odeslat žádost o přijetí změn.

| Distribuce | Práce? | Vanilla instalovat chybějící knihovny | Další kroky |
|--------------|----------|-------------------|------------------|
| Oblouk Linux (64 bitů) | Ano | Se liší. Možné knihovny: `gcr liburcu openssl-1.0 krb5 zlib icu gnome-keyring libsecret desktop-file-utils xorg-xprop` | <ul><li>Podporováno [instalačním skriptem předpokladů](#install-linux-prerequisites).</li><li>Použijte balíček [Visual Studio-Code-bin](https://aur.archlinux.org/packages/visual-studio-code-bin) AUR pro vs Code.</li><li>pro použití automatizovaného instalačního skriptu pro instalaci bude nutné nainstalovat `sudo`.</li><li>`gnome-keyring` může vyžadovat další [kroky nastavení](https://wiki.archlinux.org/index.php/GNOME/Keyring) v některých desktopových prostředích.</ul> |
| Manjaro 17,1 (64 bitů) | Ano | `xorg-xprop liburcu` | <ul><li>Podporováno [instalačním skriptem předpokladů](#install-linux-prerequisites).</li><li>Použijte balíček [Visual Studio-Code-bin](https://aur.archlinux.org/packages/visual-studio-code-bin) AUR pro vs Code.</li></ul> |
| openSuSE – 64 – 15 tam (bitů) | Ano | `libopenssl1_0_0 gnome-keyring` | <ul><li>Podporováno instalačním skriptem předpokladů.</li></ul> |
| SOLUS 3 (64 bitů) | Ano | `xprop` | <ul><li>Podporováno [instalačním skriptem předpokladů](#install-linux-prerequisites).</li><li>Verze balíčku `vscode` před verzí 57 postrádá požadované hodnoty Product. JSON ([viz níže](#vs-code-oss-issues)). Pokud chcete tento problém vyřešit, upgradujte balíček `vscode`.</li></ul> |
| Gentoo (64 bitů) | Ano | Vysoce proměnlivá proměnná. Možné chybějící balíčky: `dev-libs/openssl-1.0.2 net-libs/libgsasl dev-libs/icu sys-libs/zlib sys-apps/util-linux app-crypt/libsecret gnome-base/gnome-keyring x11-apps/xprop`| <ul><li>Je známo, že balíček `visual-studio-code` v překrytí **jorgicio** funguje.</li></ul>

## <a name="install-prerequisites-manually"></a>Nainstalovat požadavky ručně

 I když doporučujeme použít skript pro **instalaci závislostí**Live Share, v této části najdete další podrobnosti o požadavcích knihovny v události, kterou chcete provést, nebo když používáte distribuci, kterou skript nepodporuje.

Typické chybějící knihovny v instalacích Vanilla najdete v části [Tipy podle distribuce](#tips-by-distribution) a [tipů pro oddíly podporované pro distribuci komunitou](#tips-for-unsupported-distros) .

### <a name="detailed-library-requirements"></a>Podrobné požadavky knihovny

Požadavky na nativní knihovny Visual Studio Live Share pocházejí ze svého použití .NET Core 2,1, libsecret k uchování přihlašovacích údajů a integrace prohlížeče. Následující tabulka shrnuje tyto požadavky pro distribuci oficiálně podporované .NET Core.

| Distribuce | .NET Core reqs | Reqs úložiště přihlašovacích údajů| Reqs integrace prohlížeče |
|--------------|-----------|--------------------|------------|
| Ubuntu a distribuce pro podřízené | `libssl1.0.0 libkrb5-3 zlib1g libicu55` (pro Ubuntu 16,04, mentolová 18,3) nebo `libicu57` (pro Ubuntu 17,10) nebo `libicu60` (pro Ubuntu 18,04, mentolová 19) | `libsecret-1-0 gnome-keyring` (nebo libsecret support KWallet nepodporuje libsecret) | `desktop-file-utils x11-utils` |
| Debian 9 a distribuce po podřízeném | `libssl1.0.2 libkrb5-3 zlib1g libicu57` | `libsecret-1-0 gnome-keyring` (nebo libsecret support KWallet nepodporuje libsecret) | `desktop-file-utils x11-utils` |
| RHL/CentOS/Fedora | `openssl-libs krb5-libs zlib libicu` Fedora také vyžaduje `compat-openssl10`| `libsecret gnome-keyring` (nebo libsecret support KWallet nepodporuje libsecret) | `desktop-file-utils xorg-x11-utils` |
| Alpine Linux | `openssl1.0 icu krb5 zlib` | `libsecret gnome-keyring` (nebo libsecret support KWallet nepodporuje libsecret) | `desktop-file-utils xprop`

I když jiné distribuce vyžadují stejné knihovny, jejich názvy balíčků se můžou lišit. Některé z těchto tipů najdete v části [tipy pro distribuce podporované komunitou](#tips-for-unsupported-distros) .

### <a name="debian--ubuntu"></a>Debian/Ubuntu

Knihovny mohou být nainstalovány v Debian/Ubuntu na distribuci na základě spuštění `sudo apt install <library-name>` v terminálu.

U distribucí založených na Ubuntu, včetně mentolová, spusťte:

    sudo apt install libssl1.0.0 libkrb5-3 zlib1g libicu[0-9][0-9] gnome-keyring libsecret-1-0 desktop-file-utils x11-utils

Pro distribuce Debian 9 a Ubuntu pro příjem dat spusťte:

    sudo apt install libssl1.0.2 libkrb5-3 zlib1g libicu57 gnome-keyring libsecret-1-0 desktop-file-utils x11-utils

### <a name="fedora--centos--rhl"></a>Fedora/CentOS/RHL

Knihovny mohou být nainstalovány v Fedora/CentOS/RHL distribucí na základě spuštění `sudo yum install <library-name>` v terminálu. Například se nainstaluje vše:

    sudo yum install openssl-libs compat-openssl10 krb5-libs zlib libicu libsecret gnome-keyring desktop-file-utils xorg-x11-utils

## <a name="vs-code-oss-issues"></a>VS Code problémy OSS

> **Manjaro uživatelé platformy Linux/:** K tomuto problému se vyhnete pomocí balíčku AUR [Visual-Studio-bin](https://aur.archlinux.org/packages/visual-studio-code-bin) .

Balíčky Visual Studio Code, které jsou buď Vanilla nebo upravené verze VS Code OSS, můžou v `product.json` souboru chybět kritickou hodnotu, která brání Visual Studio Live Share aktivaci.

Rychlý způsob, jak zjistit, že se můžete setkat s tímto problémem, je přejít na help > "přepínat Vývojářské nástroje" a podívat se, jestli jste nenašli trasování zásobníku, které indikuje, že rozšíření Live Share nebylo aktivováno, protože používalo navržené rozhraní API.

Pokud chcete ověřit, že se jedná o váš problém, zkontrolujte obsah `product.json`. Umístění souboru se liší podle balíčku, ale obvykle je v jednom z následujících umístění:

- `/usr/share/code/resources/app/product.json`
- `/usr/share/vscode/resources/app/product.json`

Pokud vlastnost `extensionAllowedProposedApi` chybí nebo pokud se vám nezobrazuje "MS-vsliveshare. vsliveshare", používá se k tomuto problému verze OSS.

Jako **alternativní řešení**můžete do Product. JSON přidat následující:

        "extensionAllowedProposedApi": [
          "ms-vsliveshare.vsliveshare",
          "ms-vscode.node-debug",
          "ms-vscode.node-debug2"
     ]

Další podrobnosti o tom, jestli je distribuce, kterou používáte, je [podrobnější.](#tips-for-community-supported-distros)

## <a name="linux-browser-integration"></a>Integrace s prohlížečem Linux

Visual Studio Live Share obvykle **nevyžaduje další kroky instalace** , aby bylo možné povolit integraci prohlížeče na platformě Linux.

K tomu Live Share při prvním inicializaci rozšíření automaticky umístit desktopový soubor do `~/.local/share/applications` a požadovanou spouštěcí spouštěč v `~/.local/share/vsliveshare`. V případě úspěchu není vyžadována žádná akce.

V některých případech distribuce buď nepodporují toto umístění, nebo vyžaduje, aby nástroj pro práci s Vanilla instalací nevyžadoval Nástroj pro vylepšení. V těchto případech se Live Share místo toho vrátí k použití `/usr/local/share`. V důsledku toho se může stát, že se k dokončení procesu instalace **vyžaduje heslo správce (sudo)** . Zobrazí se okno terminálu s oznámením, kde se bude instalovat spouštěč prohlížeče. Po zobrazení výzvy zadejte heslo a stiskněte klávesu ENTER, až se instalace dokončí, aby se okno terminálu zavřelo.

Pokud místo toho chcete spustit příkaz sami, můžete místo toho kliknout na Kopírovat místo toho, aby se příkaz terminálu zkopíroval do schránky.

Nakonec, pokud se rozhodnete tento krok úplně přeskočit, můžete se k [relacím na spolupráci připojit ručně](../use/vscode.md#join-manually), ale nebudete se moci připojit otevřením odkazu pro pozvání v prohlížeči. Všimněte si, že můžete kdykoli znovu získat přístup k příkazu, a to tak, že podržíte **kombinaci kláves CTRL + SHIFT + P/Cmd + Shift + P** a vyberete příkaz "Live Share: spouštěcí program spouštěče".

## <a name="see-also"></a>Viz také:

- [Postupy: spolupráce pomocí Visual Studio Code](../use/vscode.md)
- [Požadavky na připojení pro Live Share](connectivity.md)
- [Funkce zabezpečení Live Share](security.md)

Máte potíže? Podívejte se na článek o [odstraňování potíží](../troubleshooting.md) nebo nám [pošlete svůj názor](../support.md).
