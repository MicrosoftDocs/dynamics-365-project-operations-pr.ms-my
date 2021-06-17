---
title: Mengapakah saya tidak dapat memadamkan rekod daripada entiti aktual?
description: Topik ini memberikan maklumat tentang sebab anda tidak boleh merekod daripada entiti aktual.
author: JPBurrows
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
ms.openlocfilehash: 434be93cedb4772616b1e6d5cbe15fc715eed19a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993112"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="25df4-103">Mengapakah saya tidak dapat memadamkan rekod daripada entiti Aktual?</span><span class="sxs-lookup"><span data-stu-id="25df4-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="25df4-104">Project Service Automation (PSA) tidak membenarkan anda memadam aktual kerana mereka berfungsi sebagai sumber kebenaran untuk transaksi yang mempunyai implikasi kewangan kepada sistem hiliran, seperti lejar am.</span><span class="sxs-lookup"><span data-stu-id="25df4-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="25df4-105">Jika aktual boleh dipadamkan, integriti transaksi pelaporan kewangan boleh dipersoalkan.</span><span class="sxs-lookup"><span data-stu-id="25df4-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="25df4-106">Untuk mewujudkan jejak audit, pelanggan hendaklah menggunakan jurnal untuk mencipta transaksi pampasan.</span><span class="sxs-lookup"><span data-stu-id="25df4-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]