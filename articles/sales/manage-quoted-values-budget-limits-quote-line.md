---
title: Gambaran keseluruhan baris sebut harga berdasarkan projek
description: Topik ini menyediakan maklumat tentang menggunakan baris sebut harga berasaskan projek untuk kerja projek.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ea54d83b1e26d1ee3520dbfab9ba56ffd1191dc9
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181868"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="1a32c-103">Gambaran keseluruhan baris sebut harga berdasarkan projek</span><span class="sxs-lookup"><span data-stu-id="1a32c-103">Project-based quote lines overview</span></span>

<span data-ttu-id="1a32c-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="1a32c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1a32c-105">Baris sebut harga berasaskan projek direka untuk membantu menganggar kerja projek pada pembabitan.</span><span class="sxs-lookup"><span data-stu-id="1a32c-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="1a32c-106">Struktur baris sebut harga berasaskan projek dilanjutkan untuk anggaran projek dengan konsep berikut:</span><span class="sxs-lookup"><span data-stu-id="1a32c-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="1a32c-107">Kaedah Pengebilan</span><span class="sxs-lookup"><span data-stu-id="1a32c-107">Billing Method</span></span>
- <span data-ttu-id="1a32c-108">Pemetaan Projek</span><span class="sxs-lookup"><span data-stu-id="1a32c-108">Project Mapping</span></span>
- <span data-ttu-id="1a32c-109">Termasuk kelas Transaksi</span><span class="sxs-lookup"><span data-stu-id="1a32c-109">Included Transaction classes</span></span>
- <span data-ttu-id="1a32c-110">Had yang tidak boleh Melebihi</span><span class="sxs-lookup"><span data-stu-id="1a32c-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="1a32c-111">Persediaan boleh dikenakan caj</span><span class="sxs-lookup"><span data-stu-id="1a32c-111">Chargeability setup</span></span>
- <span data-ttu-id="1a32c-112">Anggaran menggunakan Butiran Baris Sebut Harga</span><span class="sxs-lookup"><span data-stu-id="1a32c-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="1a32c-113">Pelanggan baris Sebut Harga</span><span class="sxs-lookup"><span data-stu-id="1a32c-113">Quote line Customers</span></span>

