---
title: Gambaran keseluruhan baris kontrak berdasarkan projek
description: Topik ini menyediakan maklumat tentang menggunakan baris kontrak berdasarkan projek.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 824fdd54d7b513b49afd1a6d76d3387df81418e2
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858169"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="9c986-103">Gambaran keseluruhan baris kontrak berdasarkan projek</span><span class="sxs-lookup"><span data-stu-id="9c986-103">Project-based contract lines overview</span></span>

<span data-ttu-id="9c986-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="9c986-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9c986-105">Baris kontrak berasaskan projek dalam Dynamics 365 Project Operations direka untuk memegang anggaran dan perjanjian pengebilan untuk komponen khusus kerja projek yang terlibat.</span><span class="sxs-lookup"><span data-stu-id="9c986-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="9c986-106">Struktur baris kontrak berasaskan projek diperluaskan untuk anggaran projek dan senario pengebilan dengan konsep berikut:</span><span class="sxs-lookup"><span data-stu-id="9c986-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="9c986-107">Kaedah pengebilan</span><span class="sxs-lookup"><span data-stu-id="9c986-107">Billing method</span></span>
- <span data-ttu-id="9c986-108">Pemetaan projek dan tugas</span><span class="sxs-lookup"><span data-stu-id="9c986-108">Project and task mapping</span></span>
- <span data-ttu-id="9c986-109">Kelas transaksi yang disertakan</span><span class="sxs-lookup"><span data-stu-id="9c986-109">Included transaction classes</span></span>
- <span data-ttu-id="9c986-110">Had yang tidak boleh melebihi</span><span class="sxs-lookup"><span data-stu-id="9c986-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="9c986-111">Persediaan boleh dikenakan caj</span><span class="sxs-lookup"><span data-stu-id="9c986-111">Chargeability setup</span></span>
- <span data-ttu-id="9c986-112">Anggaran menggunakan butiran baris kontrak</span><span class="sxs-lookup"><span data-stu-id="9c986-112">Estimates using contract line details</span></span>
- <span data-ttu-id="9c986-113">Pelanggan baris kontrak</span><span class="sxs-lookup"><span data-stu-id="9c986-113">Contract line customers</span></span>

