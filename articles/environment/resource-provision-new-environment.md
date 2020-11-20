---
title: Peruntukan persekitaran baharu
description: Topik ini memberikan maklumat tentang cara menyediakan persekitaran Operasi Projek baru.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 044a942a068b33318b98041cc94944d90c1d63c3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121184"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="fe3d6-103">Peruntukan persekitaran baharu</span><span class="sxs-lookup"><span data-stu-id="fe3d6-103">Provision a new environment</span></span>

<span data-ttu-id="fe3d6-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="fe3d6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fe3d6-105">Topik ini memberikan maklumat mengenai cara untuk menyediakan persekitaran Operasi Projek Dynamics 365 baru untuk senario berasaskan sumber/bukan stok.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="fe3d6-106">Dayakan peruntukan automatik Operasi Projek dalam projek LCS</span><span class="sxs-lookup"><span data-stu-id="fe3d6-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="fe3d6-107">Gunakan langkah berikut untuk mendayakan aliran peruntukan automatik Operasi Projek untuk projek LCS anda.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="fe3d6-108">Pergi ke [LCS](https://lcs.dynamics.com/v2) dan pilih jubin **Pengurusan ciri pratonton**.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="fe3d6-109">Dalam senarai **Ciri pratonton**, pilih **Ciri Operasi Projek**, kemudian pilih **Ciri pratonton didayakan** untuk mendayakan Operasi Projek.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="fe3d6-110">Langkah ini dilaksanakan hanya satu kali bagi setiap projek LCS.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="fe3d6-111">Menyediakan persekitaran Operasi Projek</span><span class="sxs-lookup"><span data-stu-id="fe3d6-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="fe3d6-112">Buka Dynamics 365 Finance [persekitaran demo baharu](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) atau pelaksanaan [persekitaran pengeluaran/bukan pengeluaran bersama](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="fe3d6-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="fe3d6-113">Ikuti wizard **Peruntukan persekitaran**.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="fe3d6-114">Pastikan versi aplikasi yang dipilih adalah 10.0.13 atau lebih tinggi.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="fe3d6-115">Untuk memperuntukkan Operasi Projek, di bawah **Tetapan awal**, pilih **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="fe3d6-116">Dayakan Tetapan **Common Data Service** dengan memilih **Ya** dan kemudian masukkan maklumat dalam medan yang diperlukan:</span><span class="sxs-lookup"><span data-stu-id="fe3d6-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="fe3d6-117">Nama</span><span class="sxs-lookup"><span data-stu-id="fe3d6-117">Name</span></span>
  - <span data-ttu-id="fe3d6-118">Rantau</span><span class="sxs-lookup"><span data-stu-id="fe3d6-118">Region</span></span>
  - <span data-ttu-id="fe3d6-119">Bahasa</span><span class="sxs-lookup"><span data-stu-id="fe3d6-119">Language</span></span>
  - <span data-ttu-id="fe3d6-120">Mata wang</span><span class="sxs-lookup"><span data-stu-id="fe3d6-120">Currency</span></span>
 
5. <span data-ttu-id="fe3d6-121">Dalam medan Templat **Common Data Service**, pilih **Operasi Projek**</span><span class="sxs-lookup"><span data-stu-id="fe3d6-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="fe3d6-122">Pilih jenis persekitaran untuk pelaksanaan anda.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="fe3d6-123">Percubaan berasaskan langganan membolehkan anda melaksanakan persekitaran CDS selama 30 hari.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Tetapan Pelaksanaan](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="fe3d6-125">Pilih **Setuju** untuk mengakui terma perkhidmatan dan kemudian pilih **Selesai** untuk kembali ke tetapan pelaksanaan.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Persetujuan Pelaksanaan](./media/2DeploymentConsent.png)

7. <span data-ttu-id="fe3d6-127">Lengkapkan baki medan yang diperlukan dalam wizard dan sahkan pelaksanaan.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="fe3d6-128">Masa peruntukan persekitaran berbeza mengikut jenis persekitaran.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="fe3d6-129">Peruntukan mungkin mengambil masa sehingga enam jam.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="fe3d6-130">Selepas pelaksanaan berjaya diselesaikan, persekitaran akan ditunjukkan seperti yang **Dilaksanakan**.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="fe3d6-131">Untuk mengesahkan persekitaran yang berjaya dilaksanakan, pilih **Log Masuk** dan log pada persekitaran untuk mengesahkan.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Butiran Persekitaran](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="fe3d6-133">Mohon data demo Kewangan Operasi Projek (langkah pilihan)</span><span class="sxs-lookup"><span data-stu-id="fe3d6-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="fe3d6-134">Mohon data demo Kewangan Operasi Projek ke Persekitaran Berhos Awan keluaran perkhidmatan 10.0.13 seperti yang diterangkan dalam [artikel ini](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="fe3d6-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="fe3d6-135">Gunakan kemas kini kepada persekitaran kewangan</span><span class="sxs-lookup"><span data-stu-id="fe3d6-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="fe3d6-136">Operasi Projek memerlukan persekitaran kewangan dengan versi aplikasi **10.0.13 (10.0.569.20009)** atau lebih tinggi.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="fe3d6-137">Anda mungkin perlu menggunakan kemas kini kualiti kepada persekitaran kewangan anda untuk menerima versi ini.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="fe3d6-138">Dalam LCS, pada halaman **Butiran persekitaran**, dalam bahagian **Kemas Kini Tersedia**, pilih **Lihat Kemas Kini**.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Lihat Kemas Kini](./media/5ViewUpdates.png)

2. <span data-ttu-id="fe3d6-140">Pada halaman **Kemas kini Penduaan**, pilih **Simpan pakej.**</span><span class="sxs-lookup"><span data-stu-id="fe3d6-140">On the **Binary updates** page, select **Save package.**</span></span>

![Simpan pakej](./media/6SavePackage.png)

3. <span data-ttu-id="fe3d6-142">Klik **Pilih semua** dan kemudian **Simpan pakej**.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-142">Click **Select all** and then select **Save package**.</span></span>

![Semak dan simpan kemas kini](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="fe3d6-144">Masukkan nama dan perihalan pakej, dan kemudian pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="fe3d6-145">Proses ini mungkin mengambil sedikit masa bergantung pada sambungan internet.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-145">Depending on the internet connection, this process might take some time.</span></span>

![Muat naik pakej ke Perpustakaan Aset](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="fe3d6-147">Selepas pakej disimpan, pilih **Selesai** dan simpan pakej ini ke Perpustakaan Aset dalam projek LCS anda.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="fe3d6-148">Menyimpan dan mengesahkan pakej mungkin mengambil masa ~ 15 minit.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="fe3d6-149">Untuk menggunakan kemas kini, navigasi ke halaman **Butiran persekitaran** dalam LCS dan pilih **Kekalkan** > **Gunakan kemas kini**.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Kekalkan Persekitaran](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="fe3d6-151">Dalam senarai kemas kini pilih pakej yang anda cipta dan pilih **Gunakan**.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Gunakan Kemas Kini](./media/10ApplyUpdates.png)

<span data-ttu-id="fe3d6-153">Perkhidmatan persekitaran akan mengambil sedikit masa.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-153">Environment servicing will take some time.</span></span> <span data-ttu-id="fe3d6-154">Selepas selesai, persekitaran akan kembali ke keadaan yang dilaksanakan.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-154">After it is complete, the environment will return to a deployed state.</span></span>

![Laksanakan Persekitaran](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="fe3d6-156">Wujudkan sambungan Dual Write</span><span class="sxs-lookup"><span data-stu-id="fe3d6-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="fe3d6-157">Dalam projek LCS anda, pergi ke halaman **Butiran persekitaran**.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="fe3d6-158">Di bawah Maklumat Persekitaran **Common Data Service**, pilih **Pautan ke CDS untuk Aplikasi**.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="fe3d6-159">Selepas pautan selesai, pilih **Pautkan ke CDS untuk Aplikasi** semula.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="fe3d6-160">Anda akan dihalakan semula ke Dual Write dalam kewangan.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-160">You will be redirected to Dual Write in Finance.</span></span>

![Pautkan ke CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="fe3d6-162">Pilih **Gunakan Penyelesaian** untuk mengakses entiti yang akan dipetakan dalam integrasi.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Gunakan Penyelesaian](./media/13ApplySolutions.png)

5. <span data-ttu-id="fe3d6-164">Pilih kedua-dua penyelesaian, Peta Entiti Dual Write **Dynamics 365 Finance and Operations** dan **Peta Entiti Dual Write Operasi Projek Dynamics 365**, dan kemudian pilih **Gunakan**.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Sahkan Penyelesaian](./media/14ConfirmSolutions.png)

<span data-ttu-id="fe3d6-166">Selepas penyelesaian digunakan, entiti Dual Write digunakan untuk persekitaran.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Gunakan Penyelesaian](./media/15ApplyingSolutions.png)

<span data-ttu-id="fe3d6-168">Selepas entiti digunakan, semua pemetaan yang sedia ada disenaraikan dalam persekitaran.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Peta Dual Write](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="fe3d6-170">Segar semula entiti data selepas kemas kini</span><span class="sxs-lookup"><span data-stu-id="fe3d6-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="fe3d6-171">Dalam Kewangan, pergi ke ruang kerja **Pengurusan data**.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-171">In Finance, go to the **Data management** workspace.</span></span>

![Ruang kerja Pengurusan Data](./media/16DataManagement.png)

2. <span data-ttu-id="fe3d6-173">Pilih jubin **Parameter rangka kerja**.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-173">Select the **Framework parameters** tile.</span></span>

![Parameter Rangka Kerja](./media/17FrameworkParameters.png)

3. <span data-ttu-id="fe3d6-175">Pada halaman **Tetapan entiti**, pilih senarai **Entiti Segar Semula**.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Senarai Entiti Segar Semula](./media/18RefreshEntityList.png)

