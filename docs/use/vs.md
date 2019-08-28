---
title: Spolupráce s využitím sady Visual Studio – Visual Studio Live Share | Microsoft Docs
description: Sada postupů spolupráce pro Visual Studio a Live Share.
ms.custom: ''
ms.date: 04/25/2018
ms.reviewer: ''
ms.suite: ''
ms.topic: conceptual
author: chuxel
ms.author: clantz
manager: AmandaSilver
ms.workload:
- liveshare
ms.openlocfilehash: 65c48d1a95cc94bc7505c185be353e437e3c5ba1
ms.sourcegitcommit: 6b46e300d76eda661ab34c67a3b909d5c162cd9a
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/28/2019
ms.locfileid: "70062299"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="how-to-collaborate-using-visual-studio"></a>Postupy: Spolupráce v sadě Visual Studio

Jste připraveni začít spolupracovat s Live Share v aplikaci Visual Studio? Pokud ano, jste na správném místě! V tomto článku Vás provedeme postupem, jak používat některé z konkrétních funkcí v rozšíření Visual Studio Live Share pro Visual Studio.

Všimněte si, že všechny aktivity spolupráce popsané tady zahrnují jednoho **hostitele relace pro spolupráci** a jednoho nebo více **hostů**. Hostitel je osoba, která relaci spolupráce zahájila, a host je každý, kdo se k relaci připojí.

*Hledáte zkrácený souhrn? Místo toho se podívejte do [složky](../quickstart/share.md) rychlé starty nebo se připojovat. [](../quickstart/join.md)*

> [!TIP]
> Víte, že se můžete *připojit k vlastní relaci spolupráce*? Díky tomu si můžete Live Share vyzkoušet sami nebo můžete rozjet instanci Visual Studia nebo VS Code a vzdáleně se k ní připojit. U obou instancí můžete dokonce používat stejnou identitu. Vyzkoušejte to!

## <a name="installation"></a>Instalace

Než začnete, budete muset nainstalovat **Visual studio 2019** nebo **visual Studio 2017 15,6 nebo vyšší** ve Windows 7, 8,1 nebo 10. *Ale Visual Studio 15.7 + se doporučuje, protože umožňuje místní podporu akcí zpět a znovu.*

Je jednoduché, abyste mohli začít.

