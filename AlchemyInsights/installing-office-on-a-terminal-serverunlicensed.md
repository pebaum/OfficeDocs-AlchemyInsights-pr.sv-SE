---
title: Installera office på en Terminal Server - olicensierade
ms.author: pebaum
author: pebaum
ms.date: 12/17/2018
ms.audience: ITPro
ms.topic: article
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
ms.assetid: b1074430-489e-4d49-bfe4-3d8783d8073c
ms.openlocfilehash: 971edd9c064b448446ba16361e99df4a2291c14f
ms.sourcegitcommit: 9d78905c512192ffc4675468abd2efc5f2e4baf4
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32410140"
---
# <a name="installing-office-on-a-terminal-server"></a><span data-ttu-id="5a9e4-102">Installera Office på en Terminal-Server</span><span class="sxs-lookup"><span data-stu-id="5a9e4-102">Installing Office on a Terminal Server</span></span>

<span data-ttu-id="5a9e4-103">För distribution av Office 365 ProPlus på en Windows-Server med hjälp av Remote Desktop Services (RDS), tidigare kallad Terminal Services:</span><span class="sxs-lookup"><span data-stu-id="5a9e4-103">For deploying Office 365 ProPlus on a Windows Server using Remote Desktop Services (RDS), formerly named Terminal Services:</span></span>
  
- <span data-ttu-id="5a9e4-104">Du måste ha en Office 365-plan som innehåller Office 365 ProPlus, till exempel Office 365 Enterprise E3 eller Enterprise E5.</span><span class="sxs-lookup"><span data-stu-id="5a9e4-104">You must have an Office 365 plan that includes Office 365 ProPlus, such as Office 365 Enterprise E3 or Enterprise E5.</span></span> <span data-ttu-id="5a9e4-105">Ta inte med Office 365 ProPlus Office 365 Business och Office 365 Business Premium planer.</span><span class="sxs-lookup"><span data-stu-id="5a9e4-105">The Office 365 Business and Office 365 Business Premium plans do not include Office 365 ProPlus.</span></span>
    
