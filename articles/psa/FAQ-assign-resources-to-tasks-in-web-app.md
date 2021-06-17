---
title: Bagaimanakah cara saya menugaskan sumber boleh ditempah kepada tugas dalam aplikasi web?
description: Satu gambaran keseluruhan cara anda boleh menugaskan sumber boleh ditempah.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 32a04ddef901515cd77262b5ae6be2458cb6b00c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993315"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="28cfb-103">Bagaimanakah saya menugaskan sumber boleh tempah kepada tugas dalam aplikasi web (aplikasi Project Service v2.x)?</span><span class="sxs-lookup"><span data-stu-id="28cfb-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="28cfb-104">Terdapat dua cara untuk menugaskan sumber kepada tugas dalam Project Service.</span><span class="sxs-lookup"><span data-stu-id="28cfb-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="28cfb-105">Anda boleh menempah sumber sebagai ahli pasukan dan kemudian menugaskannya kepada tugas</span><span class="sxs-lookup"><span data-stu-id="28cfb-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="28cfb-106">Atau anda boleh mencipta ahli pasukan generik melalui tugasan peranan pada tugas, menjana pasukan dan kemudian memnuhi keperluan sandaran dengan sumber yang dinamakan.</span><span class="sxs-lookup"><span data-stu-id="28cfb-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="28cfb-107">Perhatian bahawa jika anda ingin menugaskan sumber boleh tempah kepada tugas, ahli pasukan sumber boleh tempah mesti mempunyai tempahan tersedia yang secukupnya.</span><span class="sxs-lookup"><span data-stu-id="28cfb-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="28cfb-108">Status tempahan mesti Buku Keras Jenis Ikat dan Komited Status.</span><span class="sxs-lookup"><span data-stu-id="28cfb-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="28cfb-109">Jika tempahan tidak mencukupi untuk sumber, Project Service mengalih keluar tugasan dan memaparkan mesej ralat berikut:</span><span class="sxs-lookup"><span data-stu-id="28cfb-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="28cfb-110">*Tidak dapat menugaskan sumber ke tugas - Sumber berikut tidak mempunyai jam ditempah yang mencukupi terhadap projek*</span><span class="sxs-lookup"><span data-stu-id="28cfb-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="28cfb-111">Tempah sumber sebagai ahli pasukan dan kemudian tugaskan sumber kepada tugas</span><span class="sxs-lookup"><span data-stu-id="28cfb-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="28cfb-112">Dengan kaedah ini, anda menambah sumber kepada pasukan projek dan kemudian tugaskan tugas kepada sumber dalam jadual projek.</span><span class="sxs-lookup"><span data-stu-id="28cfb-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="28cfb-113">Berikut adalah cara untuk melakukan ini:</span><span class="sxs-lookup"><span data-stu-id="28cfb-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="28cfb-114">Pada grid ahli pasukan, tambah ahli pasukan baharu dengan memlih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="28cfb-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="28cfb-115">Pada skrin Cipta Pantas Ahli Pasukan, pilih nama sumber boleh tempah dan tetapkan peranan.</span><span class="sxs-lookup"><span data-stu-id="28cfb-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="28cfb-116">Pilih tarikh **Dari** dan **Sehingga**.</span><span class="sxs-lookup"><span data-stu-id="28cfb-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="28cfb-117">![Tangkapan skrin menambah ahli pasukan](media/FAQ-Resources-to-Tasks2-1.png "Tangkapan skrin menambah ahli pasukan")</span><span class="sxs-lookup"><span data-stu-id="28cfb-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="28cfb-118">Pilih satu daripada kaedah peruntukan berikut untuk tempahan sumber:</span><span class="sxs-lookup"><span data-stu-id="28cfb-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="28cfb-119">**Kapasiti Penuh** menempah kapasiti penuh sumber untuk tarikh dari dan sehingga yang dinyatakan.</span><span class="sxs-lookup"><span data-stu-id="28cfb-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="28cfb-120">**Kapasiti Peratusan** menempah sumber untuk peratusan kapasiti sumber bagi tarikh dari dan sehingga yang dinyatakan.</span><span class="sxs-lookup"><span data-stu-id="28cfb-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="28cfb-121">**Mengikut Jam Agihan Secara Rata** menempah sumber untuk bilangan jam yang dinyatakan, mengagihkan masa dengan sekata setiap hari selama tarikh dari dan sehingga.</span><span class="sxs-lookup"><span data-stu-id="28cfb-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="28cfb-122">**Mengikut Jam Muatan Depan** menempah sumber untuk bilangan jam yang dinyatakan, memuatkan depan masa setiap hari selama tarikh dari dan sehingga.</span><span class="sxs-lookup"><span data-stu-id="28cfb-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="28cfb-123">Jangan pilih **Tiada** kerana ia menambah sumber kepada pasukan tetapi tidak mencipta sebarang tempahan yang menyerap kapasiti sumber.</span><span class="sxs-lookup"><span data-stu-id="28cfb-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="28cfb-124">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="28cfb-124">Select **Save**.</span></span>

    <span data-ttu-id="28cfb-125">Perhatian bahawa jam tempahan mesti cukup untuk meliputi jam usaha dan julat tarikh tugas yang anda tugaskan kepada sumber.</span><span class="sxs-lookup"><span data-stu-id="28cfb-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="28cfb-126">Jika ia tidak sejajar, anda tidak boleh menugaskan sumber kepada tugas ini.</span><span class="sxs-lookup"><span data-stu-id="28cfb-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="28cfb-127">Pada struktir pecahan kerja (WBS) untuk tugas, klik sel ke bawah sumber.</span><span class="sxs-lookup"><span data-stu-id="28cfb-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="28cfb-128">Kemudian:</span><span class="sxs-lookup"><span data-stu-id="28cfb-128">Then:</span></span> 

    1. <span data-ttu-id="28cfb-129">Pilih **Tambah**.</span><span class="sxs-lookup"><span data-stu-id="28cfb-129">Select **Add**.</span></span>
    2. <span data-ttu-id="28cfb-130">Pilih ke bawah di bawah **Sumber** dan kemudian pilih ahli pasukan yang telah tambah di atas.</span><span class="sxs-lookup"><span data-stu-id="28cfb-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="28cfb-131">Pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="28cfb-131">Select **OK**.</span></span> <span data-ttu-id="28cfb-132">Ahli pasukan kini ditugaskan kepada kerja.</span><span class="sxs-lookup"><span data-stu-id="28cfb-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="28cfb-133">![Tangkapan skrin menambah sumber dengan WBS](media/FAQ-Resources-to-Tasks2-2.png "Tangkapan skrin menambah sumber dengan WBS")</span><span class="sxs-lookup"><span data-stu-id="28cfb-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="28cfb-134">Pada grid ahli pasukan, anda akan lihat agregat jam ditugaskan sumber di bawah Jam Ditugaskan.</span><span class="sxs-lookup"><span data-stu-id="28cfb-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="28cfb-135">Ia akan kurang daripada atau sama dengan jam ditempah untuk sumber.</span><span class="sxs-lookup"><span data-stu-id="28cfb-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="28cfb-136">![Tangkapan skrin masa yang ditugaskan untuk sumber](media/FAQ-Resources-to-Tasks2-3.png "Tangkapan skrin masa yang ditugaskan untuk sumber")</span><span class="sxs-lookup"><span data-stu-id="28cfb-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="28cfb-137">Jika tugas yang anda cuba untuk tugaskan kepada sumber bermula selepas tarikh akhir tempahan sumber, sumber tidak akan muncul dalam ke bawah.</span><span class="sxs-lookup"><span data-stu-id="28cfb-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="28cfb-138">Perhatian bahawa anda boleh menugaskans umber kepada lebih banyak jam berbanding jam ditempah mereka jika sumber mempunyai beberapa baki kapasiti tidak ditugaskan.</span><span class="sxs-lookup"><span data-stu-id="28cfb-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="28cfb-139">Dalam kes ini, sumber hanya akan ditugaskan sebahagian kepada tempahan mereka.</span><span class="sxs-lookup"><span data-stu-id="28cfb-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="28cfb-140">Anda boleh lihat baki jam tugas tidak ditugaskan dengan menambah Jam Tidak Bertugas kepada struktur pecahan kerja.</span><span class="sxs-lookup"><span data-stu-id="28cfb-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="28cfb-141">Jika sumber ditugaskan kepada jam ditempah mereka (jam ditempah mereka sama dengan jam ditugaskan mereka), anda akan nampak mesej ralat berikut semasa anda mencuba untuk menugaskan mereka tugas seterusnya:</span><span class="sxs-lookup"><span data-stu-id="28cfb-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="28cfb-142">*Tidak dapat menugaskan sumber ke tugas - Sumber berikut tidak mempunyai jam ditempah yang mencukupi terhadap projek.*</span><span class="sxs-lookup"><span data-stu-id="28cfb-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="28cfb-143">Tambahan, ahli pasukan projek lalai yang ditambah ke pasukan semasa anda mencipta projek ditambah tanpa sebarang tempahan dan tidak boleh ditugaskan kepada mana-mana tugas.</span><span class="sxs-lookup"><span data-stu-id="28cfb-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="28cfb-144">Ia tidak akan muncul dalam ke bawah sumber untuk tugas.</span><span class="sxs-lookup"><span data-stu-id="28cfb-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="28cfb-145">Jika anda ingin menugaskan sumber ini, anda perlu mengalih keluar mereka daripada pasukan dan kemudian tambah semula mereka dengan kaedah peruntukan selain daripada Tiada.</span><span class="sxs-lookup"><span data-stu-id="28cfb-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="28cfb-146">Sebab mereka ditambah ke pasukan di mana projek dicipta adalah supaya projek mempunyai sekurang-kurangnya satu pelulus projek secara lalai.</span><span class="sxs-lookup"><span data-stu-id="28cfb-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="28cfb-147">Cipta ahli pasukan generik melalui tugasan peranan pada tugas</span><span class="sxs-lookup"><span data-stu-id="28cfb-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="28cfb-148">Kaedah ini memastikan bahawa sumber mempunyai tempahan yang mencukupi untuk tugas.</span><span class="sxs-lookup"><span data-stu-id="28cfb-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="28cfb-149">Pertama sekali, anda mencipta tempat atau sumber generik yang menerangkan perwatakan sumber yang dinamakan sehingga akhirnya anda ingin mengerjakan tugas dengan menjana pasukan selepas menugaskan peranan ke tugas.</span><span class="sxs-lookup"><span data-stu-id="28cfb-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="28cfb-150">Berikut adalah cara untuk melakukan ini:</span><span class="sxs-lookup"><span data-stu-id="28cfb-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="28cfb-151">Pada struktur pecahan kerja, pilih tugas.</span><span class="sxs-lookup"><span data-stu-id="28cfb-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="28cfb-152">Pilih ikon ke bawah **Peranan Ditugaskan** dalam sel sumber.</span><span class="sxs-lookup"><span data-stu-id="28cfb-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="28cfb-153">Pilih ke bawah **Peranan** dan pilih peranan untuk sumber generik.</span><span class="sxs-lookup"><span data-stu-id="28cfb-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="28cfb-154">Pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="28cfb-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="28cfb-155">![Tangkapan skrin menggunakan WBS untuk menambah sumber](media/FAQ-Resources-to-Tasks2-4.png "Tangkapan skrin menggunakan WBS untuk menambah sumber")</span><span class="sxs-lookup"><span data-stu-id="28cfb-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="28cfb-156">Sebaik sahaja anda telah selesai menugaskan peranan kepada tugas dalam WBS, pilih **Jana Pasukan Projek**.</span><span class="sxs-lookup"><span data-stu-id="28cfb-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="28cfb-157">Project Service mencipta bilangan minimum ahli pasukan generik berdasarkan pada peranan, sumber unit organisasi dan kalendar projek dengan mengagregat tugasan tugas.</span><span class="sxs-lookup"><span data-stu-id="28cfb-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="28cfb-158">![Tangkapan skrin menjana pasukan projek](media/FAQ-Resources-to-Tasks2-5.png "Tangkapan skrin menjana pasukan projek")</span><span class="sxs-lookup"><span data-stu-id="28cfb-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="28cfb-159">Pada grid Ahli Pasukan, anda akan lihat sumber jenis Sumber Generik dengan nama peranan dan jawatan.</span><span class="sxs-lookup"><span data-stu-id="28cfb-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="28cfb-160">Jika dua sumber diperlukan untuk peranan melengkapkan kerja, ciri Jana Pasukan mencipta dua ahli pasukan dan menggunakan nama jawatan untuk membezakannya.</span><span class="sxs-lookup"><span data-stu-id="28cfb-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="28cfb-161">![Tangkapan skrin menambah dua sumber generik](media/FAQ-Resources-to-Tasks2-6.png "Tangkapan skrin menambah dua sumber generik")</span><span class="sxs-lookup"><span data-stu-id="28cfb-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="28cfb-162">Anda boleh membuka keperluan sumber sandaran untuk ahli pasukan generik dengan memilih pautan di bawah Keperluan sumber.</span><span class="sxs-lookup"><span data-stu-id="28cfb-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="28cfb-163">![Tangkapan skrin membuka keperluan sumber sokongan](media/FAQ-Resources-to-Tasks2-7.png "Tangkapan skrin membuka keperluan sumber sokongan")</span><span class="sxs-lookup"><span data-stu-id="28cfb-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="28cfb-164">Pilih **Tempah** untuk sumber generik, dan kemudian anda boleh menggunakan papan jadual untuk mencari dan menempah sumber sebenar.</span><span class="sxs-lookup"><span data-stu-id="28cfb-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="28cfb-165">Anda juga boleh menghantar keperluan untuk pemenuhan oleh pengurus sumber dengan memilih **Serah Permintaan**.</span><span class="sxs-lookup"><span data-stu-id="28cfb-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="28cfb-166">Apabila sumber generik dipenuhkan dengan sumber dinamakan, sumber generik dialih keluar daripada pasukan dan tugasan tugas untuk sumber generik ditugaskan kepada sumber dinamakan yang telah memenuhi keperluan sumber bagi sumber generik.</span><span class="sxs-lookup"><span data-stu-id="28cfb-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]