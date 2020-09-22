---
title: Cipta tempahan projek daripada papan Jadual
description: Topik ini memberikan maklumat tentang cara mencipta tempahan projek daripada papan jadual.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.prod: Dynamics 365 Project Service Automation 2.x and 3.x
ms.technology: ''
ms.assetid: bbc1bbe2-3482-4b84-9e89-f7e0e585ade8
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 7b6c7e07ea6451e0654ccf1ba7be10e7b38e0d09
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753965"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="e31d3-103">Cipta tempahan projek daripada papan Jadual</span><span class="sxs-lookup"><span data-stu-id="e31d3-103">Create a project booking from the Schedule board</span></span>

<span data-ttu-id="e31d3-104">Anda boleh menempah sumber ke dalam projek secara terus dari tab **Pasukan** projek atau dengan menjana keperluan sumber daripada tugasan ahli pasukan generik dan kemudian mengisi keperluan yang dijana dengan ahli pasukan projek.</span><span class="sxs-lookup"><span data-stu-id="e31d3-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="e31d3-105">Anda juga boleh menempah sumber ke dalam projek secara terus dari papan Jadual.</span><span class="sxs-lookup"><span data-stu-id="e31d3-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="e31d3-106">Terdapat tiga cara untuk melakukan ini:</span><span class="sxs-lookup"><span data-stu-id="e31d3-106">There are three ways to do this:</span></span>

- <span data-ttu-id="e31d3-107">**Tempah dari keperluan sumber yang dijana:** Anda boleh menjana keperluan sumber selepas anda mencipta sumber generik dan menugaskan tugas dalam projek.</span><span class="sxs-lookup"><span data-stu-id="e31d3-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="e31d3-108">**Tempah daripada keperluan utama:** Keperluan utama muncul pada papan Jadual pada tab **Projek**.</span><span class="sxs-lookup"><span data-stu-id="e31d3-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="e31d3-109">**Tempah dari keperluan sumber baharu:** Anda boleh mencipta keperluan sumber dari awal dan mengaitkannya dengan projek.</span><span class="sxs-lookup"><span data-stu-id="e31d3-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="e31d3-110">Buka papan Jadual, keperluan sumber muncul pada tab **Buka Keperluan**.</span><span class="sxs-lookup"><span data-stu-id="e31d3-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="e31d3-111">Tempah daripada keperluan sumber yang dijana.</span><span class="sxs-lookup"><span data-stu-id="e31d3-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="e31d3-112">Anda boleh mencipta sumber generik dan menugaskannya satu atau lebih tugas dalam projek.</span><span class="sxs-lookup"><span data-stu-id="e31d3-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="e31d3-113">Kemudian anda boleh menjana keperluan sumber daripada ahli pasukan generik.</span><span class="sxs-lookup"><span data-stu-id="e31d3-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="e31d3-114">Pada papan Jadual, sumber ini akan muncul pada tab **Keperluan Terbuka**. Anda mungkin perlu menggunakan penapis lajur pada grid jika anda ada banya keperluan terbuka.</span><span class="sxs-lookup"><span data-stu-id="e31d3-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="e31d3-115">![Buka tab Keperluan pada papan Jsadual](media/FAQ-Project-Booking-Schedule-Board-1.png "Tangkap layar jadual tempahan dan tugasan")</span><span class="sxs-lookup"><span data-stu-id="e31d3-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="e31d3-116">Pilih keperluan.</span><span class="sxs-lookup"><span data-stu-id="e31d3-116">Select the requirement.</span></span> <span data-ttu-id="e31d3-117">Tab **Cari Ketersediaan** akan muncul di bahagian atas baris dipilih.</span><span class="sxs-lookup"><span data-stu-id="e31d3-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="e31d3-118">Apabila anda memilih tab, mod Pembantu Jadual bagi papan Jadual dibuka dan kemudian menapis sumber tersedia yang memenuhi keperluan sumber.</span><span class="sxs-lookup"><span data-stu-id="e31d3-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="e31d3-119">Selepas itu, anda boleh menempah sumber.</span><span class="sxs-lookup"><span data-stu-id="e31d3-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="e31d3-120">Anda juga boleh heret dan jatuhkan baris terpilih dari bawah papan Jadual pada sel sumber dalam grid di atas.</span><span class="sxs-lookup"><span data-stu-id="e31d3-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="e31d3-121">Apabila anda lepaskannya, ia membuka panel **Cipta Tempahan Sumber** di sebelah kanan.</span><span class="sxs-lookup"><span data-stu-id="e31d3-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="e31d3-122">Memilih **Tempah** menempah sumber ke dalam pasukan projek.</span><span class="sxs-lookup"><span data-stu-id="e31d3-122">Selecting **Book** books the resource onto the project team.</span></span>

