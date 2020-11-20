---
title: Gambaran keseluruhan aktual
description: Topik ini memberikan maklumat tentang aktual projek.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cf9e36c99790b77f0ed6490f49b4ebeb043bcdf6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129779"
---
# <a name="actuals-overview"></a><span data-ttu-id="6270e-103">Gambaran keseluruhan aktual</span><span class="sxs-lookup"><span data-stu-id="6270e-103">Actuals overview</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6270e-104">Aktual ialah jumlah kerja yang telah disiapkan pada sebuah projek.</span><span class="sxs-lookup"><span data-stu-id="6270e-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="6270e-105">Aktual projek boleh dikesan kembali kepada dokumen sumber mereka.</span><span class="sxs-lookup"><span data-stu-id="6270e-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="6270e-106">Dokumen sumber tersebut termasuk entri masa, perbelanjaan dan jurnal dan serta invois.</span><span class="sxs-lookup"><span data-stu-id="6270e-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Cara aktual projek dikesan untuk mendapatkan dokumen sumber](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="6270e-108">Menyerahkan entri masa</span><span class="sxs-lookup"><span data-stu-id="6270e-108">Submitting a time entry</span></span>

<span data-ttu-id="6270e-109">Dalam PSA, apabila entri masa telah diserahkan untuk projek yang dipetakan kepada garis kontrak masa dan bahan, dua garisan jurnal dicipta.</span><span class="sxs-lookup"><span data-stu-id="6270e-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="6270e-110">Satu garis ialah untuk kos, dan garis lain ialah untuk jualan yang tidak dibilkan.</span><span class="sxs-lookup"><span data-stu-id="6270e-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="6270e-111">Apabila entri masa telah diserahkan untuk projek yang dipetakan kepada garis kontrak harga tetap, satu garis jurnal dicipta hanya untuk kos.</span><span class="sxs-lookup"><span data-stu-id="6270e-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="6270e-112">Logik untuk memasukkan harga lalai pada garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="6270e-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="6270e-113">Semua nilai medan daripada entri masa disalin ke garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="6270e-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="6270e-114">Medan-medan ini termasuk tarikh transaksi, baris kontrak yang projek dipetakan dan keputusan mata wang dalam senarai harga bersesuaian.</span><span class="sxs-lookup"><span data-stu-id="6270e-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="6270e-115">Medan-medan yang menjejaskan harga lalai, seperti **Peranan** dan **Unit Organisasi**, menyebabkan harga bersesuaian akan dimasukkan secara lalai pada garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="6270e-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="6270e-116">Jika anda menambah medan tersuai pada entri masa dan anda mahu nilai medan disebarkan kepada aktual, cipta medan pada entiti Aktual dan gunakan pemetaan medan untuk menyalin medan daripada entri masa kepada aktual.</span><span class="sxs-lookup"><span data-stu-id="6270e-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="6270e-117">Menyerahkan entri perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="6270e-117">Submitting an expense entry</span></span>

