---
title: Profil uživatele – Visual Studio Live Share | Microsoft Docs
description: Přehled toho, jak zobrazit a odebrat Visual Studio Live Share profil uživatele.
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
ms.openlocfilehash: 2f9f496b47db7efe260c1f09a2906c68c07762d5
ms.sourcegitcommit: 6bf13781dc42a2bf51a19312ede37dff98ab33ea
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/26/2020
ms.locfileid: "80295949"
---
<!--
Copyright &copy; Microsoft Corporation
All rights reserved.
Creative Commons Attribution 4.0 License (International): https://creativecommons.org/licenses/by/4.0/legalcode
-->

# <a name="user-profile"></a>Uživatelský profil

Při ověřování pomocí Visual Studio Live Share pro vás vytvoří profil uživatele, který jednoduše umožňuje účastníkům, se kterými spolupracujete, zjistit, kdo jste (například vaši e-mailovou adresu, avatar). V libovolném okamžiku můžete zobrazit informace o profilu, který Live Share uložil vaším jménem, a to tak, že přejdete na jednu z následujících stránek (v závislosti na použitém poskytovateli identity):

- [Účet Microsoft/Azure Active Directory](https://prod.liveshare.vsengsaas.visualstudio.com/auth/identity/microsoft/viewprofile)
- [GitHub](https://prod.liveshare.vsengsaas.visualstudio.com/auth/identity/github/viewprofile)

Tato stránka vás vyzve k přihlášení (za účelem ověření identity) a zobrazí nezpracovaný výstup JSON pro váš profil uživatele.

<img width="500px" src="media/user-profile.png" />

Pokud Visual Studio Live Share pro identitu, ke které jste se přihlásili, není uložený profil, bude vám taky informovat.

<img width="500px" src="media/no-profile.png" />

## <a name="removing-your-profile"></a>Odebírá se Váš profil.

Pokud chcete odebrat svůj uživatelský profil, můžete kliknout na tlačítko `Delete your account` na [stránce profil uživatele](#user-profile). V opačném případě bude Visual Studio Live Share automaticky odstranit profil 30 dní od posledního úspěšného přihlášení. V tomto kontextu se "úspěšné přihlášení" odkazuje na následující (v závislosti na použitém nástroji):

| IDE/Editor | Váš profil uživatele se odstraní 30 dnů od posledního spuštění... |
|-|-|
| Visual Studio | Spusťte novou instanci rozhraní IDE. Aby bylo možné podporovat jednotné přihlašování, Visual Studio Live Share aktualizuje relaci ověřování pokaždé, když otevřete novou instanci aplikace Visual Studio. |
| Visual Studio Code | Dokončete pracovní postup ověřování na základě prohlížeče (například kliknutím na tlačítko `Sign In` nebo spuštěním příkazu `Live Share: Sign in with browser`). Visual Studio Live Share si zapamatuje vaši relaci ověřování na klientovi, aby nedocházelo k tomu, že se přihlašujete pokaždé, když budete sdílet. Platnost této relace však vyprší po 30 dnech a nikdy se automaticky neaktualizuje, dokud se znovu nebudete přihlašovat přes prohlížeč. |

## <a name="see-also"></a>Viz také

- [Podpora jazyků a platforem](reference/platform-support.md)
- [Požadavky na připojení pro Live Share](reference/connectivity.md)
- [Funkce zabezpečení Live Share](reference/security.md)
- [Všechny hlavní chyby, žádosti o funkce a omezení](https://aka.ms/vsls-issues)
- [Všechny požadavky a omezení funkcí](https://aka.ms/vsls-feature-requests)

Máte potíže? Podívejte se na článek o [odstraňování potíží](troubleshooting.md) nebo nám [pošlete svůj názor](support.md).
