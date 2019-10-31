---
title: Ruční spojení – Visual Studio Live Share | Microsoft Docs
description: Informace o ručním připojení k relaci spolupráce v aplikaci Visual Studio Live Share.
ms.custom: ''
ms.date: 03/22/2018
ms.reviewer: ''
ms.suite: ''
ms.topic: reference
author: chuxel
ms.author: clantz
manager: AmandaSilver
ms.workload:
- liveshare
ms.openlocfilehash: 1057c6276302fb0df682798dd06684b4835c051e
ms.sourcegitcommit: c6ef4e5a9aec4f682718819c58efeab599e2781b
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/30/2019
ms.locfileid: "73170114"
---
# <a name="join-a-session-manually"></a>Ruční připojení k relaci

Kromě otevření odkazu v prohlížeči, který se připojí k relaci spolupráce, se můžete ručně připojit vložením odkazu do již běžícího nástroje. To může být užitečné, pokud chcete použít jiný nástroj, než obvykle, nebo pokud máte potíže s tím, že z nějakého důvodu chcete pracovat s odkazy na pozvánky.

Přesné pokyny se liší v rámci sady [Visual Studio](#join-from-visual-studio) a [Visual Studio Code](#join-from-visual-studio-code), takže si pro další informace vyberte nástroj, který chcete použít.

## <a name="join-from-visual-studio-code"></a>Připojit z Visual Studio Code

### <a name="1-sign-in"></a>1. přihlášení

>**Poznámka:** Pokud se chcete připojit k relaci spolupráce jako hosta jen pro čtení, můžete přeskočit přihlášení. Budete mít přístup k zobrazení a navigaci v okolí kódu, který je sdílený, ale nebude možné provádět úpravy.

![Informační zpráva s výzvou k přihlášení pomocí webového prohlížeče](../media/vscode-sign-in-toast.png)

Aby bylo možné spolupracovat, budete se muset Visual Studio Live Share přihlásit, aby všichni znali, kdo máte. **Klikněte** na položku Live share na stavovém řádku nebo stiskněte **kombinaci kláves CTRL + SHIFT + P/Cmd + Shift + P** a vyberte příkaz Live Share: přihlásit se pomocí prohlížeče.

![Tlačítko pro přihlášení VS Code](../media/vscode-sign-in-button.png)

Prohlížeč se spustí, když se zobrazí oznámení, že se zobrazí výzva k přihlášení. Dokončete proces přihlášení v prohlížeči a po dokončení jednoduše zavřete prohlížeč.

Pokud dochází k problémům s VS Code neúspěšném přihlášením, klikněte na odkaz "máte potíže" na obrazovce úspěšné v prohlížeči a postupujte podle pokynů. Další tipy najdete v [řešení potíží](../troubleshooting.md#sign-in) .

### <a name="2-use-the-join-command"></a>2. použijte příkaz JOIN.

Otevřete Live Share Viewlet na řádku VS Code aktivity a vyberte "připojit se k relaci pro spolupráci...". ikona nebo položka.

![Ikona připojení Viewlet](../media/vscode-join-viewlet.png)

>**Poznámka:** Pokud se připojujete jako host jen pro čtení, budete vyzváni k zadání zobrazovaného názvu, který pomůže účastníkům v relaci identifikovat.

### <a name="3-paste-the-invite-link"></a>3. Vložte odkaz pro pozvání.

Vložte adresu URL pozvánky, kterou jste poslali, a potvrďte akci ENTER.

A je to! V tuto chvíli byste měli být připojeni k relaci spolupráce.

## <a name="join-from-visual-studio"></a>Připojení ze sady Visual Studio

### <a name="1-sign-in"></a>1. přihlášení

Po instalaci spusťte aplikaci Visual Studio a přihlaste se, pokud jste to ještě neučinili. Pokud potřebujete použít jiné přihlášení pro aplikaci Visual Studio, než je váš [účet přizpůsobení](https://docs.microsoft.com/en-us/visualstudio/ide/signing-in-to-visual-studio), v nabídce **nástroje &gt; možnosti &gt; Live Share &gt; uživatelský účet**.

![VS – přihlášení](../media/vs-sign-in-button.png)

Pořád máte problémy? Viz [Poradce při potížích](../troubleshooting.md#sign-in).

### <a name="2-use-the-join-command"></a>2. použijte příkaz JOIN.

Stačí přejít na **soubor > připojit se k relaci spolupráce**.

![Nabídka VS JOIN](../media/vs-join.png)

### <a name="3-paste-the-invite-link"></a>3. Vložte odkaz pro pozvání.

Vložte adresu URL pozvánky, kterou jste poslali, a potvrďte akci ENTER.

A je to! V tuto chvíli byste měli být připojeni k relaci spolupráce.

## <a name="see-also"></a>Viz také:

Rychlý start

- [Rychlý Start: sdílení prvního projektu](../quickstart/share.md)
- [Rychlý Start: připojení první relace](../quickstart/join.md)

Postupy

- [Postupy: spolupráce pomocí Visual Studio Code](../how-to-guides/vscode.md)
- [Postupy: spolupráce pomocí sady Visual Studio](../how-to-guides/vs.md)
- [Postupy: poskytnutí zpětné vazby](../support.md)

Odkaz

- [Požadavky na připojení pro Live Share](connectivity.md)
- [Funkce zabezpečení Live Share](security.md)
- [Podrobnosti o instalaci systému Linux](linux.md)
- [Podpora jazyků a platforem](platform-support.md)
- [Podpora rozšíření](extensions.md)

Máte potíže? Podívejte se na článek o [odstraňování potíží](../troubleshooting.md) nebo nám [pošlete svůj názor](../support.md).
