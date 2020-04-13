---
title: Připojit se k rychlému startu – Visual Studio Live Share | Dokumenty společnosti Microsoft
description: Zkrácený návod při připojení k první relaci spolupráce visual studia Live Share.
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
ms.openlocfilehash: 7b8b3d9b566231f4b4205b559232ef1752fd9441
ms.sourcegitcommit: 6bf13781dc42a2bf51a19312ede37dff98ab33ea
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/09/2020
ms.locfileid: "79508569"
---
<!--
Copyright &copy; Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->


# <a name="quickstart-join-your-first-collaboration-session"></a>Úvodní příručka: Připojte se k první relaci spolupráce

Vítá vás Visual Studio Live Share! Rozšíření Live Share vám umožňuje upravovat a ladit v reálném čase společně s ostatními bez ohledu na to, jaké programovací jazyky používáte nebo jaké typy aplikací vytváříte. To vám umožní okamžitě a bezpečně připojit spoluhráče aktuální projekt, a pak podle potřeby, vstoupit do ladění relací, zobrazení a úpravy terminálových instancí, viz localhost webové aplikace, připojit hlasové hovory, a další!

Jste připraveni začít? Týmová spolupráce by měla být tak rychlá a přirozená, že je těžší to neudělat! Z tohoto důvodu visual studio live share usnadňuje začínáme, takže můžete bez problémů začít sdílet svou práci a nápady.

> [!TIP]
> Víte, že se můžete *připojit k vlastní relaci spolupráce*? Díky tomu si můžete Live Share vyzkoušet sami nebo můžete rozjet instanci Visual Studia nebo VS Code a vzdáleně se k ní připojit. U obou instancí můžete dokonce používat stejnou identitu. Vyzkoušejte to!

Stačí postupovat podle těchto kroků a připojit se k relaci spolupráce.

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
        <a href="https://aka.ms/vsls-dl/vscode" alt="Download button"><img src="../media/download.png"></a>
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

## <a name="2-optional-join-as-a-read-only-guest-in-vs-code"></a>2. [Volitelné] Připojte se jako host jen pro čtení v Kódu VS

V Kódu VS můžete po instalaci rozšíření Live Share, restartování a čekání na dokončení instalace závislostí přejít a připojit se k relaci spolupráce jako host jen pro čtení.

> [!NOTE]
> Pokud chcete provést úpravy kódu, ke kterým se připojujete, budete se muset přihlásit.

Otevřete (nebo znovu otevřete) odkaz na pozvánku v prohlížeči a dostanete oznámení, že prohlížeč chce spustit VS Code. Nechte ji spustit a začne se připojovat k relaci spolupráce.

Když se spustí VS Code, dostanete informační zprávu s žádostí o přihlášení. Chcete-li se k relaci připojit, vyberte možnost Pokračovat jako host jen pro čtení.

![Připojte se jako relace jako přípitek jen pro čtení](../media/vscode-read-only-guest.png)

Budete vyzváni k zadání zobrazované holce, které vám pomůže identifikovat vás v relaci.

![Jméno hosta jen pro čtení](../media/vscode-read-only-guest-name.png)

Poté budete připojeni k relaci jen pro čtení. Budete moci zobrazit a procházet kód, co-ladění a zobrazení sdílených serverů a terminálů (jen pro čtení).

> [!NOTE]
> Pokud chcete později získat přístup ke kódu pro čtení a zápis, můžete se přihlásit. Klikněte na své zobrazované jméno ve stavu, panelu a vyberte možnost "Přihlásit se".
![Přihlášení jen pro](../media/vscode-read-only-guest-signin.png) čtení: To to spustí váš prohlížeč a můžete si vybrat účet Microsoft nebo GitHub, pomocí kterých se chcete přihlásit.

## <a name="3-sign-in"></a>3. Přihlaste se

Po instalaci rozšíření Live Share, restartování a čekání na dokončení instalace závislostí (Kód VS) se budete chtít přihlásit, abyste ostatní účastníci věděli, kdo jste. Pokud tento krok přeskočíte, budete vyzváni k přihlášení během procesu připojení nebo se můžete připojit k relaci jako host jen pro čtení. Chcete-li začít, klepněte na položku stavového řádku "Live Share" (Kód VS) / "přihlásit se".

<table style="border: none;">
<tr style="border: none;">
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vscode-sign-in-button-new.png" width="100%" alt="Visual Studio Code sign in status bar item" />
    </td>
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vs-sign-in-button.png" width="100%" alt="Visual Studio sign in button"/>
    </td>
</tr>
</table>

Ve **VS Code**se váš prohlížeč spustí, zatímco se zobrazí oznámení s žádostí o přihlášení. Dokončete proces přihlášení ve vašem prohlížeči a po dokončení jednoduše zavřete prohlížeč.