<span data-ttu-id="1a32c-114">Jadual berikut menyediakan maklumat mengenai medan pada tab **Umum** baris sebut harga berasaskan projek.</span><span class="sxs-lookup"><span data-stu-id="1a32c-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="1a32c-115">Medan ini membantu menyediakan asas untuk anggaran terperinci dan dari bawah untuk kerja projek.</span><span class="sxs-lookup"><span data-stu-id="1a32c-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="1a32c-116">**Medan**</span><span class="sxs-lookup"><span data-stu-id="1a32c-116">**Field**</span></span> | <span data-ttu-id="1a32c-117">**Perihalan**</span><span class="sxs-lookup"><span data-stu-id="1a32c-117">**Description**</span></span> | <span data-ttu-id="1a32c-118">**Kesan hiliran**</span><span class="sxs-lookup"><span data-stu-id="1a32c-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="1a32c-119">Nama</span><span class="sxs-lookup"><span data-stu-id="1a32c-119">Name</span></span> | <span data-ttu-id="1a32c-120">Nama baris sebut harga yang sepatutnya boleh membantu anda mengenal pasti komponen tunggal sebut harga yang dianggarkan.</span><span class="sxs-lookup"><span data-stu-id="1a32c-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="1a32c-121">Disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="1a32c-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a32c-122">Kaedah Pengebilan</span><span class="sxs-lookup"><span data-stu-id="1a32c-122">Billing Method</span></span> | <span data-ttu-id="1a32c-123">Pada sebut harga dicipta daripada peluang, nilai ini disalin daripada medan berkaitan dengan baris peluang.</span><span class="sxs-lookup"><span data-stu-id="1a32c-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="1a32c-124">Medan ini termasuk dua model kontrak utama yang disokong oleh Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="1a32c-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="1a32c-125">- Harga tetap</span><span class="sxs-lookup"><span data-stu-id="1a32c-125">- Fixed price</span></span></br><span data-ttu-id="1a32c-126">- Masa dan bahan.</span><span class="sxs-lookup"><span data-stu-id="1a32c-126">- Time and material.</span></span>| <span data-ttu-id="1a32c-127">Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="1a32c-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a32c-128">Project</span><span class="sxs-lookup"><span data-stu-id="1a32c-128">Project</span></span> | <span data-ttu-id="1a32c-129">Gunakan medan pilihan ini untuk mengenal pasti projek yang akan digunakan untuk menyelesaikan kerja pada pembabitan ini.</span><span class="sxs-lookup"><span data-stu-id="1a32c-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="1a32c-130">Apabila projek dipetakan kepada baris sebut harga, ia membantu dengan menyediakan tugas yang dikenakan caj dan juga dengan membawa anggaran berasaskan projek kepada baris sebut harga sebagai butiran baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="1a32c-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="1a32c-131">Apabila projek tidak dipetakan kepada baris sebut harga berasaskan projek, anggaran perlu dicipta secara manual dengan mencipta setiap butiran baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="1a32c-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="1a32c-132">Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="1a32c-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a32c-133">Termasuk Masa</span><span class="sxs-lookup"><span data-stu-id="1a32c-133">Include Time</span></span> | <span data-ttu-id="1a32c-134">Tanda **Ya**/**Tidak** menunjukkan jika transaksi masa atau kos buruh pada projek terpilih akan dimasukkan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="1a32c-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="1a32c-135">Nilai **Tidak** menunjukkan yang transaksi masa atau kos buruh tidak akan dimasukkan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="1a32c-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="1a32c-136">Nilai **Tidak** menunjukkan yang transaksi masa atau kos buruh akan dimasukkan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="1a32c-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="1a32c-137">Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="1a32c-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a32c-138">Termasuk Perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="1a32c-138">Include Expense</span></span> | <span data-ttu-id="1a32c-139">Tanda **Ya**/**Tidak** menunjukkan jika kos perbelanjaan pada projek terpilih akan dimasukkan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="1a32c-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="1a32c-140">Nilai **Tidak** menunjukkan yang kos perbelanjaan tidak akan dimasukkan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="1a32c-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="1a32c-141">Nilai **Ya** menunjukkan yang kos perbelanjaan tidak akan dimasukkan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="1a32c-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="1a32c-142">Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="1a32c-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a32c-143">Termasuk Yuran</span><span class="sxs-lookup"><span data-stu-id="1a32c-143">Include Fee</span></span> | <span data-ttu-id="1a32c-144">Tanda **Ya**/**Tidak** menunjukkan jika bayaran pada projek terpilih akan dimasukkan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="1a32c-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="1a32c-145">Nilai **Tidak** menunjukkan yang Bayaran tidak akan dimasukkan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="1a32c-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="1a32c-146">Nilai **Ya** menunjukkan yang Bayaran tidak akan dimasukkan dalam anggaran pada baris sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="1a32c-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="1a32c-147">Nilai medan ini disalin kepada baris kontrak Projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="1a32c-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a32c-148">Amaun Disebut Harga</span><span class="sxs-lookup"><span data-stu-id="1a32c-148">Quoted Amount</span></span> | <span data-ttu-id="1a32c-149">Ini adalah jumlah yang akan disebutkan kepada pelanggan untuk semua kerja yang diramalkan pada garis sebut harga projek ini.</span><span class="sxs-lookup"><span data-stu-id="1a32c-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="1a32c-150">Pada sebut harga dicipta daripada peluang, nilai ini disalin daripada medan **Bajet Pelanggan** pada baris peluang.</span><span class="sxs-lookup"><span data-stu-id="1a32c-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="1a32c-151">Apabila baris sebut harga berasaskan projek mempunyai butiran baris, medan ini dikunci untuk pengeditan dan diringkaskan daripada jumlah pada butiran baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="1a32c-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="1a32c-152">Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="1a32c-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a32c-153">Anggaran Cukai</span><span class="sxs-lookup"><span data-stu-id="1a32c-153">Estimated Tax</span></span> | <span data-ttu-id="1a32c-154">Ini adalah medan boleh diedit untuk pengguna untuk menambah anggaran jumlah cukai pada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="1a32c-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="1a32c-155">Apabila baris sebut harga berasaskan projek mempunyai butiran baris, medan ini dikunci untuk pengeditan dan diringkaskan daripada jumlah cukai pada butiran baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="1a32c-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="1a32c-156">Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="1a32c-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a32c-157">Jumlah Sebut Harga selepas Cukai</span><span class="sxs-lookup"><span data-stu-id="1a32c-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="1a32c-158">Medan ini adalah jumlah baris sebut harga selepas cukai dan baca sahaja.</span><span class="sxs-lookup"><span data-stu-id="1a32c-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="1a32c-159">Jumlah dalam medan ini dikira sebagai *Jumlah Sebut Harga + Cukai*.</span><span class="sxs-lookup"><span data-stu-id="1a32c-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="1a32c-160">Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="1a32c-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a32c-161">Had Tidak Boleh Dilebihi</span><span class="sxs-lookup"><span data-stu-id="1a32c-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="1a32c-162">Medan ini boleh diedit dan hanya tersedia pada baris sebut harga berasaskan projek yang mempunyai kaedah pengebilan **Masa dan Bahan**.</span><span class="sxs-lookup"><span data-stu-id="1a32c-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="1a32c-163">Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="1a32c-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a32c-164">Belanjawan Pelanggan</span><span class="sxs-lookup"><span data-stu-id="1a32c-164">Customer Budget</span></span> | <span data-ttu-id="1a32c-165">Medan ini boleh diedit dan disalin daripada medan berkaitan dengan baris peluang jika sebut harga dicipta daripada peluang.</span><span class="sxs-lookup"><span data-stu-id="1a32c-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="1a32c-166">Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="1a32c-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="1a32c-167">Peraturan pengesahan untuk medan pada tab Umum bagi baris sebut harga berasaskan projek</span><span class="sxs-lookup"><span data-stu-id="1a32c-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="1a32c-168">**Peraturan 1**: Kelas transaksi tertentu pada projek terpilih hanya boleh dimasukkan pada satu baris sebut harga berasaskan projek bagi sebut harga.</span><span class="sxs-lookup"><span data-stu-id="1a32c-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="1a32c-169">**Peraturan 2**: Jika peluang mempunyai berbilang sebut harga, boleh terdapat baris sebut harga daripada sebut harga berbeza yang semuanya merujuk kepada projek yang sama dan termasuk kelas transaksi yang sama.</span><span class="sxs-lookup"><span data-stu-id="1a32c-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="1a32c-170">**Peraturan 3**: Jika sebut harga tidak tergolong kepada peluang yang sama, ia tidak boleh termasuk projek dan kelas transaksi yang sama.</span><span class="sxs-lookup"><span data-stu-id="1a32c-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="1a32c-171">
                    <strong>Peluang</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a32c-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="1a32c-172">
                    <strong>Sebut Harga</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a32c-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="1a32c-173">
                    <strong>Baris sebut harga</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a32c-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="1a32c-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a32c-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="1a32c-175">
                    <strong>Termasuk masa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a32c-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="1a32c-176">
                    <strong>Termasuk perbelanjaan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a32c-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="1a32c-177">
                    <strong>Sertakan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a32c-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="1a32c-178">
                    <strong>bayaran</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a32c-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="1a32c-179">
                    <strong>Sah / Tidak sah</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a32c-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="1a32c-180">
                    <strong>Sebab</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a32c-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1a32c-181">O1</span><span class="sxs-lookup"><span data-stu-id="1a32c-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a32c-182">S1</span><span class="sxs-lookup"><span data-stu-id="1a32c-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-183">QL1</span><span class="sxs-lookup"><span data-stu-id="1a32c-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-184">P1</span><span class="sxs-lookup"><span data-stu-id="1a32c-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a32c-185">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a32c-186">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-187">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a32c-188">Tidak sah</span><span class="sxs-lookup"><span data-stu-id="1a32c-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a32c-189">Pelanggaran Peraturan #1.</span><span class="sxs-lookup"><span data-stu-id="1a32c-189">Violation of Rule #1.</span></span> <span data-ttu-id="1a32c-190">Masa, Perbelanjaan dan Bayaran pada projek P1 termasuk pada kedua-dua baris sebut harga QL1 dan QL2.</span><span class="sxs-lookup"><span data-stu-id="1a32c-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1a32c-191">O1</span><span class="sxs-lookup"><span data-stu-id="1a32c-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a32c-192">S1</span><span class="sxs-lookup"><span data-stu-id="1a32c-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-193">QL2</span><span class="sxs-lookup"><span data-stu-id="1a32c-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-194">P1</span><span class="sxs-lookup"><span data-stu-id="1a32c-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a32c-195">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a32c-196">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-197">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-197">Yes</span></span> </p>
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
<span data-ttu-id="1a32c-198">O1</span><span class="sxs-lookup"><span data-stu-id="1a32c-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a32c-199">S1</span><span class="sxs-lookup"><span data-stu-id="1a32c-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-200">QL1</span><span class="sxs-lookup"><span data-stu-id="1a32c-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-201">P1</span><span class="sxs-lookup"><span data-stu-id="1a32c-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a32c-202">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a32c-203">Tidak</span><span class="sxs-lookup"><span data-stu-id="1a32c-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-204">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a32c-205">Tidak sah</span><span class="sxs-lookup"><span data-stu-id="1a32c-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a32c-206">Pelanggaran Peraturan #1.</span><span class="sxs-lookup"><span data-stu-id="1a32c-206">Violation of Rule #1.</span></span> <span data-ttu-id="1a32c-207">Masa dan Bayaran pada projek P1 termasuk pada kedua-dua baris sebut harga QL1 dan QL2.</span><span class="sxs-lookup"><span data-stu-id="1a32c-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1a32c-208">O1</span><span class="sxs-lookup"><span data-stu-id="1a32c-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a32c-209">S1</span><span class="sxs-lookup"><span data-stu-id="1a32c-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-210">QL2</span><span class="sxs-lookup"><span data-stu-id="1a32c-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-211">P1</span><span class="sxs-lookup"><span data-stu-id="1a32c-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a32c-212">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a32c-213">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-214">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-214">Yes</span></span> </p>
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
<span data-ttu-id="1a32c-215">O1</span><span class="sxs-lookup"><span data-stu-id="1a32c-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a32c-216">S1</span><span class="sxs-lookup"><span data-stu-id="1a32c-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-217">QL1</span><span class="sxs-lookup"><span data-stu-id="1a32c-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-218">P1</span><span class="sxs-lookup"><span data-stu-id="1a32c-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a32c-219">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a32c-220">Tidak</span><span class="sxs-lookup"><span data-stu-id="1a32c-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-221">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a32c-222">Sah</span><span class="sxs-lookup"><span data-stu-id="1a32c-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="1a32c-223">Masa dan bayaran pada projek P1 termasuk dalam QL1.</span><span class="sxs-lookup"><span data-stu-id="1a32c-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="1a32c-224">Perbelanjaan pada projek P1 termasuk dalam QL2.</span><span class="sxs-lookup"><span data-stu-id="1a32c-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="1a32c-225">Tiada pertindihan dalam sebarang yang dimasukkan pada setiap baris sebut harga, jadi ianya sah.</span><span class="sxs-lookup"><span data-stu-id="1a32c-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1a32c-226">O1</span><span class="sxs-lookup"><span data-stu-id="1a32c-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a32c-227">S1</span><span class="sxs-lookup"><span data-stu-id="1a32c-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-228">QL2</span><span class="sxs-lookup"><span data-stu-id="1a32c-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-229">P1</span><span class="sxs-lookup"><span data-stu-id="1a32c-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a32c-230">Tidak</span><span class="sxs-lookup"><span data-stu-id="1a32c-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a32c-231">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-232">Tidak</span><span class="sxs-lookup"><span data-stu-id="1a32c-232">No</span></span> </p>
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
<span data-ttu-id="1a32c-233">O1</span><span class="sxs-lookup"><span data-stu-id="1a32c-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a32c-234">S1</span><span class="sxs-lookup"><span data-stu-id="1a32c-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-235">QL1</span><span class="sxs-lookup"><span data-stu-id="1a32c-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-236">P1</span><span class="sxs-lookup"><span data-stu-id="1a32c-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a32c-237">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a32c-238">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-239">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a32c-240">Tidak sah</span><span class="sxs-lookup"><span data-stu-id="1a32c-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a32c-241">Pelanggaran Peraturan #1 di atas</span><span class="sxs-lookup"><span data-stu-id="1a32c-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="1a32c-242">Q1 termasuk Masa, Perbelanjaan dan Bayaran untuk seluruh projek P1.</span><span class="sxs-lookup"><span data-stu-id="1a32c-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="1a32c-243">QL2 termasuk Masa, Perbelanjaan dan Bayaran untuk seluruh projek P1 dan pertindihan dengan sebarang yang termasuk pada Q1.</span><span class="sxs-lookup"><span data-stu-id="1a32c-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1a32c-244">O1</span><span class="sxs-lookup"><span data-stu-id="1a32c-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a32c-245">S1</span><span class="sxs-lookup"><span data-stu-id="1a32c-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-246">QL2</span><span class="sxs-lookup"><span data-stu-id="1a32c-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-247">P1</span><span class="sxs-lookup"><span data-stu-id="1a32c-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a32c-248">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a32c-249">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-250">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-250">Yes</span></span> </p>
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
<span data-ttu-id="1a32c-251">O1</span><span class="sxs-lookup"><span data-stu-id="1a32c-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a32c-252">S1</span><span class="sxs-lookup"><span data-stu-id="1a32c-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-253">QL1</span><span class="sxs-lookup"><span data-stu-id="1a32c-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-254">P1</span><span class="sxs-lookup"><span data-stu-id="1a32c-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a32c-255">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a32c-256">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-257">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="1a32c-258">Sah</span><span class="sxs-lookup"><span data-stu-id="1a32c-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a32c-259">Berdasarkan Peraturan #2, Q1 dan Q2 adalah dua sebut harga pada peluang yang sama, jadi kedua-duanya boleh menganggar untuk komponen sama bagi projek.</span><span class="sxs-lookup"><span data-stu-id="1a32c-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1a32c-260">O1</span><span class="sxs-lookup"><span data-stu-id="1a32c-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a32c-261">S2</span><span class="sxs-lookup"><span data-stu-id="1a32c-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-262">QL1 pada Q2</span><span class="sxs-lookup"><span data-stu-id="1a32c-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-263">P1</span><span class="sxs-lookup"><span data-stu-id="1a32c-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a32c-264">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a32c-265">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-266">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-266">Yes</span></span> </p>
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
<span data-ttu-id="1a32c-267">O1</span><span class="sxs-lookup"><span data-stu-id="1a32c-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a32c-268">S1</span><span class="sxs-lookup"><span data-stu-id="1a32c-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-269">QL1</span><span class="sxs-lookup"><span data-stu-id="1a32c-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-270">P1</span><span class="sxs-lookup"><span data-stu-id="1a32c-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a32c-271">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a32c-272">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-273">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="1a32c-274">Sah</span><span class="sxs-lookup"><span data-stu-id="1a32c-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a32c-275">Berdasarkan Peraturan #3, Q1 dan Q2 adalah dua sebut harga pada peluang yang berbeza, jadi ia boleh menganggarkan untuk komponen sama bagi projek yang sama.</span><span class="sxs-lookup"><span data-stu-id="1a32c-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1a32c-276">O2</span><span class="sxs-lookup"><span data-stu-id="1a32c-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a32c-277">S1</span><span class="sxs-lookup"><span data-stu-id="1a32c-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-278">QL1</span><span class="sxs-lookup"><span data-stu-id="1a32c-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-279">P1</span><span class="sxs-lookup"><span data-stu-id="1a32c-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a32c-280">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a32c-281">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a32c-282">Ya</span><span class="sxs-lookup"><span data-stu-id="1a32c-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="1a32c-283">Tidak Sah</span><span class="sxs-lookup"><span data-stu-id="1a32c-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

