---
title: Profil uživatele – Visual Studio Live sdílenou složku | Dokumentace Microsoftu
description: Přehled o tom, jak zobrazit a odebrat profil uživatele Visual Studio Live Share.
ms.custom: ''
ms.date: 05/222/2018
ms.reviewer: ''
ms.suite: ''
ms.topic: reference
author: lostintangent
ms.author: joncart
manager: AmandaSilver
ms.workload:
- liveshare
ms.openlocfilehash: 38fb6fada1030bddac8f3437f19f0ae259f5626e
ms.sourcegitcommit: 100fce9b9bbcd7e6f68d40659bd2760e9537de37
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/29/2019
ms.locfileid: "58640026"
---
<!--
Copyright © Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="user-profile"></a>Uživatelský profil

Při ověřování pomocí Visual Studio Live Share vytvoří profil uživatele za vás, která umožňuje všechny účastníky spolupráce s kým se (například e-mailovou adresu, miniatura). V daném okamžiku můžete zobrazit informace o profilu, která uložena Live Share za vás, tak, že přejdete na jednu z následující stránky (v závislosti na poskytovateli identity, které jste použili):

- [Účet Microsoft / Azure Active Directory](https://insiders.liveshare.vsengsaas.visualstudio.com/auth/identity/microsoft/viewprofile)
- [GitHub](https://insiders.liveshare.vsengsaas.visualstudio.com/auth/identity/github/viewprofile)

Na stránce se vás vyzve k přihlášení k ověření vaší identity a pak zobrazí nezpracovaného výstupu JSON pro svůj profil uživatele.

<img width="500px" src="media/user-profile.png" />

Pokud Visual Studio Live Share nemá aktuálně profilu uložená pro identitu, kterou jste přihlášení, pak se vám dá vědět, který také.

<img width="500px" src="media/no-profile.png" />

## <a name="removing-your-profile"></a>Odebrání profilu

Pokud chcete odebrat profil uživatele, můžete kliknout na odkaz s názvem `Click here to get your data removed from our systems` na [stránku profilu uživatele](#user-profile). Alternativně můžete navštíví některý z následujících stránkách přímo (v závislosti na poskytovateli identity, které jste použili):

- [Účet Microsoft / Azure Active Directory](https://insiders.liveshare.vsengsaas.visualstudio.com/auth/identity/microsoft/deleteme)
- [GitHub](https://insiders.liveshare.vsengsaas.visualstudio.com/auth/identity/github/deleteme)

V opačném případě Visual Studio Live Share automaticky odstraní váš profil 30 dnů po posledním úspěšném přihlášení. V tomto kontextu že "úspěšné přihlášení" odkazuje na následující (v závislosti na nástroj, který používáte):

| Rozhraní IDE nebo editoru | Profil uživatele odstraní 30 dní od posledního... |
|-|-|
| Visual Studio | Spusťte novou instanci integrovaného vývojového prostředí. Aby bylo možné podporovat jednotné přihlašování, Visual Studio Live Share aktualizuje relaci ověřování při každém otevření nové instanci sady Visual Studio. |
| Visual Studio Code | Dokončit pracovní postup ověřování založené na prohlížeči (například kliknutí `Sign In` tlačítko nebo spuštění `Live Share: Sign in with browser` příkaz). Visual Studio Live Share si budou pamatovat vaše relace ověřování na straně klienta, a tím vám znemožnit museli přihlásit pokaždé, když sdílíte. Ale relace vyprší po 30 dnech a je nikdy automaticky aktualizovat, dokud je explicitní pomocí prohlížeče znovu přihlásit. |

## <a name="see-also"></a>Viz také:

- [Podpora jazyků a platforem](reference/platform-support.md)
- [Požadavky na připojení pro Live Share](reference/connectivity.md)
- [Funkce zabezpečení Live Share](reference/security.md)
- [Hlavní chyby, žádosti o funkce a omezení](https://aka.ms/vsls-issues)
- [Všechny žádosti o funkce a omezení](https://aka.ms/vsls-feature-requests)

Máte potíže? Podívejte se na článek o [odstraňování potíží](troubleshooting.md) nebo nám [pošlete svůj názor](support.md).
