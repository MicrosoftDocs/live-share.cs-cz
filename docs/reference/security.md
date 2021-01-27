---
title: Zabezpečení | Microsoft Docs
description: Informace o funkcích zabezpečení Visual Studio Live Share.
ms.custom: ''
ms.date: 12/17/2018
ms.reviewer: ''
ms.suite: ''
ms.topic: reference
author: chuxel
ms.author: clantz
manager: AmandaSilver
ms.workload:
- liveshare
ms.openlocfilehash: 2b3021e96b321976772e6ab99a18cceb56929404
ms.sourcegitcommit: 9deed590c0876b732c8eb150a9a23498a8243efc
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/27/2021
ms.locfileid: "98870877"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="security-features-of-live-share"></a>Funkce zabezpečení Live Share

Relace spolupráce v Visual Studio Live Share jsou výkonné v tom, že umožňují, aby se v relaci mohl připojit libovolný počet lidí a spolupracovat s nimi i s možností úprav, ladění a dalších možností. Vzhledem k této úrovni přístupu vám však nemusíte mít k dispozici žádné pochybnosti o funkcích zabezpečení Live Share. V tomto článku poskytneme některá doporučení a možnosti pro zabezpečení vašeho prostředí podle potřeby.

**Stejně jako u všech nástrojů pro spolupráci si pamatujte, že byste měli sdílet jenom svůj kód, obsah a aplikace s lidmi, kterým důvěřujete.**

## <a name="connectivity"></a>Připojení

Když inicializujete relaci mezi partnerskými uzly, Live Share pokusy o navázání připojení typu peer-to-peer, a to jenom v případě, že to není možné (např. kvůli branám Firewall/NAT), se vrátí k používání Cloud Relay. V obou typech připojení (P2P nebo Relay) se ale všechna data přenášená mezi partnerskými uzly zašifrují pomocí protokolu SSH. V případě připojení typu relay je šifrování SSH vrstveno nad objekty WebSocket šifrovanými protokolem TLS. To znamená, že Live Share nezávisí na zabezpečení služby Cloud Relay. I v případě, že Relay došlo k ohrožení zabezpečení, nebylo by možné dešifrovat žádnou Live Share komunikaci.

Role Live Share služby je omezená na ověřování uživatelů a zjišťování relací. Služba sama o sobě neukládá ani nikdy nemá přístup k jakémukoli obsahu relace. Veškerý obsah uživatele v Live Share se přenáší přes relaci SSH. Zahrnuje kód, terminály, sdílené servery a jakékoli další funkce pro spolupráci, které poskytuje Live Share nebo rozšíření, která jsou na něm sestavena.

Další informace o změně těchto chování a požadavcích na připojení Live Share najdete v tématu **[požadavky na připojení pro Live Share](connectivity.md)**.

### <a name="wire-encryption"></a>Šifrování drátu 

Protokol SSH používá k navázání sdíleného tajného klíče pro relaci Diffie-Hellman Key-Exchange a je odvozen z klíče pro symetrické šifrování AES. Šifrovací klíč se pravidelně otáčí po celou dobu trvání relace. Tajný klíč sdílené relace a všechny šifrovací klíče se udržují pouze v paměti obou stran a jsou platné pouze po dobu trvání relace. Nikdy se nezapisují na disk ani neodesílají do žádné služby (včetně Live Share).

### <a name="peer-authentication"></a>Partnerské ověřování

Relace SSH je také obousměrně ověřena. Hostitel (role serveru SSH) používá ověřování pomocí veřejného a privátního klíče, jako je standard pro protokol SSH. Když hostitel sdílí relaci Live Share, vygeneruje pro relaci jedinečnou dvojici veřejného a privátního klíče RSA. Privátní klíč hostitele je udržován pouze v paměti v hostitelském procesu; Nikdy se nezapisuje na disk nebo se neposílá do žádné služby, včetně služby Live Share. Veřejný klíč hostitele se publikuje ve službě Live Share společně s informacemi o připojení relace (IP adresa nebo koncový bod přenosu), kde k němu můžou přistupovat hosty prostřednictvím odkazu na pozvánku. Když se host připojí k relaci SSH hostitele, Host použije ověřovací protokol hostitele SSH k ověření, že hostitel obsahuje privátní klíč odpovídající publikovanému veřejnému klíči (bez toho, aby se uživatel mohl podívat na privátní klíč).