<span data-ttu-id="9c986-114">Jadual berikut termasuk medan pada tab **Jadual** untuk baris kontrak berasaskan projek yang membantu menyediakan asas bagi penhaturan pengebilan dan anggaran yang terperinci dan berasas untuk kerja berasaskan projek.</span><span class="sxs-lookup"><span data-stu-id="9c986-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="9c986-115">Medan</span><span class="sxs-lookup"><span data-stu-id="9c986-115">Field</span></span> | <span data-ttu-id="9c986-116">Penerangan </span><span class="sxs-lookup"><span data-stu-id="9c986-116">Description</span></span> | <span data-ttu-id="9c986-117">Kesan hiliran</span><span class="sxs-lookup"><span data-stu-id="9c986-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="9c986-118">**Nama**</span><span class="sxs-lookup"><span data-stu-id="9c986-118">**Name**</span></span> | <span data-ttu-id="9c986-119">Nama baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="9c986-119">Name of the contract line.</span></span> <span data-ttu-id="9c986-120">Ini mengenal pasti komponen berasingan untuk kontrak yang sedang dianggarkan.</span><span class="sxs-lookup"><span data-stu-id="9c986-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="9c986-121">Untuk kontrak projek yang dicipta daripada sebut harga, nilai ini akan disalin daripada nilai yang sepadan dengan baris sebut harga berasaskan projek.</span><span class="sxs-lookup"><span data-stu-id="9c986-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="9c986-122">Nama disalin kepada baris invois projek yang dicipta daripada baris kontrak ini apabila invois dicipta.</span><span class="sxs-lookup"><span data-stu-id="9c986-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="9c986-123">**Kaedah Pengebilan**</span><span class="sxs-lookup"><span data-stu-id="9c986-123">**Billing Method**</span></span> | <span data-ttu-id="9c986-124">Pada kontrak projek yang dicipta daripada sebut harga, nilai ini akan disalin daripada medan yang sepadan pada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="9c986-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="9c986-125">Ini ialah set pilihan yang mewakili dua model kontrak utama yang disokong oleh Project Operations:</span><span class="sxs-lookup"><span data-stu-id="9c986-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="9c986-126">- **Harga Tetap**</span><span class="sxs-lookup"><span data-stu-id="9c986-126">- **Fixed Price**</span></span></br><span data-ttu-id="9c986-127">- **Masa dan Bahan**</span><span class="sxs-lookup"><span data-stu-id="9c986-127">- **Time and Material**</span></span> | <span data-ttu-id="9c986-128">Berdasarkan kaedah pengebilan bagi baris kontrak rujukan, transaksi sebenar akan diproses.</span><span class="sxs-lookup"><span data-stu-id="9c986-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="9c986-129">Jika baris kontrak yang dirujuk oleh aktual mempunyai kaedah pengebilan masa dan material, rekod aktual kos dan jualan yang tidak dibilkan dicipta.</span><span class="sxs-lookup"><span data-stu-id="9c986-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="9c986-130">Jika baris kontrak yang dirujuk oleh aktual mempunyai kaedah pengebilan harga tetap, hanya aktual kos dicipta.</span><span class="sxs-lookup"><span data-stu-id="9c986-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="9c986-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="9c986-131">**Project**</span></span> | <span data-ttu-id="9c986-132">Gunakan medan ini untuk mengenal pasti projek yang akan digunakan untuk menyampaikan kerja pada penglibatan ini.</span><span class="sxs-lookup"><span data-stu-id="9c986-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="9c986-133">Nilai ini akan digunakan bersama **Tugas yang disertakan** dan **Kelas Transaksi yang Disertakan** untuk menyelesaikan rujukan baris kontrak pada rekod baris aktual atau anggaran.</span><span class="sxs-lookup"><span data-stu-id="9c986-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="9c986-134">**Tugas yang Disertakan**</span><span class="sxs-lookup"><span data-stu-id="9c986-134">**Included Tasks**</span></span> | <span data-ttu-id="9c986-135">Menunjukkan sama ada baris kontrak ini termasuk semua tugas projek untuk projek yang dipilih atau hanya subset tugas.</span><span class="sxs-lookup"><span data-stu-id="9c986-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="9c986-136">Ia ialah set pilihan yang mempunyai nilai mungkin berikut:</span><span class="sxs-lookup"><span data-stu-id="9c986-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="9c986-137">- **Semua Tugas Projek**</span><span class="sxs-lookup"><span data-stu-id="9c986-137">- **All Project Tasks**</span></span></br><span data-ttu-id="9c986-138">- **Tugas Projek Terpilih Sahaja**.</span><span class="sxs-lookup"><span data-stu-id="9c986-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="9c986-139">Nilai kosong dalam medan ini adalah sama dengan memilih **Semua Tugas Projek**.</span><span class="sxs-lookup"><span data-stu-id="9c986-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="9c986-140">Jika **Tugas yang Dipilih Sahaja** dipilih, anda boleh memilih tugas khusus dan dikaitkan kepada baris kontrak ini pada tab **Persediaan Pengebilan Tugas** pada halaman **Projek**.</span><span class="sxs-lookup"><span data-stu-id="9c986-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="9c986-141">Nilai ini akan digunakan bersempena dengan **Projek** dan kelas **Transaksi yang Disertakan** untuk menyelesaikan rujukan baris kontrak pada rekod baris aktual atau anggaran.</span><span class="sxs-lookup"><span data-stu-id="9c986-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="9c986-142">**Termasuk Masa**</span><span class="sxs-lookup"><span data-stu-id="9c986-142">**Include Time**</span></span> | <span data-ttu-id="9c986-143">Nilai **Ya**/**Tidak** menunjukkan jika transaksi masa atau kos buruh pada projek yang dipilih akan disertakan pada baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="9c986-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="9c986-144">Nilai **Tiada** menunjukkan bahawa transaksi masa atau kos buruh tidak akan dimasukkan ke dalam baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="9c986-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="9c986-145">Nilai **Ya** menunjukkan bahawa transaksi masa atau kos buruh akan dimasukkan.</span><span class="sxs-lookup"><span data-stu-id="9c986-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="9c986-146">Nilai ini digunakan bersama projek untuk menyelesaikan rujukan baris kontrak pada rekod baris aktual atau anggaran.</span><span class="sxs-lookup"><span data-stu-id="9c986-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="9c986-147">**Termasuk Perbelanjaan**</span><span class="sxs-lookup"><span data-stu-id="9c986-147">**Include Expense**</span></span> | <span data-ttu-id="9c986-148">Nilai **Ya**/**Tidak** menunjukkan jika kos perbelanjaan pada projek yang dipilih akan disertakan pada baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="9c986-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="9c986-149">Nilai **Tiada** menunjukkan bahawa kos perbelanjaan tidak akan dimasukkan ke dalam baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="9c986-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="9c986-150">Nilai **Ya** menunjukkan bahawa kos perbelanjaan akan dimasukkan.</span><span class="sxs-lookup"><span data-stu-id="9c986-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="9c986-151">Nilai ini digunakan bersama projek untuk menyelesaikan rujukan baris kontrak pada rekod baris aktual atau anggaran.</span><span class="sxs-lookup"><span data-stu-id="9c986-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="9c986-152">**Termasuk Bahan**</span><span class="sxs-lookup"><span data-stu-id="9c986-152">**Include Materials**</span></span> | <span data-ttu-id="9c986-153">Nilai **Ya**/**Tidak** menunjukkan jika kos bahan pada projek yang dipilih akan disertakan pada baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="9c986-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="9c986-154">Nilai **Tidak** menunjukkan bahawa kos bahan tidak akan disertakan pada baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="9c986-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="9c986-155">Nilai **Ya** menunjukkan bahawa kos perbelanjaan akan dimasukkan.</span><span class="sxs-lookup"><span data-stu-id="9c986-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="9c986-156">Nilai ini digunakan bersama projek untuk menyelesaikan rujukan baris kontrak pada rekod baris aktual atau anggaran.</span><span class="sxs-lookup"><span data-stu-id="9c986-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="9c986-157">**Termasuk Yuran**</span><span class="sxs-lookup"><span data-stu-id="9c986-157">**Include Fee**</span></span> | <span data-ttu-id="9c986-158">Nilai **Ya**/**Tidak** menunjukkan jika yuran bagi projek yang dipilih akan disertakan pada baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="9c986-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="9c986-159">Nilai **Tiada** menunjukkan bahawa yuran tidak akan dimasukkan ke dalam baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="9c986-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="9c986-160">Nilai **Ya** menunjukkan bahawa transaksi masa atau kos buruh akan dimasukkan.</span><span class="sxs-lookup"><span data-stu-id="9c986-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="9c986-161">Nilai ini digunakan bersama projek untuk menyelesaikan rujukan baris kontrak pada rekod baris aktual atau anggaran.</span><span class="sxs-lookup"><span data-stu-id="9c986-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="9c986-162">**Amaun Dikontrakkan**</span><span class="sxs-lookup"><span data-stu-id="9c986-162">**Contracted Amount**</span></span> | <span data-ttu-id="9c986-163">Pada baris kontrak harga tetap, amaun ini yang dipersetujui yang akan diinvoiskan kepada pelanggan untuk semua komponen kerja yang berkaitan dengan baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="9c986-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="9c986-164">Pada baris kontrak masa dan bahan, amaun ini ialah nilai anggaran yang akan diinvoiskan kepada pelanggan untuk semua komponen kerja yang berkaitan dengan baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="9c986-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="9c986-165">Pada kontrak projek yang dicipta daripada sebut harga, nilai ini akan disalin daripada medan yang sepadan pada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="9c986-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="9c986-166">Apabila baris kontrak berasaskan projek mempunyai butiran baris, medan ini dikunci untuk pengeditan dan diringkaskan daripada jumlah pada butiran baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="9c986-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="9c986-167">Apabila baris kontrak mempunyai butiran baris, nilai ini boleh diubah suai dengan mengubah jumlah pada butiran baris.</span><span class="sxs-lookup"><span data-stu-id="9c986-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="9c986-168">Pada baris kontrak harga tetap, nilai ini digunakan untuk menjana amaun sebelum cukai pada pencapaian pengebilan berkala.</span><span class="sxs-lookup"><span data-stu-id="9c986-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="9c986-169">**Anggaran Cukai**</span><span class="sxs-lookup"><span data-stu-id="9c986-169">**Estimated Tax**</span></span> | <span data-ttu-id="9c986-170">Pengguna boleh mengedit medan ini untuk memasukkan anggaran jumlah cukai pada baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="9c986-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="9c986-171">Apabila baris kontrak berasaskan projek mempunyai butiran baris, medan ini dikunci untuk pengeditan dan diringkaskan daripada jumlah cukai pada butiran baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="9c986-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="9c986-172">Apabila baris kontrak mempunyai butiran baris, nilai ini boleh diubah suai dengan mengubah jumlah cukai pada butiran baris.</span><span class="sxs-lookup"><span data-stu-id="9c986-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="9c986-173">Pada baris kontrak harga tetap, nilai ini digunakan untuk menjana cukai pada pencapaian pengebilan berkala.</span><span class="sxs-lookup"><span data-stu-id="9c986-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="9c986-174">**Amaun Kontrak selepas Cukai**</span><span class="sxs-lookup"><span data-stu-id="9c986-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="9c986-175">Amaun baris kontrak selepas cukai.</span><span class="sxs-lookup"><span data-stu-id="9c986-175">The contract line amount after tax.</span></span> <span data-ttu-id="9c986-176">Medan ini ialah baca sahaja dan dikira sebagai **Amaun Kontrak + Cukai**.</span><span class="sxs-lookup"><span data-stu-id="9c986-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="9c986-177">Pada baris kontrak harga tetap, nilai ini digunakan untuk menjana pencapaian pengebilan berkala.</span><span class="sxs-lookup"><span data-stu-id="9c986-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="9c986-178">**Had Tidak Boleh Dilebihi**</span><span class="sxs-lookup"><span data-stu-id="9c986-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="9c986-179">Pengguna boleh mengedit medan ini dan ia hanya tersedia untuk baris kontrak berdasarkan projek yang menetapkan kaedah pengebilan kepada masa dan bahan.</span><span class="sxs-lookup"><span data-stu-id="9c986-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="9c986-180">Pengguna boleh mengedit medan ini.</span><span class="sxs-lookup"><span data-stu-id="9c986-180">The user can edit this field.</span></span> <span data-ttu-id="9c986-181">Apabila aktual untuk masa dan bahan merujuk kepada baris kontrak ini untuk masa dan bahan, jumlah bagi aktual dinilai dengan had tidak melebihi pada baris kontrak ini selepas mengira jumlah yang sudah dibelanjakan dan dilakukan.</span><span class="sxs-lookup"><span data-stu-id="9c986-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="9c986-182">Penilaian ini diselesaikan selepas amaun yang telah dibelanjakan dan dilakukan diambil kira.</span><span class="sxs-lookup"><span data-stu-id="9c986-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="9c986-183">**Belanjawan Pelanggan**</span><span class="sxs-lookup"><span data-stu-id="9c986-183">**Customer Budget**</span></span> | <span data-ttu-id="9c986-184">Medan ini boleh diedit dan disalin daripada medan sepadan pada baris sebut harga jika kontrak dicipta daripada sebut harga.</span><span class="sxs-lookup"><span data-stu-id="9c986-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="9c986-185">Medan ini hanya digunakan untuk maklumat dan tidak mempunyai sebarang kepentingan hiliran.</span><span class="sxs-lookup"><span data-stu-id="9c986-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="9c986-186">Peraturan pengesahan untuk pilihan pada tab Umum baris kontrak berasaskan projek</span><span class="sxs-lookup"><span data-stu-id="9c986-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="9c986-187">Peraturan 1: Jika medan **Tugas yang Disertakan** kosong atau ditetapkan kepada **Semua Tugas Projek**, semua tugas projek akan dimasukkan ke dalam baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="9c986-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="9c986-188">Peraturan 2: Apabila medan **Tugas yang Disertakan** kosong atau secara jelas ditetapkan kepada **Semua Tugas Projek**, projek dan kelas transaksi tertentu hanya boleh dimasukkan ke dalam satu baris kontrak berasaskan projek kontrak.</span><span class="sxs-lookup"><span data-stu-id="9c986-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="9c986-189">Peraturan 3: Apabila medan **Tugas yang Disertakan** ditetapkan kepada **Tugas Projek Terpilih Sahaja**, projek dan kelas transaksi tertentu boleh dimasukkan ke dalam berbilang baris kontrak berasaskan projek kontrak.</span><span class="sxs-lookup"><span data-stu-id="9c986-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="9c986-190">
                    <strong>Kontrak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9c986-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="9c986-191">
                    <strong>Baris kontrak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9c986-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="9c986-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9c986-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="9c986-193">
                    <strong>Tugas yang disertakan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9c986-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="9c986-194">
                    <strong>Termasuk Masa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9c986-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="9c986-195">
                    <strong>Termasuk Perbelanjaan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9c986-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="9c986-196">
                    <strong>Termasuk Bahan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9c986-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="9c986-197">
                    <strong>Sertakan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9c986-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="9c986-198">
                    <strong>Yuran</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9c986-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="9c986-199">
                    <strong>Sah / Tidak sah</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9c986-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="9c986-200">
                    <strong>Sebab</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9c986-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9c986-201">C1</span><span class="sxs-lookup"><span data-stu-id="9c986-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9c986-202">CL1</span><span class="sxs-lookup"><span data-stu-id="9c986-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-203">P1</span><span class="sxs-lookup"><span data-stu-id="9c986-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="9c986-204">Kosong</span><span class="sxs-lookup"><span data-stu-id="9c986-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9c986-205">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9c986-206">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-207">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-208">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9c986-209">Tidak sah</span><span class="sxs-lookup"><span data-stu-id="9c986-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9c986-210">Pelanggaran Peraturan #2.</span><span class="sxs-lookup"><span data-stu-id="9c986-210">Violation of Rule #2.</span></span> <span data-ttu-id="9c986-211">Masa, Perbelanjaan, Bahan dan Yuran projek P1 akan disertakan pada kedua-dua Baris kontrak CL1 dan CL2.</span><span class="sxs-lookup"><span data-stu-id="9c986-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9c986-212">C1</span><span class="sxs-lookup"><span data-stu-id="9c986-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9c986-213">CL2</span><span class="sxs-lookup"><span data-stu-id="9c986-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-214">P1</span><span class="sxs-lookup"><span data-stu-id="9c986-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="9c986-215">Kosong</span><span class="sxs-lookup"><span data-stu-id="9c986-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9c986-216">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9c986-217">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-218">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-219">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-219">Yes</span></span> </p>
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
<span data-ttu-id="9c986-220">C1</span><span class="sxs-lookup"><span data-stu-id="9c986-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9c986-221">CL1</span><span class="sxs-lookup"><span data-stu-id="9c986-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-222">P1</span><span class="sxs-lookup"><span data-stu-id="9c986-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="9c986-223">Kosong</span><span class="sxs-lookup"><span data-stu-id="9c986-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9c986-224">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9c986-225">Tidak</span><span class="sxs-lookup"><span data-stu-id="9c986-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-226">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-227">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9c986-228">Tidak sah</span><span class="sxs-lookup"><span data-stu-id="9c986-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9c986-229">Pelanggaran Peraturan #2.</span><span class="sxs-lookup"><span data-stu-id="9c986-229">Violation of Rule #2.</span></span> <span data-ttu-id="9c986-230">Masa, Perbelanjaan, Bahan dan Yuran projek P1 akan disertakan pada kedua-dua Baris kontrak CL1 dan CL2.</span><span class="sxs-lookup"><span data-stu-id="9c986-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9c986-231">C1</span><span class="sxs-lookup"><span data-stu-id="9c986-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9c986-232">CL2</span><span class="sxs-lookup"><span data-stu-id="9c986-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-233">P1</span><span class="sxs-lookup"><span data-stu-id="9c986-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="9c986-234">Kosong</span><span class="sxs-lookup"><span data-stu-id="9c986-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9c986-235">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9c986-236">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-237">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-238">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-238">Yes</span></span> </p>
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
<span data-ttu-id="9c986-239">C1</span><span class="sxs-lookup"><span data-stu-id="9c986-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9c986-240">CL1</span><span class="sxs-lookup"><span data-stu-id="9c986-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-241">P1</span><span class="sxs-lookup"><span data-stu-id="9c986-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="9c986-242">Kosong</span><span class="sxs-lookup"><span data-stu-id="9c986-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9c986-243">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9c986-244">Tidak</span><span class="sxs-lookup"><span data-stu-id="9c986-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-245">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-246">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9c986-247">Sah</span><span class="sxs-lookup"><span data-stu-id="9c986-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9c986-248">Masa, Bahan dan Yuran projek P1 disertakan dalam CL1.</span><span class="sxs-lookup"><span data-stu-id="9c986-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="9c986-249">Perbelanjaan pada projek P1 termasuk dalam CL2.</span><span class="sxs-lookup"><span data-stu-id="9c986-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="9c986-250">Tiada pertindihan dalam nilai yang disertakan pada setiap Baris kontrak dan oleh itu sah.</span><span class="sxs-lookup"><span data-stu-id="9c986-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9c986-251">C1</span><span class="sxs-lookup"><span data-stu-id="9c986-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9c986-252">CL2</span><span class="sxs-lookup"><span data-stu-id="9c986-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-253">P1</span><span class="sxs-lookup"><span data-stu-id="9c986-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="9c986-254">Kosong</span><span class="sxs-lookup"><span data-stu-id="9c986-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9c986-255">Tidak</span><span class="sxs-lookup"><span data-stu-id="9c986-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9c986-256">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-257">Tidak</span><span class="sxs-lookup"><span data-stu-id="9c986-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-258">Tidak</span><span class="sxs-lookup"><span data-stu-id="9c986-258">No</span></span> </p>
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
<span data-ttu-id="9c986-259">C1</span><span class="sxs-lookup"><span data-stu-id="9c986-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9c986-260">CL1</span><span class="sxs-lookup"><span data-stu-id="9c986-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-261">P1</span><span class="sxs-lookup"><span data-stu-id="9c986-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="9c986-262">Tugas terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="9c986-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9c986-263">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9c986-264">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-265">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-266">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9c986-267">Tidak sah</span><span class="sxs-lookup"><span data-stu-id="9c986-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9c986-268">Pelanggaran Peraturan #2</span><span class="sxs-lookup"><span data-stu-id="9c986-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="9c986-269">C1 termasuk Masa, Bahan, Perbelanjaan dan Yuran pada subset tugas projek P1.</span><span class="sxs-lookup"><span data-stu-id="9c986-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="9c986-270">CL2 termasuk Masa, Bahan, Perbelanjaan dan Yuran untuk seluruh projek P1 dan oleh itu bertindih dengan nilai yang dimasukkan dalam C1.</span><span class="sxs-lookup"><span data-stu-id="9c986-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9c986-271">C1</span><span class="sxs-lookup"><span data-stu-id="9c986-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9c986-272">CL2</span><span class="sxs-lookup"><span data-stu-id="9c986-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-273">P1</span><span class="sxs-lookup"><span data-stu-id="9c986-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="9c986-274">Kosong</span><span class="sxs-lookup"><span data-stu-id="9c986-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9c986-275">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9c986-276">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-277">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-278">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-278">Yes</span></span> </p>
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
<span data-ttu-id="9c986-279">C1</span><span class="sxs-lookup"><span data-stu-id="9c986-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9c986-280">CL1</span><span class="sxs-lookup"><span data-stu-id="9c986-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-281">P1</span><span class="sxs-lookup"><span data-stu-id="9c986-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="9c986-282">Tugas terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="9c986-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9c986-283">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9c986-284">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-285">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-286">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9c986-287">Sah</span><span class="sxs-lookup"><span data-stu-id="9c986-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9c986-288">Setiap Peraturan #3</span><span class="sxs-lookup"><span data-stu-id="9c986-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="9c986-289">C1 termasuk Masa, Perbelanjaan, Bahan dan Yuran pada subset tugas projek P1.</span><span class="sxs-lookup"><span data-stu-id="9c986-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="9c986-290">CL2 termasuk Masa, Perbelanjaan, Bahan dan Yuran untuk subset tugas projek P1.</span><span class="sxs-lookup"><span data-stu-id="9c986-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="9c986-291">Satu-satunya pengesahan tambahan ialah sekitar subset tugas pada CL1 berbeza daripada subset tugas pada CL2 untuk memastikan bahawa tiada pertindihan.</span><span class="sxs-lookup"><span data-stu-id="9c986-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="9c986-292">Ini dilakukan oleh sistem apabila tugas dikaitkan.</span><span class="sxs-lookup"><span data-stu-id="9c986-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9c986-293">C1</span><span class="sxs-lookup"><span data-stu-id="9c986-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="9c986-294">CL2</span><span class="sxs-lookup"><span data-stu-id="9c986-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-295">P1</span><span class="sxs-lookup"><span data-stu-id="9c986-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="9c986-296">Tugas terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="9c986-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9c986-297">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="9c986-298">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-299">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="9c986-300">Ya</span><span class="sxs-lookup"><span data-stu-id="9c986-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
