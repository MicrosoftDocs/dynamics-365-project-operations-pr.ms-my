---
title: Kemas kini Project Operations dalam persekitaran Kewangan anda
description: Topik ini menyediakan maklumat tentang cara untuk mengemas kini Project Operations dalam persekitaran Dynamics 365 Finance anda.
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d68296ec59f0bd58f848154c90e02c58f275ab12
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291990"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="23890-103">Kemas kini Project Operations dalam persekitaran Kewangan anda</span><span class="sxs-lookup"><span data-stu-id="23890-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="23890-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="23890-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="23890-105">Topik ini menyediakan maklumat tentang cara untuk mengemas kini Dynamics 365 Project Operations dalam persekitaran Dynamics 365 Finance anda.</span><span class="sxs-lookup"><span data-stu-id="23890-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="23890-106">Terdapat tiga prosedur yang diperlukan untuk mengemas kini Project Operations kepada Kemas Kini 5 (UR5):</span><span class="sxs-lookup"><span data-stu-id="23890-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="23890-107">Import pakej ke dalam projek pratonton anda</span><span class="sxs-lookup"><span data-stu-id="23890-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="23890-108">Gunakan kemas kini</span><span class="sxs-lookup"><span data-stu-id="23890-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="23890-109">Kemas kini persekitaran Dataverse anda</span><span class="sxs-lookup"><span data-stu-id="23890-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="23890-110">Import pakej ke dalam projek LCS anda</span><span class="sxs-lookup"><span data-stu-id="23890-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="23890-111">Daftar masuk ke dalam [Lifecycle Services (LCS)](https://lcs.dynamics.com/) sebagai Pemilik Projek atau pengurus Persekitaran.</span><span class="sxs-lookup"><span data-stu-id="23890-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="23890-112">Daripada senarai projek, pilih projek LCS anda.</span><span class="sxs-lookup"><span data-stu-id="23890-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="23890-113">Pada halaman **Projek**, dalam kumpulan **Persekitaran**, buka persekitaran yang anda mahu kemas kini.</span><span class="sxs-lookup"><span data-stu-id="23890-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="23890-114">Sahkan bahawa persekitaran sedang berjalan.</span><span class="sxs-lookup"><span data-stu-id="23890-114">Verify that the environment is running.</span></span> <span data-ttu-id="23890-115">Jika ini tidak bermula, mulakan persekitaran.</span><span class="sxs-lookup"><span data-stu-id="23890-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="23890-116">Dalam bahagian **Keluaran baharu** di bawah **Kemas kini tersedia**, pilih **Lihat kemas kini** untuk 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="23890-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Lihat butang kemas kini](media/view-update.png)

6. <span data-ttu-id="23890-118">Pada halaman **Kemas kini binari**, pilih **Simpan pakej**.</span><span class="sxs-lookup"><span data-stu-id="23890-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="23890-119">Pada halaman **Semak dan simpan kemas kini**, pilih **Simpan pakej**.</span><span class="sxs-lookup"><span data-stu-id="23890-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="23890-120">Pada anak tetingkap **Simpan pakej pada pustaka eset** yang terbuka, masukkan nama pakej dan kemudian pilih **Simpan pakej**.</span><span class="sxs-lookup"><span data-stu-id="23890-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="23890-121">Apabila LCS selesai menyimpan pakej, butang **Selesai** didayakan.</span><span class="sxs-lookup"><span data-stu-id="23890-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="23890-122">Pilih **Selesai**.</span><span class="sxs-lookup"><span data-stu-id="23890-122">Select **Done**.</span></span> <span data-ttu-id="23890-123">LCS akan mengesahkan pakej.</span><span class="sxs-lookup"><span data-stu-id="23890-123">LCS will verify the package.</span></span> <span data-ttu-id="23890-124">Pengesahan mengambil masa beberapa minit atau sehingga satu jam.</span><span class="sxs-lookup"><span data-stu-id="23890-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="23890-125">Gunakan kemas kini pakej</span><span class="sxs-lookup"><span data-stu-id="23890-125">Apply the package update</span></span>

1. <span data-ttu-id="23890-126">Dalam LCS, pada halaman **Butiran persekitaran**, pilih **Selenggara** > **Gunakan Kemas Kini**.</span><span class="sxs-lookup"><span data-stu-id="23890-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="23890-127">Daripada senarai, pilih pakej yang anda simpan lebih awal, kemudian pilih **Gunakan**.</span><span class="sxs-lookup"><span data-stu-id="23890-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="23890-128">Pilih **Ya** untuk mengesahkan yang anda mahu menggunakan pakej.</span><span class="sxs-lookup"><span data-stu-id="23890-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Sahkan kota dialog pelaksanaan pakej](media/confirm-package-deployment.png)

4. <span data-ttu-id="23890-130">Pilih **Ya** untuk mengesahkan yang anda mahu mengemas kini aplikasi.</span><span class="sxs-lookup"><span data-stu-id="23890-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Sahkan kotak dialog kemas kini aplikasi](media/confirm-application-update.png)

<span data-ttu-id="23890-132">Kemas kini pelaksanaan dan aplikasi akan bermula.</span><span class="sxs-lookup"><span data-stu-id="23890-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="23890-133">Pada halaman **Butiran persekitaran**, di penjuru kanan sebelah atas, status persekitaran akan mengemas kini kepada **Penservisan**.</span><span class="sxs-lookup"><span data-stu-id="23890-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="23890-134">Dalam kira-kira dua jam, kemas kini akan selesai.</span><span class="sxs-lookup"><span data-stu-id="23890-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="23890-135">Maklumat keluaran aplikasi akan dikemas kini kepada **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** dan status persekitaran akan dikemas kini kepada **Dilaksanakan**.</span><span class="sxs-lookup"><span data-stu-id="23890-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="23890-136">Kemas kini persekitaran Dataverse anda</span><span class="sxs-lookup"><span data-stu-id="23890-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="23890-137">Daftar masuk ke [pusat pentadbiran Power Platform](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="23890-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="23890-138">Dalam senarai, cari dan buka persekitaran yang anda gunakan untuk memasang Project Operations.</span><span class="sxs-lookup"><span data-stu-id="23890-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="23890-139">Pada halaman **Persekitaran**, pilih **Sumber** > **aplikasi Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="23890-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="23890-140">Dalam senarai, cari **Microsoft Dynamics 365 Project Operations**, dan dalam lajur **Status**, pilih **Kemas Kini Tersedia**.</span><span class="sxs-lookup"><span data-stu-id="23890-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="23890-141">Pilih kotak semak **Saya bersetuju dengan syarat perkhidmatan**, kemudian pilih **Kemas kini**.</span><span class="sxs-lookup"><span data-stu-id="23890-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="23890-142">Versi penyelesaian yang terkini akan dipasang.</span><span class="sxs-lookup"><span data-stu-id="23890-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="23890-143">Selepas pemasangan selesai, versi 4.5.0.134 anda akan dipasang.</span><span class="sxs-lookup"><span data-stu-id="23890-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="23890-144">Konfigurasikan ciri baharu</span><span class="sxs-lookup"><span data-stu-id="23890-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="23890-145">Dayakan pemetaan dwitulis</span><span class="sxs-lookup"><span data-stu-id="23890-145">Enable dual-write mapping</span></span>

<span data-ttu-id="23890-146">Selepas anda melengkapkan kemas kini pada persekitaran Kewangan dan Dataverse, anda boleh mendayakan pemetaan dwitulis yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="23890-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="23890-147">Selesaikan prosedur berikut untuk mendayakan pemetaan dwitulis.</span><span class="sxs-lookup"><span data-stu-id="23890-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="23890-148">Kemas kini tetapan keselamatan pada persekitaran Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="23890-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="23890-149">Segar semula entiti data</span><span class="sxs-lookup"><span data-stu-id="23890-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="23890-150">Kemas kini dan jalankan pemetaan dwitulis</span><span class="sxs-lookup"><span data-stu-id="23890-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="23890-151">Kemas kini tetapan keselamatan pada persekitaran Dataverse</span><span class="sxs-lookup"><span data-stu-id="23890-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="23890-152">Kemas kini berikut pada kelayakan keselamatan untuk entiti diperlukan sebagai sebahagian daripada kemas kini kepada UR5.</span><span class="sxs-lookup"><span data-stu-id="23890-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="23890-153">Dalam persekitaran Dataverse anda, pergi ke **Tetapan**, dan dalam kumpulan **Sistem**, pilih **Keselamatan**.</span><span class="sxs-lookup"><span data-stu-id="23890-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Tetapan persekitaran Dataverse](media/Picture21.png)

