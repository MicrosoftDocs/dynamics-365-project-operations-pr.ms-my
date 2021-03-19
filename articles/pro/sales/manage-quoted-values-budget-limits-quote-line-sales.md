---
title: Gambaran keseluruhan baris sebut harga berdasarkan projek - lite
description: Topik ini menyediakan maklumat tentang menggunakan baris sebut harga berasaskan projek untuk kerja projek. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4865c06691fba09eacf5fe6449adfaf542444520
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272984"
---
# <a name="project-based-quote-lines-overview---lite"></a><span data-ttu-id="0372c-104">Gambaran keseluruhan baris sebut harga berdasarkan projek - lite</span><span class="sxs-lookup"><span data-stu-id="0372c-104">Project-based quote lines overview - lite</span></span>

<span data-ttu-id="0372c-105">_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_</span><span class="sxs-lookup"><span data-stu-id="0372c-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0372c-106">Baris sebut harga berasaskan projek direka untuk membantu menganggar kerja projek pada pembabitan.</span><span class="sxs-lookup"><span data-stu-id="0372c-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="0372c-107">Struktur baris sebut harga berasaskan projek dilanjutkan untuk anggaran projek dengan konsep berikut:</span><span class="sxs-lookup"><span data-stu-id="0372c-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="0372c-108">Kaedah Pengebilan</span><span class="sxs-lookup"><span data-stu-id="0372c-108">Billing Method</span></span>
- <span data-ttu-id="0372c-109">Pemetaan Projek dan Tugas</span><span class="sxs-lookup"><span data-stu-id="0372c-109">Project and Task Mapping</span></span>
- <span data-ttu-id="0372c-110">Termasuk kelas Transaksi</span><span class="sxs-lookup"><span data-stu-id="0372c-110">Included Transaction classes</span></span>
- <span data-ttu-id="0372c-111">Had yang tidak boleh Melebihi</span><span class="sxs-lookup"><span data-stu-id="0372c-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="0372c-112">Persediaan boleh dikenakan caj</span><span class="sxs-lookup"><span data-stu-id="0372c-112">Chargeability setup</span></span>
- <span data-ttu-id="0372c-113">Anggaran menggunakan Butiran Baris Sebut Harga</span><span class="sxs-lookup"><span data-stu-id="0372c-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="0372c-114">Pelanggan baris Sebut Harga</span><span class="sxs-lookup"><span data-stu-id="0372c-114">Quote line Customers</span></span>

