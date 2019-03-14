---
title: Podrobnosti o instalaci Linux – Visual Studio Live Share | Dokumentace Microsoftu
description: Podrobné informace o instalaci Visual Studio Live Share v Linuxu.
ms.custom: ''
ms.date: 10/6/2018
ms.reviewer: ''
ms.suite: ''
ms.technology:
- liveshare
ms.topic: reference
author: chuxel
ms.author: clantz
manager: AmandaSilver
ms.workload:
- liveshare
ms.openlocfilehash: 013eb234e5acca02a39e90f0697a146039bb2a89
ms.sourcegitcommit: 4f733c9053848f26da03d47050bcb734f6c98b31
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/02/2019
ms.locfileid: "57254825"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="linux-installation-details"></a>Podrobné informace o instalaci systému Linux

Je velmi proměnlivé prostředí na systémy Linux a k velkému počtu desktopové prostředí a distribuce může být složité začít pracovat. Pokud zůstanou podporovaných verzích **Ubuntu Desktop** (16.04 +), **CentOS 7**, nebo **Fedora pracovní stanice** (27 +) a pouze použití **oficiální distribuce VS Kód**, měli byste najít proces přímočaré. V případě, že používáte nestandardní konfiguraci nebo podřízené distribuce, ale může nebo nemusí narazíte na nějaké bude odolný vůči kolísání. Tento dokument obsahuje některé informace o požadavcích a některé podrobnosti o řešení potíží, které vám můžou pomoct rychle zprovoznit a spuštění i v případě, že je konfigurace je pouze komunita podporováno. Všimněte si, že Live Share podporuje pouze **64-bit Linux**.

## <a name="install-linux-prerequisites"></a>Nainstalujte požadavky pro Linux

Některých distribucích systému Linux jsou chybějící knihovny, Live Share musí fungovat. Ve výchozím nastavení Live Share pokusí rozpoznat a nainstalujte požadavky pro Linux za vás. Zobrazí se vám oznámení s informační zprávou při Live Share dojde k potížím, které můžou pocházet z chybějící knihovny, která žádá o oprávnění k instalaci.

![Informační zprávy oznámení zobrazující chybí požadavky na Linuxu](../media/vscode-linux-prereq-missing.png)

