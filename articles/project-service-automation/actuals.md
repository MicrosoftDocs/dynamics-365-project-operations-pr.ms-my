---
title: Sebenar
description: Topik ini memberikan maklumat tentang aktual projek.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753968"
---
# <a name="actuals"></a><span data-ttu-id="bb2f2-103">Sebenar</span><span class="sxs-lookup"><span data-stu-id="bb2f2-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="bb2f2-104">Aktual ialah jumlah kerja yang telah disiapkan pada sebuah projek.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="bb2f2-105">Aktual projek boleh dikesan kembali kepada dokumen sumber mereka.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="bb2f2-106">Dokumen sumber tersebut termasuk entri masa, perbelanjaan dan jurnal dan serta invois.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Cara aktual projek dikesan untuk mendapatkan dokumen sumber](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="bb2f2-108">Menyerahkan entri masa</span><span class="sxs-lookup"><span data-stu-id="bb2f2-108">Submitting a time entry</span></span>

<span data-ttu-id="bb2f2-109">Dalam PSA, apabila entri masa telah diserahkan untuk projek yang dipetakan kepada garis kontrak masa dan bahan, dua garisan jurnal dicipta.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="bb2f2-110">Satu garis ialah untuk kos, dan garis lain ialah untuk jualan yang tidak dibilkan.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="bb2f2-111">Apabila entri masa telah diserahkan untuk projek yang dipetakan kepada garis kontrak harga tetap, satu garis jurnal dicipta hanya untuk kos.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="bb2f2-112">Logik untuk memasukkan harga lalai pada garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="bb2f2-113">Semua nilai medan daripada entri masa disalin ke garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="bb2f2-114">Medan-medan ini termasuk tarikh transaksi, baris kontrak yang projek dipetakan dan keputusan mata wang dalam senarai harga bersesuaian.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="bb2f2-115">Medan-medan yang menjejaskan harga lalai, seperti **Peranan** dan **Unit Organisasi**, menyebabkan harga bersesuaian akan dimasukkan secara lalai pada garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="bb2f2-116">Jika anda menambah medan tersuai pada entri masa dan anda mahu nilai medan disebarkan kepada aktual, cipta medan pada entiti Aktual dan gunakan pemetaan medan untuk menyalin medan daripada entri masa kepada aktual.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="bb2f2-117">Menyerahkan entri perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-117">Submitting an expense entry</span></span>

<span data-ttu-id="bb2f2-118">Dalam PSA, apabila entri perbelanjaan telah diserahkan untuk projek yang dipetakan kepada garis kontrak masa dan bahan, dua garisan jurnal dicipta.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="bb2f2-119">Satu garis ialah untuk kos, dan garis lain ialah untuk jualan yang tidak dibilkan.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="bb2f2-120">Apabila entri perbelanjaan telah diserahkan untuk projek yang dipetakan kepada garis kontrak harga tetap, satu garis jurnal dicipta hanya untuk kos.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="bb2f2-121">Logik untuk memasukkan harga lalai bagi perbelanjaan adalah berdasarkan pada kategori perbelanjaan yang dipilih pada halaman **Entri perbelanjaan**.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="bb2f2-122">Tarikh transaksi, baris kontrak yang projek dipetakan dan mata wang semuanya digunakan untuk menentukan senarai harga bersesuaian.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="bb2f2-123">Walau bagaimanapun, untuk harga itu sendiri, jumlah yang pengguna masukkan ditetapkan secara langsung pada garisan jurnal perbelanjaan berkaitan untuk kos dan jualan secara lalai.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="bb2f2-124">Dalam versi terkini PSA, entri berasaskan kategori setiap unit harga lalai pada entri perbelanjaan tidak tersedia.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="bb2f2-125">Menggunakan jurnal untuk merekodkan kos</span><span class="sxs-lookup"><span data-stu-id="bb2f2-125">Using journals to record costs</span></span>