<span data-ttu-id="6270e-118">Dalam PSA, apabila entri perbelanjaan telah diserahkan untuk projek yang dipetakan kepada garis kontrak masa dan bahan, dua garisan jurnal dicipta.</span><span class="sxs-lookup"><span data-stu-id="6270e-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="6270e-119">Satu garis ialah untuk kos, dan garis lain ialah untuk jualan yang tidak dibilkan.</span><span class="sxs-lookup"><span data-stu-id="6270e-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="6270e-120">Apabila entri perbelanjaan telah diserahkan untuk projek yang dipetakan kepada garis kontrak harga tetap, satu garis jurnal dicipta hanya untuk kos.</span><span class="sxs-lookup"><span data-stu-id="6270e-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="6270e-121">Logik untuk memasukkan harga lalai bagi perbelanjaan adalah berdasarkan pada kategori perbelanjaan yang dipilih pada halaman **Entri perbelanjaan**.</span><span class="sxs-lookup"><span data-stu-id="6270e-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="6270e-122">Tarikh transaksi, baris kontrak yang projek dipetakan dan mata wang semuanya digunakan untuk menentukan senarai harga bersesuaian.</span><span class="sxs-lookup"><span data-stu-id="6270e-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="6270e-123">Walau bagaimanapun, untuk harga itu sendiri, jumlah yang pengguna masukkan ditetapkan secara langsung pada garisan jurnal perbelanjaan berkaitan untuk kos dan jualan secara lalai.</span><span class="sxs-lookup"><span data-stu-id="6270e-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="6270e-124">Dalam versi terkini PSA, entri berasaskan kategori setiap unit harga lalai pada entri perbelanjaan tidak tersedia.</span><span class="sxs-lookup"><span data-stu-id="6270e-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="6270e-125">Menggunakan jurnal Entri untuk merekodkan kos</span><span class="sxs-lookup"><span data-stu-id="6270e-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="6270e-126">Di PSA, jurnal entri membolehkan anda merekodkan kos atau hasil dalam kelas transaksi bahan, yuran, masa, perbelanjaan, atau cukai.</span><span class="sxs-lookup"><span data-stu-id="6270e-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="6270e-127">Jurnal mempunyai pengepala, baris dan tindakan **Sahkan**.</span><span class="sxs-lookup"><span data-stu-id="6270e-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="6270e-128">Berikut ialah beberapa senario di mana anda mungkin menggunakan jurnal:</span><span class="sxs-lookup"><span data-stu-id="6270e-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="6270e-129">Anda mesti merakam kos aktual bahan dan jualan pada projek.</span><span class="sxs-lookup"><span data-stu-id="6270e-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="6270e-130">Anda mesti mengalihkan transaksi aktual daripada sistem lain ke PSA.</span><span class="sxs-lookup"><span data-stu-id="6270e-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="6270e-131">Anda mesti merekodkan kos yang berlaku dalam sistem lain, seperti kos perolehan atau subkontrak.</span><span class="sxs-lookup"><span data-stu-id="6270e-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6270e-132">Menggunakan jurnal Entri untuk mewujudkan aktual hanya boleh dilakukan oleh pengguna yang menyedari sepenuhnya kesan perakaunan yang terdapat pada aktual terhadap projek tersebut.</span><span class="sxs-lookup"><span data-stu-id="6270e-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="6270e-133">Ini kerana aplikasi tidak mengesahkan jenis garisan jurnal, atau penentuan harga berkaitan yang dimasukkan pada garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="6270e-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="6270e-134">Disebabkan oleh kesan jenis jurnal ini, beri perhatian yang mencukupi kepada orang yang diberikan akses untuk mencipta jurnal Entri.</span><span class="sxs-lookup"><span data-stu-id="6270e-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="6270e-135">Merekod aktual berdasarkan peristiwa projek</span><span class="sxs-lookup"><span data-stu-id="6270e-135">Recording actuals based on project events</span></span>