- <span data-ttu-id="5a9e4-106">Du måste aktivera [delad dator](https://docs.microsoft.com/DeployOffice/overview-of-shared-computer-activation-for-office-365-proplus).</span><span class="sxs-lookup"><span data-stu-id="5a9e4-106">You need to enable [shared computer activation](https://docs.microsoft.com/DeployOffice/overview-of-shared-computer-activation-for-office-365-proplus).</span></span>
    
<span data-ttu-id="5a9e4-107">Om du vill installera Office 365 ProPlus på klientåtkomstlicenser från Office 365-portalen \*\* *som använder standardinställningarna för installationen* \*\*, gör du så här:</span><span class="sxs-lookup"><span data-stu-id="5a9e4-107">If you want to install Office 365 ProPlus on RDS from the Office 365 portal, \*\* *which uses default installation settings* \*\*, follow these steps:</span></span> 
  
1. <span data-ttu-id="5a9e4-108">Kontrollera vilken Office 365-plan du har.</span><span class="sxs-lookup"><span data-stu-id="5a9e4-108">Check what Office 365 plan you have.</span></span> [<span data-ttu-id="5a9e4-109">Lär dig hur</span><span class="sxs-lookup"><span data-stu-id="5a9e4-109">Learn how</span></span>](https://docs.microsoft.com/office365/admin/admin-overview/what-subscription-do-i-have)
    
2. <span data-ttu-id="5a9e4-110">Om det behövs, växla till en annan Office 365-plan.</span><span class="sxs-lookup"><span data-stu-id="5a9e4-110">If necessary, switch to a different Office 365 plan.</span></span> [<span data-ttu-id="5a9e4-111">Lär dig hur</span><span class="sxs-lookup"><span data-stu-id="5a9e4-111">Learn how</span></span>](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/switch-to-a-different-plan)
    
3. <span data-ttu-id="5a9e4-112">Om Office har installerats på RDS-server med hjälp av andra Office 365-planer, avinstallera den.</span><span class="sxs-lookup"><span data-stu-id="5a9e4-112">If Office is already installed on the RDS server using any other Office 365 plans, uninstall it.</span></span> <span data-ttu-id="5a9e4-113">Till exempel Gå till Kontrollpanelen genom att \> avinstallera ett program.</span><span class="sxs-lookup"><span data-stu-id="5a9e4-113">For example, by going to Control Panel \> Uninstall a program.</span></span> <span data-ttu-id="5a9e4-114">Avinstallera med hjälp av [Microsoft Support och återställning assistenten](https://aka.ms/SARA-OfficeUninstall-Alchemy) om du kör till problem.</span><span class="sxs-lookup"><span data-stu-id="5a9e4-114">Uninstall using [Microsoft Support and Recovery Assistant](https://aka.ms/SARA-OfficeUninstall-Alchemy) if you're running into issues.</span></span> 
    
4. <span data-ttu-id="5a9e4-115">Logga in på Office 365-portalen med ditt administratörskonto och [installera Office 365 ProPlus](https://portal.office.com/OLS/MySoftware.aspx)på RDS-server.</span><span class="sxs-lookup"><span data-stu-id="5a9e4-115">On the RDS server, sign in to the Office 365 portal with your administrator account and [install Office 365 ProPlus](https://portal.office.com/OLS/MySoftware.aspx).</span></span>
    
5. <span data-ttu-id="5a9e4-116">När Office har installerats \*\* *inte öppna eller logga in* \*\* för alla Office-program.</span><span class="sxs-lookup"><span data-stu-id="5a9e4-116">After Office is installed, \*\* *don't open or sign in* \*\* to any Office applications.</span></span> 
    
6. <span data-ttu-id="5a9e4-117">Aktivera delade aktivering på RDS-server genom att redigera registret så här:</span><span class="sxs-lookup"><span data-stu-id="5a9e4-117">On the RDS server, enable shared computer activation by editing the registry by following these steps:</span></span>
    
1. <span data-ttu-id="5a9e4-118">Högerklicka på Windows-knappen i det nedre vänstra hörnet av skärmen och välj kör.</span><span class="sxs-lookup"><span data-stu-id="5a9e4-118">Right-click the Windows button in the lower left-hand corner of your screen and select Run.</span></span> <span data-ttu-id="5a9e4-119">Skriv **regedit**i rutan Öppna och klicka sedan på OK.</span><span class="sxs-lookup"><span data-stu-id="5a9e4-119">In the Open box, type **regedit**, and then select OK.</span></span> 
    
2. <span data-ttu-id="5a9e4-120">Välj Ja när du uppmanas att tillåta Registereditorn att göra ändringar i din enhet.</span><span class="sxs-lookup"><span data-stu-id="5a9e4-120">Select Yes when prompted to allow Registry Editor to make changes to your device.</span></span>
    
3. <span data-ttu-id="5a9e4-121">I Registereditorn kan du lägga till ett strängvärde av **SharedComputerLicensing** med inställningen 1 under HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft \Office\ClickToRun\Configuration.</span><span class="sxs-lookup"><span data-stu-id="5a9e4-121">In the Registry Editor, add a string value of **SharedComputerLicensing** with a setting of 1 under HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft \Office\ClickToRun\Configuration.</span></span> 
    
7. <span data-ttu-id="5a9e4-122">På RDS-server \*\* *Logga in som en användare* \*\* och [Kontrollera att delade aktivering är aktiverat för Office 365 ProPlus](https://docs.microsoft.com/DeployOffice/troubleshoot-issues-with-shared-computer-activation-for-office-365-proplus#verify-that-activation-for-office-365-proplus-succeeded).</span><span class="sxs-lookup"><span data-stu-id="5a9e4-122">On the RDS server, \*\* *sign in as an end user* \*\* and [verify that shared computer activation is enabled for Office 365 ProPlus](https://docs.microsoft.com/DeployOffice/troubleshoot-issues-with-shared-computer-activation-for-office-365-proplus#verify-that-activation-for-office-365-proplus-succeeded).</span></span>
    
<span data-ttu-id="5a9e4-123">Mer information om förutsättningar, instruktioner och riktlinjer för anpassade installationer med hjälp av verktyget Office Deployment finns i [Distribuera Office 365 ProPlus med hjälp av Remote Desktop Services](https://docs.microsoft.com/DeployOffice/deploy-office-365-proplus-by-using-remote-desktop-services).</span><span class="sxs-lookup"><span data-stu-id="5a9e4-123">For more details on prerequisites, setup instructions and guidance on customized installations by using the Office Deployment Tool, please see [Deploy Office 365 ProPlus by using Remote Desktop Services](https://docs.microsoft.com/DeployOffice/deploy-office-365-proplus-by-using-remote-desktop-services).</span></span>
  
<span data-ttu-id="5a9e4-124">Åtgärda fel som är relaterade till delade aktivering finns i [Felsöka problem med delade aktivering för Office 365 ProPlus](https://docs.microsoft.com/DeployOffice/troubleshoot-issues-with-shared-computer-activation-for-office-365-proplus).</span><span class="sxs-lookup"><span data-stu-id="5a9e4-124">To fix errors related to shared computer activation, please see [Troubleshoot issues with shared computer activation for Office 365 ProPlus](https://docs.microsoft.com/DeployOffice/troubleshoot-issues-with-shared-computer-activation-for-office-365-proplus).</span></span>
  
