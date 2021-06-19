---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 32, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Kemas kini Project Service Automation Keluaran 32, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129677"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="e2f37-103">Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 32, V3</span><span class="sxs-lookup"><span data-stu-id="e2f37-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e2f37-104">Kami amat berbesar hati mengumumkan kemas kini terbaharu untuk apl Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="e2f37-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="e2f37-105">Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan.</span><span class="sxs-lookup"><span data-stu-id="e2f37-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e2f37-106">Kemas kini serasi dengan Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="e2f37-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e2f37-107">Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian dalam talian Pusat Pentadbir untuk Dynamics 365 dan pasang kemas kini.</span><span class="sxs-lookup"><span data-stu-id="e2f37-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="e2f37-108">Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="e2f37-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e2f37-109">Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 32.</span><span class="sxs-lookup"><span data-stu-id="e2f37-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="e2f37-110">Versi ini mempunyai nombor binaan V3.10.53.108 dan secara amnya boleh didapati melalui kemas kini sendiri pada bulan Jun 2021.</span><span class="sxs-lookup"><span data-stu-id="e2f37-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="e2f37-111">Keluaran Kemas kini 32</span><span class="sxs-lookup"><span data-stu-id="e2f37-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e2f37-112">Pembetulan pepijat</span><span class="sxs-lookup"><span data-stu-id="e2f37-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="e2f37-113">Umum</span><span class="sxs-lookup"><span data-stu-id="e2f37-113">General</span></span>

- <span data-ttu-id="e2f37-114">Apabila naik taraf utama gagal, hanya titik masuk aplikasi utama harus disekat, untuk memastikan entiti yang dikongsi masih boleh diakses.</span><span class="sxs-lookup"><span data-stu-id="e2f37-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="e2f37-115">Masa dan Perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="e2f37-115">Time and Expense</span></span>

<span data-ttu-id="e2f37-116">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="e2f37-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="e2f37-117">**TimeEntriesImportFromResourceAssignment** tidak mengekalkan masa mula dan akhir pada hirisan kontur tugasan sumber.</span><span class="sxs-lookup"><span data-stu-id="e2f37-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="e2f37-118">Apabila anda memilih **Emtri Terbuka** pada gris **Entri Masa**, anda mungkin akan dihalang daripada memilih borang lain.</span><span class="sxs-lookup"><span data-stu-id="e2f37-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="e2f37-119">Semasa anda mengimport tugasan ke entri masa, pertanyaan kod pelanggan boleh menjana URL panjang yang gagal pertanyaan.</span><span class="sxs-lookup"><span data-stu-id="e2f37-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="e2f37-120">Dalam grid **Entri Masa**, selepas nilai dipadamkan daripada sel, fokus tidak kekal dalam grid.</span><span class="sxs-lookup"><span data-stu-id="e2f37-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="e2f37-121">Butang **Tolak** telah dialih keluar daripada pandangan **Kelulusan pemprosesan** untuk kelulusan moden.</span><span class="sxs-lookup"><span data-stu-id="e2f37-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="e2f37-122">Kestabilan dan prestasi kelulusan pukal entri masa akan dipengaruhi oleh kunci mati dan kegagalan untuk mengendalikan penyesuaian dengan sewajarnya yang berkaitan dengan entiti **Entri Masa**.</span><span class="sxs-lookup"><span data-stu-id="e2f37-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="e2f37-123">Perancangan Projek</span><span class="sxs-lookup"><span data-stu-id="e2f37-123">Project Planning</span></span>

- <span data-ttu-id="e2f37-124">Pengecualian rujukan nol akan dijana apabila anda mengemas kini projek yang mempunyai nilai nol dalam medan **Unit Berkontrak**.</span><span class="sxs-lookup"><span data-stu-id="e2f37-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="e2f37-125">**Segar Semula Jumlah Projek** mengira baki kos dan baki jualan pada projek secara salah.</span><span class="sxs-lookup"><span data-stu-id="e2f37-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="e2f37-126">Pengiraan penetapan harga yang berlebihan mempengaruhi prestasi yang berkaitan dengan kemas kini pada kontur peruntukan sumber.</span><span class="sxs-lookup"><span data-stu-id="e2f37-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="e2f37-127">Pengurusan Sumber</span><span class="sxs-lookup"><span data-stu-id="e2f37-127">Resource Management</span></span>

<span data-ttu-id="e2f37-128">Isu berikut telah dibetulkan:</span><span class="sxs-lookup"><span data-stu-id="e2f37-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="e2f37-129">Apabila keupayaan kalendar sumber boleh ditempah lebih daripada 1, Project Service Automation mengenal pasti kapasiti sebagai 0 (sifar) secara salah.</span><span class="sxs-lookup"><span data-stu-id="e2f37-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="e2f37-130">Oleh itu, gelung tak terhingga berlaku dalam pandangan jadual.</span><span class="sxs-lookup"><span data-stu-id="e2f37-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="e2f37-131">Jualan</span><span class="sxs-lookup"><span data-stu-id="e2f37-131">Sales</span></span>

<span data-ttu-id="e2f37-132">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="e2f37-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="e2f37-133">Apabila garisan jurnal dicipta yang mempunyai jenis transaksi tersuai, pengecualian rujukan nol berikut berlaku: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="e2f37-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="e2f37-134">Peranan dan kategori yang tidak diaktifkan sebelum sebut harga disalin tidak boleh ditambah ke peranan dan kategori sebut harga yang baru disalin.</span><span class="sxs-lookup"><span data-stu-id="e2f37-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="e2f37-135">Tarikh dokumen dan tarikh perakaunan tidak sejajar dengan tarikh mula yang disediakan pada butiran baris invois yang dicipta secara langsung pada invois draf.</span><span class="sxs-lookup"><span data-stu-id="e2f37-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="e2f37-136">Pengecualian rujukan nol dijana dalam senario yang berkaitan dengan ketidakaktifan peranan dan kategori sebelum sebut harga disalin.</span><span class="sxs-lookup"><span data-stu-id="e2f37-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="e2f37-137">Tindakan **Kemas Kini Harga** pada halaman **Projek** tidak mengemas kini perbelanjaan dan anggaran penting.</span><span class="sxs-lookup"><span data-stu-id="e2f37-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
