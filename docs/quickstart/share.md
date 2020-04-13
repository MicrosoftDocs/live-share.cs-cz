---
title: Sdílet rychlý start – sdílení v sadě Visual Studio Live Share | Dokumenty společnosti Microsoft
description: Zkrácený návod na sdílení prvního projektu pomocí relace spolupráce visual studio live share.
ms.custom: ''
ms.date: 03/22/2018
ms.reviewer: ''
ms.suite: ''
ms.topic: quickstart
author: chuxel
ms.author: clantz
manager: AmandaSilver
ms.workload:
- liveshare
ms.openlocfilehash: e65656c604a9dbc479a03a503fe01d7e2d938072
ms.sourcegitcommit: 6bf13781dc42a2bf51a19312ede37dff98ab33ea
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/09/2020
ms.locfileid: "73170008"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="quickstart-share-your-first-project"></a>Úvodní příručka: Sdílení prvního projektu

Vítá vás Visual Studio Live Share! Rozšíření Live Share vám umožňuje upravovat a ladit v reálném čase společně s ostatními bez ohledu na to, jaké programovací jazyky používáte nebo jaké typy aplikací vytváříte. Umožňuje vám okamžitě a bezpečně sdílet váš aktuální projekt a pak podle potřeby sdílet ladicí relace, terminálové instance, webové aplikace místního hostitele, hlasové hovory a další věci.

Jste připraveni začít?  Týmová spolupráce by měla být tak rychlá a přirozená, že je těžší to neudělat! Z tohoto důvodu visual studio live share usnadňuje začínáme, takže můžete bez problémů začít sdílet svou práci a nápady.

> [!TIP]
> Víte, že se můžete *připojit k vlastní relaci spolupráce*? Díky tomu si můžete Live Share vyzkoušet sami nebo můžete rozjet instanci Visual Studia nebo VS Code a vzdáleně se k ní připojit. Můžete dokonce použít stejnou identitu v obou případech. Vyzkoušejte to!

Stačí postupovat podle těchto kroků a začít sdílet.
<!--
Change the instructions to Install extension for VS Code and in-tool for VS?
-->
## <a name="1-install-the-extension"></a>1. Nainstalujte rozšíření

Instalace rozšíření je snadná. Postupujte podle následujících kroků:

<table style="width: 100%; border:none;">
<tr>
    <td width="128px" style="width: 128px; text-align: center; border:none;"><img src="../media/vs-code.svg" width="128px" alt="Visual Studio Code logo"/></td>
    <td style="border:none;">
        <strong>Visual Studio Code (1.22.0+)</strong><br />
        1. Nainstalujte <a href="https://code.visualstudio.com/">Visual Studio Code</a> pro Windows (7, 8.1 nebo 10), macOS <b>(Sierra+)</b>, 64bitový Linux <b>(<a href="../use/vscode.md#installation">podrobnosti</a>)</b>.<br />
        2. Z marketplace si stáhněte a nainstalujte rozšíření Visual Studio Live Share. <br />
        3. Zvolte Znovu načíst a počkejte, až se stáhnou a nainstalují závislosti (sledujte stavový řádek).<br />
        4. <strong>Linux</strong>: Pokud se zobrazí výzva k <a href="../reference/linux.md#install-linux-prerequisites">instalaci knihoven</a>, klepněte na tlačítko Instalovat, zadejte heslo, restartujte VS Code po dokončení.<br />
        <a href="https://aka.ms/vsls-dl/vscode"><img src="../media/download.png" alt="Download button"></a>
    </td>
</tr>
<tr style="border:none;">
    <td width="128px" style="width: 128px; text-align: center; border:none;"><img src="../media/vs-ide-2019.svg" width="128px" alt="Visual Studio 2019 logo" /></td>
    <td  style="border:none;">
        <strong>Visual Studio 2019</strong><br />
        1.Nainstalujte <a href="https://visualstudio.microsoft.com/downloads/">Visual Studio 2019</a>.<br/>
        2.Nainstalujte <a href="../reference/platform-support.md">podporované úlohy</a>. (například ASP.NET, .NET Core, C++, Python a/nebo Node.js).<br />
        3. Visual Studio Live Share se standardně instaluje s těmito sadami funkcí. <br />
    </td>
</tr>
<tr style="border:none;">
    <td width="128px" style="width: 128px; text-align: center; border:none;"><img src="../media/vs-ide-2017.svg" width="128px" alt="Visual Studio 2017 logo" /></td>
    <td  style="border:none;">
        <strong>Visual Studio 2017 (verze 15.6 nebo vyšší)</strong><br />
        1.Nainstalujte nejnovější verzi <a href="https://visualstudio.microsoft.com/vs/older-downloads/">Visual Studia 2017</a> (15.6+) do Windows (7, 8.1 nebo 10).<br/>
        2.Nainstalujte <a href="../reference/platform-support.md">podporované úlohy</a>. (například ASP.NET, .NET Core, C++ a/nebo Node.js).<br />
        3. Z marketplace si stáhněte a nainstalujte rozšíření Visual Studio Live Share. <br />
        <a href="https://aka.ms/vsls-dl/vs"><img style="padding: 0; spacing: 0;" src="../media/download.png" alt="Download button" ></a><br />
    </td>
