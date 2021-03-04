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
ms.openlocfilehash: 63ad6544f0ec0a893aebd8d81f3ee895e51c294e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146134"
---
# <a name="actuals-overview"></a><span data-ttu-id="29289-103">Gambaran keseluruhan aktual</span><span class="sxs-lookup"><span data-stu-id="29289-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="29289-104">Aktual ialah jumlah kerja yang telah disiapkan pada sebuah projek.</span><span class="sxs-lookup"><span data-stu-id="29289-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="29289-105">Aktual projek boleh dikesan kembali kepada dokumen sumber mereka.</span><span class="sxs-lookup"><span data-stu-id="29289-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="29289-106">Dokumen sumber tersebut termasuk entri masa, perbelanjaan dan jurnal dan serta invois.</span><span class="sxs-lookup"><span data-stu-id="29289-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Cara aktual projek dikesan untuk mendapatkan dokumen sumber](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="29289-108">Menyerahkan entri masa</span><span class="sxs-lookup"><span data-stu-id="29289-108">Submitting a time entry</span></span>

<span data-ttu-id="29289-109">Dalam PSA, apabila entri masa telah diserahkan untuk projek yang dipetakan kepada garis kontrak masa dan bahan, dua garisan jurnal dicipta.</span><span class="sxs-lookup"><span data-stu-id="29289-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="29289-110">Satu garis ialah untuk kos, dan garis lain ialah untuk jualan yang tidak dibilkan.</span><span class="sxs-lookup"><span data-stu-id="29289-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="29289-111">Apabila entri masa telah diserahkan untuk projek yang dipetakan kepada garis kontrak harga tetap, satu garis jurnal dicipta hanya untuk kos.</span><span class="sxs-lookup"><span data-stu-id="29289-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="29289-112">Logik untuk memasukkan harga lalai pada garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="29289-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="29289-113">Semua nilai medan daripada entri masa disalin ke garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="29289-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="29289-114">Medan-medan ini termasuk tarikh transaksi, baris kontrak yang projek dipetakan dan keputusan mata wang dalam senarai harga bersesuaian.</span><span class="sxs-lookup"><span data-stu-id="29289-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="29289-115">Medan-medan yang menjejaskan harga lalai, seperti **Peranan** dan **Unit Organisasi**, menyebabkan harga bersesuaian akan dimasukkan secara lalai pada garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="29289-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="29289-116">Jika anda menambah medan tersuai pada entri masa dan anda mahu nilai medan disebarkan kepada aktual, cipta medan pada entiti Aktual dan gunakan pemetaan medan untuk menyalin medan daripada entri masa kepada aktual.</span><span class="sxs-lookup"><span data-stu-id="29289-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="29289-117">Menyerahkan entri perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="29289-117">Submitting an expense entry</span></span>