<span data-ttu-id="0372c-115">Jadual berikut menyediakan maklumat mengenai medan pada tab **Umum** baris sebut harga berasaskan projek.</span><span class="sxs-lookup"><span data-stu-id="0372c-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="0372c-116">Medan ini membantu menyediakan asas untuk anggaran terperinci dan dari bawah untuk kerja projek.</span><span class="sxs-lookup"><span data-stu-id="0372c-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="0372c-117">**Medan**</span><span class="sxs-lookup"><span data-stu-id="0372c-117">**Field**</span></span> | <span data-ttu-id="0372c-118">**Perihalan**</span><span class="sxs-lookup"><span data-stu-id="0372c-118">**Description**</span></span> | <span data-ttu-id="0372c-119">**Kesan hiliran**</span><span class="sxs-lookup"><span data-stu-id="0372c-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0372c-120">Nama</span><span class="sxs-lookup"><span data-stu-id="0372c-120">Name</span></span> | <span data-ttu-id="0372c-121">Nama baris sebut harga yang sepatutnya boleh membantu anda mengenal pasti komponen tunggal sebut harga yang dianggarkan.</span><span class="sxs-lookup"><span data-stu-id="0372c-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="0372c-122">Disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="0372c-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0372c-123">Kaedah Pengebilan</span><span class="sxs-lookup"><span data-stu-id="0372c-123">Billing Method</span></span> | <span data-ttu-id="0372c-124">Pada sebut harga dicipta daripada peluang, nilai ini disalin daripada medan berkaitan dengan baris peluang.</span><span class="sxs-lookup"><span data-stu-id="0372c-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="0372c-125">Medan ini merangkumi dua model kontrak utama yang disokong oleh Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="0372c-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="0372c-126">- Harga tetap</span><span class="sxs-lookup"><span data-stu-id="0372c-126">- Fixed price</span></span></br><span data-ttu-id="0372c-127">- Masa dan bahan.</span><span class="sxs-lookup"><span data-stu-id="0372c-127">- Time and material.</span></span>| <span data-ttu-id="0372c-128">Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="0372c-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0372c-129">Project</span><span class="sxs-lookup"><span data-stu-id="0372c-129">Project</span></span> | <span data-ttu-id="0372c-130">Gunakan medan pilihan ini untuk mengenal pasti projek yang akan digunakan untuk menyelesaikan kerja pada pembabitan ini.</span><span class="sxs-lookup"><span data-stu-id="0372c-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="0372c-131">Apabila projek dipetakan kepada baris sebut harga, ia membantu dengan menyediakan tugas yang dikenakan caj dan juga dengan membawa anggaran berasaskan projek kepada baris sebut harga sebagai butiran baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="0372c-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="0372c-132">Apabila projek tidak dipetakan kepada baris sebut harga berasaskan projek, anggaran perlu dicipta secara manual dengan mencipta setiap butiran baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="0372c-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="0372c-133">Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="0372c-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="0372c-134">Tugas yang Disertakan</span><span class="sxs-lookup"><span data-stu-id="0372c-134">Included Tasks</span></span> | <span data-ttu-id="0372c-135">Menunjukkan jika baris sebut harga digunakan untuk semua atau sesetengah tugas projek untuk projek yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="0372c-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="0372c-136">Medan ini mempunyai nilai-nilai kebarangkalian yang berikut:</span><span class="sxs-lookup"><span data-stu-id="0372c-136">This field has the following possible values:</span></span></br><span data-ttu-id="0372c-137">- Semua tugas projek</span><span class="sxs-lookup"><span data-stu-id="0372c-137">- All project tasks</span></span></br><span data-ttu-id="0372c-138">- Tugas projek terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="0372c-138">- Selected project tasks only</span></span></br><span data-ttu-id="0372c-139">Nilai kosong dalam medan ini adalah bersamaan dengan pilihan **Semua tugas projek**.</span><span class="sxs-lookup"><span data-stu-id="0372c-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="0372c-140">Apabila **Tugas projek terpilih hanya** dipilih pada halaman projek, tab **Persediaan pengebilan tugas** membenarkan anda memilih tugas khusus untuk mengaitkannya kepada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="0372c-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="0372c-141">Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="0372c-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0372c-142">Termasuk Masa</span><span class="sxs-lookup"><span data-stu-id="0372c-142">Include Time</span></span> | <span data-ttu-id="0372c-143">Tanda **Ya**/**Tidak** menunjukkan jika transaksi masa atau kos buruh pada projek terpilih akan dimasukkan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="0372c-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="0372c-144">Nilai **Tidak** menunjukkan yang transaksi masa atau kos buruh tidak akan dimasukkan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="0372c-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="0372c-145">Nilai **Tidak** menunjukkan yang transaksi masa atau kos buruh akan dimasukkan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="0372c-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="0372c-146">Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="0372c-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0372c-147">Termasuk Perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="0372c-147">Include Expense</span></span> | <span data-ttu-id="0372c-148">Tanda **Ya**/**Tidak** menunjukkan jika kos perbelanjaan pada projek terpilih akan dimasukkan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="0372c-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="0372c-149">Nilai **Tidak** menunjukkan yang kos perbelanjaan tidak akan dimasukkan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="0372c-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="0372c-150">Nilai **Ya** menunjukkan yang kos perbelanjaan tidak akan dimasukkan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="0372c-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="0372c-151">Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="0372c-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0372c-152">Termasuk Yuran</span><span class="sxs-lookup"><span data-stu-id="0372c-152">Include Fee</span></span> | <span data-ttu-id="0372c-153">Tanda **Ya**/**Tidak** menunjukkan jika bayaran pada projek terpilih akan dimasukkan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="0372c-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="0372c-154">Nilai **Tidak** menunjukkan yang Bayaran tidak akan dimasukkan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="0372c-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="0372c-155">Nilai **Ya** menunjukkan yang Bayaran tidak akan dimasukkan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="0372c-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="0372c-156">Nilai medan ini disalin kepada baris kontrak Projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="0372c-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0372c-157">Amaun Disebut Harga</span><span class="sxs-lookup"><span data-stu-id="0372c-157">Quoted Amount</span></span> | <span data-ttu-id="0372c-158">Ini adalah jumlah yang akan disebutkan kepada pelanggan untuk semua kerja yang diramalkan pada garis sebut harga projek ini.</span><span class="sxs-lookup"><span data-stu-id="0372c-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="0372c-159">Pada sebut harga dicipta daripada peluang, nilai ini disalin daripada medan **Bajet Pelanggan** pada baris peluang.</span><span class="sxs-lookup"><span data-stu-id="0372c-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="0372c-160">Apabila baris sebut harga berasaskan projek mempunyai butiran baris, medan ini dikunci untuk pengeditan dan diringkaskan daripada jumlah pada butiran baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="0372c-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="0372c-161">Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="0372c-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0372c-162">Anggaran Cukai</span><span class="sxs-lookup"><span data-stu-id="0372c-162">Estimated Tax</span></span> | <span data-ttu-id="0372c-163">Ini adalah medan boleh diedit untuk pengguna untuk menambah anggaran jumlah cukai pada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="0372c-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="0372c-164">Apabila baris sebut harga berasaskan projek mempunyai butiran baris, medan ini dikunci untuk pengeditan dan diringkaskan daripada jumlah cukai pada butiran baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="0372c-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="0372c-165">Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="0372c-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0372c-166">Jumlah Sebut Harga selepas Cukai</span><span class="sxs-lookup"><span data-stu-id="0372c-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="0372c-167">Medan ini adalah jumlah baris sebut harga selepas cukai dan baca sahaja.</span><span class="sxs-lookup"><span data-stu-id="0372c-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="0372c-168">Jumlah dalam medan ini dikira sebagai *Jumlah Sebut Harga + Cukai*.</span><span class="sxs-lookup"><span data-stu-id="0372c-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="0372c-169">Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="0372c-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0372c-170">Had Tidak Boleh Dilebihi</span><span class="sxs-lookup"><span data-stu-id="0372c-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="0372c-171">Medan ini boleh diedit dan hanya tersedia pada baris sebut harga berasaskan projek yang mempunyai kaedah pengebilan **Masa dan Bahan**.</span><span class="sxs-lookup"><span data-stu-id="0372c-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="0372c-172">Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="0372c-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0372c-173">Belanjawan Pelanggan</span><span class="sxs-lookup"><span data-stu-id="0372c-173">Customer Budget</span></span> | <span data-ttu-id="0372c-174">Medan ini boleh diedit dan disalin daripada medan berkaitan dengan baris peluang jika sebut harga dicipta daripada peluang.</span><span class="sxs-lookup"><span data-stu-id="0372c-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="0372c-175">Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="0372c-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="0372c-176">Peraturan pengesahan untuk medan pada tab Umum bagi baris sebut harga berasaskan projek</span><span class="sxs-lookup"><span data-stu-id="0372c-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="0372c-177">**Peraturan 1**: Jika medan **Tugas yang termasuk** adalah kosong atau jika ia ditetapkan kepada **Semua tugas projek**, projek dimasukkan dalam baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="0372c-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="0372c-178">**Peraturan 2**: Jika medan **Tugas yang termasuk** adalah kosong, atau jika ia ditetapkan kepada **Semua tugas projek**, projek dan kelas transaksi tertentu hanya boleh dimasukkan pada satu baris sebut harga berasaskan projek bagi sebut harga.</span><span class="sxs-lookup"><span data-stu-id="0372c-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="0372c-179">**Peraturan 3**: Jika medan **Tugas yang termasuk** ditetapkan kepada **Hanya tugas projek terpilih**, projek dan kelas transaksi tertentu boleh dimasukkan pada berbilang baris sebut harga berasaskan projek bagi sebut harga.</span><span class="sxs-lookup"><span data-stu-id="0372c-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="0372c-180">**Peraturan 4**: Jika peluang mempunyai berbilang sebut harga, boleh terdapat baris sebut harga daripada sebut harga berbeza yang semuanya merujuk kepada projek yang sama dan termasuk kelas transaksi yang sama.</span><span class="sxs-lookup"><span data-stu-id="0372c-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="0372c-181">**Peraturan 5**: Jika sebut harga tidak tergolong kepada peluang yang sama, ia tidak boleh termasuk projek dan kelas transaksi yang sama.</span><span class="sxs-lookup"><span data-stu-id="0372c-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="0372c-182">
                    <strong>Peluang</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0372c-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="0372c-183">
                    <strong>Sebut Harga</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0372c-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="0372c-184">
                    <strong>Baris sebut harga</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0372c-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="0372c-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0372c-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="0372c-186">
                    <strong>Tugas yang disertakan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0372c-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="0372c-187">
                    <strong>Termasuk Masa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0372c-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="0372c-188">
                    <strong>Termasuk Perbelanjaan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0372c-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="0372c-189">
                    <strong>Sertakan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0372c-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="0372c-190">
                    <strong>Yuran</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0372c-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="0372c-191">
                    <strong>Sah / Tidak sah</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0372c-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="0372c-192">
                    <strong>Sebab</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0372c-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0372c-193">O1</span><span class="sxs-lookup"><span data-stu-id="0372c-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0372c-194">S1</span><span class="sxs-lookup"><span data-stu-id="0372c-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-195">QL1</span><span class="sxs-lookup"><span data-stu-id="0372c-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-196">P1</span><span class="sxs-lookup"><span data-stu-id="0372c-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0372c-197">Kosong</span><span class="sxs-lookup"><span data-stu-id="0372c-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-198">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-199">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-200">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0372c-201">Tidak sah</span><span class="sxs-lookup"><span data-stu-id="0372c-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0372c-202">Pelanggaran Peraturan #2.</span><span class="sxs-lookup"><span data-stu-id="0372c-202">Violation of Rule #2.</span></span> <span data-ttu-id="0372c-203">Masa, Perbelanjaan dan Bayaran pada projek P1 termasuk pada baris sebut harga QL1 dan QL2.</span><span class="sxs-lookup"><span data-stu-id="0372c-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0372c-204">O1</span><span class="sxs-lookup"><span data-stu-id="0372c-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0372c-205">S1</span><span class="sxs-lookup"><span data-stu-id="0372c-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-206">QL2</span><span class="sxs-lookup"><span data-stu-id="0372c-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-207">P1</span><span class="sxs-lookup"><span data-stu-id="0372c-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0372c-208">Kosong</span><span class="sxs-lookup"><span data-stu-id="0372c-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-209">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-210">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-211">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-211">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0372c-212">O1</span><span class="sxs-lookup"><span data-stu-id="0372c-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0372c-213">S1</span><span class="sxs-lookup"><span data-stu-id="0372c-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-214">QL1</span><span class="sxs-lookup"><span data-stu-id="0372c-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-215">P1</span><span class="sxs-lookup"><span data-stu-id="0372c-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0372c-216">Kosong</span><span class="sxs-lookup"><span data-stu-id="0372c-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-217">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-218">Tidak</span><span class="sxs-lookup"><span data-stu-id="0372c-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-219">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0372c-220">Tidak sah</span><span class="sxs-lookup"><span data-stu-id="0372c-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0372c-221">Pelanggaran Peraturan #2.</span><span class="sxs-lookup"><span data-stu-id="0372c-221">Violation of Rule #2.</span></span> <span data-ttu-id="0372c-222">Masa dan Bayaran pada projek P1 termasuk pada baris sebut harga QL1 dan QL2.</span><span class="sxs-lookup"><span data-stu-id="0372c-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0372c-223">O1</span><span class="sxs-lookup"><span data-stu-id="0372c-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0372c-224">S1</span><span class="sxs-lookup"><span data-stu-id="0372c-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-225">QL2</span><span class="sxs-lookup"><span data-stu-id="0372c-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-226">P1</span><span class="sxs-lookup"><span data-stu-id="0372c-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0372c-227">Kosong</span><span class="sxs-lookup"><span data-stu-id="0372c-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-228">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-229">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-230">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-230">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0372c-231">O1</span><span class="sxs-lookup"><span data-stu-id="0372c-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0372c-232">S1</span><span class="sxs-lookup"><span data-stu-id="0372c-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-233">QL1</span><span class="sxs-lookup"><span data-stu-id="0372c-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-234">P1</span><span class="sxs-lookup"><span data-stu-id="0372c-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0372c-235">Kosong</span><span class="sxs-lookup"><span data-stu-id="0372c-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-236">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-237">Tidak</span><span class="sxs-lookup"><span data-stu-id="0372c-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-238">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0372c-239">Sah</span><span class="sxs-lookup"><span data-stu-id="0372c-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="0372c-240">Masa dan Bayaran pada projek P1 termasuk dalam QL1.</span><span class="sxs-lookup"><span data-stu-id="0372c-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="0372c-241">Perbelanjaan pada projek P1 termasuk dalam QL2.</span><span class="sxs-lookup"><span data-stu-id="0372c-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="0372c-242">Tiada pertindihan dalam sebarang yang dimasukkan pada setiap baris sebut harga dan ianya sah.</span><span class="sxs-lookup"><span data-stu-id="0372c-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0372c-243">O1</span><span class="sxs-lookup"><span data-stu-id="0372c-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0372c-244">S1</span><span class="sxs-lookup"><span data-stu-id="0372c-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-245">QL2</span><span class="sxs-lookup"><span data-stu-id="0372c-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-246">P1</span><span class="sxs-lookup"><span data-stu-id="0372c-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0372c-247">Kosong</span><span class="sxs-lookup"><span data-stu-id="0372c-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-248">Tidak</span><span class="sxs-lookup"><span data-stu-id="0372c-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-249">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-250">Tidak</span><span class="sxs-lookup"><span data-stu-id="0372c-250">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0372c-251">O1</span><span class="sxs-lookup"><span data-stu-id="0372c-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0372c-252">S1</span><span class="sxs-lookup"><span data-stu-id="0372c-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-253">QL1</span><span class="sxs-lookup"><span data-stu-id="0372c-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-254">P1</span><span class="sxs-lookup"><span data-stu-id="0372c-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0372c-255">Tugas terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="0372c-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-256">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-257">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-258">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0372c-259">Tidak sah</span><span class="sxs-lookup"><span data-stu-id="0372c-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0372c-260">Pelanggaran Peraturan #2 di atas</span><span class="sxs-lookup"><span data-stu-id="0372c-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="0372c-261">Q1 termasuk Masa, Perbelanjaan dan Bayaran pada subset tugas pada projek P1.</span><span class="sxs-lookup"><span data-stu-id="0372c-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="0372c-262">QL2 termasuk Masa, Perbelanjaan dan Bayaran untuk seluruh projek P1 dan pertindihan dengan sebarang yang termasuk pada Q1.</span><span class="sxs-lookup"><span data-stu-id="0372c-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0372c-263">O1</span><span class="sxs-lookup"><span data-stu-id="0372c-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0372c-264">S1</span><span class="sxs-lookup"><span data-stu-id="0372c-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-265">QL2</span><span class="sxs-lookup"><span data-stu-id="0372c-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-266">P1</span><span class="sxs-lookup"><span data-stu-id="0372c-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0372c-267">Kosong</span><span class="sxs-lookup"><span data-stu-id="0372c-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-268">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-269">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-270">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-270">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0372c-271">O1</span><span class="sxs-lookup"><span data-stu-id="0372c-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0372c-272">S1</span><span class="sxs-lookup"><span data-stu-id="0372c-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-273">QL1</span><span class="sxs-lookup"><span data-stu-id="0372c-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-274">P1</span><span class="sxs-lookup"><span data-stu-id="0372c-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0372c-275">Tugas terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="0372c-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-276">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-277">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-278">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0372c-279">Sah</span><span class="sxs-lookup"><span data-stu-id="0372c-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0372c-280">Setiap Peraturan #3 di atas,</span><span class="sxs-lookup"><span data-stu-id="0372c-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="0372c-281">Q1 termasuk Masa, Perbelanjaan dan Bayaran pada subset tugas pada projek P1.</span><span class="sxs-lookup"><span data-stu-id="0372c-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="0372c-282">QL2 termasuk Masa, Perbelanjaan dan Bayaran untuk subset tugas pada projek P1.</span><span class="sxs-lookup"><span data-stu-id="0372c-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="0372c-283">Satu-satunya pengesahan tambahan adalah sekitar subset tugas pada QL1 yang berbeza daripada subset tugas pada QL2.</span><span class="sxs-lookup"><span data-stu-id="0372c-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="0372c-284">Ini memastikan tiada pertindihan.</span><span class="sxs-lookup"><span data-stu-id="0372c-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="0372c-285">Ini dilakukan oleh sistem apabila tugas dikaitkan.</span><span class="sxs-lookup"><span data-stu-id="0372c-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0372c-286">O1</span><span class="sxs-lookup"><span data-stu-id="0372c-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0372c-287">S1</span><span class="sxs-lookup"><span data-stu-id="0372c-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-288">QL2</span><span class="sxs-lookup"><span data-stu-id="0372c-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-289">P1</span><span class="sxs-lookup"><span data-stu-id="0372c-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0372c-290">Tugas terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="0372c-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-291">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-292">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-293">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-293">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0372c-294">O1</span><span class="sxs-lookup"><span data-stu-id="0372c-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0372c-295">S1</span><span class="sxs-lookup"><span data-stu-id="0372c-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-296">QL1</span><span class="sxs-lookup"><span data-stu-id="0372c-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-297">P1</span><span class="sxs-lookup"><span data-stu-id="0372c-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0372c-298">Semua tugas projek atau kosong</span><span class="sxs-lookup"><span data-stu-id="0372c-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-299">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-300">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-301">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="0372c-302">Sah</span><span class="sxs-lookup"><span data-stu-id="0372c-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0372c-303">Berdasarkan Peraturan #5, Q1 dan Q2 adalah dua sebut harga pada peluang yang sama, jadi ia boleh menganggarkan untuk komponen projek yang sama.</span><span class="sxs-lookup"><span data-stu-id="0372c-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0372c-304">O1</span><span class="sxs-lookup"><span data-stu-id="0372c-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0372c-305">S2</span><span class="sxs-lookup"><span data-stu-id="0372c-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-306">QL1</span><span class="sxs-lookup"><span data-stu-id="0372c-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-307">P1</span><span class="sxs-lookup"><span data-stu-id="0372c-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0372c-308">Semua tugas projek atau kosong</span><span class="sxs-lookup"><span data-stu-id="0372c-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-309">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-310">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-311">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-311">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0372c-312">O1</span><span class="sxs-lookup"><span data-stu-id="0372c-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0372c-313">S1</span><span class="sxs-lookup"><span data-stu-id="0372c-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-314">QL1</span><span class="sxs-lookup"><span data-stu-id="0372c-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-315">P1</span><span class="sxs-lookup"><span data-stu-id="0372c-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0372c-316">Semua tugas projek atau kosong</span><span class="sxs-lookup"><span data-stu-id="0372c-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-317">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-318">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-319">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="0372c-320">Sah</span><span class="sxs-lookup"><span data-stu-id="0372c-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0372c-321">Berdasarkan Peraturan #4, Q1 dan Q2 adalah dua sebut harga pada peluang yang berbeza, jadi ia boleh menganggarkan untuk komponen sama bagi projek yang sama.</span><span class="sxs-lookup"><span data-stu-id="0372c-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0372c-322">O2</span><span class="sxs-lookup"><span data-stu-id="0372c-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0372c-323">S1</span><span class="sxs-lookup"><span data-stu-id="0372c-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-324">QL1</span><span class="sxs-lookup"><span data-stu-id="0372c-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-325">P1</span><span class="sxs-lookup"><span data-stu-id="0372c-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0372c-326">Semua tugas projek atau kosong</span><span class="sxs-lookup"><span data-stu-id="0372c-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-327">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0372c-328">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0372c-329">Ya</span><span class="sxs-lookup"><span data-stu-id="0372c-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="0372c-330">Tidak Sah</span><span class="sxs-lookup"><span data-stu-id="0372c-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]