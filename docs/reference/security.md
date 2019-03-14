---
title: Zabezpečení – Visual Studio Live sdílenou složku | Dokumentace Microsoftu
description: Informace o funkcích zabezpečení Visual Studio Live Share.
ms.custom: ''
ms.date: 12/17/2018
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
ms.openlocfilehash: 0bc97691ca7733f694190e86140b930e68657ade
ms.sourcegitcommit: 4f733c9053848f26da03d47050bcb734f6c98b31
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/02/2019
ms.locfileid: "57254831"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="security-features-of-live-share"></a>Zabezpečení funkce Live Share

Relace spolupráci ve Visual Studio Live Share jsou výkonné, umožňují libovolný počet lidí připojit v relaci a společně úpravy, ladění a další. Však zadána tato úroveň přístupu, můžete nepochybně bude zajímat funkce zabezpečení, které poskytuje Live Share. V tomto článku poskytujeme některá doporučení a možnosti pro zabezpečení prostředí podle potřeby.

**Stejně jako nástroj pro spolupráci, mějte na paměti, že by měl pouze sdílet kód, obsah a aplikace s uživateli, kterému můžete důvěřovat.**

## <a name="connectivity"></a>Připojení

Všechna připojení v aplikaci Visual Studio Live Share jsou SSH nebo SSL zašifrované a ověřování proti centrální služby k zajištění, že pouze ty v relaci spolupráce můžou získat přístup k jeho obsahu. Ve výchozím nastavení Live Share pokusí přímé připojení a spadne zpět na předávání přes cloud, pokud nejde navázat připojení mezi Host a hostitel. Všimněte si, že relay cloud Live Share nezachová veškerý provoz směrovat přes něj a není "stará" provoz nijak. Pokud chcete raději nechcete použít předávací služby však můžete změnit nastavení vždy připojil přímo.

Další informace o změně těchto chování a požadavky na připojení Live Share, najdete v tématu  **[požadavky na připojení pro Live Share](connectivity.md)**.

## <a name="invitations-and-join-access"></a>Pozvánky a připojení k přístupu

Pokaždé, když zahájit novou relaci pro spolupráci, Live Share generuje **nový jedinečný identifikátor** , který je umístěn v odkazu pozvánku. Tyto odkazy poskytují plnou, zabezpečené základní pozvat těch, kterým důvěřujete, protože identifikátor v odkazu je "bez uhodnutelných" a je _jediné platné po dobu trvání relace jeden spolupráci_.

### <a name="removing-an-unexpected-guest"></a>Odebírá se neočekávané hosta

Jako hostitele se automaticky zobrazí oznámení pokaždé, když se připojí relaci spolupráce hosta.

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

Stále lepší oznámení dává možnost Odebrat hosta, který je připojený, pokud z nějakého důvodu si nejste jisti je. (Například pokud jste omylem odeslali odkaz na celofiremní chatovací systém a náhodné zaměstnance připojené k.) Stačí kliknout na tlačítko "Odebrat" v oznámení, která se zobrazí a bude možné vyjmutí z relace spolupráci.

V **VS Code**, i v případě, že máte zavře oznámení spojení, máte také možnost odebrat účastníka po tomto. Tak, že otevřete Live Share zobrazení Průzkumníka nebo na vlastní kartu na panelu aktivit VS Code, můžete najeďte myší nebo klikněte pravým tlačítkem na název člena a a vyberte ikonu "Odeberte účastníka" nebo možnost.

![Odebrat člena v nástroji VS Code](../media/vscode-remove-participant.png)

### <a name="requiring-guest-approval"></a>Vyžádáním souhlasu hosta

Účastníci, které se připojit ke spolupráci relaci bude obvykle **přihlášení Live Share** pomocí pracovní nebo školní účet (AAD), osobní účet Microsoft nebo účet GitHub. While "oznámení + odebrat" výchozí pro přihlášení uživatele poskytuje dobrý poměr rychlosti a řízení pro tyto hosté, můžete chtít **uzamknout věci** o trochu výkonnější, pokud byste něco citlivé.

Kromě toho může být v některých případech vynucení všechny hosté se přihlásit k spolupráce relace problematické. Mezi příklady patří s dotazem, nové Live Share připojení jako Host, školní nebo výuka scénáře osobě nebo při spolupráci s někým, kdo nemá jeden z typů podporovaných účtu. Z těchto důvodů, Live Share umožňuje uživatelů, kteří jsou **Nepřihlášený** připojit relací spolupráci jako **jen pro čtení** hosty. Zatímco hostitele je potřeba **schválit** tyto hosté předtím, než bylo možné připojit ke ve výchozím nastavení, můžete chtít zakázat tyto "anonymní" hosté nebo místo toho je vždy schválit.

