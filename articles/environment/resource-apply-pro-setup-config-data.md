---
title: Sediakan dan gunakan data konfigurasi dalam Common Data Service untuk Operasi Projek
description: Topik ini memberikan maklumat tentang menyediakan dan menggunakan data konfigurasi dalam Operasi Projek.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d99ab4c7b2ebf6ba56b86a3e0151036c6247e484
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948990"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="796e7-103">Sediakan dan gunakan data konfigurasi dalam Common Data Service untuk Operasi Projek</span><span class="sxs-lookup"><span data-stu-id="796e7-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="796e7-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="796e7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="796e7-105">Memasang data persediaan dan konfigurasi</span><span class="sxs-lookup"><span data-stu-id="796e7-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="796e7-106">Muat turun, menyahsekat dan unzip [Pakej Data Persediaan dan Konfigurasi](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="796e7-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="796e7-107">Navigasi ke folder nyahzip dan jalankan fail boleh laku, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="796e7-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="796e7-108">Pada halaman 1 dalam Wizard Penghijrahan Konfigurasi (CMT) Common Data Service, pilih **Import Data** dan kemudian pilih **Teruskan**.</span><span class="sxs-lookup"><span data-stu-id="796e7-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrasi Konfigurasi](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="796e7-110">Pada halaman 2 dalam Wizard CMT, pilih **Office 365** sebagai **Jenis Pelaksanaan**.</span><span class="sxs-lookup"><span data-stu-id="796e7-110">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="796e7-111">Pilih **Paparkan senarai organisasi tersedia** dan kotak semak **Tunjukkan Lanjutan**.</span><span class="sxs-lookup"><span data-stu-id="796e7-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="796e7-112">Pilih rantau penyewa anda, masukkan kelayakan anda dan pilih **Log masuk**.</span><span class="sxs-lookup"><span data-stu-id="796e7-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Daftar Masuk Konfigurasi](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="796e7-114">Pada halaman 3, daripada senarai organisasi pada penyewa, pilih organisasi yang anda mahu import data demo ke dalam dan pilih **log masuk**.</span><span class="sxs-lookup"><span data-stu-id="796e7-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="796e7-115">Pada halaman 4, pilih fail zip, *SampleSetupAndConfigData* dari folder tak padat.</span><span class="sxs-lookup"><span data-stu-id="796e7-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Pilihan Fail Zip](./media/3ZipFile.png)

![Pilih fail](./media/4SelectAFile.png)

9. <span data-ttu-id="796e7-118">Selepas fail zip dipilih, pilih **Import Data**.</span><span class="sxs-lookup"><span data-stu-id="796e7-118">After the zip file is selected, select **Import Data**.</span></span>

![Import Data](./media/5ImportData.png)

10. <span data-ttu-id="796e7-120">Import akan berjalan selama kira-kira 2-10 minit bergantung pada kelajuan rangkaian anda.</span><span class="sxs-lookup"><span data-stu-id="796e7-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="796e7-121">Selepas import selesai, keluar dari CMT Wizard.</span><span class="sxs-lookup"><span data-stu-id="796e7-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="796e7-122">Semak organisasi anda untuk data dalam 19 entiti berikut:</span><span class="sxs-lookup"><span data-stu-id="796e7-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="796e7-123">Mata wang</span><span class="sxs-lookup"><span data-stu-id="796e7-123">Currency</span></span>
  - <span data-ttu-id="796e7-124">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="796e7-124">Organizational Unit</span></span>
  - <span data-ttu-id="796e7-125">Orang Hubungan</span><span class="sxs-lookup"><span data-stu-id="796e7-125">Contact</span></span>
  - <span data-ttu-id="796e7-126">Cukai Kumpulan</span><span class="sxs-lookup"><span data-stu-id="796e7-126">Tax Group</span></span>
  - <span data-ttu-id="796e7-127">Kumpulan Pelanggan</span><span class="sxs-lookup"><span data-stu-id="796e7-127">Customer Group</span></span>
  - <span data-ttu-id="796e7-128">Unit</span><span class="sxs-lookup"><span data-stu-id="796e7-128">Unit</span></span>
  - <span data-ttu-id="796e7-129">Kumpulan Unit</span><span class="sxs-lookup"><span data-stu-id="796e7-129">Unit Group</span></span>
  - <span data-ttu-id="796e7-130">Senarai Harga</span><span class="sxs-lookup"><span data-stu-id="796e7-130">Price List</span></span>
  - <span data-ttu-id="796e7-131">Senarai Harga Parameter Projek</span><span class="sxs-lookup"><span data-stu-id="796e7-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="796e7-132">Kekerapan Invois</span><span class="sxs-lookup"><span data-stu-id="796e7-132">Invoice Frequency</span></span>
  - <span data-ttu-id="796e7-133">Kategori Sumber Boleh Ditempah</span><span class="sxs-lookup"><span data-stu-id="796e7-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="796e7-134">Kategori Transaksi</span><span class="sxs-lookup"><span data-stu-id="796e7-134">Transaction Category</span></span>
  - <span data-ttu-id="796e7-135">Kategori Perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="796e7-135">Expense Category</span></span>
  - <span data-ttu-id="796e7-136">Harga Peranan</span><span class="sxs-lookup"><span data-stu-id="796e7-136">Role Price</span></span>
  - <span data-ttu-id="796e7-137">Harga Kategori Transaksi</span><span class="sxs-lookup"><span data-stu-id="796e7-137">Transaction Category Price</span></span>
  - <span data-ttu-id="796e7-138">Ciri</span><span class="sxs-lookup"><span data-stu-id="796e7-138">Characteristic</span></span>
  - <span data-ttu-id="796e7-139">Sumber Boleh Ditempah</span><span class="sxs-lookup"><span data-stu-id="796e7-139">Bookable Resource</span></span>
  - <span data-ttu-id="796e7-140">Penyekutuan kategori sumber boleh ditempah</span><span class="sxs-lookup"><span data-stu-id="796e7-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="796e7-141">Penyekutuan Cirian Sumber Boleh Ditempah</span><span class="sxs-lookup"><span data-stu-id="796e7-141">Bookable Resource Characteristic</span></span>

