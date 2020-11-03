---
title: Anggarkan jualan dan kos projek apabila sumber boleh ditempah mengisi berbilang peranan pada projek
description: Topik ini memberikan maklumat tentang cara dimensi penetapan harga yang boleh digunakan untuk menyokong penetapan harga dan kos bagi sumber yang memenuhi berbilang peranan pada projek.
author: rumant
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
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081280"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a><span data-ttu-id="e377b-103">Anggarkan jualan dan kos projek apabila sumber boleh ditempah mengisi berbilang peranan pada projek</span><span class="sxs-lookup"><span data-stu-id="e377b-103">Estimate project sales and costs when a bookable resource fills mulitple roles on a project</span></span> 

<span data-ttu-id="e377b-104">Syarikat berasaskan projek selalunya memerlukan satu sumber untuk melaksanakan berbilang peranan pada projek.</span><span class="sxs-lookup"><span data-stu-id="e377b-104">Project-based companies often have the need for one resource to perform mulitple roles on a project.</span></span> <span data-ttu-id="e377b-105">Setiap peranan ini mungkin berharga dan berkos berbeza yang bermaksud masa sumber yang sama pada projek boleh mendapatkan anggaran kewangan yang berbeza bergantung kepada kadar bil dan kos bagi setiap peranan.</span><span class="sxs-lookup"><span data-stu-id="e377b-105">Each of these roles could be priced and costed differently which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="e377b-106">Project Service Automation membolehkan penyediaan nilai pada rekod ahli pasukan untuk sumber yang bernama dan membolehkan untuk digantikan pada setiap tugas yang diberikan kepada ahli pasukan.</span><span class="sxs-lookup"><span data-stu-id="e377b-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="e377b-107">Contoh berikut menerangkan bagaimana penggantian mudah bagi nilai ini membenarkan sumber mempunyai berbilang peranan pada projek dengan kadar kos dan bil yang berbeza.</span><span class="sxs-lookup"><span data-stu-id="e377b-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="e377b-108">Cipta tugas</span><span class="sxs-lookup"><span data-stu-id="e377b-108">Create tasks</span></span>
<span data-ttu-id="e377b-109">Cipta dua tugas projek untuk 40 jam setiap satunya, Tugas A dan Tugas B. Pilih Tugas A sebagai yang terdahulu kepada Tugas B.</span><span class="sxs-lookup"><span data-stu-id="e377b-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="e377b-110">Sediakan Unit Peranan dan Organisasi untuk ahli pasukan projek generik</span><span class="sxs-lookup"><span data-stu-id="e377b-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="e377b-111">Pada halaman **Jadual** , pilih baris **Tugas** untuk Tugas A.</span><span class="sxs-lookup"><span data-stu-id="e377b-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="e377b-112">Dalam medan **Sumber** , pilih **Cipta** dalam senarai juntai bawah.</span><span class="sxs-lookup"><span data-stu-id="e377b-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="e377b-113">Pada halaman **Cipta Pantas Ahli Pasukan** , tentukan atribut ahli pasukan generik yang boleh melaksanakan tugas ini.</span><span class="sxs-lookup"><span data-stu-id="e377b-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="e377b-114">Pilih unit peranan dan organisasi yang sesuai dan kemudian pilih **Simpan dan Tutup**.</span><span class="sxs-lookup"><span data-stu-id="e377b-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="e377b-115">Ahli pasukan generik dicipta dan ditugaskan untuk tugas ini.</span><span class="sxs-lookup"><span data-stu-id="e377b-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="e377b-116">Ulangi langkah ini untuk Tugas B dan pastikan bahawa peranan dan unit organisasi pada ahli pasukan generik dicipta untuk Tugas B adalah berbeza daripada Tugas A.</span><span class="sxs-lookup"><span data-stu-id="e377b-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="e377b-117">Sediakan unit peranan dan organisasi untuk tugas projek</span><span class="sxs-lookup"><span data-stu-id="e377b-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="e377b-118">Selepas anda mencipta Tugas A, pilih tugas dan kemudian pilih **Edit tugas**.</span><span class="sxs-lookup"><span data-stu-id="e377b-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="e377b-119">Pada halaman **Butiran Tugas** , cari medan **Peranan** dan **Unit Organisasi** , tambah nilai yang memerlukan sumber yang akan melaksanakan tugas ini.</span><span class="sxs-lookup"><span data-stu-id="e377b-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="e377b-120">Jika anda melengkapkan senario ini menggunakan data demo Project Service Automation, pilih **Berunding dengan Bakal Pelanggan** untuk peranan dan **Fabrikam US** sebagai unit organisasi.</span><span class="sxs-lookup"><span data-stu-id="e377b-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="e377b-121">Pilih Tugas B dan kemudian pilih **Edit tugas**.</span><span class="sxs-lookup"><span data-stu-id="e377b-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="e377b-122">Pada halaman **Butiran Tugas** , cari medan **Peranan** dan **Unit Organisasi** , tambah nilai yang memerlukan sumber yang akan melaksanakan tugas ini.</span><span class="sxs-lookup"><span data-stu-id="e377b-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="e377b-123">Pastikan bahawa nilai dalam medan **Peranan** dan **Unit Organisasi** adalah berbeza untuk Tugas B daripada nilai untuk Tugas A.</span><span class="sxs-lookup"><span data-stu-id="e377b-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from those for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="e377b-124">Jika anda melengkapkan senario ini menggunakan data demo Project Service Automation, pilih **Juruteknik Rangkaian** untuk peranan dan **Fabrikam US** sebagai unit organisasi.</span><span class="sxs-lookup"><span data-stu-id="e377b-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="e377b-125">Simpan dan tutup halaman **Butiran Tugas**.</span><span class="sxs-lookup"><span data-stu-id="e377b-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behaviour"></a><span data-ttu-id="e377b-126">Ahli pasukan dan anggaran tingkah laku</span><span class="sxs-lookup"><span data-stu-id="e377b-126">Team member and estimates behaviour</span></span> 

