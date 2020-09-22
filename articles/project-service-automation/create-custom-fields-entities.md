---
title: Cipta medan tersuai dan entiti
description: Topik ini menerangkan cara mencipta set pilihan dan entiti dalam penyelesaian anda sendiri dalam platform Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753971"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="ede89-103">Cipta medan tersuai dan entiti</span><span class="sxs-lookup"><span data-stu-id="ede89-103">Create custom fields and entities</span></span> 

<span data-ttu-id="ede89-104">Lengkapkan langkah-langkah berikut pada bila-bila masa anda mahu mencipta set pilihan atau entiti tersuai pada platform Power Apps.</span><span class="sxs-lookup"><span data-stu-id="ede89-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="ede89-105">Prosedur dalam topik ini hendaklah diselesaikan menggunakan antara muka web Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="ede89-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ede89-106">Kami mengesyorkan agar anda membuat semua perubahan dimensi penentuan harga dalam penyelesaian berasingan.</span><span class="sxs-lookup"><span data-stu-id="ede89-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="ede89-107">Amalan terbaik penting ini memberikan kefleksibelan pada masa akan datang untuk mengemas kini atau mengalih keluar perubahan seperti yang diperlukan, akan membantu menggunakan semula kerja anda, dan memudahkan untuk port perubahan ini kepada tika lain.</span><span class="sxs-lookup"><span data-stu-id="ede89-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="ede89-108">Selepas anda membuat semua perubahan yang diperlukan, eksport penyelesaian ini sebagai **Penyelesaian terurus** dan import ini ke dalam tika lain untuk guna semula persediaan penentuan harga anda.</span><span class="sxs-lookup"><span data-stu-id="ede89-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="ede89-109">Cipta penyelesaian tersuai untuk dimensi penentuan harga</span><span class="sxs-lookup"><span data-stu-id="ede89-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="ede89-110">Dalam PSA, klik **Tetapan** > **Penyelesaian**, kemudian klik **Baharu** untuk mencipta penyelesaian baharu.</span><span class="sxs-lookup"><span data-stu-id="ede89-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="ede89-111">Namakan penyelesaian, **\<nama organisasi anda> dimensi penentuan harga**, masukkan baki maklumat yang diperlukan, kemudian klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="ede89-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Mencipta penyelesaian tersuai untuk dimensi penentuan harga](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="ede89-113">Cipta medan tersuai dan seti pilihan dalam penyelesaian dimensi penentuan harga</span><span class="sxs-lookup"><span data-stu-id="ede89-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="ede89-114">Dimensi penentuan harga boleh menjadi set pilihan atau entiti.</span><span class="sxs-lookup"><span data-stu-id="ede89-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="ede89-115">Kedua-duanya mesti dicipta dalam penyelesaian penentuan harga anda.</span><span class="sxs-lookup"><span data-stu-id="ede89-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="ede89-116">Langkah-langkah dalam prosedur ini menerangkan cara mencipta dimensi berasaskan entiti dan dimensi berasaskan set pilihan.</span><span class="sxs-lookup"><span data-stu-id="ede89-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="ede89-117">Dimensi berasaskan entiti</span><span class="sxs-lookup"><span data-stu-id="ede89-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="ede89-118">Dalam PSA, klik **Tetapan** > **Penyelesaian**, kemudian klik dua kali **\<nama organisasi anda> dimensi penentuan harga**.</span><span class="sxs-lookup"><span data-stu-id="ede89-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="ede89-119">Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Entiti**.</span><span class="sxs-lookup"><span data-stu-id="ede89-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="ede89-120">Klik **Baharu** untuk mencipta entiti baharu dipanggil **Tajuk Standard**.</span><span class="sxs-lookup"><span data-stu-id="ede89-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="ede89-121">Masukkan baki maklumat diperlukan, kemudian klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="ede89-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definisi entiti tajuk standard](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="ede89-123">Dimensi berasaskan set pilihan</span><span class="sxs-lookup"><span data-stu-id="ede89-123">Option set-based dimensions</span></span> 
<span data-ttu-id="ede89-124">Anda boleh mencipta dua dimensi berasaskan set pilihan.</span><span class="sxs-lookup"><span data-stu-id="ede89-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="ede89-125">Guna **Lokasi Kerja Sumber** untuk menjejaki harga kerja lokasi **Rumah** dan kerja **Di Tapak** dan menggunakan **Jam Bekerja Sumber** dengan nilai **Biasa** dan **Lebih Masa** untuk mengenakan tokokan apabila kerja selesai.</span><span class="sxs-lookup"><span data-stu-id="ede89-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="ede89-126">Dalam PSA, klik **Tetapan** > **Penyelesaian**, kemudian klik dua kali **\<nama organisasi anda> dimensi penentuan harga**.</span><span class="sxs-lookup"><span data-stu-id="ede89-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="ede89-127">Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Set Pilihan**.</span><span class="sxs-lookup"><span data-stu-id="ede89-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="ede89-128">Klik **Baharu** untuk mencipta set pilihan baharu, masukkan baki maklumat yang diperlukan, kemudian klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="ede89-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="ede89-129">Dimensi penentuan harga berasaskan set pilihan dipanggil Lokasi Kerja Sumber</span><span class="sxs-lookup"><span data-stu-id="ede89-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="ede89-130">Dimensi penentuan harga berasaskan set pilihan dipanggil Waktu Kerja Sumber</span><span class="sxs-lookup"><span data-stu-id="ede89-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="ede89-131">Cipta data untuk dimensi berasaskan entiti</span><span class="sxs-lookup"><span data-stu-id="ede89-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="ede89-132">Anda boleh mencipta data untuk dimensi berasaskan entiti secara manual, atau menggunakan panggilan import atau perkhidmatan Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="ede89-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="ede89-133">Guna langkah-langkah dalam prosedur ini untuk mencipta dua jawatan standard **Jurutera Sistem** dan **Jurutera Sistem Kanan** daripada dimensi berasaskan entiti, **Jawatan Standard**.</span><span class="sxs-lookup"><span data-stu-id="ede89-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="ede89-134">Jika data yang anda mahu cipta adalah kecil, seperti dalam contoh berikut, anda boleh menggunakan borang standard.</span><span class="sxs-lookup"><span data-stu-id="ede89-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="ede89-135">Dalam PSA, klik **Carian Lanjutan**.</span><span class="sxs-lookup"><span data-stu-id="ede89-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="ede89-136">Pilih entiti **Jawatan Standard** dan kemudian klik **Hasil**.</span><span class="sxs-lookup"><span data-stu-id="ede89-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="ede89-137">Semua baris dalam entiti **Jawatan Standard** akan ditunjukkan.</span><span class="sxs-lookup"><span data-stu-id="ede89-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="ede89-138">Klik **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="ede89-138">Click **New**.</span></span> <span data-ttu-id="ede89-139">Dalam medan **Nama**, masukkan "Jurutera Sistem" dan kemudian klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="ede89-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="ede89-140">Tutup borang.</span><span class="sxs-lookup"><span data-stu-id="ede89-140">Close the form.</span></span> 
4. <span data-ttu-id="ede89-141">Ulangi langkah 1 - 3 untuk mencipta jawatan lain untuk "Jurutera Sistem Kanan".</span><span class="sxs-lookup"><span data-stu-id="ede89-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="ede89-142">Data Sampel untuk entiti Jawatan Standard</span><span class="sxs-lookup"><span data-stu-id="ede89-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="ede89-143">Tambah semua entiti PSA yang diperlukan dan dokumen berkaitan dengan Penyelesaian Dimensi Penentuan Harga</span><span class="sxs-lookup"><span data-stu-id="ede89-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="ede89-144">Anda perlu menambah entiti Project Service berikut pada penyelesaian penentuan harga anda.</span><span class="sxs-lookup"><span data-stu-id="ede89-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="ede89-145">Guna langkah-langkah dalam prosedur untuk membuat perubahan penting dalam penyelesaian penentuan harga agar entiti maklum dengan dimensi penentuan harga baharu.</span><span class="sxs-lookup"><span data-stu-id="ede89-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="ede89-146">Dalam PSA, klik **Tetapan** > **Penyelesaian**, kemudian klik dua kali **\<nama organisasi anda> dimensi penentuan harga**.</span><span class="sxs-lookup"><span data-stu-id="ede89-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="ede89-147">Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Tambah Sedia Ada** > **Entiti**.</span><span class="sxs-lookup"><span data-stu-id="ede89-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="ede89-148">Dalam kotak dialog **Komponen Penyelesaian**, pilih entiti berikut:</span><span class="sxs-lookup"><span data-stu-id="ede89-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="ede89-149">Sebenar</span><span class="sxs-lookup"><span data-stu-id="ede89-149">Actual</span></span>
- <span data-ttu-id="ede89-150">Sumber Boleh Ditempah</span><span class="sxs-lookup"><span data-stu-id="ede89-150">Bookable Resource</span></span>
- <span data-ttu-id="ede89-151">Garisan Anggaran</span><span class="sxs-lookup"><span data-stu-id="ede89-151">Estimate Line</span></span>
- <span data-ttu-id="ede89-152">Butiran Baris Invois</span><span class="sxs-lookup"><span data-stu-id="ede89-152">Invoice Line Detail</span></span>
- <span data-ttu-id="ede89-153">Garisan Jurnal</span><span class="sxs-lookup"><span data-stu-id="ede89-153">Journal Line</span></span>
- <span data-ttu-id="ede89-154">Butiran Baris Kontrak Projek</span><span class="sxs-lookup"><span data-stu-id="ede89-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="ede89-155">Ahli Pasukan Projek</span><span class="sxs-lookup"><span data-stu-id="ede89-155">Project Team Member</span></span>
- <span data-ttu-id="ede89-156">Butiran Baris Sebut Harga</span><span class="sxs-lookup"><span data-stu-id="ede89-156">Quote Line Detail</span></span>
- <span data-ttu-id="ede89-157">Tokokan Harga Peranan</span><span class="sxs-lookup"><span data-stu-id="ede89-157">Role Price Markup</span></span>
- <span data-ttu-id="ede89-158">Harga Peranan</span><span class="sxs-lookup"><span data-stu-id="ede89-158">Role Price</span></span> 
- <span data-ttu-id="ede89-159">Entri Masa</span><span class="sxs-lookup"><span data-stu-id="ede89-159">Time Entry</span></span> 

> ![Tambah entiti sedia ada untuk penyelesaian dimensi penentuan harga](media/Existing-entities-to-PD-solution.png)

> ![Pilih komponen penyelesaian](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="ede89-162">Pastikan anda memasukkan semua borang dan pandangan bagi setiap entiti yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="ede89-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="ede89-163">Apabila digesa untuk memasukkan sebarang entiti bersandar untuk entiti yang dipilih di atas, klik **Tidak**.</span><span class="sxs-lookup"><span data-stu-id="ede89-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![Jangan masukkan semua komponen berkaitan](media/Do-not-include-required.png)