<span data-ttu-id="bb2f2-126">Dalam PSA, jurnal membenarkan anda merekodkan kos atau pendapatan dalam bahan, yuran, masa, perbelanjaan atau kelas-kelas transaksi cukai.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="bb2f2-127">Jurnal mempunyai pengepala, baris dan tindakan **Sahkan**.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="bb2f2-128">Berikut ialah beberapa senario di mana anda mungkin menggunakan jurnal:</span><span class="sxs-lookup"><span data-stu-id="bb2f2-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="bb2f2-129">Anda mesti merakam kos aktual bahan dan jualan pada projek.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="bb2f2-130">Anda mesti mengalihkan transaksi aktual daripada sistem lain ke PSA.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="bb2f2-131">Anda mesti merekodkan kos yang berlaku dalam sistem lain, seperti kos perolehan atau subkontrak.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="bb2f2-132">Merekod aktual berdasarkan peristiwa projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-132">Recording actuals based on project events</span></span>

<span data-ttu-id="bb2f2-133">PSA merekod transaksi kewangan yang berlaku semasa projek.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="bb2f2-134">Transaksi ini direkodkan sebagai **aktual**.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="bb2f2-135">Jadual berikut menunjukkan jenis aktual berbeza yang dicipta, bergantung pada sama ada projek itu adalah projek masa dan bahan atau projek harga tetap, dalam peringkat prajualan, atau merupakan projek dalaman.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="bb2f2-136">**Sumber tersebut tergolong dalam unit organisasi yang sama seperti unit kontrak projek**</span><span class="sxs-lookup"><span data-stu-id="bb2f2-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="bb2f2-137">Peristiwa</span><span class="sxs-lookup"><span data-stu-id="bb2f2-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="bb2f2-138">Projek boleh dibilkan atau dijual</span><span class="sxs-lookup"><span data-stu-id="bb2f2-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="bb2f2-139">Projek dalam peringkat prajualan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="bb2f2-140">Projek dalaman</span><span class="sxs-lookup"><span data-stu-id="bb2f2-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="bb2f2-141">Masa dan bahan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="bb2f2-142">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="bb2f2-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="bb2f2-143">Sebenar</span><span class="sxs-lookup"><span data-stu-id="bb2f2-143">Actuals</span></span></th>
<th><span data-ttu-id="bb2f2-144">Mata wang transaksi</span><span class="sxs-lookup"><span data-stu-id="bb2f2-144">Transaction currency</span></span></th>
<th><span data-ttu-id="bb2f2-145">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="bb2f2-145">Fixed price</span></span></th>
<th><span data-ttu-id="bb2f2-146">Mata wang transaksi</span><span class="sxs-lookup"><span data-stu-id="bb2f2-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bb2f2-147">Entri masa dicipta.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="bb2f2-148">Tiada aktiviti dalam entiti Aktual</span><span class="sxs-lookup"><span data-stu-id="bb2f2-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb2f2-149">Entri masa diserahkan.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="bb2f2-150">Tiada aktiviti dalam entiti Aktual</span><span class="sxs-lookup"><span data-stu-id="bb2f2-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="bb2f2-151">Masa telah diluluskan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku semasa kelulusan.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="bb2f2-152">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="bb2f2-152">Cost actual</span></span></td>
<td><span data-ttu-id="bb2f2-153">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="bb2f2-154">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="bb2f2-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="bb2f2-155">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="bb2f2-156">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="bb2f2-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="bb2f2-157">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="bb2f2-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb2f2-158">Jualan belum dibilkan sebenar – Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="bb2f2-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="bb2f2-159">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="bb2f2-160">Masa telah diluluskan dan tiada pengurangan dalam masa boleh dibilkan berlaku semasa kelulusan.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="bb2f2-161">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="bb2f2-161">Cost actual</span></span></td>
<td><span data-ttu-id="bb2f2-162">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="bb2f2-163">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="bb2f2-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="bb2f2-164">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="bb2f2-165">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="bb2f2-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="bb2f2-166">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="bb2f2-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb2f2-167">Jualan belum dibilkan sebenar – Boleh dituntut untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="bb2f2-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="bb2f2-168">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb2f2-169">Jualan belum dibilkan sebenar – Tidak boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="bb2f2-170">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="bb2f2-171">Invois disahkan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="bb2f2-172">Pengunduran jualan belum dibilkan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="bb2f2-173">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="bb2f2-174">Jualan dibilkan untuk pencapaian</span><span class="sxs-lookup"><span data-stu-id="bb2f2-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="bb2f2-175">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="bb2f2-176">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="bb2f2-177">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb2f2-178">Jualan dibilkan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-178">Billed sales</span></span></td>
<td><span data-ttu-id="bb2f2-179">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="bb2f2-180">Invois disahkan dan pengurangan dalam masa boleh dibilkan berlaku.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="bb2f2-181">Pengunduran jualan belum dibilkan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="bb2f2-182">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="bb2f2-183">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="bb2f2-184">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="bb2f2-185">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="bb2f2-186">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb2f2-187">Jualan dibilkan – Boleh dituntut untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="bb2f2-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="bb2f2-188">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb2f2-189">Jualan dibilkan – Tidak boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="bb2f2-190">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="bb2f2-191">Invois dibetulkan untuk menambah kuantiti yang boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="bb2f2-192">Julana dibilkan – Pengunduran</span><span class="sxs-lookup"><span data-stu-id="bb2f2-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="bb2f2-193">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="bb2f2-194">Pengunduran jualan dibilkan untuk pencapaian</span><span class="sxs-lookup"><span data-stu-id="bb2f2-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="bb2f2-195">Penukarang status pencapaian daripada <strong>Diinvoiskan</strong> kepada <strong>Sedia untuk invois</strong></span><span class="sxs-lookup"><span data-stu-id="bb2f2-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="bb2f2-196">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="bb2f2-197">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="bb2f2-198">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb2f2-199">Jualan dibilkan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-199">Billed sales</span></span></td>
<td><span data-ttu-id="bb2f2-200">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="bb2f2-201">Invois dibetulkan untuk mengurangkan kuantiti yang boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="bb2f2-202">Julana dibilkan – Pengunduran</span><span class="sxs-lookup"><span data-stu-id="bb2f2-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="bb2f2-203">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb2f2-204">Jualan dibilkan untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="bb2f2-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="bb2f2-205">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb2f2-206">Jualan tidak dibilkan – Boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="bb2f2-207">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bb2f2-208">**Sumber tersebut tergolong dalam unit organisasi yang berbeza daripada unit kontrak projek**</span><span class="sxs-lookup"><span data-stu-id="bb2f2-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="bb2f2-209">Peristiwa</span><span class="sxs-lookup"><span data-stu-id="bb2f2-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="bb2f2-210">Projek boleh dibilkan atau dijual</span><span class="sxs-lookup"><span data-stu-id="bb2f2-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="bb2f2-211">Projek dalam peringkat prajualan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="bb2f2-212">Projek dalaman</span><span class="sxs-lookup"><span data-stu-id="bb2f2-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="bb2f2-213">Masa dan bahan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="bb2f2-214">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="bb2f2-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="bb2f2-215">Sebenar</span><span class="sxs-lookup"><span data-stu-id="bb2f2-215">Actuals</span></span></th>
<th><span data-ttu-id="bb2f2-216">Mata wang transaksi</span><span class="sxs-lookup"><span data-stu-id="bb2f2-216">Transaction currency</span></span></th>
<th><span data-ttu-id="bb2f2-217">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="bb2f2-217">Fixed price</span></span></th>
<th><span data-ttu-id="bb2f2-218">Mata wang transaksi</span><span class="sxs-lookup"><span data-stu-id="bb2f2-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bb2f2-219">Entri masa dicipta.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="bb2f2-220">Tiada aktiviti dalam entiti Aktual</span><span class="sxs-lookup"><span data-stu-id="bb2f2-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb2f2-221">Entri masa diserahkan.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="bb2f2-222">Tiada aktiviti dalam entiti Aktual</span><span class="sxs-lookup"><span data-stu-id="bb2f2-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="bb2f2-223">Masa telah diluluskan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku semasa kelulusan.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="bb2f2-224">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="bb2f2-224">Cost actual</span></span></td>
<td><span data-ttu-id="bb2f2-225">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="bb2f2-226">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="bb2f2-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="bb2f2-227">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="bb2f2-228">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="bb2f2-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="bb2f2-229">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="bb2f2-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb2f2-230">Jualan belum dibilkan sebenar – Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="bb2f2-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="bb2f2-231">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb2f2-232">Kos unit persumberan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="bb2f2-233">Mata wang unit persumberan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb2f2-234">Jualan antara organisasi</span><span class="sxs-lookup"><span data-stu-id="bb2f2-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="bb2f2-235">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="bb2f2-236">Masa telah diluluskan dan tiada pengurangan dalam masa boleh dibilkan berlaku semasa kelulusan.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="bb2f2-237">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="bb2f2-237">Cost actual</span></span></td>
<td><span data-ttu-id="bb2f2-238">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="bb2f2-239">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="bb2f2-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="bb2f2-240">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="bb2f2-241">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="bb2f2-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="bb2f2-242">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="bb2f2-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb2f2-243">Kos unit persumberan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="bb2f2-244">Mata wang unit persumberan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb2f2-245">Jualan antara organisasi</span><span class="sxs-lookup"><span data-stu-id="bb2f2-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="bb2f2-246">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb2f2-247">Jualan belum dibilkan sebenar – Boleh dituntut untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="bb2f2-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="bb2f2-248">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb2f2-249">Jualan belum dibilkan sebenar – Tidak boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="bb2f2-250">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="bb2f2-251">Invois disahkan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="bb2f2-252">Pengunduran jualan belum dibilkan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="bb2f2-253">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="bb2f2-254">Jualan dibilkan untuk pencapaian</span><span class="sxs-lookup"><span data-stu-id="bb2f2-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="bb2f2-255">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="bb2f2-256">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="bb2f2-257">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb2f2-258">Jualan dibilkan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-258">Billed sales</span></span></td>
<td><span data-ttu-id="bb2f2-259">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="bb2f2-260">Invois disahkan dan pengurangan dalam masa boleh dibilkan berlaku.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="bb2f2-261">Pengunduran jualan belum dibilkan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="bb2f2-262">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="bb2f2-263">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="bb2f2-264">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="bb2f2-265">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="bb2f2-266">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb2f2-267">Jualan dibilkan – Boleh dituntut untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="bb2f2-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="bb2f2-268">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb2f2-269">Jualan dibilkan – Tidak boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="bb2f2-270">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="bb2f2-271">Invois dibetulkan untuk menambah kuantiti yang boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="bb2f2-272">Julana dibilkan – Pengunduran</span><span class="sxs-lookup"><span data-stu-id="bb2f2-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="bb2f2-273">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="bb2f2-274">Pengunduran jualan dibilkan untuk pencapaian</span><span class="sxs-lookup"><span data-stu-id="bb2f2-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="bb2f2-275">Penukarang status pencapaian daripada <strong>Diinvoiskan</strong> kepada <strong>Sedia untuk invois</strong></span><span class="sxs-lookup"><span data-stu-id="bb2f2-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="bb2f2-276">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="bb2f2-277">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="bb2f2-278">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb2f2-279">Jualan dibilkan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-279">Billed sales</span></span></td>
<td><span data-ttu-id="bb2f2-280">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="bb2f2-281">Invois dibetulkan untuk mengurangkan kuantiti yang boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="bb2f2-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="bb2f2-282">Julana dibilkan – Pengunduran</span><span class="sxs-lookup"><span data-stu-id="bb2f2-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="bb2f2-283">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb2f2-284">Jualan dibilkan untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="bb2f2-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="bb2f2-285">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bb2f2-286">Jualan tidak dibilkan – Boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="bb2f2-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="bb2f2-287">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="bb2f2-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