2. <span data-ttu-id="23890-155">Pilih **Peranan Keselamatan**.</span><span class="sxs-lookup"><span data-stu-id="23890-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="23890-156">Daripada senarai peranan, pilih **pengguna aplikasi dwitulis** dan pilih tab **Entiti Tersuai**.</span><span class="sxs-lookup"><span data-stu-id="23890-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="23890-157">Sahkan bahawa peranan mempunyai keizinan **Baca** dan **Tambah Pada** untuk:</span><span class="sxs-lookup"><span data-stu-id="23890-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="23890-158">**Jenis Kadar Tukaran Mata Wang**</span><span class="sxs-lookup"><span data-stu-id="23890-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="23890-159">**Carta Akaun**</span><span class="sxs-lookup"><span data-stu-id="23890-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="23890-160">**Kalendar Fiskal**</span><span class="sxs-lookup"><span data-stu-id="23890-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="23890-161">**Lejar**</span><span class="sxs-lookup"><span data-stu-id="23890-161">**Ledger**</span></span>

5. <span data-ttu-id="23890-162">Selepas peranan keselamatan dikemas kini, pergi ke **Tetapan** > **Keselamatan** > **Pasukan**.</span><span class="sxs-lookup"><span data-stu-id="23890-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="23890-163">Sahkan bahawa peranan **pengguna aplikasi dwitulis** telah digunakan kepada pasukan.</span><span class="sxs-lookup"><span data-stu-id="23890-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="23890-164">Segar semula entiti data daripada kemas kini</span><span class="sxs-lookup"><span data-stu-id="23890-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="23890-165">Dalam persekitaran Kewangan anda, buka ruang kerja **Pengurusan data**, kemudian buka halaman **Parameter rangka kerja**.</span><span class="sxs-lookup"><span data-stu-id="23890-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="23890-166">Pada tab **Tetapan entiti**, pilih **Segar semula senarai entiti**.</span><span class="sxs-lookup"><span data-stu-id="23890-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="23890-167">Pilih **Tutup** untuk mengesahkan segar semula entiti.</span><span class="sxs-lookup"><span data-stu-id="23890-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="23890-168">Proses ini akan mengambil masa lebih kurang 20 minit untuk dilengkapkan.</span><span class="sxs-lookup"><span data-stu-id="23890-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="23890-169">Anda akan dimaklumkan apabila segar semula selesai.</span><span class="sxs-lookup"><span data-stu-id="23890-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="23890-170">Kemas kini pemetaan dwitulis</span><span class="sxs-lookup"><span data-stu-id="23890-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="23890-171">Dalam ruang kerja **Pengurusan data**, pilih **Dwitulis**.</span><span class="sxs-lookup"><span data-stu-id="23890-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="23890-172">Pilih **Gunakan penyelesaian**, pilih kedua-dua penyelesaian dalam senarai, kemudian pilih **Gunakan**.</span><span class="sxs-lookup"><span data-stu-id="23890-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="23890-173">Pada halaman **Dwitulis**, pilih peta jadual berikut, kemudian pilih **Hentikan**.</span><span class="sxs-lookup"><span data-stu-id="23890-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="23890-174">**Aktual integrasi Project Operations (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="23890-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="23890-175">**Kategori perbelanjaan projek integrasi Project Operations (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="23890-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="23890-176">**Entiti eksport perbelanjaan projek aktual integrasi Project Operations (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="23890-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="23890-177">Halaman **Versi peta jadual**, gunakan versi peta baharu pada setiap tiga entiti.</span><span class="sxs-lookup"><span data-stu-id="23890-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="23890-178">Pada halaman **Dwitulis**, pilih jalankan untuk mulakan semula peta.</span><span class="sxs-lookup"><span data-stu-id="23890-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="23890-179">Dari senarai peta, pilih peta **Ledger (msdyn_ledgers)** yang mempunyai semua prasyarat dan pilih kotak semak **Segerak awal**.</span><span class="sxs-lookup"><span data-stu-id="23890-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="23890-180">Dalam medan **Induk untuk segerak awal**, pilih aplikasi **Finance and Operations** dan kemudian pilih **Jalankan**.</span><span class="sxs-lookup"><span data-stu-id="23890-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Penyegerakan peta lejar](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]