---
title: Sediakan dan gunakan data konfigurasi dalam Common Data Service
description: Topik ini memberikan maklumat tentang menyediakan dan menggunakan data konfigurasi dalam Operasi Projek.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ea00df6112fb69b61f1889463424fdfee79aec9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001302"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="e4195-103">Sediakan dan gunakan data konfigurasi dalam Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e4195-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="e4195-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="e4195-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="e4195-105">Prasyarat</span><span class="sxs-lookup"><span data-stu-id="e4195-105">Prerequisites</span></span>

<span data-ttu-id="e4195-106">Sebelum anda mula mengkonfigurasikan data dalam Common Data Service (CDS), prasyarat berikut mesti dipenuhi:</span><span class="sxs-lookup"><span data-stu-id="e4195-106">Before you begin to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="e4195-107">Peruntukan persekitaran CDS dan persekitaran Dynamics 365 Finance untuk Project Operations.</span><span class="sxs-lookup"><span data-stu-id="e4195-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="e4195-108">Maklumat entiti sah daripada Dynamics 365 Finance dikongsi pada persekitaran CDS.</span><span class="sxs-lookup"><span data-stu-id="e4195-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="e4195-109">Ini bermaksud bahawa entiti **Syarikat** dalam CDS mempunyai rekod syarikat berikut:</span><span class="sxs-lookup"><span data-stu-id="e4195-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="e4195-110">THPM</span><span class="sxs-lookup"><span data-stu-id="e4195-110">THPM</span></span>
  - <span data-ttu-id="e4195-111">USPM</span><span class="sxs-lookup"><span data-stu-id="e4195-111">USPM</span></span>
  - <span data-ttu-id="e4195-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="e4195-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="e4195-113">Memasang data persediaan dan konfigurasi</span><span class="sxs-lookup"><span data-stu-id="e4195-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="e4195-114">Muat turun, menyahsekat dan unzip [Pakej Data Persediaan dan Konfigurasi](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span><span class="sxs-lookup"><span data-stu-id="e4195-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span></span>