<span data-ttu-id="6270e-136">PSA merekod transaksi kewangan yang berlaku semasa projek.</span><span class="sxs-lookup"><span data-stu-id="6270e-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="6270e-137">Transaksi ini direkodkan sebagai **aktual**.</span><span class="sxs-lookup"><span data-stu-id="6270e-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="6270e-138">Jadual berikut menunjukkan jenis aktual berbeza yang dicipta, bergantung pada sama ada projek itu adalah projek masa dan bahan atau projek harga tetap, dalam peringkat prajualan, atau merupakan projek dalaman.</span><span class="sxs-lookup"><span data-stu-id="6270e-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="6270e-139">**Sumber tersebut tergolong dalam unit organisasi yang sama seperti unit kontrak projek**</span><span class="sxs-lookup"><span data-stu-id="6270e-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="6270e-140">Peristiwa</span><span class="sxs-lookup"><span data-stu-id="6270e-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="6270e-141">Projek boleh dibilkan atau dijual</span><span class="sxs-lookup"><span data-stu-id="6270e-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="6270e-142">Projek dalam peringkat prajualan</span><span class="sxs-lookup"><span data-stu-id="6270e-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="6270e-143">Projek dalaman</span><span class="sxs-lookup"><span data-stu-id="6270e-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="6270e-144">Masa dan bahan</span><span class="sxs-lookup"><span data-stu-id="6270e-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="6270e-145">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="6270e-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="6270e-146">Sebenar</span><span class="sxs-lookup"><span data-stu-id="6270e-146">Actuals</span></span></th>
<th><span data-ttu-id="6270e-147">Mata wang transaksi</span><span class="sxs-lookup"><span data-stu-id="6270e-147">Transaction currency</span></span></th>
<th><span data-ttu-id="6270e-148">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="6270e-148">Fixed price</span></span></th>
<th><span data-ttu-id="6270e-149">Mata wang transaksi</span><span class="sxs-lookup"><span data-stu-id="6270e-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6270e-150">Entri masa dicipta.</span><span class="sxs-lookup"><span data-stu-id="6270e-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="6270e-151">Tiada aktiviti dalam entiti Aktual</span><span class="sxs-lookup"><span data-stu-id="6270e-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6270e-152">Entri masa diserahkan.</span><span class="sxs-lookup"><span data-stu-id="6270e-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="6270e-153">Tiada aktiviti dalam entiti Aktual</span><span class="sxs-lookup"><span data-stu-id="6270e-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6270e-154">Masa telah diluluskan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku semasa kelulusan.</span><span class="sxs-lookup"><span data-stu-id="6270e-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="6270e-155">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="6270e-155">Cost actual</span></span></td>
<td><span data-ttu-id="6270e-156">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="6270e-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6270e-157">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="6270e-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="6270e-158">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="6270e-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="6270e-159">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="6270e-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="6270e-160">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="6270e-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6270e-161">Jualan belum dibilkan sebenar – Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="6270e-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="6270e-162">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6270e-163">Masa telah diluluskan dan tiada pengurangan dalam masa boleh dibilkan berlaku semasa kelulusan.</span><span class="sxs-lookup"><span data-stu-id="6270e-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="6270e-164">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="6270e-164">Cost actual</span></span></td>
<td><span data-ttu-id="6270e-165">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="6270e-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="6270e-166">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="6270e-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="6270e-167">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="6270e-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="6270e-168">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="6270e-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="6270e-169">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="6270e-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6270e-170">Jualan belum dibilkan sebenar – Boleh dituntut untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="6270e-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="6270e-171">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6270e-172">Jualan belum dibilkan sebenar – Tidak boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="6270e-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="6270e-173">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6270e-174">Invois disahkan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku.</span><span class="sxs-lookup"><span data-stu-id="6270e-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="6270e-175">Pengunduran jualan belum dibilkan</span><span class="sxs-lookup"><span data-stu-id="6270e-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="6270e-176">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6270e-177">Jualan dibilkan untuk pencapaian</span><span class="sxs-lookup"><span data-stu-id="6270e-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="6270e-178">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6270e-179">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="6270e-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="6270e-180">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="6270e-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6270e-181">Jualan dibilkan</span><span class="sxs-lookup"><span data-stu-id="6270e-181">Billed sales</span></span></td>
<td><span data-ttu-id="6270e-182">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6270e-183">Invois disahkan dan pengurangan dalam masa boleh dibilkan berlaku.</span><span class="sxs-lookup"><span data-stu-id="6270e-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="6270e-184">Pengunduran jualan belum dibilkan</span><span class="sxs-lookup"><span data-stu-id="6270e-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="6270e-185">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="6270e-186">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="6270e-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6270e-187">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="6270e-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6270e-188">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="6270e-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6270e-189">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="6270e-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6270e-190">Jualan dibilkan – Boleh dituntut untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="6270e-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="6270e-191">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6270e-192">Jualan dibilkan – Tidak boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="6270e-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="6270e-193">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6270e-194">Invois dibetulkan untuk menambah kuantiti yang boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="6270e-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="6270e-195">Julana dibilkan – Pengunduran</span><span class="sxs-lookup"><span data-stu-id="6270e-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="6270e-196">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="6270e-197">Pengunduran jualan dibilkan untuk pencapaian</span><span class="sxs-lookup"><span data-stu-id="6270e-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="6270e-198">Penukarang status pencapaian daripada <strong>Diinvoiskan</strong> kepada <strong>Sedia untuk invois</strong></span><span class="sxs-lookup"><span data-stu-id="6270e-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="6270e-199">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="6270e-200">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="6270e-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="6270e-201">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="6270e-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6270e-202">Jualan dibilkan</span><span class="sxs-lookup"><span data-stu-id="6270e-202">Billed sales</span></span></td>
<td><span data-ttu-id="6270e-203">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6270e-204">Invois dibetulkan untuk mengurangkan kuantiti yang boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="6270e-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="6270e-205">Julana dibilkan – Pengunduran</span><span class="sxs-lookup"><span data-stu-id="6270e-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="6270e-206">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6270e-207">Jualan dibilkan untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="6270e-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="6270e-208">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6270e-209">Jualan tidak dibilkan – Boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="6270e-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="6270e-210">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6270e-211">**Sumber tersebut tergolong dalam unit organisasi yang berbeza daripada unit kontrak projek**</span><span class="sxs-lookup"><span data-stu-id="6270e-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="6270e-212">Peristiwa</span><span class="sxs-lookup"><span data-stu-id="6270e-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="6270e-213">Projek boleh dibilkan atau dijual</span><span class="sxs-lookup"><span data-stu-id="6270e-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="6270e-214">Projek dalam peringkat prajualan</span><span class="sxs-lookup"><span data-stu-id="6270e-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="6270e-215">Projek dalaman</span><span class="sxs-lookup"><span data-stu-id="6270e-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="6270e-216">Masa dan bahan</span><span class="sxs-lookup"><span data-stu-id="6270e-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="6270e-217">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="6270e-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="6270e-218">Sebenar</span><span class="sxs-lookup"><span data-stu-id="6270e-218">Actuals</span></span></th>
<th><span data-ttu-id="6270e-219">Mata wang transaksi</span><span class="sxs-lookup"><span data-stu-id="6270e-219">Transaction currency</span></span></th>
<th><span data-ttu-id="6270e-220">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="6270e-220">Fixed price</span></span></th>
<th><span data-ttu-id="6270e-221">Mata wang transaksi</span><span class="sxs-lookup"><span data-stu-id="6270e-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6270e-222">Entri masa dicipta.</span><span class="sxs-lookup"><span data-stu-id="6270e-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="6270e-223">Tiada aktiviti dalam entiti Aktual</span><span class="sxs-lookup"><span data-stu-id="6270e-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6270e-224">Entri masa diserahkan.</span><span class="sxs-lookup"><span data-stu-id="6270e-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="6270e-225">Tiada aktiviti dalam entiti Aktual</span><span class="sxs-lookup"><span data-stu-id="6270e-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="6270e-226">Masa telah diluluskan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku semasa kelulusan.</span><span class="sxs-lookup"><span data-stu-id="6270e-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="6270e-227">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="6270e-227">Cost actual</span></span></td>
<td><span data-ttu-id="6270e-228">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="6270e-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="6270e-229">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="6270e-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="6270e-230">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="6270e-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="6270e-231">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="6270e-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="6270e-232">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="6270e-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6270e-233">Jualan belum dibilkan sebenar – Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="6270e-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="6270e-234">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6270e-235">Kos unit persumberan</span><span class="sxs-lookup"><span data-stu-id="6270e-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="6270e-236">Mata wang unit persumberan</span><span class="sxs-lookup"><span data-stu-id="6270e-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6270e-237">Jualan antara organisasi</span><span class="sxs-lookup"><span data-stu-id="6270e-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="6270e-238">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="6270e-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="6270e-239">Masa telah diluluskan dan tiada pengurangan dalam masa boleh dibilkan berlaku semasa kelulusan.</span><span class="sxs-lookup"><span data-stu-id="6270e-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="6270e-240">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="6270e-240">Cost actual</span></span></td>
<td><span data-ttu-id="6270e-241">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="6270e-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="6270e-242">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="6270e-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="6270e-243">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="6270e-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="6270e-244">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="6270e-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="6270e-245">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="6270e-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6270e-246">Kos unit persumberan</span><span class="sxs-lookup"><span data-stu-id="6270e-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="6270e-247">Mata wang unit persumberan</span><span class="sxs-lookup"><span data-stu-id="6270e-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6270e-248">Jualan antara organisasi</span><span class="sxs-lookup"><span data-stu-id="6270e-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="6270e-249">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="6270e-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6270e-250">Jualan belum dibilkan sebenar – Boleh dituntut untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="6270e-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="6270e-251">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6270e-252">Jualan belum dibilkan sebenar – Tidak boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="6270e-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="6270e-253">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6270e-254">Invois disahkan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku.</span><span class="sxs-lookup"><span data-stu-id="6270e-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="6270e-255">Pengunduran jualan belum dibilkan</span><span class="sxs-lookup"><span data-stu-id="6270e-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="6270e-256">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6270e-257">Jualan dibilkan untuk pencapaian</span><span class="sxs-lookup"><span data-stu-id="6270e-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="6270e-258">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6270e-259">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="6270e-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="6270e-260">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="6270e-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6270e-261">Jualan dibilkan</span><span class="sxs-lookup"><span data-stu-id="6270e-261">Billed sales</span></span></td>
<td><span data-ttu-id="6270e-262">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6270e-263">Invois disahkan dan pengurangan dalam masa boleh dibilkan berlaku.</span><span class="sxs-lookup"><span data-stu-id="6270e-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="6270e-264">Pengunduran jualan belum dibilkan</span><span class="sxs-lookup"><span data-stu-id="6270e-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="6270e-265">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="6270e-266">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="6270e-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6270e-267">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="6270e-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6270e-268">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="6270e-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6270e-269">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="6270e-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6270e-270">Jualan dibilkan – Boleh dituntut untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="6270e-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="6270e-271">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6270e-272">Jualan dibilkan – Tidak boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="6270e-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="6270e-273">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6270e-274">Invois dibetulkan untuk menambah kuantiti yang boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="6270e-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="6270e-275">Julana dibilkan – Pengunduran</span><span class="sxs-lookup"><span data-stu-id="6270e-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="6270e-276">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="6270e-277">Pengunduran jualan dibilkan untuk pencapaian</span><span class="sxs-lookup"><span data-stu-id="6270e-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="6270e-278">Penukarang status pencapaian daripada <strong>Diinvoiskan</strong> kepada <strong>Sedia untuk invois</strong></span><span class="sxs-lookup"><span data-stu-id="6270e-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="6270e-279">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="6270e-280">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="6270e-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="6270e-281">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="6270e-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6270e-282">Jualan dibilkan</span><span class="sxs-lookup"><span data-stu-id="6270e-282">Billed sales</span></span></td>
<td><span data-ttu-id="6270e-283">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6270e-284">Invois dibetulkan untuk mengurangkan kuantiti yang boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="6270e-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="6270e-285">Julana dibilkan – Pengunduran</span><span class="sxs-lookup"><span data-stu-id="6270e-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="6270e-286">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6270e-287">Jualan dibilkan untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="6270e-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="6270e-288">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6270e-289">Jualan tidak dibilkan – Boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="6270e-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="6270e-290">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="6270e-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
