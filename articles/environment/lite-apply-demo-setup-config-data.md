---
title: Gunakan tetapan demo dan data konfigurasi
description: Topik ini memberikan maklumat tentang cara menggunakan persediaan demo dan data konfigurasi untuk Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948987"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="1a174-103">Gunakan persediaan demo dan data konfigurasi untuk pelaksanaan lite Project Operations - urusan untuk penginvoisan proforma</span><span class="sxs-lookup"><span data-stu-id="1a174-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="1a174-104">_\*\*Pelaksanaan lite - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="1a174-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="1a174-105">Muat turun [Pakej Data Induk](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="1a174-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="1a174-106">Navigasi kepada folder *ProjOpsDemoDataSetupAndMaster - CMT Disepadukan* dan jalankan fail yang boleh dilaksanakan, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="1a174-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="1a174-107">Pada halaman 1 dalam Wizard Penghijrahan Konfigurasi (CMT) Common Data Service, pilih **Import Data** dan kemudian pilih **Teruskan**.</span><span class="sxs-lookup"><span data-stu-id="1a174-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrasi Konfigurasi](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="1a174-109">Pada halaman 2 dalam Wizard CMT, pilih **Office 365** sebagai **Jenis Pelaksanaan**.</span><span class="sxs-lookup"><span data-stu-id="1a174-109">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="1a174-110">Pilih **Paparkan senarai organisasi tersedia** dan kotak semak **Tunjukkan Lanjutan**.</span><span class="sxs-lookup"><span data-stu-id="1a174-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="1a174-111">Pilih rantau penyewa anda, masukkan kelayakan anda dan kemudian pilih **Log masuk**.</span><span class="sxs-lookup"><span data-stu-id="1a174-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Daftar Masuk Konfigurasi](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="1a174-113">Pada halaman 3, daripada senarai Organisasi pada Penyewa, pilih organisasi yang anda mahu import data demo dan pilih **Log masuk**.</span><span class="sxs-lookup"><span data-stu-id="1a174-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="1a174-114">Pada halaman 4, pilih fail zip, *MasterAndSetupData* daripada folder yang dibuka, *ProjOpsDemoDataSetupAndMaster - CMT Disepadukan*.</span><span class="sxs-lookup"><span data-stu-id="1a174-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Fail Zip](./media/3ZipFile.png)

![Pilih fail](./media/4SelectAFile.png)

9. <span data-ttu-id="1a174-117">Selepas fail zip dipilih, pilih **Import Data**.</span><span class="sxs-lookup"><span data-stu-id="1a174-117">After the zip file is selected, select **Import Data**.</span></span>

![Import data](./media/5ImportData.png)

10. <span data-ttu-id="1a174-119">Import akan berjalan selama kira-kira 2-10 minit bergantung pada kelajuan rangkaian anda.</span><span class="sxs-lookup"><span data-stu-id="1a174-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="1a174-120">Selepas import selesai, keluar dari Wizard CMT.</span><span class="sxs-lookup"><span data-stu-id="1a174-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="1a174-121">Semak organisasi anda untuk data dalam 20 entiti berikut:</span><span class="sxs-lookup"><span data-stu-id="1a174-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="1a174-122">Mata wang</span><span class="sxs-lookup"><span data-stu-id="1a174-122">Currency</span></span>
- <span data-ttu-id="1a174-123">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="1a174-123">Organizational Unit</span></span>
- <span data-ttu-id="1a174-124">Orang Hubungan</span><span class="sxs-lookup"><span data-stu-id="1a174-124">Contact</span></span>
- <span data-ttu-id="1a174-125">Cukai Kumpulan</span><span class="sxs-lookup"><span data-stu-id="1a174-125">Tax Group</span></span>
- <span data-ttu-id="1a174-126">Kumpulan Pelanggan</span><span class="sxs-lookup"><span data-stu-id="1a174-126">Customer Group</span></span>
- <span data-ttu-id="1a174-127">Unit</span><span class="sxs-lookup"><span data-stu-id="1a174-127">Unit</span></span>
- <span data-ttu-id="1a174-128">Kumpulan Unit</span><span class="sxs-lookup"><span data-stu-id="1a174-128">Unit Group</span></span>
- <span data-ttu-id="1a174-129">Senarai Harga</span><span class="sxs-lookup"><span data-stu-id="1a174-129">Price List</span></span>
- <span data-ttu-id="1a174-130">Senarai Harga Parameter Projek</span><span class="sxs-lookup"><span data-stu-id="1a174-130">Project Parameter Price List</span></span>
- <span data-ttu-id="1a174-131">Kekerapan Invois</span><span class="sxs-lookup"><span data-stu-id="1a174-131">Invoice Frequency</span></span>
- <span data-ttu-id="1a174-132">Butiran Kekerapan Invois</span><span class="sxs-lookup"><span data-stu-id="1a174-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="1a174-133">Kategori Sumber Boleh Ditempah</span><span class="sxs-lookup"><span data-stu-id="1a174-133">Bookable Resource Category</span></span>
- <span data-ttu-id="1a174-134">Kategori Transaksi</span><span class="sxs-lookup"><span data-stu-id="1a174-134">Transaction Category</span></span>
- <span data-ttu-id="1a174-135">Kategori Perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="1a174-135">Expense Category</span></span>
- <span data-ttu-id="1a174-136">Harga Peranan</span><span class="sxs-lookup"><span data-stu-id="1a174-136">Role Price</span></span>
- <span data-ttu-id="1a174-137">Harga Kategori Transaksi</span><span class="sxs-lookup"><span data-stu-id="1a174-137">Transaction Category Price</span></span>
- <span data-ttu-id="1a174-138">Ciri</span><span class="sxs-lookup"><span data-stu-id="1a174-138">Characteristic</span></span>
- <span data-ttu-id="1a174-139">Sumber Boleh Ditempah</span><span class="sxs-lookup"><span data-stu-id="1a174-139">Bookable Resource</span></span>
- <span data-ttu-id="1a174-140">Penyekutuan kategori sumber boleh ditempah</span><span class="sxs-lookup"><span data-stu-id="1a174-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="1a174-141">Penyekutuan Cirian Sumber Boleh Ditempah</span><span class="sxs-lookup"><span data-stu-id="1a174-141">Bookable Resource Characteristic</span></span>

![Lengkapkan Import](./media/6CompleteImport.png)