<span data-ttu-id="29289-118">Dalam PSA, apabila entri perbelanjaan telah diserahkan untuk projek yang dipetakan kepada garis kontrak masa dan bahan, dua garisan jurnal dicipta.</span><span class="sxs-lookup"><span data-stu-id="29289-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="29289-119">Satu garis ialah untuk kos, dan garis lain ialah untuk jualan yang tidak dibilkan.</span><span class="sxs-lookup"><span data-stu-id="29289-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="29289-120">Apabila entri perbelanjaan telah diserahkan untuk projek yang dipetakan kepada garis kontrak harga tetap, satu garis jurnal dicipta hanya untuk kos.</span><span class="sxs-lookup"><span data-stu-id="29289-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="29289-121">Logik untuk memasukkan harga lalai bagi perbelanjaan adalah berdasarkan pada kategori perbelanjaan yang dipilih pada halaman **Entri perbelanjaan**.</span><span class="sxs-lookup"><span data-stu-id="29289-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="29289-122">Tarikh transaksi, baris kontrak yang projek dipetakan dan mata wang semuanya digunakan untuk menentukan senarai harga bersesuaian.</span><span class="sxs-lookup"><span data-stu-id="29289-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="29289-123">Walau bagaimanapun, untuk harga itu sendiri, jumlah yang pengguna masukkan ditetapkan secara langsung pada garisan jurnal perbelanjaan berkaitan untuk kos dan jualan secara lalai.</span><span class="sxs-lookup"><span data-stu-id="29289-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="29289-124">Dalam versi terkini PSA, entri berasaskan kategori setiap unit harga lalai pada entri perbelanjaan tidak tersedia.</span><span class="sxs-lookup"><span data-stu-id="29289-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="29289-125">Menggunakan jurnal Entri untuk merekodkan kos</span><span class="sxs-lookup"><span data-stu-id="29289-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="29289-126">Di PSA, jurnal entri membolehkan anda merekodkan kos atau hasil dalam kelas transaksi bahan, yuran, masa, perbelanjaan, atau cukai.</span><span class="sxs-lookup"><span data-stu-id="29289-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="29289-127">Jurnal mempunyai pengepala, baris dan tindakan **Sahkan**.</span><span class="sxs-lookup"><span data-stu-id="29289-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="29289-128">Berikut ialah beberapa senario di mana anda mungkin menggunakan jurnal:</span><span class="sxs-lookup"><span data-stu-id="29289-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="29289-129">Anda mesti merakam kos aktual bahan dan jualan pada projek.</span><span class="sxs-lookup"><span data-stu-id="29289-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="29289-130">Anda mesti mengalihkan transaksi aktual daripada sistem lain ke PSA.</span><span class="sxs-lookup"><span data-stu-id="29289-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="29289-131">Anda mesti merekodkan kos yang berlaku dalam sistem lain, seperti kos perolehan atau subkontrak.</span><span class="sxs-lookup"><span data-stu-id="29289-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="29289-132">Menggunakan jurnal Entri untuk mewujudkan aktual hanya boleh dilakukan oleh pengguna yang menyedari sepenuhnya kesan perakaunan yang terdapat pada aktual terhadap projek tersebut.</span><span class="sxs-lookup"><span data-stu-id="29289-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="29289-133">Ini kerana aplikasi tidak mengesahkan jenis garisan jurnal, atau penentuan harga berkaitan yang dimasukkan pada garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="29289-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="29289-134">Disebabkan oleh kesan jenis jurnal ini, beri perhatian yang mencukupi kepada orang yang diberikan akses untuk mencipta jurnal Entri.</span><span class="sxs-lookup"><span data-stu-id="29289-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="29289-135">Merekod aktual berdasarkan peristiwa projek</span><span class="sxs-lookup"><span data-stu-id="29289-135">Recording actuals based on project events</span></span>

