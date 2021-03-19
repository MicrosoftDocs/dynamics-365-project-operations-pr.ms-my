---
title: Mengapakah saya tidak dapat memadamkan rekod daripada entiti aktual?
description: Topik ini memberikan maklumat tentang sebab anda tidak boleh merekod daripada entiti aktual.
author: JPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e3122c5d9495b3ff9a683f477e719ce0c228a84d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286079"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="3498c-103">Mengapakah saya tidak dapat memadamkan rekod daripada entiti Aktual?</span><span class="sxs-lookup"><span data-stu-id="3498c-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="3498c-104">Project Service Automation (PSA) tidak membenarkan anda memadam aktual kerana mereka berfungsi sebagai sumber kebenaran untuk transaksi yang mempunyai implikasi kewangan kepada sistem hiliran, seperti lejar am.</span><span class="sxs-lookup"><span data-stu-id="3498c-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="3498c-105">Jika aktual boleh dipadamkan, integriti transaksi pelaporan kewangan boleh dipersoalkan.</span><span class="sxs-lookup"><span data-stu-id="3498c-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="3498c-106">Untuk mewujudkan jejak audit, pelanggan hendaklah menggunakan jurnal untuk mencipta transaksi pampasan.</span><span class="sxs-lookup"><span data-stu-id="3498c-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]