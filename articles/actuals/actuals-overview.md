---
title: Aktual
description: Topik ini memberikan maklumat tentang cara bekerja dengan aktual dalam Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 13c429763fa805fae5324e4dcf1bf7669e842281
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126322"
---
# <a name="actuals"></a><span data-ttu-id="76746-103">Aktual</span><span class="sxs-lookup"><span data-stu-id="76746-103">Actuals</span></span> 

<span data-ttu-id="76746-104">_**Gunakan pada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="76746-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="76746-105">Aktual ialah jumlah kerja yang telah disiapkan pada sebuah projek.</span><span class="sxs-lookup"><span data-stu-id="76746-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="76746-106">Ia dicipta sebagai hasil daripada entri masa dan perbelanjaan, serta entri jurnal dan invois.</span><span class="sxs-lookup"><span data-stu-id="76746-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="76746-107">Garisan jurnal dan serahan masa</span><span class="sxs-lookup"><span data-stu-id="76746-107">Journal lines and time submission</span></span>

<span data-ttu-id="76746-108">Untuk mendapatkan maklumat lanjut tentang entri masa, lihat [Gambaran keseluruhan entri masa](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="76746-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="76746-109">Masa dan bahan</span><span class="sxs-lookup"><span data-stu-id="76746-109">Time and materials</span></span>

<span data-ttu-id="76746-110">Apabila entri masa yang diserahkan telah dipautkan dengan projek yang dipetakan dengan baris kontrak masa dan bahan, sistem mencipta dua garisan jurnal, satu untuk kos dan satu untuk jualan yang tidak dibilkan.</span><span class="sxs-lookup"><span data-stu-id="76746-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="76746-111">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="76746-111">Fixed price</span></span>

<span data-ttu-id="76746-112">Apabila entri masa yang telah diserahkan dipautkan kepada projek yang dipetakan kepada baris kontrak harga tetap, sistem mencipta satu garisan jurnal untuk kos.</span><span class="sxs-lookup"><span data-stu-id="76746-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="76746-113">Penetapan harga lalai</span><span class="sxs-lookup"><span data-stu-id="76746-113">Default pricing</span></span>

<span data-ttu-id="76746-114">Logik untuk mencipta harga lalai terletak pada garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="76746-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="76746-115">Nilai medan daripada entri masa disalin kepada garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="76746-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="76746-116">Nilai-nilai ini termasuk tarikh transaksi, baris kontrak yang projek dipetakan padanya, dan mata wang yang menghasilkan senarai harga yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="76746-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="76746-117">Medan-medan yang mempengaruhi penetapan harga lalai, seperti **Peranan** dan **Unit Organisasi**, digunakan untuk menentukan harga yang sesuai pada garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="76746-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="76746-118">Anda boleh menambah medan tersuai pada entri masa.</span><span class="sxs-lookup"><span data-stu-id="76746-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="76746-119">Jika anda mahu nilai medan disebarkan kepada aktual, cipta medan pada entiti Aktual dan gunakan pemetaan medan untuk menyalin medan daripada entri masa kepada aktual.</span><span class="sxs-lookup"><span data-stu-id="76746-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="76746-120">Serahan garisan jurnal dan perbelanjaan asas</span><span class="sxs-lookup"><span data-stu-id="76746-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="76746-121">Untuk mendapatkan maklumat lanjut tentang entri perbelanjaan, lihat [Gambaran keseluruhan perbelanjaan](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="76746-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="76746-122">Masa dan bahan</span><span class="sxs-lookup"><span data-stu-id="76746-122">Time and materials</span></span>

<span data-ttu-id="76746-123">Apabila entri perbelanjaan asas yang diserahkan telah dipautkan kepada projek yang dipetakan kepada baris kontrak masa dan bahan, sistem mencipta dua garisan jurnal, satu untuk kos dan satu untuk jualan yang tidak dibilkan.</span><span class="sxs-lookup"><span data-stu-id="76746-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="76746-124">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="76746-124">Fixed price</span></span>

<span data-ttu-id="76746-125">Apabila entri perbelanjaan asas yang telah diserahkan dipautkan kepada projek yang dipetakan kepada baris kontrak harga tetap, sistem mencipta satu garisan jurnal untuk kos.</span><span class="sxs-lookup"><span data-stu-id="76746-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="76746-126">Penetapan harga lalai</span><span class="sxs-lookup"><span data-stu-id="76746-126">Default pricing</span></span>

<span data-ttu-id="76746-127">Logik untuk memasukkan harga lalai bagi perbelanjaan adalah berdasarkan kategori perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="76746-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="76746-128">Tarikh transaksi, baris kontrak yang projek dipetakan dan mata wang semuanya digunakan untuk menentukan senarai harga bersesuaian.</span><span class="sxs-lookup"><span data-stu-id="76746-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="76746-129">Walau bagaimanapun, secara lalai, jumlah yang dimasukkan untuk harga itu sendiri ditetapkan secara langsung pada garisan jurnal perbelanjaan bagi kos dan jualan.</span><span class="sxs-lookup"><span data-stu-id="76746-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="76746-130">Entri berasaskan kategori bagi setiap unit harga lalai pada entri perbelanjaan tidak tersedia.</span><span class="sxs-lookup"><span data-stu-id="76746-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="76746-131">Gunakan jurnal entri untuk merekodkan kos</span><span class="sxs-lookup"><span data-stu-id="76746-131">Use entry journals to record costs</span></span>

<span data-ttu-id="76746-132">Anda boleh menggunakan jurnal entri untuk merekodkan kos atau hasil dalam kelas bahan, yuran, masa, perbelanjaan, atau transaksi cukai.</span><span class="sxs-lookup"><span data-stu-id="76746-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="76746-133">Jurnal boleh digunakan untuk tujuan berikut:</span><span class="sxs-lookup"><span data-stu-id="76746-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="76746-134">Rekodkan kos aktual bahan dan jualan pada projek.</span><span class="sxs-lookup"><span data-stu-id="76746-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="76746-135">Alihkan transaksi aktual daripada sistem lain kepada Microsoft Dynamics 365 Project Operations..</span><span class="sxs-lookup"><span data-stu-id="76746-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="76746-136">Rekodkan kos yang berlaku dalam sistem yang lain.</span><span class="sxs-lookup"><span data-stu-id="76746-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="76746-137">Kos ini boleh merangkumi kos perolehan atau subkontrak.</span><span class="sxs-lookup"><span data-stu-id="76746-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="76746-138">Aplikasi ini tidak mengesahkan jenis garisan jurnal atau penetapan harga yang berkaitan yang dimasukkan pada garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="76746-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="76746-139">Oleh itu, hanya pengguna yang menyedari sepenuhnya kesan perakaunan yang aktual ada pada projek itu, harus menggunakan jurnal entri untuk mencipta aktual.</span><span class="sxs-lookup"><span data-stu-id="76746-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="76746-140">Disebabkan oleh kesan jenis Jurnal ini, anda perlu memilih dengan teliti orang yang mempunyai akses untuk mencipta jurnal entri.</span><span class="sxs-lookup"><span data-stu-id="76746-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="76746-141">Rekodkan aktual berdasarkan peristiwa projek</span><span class="sxs-lookup"><span data-stu-id="76746-141">Record actuals based on project events</span></span>

<span data-ttu-id="76746-142">Project Operations merekodkan transaksi kewangan yang berlaku semasa projek.</span><span class="sxs-lookup"><span data-stu-id="76746-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="76746-143">Transaksi ini direkodkan sebagai aktual.</span><span class="sxs-lookup"><span data-stu-id="76746-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="76746-144">Jadual berikut menunjukkan jenis aktual berbeza yang dicipta, bergantung pada sama ada projek itu adalah projek masa dan bahan atau projek harga tetap, dalam peringkat prajualan, atau merupakan projek dalaman.</span><span class="sxs-lookup"><span data-stu-id="76746-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="76746-145">Sumber tersebut tergolong dalam unit organisasi yang sama seperti unit kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="76746-146">Peristiwa</span><span class="sxs-lookup"><span data-stu-id="76746-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="76746-147">Projek boleh dibilkan atau dijual</span><span class="sxs-lookup"><span data-stu-id="76746-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="76746-148">Projek dalam peringkat prajualan</span><span class="sxs-lookup"><span data-stu-id="76746-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="76746-149">Projek dalaman</span><span class="sxs-lookup"><span data-stu-id="76746-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="76746-150">Masa dan bahan</span><span class="sxs-lookup"><span data-stu-id="76746-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="76746-151">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="76746-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="76746-152">Sebenar</span><span class="sxs-lookup"><span data-stu-id="76746-152">Actuals</span></span></th>
<th><span data-ttu-id="76746-153">Mata wang transaksi</span><span class="sxs-lookup"><span data-stu-id="76746-153">Transaction currency</span></span></th>
<th><span data-ttu-id="76746-154">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="76746-154">Fixed price</span></span></th>
<th><span data-ttu-id="76746-155">Mata wang transaksi</span><span class="sxs-lookup"><span data-stu-id="76746-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76746-156">Entri masa dicipta.</span><span class="sxs-lookup"><span data-stu-id="76746-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="76746-157">Tiada aktiviti dalam entiti Aktual</span><span class="sxs-lookup"><span data-stu-id="76746-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76746-158">Entri masa diserahkan.</span><span class="sxs-lookup"><span data-stu-id="76746-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="76746-159">Tiada aktiviti dalam entiti Aktual</span><span class="sxs-lookup"><span data-stu-id="76746-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="76746-160">Masa telah diluluskan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku semasa kelulusan.</span><span class="sxs-lookup"><span data-stu-id="76746-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="76746-161">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="76746-161">Cost actual</span></span></td>
<td><span data-ttu-id="76746-162">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="76746-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="76746-163">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="76746-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="76746-164">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="76746-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="76746-165">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="76746-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="76746-166">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="76746-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76746-167">Jualan belum dibilkan sebenar – Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="76746-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="76746-168">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="76746-169">Masa telah diluluskan dan tiada pengurangan dalam masa boleh dibilkan berlaku semasa kelulusan.</span><span class="sxs-lookup"><span data-stu-id="76746-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="76746-170">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="76746-170">Cost actual</span></span></td>
<td><span data-ttu-id="76746-171">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="76746-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="76746-172">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="76746-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="76746-173">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="76746-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="76746-174">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="76746-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="76746-175">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="76746-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76746-176">Jualan belum dibilkan sebenar – Boleh dituntut untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="76746-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="76746-177">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76746-178">Jualan belum dibilkan sebenar – Tidak boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="76746-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="76746-179">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="76746-180">Invois disahkan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku.</span><span class="sxs-lookup"><span data-stu-id="76746-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="76746-181">Pengunduran jualan belum dibilkan</span><span class="sxs-lookup"><span data-stu-id="76746-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="76746-182">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="76746-183">Jualan dibilkan untuk pencapaian</span><span class="sxs-lookup"><span data-stu-id="76746-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="76746-184">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="76746-185">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="76746-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="76746-186">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="76746-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76746-187">Jualan dibilkan</span><span class="sxs-lookup"><span data-stu-id="76746-187">Billed sales</span></span></td>
<td><span data-ttu-id="76746-188">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="76746-189">Invois disahkan dan pengurangan dalam masa boleh dibilkan berlaku.</span><span class="sxs-lookup"><span data-stu-id="76746-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="76746-190">Pengunduran jualan belum dibilkan</span><span class="sxs-lookup"><span data-stu-id="76746-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="76746-191">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="76746-192">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="76746-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="76746-193">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="76746-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="76746-194">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="76746-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="76746-195">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="76746-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76746-196">Jualan dibilkan – Boleh dituntut untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="76746-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="76746-197">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76746-198">Jualan dibilkan – Tidak boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="76746-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="76746-199">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="76746-200">Invois dibetulkan untuk menambah kuantiti yang boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="76746-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="76746-201">Julana dibilkan – Pengunduran</span><span class="sxs-lookup"><span data-stu-id="76746-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="76746-202">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="76746-203">Pengunduran jualan dibilkan untuk pencapaian</span><span class="sxs-lookup"><span data-stu-id="76746-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="76746-204">Penukarang status pencapaian daripada <strong>Diinvoiskan</strong> kepada <strong>Sedia untuk invois</strong></span><span class="sxs-lookup"><span data-stu-id="76746-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="76746-205">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="76746-206">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="76746-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="76746-207">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="76746-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76746-208">Jualan dibilkan</span><span class="sxs-lookup"><span data-stu-id="76746-208">Billed sales</span></span></td>
<td><span data-ttu-id="76746-209">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="76746-210">Invois dibetulkan untuk mengurangkan kuantiti yang boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="76746-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="76746-211">Julana dibilkan – Pengunduran</span><span class="sxs-lookup"><span data-stu-id="76746-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="76746-212">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76746-213">Jualan dibilkan untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="76746-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="76746-214">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76746-215">Jualan tidak dibilkan – Boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="76746-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="76746-216">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="76746-217">Sumber tersebut tergolong dalam unit organisasi yang berbeza daripada unit kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="76746-218">Peristiwa</span><span class="sxs-lookup"><span data-stu-id="76746-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="76746-219">Projek boleh dibilkan atau dijual</span><span class="sxs-lookup"><span data-stu-id="76746-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="76746-220">Projek dalam peringkat prajualan</span><span class="sxs-lookup"><span data-stu-id="76746-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="76746-221">Projek dalaman</span><span class="sxs-lookup"><span data-stu-id="76746-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="76746-222">Masa dan bahan</span><span class="sxs-lookup"><span data-stu-id="76746-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="76746-223">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="76746-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="76746-224">Sebenar</span><span class="sxs-lookup"><span data-stu-id="76746-224">Actuals</span></span></th>
<th><span data-ttu-id="76746-225">Mata wang transaksi</span><span class="sxs-lookup"><span data-stu-id="76746-225">Transaction currency</span></span></th>
<th><span data-ttu-id="76746-226">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="76746-226">Fixed price</span></span></th>
<th><span data-ttu-id="76746-227">Mata wang transaksi</span><span class="sxs-lookup"><span data-stu-id="76746-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76746-228">Entri masa dicipta.</span><span class="sxs-lookup"><span data-stu-id="76746-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="76746-229">Tiada aktiviti dalam entiti Aktual</span><span class="sxs-lookup"><span data-stu-id="76746-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76746-230">Entri masa diserahkan.</span><span class="sxs-lookup"><span data-stu-id="76746-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="76746-231">Tiada aktiviti dalam entiti Aktual</span><span class="sxs-lookup"><span data-stu-id="76746-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="76746-232">Masa telah diluluskan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku semasa kelulusan.</span><span class="sxs-lookup"><span data-stu-id="76746-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="76746-233">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="76746-233">Cost actual</span></span></td>
<td><span data-ttu-id="76746-234">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="76746-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="76746-235">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="76746-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="76746-236">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="76746-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="76746-237">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="76746-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="76746-238">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="76746-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76746-239">Jualan belum dibilkan sebenar – Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="76746-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="76746-240">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76746-241">Kos unit persumberan</span><span class="sxs-lookup"><span data-stu-id="76746-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="76746-242">Mata wang unit persumberan</span><span class="sxs-lookup"><span data-stu-id="76746-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76746-243">Jualan antara organisasi</span><span class="sxs-lookup"><span data-stu-id="76746-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="76746-244">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="76746-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="76746-245">Masa telah diluluskan dan tiada pengurangan dalam masa boleh dibilkan berlaku semasa kelulusan.</span><span class="sxs-lookup"><span data-stu-id="76746-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="76746-246">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="76746-246">Cost actual</span></span></td>
<td><span data-ttu-id="76746-247">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="76746-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="76746-248">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="76746-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="76746-249">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="76746-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="76746-250">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="76746-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="76746-251">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="76746-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76746-252">Kos unit persumberan</span><span class="sxs-lookup"><span data-stu-id="76746-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="76746-253">Mata wang unit persumberan</span><span class="sxs-lookup"><span data-stu-id="76746-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76746-254">Jualan antara organisasi</span><span class="sxs-lookup"><span data-stu-id="76746-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="76746-255">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="76746-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76746-256">Jualan belum dibilkan sebenar – Boleh dituntut untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="76746-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="76746-257">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76746-258">Jualan belum dibilkan sebenar – Tidak boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="76746-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="76746-259">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="76746-260">Invois disahkan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku.</span><span class="sxs-lookup"><span data-stu-id="76746-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="76746-261">Pengunduran jualan belum dibilkan</span><span class="sxs-lookup"><span data-stu-id="76746-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="76746-262">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="76746-263">Jualan dibilkan untuk pencapaian</span><span class="sxs-lookup"><span data-stu-id="76746-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="76746-264">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="76746-265">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="76746-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="76746-266">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="76746-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76746-267">Jualan dibilkan</span><span class="sxs-lookup"><span data-stu-id="76746-267">Billed sales</span></span></td>
<td><span data-ttu-id="76746-268">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="76746-269">Invois disahkan dan pengurangan dalam masa boleh dibilkan berlaku.</span><span class="sxs-lookup"><span data-stu-id="76746-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="76746-270">Pengunduran jualan belum dibilkan</span><span class="sxs-lookup"><span data-stu-id="76746-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="76746-271">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="76746-272">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="76746-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="76746-273">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="76746-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="76746-274">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="76746-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="76746-275">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="76746-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76746-276">Jualan dibilkan – Boleh dituntut untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="76746-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="76746-277">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76746-278">Jualan dibilkan – Tidak boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="76746-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="76746-279">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="76746-280">Invois dibetulkan untuk menambah kuantiti yang boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="76746-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="76746-281">Julana dibilkan – Pengunduran</span><span class="sxs-lookup"><span data-stu-id="76746-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="76746-282">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="76746-283">Pengunduran jualan dibilkan untuk pencapaian</span><span class="sxs-lookup"><span data-stu-id="76746-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="76746-284">Penukarang status pencapaian daripada <strong>Diinvoiskan</strong> kepada <strong>Sedia untuk invois</strong></span><span class="sxs-lookup"><span data-stu-id="76746-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="76746-285">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="76746-286">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="76746-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="76746-287">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="76746-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76746-288">Jualan dibilkan</span><span class="sxs-lookup"><span data-stu-id="76746-288">Billed sales</span></span></td>
<td><span data-ttu-id="76746-289">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="76746-290">Invois dibetulkan untuk mengurangkan kuantiti yang boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="76746-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="76746-291">Julana dibilkan – Pengunduran</span><span class="sxs-lookup"><span data-stu-id="76746-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="76746-292">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76746-293">Jualan dibilkan untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="76746-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="76746-294">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76746-295">Jualan tidak dibilkan – Boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="76746-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="76746-296">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="76746-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
