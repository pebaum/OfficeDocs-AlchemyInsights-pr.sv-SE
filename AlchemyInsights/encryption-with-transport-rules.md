---
title: Kryptering med transportregler
ms.author: pebaum
author: pebaum
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Priority
ms.collection: Adm_O365
ms.custom:
- "9002635"
- "5154"
ms.openlocfilehash: 3f16c7e7be99a50cd57f47ea2801b3022c4aec95
ms.sourcegitcommit: 07725fcaf073f0ac145f98653b989afdb34c5ad0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/28/2020
ms.locfileid: "43915287"
---
# <a name="encryption-with-transport-rules"></a>Kryptering med transportregler

I [Administrationscenter för Exchange](https://go.microsoft.com/fwlink/p/?linkid=834822) (EAC) kan du använda OME-funktioner (Office Message Encryption) i reglerna för e-postflöde för att initiera meddelandekryptering. Välj **Tillämpa meddelandekryptering och behörighetsskydd för Office 365** i transportregelns villkor.

- Mer information finns i [Definiera regeln för e-postflöde för att kryptera](https://docs.microsoft.com/microsoft-365/compliance/define-mail-flow-rules-to-encrypt-email).

- I PowerShell använder du [cmdleten New-TransportRule](https://docs.microsoft.com/microsoft-365/compliance/define-mail-flow-rules-to-encrypt-email?view=o365-worldwide#use-exchange-online-powershell-to-create-a-mail-flow-rule-for-encrypting-email-messages-without-the-new-ome-capabilities) och anger parametern *ApplyOME* till $true.
