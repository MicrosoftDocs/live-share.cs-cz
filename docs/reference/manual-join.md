---
title: Ruční spojení – Visual Studio Live Share | Dokumentace Microsoftu
description: Informace o ruční spojování relaci spolupráce v aplikaci Visual Studio naživo sdílet.
ms.custom: ''
ms.date: 03/22/2018
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
ms.openlocfilehash: 57d26c2c63bd5b92e62a72368f97bb8aee63313c
ms.sourcegitcommit: 4f733c9053848f26da03d47050bcb734f6c98b31
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/02/2019
ms.locfileid: "57254827"
---
# <a name="join-a-session-manually"></a>Připojte se k relaci ručně

Kromě Otevřít odkaz v prohlížeči připojit k relaci spolupráce, můžete ručně připojit zadáním nebo vložením odkazu do je už spuštěný nástroj. To může být užitečné, pokud chcete použít jiný nástroj, než lze obvykle provést, nebo pokud se vám nedaří se získat pozvánky odkazy na pracovní z nějakého důvodu.

Přesné pokyny se liší mezi [sady Visual Studio](#join-from-visual-studio) a [Visual Studio Code](#join-from-visual-studio-code), si vyberte jakýkoliv nástroj, který máte v úmyslu používat pro další informace.

## <a name="join-from-visual-studio-code"></a>Připojte se k Visual Studio Code

### <a name="1-sign-in"></a>1. Přihlášení

>**Poznámka:** Pokud chcete připojit k relaci spolupráci jako Host jen pro čtení, můžete přeskočit přihlášení. Bude mít přístup k zobrazení a navigace kódu, jež jsou sdílena ale nebudete moci provádět úpravy.

![Informační zpráva s výzvou k přihlášení pomocí webového prohlížeče](../media/vscode-sign-in-toast.png)

Abyste mohli spolupracovat, budete potřebovat přihlášení do aplikace Visual Studio Live Share tak všem uživatelům ví, kdo jste. **Klikněte na tlačítko** na "Live Share" stavový řádek položky nebo stisknutím klávesy **Ctrl + Shift + P / Cmd + Shift + P** a vyberte "živé sdílené složky: Přihlaste se pomocí prohlížeče"příkaz.

![VS Code přihlašovací tlačítko](../media/vscode-sign-in-button.png)

Při oznámení se zobrazí spuštění s výzvou, abyste se přihlásili, spustí se váš prohlížeč. Dokončete proces v prohlížeči přihlašování a pak jednoduše zavřít prohlížeč, až budete hotovi.

Pokud používáte o problémech s VS Code není ujímají úspěšné přihlášení, klikněte na odkaz "Nedaří" na obrazovce úspěch v prohlížeči a postupujte podle pokynů. Podívejte se na [řešení potíží s](../troubleshooting.md#sign-in) další tipy.

### <a name="2-use-the-join-command"></a>2. Použití příkazu join

Otevřete Live Share viewlet na panelu aktivit VS Code a vyberte "připojení k relaci spolupráce..." ikona nebo položku.

![Ikona viewlet spojení](../media/vscode-join-viewlet.png)

>**Poznámka:** Pokud se připojíte jako Host jen pro čtení, můžete pak požádáni o zadání zobrazovaný název, který pomůže účastníky můžete identifikovat v relaci.

### <a name="3-paste-the-invite-link"></a>3. Vložte odkaz pozvánky

Vložte adresu URL pozvánky byly odeslány a přístupů 'zadejte potvrzení.

A to je vše! Musí být připojené k okamžité relaci spolupráce.

## <a name="join-from-visual-studio"></a>Připojte se k ze sady Visual Studio

### <a name="1-sign-in"></a>1. Přihlášení

Po instalaci, spusťte sadu Visual Studio a přihlásit, pokud nemáte. Pokud budete muset použít jiné přihlášení pro sadu Visual Studio než vaše [aktivního účtu přizpůsobení](https://docs.microsoft.com/en-us/visualstudio/ide/signing-in-to-visual-studio), přejděte na stránku **nástroje &gt; možnosti &gt; Live Share &gt; uživatelský účet**.

![Přihlaste se VS](../media/vs-sign-in-button.png)

Stále se nedaří? Zobrazit [řešení potíží s](../troubleshooting.md#sign-in).

### <a name="2-use-the-join-command"></a>2. Použití příkazu join

Jednoduše přejděte na **soubor > připojte se k relaci spolupráce**.

![Připojení k nabídce VS](../media/vs-join.png)

### <a name="3-paste-the-invite-link"></a>3. Vložte odkaz pozvánky

Vložte adresu URL pozvánky byly odeslány a přístupů 'zadejte potvrzení.

A to je vše! Musí být připojené k okamžité relaci spolupráce.

## <a name="see-also"></a>Viz také:

Rychlý start

- [Rychlý start: Sdílejte svůj první projekt](../quickstart/share.md)
- [Rychlý start: Připojte se k první relace](../quickstart/join.md)

Postupy

- [Postupy: Spolupráce pomocí Visual Studio Code](../use/vscode.md)
- [Postupy: Spolupráce pomocí sady Visual Studio](../use/vs.md)
- [Postupy: Poskytnout zpětnou vazbu](../support.md)

Odkaz

- [Požadavky na připojení pro Live Share](connectivity.md)
- [Funkce zabezpečení Live Share](security.md)
- [Podrobnosti o instalaci systému Linux](linux.md)
- [Podpora jazyků a platforem](platform-support.md)
- [Podpora rozšíření](extensions.md)

Máte potíže? Podívejte se na článek o [odstraňování potíží](../troubleshooting.md) nebo nám [pošlete svůj názor](../support.md).