Host používá token Live Share k ověření samotného hostitele. Token je podepsaný token JWT vydaný službou Live Share, který obsahuje deklarace identity uživatele (získané prostřednictvím přihlášení MSA, AAD nebo GitHub). Token má také deklarace identity, které naznačují, že host má povolený přístup k této konkrétní Live Share relaci (protože měl odkaz na pozvánku a/nebo byl speciálně pozván hostitel). Hostitel tento token ověří a zkontroluje deklarace identity (a v závislosti na možnostech se může uživateli zobrazit výzva k zadání hostitele) předtím, než se povolí hostovi připojit k relaci.

## <a name="invitations-and-join-access"></a>Pozvánky a přístup k nim

Pokaždé, když spustíte novou relaci spolupráce, Live Share vygeneruje **Nový jedinečný identifikátor** , který je umístěný v odkazu na pozvánku. Tyto odkazy poskytují Solid, zabezpečený základ pro pozvání, kterým důvěřujete, protože identifikátor v odkazu je "neuhodnoutelné" a je _platný pouze po dobu trvání jedné relace spolupráce_.

### <a name="removing-an-unexpected-guest"></a>Odebrání neočekávaného hosta

Jako hostitel se automaticky oznámí, kdykoli se host připojí k relaci spolupráce.

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

Ještě lepší je, že vám oznámení umožní odebrat hosta, který se připojí, pokud z nějakého důvodu ho neznáte. (Pokud jste například omylem publikovali odkaz na systém chatu v rámci společnosti a náhodný zaměstnanec byl připojen.) Jednoduše klikněte na tlačítko odebrat v zobrazeném oznámení a budou vysunuty z relace spolupráce.

V **vs Code** i v případě, že jste odzavřeli oznámení o připojení, máte také možnost odebrat účastníka. Otevřením zobrazení Live Share v Průzkumníkovi nebo vlastní karty na panelu VS Code aktivity můžete ukazatel myši napravit nebo kliknout pravým tlačítkem na jméno účastníka a vybrat ikonu odebrat účastníka nebo možnost.

![Odebrat účastníka v VS Code](../media/vscode-remove-participant.png)

### <a name="requiring-guest-approval"></a>Vyžadování schválení hostů

Účastníci, kteří se připojí k relaci spolupráce, budou obvykle **přihlášeni Live Share** pomocí pracovního nebo školního účtu Microsoft (AAD), osobního účet Microsoft nebo účtu GitHub. Zatímco výchozí nastavení Notification + Remove pro přihlášené uživatele má dobrou kombinaci rychlosti a řízení pro tyto hosty, možná budete chtít při práci s citlivými **objekty uzamknout** trochu víc.

V některých případech se může stát, že se všem hostům přihlašujete, aby se mohl připojit k relaci spolupráce, můžou být problematické. Mezi příklady patří požadavek někoho nového na Live Share, aby se mohl připojit jako scénář pro hosty, učebnu nebo výuku, nebo když spolupracuje s někým, kdo nemá některý z podporovaných typů účtů. Z těchto důvodů můžou Live Share umožnit uživatelům, kteří nejsou **přihlášení** , připojit se k relacím spolupráce jenom jako hosté s **oprávněním jen pro čtení** . I když hostitel potřebuje **schválit** tyto hosty ještě předtím, než se může připojit ve výchozím nastavení, možná budete chtít zakázat tyto "anonymní" hosty, nebo je místo toho vždy schvalovat.

#### <a name="requiring-guest-approval-for-signed-in-users"></a>Vyžadování schválení hostů pro přihlášené uživatele

Pokud chcete zabránit přihlášenému hostům v připojení k vašim relacím o spolupráci, dokud je neschválíte, změňte následující nastavení:

* V **vs Code** přidejte následující příkaz pro settings.js(> předvolby souboru > nastavení):

    ```json
    "liveshare.guestApprovalRequired": true
    ```

