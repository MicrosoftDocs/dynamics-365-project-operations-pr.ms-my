---
title: Peruntukan persekitaran baharu
description: Topik ini memberikan maklumat tentang cara menyediakan persekitaran Operasi Projek baru.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 50e623d3716c9dd03ce34ec293ba57b5d966d39e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276899"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="4a6d9-103">Peruntukan persekitaran baharu</span><span class="sxs-lookup"><span data-stu-id="4a6d9-103">Provision a new environment</span></span>

<span data-ttu-id="4a6d9-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="4a6d9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="4a6d9-105">Topik ini menyediakan maklumat tentang cara untuk memperuntukkan persekitaran Dynamics 365 Project Operations baharu untuk senarroi berdasarkan sumber/tidak distok.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="4a6d9-106">Dayakan peruntukan automatik Operasi Projek dalam projek LCS</span><span class="sxs-lookup"><span data-stu-id="4a6d9-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="4a6d9-107">Gunakan langkah berikut untuk mendayakan aliran peruntukan automatik Operasi Projek untuk projek LCS anda.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="4a6d9-108">Pergi ke [LCS](https://lcs.dynamics.com/v2) dan pilih jubin **Pengurusan ciri pratonton**.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="4a6d9-109">Dalam senarai **Ciri pratonton**, pilih **Ciri Operasi Projek**, kemudian pilih **Ciri pratonton didayakan** untuk mendayakan Operasi Projek.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="4a6d9-110">Langkah ini dilaksanakan hanya satu kali bagi setiap projek LCS.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="4a6d9-111">Menyediakan persekitaran Operasi Projek</span><span class="sxs-lookup"><span data-stu-id="4a6d9-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="4a6d9-112">Buka Dynamics 365 Finance [persekitaran demo baharu](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) atau pelaksanaan [persekitaran pengeluaran/bukan pengeluaran bersama](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="4a6d9-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="4a6d9-113">Ikuti wizard **Peruntukan persekitaran**.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="4a6d9-114">Pastikan versi aplikasi yang dipilih adalah 10.0.13 atau lebih tinggi.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="4a6d9-115">Untuk memperuntukkan Operasi Projek, di bawah **Tetapan awal**, pilih **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="4a6d9-116">Dayakan Tetapan **Common Data Service** dengan memilih **Ya** dan kemudian masukkan maklumat dalam medan yang diperlukan:</span><span class="sxs-lookup"><span data-stu-id="4a6d9-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="4a6d9-117">Nama</span><span class="sxs-lookup"><span data-stu-id="4a6d9-117">Name</span></span>
  - <span data-ttu-id="4a6d9-118">Rantau</span><span class="sxs-lookup"><span data-stu-id="4a6d9-118">Region</span></span>
  - <span data-ttu-id="4a6d9-119">Bahasa</span><span class="sxs-lookup"><span data-stu-id="4a6d9-119">Language</span></span>
  - <span data-ttu-id="4a6d9-120">Mata wang</span><span class="sxs-lookup"><span data-stu-id="4a6d9-120">Currency</span></span>
 
5. <span data-ttu-id="4a6d9-121">Dalam medan Templat **Common Data Service**, pilih **Operasi Projek**</span><span class="sxs-lookup"><span data-stu-id="4a6d9-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="4a6d9-122">Pilih jenis persekitaran untuk pelaksanaan anda.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="4a6d9-123">Percubaan berasaskan langganan membolehkan anda melaksanakan persekitaran CDS selama 30 hari.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Tetapan Pelaksanaan](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="4a6d9-125">Pilih **Setuju** untuk mengakui terma perkhidmatan dan kemudian pilih **Selesai** untuk kembali ke tetapan pelaksanaan.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Persetujuan Pelaksanaan](./media/2DeploymentConsent.png)

7. <span data-ttu-id="4a6d9-127">Pilihan - Gunakan data demo pada persekitaran.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="4a6d9-128">Pergi ke **Tetapan lanjutan**, pilih **Sesuaikan Konfigurasi Pangkalan Data SQL**, dan tetapkan **Nyatakan set data untuk pangkalan data Aplikasi** kepada **Demo**.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="4a6d9-129">Lengkapkan baki medan yang diperlukan dalam wizard dan sahkan pelaksanaan.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="4a6d9-130">Masa untuk peruntukan persekitaran berbeza berdasarkan pada jenis persekitaran.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="4a6d9-131">Peruntukan mungkin mengambil masa sehingga enam jam.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="4a6d9-132">Selepas pelaksanaan berjaya diselesaikan, persekitaran akan ditunjukkan seperti yang **Dilaksanakan**.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="4a6d9-133">Untuk mengesahkan bahawa persekitaran telah berjaya digunakan, pilih **Log masuk** dan log masuk pada persekitaran untuk mengesahkan.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Butiran Persekitaran](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="4a6d9-135">Gunakan kemas kini kepada persekitaran kewangan</span><span class="sxs-lookup"><span data-stu-id="4a6d9-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="4a6d9-136">Operasi Projek memerlukan persekitaran kewangan dengan versi aplikasi **10.0.13 (10.0.569.20009)** atau lebih tinggi.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="4a6d9-137">Anda mungkin perlu menggunakan kemas kini kualiti kepada persekitaran kewangan anda untuk menerima versi ini.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="4a6d9-138">Dalam LCS, pada halaman **Butiran persekitaran**, dalam bahagian **Kemas Kini Tersedia**, pilih **Lihat Kemas Kini**.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Lihat Kemas Kini](./media/5ViewUpdates.png)

2. <span data-ttu-id="4a6d9-140">Pada halaman **Kemas kini binari**, pilih **Simpan pakej.**</span><span class="sxs-lookup"><span data-stu-id="4a6d9-140">On the **Binary updates** page, select **Save package.**</span></span>

![Simpan pakej](./media/6SavePackage.png)

3. <span data-ttu-id="4a6d9-142">Klik **Pilih semua** dan kemudian **Simpan pakej**.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-142">Click **Select all** and then select **Save package**.</span></span>

![Semak dan simpan kemas kini](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="4a6d9-144">Masukkan nama dan perihalan pakej, dan kemudian pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="4a6d9-145">Proses ini mungkin mengambil sedikit masa bergantung pada sambungan internet.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-145">Depending on the internet connection, this process might take some time.</span></span>

![Muat naik pakej ke Perpustakaan Aset](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="4a6d9-147">Selepas pakej disimpan, pilih **Selesai** dan simpan pakej ini ke Perpustakaan Aset dalam projek LCS anda.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="4a6d9-148">Menyimpan dan mengesahkan pakej mungkin mengambil masa ~ 15 minit.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="4a6d9-149">Untuk menggunakan kemas kini, navigasi ke halaman **Butiran persekitaran** dalam LCS dan pilih **Kekalkan** > **Gunakan kemas kini**.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Kekalkan Persekitaran](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="4a6d9-151">Dalam senarai kemas kini pilih pakej yang anda cipta dan pilih **Gunakan**.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Gunakan Kemas Kini](./media/10ApplyUpdates.png)

<span data-ttu-id="4a6d9-153">Perkhidmatan persekitaran akan mengambil sedikit masa.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-153">Environment servicing will take some time.</span></span> <span data-ttu-id="4a6d9-154">Selepas selesai, persekitaran akan kembali ke keadaan yang dilaksanakan.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-154">After it is complete, the environment will return to a deployed state.</span></span>

![Laksanakan Persekitaran](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="4a6d9-156">Wujudkan sambungan Dual Write</span><span class="sxs-lookup"><span data-stu-id="4a6d9-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="4a6d9-157">Dalam projek LCS anda, pergi ke halaman **Butiran persekitaran**.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="4a6d9-158">Di bawah Maklumat Persekitaran **Common Data Service**, pilih **Pautan ke CDS untuk Aplikasi**.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="4a6d9-159">Selepas pautan selesai, pilih **Pautkan ke CDS untuk Aplikasi** semula.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="4a6d9-160">Anda akan dihalakan semula ke Dual Write dalam kewangan.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-160">You will be redirected to Dual Write in Finance.</span></span>

![Pautkan ke CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="4a6d9-162">Pilih **Gunakan Penyelesaian** untuk mengakses entiti yang akan dipetakan dalam integrasi.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Gunakan Penyelesaian](./media/13ApplySolutions.png)

5. <span data-ttu-id="4a6d9-164">Pilih kedua-dua penyelesaian, **Peta Entiti Dwi Tulis Dynamics 365 Finance and Operations** dan **Peta Entiti Dwi Tulis Dynamics 365 Project Operations**, dan kemudian pilih **Gunakan**.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Sahkan Penyelesaian](./media/14ConfirmSolutions.png)

<span data-ttu-id="4a6d9-166">Selepas penyelesaian digunakan, entiti Dual Write digunakan untuk persekitaran.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Gunakan Penyelesaian](./media/15ApplyingSolutions.png)

<span data-ttu-id="4a6d9-168">Selepas entiti digunakan, semua pemetaan yang sedia ada disenaraikan dalam persekitaran.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Peta Dual Write](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="4a6d9-170">Segar semula entiti data selepas kemas kini</span><span class="sxs-lookup"><span data-stu-id="4a6d9-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="4a6d9-171">Dalam Kewangan, pergi ke ruang kerja **Pengurusan data**.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-171">In Finance, go to the **Data management** workspace.</span></span>

![Ruang kerja Pengurusan Data](./media/16DataManagement.png)

2. <span data-ttu-id="4a6d9-173">Pilih jubin **Parameter rangka kerja**.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-173">Select the **Framework parameters** tile.</span></span>

![Parameter Rangka Kerja](./media/17FrameworkParameters.png)

3. <span data-ttu-id="4a6d9-175">Pada halaman **Tetapan entiti**, pilih senarai **Entiti Segar Semula**.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Senarai Entiti Segar Semula](./media/18RefreshEntityList.png)

