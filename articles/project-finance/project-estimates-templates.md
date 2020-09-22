---
title: Segerakkan anggaran projek secara langsung daripada Project Service Automation kepada Finance and Operations
description: Topik ini menerangkan templat dan tugas asas yang digunakan untuk menyegerakkan anggaran jam projek dan anggaran perbelanjaan projek secara langsung daripada Microsoft Dynamics 365 Project Service Automation kepada Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: d688ce9a-41e3-4ebe-952e-700f8351fbe9
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a24a967d82c2e005e61234d34da8a583b61ff7b1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753894"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="35089-103">Segerakkan anggaran projek secara langsung daripada Project Service Automation kepada Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="35089-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="35089-104">Topik ini menerangkan templat dan tugas asas yang digunakan untuk menyegerakkan anggaran jam projek dan anggaran perbelanjaan projek secara langsung daripada Dynamics 365 Project Service Automation kepada Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="35089-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="35089-105">Integrasi tugas projek, kategori transaksi perbelanjaan, anggaran jam, anggaran perbelanjaan dan penguncian fungsi tersedia dalam versi 8.0.</span><span class="sxs-lookup"><span data-stu-id="35089-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="35089-106">Integrasi aktual tersedia dalam versi 8.0.1 atau kemudian.</span><span class="sxs-lookup"><span data-stu-id="35089-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="35089-107">Aliran data untuk Project Service Automation kepada Finance</span><span class="sxs-lookup"><span data-stu-id="35089-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="35089-108">Penyelesaian integrasi Project Service Automation kepada Finance menggunakan ciri integrasi Data untuk menyegerakkan data merentasi tika Project Service Automation dan Finance.</span><span class="sxs-lookup"><span data-stu-id="35089-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="35089-109">Templat integrasi yang tersedia dengan ciri Integrasi data mendayakan aliran data tentang anggaran jam projek dan anggaran perbelanjaan projek daripada Project Service Automation kepada Kewangan.</span><span class="sxs-lookup"><span data-stu-id="35089-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="35089-110">Ilustrasi berikut menunjukkan cara data disegerakkan antara Project Service Automation dan Finance.</span><span class="sxs-lookup"><span data-stu-id="35089-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="35089-111">[![Aliran data untuk integrasi Project Service Automation dengan Kewangan](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="35089-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="35089-112">Anggaran jam projek</span><span class="sxs-lookup"><span data-stu-id="35089-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="35089-113">Templat dan tugas</span><span class="sxs-lookup"><span data-stu-id="35089-113">Template and tasks</span></span>

<span data-ttu-id="35089-114">Untuk mengakses templat yang tersedia, dalam pusat pentadbiran Microsoft Power Apps, pilih **Projek** dan kemudian, di sudut kanan atas, pilih **Projek baharu** untuk memilih templat awam.</span><span class="sxs-lookup"><span data-stu-id="35089-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="35089-115">Templat dan tugas asas berikut digunakan untuk menyegerakkan anggaran jam projek daripada Project Service Automation kepada Kewangan:</span><span class="sxs-lookup"><span data-stu-id="35089-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="35089-116">**Nama templat dalam Integrasi data:** Anggaran jam projek (PSA kepada Fin dan Ops)</span><span class="sxs-lookup"><span data-stu-id="35089-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="35089-117">**Nama tugas dalam projek:**</span><span class="sxs-lookup"><span data-stu-id="35089-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="35089-118">Hubungan transaksi</span><span class="sxs-lookup"><span data-stu-id="35089-118">Transaction relationships</span></span>
    - <span data-ttu-id="35089-119">Anggaran perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="35089-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="35089-120">Set entiti</span><span class="sxs-lookup"><span data-stu-id="35089-120">Entity set</span></span>

| <span data-ttu-id="35089-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="35089-121">Project Service Automation</span></span> | <span data-ttu-id="35089-122">Kewangan</span><span class="sxs-lookup"><span data-stu-id="35089-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="35089-123">Tugas projek</span><span class="sxs-lookup"><span data-stu-id="35089-123">Project tasks</span></span>              | <span data-ttu-id="35089-124">Entiti integrasi untuk anggaran jam projek</span><span class="sxs-lookup"><span data-stu-id="35089-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="35089-125">Aliran entiti</span><span class="sxs-lookup"><span data-stu-id="35089-125">Entity flow</span></span>

