---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 19, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas kini Project Service Automation 19, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: b9baeca9e79e233c25a6310e426d755b9162bbad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280724"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="0dbae-103">Project Service Automation, Keluaran Kemas kini 19, V3</span><span class="sxs-lookup"><span data-stu-id="0dbae-103">Project Service Automation Update Release 19, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="0dbae-104">Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="0dbae-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="0dbae-105">Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan.</span><span class="sxs-lookup"><span data-stu-id="0dbae-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="0dbae-106">Keluaran ini serasi dengan Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="0dbae-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="0dbae-107">Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini.</span><span class="sxs-lookup"><span data-stu-id="0dbae-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="0dbae-108">Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="0dbae-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="0dbae-109">Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk PSA V3, Keluaran Kemas kini 19.</span><span class="sxs-lookup"><span data-stu-id="0dbae-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="0dbae-110">Versi ini mempunyai nombor binaan V3.10.30.41 dan secara amnya boleh didapati melalui kemas kini sendiri pada Mei 2020.</span><span class="sxs-lookup"><span data-stu-id="0dbae-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="0dbae-111">Keluaran Kemas kini 19</span><span class="sxs-lookup"><span data-stu-id="0dbae-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="0dbae-112">Pembetulan pepijat</span><span class="sxs-lookup"><span data-stu-id="0dbae-112">Bug fixes</span></span>

<span data-ttu-id="0dbae-113">**Masa dan Perbelanjaan**</span><span class="sxs-lookup"><span data-stu-id="0dbae-113">**Time and Expense**</span></span>

<span data-ttu-id="0dbae-114">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="0dbae-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="0dbae-115">Ralat yang diperolehi daripada import kemasukan masa tidak timbul dengan betul.</span><span class="sxs-lookup"><span data-stu-id="0dbae-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="0dbae-116">Grid Entri Masa tidak menyokong tingkah laku medan **Tarikh Sahaja**.</span><span class="sxs-lookup"><span data-stu-id="0dbae-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="0dbae-117">Sumber projek tidak dapat mencipta perbelanjaan dengan projek.</span><span class="sxs-lookup"><span data-stu-id="0dbae-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="0dbae-118">**Pengurusan Projek**</span><span class="sxs-lookup"><span data-stu-id="0dbae-118">**Project Management**</span></span>

<span data-ttu-id="0dbae-119">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="0dbae-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="0dbae-120">Tugas cucu menyebabkan anggaran yang salah tidak betul semasa Pengiraan Siap (EAC).</span><span class="sxs-lookup"><span data-stu-id="0dbae-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="0dbae-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="0dbae-121">**Sales**</span></span>

<span data-ttu-id="0dbae-122">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="0dbae-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="0dbae-123">**Tindakan mengira semula** tidak berfungsi dengan butiran baris kontrak perbelanjaan atau butiran baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="0dbae-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="0dbae-124">**Harga Kemas kini** hilang untuk anggaran perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="0dbae-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="0dbae-125">Pelanggan tidak boleh memilih sebab status kontrak tersuai daripada halaman **Kontrak Projek**.</span><span class="sxs-lookup"><span data-stu-id="0dbae-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="0dbae-126">Pelanggan mengalami prestasi yang diturun taraf apabila mencipta senarai harga tersuai daripada sebut harga.</span><span class="sxs-lookup"><span data-stu-id="0dbae-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="0dbae-127">Pelanggan mengalami ketidakselarasan dengan **unit** lalai pada **Butiran Baris Sebut Harga** dan halaman **Butiran Baris Kontrak**.</span><span class="sxs-lookup"><span data-stu-id="0dbae-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="0dbae-128">Menambah butiran kategori transaksi tidak boleh dikenakan ke baris kontrak bercukai tidak akan menghormati jenis **Pengebilan tidak boleh dituntut** pada kategori transaksi.</span><span class="sxs-lookup"><span data-stu-id="0dbae-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="0dbae-129">Pelanggan tidak boleh menggunakan peranan dan kategori baru yang ditambah pada kontrak yang dicipta sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="0dbae-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="0dbae-130">Pelanggan mengalami prestasi yang diturun taraf yang tidak perlu untuk mendapatkan dalam Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span><span class="sxs-lookup"><span data-stu-id="0dbae-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="0dbae-131">Peranan yang ditetapkan sebagai tidak boleh digunakan dalam senarai **Kategori Sumber** harus ditambah ke tab **Peranan boleh dituntut** sebagai **Tidak tidak boleh dituntut** pada baris kontrak untuk projek.</span><span class="sxs-lookup"><span data-stu-id="0dbae-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="0dbae-132">Pelanggan mungkin mengalami prestasi yang diturun taraf apabila mencipta projek kerana **GetBookableResourceIdFromUser** mendapatkan semua kolum sumber boleh ditempah bukan sekadar ID utama.</span><span class="sxs-lookup"><span data-stu-id="0dbae-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="0dbae-133">Entiti **TransactionType** kehilangan pasang masuk kemas kini pra pengesahan untuk mengelakkan pengguna daripada memasuki **Unit** dan **UnitGroups** yang tidak sah untuk jenis transaksi.</span><span class="sxs-lookup"><span data-stu-id="0dbae-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="0dbae-134">Langkah **Keluarkan** tidak berfungsi untuk import kemasukan masa.</span><span class="sxs-lookup"><span data-stu-id="0dbae-134">The **Remove** step does not work for time entry import.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]