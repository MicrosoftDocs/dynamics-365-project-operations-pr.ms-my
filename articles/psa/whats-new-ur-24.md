---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 24, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas kini Project Service Automation 24, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6c8348e65307f63a251f97bf1ea17578e7026da8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081180"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="8fbc1-103">Project Service Automation, Keluaran Kemas kini 24, V3</span><span class="sxs-lookup"><span data-stu-id="8fbc1-103">Project Service Automation Update Release 24, V3</span></span>

<span data-ttu-id="8fbc1-104">Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="8fbc1-105">Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="8fbc1-106">Keluaran ini serasi dengan Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="8fbc1-107">Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="8fbc1-108">Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="8fbc1-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="8fbc1-109">Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 24.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="8fbc1-110">Versi ini mempunyai nombor bina V 3.10.42.43 dan secara amnya boleh didapati melalui kemas kini kendiri pada Oktober 2020.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="8fbc1-111">Keluaran Kemas kini 24</span><span class="sxs-lookup"><span data-stu-id="8fbc1-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="8fbc1-112">Pembetulan pepijat</span><span class="sxs-lookup"><span data-stu-id="8fbc1-112">Bug fixes</span></span>

<span data-ttu-id="8fbc1-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="8fbc1-113">**Sales**</span></span>

<span data-ttu-id="8fbc1-114">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="8fbc1-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="8fbc1-115">Masalah semasa menetapkan senarai harga lalai produk.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="8fbc1-116">Prestasi menang Sebut Harga perlahan disebabkan senarai harga terbenam dan salinan rekod harga peranan.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="8fbc1-117">**Kontrak Projek/Hab Jualan** > **Item Baris Produk/Kuantiti Baris Pesanan** dibundarkan secara automatik kepada integer terdekat.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="8fbc1-118">Tingkatkan kepada kelayakan sistem apabila membaca senarai harga.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="8fbc1-119">Salin medan alamat pelanggan **address1_freighttermscode** dan **address1_shippingmethodcode** kepada Sebut Harga/Pesanan.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="8fbc1-120">**Masa dan Perbelanjaan**</span><span class="sxs-lookup"><span data-stu-id="8fbc1-120">**Time and Expense**</span></span>

<span data-ttu-id="8fbc1-121">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="8fbc1-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="8fbc1-122">**Grid Entri Masa** tidak menyokong tingkah laku masa **Tarikh Sahaja**.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="8fbc1-123">**Entri Masa** tidak disegarkan semula secara automatik.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="8fbc1-124">Segar semula manual diperlukan.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-124">A manual refresh is required.</span></span>
- <span data-ttu-id="8fbc1-125">Tidak dapat mengimport entri masa daripada tugasan apabila terdapat rehat (0 jam) dalam tugasan sumber.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="8fbc1-126">Apabila mencipta entri masa, tetapkan mula sama seperti **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="8fbc1-127">Dayakan semula edit pukal untuk entri masa.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="8fbc1-128">**Pengurusan Sumber**</span><span class="sxs-lookup"><span data-stu-id="8fbc1-128">**Resource Management**</span></span>

<span data-ttu-id="8fbc1-129">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="8fbc1-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="8fbc1-130">Mencuba untuk mengemas kini status tempahan antara hari tanpa keperluan akan membuang pengecualian rujukan yang tidak sah.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="8fbc1-131">Ralat memuatkan **Pandangan Penyesuaian**.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="8fbc1-132">**Pengurusan Projek**</span><span class="sxs-lookup"><span data-stu-id="8fbc1-132">**Project Management**</span></span>

<span data-ttu-id="8fbc1-133">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="8fbc1-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="8fbc1-134">Dalam **Jadual Projek** , apabila mengubah daripada **Manual** kepada **Auto** , simpan auto tidak selesai.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-134">In the **Project Schedule** , when changing from **Manual** to **Auto** , auto save is not completing.</span></span>
- <span data-ttu-id="8fbc1-135">Kos perbelanjaan tidak sepatutnya dikira ke atas varians pada **Grid Penjejakan Projek**.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="8fbc1-136">Tingkah laku yang tidak konsisten untuk lajur **Tag anggaran** semasa beban berbanding mengubah jenis **Fasa Masa**.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="8fbc1-137">Kos sebenar ke atas projek mungkin tidak menggambarkan jumlah daripada **Sebenar**.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="8fbc1-138">**Anggaran Tarikh Tamat** pada tab **Ringkasan** tidak sepadan dengan **Jadual WBS**.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="8fbc1-139">**Kemas Kini Masa Sebenar** di luar tidak berfungsi dengan betul.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="8fbc1-140">Pengurus Projek di luar akar **BU** tidak boleh mencipta projek.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="8fbc1-141">Perubahan kepada tugas atau kategori tentang **Anggaran Perbelanjaan** tidak diteruskan.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="8fbc1-142">**Salinan kontrak** menyalin jadual invois dan status jalanan.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="8fbc1-143">Butang **Segar Semula Sebenar** mengira tugasan ringkasan dengan salah.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="8fbc1-144">Tambahan Projek Microsoft: Betulkan ralat rujukan tidak sah jika mana-mana ahli pasukan mempunyai unit penyumberan kosong.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>