* V sadě **Visual Studio** nastavte nástroje > možnosti > Live Share > "vyžadovat schválení hostů" na hodnotu true.

    ![Okno nastavení sady Visual Studio s vybraným nastavením schválení hosta](../media/vs-setting-guestapproval.png)

Od tohoto okamžiku budete požádáni o schválení každého hosta, který se připojí.

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

Pokud se stanete hostem, když se připojíte k relaci s povoleným nastavením hostitel, zobrazí se oznámení ve stavovém řádku nebo dialogovém okně připojit, které Live Share čeká na schválení hostitele.

#### <a name="auto-rejecting-or-accepting-users-that-are-not-signed-in-anonymous"></a>Automatické odmítnutí nebo přijetí nepodepsaných uživatelů (anonymní)

Jak je popsáno výše, Live Share lze nakonfigurovat tak, aby umožňovala **uživatelům, kteří nejsou přihlášeni** , připojit relaci spolupráce jako hosty **jen pro čtení** .  I když tyto **"anonymní" hosty musí při připojování zadat název** , jednoduchý název neposkytuje stejnou úroveň záruky jako reálné přihlášení. Proto **je hostitel ve výchozím nastavení vyzván ke schválení** anonymního hosta bez ohledu na nastavení "vyžadovat schválení hostů".

Můžete **vždycky odmítat** (zakázat anonymní hosty) nebo **Vždy přijímat** anonymní uživatele, a to následujícím způsobem:

* V **vs Code** nastavte `liveshare.anonymousGuestApproval` v settings.jszapnuto (Souborová > předvolby > nastavení) na `accept` , `reject` nebo `prompt` (výchozí) podle potřeby.

* V sadě **Visual Studio** nastavte nástroje > možnosti > Live Share > "anonymního schvalování hostů" pro přijetí, odmítnutí nebo zadání výzvy (výchozí) podle potřeby.

 **Bez ohledu na to, že byste měli odesílat Live Share odkazy na pozvánky osobám, kterým důvěřujete.**

## <a name="controlling-file-access-and-visibility"></a>Řízení přístupu k souborům a jejich viditelnost

Vzdálený model Live Share Host vám poskytne rychlý přístup pro čtení a zápis k souborům a složkám, které s vámi hostitel sdílí, a to bez nutnosti synchronizovat celý obsah projektu. Proto můžete nezávisle Procházet a upravovat soubory v celém stromu sdíleného souboru. **Tato volnost ale představuje určité riziko pro hostitele.** V rámci konceptu může vývojář použít a upravit zdrojový kód bez vašeho vědomí nebo zobrazit citlivý zdrojový kód nebo "tajné klíče", které jsou umístěné někde ve stromu sdílených souborů. V důsledku toho je možné, že jako hostitel nebudete vždy chtít, aby měl Host přístup k celému projektu, který sdílíte. Naštěstí, což je výhodou tohoto vzdáleného modelu, je, že se můžete rozhodnout, že nechcete sdílet soubory, které nechcete sdílet s kýmkoli, aniž by došlo ke ztrátě funkčnosti. Vaše hosty se můžou pořád zúčastnit, jako jsou relace ladění, které by obvykle vyžadovaly přístup k těmto souborům, pokud by si chtěli dělat vlastní věci.

To lze provést přidáním **.vsls.js** do souboru do složky nebo projektu, který sdílíte. Všechna nastavení, která přidáte do tohoto souboru ve formátu JSON, mění způsob, jakým Live Share zpracovává soubory. Kromě toho, že máte přímý ovládací prvek, mohou být tyto soubory také zapsány do správy zdrojových kódů, aby každý klonování projektu mohli využít výhod těchto pravidel bez dalšího úsilí na jejich část.

