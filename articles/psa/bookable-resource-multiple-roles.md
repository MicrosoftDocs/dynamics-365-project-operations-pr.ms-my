---
title: Anggarkan jualan dan kos projek apabila sumber boleh ditempah mengisi berbilang peranan untuk projek
description: Topik ini memberikan maklumat tentang cara dimensi penentuan harga boleh digunakan untuk menyokong penentuan harga dan kos untuk sumber yang mengisi berbilang peranan pada projek.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5b2b57f5268a92168952b6da5123886df70cd4e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013272"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a><span data-ttu-id="2b1a6-103">Anggarkan jualan dan kos projek apabila sumber boleh ditempah mengisi berbilang peranan untuk projek</span><span class="sxs-lookup"><span data-stu-id="2b1a6-103">Estimate project sales and costs when a bookable resource fills multiple roles for a project</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="2b1a6-104">Syarikat berasaskan projek selalunya mempunyai keperluan bagi satu sumber untuk melaksanakan berbilang peranan pada projek.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-104">Project-based companies often have the need for one resource to perform multiple roles on a project.</span></span> <span data-ttu-id="2b1a6-105">Setiap peranan ini mungkin berharga dan berkos berbeza, yang bermaksud masa sumber yang sama pada projek boleh mendapatkan anggaran kewangan yang berbeza bergantung kepada kadar bil dan kos bagi setiap peranan.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-105">Each of these roles could be priced and costed differently, which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="2b1a6-106">Project Service Automation membolehkan penyediaan nilai pada rekod ahli pasukan untuk sumber yang bernama dan membolehkan untuk digantikan pada setiap tugas yang diberikan kepada ahli pasukan.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="2b1a6-107">Contoh berikut menerangkan bagaimana penggantian mudah bagi nilai ini membenarkan sumber mempunyai berbilang peranan pada projek dengan kadar kos dan bil yang berbeza.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="2b1a6-108">Cipta tugas</span><span class="sxs-lookup"><span data-stu-id="2b1a6-108">Create tasks</span></span>
<span data-ttu-id="2b1a6-109">Cipta dua tugas projek untuk 40 jam setiap satunya, Tugas A dan Tugas B. Pilih Tugas A sebagai yang terdahulu kepada Tugas B.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="2b1a6-110">Sediakan Unit Peranan dan Organisasi untuk ahli pasukan projek generik</span><span class="sxs-lookup"><span data-stu-id="2b1a6-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="2b1a6-111">Pada halaman **Jadual**, pilih baris **Tugas** untuk Tugas A.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="2b1a6-112">Dalam medan **Sumber**, pilih **Cipta** dalam senarai juntai bawah.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="2b1a6-113">Pada halaman **Cipta Pantas Ahli Pasukan**, tentukan atribut ahli pasukan generik yang boleh melaksanakan tugas ini.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="2b1a6-114">Pilih unit peranan dan organisasi yang sesuai dan kemudian pilih **Simpan dan Tutup**.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="2b1a6-115">Ahli pasukan generik dicipta dan ditugaskan untuk tugas ini.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="2b1a6-116">Ulangi langkah ini untuk Tugas B dan pastikan bahawa peranan dan unit organisasi pada ahli pasukan generik dicipta untuk Tugas B adalah berbeza daripada Tugas A.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="2b1a6-117">Sediakan unit peranan dan organisasi untuk tugas projek</span><span class="sxs-lookup"><span data-stu-id="2b1a6-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="2b1a6-118">Selepas anda mencipta Tugas A, pilih tugas dan kemudian pilih **Edit tugas**.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="2b1a6-119">Pada halaman **Butiran Tugas**, cari medan **Peranan** dan **Unit Organisasi**, tambah nilai yang memerlukan sumber yang akan melaksanakan tugas ini.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="2b1a6-120">Jika anda melengkapkan senario ini menggunakan data demo Project Service Automation, pilih **Berunding dengan Bakal Pelanggan** untuk peranan dan **Fabrikam US** sebagai unit organisasi.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="2b1a6-121">Pilih Tugas B dan kemudian pilih **Edit tugas**.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="2b1a6-122">Pada halaman **Butiran Tugas**, cari medan **Peranan** dan **Unit Organisasi**, tambah nilai yang memerlukan sumber yang akan melaksanakan tugas ini.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="2b1a6-123">Pastikan bahawa nilai dalam medan **Peranan** dan **Unit Organisasi** adalah berbeza untuk Tugas B daripada nilai Tugas A.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from the values for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="2b1a6-124">Jika anda melengkapkan senario ini menggunakan data demo Project Service Automation, pilih **Juruteknik Rangkaian** untuk peranan dan **Fabrikam US** sebagai unit organisasi.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="2b1a6-125">Simpan dan tutup halaman **Butiran Tugas**.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behavior"></a><span data-ttu-id="2b1a6-126">Ahli pasukan dan anggaran tingkah laku</span><span class="sxs-lookup"><span data-stu-id="2b1a6-126">Team member and estimates behavior</span></span> 