<span data-ttu-id="4a6d9-177">Segar semula akan mengambil masa kira-kira 20 minit.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="4a6d9-178">Anda akan menerima isyarat apabila ia selesai.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-178">You will receive an alert when it is complete.</span></span>

![Pengesahan Segar Semula](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="4a6d9-180">Kemas kini tetapan keselamatan pada Project Operations pada Dataverse</span><span class="sxs-lookup"><span data-stu-id="4a6d9-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="4a6d9-181">Pergi ke Project Operations pada persekitaran Dataverse anda.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="4a6d9-182">Pergi ke **Tetapan** > **Keselamatan** > **Peranan keselamatan**.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="4a6d9-183">Pada halaman **Peranan keselamatan**, dalam senarai peranan, pilih **pengguna aplikasi dwitulis** dan pilih tab **Entiti Tersuai**.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="4a6d9-184">Sahkan bahawa peranan mempunyai keizinan **Baca** dan **Tambah Pada** untuk:</span><span class="sxs-lookup"><span data-stu-id="4a6d9-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="4a6d9-185">**Jenis Kadar Tukaran Mata Wang**</span><span class="sxs-lookup"><span data-stu-id="4a6d9-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="4a6d9-186">**Carta Akaun**</span><span class="sxs-lookup"><span data-stu-id="4a6d9-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="4a6d9-187">**Kalendar Fiskal**</span><span class="sxs-lookup"><span data-stu-id="4a6d9-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="4a6d9-188">**Lejar**</span><span class="sxs-lookup"><span data-stu-id="4a6d9-188">**Ledger**</span></span>

5. <span data-ttu-id="4a6d9-189">Selepas peranan keselamatan dikemas kini, pergi ke **Tetapan** > **Keselamatan** > **Pasukan**, dan pilih pasukan lalai dalam paparan pasukan **Pemilik Perniagaan Tempatan**.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="4a6d9-190">Pilih **Urus Peranan** dan sahkan bahawa kelayakan keselamatan **pengguna aplikasi dwitulis** telah dikenakan kepada mereka.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="4a6d9-191">Jalankan peta Dual Write Operasi Projek</span><span class="sxs-lookup"><span data-stu-id="4a6d9-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="4a6d9-192">Dalam projek LCS anda, pergi ke halaman **Butiran persekitaran**.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="4a6d9-193">Di bawah Maklumat Persekitaran **Common Data Service**, pilih **Pautkan ke CDS untuk Aplikasi.**</span><span class="sxs-lookup"><span data-stu-id="4a6d9-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="4a6d9-194">Selepas anda memilih pautan tersebut, anda akan dihalakan semula ke senarai entiti dalam pemetaan.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="4a6d9-195">Mulakan peta seperti yang diterangkan dalam jadual berikut.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="4a6d9-196">Pastikan anda mengikuti urutan seperti yang disenaraikan.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="4a6d9-197">**Peta Entiti**</span><span class="sxs-lookup"><span data-stu-id="4a6d9-197">**Entity Map**</span></span> | <span data-ttu-id="4a6d9-198">**Entiti segar semula**</span><span class="sxs-lookup"><span data-stu-id="4a6d9-198">**Refresh entity**</span></span> | <span data-ttu-id="4a6d9-199">**Penyegerakan awal**</span><span class="sxs-lookup"><span data-stu-id="4a6d9-199">**Initial sync**</span></span> | <span data-ttu-id="4a6d9-200">**Induk untuk penyegerakan awal**</span><span class="sxs-lookup"><span data-stu-id="4a6d9-200">**Master for initial sync**</span></span> | <span data-ttu-id="4a6d9-201">**Jalankan prasyarat:**</span><span class="sxs-lookup"><span data-stu-id="4a6d9-201">**Run prerequisites**</span></span> | <span data-ttu-id="4a6d9-202">**Segerakkan permulaan prasyarat**</span><span class="sxs-lookup"><span data-stu-id="4a6d9-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="4a6d9-203">**Peranan Sumber Projek untuk Semua Syarikat (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="4a6d9-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="4a6d9-204">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-204">No</span></span> | <span data-ttu-id="4a6d9-205">Ya</span><span class="sxs-lookup"><span data-stu-id="4a6d9-205">Yes</span></span> | <span data-ttu-id="4a6d9-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4a6d9-206">Common Data Service</span></span> | <span data-ttu-id="4a6d9-207">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-207">No</span></span> | <span data-ttu-id="4a6d9-208">T\A</span><span class="sxs-lookup"><span data-stu-id="4a6d9-208">N\A</span></span> |
| <span data-ttu-id="4a6d9-209">**Entiti sah (cdm\_syarikat)**</span><span class="sxs-lookup"><span data-stu-id="4a6d9-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="4a6d9-210">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-210">No</span></span> | <span data-ttu-id="4a6d9-211">Ya</span><span class="sxs-lookup"><span data-stu-id="4a6d9-211">Yes</span></span> | <span data-ttu-id="4a6d9-212">Aplikasi Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4a6d9-212">Finance and Operations apps</span></span> | <span data-ttu-id="4a6d9-213">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-213">No</span></span> | <span data-ttu-id="4a6d9-214">T\A</span><span class="sxs-lookup"><span data-stu-id="4a6d9-214">N\A</span></span> |
| <span data-ttu-id="4a6d9-215">**Lejar (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="4a6d9-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="4a6d9-216">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-216">No</span></span> | <span data-ttu-id="4a6d9-217">Ya</span><span class="sxs-lookup"><span data-stu-id="4a6d9-217">Yes</span></span> | <span data-ttu-id="4a6d9-218">Aplikasi Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4a6d9-218">Finance and Operations apps</span></span> | <span data-ttu-id="4a6d9-219">Ya</span><span class="sxs-lookup"><span data-stu-id="4a6d9-219">Yes</span></span> | <span data-ttu-id="4a6d9-220">Ya, aplikasi Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4a6d9-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="4a6d9-221">**Aktual integrasi Project Operations (msdyn\_aktual)**</span><span class="sxs-lookup"><span data-stu-id="4a6d9-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="4a6d9-222">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-222">No</span></span> | <span data-ttu-id="4a6d9-223">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-223">No</span></span> | <span data-ttu-id="4a6d9-224">T\A</span><span class="sxs-lookup"><span data-stu-id="4a6d9-224">N\A</span></span> | <span data-ttu-id="4a6d9-225">Ya</span><span class="sxs-lookup"><span data-stu-id="4a6d9-225">Yes</span></span> | <span data-ttu-id="4a6d9-226">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-226">No</span></span> |
| <span data-ttu-id="4a6d9-227">**Baris kontrak projek (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="4a6d9-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="4a6d9-228">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-228">No</span></span> | <span data-ttu-id="4a6d9-229">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-229">No</span></span> | <span data-ttu-id="4a6d9-230">T\A</span><span class="sxs-lookup"><span data-stu-id="4a6d9-230">N\A</span></span> | <span data-ttu-id="4a6d9-231">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-231">No</span></span> | <span data-ttu-id="4a6d9-232">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-232">No</span></span> |
| <span data-ttu-id="4a6d9-233">**Entiti integrasi untuk hubungan transaksi projek (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="4a6d9-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="4a6d9-234">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-234">No</span></span> | <span data-ttu-id="4a6d9-235">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-235">No</span></span> | <span data-ttu-id="4a6d9-236">T\A</span><span class="sxs-lookup"><span data-stu-id="4a6d9-236">N\A</span></span> | <span data-ttu-id="4a6d9-237">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-237">No</span></span> | <span data-ttu-id="4a6d9-238">T\A</span><span class="sxs-lookup"><span data-stu-id="4a6d9-238">N\A</span></span> |
| <span data-ttu-id="4a6d9-239">**Pencapaian baris kontrak integrasi Operasi Projek (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="4a6d9-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="4a6d9-240">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-240">No</span></span> | <span data-ttu-id="4a6d9-241">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-241">No</span></span> | <span data-ttu-id="4a6d9-242">T\A</span><span class="sxs-lookup"><span data-stu-id="4a6d9-242">N\A</span></span> | <span data-ttu-id="4a6d9-243">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-243">No</span></span> | <span data-ttu-id="4a6d9-244">T\A</span><span class="sxs-lookup"><span data-stu-id="4a6d9-244">N\A</span></span> |
| <span data-ttu-id="4a6d9-245">**Entiti integrasi Operasi Projek untuk anggaran perbelanjaan (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="4a6d9-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="4a6d9-246">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-246">No</span></span> | <span data-ttu-id="4a6d9-247">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-247">No</span></span> | <span data-ttu-id="4a6d9-248">T\A</span><span class="sxs-lookup"><span data-stu-id="4a6d9-248">N\A</span></span> | <span data-ttu-id="4a6d9-249">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-249">No</span></span> | <span data-ttu-id="4a6d9-250">T\A</span><span class="sxs-lookup"><span data-stu-id="4a6d9-250">N\A</span></span> |
| <span data-ttu-id="4a6d9-251">**Kategori perbelanjaan projek integrasi Operasi Projek entiti eksport (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="4a6d9-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="4a6d9-252">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-252">No</span></span> | <span data-ttu-id="4a6d9-253">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-253">No</span></span> | <span data-ttu-id="4a6d9-254">T\A</span><span class="sxs-lookup"><span data-stu-id="4a6d9-254">N\A</span></span> | <span data-ttu-id="4a6d9-255">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-255">No</span></span> | <span data-ttu-id="4a6d9-256">T\A</span><span class="sxs-lookup"><span data-stu-id="4a6d9-256">N\A</span></span> |
| <span data-ttu-id="4a6d9-257">**Perbelanjaan projek integrasi Operasi Projek entiti eksport (msdyn\_perbelanjaan)**</span><span class="sxs-lookup"><span data-stu-id="4a6d9-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="4a6d9-258">Ya</span><span class="sxs-lookup"><span data-stu-id="4a6d9-258">Yes</span></span> | <span data-ttu-id="4a6d9-259">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-259">No</span></span> | <span data-ttu-id="4a6d9-260">T\A</span><span class="sxs-lookup"><span data-stu-id="4a6d9-260">N\A</span></span> | <span data-ttu-id="4a6d9-261">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-261">No</span></span> | <span data-ttu-id="4a6d9-262">T\A</span><span class="sxs-lookup"><span data-stu-id="4a6d9-262">N\A</span></span> |
| <span data-ttu-id="4a6d9-263">**Entiti integrasi Operasi Projek untuk anggaran jam (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="4a6d9-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="4a6d9-264">Ya</span><span class="sxs-lookup"><span data-stu-id="4a6d9-264">Yes</span></span> | <span data-ttu-id="4a6d9-265">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-265">No</span></span> | <span data-ttu-id="4a6d9-266">T\A</span><span class="sxs-lookup"><span data-stu-id="4a6d9-266">N\A</span></span> | <span data-ttu-id="4a6d9-267">Tidak</span><span class="sxs-lookup"><span data-stu-id="4a6d9-267">No</span></span> | <span data-ttu-id="4a6d9-268">T\A</span><span class="sxs-lookup"><span data-stu-id="4a6d9-268">N\A</span></span> |


4. <span data-ttu-id="4a6d9-269">Untuk menyegarkan semula entiti, pilih nama peta dan kemudian pilih **Segar semula entiti**.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Segar Semula Peta](./media/20RefreshMapping.png)

5. <span data-ttu-id="4a6d9-271">Selepas segar semula selesai, jalankan peta.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="4a6d9-272">Sebelum anda mendayakan peta seterusnya, sahkan bahawa peta dalam jadual dalam keadaan **Berjalan**.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="4a6d9-273">Jalankan peta dengan bilangan prasyarat yang lebih besar mungkin mengambil sedikit masa.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="4a6d9-274">Untuk menjalankan peta dengan prasyarat, dayakan togol **Tunjukkan peta entiti berkaitan**.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="4a6d9-275">Jika jadual menunjukkan **Penyegerakkan awal pra-syarat** **Tidak**, sahkan bahawa bendera **Penyegerakkan awal** **Dipadamkan** dalam semua peta pra-syarat sebelum anda menjalankannya.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Jalankan Peta](./media/21RunMap.png)

6. <span data-ttu-id="4a6d9-277">Mengesahkan semua peta berkaitan projek adalah dalam keadaan berjalan.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-277">Validate all project related maps are in the running state.</span></span>

![Semua Peta Berjalan](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="4a6d9-279">Gunakan data konfigurasi dalam CDS untuk Project Operations (pilihan)</span><span class="sxs-lookup"><span data-stu-id="4a6d9-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="4a6d9-280">Jika anda telah menggunakan data demo pada persekitaran Kewangan, lihat [sediakan dan gunakan data konfigurasi dalam Common Data Service untuk Project Operations](resource-apply-pro-setup-config-data.md) untuk menggunakan data demo pada persekitaran CDS.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="4a6d9-281">Persekitaran Operasi Projek anda kini diperuntukkan dan dikonfigurasikan.</span><span class="sxs-lookup"><span data-stu-id="4a6d9-281">Your Project Operations environment is now provisioned and configured.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]