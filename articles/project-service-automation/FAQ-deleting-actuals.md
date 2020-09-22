---
title: Mengapakah saya tidak dapat memadamkan rekod daripada entiti aktual?
description: Topik ini memberikan maklumat tentang sebab anda tidak boleh merekod daripada entiti aktual.
author: JPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.prod: Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: ff504c34-7337-474f-89e8-d8afdd1e0a98
ms.author: Jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5817940933c161dccac0fe549fabacbe57e7077a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753859"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="83c61-103">Mengapakah saya tidak dapat memadamkan rekod daripada entiti Aktual?</span><span class="sxs-lookup"><span data-stu-id="83c61-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="83c61-104">Project Service Automation (PSA) tidak membenarkan anda memadam aktual kerana mereka berfungsi sebagai sumber kebenaran untuk transaksi yang mempunyai implikasi kewangan kepada sistem hiliran, seperti lejar am.</span><span class="sxs-lookup"><span data-stu-id="83c61-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="83c61-105">Jika aktual boleh dipadamkan, integriti transaksi pelaporan kewangan boleh dipersoalkan.</span><span class="sxs-lookup"><span data-stu-id="83c61-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="83c61-106">Untuk mewujudkan jejak audit, pelanggan hendaklah menggunakan jurnal untuk mencipta transaksi pampasan.</span><span class="sxs-lookup"><span data-stu-id="83c61-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