1. <span data-ttu-id="2b1a6-127">Pada halaman **Butiran Tugas**, pada **Ahli Pasukan**, pilih dua ahli pasukan generik dan kemudian pilih **Jana Keperluan**.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-127">On the **Task Details** page, on the **Team Member**, select the two generic team Members and then select **Generate Requirements**.</span></span> 
2. <span data-ttu-id="2b1a6-128">Pilih baris ahli pasukan untuk **Berunding dengan Bakal Pelanggan** dan kemudian pilih **Tempah**.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-128">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="2b1a6-129">Papan jadual membuka dan menempah sumber mengikut keperluan tersebut.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-129">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="2b1a6-130">Pilih baris ahli pasukan untuk **Juruteknik Rangkaian** dan kemudian pilih **Tempah**.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-130">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="2b1a6-131">Papan jadual membuka dan menempah sumber yang sama mengikut keperluan tersebut.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-131">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="2b1a6-132">Grid Ahli Pasukan</span><span class="sxs-lookup"><span data-stu-id="2b1a6-132">Team Member grid</span></span> 
<span data-ttu-id="2b1a6-133">Pada grid **Ahli Pasukan**, perhatikan bahawa kedua-dua rekod ahli pasukan generik telah dipadamkan dan telah digantikan dengan satu sumber.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-133">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="2b1a6-134">Terdapat satu set nilai untuk sumber itu yang menunjukkan set nilai lalai untuk **Peranan** dan **Unit Organisasi**.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-134">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="2b1a6-135">Apabila anda mengembangkan baris rekod Ahli Pasukan tersebut, anda boleh melihat tugasan berbeza pada rekod ahli pasukan bagi kedua-dua tugas tersebut.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-135">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="2b1a6-136">Setiap baris penugasan mempunyai nilai khusus tugas untuk **Peranan** dan **Unit Organisasi**.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-136">Each assignment row has task-specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="2b1a6-137">Grid anggaran</span><span class="sxs-lookup"><span data-stu-id="2b1a6-137">Estimates grid</span></span> 
<span data-ttu-id="2b1a6-138">Apabila anda menavigasi ke grid **Anggaran**, anda akan dapati bahawa kedua-dua tugasan untuk sumber yang sama berharga berbeza.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-138">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="2b1a6-139">Tugasan untuk sumber pada Tugas A adalah berharga menggunakan nilai atribut **Peranan** bagi **Berunding dengan Bakal Pelanggan**.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-139">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="2b1a6-140">Tugasan untuk sumber sama pada Tugas B adalah berharga menggunakan nilai atribut **Peranan** bagi **Juruteknik Rangkaian**.</span><span class="sxs-lookup"><span data-stu-id="2b1a6-140">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]