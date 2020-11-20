---
title: Sediakan dan gunakan data konfigurasi dalam Common Data Service
description: Topik ini memberikan maklumat tentang menyediakan dan menggunakan data konfigurasi dalam Operasi Projek.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7de8db5e91265c77c79f34a513bf27d9a55b789a
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401139"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="5fec3-103">Sediakan dan gunakan data konfigurasi dalam Common Data Service</span><span class="sxs-lookup"><span data-stu-id="5fec3-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="5fec3-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="5fec3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5fec3-105">Prasyarat</span><span class="sxs-lookup"><span data-stu-id="5fec3-105">Prerequisites</span></span>

<span data-ttu-id="5fec3-106">Sebelum anda mula mengkonfigurasikan data dalam Common Data Service (CDS), prasyarat berikut mesti dipenuhi:</span><span class="sxs-lookup"><span data-stu-id="5fec3-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="5fec3-107">Peruntukan persekitaran CDS dan persekitaran Dynamics 365 Finance untuk Project Operations.</span><span class="sxs-lookup"><span data-stu-id="5fec3-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="5fec3-108">Maklumat entiti sah daripada Dynamics 365 Finance dikongsi pada persekitaran CDS.</span><span class="sxs-lookup"><span data-stu-id="5fec3-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="5fec3-109">Ini bermaksud bahawa entiti **Syarikat** dalam CDS mempunyai rekod syarikat berikut:</span><span class="sxs-lookup"><span data-stu-id="5fec3-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="5fec3-110">THPM</span><span class="sxs-lookup"><span data-stu-id="5fec3-110">THPM</span></span>
  - <span data-ttu-id="5fec3-111">USPM</span><span class="sxs-lookup"><span data-stu-id="5fec3-111">USPM</span></span>
  - <span data-ttu-id="5fec3-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="5fec3-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="5fec3-113">Memasang data persediaan dan konfigurasi</span><span class="sxs-lookup"><span data-stu-id="5fec3-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="5fec3-114">Muat turun, menyahsekat dan unzip [Pakej Data Persediaan dan Konfigurasi](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="5fec3-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="5fec3-115">Navigasi ke folder nyahzip dan jalankan fail boleh laku, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="5fec3-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="5fec3-116">Pada halaman 1 dalam Wizard Penghijrahan Konfigurasi (CMT) Common Data Service, pilih **Import Data** dan kemudian pilih **Teruskan**.</span><span class="sxs-lookup"><span data-stu-id="5fec3-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrasi Konfigurasi](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="5fec3-118">Pada Halaman 2 dalam Wizard CMT, pilih **Microsoft 365** sebagai **Jenis Perlaksanaan**.</span><span class="sxs-lookup"><span data-stu-id="5fec3-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="5fec3-119">Pilih **Paparkan senarai organisasi tersedia** dan kotak semak **Tunjukkan Lanjutan**.</span><span class="sxs-lookup"><span data-stu-id="5fec3-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="5fec3-120">Pilih rantau penyewa anda, masukkan kelayakan anda dan pilih **Log masuk**.</span><span class="sxs-lookup"><span data-stu-id="5fec3-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Daftar Masuk Konfigurasi](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="5fec3-122">Pada halaman 3, daripada senarai organisasi pada penyewa, pilih organisasi yang anda mahu import data demo ke dalam dan pilih **log masuk**.</span><span class="sxs-lookup"><span data-stu-id="5fec3-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="5fec3-123">Pada halaman 4, pilih fail zip, *SampleSetupAndConfigData* dari folder tak padat.</span><span class="sxs-lookup"><span data-stu-id="5fec3-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Pilihan Fail Zip](./media/3ZipFile.png)

![Pilih fail](./media/4SelectAFile.png)

9. <span data-ttu-id="5fec3-126">Selepas fail zip dipilih, pilih **Import Data**.</span><span class="sxs-lookup"><span data-stu-id="5fec3-126">After the zip file is selected, select **Import Data**.</span></span>

![Import Data](./media/5ImportData.png)

10. <span data-ttu-id="5fec3-128">Import akan berjalan selama kira-kira 2-10 minit bergantung pada kelajuan rangkaian anda.</span><span class="sxs-lookup"><span data-stu-id="5fec3-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="5fec3-129">Selepas import selesai, keluar dari CMT Wizard.</span><span class="sxs-lookup"><span data-stu-id="5fec3-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="5fec3-130">Semak organisasi anda untuk data dalam 19 entiti berikut:</span><span class="sxs-lookup"><span data-stu-id="5fec3-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="5fec3-131">Mata wang</span><span class="sxs-lookup"><span data-stu-id="5fec3-131">Currency</span></span>
  - <span data-ttu-id="5fec3-132">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="5fec3-132">Organizational Unit</span></span>
  - <span data-ttu-id="5fec3-133">Orang Hubungan</span><span class="sxs-lookup"><span data-stu-id="5fec3-133">Contact</span></span>
  - <span data-ttu-id="5fec3-134">Cukai Kumpulan</span><span class="sxs-lookup"><span data-stu-id="5fec3-134">Tax Group</span></span>
  - <span data-ttu-id="5fec3-135">Kumpulan Pelanggan</span><span class="sxs-lookup"><span data-stu-id="5fec3-135">Customer Group</span></span>
  - <span data-ttu-id="5fec3-136">Unit</span><span class="sxs-lookup"><span data-stu-id="5fec3-136">Unit</span></span>
  - <span data-ttu-id="5fec3-137">Kumpulan Unit</span><span class="sxs-lookup"><span data-stu-id="5fec3-137">Unit Group</span></span>
  - <span data-ttu-id="5fec3-138">Senarai Harga</span><span class="sxs-lookup"><span data-stu-id="5fec3-138">Price List</span></span>
  - <span data-ttu-id="5fec3-139">Senarai Harga Parameter Projek</span><span class="sxs-lookup"><span data-stu-id="5fec3-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="5fec3-140">Kekerapan Invois</span><span class="sxs-lookup"><span data-stu-id="5fec3-140">Invoice Frequency</span></span>
  - <span data-ttu-id="5fec3-141">Kategori Sumber Boleh Ditempah</span><span class="sxs-lookup"><span data-stu-id="5fec3-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="5fec3-142">Kategori Transaksi</span><span class="sxs-lookup"><span data-stu-id="5fec3-142">Transaction Category</span></span>
  - <span data-ttu-id="5fec3-143">Kategori Perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="5fec3-143">Expense Category</span></span>
  - <span data-ttu-id="5fec3-144">Harga Peranan</span><span class="sxs-lookup"><span data-stu-id="5fec3-144">Role Price</span></span>
  - <span data-ttu-id="5fec3-145">Harga Kategori Transaksi</span><span class="sxs-lookup"><span data-stu-id="5fec3-145">Transaction Category Price</span></span>
  - <span data-ttu-id="5fec3-146">Ciri</span><span class="sxs-lookup"><span data-stu-id="5fec3-146">Characteristic</span></span>
  - <span data-ttu-id="5fec3-147">Sumber Boleh Ditempah</span><span class="sxs-lookup"><span data-stu-id="5fec3-147">Bookable Resource</span></span>
  - <span data-ttu-id="5fec3-148">Penyekutuan kategori sumber boleh ditempah</span><span class="sxs-lookup"><span data-stu-id="5fec3-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="5fec3-149">Penyekutuan Cirian Sumber Boleh Ditempah</span><span class="sxs-lookup"><span data-stu-id="5fec3-149">Bookable Resource Characteristic</span></span>

![Lengkapkan Import](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="5fec3-151">Kemas kini konfigurasi Operasi Projek</span><span class="sxs-lookup"><span data-stu-id="5fec3-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="5fec3-152">Navigasi ke persekitaran CE.</span><span class="sxs-lookup"><span data-stu-id="5fec3-152">Navigate to the CE environment.</span></span> <span data-ttu-id="5fec3-153">Anda boleh menemuinya dengan membuka Pusat pentadbir [Power Platform](https://admin.powerplatform.microsoft.com/environments), memilih persekitaran dan kemudian memilih **Persekitaran Terbuka**.</span><span class="sxs-lookup"><span data-stu-id="5fec3-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Persekitaran Terbuka](./media/7OpenEnvironment.png)

2. <span data-ttu-id="5fec3-155">Pergi ke **Sumber** > **Projek** dan kemudian pilih **Baharu** untuk mencipta sumber boleh ditempah untuk pengguna anda.</span><span class="sxs-lookup"><span data-stu-id="5fec3-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Sumber Boleh Ditempah](./media/8BookableResources.png)

3. <span data-ttu-id="5fec3-157">Pada tab **Umum**, pilih pengguna pentadbir anda.</span><span class="sxs-lookup"><span data-stu-id="5fec3-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="5fec3-158">Sahkan bahawa zon waktu sepadan dengan yang anda berada.</span><span class="sxs-lookup"><span data-stu-id="5fec3-158">Verify that the time zone matches the one you are in.</span></span> 

![Sumber Boleh Ditempah Baharu](./media/9NewBookableResource.png)

4. <span data-ttu-id="5fec3-160">Pada tab **Penjadualan**, dalam medan **Syarikat**, pilih syarikat **USPM** dan kemudian pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="5fec3-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Tab Penjadualan](./media/10SchedulingTab.png)

5. <span data-ttu-id="5fec3-162">Pilih tab **Waktu kerja**.</span><span class="sxs-lookup"><span data-stu-id="5fec3-162">Select the **Work hours** tab.</span></span>  

![Jam Kerja](./media/11WorkHours.png)

6. <span data-ttu-id="5fec3-164">Klik dua kali pada mana-mana nilai dalam kalendar dan pilih **Edit** > **Semua acara dalam siri ini**.</span><span class="sxs-lookup"><span data-stu-id="5fec3-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Kalendar Kerja](./media/12WorkCalendar.png)

7. <span data-ttu-id="5fec3-166">Tukar masa kerja ke lapan (8) jam hari kerja, tandakan hujung minggu sebagai hari bukan kerja, dan pastikan zon waktu sepadan dengan anda.</span><span class="sxs-lookup"><span data-stu-id="5fec3-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="5fec3-167">Pilih **Simpan dan tutup**.</span><span class="sxs-lookup"><span data-stu-id="5fec3-167">Select **Save and close**.</span></span>

![Kemas Kini Kalendar](./media/13UpdateCalendar.png)

9. <span data-ttu-id="5fec3-169">Pergi ke **Tetapan** > **Templat kalendar** dan pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="5fec3-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Templat Kalendar](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="5fec3-171">Masukkan nama, pilih sumber templat yang anda cipta dan kemudian pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="5fec3-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Simpan Templat Kalendar](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="5fec3-173">Pergi ke **Parameter** dan klik dua kali pada rekod.</span><span class="sxs-lookup"><span data-stu-id="5fec3-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parameter Projek](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="5fec3-175">Kemas kini medan berikut:</span><span class="sxs-lookup"><span data-stu-id="5fec3-175">Update the following fields:</span></span>

 - <span data-ttu-id="5fec3-176">**Syarikat lalai**: USPM</span><span class="sxs-lookup"><span data-stu-id="5fec3-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="5fec3-177">**Unit Organisasi Lalai** : Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="5fec3-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="5fec3-178">**Frekuensi Invois**: Ketujuh dan Hari Terakhir</span><span class="sxs-lookup"><span data-stu-id="5fec3-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="5fec3-179">**Templat jam kerja**: Tukar ke templat yang anda cipta.</span><span class="sxs-lookup"><span data-stu-id="5fec3-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="5fec3-180">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="5fec3-180">Select **Save**.</span></span> 

![Parameter Projek Dikemas Kini](./media/17UpdatedProjectParameters.png)
