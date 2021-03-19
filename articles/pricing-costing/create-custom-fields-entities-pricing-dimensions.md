---
title: Cipta medan dan entiti tersuai sebagai dimensi penentuan harga
description: Topik ini menyediakan maklumat tentang cara mencipta set pilihan atau entiti tersuai.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 089481cd3e7c0f8f1d1aa880d64cb79e8d677c2d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275639"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="2bac6-103">Cipta medan dan entiti tersuai sebagai dimensi penentuan harga</span><span class="sxs-lookup"><span data-stu-id="2bac6-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="2bac6-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="2bac6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2bac6-105">Lengkapkan langkah berikut apabila anda mahu mencipta set pilihan atau entiti tersuai untuk menggunakan sebagai dimensi penentuan harga.</span><span class="sxs-lookup"><span data-stu-id="2bac6-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="2bac6-106">Untuk mendapatkan maklumat lanjut, lihat [Gambaran keseluruhan dimensi penentuan harga](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2bac6-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="2bac6-107">Kami mengesyorkan agar anda membuat semua perubahan dimensi penentuan harga dalam penyelesaian berasingan.</span><span class="sxs-lookup"><span data-stu-id="2bac6-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="2bac6-108">Amalan terbaik yang penting ini memberikan fleksibiliti pada masa depan untuk mengemas kini atau mengalih keluar perubahan seperti yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="2bac6-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="2bac6-109">Ini juga akan membantu dengan penggunaan semula kerja anda dan menjadikan ia lebih mudah untuk port perubahan ini kepada tika lain. Selepas anda membuat semua perubahan yang diperlukan, eksport penyelesaian ini sebagai **Penyelesaian terurus** dan mengimport ke dalam tika lain untuk menggunakan semula persediaan penentuan harga anda.</span><span class="sxs-lookup"><span data-stu-id="2bac6-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="2bac6-110">Cipta medan tersuai dan seti pilihan dalam penyelesaian dimensi penentuan harga</span><span class="sxs-lookup"><span data-stu-id="2bac6-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="2bac6-111">Dimensi penentuan harga boleh menjadi set pilihan atau entiti.</span><span class="sxs-lookup"><span data-stu-id="2bac6-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="2bac6-112">Kedua-duanya mesti dicipta dalam penyelesaian penentuan harga anda.</span><span class="sxs-lookup"><span data-stu-id="2bac6-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="2bac6-113">Langkah-langkah dalam prosedur ini menerangkan cara mencipta dimensi berasaskan entiti dan dimensi berasaskan set pilihan.</span><span class="sxs-lookup"><span data-stu-id="2bac6-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="2bac6-114">Dimensi berasaskan entiti</span><span class="sxs-lookup"><span data-stu-id="2bac6-114">Entity-based dimensions</span></span>
<span data-ttu-id="2bac6-115">Untuk mencipta dimensi berasaskan entiti, ikuti langkah ini:</span><span class="sxs-lookup"><span data-stu-id="2bac6-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="2bac6-116">Pergi ke **Tetapan** > **Penyelesaian** dan kemudian klik dua kali **\<your organization name> dimensi penetapan harga**.</span><span class="sxs-lookup"><span data-stu-id="2bac6-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="2bac6-117">Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Entiti**.</span><span class="sxs-lookup"><span data-stu-id="2bac6-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="2bac6-118">Pilih **Baharu** untuk mencipta entiti baharu dipanggil **Tajuk Standard**.</span><span class="sxs-lookup"><span data-stu-id="2bac6-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="2bac6-119">Masukkan baki maklumat diperlukan dan kemudian pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="2bac6-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Definisi entiti tajuk standard](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="2bac6-121">Dimensi berasaskan set pilihan</span><span class="sxs-lookup"><span data-stu-id="2bac6-121">Option set-based dimensions</span></span> 
<span data-ttu-id="2bac6-122">Anda boleh mencipta dua dimensi berasaskan set pilihan.</span><span class="sxs-lookup"><span data-stu-id="2bac6-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="2bac6-123">Gunakan **Lokasi Kerja Sumber** untuk menjejaki harga kerja lokasi **Rumah** dan kerja **Di Tapak**.</span><span class="sxs-lookup"><span data-stu-id="2bac6-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="2bac6-124">Gunakan **jam Kerja Sumber** dengan nilai **Biasa** dan **Kerja Lebih Masa** untuk menggunakan tokokan apabila kerja selesai.</span><span class="sxs-lookup"><span data-stu-id="2bac6-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="2bac6-125">Grafik berikut menyediakan pandangan dimensi **Lokasi Kerja Sumber**.</span><span class="sxs-lookup"><span data-stu-id="2bac6-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Dimensi penentuan harga berasaskan set pilihan dipanggil Lokasi Kerja Sumber](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="2bac6-127">Grafik berikut menyediakan pandangan dimensi **Waktu Kerja Sumber**.</span><span class="sxs-lookup"><span data-stu-id="2bac6-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Dimensi penentuan harga berasaskan set pilihan dipanggil Waktu Kerja Sumber](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="2bac6-129">Pergi ke **Tetapan** > **Penyelesaian** dan klik dua kali **\<your organization name> dimensi penetapan harga**.</span><span class="sxs-lookup"><span data-stu-id="2bac6-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="2bac6-130">Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Set Pilihan**.</span><span class="sxs-lookup"><span data-stu-id="2bac6-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="2bac6-131">Pilih **Baharu** untuk mencipta set pilihan baharu, masukkan baki maklumat yang diperlukan, kemudian pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="2bac6-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="2bac6-132">Cipta data untuk dimensi berasaskan entiti</span><span class="sxs-lookup"><span data-stu-id="2bac6-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="2bac6-133">Anda boleh mencipta data untuk dimensi berasaskan entiti secara manual, atau menggunakan panggilan import atau perkhidmatan Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="2bac6-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="2bac6-134">Guna langkah-langkah dalam prosedur ini untuk mencipta dua jawatan standard **Jurutera Sistem** dan **Jurutera Sistem Kanan** daripada dimensi berasaskan entiti, **Jawatan Standard**.</span><span class="sxs-lookup"><span data-stu-id="2bac6-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="2bac6-135">Jika data yang anda mahu cipta adalah kecil, seperti dalam contoh berikut, anda boleh menggunakan borang standard.</span><span class="sxs-lookup"><span data-stu-id="2bac6-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="2bac6-136">Pilih **Carian Lanjutan**.</span><span class="sxs-lookup"><span data-stu-id="2bac6-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="2bac6-137">Pilih entiti **Jawatan Standard** dan kemudian pilih **Hasil**.</span><span class="sxs-lookup"><span data-stu-id="2bac6-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="2bac6-138">Semua baris dalam entiti **Jawatan Standard** akan ditunjukkan.</span><span class="sxs-lookup"><span data-stu-id="2bac6-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="2bac6-139">Pilih **Baharu** dan dalam medan **Nama**, masukkan "Jurutera Sistem" dan kemudian pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="2bac6-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="2bac6-140">Tutup halaman.</span><span class="sxs-lookup"><span data-stu-id="2bac6-140">Close the page.</span></span> 
5. <span data-ttu-id="2bac6-141">Ulangi langkah 1 - 3 untuk mencipta jawatan lain untuk "Jurutera Sistem Kanan".</span><span class="sxs-lookup"><span data-stu-id="2bac6-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Data sampel untuk entiti Jawatan Standard](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]