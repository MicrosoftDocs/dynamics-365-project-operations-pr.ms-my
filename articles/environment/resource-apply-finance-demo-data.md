---
title: Gunakan data demo pada persekitaran berhos Awan Kewangan
description: Topik ini menerangkan cara menggunakan data demo daripada Operasi Projek kepada Dynamics 365 Finance persekitaran berhos Awan.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a7cdbd2847ce45972aadd0d1a2d4f26270727ad9
ms.sourcegitcommit: d33ef0ae39f90fe3b0f6b4524f483e8052057361
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/03/2020
ms.locfileid: "4365249"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="959d0-103">Gunakan data demo pada persekitaran berhos Awan Kewangan</span><span class="sxs-lookup"><span data-stu-id="959d0-103">Apply demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="959d0-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="959d0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="959d0-105">Topik ini hanya diguna pakai bagi Microsoft Dynamics 365 Finance versi 10.0.13 dan hanya boleh dilakukan pada persekitaran berhos Awan.</span><span class="sxs-lookup"><span data-stu-id="959d0-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="959d0-106">Lengkapkan langkah dalam topik ini **SEBELUM** anda menggunakan kemas kini kualiti kepada persekitaran.</span><span class="sxs-lookup"><span data-stu-id="959d0-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="959d0-107">Dalam projek LCS anda, buka halaman **Butiran persekitaran**.</span><span class="sxs-lookup"><span data-stu-id="959d0-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="959d0-108">Perhatikan bahawa ia termasuk butiran yang diperlukan untuk menyambung ke persekitaran dengan menggunakan Protokol Desktop Jarak Jauh (RDP).</span><span class="sxs-lookup"><span data-stu-id="959d0-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![Butiran Persekitaran](./media/1EnvironmentDetails.png)

<span data-ttu-id="959d0-110">Set kelayakan pertama yang diserlahkan ialah kelayakan akaun tempatan dan mengandungi hiperpautan ke sambungan desktop jarak jauh.</span><span class="sxs-lookup"><span data-stu-id="959d0-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="959d0-111">Kelayakan termasuk nama pengguna pentadbir persekitaran dan kata laluan.</span><span class="sxs-lookup"><span data-stu-id="959d0-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="959d0-112">Set kedua kelayakan digunakan untuk log masuk ke Pelayan SQL dalam persekitaran ini.</span><span class="sxs-lookup"><span data-stu-id="959d0-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="959d0-113">Sambung kepada persekitaran oleh hiperpautan dalam **Akaun Tempatan** dan gunakan **Kelayakan Akaun Tempatan** untuk pengesahan.</span><span class="sxs-lookup"><span data-stu-id="959d0-113">Remote to the environment by the hyperlink in **Local Accounts**, and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="959d0-114">Pergi ke **Perkhidmatan Maklumat Internet** > **Himpunan Aplikasi** > **PerkhidmatanAOS** dan menghentikan perkhidmatan.</span><span class="sxs-lookup"><span data-stu-id="959d0-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="959d0-115">Anda akan menghentikan perkhidmatan pada masa ini supaya anda boleh terus menggantikan pangkalan data SQL.</span><span class="sxs-lookup"><span data-stu-id="959d0-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![Hentikan AOS](./media/2StopAOS.png)

4. <span data-ttu-id="959d0-117">Pergi ke **Perkhidmatan** dan hentikan dua item berikut:</span><span class="sxs-lookup"><span data-stu-id="959d0-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="959d0-118">Microsoft Dynamics 365 Unified Operations: Perkhidmatan Pengurusan Kelompok</span><span class="sxs-lookup"><span data-stu-id="959d0-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="959d0-119">Microsoft Dynamics 365 Unified Operations : Rangka Kerja Eksport Import Data</span><span class="sxs-lookup"><span data-stu-id="959d0-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Menghentikan Perkhidmatan](./media/3StopServices.png)

