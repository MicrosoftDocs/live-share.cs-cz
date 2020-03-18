---
title: Rychlý Start – Visual Studio Live Share | Microsoft Docs
description: Zkrácený návod k připojení první Visual Studio Live Share relace spolupráce.
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
ms.sourcegitcommit: 382f069abbd81ed258d497a974b30379be36b4f0
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "79508569"
---
<!--
Copyright &copy; Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->


# <a name="quickstart-join-your-first-collaboration-session"></a>Rychlý Start: připojení první relace spolupráce

Vítá vás Visual Studio Live Share! Rozšíření Live Share vám umožňuje upravovat a ladit v reálném čase společně s ostatními bez ohledu na to, jaké programovací jazyky používáte nebo jaké typy aplikací vytváříte. Umožňuje okamžité a zabezpečené připojení k aktuálnímu projektu společník a pak podle potřeby zadávat do relací ladění, zobrazovat a upravovat instance terminálů, přečtěte si téma webové aplikace v localhostu, spojit hlasové hovory a další!

Jste připraveni začít? Týmová spolupráce by měla být tak rychlá a přirozená, takže ji nebudete moct dělat těžší. Z tohoto důvodu je Visual Studio Live Share snadné začít, takže můžete hladce začít sdílet práci a nápady.

> [!TIP]
> Víte, že se můžete *připojit k vlastní relaci spolupráce*? Díky tomu si můžete Live Share vyzkoušet sami nebo můžete rozjet instanci Visual Studia nebo VS Code a vzdáleně se k ní připojit. U obou instancí můžete dokonce používat stejnou identitu. Vyzkoušejte to!

Stačí postupovat podle těchto kroků, abyste se připojili k relaci spolupráce.

## <a name="1-install-the-extension"></a>1. Instalace rozšíření

Instalace rozšíření je snadná. Stačí postupovat podle těchto kroků:

<table style="width: 100%; border:none;">
<tr>
    <td width="128px" style="width: 128px; text-align: center; border:none;"><img src="../media/vs-code.svg" width="128px" alt="Visual Studio Code logo"/></td>
    <td style="border:none;">
        <strong>Visual Studio Code (1.22.0+)</strong><br />
        1. Nainstalujte <a href="https://code.visualstudio.com/">Visual Studio Code</a> pro Windows (7, 8.1 nebo 10), macOS <b>(Sierra+)</b>, 64bitový Linux <b>(<a href="../use/vscode.md#installation">podrobnosti</a>)</b>.<br />
        2. Z marketplace si stáhněte a nainstalujte rozšíření Visual Studio Live Share. <br />
        3. Zvolte Znovu načíst a počkejte, až se stáhnou a nainstalují závislosti (sledujte stavový řádek).<br />
        4. <strong>Linux</strong>: Pokud se zobrazí výzva k <a href="../reference/linux.md#install-linux-prerequisites">instalaci knihoven</a>, klikněte na nainstalovat, zadejte heslo a po dokončení vs Code restartujte.<br />
        <a href="https://aka.ms/vsls-dl/vscode" alt="Download button"><img src="../media/download.png"></a>
    </td>
</tr>
<tr style="border:none;">
    <td width="128px" style="width: 128px; text-align: center; border:none;"><img src="../media/vs-ide-2019.svg" width="128px" alt="Visual Studio 2019 logo" /></td>
    <td  style="border:none;">
        <strong>Visual Studio 2019 </strong><br />
        1.Nainstalujte sadu <a href="https://visualstudio.microsoft.com/downloads/">Visual Studio 2019</a>.<br/>
        2. Nainstalujte <a href="../reference/platform-support.md">podporované sady funkcí</a> (například ASP.NET, .NET Core, C++, Python a/nebo Node.js).<br />
        3. Visual Studio Live Share se standardně instaluje s těmito sadami funkcí. <br />
    </td>
