---
title: Spolupráce pomocí Visual Studio Code-Visual Studio Live Share | Microsoft Docs
description: Sada postupů spolupráce pro Visual Studio Code a Live Share.
ms.custom: ''
ms.date: 04/27/2018
ms.reviewer: ''
ms.suite: ''
ms.topic: conceptual
author: chuxel
ms.author: clantz
manager: AmandaSilver
ms.workload:
- liveshare
ms.openlocfilehash: a720a93f0e98b28400a62874c26f3f4cdda57ef7
ms.sourcegitcommit: c6ef4e5a9aec4f682718819c58efeab599e2781b
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/30/2019
ms.locfileid: "73179902"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="how-to-collaborate-using-visual-studio-code"></a>Postupy: spolupráce pomocí Visual Studio Code

Jste připraveni začít spolupracovat s Live Share v VS Code?  Pokud ano, jste na správném místě! V tomto článku Vás provedeme postupem, jak používat některé z konkrétních funkcí v rozšíření Visual Studio Live Share pro Visual Studio Code.

Všimněte si, že všechny výše popsané aktivity spolupráce zahrnují jednoho **hostitele relace pro spolupráci** a jednoho nebo více **hostů**. Hostitel je osoba, která relaci spolupráce zahájila, a host je každý, kdo se k relaci připojí.

*Hledáte zkrácený souhrn? Místo toho se podívejte do [složky](../quickstart/share.md) rychlé starty nebo se [připojovat](../quickstart/join.md) .*

> [!TIP]
> Víte, že se můžete *připojit k vlastní relaci spolupráce*? Díky tomu si můžete Live Share vyzkoušet sami nebo můžete rozjet instanci Visual Studia nebo VS Code a vzdáleně se k ní připojit. Stejnou identitu můžete dokonce použít i v obou instancích. Vyzkoušejte to!

## <a name="installation"></a>Instalace

Než začnete, musíte mít jistotu, že máte nainstalovanou verzi Visual Studio Code, která splňuje základní požadavky Live Share. Budete potřebovat **Visual Studio Code (1.22.0 nebo vyšší)** spuštěné na:

- **Windows**: 7, 8,1 nebo 10

