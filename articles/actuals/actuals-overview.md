---
title: Aktual
description: Topik ini memberikan maklumat tentang cara untuk bekerja dengan aktual dalam Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 04/01/2021
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
ms.openlocfilehash: 304c51a4e502ad6ecec1fd821e98d6604ddd59ba
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852555"
---
# <a name="actuals"></a><span data-ttu-id="af6ea-103">Aktual</span><span class="sxs-lookup"><span data-stu-id="af6ea-103">Actuals</span></span> 

<span data-ttu-id="af6ea-104">_**Gunakan pada:** Project Operations untuk senario berdasarkan sumber/bukan stok, Pelaksanaan ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="af6ea-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="af6ea-105">Aktual mewakili kemajuan kewangan dan jadual yang disemak dan diluluskan untuk sesuatu projek.</span><span class="sxs-lookup"><span data-stu-id="af6ea-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="af6ea-106">Ia dicipta hasil daripada kelulusan masa, perbelanjaan, entri penggunaan bahan serta entri jurnal dan invois.</span><span class="sxs-lookup"><span data-stu-id="af6ea-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="af6ea-107">Garisan jurnal dan serahan masa</span><span class="sxs-lookup"><span data-stu-id="af6ea-107">Journal lines and time submission</span></span>

<span data-ttu-id="af6ea-108">Untuk mendapatkan maklumat lanjut tentang entri masa, lihat [Gambaran keseluruhan entri masa](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="af6ea-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="af6ea-109">Masa dan bahan</span><span class="sxs-lookup"><span data-stu-id="af6ea-109">Time and materials</span></span>

<span data-ttu-id="af6ea-110">Apabila entri masa yang diserahkan telah dipautkan dengan projek yang dipetakan dengan baris kontrak masa dan bahan, sistem mencipta dua garisan jurnal, satu untuk kos dan satu untuk jualan yang tidak dibilkan.</span><span class="sxs-lookup"><span data-stu-id="af6ea-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="af6ea-111">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="af6ea-111">Fixed price</span></span>

<span data-ttu-id="af6ea-112">Apabila entri masa yang telah diserahkan dipautkan kepada projek yang dipetakan kepada baris kontrak harga tetap, sistem mencipta satu garisan jurnal untuk kos.</span><span class="sxs-lookup"><span data-stu-id="af6ea-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="af6ea-113">Penetapan harga lalai</span><span class="sxs-lookup"><span data-stu-id="af6ea-113">Default pricing</span></span>

<span data-ttu-id="af6ea-114">Logik untuk mencipta harga lalai terletak pada garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="af6ea-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="af6ea-115">Nilai medan daripada entri masa disalin kepada garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="af6ea-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="af6ea-116">Nilai-nilai ini termasuk tarikh transaksi, baris kontrak yang projek dipetakan padanya, dan mata wang yang menghasilkan senarai harga yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="af6ea-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="af6ea-117">Medan yang menjejaskan penetapan harga lalai, seperti **Peranan** dan **Unit Penyumberan**, digunakan untuk menentukan harga bersesuaian pada garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="af6ea-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="af6ea-118">Anda boleh menambah medan tersuai pada entri masa.</span><span class="sxs-lookup"><span data-stu-id="af6ea-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="af6ea-119">Jika anda mahu nilai medan disebarluaskan pada aktual, cipta medan dalam jadual **Aktual** dan **Garisan Jurnal**.</span><span class="sxs-lookup"><span data-stu-id="af6ea-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="af6ea-120">Gunakan kod tersuai untuk menyebarluaskan nilai medan yang dipilih daripada Entri Masa kepada Aktual melalui baris jurnal menggunakan asal transaksi.</span><span class="sxs-lookup"><span data-stu-id="af6ea-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="af6ea-121">Untuk mendapatkan maklumat lanjut tentang asal transaksi dan sambungan, lihat [Memautkan aktual pada rekod asal](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="af6ea-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="af6ea-122">Serahan garisan jurnal dan perbelanjaan asas</span><span class="sxs-lookup"><span data-stu-id="af6ea-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="af6ea-123">Untuk mendapatkan maklumat lanjut tentang entri perbelanjaan, lihat [Gambaran keseluruhan perbelanjaan](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="af6ea-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="af6ea-124">Masa dan bahan</span><span class="sxs-lookup"><span data-stu-id="af6ea-124">Time and materials</span></span>

<span data-ttu-id="af6ea-125">Apabila entri perbelanjaan asas yang diserahkan telah dipautkan kepada projek yang dipetakan kepada baris kontrak masa dan bahan, sistem mencipta dua garisan jurnal, satu untuk kos dan satu untuk jualan yang tidak dibilkan.</span><span class="sxs-lookup"><span data-stu-id="af6ea-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="af6ea-126">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="af6ea-126">Fixed price</span></span>

<span data-ttu-id="af6ea-127">Apabila entri perbelanjaan asas yang diserahkan dipautkan pada projek yang dipetakan kepada baris kontrak harga tetap, sistem mencipta satu garisan jurnal untuk kos.</span><span class="sxs-lookup"><span data-stu-id="af6ea-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="af6ea-128">Penetapan harga lalai</span><span class="sxs-lookup"><span data-stu-id="af6ea-128">Default pricing</span></span>

<span data-ttu-id="af6ea-129">Logik untuk memasukkan harga lalai bagi perbelanjaan adalah berdasarkan kategori perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="af6ea-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="af6ea-130">Tarikh transaksi, baris kontrak yang projek dipetakan dan mata wang, semuanya digunakan untuk menentukan senarai harga bersesuaian.</span><span class="sxs-lookup"><span data-stu-id="af6ea-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="af6ea-131">Medan yang menjejaskan penetapan harga lalai, seperti **Kategori Transaksi** dan **Unit**, digunakan untuk menentukan harga bersesuaian pada garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="af6ea-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="af6ea-132">Walau bagaimanapun, ini hanya berfungsi apabila kaedah penetapan harga dalam senarai harga ialah **Harga setiap unit**.</span><span class="sxs-lookup"><span data-stu-id="af6ea-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="af6ea-133">Jika kaedah penetapan harga ialah **Pada kos** atau **Tokokan ke atas kos**, harga yang dimasukkan apabila entri perbelanjaan dicipta akan digunakan untuk kos dan harga pada garisan jurnal jualan dikira berdasarkan kaedah penetapan harga.</span><span class="sxs-lookup"><span data-stu-id="af6ea-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="af6ea-134">Anda boleh menambahkan medan tersuai pada entri perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="af6ea-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="af6ea-135">Jika anda mahu nilai medan disebarluaskan pada aktual, cipta medan dalam jadual **Aktual** dan **Garisan Jurnal**.</span><span class="sxs-lookup"><span data-stu-id="af6ea-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="af6ea-136">Gunakan kod tersuai untuk menyebarluaskan nilai medan yang dipilih daripada Entri Masa kepada Aktual melalui baris jurnal menggunakan asal transaksi.</span><span class="sxs-lookup"><span data-stu-id="af6ea-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="af6ea-137">Untuk mendapatkan maklumat lanjut tentang asal transaksi dan sambungan, lihat [Memautkan aktual pada rekod asal](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="af6ea-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="af6ea-138">Penyerahan log garisan jurnal dan penggunaan bahan</span><span class="sxs-lookup"><span data-stu-id="af6ea-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="af6ea-139">Untuk mendapatkan maklumat lanjut tentang entri perbelanjaan, lihat [Log Penggunaan Bahan](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="af6ea-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="af6ea-140">Masa dan bahan</span><span class="sxs-lookup"><span data-stu-id="af6ea-140">Time and materials</span></span>

<span data-ttu-id="af6ea-141">Apabila entri log penggunaan bahan yang diserahkan dikaitkan dengan projek yang dipetakan kepada baris kontrak masa dan bahan, sistem mencipta dua garisan jurnal, satu untuk kos dan satu untuk jualan yang belum dibilkan.</span><span class="sxs-lookup"><span data-stu-id="af6ea-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="af6ea-142">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="af6ea-142">Fixed price</span></span>

<span data-ttu-id="af6ea-143">Apabila entri log penggunaan bahan yang diserahkan dipautkan pada projek yang dipetakan kepada baris kontrak harga tetap, sistem mencipta satu garisan jurnal untuk kos.</span><span class="sxs-lookup"><span data-stu-id="af6ea-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="af6ea-144">Penetapan harga lalai</span><span class="sxs-lookup"><span data-stu-id="af6ea-144">Default pricing</span></span>

<span data-ttu-id="af6ea-145">Logik untuk memasukkan harga lalai bagi bahan adalah berdasarkan gabungan produk dan unit.</span><span class="sxs-lookup"><span data-stu-id="af6ea-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="af6ea-146">Tarikh transaksi, baris kontrak yang projek dipetakan dan mata wang, semuanya digunakan untuk menentukan senarai harga bersesuaian.</span><span class="sxs-lookup"><span data-stu-id="af6ea-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="af6ea-147">Medan yang menjejaskan penetapan harga lalai, seperti **ID Produk** dan **Unit**, digunakan untuk menentukan harga bersesuaian pada garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="af6ea-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="af6ea-148">Walau bagaimanapun, ini hanya berfungsi untuk produk katalog.</span><span class="sxs-lookup"><span data-stu-id="af6ea-148">However, this only works for catalog products.</span></span> <span data-ttu-id="af6ea-149">Untuk produk masukan manual, harga yang dimasukkan apabila entri log penggunaan bahan dicipta digunakan untuk kos dan harga jualan pada garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="af6ea-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="af6ea-150">Anda boleh menambahkan medan tersuai pada entri **Log Penggunaan Bahan**.</span><span class="sxs-lookup"><span data-stu-id="af6ea-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="af6ea-151">Jika anda mahu nilai medan disebarluaskan pada aktual, cipta medan dalam jadual **Aktual** dan **Garisan Jurnal**.</span><span class="sxs-lookup"><span data-stu-id="af6ea-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="af6ea-152">Gunakan kod tersuai untuk menyebarluaskan nilai medan yang dipilih daripada Entri Masa kepada Aktual melalui baris jurnal menggunakan asal transaksi.</span><span class="sxs-lookup"><span data-stu-id="af6ea-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="af6ea-153">Untuk mendapatkan maklumat lanjut tentang asal transaksi dan sambungan, lihat [Memautkan aktual pada rekod asal](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="af6ea-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="af6ea-154">Gunakan jurnal entri untuk merekodkan kos</span><span class="sxs-lookup"><span data-stu-id="af6ea-154">Use entry journals to record costs</span></span>

<span data-ttu-id="af6ea-155">Anda boleh menggunakan jurnal entri untuk merekodkan kos atau hasil dalam kelas bahan, yuran, masa, perbelanjaan, atau transaksi cukai.</span><span class="sxs-lookup"><span data-stu-id="af6ea-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="af6ea-156">Jurnal boleh digunakan untuk tujuan berikut:</span><span class="sxs-lookup"><span data-stu-id="af6ea-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="af6ea-157">Alihkan aktual transaksi daripada sistem lain kepada Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="af6ea-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="af6ea-158">Rekodkan kos yang berlaku dalam sistem yang lain.</span><span class="sxs-lookup"><span data-stu-id="af6ea-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="af6ea-159">Kos ini boleh merangkumi kos perolehan atau subkontrak.</span><span class="sxs-lookup"><span data-stu-id="af6ea-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="af6ea-160">Aplikasi ini tidak mengesahkan jenis garisan jurnal atau penetapan harga yang berkaitan yang dimasukkan pada garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="af6ea-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="af6ea-161">Oleh itu, hanya pengguna yang menyedari sepenuhnya kesan perakaunan yang aktual ada pada projek itu, harus menggunakan jurnal entri untuk mencipta aktual.</span><span class="sxs-lookup"><span data-stu-id="af6ea-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="af6ea-162">Disebabkan oleh kesan jenis Jurnal ini, anda perlu memilih dengan teliti orang yang mempunyai akses untuk mencipta jurnal entri.</span><span class="sxs-lookup"><span data-stu-id="af6ea-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="af6ea-163">Rekodkan aktual berdasarkan peristiwa projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-163">Record actuals based on project events</span></span>

<span data-ttu-id="af6ea-164">Project Operations merekodkan transaksi kewangan yang berlaku semasa projek.</span><span class="sxs-lookup"><span data-stu-id="af6ea-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="af6ea-165">Transaksi ini direkodkan sebagai aktual.</span><span class="sxs-lookup"><span data-stu-id="af6ea-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="af6ea-166">Jadual berikut menunjukkan jenis aktual berbeza yang dicipta, bergantung pada sama ada projek itu adalah projek masa dan bahan atau projek harga tetap, dalam peringkat prajualan, atau merupakan projek dalaman.</span><span class="sxs-lookup"><span data-stu-id="af6ea-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="af6ea-167">Sumber tersebut tergolong dalam unit organisasi yang sama seperti unit kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="af6ea-168">Peristiwa</span><span class="sxs-lookup"><span data-stu-id="af6ea-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="af6ea-169">Projek boleh dibilkan atau dijual</span><span class="sxs-lookup"><span data-stu-id="af6ea-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="af6ea-170">Projek dalam peringkat prajualan</span><span class="sxs-lookup"><span data-stu-id="af6ea-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="af6ea-171">Projek dalaman</span><span class="sxs-lookup"><span data-stu-id="af6ea-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="af6ea-172">Masa dan bahan</span><span class="sxs-lookup"><span data-stu-id="af6ea-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="af6ea-173">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="af6ea-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="af6ea-174">Sebenar</span><span class="sxs-lookup"><span data-stu-id="af6ea-174">Actuals</span></span></th>
<th><span data-ttu-id="af6ea-175">Mata wang transaksi</span><span class="sxs-lookup"><span data-stu-id="af6ea-175">Transaction currency</span></span></th>
<th><span data-ttu-id="af6ea-176">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="af6ea-176">Fixed price</span></span></th>
<th><span data-ttu-id="af6ea-177">Mata wang transaksi</span><span class="sxs-lookup"><span data-stu-id="af6ea-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="af6ea-178">Entri masa dicipta.</span><span class="sxs-lookup"><span data-stu-id="af6ea-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="af6ea-179">Tiada aktiviti dalam entiti Aktual</span><span class="sxs-lookup"><span data-stu-id="af6ea-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af6ea-180">Entri masa diserahkan.</span><span class="sxs-lookup"><span data-stu-id="af6ea-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="af6ea-181">Tiada aktiviti dalam entiti Aktual</span><span class="sxs-lookup"><span data-stu-id="af6ea-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="af6ea-182">Masa telah diluluskan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku semasa kelulusan.</span><span class="sxs-lookup"><span data-stu-id="af6ea-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="af6ea-183">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="af6ea-183">Cost actual</span></span></td>
<td><span data-ttu-id="af6ea-184">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="af6ea-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="af6ea-185">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="af6ea-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="af6ea-186">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="af6ea-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="af6ea-187">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="af6ea-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="af6ea-188">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="af6ea-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af6ea-189">Jualan belum dibilkan sebenar – Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="af6ea-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="af6ea-190">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="af6ea-191">Masa telah diluluskan dan tiada pengurangan dalam masa boleh dibilkan berlaku semasa kelulusan.</span><span class="sxs-lookup"><span data-stu-id="af6ea-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="af6ea-192">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="af6ea-192">Cost actual</span></span></td>
<td><span data-ttu-id="af6ea-193">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="af6ea-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="af6ea-194">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="af6ea-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="af6ea-195">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="af6ea-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="af6ea-196">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="af6ea-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="af6ea-197">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="af6ea-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af6ea-198">Jualan belum dibilkan sebenar – Boleh dituntut untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="af6ea-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="af6ea-199">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af6ea-200">Jualan belum dibilkan sebenar – Tidak boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="af6ea-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="af6ea-201">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="af6ea-202">Invois disahkan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku.</span><span class="sxs-lookup"><span data-stu-id="af6ea-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="af6ea-203">Pengunduran jualan belum dibilkan</span><span class="sxs-lookup"><span data-stu-id="af6ea-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="af6ea-204">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="af6ea-205">Jualan dibilkan untuk pencapaian</span><span class="sxs-lookup"><span data-stu-id="af6ea-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="af6ea-206">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="af6ea-207">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="af6ea-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="af6ea-208">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="af6ea-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af6ea-209">Jualan dibilkan</span><span class="sxs-lookup"><span data-stu-id="af6ea-209">Billed sales</span></span></td>
<td><span data-ttu-id="af6ea-210">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="af6ea-211">Invois disahkan dan pengurangan dalam masa boleh dibilkan berlaku.</span><span class="sxs-lookup"><span data-stu-id="af6ea-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="af6ea-212">Pengunduran jualan belum dibilkan</span><span class="sxs-lookup"><span data-stu-id="af6ea-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="af6ea-213">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="af6ea-214">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="af6ea-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="af6ea-215">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="af6ea-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="af6ea-216">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="af6ea-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="af6ea-217">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="af6ea-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af6ea-218">Jualan dibilkan – Boleh dituntut untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="af6ea-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="af6ea-219">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af6ea-220">Jualan dibilkan – Tidak boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="af6ea-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="af6ea-221">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="af6ea-222">Invois dibetulkan untuk menambah kuantiti yang boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="af6ea-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="af6ea-223">Julana dibilkan – Pengunduran</span><span class="sxs-lookup"><span data-stu-id="af6ea-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="af6ea-224">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="af6ea-225">Pengunduran jualan dibilkan untuk pencapaian</span><span class="sxs-lookup"><span data-stu-id="af6ea-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="af6ea-226">Penukarang status pencapaian daripada <strong>Diinvoiskan</strong> kepada <strong>Sedia untuk invois</strong></span><span class="sxs-lookup"><span data-stu-id="af6ea-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="af6ea-227">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="af6ea-228">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="af6ea-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="af6ea-229">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="af6ea-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af6ea-230">Jualan dibilkan</span><span class="sxs-lookup"><span data-stu-id="af6ea-230">Billed sales</span></span></td>
<td><span data-ttu-id="af6ea-231">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="af6ea-232">Invois dibetulkan untuk mengurangkan kuantiti yang boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="af6ea-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="af6ea-233">Julana dibilkan – Pengunduran</span><span class="sxs-lookup"><span data-stu-id="af6ea-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="af6ea-234">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af6ea-235">Jualan dibilkan untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="af6ea-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="af6ea-236">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af6ea-237">Jualan tidak dibilkan – Boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="af6ea-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="af6ea-238">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="af6ea-239">Sumber tersebut tergolong dalam unit organisasi yang berbeza daripada unit kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="af6ea-240">Peristiwa</span><span class="sxs-lookup"><span data-stu-id="af6ea-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="af6ea-241">Projek boleh dibilkan atau dijual</span><span class="sxs-lookup"><span data-stu-id="af6ea-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="af6ea-242">Projek dalam peringkat prajualan</span><span class="sxs-lookup"><span data-stu-id="af6ea-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="af6ea-243">Projek dalaman</span><span class="sxs-lookup"><span data-stu-id="af6ea-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="af6ea-244">Masa dan bahan</span><span class="sxs-lookup"><span data-stu-id="af6ea-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="af6ea-245">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="af6ea-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="af6ea-246">Sebenar</span><span class="sxs-lookup"><span data-stu-id="af6ea-246">Actuals</span></span></th>
<th><span data-ttu-id="af6ea-247">Mata wang transaksi</span><span class="sxs-lookup"><span data-stu-id="af6ea-247">Transaction currency</span></span></th>
<th><span data-ttu-id="af6ea-248">Harga tetap</span><span class="sxs-lookup"><span data-stu-id="af6ea-248">Fixed price</span></span></th>
<th><span data-ttu-id="af6ea-249">Mata wang transaksi</span><span class="sxs-lookup"><span data-stu-id="af6ea-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="af6ea-250">Entri masa dicipta.</span><span class="sxs-lookup"><span data-stu-id="af6ea-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="af6ea-251">Tiada aktiviti dalam entiti Aktual</span><span class="sxs-lookup"><span data-stu-id="af6ea-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af6ea-252">Entri masa diserahkan.</span><span class="sxs-lookup"><span data-stu-id="af6ea-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="af6ea-253">Tiada aktiviti dalam entiti Aktual</span><span class="sxs-lookup"><span data-stu-id="af6ea-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="af6ea-254">Masa telah diluluskan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku semasa kelulusan.</span><span class="sxs-lookup"><span data-stu-id="af6ea-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="af6ea-255">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="af6ea-255">Cost actual</span></span></td>
<td><span data-ttu-id="af6ea-256">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="af6ea-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="af6ea-257">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="af6ea-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="af6ea-258">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="af6ea-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="af6ea-259">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="af6ea-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="af6ea-260">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="af6ea-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af6ea-261">Jualan belum dibilkan sebenar – Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="af6ea-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="af6ea-262">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af6ea-263">Kos unit persumberan</span><span class="sxs-lookup"><span data-stu-id="af6ea-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="af6ea-264">Mata wang unit persumberan</span><span class="sxs-lookup"><span data-stu-id="af6ea-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af6ea-265">Jualan antara organisasi</span><span class="sxs-lookup"><span data-stu-id="af6ea-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="af6ea-266">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="af6ea-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="af6ea-267">Masa telah diluluskan dan tiada pengurangan dalam masa boleh dibilkan berlaku semasa kelulusan.</span><span class="sxs-lookup"><span data-stu-id="af6ea-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="af6ea-268">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="af6ea-268">Cost actual</span></span></td>
<td><span data-ttu-id="af6ea-269">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="af6ea-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="af6ea-270">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="af6ea-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="af6ea-271">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="af6ea-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="af6ea-272">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="af6ea-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="af6ea-273">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="af6ea-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af6ea-274">Kos unit persumberan</span><span class="sxs-lookup"><span data-stu-id="af6ea-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="af6ea-275">Mata wang unit persumberan</span><span class="sxs-lookup"><span data-stu-id="af6ea-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af6ea-276">Jualan antara organisasi</span><span class="sxs-lookup"><span data-stu-id="af6ea-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="af6ea-277">Mata wang unit pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="af6ea-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af6ea-278">Jualan belum dibilkan sebenar – Boleh dituntut untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="af6ea-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="af6ea-279">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af6ea-280">Jualan belum dibilkan sebenar – Tidak boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="af6ea-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="af6ea-281">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="af6ea-282">Invois disahkan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku.</span><span class="sxs-lookup"><span data-stu-id="af6ea-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="af6ea-283">Pengunduran jualan belum dibilkan</span><span class="sxs-lookup"><span data-stu-id="af6ea-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="af6ea-284">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="af6ea-285">Jualan dibilkan untuk pencapaian</span><span class="sxs-lookup"><span data-stu-id="af6ea-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="af6ea-286">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="af6ea-287">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="af6ea-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="af6ea-288">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="af6ea-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af6ea-289">Jualan dibilkan</span><span class="sxs-lookup"><span data-stu-id="af6ea-289">Billed sales</span></span></td>
<td><span data-ttu-id="af6ea-290">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="af6ea-291">Invois disahkan dan pengurangan dalam masa boleh dibilkan berlaku.</span><span class="sxs-lookup"><span data-stu-id="af6ea-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="af6ea-292">Pengunduran jualan belum dibilkan</span><span class="sxs-lookup"><span data-stu-id="af6ea-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="af6ea-293">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="af6ea-294">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="af6ea-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="af6ea-295">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="af6ea-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="af6ea-296">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="af6ea-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="af6ea-297">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="af6ea-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af6ea-298">Jualan dibilkan – Boleh dituntut untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="af6ea-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="af6ea-299">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af6ea-300">Jualan dibilkan – Tidak boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="af6ea-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="af6ea-301">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="af6ea-302">Invois dibetulkan untuk menambah kuantiti yang boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="af6ea-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="af6ea-303">Julana dibilkan – Pengunduran</span><span class="sxs-lookup"><span data-stu-id="af6ea-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="af6ea-304">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="af6ea-305">Pengunduran jualan dibilkan untuk pencapaian</span><span class="sxs-lookup"><span data-stu-id="af6ea-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="af6ea-306">Penukarang status pencapaian daripada <strong>Diinvoiskan</strong> kepada <strong>Sedia untuk invois</strong></span><span class="sxs-lookup"><span data-stu-id="af6ea-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="af6ea-307">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="af6ea-308">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="af6ea-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="af6ea-309">Tidak berkenaan</span><span class="sxs-lookup"><span data-stu-id="af6ea-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af6ea-310">Jualan dibilkan</span><span class="sxs-lookup"><span data-stu-id="af6ea-310">Billed sales</span></span></td>
<td><span data-ttu-id="af6ea-311">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="af6ea-312">Invois dibetulkan untuk mengurangkan kuantiti yang boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="af6ea-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="af6ea-313">Julana dibilkan – Pengunduran</span><span class="sxs-lookup"><span data-stu-id="af6ea-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="af6ea-314">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af6ea-315">Jualan dibilkan untuk kuantiti baharu</span><span class="sxs-lookup"><span data-stu-id="af6ea-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="af6ea-316">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="af6ea-317">Jualan tidak dibilkan – Boleh dituntut untuk perbezaan</span><span class="sxs-lookup"><span data-stu-id="af6ea-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="af6ea-318">Mata wang kontrak projek</span><span class="sxs-lookup"><span data-stu-id="af6ea-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