For Visual Studio 2019
1. Nainstalujte všechny edice sady [Visual Studio 2019](https://visualstudio.microsoft.com/vs/).
2. Nainstalujte [podporované sady funkcí](../reference/platform-support.md). (například ASP.NET, .NET Core, C++, Python a/nebo Node.js).
3. Visual Studio Live Share se standardně instaluje s těmito sadami funkcí.

For Visual Studio 2017
1. Nainstalujte všechny edice sady [Visual Studio 2017](https://visualstudio.microsoft.com/vs/older-downloads/) 15.6 +.
2. Nainstalujte [podporované sady funkcí](../reference/platform-support.md). (například ASP.NET, .NET Core, C++ a/nebo Node.js).
3. [Stáhněte](https://aka.ms/vsls-dl/vs) a nainstalujte Visual Studio Live Share rozšíření z webu Marketplace.

Stažením a používáním rozšíření Visual Studio Live Share vyjadřujete souhlas s [licenčními podmínkami](https://aka.ms/vsls-license) a [prohlášením o zásadách ochrany osobních údajů](https://www.microsoft.com/en-us/privacystatement/EnterpriseDev/default.aspx). Pokud narazíte na problémy, podívejte se na článek o [odstraňování potíží](../troubleshooting.md).

[![Stáhnout](../media/download.png)](https://aka.ms/vsls-dl/vs)

## <a name="sign-in"></a>Přihlášení

Aby bylo možné spolupracovat, budete se muset Visual Studio Live Share přihlásit, aby všichni znali, kdo máte. Toto je čistě bezpečnostní opatření a neumožňuje vás při jakémkoli marketingovém nebo jiných výzkumných aktivitách. Můžete se přihlásit pomocí osobního účtu Microsoft (např. @outlook.com), pracovního nebo školního účtu (AAD) založeného na Microsoftu nebo účtu GitHub. Přihlašování je snadné.

Ve výchozím nastavení používá Visual Studio váš [účet přizpůsobení](https://docs.microsoft.com/en-us/visualstudio/ide/signing-in-to-visual-studio) , takže pokud už jste přihlášeni k aplikaci Visual Studio, může být možné tento krok přeskočit. Jinak se podepište jako normálně.

![Tlačítko pro přihlášení VS](../media/vs-sign-in-button.png)


Pokud chcete použít jiné přihlášení, než je váš [účet přizpůsobení](https://docs.microsoft.com/en-us/visualstudio/ide/signing-in-to-visual-studio)sady Visual Studio, přejděte do **možností nástroje &gt; možnosti &gt; &gt; Live Share uživatelský účet** pro přepnutí přihlašovacích údajů.

![Možnosti nástrojů VS Live Share](../media/vs-tools-options-new.png)

Výběr **externího účtu** umožňuje vybrat účet, který není podporován funkcí přizpůsobení sady Visual Studio, jako je GitHub. Prohlížeč se automaticky zobrazí při prvním použití funkce Live Share, abyste mohli dokončit přihlášení.
>[!Tip]
>Věděli jste, že pro zobrazení všech výchozích nastavení Live Share můžete přejít na **možnosti &gt; &gt; nástroje Live Share &gt; obecné** ? Přizpůsobte si prostředí pro spolupráci podle svých potřeb. Můžete také vyzkoušet všechny nové funkce Live Share tím, že v obecném nastavení Live Share vyberete  **&gt; rozšířené funkce &gt; Insider** .  

Pokud narazíte na problémy, podívejte se na [řešení potíží](../troubleshooting.md#sign-in) , kde najdete další tipy.

## <a name="share-a-project"></a>Sdílení projektu

Po stažení a instalaci Visual Studio Live Share postupujte podle těchto kroků a zahajte relaci spolupráce a pozvěte kolegu, aby s vámi spolupracovali.

1. **Přihlásit se**

    Teď, když jste přihlášeni, jste připraveni začít svoji vlastní relaci spolupráce.
    Nejste přihlášení? Další podrobnosti najdete [v přihlašování](#sign-in) .

2. **Otevření řešení, projektu nebo složky**

    Použijte běžný pracovní postup k otevření složky, projektu nebo řešení, které chcete sdílet s hosty.

3. **Volitelné Aktualizace skrytých nebo vyloučených souborů**

    Ve výchozím nastavení Live Share **skrývá** všechny soubory nebo složky, na které se odkazuje v souborech. gitignore v projektu od hostů. **Skrytím** souboru zabráníte jeho zobrazení ve stromu souborů a zároveň se tím vyloučí, že se přestane přenášet i během operací, jako je ladění. Pokud chcete skrýt nebo vyloučit různé soubory, můžete do projektu pomocí těchto nastavení přidat soubor **. vsls. JSON** . Podrobnosti najdete v tématu [řízení přístupu k souborům a viditelnost](../reference/security.md#controlling-file-access-and-visibility) .

4. **Spustit relaci spolupráce**

    Nyní kliknutím na tlačítko Live Share v pravém horním rohu spustíte relaci Live Share.     Odkaz na sdílení relace pro spolupráci se automaticky zkopíruje do schránky. 

    ![Tlačítko pro sdílení VS](../media/vs-share-button.png)

    Po prvním spuštění relace spolupráce se zobrazí okno Live Share nástrojů. Ujistěte se, že jste toto okno nastavili, abyste se ujistili, že se zobrazí při příštím spuštění relace Live Share.

   ![Okno nástroje VS Live Share](../media/vs-live-share-tool-window.png)

    > [!NOTE]
    > Možná budete požádáni o váš software brány firewall na ploše, aby mohl agent Live Share otevřít port při prvním sdílení. Přijetí je zcela volitelné, ale umožňuje zabezpečený "přímý režim", aby se zlepšil výkon, když osoba, se kterou pracujete, je ve stejné síti jako vy. Podrobnosti najdete v tématu [Změna režimu připojení](../reference/connectivity.md#changing-the-connection-mode) .

5. **Volitelné Povolit režim jen pro čtení**

    Po zahájení relace spolupráce můžete nastavit relaci jen pro čtení a zabránit tak hostům v provádění úprav v kódu, který se sdílí.

    Po sdílení se dostanete oznámení, že se odkaz na pozvánku zkopíroval do schránky. Pak můžete vybrat možnost nastavit relaci jen pro čtení.

    ![Režim jen pro čtení VS](../media/vs-read-only-notification.png)

6. **Poslat někomu odkaz**

    Pošlete odkaz prostřednictvím e-mailu, časové rezervy, Skypu atd. na ty, které chcete pozvat. Všimněte si, že vzhledem k tomu, že úroveň přístupu Live Share relace může poskytnout hostům, **byste měli sdílet jenom s lidmi, kterým důvěřujete** , a zamyslete se nad důsledky sdílení.

    > **Tip zabezpečení:** Chcete pochopit důsledky zabezpečení některých funkcí Live Share? Podívejte se na článek o [zabezpečení](../reference/security.md) .

    Pokud má host, který jste pozvali, dotazy[, "rychlý Start: Připojte se k první](../quickstart/join.md)relaci. v článku najdete další informace o tom, jak začít pracovat jako host.

7. **Volitelné Schválit hosta**

    Ve výchozím nastavení se hostům automaticky připojí k vaší relaci spolupráce a budete upozorněni, až budou připraveni s vámi pracovat. I když vám toto oznámení umožní odebrat je z relace, můžete také místo toho vyžadovat explicitní schválení pro kohokoli, co se připojuje.

    Jednoduše změňte **nástroje > možnosti > Live Share >** pro povolení této funkce vyžadovat schválení hostů na hodnotu true. Jakmile je toto nastavení zapnuté, zobrazí se výzva k potvrzení, že hosta se bude moci připojit.

    ![Žádost o schválení připojení sady Visual Studio](../media/vs-join-approval.png)

    Další podrobnosti o požadavcích na zabezpečení pozvánky najdete v tématu [pozvánky a přístup k nim](../reference/security.md#invitations-and-join-access) .

8. **Správa relace Live Share**
    
    Jakmile Host otevře odkaz na vaši sdílenou relaci v VS Code nebo v aplikaci Visual Studio, zobrazí se jim v seznamu Účastníci v okně nástroje Live Share. Teď si můžete zobrazit, který soubor hosta je v současné době vedle svého jména.  
    
    ![Okno nástroje VS Live Share](../media/vs-live-share-tool-window-participant.png)

    Okno nástroje Live Share umožňuje přístup ke všem klíčovým funkcím pro správu relace na jednom místě. 

    > [!TIP]
    > V průběhu vašich relací už nevidíte okno Live Share Tool? Vždycky můžete přejít k **zobrazení &gt; dalších Live Share Windows &gt;**  a najít

### <a name="ending-the-collaboration-session"></a>Ukončení relace spolupráce

Jako hostitel můžete ukončit sdílení úplně a ukončit relaci spolupráce kliknutím na tlačítko sdílet/vytvořit stav relace (v pravém horním rohu) a výběrem možnosti ukončit relaci spolupráce.

![Ukončit sdílení](../media/vs-stop-sharing.png)

Všichni hosté budou upozorněni, že relace skončila. Po ukončení relace nebudou mít hosté přístup k obsahu a žádné dočasné soubory se automaticky vyčistí.

Máte problémy se sdílením? Podívejte se na [řešení potíží](../troubleshooting.md#share-and-join).

## <a name="join-a-collaboration-session"></a>Připojit se k relaci spolupráce

Po stažení a instalaci Visual Studio Live Share musí hosty provést několik kroků, než se připojí k hostované relaci spolupráce. Existují dva způsoby, jak se připojit: [přes prohlížeč](#join-via-the-browser) a [ručně](#join-manually).

> **Tip zabezpečení:** Jako host se připojuje k relaci spolupráce, je důležité pochopit, že hostitelé můžou omezovat přístup k určitým souborům nebo funkcím. Chcete pochopit důsledky zabezpečení některých funkcí a nastavení Live Share? Podívejte se na článek o [zabezpečení](../reference/security.md) .

### <a name="join-via-the-browser"></a>Připojení přes prohlížeč

Nejjednodušší způsob, jak se připojit k relaci spolupráce, je jednoduše otevřít odkaz pro pozvání ve webovém prohlížeči. Můžete očekávat, že budete postupovat podle tohoto toku.

1. **Přihlásit se**

    Po instalaci rozšíření Live Share se budete chtít přihlásit, aby mohli jiní spolupracovníky informovat o tom, kdo máte. Ve výchozím nastavení používá Visual Studio účet pro přizpůsobení, takže tento krok bude možné úplně přeskočit.

    Další podrobnosti najdete v tématu věnovaném [přihlášení](#sign-in) .

2. **Klikněte na odkaz pozvat nebo otevřete pozvánku v prohlížeči.**

    Nyní stačí otevřít (nebo znovu otevřít) odkaz na pozvánku v prohlížeči.

    > **Poznámka:** Pokud jste ještě nenainstalovali rozšíření Live Share, zobrazí se odkazy na tržiště rozšíření. Nainstalujte rozšíření a restartujte nástroj a zkuste to znovu.

    Měli byste upozornit, že prohlížeč chce spustit nástroj s povoleným Live Share. Pokud necháte vybraný nástroj spuštěný, budete po jeho spuštění připojeni k relaci spolupráce.

    ![Připojit stránku](../media/join-page.png)

    Pokud je hostitel v režimu offline, budete místo toho upozorněni v tomto okamžiku. Pak se můžete obrátit na hostitele a požádat ho, aby se znovu sdílel.

    > [!NOTE]
    > Pořád máte problémy? Podívejte se na téma [ruční připojení](#join-manually).

3. **Uložte**

    To je! Za chvíli budete připojeni a můžete začít spolupracovat.

    Po přechodu na tlačítko "Live Share" se zobrazí zpráva "stav relace". Podívejte se na informace o [stavu relace](#session-states) níže, aby to vypadalo takto.

    Po dokončení připojení se pak automaticky provedete na soubor, který hostitel momentálně upravuje.

### <a name="join-manually"></a>Ruční připojení

Můžete se také ručně připojit bez použití webového prohlížeče, který může být užitečný v situacích, kdy je již spuštěný nástroj, který chcete použít, chcete použít jiný nástroj, který není obvykle k dispozici, nebo pokud máte potíže s tím, že budete mít k dispozici odkazy na pozvání z nějakého důvodu. Proces je jednoduchý:

1. **Přihlásit se**

    Po instalaci rozšíření Live Share se budete chtít přihlásit, aby mohli jiní spolupracovníky informovat o tom, kdo máte. Ve výchozím nastavení používá Visual Studio účet pro přizpůsobení, takže tento krok bude možné úplně přeskočit.

    Další podrobnosti najdete v tématu věnovaném [přihlášení](#sign-in) .

2. **Použití příkazu JOIN**

    Jednoduše přejít na **soubor > připojit Live Share relaci**

    ![Nabídka VS JOIN](../media/vs-join.png)

3. **Vložit odkaz pro pozvání**

    Vložte adresu URL pozvánky, kterou jste poslali a zkontrolovali.

4. **Uložte!**

    A to je vše! V tuto chvíli byste měli být připojeni k relaci spolupráce.

    Po přechodu na tlačítko "Live Share" se zobrazí zpráva "stav relace". Podívejte se na informace o [stavu relace](#session-states) níže, aby to vypadalo takto.

    Po dokončení připojení se pak automaticky provedete, kde se hostitel momentálně upravuje.

### <a name="leave-the-collaboration-session"></a>Opustit relaci spolupráce

Jako hosta můžete opustit relaci spolupráce bez jejího ukončení pro jiné tím, že nástroj jednoduše zavřete a kliknete na tlačítko sdílet/vytvořit stav a vyberete opustit relaci pro spolupráci.

![Nabídka VS JOIN](../media/vs-leave-session.png)

Všechny dočasné soubory se automaticky vyčistí, takže není potřeba žádná další akce.

Máte problémy s připojením? Podívejte se na [řešení potíží](../troubleshooting.md#share-and-join).

## <a name="co-editing"></a>Společné úpravy

Jakmile se host připojí k relaci spolupráce, všichni spolupracovníci budou moci okamžitě zobrazit všechny ostatní úpravy a výběry v reálném čase. Vše, co potřebujete udělat, je vybrat soubor z Průzkumníka souborů a začít upravovat. Hostitelé i hosté uvidí úpravy, jak je provedete, a mohou přispět k tomu, aby se daly snadno iterovat a rychle nail řešení.

> [!NOTE]
> Připojení relace pro spolupráci, která je jen pro čtení, brání hostům v tom, aby mohli provádět úpravy souborů. Hostitel může [při sdílení povolit režim jen pro čtení](#share-a-project). Jako Host můžete zjistit, jestli jste se připojili k relaci jen pro čtení, a to tak, že prohlížíte [stav relace](#session-states).

![Snímek obrazovky znázorňující souběžné úpravy](../media/vs-coedit.png)

> [!NOTE]
> Společné úpravy mají několik omezení pro určité jazyky. Stav funkcí podle jazyků najdete v článku [o podpoře platforem](../reference/platform-support.md).

Výběry, které provedete, jsou kromě kurzorů a úprav viditelné i pro všechny účastníky ve stejném souboru. To usnadňuje zdůraznění, kde možná existují problémy, nebo vyjádřete nápady.

![Snímek obrazovky znázorňující zvýraznění](../media/vs-highlight.png)

Ještě lepší a ostatní účastníci můžou přejít na libovolný soubor ve sdíleném projektu. Můžete buď upravit dohromady, nebo nezávisle na tom, co můžete bez problémů přepínat mezi vyšetřováním, drobnými vylepšeními a kompletními úpravami spolupráce.

> [!NOTE]
> Ve výchozím nastavení Live Share sdílet otevřené soubory mimo sdílené řešení. Pokud chcete tuto funkci zakázat, aktualizujte v nabídce nástroje &gt; možnost &gt; sdílet externí soubory Live share na hodnotu NEPRAVDA.

Výsledné úpravy jsou uložené v počítači hostitele při uložení, takže nemusíte po dokončení úprav provádět synchronizaci, vkládání ani posílání souborů. Úpravy jsou "jenom tam."

> **Tip zabezpečení:** Vzhledem k tomu, že všichni účastníci můžou nezávisle Procházet a upravovat soubory jako hostitel, možná budete chtít omezit, které soubory hostů mají mít přístup k vašemu projektu prostřednictvím souboru. vsls. JSON. Jako host je také důležité si uvědomit, že v důsledku těchto nastavení se některé soubory nezobrazuje. Podrobnosti najdete v tématu [řízení přístupu k souborům a viditelnost](../reference/security.md#controlling-file-access-and-visibility) .

### <a name="changing-participant-flag-behaviors"></a>Změna chování příznaku účastníka

Ve výchozím nastavení Visual Studio Live Share automaticky zobrazuje příznak vedle kurzoru účastníka při najetí myší nebo při úpravách, zvýraznění nebo přesunutí kurzoru. V některých případech můžete chtít toto chování změnit. Postup:

1. V **nabídce nástroje > možnosti > Live Share**
2. Změňte možnost **viditelnosti** příznaku na jednu z následujících možností:

| Možnost | Chování |
|--------|----------|
| OnHoverOnly | Příznak se zobrazí, pouze když najedete myší na kurzor. |
| OnHoverOrActivity | Toto nastavení je výchozí. Příznak se zobrazí při najetí myší nebo v případě, že se kurzor upraví, zvýrazní nebo přesune. |
| Vždy | Příznak je vždy zobrazen.

## <a name="following"></a>Důsledku

Pokaždé, když jste v relaci spolupráce, uvidíte, že se v pravém horním rohu v editoru vedle tlačítka přihlásit zobrazí iniciály každého účastníka. Po najetí myší na iniciály se zobrazí úplné informace o účastníkůch.

![Snímek obrazovky znázorňující uživatele](../media/vs-person.png)

Někdy může být nutné vysvětlit problém nebo návrh, který zahrnuje více souborů nebo umístění v kódu. V těchto situacích může být užitečné dočasně sledovat kolegy při pohybu v rámci projektu. Z tohoto důvodu jako hosta, když se připojíte k relaci spolupráce, budete automaticky sledovat hostitele. V případě, že následuje po účastníkovi, zůstane Editor synchronizován s aktuálně otevřeným souborem, kurzorem a umístěním posuvníku.

> [!NOTE]
> Ve výchozím nastavení Live Share sdílet otevřené soubory mimo sdílené řešení. Pokud chcete tuto funkci zakázat, aktualizujte v nabídce nástroje &gt; možnost &gt; sdílet externí soubory Live share na hodnotu NEPRAVDA.

Chcete-li se snadno přepnout z režimu "Sledujte" a začít upravovat sami, přestanou sledovat, pokud dojde k některé z následujících akcí:

1. Můžete upravit, přesunout kurzor nebo provést výběr.
2. Vyberete jiný soubor

Kdykoli můžete v pravém horním rohu kliknout na iniciály osoby, kterou máte pod tímto tlačítkem zastavit. Kolem iniciály účastníka, která označuje, že se vám tato označení dostanou, zmizí.

![Sledovaný účastník sady Visual Studio](../media/vs-pinned.png) ![Účastník sady Visual Studio není následován](../media/vs-pin-hover.png)

Kliknutím na jakékoli iniciály v tomto umístění můžete v relaci spolupráce sledovat všechny hostitele nebo hosta. Všimněte si, že pokud chcete pouze přejít na místo, kde se nachází, stačí dvakrát kliknout na jejich iniciály.

## <a name="focusing"></a>Zaměřovat

Občas můžete chtít, aby všichni uživatelé v relaci spolupráce pocházeli a prohlédli se na něco, co děláte. Live Share vám umožní položit vás o tom, že vás na vás bude věnovat oznámení, které vám usnadní vám to, abyste mohli postupovat zpátky.

Stačí kliknout na tlačítko stav relace/sdílet v pravém horním rohu a vybrat možnost účastníci – výběr.

![Možnost detailní nabídky](../media/vs-focus.png)

Všichni uživatelé v relaci spolupráce získají oznámení, že jste si vyžádali upozornění.

![Informační zpráva soustředěného oznámení](../media/vs-focus-toast.png)

Potom můžou kliknout na sledovat hned z oznámení, když jsou připravení na vás na vás soustředit.

## <a name="co-debugging"></a>Společné ladění

Funkce pro spolupráci při ladění Visual Studio Live Share je účinný a jedinečný způsob, jak tento problém ladit. Kromě povolení prostředí pro spolupráci při řešení problémů, ale i dalších účastníků ve vaší relaci je schopnost prozkoumat problémy, které můžou být specifické pro prostředí, tím, že poskytuje sdílenou relaci ladění v počítači hostitele.

> **Tip zabezpečení:** Vzhledem k tomu, že všichni účastníci můžou nezávisle Procházet a upravovat soubory jako hostitel, možná budete chtít omezit, které soubory hostů mají mít přístup k vašemu projektu prostřednictvím souboru. vsls. JSON. Měli byste taky mít na paměti, že konzola/REPL přístup znamená, že účastníci můžou na svém počítači spouštět příkazy, takže byste měli jenom ladit jenom ty, které důvěřujete. Jako host je také důležité si uvědomit, že v důsledku těchto nastavení nemusí být možné sledovat ladicí program jako krok do určitých souborů s omezenými oprávněními. Podrobnosti najdete v tématu [řízení přístupu k souborům a viditelnost](../reference/security.md#controlling-file-access-and-visibility) .

Jednoduché použití. Hostitel relace pro spolupráci jednoduše potřebuje spustit ladění prostřednictvím obvyklých způsobů v aplikaci Visual Studio.

![Tlačítko ladění VS](../media/vs-debug-button.png)

Jakmile se ladicí program připojí na straně hostitele, automaticky se připojí i všichni hosté. I když je na počítači hostitele spuštěná jedna ladění "relace", všichni účastníci jsou k němu připojeni a mají vlastní zobrazení.

> [!TIP]
> Pokud chcete změnit, kdy a jak probíhá společné ladění, můžete změnit výchozí chování prostřednictvím nastavení v části **nástroje > možnosti > Live Share**.

![Připojený ladicí program VS](../media/vs-debugger.png)

Kdokoli může procházet proces ladění, který umožňuje bezproblémové přepínání mezi spolupracovníky bez nutnosti vyjednávání řízení.

> [!NOTE]
> Stav funkcí ladění podle jazyků a platforem najdete v článku [o podpoře platforem](../reference/platform-support.md).

Každý spolupracovníka může prozkoumat různé proměnné, přejít na jiné soubory v zásobníku volání, kontrolovat proměnné a dokonce přidávat nebo odebírat zarážky. Funkce společného úprav pak umožní každému účastníkovi Orator sledovat, kde jsou ostatní, a poskytnout tak jedinečnou schopnost plynule přepínat mezi současným zkoumáním různých aspektů problému a laděním v rámci spolupráce.

> [!NOTE]
> V relaci pro spolupráci, která je jen pro čtení, Host nebude moci procházet procesem ladění. Mohou však stále přidávat nebo odebírat zarážky a kontrolovat proměnné.

> [!TIP]
> Můžete se také zúčastnit VS Code ladicích cvičení ze sady Visual Studio a naopak. Další informace najdete v pokynech k [aplikaci Visual Studio](vscode.md#co-debugging) ve společném ladění.

### <a name="automatic-web-app-sharing"></a>Automatické sdílení webových aplikací

Ještě lepší pro projekty webové aplikace v ASP.NET ve výchozím nastavení, pokud je projekt hostitele nakonfigurovaný tak, aby automaticky spouštěl webový prohlížeč pro připojení k běžící webové aplikaci při ladění, Live Share automaticky provede totéž na počítači hosta! To se provádí zabezpečeným způsobem a vzdálená webová aplikace je k dispozici pouze hostům během relace ladění ve výchozím nastavení.

Informace o tom, jak sdílet přístup k serveru pro jiné typy projektů a/nebo po dobu trvání relace, najdete v tématu věnovaném [sdílení serveru](#share-a-server) .

> [!TIP]
> Pokud se vám nelíbí automatické sdílení prohlížeče a chcete ho změnit, můžete aktualizovat nastavení v části **nástroje > možnosti > Live Share**.

![Animace souběžného ladění](../media/co-debug.gif)

### <a name="change-when-visual-studio-joins-debugging-sessions"></a>Změnit, kdy se Visual Studio připojí k ladění relací

Ve výchozím nastavení se jako host automaticky připojí k ladicím relacím, když jsou sdíleny hostitelem. V některých případech ale může dojít k narušení tohoto chování. Naštěstí je můžete změnit následujícím způsobem:

1. V **nabídce nástroje > možnosti > Live Share**
2. Změňte **možnost připojit relaci ladění** na jednu z následujících možností:

| Možnost | Chování |
|--------|----------|
| Automatické | Výchozí nastavení Jako host se automaticky připojíte k libovolné sdílené relaci ladění, kterou hostitel spustí. |
| Dotazován | Jako host se zobrazí výzva k tomu, zda se chcete připojit ke sdílené relaci ladění při jejím spuštění hostitelem. |
| Zásah | Jako host bude nutné ručně připojit všechny relace ladění. Viz [odpojování a opětovné připojení](#detaching-and-reattaching).|

### <a name="detaching-and-reattaching"></a>Odpojování a opětovné připojování

Jako hosta můžete chtít dočasně zastavit ladění. Naštěstí můžete jednoduše kliknout na ikonu stop (zastavit) na panelu nástrojů ladění a odpojit ladicí program bez vlivu na hostitele nebo jiné hosty.

Pokud jste aktualizovali nastavení, takže se už nebudete automaticky připojovat, nebo pokud se chcete jednoduše znovu připojit později, můžete jednoduše vybrat požadovanou spuštěnou relaci ladění z části vybrat položku po spuštění... rozevírací seznam...

![Tlačítko ladění VS](../media/vs-select-reattach.png)

... a potom klikněte na něj pro připojení.

![Tlačítko ladění VS](../media/vs-reattach.png)

## <a name="share-a-server"></a>Sdílení serveru

V době od času jako hostitel relace pro spolupráci můžete zjistit, že chcete sdílet další místní servery nebo služby s hosty. To může být v rozsahu od jiných RESTful koncových bodů databází nebo jiných serverů. Visual Studio Live Share vám umožní zadat číslo místního portu, případně jim přiřadit název a potom ho sdílet se všemi hosty.

Hosté pak budou mít přístup k serveru, který jste sdíleli na tomto portu z vlastního místního počítače na stejném stejném portu. Pokud například sdílíte webový server **běžící na portu 3000**, může host přistupovat ke stejnému běžícímu webovému serveru na svém http://localhost:3000 **vlastním počítači** . To se provádí prostřednictvím zabezpečeného tunelu SSH nebo SSL mezi hostitelem a hostů a ověřených prostřednictvím služby, abyste měli jistotu, že budou mít přístup jenom uživatelé v relaci spolupráce.

> **Tip zabezpečení:** Jako hostitel byste měli být velmi selektivní pomocí portů, které sdílíte s hosty, a přidružit je k portům aplikací (místo sdílení portu systému). Pro hosty se budou sdílené porty chovat stejně, jako by byly spuštěné na svém vlastním počítači na serveru nebo službě. To je velmi užitečné, ale pokud je nesprávný port sdílený, může být také riskantní.

Pro účely zabezpečení jsou k dispozici pouze servery, které jsou spuštěny na zadaných portech pro ostatní hosty. Naštěstí je snadné přidat ho jako **hostitele**relace pro spolupráci. Tady je postup:

1. Klikněte na tlačítko sdílet/nastavit stav v pravém horním rohu a vyberte Spravovat sdílené místní servery.

    ![Správa sdílených místních serverů](../media/vs-share-local-servers.png)

2. V zobrazeném dialogovém okně klikněte na Přidat a zadejte číslo portu, na kterém běží server místně, zadejte název, stiskněte klávesu ENTER a pak klikněte na OK.

    ![Správa sdílených místních serverů](../media/vs-manage-local-shared-servers.png)

A to je vše! Server na portu, který jste zadali, se teď namapuje na localhost každého hostitele na stejném portu (Pokud se tento port už nepoužívá)!

Pokud se port již používá v počítači hosta, je automaticky vybrán jiný. Naštěstí se jako host zobrazí seznam aktuálně sdílených portů (podle názvu, pokud je zadaný), kliknutím na tlačítko sdílet/vytvořit stav relace v pravém horním rohu a výběrem možnosti zobrazit sdílené místní servery.

![Sdílené místní servery viw](../media/vs-view-shared-servers.png)

Všimněte si, že *hosté nemůžou* řídit, které porty v počítači hostitele se sdílejí z bezpečnostních důvodů.

Aby bylo možné **ukončit** sdílení místního serveru, stačí jednoduše kliknout na tlačítko sdílet/vytvořit stav relace v pravém horním rohu výše, vybrat možnost spravovat sdílené místní servery a vybrat příslušný port a kliknout na tlačítko Odebrat.

## <a name="share-a-terminal"></a>Sdílení terminálu

Moderní vývojáři často používají celou řadu nástrojů příkazového řádku. Naštěstí Live Share umožňuje jako hostitele volitelně "sdílet terminál" s hosty. Sdílený terminál může být jen pro čtení nebo zcela spolupracovat, takže vy i hosté můžou spustit příkazy a zobrazit výsledky. Hostům můžete dát možnost zobrazit výstup terminálu nebo jim umožnit, aby mohli provádět testy, sestavení nebo dokonce třídění specifických problémů prostředí, ke kterým dochází pouze v počítači.

Ale terminály nejsou ve výchozím nastavení sdílené, protože dávají hostům alespoň přístup jen pro čtení k výstupu příkazů, které spouštíte (Pokud není možnost spouštět samotné příkazy). Tímto způsobem můžete volně spouštět příkazy v místních terminálech bez rizika a sdílet je jenom v případě, že to skutečně vyžaduje. Sdílené terminály můžou navíc spustit jenom hostitelé a zabránit tak tomu, aby mohli hosté spustit jednu z nich a něco neočekáváte nebo nesledujete.

Jako hostitel můžete terminál sdílet kliknutím na tlačítko stavu relace/sdílení v pravém horním rohu a výběrem jedné z položek nabídky "sdílet terminál".

![Nabídka terminálu](../media/vs-terminal-menu.png)

V tomto okamžiku můžete z nabídky vybrat terminálu jen pro čtení nebo pro čtení a zápis. Když je terminál pro čtení a zápis, každý může do terminálu zadat, včetně hostitele, což usnadňuje zaznamenání toho, jestli uživatel nedělá něco, co nelíbíte. Aby bylo ale bezpečné, měli byste **hostům udělit přístup pro čtení a zápis jenom v případě, že víte, že ho skutečně potřebují** a že mají na scénářích, kde chcete, aby host zobrazil výstup všech spuštěných příkazů.

> [!NOTE]
> Pokud je relace spolupráce v režimu jen pro čtení, může hostitel sdílet jenom terminály jen pro čtení.

Po výběru typu sdíleného terminálu, který chcete spustit, se zobrazí nový sdílený terminál pro všechny účastníky se správnými oprávněními. I když Visual Studio Code má vestavěnou podporu terminálů, aplikace Visual Studio nemá žádné z nich. Proto se ve výchozím nastavení zobrazí nové okno obsahující terminál. Pokud se ale [rozšíření terminálu/Swagger/docs/v1./Swagger/docs/v1.](https://marketplace.visualstudio.com/items?itemName=DanielGriffen.WhackWhackTerminal), Live Share místo toho vytvoří integrovaný terminál. Visual Studio vám poskytne odkaz na jeho instalaci při prvním spuštění nebo připojení ke sdílenému terminálu.

![Oznámení o instalaci Terminálové zprávy](../media/vs-terminal-install.png)

Chcete-li ukončit relaci terminálu, jednoduše zadejte příkaz exit nebo zavřete okno terminálu a každý z nich bude odpojen.

## <a name="session-states"></a>Stavy relací

Po spuštění nebo připojení relace spolupráce a přístup ke sdílenému obsahu bude tlačítko Live Share v pravém horním rohu aktualizovat jeho vzhled tak, aby odrážel stav aktivní relace spolupráce.

Tady jsou stavy, které obvykle vidíte:

| Stav | Tlačítko | Popis |
|-------|--------|-------------|
| Termín | ![VS – stav: neaktivní](../media/vs-status-share.png) | Žádná aktivní relace spolupráce a nic se nesdílí. |
| Provoz Sdílení probíhá | ![VS stav: probíhá sdílení](../media/vs-status-sharing.png) | Spouští se relace spolupráce a v krátké době začne sdílení obsahu. |
| Provoz Sdílení | ![VS – stav: sdílení aktivní ](../media/vs-status-active.png) | Relace spolupráce je aktivní a obsah se sdílí. |
| Provoz Sdílení jen pro čtení | ![VS stav: sdílení jen pro čtení](../media/vs-status-sharing-read-only.png)| Sdílení relace pro spolupráci jen pro čtení. |
| Jedná Relace se připojuje | ![Stav VS Code: spojování](../media/vs-status-joining.png) | Připojení k existující relaci spolupráce |
| Jedná Připojené k | ![VS – stav: připojeno](../media/vs-status-joined.png) | Připojená a připojená k aktivní relaci spolupráce a příjem sdíleného obsahu. |
| Jedná Připojeno jen pro čtení | ![VS stav: připojeno jen pro čtení](../media/vs-status-joined-read-only.png) | Připojeno a připojeno k aktivní relaci pro spolupráci jen pro čtení. |

## <a name="guest-limitations"></a>Omezení hostů

I když jsou v současné době k dispozici některé nedostatky hostů, při používání výše popsaných funkcí si hostitel relace spolupráce zachová kompletní funkce jejich nástroje podle vlastního výběru. Další informace najdete v následujících tématech:

- [Podpora jazyků a platforem](../reference/platform-support.md)
- [Podpora rozšíření](../reference/extensions.md)
- [Všechny hlavní chyby, žádosti o funkce a omezení](https://aka.ms/vsls-issues)
- [Všechny požadavky a omezení funkcí](https://aka.ms/vsls-feature-requests)

## <a name="next-steps"></a>Další kroky

Další informace najdete v těchto dalších článcích.

- [Rychlý start: Sdílení prvního projektu](../quickstart/share.md)
- [Rychlý start: Připojte se k první relaci.](../quickstart/join.md)
- [Postupy: Spolupráce pomocí Visual Studio Code](vscode.md)
- [Požadavky na připojení pro Live Share](../reference/connectivity.md)
- [Funkce zabezpečení Live Share](../reference/security.md)

Máte potíže? Podívejte se na článek o [odstraňování potíží](../troubleshooting.md) nebo nám [pošlete svůj názor](../support.md).