#### <a name="requiring-guest-approval-for-signed-in-users"></a>Vyžádání schválení hosta pro přihlášení uživatele

Pokud chcete zabránit přihlášení hostů v připojení k vaší spolupráci až do "schválení" je, změňte následující nastavení:

* V **VS Code**, přidejte následující settings.json (Soubor > Předvolby > Nastavení):

    ```json
    "liveshare.guestApprovalRequired": true
    ```

* V **sady Visual Studio**, nastavte nástroje > Možnosti > Live Share > "Požadovat schválení guest" na hodnotu True.

    ![Visual Studio okno nastavení s hosta schválení nastavení zvýrazněné](../media/vs-setting-guestapproval.png)

Od této chvíle budete vyzváni ke schválení každého typu Host, který připojí.

<table style="border: none;">
<tr style="border: none;">
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vscode-join-approval.png" width="100%" alt="Visual Studio Code join approval request" />
    </td>
    <td width="50%" style="vertical-align: top; border: none;">
        <img src="../media/vs-join-approval.png" width="100%" alt="Visual Studio join approval request"/>
    </td>
</tr>
</table>

Jako Host Pokud připojíte k relaci kde hostitele má toto nastavení povolené, vám dáme vědět ve stavovém řádku nebo se připojit dialogové okno, které Live Share čeká na hostiteli ke schválení.

#### <a name="auto-rejecting-or-accepting-users-that-are-not-signed-in-anonymous"></a>Zamítnutí automatického nebo přijímá uživatelů, které nejste přihlášení (anonymní)

Jak je popsáno výše, Live Share můžete nakonfigurovat tak, aby **uživatele, kteří nejsou přihlášeni** připojit k relaci spolupráci jako **jen pro čtení** hosty.  Přestože tyto **"anonymní" hosté musíte zadat název** při připojování, jednoduchý název neposkytuje stejnou úroveň záruky jako skutečné přihlášení. Proto **ve výchozím nastavení, hostitel se zobrazí výzva ke schválení** žádné anonymního typu Host bez ohledu na nastavení "požadovat schválení guest" nastavení popsané výše.

Je možné **vždy odmítnout** (zakázat anonymní hostů) nebo **vždy přijmout** anonymní uživatele místo toho následujícím způsobem:

* V **VS Code**, nastavte `liveshare.anonymousGuestApproval` v settings.json (Soubor > Předvolby > Nastavení) k `accept`, `reject`, nebo `prompt` (výchozí) podle potřeby.

* V **sady Visual Studio**, nastavte nástroje > Možnosti > Live Share > "schválení anonymního typu host" na přijmout, zamítnutí nebo se zeptat (výchozí) jako odpovídající.

 **Bez ohledu na to, mějte na paměti, že by měl odeslat pouze Live Share pozvánku odkazy na osoby, které důvěřujete.**

## <a name="controlling-file-access-and-visibility"></a>Řízení přístupu k souborům a viditelnost

Live Share vzdálené modelu jako Host, poskytuje přístup Rychlé čtení a zápisu u souborů a složek, aniž by bylo nutné synchronizovat celý obsah projektu s vámi sdílí hostitele. Můžete proto nezávisle na sobě Procházet a upravovat soubory ve stromové struktuře celý sdílený soubor. **Tato volnost však představovat rizika pro hostitele.** V koncept vývojář může vyjádřit souhlas se službou zúčastnit a upravovat zdrojový kód bez vašeho vědomí nebo si přečtěte citlivé zdrojový kód nebo "tajné" nachází někde ve stromové struktuře sdílený soubor. V důsledku toho jako hostitel nemusí být vždy žádoucí hostem a mají přístup k rozsahu projektu, který chcete sdílet. Další výhodou tohoto modelu vzdálené Naštěstí je, že můžete se rozhodnout "vyloučit" soubory, které nechcete sdílet s kýmkoli, aniž byste museli obětovat na funkci. Hosté můžou stále účastnit věci, jako je ladění relace, které by obvykle vyžadovaly k těmto souborům přístup, pokud chtěli podobně své vlastní.

Můžete to udělat tak, že přidáte **. vsls.json** soubor do složky nebo projektu, jsou sdílení. Všechna nastavení, které přidáte do této formátovaného souboru json změní způsob Live Share zpracování souborů. Kromě toho, že přímou kontrolu, tyto soubory lze také potvrdit do správy zdrojového kódu, kdokoli klonování projektu budete moct využít výhod tato pravidla se žádné další úsilí na jejich část.

