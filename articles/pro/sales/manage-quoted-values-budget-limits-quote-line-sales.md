---
title: Gambaran keseluruhan baris sebut harga berdasarkan projek
description: Topik ini menyediakan maklumat tentang menggunakan baris sebut harga berasaskan projek untuk kerja projek.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: b7076a4b9280472f8c30d0b58c3aa9b9bc86d651
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369882"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="848b8-103">Gambaran keseluruhan baris sebut harga berdasarkan projek</span><span class="sxs-lookup"><span data-stu-id="848b8-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="848b8-104">_**Gunakan Pada:** Pelaksanaan ringan - urusan untuk penginvoisan proforma, Project Operations untuk senario berdasarkan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="848b8-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="848b8-105">Baris sebut harga berasaskan projek direka untuk membantu menganggar kerja projek pada pembabitan.</span><span class="sxs-lookup"><span data-stu-id="848b8-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="848b8-106">Struktur baris sebut harga berasaskan projek dilanjutkan untuk anggaran projek dengan konsep berikut:</span><span class="sxs-lookup"><span data-stu-id="848b8-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="848b8-107">Kaedah Pengebilan</span><span class="sxs-lookup"><span data-stu-id="848b8-107">Billing Method</span></span>
- <span data-ttu-id="848b8-108">Pemetaan Projek dan Tugas</span><span class="sxs-lookup"><span data-stu-id="848b8-108">Project and Task Mapping</span></span>
- <span data-ttu-id="848b8-109">Termasuk kelas Transaksi</span><span class="sxs-lookup"><span data-stu-id="848b8-109">Included Transaction classes</span></span>
- <span data-ttu-id="848b8-110">Had yang tidak boleh Melebihi</span><span class="sxs-lookup"><span data-stu-id="848b8-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="848b8-111">Persediaan boleh dikenakan caj</span><span class="sxs-lookup"><span data-stu-id="848b8-111">Chargeability setup</span></span>
- <span data-ttu-id="848b8-112">Anggaran menggunakan Butiran Baris Sebut Harga</span><span class="sxs-lookup"><span data-stu-id="848b8-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="848b8-113">Pelanggan baris Sebut Harga</span><span class="sxs-lookup"><span data-stu-id="848b8-113">Quote line Customers</span></span>