- **MacOS**: pouze Sierra (10,12) a vyšší.
    - _Capitan (10,11) a níže nejsou aktuálně podporovány z důvodu [požadavků .NET Core 2,0](https://go.microsoft.com/fwlink/?linkid=872315)._

- **Linux**: 64-bit Ubuntu Desktop 16.04 +, Fedora Workstation 27 +, CentOS 7

    - Live Share vyžaduje počet požadovaných součástí pro [Linux](#linux-install-steps) , může se zobrazit výzva k instalaci.
    - _32-bit Linux není podporován z důvodu [požadavků .NET Core 2,0](https://go.microsoft.com/fwlink/?linkid=872314)._
    - V tuto chvíli se nepodporuje i ARM.
    - Podrobnosti o používání podřízených a dalších distribucí najdete v článku [Podrobnosti o instalaci pro Linux](../reference/linux.md) .

Stažení a instalace rozšíření Visual Studio Live Share pak bude hračka:

1. Nainstalovat <a href="https://code.visualstudio.com/">Visual Studio Code</a>
2. [Stáhněte](https://aka.ms/vsls-dl/vscode) a nainstalujte Visual Studio Live Share rozšíření z webu Marketplace.
3. Znovu načíst Visual Studio Code
4. Počkejte na stažení a instalaci závislostí (viz stavový řádek).<br/>
    ![dokončení instalace](../media/vscode-finishing-install.png)
5. **Linux**: Pokud se zobrazí oznámení o instalaci chybějících knihoven:
    1. V oznámení klikněte na nainstalovat.
    2. Po zobrazení výzvy zadejte heslo správce (sudo).
    3. Po dokončení restartujte VS Code.

Stažením a používáním rozšíření Visual Studio Live Share vyjadřujete souhlas s [licenčními podmínkami](https://aka.ms/vsls-license) a [prohlášením o zásadách ochrany osobních údajů](https://www.microsoft.com/en-us/privacystatement/EnterpriseDev/default.aspx). Pokud narazíte na problémy, podívejte se na článek o [odstraňování potíží](../troubleshooting.md).

[Stažení ![](../media/download.png)](https://aka.ms/vsls-dl/vscode)

### <a name="linux-install-steps"></a>Kroky instalace pro Linux

Linux je vysoce proměnlivé prostředí a s sheerm počtem desktopových prostředí a distribucí může být složitější, aby bylo možné pracovat. Pokud se přiřadíte k podporovaným verzím **Ubuntu desktopu** (16.04 +) nebo **pracovní stanici Fedora** (27 +), **CentOS 7** a používáte pouze **oficiální distribuce vs Code**, měli byste tento proces jednoduše najít. V případě, že používáte nestandardní konfiguraci nebo distribuci pro příjem dat, je však možné, že nebudete moci spustit hiccups. Další informace najdete v tématu [Podrobnosti o instalaci systému Linux](../reference/linux.md) .

#### <a name="install-linux-prerequisites"></a>Nainstalovat požadavky pro Linux

V některých distribucích systému Linux chybí knihovny Live Share musí fungovat. Ve výchozím nastavení se Live Share pokusí zjistit a nainstalovat požadavky systému Linux za vás. Zobrazí se informační zpráva, když Live Share narazí na problém, který může pocházet z chybějících knihoven, které vás požádají o oprávnění k jejich instalaci.

![Informační zpráva ukazující zprávu, že chybí předpoklady pro Linux](../media/vscode-linux-prereq-missing.png)

Po kliknutí na nainstalovat se zobrazí okno terminálu, kde budete muset zadat heslo správce (sudo), abyste mohli pokračovat. Za předpokladu, že se úspěšně dokončí, restartujte Visual Studio Code měli byste mít všechno nastavené! Můžete také chtít vyzkoušet **[Tipy podle distribuce](../reference/linux.md#tips-by-distribution)** pro jiné tipy a alternativní řešení, pokud existují.

Pokud se zobrazí zpráva oznamující, že skript nepodporuje vaši distribuci, přečtěte si **[tipy pro distribuce s podporou komunity](../reference/linux.md#tips-for-community-supported-distros)** pro informace, které komunita sdílí s námi.

Pokud nechcete, **vs Code příkaz Spustit**, můžete také kdykoli spustit následující příkaz z okna terminálu a kdykoli znovu spustit nejnovější verzi tohoto skriptu, a to tak dlouho.

    wget -O ~/vsls-reqs https://aka.ms/vsls-linux-prereq-script && chmod +x ~/vsls-reqs && ~/vsls-reqs

#### <a name="linux-browser-integration"></a>Integrace s prohlížečem Linux

Visual Studio Live Share obvykle **nevyžaduje další kroky instalace** , aby bylo možné povolit integraci prohlížeče na platformě Linux.

V některých distribucích může být neobvyklá zpráva, že k dokončení procesu instalace **je potřeba vaše heslo správce (sudo)** . Zobrazí se okno terminálu s oznámením, kde se bude instalovat spouštěč prohlížeče. Po zobrazení výzvy zadejte heslo a stiskněte klávesu ENTER, až se instalace dokončí, aby se okno terminálu zavřelo.

Můžete si přečíst další informace o tom, proč je to nutné a kde Live Share umístí soubory **[sem](../reference/linux.md#linux-browser-integration)** . Poznámka: i když nemůžete získat integraci prohlížeče, můžete **[k relacím na spolupráci připojit ručně](../how-to-guides/vscode.md#join-manually)** .

## <a name="sign-in"></a>Přihlásit se

Aby bylo možné spolupracovat, budete se muset Visual Studio Live Share přihlásit, aby všichni znali, kdo máte. Toto je čistě bezpečnostní opatření a **neumožňuje vás** při jakémkoli marketingovém nebo jiných výzkumných aktivitách. Můžete se přihlásit pomocí osobního účtu Microsoft (například @outlook.com), pracovního nebo školního účtu (AAD) založeného na Microsoftu nebo účtu GitHub. Přihlašování je snadné.

**Klikněte** na položku Live share na stavovém řádku nebo stiskněte **kombinaci kláves CTRL + SHIFT + P/Cmd + Shift + P** a vyberte příkaz Live Share: přihlásit se pomocí prohlížeče.

![Tlačítko pro přihlášení VS Code](../media/vscode-sign-in-button.png)

Zobrazí se oznámení s výzvou, abyste se přihlásili pomocí webového prohlížeče. Kliknutím na spustit přihlášení otevřete prohlížeč, který můžete použít k dokončení procesu přihlašování. Po dokončení jednoduše zavřete prohlížeč.

![Informační zpráva s výzvou k přihlášení pomocí webového prohlížeče](../media/vscode-sign-in-toast.png)

> **Uživatelé systému Linux:** Pokud používáte starší verzi Live Share (v 0.3.295 nebo níže), může se zobrazit výzva k zadání kódu uživatele. Aktualizujte na nejnovější verzi rozšíření nebo klikněte na "máte potíže?" odkaz po přihlášení, aby se zobrazil kód [Podrobnosti najdete níže](#sign-in-using-a-user-code).

#

> **Rozšířený Tip:** Nastavení `liveshare.account` a `liveshare.accountProvider` umožňují vybrat účet, který se má použít pro automatické přihlašování v případě, že máte k dispozici přihlašovací údaje pro více účtů v mezipaměti.
> Představte si například, že pracujete se 2 projekty, se kterými se chcete přihlásit pomocí různých identit. V nastavení pracovního prostoru VSCode můžete nastavit nastavení `liveshare.account` na jiné e-mailové adresy v každém adresáři projektu, abyste se ujistili, že se všechny automaticky přihlásí ke správnému účtu. Nastavení `liveshare.accountProvider` může být nastavené na hodnotu `"microsoft"` nebo `"github"` pro případ, že použijete stejnou e-mailovou adresu s více zprostředkovateli.

Pokud se po dokončení procesu přihlášení v prohlížeči Visual Studio Code nemusíte přihlašovat, přečtěte si téma [přihlášení pomocí uživatelského kódu](#sign-in-using-a-user-code). V opačném případě se podívejte na [řešení potíží](../troubleshooting.md#sign-in) , kde najdete další tipy.

### <a name="sign-in-using-a-user-code"></a>Přihlaste se pomocí uživatelského kódu.

Pokud dochází k problémům s VS Code nemusíte vybírat dokončená přihlášení, můžete místo toho zadat "kód uživatele".

1. Stiskněte **kombinaci kláves CTRL + SHIFT + P/Cmd + Shift + P** a spusťte příkaz "Live Share: přihlásit pomocí uživatelského kódu".

2. K dokončení procesu přihlášení by se měl použít prohlížeč.

    > [!NOTE]
    > Pokud se prohlížeč nezobrazí automaticky, otevřete [Toto umístění](https://insiders.liveshare.vsengsaas.visualstudio.com/auth/login) v prohlížeči a přihlaste se.

3. Až budete hotovi, klikněte na "máte potíže? Pokud chcete zobrazit uživatelský kód, klikněte sem pro směry uživatelského kódu.

    ![Obrázek uživatelského kódu v prohlížeči](../media/vscode-user-code-browser.png)

4. Zkopírujte kód uživatele.

5. Nakonec vložte kód uživatele do vstupního pole, které se zobrazilo při spuštění příkazu, a stisknutím klávesy ENTER dokončete proces přihlašování.

    ![Obrázek pole pro zadání uživatelského kódu](../media/vscode-user-code.png)

## <a name="using-the-live-share-viewlet"></a>Použití Live Share Viewlet

Po instalaci Visual Studio Live Share bude na řádek aktivity VS Code přidána vlastní karta. Na této kartě máte přístup ke všem funkcím Live Share, abyste mohli spolupracovat. Kromě toho, když sdílíte nebo přistupujete k relaci spolupráce, zobrazí se také zobrazení na kartě Průzkumník, abyste měli přístup ke všem těmto funkcím.

<table style="border: none;">
<tr style="border: none;">
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vscode-custom-tab.png" width="100%" alt="Live Share custom tab" />
    </td>
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vscode-explorer-view.png" width="100%" alt="Live Share explorer view"
</tr>
</table>

Pomocí těchto zobrazení se můžete podívat na umístění účastníka ve sdíleném kódu, kliknout na účastníka a postupovat podle nich, soustředit se na účastníky, přistupovat ke sdíleným serverům a terminálům a další.

## <a name="using-the-scoped-command-menu"></a>Použití oboru příkazů nabídky

Kromě toho jsou všechny funkce Visual Studio Live Share k dispozici z Visual Studio Code "paleta příkazů", ke kterým lze získat přístup stisknutím kombinace kláves CTRL + SHIFT + P/Cmd + Shift + P nebo F1. Úplný seznam příkazů můžete najít zadáním "Live Share".

Vzhledem k tomu, že tento seznam může trvat dlouhou dobu, může být jednodušší využít nabídku příkazů vymezenou ze stavového řádku. Kliknutím na ikonu pro přihlášení/stav relace ve stavovém řádku okamžitě zobrazíte kontextový seznam příkazů, které jsou k dispozici pro použití.

![Ikona stavu relace VS Code](../media/vscode-share-state.png)

## <a name="share-a-project"></a>Sdílení projektu

Po stažení a instalaci Visual Studio Live Share postupujte podle těchto kroků a zahajte relaci spolupráce a pozvěte kolegu, aby s vámi spolupracovali.

1. **Přihlásit se**

    Po instalaci rozšíření Live Share, opětovném načítání a čekání na dokončení instalace závislostí se budete chtít přihlásit, aby mohli jiní spolupracovníky informovat o tom, kdo jste vy. Další podrobnosti najdete v tématu věnovaném [přihlášení](#sign-in) .

2. **Otevření složky**

    Použijte běžný pracovní postup k otevření složky, projektu nebo řešení, které chcete sdílet s hosty.

3. **Volitelné Aktualizace skrytých nebo vyloučených souborů**

    Ve výchozím nastavení Live Share **skrývá** všechny soubory nebo složky, na které se odkazuje ve sdílených složkách z hostů. **Skrytím** souboru znemožníte jeho zobrazení ve stromu souborů hosta. **Vyloučení** souboru platí přísnější pravidlo, které zabrání Live Share jeho otevření pro hosta v situacích, jako je jít na definici, nebo pokud se při ladění nebo za "následováno" zadáte krok do souboru. Pokud chcete skrýt nebo vyloučit různé soubory, můžete do projektu pomocí těchto nastavení přidat soubor **. vsls. JSON** . Podrobnosti najdete v tématu [řízení přístupu k souborům a viditelnost](../reference/security.md#controlling-file-access-and-visibility) .

4. **Spustit relaci spolupráce**

    Nyní jednoduše **klikněte** na položku Live share na stavovém řádku nebo stiskněte **kombinaci kláves CTRL + SHIFT + P/Cmd + Shift + P** a vyberte možnost "Live Share: spustit relaci spolupráce (sdílená složka)".

    ![Tlačítko sdílet](../media/vscode-share-button-new.png)

    > [!NOTE]
    > Možná budete požádáni o váš software brány firewall na ploše, aby mohl agent Live Share otevřít port při prvním sdílení. Přijetí je zcela volitelné, ale umožňuje zabezpečený "přímý režim", aby se zlepšil výkon, když osoba, se kterou pracujete, je ve stejné síti jako vy. Podrobnosti najdete v tématu [Změna režimu připojení](../reference/connectivity.md#changing-the-connection-mode) .

    Odkaz pro pozvání bude automaticky zkopírován do schránky. Při otevření v prohlížeči tento odkaz umožňuje ostatním uživatelům připojit se k nové relaci spolupráce, která s nimi sdílí obsah těchto složek.

    Zobrazí se také přechod položky stavového řádku Live Share, který představuje stav relace. Podívejte se na informace o [stavu relace](#session-states) níže, aby to vypadalo takto.

    Všimněte si, že pokud po zahájení sdílení potřebujete znovu získat odkaz pro pozvání, budete k němu mít znovu přístup kliknutím na ikonu stavového řádku stavu relace a vybráním možnosti pozvat ostatní (Kopírovat odkaz).

5. **Volitelné Povolit režim jen pro čtení**

    Po zahájení relace spolupráce můžete nastavit relaci jen pro čtení a zabránit tak hostům v provádění úprav v kódu, který se sdílí.

    Po sdílení se dostanete oznámení, že se odkaz na pozvánku zkopíroval do schránky. Pak můžete vybrat možnost nastavit relaci jen pro čtení.

    ![VS Code režimu jen pro čtení](../media/vscode-read-only-toast.png)

6. **Poslat někomu odkaz**

    Pošlete odkaz prostřednictvím e-mailu, časové rezervy, Skypu atd. na ty, které chcete pozvat. Všimněte si, že vzhledem k tomu, že úroveň přístupu Live Share relace může poskytnout hostům, **byste měli sdílet jenom s lidmi, kterým důvěřujete** , a zamyslete se nad důsledky sdílení.

    > **Tip zabezpečení:** Chcete pochopit důsledky zabezpečení některých funkcí Live Share? Podívejte se na článek o [zabezpečení](../reference/security.md) .

    Pokud má host, který jste pozvali, dotazy, najdete v článku "[rychlý Start: připojení k první relaci](../quickstart/join.md)" Další informace o tom, jak začít pracovat jako host.

7. **Volitelné Schválit hosta**

    Ve výchozím nastavení se hostů připojí k vaší relaci spolupráce automaticky a budete upozorněni, až budou připraveni s vámi pracovat. I když vám toto oznámení umožní odebrat je z relace, můžete také místo toho vyžadovat explicitní schválení pro kohokoli, co se připojuje.

    Pokud chcete tuto funkci povolit, stačí do nastavení. JSON přidat následující:

         "liveshare.guestApprovalRequired": true

    Jakmile je toto nastavení zapnuté, zobrazí se výzva k potvrzení, že hosta se bude moci připojit.

    ![Žádost o schválení Visual Studio Codeho připojení](../media/vscode-join-approval.png)

    Další podrobnosti o požadavcích na zabezpečení pozvánky najdete v tématu [pozvánky a přístup k nim](../reference/security.md#invitations-and-join-access) .

To je!

### <a name="stop-the-collaboration-session"></a>Zastavení relace spolupráce

Jako hostitel můžete ukončit sdílení úplně a ukončit relaci spolupráce kdykoli tím, že otevřete zobrazení Live Share v Průzkumníkovi nebo na vlastní kartě Live Share a vyberete ikonu ukončit relaci spolupráce.

![Zastavit relaci spolupráce](../media/vscode-end-collaboration-viewlet.png)

Všichni hosté budou upozorněni, že relace skončila.  Po ukončení relace nebudou mít hosté přístup k obsahu a žádné dočasné soubory se automaticky vyčistí.

Máte problémy se sdílením? Podívejte se na [řešení potíží](../troubleshooting.md#share-and-join).

## <a name="join-a-collaboration-session"></a>Připojit se k relaci spolupráce

Po stažení a instalaci Visual Studio Live Share musí hosty provést několik kroků, než se připojí k hostované relaci spolupráce. Existují dva způsoby, jak se připojit: [přes prohlížeč](#join-via-the-browser) a [ručně](#join-manually).

> **Tip zabezpečení:** Jako host se připojuje k relaci spolupráce, je důležité pochopit, že hostitelé můžou omezovat přístup k určitým souborům nebo funkcím. Chcete pochopit důsledky zabezpečení některých funkcí a nastavení Live Share? Podívejte se na článek o [zabezpečení](../reference/security.md) .

### <a name="join-via-the-browser"></a>Připojení přes prohlížeč

Nejjednodušší způsob, jak se připojit k relaci spolupráce, je jednoduše otevřít odkaz pro pozvání ve webovém prohlížeči. Můžete očekávat, že budete postupovat podle tohoto toku.

1. **Přihlásit se**

    Po instalaci rozšíření Live Share, opětovném načítání a čekání na dokončení instalace závislostí se budete chtít přihlásit, aby mohli jiní spolupracovníky informovat o tom, kdo jste vy. Další podrobnosti najdete v tématu věnovaném [přihlášení](#sign-in) .

2. **Klikněte na odkaz pozvat nebo otevřete pozvánku v prohlížeči.**

    Nyní stačí otevřít (nebo znovu otevřít) odkaz na pozvánku v prohlížeči.

    > **Poznámka**: Pokud jste ještě nenainstalovali rozšíření Live Share, zobrazí se odkazy na tržiště rozšíření. Nainstalujte rozšíření a restartujte nástroj a zkuste to znovu.

    Měli byste upozornit, že prohlížeč chce spustit nástroj s povoleným Live Share. Pokud necháte vybraný nástroj spuštěný, budete po jeho spuštění připojeni k relaci spolupráce.

    ![Připojit stránku](../media/join-page.png)

    Pokud je hostitel v režimu offline, budete místo toho upozorněni v tomto okamžiku. Pak se můžete obrátit na hostitele a požádat ho, aby se znovu sdílel.

    > [!NOTE]
    > Ujistěte se, že jste **Nástroj spustili aspoň jednou** po instalaci rozšíření Visual Studio Live Share a povolili dokončení instalace nebo opětovného otevření stránky pozvání. Pořád máte problémy? Podívejte se na téma [ruční připojení](#join-manually).

3. **Uložte**

    A je to! Za chvíli budete připojeni a můžete začít spolupracovat.

    Po přechodu na tlačítko "Live Share" se zobrazí zpráva "stav relace". Podívejte se na informace o [stavu relace](#session-states) níže, aby to vypadalo takto.

    Po dokončení připojení se pak automaticky provedete na soubor, který hostitel momentálně upravuje.

### <a name="join-manually"></a>Ruční připojení

Můžete se také ručně připojit bez použití webového prohlížeče, který může být užitečný v situacích, kdy je již spuštěný nástroj, který chcete použít, chcete použít jiný nástroj, který není obvykle k dispozici, nebo pokud máte potíže s tím, že budete mít k dispozici odkazy na pozvání z nějakého důvodu. Proces je jednoduchý:

1. **Přihlásit se**

    Po instalaci rozšíření Live Share, opětovném načítání a čekání na dokončení instalace závislostí se budete chtít přihlásit, aby mohli jiní spolupracovníky informovat o tom, kdo jste vy. Další podrobnosti najdete v tématu věnovaném [přihlášení](#sign-in) .

2. **Použití příkazu JOIN**

    Otevřete Live Share vlastní kartu na řádku VS Code aktivity a vyberte "připojit se k relaci pro spolupráci...". ikona nebo položka.

    ![Ikona připojení Viewlet](../media/vscode-join-viewlet.png)

3. **Vložit odkaz pro pozvání**

    Vložte adresu URL pozvánky, kterou jste poslali, a stisknutím klávesy ENTER ji potvrďte.

4. **Uložte!**

    A je to! V tuto chvíli byste měli být připojeni k relaci spolupráce.

    Po přechodu na tlačítko "Live Share" se zobrazí zpráva "stav relace". Podívejte se na informace o [stavu relace](#session-states) níže, aby to vypadalo takto.

    Po dokončení připojení se pak automaticky provedete na soubor, který hostitel momentálně upravuje.

### <a name="leave-the-collaboration-session"></a>Opustit relaci spolupráce

Jako hosta můžete opustit relaci spolupráce bez jejího ukončení, a to pouhým zavřením okna VS Code. Pokud byste chtěli ponechat okno otevřené, můžete otevřít Live Share zobrazení Průzkumníka nebo Live Share vlastní kartu a vybrat ikonu opustit relaci pro spolupráci.

![Ponechá ikonu relace](../media/vscode-leave-session-viewlet.png)

Všechny dočasné soubory se automaticky vyčistí, takže není potřeba žádná další akce.

Máte problémy s připojením? Podívejte se na [řešení potíží](../troubleshooting.md#share-and-join).

## <a name="co-editing"></a>Společné úpravy

Jakmile se host připojí k relaci spolupráce, všichni spolupracovníci budou moct hned zobrazit úpravy a výběr vzájemných úprav v reálném čase. Vše, co potřebujete udělat, je vybrat soubor z Průzkumníka souborů a začít upravovat. Hostitelé i hosté uvidí úpravy, jak je provedete, a mohou přispět k tomu, aby se daly snadno iterovat a rychle nail řešení.

> [!NOTE]
> Připojení relace pro spolupráci, která je jen pro čtení, brání hostům v tom, aby mohli provádět úpravy souborů. Hostitel může [při sdílení povolit režim jen pro čtení](#share-a-project). Jako Host můžete zjistit, jestli jste se připojili k relaci jen pro čtení, a to tak, že prohlížíte [stav relace](#session-states).

![Snímek obrazovky znázorňující souběžné úpravy](../media/vscode-coedit.png)

> [!NOTE]
> Společné úpravy mají omezení pro určité jazyky. Stav funkcí podle jazyků najdete v článku [o podpoře platforem](../reference/platform-support.md).

Výběry, které provedete, jsou kromě kurzorů a úprav viditelné i pro všechny účastníky ve stejném souboru. To usnadňuje zdůraznění, kde možná existují problémy, nebo vyjádřete nápady.

![Snímek obrazovky znázorňující zvýraznění](../media/vscode-highlight.png)

Ještě lepší a ostatní účastníci můžou přejít na libovolný soubor ve sdíleném projektu. Můžete buď upravit dohromady, nebo nezávisle na tom, co můžete bezproblémově přepínat mezi vyšetřováním, dělat malé úpravy a úplné úpravy spolupráce.

Výsledné úpravy jsou uložené v počítači hostitele při uložení, takže nemusíte po dokončení úprav provádět synchronizaci, vkládání ani posílání souborů. Úpravy jsou "jenom tam."

> **Tip zabezpečení:** Vzhledem k tomu, že všichni účastníci můžou nezávisle Procházet a upravovat soubory jako hostitel, možná budete chtít omezit, které soubory hostů mají mít přístup k vašemu projektu prostřednictvím souboru. vsls. JSON. Jako host je také důležité si uvědomit, že v důsledku těchto nastavení se některé soubory nezobrazuje. Podrobnosti najdete v tématu [řízení přístupu k souborům a viditelnost](../reference/security.md#controlling-file-access-and-visibility) .

### <a name="changing-participant-flag-behaviors"></a>Změna chování příznaku účastníka

Ve výchozím nastavení Visual Studio Live Share automaticky zobrazuje příznak vedle kurzoru účastníka při najetí myší nebo při úpravách, zvýraznění nebo přesunutí kurzoru. V některých případech můžete chtít toto chování změnit.

Jednoduše **upravte Settings. JSON** (> předvolby souboru > nastavení), přidejte jeden z následujících řádků a pak restartujte vs Code:

| Nastavením | Předvídatelně |
|---------|----------|
| ``"liveshare.nameTagVisibility":"Never"`` | Příznak se zobrazí, pouze když najedete myší na kurzor. |
| ``"liveshare.nameTagVisibility":"Activity"`` | Toto nastavení je výchozí. Příznak se zobrazí při najetí myší nebo v případě, že se kurzor upraví, zvýrazní nebo přesune. |
| ``"liveshare.nameTagVisibility":"Always"`` | Příznak je vždy zobrazen. |

## <a name="following"></a>Důsledku

Někdy potřebujete objasnit problém nebo návrh, který se týká více souborů nebo míst v kódu. V těchto situacích může být užitečné dočasně sledovat kolegy při pohybu v rámci projektu. Z tohoto důvodu, když se připojíte k relaci spolupráce, budete automaticky sledovat hostitele. Když někomu přijdete, váš Editor zůstane synchronizovaný s aktuálně otevřeným souborem a pozicí posunutí.

> [!NOTE]
> Ve výchozím nastavení Live Share sdílí i otevřené soubory mimo sdílenou složku. Pokud chcete tuto funkci zakázat, aktualizujte `liveshare.shareExternalFiles` Live Share na `false` v Settings. JSON.

Pokud chcete začít sledovat účastníka (jako hostitele nebo hosta), klikněte na jméno v seznamu účastníci na kartě zobrazení nebo vlastní karta aplikace Live Share. Kruh vedle jejich jména se vyplní, aby označoval, že se vám dostanou.

![VS Code sledovat z Viewlet](../media/vscode-follow-multiple-viewlet.png)

Případně můžete kliknout na ikonu připnutí v pravém horním rohu skupiny editoru nebo stisknout **CTRL + ALT + F/Cmd + Alt + F**.

![VS Code kód PIN](../media/vscode-pin.png)

> [!NOTE]
> Pokud je v relaci spolupráce více než jedna jiná osoba, budete požádáni o výběr účastníka, kterého chcete sledovat.
>
>![Snímek obrazovky znázorňující seznam spolupracovníků](../media/vscode-list-collaborators.png)

Vzhledem k tomu, že je následující možnost svázána se skupinou editorů, můžete použít rozdělené zobrazení (nebo rozložení mřížky), které má skupinu po účastníkovi a skupině, která není. To vám umožní provádět pořídit někoho a zároveň pracovat nezávisle na něčem. Když je vybraná skupina editorů, můžete vybrat účastníka v seznamu Účastníci a pořídit si ho.

![Kód PIN VS Code v rozděleném zobrazení](../media/vscode-follow-split.png)

Chcete-li se snadno přepnout z "režimu sledování" a začít upravovat sami, můžete automaticky zastavit následující, pokud dojde k některé z těchto situací:

1. Začnete upravovat aktuálně aktivní soubor
1. Otevřete jiný soubor.
1. Zavřete aktuálně aktivní soubor

Kromě toho můžete po kliknutí na ikonu připnutí znovu explicitně zastavit nebo podržet **kombinaci kláves CTRL + ALT + f/Cmd + Alt + F**.

## <a name="listing-participants"></a>Výpis účastníků

Rychlý způsob, jak zjistit, kdo je v relaci spolupráce, je prohlédnout si seznam účastníků na kartě zobrazení nebo vlastní karty v Průzkumníkovi Live Share. Zobrazení budou zobrazovat všechny účastníky v relaci.

![Snímek obrazovky znázorňující ikonu stavového řádku uživatele](../media/vscode-explorer-view.png)

Kliknutím na libovolného účastníka v tomto seznamu se budete řídit v aktivní skupině Editor.

Případně můžete stisknout **kombinaci kláves CTRL + SHIFT + P/Cmd + Shift + P** a vybrat příkaz Live Share: seznam účastníků nebo **kliknout** na položku stavového řádku, která zobrazuje počet účastníků ve vaší relaci.

![Snímek obrazovky znázorňující ikonu stavového řádku uživatele](../media/vscode-user-status.png)

Zobrazí se seznam všech účastníků v relaci. Na rozdíl od kliknutí na ikonu připnutí se tento seznam zobrazí i v případě, že relace obsahuje jenom jednu jinou osobu, takže můžete vždycky rychle zjistit, kde se nachází někdo jiný. Pro praktické účely, jako je ikona připnutí, si pak můžete vybrat jednoho ze seznamu účastníků. Pokud chcete místo toho skončit, stiskněte klávesu ESC.

## <a name="focusing"></a>Zaměřovat

Občas můžete chtít, aby všichni uživatelé v relaci spolupráce pocházeli a prohlédli se na něco, co děláte. Live Share vám umožní položit vás o tom, že vás na vás bude věnovat oznámení, které vám usnadní vám to, abyste mohli postupovat zpátky.

Otevřete kartu Live Share vlastní na řádku VS Code aktivity nebo v zobrazení Průzkumník Live Share a vyberte ikonu "účastníci – fokus".

![Ikona Viewlet fokusu](../media/vscode-focus-viewlet.png)

Po spuštění příkazu se uživatelům v relaci spolupráce zobrazí oznámení, že jste si vyžádali upozornění.

![Informační zpráva soustředěného oznámení](../media/vscode-focus-toast.png)

Potom můžou kliknout na sledovat hned z oznámení, když jsou připravení na vás na vás soustředit.

## <a name="co-debugging"></a>Společné ladění

Funkce pro spolupráci při ladění Visual Studio Live Share je účinný a jedinečný způsob, jak tento problém ladit. Kromě povolení prostředí pro spolupráci při řešení problémů vám taky poskytuje a ostatním účastníkům v relaci možnost prozkoumat problémy, které můžou být specifické pro prostředí, a to tak, že v počítači hostitele zadají sdílenou relaci ladění.

> **Tip zabezpečení:** Vzhledem k tomu, že všichni účastníci můžou nezávisle Procházet a upravovat soubory jako hostitel, možná budete chtít omezit, které soubory hostů mají mít přístup k vašemu projektu prostřednictvím souboru. vsls. JSON. Měli byste taky mít na paměti, že konzola/REPL přístup znamená, že účastníci můžou na svém počítači spouštět příkazy, takže byste měli jenom ladit jenom ty, které důvěřujete. Jako host je také důležité si uvědomit, že v důsledku těchto nastavení nemusí být možné postupovat podle pokynů k souborům s omezeným přístupem k určitým souborům s omezenými oprávněními. Podrobnosti najdete v tématu [řízení přístupu k souborům a viditelnost](../reference/security.md#controlling-file-access-and-visibility) .

Použití je jednoduché.

1. Ujistěte se, že hostitel i všichni hosté mají nainstalované příslušné ladicí rozšíření. (Technicky to není vždy nutné, ale je to obvykle dobrý nápad.)

2. Jako hostitel, pokud ještě není nastavený pro projekt, byste měli [nakonfigurovat soubor Launch. JSON](https://code.visualstudio.com/Docs/editor/debugging#_launch-configurations) pro ladění aplikace z vs Code stejným způsobem jako normálně. Nevyžaduje se žádné speciální nastavení.

3. V dalším kroku může hostitel spustit ladění pomocí tlačítka na kartě ladit jako normální.

    ![VS Code – tlačítko ladění](../media/vscode-debug-button.png)

    > [!TIP]
    > Můžete se také zúčastnit relace ladění sady Visual Studio z VS Code a naopak. Další informace najdete v [pokynech k aplikaci Visual Studio](vs.md#co-debugging) ve společném ladění.

Jakmile se ladicí program připojí na straně hostitele, všechna hosta se také automaticky připojí. I když je na počítači hostitele spuštěná jedna ladění "relace", všichni účastníci jsou k němu připojeni a mají vlastní zobrazení.

![Připojený ladicí program VS Code](../media/vscode-debugger.png)

Kdokoli může procházet proces ladění, který umožňuje bezproblémové přepínání mezi spolupracovníky bez nutnosti vyjednávání řízení.

> [!NOTE]
> Stav funkcí ladění podle jazyků a platforem najdete v článku [o podpoře platforem](../reference/platform-support.md).

Každý spolupracovníka může prozkoumat různé proměnné, přejít na jiné soubory v zásobníku volání, kontrolovat proměnné a dokonce přidávat nebo odebírat zarážky. Funkce společného úprav pak umožní každému účastníkovi Orator sledovat, kde jsou ostatní, a poskytnout tak jedinečnou schopnost plynule přepínat mezi současným zkoumáním různých aspektů problému a laděním v rámci spolupráce.

> [!NOTE]
> V relaci pro spolupráci, která je jen pro čtení, Host nebude moci procházet procesem ladění. Mohou však stále přidávat nebo odebírat zarážky a kontrolovat proměnné.

![Animace souběžného ladění](../media/co-debug.gif)

### <a name="change-when-vs-code-joins-debugging-sessions"></a>Změnit, když se VS Code spojí s relacemi ladění

Ve výchozím nastavení se jako host automaticky připojí k ladicím relacím, když jsou sdíleny hostitelem. V některých případech ale může dojít k narušení tohoto chování. Naštěstí je můžete změnit následujícím způsobem:

Jednoduše **upravte Settings. JSON** (> předvolby souboru > nastavení), přidejte jeden z následujících řádků a pak restartujte vs Code:

| Nastavením | Předvídatelně |
|---------|----------|
|``"liveshare.joinDebugSessionOption":"Automatic"`` | Výchozí nastavení Jako host se automaticky připojíte k libovolné sdílené relaci ladění, kterou hostitel spustí. |
| ``"liveshare.joinDebugSessionOption":"Prompt"`` | Jako host se zobrazí výzva k tomu, zda se chcete připojit ke sdílené relaci ladění při jejím spuštění hostitelem. |
| ``"liveshare.joinDebugSessionOption":"Manual"`` | Jako host bude nutné ručně připojit všechny relace ladění. Viz [odpojování a opětovné připojení](#detaching-and-reattaching). |

### <a name="detaching-and-reattaching"></a>Odpojování a opětovné připojování

Jako hosta můžete chtít dočasně zastavit ladění. Naštěstí můžete jednoduše kliknout na ikonu stop (zastavit) na panelu nástrojů ladění a odpojit ladicí program bez vlivu na hostitele nebo jiné hosty.

![VS Code – tlačítko pro zastavení ladicího programu](../media/vscode-debug-stop.png)

Pokud jste aktualizovali nastavení, takže se už nebudete automaticky připojovat, nebo pokud se chcete jednoduše znovu připojit později, můžete to udělat stisknutím **kombinace kláves CTRL + SHIFT + P/Cmd + Shift + P** nebo **kliknutím** na položku stavového řádku stavu relace a výběrem možnosti připojit ke sdílenému ladění. Relace ".

![VS Code připojit ladicí program](../media/vscode-reattach.png)

### <a name="sharing-the-running-application-in-a-browser"></a>Sdílení běžící aplikace v prohlížeči

Visual Studio Code nemá koncept známého "portu webové aplikace", jako je například Visual Studio pro typy projektů, jako je například ASP.NET. Pokud se však připojujete k relaci spolupráce z hostitele sady Visual Studio, může se automaticky zobrazit výchozí prohlížeč při spuštění ladění, které se pak automaticky připojí k aplikacím hostitele, na kterých běží. Další podrobnosti najdete v tématu [funkce sady Visual Studio](vs.md#automatic-web-app-sharing) .

Jako hostitel můžete dosáhnout podobného způsobu ručním sdílením aplikace nebo jiných koncových bodů, jako jsou RESTful Services, pomocí funkce sdílet místní server. Visual Studio a VS Code hostů potom můžou otevřít prohlížeč na stejném portu localhost a zobrazit spuštěnou aplikaci.  Další podrobnosti najdete v tématu věnovaném [sdílení serveru](#share-a-server) .

## <a name="share-a-server"></a>Sdílení serveru

V době od času jako hostitel relace pro spolupráci můžete zjistit, že chcete sdílet webové aplikace nebo jiné místně běžící servery nebo služby s hosty. To může být v rozsahu od jiných RESTful koncových bodů databází a dalších serverů. Visual Studio Live Share vám umožní zadat číslo místního portu, případně jim přiřadit název a potom ho sdílet se všemi hosty.

Hosté pak budou mít přístup k serveru, který jste sdíleli na tomto portu z vlastního místního počítače na stejném stejném portu. Pokud například sdílíte webový server **běžící na portu 3000**, může host přistupovat ke stejnému běžícímu webovému serveru na svém **vlastním počítači** v http://localhost:3000! To se provádí prostřednictvím zabezpečeného tunelu SSH nebo SSL mezi hostitelem a hostů a ověřených prostřednictvím služby, abyste měli jistotu, že budou mít přístup jenom uživatelé v relaci spolupráce.

> **Tip zabezpečení:** Jako hostitel byste měli být velmi selektivní pomocí portů, které sdílíte s hosty, a přidružit je k portům aplikací (místo sdílení portu systému). Pro hosty se budou sdílené porty chovat stejně, jako by byly spuštěné na svém vlastním počítači na serveru nebo službě. To je velmi užitečné, ale pokud je nesprávný port sdílený, může být také riskantní.

Pro účely zabezpečení jsou k dispozici pouze servery, které jsou spuštěny na zadaných portech pro ostatní hosty. Naštěstí je snadné přidat ho jako **hostitele**relace pro spolupráci. Tady je postup:

1. Otevřete Live Share vlastní kartu na řádku VS Code aktivity nebo v zobrazení Průzkumník Live Share a vyberte sdílet server... položku nebo klikněte na ikonu.

    ![VS Code sdílet místní server](../media/vscode-share-local-server-viewlet.png)<br />

1. Zadejte číslo portu, na kterém server běží, a volitelně i název.

    ![Snímek obrazovky s výzvou k zadání čísla portu](../media/vscode-enter-port.png)<br />

A je to! Server na portu, který jste zadali, se teď namapuje na localhost každého hostitele na stejném portu (Pokud se tento port už nepoužívá)!

Pokud se port již používá v počítači hosta, je automaticky vybrán jiný. Naštěstí se jako host zobrazí seznam aktuálně sdílených portů (podle názvu, pokud je zadaný), na kartě zobrazení Live Share nebo vlastní karty na panelu VS Code aktivity a v seznamu sdílené servery. Výběr položky otevře tento server v prohlížeči. Můžete také kliknout pravým tlačítkem a vybrat možnost zkopírovat odkaz na server do schránky.

![Přístup k místnímu serveru VS Code](../media/vscode-access-shared-server-viewlet.png)<br />

Všimněte si, že *hosté nemůžou* řídit, které porty v počítači hostitele se sdílejí z bezpečnostních důvodů.

Chcete-li **ukončit** sdílení místního serveru jako hostitele, najeďte myší na položku serveru v seznamu sdílené servery na kartě zobrazení nebo vlastní karty aplikace Live Share Explorer a klikněte na ikonu zrušit sdílení serveru.

![VS Code zastavit sdílení serveru](../media/vscode-stop-sharing-server-viewlet.png)<br />

## <a name="share-a-terminal"></a>Sdílení terminálu

Moderní vývojáři často používají celou řadu nástrojů příkazového řádku. Naštěstí Live Share umožňuje jako hostitele volitelně "sdílet terminál" s hosty. Sdílený terminál může být jen pro čtení nebo zcela spolupracovat, takže vy i hosté můžou spustit příkazy a zobrazit výsledky. Hostům můžete umožnit zobrazení výstupu terminálu nebo umožnit jim získat praktická a spuštěná testování, sestavení nebo dokonce třídění problémů specifických pro prostředí, ke kterým dochází pouze v počítači.

Ale terminály nejsou **ve výchozím nastavení sdílené,** protože dávají hostům alespoň přístup jen pro čtení k výstupu příkazů, které spouštíte (Pokud není možnost spouštět samotné příkazy). Tímto způsobem můžete volně spouštět příkazy v místních terminálech bez rizika a sdílet je jenom v případě, že to skutečně vyžaduje. Sdílené terminály můžou navíc spustit jenom hostitelé a zabránit tak tomu, aby mohli hosté spustit jednu z nich a něco neočekáváte nebo nesledujete.

Jako hostitel můžete terminál sdílet otevřením Live Share vlastní karty na panelu VS Code aktivity nebo v zobrazení Průzkumník Live Share a výběrem možnosti "sdílet server...". zadání nebo kliknutí na ikonu.

![VS Code sdílet terminál](../media/vscode-share-terminal-viewlet.png)<br />

V tomto okamžiku můžete z nabídky vybrat terminálu jen pro čtení nebo pro čtení a zápis. Když je terminál pro čtení a zápis, každý může do terminálu zadat, včetně hostitele, což usnadňuje zaznamenání toho, jestli uživatel nedělá něco, co nelíbíte. Aby bylo ale bezpečné, měli byste **hostům udělit přístup pro čtení a zápis jenom v případě, že víte, že ho skutečně potřebují** a že mají na scénářích, kde chcete, aby host zobrazil výstup všech spuštěných příkazů.

> [!NOTE]
> Pokud je relace spolupráce v režimu jen pro čtení, může hostitel sdílet jenom terminály jen pro čtení.

![Výběr jen pro čtení nebo čtení/zápis](../media/vscode-share-terminal-ro-rw.png)<br />

Jakmile vyberete typ sdíleného terminálu, který chcete spustit, na kartě terminály VS Code se zobrazí nový sdílený terminál.

![Běh sdíleného terminálu](../media/vscode-share-terminal-up.png)<br />

Pokud sdílíte více terminálů, nebo se fokus nachází na jiné kartě, můžete se zaměřit na konkrétního terminálu tak, že vyberete položku v seznamu sdílené terminály.

![Zaměřte se na sdílený terminál](../media/vscode-shared-terminal-focus.png)<br />

Chcete-li ukončit relaci terminálu, stačí zadat příkaz exit, zavřít okno terminálu nebo kliknout na ikonu zrušit sdílení terminálu v zobrazení Průzkumníka Live Share nebo na vlastní kartě a každý bude odpojen.

## <a name="session-states"></a>Stavy relací

Po spuštění nebo připojení relace spolupráce a přístup ke sdílenému obsahu Visual Studio Live Share položky stavového řádku aktualizují jejich vzhled tak, aby odrážel stav aktivní relace spolupráce.

Tady jsou stavy, které obvykle vidíte:

| Stav | Stavový řádek | Popis |
|-------|--------------------|-------------|
| Termín | ![Stav VS Code: neaktivní](../media/vscode-status-share.png) | Žádná aktivní relace spolupráce a nic se nesdílí. |
| Hostitel: probíhá sdílení. | ![Stav VS Code: probíhá sdílená složka.](../media/vscode-status-sharing.png)| Spouští se relace spolupráce a v krátké době začne sdílení obsahu. |
| Hostitel: sdílení | ![Stav VS Code: sdílení aktivní ](../media/vscode-status-active.png)| Relace spolupráce je aktivní a obsah se sdílí. |
| Hostitel: sdílení jen pro čtení | ![Stav VS Code: sdílí se jen pro čtení.](../media/vscode-status-sharing-read-only.png)| Sdílení relace pro spolupráci jen pro čtení. |
| Host: připojení relace | ![Stav VS Code: spojování](../media/vscode-status-joining.png)| Připojení k existující relaci spolupráce |
| Host: připojeno | ![Stav VS Code: připojeno](../media/vscode-status-active.png) | Připojená a připojená k aktivní relaci spolupráce a příjem sdíleného obsahu. |
| Host: připojeno jen pro čtení | ![Stav VS Code: připojeno jen pro čtení](../media/vscode-status-joined-read-only.png) | Připojeno a připojeno k aktivní relaci pro spolupráci jen pro čtení. |

## <a name="guest-limitations"></a>Omezení hostů

I když jsou v současné době k dispozici některé nedostatky hostů, při používání výše popsaných funkcí si hostitel relace spolupráce zachová kompletní funkce jejich nástroje podle vlastního výběru. Další informace najdete v následujících tématech:

- [Podpora jazyků a platforem](../reference/platform-support.md)
- [Podpora rozšíření](../reference/extensions.md)
- [Všechny hlavní chyby, žádosti o funkce a omezení](https://aka.ms/vsls-issues)
- [Všechny požadavky a omezení funkcí](https://aka.ms/vsls-feature-requests)
- [Odstraňování potíží](../troubleshooting.md)

## <a name="next-steps"></a>Další kroky

Další informace najdete v těchto dalších článcích.

- [Rychlý Start: sdílení prvního projektu](../quickstart/share.md)
- [Rychlý Start: připojení první relace](../quickstart/share.md)
- [Postupy: spolupráce pomocí sady Visual Studio](vs.md)
- [Požadavky na připojení pro Live Share](../reference/connectivity.md)
- [Funkce zabezpečení Live Share](../reference/security.md)
- [Podrobnosti instalace pro Linux](../reference/linux.md)

Máte potíže? Podívejte se na článek o [odstraňování potíží](../troubleshooting.md) nebo nám [pošlete svůj názor](../support.md).