<span data-ttu-id="35089-126">Anggaran jam projek diuruskan dalam Project Service Automation dan ia disegerakkan kepada Kewangan sebagai ramalan jam projek.</span><span class="sxs-lookup"><span data-stu-id="35089-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="35089-127">Prasyarat</span><span class="sxs-lookup"><span data-stu-id="35089-127">Prerequisites</span></span>

<span data-ttu-id="35089-128">Sebelum penyegerakan anggaran jam projek boleh dijalankan, anda mesti menyegerakkan projek, tugas projek dan kategori transaksi perbelanjaan projek.</span><span class="sxs-lookup"><span data-stu-id="35089-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="35089-129">Pertanyaan Kuasa</span><span class="sxs-lookup"><span data-stu-id="35089-129">Power Query</span></span>

<span data-ttu-id="35089-130">Dalam templat anggaran jam projek, anda mesti menggunakan Microsoft Power Query for Excel untuk melengkapkan tugas ini:</span><span class="sxs-lookup"><span data-stu-id="35089-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="35089-131">Tetapkan ID model ramalan lalai yang akan digunakan apabila integrasi mencipta ramalan jam baharu.</span><span class="sxs-lookup"><span data-stu-id="35089-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="35089-132">Tapis keluar mana-mana rekod khusus sumber dalam tugas yang akan gagalkan integrasi ke dalam ramalan jam.</span><span class="sxs-lookup"><span data-stu-id="35089-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="35089-133">Tapis keluar mana-mana baris kategori transaksi yang kosong.</span><span class="sxs-lookup"><span data-stu-id="35089-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="35089-134">Kegagalan untuk melengkapkan tugas ini mungkin menghasilkan ramalan jam yang tidak betul.</span><span class="sxs-lookup"><span data-stu-id="35089-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="35089-135">Tetapkan ID model ramalan lalai</span><span class="sxs-lookup"><span data-stu-id="35089-135">Set the default forecast model ID</span></span>

<span data-ttu-id="35089-136">Untuk mengemas kini ID model ramalan lalai dalam templat, klik anak panah **Peta** untuk membuka pemetaan.</span><span class="sxs-lookup"><span data-stu-id="35089-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="35089-137">Kemudian pilih pautan **Pertanyaan Lanjutan dan Penapisan**.</span><span class="sxs-lookup"><span data-stu-id="35089-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="35089-138">Jika anda menggunakan templat anggaran jam Projek lalai (PSA kepada Fin dan Ops), pilih **Syarat yang Dimasukkan** dalam senarai **Langkah Digunakan**.</span><span class="sxs-lookup"><span data-stu-id="35089-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="35089-139">Dalam entri **Fungsi**, gantikan **O\_forecast** dengan nama ID model ramalan yang harus digunakan dengan integrasi.</span><span class="sxs-lookup"><span data-stu-id="35089-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="35089-140">Templat lalai mempunyai ID model ramalan daripada data demo.</span><span class="sxs-lookup"><span data-stu-id="35089-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="35089-141">Jika anda mencipta templat baharu, anda mesti menambah lajur ini.</span><span class="sxs-lookup"><span data-stu-id="35089-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="35089-142">Dalam Power Query, pilih **Tambah Lajur Bersyarat**, dan masukkan nama untuk lajur baharu, seperti **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="35089-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="35089-143">Masukkan syarat untuk lajur, yang, jika tugas Projek bukan nol, maka \<masukkan ID model ramalan\>; jika tidak, nol.</span><span class="sxs-lookup"><span data-stu-id="35089-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="35089-144">Tapis keluar rekod khusus sumber</span><span class="sxs-lookup"><span data-stu-id="35089-144">Filter out resource-specific records</span></span>

