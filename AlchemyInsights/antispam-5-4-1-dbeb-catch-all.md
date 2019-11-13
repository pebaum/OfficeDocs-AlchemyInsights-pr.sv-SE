---
title: AntiSpam 5.4.1 DBEB catch-all
ms.author: pebaum
author: pebaum
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
ms.collection: Adm_O365
ms.custom:
- "9001209"
- "3167"
ms.openlocfilehash: 4a56cfe74d8940e53a316d3bcc3809e8666c2e37
ms.sourcegitcommit: a8945ab0008f138b2992175b0640e78a505d29e1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/04/2019
ms.locfileid: "37964337"
---
# <a name="fix-delivery-issues-for-error-code-550-541-relay-access-denied"></a>Åtgärda leveransproblem för felkod 550 5.4.1 Relä åtkomst nekad

Det här problemet uppstår när [du kontrollerar om en e-postadress är giltig för att förhindra studsar](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-directory-based-edge-blocking) när du anger Office 365-nätverket. Prova följande:

1. Ta reda på om problemet är specifikt för en hel domän eller en enskild e-postadress:
    - Hela domänen: ibland måste domänen synkroniseras; försök att [ange domänen till intern och sedan tillbaka till auktoritativ](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).
     - En e-postadress: ibland måste adressen synkroniseras; ändra SMTP-proxyadressen och sedan ändra tillbaka den kan hjälpa.
2. Ta reda på om problemet är specifikt för en grupp eller en offentlig mapp. För vissa objekttyper kan objekten behöva skapas manuellt i Azure Active Directory.

Om du behöver ytterligare hjälp, öppna ett supportärende och ange omfattningen av problemet (includidng typ av objekt som du skickar till) så att vi kan hjälpa dig bättre.