![Lengkapkan Import](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="796e7-143">Kemas kini konfigurasi Operasi Projek</span><span class="sxs-lookup"><span data-stu-id="796e7-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="796e7-144">Navigasi ke persekitaran CE.</span><span class="sxs-lookup"><span data-stu-id="796e7-144">Navigate to the CE environment.</span></span> <span data-ttu-id="796e7-145">Anda boleh menemuinya dengan membuka Pusat pentadbir [Power Platform](https://admin.powerplatform.microsoft.com/environments), memilih persekitaran dan kemudian memilih **Persekitaran Terbuka**.</span><span class="sxs-lookup"><span data-stu-id="796e7-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Persekitaran Terbuka](./media/7OpenEnvironment.png)

2. <span data-ttu-id="796e7-147">Pergi ke **Sumber** > **Projek** dan kemudian pilih **Baharu** untuk mencipta sumber boleh ditempah untuk pengguna anda.</span><span class="sxs-lookup"><span data-stu-id="796e7-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Sumber Boleh Ditempah](./media/8BookableResources.png)

3. <span data-ttu-id="796e7-149">Pada tab **Umum**, pilih pengguna pentadbir anda.</span><span class="sxs-lookup"><span data-stu-id="796e7-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="796e7-150">Sahkan bahawa zon waktu sepadan dengan yang anda berada.</span><span class="sxs-lookup"><span data-stu-id="796e7-150">Verify that the time zone matches the one you are in.</span></span> 

![Sumber Boleh Ditempah Baharu](./media/9NewBookableResource.png)

4. <span data-ttu-id="796e7-152">Pada tab **Penjadualan**, dalam medan **Syarikat**, pilih syarikat **USPM** dan kemudian pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="796e7-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Tab Penjadualan](./media/10SchedulingTab.png)

5. <span data-ttu-id="796e7-154">Pilih tab **Waktu kerja**.</span><span class="sxs-lookup"><span data-stu-id="796e7-154">Select the **Work hours** tab.</span></span>  

![Jam Kerja](./media/11WorkHours.png)

6. <span data-ttu-id="796e7-156">Klik dua kali pada mana-mana nilai dalam kalendar dan pilih **Edit** > **Semua acara dalam siri ini**.</span><span class="sxs-lookup"><span data-stu-id="796e7-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Kalendar Kerja](./media/12WorkCalendar.png)

7. <span data-ttu-id="796e7-158">Tukar masa kerja ke lapan (8) jam hari kerja, tandakan hujung minggu sebagai hari bukan kerja, dan pastikan zon waktu sepadan dengan anda.</span><span class="sxs-lookup"><span data-stu-id="796e7-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="796e7-159">Pilih **Simpan dan tutup**.</span><span class="sxs-lookup"><span data-stu-id="796e7-159">Select **Save and close**.</span></span>

![Kemas Kini Kalendar](./media/13UpdateCalendar.png)

9. <span data-ttu-id="796e7-161">Pergi ke **Tetapan** > **Templat kalendar** dan pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="796e7-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Templat Kalendar](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="796e7-163">Masukkan nama, pilih sumber templat yang anda cipta dan kemudian pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="796e7-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Simpan Templat Kalendar](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="796e7-165">Pergi ke **Parameter** dan klik dua kali pada rekod.</span><span class="sxs-lookup"><span data-stu-id="796e7-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parameter Projek](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="796e7-167">Kemas kini medan berikut:</span><span class="sxs-lookup"><span data-stu-id="796e7-167">Update the following fields:</span></span>

 - <span data-ttu-id="796e7-168">**Syarikat lalai**: USPM</span><span class="sxs-lookup"><span data-stu-id="796e7-168">**Default company**: USPM</span></span>
 - <span data-ttu-id="796e7-169">**Unit Organisasi Lalai** : Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="796e7-169">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="796e7-170">**Frekuensi Invois**: Ketujuh dan Hari Terakhir</span><span class="sxs-lookup"><span data-stu-id="796e7-170">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="796e7-171">**Templat jam kerja**: Tukar ke templat yang anda cipta.</span><span class="sxs-lookup"><span data-stu-id="796e7-171">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="796e7-172">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="796e7-172">Select **Save**.</span></span> 

![Parameter Projek Dikemas Kini](./media/17UpdatedProjectParameters.png)