Tady je příklad. vsls.json souboru:

```json
{
    "$schema": "http://json.schemastore.org/vsls",
    "gitignore":"none",
    "excludeFiles":[
        "*.p12",
        "*.cer",
        "token",
        ".gitignore"
    ],
    "hideFiles": [
        "bin",
        "obj"
    ]
}
```

> [!NOTE]
> Můžete provést také všechny soubory či složky sdíleného **jen pro čtení** při spuštění relace spolupráci. Zobrazit [níže](#read-only-mode) podrobnosti.

Projděme si jak těchto vlastností změnit, co můžete dělat.

### <a name="properties"></a>Vlastnosti

**ExcludeFiles** vlastnost umožňuje určit seznam vzorů souborů glob (velmi podobně jako ty najít soubory .gitignore), který brání Live Share v otevření určité soubory nebo složky pro hosty. Mějte na paměti, že jde o včetně scénáře, jako jsou Host _následující nebo přechod na vaši polohu úpravy krokování s vnořením do souboru během ladění spolupráce žádné funkce pro navigaci kódu, jako jsou přejít k definici a další._ Je určená pro soubory, které nechcete sdílet za žádných okolností, například těch, které obsahují tajné kódy, certifikáty a hesla. Například od té doby se ovládací prvek zabezpečení,. vsls.json soubory jsou vždycky vyloučení.

**HideFiles** vlastnost je podobné, ale není úplně jako strict. Tyto soubory jsou skryté jednoduše ze stromu souborů. Pokud například chcete-li do jedné z těchto souborů během ladění, je stále otevřený v editoru. Tato vlastnost je primárně užitečná, pokud nemáte instalační soubor .gitignore (jako by tomu bylo pokud používáte systém správy různých zdrojového kódu) nebo pokud chcete jednoduše rozšířit, co je již existuje vyhnout se nepořádku nebo nejasnosti.

**Gitignore** nastavení zjistí, jak má Live Share zpracovat obsah souborů .gitignore ve sdílených složkách. Ve výchozím nastavení jsou považovány všechny globy najít v souborech .gitignore, jako kdyby byly zadány ve vlastnosti "hideFiles". Ale můžete použít různé chování pomocí jedné z následujících hodnot:

| Možnost    | Výsledek                                                                                                                 |
| --------- | ---------------------------------------------------------------------------------------------------------------------- |
| `none`    | obsah souboru .gitignore jsou viditelné pro hosty stromovou strukturu souborů (za předpokladu, že nejsou filtrovány podle typu Host editor nastavení). |
| `hide`    | **Výchozí hodnota.** Globy uvnitř .gitignore jsou zpracovávány jako by byly ve vlastnosti "hideFiles".                   |
| `exclude` | Globy uvnitř .gitignore jsou zpracovávány jako by byly ve vlastnosti "excludeFiles".                                 |

Z nevýhod `exclude` nastavení je, že obsah složky, například node_modules jsou často používány .gitignore, ale může být užitečná pro krokování s vnořením během ladění. V důsledku toho Live Share podporuje možnost vrátit pravidlem využívajícím "!" ve vlastnosti excludeFiles. Například to. soubor vsls.json by vyloučit vše, co v ".gitignore" s výjimkou node_modules:

```json
{
    "$schema": "http://json.schemastore.org/vsls",
    "gitignore":"exclude",
    "excludeFiles":[
        "!node_modules"
    ]
}
```

Skrýt a vyloučení pravidla se zpracovávají odděleně, tak pokud stále chcete skrýt node_modules přehlednost bez skutečně s výjimkou, lze jednoduše upravit soubor následujícím způsobem:

```json
{
    "$schema": "http://json.schemastore.org/vsls",
    "gitignore":"exclude",
    "excludeFiles":[
        "!node_modules"
    ],
    "hideFiles":[
        "node_modules"
    ]
}
```

### <a name="vslsjson-files-in-sub-folders"></a>. vsls.json soubory v podsložkách

A konečně, stejně jako .gitignore,. vsls.json soubory mohou být umístěny v podsložkách. Skrýt/vyloučit pravidla jsou určeny začínající. vsls.json soubor v kořenové složce jste sdíleli (pokud existuje) a potom provede na každou podsložku ze zde nejlepší pro daný soubor hledat. vsls.json souborů ke zpracování. Obsah. vsls.json souborů ve složkách dále dolů stromovou strukturu souborů pak doplňují (nebo přepsat) pravidla naváže na vyšších úrovních.

### <a name="disabling-external-file-sharing"></a>Zakázání sdílení externího souboru

Ve výchozím nastavení, Live Share budou také mluvit o hostitele se otevře všechny soubory, které jsou externí sdílené složky nebo řešení. To usnadňuje rychlé otevřete další související soubory bez nutnosti opětovné sdílení.

Pokud chcete zakázat tuto funkci:

* V **VS Code**, přidejte do settings.json následující:

    ```json
    "liveshare.shareExternalFiles": false
    ```

* V **sady Visual Studio**, nastavte nástroje &gt; možnosti &gt; Live Share &gt; "Sdílené složky externích souborů" na hodnotu False

## <a name="read-only-mode"></a>Režim jen pro čtení

Někdy, když budete sdílet váš kód jako hostitele, nechcete hosté provádět úpravy. Je třeba vaše hostem a podívejte se na část kódu nebo váš projekt se zobrazují na velký počet hostů a nechcete, aby veškeré úpravy zbytečné nebo nechtěné má být provedeno. Sdílené složky za provozu nabízí možnost sdílení projektů v režimu jen pro čtení.

Jako hostitele, při sdílení máte možnost povolit režimu jen pro čtení pro relaci spolupráci. Poté, co Host připojí, nebudou moct provádět úpravy kódu, i když vám může stále vidět uživatele toho druhého kurzory a zvýrazní také procházet projektu.

Budete moci stále společně ladit s hostů v režimu jen pro čtení. Hosté nebude se moct projít procesem ladění, ale můžete pořád přidat nebo odebrat zarážky a kontrolovat proměnné. Kromě toho můžete sdílet terminály (jen pro čtení) a servery s hosty.

Další informace o spuštění relace spolupráci jen pro čtení: [![VS Code](../media/vscode-icon-15x15.png)](../use/vscode.md#share-a-project) [![VS](../media/vs-icon-15x15.png)](../use/vs.md#share-a-project)

## <a name="co-debugging"></a>Společné ladění

Při jste řešení kódování palčivé problémy nebo chyby, může být velice užitečné při ladění s další pár očí. Visual Studio Live Share umožňuje "spolupráci ladění" nebo "společně ladění" sdílením relace ladění se všechny hosté při každém spuštění hostitele ladění.

Jako hostitele budete mít plnou kontrolu nad při spuštění relace ladění nebo zastaví, ale společně ladění představují některé riziko, pokud obsah sdílíte s někým, kterým nedůvěřujete. Sdílená složka za provozu umožňuje hosté pozvat spouštět příkazy konzoly/REPL a není proto **riziko škodlivý objekt actor spuštěním příkazu není vhodné, aby běžela**.

V důsledku toho byste měli **pouze společně s těmi, že důvěřujete ladění.**

Víc se uč: [![VS Code](../media/vscode-icon-15x15.png)](../use/vscode.md#co-debugging) [![VS](../media/vs-icon-15x15.png)](../use/vs.md#co-debugging)

## <a name="sharing-a-local-server"></a>Sdílení místního serveru

Při společném ladění může být opravdu užitečné mít přístup k různým částem aplikace obsluhované hostitelem pro ladicí relaci. Můžete chtít přístup k aplikaci v prohlížeči, přístup k místní databázi nebo stiskněte tlačítko koncového bodu REST z vašich nástrojů. Sdílené složky za provozu umožňuje "sdílení na serveru", který mapuje na přesně stejný port na počítači hosta na počítači hostitele jiný místní port. V roli hosta, můžete pak můžou pracovat s aplikací stejně, jako kdyby byla spuštěná místně na svém počítači (například hostitele a hosta můžete jak přístup do webové aplikace spuštěné http://localhost:3000).

Nicméně jako hostitele, měli byste **velmi pečlivě s porty sdílíte** s hostů a pouze sdílené složky aplikace porty spíše systému porty. Pro hosty sdílené porty budou chovat stejně, jako kdyby je sdíleli, pokud byla spuštěna služba server nebo na vlastní počítač. To je velmi užitečný, ale pokud sdílí se Chybný port může být také rizikové. Z tohoto důvodu se neprovede Live Share nevyvozujte předpoklady o tom, co by měl nebo by se neměly sdílet bez nastavení konfigurace a na hostiteli provést akci.

V sadě Visual Studio **webové aplikace port** zadaný v projektech ASP.NET je **automaticky sdílené během ladění pouze** usnadnit přístup hosta s webovou aplikací při spuštění. Ale můžete vypnout tato automatizace nastavením nástroje > Možnosti > Live Share > "Sdílené složky webovou aplikaci na ladění" do "False", který preferujete.

Ve Visual Studio Code, Live Share pokusí **detekovat porty příslušná aplikace** a sdílet je. Můžete to však zakázat přidáním následujícího kódu do settings.json:

        liveshare.autoShareServers: false

V obou případech buďte opatrní při sdílení další porty.

Další informace o konfiguraci funkce tady: [![VS Code](../media/vscode-icon-15x15.png)](../use/vscode.md#share-a-server) [![VS](../media/vs-icon-15x15.png)](../use/vs.md#share-a-server)

## <a name="sharing-a-terminal"></a>Sdílení terminálu

Moderní vývojáři často používají celou řadu nástrojů příkazového řádku. Live Share vám jako hostiteli naštěstí umožňuje volitelné „sdílení terminálu“ s hosty. Sdílený terminál může být jen pro čtení nebo plně spolupráci, tak i u hostů můžete spouštět příkazy a analyzovat výsledky. Jako hostitele budete moct povolit další spolupracovníci buď jenom zobrazit výstup, nebo použít libovolný počet příkazového řádku nástroje pro spuštění testů, sestavení, nebo dokonce i Třiďte problémy specifické pro prostředí.

Pouze hostitelé, můžete začít sdílené terminály, aby se zabránilo hostů z jednoho spuštění a něco se očekává nebo sledování. Když spustíte sdílený terminál jako hostitele, můžete určit, zda by měla být jen pro čtení nebo pro čtení a zápisu. Čtení a zápisu po terminálu everyone zadejte v terminálu, včetně hostitele, což usnadňuje zasáhnout, jestliže Host dělá něco, co nesouhlasíte. Však být bezpečné, měli byste **pouze poskytnout přístup pro čtení a zápisu pro hosty, když víte, které skutečně potřebují** a Zůstaňte u terminálů jen pro čtení pro scénáře, kde chceš jenom hostem a zobrazit výstup všechny příkazy spustíte.

V sadě Visual Studio nejsou terminály sdílené ve výchozím nastavení. V nástroji VS Code, jsou automaticky sdílet terminály **jen pro čtení** ve výchozím nastavení. Můžete to však zakázat přidáním následujícího kódu do settings.json:

```json
"liveshare.autoShareTerminals": false
```

Víc se uč: [![VS Code](../media/vscode-icon-15x15.png)](../use/vscode.md#share-a-terminal) [![VS](../media/vs-icon-15x15.png)](../use/vs.md#share-a-terminal)

## <a name="aad-admin-consent"></a>AAD Admin Consent

Po přihlášení pomocí služby Microsoft zajišťuje **pracovní nebo školní e-mailovou adresu** může se zobrazit zpráva s oznámením **"Vyžaduje schválení správcem"** při přihlášení. Je to proto Live Share vyžaduje přístup pro čtení k uživatelské informace pro jeho funkce zabezpečení a vašeho tenanta Azure AD je nastavit tak, aby vyžadovala "souhlas správce" pro přístup k obsahu adresáře nové aplikace.

Správce AD by potřeba tento problém vyřešit pomocí následujících informací:

* **Název aplikace**: Visual Studio za sdílené složky (Insider)
* **Typ aplikace**: Webové aplikace
* **Stav aplikace**: Produkční
* **Delegovaná oprávnění**: User.Read
* **Adresa URL aplikace**: https://insiders.liveshare.vsengsaas.visualstudio.com/
* **Adresa URL pro odpověď**: https://insiders.liveshare.vsengsaas.visualstudio.com/auth/redirect/windowslive/

To by stačí provést jednou pro každého, kdo pomocí Live Share. Zobrazit [tady](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-v2-scopes#admin-restricted-scopes) a [tady](https://stackoverflow.com/questions/39861830/azure-ad-admin-consent-from-the-azure-portal) podrobnosti.

## <a name="see-also"></a>Viz také:

* [Postupy: Spolupráce pomocí Visual Studio Code](../use/vscode.md)
* [Postupy: Spolupráce pomocí sady Visual Studio](../use/vs.md)
* [Požadavky na připojení pro Live Share](connectivity.md)

Máte potíže? Podívejte se na článek o [odstraňování potíží](../troubleshooting.md) nebo nám [pošlete svůj názor](../support.md).