</tr>
<tr style="border:none;">
    <td width="128px" style="width: 128px; text-align: center; border:none;"><img src="../media/vs-ide-2017.svg" width="128px" alt="Visual Studio 2017 logo" /></td>
    <td  style="border:none;">
        <strong>Visual Studio 2017 15.6 nebo vyšší</strong><br />
        1. Nainstalujte nejnovější verzi sady <a href="https://visualstudio.microsoft.com/vs/older-downloads/">Visual Studio 2017</a> (15.6+) na Windows (7, 8.1 nebo 10).<br/>
        2. Nainstalujte <a href="../reference/platform-support.md">podporované sady funkcí</a> (například ASP.NET, .NET Core, C++ a/nebo Node.js).<br />
        3. Z marketplace si stáhněte a nainstalujte rozšíření Visual Studio Live Share. <br />
        <a href="https://aka.ms/vsls-dl/vs"><img style="padding: 0; spacing: 0;" src="../media/download.png" alt="Download button" ></a><br />
    </td>
</tr>
</table>

Stažením a používáním rozšíření Visual Studio Live Share vyjadřujete souhlas s [licenčními podmínkami](https://aka.ms/vsls-license) a [prohlášením o zásadách ochrany osobních údajů](https://www.microsoft.com/en-us/privacystatement/EnterpriseDev/default.aspx). Pokud narazíte na problémy, podívejte se na článek o [odstraňování potíží](../troubleshooting.md).

## <a name="2-optional-join-as-a-read-only-guest-in-vs-code"></a>2. [volitelné] Připojte se jako host určený jen pro čtení v VS Code

V VS Code můžete po instalaci rozšíření Live Share, restartování a čekání na dokončení instalace závislostí přejít do a připojit se k relaci spolupráce jako host jen pro čtení.

> [!NOTE]
> Pokud chcete upravit kód, ke kterému se připojujete, musíte se přihlásit.

Otevřete (nebo znovu otevřete) odkaz na pozvánku v prohlížeči a dostanete oznámení, že prohlížeč bude chtít spustit VS Code. Nechte ho spuštěný a začne se připojovat k relaci spolupráce.

Když se VS Code spustí, zobrazí se informační zpráva s výzvou, abyste se přihlásili. Pro připojení k relaci vyberte možnost pokračovat jako hosta jen pro čtení.

![Připojit jako relaci jako informační zprávy hosta jen pro čtení](../media/vscode-read-only-guest.png)

Zobrazí se výzva k zadání zobrazovaného názvu, který bude pomáhat účastníkům v relaci identifikovat.

![Název hosta jen pro čtení](../media/vscode-read-only-guest-name.png)

Následně se k relaci připojíte jako jen pro čtení. Budete moci zobrazit a procházet kód, společně ladit a zobrazit sdílené servery a terminály (jen pro čtení).

> [!NOTE]
> Pokud chcete později získat přístup pro čtení a zápis kódu, můžete se přihlásit. Ve stavovém řádku klikněte na své zobrazované jméno a vyberte možnost přihlásit se.
![přihlášení hosta jen pro čtení](../media/vscode-read-only-guest-signin.png) tím se spustí váš prohlížeč a můžete zvolit účet Microsoft nebo GitHub pro přihlášení.

## <a name="3-sign-in"></a>3. přihlášení

Po instalaci rozšíření Live Share, restartování a čekání na dokončení instalace (VS Code) se budete chtít přihlásit, aby mohli ostatní účastníci informovat o tom, kdo máte. Pokud tento krok přeskočíte, zobrazí se výzva, abyste se přihlásili během procesu připojení nebo aby se relace mohla připojit jako host určený jen pro čtení. Začněte tím, že kliknete na tlačítko "Live Share" položka stavového řádku (VS Code)/"přihlášení" (a).

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

V **vs Code**se prohlížeč spustí, když se zobrazí oznámení o spuštění, které vás vyzve k přihlášení. Dokončete proces přihlášení v prohlížeči a po dokončení jednoduše zavřete prohlížeč.

![Informační zpráva s výzvou k přihlášení pomocí webového prohlížeče](../media/vscode-sign-in-toast.png)

> **Uživatelé systému Linux:** Pokud používáte starší verzi Live Share (v 0.3.295 nebo níže), může se zobrazit výzva k zadání kódu uživatele. Aktualizujte na nejnovější verzi rozšíření nebo klikněte na "máte potíže?" odkaz po přihlášení, aby se zobrazil kód [Podrobnosti najdete tady](../use/vscode.md#sign-in-using-a-user-code).

V **aplikaci Visual Studio**Live Share automaticky používá váš [účet přizpůsobení](https://docs.microsoft.com/en-us/visualstudio/ide/signing-in-to-visual-studio). V důsledku toho se můžete jednoduše přihlásit stejným způsobem jako normálně. Pokud ale dáváte přednost jinému přihlášení než k vašemu účtu přizpůsobení sady Visual Studio, v nabídce **nástroje &gt; možnosti &gt; Live Share &gt; uživatelský účet** a vyberte jiné přihlašovací údaje.

Pokud stále dochází k potížím, přečtěte si téma [řešení potíží](../troubleshooting.md#sign-in) .

## <a name="4-openre-open-the-invite-link-in-a-browser"></a>4. Otevřete nebo znovu otevřete odkaz Pozvánka v prohlížeči.

Nyní stačí otevřít (nebo znovu otevřít) odkaz na pozvánku v prohlížeči.

> **Poznámka**: Pokud jste ještě nenainstalovali rozšíření Live Share, zobrazí se odkazy na tržiště rozšíření. Nainstalujte rozšíření a restartujte nástroj a zkuste to znovu.

Měli byste upozornit, že prohlížeč chce spustit nástroj s povoleným Live Share. Pokud necháte vybraný nástroj spuštěný, budete po jeho spuštění připojeni k relaci spolupráce.

![Připojit stránku](../media/join-page.png)

Pokud je hostitel v režimu offline, budete místo toho upozorněni v tomto okamžiku. Pak se můžete obrátit na hostitele a požádat ho, aby se znovu sdílel.

> **Tip Poradce při potížích:** Při použití VS Code se ujistěte, že jste **Nástroj spustili aspoň jednou** po instalaci rozšíření a čekali na dokončení instalace (viz stavový řádek) před otevřením nebo opakovaným otevřením stránky pozvání. Pořád máte problémy? Podrobnosti najdete v tématu [ruční připojení](../reference/manual-join.md) .

## <a name="5-collaborate"></a>5. spolupráce

A to je vše! Za chvíli budete připojeni k relaci spolupráce vašeho kolegů. Ve výchozím nastavení hostitel automaticky akceptuje lidi, kteří se připojují, ale pokud je hostitel nastavený tak, aby [vyžadoval schválení hosta](../reference/security.md#requiring-guest-approval) , zobrazí se v dialogovém okně stavový řádek/spojení, že Live share na hostiteli čeká na schválení vaší žádosti o připojení.

> **Tip zabezpečení:** Jako host se připojuje k relaci spolupráce, je důležité pochopit, že hostitelé můžou omezovat přístup k určitým souborům nebo funkcím. Chcete pochopit důsledky zabezpečení některých funkcí a nastavení Live Share? Podívejte se na článek o [zabezpečení](../reference/security.md) .

Tady je několik věcí, které můžete vyzkoušet:

1. Pohyb v rámci projektu nezávisle a udělejte úpravy
2. Podívejte se na pracovní technologii IntelliSense pro JavaScript, TypeScript a/ C# nebo kód
3. Upravit něco společně s hostitelem
4. Sledujte hostitele a při procházení a provádění úprav v různých souborech se pohybujte s nimi.
5. Spustit relaci spoluladění s hostitelem
6. Požádejte hostitele, aby nasdílel Server, abyste se mohli podívat, jak webová aplikace běží na svém počítači.
7. Požádat hostitele o sdílení terminálu a spuštění některých příkazů

Máte potíže? Podívejte se na článek o [odstraňování potíží](../troubleshooting.md) nebo nám [pošlete svůj názor](../support.md).

## <a name="next-steps"></a>Další kroky

Další informace najdete v těchto dalších článcích.

- [Rychlý Start: sdílení prvního projektu](share.md)
- [Postupy: spolupráce pomocí Visual Studio Code](../use/vscode.md)
- [Postupy: spolupráce pomocí sady Visual Studio](../use/vs.md)

Referenční informace

- [Požadavky na připojení pro Live Share](../reference/connectivity.md)
- [Funkce zabezpečení Live Share](../reference/security.md)
- [Podpora jazyků a platforem](../reference/platform-support.md)
- [Podpora rozšíření](../reference/extensions.md)
