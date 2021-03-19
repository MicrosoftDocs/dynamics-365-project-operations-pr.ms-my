---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 25, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Kemas kini Project Service Automation Keluaran 25, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 30822ec64b31e110202a587dd941bdff60116712
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280454"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="b81ee-103">Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 25, V3</span><span class="sxs-lookup"><span data-stu-id="b81ee-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b81ee-104">Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b81ee-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="b81ee-105">Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan.</span><span class="sxs-lookup"><span data-stu-id="b81ee-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b81ee-106">Keluaran ini serasi dengan Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="b81ee-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b81ee-107">Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini.</span><span class="sxs-lookup"><span data-stu-id="b81ee-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="b81ee-108">Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="b81ee-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b81ee-109">Topik ini menyenaraikan ciri dan pembetulan yang baharu atau ditukar untuk Project Service Automation V3, Kemas Kini Keluaran 25. Versi ini mempunyai nombor binaan V 3.10.43.76 dan secara umumnya tersedia melalui kemas kini dengan sendiri pada Oktober 2020.</span><span class="sxs-lookup"><span data-stu-id="b81ee-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="b81ee-110">Keluaran Kemas kini 25</span><span class="sxs-lookup"><span data-stu-id="b81ee-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b81ee-111">Pembetulan pepijat</span><span class="sxs-lookup"><span data-stu-id="b81ee-111">Bug fixes</span></span>

<span data-ttu-id="b81ee-112">**Masa dan Perbelanjaan**</span><span class="sxs-lookup"><span data-stu-id="b81ee-112">**Time and Expense**</span></span>

<span data-ttu-id="b81ee-113">Isu berikut telah dibetulkan:</span><span class="sxs-lookup"><span data-stu-id="b81ee-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="b81ee-114">Carta entri masa menunjukkan data tambahan berdasarkan terlalu besar tempoh masa yang diambil.</span><span class="sxs-lookup"><span data-stu-id="b81ee-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="b81ee-115">**Pengurusan Sumber**</span><span class="sxs-lookup"><span data-stu-id="b81ee-115">**Resource Management**</span></span>

<span data-ttu-id="b81ee-116">Isu berikut telah dibetulkan:</span><span class="sxs-lookup"><span data-stu-id="b81ee-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="b81ee-117">Menambahkan kod Package Deployer untuk melangkau import tampalan Universal Resource Scheduling jika tampalan versi lebih tinggi telah wujud.</span><span class="sxs-lookup"><span data-stu-id="b81ee-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="b81ee-118">**Pengurusan Projek**</span><span class="sxs-lookup"><span data-stu-id="b81ee-118">**Project Management**</span></span>

<span data-ttu-id="b81ee-119">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="b81ee-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="b81ee-120">Percanggahan pembundaran dan kadar pertukaran yang dibetulkan menyebabkan kos dirancang tidak betul dalam grid penjejakan projek.</span><span class="sxs-lookup"><span data-stu-id="b81ee-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="b81ee-121">Sokong keupayaan untuk memaparkan dua atau beberapa grid yang bertindak balas pada borang **Projek**.</span><span class="sxs-lookup"><span data-stu-id="b81ee-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="b81ee-122">Berikan pengesahan bagi menyelesaikan keupayaan untuk menugaskan tugas melepasi tarikh tamat kalendar, yang menyebabkan penugasan sumber gagal.</span><span class="sxs-lookup"><span data-stu-id="b81ee-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="b81ee-123">Pengendalian ralat yang ditambah baik untuk menangani Pengecualian Rujukan Nol yang dijana daripada berikut:</span><span class="sxs-lookup"><span data-stu-id="b81ee-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="b81ee-124">Pasang masuk **PreValidateProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="b81ee-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="b81ee-125">**PreValidateProjectTaskCreate** apabila tugas projek dicipta tanpa projek berkaitan</span><span class="sxs-lookup"><span data-stu-id="b81ee-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="b81ee-126">Pasang masuk **PreValidateProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="b81ee-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="b81ee-127">Pasang masuk **PreValidateProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="b81ee-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="b81ee-128">Pasang masuk **PreValidateProjectTaskDelete**</span><span class="sxs-lookup"><span data-stu-id="b81ee-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="b81ee-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="b81ee-129">**Sales**</span></span>

<span data-ttu-id="b81ee-130">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="b81ee-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="b81ee-131">Pengendalian ralat yang ditambah baik untuk menangani Pengecualian Rujukan Nol yang dijana daripada **Projek Salinan: Anggaran Pengurusan HelperResource**.</span><span class="sxs-lookup"><span data-stu-id="b81ee-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="b81ee-132">**Tidak bersedia diinvois** pada **Tunggakan Pengebilan Masa dan Bahan** tidak menjelaskan status pengebilan.</span><span class="sxs-lookup"><span data-stu-id="b81ee-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="b81ee-133">Membetulkan butang **Harga** yang tersalah label pada tab **Harga Peranan** dan **Item Katalog**.</span><span class="sxs-lookup"><span data-stu-id="b81ee-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]