<span data-ttu-id="35089-145">Templat anggaran jam Projek (PSA kepada Fin dan Ops) mempunyai penapis lalai yang mengalih keluar apa-apa rekod khusus sumber.</span><span class="sxs-lookup"><span data-stu-id="35089-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="35089-146">Jika anda mencipta templat anda sendiri, anda mesti menambahkan penapis ini.</span><span class="sxs-lookup"><span data-stu-id="35089-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="35089-147">Pilih pautan **Pertanyaan Lanjutan dan Penapisan** untuk menapis pada lajur **msdyn\_islinetask** supaya hanya rekod **Salah** disertakan.</span><span class="sxs-lookup"><span data-stu-id="35089-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="35089-148">Tapis keluar baris kategori transaksi yang kosong</span><span class="sxs-lookup"><span data-stu-id="35089-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="35089-149">Anda mesti menambah penapis untuk mengalih keluar mana-mana baris yang mempunyai kategori transaksi yang kosong.</span><span class="sxs-lookup"><span data-stu-id="35089-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="35089-150">Tugas ini diperlukan, tanpa mengira sama ada anda menggunakan templat lalai atau mencipta templat anda sendiri.</span><span class="sxs-lookup"><span data-stu-id="35089-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="35089-151">Penapis ini mengalih keluar mana-mana baris ringkasan daripada Project Service Automation yang mungkin menyebabkan ramalan jam dalam Kewangan menjadi tidak betul.</span><span class="sxs-lookup"><span data-stu-id="35089-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="35089-152">Pilih pautan **Pertanyaan Lanjutan dan Penapisan** untuk menapis keluar rekod nol dalam lajur **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="35089-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="35089-153">Pemetaan tempat dalam integrasi Data</span><span class="sxs-lookup"><span data-stu-id="35089-153">Template mapping in Data integration</span></span>