![Informační zpráva s žádostí o přihlášení pomocí webového prohlížeče](../media/vscode-sign-in-toast.png)

> **Uživatelé Linuxu:** Pokud používáte starší verzi live share (v0.3.295 nebo nižší), můžete být vyzváni k zadání uživatelského kódu. Aktualizujte na nejnovější verzi rozšíření nebo klikněte na tlačítko "Potíže?" odkaz po přihlášení zobrazíte kód. Podrobnosti naleznete [zde](../use/vscode.md#sign-in-using-a-user-code).

V **sadě Visual Studio**live share automaticky používá váš účet [individuálního nastavení](https://docs.microsoft.com/en-us/visualstudio/ide/signing-in-to-visual-studio). V důsledku toho se můžete jednoduše přihlásit jako obvykle. Pokud však dáváte přednost použití jiného přihlašovacího účtu, než je váš účet přizpůsobení sady Visual Studio, přejděte na **účet Nástroje &gt; možnosti &gt; živého &gt; sdílení a** vyberte různá pověření.

Viz [řešení potíží,](../troubleshooting.md#sign-in) pokud stále řešíte problémy.

## <a name="4-openre-open-the-invite-link-in-a-browser"></a>4. Otevření/opětovné otevření odkazu pro pozvánku v prohlížeči

Nyní jednoduše otevřete (nebo znovu otevřete) odkaz na pozvánku v prohlížeči.

> **Poznámka:** Pokud jste rozšíření Live Share ještě nenainstalovali, zobrazí se odkazy na tržiště rozšíření. Nainstalujte rozšíření a restartujte nástroj a opakujte akci.

Měli byste být upozorněni, že prohlížeč chce spustit nástroj s podporou live share. Pokud necháte vybraný nástroj spustit, budete po spuštění připojeni k relaci spolupráce.

![Stránka připojit se](../media/join-page.png)

Pokud je hostitel offline, budete upozorněni v tomto okamžiku místo. Poté můžete kontaktovat hostitele a požádat ho, aby jej znovu sdílel.

> **Tip pro řešení potíží:** Při použití kódu VS se ujistěte, že jste **nástroj spustili alespoň jednou** po instalaci rozšíření a před otevřením/opětovným otevřením stránky s pozvánkou čekali na dokončení instalace závislostí (viz stavový řádek). Stále se nedaří? Podrobnosti najdete ručně, viz [spojení.](../reference/manual-join.md)

## <a name="5-collaborate"></a>5. Spolupracujte!

A to je vše! Za chvíli budete připojeni k relaci spolupráce svého kolegy. Ve výchozím nastavení hostitel automaticky přijímá osoby, které se připojují, ale pokud je hostitel nastaven tak, aby [vyžadoval schválení hosta,](../reference/security.md#requiring-guest-approval) zobrazí se stavový řádek / dialog o spojení, který uvádí, že Live Share čeká na hostitele, aby schválil vaši žádost o připojení.

> **Bezpečnostní tip:** Jako host, který se připojuje k relaci spolupráce, je důležité si uvědomit, že hostitelé mohou omezit váš přístup k určitým souborům nebo funkcím. Chcete porozumět bezpečnostním důsledkům některých funkcí a nastavení služby Live Share? Podívejte se na [bezpečnostní](../reference/security.md) článek.

Zde je několik věcí, které můžete vyzkoušet:

1. Pohybujte se po projektu nezávisle a provázte některé úpravy
2. Podívejte se na práci intellisense pro JavaScript, TypeScript a / nebo C# kód
3. Úprava společně s hostitelem
4. Sledujte hostitele a pohybujte se s ním při navigaci a úpravách v různých souborech
5. Spuštění společné relace ladění s hostitelem
6. Požádejte hostitele, aby sdílel server, abyste se mohli podívat na něco jako webovou aplikaci spuštěnou na jejich počítači
7. Požádejte hostitele, aby sdílel terminál a spouštěl některé příkazy.

Máte potíže? Podívejte se na článek o [odstraňování potíží](../troubleshooting.md) nebo nám [pošlete svůj názor](../support.md).

## <a name="next-steps"></a>Další kroky

Podívejte se na tyto další články pro více informací.

- [Úvodní příručka: Sdílení prvního projektu](share.md)
- [Postup: Spolupráce pomocí kódu sady Visual Studio](../use/vscode.md)
- [Postup: Spolupráce pomocí Sady Visual Studio](../use/vs.md)

Referenční informace

- [Požadavky na připojení pro Live Share](../reference/connectivity.md)
- [Funkce zabezpečení Live Share](../reference/security.md)
- [Podpora jazyků a platforem](../reference/platform-support.md)
- [Podpora rozšíření](../reference/extensions.md)
