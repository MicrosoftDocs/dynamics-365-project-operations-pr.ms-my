---
title: Aktual
description: Topik ini memberikan maklumat tentang cara untuk bekerja dengan aktual dalam Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6a94bd143b0d0dad2a08511a34e592a057b6d2a1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291810"
---
# <a name="actuals"></a><span data-ttu-id="174e6-103">Aktual</span><span class="sxs-lookup"><span data-stu-id="174e6-103">Actuals</span></span> 

<span data-ttu-id="174e6-104">_**Gunakan pada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="174e6-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="174e6-105">Aktual ialah jumlah kerja yang telah disiapkan pada sebuah projek.</span><span class="sxs-lookup"><span data-stu-id="174e6-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="174e6-106">Ia dicipta sebagai hasil daripada entri masa dan perbelanjaan, serta entri jurnal dan invois.</span><span class="sxs-lookup"><span data-stu-id="174e6-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="174e6-107">Garisan jurnal dan serahan masa</span><span class="sxs-lookup"><span data-stu-id="174e6-107">Journal lines and time submission</span></span>

<span data-ttu-id="174e6-108">Untuk mendapatkan maklumat lanjut tentang entri masa, lihat [Gambaran keseluruhan entri masa](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="174e6-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="174e6-109">Masa dan bahan</span><span class="sxs-lookup"><span data-stu-id="174e6-109">Time and materials</span></span>

<span data-ttu-id="174e6-110">Apabila entri masa yang diserahkan telah dipautkan dengan projek yang dipetakan dengan baris kontrak masa dan bahan, sistem mencipta dua garisan jurnal, satu untuk kos dan satu untuk jualan yang tidak dibilkan.</span><span class="sxs-lookup"><span data-stu-id="174e6-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="174e6-111">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="174e6-111">Fixed price</span></span>

<span data-ttu-id="174e6-112">Apabila entri masa yang telah diserahkan dipautkan kepada projek yang dipetakan kepada baris kontrak harga tetap, sistem mencipta satu garisan jurnal untuk kos.</span><span class="sxs-lookup"><span data-stu-id="174e6-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="174e6-113">Penetapan harga lalai</span><span class="sxs-lookup"><span data-stu-id="174e6-113">Default pricing</span></span>

<span data-ttu-id="174e6-114">Logik untuk mencipta harga lalai terletak pada garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="174e6-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="174e6-115">Nilai medan daripada entri masa disalin kepada garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="174e6-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="174e6-116">Nilai-nilai ini termasuk tarikh transaksi, baris kontrak yang projek dipetakan padanya, dan mata wang yang menghasilkan senarai harga yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="174e6-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="174e6-117">Medan-medan yang mempengaruhi penetapan harga lalai, seperti **Peranan** dan **Unit Organisasi**, digunakan untuk menentukan harga yang sesuai pada garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="174e6-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="174e6-118">Anda boleh menambah medan tersuai pada entri masa.</span><span class="sxs-lookup"><span data-stu-id="174e6-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="174e6-119">Jika anda mahu nilai medan disebarkan kepada aktual, cipta medan pada entiti Aktual dan gunakan pemetaan medan untuk menyalin medan daripada entri masa kepada aktual.</span><span class="sxs-lookup"><span data-stu-id="174e6-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="174e6-120">Serahan garisan jurnal dan perbelanjaan asas</span><span class="sxs-lookup"><span data-stu-id="174e6-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="174e6-121">Untuk mendapatkan maklumat lanjut tentang entri perbelanjaan, lihat [Gambaran keseluruhan perbelanjaan](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="174e6-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="174e6-122">Masa dan bahan</span><span class="sxs-lookup"><span data-stu-id="174e6-122">Time and materials</span></span>

<span data-ttu-id="174e6-123">Apabila entri perbelanjaan asas yang diserahkan telah dipautkan kepada projek yang dipetakan kepada baris kontrak masa dan bahan, sistem mencipta dua garisan jurnal, satu untuk kos dan satu untuk jualan yang tidak dibilkan.</span><span class="sxs-lookup"><span data-stu-id="174e6-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="174e6-124">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="174e6-124">Fixed price</span></span>

<span data-ttu-id="174e6-125">Apabila entri perbelanjaan asas yang telah diserahkan dipautkan kepada projek yang dipetakan kepada baris kontrak harga tetap, sistem mencipta satu garisan jurnal untuk kos.</span><span class="sxs-lookup"><span data-stu-id="174e6-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="174e6-126">Penetapan harga lalai</span><span class="sxs-lookup"><span data-stu-id="174e6-126">Default pricing</span></span>

<span data-ttu-id="174e6-127">Logik untuk memasukkan harga lalai bagi perbelanjaan adalah berdasarkan kategori perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="174e6-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="174e6-128">Tarikh transaksi, baris kontrak yang projek dipetakan dan mata wang semuanya digunakan untuk menentukan senarai harga bersesuaian.</span><span class="sxs-lookup"><span data-stu-id="174e6-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="174e6-129">Walau bagaimanapun, secara lalai, jumlah yang dimasukkan untuk harga itu sendiri ditetapkan secara langsung pada garisan jurnal perbelanjaan bagi kos dan jualan.</span><span class="sxs-lookup"><span data-stu-id="174e6-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="174e6-130">Entri berasaskan kategori bagi setiap unit harga lalai pada entri perbelanjaan tidak tersedia.</span><span class="sxs-lookup"><span data-stu-id="174e6-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="174e6-131">Gunakan jurnal entri untuk merekodkan kos</span><span class="sxs-lookup"><span data-stu-id="174e6-131">Use entry journals to record costs</span></span>

<span data-ttu-id="174e6-132">Anda boleh menggunakan jurnal entri untuk merekodkan kos atau hasil dalam kelas bahan, yuran, masa, perbelanjaan, atau transaksi cukai.</span><span class="sxs-lookup"><span data-stu-id="174e6-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="174e6-133">Jurnal boleh digunakan untuk tujuan berikut:</span><span class="sxs-lookup"><span data-stu-id="174e6-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="174e6-134">Rekodkan kos aktual bahan dan jualan pada projek.</span><span class="sxs-lookup"><span data-stu-id="174e6-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="174e6-135">Alihkan aktual transaksi daripada sistem lain kepada Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="174e6-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="174e6-136">Rekodkan kos yang berlaku dalam sistem yang lain.</span><span class="sxs-lookup"><span data-stu-id="174e6-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="174e6-137">Kos ini boleh merangkumi kos perolehan atau subkontrak.</span><span class="sxs-lookup"><span data-stu-id="174e6-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="174e6-138">Aplikasi ini tidak mengesahkan jenis garisan jurnal atau penetapan harga yang berkaitan yang dimasukkan pada garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="174e6-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="174e6-139">Oleh itu, hanya pengguna yang menyedari sepenuhnya kesan perakaunan yang aktual ada pada projek itu, harus menggunakan jurnal entri untuk mencipta aktual.</span><span class="sxs-lookup"><span data-stu-id="174e6-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="174e6-140">Disebabkan oleh kesan jenis Jurnal ini, anda perlu memilih dengan teliti orang yang mempunyai akses untuk mencipta jurnal entri.</span><span class="sxs-lookup"><span data-stu-id="174e6-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="174e6-141">Rekodkan aktual berdasarkan peristiwa projek</span><span class="sxs-lookup"><span data-stu-id="174e6-141">Record actuals based on project events</span></span>

<span data-ttu-id="174e6-142">Project Operations merekodkan transaksi kewangan yang berlaku semasa projek.</span><span class="sxs-lookup"><span data-stu-id="174e6-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="174e6-143">Transaksi ini direkodkan sebagai aktual.</span><span class="sxs-lookup"><span data-stu-id="174e6-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="174e6-144">Jadual berikut menunjukkan jenis aktual berbeza yang dicipta, bergantung pada sama ada projek itu adalah projek masa dan bahan atau projek harga tetap, dalam peringkat prajualan, atau merupakan projek dalaman.</span><span class="sxs-lookup"><span data-stu-id="174e6-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="174e6-145">Sumber tersebut tergolong dalam unit organisasi yang sama seperti unit kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="174e6-146">Peristiwa</span><span class="sxs-lookup"><span data-stu-id="174e6-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="174e6-147">Projek boleh dibilkan atau dijual</span><span class="sxs-lookup"><span data-stu-id="174e6-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="174e6-148">Projek dalam peringkat prajualan</span><span class="sxs-lookup"><span data-stu-id="174e6-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="174e6-149">Projek dalaman</span><span class="sxs-lookup"><span data-stu-id="174e6-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="174e6-150">Masa dan bahan</span><span class="sxs-lookup"><span data-stu-id="174e6-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="174e6-151">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="174e6-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="174e6-152">Sebenar</span><span class="sxs-lookup"><span data-stu-id="174e6-152">Actuals</span></span></th>
<th><span data-ttu-id="174e6-153">Mata wang transaksi</span><span class="sxs-lookup"><span data-stu-id="174e6-153">Transaction currency</span></span></th>
<th><span data-ttu-id="174e6-154">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="174e6-154">Fixed price</span></span></th>
<th><span data-ttu-id="174e6-155">Mata wang transaksi</span><span class="sxs-lookup"><span data-stu-id="174e6-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="174e6-156">Entri masa dicipta.</span><span class="sxs-lookup"><span data-stu-id="174e6-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="174e6-157">Tiada aktiviti dalam entiti Aktual</span><span class="sxs-lookup"><span data-stu-id="174e6-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="174e6-158">Entri masa diserahkan.</span><span class="sxs-lookup"><span data-stu-id="174e6-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="174e6-159">Tiada aktiviti dalam entiti Aktual</span><span class="sxs-lookup"><span data-stu-id="174e6-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="174e6-160">Masa telah diluluskan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku semasa kelulusan.</span><span class="sxs-lookup"><span data-stu-id="174e6-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="174e6-161">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="174e6-161">Cost actual</span></span></td>
<td><span data-ttu-id="174e6-162">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="174e6-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="174e6-163">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="174e6-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="174e6-164">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="174e6-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="174e6-165">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="174e6-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="174e6-166">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="174e6-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="174e6-167">Jualan belum dibilkan sebenar – Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="174e6-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="174e6-168">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="174e6-169">Masa telah diluluskan dan tiada pengurangan dalam masa boleh dibilkan berlaku semasa kelulusan.</span><span class="sxs-lookup"><span data-stu-id="174e6-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="174e6-170">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="174e6-170">Cost actual</span></span></td>
<td><span data-ttu-id="174e6-171">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="174e6-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="174e6-172">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="174e6-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="174e6-173">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="174e6-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="174e6-174">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="174e6-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="174e6-175">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="174e6-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="174e6-176">Jualan belum dibilkan sebenar – Boleh dituntut untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="174e6-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="174e6-177">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="174e6-178">Jualan belum dibilkan sebenar – Tidak boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="174e6-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="174e6-179">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="174e6-180">Invois disahkan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku.</span><span class="sxs-lookup"><span data-stu-id="174e6-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="174e6-181">Pengunduran jualan belum dibilkan</span><span class="sxs-lookup"><span data-stu-id="174e6-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="174e6-182">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="174e6-183">Jualan dibilkan untuk pencapaian</span><span class="sxs-lookup"><span data-stu-id="174e6-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="174e6-184">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="174e6-185">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="174e6-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="174e6-186">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="174e6-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="174e6-187">Jualan dibilkan</span><span class="sxs-lookup"><span data-stu-id="174e6-187">Billed sales</span></span></td>
<td><span data-ttu-id="174e6-188">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="174e6-189">Invois disahkan dan pengurangan dalam masa boleh dibilkan berlaku.</span><span class="sxs-lookup"><span data-stu-id="174e6-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="174e6-190">Pengunduran jualan belum dibilkan</span><span class="sxs-lookup"><span data-stu-id="174e6-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="174e6-191">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="174e6-192">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="174e6-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="174e6-193">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="174e6-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="174e6-194">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="174e6-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="174e6-195">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="174e6-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="174e6-196">Jualan dibilkan – Boleh dituntut untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="174e6-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="174e6-197">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="174e6-198">Jualan dibilkan – Tidak boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="174e6-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="174e6-199">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="174e6-200">Invois dibetulkan untuk menambah kuantiti yang boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="174e6-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="174e6-201">Julana dibilkan – Pengunduran</span><span class="sxs-lookup"><span data-stu-id="174e6-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="174e6-202">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="174e6-203">Pengunduran jualan dibilkan untuk pencapaian</span><span class="sxs-lookup"><span data-stu-id="174e6-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="174e6-204">Penukarang status pencapaian daripada <strong>Diinvoiskan</strong> kepada <strong>Sedia untuk invois</strong></span><span class="sxs-lookup"><span data-stu-id="174e6-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="174e6-205">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="174e6-206">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="174e6-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="174e6-207">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="174e6-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="174e6-208">Jualan dibilkan</span><span class="sxs-lookup"><span data-stu-id="174e6-208">Billed sales</span></span></td>
<td><span data-ttu-id="174e6-209">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="174e6-210">Invois dibetulkan untuk mengurangkan kuantiti yang boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="174e6-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="174e6-211">Julana dibilkan – Pengunduran</span><span class="sxs-lookup"><span data-stu-id="174e6-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="174e6-212">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="174e6-213">Jualan dibilkan untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="174e6-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="174e6-214">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="174e6-215">Jualan tidak dibilkan – Boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="174e6-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="174e6-216">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="174e6-217">Sumber tersebut tergolong dalam unit organisasi yang berbeza daripada unit kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="174e6-218">Peristiwa</span><span class="sxs-lookup"><span data-stu-id="174e6-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="174e6-219">Projek boleh dibilkan atau dijual</span><span class="sxs-lookup"><span data-stu-id="174e6-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="174e6-220">Projek dalam peringkat prajualan</span><span class="sxs-lookup"><span data-stu-id="174e6-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="174e6-221">Projek dalaman</span><span class="sxs-lookup"><span data-stu-id="174e6-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="174e6-222">Masa dan bahan</span><span class="sxs-lookup"><span data-stu-id="174e6-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="174e6-223">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="174e6-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="174e6-224">Sebenar</span><span class="sxs-lookup"><span data-stu-id="174e6-224">Actuals</span></span></th>
<th><span data-ttu-id="174e6-225">Mata wang transaksi</span><span class="sxs-lookup"><span data-stu-id="174e6-225">Transaction currency</span></span></th>
<th><span data-ttu-id="174e6-226">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="174e6-226">Fixed price</span></span></th>
<th><span data-ttu-id="174e6-227">Mata wang transaksi</span><span class="sxs-lookup"><span data-stu-id="174e6-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="174e6-228">Entri masa dicipta.</span><span class="sxs-lookup"><span data-stu-id="174e6-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="174e6-229">Tiada aktiviti dalam entiti Aktual</span><span class="sxs-lookup"><span data-stu-id="174e6-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="174e6-230">Entri masa diserahkan.</span><span class="sxs-lookup"><span data-stu-id="174e6-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="174e6-231">Tiada aktiviti dalam entiti Aktual</span><span class="sxs-lookup"><span data-stu-id="174e6-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="174e6-232">Masa telah diluluskan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku semasa kelulusan.</span><span class="sxs-lookup"><span data-stu-id="174e6-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="174e6-233">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="174e6-233">Cost actual</span></span></td>
<td><span data-ttu-id="174e6-234">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="174e6-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="174e6-235">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="174e6-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="174e6-236">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="174e6-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="174e6-237">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="174e6-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="174e6-238">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="174e6-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="174e6-239">Jualan belum dibilkan sebenar – Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="174e6-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="174e6-240">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="174e6-241">Kos unit persumberan</span><span class="sxs-lookup"><span data-stu-id="174e6-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="174e6-242">Mata wang unit persumberan</span><span class="sxs-lookup"><span data-stu-id="174e6-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="174e6-243">Jualan antara organisasi</span><span class="sxs-lookup"><span data-stu-id="174e6-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="174e6-244">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="174e6-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="174e6-245">Masa telah diluluskan dan tiada pengurangan dalam masa boleh dibilkan berlaku semasa kelulusan.</span><span class="sxs-lookup"><span data-stu-id="174e6-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="174e6-246">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="174e6-246">Cost actual</span></span></td>
<td><span data-ttu-id="174e6-247">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="174e6-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="174e6-248">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="174e6-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="174e6-249">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="174e6-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="174e6-250">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="174e6-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="174e6-251">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="174e6-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="174e6-252">Kos unit persumberan</span><span class="sxs-lookup"><span data-stu-id="174e6-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="174e6-253">Mata wang unit persumberan</span><span class="sxs-lookup"><span data-stu-id="174e6-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="174e6-254">Jualan antara organisasi</span><span class="sxs-lookup"><span data-stu-id="174e6-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="174e6-255">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="174e6-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="174e6-256">Jualan belum dibilkan sebenar – Boleh dituntut untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="174e6-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="174e6-257">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="174e6-258">Jualan belum dibilkan sebenar – Tidak boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="174e6-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="174e6-259">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="174e6-260">Invois disahkan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku.</span><span class="sxs-lookup"><span data-stu-id="174e6-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="174e6-261">Pengunduran jualan belum dibilkan</span><span class="sxs-lookup"><span data-stu-id="174e6-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="174e6-262">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="174e6-263">Jualan dibilkan untuk pencapaian</span><span class="sxs-lookup"><span data-stu-id="174e6-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="174e6-264">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="174e6-265">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="174e6-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="174e6-266">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="174e6-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="174e6-267">Jualan dibilkan</span><span class="sxs-lookup"><span data-stu-id="174e6-267">Billed sales</span></span></td>
<td><span data-ttu-id="174e6-268">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="174e6-269">Invois disahkan dan pengurangan dalam masa boleh dibilkan berlaku.</span><span class="sxs-lookup"><span data-stu-id="174e6-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="174e6-270">Pengunduran jualan belum dibilkan</span><span class="sxs-lookup"><span data-stu-id="174e6-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="174e6-271">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="174e6-272">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="174e6-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="174e6-273">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="174e6-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="174e6-274">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="174e6-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="174e6-275">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="174e6-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="174e6-276">Jualan dibilkan – Boleh dituntut untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="174e6-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="174e6-277">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="174e6-278">Jualan dibilkan – Tidak boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="174e6-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="174e6-279">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="174e6-280">Invois dibetulkan untuk menambah kuantiti yang boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="174e6-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="174e6-281">Julana dibilkan – Pengunduran</span><span class="sxs-lookup"><span data-stu-id="174e6-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="174e6-282">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="174e6-283">Pengunduran jualan dibilkan untuk pencapaian</span><span class="sxs-lookup"><span data-stu-id="174e6-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="174e6-284">Penukarang status pencapaian daripada <strong>Diinvoiskan</strong> kepada <strong>Sedia untuk invois</strong></span><span class="sxs-lookup"><span data-stu-id="174e6-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="174e6-285">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="174e6-286">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="174e6-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="174e6-287">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="174e6-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="174e6-288">Jualan dibilkan</span><span class="sxs-lookup"><span data-stu-id="174e6-288">Billed sales</span></span></td>
<td><span data-ttu-id="174e6-289">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="174e6-290">Invois dibetulkan untuk mengurangkan kuantiti yang boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="174e6-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="174e6-291">Julana dibilkan – Pengunduran</span><span class="sxs-lookup"><span data-stu-id="174e6-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="174e6-292">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="174e6-293">Jualan dibilkan untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="174e6-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="174e6-294">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="174e6-295">Jualan tidak dibilkan – Boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="174e6-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="174e6-296">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="174e6-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]