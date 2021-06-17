---
title: Gambaran keseluruhan baris kontrak berdasarkan projek
description: Topik ini menyediakan maklumat tentang menggunakan baris kontrak berdasarkan projek.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8af32b0475650db9c5862ea23d185588a631ade6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003147"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="8176f-103">Gambaran keseluruhan baris kontrak berdasarkan projek</span><span class="sxs-lookup"><span data-stu-id="8176f-103">Project-based contract lines overview</span></span>

<span data-ttu-id="8176f-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="8176f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8176f-105">Baris kontrak berasaskan projek dalam Dynamics 365 Project Operations direka untuk memegang anggaran dan perjanjian pengebilan untuk komponen khusus kerja projek yang terlibat.</span><span class="sxs-lookup"><span data-stu-id="8176f-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="8176f-106">Struktur baris kontrak berasaskan projek diperluaskan untuk anggaran projek dan senario pengebilan dengan konsep berikut:</span><span class="sxs-lookup"><span data-stu-id="8176f-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="8176f-107">Kaedah pengebilan</span><span class="sxs-lookup"><span data-stu-id="8176f-107">Billing method</span></span>
- <span data-ttu-id="8176f-108">Pemetaan projek dan tugas</span><span class="sxs-lookup"><span data-stu-id="8176f-108">Project and task mapping</span></span>
- <span data-ttu-id="8176f-109">Kelas transaksi yang disertakan</span><span class="sxs-lookup"><span data-stu-id="8176f-109">Included transaction classes</span></span>
- <span data-ttu-id="8176f-110">Had yang tidak boleh melebihi</span><span class="sxs-lookup"><span data-stu-id="8176f-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="8176f-111">Persediaan boleh dikenakan caj</span><span class="sxs-lookup"><span data-stu-id="8176f-111">Chargeability setup</span></span>
- <span data-ttu-id="8176f-112">Anggaran menggunakan butiran baris kontrak</span><span class="sxs-lookup"><span data-stu-id="8176f-112">Estimates using contract line details</span></span>
- <span data-ttu-id="8176f-113">Pelanggan baris kontrak</span><span class="sxs-lookup"><span data-stu-id="8176f-113">Contract line customers</span></span>

