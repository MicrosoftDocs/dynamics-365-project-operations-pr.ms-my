---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 24, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas kini Project Service Automation 24, V3.
author: ruhercul
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
ms.openlocfilehash: c95a9dcada4fbf6c462df29d450aaafab4e73aa5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000267"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="465bc-103">Project Service Automation, Keluaran Kemas kini 24, V3</span><span class="sxs-lookup"><span data-stu-id="465bc-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="465bc-104">Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="465bc-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="465bc-105">Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan.</span><span class="sxs-lookup"><span data-stu-id="465bc-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="465bc-106">Keluaran ini serasi dengan Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="465bc-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="465bc-107">Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini.</span><span class="sxs-lookup"><span data-stu-id="465bc-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="465bc-108">Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="465bc-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="465bc-109">Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 24.</span><span class="sxs-lookup"><span data-stu-id="465bc-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="465bc-110">Versi ini mempunyai nombor bina V 3.10.42.43 dan secara amnya boleh didapati melalui kemas kini kendiri pada Oktober 2020.</span><span class="sxs-lookup"><span data-stu-id="465bc-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="465bc-111">Keluaran Kemas kini 24</span><span class="sxs-lookup"><span data-stu-id="465bc-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="465bc-112">Pembetulan pepijat</span><span class="sxs-lookup"><span data-stu-id="465bc-112">Bug fixes</span></span>

<span data-ttu-id="465bc-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="465bc-113">**Sales**</span></span>

<span data-ttu-id="465bc-114">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="465bc-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="465bc-115">Masalah semasa menetapkan senarai harga lalai produk.</span><span class="sxs-lookup"><span data-stu-id="465bc-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="465bc-116">Prestasi menang Sebut Harga perlahan disebabkan senarai harga terbenam dan salinan rekod harga peranan.</span><span class="sxs-lookup"><span data-stu-id="465bc-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="465bc-117">**Kontrak Projek/Hab Jualan** > **Item Baris Produk/Kuantiti Baris Pesanan** dibundarkan secara automatik kepada integer terdekat.</span><span class="sxs-lookup"><span data-stu-id="465bc-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="465bc-118">Tingkatkan kepada kelayakan sistem apabila membaca senarai harga.</span><span class="sxs-lookup"><span data-stu-id="465bc-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="465bc-119">Salin medan alamat pelanggan **address1_freighttermscode** dan **address1_shippingmethodcode** kepada Sebut Harga/Pesanan.</span><span class="sxs-lookup"><span data-stu-id="465bc-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="465bc-120">**Masa dan Perbelanjaan**</span><span class="sxs-lookup"><span data-stu-id="465bc-120">**Time and Expense**</span></span>

<span data-ttu-id="465bc-121">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="465bc-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="465bc-122">**Grid Entri Masa** tidak menyokong tingkah laku masa **Tarikh Sahaja**.</span><span class="sxs-lookup"><span data-stu-id="465bc-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="465bc-123">**Entri Masa** tidak disegarkan semula secara automatik.</span><span class="sxs-lookup"><span data-stu-id="465bc-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="465bc-124">Segar semula manual diperlukan.</span><span class="sxs-lookup"><span data-stu-id="465bc-124">A manual refresh is required.</span></span>
- <span data-ttu-id="465bc-125">Tidak dapat mengimport entri masa daripada tugasan apabila terdapat rehat (0 jam) dalam tugasan sumber.</span><span class="sxs-lookup"><span data-stu-id="465bc-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="465bc-126">Apabila mencipta entri masa, tetapkan mula sama seperti **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="465bc-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="465bc-127">Dayakan semula edit pukal untuk entri masa.</span><span class="sxs-lookup"><span data-stu-id="465bc-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="465bc-128">**Pengurusan Sumber**</span><span class="sxs-lookup"><span data-stu-id="465bc-128">**Resource Management**</span></span>

<span data-ttu-id="465bc-129">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="465bc-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="465bc-130">Mencuba untuk mengemas kini status tempahan antara hari tanpa keperluan akan membuang pengecualian rujukan yang tidak sah.</span><span class="sxs-lookup"><span data-stu-id="465bc-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="465bc-131">Ralat memuatkan **Pandangan Penyesuaian**.</span><span class="sxs-lookup"><span data-stu-id="465bc-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="465bc-132">**Pengurusan Projek**</span><span class="sxs-lookup"><span data-stu-id="465bc-132">**Project Management**</span></span>

<span data-ttu-id="465bc-133">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="465bc-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="465bc-134">Dalam **Jadual Projek**, apabila mengubah daripada **Manual** kepada **Auto**, simpan auto tidak selesai.</span><span class="sxs-lookup"><span data-stu-id="465bc-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="465bc-135">Kos perbelanjaan tidak sepatutnya dikira ke atas varians pada **Grid Penjejakan Projek**.</span><span class="sxs-lookup"><span data-stu-id="465bc-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="465bc-136">Tingkah laku yang tidak konsisten untuk lajur **Tag anggaran** semasa beban berbanding mengubah jenis **Fasa Masa**.</span><span class="sxs-lookup"><span data-stu-id="465bc-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="465bc-137">Kos sebenar ke atas projek mungkin tidak menggambarkan jumlah daripada **Sebenar**.</span><span class="sxs-lookup"><span data-stu-id="465bc-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="465bc-138">**Anggaran Tarikh Tamat** pada tab **Ringkasan** tidak sepadan dengan **Jadual WBS**.</span><span class="sxs-lookup"><span data-stu-id="465bc-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="465bc-139">**Kemas Kini Masa Sebenar** di luar tidak berfungsi dengan betul.</span><span class="sxs-lookup"><span data-stu-id="465bc-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="465bc-140">Pengurus Projek di luar akar **BU** tidak boleh mencipta projek.</span><span class="sxs-lookup"><span data-stu-id="465bc-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="465bc-141">Perubahan kepada tugas atau kategori tentang **Anggaran Perbelanjaan** tidak diteruskan.</span><span class="sxs-lookup"><span data-stu-id="465bc-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="465bc-142">**Salinan kontrak** menyalin jadual invois dan status jalanan.</span><span class="sxs-lookup"><span data-stu-id="465bc-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="465bc-143">Butang **Segar Semula Sebenar** mengira tugasan ringkasan dengan salah.</span><span class="sxs-lookup"><span data-stu-id="465bc-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="465bc-144">Tambahan Projek Microsoft: Betulkan ralat rujukan tidak sah jika mana-mana ahli pasukan mempunyai unit penyumberan kosong.</span><span class="sxs-lookup"><span data-stu-id="465bc-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]