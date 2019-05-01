---
title: 1554 Winsock-fel 10061
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 12/7/2018
ms.audience: ITPro
ms.topic: article
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
ms.custom: 1554
ms.assetid: caecfa19-86c9-4aa4-9c83-b8a974ce60b9
ms.openlocfilehash: 7651effc43cb0c4bc2fbbe5349bb72303943f493
ms.sourcegitcommit: 9d78905c512192ffc4675468abd2efc5f2e4baf4
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32419998"
---
# <a name="winsock-error-10061"></a><span data-ttu-id="1c5bd-102">Winsock-fel 10061</span><span class="sxs-lookup"><span data-stu-id="1c5bd-102">Winsock error 10061</span></span>

<span data-ttu-id="1c5bd-103">Felet innebär att Office 365 gick inte att upprätta en TCP-socket (anslutning) med målvärden.</span><span class="sxs-lookup"><span data-stu-id="1c5bd-103">This error code means that Office 365 couldn't establish a TCP socket (connection) with the target host.</span></span> <span data-ttu-id="1c5bd-104">Den mest troliga orsaken till detta fel är ett problem med konfigurationen av brandväggen.</span><span class="sxs-lookup"><span data-stu-id="1c5bd-104">The most likely cause of this error is a problem with your firewall configuration.</span></span> <span data-ttu-id="1c5bd-105">Åtgärda problemet genom att kontrollera inställningarna:</span><span class="sxs-lookup"><span data-stu-id="1c5bd-105">To fix the problem, check these settings:</span></span>

- <span data-ttu-id="1c5bd-106">Kontrollera konfigurationen av brandväggen med informationen i [Office 365-adresser och IP-adressintervall](https://docs.microsoft.com/office365/enterprise/urls-and-ip-address-ranges)</span><span class="sxs-lookup"><span data-stu-id="1c5bd-106">Verify your firewall configuration with the information in [Office 365 URLs and IP address ranges](https://docs.microsoft.com/office365/enterprise/urls-and-ip-address-ranges)</span></span>

- <span data-ttu-id="1c5bd-107">Om felet är specifikt till Exchange Online skydd (EOP), bör du tidigare anmälts till en ändring till [Exchange Online skydd IP-adresser](https://docs.microsoft.com/office365/SecurityCompliance/eop/exchange-online-protection-ip-addresses).</span><span class="sxs-lookup"><span data-stu-id="1c5bd-107">If the error is specific to Exchange Online Protection (EOP), you should have been previously notified to a change to the [Exchange Online Protection IP addresses](https://docs.microsoft.com/office365/SecurityCompliance/eop/exchange-online-protection-ip-addresses).</span></span>

- <span data-ttu-id="1c5bd-108">Kontrollera att porten inte blockering av Internet Service Provider (ISP).</span><span class="sxs-lookup"><span data-stu-id="1c5bd-108">Verify that your Internet Service Provider (ISP) isn't blocking the port.</span></span>

- <span data-ttu-id="1c5bd-109">Kontrollera smart värd- och måldator-serverinställningarna i kopplingar.</span><span class="sxs-lookup"><span data-stu-id="1c5bd-109">Verify the smart host and target server settings in your connectors.</span></span>

<span data-ttu-id="1c5bd-110">Observera att Office 365 inte blockerar *inkommande* anslutningar på detta sätt.</span><span class="sxs-lookup"><span data-stu-id="1c5bd-110">Note that Office 365 doesn't block *incoming* connections in this manner.</span></span>