5. <span data-ttu-id="959d0-121">Buka Studio Pengurusan Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="959d0-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="959d0-122">Log masuk dengan kelayakan pelayan SQL dan gunakan pengguna axdbadmin dan kata laluan daripada halaman **Butiran persekitaran** LCS.</span><span class="sxs-lookup"><span data-stu-id="959d0-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="959d0-124">Dalam Explorer Objek, **Pangkalan Data** dan cari **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="959d0-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="959d0-125">Anda akan menggantikan pangkalan data dengan pangkalan data baru yang terletak di [Pusat Muat turun](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span><span class="sxs-lookup"><span data-stu-id="959d0-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="959d0-126">Salin fail zip ke VM yang anda akan diasingkan dan ekstrak kandungan zip.</span><span class="sxs-lookup"><span data-stu-id="959d0-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="959d0-127">Dalam Studio Pengurusan Pelayan SQL, klik kanan **AxDB**, dan kemudian pilih **Tugas** > **Pulihkan** > **Pangkalan Data**.</span><span class="sxs-lookup"><span data-stu-id="959d0-127">In SQL Server Management Studio, right-click **AxDB**, and then select **Tasks** > **Restore** > **Database**.</span></span>

![Pulihkan Pangkalan Data](./media/5RestoreDatabase.png)

9. <span data-ttu-id="959d0-129">Pilih **Peranti Sumber** dan navigasi ke fail yang diekstrak dari zip yang disalin.</span><span class="sxs-lookup"><span data-stu-id="959d0-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Peranti sumber](./media/6SourceDevice.png)

10. <span data-ttu-id="959d0-131">Pilih **Pilihan** dan kemudian pilih **Tulis Ganti pangkalan data sedia ada** dan **Tutup sambungan sedia ada ke pangkalan data destinasi**.</span><span class="sxs-lookup"><span data-stu-id="959d0-131">Select **Options**, and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="959d0-132">Pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="959d0-132">Select **OK**.</span></span>

![Pulihkan Tetapan](./media/7RestoreSetting.png)

<span data-ttu-id="959d0-134">Anda akan menerima pengesahan bahawa pemulihan AXDB telah berjaya.</span><span class="sxs-lookup"><span data-stu-id="959d0-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="959d0-135">Selepas anda menerima pengesahan ini, anda boleh menutup Studio Pengurusan Perkhidmatan SQL.</span><span class="sxs-lookup"><span data-stu-id="959d0-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="959d0-136">Pergi ke **Perkhidmatan Maklumat Internet** > **Himpunan Aplikasi** > **PerkhidmatanAOS** dan memulakan PerkhidmatanAOS.</span><span class="sxs-lookup"><span data-stu-id="959d0-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="959d0-137">Pergi ke **Perkhidmatan** dan memulakan dua perkhidmatan yang anda telah berhenti lebih awal.</span><span class="sxs-lookup"><span data-stu-id="959d0-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="959d0-138">Mencari alat AdminUserProvisioning pada VM ini.</span><span class="sxs-lookup"><span data-stu-id="959d0-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="959d0-139">Lihat di bawah, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span><span class="sxs-lookup"><span data-stu-id="959d0-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="959d0-140">Jalankan fail .ext menggunakan alamat pengguna anda dalam medan **Alamat E-mel**.</span><span class="sxs-lookup"><span data-stu-id="959d0-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="959d0-141">Pilih **Serahkan**.</span><span class="sxs-lookup"><span data-stu-id="959d0-141">Select **Submit**.</span></span>

![Peruntukan Pengguna Pentadbir](./media/8AdminUserProvisioning.png)

<span data-ttu-id="959d0-143">Ini mengambil masa beberapa minit untuk dilengkapkan.</span><span class="sxs-lookup"><span data-stu-id="959d0-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="959d0-144">Anda akan menerima mesej pengesahan yang pengguna Pentadbir telah berjaya dikemas kini.</span><span class="sxs-lookup"><span data-stu-id="959d0-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="959d0-145">Akhir sekali, jalankan Prom Arahan sebagai Pentadbir dan lakukan iisset semula</span><span class="sxs-lookup"><span data-stu-id="959d0-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![Set semula IIS](./media/9IISReset.png)

18. <span data-ttu-id="959d0-147">Tutup sesi desktop jarak jauh dan gunakan halaman **butiran persekitaran LCS** untuk log masuk ke persekitaran bagi mengesahkannya, ia berfungsi seperti yang dijangkakan.</span><span class="sxs-lookup"><span data-stu-id="959d0-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)