<span data-ttu-id="fe3d6-177">Segar semula akan mengambil masa kira-kira 20 minit.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="fe3d6-178">Anda akan menerima isyarat apabila ia selesai.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-178">You will receive an alert when it is complete.</span></span>

![Pengesahan Segar Semula](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="fe3d6-180">Jalankan peta Dual Write Operasi Projek</span><span class="sxs-lookup"><span data-stu-id="fe3d6-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="fe3d6-181">Dalam projek LCS anda, pergi ke halaman **Butiran persekitaran**.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="fe3d6-182">Di bawah Maklumat Persekitaran **Common Data Service**, pilih **Pautkan ke CDS untuk Aplikasi.**</span><span class="sxs-lookup"><span data-stu-id="fe3d6-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="fe3d6-183">Selepas anda memilih pautan tersebut, anda akan dihalakan semula ke senarai entiti dalam pemetaan.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="fe3d6-184">Mulakan peta seperti yang diterangkan dalam jadual berikut.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="fe3d6-185">Pastikan anda mengikuti urutan seperti yang disenaraikan.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="fe3d6-186">**Peta Entiti**</span><span class="sxs-lookup"><span data-stu-id="fe3d6-186">**Entity Map**</span></span> | <span data-ttu-id="fe3d6-187">**Entiti segar semula**</span><span class="sxs-lookup"><span data-stu-id="fe3d6-187">**Refresh entity**</span></span> | <span data-ttu-id="fe3d6-188">**Penyegerakan awal**</span><span class="sxs-lookup"><span data-stu-id="fe3d6-188">**Initial sync**</span></span> | <span data-ttu-id="fe3d6-189">**Induk untuk penyegerakan awal**</span><span class="sxs-lookup"><span data-stu-id="fe3d6-189">**Master for initial sync**</span></span> | <span data-ttu-id="fe3d6-190">**Jalankan prasyarat:**</span><span class="sxs-lookup"><span data-stu-id="fe3d6-190">**Run prerequisites**</span></span> | <span data-ttu-id="fe3d6-191">**Segerakkan permulaan prasyarat**</span><span class="sxs-lookup"><span data-stu-id="fe3d6-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="fe3d6-192">**Peranan Sumber Projek untuk Semua Syarikat (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="fe3d6-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="fe3d6-193">Tidak</span><span class="sxs-lookup"><span data-stu-id="fe3d6-193">No</span></span> | <span data-ttu-id="fe3d6-194">Ya</span><span class="sxs-lookup"><span data-stu-id="fe3d6-194">Yes</span></span> | <span data-ttu-id="fe3d6-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="fe3d6-195">Common Data Service</span></span> | <span data-ttu-id="fe3d6-196">Tidak</span><span class="sxs-lookup"><span data-stu-id="fe3d6-196">No</span></span> | <span data-ttu-id="fe3d6-197">T\A</span><span class="sxs-lookup"><span data-stu-id="fe3d6-197">N\A</span></span> |
| <span data-ttu-id="fe3d6-198">**Entiti sah (cdm\_syarikat)**</span><span class="sxs-lookup"><span data-stu-id="fe3d6-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="fe3d6-199">Tidak</span><span class="sxs-lookup"><span data-stu-id="fe3d6-199">No</span></span> | <span data-ttu-id="fe3d6-200">Ya</span><span class="sxs-lookup"><span data-stu-id="fe3d6-200">Yes</span></span> | <span data-ttu-id="fe3d6-201">Aplikasi Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="fe3d6-201">Finance and Operations apps</span></span> | <span data-ttu-id="fe3d6-202">Tidak</span><span class="sxs-lookup"><span data-stu-id="fe3d6-202">No</span></span> | <span data-ttu-id="fe3d6-203">T\A</span><span class="sxs-lookup"><span data-stu-id="fe3d6-203">N\A</span></span> |
| <span data-ttu-id="fe3d6-204">**Aktual integrasi Operasi Projek (msdyn\_aktual)**</span><span class="sxs-lookup"><span data-stu-id="fe3d6-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="fe3d6-205">Tidak</span><span class="sxs-lookup"><span data-stu-id="fe3d6-205">No</span></span> | <span data-ttu-id="fe3d6-206">Tidak</span><span class="sxs-lookup"><span data-stu-id="fe3d6-206">No</span></span> | <span data-ttu-id="fe3d6-207">T\A</span><span class="sxs-lookup"><span data-stu-id="fe3d6-207">N\A</span></span> | <span data-ttu-id="fe3d6-208">Ya</span><span class="sxs-lookup"><span data-stu-id="fe3d6-208">Yes</span></span> | <span data-ttu-id="fe3d6-209">Tidak</span><span class="sxs-lookup"><span data-stu-id="fe3d6-209">No</span></span> |
| <span data-ttu-id="fe3d6-210">**Baris kontrak projek (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="fe3d6-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="fe3d6-211">Tidak</span><span class="sxs-lookup"><span data-stu-id="fe3d6-211">No</span></span> | <span data-ttu-id="fe3d6-212">Tidak</span><span class="sxs-lookup"><span data-stu-id="fe3d6-212">No</span></span> | <span data-ttu-id="fe3d6-213">T\A</span><span class="sxs-lookup"><span data-stu-id="fe3d6-213">N\A</span></span> | <span data-ttu-id="fe3d6-214">Tidak</span><span class="sxs-lookup"><span data-stu-id="fe3d6-214">No</span></span> | <span data-ttu-id="fe3d6-215">Tidak</span><span class="sxs-lookup"><span data-stu-id="fe3d6-215">No</span></span> |
| <span data-ttu-id="fe3d6-216">**Entiti integrasi untuk hubungan transaksi projek (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="fe3d6-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="fe3d6-217">Tidak</span><span class="sxs-lookup"><span data-stu-id="fe3d6-217">No</span></span> | <span data-ttu-id="fe3d6-218">Tidak</span><span class="sxs-lookup"><span data-stu-id="fe3d6-218">No</span></span> | <span data-ttu-id="fe3d6-219">T\A</span><span class="sxs-lookup"><span data-stu-id="fe3d6-219">N\A</span></span> | <span data-ttu-id="fe3d6-220">Tidak</span><span class="sxs-lookup"><span data-stu-id="fe3d6-220">No</span></span> | <span data-ttu-id="fe3d6-221">T\A</span><span class="sxs-lookup"><span data-stu-id="fe3d6-221">N\A</span></span> |
| <span data-ttu-id="fe3d6-222">**Pencapaian baris kontrak integrasi Operasi Projek (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="fe3d6-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="fe3d6-223">Tidak</span><span class="sxs-lookup"><span data-stu-id="fe3d6-223">No</span></span> | <span data-ttu-id="fe3d6-224">Tidak</span><span class="sxs-lookup"><span data-stu-id="fe3d6-224">No</span></span> | <span data-ttu-id="fe3d6-225">T\A</span><span class="sxs-lookup"><span data-stu-id="fe3d6-225">N\A</span></span> | <span data-ttu-id="fe3d6-226">Tidak</span><span class="sxs-lookup"><span data-stu-id="fe3d6-226">No</span></span> | <span data-ttu-id="fe3d6-227">T\A</span><span class="sxs-lookup"><span data-stu-id="fe3d6-227">N\A</span></span> |
| <span data-ttu-id="fe3d6-228">**Entiti integrasi Operasi Projek untuk anggaran perbelanjaan (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="fe3d6-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="fe3d6-229">Tidak</span><span class="sxs-lookup"><span data-stu-id="fe3d6-229">No</span></span> | <span data-ttu-id="fe3d6-230">Tidak</span><span class="sxs-lookup"><span data-stu-id="fe3d6-230">No</span></span> | <span data-ttu-id="fe3d6-231">T\A</span><span class="sxs-lookup"><span data-stu-id="fe3d6-231">N\A</span></span> | <span data-ttu-id="fe3d6-232">Tidak</span><span class="sxs-lookup"><span data-stu-id="fe3d6-232">No</span></span> | <span data-ttu-id="fe3d6-233">T\A</span><span class="sxs-lookup"><span data-stu-id="fe3d6-233">N\A</span></span> |
| <span data-ttu-id="fe3d6-234">**Kategori perbelanjaan projek integrasi Operasi Projek entiti eksport (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="fe3d6-234">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="fe3d6-235">Tidak</span><span class="sxs-lookup"><span data-stu-id="fe3d6-235">No</span></span> | <span data-ttu-id="fe3d6-236">Tidak</span><span class="sxs-lookup"><span data-stu-id="fe3d6-236">No</span></span> | <span data-ttu-id="fe3d6-237">T\A</span><span class="sxs-lookup"><span data-stu-id="fe3d6-237">N\A</span></span> | <span data-ttu-id="fe3d6-238">Tidak</span><span class="sxs-lookup"><span data-stu-id="fe3d6-238">No</span></span> | <span data-ttu-id="fe3d6-239">T\A</span><span class="sxs-lookup"><span data-stu-id="fe3d6-239">N\A</span></span> |
| <span data-ttu-id="fe3d6-240">**Perbelanjaan projek integrasi Operasi Projek entiti eksport (msdyn\_perbelanjaan)**</span><span class="sxs-lookup"><span data-stu-id="fe3d6-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="fe3d6-241">Ya</span><span class="sxs-lookup"><span data-stu-id="fe3d6-241">Yes</span></span> | <span data-ttu-id="fe3d6-242">Tidak</span><span class="sxs-lookup"><span data-stu-id="fe3d6-242">No</span></span> | <span data-ttu-id="fe3d6-243">T\A</span><span class="sxs-lookup"><span data-stu-id="fe3d6-243">N\A</span></span> | <span data-ttu-id="fe3d6-244">Tidak</span><span class="sxs-lookup"><span data-stu-id="fe3d6-244">No</span></span> | <span data-ttu-id="fe3d6-245">T\A</span><span class="sxs-lookup"><span data-stu-id="fe3d6-245">N\A</span></span> |
| <span data-ttu-id="fe3d6-246">**Entiti integrasi Operasi Projek untuk anggaran jam (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="fe3d6-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="fe3d6-247">Ya</span><span class="sxs-lookup"><span data-stu-id="fe3d6-247">Yes</span></span> | <span data-ttu-id="fe3d6-248">Tidak</span><span class="sxs-lookup"><span data-stu-id="fe3d6-248">No</span></span> | <span data-ttu-id="fe3d6-249">T\A</span><span class="sxs-lookup"><span data-stu-id="fe3d6-249">N\A</span></span> | <span data-ttu-id="fe3d6-250">Tidak</span><span class="sxs-lookup"><span data-stu-id="fe3d6-250">No</span></span> | <span data-ttu-id="fe3d6-251">T\A</span><span class="sxs-lookup"><span data-stu-id="fe3d6-251">N\A</span></span> |


4. <span data-ttu-id="fe3d6-252">Untuk menyegarkan semula entiti, pilih nama peta dan kemudian pilih **Segar semula entiti**.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Segar Semula Peta](./media/20RefreshMapping.png)

5. <span data-ttu-id="fe3d6-254">Selepas segar semula selesai, jalankan peta.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-254">After the refresh is complete, run the map.</span></span> <span data-ttu-id="fe3d6-255">Sebelum anda mendayakan peta seterusnya, sahkan bahawa peta dalam jadual dalam keadaan **Berjalan**.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="fe3d6-256">Jalankan peta dengan bilangan prasyarat yang lebih besar mungkin mengambil sedikit masa.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="fe3d6-257">Untuk menjalankan peta dengan prasyarat, dayakan togol **Tunjukkan peta entiti berkaitan**.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="fe3d6-258">Jika jadual menunjukkan **Penyegerakkan awal pra-syarat** **Tidak**, sahkan bahawa bendera **Penyegerakkan awal** **Dipadamkan** dalam semua peta pra-syarat sebelum anda menjalankannya.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-258">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Jalankan Peta](./media/21RunMap.png)

6. <span data-ttu-id="fe3d6-260">Mengesahkan semua peta berkaitan projek adalah dalam keadaan berjalan.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-260">Validate all project related maps are in the running state.</span></span>

![Semua Peta Berjalan](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="fe3d6-262">Gunakan data konfigurasi dalam CDS untuk Project Operations (pilihan)</span><span class="sxs-lookup"><span data-stu-id="fe3d6-262">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="fe3d6-263">Jika anda telah menggunakan data demo pada persekitaran Kewangan, lihat [sediakan dan gunakan data konfigurasi dalam Common Data Service untuk Project Operations](resource-apply-pro-setup-config-data.md) untuk menggunakan data demo pada persekitaran CDS.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-263">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="fe3d6-264">Persekitaran Operasi Projek anda kini diperuntukkan dan dikonfigurasikan.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-264">Your Project Operations environment is now provisioned and configured.</span></span> 
