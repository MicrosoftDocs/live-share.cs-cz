---
title: Spolupráce pomocí sady Visual Studio – Visual Studio Live Share | Dokumentace Microsoftu
description: Nastavení spolupráci postupy pro Visual Studio a Live Share.
ms.custom: ''
ms.date: 04/25/2018
ms.reviewer: ''
ms.suite: ''
ms.technology:
- liveshare
ms.topic: conceptual
author: chuxel
ms.author: clantz
manager: AmandaSilver
ms.workload:
- liveshare
ms.openlocfilehash: 995c9e16d24328bb2680deb99cd7e7d421af945c
ms.sourcegitcommit: 4f733c9053848f26da03d47050bcb734f6c98b31
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/02/2019
ms.locfileid: "57254879"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="how-to-collaborate-using-visual-studio"></a>Postupy: Spolupráce pomocí sady Visual Studio

Jste připraveni k získání spolupráce s Live Share v sadě Visual Studio? Pokud ano, jste na správné místo! V tomto článku jsme vás provedeme jak používat některé konkrétní funkce v aplikaci Visual Studio Live Share rozšíření pro sadu Visual Studio.

Všimněte si, že všechny aktivity spolupráce v je zde popsáno, zahrnují jeden **hostitele relace spolupráci** a jeden nebo více **hosté**. Hostitel je osoba, která relaci spolupráce zahájila, a host je každý, kdo se k relaci připojí.

*Hledáte stručné shrnutí? Podívejte se [sdílet](../quickstart/share.md) nebo [spojení](../quickstart/join.md) rychlých startů místo.*

> [!TIP]
> Víte, že se můžete *připojit k vlastní relaci spolupráce*? Díky tomu si můžete Live Share vyzkoušet sami nebo můžete rozjet instanci Visual Studia nebo VS Code a vzdáleně se k ní připojit. U obou instancí můžete dokonce používat stejnou identitu. Vyzkoušejte to!

## <a name="installation"></a>Instalace

Než začnete, budete muset nainstalovat **sady Visual Studio 2017 15.6 nebo vyšší** na Windows 7, 8.1 nebo 10. *Visual Studio 15.7 + se však doporučuje jako umožňuje to podporu místní zpět/znovu.*

Získávání přechodu je jednoduchý:

