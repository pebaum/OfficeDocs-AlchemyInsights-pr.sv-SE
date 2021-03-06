---
title: Felsöka problem med PST-import
ms.author: pebaum
author: pebaum
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Priority
ms.collection: Adm_O365
ms.custom:
- "1800027"
- "1225"
ms.openlocfilehash: 58fdd509fae5e87bf5ae72db5d8926c4367cdd64
ms.sourcegitcommit: 87aa36e3ff4835efb120a320c5169bfa77199ec4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/01/2020
ms.locfileid: "43991384"
---
# <a name="troubleshooting-pst-import-issues"></a>Felsöka problem med PST-import

- Om du importerar i själva Outlook-klienten kan du läsa [Åtgärda problem med att importera en Outlook .pst-fil](https://support.office.com/article/Fix-problems-importing-an-Outlook-pst-file-2d2e50dc-5c36-4ab2-ab50-f1be733b3d6e).

- Om du använder Import Service och den har fastnat bör du tänka på att varje PST-fil som du laddar upp till Azure Storage-platsen inte ska vara större än 20 GB. PST-filer som är större än 20 GB kan påverka prestandan för PST-importprocessen.

- Om du vill kontrollera status för ett enskilt importjobb kan du använda [Get-MailboxImportRequest -batchname](https://docs.microsoft.com/powershell/module/exchange/mailboxes/get-mailboximportrequest).

- Fullständig information om importtjänsten finns i [översikten över hur du importerar organisationens PST-filer](https://docs.microsoft.com/microsoft-365/compliance/importing-pst-files-to-office-365?view=o365-worldwide).
