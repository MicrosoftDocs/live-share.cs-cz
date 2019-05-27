---
title: Spolupráce pomocí Visual Studio Code – Visual Studio Live Share | Dokumentace Microsoftu
description: Nastavení spolupráci postupy pro Visual Studio Code a Live Share.
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
ms.openlocfilehash: bda0ca256af4a561724d96777e640eec1ca0f0fb
ms.sourcegitcommit: bfa1020882095fcc7d31cd71cf1f2e601e3bea06
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/25/2019
ms.locfileid: "66224728"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="how-to-collaborate-using-visual-studio-code"></a>Postupy: Spolupráce ve Visual Studio Code

Jste připraveni k získání spolupráce s Live Share v nástroji VS Code?  Pokud ano, jste na správné místo! V tomto článku jsme vás provedeme jak používat některé specifické funkce v aplikaci Visual Studio Live Share rozšíření pro Visual Studio Code.

Všimněte si, že všechny aktivity spolupráce je zde popsáno, zahrnují jeden **hostitele relace spolupráci** a jeden nebo více **hosté**. Hostitel je osoba, která relaci spolupráce zahájila, a host je každý, kdo se k relaci připojí.

*Hledáte stručné shrnutí? Podívejte se [sdílet](../quickstart/share.md) nebo [spojení](../quickstart/join.md) rychlých startů místo.*

> [!TIP]
> Víte, že se můžete *připojit k vlastní relaci spolupráce*? Díky tomu si můžete Live Share vyzkoušet sami nebo můžete rozjet instanci Visual Studia nebo VS Code a vzdáleně se k ní připojit. V obou případech můžete použít i stejnou identitu. Vyzkoušejte to!

## <a name="installation"></a>Instalace

Než začnete, budete potřebovat k mít jistotu, že máte verzi Visual Studio nainstalovat kód, který splňuje základní požadavky na Live Share. Budete potřebovat **Visual Studio Code (1.22.0 nebo vyšší)** běžící na:

- **Windows:** 7, 8.1 nebo 10

