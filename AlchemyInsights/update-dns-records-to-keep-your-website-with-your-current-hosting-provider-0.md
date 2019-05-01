---
title: Uppdatera DNS-poster för att behålla din webbplats hos ditt nuvarande webbhotell
ms.author: pebaum
author: pebaum
manager: mnirkhe
ms.date: 5/2/2018
ms.audience: Admin
ms.topic: article
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
ms.collection: Adm_O365
ms.custom: ''
ms.assetid: 48251355-7383-4fdc-a1e1-9dc2c85a8d29
ms.openlocfilehash: f2cdb319e56b82c09b7a9856c81a45e69dee6759
ms.sourcegitcommit: 9d78905c512192ffc4675468abd2efc5f2e4baf4
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32423741"
---
# <a name="update-dns-records-to-keep-your-website-with-your-current-hosting-provider"></a><span data-ttu-id="4da03-102">Uppdatera DNS-poster för att behålla din webbplats hos ditt nuvarande webbhotell</span><span class="sxs-lookup"><span data-stu-id="4da03-102">Update DNS records to keep your website with your current hosting provider</span></span>

1. <span data-ttu-id="4da03-103">På sidan [Domäner](https://portal.office.com/adminportal/home#/Domains), i listan över domäner, väljer du den domän du använder för webbplatsen och väljer sedan **DNS-inställningar** i hanteringsfönstret.</span><span class="sxs-lookup"><span data-stu-id="4da03-103">On the [Domains](https://portal.office.com/adminportal/home#/Domains) page, in the list of domains, select the domain you're using for your website, and then select **DNS settings** in the management pane.</span></span> 
    
2. <span data-ttu-id="4da03-104">Välj **+ Ny anpassad post** och ange följande:</span><span class="sxs-lookup"><span data-stu-id="4da03-104">Select **+ New custom record** and enter the following:</span></span> 
    
  - <span data-ttu-id="4da03-105">Ange följande för **DNS-typ**: **A (adress)**</span><span class="sxs-lookup"><span data-stu-id="4da03-105">For **DNS type** enter: **A (Address)**</span></span>
    
  - <span data-ttu-id="4da03-106">I **Värdnamn eller alias** skriver du in **@**</span><span class="sxs-lookup"><span data-stu-id="4da03-106">For **Host name or Alias**, type the following: **@**</span></span>
    
  - <span data-ttu-id="4da03-107">I **IP-adress** skriver du in den statiska IP-adress där webbplatsen finns för närvarande (till exempel 172.16.140.1).</span><span class="sxs-lookup"><span data-stu-id="4da03-107">For **IP Address**, type the static IP address for your website where it's currently hosted (for example, 172.16.140.1).</span></span> 
    
    <span data-ttu-id="4da03-p101">Det måste vara en  *statisk*  IP-adress för webbplatsen, inte en  *dynamisk*  IP-adress.Kontrollera med webbplatsen som är värd för din webbplats för att se till att du kan få en statisk IP-adress till din offentliga webbplats.</span><span class="sxs-lookup"><span data-stu-id="4da03-p101">This must be a  *static*  IP address for the website, not a  *dynamic*  IP address. Check with site where your website is hosted to make sure you can get a static IP address for your public website.</span></span> 
    
3. <span data-ttu-id="4da03-110">Välj **Spara**.</span><span class="sxs-lookup"><span data-stu-id="4da03-110">Select **Save**.</span></span> 
    
<span data-ttu-id="4da03-111">Du kan dessutom skapa en CNAME-post för att kunderna lättare ska kunna hitta till webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="4da03-111">In addition, you can create a CNAME record to help customers find your website.</span></span>
  
1. <span data-ttu-id="4da03-112">Välj **+ Ny anpassad post** och ange följande:</span><span class="sxs-lookup"><span data-stu-id="4da03-112">Select **+ New custom record** and enter the following:</span></span> 
    
  - <span data-ttu-id="4da03-113">Ange följande för **DNS-typ**: **CNAME (alias)**</span><span class="sxs-lookup"><span data-stu-id="4da03-113">For **DNS type** enter: **CNAME (Alias)**</span></span>
    
  - <span data-ttu-id="4da03-114">I **Värdnamn eller alias** skriver du in **www**</span><span class="sxs-lookup"><span data-stu-id="4da03-114">For **Host name or Alias**, type the following: **www**</span></span>
    
  - <span data-ttu-id="4da03-115">I **Pekar på adress** skriver du in det fullständiga domännamnet (FQDN) för webbplatsen (till exempel contoso.com).</span><span class="sxs-lookup"><span data-stu-id="4da03-115">For **Points to address**, type the fully qualified domain name (FQDN) for your website (for example, contoso.com).</span></span> 
    
2. <span data-ttu-id="4da03-116">Välj **Spara**.</span><span class="sxs-lookup"><span data-stu-id="4da03-116">Select **Save**.</span></span> 
    