Po kliknutí na "Instalaci" okně terminálu se zobrazí, kde váš operační systém vás vyzve k zadejte váš správce / root (sudo) heslo, abyste mohli pokračovat. Předpokládáme, že úspěšném dokončení skriptu a znovu načíst Visual Studio Code po zobrazení výzvy, které by měl být nastavené! Můžete také zkontrolovat **[tipy distribucí](#tips-by-distribution)** jiných pomocných parametrů a alternativní řešení, pokud nějaké existují.

Pokud se zobrazí zpráva, skript nepodporuje vaší distribuci, naleznete v tématu **[tipy pro komunity podporované distribuce](#tips-for-unsupported-distros)** informace komunita sdílí s námi.

Pokud jste **nechcete mít VS Code, spusťte příkaz pro vás**, můžete se také rozhodnout k opětovnému spuštění nejnovější verze tohoto skriptu kdykoli ručně pomocí následujícího příkazu v okně terminálu:

    wget -O ~/vsls-reqs https://aka.ms/vsls-linux-prereq-script && chmod +x ~/vsls-reqs && ~/vsls-reqs

## <a name="tips-by-distribution"></a>Tipy distribucí

V průběhu instalace požadovaného softwaru skript výše zahrnuje celou řadu distribucí, vás může zajímat, co je obvykle chybějící z vanilla instalací. Následující seznam obsahuje klíčové knihoven, které chyběly v čerstvou instalaci dané distribuce. Seznam obsahuje také některé tipy, které vám pomůžou začít pracovat Pokud dosáhnete problém.

| Distribuce | Vanilla nainstalujte chybějící knihovny | Další kroky |
|--------|-------------------|----|
| Ubuntu Desktop 18.04 (64 bitů) | &lt;None&gt;  | &lt;None&gt; |
| Desktop Ubuntu 16.04 (64 bitů) | &lt;None&gt; | &lt;None&gt; |
| Kubuntu 18.04 (64 bitů) | `gnome-keyring desktop-file-utils` | &lt;None&gt; |
| Kubuntu 16.04 (64 bitů) | `gnome-keyring desktop-file-utils` | &lt;None&gt; |
| Xubuntu 18.04 (64 bitů) |&lt;None&gt;  | <ul><li>Zajištění "spuštění služby GNOME při spuštění" se změnami na kartě "Pokročilé" z "A spuštění relace".</li><li>Pokud narazíte na potíže při přihlašování, nainstalujte `seahorse`, start "hesla a klíčů. Zkontrolujte, máte"Login"klíčů a, můžete ji odemknout.</li></ul> |
| Xubuntu 16.04 (64 bitů) | &lt;None&gt; | <ul><li>Zajištění "spuštění služby GNOME při spuštění" se změnami na kartě "Pokročilé" z "A spuštění relace".</li><li>Pokud narazíte na potíže při přihlašování, nainstalujte `seahorse`, start "hesla a klíčů. Zkontrolujte, máte"Login"klíčů a, můžete ji odemknout.</li></ul> |
| Mint 19 skořice (64 bitů) | &lt;None&gt;  | &lt;None&gt; |
| Mint 18.3 skořice (64 bitů) | &lt;None&gt;  | &lt;None&gt; |
| Debian 10 (Buster) testování (64 bitů) | Verze není stabilní, takže neznámý. | <ul><li>Debian testování a Unstable (Sid) nejsou oficiálně podporované.</li><li>Je [známý problém](https://github.com/dotnet/corefx/issues/33179) v .NET Core, který má vliv Live Share. </li><li>Zobrazit [zde jeho řešení](https://github.com/dotnet/corefx/issues/33179#issuecomment-435118249).</li></ul> |
| Debian Desktop 9 GNOME (64 bitů) | &lt;None&gt; | <ul><li>Je potřeba nainstalovat `sudo` a přidání uživatelů do skupiny sudo pomocí skriptu pro automatickou instalaci.</li>  |
| Pracovní stanice fedora 29 (64 bitů) | `openssl-compat10` | &lt;None&gt; |
| Pracovní stanice fedora 28 (64 bitů) | &lt;None&gt; | &lt;None&gt; |
| Pracovní stanice fedora 27 (64 bitů) | &lt;None&gt; | &lt;None&gt; |
| Desktop GNOME centOS 7 (64 bitů) | &lt;None&gt; | &lt;None&gt; |

Zobrazit **[tipy pro komunity podporované distribuce](#tips-for-community-supported-distros)** informace o jiných než Debian / Ubuntu nebo RHL distribucích založených na.

Další podrobnosti najdete také [níže](#detailed-library-requirements) na konkrétní knihovny Live Share potřebuje.

<a name="tips-for-unsupported-distros"></a>

## <a name="tips-for-community-supported-distros"></a>Tipy pro komunitu podporované distribuce

Distribuce mimo Debian / Ubuntu nebo RHL stromů nejsou oficiálně podporován ve Visual Studio Code nebo .NET Core. Proto při rozšíření i pro nepodporují oficiálně Visual Studio Live Share buď. Společenství však přispěl některé užitečné informace o Live Share zprovoznění na celé řadě dalších distribucí.

> **Vítejte v žádosti o přijetí změn:** Pokud vás zajímá aktualizaci těchto informací vaší oblíbené distribuce, odešlete žádost o přijetí změn pro [tento soubor](https://github.com/MicrosoftDocs/live-share/tree/master/docs/reference/linux.md) v úložišti Githubu naší dokumentace. Ještě lepší, pokud chcete získat instalační program závislosti, které podporuje vaše oblíbené distribuce, můžete odeslat žádost o přijetí změn [pro tento soubor](https://github.com/MicrosoftDocs/live-share/blob/master/scripts/linux-prereqs.sh).

| Distribuce | Práce? | Vanilla nainstalujte chybějící knihovny | Další kroky |
|--------------|----------|-------------------|------------------|
| Arch Linux (64 bitů) | Ano | Se liší. Je to možné knihovny: `gcr liburcu openssl-1.0 krb5 zlib icu gnome-keyring libsecret desktop-file-utils xorg-xprop` | <ul><li>Nepodporuje [skriptů předpoklad instalace](#install-linux-prerequisites).</li><li>Použití [visual studio code bin](https://aur.archlinux.org/packages/visual-studio-code-bin) AUR balíček pro VS Code.</li><li>`sudo` potřebujete k instalaci použít automatizované kontrolu požadovaných součástí nainstaluje skriptu.</li><li>`gnome-keyring` může vyžadovat další [kroků nastavení](https://wiki.archlinux.org/index.php/GNOME/Keyring) v některých prostředích klasické pracovní plochy.</ul> |
| Manjaro 17.1 (64 bitů) | Ano | `xorg-xprop liburcu` | <ul><li>Nepodporuje [skriptů předpoklad instalace](#install-linux-prerequisites).</li><li>Použití [visual studio code bin](https://aur.archlinux.org/packages/visual-studio-code-bin) AUR balíček pro VS Code.</li></ul> |
| openSuSE SKOK KDE 15 (64 bitů) | Ano | `libopenssl1_0_0 gnome-keyring` | <ul><li>Podporuje skriptů předpoklad instalace.</li></ul> |
| Solus 3 (64 bitů) | Ano | `xprop` | <ul><li>Nepodporuje [skriptů předpoklad instalace](#install-linux-prerequisites).</li><li>Verze `vscode` byly chybí balíček. před vydáním verze 57 product.json požadované hodnoty ([viz níže](#vs-code-oss-issues)). Upgrade `vscode` balíčku k vyřešení tohoto problému.</li></ul> |
| Gentoo (64 bitů) | Ano | Velmi proměnlivá. Je to možné chybějící balíčky: `dev-libs/openssl-1.0.2 net-libs/libgsasl dev-libs/icu sys-libs/zlib sys-apps/util-linux app-crypt/libsecret gnome-base/gnome-keyring x11-apps/xprop`| <ul><li>`visual-studio-code` Zabalíte **jorgicio** překrytí se označuje práci.</li></ul>

## <a name="install-prerequisites-manually"></a>Instalace požadovaných součástí ručně

 Přestože doporučujeme používat Live Share **závislosti nainstalujete skript**, tato část obsahuje další podrobnosti o požadavky knihoven v případě, že chcete, proveďte tyto kroky nebo používáte distribuci, nejsou podporovány skript.

Typické chybějící knihovny v vanilla instalacích najdete v [tipy distribucí](#tips-by-distribution) a [tipy pro komunity podporované distribuce](#tips-for-unsupported-distros) oddíly.

### <a name="detailed-library-requirements"></a>Požadavky na podrobné knihovny

Visual Studio Live Share na nativní knihovnu požadavky pocházejí z jeho použití .NET Core 2.1 libsecret k uchování přihlašovacích údajů a jejích prostředí integration prohlížeče. Následující tabulka shrnuje tyto požadavky pro distribuce oficiálně podporované pomocí .NET Core.

| Distribuce | .NET core na systém | Přihlašovací údaje Storage na systém| Integrace prohlížeče na systém |
|--------------|-----------|--------------------|------------|
| Ubuntu a podřízené distribuce | `libssl1.0.0 libkrb5-3 zlib1g libicu55` (Ubuntu 16.04 Mátová 18.3) nebo `libicu57` (pro Ubuntu 17.10) nebo `libicu60` (Ubuntu 18.04 Mátová 19) | `libsecret-1-0 gnome-keyring` (nebo klíčů podporovány libsecret – Kwallet nepodporuje libsecret) | `desktop-file-utils x11-utils` |
| Distribuce debian 9 a příjem dat | `libssl1.0.2 libkrb5-3 zlib1g libicu57` | `libsecret-1-0 gnome-keyring` (nebo klíčů podporovány libsecret – Kwallet nepodporuje libsecret) | `desktop-file-utils x11-utils` |
| RHL / CentOS / Fedora | `openssl-libs krb5-libs zlib libicu` Fedora také vyžaduje. `compat-openssl10`| `libsecret gnome-keyring` (nebo klíčů podporovány libsecret – Kwallet nepodporuje libsecret) | `desktop-file-utils xorg-x11-utils` |
| Nástroj Alpine Linuxu | `openssl1.0 icu krb5 zlib` | `libsecret gnome-keyring` (nebo klíčů podporovány libsecret – Kwallet nepodporuje libsecret) | `desktop-file-utils xprop`

Zatímco jiné distribuce vyžadují stejné knihovny, jejich názvy balíčků se může lišit. Můžete najít některé z nich najdete v [tipy pro komunity podporované distribuce](#tips-for-unsupported-distros) oddílu.

### <a name="debian--ubuntu"></a>Debian / Ubuntu

Knihovny může být nainstalována distribuce Debian nebo Ubuntu na základě spuštěním `sudo apt install <library-name>` v terminálu.

Pro distribuce založenou na Ubuntu včetně Mint spusťte:

    sudo apt install libssl1.0.0 libkrb5-3 zlib1g libicu[0-9][0-9] gnome-keyring libsecret-1-0 desktop-file-utils x11-utils

Debian 9 a podřízené distribucí mimo Ubuntu spusťte:

    sudo apt install libssl1.0.2 libkrb5-3 zlib1g libicu57 gnome-keyring libsecret-1-0 desktop-file-utils x11-utils

### <a name="fedora--centos--rhl"></a>Fedora / CentOS / RHL

Knihovny může být nainstalována Fedora nebo CentOS/RHL na základě distribuce spuštěním `sudo yum install <library-name>` v terminálu. Například tím se nainstaluje všechno, co:

    sudo yum install openssl-libs compat-openssl10 krb5-libs zlib libicu libsecret gnome-keyring desktop-file-utils xorg-x11-utils

## <a name="vs-code-oss-issues"></a>VS Code OSS problémy

> **Arch Linux/Manjaro uživatele:** Použití [visual-studio-bin](https://aur.archlinux.org/packages/visual-studio-code-bin) AUR balíček tomuto problému zabráníte tak.

Balíčky Visual Studio Code, které jsou buď vanilla nebo upraveny verze VS Code OSS může chybět kritická hodnota v `product.json` soubor, který brání aktivaci Visual Studio Live Share.

Rychlý způsob, jak zobrazit, může se tím tento problém je přejít do nápovědy > "Přepínací tlačítko vývojářské nástroje" a zda je najít trasování zásobníku, která rozšíření Live Share nezdařila aktivace protože díky "Navrhovaných API."

Pokud chcete ověřit, to je problém, zkontrolujte obsah `product.json`. Umístění souboru se liší podle balíček, ale je obvykle v jednom z následujících umístění:

- `/usr/share/code/resources/app/product.json`
- `/usr/share/vscode/resources/app/product.json`

Pokud `extensionAllowedProposedApi` chybí vlastnost nebo se nezobrazí "ms-vsliveshare.vsliveshare" odkazuje, se používá verzi OSS s tímto problémem.

Jako **řešení**, můžete přidat následující kód do product.json:

        "extensionAllowedProposedApi": [
          "ms-vsliveshare.vsliveshare",
          "ms-vscode.node-debug",
          "ms-vscode.node-debug2"
     ]

Zobrazit [nad](#tips-for-community-supported-distros) najdete další podrobnosti o Určuje, zda se distribuce používáte označuje práci.

## <a name="linux-browser-integration"></a>Linux integration prohlížeče

Visual Studio Live sdílet obvykle **nevyžaduje další instalační kroky** se povolit integraci prohlížeče v Linuxu.

Live Share jak toho dosáhnout, je automaticky umístí soubor plochy v `~/.local/share/applications` a požadované Spouštěč sám v `~/.local/share/vsliveshare` při prvním inicializuje rozšíření. Pokud se toto povede vaší nevyžaduje žádné akce.

V některých případech může distribuce buď toto umístění ani nevyžaduje vylepšení zobrazíte ho na spolupráci s jejich vanilla nainstaluje. V těchto případech Live Share přejde k použití `/usr/local/share` místo. V důsledku toho **můžete být upozorněni, že vaše heslo správce (sudo) je vyžadována** k dokončení procesu instalace. Okno terminálu se zobrazí informující o nainstalovanou Spouštěč prohlížeče. Jednoduše zadejte svoje heslo po zobrazení výzvy a stisknutím klávesy enter po dokončení instalace zavřete okno terminálu.

Pokud chcete spustit příkaz, sami místo toho, klikněte na tlačítko "Zkopírujte místo" které příkazu terminálu zkopíruje do schránky. místo toho.

Nakonec, pokud se rozhodnete zcela Přeskočit tento krok, můžete ji [ručně připojit k relacím spolupráci](../use/vscode.md#join-manually), ale nebudete moci připojit k tak, že v prohlížeči otevřete odkaz na pozvánku. Všimněte si, že budete mít vždy příkaz znovu později přístup, tím, že kliknete **Ctrl + Shift + P / Cmd + Shift + P** a vyberete "živé sdílené složky: Příkaz pro nastavení Spouštěč".

## <a name="see-also"></a>Viz také:

- [Postupy: Spolupráce pomocí Visual Studio Code](../use/vscode.md)
- [Požadavky na připojení pro Live Share](connectivity.md)
- [Funkce zabezpečení Live Share](security.md)

Máte potíže? Podívejte se na článek o [odstraňování potíží](../troubleshooting.md) nebo nám [pošlete svůj názor](../support.md).