- **macOS**: Sierra (10.12) a výše pouze.
    - _El Capitan (10.11) a dále z důvodu nejsou aktuálně podporovány [požadavky rozhraní .NET Core 2.0](https://go.microsoft.com/fwlink/?linkid=872315)._

- **Linux:** 64-bit Desktop Ubuntu 16.04 +, Fedora pracovní stanice 27 +, CentOS 7

    - Sdílené složky za provozu vyžaduje několik [požadavky pro Linux](#linux-install-steps) můžete být vyzváni k instalaci.
    - _32bitová verze systému Linux není podporována z důvodu [požadavky rozhraní .NET Core 2.0](https://go.microsoft.com/fwlink/?linkid=872314)._
    - Také se aktuálně nepodporuje ARM.
    - Zobrazit [Linuxem nainstalovat podrobnosti](../reference/linux.md) , kde najdete podrobnosti o použití distribuce příjem dat a další.

Stažení a instalace rozšíření Visual Studio Live Share pak bude hračka:

1. Install <a href="https://code.visualstudio.com/">Visual Studio Code</a>
2. [Stáhněte si](https://aka.ms/vsls-dl/vscode) a nainstalovat rozšíření Visual Studio Live Share z webu marketplace.
3. Znovu načíst Visual Studio Code
4. Počkejte závislostí ke stažení a instalaci (viz stavový řádek).<br/>
    ![Dokončení instalace](../media/vscode-finishing-install.png)
5. **Linux:** Pokud se zobrazí oznámení o instalaci chybějící knihovny:
    1. Klikněte na tlačítko "Instalaci" v oznámení.
    2. Zadejte heslo správce (sudo), po zobrazení výzvy.
    3. Znovu spusťte VS Code, až budete hotovi.

Stažením a používáním rozšíření Visual Studio Live Share vyjadřujete souhlas s [licenčními podmínkami](https://aka.ms/vsls-license) a [prohlášením o zásadách ochrany osobních údajů](https://www.microsoft.com/en-us/privacystatement/EnterpriseDev/default.aspx). Pokud narazíte na problémy, podívejte se na článek o [odstraňování potíží](../troubleshooting.md).

[![Stáhnout](../media/download.png)](https://aka.ms/vsls-dl/vscode)

### <a name="linux-install-steps"></a>Postup instalace v Linuxu

Je velmi proměnlivé prostředí na systémy Linux a k velkému počtu desktopové prostředí a distribuce může být složité začít pracovat. Pokud zůstanou podporovaných verzích **Ubuntu Desktop** (16.04 +) nebo **pracovní stanice Fedora** (27 +), **CentOS 7** a používat pouze **oficiální distribuce VS Kód**, měli byste najít proces jednoduché. V případě, že používáte nestandardní konfiguraci nebo podřízené distribuce, ale může nebo nemusí narazíte na nějaké bude odolný vůči kolísání. Zobrazit [podrobné informace o instalaci Linux](../reference/linux.md) Další informace.

#### <a name="install-linux-prerequisites"></a>Nainstalujte požadavky pro Linux

Některých distribucích systému Linux jsou chybějící knihovny, Live Share musí fungovat. Ve výchozím nastavení Live Share pokusí rozpoznat a nainstalujte požadavky pro Linux za vás. Zobrazí se vám oznámení s informační zprávou při Live Share dojde k potížím, které můžou pocházet z chybějící knihovny, která žádá o oprávnění k instalaci.

![Chybí informační zpráva zobrazující požadavky tohoto systému Linux](../media/vscode-linux-prereq-missing.png)

Po kliknutí na "Instalaci" okně terminálu se zobrazí, ve kterém bude nutné zadat vaše heslo správce (sudo) Chcete-li pokračovat. Za předpokladu, že se že úspěšně nedokončí, restartujte Visual Studio Code, by měly být všechny nastavíte! Můžete také zkontrolovat **[tipy distribucí](../reference/linux.md#tips-by-distribution)** jiných pomocných parametrů a alternativní řešení, pokud nějaké existují.

Pokud se zobrazí zpráva, skript nepodporuje vaší distribuci, naleznete v tématu **[tipy pro komunity podporované distribuce](../reference/linux.md#tips-for-community-supported-distros)** informace komunita sdílí s námi.

Pokud jste **nechcete mít VS Code, spusťte příkaz pro vás**, můžete se také rozhodnout k opětovnému spuštění nejnovější verze tohoto skriptu kdykoli ručně spuštěním následujícího příkazu z okna terminálu:

    wget -O ~/vsls-reqs https://aka.ms/vsls-linux-prereq-script && chmod +x ~/vsls-reqs && ~/vsls-reqs

#### <a name="linux-browser-integration"></a>Linux integration prohlížeče

Visual Studio Live sdílet obvykle **nevyžaduje další instalační kroky** se povolit integraci prohlížeče v Linuxu.

Při neobvyklé, v některých distribucích budete **může být oznámeno, že vaše heslo správce (sudo) je vyžadována** k dokončení procesu instalace. Okno terminálu se zobrazí informující o nainstalovanou Spouštěč prohlížeče. Jednoduše zadejte svoje heslo po zobrazení výzvy a stisknutím klávesy enter po dokončení instalace zavřete okno terminálu.

Můžete si přečíst další informace o Proč je to nezbytné, a kde Live sdílet místa soubory  **[tady](../reference/linux.md#linux-browser-integration)**. Mějte na paměti i v případě, že nebudete moci začít pracovat integrace prohlížeče se můžete stále  **[ručně připojit k relacím spolupráci](../use/vscode.md#join-manually)**.

## <a name="sign-in"></a>Přihlášení

Pokud chcete spolupracovat, budete potřebovat k přihlášení do Visual Studio Live Share, takže všichni ví, kdo jste. Jedná se čistě v rámci bezpečnostních opatření a nemá **není** přihlašují jakékoli marketing nebo jiných výzkumu. Můžete se přihlásit pomocí osobního účtu Microsoft (třeba @outlook.com), zajišťuje Microsoft pracovní nebo školní účet (AAD) nebo účet GitHub. Přihlášení je snadné.

**Klikněte na tlačítko** na "Live Share" stavový řádek položky nebo stisknutím klávesy **Ctrl + Shift + P / Cmd + Shift + P** a vyberte "živé sdílené složky: Přihlaste se pomocí prohlížeče"příkaz.

![VS Code přihlašovací tlačítko](../media/vscode-sign-in-button.png)

Oznámení se zobrazí s výzvou, abyste se přihlásili pomocí webového prohlížeče. Kliknutím na "spuštění přihlášení" otevřete prohlížeč, můžete použít k dokončení procesu přihlášení. Zavřete prohlížeč, až budete hotovi.

![Informační zpráva s výzvou k přihlášení pomocí webového prohlížeče](../media/vscode-sign-in-toast.png)

> **Uživatelé Linuxu:** Můžete být vyzváni k zadání uživatelského kódu, pokud používáte starší verzi Live Share (v0.3.295 nebo níže). Aktualizovat na nejnovější verzi rozšíření, nebo klikněte "s vlastním?" Chcete-li zobrazit kód odkaz po přihlášení. Zobrazit [níže podrobnosti](#sign-in-using-a-user-code).

#

> **Pokročilé tip:** `liveshare.account` a `liveshare.accountProvider` nastavení umožňuje vybrat, který účet se použije pro automatické přihlášení v případě, že jste do mezipaměti přihlašovací údaje k několika účtům, které jsou k dispozici. 

> Představte si například, že při práci na 2 projekty, které se chcete přihlásit pomocí jiné identity. V pracovním prostoru nastavení VSCode, můžete nastavit `liveshare.account` nastavení na různé e-mailové adresy v každém adresáři projektu, aby každá automaticky přihlásit pod správným účtem. `liveshare.accountProvider` Nastavení může být nastaven na hodnotu `"microsoft"` nebo `"github"` v případě, že používáte stejnou e-mailovou adresu s několika poskytovateli.

Pokud Visual Studio Code se ujímají přihlášení po dokončení procesu přihlášení v prohlížeči, přečtěte si téma [Přihlaste se pomocí uživatelského kódu](#sign-in-using-a-user-code). Jinak, podívejte se na [řešení potíží s](../troubleshooting.md#sign-in) další tipy.

### <a name="sign-in-using-a-user-code"></a>Přihlaste se pomocí uživatelského kódu

Pokud používáte o problémech s VS Code není ujímají dokončené přihlášení, můžete místo toho zadat "uživatelský kód".

1. Stisknutím klávesy **Ctrl + Shift + P / Cmd + Shift + P** a spustit "živé sdílené složky: Přihlaste se pomocí uživatelského kódu"příkaz.

2. V prohlížeči by se zobrazit použijte dokončete proces přihlašování.

    > [!NOTE]
    > Pokud prohlížeč nezobrazí automaticky, otevřete [toto umístění](https://insiders.liveshare.vsengsaas.visualstudio.com/auth/login) v prohlížeči a přihlaste se.

3. Jakmile budete hotovi, klikněte na tlačítko "se nedaří? Kliknutím sem ohledně kódu uživatele"Pokud chcete zobrazit kód uživatele.

    ![Obrázek uživatelského kódu v prohlížeči](../media/vscode-user-code-browser.png)

4. Zkopírujte kód uživatele.

5. Nakonec vložte kód uživatele do vstupního pole, které se zobrazovalo při spuštění příkazu a stisknutím klávesy enter dokončete proces přihlašování.

    ![Obrázek vstupní pole kódu uživatele](../media/vscode-user-code.png)

## <a name="using-the-live-share-viewlet"></a>Pomocí Live Share viewlet

Po instalaci Visual Studio Live Share, přidá vlastní kartu na panelu aktivit VS Code. Na této kartě můžete přistupovat všechny funkce Live Share ke spolupráci. Kromě toho při sdílení a připojte se k relaci spolupráce, zobrazení se zobrazí také na kartě Průzkumník pro přístup k všechny tyto funkce také.

<table style="border: none;">
<tr style="border: none;">
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vscode-custom-tab.png" width="100%" alt="Live Share custom tab" />
    </td>
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vscode-explorer-view.png" width="100%" alt="Live Share explorer view"
</tr>
</table>

V těchto zobrazeních můžete zobrazit účastníka umístění sdíleného kódu, klikněte na účastníkem sledování, zaměřte účastníky, přístup ke sdílené servery a terminály a další.

## <a name="using-the-scoped-command-menu"></a>Pomocí vymezených příkazu nabídky

Kromě toho jsou všechny funkce aplikace Visual Studio Live Share dostupné z Visual Studio Code "Paletu příkazů", který je přístupný stisknutím kombinace kláves Ctrl + Shift + P / Cmd + Shift + P nebo stisknutím F1. Úplný seznam příkazů můžete najít zadáním "živé sdílení".

Vzhledem k tomu, že tento seznam můžete získat dlouho, možná bude jednodušší využít s vymezeným oborem příkaz nabídky, který je k dispozici ve stavovém řádku. Kliknutím na přihlášení / ikonu stavu relace ve stavovém řádku se okamžitě zobrazí contextualized seznam příkazů, které jsou k dispozici pro použití.

![Ikona stavu relace VS Code](../media/vscode-share-state.png)

## <a name="share-a-project"></a>Sdílení projektu

Po stažení a instalaci Visual Studio Live Share, postupujte podle následujících kroků spustit relaci spolupráci a pozvat kolegu pro práci s vámi.

1. **Přihlásit se**

    Po instalaci rozšíření Live Share, znovu načíst a čeká se závislosti pro dokončení instalace, budete chtít přihlásit, aby další spolupracovníci vědět, kdo jste. Zobrazit [přihlášení](#sign-in) další podrobnosti.

2. **Otevřít složku**

    Otevřete složku, projekt nebo řešení, které chcete sdílet s vaší hostů pomocí normálním pracovním postupu.

3. **[Volitelné] Vyloučeno nebo skryté soubory aktualizace**

    Ve výchozím nastavení, Live Share **skryje** všech souborů a složek odkazovat v souborech .gitignore ve sdílených složkách hostů. **Skrytí** soubor zabraňuje zobrazování v stromovou strukturu souborů hosta. **S výjimkou** souboru se vztahuje přísnější pravidla, které brání otevření pro hostovaný v situacích, jako přejít k definici nebo pokud jste se přesunuli do souboru při ladění nebo "splňovalo" Live Share. Pokud chcete skrýt nebo vyloučit jiné soubory, **. vsls.json** soubor lze přidat do projektu s tímto nastavením. Zobrazit [řízení přístupu k souborům a viditelnost](../reference/security.md#controlling-file-access-and-visibility) podrobnosti.

4. **Spustit relaci spolupráce**

    Nyní jednoduše **klikněte na tlačítko** "Live Share" stavový řádek položky nebo položek **Ctrl + Shift + P / Cmd + Shift + P** a vyberte "sdílené složky za provozu: Spustit relaci spolupráce (sdílet) ".

    ![Tlačítko sdílet](../media/vscode-share-button.png)

    > [!NOTE]
    > Můžete být vyzváni softwarem klasické pracovní plochy brány firewall umožňující Live Share agenta pro otevření portu okamžiku, kdy budete sdílet. Přijímá to je naprosto volitelné, ale umožňuje zabezpečené "přímý režim" ke zlepšení výkonu při osoby, že pracujete s je ve stejné síti jako vy. Zobrazit [Změna režimu připojení](../reference/connectivity.md#changing-the-connection-mode) podrobnosti.

    Odkaz na pozvánku bude automaticky zkopíruje do schránky. Při otevření v prohlížeči, tento odkaz umožňuje ostatním uživatelům připojit se k nové relaci spolupráce, který s nimi sdílí obsah těchto složek.

    Zobrazí se také přechodu "Live Share" stav panelu položku představující stav relace. Zobrazit [stav relace](#session-states) následující informace pro jak to vypadá.

    Všimněte si, že pokud je potřeba získat odkaz na pozvánku znovu po jste začali, sdílení, můžete k němu přístup znovu kliknutím na ikonu panelu Stav stavu relace a vybrat pozvat ostatní (Kopírovat odkaz).

5. **[Volitelné] Povolení režimu jen pro čtení**

    Po spuštění relace spolupráce, můžete nastavit relace, která má být jen pro čtení pro hosty zabránit v provádění úprav kódu sdílením.

    Po sdílení, zobrazí se oznámení, pozvánky odkaz byl zkopírován do schránky. Pak můžete vybrat možnost nastavit relaci jen pro čtení.

    ![Režimu jen pro čtení VS Code](../media/vscode-read-only-toast.png)

6. **Odeslání odkazu**

    Odkaz na odeslání e-mailu, Slack, Skype, atd. a těch, které chcete pozvat. Všimněte si, že udělená úroveň přístupu, Live Share relací může poskytovat hosté, **pouze by měly sdílet s lidmi, kterým důvěřujete** a přemýšlení prostřednictvím důsledky sdílení.

    > **Tip zabezpečení:** Chcete pochopili důsledky zabezpečení některé funkce Live Share? Podívejte se [zabezpečení](../reference/security.md) článku.

    Pokud vás pozvat hosta má otázky, "[rychlý start: Připojte se k relaci první](../quickstart/join.md)"článek poskytuje některé další informace o zprovoznění jako Host.

7. **[Volitelné] Schválit hosta**

    Ve výchozím nastavení hosté se automaticky připojí k relaci spolupráci a budete upozorněni na kdy jsou připraveni spolupracovat s vámi. Zatímco tato oznámení obsahují možností jejich odebrání z relace, můžete se také rozhodnout tak, aby místo toho vyžadovala explicitní "schválení" pro každého připojení.

    Pokud chcete povolit tuto funkci, jednoduše přidejte následující do settings.json:

         "liveshare.guestApprovalRequired": true

    Jakmile budete mít toto nastavení zapnuté, oznámení vás vyzve k předtím, než bylo možné připojit ke schválení hosta.

    ![Žádost o schválení připojení k Visual Studio Code](../media/vscode-join-approval.png)

    V tématu [pozvánky a spojení přístup](../reference/security.md#invitations-and-join-access) najdete další podrobnosti o pozvání aspekty zabezpečení.

To je všechno!

### <a name="stop-the-collaboration-session"></a>Zastavit relaci spolupráce

Jako hostitele můžete ukončit sdílení úplně a ukončení relace spolupráce v každém okamžiku otevření zobrazení Live Share v Průzkumníku nebo na vlastní kartě Live Share a výběrem ikony "Zastavit relaci spolupráce".

![Zastavit relaci spolupráce](../media/vscode-end-collaboration-viewlet.png)

Všechny hostů budete informováni, že relace skončila.  Jakmile relace skončila, guests nebude mít přístup k obsahu a všechny dočasné soubory se automaticky vyčistí.

Máte problémy s sdílení? Podívejte se na [řešení potíží s](../troubleshooting.md#share-and-join).

## <a name="join-a-collaboration-session"></a>Připojte se k relaci spolupráce

Po stažení a instalaci Visual Studio Live Share, guests stačí provést několik kroků připojit k relaci prostředí pro spolupráci. Existují dva způsoby, jak připojit: [prostřednictvím prohlížeče](#join-via-the-browser) a [ručně](#join-manually).

> **Tip zabezpečení:** V roli hosta připojení k relaci spolupráce je důležité pochopit, že hostitelé může omezit přístup k určité soubory nebo funkce. Chcete si uvědomit důsledky zabezpečení některých funkcích a nastaveních Live Share? Podívejte se [zabezpečení](../reference/security.md) článku.

### <a name="join-via-the-browser"></a>Připojte se k prostřednictvím prohlížeče

Nejjednodušší způsob, jak připojit ke spolupráci relaci je jednoduše otevřete odkaz na pozvánku ve webovém prohlížeči. Zde je, co můžete očekávat Pokud budete postupovat podle tohoto toku.

1. **Přihlásit se**

    Po instalaci rozšíření Live Share, znovu načíst a čeká se závislosti pro dokončení instalace, budete chtít přihlásit, aby další spolupracovníci vědět, kdo jste. Zobrazit [přihlášení](#sign-in) další podrobnosti.

2. **Klikněte na odkaz na pozvánku nebo pozvání otevřít v prohlížeči**

    Teď stačí otevřít místní (nebo znovu otevřete) odkaz pozvání v prohlížeči.

    > **Poznámka:** Pokud jste ještě nenainstalovali rozšíření Live Share, zobrazí se vám s odkazy na marketplace pro rozšíření. Instalace rozšíření a restartujte nástroj a zkuste to znovu.

    Zobrazí se oznámení, spustí se nástroj Live Share povolené vyžaduje prohlížeče. Pokud jste povolili jeho spuštění vybrané nástroje, už budete připojíte k relaci spolupráce po jeho spuštění.

    ![Připojte se k stránky](../media/join-page.png)

    Pokud je hostitel v režimu offline, zobrazí se upozornění v tuto chvíli místo. Potom můžete kontaktovat hostitele a požádejte ho, aby znovu sdílet.

    > [!NOTE]
    > Ujistěte se, když jste **alespoň jednou spuštěn nástroj** po instalaci rozšíření Visual Studio Live Share a povolené na dokončení před levou nebo jejich opakované-opening pozvánku stránce instalace. Stále se nedaří? Zobrazit [ručně připojit](#join-manually).

3. **Spolupráce**

    A to je vše! Za malou chvíli bude připojen a můžete začít spolupracovat.

    Zobrazí se tlačítko "Live Share" přechod k předání "Stav relace". Zobrazit [stav relace](#session-states) následující informace pro jak to vypadá.

    Potom automaticky přejdete do souboru hostitele je právě se upravuje po dokončení připojení.

### <a name="join-manually"></a>Připojte se k ručně

Můžete také ručně připojit bez použití webového prohlížeče, které mohou být užitečné v situacích, kdy už běží nástroj, který chcete použít, chcete použít jiný nástroj, než lze obvykle provést, nebo pokud máte potíže s získávání pozvat odkazy na pracovní z nějakého důvodu. Postup je jednoduchý:

1. **Přihlásit se**

    Po instalaci rozšíření Live Share, znovu načíst a čeká se závislosti pro dokončení instalace, budete chtít přihlásit, aby další spolupracovníci vědět, kdo jste. Zobrazit [přihlášení](#sign-in) další podrobnosti.

2. **Použití příkazu join**

    Otevřete Live Share vlastní kartu na panelu aktivit VS Code a vyberte "připojení k relaci spolupráce..." ikona nebo položku.

    ![Ikona viewlet spojení](../media/vscode-join-viewlet.png)

3. **Vložte odkaz pozvánky**

    Vložte adresu URL pozvánky byly odeslány a stiskněte enter, čímž potvrdíte.

4. **Spolupracujte!**

    A to je vše! Musí být připojené k okamžité relaci spolupráce.

    Zobrazí se tlačítko "Live Share" přechod k předání "Stav relace". Zobrazit [stav relace](#session-states) následující informace pro jak to vypadá.

    Potom automaticky přejdete do souboru hostitele je právě se upravuje po dokončení připojení.

### <a name="leave-the-collaboration-session"></a>Nechte relaci spolupráce

V roli hosta můžete nechat relaci spolupráce bez ukončení pro ostatní jednoduše zavřením okna nástroje VS Code. Pokud si přejete nechte okno otevřené, můžete otevřít zobrazení Live Průzkumníka sdílené složky nebo na vlastní kartu Live Share a vyberte ikonu "Nechte relaci spolupráce".

![Ikona ponechá relace](../media/vscode-leave-session-viewlet.png)

Všechny dočasné soubory se automaticky vyčistí proto není potřeba žádná další akce.

Potíže s připojení? Podívejte se na [řešení potíží s](../troubleshooting.md#share-and-join).

## <a name="co-editing"></a>Společné úpravy

Po Host připojena ke spolupráci relace, všechny spolupracovníci okamžitě bude moci zobrazit úpravy a výběry v reálném čase. Všechno, co je třeba provést je v Průzkumníku souborů vyberte soubor a můžete začít upravovat. Hostitelích a hostech uvidí úpravy daly a sami díky tomu je snadné iterovat a rychle nail nižší řešení můžete přispívat.

> [!NOTE]
> Připojení k relaci spolupráci jen pro čtení zabrání hosté nebudou moct provádět úpravy souborů. Hostitel může [povolení režimu jen pro čtení při sdílení](#share-a-project). V roli hosta, poznáte, pokud jste se připojili relaci jen pro čtení zobrazením vašich [stav relace](#session-states).

![Snímek obrazovky znázorňující společně úpravy](../media/vscode-coedit.png)

> [!NOTE]
> Společné úpravy má omezení pro některé jazyky. Stav funkcí podle jazyků najdete v článku [o podpoře platforem](../reference/platform-support.md).

Kromě kurzory a úpravy jsou také vámi provedených výběrů viditelné pro všechny účastníky, kterými tento stejný soubor. To usnadňuje zvýrazněte kde problémy mohou existovat zprostředkovat nápady.

![Snímek obrazovky znázorňující zvýraznění](../media/vscode-highlight.png)

Ještě lepší je a ostatní účastníky můžete přejít na všechny soubory ve sdíleném projektu. Buď můžete upravit společně nebo samostatně to znamená, že můžete bez problémů přepínat mezi šetření, vytváření, malá vylepšení a úplné společné úpravy.

Výsledný úpravy jsou trvalé na počítači hostitele na Uložit tady není nutné synchronizovat, vkládání nebo odesílání souborů, až budete hotovi úprav. Úpravy existují "právě."

> **Tip zabezpečení:** Zadaný všichni účastníci můžou nezávisle na sobě přejděte a úpravy souborů, jako hostitele, můžete chtít omezit, které soubory Hosté mají přístup k ve vašem projektu prostřednictvím. vsls.json souboru. V roli hosta je také důležité si uvědomit, že se že nezobrazí určité soubory výsledkem tohoto nastavení. Zobrazit [řízení přístupu k souborům a viditelnost](../reference/security.md#controlling-file-access-and-visibility) podrobnosti.

### <a name="changing-participant-flag-behaviors"></a>Změna chování účastníka příznak

Ve výchozím nastavení Visual Studio Live Share automaticky zobrazí "flag" vedle účastníka kurzoru při najetí myší, nebo při úpravách, zvýrazněte nebo přesunutí jejich kurzoru. V některých případech můžete chtít toto chování změnit.

Jednoduše **upravit settings.json** (Soubor > Předvolby > Nastavení), přidejte jeden z následujících řádků a potom znovu spusťte VS Code:

| Nastavení | Chování |
|---------|----------|
| ``"liveshare.nameTagVisibility":"Never"`` | Příznak se zobrazí, pouze když najedete myší kurzor. |
| ``"liveshare.nameTagVisibility":"Activity"`` | Toto nastavení je výchozí. Příznak je viditelné při najetí myší nebo pokud účastník upraví, zvýrazní nebo přesune kurzor. |
| ``"liveshare.nameTagVisibility":"Always"`` | Příznak je vždy viditelné. |

## <a name="following"></a>Následující

Někdy potřebujete objasnit problém nebo návrh, který se týká více souborů nebo míst v kódu. V těchto situacích může být užitečné dočasně použít kolegu při přechodu během celého projektu. Z tohoto důvodu když se připojí k relaci spolupráce automaticky "postupujte podle" hostitele. Podle uživatele, bude zůstávat synchronizovaný s aktuálně otevřený soubor a posuňte pozici editoru.

> [!NOTE]
> Ve výchozím nastavení Live Share složky otevřít externí ke sdílené složce souborů. Pokud chcete tuto funkci zakázat, aktualizujte `liveshare.shareExternalFiles` Live Share k `false` v Settings.JSON v nástroji.

Chcete-li začít sledovat účastníka (jako hostitele nebo hosta), klikněte na jejich název v seznamu účastníků v zobrazení živého Průzkumníka sdílené složky nebo vlastní karta. Kroužek vedle jejich názvu vyplní označující, že je dodržujete.

![Z viewlet postupujte Vscode](../media/vscode-follow-multiple-viewlet.png)

Alternativně můžete kliknout na ikonu připínáčku v pravém horním rohu skupiny editor nebo stisknutím klávesy **Ctrl + Alt + F / Cmd + Alt + F**.

![Pin kód VS](../media/vscode-pin.png)

> [!NOTE]
> Pokud více než jednomu uživateli je v relaci spolupráce, budete vyzváni k výběru účastníka, který chcete sledovat.
>
>![Snímek obrazovky zobrazující seznam spolupracovníků](../media/vscode-list-collaborators.png)

Protože toto je vázán na skupinu editoru, můžete rozdělené zobrazení (nebo rozložení mřížky!) mít skupinu, která sleduje účastník a skupiny, které není. To umožňuje jenom pasivně někdo postupujte při práci i na něco nezávisle na sobě. Se skupinou editor vybraná můžete vybrat účastníka seznam Účastníci mají skupiny postupovat podle nich.

![Pin kód VS v rozděleném zobrazení](../media/vscode-follow-split.png)

Abyste usnadnili snadnou přepínání z "podle režimu" a můžete začít upravovat sami, budete automaticky přestat, sledovat, pokud dojde k některé z těchto:

1. Můžete začít upravovat aktuálně aktivního souboru.
1. Otevřete si jiný soubor
1. Zavřít aktuálně aktivního souboru.

Kromě toho můžete explicitně ukončit po někdo znovu kliknutím na ikonu připínáčku nebo dosažení **Ctrl + Alt + F / Cmd + Alt + F**.

## <a name="listing-participants"></a>Seznam účastníků

Rychlý způsob, jak zjistit, který je v relaci spolupráce je podívat se na seznam účastníků v zobrazení živého Průzkumníka sdílené složky nebo vlastní kartu. Zobrazení se zobrazí všechny účastníky v relaci.

![Ikona snímek obrazovky zobrazující uživatele stavového řádku](../media/vscode-explorer-view.png)

Kliknutím na kterýkoli účastník v tomto seznamu budou postupovat podle nich ve skupině pro aktivní editor.

Alternativně můžete dosáhnete **Ctrl + Shift + P / Cmd + Shift + P** a vyberte "živé sdílené složky: Příkaz list účastníky"nebo **klikněte na tlačítko** na položky stavového řádku, který zobrazuje počet účastníků v relaci.

![Ikona snímek obrazovky zobrazující uživatele stavového řádku](../media/vscode-user-status.png)

Pak se zobrazí seznam všech účastníků v relaci. Na rozdíl od kliknutí na ikonu připínáčku se tento seznam se zobrazí i v případě jednomu uživateli v relaci s vámi, můžete vždy rychle zjistit, kde se nachází někdo jiný. V zájmu usnadnění práce jako ikonu připínáčku můžete pak vybrat jeden z účastníků ze seznamu postupovat podle nich. Pokud chcete místo toho ukončit, stiskněte klávesu ESC.

## <a name="focusing"></a>Zaměření

Občas můžete chtít všem uživatelům v relaci spolupráce se sem a podívejte se na něco, co děláte. Živé sdílené složky můžete pokládat, že všichni "zaměřit" jejich pozornost na vás s oznámením, která umožňuje jednoduše sledovat zpět.

Otevřete na vlastní kartu Live Share v panelu aktivit VS Code nebo v zobrazení Průzkumník Live sdílené složky a vyberte ikonu "Zaměřit účastníky".

![Ikona detailního viewlet](../media/vscode-focus-viewlet.png)

Po spuštění příkazu všichni uživatelé v relaci spolupráce se pak dostanete oznámení, kterou jste požadovali jejich pozornost.

![Oznámení s informační zprávou fokus](../media/vscode-focus-toast.png)

Jsou pak stačí kliknout na "Sledovat" přímo z oznámení až budou připravené na jejich zaměřit na vás.

## <a name="co-debugging"></a>Společné ladění

Visual Studio Live Share na spolupráci funkce ladění je jedinečný a efektivní způsob, jak ladit problém. Kromě povolení prostředí pro spolupráci na řešení problémů také poskytuje vás a ostatní účastníci relace umožňuje prozkoumat problémy, které mohou být konkrétní prostředí tím, že na počítači hostiteli poskytuje sdílené relace ladění.

> **Tip zabezpečení:** Zadaný všichni účastníci můžou nezávisle na sobě přejděte a úpravy souborů, jako hostitele, můžete chtít omezit, které soubory Hosté mají přístup k ve vašem projektu prostřednictvím. vsls.json souboru. Jste měli také něco vědět, že přístup konzoly/REPL znamená, že účastníci spouštět náležité příkazy na svém počítači, by měla pouze společně ladění s těmi, které důvěřujete. V roli hosta je také důležité si uvědomit, že nebudete moci postupujte podle ladicí program vstoupí do určité soubory s omezeným přístupem soubory výsledkem tohoto nastavení. Zobrazit [řízení přístupu k souborům a viditelnost](../reference/security.md#controlling-file-access-and-visibility) podrobnosti.

Její použití je jednoduché.

1. Ujistěte se, že hostitel a všechny Hosté mají odpovídající ladění rozšíření nainstalované. (Technicky to není vždy nutné, ale je obecně vhodné.)

2. Jako hostitele, není-li již nastavili pro projekt, měli byste [nakonfigurovat launch.json](https://code.visualstudio.com/Docs/editor/debugging#_launch-configurations) k ladění aplikace v nástroji VS Code běžným způsobem. Není zapotřebí žádné speciální nastavení.

3. V dalším kroku hostitel může začít ladění pomocí tlačítka v kartě ladění jako za normálních okolností.

    ![Tlačítko ladění VS Code](../media/vscode-debug-button.png)

    > [!TIP]
    > Také se můžete zúčastnit v sadě Visual Studio ladicími relacemi z VS Code a naopak. Podívejte se [sady Visual Studio pokyny](vs.md#co-debugging) společně ladění pro další informace.

Po ladicí program připojí na straně hostitele, jsou také automaticky připojeny všechny hosty. Při jedné "relace ladění" na počítači hostitele všichni účastníci jsou připojené k němu a má své vlastní zobrazení.

![Připojit ladicí program VS Code](../media/vscode-debugger.png)

Všem uživatelům procházení ladění procesu, které umožňuje bezproblémové přepínání mezi spolupracovníci, aniž byste museli vyjednávání ovládacího prvku.

> [!NOTE]
> Stav funkcí ladění podle jazyků a platforem najdete v článku [o podpoře platforem](../reference/platform-support.md).

Každého spolupracovníka můžete prozkoumat různé proměnné, přejít na různé soubory v zásobníku volání, kontrolovat proměnné a dokonce i přidat nebo odebrat zarážky. Společné úpravy funkce pak umožňují každý účastníka krásně sledovat, kde jsou ostatní umístěné, poskytují jedinečné možnost bez problémů přepínání mezi současně zkoumání různých aspektů problém a společně ladění.

> [!NOTE]
> V relaci spolupráci jen pro čtení, nebude možné pro jednotlivé kroky v procesu ladění hosta. Mohou však stále přidat nebo odebrat zarážky a kontrolovat proměnné.

![Animace souběžných ladění](../media/co-debug.gif)

### <a name="change-when-vs-code-joins-debugging-sessions"></a>Při změně VS Code spojení ladicími relacemi

Ve výchozím nastavení jako Host, které budete automaticky připojí k ladicími relacemi, když se sdílí hostitele. Nicméně v některých případech může být pro vás toto chování rušivé. Naštěstí můžete změnit ho následujícím způsobem:

Jednoduše **upravit settings.json** (Soubor > Předvolby > Nastavení), přidejte jeden z následujících řádků a potom znovu spusťte VS Code:

| Nastavení | Chování |
|---------|----------|
|``"liveshare.joinDebugSessionOption":"Automatic"`` | Výchozí nastavení V roli hosta budete automaticky připojí k sdílené ladicí relace, které spuštění hostitele. |
| ``"liveshare.joinDebugSessionOption":"Prompt"`` | V roli hosta zobrazí se výzva, jestli chcete připojit ke sdílené ladicí relaci při spuštění hostitele. |
| ``"liveshare.joinDebugSessionOption":"Manual"`` | V roli hosta budete muset ručně připojit ladicí relace. Zobrazit [odpojení a opětovné](#detaching-and-reattaching). |

### <a name="detaching-and-reattaching"></a>Odpojení a opětovné

V roli hosta můžete chtít Zastavit ladění dočasně. Naštěstí můžete stačí kliknout na ikonu "stop" v panelu nástrojů ladění můžete odpojit ladicí program, aniž by to ovlivnilo jiné hosty nebo hostitele.

![Tlačítko Zastavit ladicí program VS Code](../media/vscode-debug-stop.png)

Pokud jste aktualizovali nastavení tak, že jste už automatické připojení nebo pokud chcete jednoduše znovu připojit později, je to tak, že stisknete **Ctrl + Shift + P / Cmd + Shift + P** nebo **kliknutím** na položku panelu Stav stavu relace a Výběr "Připojit k sdílet relaci ladění".

![Připojit ladicí program VS Code](../media/vscode-reattach.png)

### <a name="sharing-the-running-application-in-a-browser"></a>Spuštění aplikace v prohlížeči pro sdílení obsahu

Visual Studio Code nemá koncept známý "port webové aplikace" jako v aplikaci Visual Studio pro typy projektů, jako je například technologie ASP.NET. Ale pokud jsou připojení k relaci spolupráce z hostitele sady Visual Studio, může automaticky zobrazí výchozí prohlížeč zobrazí při spuštění, který je pak automaticky připojen k spouštění aplikací hostitele ladění. Zobrazit [funkcemi sady Visual Studio](vs.md#automatic-web-app-sharing) další podrobnosti.

Jako hostitele můžete dosáhnout něco podobného ručně sdílení aplikace nebo jiné koncové body, jako jsou služby RESTful pomocí funkce "Sdílet místní Server". Hosté sady Visual Studio a VS Code můžete otevřít prohlížeč na stejný port místního hostitele zobrazíte běžící aplikaci.  Zobrazit [sdílet server](#share-a-server) další podrobnosti.

## <a name="share-a-server"></a>Sdílení serveru

Čas od času, jako hostitel relace spolupráce může se stát, že chcete sdílet webovou aplikaci nebo jiný místní spuštění s hosté serverů nebo služeb. To může v rozsahu od jiné koncové body RESTful do databáze a dalších serverů. Visual Studio Live Share umožňuje zadat číslo místního portu, volitelně zadat název a pak ho nasdílet všechny hosty.

Hostům pak budou mít přístup k serveru, který jste sdíleli na tomto portu z místního počítače na přesně stejný port. Například, pokud jste sdíleli webový server **běžící na port 3000**, Host dostanete Tento stejný spuštěný webový server na jejich **vlastní počítače** na http://localhost:3000! Toto je nakonfigurovat pomocí bezpečného tunelu SSH nebo SSL mezi hostiteli a hosté a ověření prostřednictvím služby, takže máte jistotu, že pouze ty v relaci spolupráce mají přístup.

> **Tip zabezpečení:** Jako hostitele byste měli pečlivě zvažte, s porty sdílet s hosty a zůstanou aplikace porty (spíše než sdílení portu systému). Pro hosty sdílené porty budou chovat stejně, jako kdyby je sdíleli, pokud byla spuštěna služba server nebo na vlastní počítač. To je velmi užitečný, ale pokud sdílí se Chybný port může být také rizikové.

Z bezpečnostních důvodů jsou k dispozici pro jiné hosty jenom servery se systémem na porty, které zadáte. Je naštěstí snadné přidat jako relaci spolupráce **hostitele**. Tady je způsob:

1. Otevřete na vlastní kartu Live Share v panelu aktivit VS Code nebo v zobrazení Průzkumník Live sdílené složky a vyberte "sdílené složky serveru..." Položka nebo klikněte na ikonu.

    ![VS Code sdílené složky místního serveru](../media/vscode-share-local-server-viewlet.png)<br />

1. Zadejte číslo portu, který na serveru běží na a volitelně název.

    ![Snímek obrazovky okna port číslo řádku](../media/vscode-enter-port.png)<br />

A to je vše! Server na portu, který jste zadali bude nyní namapována na localhost každý hostovaný na stejném portu (Pokud je tento port již byl zaneprázdněn)!

Pokud port, který se už používá v počítači hosta, vybere se automaticky jiný. Naštěstí jako Host zobrazí se seznam aktuálně sdílené portů (podle názvu, je-li zadán) v zobrazení živého Průzkumníka sdílené složky nebo vlastní kartu na panelu aktivit VS Code a najdete v seznamu sdílených serverů. Tento server výběrem položky v prohlížeči otevře. Můžete také klikněte pravým tlačítkem myši a vyberte možnost Kopírovat odkaz do serveru do schránky.

![VS Code přístup místního serveru](../media/vscode-access-shared-server-viewlet.png)<br />

Všimněte si, že *hosté nelze* řídit, které porty na hostitelském počítači sdílejí z bezpečnostních důvodů.

K **Zastavit** sdílení místního serveru jako hostitele, najeďte myší položky serveru v seznamu serverů sdílené v zobrazení Průzkumníka Live sdílené složky nebo vlastní karty a klikněte na ikonu "Zrušení sdílení serveru".

![VS Code stop sdílení serveru](../media/vscode-stop-sharing-server-viewlet.png)<br />

## <a name="share-a-terminal"></a>Sdílení terminálu

Moderní vývojáři často používají celou řadu nástrojů příkazového řádku. Naštěstí Live Share umožňuje uživatelům, jako hostitele, volitelně "sdílely terminálu" hosty. Sdílený terminál může být jen pro čtení nebo plně spolupráci, tak i u hostů můžete spouštět příkazy a analyzovat výsledky. Můžete poskytnout viditelnost hosty do terminálu výstupu nebo mohly získat praktické a spuštění testů, sestavení nebo dokonce třídění specifických pro prostředí problémy, které mohlo dojít pouze v počítači.

Terminály jsou však **není** sdílené ve výchozím nastavení, protože poskytují alespoň přístup jen pro čtení pro hosty do výstupu příkazy spuštění (Pokud není možnost spouštět příkazy samotné). Tímto způsobem můžete volně spouštění příkazů v místní terminály bez rizika a sdílet jenom, když ve skutečnosti je potřeba udělat. Kromě toho můžete spuštění pouze hostitelů sdílené terminály, aby se zabránilo hostů z jednoho spuštění a něco se očekává nebo sledování.

Jako hostitele můžete sdílet terminálu otevřít na vlastní kartu Live Share v panelu aktivit VS Code nebo zobrazení Live sdílet Průzkumníka a vyberte "sdílené složky serveru..." Položka nebo kliknutím na ikonu.

![VS Code sdílené složky terminálu](../media/vscode-share-terminal-viewlet.png)<br />

V tuto chvíli můžete vybrat jen pro čtení nebo pro čtení a zápis terminálu z nabídky. Čtení a zápisu po terminálu everyone zadejte v terminálu, včetně hostitele, což usnadňuje zasáhnout, jestliže Host dělá něco, co nesouhlasíte. Však být bezpečné, měli byste **pouze poskytnout přístup pro čtení a zápisu pro hosty, když víte, které skutečně potřebují** a Zůstaňte u terminálů jen pro čtení pro scénáře, kde chceš jenom hostem a zobrazit výstup všechny příkazy spustíte.

> [!NOTE]
> Pokud se spolupráce relace v režimu jen pro čtení, může být sdílen hostitele terminály jen pro čtení.

![Jen pro čtení nebo pro čtení a zápis výběr](../media/vscode-share-terminal-ro-rw.png)<br />

Po výběru typu sdílený terminál, kterou chcete spustit, zobrazí se nový sdílený terminál terminály na kartě VS Code.

![Sdílené terminálu spuštění](../media/vscode-share-terminal-up.png)<br />

Pokud jsou sdíleny více terminály nebo na jiné kartě je vaším cílem, do konkrétní terminálu můžete přinést fokus tak, že vyberete položku v seznamu sdílených terminály.

![Sdílený terminál umístěte fokus](../media/vscode-shared-terminal-focus.png)<br />

Ukončit relaci Terminálové, jednoduše zadejte ukončení, zavřete okno terminálu, nebo klikněte na ikonu "Zrušení sdílení terminálu" v zobrazení živého Průzkumníka sdílené složky nebo vlastní karty i všem ostatním budou odpojeny.

## <a name="session-states"></a>Stavy relací

Po spuštění nebo připojené k relaci spolupráce a mají přístup k sdílený obsah, Visual Studio Live Share stavového řádku aktualizace položek jejich vzhled tak, aby odrážel stav relace aktivní spolupráci.

Tady jsou stavy, které se obvykle zobrazí:

| Stav | Stavový řádek | Popis |
|-------|--------------------|-------------|
| Neaktivní | ![Stav VS Code: neaktivní](../media/vscode-status-share.png) | Žádné relace aktivní spolupráce, ale nic se sdílí. |
| Hostitel: Sdílení v průběhu | ![VS Code stav: Probíhá sdílet](../media/vscode-status-sharing.png)| Spouští se relace spolupráci a sdílení obsahu se začne za chvíli. |
| Hostitel: Sdílení | ![Stav VS Code: sdílení active ](../media/vscode-status-active.png)| Je aktivní relace spolupráci a sdíleného obsahu. |
| Hostitel: Sdílení jen pro čtení | ![Stav VS Code: sdílení jen pro čtení](../media/vscode-status-sharing-read-only.png)| Sdílení je jen pro čtení spolupráci relace. |
| Host: Připojení k relaci | ![Stav VS Code: připojení](../media/vscode-status-joining.png)| Připojení k existující relaci spolupráci. |
| Host: Připojený | ![Stav VS Code: připojený](../media/vscode-status-active.png) | Připojené a připojené do relace aktivní spolupráci a přijímající sdíleného obsahu. |
| Host: Připojený jen pro čtení | ![Stav VS Code: připojený jen pro čtení](../media/vscode-status-joined-read-only.png) | Připojené a připojení k relaci aktivní spolupráci jen pro čtení. |

## <a name="guest-limitations"></a>Omezení typu Host

Jsou aktuálně nějaké nedostatky, které hosté dojde při použití funkce popsané výše, hostitele relace spolupráci zachovat úplné funkce upřednostňovaném nástroji. Si přečtěte následující informace:

- [Podpora jazyků a platforem](../reference/platform-support.md)
- [Podpora rozšíření](../reference/extensions.md)
- [Hlavní chyby, žádosti o funkce a omezení](https://aka.ms/vsls-issues)
- [Všechny žádosti o funkce a omezení](https://aka.ms/vsls-feature-requests)
- [Odstraňování potíží](../troubleshooting.md)

## <a name="next-steps"></a>Další kroky

Prohlédněte si tyto další články pro další informace.

- [Rychlý start: Sdílejte svůj první projekt](../quickstart/share.md)
- [Rychlý start: Připojte se k první relace](../quickstart/share.md)
- [Postupy: Spolupráce pomocí sady Visual Studio](vs.md)
- [Požadavky na připojení pro Live Share](../reference/connectivity.md)
- [Funkce zabezpečení Live Share](../reference/security.md)
- [Podrobné informace o instalaci systému Linux](../reference/linux.md)

Máte potíže? Podívejte se na článek o [odstraňování potíží](../troubleshooting.md) nebo nám [pošlete svůj názor](../support.md).
