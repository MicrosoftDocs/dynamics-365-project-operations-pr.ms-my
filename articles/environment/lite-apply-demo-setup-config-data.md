---
title: Gunakan persediaan tunjuk cara dan data konfigurasi - lite
description: Topik ini memberikan maklumat tentang cara menggunakan persediaan demo dan data konfigurasi untuk Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5cfc270c07a568d692f6cd180b9c367ae185044c
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401274"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="1e693-103">Gunakan persediaan tunjuk cara dan data konfigurasi dalam untuk Project Operations - lite</span><span class="sxs-lookup"><span data-stu-id="1e693-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="1e693-104">_\*\*Pelaksanaan lite - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="1e693-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1e693-105">Prasyarat</span><span class="sxs-lookup"><span data-stu-id="1e693-105">Prerequisites</span></span>

<span data-ttu-id="1e693-106">Sebelum anda mulakan konfigurasi, anda mesti mempunyai persekitaran Common Data Service (CDS) yang diperuntukkan untuk Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="1e693-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="1e693-107">Arahan</span><span class="sxs-lookup"><span data-stu-id="1e693-107">Instructions</span></span>

1. <span data-ttu-id="1e693-108">Muat turun [Pakej Data Induk](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="1e693-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="1e693-109">Navigasi kepada folder *ProjOpsDemoDataSetupAndMaster - CMT Disepadukan* dan jalankan fail yang boleh dilaksanakan, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="1e693-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="1e693-110">Pada halaman 1 dalam Wizard Penghijrahan Konfigurasi (CMT) Common Data Service, pilih **Import Data** dan kemudian pilih **Teruskan**.</span><span class="sxs-lookup"><span data-stu-id="1e693-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrasi Konfigurasi](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="1e693-112">Pada Halaman 2 dalam Wizard CMT, pilih **Microsoft 365** sebagai **Jenis Perlaksanaan**.</span><span class="sxs-lookup"><span data-stu-id="1e693-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="1e693-113">Pilih **Paparkan senarai organisasi tersedia** dan kotak semak **Tunjukkan Lanjutan**.</span><span class="sxs-lookup"><span data-stu-id="1e693-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="1e693-114">Pilih rantau penyewa anda, masukkan kelayakan anda dan kemudian pilih **Log masuk**.</span><span class="sxs-lookup"><span data-stu-id="1e693-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Daftar Masuk Konfigurasi](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="1e693-116">Pada halaman 3, daripada senarai Organisasi pada Penyewa, pilih organisasi yang anda mahu import data demo dan pilih **Log masuk**.</span><span class="sxs-lookup"><span data-stu-id="1e693-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="1e693-117">Pada halaman 4, pilih fail zip, *MasterAndSetupData* daripada folder yang dibuka, *ProjOpsDemoDataSetupAndMaster - CMT Disepadukan*.</span><span class="sxs-lookup"><span data-stu-id="1e693-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Fail Zip](./media/3ZipFile.png)

![Pilih fail](./media/4SelectAFile.png)

9. <span data-ttu-id="1e693-120">Selepas fail zip dipilih, pilih **Import Data**.</span><span class="sxs-lookup"><span data-stu-id="1e693-120">After the zip file is selected, select **Import Data**.</span></span>

![Import data](./media/5ImportData.png)

10. <span data-ttu-id="1e693-122">Import akan berjalan selama kira-kira 2-10 minit bergantung pada kelajuan rangkaian anda.</span><span class="sxs-lookup"><span data-stu-id="1e693-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="1e693-123">Selepas import selesai, keluar dari Wizard CMT.</span><span class="sxs-lookup"><span data-stu-id="1e693-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="1e693-124">Semak organisasi anda untuk data dalam 20 entiti berikut:</span><span class="sxs-lookup"><span data-stu-id="1e693-124">Check your organization for data in the following 20 entities:</span></span>

-   <span data-ttu-id="1e693-125">Mata wang</span><span class="sxs-lookup"><span data-stu-id="1e693-125">Currency</span></span>
-   <span data-ttu-id="1e693-126">Akaun</span><span class="sxs-lookup"><span data-stu-id="1e693-126">Account</span></span>
-   <span data-ttu-id="1e693-127">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="1e693-127">Organizational Unit</span></span>
-   <span data-ttu-id="1e693-128">Orang Hubungan</span><span class="sxs-lookup"><span data-stu-id="1e693-128">Contact</span></span>
-   <span data-ttu-id="1e693-129">Cukai Kumpulan</span><span class="sxs-lookup"><span data-stu-id="1e693-129">Tax Group</span></span>
-   <span data-ttu-id="1e693-130">Kumpulan Pelanggan</span><span class="sxs-lookup"><span data-stu-id="1e693-130">Customer Group</span></span>
-   <span data-ttu-id="1e693-131">Unit</span><span class="sxs-lookup"><span data-stu-id="1e693-131">Unit</span></span>
-   <span data-ttu-id="1e693-132">Kumpulan Unit</span><span class="sxs-lookup"><span data-stu-id="1e693-132">Unit Group</span></span>
-   <span data-ttu-id="1e693-133">Senarai Harga</span><span class="sxs-lookup"><span data-stu-id="1e693-133">Price List</span></span>
-   <span data-ttu-id="1e693-134">Senarai Harga Parameter Projek</span><span class="sxs-lookup"><span data-stu-id="1e693-134">Project Parameter Price List</span></span> 
-   <span data-ttu-id="1e693-135">Kekerapan Invois</span><span class="sxs-lookup"><span data-stu-id="1e693-135">Invoice Frequency</span></span>
-   <span data-ttu-id="1e693-136">Kategori Sumber Boleh Ditempah</span><span class="sxs-lookup"><span data-stu-id="1e693-136">Bookable Resource Category</span></span>
-   <span data-ttu-id="1e693-137">Kategori Transaksi</span><span class="sxs-lookup"><span data-stu-id="1e693-137">Transaction Category</span></span>
-   <span data-ttu-id="1e693-138">Kategori Perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="1e693-138">Expense Category</span></span>
-   <span data-ttu-id="1e693-139">Harga Peranan</span><span class="sxs-lookup"><span data-stu-id="1e693-139">Role Price</span></span>
-   <span data-ttu-id="1e693-140">Harga Kategori Transaksi</span><span class="sxs-lookup"><span data-stu-id="1e693-140">Transaction Category Price</span></span>
-   <span data-ttu-id="1e693-141">Ciri</span><span class="sxs-lookup"><span data-stu-id="1e693-141">Characteristic</span></span>
-   <span data-ttu-id="1e693-142">Sumber Boleh Ditempah</span><span class="sxs-lookup"><span data-stu-id="1e693-142">Bookable Resource</span></span>
-   <span data-ttu-id="1e693-143">Penyekutuan kategori sumber boleh ditempah</span><span class="sxs-lookup"><span data-stu-id="1e693-143">Bookable resource category Assn</span></span>
-   <span data-ttu-id="1e693-144">Penyekutuan Cirian Sumber Boleh Ditempah</span><span class="sxs-lookup"><span data-stu-id="1e693-144">Bookable Resource Characteristic</span></span>

![Lengkapkan Import](./media/6CompleteImport.png)
