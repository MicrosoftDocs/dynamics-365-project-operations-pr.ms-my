---
title: Cipta medan tersuai dan entiti
description: Topik ini menerangkan cara mencipta set pilihan dan entiti dalam penyelesaian anda sendiri dalam platform Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: c58745a46e84a40b90fbb3cbf89b10e293588fc3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290549"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="98415-103">Cipta medan tersuai dan entiti</span><span class="sxs-lookup"><span data-stu-id="98415-103">Create custom fields and entities</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="98415-104">Lengkapkan langkah-langkah berikut pada bila-bila masa anda mahu mencipta set pilihan atau entiti tersuai pada platform Power Apps.</span><span class="sxs-lookup"><span data-stu-id="98415-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="98415-105">Prosedur dalam topik ini hendaklah diselesaikan menggunakan antara muka web Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="98415-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="98415-106">Kami mengesyorkan agar anda membuat semua perubahan dimensi penentuan harga dalam penyelesaian berasingan.</span><span class="sxs-lookup"><span data-stu-id="98415-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="98415-107">Amalan terbaik penting ini memberikan kefleksibelan pada masa akan datang untuk mengemas kini atau mengalih keluar perubahan seperti yang diperlukan, akan membantu menggunakan semula kerja anda, dan memudahkan untuk port perubahan ini kepada tika lain.</span><span class="sxs-lookup"><span data-stu-id="98415-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="98415-108">Selepas anda membuat semua perubahan yang diperlukan, eksport penyelesaian ini sebagai **Penyelesaian terurus** dan import ini ke dalam tika lain untuk guna semula persediaan penentuan harga anda.</span><span class="sxs-lookup"><span data-stu-id="98415-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="98415-109">Cipta medan tersuai dan seti pilihan dalam penyelesaian dimensi penentuan harga</span><span class="sxs-lookup"><span data-stu-id="98415-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="98415-110">Dimensi penentuan harga boleh menjadi set pilihan atau entiti.</span><span class="sxs-lookup"><span data-stu-id="98415-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="98415-111">Kedua-duanya mesti dicipta dalam penyelesaian penentuan harga anda.</span><span class="sxs-lookup"><span data-stu-id="98415-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="98415-112">Langkah-langkah dalam prosedur ini menerangkan cara mencipta dimensi berasaskan entiti dan dimensi berasaskan set pilihan.</span><span class="sxs-lookup"><span data-stu-id="98415-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="98415-113">Dimensi berasaskan entiti</span><span class="sxs-lookup"><span data-stu-id="98415-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="98415-114">Dalam PSA, klik **Tetapan** > **Penyelesaian** dan kemudian klik dua kali dimensi penetapan harga **\<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="98415-114">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="98415-115">Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Entiti**.</span><span class="sxs-lookup"><span data-stu-id="98415-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="98415-116">Klik **Baharu** untuk mencipta entiti baharu dipanggil **Tajuk Standard**.</span><span class="sxs-lookup"><span data-stu-id="98415-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="98415-117">Masukkan baki maklumat diperlukan, kemudian klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="98415-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definisi entiti tajuk standard](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="98415-119">Dimensi berasaskan set pilihan</span><span class="sxs-lookup"><span data-stu-id="98415-119">Option set-based dimensions</span></span> 
<span data-ttu-id="98415-120">Anda boleh mencipta dua dimensi berasaskan set pilihan.</span><span class="sxs-lookup"><span data-stu-id="98415-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="98415-121">Guna **Lokasi Kerja Sumber** untuk menjejaki harga kerja lokasi **Rumah** dan kerja **Di Tapak** dan menggunakan **Jam Bekerja Sumber** dengan nilai **Biasa** dan **Lebih Masa** untuk mengenakan tokokan apabila kerja selesai.</span><span class="sxs-lookup"><span data-stu-id="98415-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="98415-122">Dalam PSA, klik **Tetapan** > **Penyelesaian** dan kemudian klik dua kali dimensi penetapan harga **\<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="98415-122">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="98415-123">Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Set Pilihan**.</span><span class="sxs-lookup"><span data-stu-id="98415-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="98415-124">Klik **Baharu** untuk mencipta set pilihan baharu, masukkan baki maklumat yang diperlukan, kemudian klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="98415-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="98415-125">Dimensi penentuan harga berasaskan set pilihan dipanggil Lokasi Kerja Sumber</span><span class="sxs-lookup"><span data-stu-id="98415-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="98415-126">Dimensi penentuan harga berasaskan set pilihan dipanggil Waktu Kerja Sumber</span><span class="sxs-lookup"><span data-stu-id="98415-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="98415-127">Cipta data untuk dimensi berasaskan entiti</span><span class="sxs-lookup"><span data-stu-id="98415-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="98415-128">Anda boleh mencipta data untuk dimensi berasaskan entiti secara manual, atau menggunakan panggilan import atau perkhidmatan Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="98415-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="98415-129">Guna langkah-langkah dalam prosedur ini untuk mencipta dua jawatan standard **Jurutera Sistem** dan **Jurutera Sistem Kanan** daripada dimensi berasaskan entiti, **Jawatan Standard**.</span><span class="sxs-lookup"><span data-stu-id="98415-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="98415-130">Jika data yang anda mahu cipta adalah kecil, seperti dalam contoh berikut, anda boleh menggunakan borang standard.</span><span class="sxs-lookup"><span data-stu-id="98415-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="98415-131">Dalam PSA, klik **Carian Lanjutan**.</span><span class="sxs-lookup"><span data-stu-id="98415-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="98415-132">Pilih entiti **Jawatan Standard** dan kemudian klik **Hasil**.</span><span class="sxs-lookup"><span data-stu-id="98415-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="98415-133">Semua baris dalam entiti **Jawatan Standard** akan ditunjukkan.</span><span class="sxs-lookup"><span data-stu-id="98415-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="98415-134">Klik **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="98415-134">Click **New**.</span></span> <span data-ttu-id="98415-135">Dalam medan **Nama**, masukkan "Jurutera Sistem" dan kemudian klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="98415-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="98415-136">Tutup borang.</span><span class="sxs-lookup"><span data-stu-id="98415-136">Close the form.</span></span> 
4. <span data-ttu-id="98415-137">Ulangi langkah 1 - 3 untuk mencipta jawatan lain untuk "Jurutera Sistem Kanan".</span><span class="sxs-lookup"><span data-stu-id="98415-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="98415-138">Data Sampel untuk entiti Jawatan Standard</span><span class="sxs-lookup"><span data-stu-id="98415-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]