1. <span data-ttu-id="e377b-127">Pada halaman **Butiran Tugas** , pada **Ahli Pasukan** , pilih dua ahli pasukan generik dan kemudian pilih **Jana Keperluan**.</span><span class="sxs-lookup"><span data-stu-id="e377b-127">On the **Task Details** page, on the **Team Member** , select the two generic team Members and then select **Generate Requirements**.</span></span> <span data-ttu-id="e377b-128">Ini akan menjana keperluan sumber.</span><span class="sxs-lookup"><span data-stu-id="e377b-128">This will generate resource requirements.</span></span> 
2. <span data-ttu-id="e377b-129">Pilih baris ahli pasukan untuk **Berunding dengan Bakal Pelanggan** dan kemudian pilih **Tempah**.</span><span class="sxs-lookup"><span data-stu-id="e377b-129">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="e377b-130">Papan jadual membuka dan menempah sumber mengikut keperluan tersebut.</span><span class="sxs-lookup"><span data-stu-id="e377b-130">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="e377b-131">Pilih baris ahli pasukan untuk **Juruteknik Rangkaian** dan kemudian pilih **Tempah**.</span><span class="sxs-lookup"><span data-stu-id="e377b-131">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="e377b-132">Papan jadual membuka dan menempah sumber yang sama mengikut keperluan tersebut.</span><span class="sxs-lookup"><span data-stu-id="e377b-132">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="e377b-133">Grid Ahli Pasukan</span><span class="sxs-lookup"><span data-stu-id="e377b-133">Team Member grid</span></span> 
<span data-ttu-id="e377b-134">Pada grid **Ahli Pasukan** , perhatikan bahawa kedua-dua rekod ahli pasukan generik telah dipadamkan dan telah digantikan dengan satu sumber.</span><span class="sxs-lookup"><span data-stu-id="e377b-134">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="e377b-135">Terdapat satu set nilai untuk sumber itu yang menunjukkan set nilai lalai untuk **Peranan** dan **Unit Organisasi**.</span><span class="sxs-lookup"><span data-stu-id="e377b-135">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="e377b-136">Apabila anda mengembangkan baris rekod Ahli Pasukan tersebut, anda boleh melihat tugasan berbeza pada rekod ahli pasukan bagi kedua-dua tugas tersebut.</span><span class="sxs-lookup"><span data-stu-id="e377b-136">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="e377b-137">Setiap baris tugasan mempunyai peranan yang khusus untuk **Peranan** dan **Unit Organisasi**.</span><span class="sxs-lookup"><span data-stu-id="e377b-137">Each assignment row has task specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="e377b-138">Grid anggaran</span><span class="sxs-lookup"><span data-stu-id="e377b-138">Estimates grid</span></span> 
<span data-ttu-id="e377b-139">Apabila anda menavigasi ke grid **Anggaran** , anda akan dapati bahawa kedua-dua tugasan untuk sumber yang sama berharga berbeza.</span><span class="sxs-lookup"><span data-stu-id="e377b-139">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="e377b-140">Tugasan untuk sumber pada Tugas A adalah berharga menggunakan nilai atribut **Peranan** bagi **Berunding dengan Bakal Pelanggan**.</span><span class="sxs-lookup"><span data-stu-id="e377b-140">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="e377b-141">Tugasan untuk sumber sama pada Tugas B adalah berharga menggunakan nilai atribut **Peranan** bagi **Juruteknik Rangkaian**.</span><span class="sxs-lookup"><span data-stu-id="e377b-141">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>