<span data-ttu-id="848b8-114">Jadual berikut menyediakan maklumat mengenai medan pada tab **Umum** baris sebut harga berasaskan projek.</span><span class="sxs-lookup"><span data-stu-id="848b8-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="848b8-115">Medan ini membantu menyediakan asas untuk anggaran terperinci dan dari bawah untuk kerja projek.</span><span class="sxs-lookup"><span data-stu-id="848b8-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="848b8-116">**Medan**</span><span class="sxs-lookup"><span data-stu-id="848b8-116">**Field**</span></span> | <span data-ttu-id="848b8-117">**Perihalan**</span><span class="sxs-lookup"><span data-stu-id="848b8-117">**Description**</span></span> | <span data-ttu-id="848b8-118">**Kesan hiliran**</span><span class="sxs-lookup"><span data-stu-id="848b8-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="848b8-119">Nama</span><span class="sxs-lookup"><span data-stu-id="848b8-119">Name</span></span> | <span data-ttu-id="848b8-120">Nama baris sebut harga yang membantu anda mengenal pasti komponen diskret sebut harga yang sedang dianggarkan.</span><span class="sxs-lookup"><span data-stu-id="848b8-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="848b8-121">Disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="848b8-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="848b8-122">Kaedah Pengebilan</span><span class="sxs-lookup"><span data-stu-id="848b8-122">Billing Method</span></span> | <span data-ttu-id="848b8-123">Pada sebut harga dicipta daripada peluang, nilai ini disalin daripada medan berkaitan dengan baris peluang.</span><span class="sxs-lookup"><span data-stu-id="848b8-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="848b8-124">Medan ini merangkumi dua model kontrak utama yang disokong oleh Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="848b8-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="848b8-125">- Harga tetap</span><span class="sxs-lookup"><span data-stu-id="848b8-125">- Fixed price</span></span></br><span data-ttu-id="848b8-126">- Masa dan bahan.</span><span class="sxs-lookup"><span data-stu-id="848b8-126">- Time and material.</span></span>| <span data-ttu-id="848b8-127">Nilai ini disalin ke baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="848b8-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="848b8-128">Project</span><span class="sxs-lookup"><span data-stu-id="848b8-128">Project</span></span> | <span data-ttu-id="848b8-129">Gunakan medan pilihan ini untuk mengenal pasti projek yang akan digunakan untuk menyelesaikan kerja pada pembabitan ini.</span><span class="sxs-lookup"><span data-stu-id="848b8-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="848b8-130">Apabila projek dipetakan kepada baris sebut harga, ia membantu dengan menyediakan tugas yang dikenakan caj dan juga dengan membawa anggaran berasaskan projek kepada baris sebut harga sebagai butiran baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="848b8-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="848b8-131">Apabila projek tidak dipetakan kepada baris sebut harga berasaskan projek, anggaran perlu dicipta secara manual dengan mencipta setiap butiran baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="848b8-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="848b8-132">Nilai ini disalin ke baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="848b8-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="848b8-133">Tugas yang Disertakan</span><span class="sxs-lookup"><span data-stu-id="848b8-133">Included Tasks</span></span> | <span data-ttu-id="848b8-134">Menunjukkan jika baris sebut harga digunakan untuk semua atau sesetengah tugas projek untuk projek yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="848b8-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="848b8-135">Medan ini mempunyai nilai-nilai kebarangkalian yang berikut:</span><span class="sxs-lookup"><span data-stu-id="848b8-135">This field has the following possible values:</span></span></br><span data-ttu-id="848b8-136">- Semua tugas projek</span><span class="sxs-lookup"><span data-stu-id="848b8-136">- All project tasks</span></span></br><span data-ttu-id="848b8-137">- Tugas projek terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="848b8-137">- Selected project tasks only</span></span></br><span data-ttu-id="848b8-138">Nilai kosong dalam medan ini adalah bersamaan dengan pilihan **Semua tugas projek**.</span><span class="sxs-lookup"><span data-stu-id="848b8-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="848b8-139">Apabila **Tugas projek yang dipilih sahaja** dipilih pada halaman projek, tab **Persediaan pengebilan Tugas** membolehkan anda memilih tugas khusus untuk mengaitkannya dengan baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="848b8-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="848b8-140">Nilai ini disalin ke baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="848b8-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="848b8-141">Termasuk Masa</span><span class="sxs-lookup"><span data-stu-id="848b8-141">Include Time</span></span> | <span data-ttu-id="848b8-142">Nilai **Ya**/**Tidak** menunjukkan jika transaksi masa atau kos buruh pada projek yang dipilih akan disertakan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="848b8-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="848b8-143">Nilai **Tidak** menunjukkan yang transaksi masa atau kos buruh tidak akan dimasukkan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="848b8-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="848b8-144">Nilai **Tidak** menunjukkan yang transaksi masa atau kos buruh akan dimasukkan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="848b8-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="848b8-145">Nilai ini disalin ke baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="848b8-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="848b8-146">Termasuk Perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="848b8-146">Include Expense</span></span> | <span data-ttu-id="848b8-147">Nilai **Ya**/**Tidak** menunjukkan jika kos perbelanjaan pada projek yang dipilih akan disertakan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="848b8-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="848b8-148">Nilai **Tidak** menunjukkan yang kos perbelanjaan tidak akan dimasukkan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="848b8-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="848b8-149">Nilai **Ya** menunjukkan yang kos perbelanjaan tidak akan dimasukkan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="848b8-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="848b8-150">Nilai ini disalin pada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="848b8-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="848b8-151">Termasuk Bahan</span><span class="sxs-lookup"><span data-stu-id="848b8-151">Include Material</span></span> | <span data-ttu-id="848b8-152">Nilai **Ya**/**Tidak** menunjukkan jika kos bahan pada projek yang dipilih akan disertakan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="848b8-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="848b8-153">Nilai **Tidak** menunjukkan bahawa kos bahan tidak akan disertakan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="848b8-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="848b8-154">Nilai **Ya** menunjukkan bahawa kos bahan akan disertakan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="848b8-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="848b8-155">Nilai ini disalin pada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="848b8-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="848b8-156">Termasuk Yuran</span><span class="sxs-lookup"><span data-stu-id="848b8-156">Include Fee</span></span> | <span data-ttu-id="848b8-157">Nilai **Ya**/**Tidak** menunjukkan jika yuran bagi projek yang dipilih akan disertakan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="848b8-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="848b8-158">Nilai **Tidak** menunjukkan bahawa yuran tidak akan disertakan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="848b8-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="848b8-159">Nilai **Ya** menunjukkan bahawa yuran tidak akan disertakan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="848b8-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="848b8-160">Nilai ini disalin ke baris kontrak Projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="848b8-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="848b8-161">Amaun Disebut Harga</span><span class="sxs-lookup"><span data-stu-id="848b8-161">Quoted Amount</span></span> | <span data-ttu-id="848b8-162">Ini ialah amaun yang akan digunakan dalam sebut harga kepada pelanggan untuk semua kerja yang diramalkan pada baris sebut harga berdasarkan projek ini.</span><span class="sxs-lookup"><span data-stu-id="848b8-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="848b8-163">Pada sebut harga dicipta daripada peluang, nilai ini disalin daripada medan **Bajet Pelanggan** pada baris peluang.</span><span class="sxs-lookup"><span data-stu-id="848b8-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="848b8-164">Apabila baris sebut harga berasaskan projek mempunyai butiran baris, medan ini dikunci untuk pengeditan dan diringkaskan daripada jumlah pada butiran baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="848b8-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="848b8-165">Nilai ini disalin ke baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="848b8-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="848b8-166">Anggaran Cukai</span><span class="sxs-lookup"><span data-stu-id="848b8-166">Estimated Tax</span></span> | <span data-ttu-id="848b8-167">Ini adalah medan boleh diedit untuk pengguna untuk menambah anggaran jumlah cukai pada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="848b8-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="848b8-168">Apabila baris sebut harga berasaskan projek mempunyai butiran baris, medan ini dikunci untuk pengeditan dan diringkaskan daripada jumlah cukai pada butiran baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="848b8-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="848b8-169">Nilai ini disalin ke baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="848b8-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="848b8-170">Jumlah Sebut Harga selepas Cukai</span><span class="sxs-lookup"><span data-stu-id="848b8-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="848b8-171">Medan ini adalah jumlah baris sebut harga selepas cukai dan baca sahaja.</span><span class="sxs-lookup"><span data-stu-id="848b8-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="848b8-172">Jumlah dalam medan ini dikira sebagai *Jumlah Sebut Harga + Cukai*.</span><span class="sxs-lookup"><span data-stu-id="848b8-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="848b8-173">Nilai ini disalin ke baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="848b8-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="848b8-174">Had Tidak Boleh Dilebihi</span><span class="sxs-lookup"><span data-stu-id="848b8-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="848b8-175">Medan ini boleh diedit dan hanya tersedia pada baris sebut harga berasaskan projek yang mempunyai kaedah pengebilan **Masa dan Bahan**.</span><span class="sxs-lookup"><span data-stu-id="848b8-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="848b8-176">Nilai ini disalin ke baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="848b8-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="848b8-177">Belanjawan Pelanggan</span><span class="sxs-lookup"><span data-stu-id="848b8-177">Customer Budget</span></span> | <span data-ttu-id="848b8-178">Medan ini boleh diedit dan disalin daripada medan berkaitan dengan baris peluang jika sebut harga dicipta daripada peluang.</span><span class="sxs-lookup"><span data-stu-id="848b8-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="848b8-179">Nilai ini disalin ke baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="848b8-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="848b8-180">Peraturan pengesahan untuk medan pada tab Umum bagi baris sebut harga berasaskan projek</span><span class="sxs-lookup"><span data-stu-id="848b8-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="848b8-181">**Peraturan 1**: Jika medan **Tugas yang termasuk** adalah kosong atau jika ia ditetapkan kepada **Semua tugas projek**, projek dimasukkan dalam baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="848b8-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="848b8-182">**Peraturan 2**: Jika medan **Tugas yang termasuk** adalah kosong, atau jika ia ditetapkan kepada **Semua tugas projek**, projek dan kelas transaksi tertentu hanya boleh dimasukkan pada satu baris sebut harga berasaskan projek bagi sebut harga.</span><span class="sxs-lookup"><span data-stu-id="848b8-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="848b8-183">**Peraturan 3**: Jika medan **Tugas yang termasuk** ditetapkan kepada **Hanya tugas projek terpilih**, projek dan kelas transaksi tertentu boleh dimasukkan pada berbilang baris sebut harga berasaskan projek bagi sebut harga.</span><span class="sxs-lookup"><span data-stu-id="848b8-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="848b8-184">**Peraturan 4**: Jika peluang mempunyai berbilang sebut harga, boleh terdapat baris sebut harga daripada sebut harga berbeza yang semuanya merujuk kepada projek yang sama dan termasuk kelas transaksi yang sama.</span><span class="sxs-lookup"><span data-stu-id="848b8-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="848b8-185">**Peraturan 5**: Jika sebut harga tidak tergolong kepada peluang yang sama, ia tidak boleh termasuk projek dan kelas transaksi yang sama.</span><span class="sxs-lookup"><span data-stu-id="848b8-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="848b8-186">
                    <strong>Peluang</strong>
                </span><span class="sxs-lookup"><span data-stu-id="848b8-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="848b8-187">
                    <strong>Sebut Harga</strong>
                </span><span class="sxs-lookup"><span data-stu-id="848b8-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="848b8-188">
                    <strong>Baris sebut harga</strong>
                </span><span class="sxs-lookup"><span data-stu-id="848b8-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="848b8-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="848b8-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="848b8-190">
                    <strong>Tugas yang disertakan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="848b8-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="848b8-191">
                    <strong>Termasuk Masa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="848b8-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="848b8-192">
                    <strong>Termasuk Perbelanjaan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="848b8-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="848b8-193">
                    <strong>Termasuk Bahan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="848b8-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="848b8-194">
                    <strong>Sertakan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="848b8-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="848b8-195">
                    <strong>Yuran</strong>
                </span><span class="sxs-lookup"><span data-stu-id="848b8-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="848b8-196">
                    <strong>Sah / Tidak sah</strong>
                </span><span class="sxs-lookup"><span data-stu-id="848b8-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="848b8-197">
                    <strong>Sebab</strong>
                </span><span class="sxs-lookup"><span data-stu-id="848b8-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="848b8-198">O1</span><span class="sxs-lookup"><span data-stu-id="848b8-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="848b8-199">S1</span><span class="sxs-lookup"><span data-stu-id="848b8-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="848b8-200">QL1</span><span class="sxs-lookup"><span data-stu-id="848b8-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-201">P1</span><span class="sxs-lookup"><span data-stu-id="848b8-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="848b8-202">Kosong</span><span class="sxs-lookup"><span data-stu-id="848b8-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="848b8-203">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="848b8-204">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="848b8-205">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-206">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="848b8-207">Tidak sah</span><span class="sxs-lookup"><span data-stu-id="848b8-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="848b8-208">Pelanggaran Peraturan #2.</span><span class="sxs-lookup"><span data-stu-id="848b8-208">Violation of Rule #2.</span></span> <span data-ttu-id="848b8-209">Masa, Perbelanjaan dan Yuran pada projek P1 disertakan pada baris sebut harga QL1 dan QL2</span><span class="sxs-lookup"><span data-stu-id="848b8-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="848b8-210">O1</span><span class="sxs-lookup"><span data-stu-id="848b8-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="848b8-211">S1</span><span class="sxs-lookup"><span data-stu-id="848b8-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="848b8-212">QL2</span><span class="sxs-lookup"><span data-stu-id="848b8-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-213">P1</span><span class="sxs-lookup"><span data-stu-id="848b8-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="848b8-214">Kosong</span><span class="sxs-lookup"><span data-stu-id="848b8-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="848b8-215">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="848b8-216">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="848b8-217">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-218">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="848b8-219">O1</span><span class="sxs-lookup"><span data-stu-id="848b8-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="848b8-220">S1</span><span class="sxs-lookup"><span data-stu-id="848b8-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="848b8-221">QL1</span><span class="sxs-lookup"><span data-stu-id="848b8-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-222">P1</span><span class="sxs-lookup"><span data-stu-id="848b8-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="848b8-223">Kosong</span><span class="sxs-lookup"><span data-stu-id="848b8-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="848b8-224">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="848b8-225">Tidak</span><span class="sxs-lookup"><span data-stu-id="848b8-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="848b8-226">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-227">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="848b8-228">Tidak sah</span><span class="sxs-lookup"><span data-stu-id="848b8-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="848b8-229">Pelanggaran Peraturan #2.</span><span class="sxs-lookup"><span data-stu-id="848b8-229">Violation of Rule #2.</span></span> <span data-ttu-id="848b8-230">Masa, Bahan dan Yuran bagi projek P1 disertakan pada baris sebut harga QL1 dan QL2</span><span class="sxs-lookup"><span data-stu-id="848b8-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="848b8-231">O1</span><span class="sxs-lookup"><span data-stu-id="848b8-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="848b8-232">S1</span><span class="sxs-lookup"><span data-stu-id="848b8-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="848b8-233">QL2</span><span class="sxs-lookup"><span data-stu-id="848b8-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-234">P1</span><span class="sxs-lookup"><span data-stu-id="848b8-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="848b8-235">Kosong</span><span class="sxs-lookup"><span data-stu-id="848b8-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="848b8-236">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="848b8-237">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="848b8-238">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-239">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="848b8-240">O1</span><span class="sxs-lookup"><span data-stu-id="848b8-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="848b8-241">S1</span><span class="sxs-lookup"><span data-stu-id="848b8-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="848b8-242">QL1</span><span class="sxs-lookup"><span data-stu-id="848b8-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-243">P1</span><span class="sxs-lookup"><span data-stu-id="848b8-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="848b8-244">Kosong</span><span class="sxs-lookup"><span data-stu-id="848b8-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="848b8-245">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="848b8-246">Tidak</span><span class="sxs-lookup"><span data-stu-id="848b8-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="848b8-247">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-248">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="848b8-249">Sah</span><span class="sxs-lookup"><span data-stu-id="848b8-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="848b8-250">Masa, Bahan dan Yuran bagi projek P1 disertakan dalam QL1</span><span class="sxs-lookup"><span data-stu-id="848b8-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="848b8-251">Perbelanjaan bagi projek P1 disertakan dalam QL2</span><span class="sxs-lookup"><span data-stu-id="848b8-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="848b8-252">Tiada pertindihan dalam nilai yang disertakan pada setiap baris kontrak dan oleh itu sah.</span><span class="sxs-lookup"><span data-stu-id="848b8-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="848b8-253">O1</span><span class="sxs-lookup"><span data-stu-id="848b8-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="848b8-254">S1</span><span class="sxs-lookup"><span data-stu-id="848b8-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="848b8-255">QL2</span><span class="sxs-lookup"><span data-stu-id="848b8-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-256">P1</span><span class="sxs-lookup"><span data-stu-id="848b8-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="848b8-257">Kosong</span><span class="sxs-lookup"><span data-stu-id="848b8-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="848b8-258">Tidak</span><span class="sxs-lookup"><span data-stu-id="848b8-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="848b8-259">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="848b8-260">Tidak</span><span class="sxs-lookup"><span data-stu-id="848b8-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-261">Tidak</span><span class="sxs-lookup"><span data-stu-id="848b8-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="848b8-262">O1</span><span class="sxs-lookup"><span data-stu-id="848b8-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="848b8-263">S1</span><span class="sxs-lookup"><span data-stu-id="848b8-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="848b8-264">QL1</span><span class="sxs-lookup"><span data-stu-id="848b8-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-265">P1</span><span class="sxs-lookup"><span data-stu-id="848b8-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="848b8-266">Tugas terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="848b8-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="848b8-267">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="848b8-268">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="848b8-269">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-270">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="848b8-271">Tidak sah</span><span class="sxs-lookup"><span data-stu-id="848b8-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="848b8-272">Pelanggaran Peraturan #2</span><span class="sxs-lookup"><span data-stu-id="848b8-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="848b8-273">Q1 termasuk Masa, Bahan, Perbelanjaan dan Yuran bagi subset tugas pada projek P1</span><span class="sxs-lookup"><span data-stu-id="848b8-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="848b8-274">QL2 termasuk Masa, Perbelanjaan dan Yuran untuk seluruh projek P1 dan oleh itu bertindih dengan nilai yang disertakan dalam Q1.</span><span class="sxs-lookup"><span data-stu-id="848b8-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="848b8-275">O1</span><span class="sxs-lookup"><span data-stu-id="848b8-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="848b8-276">S1</span><span class="sxs-lookup"><span data-stu-id="848b8-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="848b8-277">QL2</span><span class="sxs-lookup"><span data-stu-id="848b8-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-278">P1</span><span class="sxs-lookup"><span data-stu-id="848b8-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="848b8-279">Kosong</span><span class="sxs-lookup"><span data-stu-id="848b8-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="848b8-280">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="848b8-281">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="848b8-282">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-283">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="848b8-284">O1</span><span class="sxs-lookup"><span data-stu-id="848b8-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="848b8-285">S1</span><span class="sxs-lookup"><span data-stu-id="848b8-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="848b8-286">QL1</span><span class="sxs-lookup"><span data-stu-id="848b8-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-287">P1</span><span class="sxs-lookup"><span data-stu-id="848b8-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="848b8-288">Tugas terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="848b8-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="848b8-289">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="848b8-290">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="848b8-291">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-292">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="848b8-293">Sah</span><span class="sxs-lookup"><span data-stu-id="848b8-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="848b8-294">Menurut Peraturan #3,</span><span class="sxs-lookup"><span data-stu-id="848b8-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="848b8-295">Q1 termasuk Masa, Bahan, Perbelanjaan dan Yuran bagi subset tugas pada projek P1.</span><span class="sxs-lookup"><span data-stu-id="848b8-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="848b8-296">QL2 termasuk Masa, Bahan, Perbelanjaan dan Yuran untuk subset tugas pada projek P1.</span><span class="sxs-lookup"><span data-stu-id="848b8-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="848b8-297">Satu-satunya pengesahan tambahan ialah sekitar subset tugas pada QL1 yang berbeza daripada subset tugas pada QL2 untuk memastikan bahawa tiada pertindihan.</span><span class="sxs-lookup"><span data-stu-id="848b8-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="848b8-298">Ini dilakukan oleh sistem apabila tugas dikaitkan.</span><span class="sxs-lookup"><span data-stu-id="848b8-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="848b8-299">O1</span><span class="sxs-lookup"><span data-stu-id="848b8-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="848b8-300">S1</span><span class="sxs-lookup"><span data-stu-id="848b8-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="848b8-301">QL2</span><span class="sxs-lookup"><span data-stu-id="848b8-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-302">P1</span><span class="sxs-lookup"><span data-stu-id="848b8-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="848b8-303">Tugas terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="848b8-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="848b8-304">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="848b8-305">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="848b8-306">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-307">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="848b8-308">O1</span><span class="sxs-lookup"><span data-stu-id="848b8-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="848b8-309">S1</span><span class="sxs-lookup"><span data-stu-id="848b8-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="848b8-310">QL1</span><span class="sxs-lookup"><span data-stu-id="848b8-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-311">P1</span><span class="sxs-lookup"><span data-stu-id="848b8-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="848b8-312">Semua tugas projek atau kosong</span><span class="sxs-lookup"><span data-stu-id="848b8-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="848b8-313">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="848b8-314">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="848b8-315">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-316">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="848b8-317">Sah</span><span class="sxs-lookup"><span data-stu-id="848b8-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="848b8-318">Menurut Peraturan #5, Q1 dan Q2 adalah dua sebut harga pada peluang yang sama, jadi kedua-duanya boleh menganggarkan untuk komponen projek yang sama.</span><span class="sxs-lookup"><span data-stu-id="848b8-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="848b8-319">O1</span><span class="sxs-lookup"><span data-stu-id="848b8-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="848b8-320">S2</span><span class="sxs-lookup"><span data-stu-id="848b8-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="848b8-321">QL1</span><span class="sxs-lookup"><span data-stu-id="848b8-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-322">P1</span><span class="sxs-lookup"><span data-stu-id="848b8-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="848b8-323">Semua tugas projek atau kosong</span><span class="sxs-lookup"><span data-stu-id="848b8-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="848b8-324">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="848b8-325">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="848b8-326">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-327">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="848b8-328">O1</span><span class="sxs-lookup"><span data-stu-id="848b8-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="848b8-329">S1</span><span class="sxs-lookup"><span data-stu-id="848b8-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="848b8-330">QL1</span><span class="sxs-lookup"><span data-stu-id="848b8-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-331">P1</span><span class="sxs-lookup"><span data-stu-id="848b8-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="848b8-332">Semua tugas projek atau kosong</span><span class="sxs-lookup"><span data-stu-id="848b8-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="848b8-333">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="848b8-334">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="848b8-335">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-336">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="848b8-337">Tidak Sah</span><span class="sxs-lookup"><span data-stu-id="848b8-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="848b8-338">Menurut Peraturan #4, Q1 dan Q2 adalah dua sebut harga pada peluang yang berbeza, jadi kedua-duanya tidak boleh menganggarkan untuk komponen sama bagi projek yang sama.</span><span class="sxs-lookup"><span data-stu-id="848b8-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="848b8-339">O2</span><span class="sxs-lookup"><span data-stu-id="848b8-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="848b8-340">S1</span><span class="sxs-lookup"><span data-stu-id="848b8-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="848b8-341">QL1</span><span class="sxs-lookup"><span data-stu-id="848b8-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-342">P1</span><span class="sxs-lookup"><span data-stu-id="848b8-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="848b8-343">Semua tugas projek atau kosong</span><span class="sxs-lookup"><span data-stu-id="848b8-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="848b8-344">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="848b8-345">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="848b8-346">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="848b8-347">Ya</span><span class="sxs-lookup"><span data-stu-id="848b8-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