2. <span data-ttu-id="e4195-115">Navigasi ke folder nyahzip dan jalankan fail boleh laku, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="e4195-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="e4195-116">Pada halaman 1 dalam Wizard Penghijrahan Konfigurasi (CMT) Common Data Service, pilih **Import Data** dan kemudian pilih **Teruskan**.</span><span class="sxs-lookup"><span data-stu-id="e4195-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrasi Konfigurasi](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="e4195-118">Pada Halaman 2 dalam Wizard CMT, pilih **Microsoft 365** sebagai **Jenis Perlaksanaan**.</span><span class="sxs-lookup"><span data-stu-id="e4195-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="e4195-119">Pilih **Paparkan senarai organisasi tersedia** dan kotak semak **Tunjukkan Lanjutan**.</span><span class="sxs-lookup"><span data-stu-id="e4195-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="e4195-120">Pilih rantau penyewa anda, masukkan kelayakan anda dan pilih **Log masuk**.</span><span class="sxs-lookup"><span data-stu-id="e4195-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Daftar Masuk Konfigurasi](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="e4195-122">Pada halaman 3, daripada senarai organisasi pada penyewa, pilih organisasi yang anda mahu import data demo ke dalam dan pilih **log masuk**.</span><span class="sxs-lookup"><span data-stu-id="e4195-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="e4195-123">Pada halaman 4, pilih fail zip, *SampleSetupAndConfigData* dari folder tak padat.</span><span class="sxs-lookup"><span data-stu-id="e4195-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Pilihan Fail Zip](./media/3ZipFile.png)

![Pilih fail](./media/4SelectAFile.png)

9. <span data-ttu-id="e4195-126">Selepas fail zip dipilih, pilih **Import Data**.</span><span class="sxs-lookup"><span data-stu-id="e4195-126">After the zip file is selected, select **Import Data**.</span></span>

![Import Data](./media/5ImportData.png)

10. <span data-ttu-id="e4195-128">Import akan berjalan selama kira-kira 2-10 minit bergantung pada kelajuan rangkaian anda.</span><span class="sxs-lookup"><span data-stu-id="e4195-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="e4195-129">Selepas import selesai, keluar dari CMT Wizard.</span><span class="sxs-lookup"><span data-stu-id="e4195-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="e4195-130">Semak organisasi anda untuk data dalam 26 entiti berikut:</span><span class="sxs-lookup"><span data-stu-id="e4195-130">Check your organization for data in the following 26 entities:</span></span>

  - <span data-ttu-id="e4195-131">Mata wang</span><span class="sxs-lookup"><span data-stu-id="e4195-131">Currency</span></span>
  - <span data-ttu-id="e4195-132">Carta Akaun</span><span class="sxs-lookup"><span data-stu-id="e4195-132">Chart of Accounts</span></span>
  - <span data-ttu-id="e4195-133">Kalendar Fiskal</span><span class="sxs-lookup"><span data-stu-id="e4195-133">Fiscal Calendar</span></span>
  - <span data-ttu-id="e4195-134">Jenis Kadar Tukaran Mata Wang</span><span class="sxs-lookup"><span data-stu-id="e4195-134">Currency Exchange Rate Types</span></span>
  - <span data-ttu-id="e4195-135">Hari Pembayaran</span><span class="sxs-lookup"><span data-stu-id="e4195-135">Payment Day</span></span>
  - <span data-ttu-id="e4195-136">Jadual Pembayaran</span><span class="sxs-lookup"><span data-stu-id="e4195-136">Payment Schedule</span></span>
  - <span data-ttu-id="e4195-137">Terma Pembayaran</span><span class="sxs-lookup"><span data-stu-id="e4195-137">Payment Term</span></span>
  - <span data-ttu-id="e4195-138">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="e4195-138">Organizational Unit</span></span>
  - <span data-ttu-id="e4195-139">Kenalan</span><span class="sxs-lookup"><span data-stu-id="e4195-139">Contact</span></span>
  - <span data-ttu-id="e4195-140">Cukai Kumpulan</span><span class="sxs-lookup"><span data-stu-id="e4195-140">Tax Group</span></span>
  - <span data-ttu-id="e4195-141">Kumpulan Pelanggan</span><span class="sxs-lookup"><span data-stu-id="e4195-141">Customer Group</span></span>
  - <span data-ttu-id="e4195-142">Kumpulan Vendor</span><span class="sxs-lookup"><span data-stu-id="e4195-142">Vendor Group</span></span>
  - <span data-ttu-id="e4195-143">Unit</span><span class="sxs-lookup"><span data-stu-id="e4195-143">Unit</span></span>
  - <span data-ttu-id="e4195-144">Kumpulan Unit</span><span class="sxs-lookup"><span data-stu-id="e4195-144">Unit Group</span></span>
  - <span data-ttu-id="e4195-145">Senarai Harga</span><span class="sxs-lookup"><span data-stu-id="e4195-145">Price List</span></span>
  - <span data-ttu-id="e4195-146">Senarai Harga Parameter Projek</span><span class="sxs-lookup"><span data-stu-id="e4195-146">Project Parameter Price List</span></span>
  - <span data-ttu-id="e4195-147">Kekerapan Invois</span><span class="sxs-lookup"><span data-stu-id="e4195-147">Invoice Frequency</span></span>
  - <span data-ttu-id="e4195-148">Kategori Sumber Boleh Ditempah</span><span class="sxs-lookup"><span data-stu-id="e4195-148">Bookable Resource Category</span></span>
  - <span data-ttu-id="e4195-149">Kategori Transaksi</span><span class="sxs-lookup"><span data-stu-id="e4195-149">Transaction Category</span></span>
  - <span data-ttu-id="e4195-150">Kategori Perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="e4195-150">Expense Category</span></span>
  - <span data-ttu-id="e4195-151">Harga Peranan</span><span class="sxs-lookup"><span data-stu-id="e4195-151">Role Price</span></span>
  - <span data-ttu-id="e4195-152">Harga Kategori Transaksi</span><span class="sxs-lookup"><span data-stu-id="e4195-152">Transaction Category Price</span></span>
  - <span data-ttu-id="e4195-153">Ciri</span><span class="sxs-lookup"><span data-stu-id="e4195-153">Characteristic</span></span>
  - <span data-ttu-id="e4195-154">Sumber Boleh Ditempah</span><span class="sxs-lookup"><span data-stu-id="e4195-154">Bookable Resource</span></span>
  - <span data-ttu-id="e4195-155">Penyekutuan kategori sumber boleh ditempah</span><span class="sxs-lookup"><span data-stu-id="e4195-155">Bookable resource category Assn</span></span>
  - <span data-ttu-id="e4195-156">Penyekutuan Cirian Sumber Boleh Ditempah</span><span class="sxs-lookup"><span data-stu-id="e4195-156">Bookable Resource Characteristic</span></span>

![Lengkapkan Import](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="e4195-158">Kemas kini konfigurasi Operasi Projek</span><span class="sxs-lookup"><span data-stu-id="e4195-158">Update Project Operations configurations</span></span>

1. <span data-ttu-id="e4195-159">Navigasi ke persekitaran CE.</span><span class="sxs-lookup"><span data-stu-id="e4195-159">Navigate to the CE environment.</span></span> <span data-ttu-id="e4195-160">Anda boleh menemuinya dengan membuka Pusat pentadbir [Power Platform](https://admin.powerplatform.microsoft.com/environments), memilih persekitaran dan kemudian memilih **Persekitaran Terbuka**.</span><span class="sxs-lookup"><span data-stu-id="e4195-160">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Persekitaran Terbuka](./media/7OpenEnvironment.png)

2. <span data-ttu-id="e4195-162">Pergi ke **Sumber** > **Projek** dan kemudian pilih **Baharu** untuk mencipta sumber boleh ditempah untuk pengguna anda.</span><span class="sxs-lookup"><span data-stu-id="e4195-162">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Sumber Boleh Ditempah](./media/8BookableResources.png)

3. <span data-ttu-id="e4195-164">Pada tab **Umum**, pilih pengguna pentadbir anda.</span><span class="sxs-lookup"><span data-stu-id="e4195-164">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="e4195-165">Sahkan bahawa zon waktu sepadan dengan yang anda berada.</span><span class="sxs-lookup"><span data-stu-id="e4195-165">Verify that the time zone matches the one you are in.</span></span> 

![Sumber Boleh Ditempah Baharu](./media/9NewBookableResource.png)

4. <span data-ttu-id="e4195-167">Pada tab **Penjadualan**, dalam medan **Syarikat**, pilih syarikat **USPM** dan kemudian pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="e4195-167">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Tab Penjadualan](./media/10SchedulingTab.png)

5. <span data-ttu-id="e4195-169">Pilih tab **Waktu kerja**.</span><span class="sxs-lookup"><span data-stu-id="e4195-169">Select the **Work hours** tab.</span></span>  

![Jam Kerja](./media/11WorkHours.png)

6. <span data-ttu-id="e4195-171">Klik dua kali pada mana-mana nilai dalam kalendar dan pilih **Edit** > **Semua acara dalam siri ini**.</span><span class="sxs-lookup"><span data-stu-id="e4195-171">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Kalendar Kerja](./media/12WorkCalendar.png)

