---
title: Åtkomst nekad när du visar ett arbetsflöde
ms.author: kirks
author: Techwriter40
ms.date: 11/27/2018
ms.audience: ITPro
ms.topic: article
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
ms.assetid: 47ceb983-f9a4-4c55-a40c-03d5c3d75dc9
ms.openlocfilehash: 43369c600687d6ac253f70a8535dc2bd0d41687e
ms.sourcegitcommit: 9d78905c512192ffc4675468abd2efc5f2e4baf4
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32389905"
---
# <a name="access-denied-when-viewing-a-workflow"></a><span data-ttu-id="22cc1-102">Åtkomst nekad när du visar ett arbetsflöde</span><span class="sxs-lookup"><span data-stu-id="22cc1-102">Access denied when viewing a Workflow</span></span>

<span data-ttu-id="22cc1-103">Arbetsflöden för SharePoint 2013 som försöker skicka ett e-postmeddelande till en SharePoint-grupp kan misslyckas med felmeddelandet ”åtkomst nekad” om medlemskap i SharePoint-gruppen inte har angetts för alla.</span><span class="sxs-lookup"><span data-stu-id="22cc1-103">SharePoint 2013 Workflows that attempt to send an email to a SharePoint group can fail with an "Access Denied" error message if the membership of the SharePoint group is not set to Everyone.</span></span>
  
 <span data-ttu-id="22cc1-104">**Lös problemet genom att utföra de här stegen:**</span><span class="sxs-lookup"><span data-stu-id="22cc1-104">**To resolve this issue, do these steps:**</span></span>
  
 1. <span data-ttu-id="22cc1-105">Kan alla se medlemmarna i SharePoint-gruppen.</span><span class="sxs-lookup"><span data-stu-id="22cc1-105">Allow everybody to see the members of the SharePoint group.</span></span> 
  
 2. <span data-ttu-id="22cc1-106">Ta bort SharePoint-gruppen från rutan till eller kopia raden i e-postmeddelandet.</span><span class="sxs-lookup"><span data-stu-id="22cc1-106">Remove the SharePoint group from the To or CC line of the email.</span></span> 
  
 3. <span data-ttu-id="22cc1-107">Lägga till användare i till eller kopia uttryckligen rad om medlemskap synligheten inte kan ändras för SharePoint-grupp.</span><span class="sxs-lookup"><span data-stu-id="22cc1-107">Explicitly add the users to the To or CC line if the membership visibility cannot be changed for SharePoint group.</span></span> 
  
<span data-ttu-id="22cc1-108">Om du vill visa finns mer information i [Http-obehörig till /_vti_bin/client.svc/sp.utilities.utility.SendEmail ](https://go.microsoft.com/fwlink/?linkid=2044694&amp;clcid=0x409).</span><span class="sxs-lookup"><span data-stu-id="22cc1-108">To view more details please refer to [HTTP Unauthorized to /_vti_bin/client.svc/sp.utilities.utility.SendEmail ](https://go.microsoft.com/fwlink/?linkid=2044694&amp;clcid=0x409).</span></span>
  