![Cipta panel Tempahan Sumber](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="e31d3-124">Tempah dari Keperluan Utama</span><span class="sxs-lookup"><span data-stu-id="e31d3-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="e31d3-125">Mencipta projek dalam Project Service secara automatik mencipta keperluan sumber yang dipanggil Keperluan Utama.</span><span class="sxs-lookup"><span data-stu-id="e31d3-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="e31d3-126">Ini adalah keperluan kosong yang digunakan untuk menempah sumber dengan cepat menggunakan papan Jadual tanpa menjana keperluan atau mencipta dari awal.</span><span class="sxs-lookup"><span data-stu-id="e31d3-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="e31d3-127">Disebabkan keperluan kosong, anda perlu menyatakan tarikh serta kaedah peruntukan dan jam, jika berkenaan.</span><span class="sxs-lookup"><span data-stu-id="e31d3-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="e31d3-128">Untuk menempah sumber dengan Keperluan Utama, pada papan Jadual, pilih tab **Projek**. Anda mungkin perlu menggunakan penapis lajur ke atas lajur **Projek** jika anda ada banyak projek.</span><span class="sxs-lookup"><span data-stu-id="e31d3-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="e31d3-129">![Penapis lajur pada papan Jadual](media/FAQ-Project-Booking-Schedule-Board-2.png "Tangkap layar jadual tempahan dan tugasan")</span><span class="sxs-lookup"><span data-stu-id="e31d3-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="e31d3-130">Pilih keperluan yang hanya mempunyai nama projek sebagai namanya dan mempunyai tempoh sifar (0).</span><span class="sxs-lookup"><span data-stu-id="e31d3-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="e31d3-131">Pilih tab **Cari Ketersediaan** yang muncul pada baris.</span><span class="sxs-lookup"><span data-stu-id="e31d3-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="e31d3-132">Anda juga boleh heret dan jatuhkan baris terpilih dari bawah papan Jadual pada sel sumber dalam grid di atas.</span><span class="sxs-lookup"><span data-stu-id="e31d3-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="e31d3-133">Disebabkan **Keperluan Utama** adalah keperluan kosong dengan tempoh sifar (0), anda perlu menetapkan tempoh pada panel **Cipta Tempahan Sumber** apabila memilih dan menempah sumber.</span><span class="sxs-lookup"><span data-stu-id="e31d3-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="e31d3-134">Anda juga boleh memilih **Keperluan Utama Projek** di bahagian bawah papan Jadual dan seret dan jatuhkannya pada sumber untuk menempahnya.</span><span class="sxs-lookup"><span data-stu-id="e31d3-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="e31d3-135">Disebabkan **Keperluan Utama** adalah keperluan kosong yang mempunyai tempoh sifar (0), anda perlu menetapkan tempoh pada panel **Cipta Tempahan Sumber** apabila anda memilih dan menempah sumber.</span><span class="sxs-lookup"><span data-stu-id="e31d3-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="e31d3-136">Apabila anda menempah sumber melalui **Keperluan Utama** pada papan Jadual, anda menambahnya kepada pasukan projek tanpa sebarang tugasan.</span><span class="sxs-lookup"><span data-stu-id="e31d3-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="e31d3-137">Tempah daripada keperluan sumber baharu.</span><span class="sxs-lookup"><span data-stu-id="e31d3-137">Book from a new resource requirement</span></span>
<span data-ttu-id="e31d3-138">Lengkapkan langkah-langkah berikut untuk menempah daripada keperluan sumber baharu.</span><span class="sxs-lookup"><span data-stu-id="e31d3-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="e31d3-139">Pergi ke **Keperluan Sumber**, kemudian pilih **Baharu** untuk mencipta keperluan sumber baharu.</span><span class="sxs-lookup"><span data-stu-id="e31d3-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="e31d3-140">Pada tab **Projek**, pilih projek untuk mengaitkan keperluan dengan projek.</span><span class="sxs-lookup"><span data-stu-id="e31d3-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="e31d3-141">Pada papan Jadual, keperluan baharu ini ditunjukkan sebagai **Keperluan Terbuka** yang anda boleh isi.</span><span class="sxs-lookup"><span data-stu-id="e31d3-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="e31d3-142">Tempah sumber untuk menambahnya pada pasukan projek.</span><span class="sxs-lookup"><span data-stu-id="e31d3-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="e31d3-143">Setelah sumber ditempah, anda mesti menugaskan tugas secara manual.</span><span class="sxs-lookup"><span data-stu-id="e31d3-143">Now that the resource is booked, you must assign tasks manually.</span></span>