7. <span data-ttu-id="e4195-173">Tukar masa kerja ke lapan (8) jam hari kerja, tandakan hujung minggu sebagai hari bukan kerja, dan pastikan zon waktu sepadan dengan anda.</span><span class="sxs-lookup"><span data-stu-id="e4195-173">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="e4195-174">Pilih **Simpan dan tutup**.</span><span class="sxs-lookup"><span data-stu-id="e4195-174">Select **Save and close**.</span></span>

![Kemas Kini Kalendar](./media/13UpdateCalendar.png)

9. <span data-ttu-id="e4195-176">Pergi ke **Tetapan** > **Templat kalendar** dan pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="e4195-176">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Templat Kalendar](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="e4195-178">Masukkan nama, pilih sumber templat yang anda cipta dan kemudian pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="e4195-178">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Simpan Templat Kalendar](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="e4195-180">Pergi ke **Parameter** dan klik dua kali pada rekod.</span><span class="sxs-lookup"><span data-stu-id="e4195-180">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parameter Projek](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="e4195-182">Kemas kini medan berikut:</span><span class="sxs-lookup"><span data-stu-id="e4195-182">Update the following fields:</span></span>

 - <span data-ttu-id="e4195-183">**Syarikat lalai**: USPM</span><span class="sxs-lookup"><span data-stu-id="e4195-183">**Default company**: USPM</span></span>
 - <span data-ttu-id="e4195-184">**Unit Organisasi Lalai**: Global Robotik Contoso</span><span class="sxs-lookup"><span data-stu-id="e4195-184">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="e4195-185">**Frekuensi Invois**: Ketujuh dan Hari Terakhir</span><span class="sxs-lookup"><span data-stu-id="e4195-185">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="e4195-186">**Templat jam kerja**: Tukar ke templat yang anda cipta.</span><span class="sxs-lookup"><span data-stu-id="e4195-186">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="e4195-187">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="e4195-187">Select **Save**.</span></span> 

![Parameter Projek Dikemas Kini](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
