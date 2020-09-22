---
title: Tugaskan sumber kepada tugas
description: Topik ini memberikan maklumat tentang cara menugaskan sumber kepada tugas.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.prod: Project Service
ms.technology: Dynamics 365 Project Service Automation 3.x
ms.assetid: 3ea9516c-0276-4e30-b308-f792f64d608b
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 509f7a4464b2e810900b31a78219ba696192a18b
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754007"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="654a5-103">Tugaskan sumber kepada tugas</span><span class="sxs-lookup"><span data-stu-id="654a5-103">Assign a resource to a task</span></span>

<span data-ttu-id="654a5-104">Terdapat tiga cara untuk menugaskan sumber kepada tugas dalam Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="654a5-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="654a5-105">Tempah sumber sebagai ahli pasukan, kemudian tugaskan sumber kepada tugas</span><span class="sxs-lookup"><span data-stu-id="654a5-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="654a5-106">Anda boleh menambah sumber kepada pasukan projek, kemudian tugaskan sumber kepada tugas dalam jadual projek.</span><span class="sxs-lookup"><span data-stu-id="654a5-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="654a5-107">Pada tab **Ahli Pasukan**. tambah ahli pasukan baharu dengan memilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="654a5-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="654a5-108">Panel **Cipta Pantas Ahli Pasukan** dibuka, di mana anda boleh memilih nama sumber boleh ditempah dan menetapkan peranan.</span><span class="sxs-lookup"><span data-stu-id="654a5-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="654a5-109">Pilih salah satu daripada kaedah peruntukan berikut untuk tempahan sumber?</span><span class="sxs-lookup"><span data-stu-id="654a5-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="654a5-110">**Kapasiti Penuh** menempah kapasiti penuh sumber untuk tarikh dari dan sehingga yang dinyatakan.</span><span class="sxs-lookup"><span data-stu-id="654a5-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="654a5-111">**Kapasiti Peratusan** menempah sumber untuk peratusan kapasiti sumber bagi tarikh dari dan sehingga yang dinyatakan.</span><span class="sxs-lookup"><span data-stu-id="654a5-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="654a5-112">**Mengikut Jam Mengagih Sama Rata** menempah sumber untuk jumlah jam tertentu, mengagihkan masa tersebut secara sama rata setiap hari selama tempoh tarikh dari dan tarikh hingga khusus.</span><span class="sxs-lookup"><span data-stu-id="654a5-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="654a5-113">**Mengikut Jam Muatan Depan** menempah sumber untuk bilangan jam yang dinyatakan, memuatkan depan masa setiap hari selama tarikh dari dan sehingga.</span><span class="sxs-lookup"><span data-stu-id="654a5-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="654a5-114">**Tiada** menambah sumber kepada pasukan tetapi tidak mencipta sebarang tempahan yang menyerap kapasiti mereka.</span><span class="sxs-lookup"><span data-stu-id="654a5-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="654a5-115">Pada grid **Jadual** untuk tugas, pilih ikon **Sumber** dalam sel sumber, kemudian di bawah **Ahli Pasukan**, pilih ahli pasukan yang anda baharu tambah.</span><span class="sxs-lookup"><span data-stu-id="654a5-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members**, select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="654a5-116">Pada tab **Ahli Pasukan** dan **Penyesuaian**, sumber menunjukkan jam ditempah dan ditugaskan.</span><span class="sxs-lookup"><span data-stu-id="654a5-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="654a5-117">Jam hendaklah sama, tetapi tidak diperlukan memandangkan tempahan dan tugasan tidaklah terlalu bergandingan.</span><span class="sxs-lookup"><span data-stu-id="654a5-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="654a5-118">Tab **Penyesuaian** memberikan butiran kepada anda apabila ia berbeza, seperti apabila anda menugaskan sumber lebih jam berbanding yang anda telah tempah.</span><span class="sxs-lookup"><span data-stu-id="654a5-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="654a5-119">Jika perlu, anda boleh membetulkan maklumat dengan melanjutkan tempahan sumber atau menukar tugasan.</span><span class="sxs-lookup"><span data-stu-id="654a5-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="654a5-120">Cipta ahli pasukan generik melalui tugasan tugas</span><span class="sxs-lookup"><span data-stu-id="654a5-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="654a5-121">Apabila anda mencipta ahli pasukan generik melalui tugasan tugas, anda mencipta pemegang ruang atau sumber generik yang menggambarkan sifat sumber bernama yang anda mahu menguruskan tugas tersebut.</span><span class="sxs-lookup"><span data-stu-id="654a5-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="654a5-122">Kemudian, anda boleh menjana keperluan (atau menyerahkan permintaan menggunakan keperluan) yang digunakan untuk mencari dan menempah sumber bernama.</span><span class="sxs-lookup"><span data-stu-id="654a5-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="654a5-123">Pada grid **Jadual** untuk tugas, pilih ikon **Sumber** dalam sel sumber.</span><span class="sxs-lookup"><span data-stu-id="654a5-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="654a5-124">Taipkan nama untuk berfungsi sebagai nama sumber pemegang ruang.</span><span class="sxs-lookup"><span data-stu-id="654a5-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="654a5-125">Contohnya, Pengurus Program.</span><span class="sxs-lookup"><span data-stu-id="654a5-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="654a5-126">Pilih **Cipta**, dan dalam medan **Cipta Pantas Ahli Pasukan Projek**, tetapkan peranan untuk sumber generik.</span><span class="sxs-lookup"><span data-stu-id="654a5-126">Select **Create**, and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="654a5-127">Anda boleh teruskan menugaskan tugas kepada sumber pemegang ruang ini dengan memilih sumber pada **Pemilih Sumber** untuk tugas tersebut.</span><span class="sxs-lookup"><span data-stu-id="654a5-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="654a5-128">Ia tersenarai di bawah **Ahli Pasukan**.</span><span class="sxs-lookup"><span data-stu-id="654a5-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="654a5-129">Apabila anda selesai menugaskan sumber generik, pilih sumber generik pada tab **Pasukan**, kemudian pilih **Jana Keperluan** untuk mencipta keperluan sumber untuk sumber generik.</span><span class="sxs-lookup"><span data-stu-id="654a5-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="654a5-130">Pilih **Tempah** untuk sumber generik.</span><span class="sxs-lookup"><span data-stu-id="654a5-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="654a5-131">Kemudian, anda boleh menggunakan papan Jadual untuk mencari dan menempah sumber sebenar.</span><span class="sxs-lookup"><span data-stu-id="654a5-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="654a5-132">Anda juga boleh menghantar keperluan untuk pemenuhan oleh pengurus sumber.</span><span class="sxs-lookup"><span data-stu-id="654a5-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="654a5-133">Apabila sumber generik dipenuhkan dengan sumber dinamakan, sumber generik dialih keluar daripada pasukan dan tugasan tugas untuk sumber generik ditugaskan kepada sumber dinamakan yang telah memenuhi keperluan sumber bagi sumber generik.</span><span class="sxs-lookup"><span data-stu-id="654a5-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="654a5-134">Tugaskan sumber bernama dari senarai semua sumber boleh dtitempah</span><span class="sxs-lookup"><span data-stu-id="654a5-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="654a5-135">Anda boleh menggunakan kotak carian dalam **Pemilih Sumber** untuk mencari semua sumber boleh ditempah dan menugaskannya kepada tugas.</span><span class="sxs-lookup"><span data-stu-id="654a5-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="654a5-136">Sumber yang ditugaskan dengan cara ini ditambah kepada pasukan tanpa sebarang tempahan.</span><span class="sxs-lookup"><span data-stu-id="654a5-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="654a5-137">Ini serupa dengan menambah ahli pasukan dan memilih Tiada sebagai kaedah peruntukan.</span><span class="sxs-lookup"><span data-stu-id="654a5-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="654a5-138">Sumber dipaparkan dalam tab **Pasukan** dan **Penyesuaian** sebagai sumber yang mempunyai hanya tugasan dan defisit tempahan.</span><span class="sxs-lookup"><span data-stu-id="654a5-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="654a5-139">Tempah mereka jika anda ingin menggunakan ketersediaan mereka.</span><span class="sxs-lookup"><span data-stu-id="654a5-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="654a5-140">Pada grid **Jadual** untuk tugas, pilih ikon **Sumber** dalam sel sumber.</span><span class="sxs-lookup"><span data-stu-id="654a5-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="654a5-141">Mula menaip nama.</span><span class="sxs-lookup"><span data-stu-id="654a5-141">Start typing a name.</span></span> <span data-ttu-id="654a5-142">Hasil carian untuk nama dipaparkan dalam **Pemilih Sumber** di bawah **Sumber Lain**.</span><span class="sxs-lookup"><span data-stu-id="654a5-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="654a5-143">Pilih sumber yang anda mahu tugaskan kepada tugas.</span><span class="sxs-lookup"><span data-stu-id="654a5-143">Select the resource that you want to assign to the task.</span></span>