Tady je příklad .vsls.jssouboru:

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
> Všechny soubory a složky, které sdílíte, můžete také nastavit tak, aby při zahájení relace spolupráce byly sdílené jen **pro čtení** . Podrobnosti najdete [níže](#read-only-mode) .

Podívejme se, jak se tyto vlastnosti mění, co můžou hosté dělat.

### <a name="properties"></a>Vlastnosti

Vlastnost **excludeFiles** umožňuje určit seznam vzorů souborů glob (velmi podobně jako u nalezených souborů. gitignore), které brání Live Share otevírání určitých souborů nebo složek pro hosty. Pamatujte na to, že se jedná o scénáře, jako je například Host, _nebo přechod do umístění pro úpravy, krokování do souboru během ladění s možností spolupráce, všechny funkce pro navigaci v kódu, jako je například přejít k definici a další._ Je určený pro soubory, které nikdy nechcete sdílet, jako ty, které obsahují tajné klíče, certifikáty nebo hesla. Například vzhledem k tomu, že se zabezpečení řídí, .vsls.jssoubory jsou vždy vyloučeny.

Vlastnost **hideFiles** je podobná, ale ne poměrně jako striktní. Tyto soubory jsou ze stromu souborů jednoduše skryté. Například pokud jste se v průběhu ladění přestali Krokovat s jedním z těchto souborů, je stále otevřen v editoru. Tato vlastnost je primárně užitečná, pokud nemáte instalaci souboru. gitignore (jak by to bylo v případě, že používáte jiný systém správy zdrojového kódu), nebo pokud chcete jednoduše rozšířit to, co už je, aby nedocházelo k zbytečnému zaplnění nebo nejasnostem.

Nastavení **gitignore** určuje, jak má Live Share zpracovat obsah souborů. gitignore ve sdílených složkách. Ve výchozím nastavení se všechny globy nalezené v souborech. gitignore považují za, jako kdyby byly zadány ve vlastnosti "hideFiles". Můžete ale zvolit jiné chování pomocí jedné z následujících hodnot:

| Možnost    | Výsledek                                                                                                                 |
| --------- | ---------------------------------------------------------------------------------------------------------------------- |
| `none`    | obsah. gitignore je viditelný pro hosty ve stromu souborů (za předpokladu, že nejsou filtrovány pomocí nastavení editoru hosta). |
| `hide`    | **Výchozí nastavení** Globy uvnitř. gitignore se zpracovávají, jako kdyby byly ve vlastnosti "hideFiles".                   |
| `exclude` | Globy uvnitř. gitignore se zpracovávají, jako kdyby byly ve vlastnosti "excludeFiles".                                 |

Nevýhodou `exclude` nastavení je, že obsah složek, jako node_modules, jsou často v. gitignore, ale může být užitečný pro krokování během ladění. V důsledku toho Live Share podporuje možnost obrátit pravidlo pomocí "!" ve vlastnosti excludeFiles. Například tato .vsls.jsv souboru vyloučí vše z ". gitignore" s výjimkou node_modules:

```json
{
    "$schema": "http://json.schemastore.org/vsls",
    "gitignore":"exclude",
    "excludeFiles":[
        "!node_modules"
    ]
}
```

Pravidla pro skrytí a vyloučení se zpracovávají samostatně, takže pokud stále chcete skrýt node_modules pro snížení zbytečných souborů bez toho, abyste je skutečně vyloučili, můžete soubor jednoduše upravit následujícím způsobem:

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

### <a name="vslsjson-files-in-sub-folders"></a>.vsls.jssouborů v podsložkách

Nakonec, stejně jako soubor. gitignore, .vsls.jsna soubory lze umístit do podadresářů. Pravidla pro skrytí nebo vyloučení se určují spuštěním .vsls.jsv souboru v kořenové složce, kterou jste sdíleli (Pokud je k dispozici), a následným prohledáním v každé podsložce, která je od začátku do daného souboru, a vyhledejte .vsls.jssouborů, které se mají zpracovat. Obsah .vsls.jssouborů ve složkách dále rozchází ke stromu souborů a pak doplňují (nebo přepíší) pravidla vytvořená na vyšších úrovních.

### <a name="disabling-external-file-sharing"></a>Zakazování sdílení externích souborů

Ve výchozím nastavení bude Live Share sdílet taky všechny soubory, které hostitel otevře, které jsou externí pro sdílenou složku nebo řešení. Díky tomu můžete snadno rychle otevřít další související soubory, aniž byste museli znovu sdílet.

Pokud chcete zakázat tuto funkci:

* V **vs Code** přidejte následující pro settings.jsna:

    ```json
    "liveshare.shareExternalFiles": false
    ```

* V sadě **Visual Studio** nastavte &gt; Možnosti nástrojů &gt; Live Share &gt; "sdílet externí soubory" na hodnotu false.

## <a name="read-only-mode"></a>Režim jen pro čtení

Někdy, když sdílíte kód jako hostitele, nechcete, aby mohli vaši hosté provádět úpravy. Může být nutné, aby se váš host prohlédl na některém z vašich kódů nebo aby se váš projekt zobrazoval na velký počet hostů a nemuseli být provedeny žádné zbytečné nebo náhodné úpravy. Live Share nabízí možnost sdílet projekty v režimu jen pro čtení.

Při sdílení máte jako hostitele možnost povolit režim jen pro čtení pro relaci spolupráce. Když se připojí hostů, nebude moct provádět úpravy kódu, i když stále vidíte kurzory a světla každého druhého a také můžete procházet projekt.

V režimu jen pro čtení můžete stále společně ladit s hosty. Hosté nebudou mít možnost Procházet proces ladění, ale přesto mohou přidávat nebo odebírat zarážky a kontrolovat proměnné. Kromě toho můžete s hosty sdílet i servery a terminály (jen pro čtení).

Můžete se dozvědět více o spuštění relace spolupráce jen pro čtení: [ ![ vs Code](../media/vscode-icon-15x15.png)](../use/vscode.md#share-a-project) [ ![ vs](../media/vs-icon-15x15.png)](../use/vs.md#share-a-project)

## <a name="co-debugging"></a>Společné ladění

Při řešení problémů s obtížovým kódováním nebo chybám, které mají další pár očí, když může být ladění skutečně užitečné. Visual Studio Live Share umožňuje "společné ladění" nebo "společné ladění" sdílením relace ladění se všemi hosty, kdykoli hostitel spustí ladění.

Jako hostitel máte při spuštění nebo zastavení relace ladění úplnou kontrolu, ale pokud sdílíte s někým, kterému nedůvěřujete, může společné ladění představovat některá rizika. Live Share umožňuje hostům pozvat na spouštění příkazů Console/REPL a existuje riziko, že **škodlivý objekt actor spouští příkazy, které nechcete spouštět**.

V důsledku toho byste měli **jenom ladit společně s důvěryhodnými.**

Další informace: [ ![ vs Code](../media/vscode-icon-15x15.png)](../use/vscode.md#co-debugging) [ ![ vs](../media/vs-icon-15x15.png)](../use/vs.md#co-debugging)

## <a name="sharing-a-local-server"></a>Sdílení místního serveru

Při společném ladění může být opravdu užitečné mít přístup k různým částem aplikace obsluhované hostitelem pro ladicí relaci. Můžete chtít mít přístup k aplikaci v prohlížeči, získat přístup k místní databázi nebo přejít z nástrojů na koncový bod REST. Live Share umožňuje "sdílet server", který mapuje místní port na počítači hostitele na přesný stejný port na počítači hosta. Jako host pak můžete s aplikací pracovat přesně stejně, jako kdyby běžela místně na vašem počítači (např. hostitel a Host může přistupovat k webové aplikaci běžící na http://localhost:3000) .

Nicméně jako hostitel byste měli **být velmi selektivními porty, které sdílíte** s hosty, a sdílet jenom porty aplikací namísto systémových portů. Pro hosty se budou sdílené porty chovat stejně, jako by byly spuštěné na svém vlastním počítači na serveru nebo službě. To je velmi užitečné, ale pokud je nesprávný port sdílený, může být také riskantní. Z tohoto důvodu Live Share neprovádí žádné předpoklady týkající se toho, co by se mělo nebo neměl sdílet bez nastavení konfigurace a hostitele, který provádí akci.

V aplikaci Visual Studio je **port webové aplikace** zadaný v projektech ASP.NET **automaticky sdílen pouze během ladění** , aby se usnadnil přístup hosta k webové aplikaci při spuštění. Tuto automatizaci ale můžete vypnout nastavením nástrojů > možností > Live Share > "sdílet webovou aplikaci při ladění" na hodnotu "false", pokud to dáváte přednost.

V Visual Studio Code se Live Share pokusí **zjistit správné porty aplikací** a sdílet je. Můžete to však zakázat přidáním následujících settings.jspro:

        liveshare.autoShareServers: false

V obou případech můžete při sdílení dalších portů dbát na výkon.

Další informace o konfiguraci této funkce najdete tady: [ ![ vs Code](../media/vscode-icon-15x15.png)](../use/vscode.md#share-a-server) [ ![ vs](../media/vs-icon-15x15.png)](../use/vs.md#share-a-server) .

## <a name="sharing-a-terminal"></a>Sdílení terminálu

Moderní vývojáři často používají celou řadu nástrojů příkazového řádku. Live Share vám jako hostiteli naštěstí umožňuje volitelné „sdílení terminálu“ s hosty. Sdílený terminál může být jen pro čtení nebo zcela spolupracovat, takže vy i hosté můžou spustit příkazy a zobrazit výsledky. Jako hostitel můžete ostatním spolupracovníkům dovolit buď pouze zobrazit výstup, nebo použít libovolný počet nástrojů příkazového řádku pro spuštění testů, sestavení nebo dokonce třídění problémů specifických pro prostředí.

Jenom hostitelé můžou zahájit sdílené terminály, aby mohli hosté spustit jednu z nich a provádět něco, co neočekáváte nebo sledujete. Když spustíte sdílený terminál jako hostitele, můžete určit, jestli má být jen pro čtení nebo pro čtení a zápis. Když je terminál pro čtení a zápis, každý může do terminálu zadat, včetně hostitele, což usnadňuje zaznamenání toho, jestli uživatel nedělá něco, co nelíbíte. Aby bylo ale bezpečné, měli byste **hostům udělit přístup pro čtení a zápis jenom v případě, že víte, že ho skutečně potřebují** a že mají na scénářích, kde chcete, aby host zobrazil výstup všech spuštěných příkazů.

V aplikaci Visual Studio nejsou terminály sdíleny ve výchozím nastavení. V VS Code jsou terminály ve výchozím nastavení automaticky sdíleny **jen pro čtení** . Můžete to však zakázat přidáním následujících settings.jspro:

```json
"liveshare.autoShareTerminals": false
```

Další informace: [ ![ vs Code](../media/vscode-icon-15x15.png)](../use/vscode.md#share-a-terminal) [ ![ vs](../media/vs-icon-15x15.png)](../use/vs.md#share-a-terminal)

## <a name="aad-admin-consent"></a>Souhlas správce AAD

Při přihlašování pomocí **pracovní nebo školní e-mailové adresy** Microsoftu se při přihlašování může zobrazit zpráva, že je **potřeba schválit správce** . Důvodem je to, že Live Share vyžaduje přístup pro čtení k informacím uživatelů pro své funkce zabezpečení a váš tenant služby Azure AD je nastavený tak, aby pro nové aplikace přistupující k obsahu adresáře vyžadoval souhlas správce.

Správce služby AD by tuto chybu musel vyřešit pomocí následujících informací:

* **Název aplikace**: Visual Studio Live Share (Insider)
* **Typ aplikace**: webová aplikace
* **Stav aplikací**: provozní
* **Delegovaná oprávnění**: uživatel. čtení
* **Adresa URL aplikace**: https://insiders.liveshare.vsengsaas.visualstudio.com/
* **Adresa URL odpovědi**: https://insiders.liveshare.vsengsaas.visualstudio.com/auth/redirect/windowslive/

To je potřeba udělat jenom jednou pro kohokoli, kdo používají Live Share. Podrobnosti najdete [tady](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-v2-scopes#admin-restricted-scopes) . [](https://stackoverflow.com/questions/39861830/azure-ad-admin-consent-from-the-azure-portal)

## <a name="see-also"></a>Viz také

* [Postupy: spolupráce pomocí Visual Studio Code](../use/vscode.md)
* [Postupy: spolupráce pomocí sady Visual Studio](../use/vs.md)
* [Požadavky na připojení pro Live Share](connectivity.md)

Máte potíže? Podívejte se na článek o [odstraňování potíží](../troubleshooting.md) nebo nám [pošlete svůj názor](../support.md).