<span data-ttu-id="29289-136">PSA merekod transaksi kewangan yang berlaku semasa projek.</span><span class="sxs-lookup"><span data-stu-id="29289-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="29289-137">Transaksi ini direkodkan sebagai **aktual**.</span><span class="sxs-lookup"><span data-stu-id="29289-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="29289-138">Jadual berikut menunjukkan jenis aktual berbeza yang dicipta, bergantung pada sama ada projek itu adalah projek masa dan bahan atau projek harga tetap, dalam peringkat prajualan, atau merupakan projek dalaman.</span><span class="sxs-lookup"><span data-stu-id="29289-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="29289-139">**Sumber tersebut tergolong dalam unit organisasi yang sama seperti unit kontrak projek**</span><span class="sxs-lookup"><span data-stu-id="29289-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="29289-140">Peristiwa</span><span class="sxs-lookup"><span data-stu-id="29289-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="29289-141">Projek boleh dibilkan atau dijual</span><span class="sxs-lookup"><span data-stu-id="29289-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="29289-142">Projek dalam peringkat prajualan</span><span class="sxs-lookup"><span data-stu-id="29289-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="29289-143">Projek dalaman</span><span class="sxs-lookup"><span data-stu-id="29289-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="29289-144">Masa dan bahan</span><span class="sxs-lookup"><span data-stu-id="29289-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="29289-145">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="29289-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="29289-146">Sebenar</span><span class="sxs-lookup"><span data-stu-id="29289-146">Actuals</span></span></th>
<th><span data-ttu-id="29289-147">Mata wang transaksi</span><span class="sxs-lookup"><span data-stu-id="29289-147">Transaction currency</span></span></th>
<th><span data-ttu-id="29289-148">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="29289-148">Fixed price</span></span></th>
<th><span data-ttu-id="29289-149">Mata wang transaksi</span><span class="sxs-lookup"><span data-stu-id="29289-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29289-150">Entri masa dicipta.</span><span class="sxs-lookup"><span data-stu-id="29289-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="29289-151">Tiada aktiviti dalam entiti Aktual</span><span class="sxs-lookup"><span data-stu-id="29289-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29289-152">Entri masa diserahkan.</span><span class="sxs-lookup"><span data-stu-id="29289-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="29289-153">Tiada aktiviti dalam entiti Aktual</span><span class="sxs-lookup"><span data-stu-id="29289-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="29289-154">Masa telah diluluskan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku semasa kelulusan.</span><span class="sxs-lookup"><span data-stu-id="29289-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="29289-155">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="29289-155">Cost actual</span></span></td>
<td><span data-ttu-id="29289-156">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="29289-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="29289-157">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="29289-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="29289-158">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="29289-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="29289-159">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="29289-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="29289-160">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="29289-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29289-161">Jualan belum dibilkan sebenar – Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="29289-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="29289-162">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="29289-163">Masa telah diluluskan dan tiada pengurangan dalam masa boleh dibilkan berlaku semasa kelulusan.</span><span class="sxs-lookup"><span data-stu-id="29289-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="29289-164">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="29289-164">Cost actual</span></span></td>
<td><span data-ttu-id="29289-165">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="29289-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="29289-166">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="29289-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="29289-167">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="29289-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="29289-168">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="29289-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="29289-169">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="29289-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29289-170">Jualan belum dibilkan sebenar – Boleh dituntut untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="29289-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="29289-171">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29289-172">Jualan belum dibilkan sebenar – Tidak boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="29289-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="29289-173">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="29289-174">Invois disahkan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku.</span><span class="sxs-lookup"><span data-stu-id="29289-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="29289-175">Pengunduran jualan belum dibilkan</span><span class="sxs-lookup"><span data-stu-id="29289-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="29289-176">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="29289-177">Jualan dibilkan untuk pencapaian</span><span class="sxs-lookup"><span data-stu-id="29289-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="29289-178">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="29289-179">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="29289-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="29289-180">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="29289-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29289-181">Jualan dibilkan</span><span class="sxs-lookup"><span data-stu-id="29289-181">Billed sales</span></span></td>
<td><span data-ttu-id="29289-182">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="29289-183">Invois disahkan dan pengurangan dalam masa boleh dibilkan berlaku.</span><span class="sxs-lookup"><span data-stu-id="29289-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="29289-184">Pengunduran jualan belum dibilkan</span><span class="sxs-lookup"><span data-stu-id="29289-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="29289-185">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="29289-186">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="29289-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="29289-187">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="29289-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="29289-188">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="29289-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="29289-189">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="29289-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29289-190">Jualan dibilkan – Boleh dituntut untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="29289-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="29289-191">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29289-192">Jualan dibilkan – Tidak boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="29289-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="29289-193">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="29289-194">Invois dibetulkan untuk menambah kuantiti yang boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="29289-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="29289-195">Julana dibilkan – Pengunduran</span><span class="sxs-lookup"><span data-stu-id="29289-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="29289-196">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="29289-197">Pengunduran jualan dibilkan untuk pencapaian</span><span class="sxs-lookup"><span data-stu-id="29289-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="29289-198">Penukarang status pencapaian daripada <strong>Diinvoiskan</strong> kepada <strong>Sedia untuk invois</strong></span><span class="sxs-lookup"><span data-stu-id="29289-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="29289-199">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="29289-200">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="29289-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="29289-201">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="29289-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29289-202">Jualan dibilkan</span><span class="sxs-lookup"><span data-stu-id="29289-202">Billed sales</span></span></td>
<td><span data-ttu-id="29289-203">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="29289-204">Invois dibetulkan untuk mengurangkan kuantiti yang boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="29289-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="29289-205">Julana dibilkan – Pengunduran</span><span class="sxs-lookup"><span data-stu-id="29289-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="29289-206">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29289-207">Jualan dibilkan untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="29289-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="29289-208">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29289-209">Jualan tidak dibilkan – Boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="29289-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="29289-210">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="29289-211">**Sumber tersebut tergolong dalam unit organisasi yang berbeza daripada unit kontrak projek**</span><span class="sxs-lookup"><span data-stu-id="29289-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="29289-212">Peristiwa</span><span class="sxs-lookup"><span data-stu-id="29289-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="29289-213">Projek boleh dibilkan atau dijual</span><span class="sxs-lookup"><span data-stu-id="29289-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="29289-214">Projek dalam peringkat prajualan</span><span class="sxs-lookup"><span data-stu-id="29289-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="29289-215">Projek dalaman</span><span class="sxs-lookup"><span data-stu-id="29289-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="29289-216">Masa dan bahan</span><span class="sxs-lookup"><span data-stu-id="29289-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="29289-217">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="29289-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="29289-218">Sebenar</span><span class="sxs-lookup"><span data-stu-id="29289-218">Actuals</span></span></th>
<th><span data-ttu-id="29289-219">Mata wang transaksi</span><span class="sxs-lookup"><span data-stu-id="29289-219">Transaction currency</span></span></th>
<th><span data-ttu-id="29289-220">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="29289-220">Fixed price</span></span></th>
<th><span data-ttu-id="29289-221">Mata wang transaksi</span><span class="sxs-lookup"><span data-stu-id="29289-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29289-222">Entri masa dicipta.</span><span class="sxs-lookup"><span data-stu-id="29289-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="29289-223">Tiada aktiviti dalam entiti Aktual</span><span class="sxs-lookup"><span data-stu-id="29289-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29289-224">Entri masa diserahkan.</span><span class="sxs-lookup"><span data-stu-id="29289-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="29289-225">Tiada aktiviti dalam entiti Aktual</span><span class="sxs-lookup"><span data-stu-id="29289-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="29289-226">Masa telah diluluskan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku semasa kelulusan.</span><span class="sxs-lookup"><span data-stu-id="29289-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="29289-227">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="29289-227">Cost actual</span></span></td>
<td><span data-ttu-id="29289-228">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="29289-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="29289-229">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="29289-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="29289-230">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="29289-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="29289-231">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="29289-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="29289-232">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="29289-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29289-233">Jualan belum dibilkan sebenar – Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="29289-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="29289-234">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29289-235">Kos unit persumberan</span><span class="sxs-lookup"><span data-stu-id="29289-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="29289-236">Mata wang unit persumberan</span><span class="sxs-lookup"><span data-stu-id="29289-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29289-237">Jualan antara organisasi</span><span class="sxs-lookup"><span data-stu-id="29289-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="29289-238">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="29289-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="29289-239">Masa telah diluluskan dan tiada pengurangan dalam masa boleh dibilkan berlaku semasa kelulusan.</span><span class="sxs-lookup"><span data-stu-id="29289-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="29289-240">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="29289-240">Cost actual</span></span></td>
<td><span data-ttu-id="29289-241">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="29289-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="29289-242">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="29289-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="29289-243">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="29289-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="29289-244">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="29289-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="29289-245">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="29289-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29289-246">Kos unit persumberan</span><span class="sxs-lookup"><span data-stu-id="29289-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="29289-247">Mata wang unit persumberan</span><span class="sxs-lookup"><span data-stu-id="29289-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29289-248">Jualan antara organisasi</span><span class="sxs-lookup"><span data-stu-id="29289-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="29289-249">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="29289-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29289-250">Jualan belum dibilkan sebenar – Boleh dituntut untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="29289-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="29289-251">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29289-252">Jualan belum dibilkan sebenar – Tidak boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="29289-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="29289-253">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="29289-254">Invois disahkan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku.</span><span class="sxs-lookup"><span data-stu-id="29289-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="29289-255">Pengunduran jualan belum dibilkan</span><span class="sxs-lookup"><span data-stu-id="29289-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="29289-256">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="29289-257">Jualan dibilkan untuk pencapaian</span><span class="sxs-lookup"><span data-stu-id="29289-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="29289-258">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="29289-259">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="29289-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="29289-260">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="29289-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29289-261">Jualan dibilkan</span><span class="sxs-lookup"><span data-stu-id="29289-261">Billed sales</span></span></td>
<td><span data-ttu-id="29289-262">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="29289-263">Invois disahkan dan pengurangan dalam masa boleh dibilkan berlaku.</span><span class="sxs-lookup"><span data-stu-id="29289-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="29289-264">Pengunduran jualan belum dibilkan</span><span class="sxs-lookup"><span data-stu-id="29289-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="29289-265">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="29289-266">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="29289-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="29289-267">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="29289-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="29289-268">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="29289-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="29289-269">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="29289-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29289-270">Jualan dibilkan – Boleh dituntut untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="29289-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="29289-271">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29289-272">Jualan dibilkan – Tidak boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="29289-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="29289-273">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="29289-274">Invois dibetulkan untuk menambah kuantiti yang boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="29289-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="29289-275">Julana dibilkan – Pengunduran</span><span class="sxs-lookup"><span data-stu-id="29289-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="29289-276">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="29289-277">Pengunduran jualan dibilkan untuk pencapaian</span><span class="sxs-lookup"><span data-stu-id="29289-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="29289-278">Penukarang status pencapaian daripada <strong>Diinvoiskan</strong> kepada <strong>Sedia untuk invois</strong></span><span class="sxs-lookup"><span data-stu-id="29289-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="29289-279">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="29289-280">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="29289-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="29289-281">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="29289-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29289-282">Jualan dibilkan</span><span class="sxs-lookup"><span data-stu-id="29289-282">Billed sales</span></span></td>
<td><span data-ttu-id="29289-283">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="29289-284">Invois dibetulkan untuk mengurangkan kuantiti yang boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="29289-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="29289-285">Julana dibilkan – Pengunduran</span><span class="sxs-lookup"><span data-stu-id="29289-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="29289-286">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29289-287">Jualan dibilkan untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="29289-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="29289-288">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29289-289">Jualan tidak dibilkan – Boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="29289-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="29289-290">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="29289-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
