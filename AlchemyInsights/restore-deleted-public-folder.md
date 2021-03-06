---
title: Återställa en borttagen gemensam mapp
ms.author: pebaum
author: pebaum
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
ms.collection: Adm_O365
ms.custom:
- "3500007"
- "3488"
ms.openlocfilehash: cd85dd3c0eb14f6e02ac4f912e733468403387aa
ms.sourcegitcommit: 2a9d059262c07c33f9a740b3da4e6e3366b2f925
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/20/2020
ms.locfileid: "42158544"
---
# <a name="restore-a-deleted-public-folder"></a>Återställa en borttagen gemensam mapp

**Så här återställer du borttagna objekt från en gemensam mapp:**

- Se [Du kan inte återställa borttagna objekt från en gemensam mapp som inte skickas i Outlook 2016](https://aka.ms/pfrec).
 
**Så här återställer du en borttagen gemensam mapp (av vilken typ som helst)**: 

- Använd följande KOMMANDOT EXO PowerShell:

    Syntax:

     `$pf=Get-PublicFolder \NON_IPM_SUBTREE\DUMPSTER_ROOT -Recurse  | ?{$_.Name -eq "\<name_of_deleted_public_Folder"};Set-PublicFolder $pf.identity -Path \<path where the folder will be restored>`

    Exempel: Följande kommando återställer undermapp1 och placerar den under \Parent1:

    `$pf=Get-PublicFolder \NON_IPM_SUBTREE\DUMPSTER_ROOT -Recurse | ?{$_.Name -eq "Subfolder1"};Set-PublicFolder $pf.identity -Path \Parent1`

Mer information finns i [Återställa en borttagen gemensam mapp.](https://docs.microsoft.com/exchange/collaboration-exo/public-folders/restore-deleted-public-folder)