<span data-ttu-id="35089-154">Ilustrasi berikut menunjukkan contoh pemetaan tugas templat dalam Integrasi data.</span><span class="sxs-lookup"><span data-stu-id="35089-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="35089-155">Pemetaan menunjukkan maklumat medan yang akan disegerakkan daripada Project Service Automation kepada Finance.</span><span class="sxs-lookup"><span data-stu-id="35089-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="35089-156">[![Pemetaan templat](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="35089-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="35089-157">Anggaran perbelanjaan projek</span><span class="sxs-lookup"><span data-stu-id="35089-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="35089-158">Templat dan tugas</span><span class="sxs-lookup"><span data-stu-id="35089-158">Template and tasks</span></span>

<span data-ttu-id="35089-159">Templat dan tugas asas berikut digunakan untuk menyegerakkan anggaran perbelanjaan projek daripada Project Service Automation kepada Kewangan:</span><span class="sxs-lookup"><span data-stu-id="35089-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="35089-160">**Nama templat dalam Integrasi data:** Anggaran perbelanjaan projek (PSA kepada Fin dan Ops)</span><span class="sxs-lookup"><span data-stu-id="35089-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="35089-161">**Nama tugas dalam projek:**</span><span class="sxs-lookup"><span data-stu-id="35089-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="35089-162">Hubungan transaksi</span><span class="sxs-lookup"><span data-stu-id="35089-162">Transaction relationships</span></span> 
    - <span data-ttu-id="35089-163">Anggaran perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="35089-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="35089-164">Set entiti</span><span class="sxs-lookup"><span data-stu-id="35089-164">Entity set</span></span>

| <span data-ttu-id="35089-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="35089-165">Project Service Automation</span></span> | <span data-ttu-id="35089-166">Kewangan</span><span class="sxs-lookup"><span data-stu-id="35089-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="35089-167">Sambungan Transaksi</span><span class="sxs-lookup"><span data-stu-id="35089-167">Transaction Connections</span></span>    | <span data-ttu-id="35089-168">Entiti integrasi untuk hubungan transaksi projek</span><span class="sxs-lookup"><span data-stu-id="35089-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="35089-169">Garisan Anggaran</span><span class="sxs-lookup"><span data-stu-id="35089-169">Estimate Lines</span></span>             | <span data-ttu-id="35089-170">Entiti integrasi untuk anggaran perbelanjaan projek</span><span class="sxs-lookup"><span data-stu-id="35089-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="35089-171">Aliran entiti</span><span class="sxs-lookup"><span data-stu-id="35089-171">Entity flow</span></span>

<span data-ttu-id="35089-172">Anggaran perbelanjaan projek diuruskan dalam Project Service Automation dan ia disegerakkan kepada Kewangan sebagai ramalan perbelanjaan projek.</span><span class="sxs-lookup"><span data-stu-id="35089-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="35089-173">Prasyarat</span><span class="sxs-lookup"><span data-stu-id="35089-173">Prerequisites</span></span>

<span data-ttu-id="35089-174">Sebelum penyegerakan anggaran perbelanjaan projek boleh dijalankan, anda mesti menyegerakkan projek, tugas projek dan kategori transaksi perbelanjaan projek.</span><span class="sxs-lookup"><span data-stu-id="35089-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="35089-175">Pertanyaan Kuasa</span><span class="sxs-lookup"><span data-stu-id="35089-175">Power Query</span></span>

<span data-ttu-id="35089-176">Dalam templat anggaran perbelanjaan projek, anda mesti menggunakan Power Query untuk melengkapkan tugas berikut:</span><span class="sxs-lookup"><span data-stu-id="35089-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="35089-177">Penapis untuk hanya menyertakan rekod baris anggaran perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="35089-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="35089-178">Tetapkan ID model ramalan lalai yang akan digunakan apabila integrasi mencipta ramalan jam baharu.</span><span class="sxs-lookup"><span data-stu-id="35089-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="35089-179">Mengubah jenis pengebilan.</span><span class="sxs-lookup"><span data-stu-id="35089-179">Transform the billing types.</span></span>
- <span data-ttu-id="35089-180">Mengubah jenis transaksi.</span><span class="sxs-lookup"><span data-stu-id="35089-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="35089-181">Penapis untuk hanya menyertakan baris anggaran perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="35089-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="35089-182">Templat anggaran perbelanjaan Projek (PSA kepada Fin dan Ops) mempunyai penapis lalai yang hanya menyertakan baris perbelanjaan dalam integrasi.</span><span class="sxs-lookup"><span data-stu-id="35089-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="35089-183">Jika anda mencipta templat anda sendiri, anda mesti menambahkan penapis ini.</span><span class="sxs-lookup"><span data-stu-id="35089-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="35089-184">Pilih tugas **Hubungan transaksi**, dan kemudian klik anak panah **Peta** untuk membuka pemetaan.</span><span class="sxs-lookup"><span data-stu-id="35089-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="35089-185">Pilih pautan **Pertanyaan Lanjutan dan Penapisan**.</span><span class="sxs-lookup"><span data-stu-id="35089-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="35089-186">Tapis lajur **msdyn\_transactiontype1** supaya ia hanya menyertakan **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="35089-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="35089-187">Tetapkan ID model ramalan lalai</span><span class="sxs-lookup"><span data-stu-id="35089-187">Set the default forecast model ID</span></span>

<span data-ttu-id="35089-188">Untuk mengemas kini ID model ramalan lalai dalam templat, pilih tugas **Anggaran perbelanjaan**, dan kemudian klik anak panah **Peta** untuk membuka pemetaan.</span><span class="sxs-lookup"><span data-stu-id="35089-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="35089-189">Pilih pautan **Pertanyaan Lanjutan dan Penapisan**.</span><span class="sxs-lookup"><span data-stu-id="35089-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="35089-190">Jika anda menggunakan templat anggaran perbelanjaan Projek lalai (PSA kepada Fin dan Ops), dalam Power Query, pilih **Syarat yang Dimasukkan** pertama daripada bahagian **Langkah Digunakan**.</span><span class="sxs-lookup"><span data-stu-id="35089-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="35089-191">Dalam entri **Fungsi**, gantikan **O\_forecast** dengan nama ID model ramalan yang harus digunakan dengan integrasi.</span><span class="sxs-lookup"><span data-stu-id="35089-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="35089-192">Templat lalai mempunyai ID model ramalan daripada data demo.</span><span class="sxs-lookup"><span data-stu-id="35089-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="35089-193">Jika anda mencipta templat baharu, anda mesti menambah lajur ini.</span><span class="sxs-lookup"><span data-stu-id="35089-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="35089-194">Dalam Power Query, pilih **Tambah Lajur Bersyarat**, dan masukkan nama untuk lajur baharu, seperti **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="35089-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="35089-195">Masukkan syarat untuk lajur, yang, jika ID baris Anggaran bukan nol, maka \<masukkan ID model ramalan\>; jika tidak, nol.</span><span class="sxs-lookup"><span data-stu-id="35089-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="35089-196">Mengubah jenis pengebilan</span><span class="sxs-lookup"><span data-stu-id="35089-196">Transform the billing types</span></span>

<span data-ttu-id="35089-197">Templat anggaran perbelanjaan Projek (PSA kepada Fin dan Ops) termasuk lajur bersyarat yang digunakan untuk mengubah jenis pengebilan yang diterima daripada Project Service Automation semasa integrasi.</span><span class="sxs-lookup"><span data-stu-id="35089-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="35089-198">Jika anda mencipta templat anda sendiri, anda mesti menambah lajur bersyarat ini.</span><span class="sxs-lookup"><span data-stu-id="35089-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="35089-199">Pilih pautan **Pertanyaan Lanjutan dan Penapisan** dan kemudian pilih **Tambah Lajur Bersyarat**.</span><span class="sxs-lookup"><span data-stu-id="35089-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="35089-200">Masukkan nama untuk lajur baharu, seperti **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="35089-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="35089-201">Kemudian masukkan syarat berikut:</span><span class="sxs-lookup"><span data-stu-id="35089-201">Then enter the following condition:</span></span>

<span data-ttu-id="35089-202">Jika **msdyn\_billingtype** = 192350000, maka **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="35089-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="35089-203">jika tidak, jika **msdyn\_billingtype** = 192350001, maka **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="35089-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="35089-204">jika tidak, jika **msdyn\_billingtype** = 192350002, maka **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="35089-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="35089-205">jika tidak, **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="35089-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="35089-206">Mengubah jenis transaksi</span><span class="sxs-lookup"><span data-stu-id="35089-206">Transform the transaction types</span></span>

<span data-ttu-id="35089-207">Templat anggaran perbelanjaan Projek (PSA kepada Fin dan Ops) termasuk lajur bersyarat yang digunakan untuk mengubah jenis transaksi yang diterima daripada Project Service Automation semasa integrasi.</span><span class="sxs-lookup"><span data-stu-id="35089-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="35089-208">Jika anda mencipta templat anda sendiri, anda mesti menambah lajur bersyarat ini.</span><span class="sxs-lookup"><span data-stu-id="35089-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="35089-209">Pilih pautan **Pertanyaan Lanjutan dan Penapisan** dan kemudian pilih **Tambah Lajur Bersyarat**.</span><span class="sxs-lookup"><span data-stu-id="35089-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="35089-210">Masukkan nama untuk lajur baharu, seperti **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="35089-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="35089-211">Kemudian masukkan syarat berikut:</span><span class="sxs-lookup"><span data-stu-id="35089-211">Then enter the following condition:</span></span>

<span data-ttu-id="35089-212">Jika **msdyn\_transactiontypecode** = 192350000, maka **Cost**</span><span class="sxs-lookup"><span data-stu-id="35089-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="35089-213">jika tidak, jika **msdyn\_transactiontypecode** = 192350005, maka **Sales**</span><span class="sxs-lookup"><span data-stu-id="35089-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="35089-214">jika tidak, **null**</span><span class="sxs-lookup"><span data-stu-id="35089-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="35089-215">Pemetaan tempat dalam integrasi Data</span><span class="sxs-lookup"><span data-stu-id="35089-215">Template mapping in Data integration</span></span>

<span data-ttu-id="35089-216">Ilustrasi yang berikut menunjukkan contoh pemetaan tugas templat dalam integrasi Data.</span><span class="sxs-lookup"><span data-stu-id="35089-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="35089-217">Pemetaan menunjukkan maklumat medan yang akan disegerakkan daripada Project Service Automation kepada Finance.</span><span class="sxs-lookup"><span data-stu-id="35089-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="35089-218">[![Pemetaan templat](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="35089-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="35089-219">[![Pemetaan templat](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="35089-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
