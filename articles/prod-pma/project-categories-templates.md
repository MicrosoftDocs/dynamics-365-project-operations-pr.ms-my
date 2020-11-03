---
title: Segerakkan kategori perbelanjaan projek antara Finance and Operations dan Project Service Automation
description: Topik ini menerangkan templat dan tugas dasar yang digunakan untuk segerakkan kategori perbelanjaan projek antara Microsoft Dynamics 365 Finance dan Dynamics 365 Project Service Automation.
author: Yowelle
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
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: ed7ca3c85d3f99b7eefe10f4ddec822b9aeb1684
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081367"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="f102f-103">Segerakkan kategori perbelanjaan projek antara Finance and Operations dan Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f102f-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f102f-104">Topik ini menerangkan templat dan tugas dasar yang digunakan untuk segerakkan kategori perbelanjaan projek antara Dynamics 365 Finance dan Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="f102f-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="f102f-105">Integrasi tugas projek, kategori transaksi perbelanjaan, anggaran jam, anggaran perbelanjaan dan penguncian fungsi tersedia dalam versi 8.0.</span><span class="sxs-lookup"><span data-stu-id="f102f-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="f102f-106">Integrasi aktual tersedia dalam versi 8.0.1 atau kemudian.</span><span class="sxs-lookup"><span data-stu-id="f102f-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="f102f-107">Jika anda menggunakan Enterprise Edition 7.3.0, selepas anda memasang KB 4132657 dan KB 4132660, anda akan dapat menggunakan templat untuk mengintegrasikan tugas projek, kategori transaksi perbelanjaan, anggaran jam, anggaran perbelanjaan dan aktual serta untuk mengkonfigurasi fungsi penguncian.</span><span class="sxs-lookup"><span data-stu-id="f102f-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="f102f-108">Jika anda mesti tetapkan semula pengedaran perakaunan, kami mengesyorkan agar anda juga memasang KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="f102f-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="f102f-109">Aliran data untuk Project Service Automation dan Finance</span><span class="sxs-lookup"><span data-stu-id="f102f-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="f102f-110">Penyelesaian integrasi Project Service Automation dan Finance menggunakan ciri Integrasi data untuk menyegerakkan data merentasi tika Project Service Automation dan Finance.</span><span class="sxs-lookup"><span data-stu-id="f102f-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="f102f-111">Templat integrasi yang tersedia dengan ciri Integrasi data mendayakan aliran data tentang kategori transaksi perbelanjaan projek antara Finance dan Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="f102f-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="f102f-112">Jika kategori perbelanjaan projek dikuasai dalam Finance, aliran integrasi adalah mulanya daripada Finance kepada Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="f102f-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="f102f-113">ID integrasi kategori perbelanjaan projek kemudian dikemas kini melalui penyegerakan daripada Project Service Automation kepada Finance.</span><span class="sxs-lookup"><span data-stu-id="f102f-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="f102f-114">Jika kategori perbelanjaan projek dikuasai dalam Project Service Automation, aliran integrasi adalah mulanya daripada Project Service Automation kepada Finance.</span><span class="sxs-lookup"><span data-stu-id="f102f-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="f102f-115">Kategori projek mesti telah dikonfigurasikan dalam Finance sebelum penyegerakan daripada Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="f102f-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="f102f-116">Kemudian segerakkan daripada Finance kembali kepada Project Service Automation, dan kemudian segerakkan daripada Project Service Automation kepada Finance semula.</span><span class="sxs-lookup"><span data-stu-id="f102f-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="f102f-117">Dengan cara ini, anda membantu menjamin bahawa kategori telah dipautkan dan tiada pendua dihasilkan.</span><span class="sxs-lookup"><span data-stu-id="f102f-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="f102f-118">Lazimnya, kategori perbelanjaan projek dikuasai dalam Finance.</span><span class="sxs-lookup"><span data-stu-id="f102f-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="f102f-119">Walau bagaimanapun, jika ia tidak dikuasai dalam Finance, atau jika kategori perbelanjaan telah dicipta dalam Project Service Automation, anda mesti segerakkan terlebih dahulu dengan menggunakan templat Kategori transaksi perbelanjaan projek (PSA kepada Fin dan Ops).</span><span class="sxs-lookup"><span data-stu-id="f102f-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="f102f-120">Kemudian segerakkan dengan menggunakan templat Kategori transaksi perbelanjaan projek (Fin dan Ops kepada PSA).</span><span class="sxs-lookup"><span data-stu-id="f102f-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="f102f-121">Kemudian anda perlu menjalankan penyegerakan daripada Project Service Automation kepada Finance sekali lagi.</span><span class="sxs-lookup"><span data-stu-id="f102f-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="f102f-122">Jika anda menyegerakkan dahulu daripada Project Service Automation, keperluan berikut mesti dipenuhi dalam Finance sebelum penyegerakan dijalankan:</span><span class="sxs-lookup"><span data-stu-id="f102f-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="f102f-123">Kategori dikongsi yang sepadan dengan kategori projek yang ditetapkan dalam Project Service Automation mesti wujud dan ia mesti didayakan untuk **Projek** dan **Perbelanjaan**.</span><span class="sxs-lookup"><span data-stu-id="f102f-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="f102f-124">Bagi setiap entiti undang-undang Finance yang mesti diintegrasikan dengannya, kategori projek berikut mesti wujud:</span><span class="sxs-lookup"><span data-stu-id="f102f-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="f102f-125">**Kategori projek** wujud.</span><span class="sxs-lookup"><span data-stu-id="f102f-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="f102f-126">**Penggunaan dalam Perbelanjaan** didayakan.</span><span class="sxs-lookup"><span data-stu-id="f102f-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="f102f-127">**Aktif dalam jurnal** didayakan.</span><span class="sxs-lookup"><span data-stu-id="f102f-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="f102f-128">**Jenis transaksi** ditetapkan kepada **Perbelanjaan**.</span><span class="sxs-lookup"><span data-stu-id="f102f-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="f102f-129">Ilustrasi berikut menunjukkan cara data disegerakkan antara Project Service Automation dan Finance.</span><span class="sxs-lookup"><span data-stu-id="f102f-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="f102f-130">[![Aliran data untuk integrasi Project Service Automation dengan Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="f102f-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="f102f-131">Penyegerakan kategori perbelanjaan projek daripada Finance kepada Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f102f-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="f102f-132">Templat dan tugas</span><span class="sxs-lookup"><span data-stu-id="f102f-132">Template and task</span></span>

<span data-ttu-id="f102f-133">Untuk mengakses templat, dalam pusat pentadbir Microsoft Power Apps, pilih **Projek** dan kemudian, di sudut kanan atas, pilih **Projek baharu** untuk memilih templat awam.</span><span class="sxs-lookup"><span data-stu-id="f102f-133">To access the template, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="f102f-134">Templat dan tugas asas berikut digunakan untuk menyegerakkan kategori perbelanjaan projek daripada Finance kepada Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="f102f-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="f102f-135">**Nama templat dalam Integrasi data:** Kategori transaksi perbelanjaan projek (Fin dan Ops kepada PSA)</span><span class="sxs-lookup"><span data-stu-id="f102f-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="f102f-136">**Nama tugas dalam projek:** Segerakkan kategori kepada PSA</span><span class="sxs-lookup"><span data-stu-id="f102f-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="f102f-137">Set entiti</span><span class="sxs-lookup"><span data-stu-id="f102f-137">Entity set</span></span>

| <span data-ttu-id="f102f-138">Finance</span><span class="sxs-lookup"><span data-stu-id="f102f-138">Finance</span></span>                           | <span data-ttu-id="f102f-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f102f-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="f102f-140">Entiti integrasi untuk kategori</span><span class="sxs-lookup"><span data-stu-id="f102f-140">Integration entity for categories</span></span> | <span data-ttu-id="f102f-141">Kategori transaksi</span><span class="sxs-lookup"><span data-stu-id="f102f-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="f102f-142">Aliran entiti</span><span class="sxs-lookup"><span data-stu-id="f102f-142">Entity flow</span></span>

<span data-ttu-id="f102f-143">Kategori perbelanjaan projek dikendalikan dalam Finance, dan disegerakkan kepada Project Service Automation sebagai kategori transaksi.</span><span class="sxs-lookup"><span data-stu-id="f102f-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="f102f-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="f102f-144">Power Query</span></span>

<span data-ttu-id="f102f-145">Apabila anda menyegerakkan kepada Project Service Automation, anda mesti menggunakan Microsoft Power Query for Excel untuk menetapkan jenis pengebilan pada kategori transaksi.</span><span class="sxs-lookup"><span data-stu-id="f102f-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="f102f-146">Templat kategori transaksi perbelanjaan projek (Fin dan Ops kepada PSA) menyediakan lajur dan pemetaan lalai.</span><span class="sxs-lookup"><span data-stu-id="f102f-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="f102f-147">Jika anda mencipta templat anda sendiri, anda mesti menambah lajur dalam Power Query.</span><span class="sxs-lookup"><span data-stu-id="f102f-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="f102f-148">Ikut langkah ini.</span><span class="sxs-lookup"><span data-stu-id="f102f-148">Follow these steps.</span></span>

1. <span data-ttu-id="f102f-149">Klik anak panah untuk membuka pemetaan tugas kategori perbelanjaan projek dalam Kategori transaksi perbelanjaan projek (Fin dan Ops kepada PSA).</span><span class="sxs-lookup"><span data-stu-id="f102f-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="f102f-150">Klik pautan **Pertanyaan Lanjutan dan Penapisan** untuk membuka Power Query.</span><span class="sxs-lookup"><span data-stu-id="f102f-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="f102f-151">Pilih **Tambah Lajur Bersyarat**.</span><span class="sxs-lookup"><span data-stu-id="f102f-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="f102f-152">Masukkan nama untuk lajur baharu, seperti **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="f102f-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="f102f-153">Masukkan syarat berikut: **jika CATEGORYID tidak sama dengan nol, maka 19235001, Sebaliknya, nol**.</span><span class="sxs-lookup"><span data-stu-id="f102f-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="f102f-154">Klik **OK** pada lajur.</span><span class="sxs-lookup"><span data-stu-id="f102f-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="f102f-155">Pastikan anda memetakan lajur baharu ini pada halaman pemetaan.</span><span class="sxs-lookup"><span data-stu-id="f102f-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="f102f-156">Ilustrasi berikut menunjukkan contoh pemetaan tugas templat dalam Integrasi data.</span><span class="sxs-lookup"><span data-stu-id="f102f-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="f102f-157">Pemetaan menunjukkan maklumat medan yang akan disegerakkan daripada Finance kepada Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="f102f-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="f102f-158">[![Kategori perbelanjaan projek kepada pemetaan templat Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="f102f-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="f102f-159">Penyegerakan kategori perbelanjaan projek daripada Project Service Automation kepada Finance</span><span class="sxs-lookup"><span data-stu-id="f102f-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="f102f-160">Templat dan tugas</span><span class="sxs-lookup"><span data-stu-id="f102f-160">Template and task</span></span>

<span data-ttu-id="f102f-161">Templat dan tugas asas berikut digunakan untuk menyegerakkan kategori perbelanjaan projek daripada Project Service Automation kepada Finance:</span><span class="sxs-lookup"><span data-stu-id="f102f-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="f102f-162">**Nama templat dalam Integrasi data:** Kategori transaksi perbelanjaan projek (PSA kepada Fin dan Ops)</span><span class="sxs-lookup"><span data-stu-id="f102f-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="f102f-163">**Nama tugas dalam projek:** Segerakkan kategori kepada Fin Ops</span><span class="sxs-lookup"><span data-stu-id="f102f-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="f102f-164">Set entiti</span><span class="sxs-lookup"><span data-stu-id="f102f-164">Entity set</span></span>

| <span data-ttu-id="f102f-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f102f-165">Project Service Automation</span></span> | <span data-ttu-id="f102f-166">Finance</span><span class="sxs-lookup"><span data-stu-id="f102f-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="f102f-167">Kategori transaksi</span><span class="sxs-lookup"><span data-stu-id="f102f-167">Transaction categories</span></span>     | <span data-ttu-id="f102f-168">Entiti integrasi untuk kategori</span><span class="sxs-lookup"><span data-stu-id="f102f-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="f102f-169">Aliran entiti</span><span class="sxs-lookup"><span data-stu-id="f102f-169">Entity flow</span></span>

<span data-ttu-id="f102f-170">Kategori perbelanjaan projek dikendalikan dalam Finance, dan disegerakkan kepada Project Service Automation sebagai kategori transaksi.</span><span class="sxs-lookup"><span data-stu-id="f102f-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="f102f-171">Penyegerakan kembali kepada Finance mengemas kini kategori projek dalam Finance dengan ID integrasi daripada Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="f102f-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f102f-172">Pemetaan tempat dalam integrasi Data</span><span class="sxs-lookup"><span data-stu-id="f102f-172">Template mapping in Data integration</span></span>

<span data-ttu-id="f102f-173">Ilustrasi berikut menunjukkan contoh pemetaan tugas templat dalam Integrasi data.</span><span class="sxs-lookup"><span data-stu-id="f102f-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="f102f-174">Pemetaan menunjukkan maklumat medan yang akan disegerakkan daripada Project Service Automation kepada Finance.</span><span class="sxs-lookup"><span data-stu-id="f102f-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="f102f-175">[![Project Service Automation kepada pemetaan templat Kewangan](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="f102f-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
