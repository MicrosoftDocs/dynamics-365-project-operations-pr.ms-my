---
title: Tempah sumber boleh ditempah dinamakan untuk pasukan projek dan menugaskan tugasan
description: Topik ini memberikan maklumat tentang tempahan sumber dinamakan kepada pasukan projek dan menugaskannya kepada tugasan.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: e947986a-e83a-42f4-813e-c82bdfbec33c
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 079ba299f912c75f9ed739d4b6aa3c63189d11d0
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753858"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="02f46-103">Tempah sumber boleh ditempah dinamakan untuk pasukan projek dan menugaskan tugasan</span><span class="sxs-lookup"><span data-stu-id="02f46-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="02f46-104">Anda boleh menambahkan sumber yang dinamakan kepada pasukan projek anda dengan menempahnya secara langsung kepada pasukan.</span><span class="sxs-lookup"><span data-stu-id="02f46-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="02f46-105">Untuk melakukan ini, lengkapkan langkah-langkah berikut.</span><span class="sxs-lookup"><span data-stu-id="02f46-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="02f46-106">Dalam Project Service Automation, pergi ke **Projek**dan pilih buka projek yang anda tempah.</span><span class="sxs-lookup"><span data-stu-id="02f46-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="02f46-107">Pada halaman **Projek**, pada tab **Pasuka**, klik **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="02f46-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Menambah ahli pasukan daripada tab pasukan](media/RM-how-to-1.png)

3. <span data-ttu-id="02f46-109">Dalam kotak dialog **Ahli Pasukan Projek Cipta Pantas**, pilih sumber boleh ditempah.</span><span class="sxs-lookup"><span data-stu-id="02f46-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="02f46-110">Medan **Peranan** akan mengisi peranan lalai sumber jika mereka mempunyai satu yang ditugaskan.</span><span class="sxs-lookup"><span data-stu-id="02f46-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="02f46-111">Anda boleh mengubahnya peranan jika perlu.</span><span class="sxs-lookup"><span data-stu-id="02f46-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="02f46-112">Pilih tarikh dari dan hingga yang sumber akan perlu dan pilih kaedah peruntukan bagi kapasiti sumber.</span><span class="sxs-lookup"><span data-stu-id="02f46-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="02f46-113">Jika anda mahu ahli pasukan untuk menjadi pelulus projek, pilih **Ya** dalam medan **Pelulus Projek**.</span><span class="sxs-lookup"><span data-stu-id="02f46-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="02f46-114">Ini bermakna ahli pasukan boleh meluluskan entri masa dan perbelanjaan yang diserahkan untuk projek ini.</span><span class="sxs-lookup"><span data-stu-id="02f46-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="02f46-115">Klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="02f46-115">Click **Save**.</span></span>

![Menambah ahli pasukan pada borang cipta cepat](media/RM-how-to-2.png)


<span data-ttu-id="02f46-117">Anda kini boleh menugaskan sumber boleh ditempah kepada tugasan pada projek.</span><span class="sxs-lookup"><span data-stu-id="02f46-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="02f46-118">Pada halaman **Projek**, klik tab **Jadual** untuk menugaskan tugasan ke sumber baharu.</span><span class="sxs-lookup"><span data-stu-id="02f46-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="02f46-119">Pemilih sumber yang dilancarkan daripada medan **Sumber** dalam grid tugas akan menunjukkan ahli pasukan yang anda boleh pilih.</span><span class="sxs-lookup"><span data-stu-id="02f46-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Menugaskan ahli pasukan kepada tugas pada tab jadual](media/RM-how-to-3.png)

<span data-ttu-id="02f46-121">Dalam versi 3 untuk Project Service Automation (PSA), tempahan sumber dan tugasan tugas tidak disertakan dengan ketat.</span><span class="sxs-lookup"><span data-stu-id="02f46-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="02f46-122">Ini bermaksud apabila anda menggunakan pemilih sumber dalam jadual, anda boleh menugaskan tugas kepada ahli pasukan untuk lebih masa lebih daripada liputan penempahan mereka pada projek.</span><span class="sxs-lookup"><span data-stu-id="02f46-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="02f46-123">Anda boleh melihat perbezaan antara tempahan ahli pasukan dan tugasan pada tab **Pasukan** atau tab **Penyelarasan Sumber**. Anda juga boleh menyelaraskan perbezaan antara penempahan dan tugasan untuk sumber pada tahap yang lebih terperinci.</span><span class="sxs-lookup"><span data-stu-id="02f46-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Tab penyelarasan sumber](media/RM-how-to-4.png)

<span data-ttu-id="02f46-125">Anda juga boleh menggunakan pemilih sumber pada tab **Jadual** untuk mencari dan memilih sumber boleh ditempah yang bukan sudah sebahagian daripada pasukan projek.</span><span class="sxs-lookup"><span data-stu-id="02f46-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="02f46-126">Ini ditunjukkan dalam pemilih sumber sebagai **Sumber Lain**.</span><span class="sxs-lookup"><span data-stu-id="02f46-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Memperuntukkan sumber ahli bukan pasukan kepada tugas](media/RM-how-to-5.png)

<span data-ttu-id="02f46-128">Apabila anda lakukan ini, sumber ditambah kepada pasukan projek dan ditugaskan kepada tugas, tetapi tiada tempahan yang dijana.</span><span class="sxs-lookup"><span data-stu-id="02f46-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Ahli pasukan dengan tugasan dan tiada tempahan](media/RM-how-to-6.png)

<span data-ttu-id="02f46-130">Anda boleh menggunakan keupayaan tempahan lanjutan tab **Penyelarasan** atau **Papan Jadual** untuk menempah kapasiti sumber untuk projek.</span><span class="sxs-lookup"><span data-stu-id="02f46-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Memperluas penempahan untuk ahli pasukan pada tab penyelarasan sumber](media/RM-how-to-7.png)

<span data-ttu-id="02f46-132">Selepas ahli pasukan ditempah dalam projek anda, anda boleh menggunakan tempahan mengekalkan atau menggunakan Papan Jadual secara langsung untuk menguruskan tempahan mereka.</span><span class="sxs-lookup"><span data-stu-id="02f46-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>