1. Nainstalujte libovolnou verzi sady [Visual Studio 2017](https://visualstudio.microsoft.com/vs/) 15.6 +.
2. Instalace [podporované úlohy](../reference/platform-support.md). (například ASP.NET, .NET Core, C++ a/nebo Node.js).
3. [Stáhněte si](https://aka.ms/vsls-dl/vs) a nainstalovat rozšíření Visual Studio Live Share z webu marketplace.

Stažením a používáním rozšíření Visual Studio Live Share vyjadřujete souhlas s [licenčními podmínkami](https://aka.ms/vsls-license) a [prohlášením o zásadách ochrany osobních údajů](https://www.microsoft.com/en-us/privacystatement/EnterpriseDev/default.aspx). Pokud narazíte na problémy, podívejte se na článek o [odstraňování potíží](../troubleshooting.md).

[![Stáhnout](../media/download.png)](https://aka.ms/vsls-dl/vs)

## <a name="sign-in"></a>Přihlášení

Abyste mohli spolupracovat, budete potřebovat přihlášení do aplikace Visual Studio Live Share tak všem uživatelům ví, kdo jste. Jedná se čistě v rámci bezpečnostních opatření a nemá **není** přihlašují jakékoli marketing nebo jiných výzkumu. Můžete se přihlásit pomocí osobního účtu Microsoft (třeba @outlook.com), zajišťuje Microsoft pracovní nebo školní účet (AAD) nebo účet GitHub. Přihlášení je snadné.

Ve výchozím nastavení používá Visual Studio vaše [aktivního účtu přizpůsobení](https://docs.microsoft.com/en-us/visualstudio/ide/signing-in-to-visual-studio) , pokud jste už přihlášení do sady Visual Studio, je možné tento krok můžete přeskočit. Jinak se přihlaste běžným způsobem.

![VS přihlašovací tlačítko](../media/vs-sign-in-button.png)

Pokud chcete použít jiný znak než Visual Studio [aktivního účtu přizpůsobení](https://docs.microsoft.com/en-us/visualstudio/ide/signing-in-to-visual-studio), přejděte na stránku **nástroje &gt; možnosti &gt; Live Share &gt; uživatelský účet** pro přepnutí přihlašovací údaje.

![Možnosti nástrojů VS Live sdílené složky](../media/vs-tools-options.png)

Výběr **externího účtu k** vám umožní vybrat účet nepodporuje funkci přizpůsobení sady Visual Studio jako GitHub. Prohlížeč se automaticky zobrazí při prvním použití funkce Live Share tak může provést přihlášení.

Pokud narazíte na problémy, projděte si [řešení potíží s](../troubleshooting.md#sign-in) další tipy.

## <a name="share-a-project"></a>Sdílet projekt

Po stažení a instalaci Visual Studio Live Share, postupujte podle následujících kroků spustit relaci spolupráci a pozvat kolegu pro práci s vámi.

1. **Přihlásit se**

    Po instalaci rozšíření Live Share, budete chtít přihlásit, aby další spolupracovníci vědět, kdo jste. Ve výchozím nastavení používá Visual Studio, je možné tento krok přeskočit zcela vaším účtem přizpůsobení.

    Zobrazit [přihlášení](#sign-in) další podrobnosti.

2. **Otevřete řešení, projektu nebo složky**

    Otevřete složku, projekt nebo řešení, které chcete sdílet s vaší hostů pomocí normálním pracovním postupu.

3. **[Volitelné] Vyloučeno nebo skryté soubory aktualizace**

    Ve výchozím nastavení, Live Share **skryje** všech souborů a složek odkazovat v souborech .gitignore ve vašem projektu z hostů. **Skrytí** soubor zabraňuje zobrazování v stromovou strukturu souborů při **s výjimkou** zastaví z přenosu i během operací, jako je ladění. Pokud chcete skrýt nebo vyloučit jiné soubory, **. vsls.json** soubor lze přidat do projektu s tímto nastavením. Zobrazit [řízení přístupu k souborům a viditelnost](../reference/security.md#controlling-file-access-and-visibility) podrobnosti.

4. **Spustit relaci spolupráce**

    Nyní stačí klikněte na tlačítko "Sdílení" v pravém horním rohu.

    ![Tlačítko sdílet VS](../media/vs-share-button.png)

    > [!NOTE]
    > Můžete být vyzváni softwarem klasické pracovní plochy brány firewall umožňující Live Share agenta pro otevření portu okamžiku, kdy budete sdílet. Přijímá to je naprosto volitelné, ale umožňuje zabezpečené "přímý režim" ke zlepšení výkonu při osoby, že pracujete s je ve stejné síti jako vy. Zobrazit [Změna režimu připojení](../reference/connectivity.md#changing-the-connection-mode) podrobnosti.

    Odkaz na pozvánku bude automaticky zkopíruje do schránky. Při otevření v prohlížeči, tento odkaz umožňuje ostatním uživatelům připojit se k nové relaci spolupráce, který s nimi sdílí obsah těchto složek.

    Zobrazí se také "Sdílení" tlačítko přechodu k předání "Stav relace". Zobrazit [stav relace](#session-states) informace níže v jak to vypadá.

    Všimněte si, že pokud je potřeba získat odkaz na pozvánku znovu poté, co jste začali, sdílení, můžete k němu přístup kliknutím na sdílenou složku / relaci stav tlačítka a vyberte "Kopírovat odkaz".

5. **[Volitelné] Povolení režimu jen pro čtení**

    Po spuštění relace spolupráce, můžete nastavit relace, která má být jen pro čtení pro hosty zabránit v provádění úprav kódu sdílením.

    Po sdílení, zobrazí se oznámení, pozvánky odkaz byl zkopírován do schránky. Pak můžete vybrat možnost nastavit relaci jen pro čtení.

    ![VS režimu jen pro čtení](../media/vs-read-only-notification.png)

6. **Odeslání odkazu**

    Odkaz na odeslání e-mailu, Slack, Skype, atd. a těch, které chcete pozvat. Všimněte si, že udělená úroveň přístupu, Live Share relací může poskytovat hosté, **pouze by měly sdílet s lidmi, kterým důvěřujete** a přemýšlení prostřednictvím důsledky sdílení.

    > **Tip zabezpečení:** Chcete pochopili důsledky zabezpečení některé funkce Live Share? Podívejte se [zabezpečení](../reference/security.md) článku.

    Pokud vás pozvat hosta má otázky, "[rychlý start: Připojte se k relaci první](../quickstart/join.md)"článek poskytuje některé další informace o zprovoznění jako Host.

7. **[Volitelné] Schválit hosta**

    Ve výchozím nastavení hosté se automaticky připojí k relaci spolupráci a budete upozorněni při, jste připravení spolupracovat s vámi. Zatímco tato oznámení obsahují možností jejich odebrání z relace, můžete se také rozhodnout tak, aby místo toho vyžadovala explicitní "schválení" pro každého připojení.

    Jednoduše změňte **nástroje > Možnosti > Live Share > vyžadovat schválení hosta** na hodnotu True pro povolení této funkce. Jakmile budete mít toto nastavení zapnuté, oznámení vás vyzve k předtím, než bylo možné připojit ke schválení hosta.

    ![Žádost o schválení připojení k Visual Studio](../media/vs-join-approval.png)

    V tématu [pozvánky a spojení přístup](../reference/security.md#invitations-and-join-access) najdete další podrobnosti o pozvání aspekty zabezpečení.

To je všechno!

### <a name="ending-the-collaboration-session"></a>Ukončení relace spolupráce

Jako hostitele, můžete ukončit sdílení úplně a ukončení relace spolupráci klikněte na sdílenou složku / relaci stav tlačítka (v pravém horním rohu) a výběrem možnosti "ukončit spolupráci relaci".

![Ukončit sdílení](../media/vs-stop-sharing.png)

Všechny hostů budete informováni, že relace skončila. Jakmile relace skončila, guests nebude mít přístup k obsahu a všechny dočasné soubory se automaticky vyčistí.

Máte problémy s sdílení? Podívejte se na [řešení potíží s](../troubleshooting.md#share-and-join).

## <a name="join-a-collaboration-session"></a>Připojte se k relaci spolupráce

Po stažení a instalaci Visual Studio Live Share, guests stačí provést několik kroků připojit k relaci prostředí pro spolupráci. Existují dva způsoby, jak připojit: [prostřednictvím prohlížeče](#join-via-the-browser) a [ručně](#join-manually).

> **Tip zabezpečení:** V roli hosta připojení k relaci spolupráce je důležité pochopit, že hostitelé může omezit přístup k určité soubory nebo funkce. Chcete si uvědomit důsledky zabezpečení některých funkcích a nastaveních Live Share? Podívejte se [zabezpečení](../reference/security.md) článku.

### <a name="join-via-the-browser"></a>Připojte se k prostřednictvím prohlížeče

Nejjednodušší způsob, jak připojit ke spolupráci relaci je jednoduše otevřete odkaz na pozvánku ve webovém prohlížeči. Zde je, co můžete očekávat Pokud budete postupovat podle tohoto toku.

1. **Přihlásit se**

    Po instalaci rozšíření Live Share, budete chtít přihlásit, aby další spolupracovníci vědět, kdo jste. Ve výchozím nastavení používá Visual Studio, je možné tento krok přeskočit zcela vaším účtem přizpůsobení.

    Zobrazit [přihlášení](#sign-in) další podrobnosti.

2. **Klikněte na odkaz na pozvánku nebo pozvání otevřít v prohlížeči**

    Teď stačí otevřít místní (nebo znovu otevřete) odkaz pozvání v prohlížeči.

    > **Poznámka:**: Pokud jste ještě nenainstalovali rozšíření Live Share, zobrazí se vám s odkazy na marketplace pro rozšíření. Instalace rozšíření a restartujte nástroj a zkuste to znovu.

    Zobrazí se oznámení, spustí se nástroj Live Share povolené vyžaduje prohlížeče. Pokud jste povolili jeho spuštění vybrané nástroje, už budete připojíte k relaci spolupráce po jeho spuštění.

    ![Připojte se k stránky](../media/join-page.png)

    Pokud je hostitel v režimu offline, zobrazí se upozornění v tuto chvíli místo. Potom můžete kontaktovat hostitele a požádejte ho, aby znovu sdílet.

    > [!NOTE]
    > Stále se nedaří? Zobrazit [ručně připojit](#join-manually).

3. **Spolupráce**

    To je všechno! Za malou chvíli bude připojen a můžete začít spolupracovat.

    Zobrazí se tlačítko "Sdílení" přechod k předání "Stav relace". Zobrazit [stav relace](#session-states) následující informace pro jak to vypadá.

    Potom automaticky přejdete do souboru hostitele je právě se upravuje po dokončení připojení.

### <a name="join-manually"></a>Připojte se k ručně

Můžete také ručně připojit bez použití webového prohlížeče, které mohou být užitečné v situacích, kdy už běží nástroj, který chcete použít, chcete použít jiný nástroj, než lze obvykle provést, nebo pokud máte potíže s získávání pozvat odkazy na pracovní z nějakého důvodu. Postup je jednoduchý:

1. **Přihlásit se**

    Po instalaci rozšíření Live Share, budete chtít přihlásit, aby další spolupracovníci vědět, kdo jste. Ve výchozím nastavení používá Visual Studio, je možné tento krok přeskočit zcela vaším účtem přizpůsobení.

    Zobrazit [přihlášení](#sign-in) další podrobnosti.

2. **Použití příkazu join**

    Jednoduše přejděte na **soubor > připojte se k relaci spolupráce**

    ![Připojení k nabídce VS](../media/vs-join.png)

3. **Vložte odkaz pozvánky**

    Vložte adresu URL pozvánky byly odeslány a potvrďte.

4. **Spolupracujte!**

    A to je vše! Musí být připojené k okamžité relaci spolupráce.

    Zobrazí se tlačítko "Sdílení" přechod k předání "Stav relace". Zobrazit [stav relace](#session-states) následující informace pro jak to vypadá.

    Potom automaticky přejdete do kde hostitele je právě se upravuje po dokončení připojení.

### <a name="leave-the-collaboration-session"></a>Nechte relaci spolupráce

V roli hosta, můžete nechat relaci spolupráce bez ukončení pro ostatní uživatele, jednoduše ukončením nástroj nebo klikněte na sdílenou složku / relaci stav tlačítka a vyberte "Opustit spolupráci relaci".

![Připojení k nabídce VS](../media/vs-leave-session.png)

Všechny dočasné soubory se automaticky vyčistí proto není potřeba žádná další akce.

Potíže s připojení? Podívejte se na [řešení potíží s](../troubleshooting.md#share-and-join).

## <a name="co-editing"></a>Společné úpravy

Po Host připojena ke spolupráci relace, všechny spolupracovníci okamžitě bude moci zobrazit každý další úpravy a požadované změny v reálném čase. Všechno, co je třeba provést je v Průzkumníku souborů vyberte soubor a můžete začít upravovat. Hostitelích a hostech uvidí úpravy daly a sami díky tomu je snadné iterovat a rychle nail nižší řešení můžete přispívat.

> [!NOTE]
> Připojení k relaci spolupráci jen pro čtení zabrání hosté nebudou moct provádět úpravy souborů. Hostitel může [povolení režimu jen pro čtení při sdílení](#share-a-project). V roli hosta, poznáte, pokud jste se připojili relaci jen pro čtení zobrazením vašich [stav relace](#session-states).

![Snímek obrazovky znázorňující společně úpravy](../media/vs-coedit.png)

> [!NOTE]
> Společné úpravy má několik omezení pro některé jazyky. Stav funkcí podle jazyků najdete v článku [o podpoře platforem](../reference/platform-support.md).

Kromě kurzory a úpravy jsou také vámi provedených výběrů viditelné pro všechny účastníky, kterými tento stejný soubor. To usnadňuje zvýrazněte kde problémy mohou existovat zprostředkovat nápady.

![Snímek obrazovky znázorňující zvýraznění](../media/vs-highlight.png)

Ještě lepší je a ostatní účastníky můžete přejít na všechny soubory ve sdíleném projektu. Buď můžete upravit společně nebo samostatně to znamená, že můžete bez problémů přepínat mezi šetření, vytváření, malá vylepšení a úplné společné úpravy.

> [!NOTE]
> Ve výchozím nastavení sdílené složky za sdílené složky otevřené soubory externí sdílené řešení. Pokud chcete tuto funkci zakázat, aktualizujte externí sdílení souborů v nástrojích &gt; možnosti &gt; Live Share na hodnotu False.

Výsledný úpravy jsou trvalé na počítači hostitele na Uložit tady není nutné synchronizovat, vkládání nebo odesílání souborů, až budete hotovi úprav. Úpravy existují "právě."

> **Tip zabezpečení:** Zadaný všichni účastníci můžou nezávisle na sobě přejděte a úpravy souborů, jako hostitele, můžete chtít omezit, které soubory Hosté mají přístup k ve vašem projektu prostřednictvím. vsls.json souboru. V roli hosta je také důležité si uvědomit, že se že nezobrazí určité soubory výsledkem tohoto nastavení. Zobrazit [řízení přístupu k souborům a viditelnost](../reference/security.md#controlling-file-access-and-visibility) podrobnosti.

### <a name="changing-participant-flag-behaviors"></a>Změna chování účastníka příznak

Ve výchozím nastavení Visual Studio Live Share automaticky zobrazí "flag" vedle účastníka kurzoru při najetí myší, nebo při úpravách, zvýrazněte nebo přesunutí jejich kurzoru. V některých případech můžete chtít toto chování změnit. Postup:

1. Přejděte na **nástroje > Možnosti > Live sdílené složky**
2. Změnit **příznak viditelnosti** možnost na jednu z následujících akcí:

| Možnost | Chování |
|--------|----------|
| OnHoverOnly | Příznak se zobrazí, pouze když najedete myší kurzor. |
| OnHoverOrActivity | Toto nastavení je výchozí. Příznak je viditelné při najetí myší nebo pokud účastník upraví, zvýrazní nebo přesune kurzor. |
| Vždy | Příznak je vždy viditelné.

## <a name="following"></a>Následující

Pokaždé, když jste v relaci spolupráce, budete mít možnost vidět každý účastník iniciály v pravém horním rohu editoru vedle tlačítko pro přihlášení. Iniciály ukazatel myši zobrazí úplné informace účastníka.

![Snímek obrazovky zobrazující uživatele](../media/vs-person.png)

V některých případech budete muset vysvětlení problému nebo návrhu, která zahrnuje více souborů nebo umístění v kódu. V těchto situacích může užitečné dočasně použít kolegu při přechodu během celého projektu. Z tohoto důvodu jako hosta, když se připojí k relaci spolupráce automaticky "postupujte podle" hostitele. Podle účastníka, editor bude zůstávat synchronizovaný s jejich aktuálně otevřený soubor kurzoru a pozici posunutí.

> [!NOTE]
> Ve výchozím nastavení sdílené složky za sdílené složky otevřené soubory externí sdílené řešení. Pokud chcete tuto funkci zakázat, aktualizujte externí sdílení souborů v nástrojích &gt; možnosti &gt; Live Share na hodnotu False.

Abyste usnadnili snadnou přepínání z "podle režimu" a můžete začít upravovat sami, budete přestat, sledovat případě kterýkoli z následujících:

1. Upravit, přesuňte ukazatel myši nebo provést výběr
2. Vyberte jiný soubor

Můžete také zastavit podle kdykoli kliknutím iniciály osoby, kterou sledujete v pravém horním rohu. Kruh Iniciály účastníka, který označuje, že sledujete jejich pak zmizí.

![Visual Studio účastníka splňovalo](../media/vs-pinned.png) ![Visual Studio účastníka naprostou postupovali podle](../media/vs-pin-hover.png)

Můžete kliknout na jakékoli iniciály ve stejném umístění dodržovat všechny hostitele nebo hosta v relaci spolupráce. Poznámka: Pokud chcete přejít na jiného uživatele umístění spíše než po, jednoduše klikněte dvakrát na jejich značky.

## <a name="focusing"></a>Zaměření

Občas můžete chtít všem uživatelům v relaci spolupráce se sem a podívejte se na něco, co děláte. Živé sdílené složky můžete pokládat, že všichni "zaměřit" jejich pozornost na vás s oznámením, která umožňuje jednoduše sledovat zpět.

Právě klikněte na stav relace / sdílet tlačítko v pravém horním rohu a vyberte "Fokus účastníky".

![Možnost nabídky fokus](../media/vs-focus.png)

Všichni uživatelé v relaci spolupráce se pak dostanete oznámení, kterou jste požadovali jejich pozornost

![Oznámení s informační zprávou fokus](../media/vs-focus-toast.png)

Jsou pak stačí kliknout na "Sledovat" přímo z oznámení až budou připravené na jejich zaměřit na vás.

## <a name="co-debugging"></a>Společné ladění

Visual Studio Live Share na spolupráci funkce ladění je jedinečný a efektivní způsob, jak ladit problém. Kromě povolení prostředí pro spolupráci na řešení problémů, také můžete a ostatní účastníci relace, které umožňuje prozkoumat problémy, které může být konkrétní prostředí tím, že na počítači hostiteli poskytuje sdílené relace ladění.

> **Tip zabezpečení:** Zadaný všichni účastníci můžou nezávisle na sobě přejděte a úpravy souborů, jako hostitele, můžete chtít omezit, které soubory Hosté mají přístup k ve vašem projektu prostřednictvím. vsls.json souboru. Jste měli také něco vědět, že přístup konzoly/REPL znamená, že účastníci spouštět náležité příkazy na svém počítači, by měla pouze společně ladění s těmi, které důvěřujete. V roli hosta je také důležité si uvědomit, že nebudete moci postupujte podle ladicí program, jak ho můžete krokovat s vnořením určité soubory s omezeným přístupem soubory výsledkem tohoto nastavení. Zobrazit [řízení přístupu k souborům a viditelnost](../reference/security.md#controlling-file-access-and-visibility) podrobnosti.

Použití je jednoduché. Hostitel relace spolupráci jednoduše spustit ladění přes obvykle znamená, že v sadě Visual Studio.

![Tlačítko ladění VS](../media/vs-debug-button.png)

Když ladicí program připojí na straně hostitele, všechny hosté také automaticky připojí také. Při jedné "relace ladění" na počítači hostitele všichni účastníci jsou připojené k němu a má své vlastní zobrazení.

> [!TIP]
> Pokud chcete změnit, kdy a jak společně ladění se stane, můžete změnit výchozí chování v pomocí nastavení **nástroje > Možnosti > Live Share**.

![Připojit ladicí program VS](../media/vs-debugger.png)

Všem uživatelům procházení ladění procesu, které umožňuje bezproblémové přepínání mezi spolupracovníci, aniž byste museli vyjednávání ovládacího prvku.

> [!NOTE]
> Stav funkcí ladění podle jazyků a platforem najdete v článku [o podpoře platforem](../reference/platform-support.md).

Každého spolupracovníka můžete prozkoumat různé proměnné, přejít na různé soubory v zásobníku volání, kontrolovat proměnné a dokonce i přidat nebo odebrat zarážky. Společné úpravy funkce pak umožňují každý účastníka krásně sledovat, kde jsou ostatní umístěné, poskytují jedinečné možnost bez problémů přepínání mezi současně zkoumání různých aspektů problém a společně ladění.

> [!NOTE]
> V relaci spolupráci jen pro čtení, nebude možné pro jednotlivé kroky v procesu ladění hosta. Mohou však stále přidat nebo odebrat zarážky a kontrolovat proměnné.

> [!TIP]
> Také se můžete zúčastnit ve VS Code ladicími relacemi ze sady Visual Studio a naopak. Podívejte se [sady Visual Studio pokyny](vscode.md#co-debugging) společně ladění pro další informace.

### <a name="automatic-web-app-sharing"></a>Sdílení automatické webové aplikace

Ještě lepší u projektů webové aplikace ASP.NET ve výchozím nastavení pokud hostitele projekt je nakonfigurován na automatické spuštění webového prohlížeče pro připojení k běžící aplikaci web při ladění, Live Share automaticky provede stejné na každý hostovaný počítač! To se provádí v bezpečný a vzdálené webové aplikace je k dispozici pro hosty jenom během relace ladění ve výchozím nastavení.

Zobrazit [sdílet server](#share-a-server) informace o tom, jak sdílet přístup k serveru pro ostatní typy projektů a/nebo po dobu trvání relace.

> [!TIP]
> Pokud nemáte, jako jsou automatizované prohlížeče chování pro sdílení obsahu a chcete ho změnit, můžete aktualizovat nastavení v **nástroje > Možnosti > Live Share**.

![Animace souběžných ladění](../media/co-debug.gif)

### <a name="change-when-visual-studio-joins-debugging-sessions"></a>Změnit při ladění relace spojení sady Visual Studio

Ve výchozím nastavení jako Host, které budete automaticky připojí k ladicími relacemi, když se sdílí hostitele. Nicméně v některých případech může být pro vás toto chování rušivě. Naštěstí můžete změnit ho následujícím způsobem:

1. Přejděte na **nástroje > Možnosti > Live sdílené složky**
2. Změnit **možnost ladicí relace spojení** na jednu z následujících akcí:

| Možnost | Chování |
|--------|----------|
| Automatické | Výchozí nastavení V roli hosta budete automaticky připojí k sdílené ladicí relace, které spuštění hostitele. |
| Zobrazení výzvy | V roli hosta zobrazí se výzva, jestli chcete připojit ke sdílené ladicí relaci při spuštění hostitele. |
| Ruční | V roli hosta budete muset ručně připojit ladicí relace. Zobrazit [odpojení a opětovné](#detaching-and-reattaching).|

### <a name="detaching-and-reattaching"></a>Odpojení a opětovné

V roli hosta můžete chtít Zastavit ladění dočasně. Naštěstí můžete stačí kliknout na ikonu "stop" v panelu nástrojů ladění můžete odpojit ladicí program, aniž by to ovlivnilo jiné hosty nebo hostitele.

Pokud nastavení jste aktualizovali tak, že jste už automatické připojení, nebo pokud chcete jednoduše znovu připojit později, můžete jednoduše vybrat požadovanou spuštěná ladicí relace, od "vybrat spouštěcí položku..." Rozevírací nabídka...

![Tlačítko ladění VS](../media/vs-select-reattach.png)

... a pak klikněte na připojit.

![Tlačítko ladění VS](../media/vs-reattach.png)

## <a name="share-a-server"></a>Sdílení serveru

Z času na čas jako hostitel relace spolupráce může se stát, že chcete sdílet další místní servery nebo služby s hosté. To může v rozsahu od jiné koncové body RESTful do databáze nebo jiné servery. Visual Studio Live Share umožňuje zadat číslo místního portu, volitelně zadat název a pak ho nasdílet všechny hosty.

Hostům pak budou mít přístup k serveru, který jste sdíleli na tomto portu z místního počítače na přesně stejný port. Například, pokud jste sdíleli webový server **běžící na port 3000**, Host dostanete Tento stejný spuštěný webový server na jejich **vlastní počítače** na http://localhost:3000! Toto je nakonfigurovat pomocí bezpečného tunelu SSH nebo SSL mezi hostiteli a hosté a ověření prostřednictvím služby, takže máte jistotu, že pouze ty v relaci spolupráce mají přístup.

> **Tip zabezpečení:** Jako hostitele byste měli pečlivě zvažte, s porty sdílet s hosty a zůstanou aplikace porty (spíše než sdílení portu systému). Pro hosty sdílené porty budou chovat stejně, jako kdyby je sdíleli, pokud byla spuštěna služba server nebo na vlastní počítač. To je velmi užitečný, ale pokud sdílí se Chybný port může být také rizikové.

Z bezpečnostních důvodů jsou k dispozici pro jiné hosty jenom servery se systémem na porty, které zadáte. Naštěstí se dají snadno přidat jako relaci spolupráce **hostitele**. Tady je způsob:

1. Klikněte na sdílenou složku / stav relace tlačítko v pravém horním rohu a vyberte "Spravovat sdílené místní servery"

    ![Spravovat sdílené místní servery](../media/vs-share-local-servers.png)

2. V zobrazeném dialogovém okně klikněte na tlačítko "Přidat" a zadejte číslo portu na serveru běží na místním počítači, zadejte název, stiskněte klávesu enter, pak OK.

    ![Spravovat sdílené místní servery](../media/vs-manage-local-shared-servers.png)

A to je vše! Server na portu, který jste zadali bude nyní namapována na localhost každý hostovaný na stejném portu (Pokud je tento port již byl zaneprázdněn)!

Pokud port je již používána na hostovaný počítač, vybere se automaticky jiný. Naštěstí hosta můžete zobrazit seznam aktuálně sdílené porty (podle názvu, je-li zadán) klikněte na sdílenou složku / stav relace tlačítko v pravém horním rohu a výběrem možnosti "zobrazení Shared místních serverů."

![Viw sdílené místní servery](../media/vs-view-shared-servers.png)

Všimněte si, že *hosté nelze* řídit, které porty na hostitelském počítači sdílejí z bezpečnostních důvodů.

K **Zastavit** místního serveru pro sdílení obsahu, hostitele jednoduše klikněte na sdílenou složku / stav relace tlačítko v horním pravém rohu jako výše, vyberte možnost "Spravovat sdílené místní servery", vyberte příslušný port a klikněte na tlačítko "Odebrat".

## <a name="share-a-terminal"></a>Sdílet terminálu

Moderní vývojáři často používají celou řadu nástrojů příkazového řádku. Naštěstí Live Share umožňuje uživatelům, jako hostitele, volitelně "sdílely terminálu" hosty. Sdílený terminál může být jen pro čtení nebo plně spolupráci, tak i u hostů můžete spouštět příkazy a analyzovat výsledky. Můžete poskytnout viditelnost hosty do terminálu výstupu nebo mohly vyzkoušejte v praxi a spouštění testů, sestavení nebo prostředí i třídění konkrétní se problémy, které mohlo dojít pouze v počítači.

Terminály jsou však **není** sdílené ve výchozím nastavení, protože poskytují alespoň přístup jen pro čtení pro hosty do výstupu příkazy spuštění (Pokud není možnost spouštět příkazy samotné). Tímto způsobem můžete volně spouštění příkazů v místní terminály bez rizika a sdílet jenom, když ve skutečnosti je potřeba udělat. Kromě toho můžete spuštění pouze hostitelů sdílené terminály, aby se zabránilo hostů z jednoho spuštění a něco se očekává nebo sledování.

Jako hostitele můžete sdílet terminálu tak, že kliknete na stav relace nebo sdílet tlačítko v pravém horním rohu a vyberete jednu z položek nabídky "Sdílení terminálu".

![Nabídka Terminál](../media/vs-terminal-menu.png)

V tuto chvíli můžete vybrat jen pro čtení nebo pro čtení a zápis terminálu z nabídky. Čtení a zápisu po terminálu everyone zadejte v terminálu, včetně hostitele, což usnadňuje zasáhnout, jestliže Host dělá něco, co nesouhlasíte. Však být bezpečné, měli byste **pouze poskytnout přístup pro čtení a zápisu pro hosty, když víte, které skutečně potřebují** a Zůstaňte u terminálů jen pro čtení pro scénáře, kde chceš jenom hostem a zobrazit výstup všechny příkazy spustíte.

> [!NOTE]
> Pokud se spolupráce relace v režimu jen pro čtení, může být sdílen hostitele terminály jen pro čtení.

Jakmile vyberete typ sdílený terminál, kterou chcete spustit, zobrazí se nový sdílený terminál pro všechny účastníky se správnými oprávněními. Když Visual Studio Code je terminálu podporuje integrované sady Visual Studio nemá mimo pole. Ve výchozím nastavení, proto se zobrazí nové okno obsahující terminálu. Nicméně pokud [která která terminálu rozšíření](https://marketplace.visualstudio.com/items?itemName=DanielGriffen.WhackWhackTerminal), Live Share se místo toho vytvořit integrovaný terminál. Visual Studio vám poskytne odkazu na její instalaci při prvním spuštění nebo připojení sdílený terminál.

![Oznámení s informační zprávou terminálu instalace](../media/vs-terminal-install.png)

Ukončení Terminálové relaci, stačí zadat ukončit nebo zavřít okno terminálu a všichni budou odpojeny.

## <a name="session-states"></a>Stavy relací

Po spuštění nebo připojené k relaci spolupráce a sdíleli přístup k obsahu, aktualizuje "Sdílení" tlačítko v pravém horním rohu jeho vzhled tak, aby odrážel stav relace aktivní spolupráci.

Tady jsou stavy, které se obvykle zobrazí:

| Stav | Tlačítko | Popis |
|-------|--------|-------------|
| Neaktivní | ![Stav VS: neaktivní](../media/vs-status-share.png) | Žádné relace aktivní spolupráce, ale nic se sdílí. |
| Hostitel: Sdílení v průběhu | ![Vs – stav: Probíhá sdílet](../media/vs-status-sharing.png) | Spouští se relace spolupráci a sdílení obsahu se začne za chvíli. |
| Hostitel: Sdílení | ![Stav VS: sdílení active ](../media/vs-status-active.png) | Je aktivní relace spolupráci a sdíleného obsahu. |
| Hostitel: Sdílení jen pro čtení | ![Stav VS: sdílení jen pro čtení](../media/vs-status-sharing-read-only.png)| Sdílení je jen pro čtení spolupráci relace. |
| Host: Připojení k relaci | ![Stav VS Code: připojení](../media/vs-status-joining.png) | Připojení k existující relaci spolupráci. |
| Host: Připojený | ![Stav VS: připojený](../media/vs-status-joined.png) | Připojené a připojené do relace aktivní spolupráci a přijímající sdíleného obsahu. |
| Host: Připojený jen pro čtení | ![Stav VS: připojený jen pro čtení](../media/vs-status-joined-read-only.png) | Připojené a připojení k relaci aktivní spolupráci jen pro čtení. |

## <a name="guest-limitations"></a>Omezení typu Host

Jsou aktuálně nějaké nedostatky, které hosté dojde při použití funkce popsané výše, hostitele relace spolupráci zachovat úplné funkce upřednostňovaném nástroji. Si přečtěte následující informace:

- [Podpora jazyků a platforem](../reference/platform-support.md)
- [Podpora rozšíření](../reference/extensions.md)
- [Hlavní chyby, žádosti o funkce a omezení](https://aka.ms/vsls-issues)
- [Všechny žádosti o funkce a omezení](https://aka.ms/vsls-feature-requests)

## <a name="next-steps"></a>Další kroky

Prohlédněte si tyto další články pro další informace.

- [Rychlý start: Sdílejte svůj první projekt](../quickstart/share.md)
- [Rychlý start: Připojte se k první relace](../quickstart/join.md)
- [Postupy: Spolupráce pomocí Visual Studio Code](vscode.md)
- [Požadavky na připojení pro Live Share](../reference/connectivity.md)
- [Funkce zabezpečení Live Share](../reference/security.md)

Máte potíže? Podívejte se na článek o [odstraňování potíží](../troubleshooting.md) nebo nám [pošlete svůj názor](../support.md).
