---
title: DLP-regel för kreditkortsnummer fungerar inte
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
ms.date: 11/5/2018
ms.audience: ITPro
ms.topic: article
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
ms.assetid: 30496c79-c8b4-4337-a46d-abed12864209
ms.openlocfilehash: e1d60c493a27efb7f724d57051e21fad5bd0242f
ms.sourcegitcommit: 9d78905c512192ffc4675468abd2efc5f2e4baf4
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32404544"
---
<span data-ttu-id="c85e7-102">Har du problem med **Data förlust Prevention (DLP)** fungerar inte för innehåll som innehåller ett **Kreditkortsnummer** när du använder en DLP känslig informationstyp i O365?</span><span class="sxs-lookup"><span data-stu-id="c85e7-102">Are you having problems with **Data Loss Prevention (DLP)** not working for content containing a **Credit Card Number** when using a DLP sensitive information type in O365?</span></span> <span data-ttu-id="c85e7-103">Om så är fallet, kontrollera innehållet innehåller informationen som krävs för att utlösa den DLP-principen när det utvärderas.</span><span class="sxs-lookup"><span data-stu-id="c85e7-103">If so, make sure your content contains the needed information to trigger the the DLP policy when it is evaluated.</span></span> <span data-ttu-id="c85e7-104">Till exempel ett **kreditkort princip** konfigureras med en konfidensnivå på 85%, följande utvärderas och måste identifieras att utlösa regeln:</span><span class="sxs-lookup"><span data-stu-id="c85e7-104">For example, for a **Credit Card policy** configured with a confidence level of 85%, the following are evaluated and must be detected for the rule to trigger:</span></span> 
  
- <span data-ttu-id="c85e7-105">**[Format:](https://docs.microsoft.com/office365/securitycompliance/what-the-sensitive-information-types-look-for#format-19)** 16 siffror som kan vara formaterad eller oformaterad (dddddddddddddddd) och måste klara Luhn-testet.</span><span class="sxs-lookup"><span data-stu-id="c85e7-105">**[Format:](https://docs.microsoft.com/office365/securitycompliance/what-the-sensitive-information-types-look-for#format-19)** 16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span> 
    
- <span data-ttu-id="c85e7-106">**[Mönster:](https://docs.microsoft.com/office365/securitycompliance/what-the-sensitive-information-types-look-for#pattern-19)** Mycket komplexa och robust mönster som identifierar kort från alla stora varumärken över hela världen, inklusive Visa, Mastercard, Discover-kort, JCB, American Express, presentkort och diner-kort.</span><span class="sxs-lookup"><span data-stu-id="c85e7-106">**[Pattern:](https://docs.microsoft.com/office365/securitycompliance/what-the-sensitive-information-types-look-for#pattern-19)** Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span> 
    
- <span data-ttu-id="c85e7-107">**[Kontrollsumma:](https://docs.microsoft.com/office365/securitycompliance/what-the-sensitive-information-types-look-for#checksum-19)** Ja, Luhn-kontrollsumma</span><span class="sxs-lookup"><span data-stu-id="c85e7-107">**[Checksum:](https://docs.microsoft.com/office365/securitycompliance/what-the-sensitive-information-types-look-for#checksum-19)** Yes, the Luhn checksum</span></span> 
    
- <span data-ttu-id="c85e7-108">**[Definition:](https://docs.microsoft.com/office365/securitycompliance/what-the-sensitive-information-types-look-for#definition-19)** En DLP-princip är 85% säker på att den har upptäckt att den här typen av känslig information om inom ett avstånd av 300 tecken:</span><span class="sxs-lookup"><span data-stu-id="c85e7-108">**[Definition:](https://docs.microsoft.com/office365/securitycompliance/what-the-sensitive-information-types-look-for#definition-19)** A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span> 
    
  - <span data-ttu-id="c85e7-109">Funktionen Func_credit_card returnerar innehåll som matchar mönstret.</span><span class="sxs-lookup"><span data-stu-id="c85e7-109">The function Func_credit_card finds content that matches the pattern.</span></span>
    
  - <span data-ttu-id="c85e7-110">Något av följande är sant:</span><span class="sxs-lookup"><span data-stu-id="c85e7-110">One of the following is true:</span></span> 
    
  - <span data-ttu-id="c85e7-111">Det finns ett nyckelord från Keyword_cc_verification.</span><span class="sxs-lookup"><span data-stu-id="c85e7-111">A keyword from Keyword_cc_verification is found.</span></span>
    
  - <span data-ttu-id="c85e7-112">Ett nyckelord från Keyword_cc_name hittades</span><span class="sxs-lookup"><span data-stu-id="c85e7-112">A keyword from Keyword_cc_name is found</span></span>
    
  - <span data-ttu-id="c85e7-113">Funktionen Func_expiration_date söker efter ett datum i formatet rätt datum.</span><span class="sxs-lookup"><span data-stu-id="c85e7-113">The function Func_expiration_date finds a date in the right date format.</span></span>
    
  - <span data-ttu-id="c85e7-114">Kontrollsumman passerar</span><span class="sxs-lookup"><span data-stu-id="c85e7-114">The checksum passes</span></span>
    
    <span data-ttu-id="c85e7-115">Till exempel initierar i följande exempel principens DLP kreditkort nummer:</span><span class="sxs-lookup"><span data-stu-id="c85e7-115">For example, the following sample would trigger for a DLP Credit Card Number Policy:</span></span>
    
  - <span data-ttu-id="c85e7-116">Visa: 4485 3647 3952 7352</span><span class="sxs-lookup"><span data-stu-id="c85e7-116">Visa: 4485 3647 3952 7352</span></span> 
    
  - <span data-ttu-id="c85e7-117">Förfaller: 2/2009</span><span class="sxs-lookup"><span data-stu-id="c85e7-117">Expires: 2/2009</span></span>
    
<span data-ttu-id="c85e7-118">Mer information om vad som krävs för ett **Kreditkortsnummer** ska identifieras för ditt innehåll finns i följande avsnitt i den här artikeln: [Vad den känsliga informationstyper leta efter kreditkort #](https://docs.microsoft.com/office365/securitycompliance/what-the-sensitive-information-types-look-for#credit-card-number)</span><span class="sxs-lookup"><span data-stu-id="c85e7-118">For more information on what is required for a **Credit Card Number** to be detected for your content, see the following section in this article: [What the Sensitive Information Types look for Credit Card#](https://docs.microsoft.com/office365/securitycompliance/what-the-sensitive-information-types-look-for#credit-card-number)</span></span>
  
<span data-ttu-id="c85e7-119">Med en annan inbyggd känslig information-typ finns i följande artikel för information om vad som krävs för andra typer: [vad den känsliga informationstyper leta efter](https://docs.microsoft.com/office365/securitycompliance/what-the-sensitive-information-types-look-for)</span><span class="sxs-lookup"><span data-stu-id="c85e7-119">Using a different built-in sensitive information type, see the following article for information on what is required for other types: [What the Sensitive Information Types look for](https://docs.microsoft.com/office365/securitycompliance/what-the-sensitive-information-types-look-for)</span></span>
  