</tr>
</table>

Stažením a používáním rozšíření Visual Studio Live Share vyjadřujete souhlas s [licenčními podmínkami](https://aka.ms/vsls-license) a [prohlášením o zásadách ochrany osobních údajů](https://www.microsoft.com/en-us/privacystatement/EnterpriseDev/default.aspx). Pokud narazíte na problémy, podívejte se na článek o [odstraňování potíží](../troubleshooting.md).

## <a name="2-sign-in"></a>2. Přihlaste se

<!--
Re-write the grammar here- run on sentence does not make sense. Change screen shots. There is another way of signing in as well- what if a user goes directly to the start collaboration. 
-->
Po instalaci rozšíření Live Share, restartování a čekání na dokončení instalace závislostí (Kód VS) se budete chtít přihlásit, abyste ostatní účastníci věděli, kdo jste. Stačí kliknout na položku stavového řádku "Live Share" (Kód VS) / "Přihlásit se" (VS), abyste mohli začít.

<table style="border: none;">
<tr style="border: none;">
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vscode-sign-in-button-new.png" width="100%" alt="Visual Studio Code sign in status bar item"/>
    </td>
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vs-sign-in-button.png" width="100%" alt="Visual Studio sign in button"/>
    </td>
</tr>
</table>

Ve **VS Code**se váš prohlížeč spustí, zatímco se zobrazí oznámení s žádostí o přihlášení. Dokončete proces přihlášení ve vašem prohlížeči a po dokončení jednoduše zavřete prohlížeč.

![Informační zpráva s žádostí o přihlášení pomocí webového prohlížeče](../media/vscode-sign-in-toast.png)

> **Uživatelé Linuxu:** Pokud používáte starší verzi live share (v0.3.295 nebo nižší), můžete být vyzváni k zadání uživatelského kódu. Aktualizujte na nejnovější verzi rozšíření nebo klikněte na tlačítko "Potíže?" odkaz po přihlášení zobrazíte kód. Podrobnosti naleznete [zde](../use/vscode.md#sign-in-using-a-user-code).

V **sadě Visual Studio**live share automaticky používá váš účet [individuálního nastavení](https://docs.microsoft.com/en-us/visualstudio/ide/signing-in-to-visual-studio). V důsledku toho se můžete jednoduše přihlásit jako obvykle. Pokud však dáváte přednost použití jiného přihlášení než váš účet přizpůsobení sady Visual Studio, přejděte na **účet Nástroje &gt; možnosti &gt; živého sdílení &gt; a** vyberte různá pověření.

Viz [řešení potíží,](../troubleshooting.md#sign-in) pokud stále řešíte problémy.

## <a name="3-open-a-folder-project-or-solution"></a>3. Otevření složky, projektu nebo řešení

Normální pracovní postup použijte k otevření složky, projektu nebo řešení, které chcete sdílet v sadě Visual Studio nebo Visual Studio Code.

### <a name="4-optional-update-hidden-or-excluded-files"></a>4. [Volitelné] Aktualizace skrytých nebo vyloučených souborů

Ve výchozím nastavení live share **skryje** všechny soubory nebo složky odkazované v souborech .gitignore ve sdílených složkách před hosty. **Skrytí** souboru zabrání jeho zobrazení ve stromu souborů hosta. **Vyloučení** souboru platí přísnější pravidlo, které brání Live Share z otevření pro hosta v situacích, jako je přejít na definici, nebo pokud krok do souboru při ladění nebo je "následovat". Chcete-li skrýt nebo vyloučit různé soubory, lze do projektu přidat soubor **.vsls.json** s těmito nastaveními. Podrobnosti [najdete v tématu řízení přístupu k souborům a viditelnosti.](../reference/security.md#controlling-file-access-and-visibility)

## <a name="5-start-a-collaboration-session"></a>5. Zahájení relace spolupráce

<!--
-->
Dále jednoduše klikněte na tlačítko "Live Share" v nástroji a odkaz na pozvánku se automaticky zkopíruje do schránky.

<table style="border: none;">
<tr style="border: none;">
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vscode-share-button-new.png" width="100%" alt="Visual Studio Code share status bar item" />
    </td>
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vs-share-button.png" width="100%" alt="Visual Studio share button"/>
    </td>
</tr>
</table>

> [!NOTE]
> Software brány firewall plochy vás může požádat, aby agentovi Live Share povolil otevřít port při prvním sdílení. Přijetí je zcela volitelné, ale umožňuje zabezpečené "přímý režim" ke zlepšení výkonu, když osoba, se kterou pracujete, je ve stejné síti jako vy. Podrobnosti naleznete [v tématu změna režimu připojení.](../reference/connectivity.md#changing-the-connection-mode)

## <a name="6-optional-enable-read-only-mode"></a>6. [Volitelně] Povolit režim jen pro čtení

Po spuštění relace spolupráce můžete nastavit relaci jen pro čtení, abyste zabránili hostům v úpravách sdíleného kódu.

Po sdílení obdržíte oznámení, že odkaz na pozvánku byl zkopírován do schránky. Poté můžete vybrat možnost, aby byla relace jen pro čtení.

<table style="border: none;">
<tr style="border: none;">
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vscode-read-only-toast.png" width="100%" alt="Visual Studio Code read-only option" />
    </td>
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vs-read-only-notification.png" width="100%" alt="Visual Studio read-only option"/>
    </td>
</tr>
</table>

V **kódu VS**můžete také spustit relaci jen pro čtení na kartě Live Share viewlet.

![Informační zpráva s žádostí o přihlášení pomocí webového prohlížeče](../media/vscode-read-only-viewlet.png)

### <a name="7-send-someone-the-invite-link"></a>7. Poslat někomu odkaz na pozvánku

Pošlete odkaz přes e-mail, Slack, Skype atd. Otevření odkazu v prohlížeči jim umožňuje připojit se k relaci spolupráce, která sdílí obsah složky, projektu nebo řešení, které jste otevřeli. Upozorňujeme, že vzhledem k úrovni přístupu k relacím live share, které mohou hosté poskytnout, **byste měli sdílet pouze s lidmi, kterým důvěřujete,** a promyslet si důsledky toho, co sdílíte.

> **Bezpečnostní tip:** Chcete porozumět bezpečnostním důsledkům některých funkcí služby Live Share? Podívejte se na [bezpečnostní](../reference/security.md) článek.

Pokud má pozvaný host otázky, [článek Úvodní příručka: Připojte se k prvnímu](join.md) článku o zahájení relace poskytuje další informace o tom, jak hosta zprovoznit.

## <a name="8-optional-approve-the-guest"></a>8. [Nepovinné] Schválit hosta

Ve výchozím nastavení se hosté automaticky připojí k vaší relaci spolupráce a budete upozorněni, až budou připraveni s vámi spolupracovat.

<table style="border: none;">
<tr style="border: none;">
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vscode-join-notification.png" width="100%" alt="Visual Studio Code join notification" />
    </td>
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vs-join-notification.png" width="100%" alt="Visual Studio join notification"/>
    </td>
</tr>
</table>

Můžete se rozhodnout vyžadovat explicitní "schválení" pro každého, kdo se místo toho připojí. Pokud máte toto nastavení zapnuté, zobrazí se oznámení s výzvou ke schválení hosta při pokusu o připojení k relaci.

Podrobnosti o zapnutí této funkce naleznete [v části vyžadování schválení hostem.](../reference/security.md#requiring-guest-approval)

## <a name="9-collaborate"></a>9. Spolupracujte!

A to je vše! Po vstupu hosta do vás můžete vyzkoušet několik věcí:

1. Přecházat k různým souborům v projektu nezávisle a provést některé úpravy
1. Sledujte hosta a sledujte, jak se posouvají, dělají úpravy a přecházejí do různých souborů
1. Spuštění společné relace ladění s nimi
1. Sdílení serveru, abyste se mohli podívat na něco jako webovou aplikaci spuštěnou na jejich počítači
1. Sdílení terminálu a spuštění některých příkazů

Podívejte se na [Visual Studio Kód](../use/vscode.md) a Visual [Studio](../use/vs.md) rozšíření dokumenty informace o tom, jak provádět tyto akce a další.

Máte potíže? Podívejte se na článek o [odstraňování potíží](../troubleshooting.md) nebo nám [pošlete svůj názor](../support.md).

## <a name="next-steps"></a>Další kroky

Podívejte se na tyto další články pro více informací.

- [Úvodní příručka: Připojte se k první relaci spolupráce](join.md)
- [Postup: Spolupráce pomocí kódu sady Visual Studio](../use/vscode.md)
- [Postup: Spolupráce pomocí Sady Visual Studio](../use/vs.md)

Referenční informace

- [Požadavky na připojení pro Live Share](../reference/connectivity.md)
- [Funkce zabezpečení Live Share](../reference/security.md)
- [Podpora jazyků a platforem](../reference/platform-support.md)
- [Podpora rozšíření](../reference/extensions.md)