<span data-ttu-id="8176f-114">Jadual berikut termasuk medan pada tab **Jadual** untuk baris kontrak berasaskan projek yang membantu menyediakan asas bagi penhaturan pengebilan dan anggaran yang terperinci dan berasas untuk kerja berasaskan projek.</span><span class="sxs-lookup"><span data-stu-id="8176f-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="8176f-115">Medan</span><span class="sxs-lookup"><span data-stu-id="8176f-115">Field</span></span> | <span data-ttu-id="8176f-116">Penerangan </span><span class="sxs-lookup"><span data-stu-id="8176f-116">Description</span></span> | <span data-ttu-id="8176f-117">Kesan hiliran</span><span class="sxs-lookup"><span data-stu-id="8176f-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="8176f-118">**Nama**</span><span class="sxs-lookup"><span data-stu-id="8176f-118">**Name**</span></span> | <span data-ttu-id="8176f-119">Nama baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="8176f-119">Name of the contract line.</span></span> <span data-ttu-id="8176f-120">Ini mengenal pasti komponen berasingan untuk kontrak yang sedang dianggarkan.</span><span class="sxs-lookup"><span data-stu-id="8176f-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="8176f-121">Untuk kontrak projek yang dicipta daripada sebut harga, nilai ini akan disalin daripada nilai yang sepadan dengan baris sebut harga berasaskan projek.</span><span class="sxs-lookup"><span data-stu-id="8176f-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="8176f-122">Nama disalin kepada baris invois projek yang dicipta daripada baris kontrak ini apabila invois dicipta.</span><span class="sxs-lookup"><span data-stu-id="8176f-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="8176f-123">**Kaedah Pengebilan**</span><span class="sxs-lookup"><span data-stu-id="8176f-123">**Billing Method**</span></span> | <span data-ttu-id="8176f-124">Pada kontrak projek yang dicipta daripada sebut harga, nilai ini akan disalin daripada medan yang sepadan pada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="8176f-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="8176f-125">Ini ialah set pilihan yang mewakili dua model kontrak utama yang disokong oleh Project Operations:</span><span class="sxs-lookup"><span data-stu-id="8176f-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="8176f-126">- **Harga Tetap**</span><span class="sxs-lookup"><span data-stu-id="8176f-126">- **Fixed Price**</span></span></br><span data-ttu-id="8176f-127">- **Masa dan Bahan**</span><span class="sxs-lookup"><span data-stu-id="8176f-127">- **Time and Material**</span></span> | <span data-ttu-id="8176f-128">Berdasarkan kaedah pengebilan bagi baris kontrak rujukan, transaksi sebenar akan diproses.</span><span class="sxs-lookup"><span data-stu-id="8176f-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="8176f-129">Jika baris kontrak yang dirujuk oleh aktual mempunyai kaedah pengebilan masa dan material, rekod aktual kos dan jualan yang tidak dibilkan dicipta.</span><span class="sxs-lookup"><span data-stu-id="8176f-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="8176f-130">Jika baris kontrak yang dirujuk oleh aktual mempunyai kaedah pengebilan harga tetap, hanya aktual kos dicipta.</span><span class="sxs-lookup"><span data-stu-id="8176f-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="8176f-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="8176f-131">**Project**</span></span> | <span data-ttu-id="8176f-132">Gunakan medan ini untuk mengenal pasti projek yang akan digunakan untuk menyampaikan kerja pada penglibatan ini.</span><span class="sxs-lookup"><span data-stu-id="8176f-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="8176f-133">Nilai ini akan digunakan bersama **Tugas yang disertakan** dan **Kelas Transaksi yang Disertakan** untuk menyelesaikan rujukan baris kontrak pada rekod baris aktual atau anggaran.</span><span class="sxs-lookup"><span data-stu-id="8176f-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="8176f-134">**Tugas yang Disertakan**</span><span class="sxs-lookup"><span data-stu-id="8176f-134">**Included Tasks**</span></span> | <span data-ttu-id="8176f-135">Menunjukkan sama ada baris kontrak ini termasuk semua tugas projek untuk projek yang dipilih atau hanya subset tugas.</span><span class="sxs-lookup"><span data-stu-id="8176f-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="8176f-136">Ia ialah set pilihan yang mempunyai nilai mungkin berikut:</span><span class="sxs-lookup"><span data-stu-id="8176f-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="8176f-137">- **Semua Tugas Projek**</span><span class="sxs-lookup"><span data-stu-id="8176f-137">- **All Project Tasks**</span></span></br><span data-ttu-id="8176f-138">- **Tugas Projek Terpilih Sahaja**.</span><span class="sxs-lookup"><span data-stu-id="8176f-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="8176f-139">Nilai kosong dalam medan ini adalah sama dengan memilih **Semua Tugas Projek**.</span><span class="sxs-lookup"><span data-stu-id="8176f-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="8176f-140">Jika **Tugas yang Dipilih Sahaja** dipilih, anda boleh memilih tugas khusus dan dikaitkan kepada baris kontrak ini pada tab **Persediaan Pengebilan Tugas** pada halaman **Projek**.</span><span class="sxs-lookup"><span data-stu-id="8176f-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="8176f-141">Nilai ini akan digunakan bersempena dengan **Projek** dan kelas **Transaksi yang Disertakan** untuk menyelesaikan rujukan baris kontrak pada rekod baris aktual atau anggaran.</span><span class="sxs-lookup"><span data-stu-id="8176f-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="8176f-142">**Termasuk Masa**</span><span class="sxs-lookup"><span data-stu-id="8176f-142">**Include Time**</span></span> | <span data-ttu-id="8176f-143">Nilai **Ya**/**Tidak** menunjukkan jika transaksi masa atau kos buruh pada projek yang dipilih akan disertakan pada baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="8176f-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="8176f-144">Nilai **Tiada** menunjukkan bahawa transaksi masa atau kos buruh tidak akan dimasukkan ke dalam baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="8176f-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="8176f-145">Nilai **Ya** menunjukkan bahawa transaksi masa atau kos buruh akan dimasukkan.</span><span class="sxs-lookup"><span data-stu-id="8176f-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="8176f-146">Nilai ini digunakan bersama projek untuk menyelesaikan rujukan baris kontrak pada rekod baris aktual atau anggaran.</span><span class="sxs-lookup"><span data-stu-id="8176f-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="8176f-147">**Termasuk Perbelanjaan**</span><span class="sxs-lookup"><span data-stu-id="8176f-147">**Include Expense**</span></span> | <span data-ttu-id="8176f-148">Nilai **Ya**/**Tidak** menunjukkan jika kos perbelanjaan pada projek yang dipilih akan disertakan pada baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="8176f-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="8176f-149">Nilai **Tiada** menunjukkan bahawa kos perbelanjaan tidak akan dimasukkan ke dalam baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="8176f-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="8176f-150">Nilai **Ya** menunjukkan bahawa kos perbelanjaan akan dimasukkan.</span><span class="sxs-lookup"><span data-stu-id="8176f-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="8176f-151">Nilai ini digunakan bersama projek untuk menyelesaikan rujukan baris kontrak pada rekod baris aktual atau anggaran.</span><span class="sxs-lookup"><span data-stu-id="8176f-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="8176f-152">**Termasuk Bahan**</span><span class="sxs-lookup"><span data-stu-id="8176f-152">**Include Materials**</span></span> | <span data-ttu-id="8176f-153">Nilai **Ya**/**Tidak** menunjukkan jika kos bahan pada projek yang dipilih akan disertakan pada baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="8176f-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="8176f-154">Nilai **Tidak** menunjukkan bahawa kos bahan tidak akan disertakan pada baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="8176f-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="8176f-155">Nilai **Ya** menunjukkan bahawa kos perbelanjaan akan dimasukkan.</span><span class="sxs-lookup"><span data-stu-id="8176f-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="8176f-156">Nilai ini digunakan bersama projek untuk menyelesaikan rujukan baris kontrak pada rekod baris aktual atau anggaran.</span><span class="sxs-lookup"><span data-stu-id="8176f-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="8176f-157">**Termasuk Yuran**</span><span class="sxs-lookup"><span data-stu-id="8176f-157">**Include Fee**</span></span> | <span data-ttu-id="8176f-158">Nilai **Ya**/**Tidak** menunjukkan jika yuran bagi projek yang dipilih akan disertakan pada baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="8176f-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="8176f-159">Nilai **Tiada** menunjukkan bahawa yuran tidak akan dimasukkan ke dalam baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="8176f-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="8176f-160">Nilai **Ya** menunjukkan bahawa transaksi masa atau kos buruh akan dimasukkan.</span><span class="sxs-lookup"><span data-stu-id="8176f-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="8176f-161">Nilai ini digunakan bersama projek untuk menyelesaikan rujukan baris kontrak pada rekod baris aktual atau anggaran.</span><span class="sxs-lookup"><span data-stu-id="8176f-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="8176f-162">**Amaun Dikontrakkan**</span><span class="sxs-lookup"><span data-stu-id="8176f-162">**Contracted Amount**</span></span> | <span data-ttu-id="8176f-163">Pada baris kontrak harga tetap, amaun ini yang dipersetujui yang akan diinvoiskan kepada pelanggan untuk semua komponen kerja yang berkaitan dengan baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="8176f-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="8176f-164">Pada baris kontrak masa dan bahan, amaun ini ialah nilai anggaran yang akan diinvoiskan kepada pelanggan untuk semua komponen kerja yang berkaitan dengan baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="8176f-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="8176f-165">Pada kontrak projek yang dicipta daripada sebut harga, nilai ini akan disalin daripada medan yang sepadan pada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="8176f-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="8176f-166">Apabila baris kontrak berasaskan projek mempunyai butiran baris, medan ini dikunci untuk pengeditan dan diringkaskan daripada jumlah pada butiran baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="8176f-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="8176f-167">Apabila baris kontrak mempunyai butiran baris, nilai ini boleh diubah suai dengan mengubah jumlah pada butiran baris.</span><span class="sxs-lookup"><span data-stu-id="8176f-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="8176f-168">Pada baris kontrak harga tetap, nilai ini digunakan untuk menjana amaun sebelum cukai pada pencapaian pengebilan berkala.</span><span class="sxs-lookup"><span data-stu-id="8176f-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="8176f-169">**Anggaran Cukai**</span><span class="sxs-lookup"><span data-stu-id="8176f-169">**Estimated Tax**</span></span> | <span data-ttu-id="8176f-170">Pengguna boleh mengedit medan ini untuk memasukkan anggaran jumlah cukai pada baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="8176f-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="8176f-171">Apabila baris kontrak berasaskan projek mempunyai butiran baris, medan ini dikunci untuk pengeditan dan diringkaskan daripada jumlah cukai pada butiran baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="8176f-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="8176f-172">Apabila baris kontrak mempunyai butiran baris, nilai ini boleh diubah suai dengan mengubah jumlah cukai pada butiran baris.</span><span class="sxs-lookup"><span data-stu-id="8176f-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="8176f-173">Pada baris kontrak harga tetap, nilai ini digunakan untuk menjana cukai pada pencapaian pengebilan berkala.</span><span class="sxs-lookup"><span data-stu-id="8176f-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="8176f-174">**Amaun Kontrak selepas Cukai**</span><span class="sxs-lookup"><span data-stu-id="8176f-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="8176f-175">Amaun baris kontrak selepas cukai.</span><span class="sxs-lookup"><span data-stu-id="8176f-175">The contract line amount after tax.</span></span> <span data-ttu-id="8176f-176">Medan ini ialah baca sahaja dan dikira sebagai **Amaun Kontrak + Cukai**.</span><span class="sxs-lookup"><span data-stu-id="8176f-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="8176f-177">Pada baris kontrak harga tetap, nilai ini digunakan untuk menjana pencapaian pengebilan berkala.</span><span class="sxs-lookup"><span data-stu-id="8176f-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="8176f-178">**Had Tidak Boleh Dilebihi**</span><span class="sxs-lookup"><span data-stu-id="8176f-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="8176f-179">Pengguna boleh mengedit medan ini dan ia hanya tersedia untuk baris kontrak berdasarkan projek yang menetapkan kaedah pengebilan kepada masa dan bahan.</span><span class="sxs-lookup"><span data-stu-id="8176f-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="8176f-180">Pengguna boleh mengedit medan ini.</span><span class="sxs-lookup"><span data-stu-id="8176f-180">The user can edit this field.</span></span> <span data-ttu-id="8176f-181">Apabila aktual untuk masa dan bahan merujuk kepada baris kontrak ini untuk masa dan bahan, jumlah bagi aktual dinilai dengan had tidak melebihi pada baris kontrak ini selepas mengira jumlah yang sudah dibelanjakan dan dilakukan.</span><span class="sxs-lookup"><span data-stu-id="8176f-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="8176f-182">Penilaian ini diselesaikan selepas amaun yang telah dibelanjakan dan dilakukan diambil kira.</span><span class="sxs-lookup"><span data-stu-id="8176f-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="8176f-183">**Belanjawan Pelanggan**</span><span class="sxs-lookup"><span data-stu-id="8176f-183">**Customer Budget**</span></span> | <span data-ttu-id="8176f-184">Medan ini boleh diedit dan disalin daripada medan sepadan pada baris sebut harga jika kontrak dicipta daripada sebut harga.</span><span class="sxs-lookup"><span data-stu-id="8176f-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="8176f-185">Medan ini hanya digunakan untuk maklumat dan tidak mempunyai sebarang kepentingan hiliran.</span><span class="sxs-lookup"><span data-stu-id="8176f-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="8176f-186">Peraturan pengesahan untuk pilihan pada tab Umum baris kontrak berasaskan projek</span><span class="sxs-lookup"><span data-stu-id="8176f-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="8176f-187">Peraturan 1: Jika medan **Tugas yang Disertakan** kosong atau ditetapkan kepada **Semua Tugas Projek**, semua tugas projek akan dimasukkan ke dalam baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="8176f-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="8176f-188">Peraturan 2: Apabila medan **Tugas yang Disertakan** kosong atau secara jelas ditetapkan kepada **Semua Tugas Projek**, projek dan kelas transaksi tertentu hanya boleh dimasukkan ke dalam satu baris kontrak berasaskan projek kontrak.</span><span class="sxs-lookup"><span data-stu-id="8176f-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="8176f-189">Peraturan 3: Apabila medan **Tugas yang Disertakan** ditetapkan kepada **Tugas Projek Terpilih Sahaja**, projek dan kelas transaksi tertentu boleh dimasukkan ke dalam berbilang baris kontrak berasaskan projek kontrak.</span><span class="sxs-lookup"><span data-stu-id="8176f-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="8176f-190">
                    <strong>Kontrak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8176f-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="8176f-191">
                    <strong>Baris kontrak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8176f-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="8176f-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8176f-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="8176f-193">
                    <strong>Tugas yang disertakan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8176f-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="8176f-194">
                    <strong>Termasuk Masa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8176f-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="8176f-195">
                    <strong>Termasuk Perbelanjaan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8176f-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="8176f-196">
                    <strong>Termasuk Bahan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8176f-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="8176f-197">
                    <strong>Sertakan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8176f-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="8176f-198">
                    <strong>Yuran</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8176f-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="8176f-199">
                    <strong>Sah / Tidak sah</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8176f-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="8176f-200">
                    <strong>Sebab</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8176f-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8176f-201">C1</span><span class="sxs-lookup"><span data-stu-id="8176f-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8176f-202">CL1</span><span class="sxs-lookup"><span data-stu-id="8176f-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-203">P1</span><span class="sxs-lookup"><span data-stu-id="8176f-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="8176f-204">Kosong</span><span class="sxs-lookup"><span data-stu-id="8176f-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8176f-205">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8176f-206">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-207">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-208">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8176f-209">Tidak sah</span><span class="sxs-lookup"><span data-stu-id="8176f-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8176f-210">Pelanggaran Peraturan #2.</span><span class="sxs-lookup"><span data-stu-id="8176f-210">Violation of Rule #2.</span></span> <span data-ttu-id="8176f-211">Masa, Perbelanjaan, Bahan dan Yuran projek P1 akan disertakan pada kedua-dua Baris kontrak CL1 dan CL2.</span><span class="sxs-lookup"><span data-stu-id="8176f-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8176f-212">C1</span><span class="sxs-lookup"><span data-stu-id="8176f-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8176f-213">CL2</span><span class="sxs-lookup"><span data-stu-id="8176f-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-214">P1</span><span class="sxs-lookup"><span data-stu-id="8176f-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="8176f-215">Kosong</span><span class="sxs-lookup"><span data-stu-id="8176f-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8176f-216">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8176f-217">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-218">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-219">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8176f-220">C1</span><span class="sxs-lookup"><span data-stu-id="8176f-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8176f-221">CL1</span><span class="sxs-lookup"><span data-stu-id="8176f-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-222">P1</span><span class="sxs-lookup"><span data-stu-id="8176f-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="8176f-223">Kosong</span><span class="sxs-lookup"><span data-stu-id="8176f-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8176f-224">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8176f-225">Tidak</span><span class="sxs-lookup"><span data-stu-id="8176f-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-226">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-227">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8176f-228">Tidak sah</span><span class="sxs-lookup"><span data-stu-id="8176f-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8176f-229">Pelanggaran Peraturan #2.</span><span class="sxs-lookup"><span data-stu-id="8176f-229">Violation of Rule #2.</span></span> <span data-ttu-id="8176f-230">Masa, Perbelanjaan, Bahan dan Yuran projek P1 akan disertakan pada kedua-dua Baris kontrak CL1 dan CL2.</span><span class="sxs-lookup"><span data-stu-id="8176f-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8176f-231">C1</span><span class="sxs-lookup"><span data-stu-id="8176f-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8176f-232">CL2</span><span class="sxs-lookup"><span data-stu-id="8176f-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-233">P1</span><span class="sxs-lookup"><span data-stu-id="8176f-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="8176f-234">Kosong</span><span class="sxs-lookup"><span data-stu-id="8176f-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8176f-235">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8176f-236">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-237">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-238">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8176f-239">C1</span><span class="sxs-lookup"><span data-stu-id="8176f-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8176f-240">CL1</span><span class="sxs-lookup"><span data-stu-id="8176f-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-241">P1</span><span class="sxs-lookup"><span data-stu-id="8176f-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="8176f-242">Kosong</span><span class="sxs-lookup"><span data-stu-id="8176f-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8176f-243">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8176f-244">Tidak</span><span class="sxs-lookup"><span data-stu-id="8176f-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-245">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-246">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8176f-247">Sah</span><span class="sxs-lookup"><span data-stu-id="8176f-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8176f-248">Masa, Bahan dan Yuran projek P1 disertakan dalam CL1.</span><span class="sxs-lookup"><span data-stu-id="8176f-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="8176f-249">Perbelanjaan pada projek P1 termasuk dalam CL2.</span><span class="sxs-lookup"><span data-stu-id="8176f-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="8176f-250">Tiada pertindihan dalam nilai yang disertakan pada setiap Baris kontrak dan oleh itu sah.</span><span class="sxs-lookup"><span data-stu-id="8176f-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8176f-251">C1</span><span class="sxs-lookup"><span data-stu-id="8176f-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8176f-252">CL2</span><span class="sxs-lookup"><span data-stu-id="8176f-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-253">P1</span><span class="sxs-lookup"><span data-stu-id="8176f-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="8176f-254">Kosong</span><span class="sxs-lookup"><span data-stu-id="8176f-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8176f-255">Tidak</span><span class="sxs-lookup"><span data-stu-id="8176f-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8176f-256">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-257">Tidak</span><span class="sxs-lookup"><span data-stu-id="8176f-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-258">Tidak</span><span class="sxs-lookup"><span data-stu-id="8176f-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8176f-259">C1</span><span class="sxs-lookup"><span data-stu-id="8176f-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8176f-260">CL1</span><span class="sxs-lookup"><span data-stu-id="8176f-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-261">P1</span><span class="sxs-lookup"><span data-stu-id="8176f-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="8176f-262">Tugas terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="8176f-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8176f-263">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8176f-264">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-265">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-266">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8176f-267">Tidak sah</span><span class="sxs-lookup"><span data-stu-id="8176f-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8176f-268">Pelanggaran Peraturan #2</span><span class="sxs-lookup"><span data-stu-id="8176f-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="8176f-269">C1 termasuk Masa, Bahan, Perbelanjaan dan Yuran pada subset tugas projek P1.</span><span class="sxs-lookup"><span data-stu-id="8176f-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="8176f-270">CL2 termasuk Masa, Bahan, Perbelanjaan dan Yuran untuk seluruh projek P1 dan oleh itu bertindih dengan nilai yang dimasukkan dalam C1.</span><span class="sxs-lookup"><span data-stu-id="8176f-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8176f-271">C1</span><span class="sxs-lookup"><span data-stu-id="8176f-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8176f-272">CL2</span><span class="sxs-lookup"><span data-stu-id="8176f-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-273">P1</span><span class="sxs-lookup"><span data-stu-id="8176f-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="8176f-274">Kosong</span><span class="sxs-lookup"><span data-stu-id="8176f-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8176f-275">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8176f-276">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-277">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-278">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8176f-279">C1</span><span class="sxs-lookup"><span data-stu-id="8176f-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8176f-280">CL1</span><span class="sxs-lookup"><span data-stu-id="8176f-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-281">P1</span><span class="sxs-lookup"><span data-stu-id="8176f-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="8176f-282">Tugas terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="8176f-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8176f-283">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8176f-284">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-285">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-286">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8176f-287">Sah</span><span class="sxs-lookup"><span data-stu-id="8176f-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8176f-288">Setiap Peraturan #3</span><span class="sxs-lookup"><span data-stu-id="8176f-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="8176f-289">C1 termasuk Masa, Perbelanjaan, Bahan dan Yuran pada subset tugas projek P1.</span><span class="sxs-lookup"><span data-stu-id="8176f-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="8176f-290">CL2 termasuk Masa, Perbelanjaan, Bahan dan Yuran untuk subset tugas projek P1.</span><span class="sxs-lookup"><span data-stu-id="8176f-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="8176f-291">Satu-satunya pengesahan tambahan ialah sekitar subset tugas pada CL1 berbeza daripada subset tugas pada CL2 untuk memastikan bahawa tiada pertindihan.</span><span class="sxs-lookup"><span data-stu-id="8176f-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="8176f-292">Ini dilakukan oleh sistem apabila tugas dikaitkan.</span><span class="sxs-lookup"><span data-stu-id="8176f-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8176f-293">C1</span><span class="sxs-lookup"><span data-stu-id="8176f-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8176f-294">CL2</span><span class="sxs-lookup"><span data-stu-id="8176f-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-295">P1</span><span class="sxs-lookup"><span data-stu-id="8176f-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="8176f-296">Tugas terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="8176f-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8176f-297">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8176f-298">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-299">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8176f-300">Ya</span><span class="sxs-lookup"><span data-stu-id="8176f-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
