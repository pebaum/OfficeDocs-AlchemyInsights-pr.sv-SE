---
title: Åtgärda Office-appar Tyvärr har vi ett meddelande om tillfälliga serverproblem
ms.author: pebaum
author: pebaum
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
ms.collection: Adm_O365
ms.custom:
- "3420"
- "9001430"
ms.openlocfilehash: a1ac62f3587e318d563cfea1df8db23b720358a6
ms.sourcegitcommit: 631cbb5f03e5371f0995e976536d24e9d13746c3
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/22/2020
ms.locfileid: "43764135"
---
# <a name="fixing-the-office-apps-sorry-we-are-having-temporary-server-issues-message"></a>Åtgärda meddelandet "Tyvärr, vi har tillfälliga serverproblem"

Om du får det här meddelandet kan du prova följande:

1. Kontrollera brandväggen, antivirusprogrammet och proxyinställningarna för att bekräfta att de inte blockerar Internetåtkomst till Office-appar. Se [webbadresser och IP-adressintervall](https://docs.microsoft.com/office365/enterprise/urls-and-ip-address-ranges).

2. Gå till > **Startkörning**och skriv sedan **services.msc**. **Start** Kontrollera att alla följande tjänster körs:
    - Automatisk installation av nätverksanslutna enheter
    - Tjänsten Nätverkslista
    - Medvetenhet om nätverksplats
    - Windows-händelselogg

Om en av dessa tjänster inte körs försöker du starta den. Om du har problem med att starta tjänsten kör du följande kommando genom att öppna en kommandotolk med förhöjda behörigheter:

**sfc /scannow**

När det här kommandot är klart startar du om datorn.

Detaljerad information finns i ["Tyvärr, vi kan inte ansluta till ditt konto. Försök igen senare" fel när du aktiverar](https://docs.microsoft.com/office/troubleshoot/activation-installation/issue-when-activate-office-from-office-365).