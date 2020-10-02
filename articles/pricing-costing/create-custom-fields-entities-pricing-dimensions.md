---
title: Cipta medan dan entiti tersuai sebagai dimensi penentuan harga
description: Topik ini menyediakan maklumat tentang cara mencipta set pilihan atau entiti tersuai.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2000f7e710267560fe2bd52b0e33024617d108ea
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898272"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="045f2-103">Cipta medan dan entiti tersuai sebagai dimensi penentuan harga</span><span class="sxs-lookup"><span data-stu-id="045f2-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="045f2-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="045f2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="045f2-105">Lengkapkan langkah berikut pada bila-bila masa anda mahu mencipta set pilihan atau entiti tersuai.</span><span class="sxs-lookup"><span data-stu-id="045f2-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="045f2-106">Kami mengesyorkan agar anda membuat semua perubahan dimensi penentuan harga dalam penyelesaian berasingan.</span><span class="sxs-lookup"><span data-stu-id="045f2-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="045f2-107">Amalan terbaik penting ini memberikan kefleksibelan pada masa akan datang untuk mengemas kini atau mengalih keluar perubahan seperti yang diperlukan, akan membantu menggunakan semula kerja anda, dan memudahkan untuk port perubahan ini kepada tika lain.</span><span class="sxs-lookup"><span data-stu-id="045f2-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="045f2-108">Selepas anda membuat semua perubahan yang diperlukan, eksport penyelesaian ini sebagai **Penyelesaian terurus** dan import ini ke dalam tika lain untuk guna semula persediaan penentuan harga anda.</span><span class="sxs-lookup"><span data-stu-id="045f2-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="045f2-109">Cipta penyelesaian tersuai untuk dimensi penentuan harga</span><span class="sxs-lookup"><span data-stu-id="045f2-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="045f2-110">Pergi ke **Tetapan** > **Penyelesaian** dan, kemudian pilih **Baharu** untuk mencipta penyelesaian baharu.</span><span class="sxs-lookup"><span data-stu-id="045f2-110">Go to **Settings** > **Solutions**, and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="045f2-111">Namakan penyelesaian, **\<your organization name> dimensi penetapan harga**, masukkan baki maklumat yang diperlukan dan kemudian pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="045f2-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="045f2-112">Cipta medan tersuai dan seti pilihan dalam penyelesaian dimensi penentuan harga</span><span class="sxs-lookup"><span data-stu-id="045f2-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="045f2-113">Dimensi penentuan harga boleh menjadi set pilihan atau entiti.</span><span class="sxs-lookup"><span data-stu-id="045f2-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="045f2-114">Kedua-duanya mesti dicipta dalam penyelesaian penentuan harga anda.</span><span class="sxs-lookup"><span data-stu-id="045f2-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="045f2-115">Langkah-langkah dalam prosedur ini menerangkan cara mencipta dimensi berasaskan entiti dan dimensi berasaskan set pilihan.</span><span class="sxs-lookup"><span data-stu-id="045f2-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="045f2-116">Dimensi berasaskan entiti</span><span class="sxs-lookup"><span data-stu-id="045f2-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="045f2-117">Pergi ke **Tetapan** > **Penyelesaian** dan kemudian klik dua kali **\<your organization name> dimensi penetapan harga**.</span><span class="sxs-lookup"><span data-stu-id="045f2-117">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="045f2-118">Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Entiti**.</span><span class="sxs-lookup"><span data-stu-id="045f2-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="045f2-119">Pilih **Baharu** untuk mencipta entiti baharu dipanggil **Tajuk Standard**.</span><span class="sxs-lookup"><span data-stu-id="045f2-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="045f2-120">Masukkan baki maklumat diperlukan dan kemudian pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="045f2-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="045f2-121">Dimensi berasaskan set pilihan</span><span class="sxs-lookup"><span data-stu-id="045f2-121">Option set-based dimensions</span></span> 
<span data-ttu-id="045f2-122">Anda boleh mencipta dua dimensi berasaskan set pilihan.</span><span class="sxs-lookup"><span data-stu-id="045f2-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="045f2-123">Guna **Lokasi Kerja Sumber** untuk menjejaki harga kerja lokasi **Rumah** dan kerja **Di Tapak** dan menggunakan **Jam Bekerja Sumber** dengan nilai **Biasa** dan **Lebih Masa** untuk mengenakan tokokan apabila kerja selesai.</span><span class="sxs-lookup"><span data-stu-id="045f2-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="045f2-124">Pergi ke **Tetapan** > **Penyelesaian** dan klik dua kali **\<your organization name> dimensi penetapan harga**.</span><span class="sxs-lookup"><span data-stu-id="045f2-124">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="045f2-125">Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Set Pilihan**.</span><span class="sxs-lookup"><span data-stu-id="045f2-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="045f2-126">Pilih **Baharu** untuk mencipta set pilihan baharu, masukkan baki maklumat yang diperlukan, kemudian pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="045f2-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="045f2-127">Cipta data untuk dimensi berasaskan entiti</span><span class="sxs-lookup"><span data-stu-id="045f2-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="045f2-128">Anda boleh mencipta data untuk dimensi berasaskan entiti secara manual, atau menggunakan panggilan import atau perkhidmatan Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="045f2-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="045f2-129">Guna langkah-langkah dalam prosedur ini untuk mencipta dua jawatan standard **Jurutera Sistem** dan **Jurutera Sistem Kanan** daripada dimensi berasaskan entiti, **Jawatan Standard**.</span><span class="sxs-lookup"><span data-stu-id="045f2-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="045f2-130">Jika data yang anda mahu cipta adalah kecil, seperti dalam contoh berikut, anda boleh menggunakan borang standard.</span><span class="sxs-lookup"><span data-stu-id="045f2-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="045f2-131">Pilih **Carian Lanjutan**, pilih entiti **Tajuk Standard** dan kemudian pilih **Keputusan**.</span><span class="sxs-lookup"><span data-stu-id="045f2-131">Select **Advanced Find**, select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="045f2-132">Semua baris dalam entiti **Jawatan Standard** akan ditunjukkan.</span><span class="sxs-lookup"><span data-stu-id="045f2-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="045f2-133">Pilih **Baharu** dan dalam medan **Nama**, masukkan "Jurutera Sistem" dan kemudian pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="045f2-133">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="045f2-134">Tutup borang.</span><span class="sxs-lookup"><span data-stu-id="045f2-134">Close the form.</span></span> 
4. <span data-ttu-id="045f2-135">Ulangi langkah 1 - 3 untuk mencipta jawatan lain untuk "Jurutera Sistem Kanan".</span><span class="sxs-lookup"><span data-stu-id="045f2-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="045f2-136">Tambah semua entiti yang diperlukan dan dokumen berkaitan ke Penyelesaian Dimensi Penetapan Harga</span><span class="sxs-lookup"><span data-stu-id="045f2-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="045f2-137">Anda perlu menambah entiti berikut ke penyelesaian penetapan harga anda.</span><span class="sxs-lookup"><span data-stu-id="045f2-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="045f2-138">Guna langkah-langkah dalam prosedur untuk membuat perubahan penting dalam penyelesaian penentuan harga agar entiti maklum dengan dimensi penentuan harga baharu.</span><span class="sxs-lookup"><span data-stu-id="045f2-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="045f2-139">Pilih **Tetapan** > **Penyelesaian** dan klik dua kali **\<your organization name> dimensi penetapan harga**.</span><span class="sxs-lookup"><span data-stu-id="045f2-139">Select **Settings** > **Solutions**, and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="045f2-140">Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Tambah Sedia Ada** > **Entiti**.</span><span class="sxs-lookup"><span data-stu-id="045f2-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="045f2-141">Dalam kotak dialog **Komponen Penyelesaian**, pilih entiti berikut:</span><span class="sxs-lookup"><span data-stu-id="045f2-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="045f2-142">Sebenar</span><span class="sxs-lookup"><span data-stu-id="045f2-142">Actual</span></span>
  - <span data-ttu-id="045f2-143">Sumber Boleh Ditempah</span><span class="sxs-lookup"><span data-stu-id="045f2-143">Bookable Resource</span></span>
  - <span data-ttu-id="045f2-144">Garisan Anggaran</span><span class="sxs-lookup"><span data-stu-id="045f2-144">Estimate Line</span></span>
  - <span data-ttu-id="045f2-145">Butiran Baris Invois</span><span class="sxs-lookup"><span data-stu-id="045f2-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="045f2-146">Garisan Jurnal</span><span class="sxs-lookup"><span data-stu-id="045f2-146">Journal Line</span></span>
  - <span data-ttu-id="045f2-147">Butiran Baris Kontrak Projek</span><span class="sxs-lookup"><span data-stu-id="045f2-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="045f2-148">Ahli Pasukan Projek</span><span class="sxs-lookup"><span data-stu-id="045f2-148">Project Team Member</span></span>
  - <span data-ttu-id="045f2-149">Butiran Baris Sebut Harga</span><span class="sxs-lookup"><span data-stu-id="045f2-149">Quote Line Detail</span></span>
  - <span data-ttu-id="045f2-150">Tokokan Harga Peranan</span><span class="sxs-lookup"><span data-stu-id="045f2-150">Role Price Markup</span></span>
  - <span data-ttu-id="045f2-151">Harga Peranan</span><span class="sxs-lookup"><span data-stu-id="045f2-151">Role Price</span></span> 
  - <span data-ttu-id="045f2-152">Entri Masa</span><span class="sxs-lookup"><span data-stu-id="045f2-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="045f2-153">Pastikan anda memasukkan semua borang dan pandangan bagi setiap entiti yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="045f2-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="045f2-154">Apabila digesa untuk memasukkan sebarang entiti bersandar bagi entiti yang dipilih di atas, pilih **Tidak**.</span><span class="sxs-lookup"><span data-stu-id="045f2-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

