---
title: Peningkatan pertimbangan untuk struktur pecahan kerja
description: Topik ini memberikan maklumat mengenai menaik taraf struktur pecahan kerja daripada Project Service Automation 2.x ke 3.x.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x
author: ruhercul
ms.assetid: 9e43d5b5-ca5d-41f5-9012-c48f8e3080f9
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9aa35dd8784bfa55737b0836e653afd0442b80c2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753942"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="45e41-103">Peningkatan pertimbangan untuk struktur pecahan kerja</span><span class="sxs-lookup"><span data-stu-id="45e41-103">Upgrade considerations for the work breakdown structure</span></span>
<span data-ttu-id="45e41-104">Topik ini memberikan maklumat mengenai menaik taraf struktur pecahan kerja daripada Project Service Automation 2.x ke 3.x.</span><span class="sxs-lookup"><span data-stu-id="45e41-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="45e41-105">Topik ini mentakrifkan keadaan sihat projek dalam Project Service Automation (PSA) yang diperlukan untuk naik taraf yang berjaya.</span><span class="sxs-lookup"><span data-stu-id="45e41-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="45e41-106">Terdapat juga maklumat mengenai syarat menyekat umum yang akan menyebabkan peningkatan untuk gagal.</span><span class="sxs-lookup"><span data-stu-id="45e41-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="45e41-107">Untuk mendapatkan maklumat lanjut tentang mentakrifkan tugas projek dan fungsi mereka dalam jadual projek, lihat [Jadual project](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="45e41-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="45e41-108">Entiti utama</span><span class="sxs-lookup"><span data-stu-id="45e41-108">Key entities</span></span>
<span data-ttu-id="45e41-109">Untuk struktur pecahan kerja yang tepat yang sudah dimuatkan dengan sumber, entiti berikut diperlukan:</span><span class="sxs-lookup"><span data-stu-id="45e41-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="45e41-110">Projek</span><span class="sxs-lookup"><span data-stu-id="45e41-110">Project</span></span>](../developer/entities/msdyn_project.md)
- [<span data-ttu-id="45e41-111">Pasukan Projek</span><span class="sxs-lookup"><span data-stu-id="45e41-111">Project Team</span></span>](../developer/entities/msdyn_projectteam.md)
- [<span data-ttu-id="45e41-112">Tugas Projek</span><span class="sxs-lookup"><span data-stu-id="45e41-112">Project Task</span></span>](../developer/entities/msdyn_projecttask.md)
- [<span data-ttu-id="45e41-113">Penugasan Sumber</span><span class="sxs-lookup"><span data-stu-id="45e41-113">Resource Assignments</span></span>](../developer/entities/msdyn_resourceassignment.md)
- [<span data-ttu-id="45e41-114">Kebergantungan Tugas Projek</span><span class="sxs-lookup"><span data-stu-id="45e41-114">Project Task Dependency</span></span>](../developer/entities/msdyn_projecttaskdependency.md)
- [<span data-ttu-id="45e41-115">Sumber Boleh Ditempah</span><span class="sxs-lookup"><span data-stu-id="45e41-115">Bookable Resources</span></span>](../developer/entities/bookableresource.md)

<span data-ttu-id="45e41-116">Untuk mentakrifkan struktur pecahan kerja sumber yang dimuatkan, anda mesti melengkapkan langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="45e41-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="45e41-117">Cipta projek baharu.</span><span class="sxs-lookup"><span data-stu-id="45e41-117">Create a new project.</span></span> <span data-ttu-id="45e41-118">Untuk maklumat lanjut mengenai cara untuk mencipta projek baharu, lihat [msdyn_project](../developer/entities/msdyn_project.md).</span><span class="sxs-lookup"><span data-stu-id="45e41-118">For more information about how to create a new project, see [msdyn_project](../developer/entities/msdyn_project.md).</span></span>
2. <span data-ttu-id="45e41-119">Cipta satu atau lebih tugas.</span><span class="sxs-lookup"><span data-stu-id="45e41-119">Create one or more tasks.</span></span> <span data-ttu-id="45e41-120">Untuk maklumat lanjut mengenai cara untuk mencipta tugasan baharu, lihat [msdyn_projecttask](../developer/entities/msdyn_projecttask.md).</span><span class="sxs-lookup"><span data-stu-id="45e41-120">For more information about how to create a task, see [msdyn_projecttask](../developer/entities/msdyn_projecttask.md).</span></span>
3. <span data-ttu-id="45e41-121">Takrifkan kebergantungan tugas.</span><span class="sxs-lookup"><span data-stu-id="45e41-121">Define the task dependencies.</span></span> <span data-ttu-id="45e41-122">Untuk mendapatkan maklumat lanjut, lihat [Kebergantungan Tugas Projek](../developer/entities/msdyn_projecttaskdependency.md).</span><span class="sxs-lookup"><span data-stu-id="45e41-122">For more information, see [Project Task Dependency](../developer/entities/msdyn_projecttaskdependency.md).</span></span>
4. <span data-ttu-id="45e41-123">Tugaskan ahli pasukan projek ke projek.</span><span class="sxs-lookup"><span data-stu-id="45e41-123">Assign project team members to the project.</span></span> <span data-ttu-id="45e41-124">Untuk mendapatkan maklumat lanjut, lihat [msdyn_projectteam](../developer/entities/msdyn_projectteam.md).</span><span class="sxs-lookup"><span data-stu-id="45e41-124">For more information, see [msdyn_projectteam](../developer/entities/msdyn_projectteam.md).</span></span>
5. <span data-ttu-id="45e41-125">Tugaskan ahli pasukan projek ke tugasan.</span><span class="sxs-lookup"><span data-stu-id="45e41-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="45e41-126">Untuk mendapatkan maklumat lanjut, lihat [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).</span><span class="sxs-lookup"><span data-stu-id="45e41-126">For more information, see [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="45e41-127">Perhubungan pasukan projek</span><span class="sxs-lookup"><span data-stu-id="45e41-127">Project team relationships</span></span>

<span data-ttu-id="45e41-128">Untuk memastikan peningkatan yang berjaya, perhubungan berikut mesti diselenggara dengan betul:</span><span class="sxs-lookup"><span data-stu-id="45e41-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="45e41-129">Semua ahli pasukan projek mesti dikaitkan dengan sumber boleh ditempah.</span><span class="sxs-lookup"><span data-stu-id="45e41-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="45e41-130">Semua ahli pasukan projek mesti dikaitkan dengan projek yang sama.</span><span class="sxs-lookup"><span data-stu-id="45e41-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="45e41-131">Perhubungan tugas projek</span><span class="sxs-lookup"><span data-stu-id="45e41-131">Project task relationships</span></span>
<span data-ttu-id="45e41-132">Untuk memastikan peningkatan yang berjaya, perhubungan berikut mesti diselenggara dengan betul:</span><span class="sxs-lookup"><span data-stu-id="45e41-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="45e41-133">Sebarang tugas berkaitan mesti dikaitkan dengan projek yang sama.</span><span class="sxs-lookup"><span data-stu-id="45e41-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="45e41-134">Setiap tugas baris mesti mempunyai tugas induk.</span><span class="sxs-lookup"><span data-stu-id="45e41-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="45e41-135">Setiap tugas baris mesti mempunyai tugas projek.</span><span class="sxs-lookup"><span data-stu-id="45e41-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="45e41-136">Syarat sah</span><span class="sxs-lookup"><span data-stu-id="45e41-136">Valid conditions</span></span>

- <span data-ttu-id="45e41-137">Semua tugas tempoh mesti lebih besar daripada atau sama dengan (>=) sejam dan kurang daripada 1,800,000 minit (1,250 hari).\*</span><span class="sxs-lookup"><span data-stu-id="45e41-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="45e41-138">Semua tugas mesti mempunyai tarikh mula tidak lebih awal daripada 01/01/2000.\*</span><span class="sxs-lookup"><span data-stu-id="45e41-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="45e41-139">Semua tugas mesti mempunyai tarikh mula tidak melebihi 17 tahun dari hari sekarang.\*</span><span class="sxs-lookup"><span data-stu-id="45e41-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="45e41-140">Semua tugas mesti mempunyai tarikh mula lebih awal atau sama dengan tarikh penamat mereka.</span><span class="sxs-lookup"><span data-stu-id="45e41-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="45e41-141">Semua jenis transaksi pada pengelasan (Perbelanjaan, Bahan, Cukai dan Masa) mesti mempunyai nilai untuk **Unit Lalai** dan **Kumpulan Unit**.</span><span class="sxs-lookup"><span data-stu-id="45e41-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="45e41-142">Format tarikh dengan huruf perlu dielakkan.</span><span class="sxs-lookup"><span data-stu-id="45e41-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="45e41-143">Langkah pengurangan berpotensi</span><span class="sxs-lookup"><span data-stu-id="45e41-143">Potential mitigation steps</span></span>
- <span data-ttu-id="45e41-144">Gunakan Carian Lanjutan untuk mengenal pasti tugas Projek yang tidak mengandungi ID Projek.</span><span class="sxs-lookup"><span data-stu-id="45e41-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="45e41-145">Gunakan Carian Lanjutan untuk mengenal pasti tugas Projek apabila tempoh dijadualkan lebih besar daripada > 1,800,000.</span><span class="sxs-lookup"><span data-stu-id="45e41-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="45e41-146">Sebelum membuat sebarang perubahan data, anda perlu menyiasat sebarang penyesuaian yang berkaitan dengan entiti yang mungkin telah menyebabkan data berada dalam keadaan buruk.</span><span class="sxs-lookup"><span data-stu-id="45e41-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="45e41-147">Penyesuaian ini perlu ditangani sebelum meneruskan dengan sebarang kemas kini berkaitan dengan data.</span><span class="sxs-lookup"><span data-stu-id="45e41-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="45e41-148">Untuk tugas yang dikenal pasti telah menjadi yatim, pertimbangkan untuk memadam tugas ini jika ia tidak diperlukan atau jika ia harus dikaitkan dengan projek induk yang betul.</span><span class="sxs-lookup"><span data-stu-id="45e41-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="45e41-149">Untuk sebarang tugas yang tempohnya adalah lebih besar daripada 1,250 hari, pertimbangkan menambah pelbagai tugas untuk mewakili jumlah tempoh, jika boleh dilaksanakan.</span><span class="sxs-lookup"><span data-stu-id="45e41-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="45e41-150">Item yang direkodkan dengan asterisk (\*) mempunyai had yang disebabkan oleh hakikat bahawa pengurusan perhubungan pelanggan (CRM) menyokong hanya 7,320 pengembangan yang berulang.</span><span class="sxs-lookup"><span data-stu-id="45e41-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="45e41-151">Anda mesti kekal di bawah had ini.</span><span class="sxs-lookup"><span data-stu-id="45e41-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="45e41-152">Perhubungan Tugasan Sumber</span><span class="sxs-lookup"><span data-stu-id="45e41-152">Resource Assignment relationships</span></span>
<span data-ttu-id="45e41-153">Untuk memastikan peningkatan yang berjaya, perhubungan berikut mesti diselenggara dengan betul:</span><span class="sxs-lookup"><span data-stu-id="45e41-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="45e41-154">Semua Tugasan Sumber dalam struktur pecahan kerja mesti mempunyai kaitan dengan projek yang sama.</span><span class="sxs-lookup"><span data-stu-id="45e41-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="45e41-155">Semua Tugasan Sumber dalam struktur pecahan kerja mesti mempunyai kaitan dengan ahli pasukan dalam projek yang sama.</span><span class="sxs-lookup"><span data-stu-id="45e41-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="45e41-156">Langkah pengurangan berpotensi</span><span class="sxs-lookup"><span data-stu-id="45e41-156">Potential mitigation steps</span></span>
- <span data-ttu-id="45e41-157">Kenal pasti semua tugas yang berada di luar keadaan yang diterangkan di atas.</span><span class="sxs-lookup"><span data-stu-id="45e41-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="45e41-158">Sebarang Tugasan Sumber yang tidak lagi sah perlu dipadamkan.</span><span class="sxs-lookup"><span data-stu-id="45e41-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="45e41-159">Perhubungan kebergantungan tugasan projek</span><span class="sxs-lookup"><span data-stu-id="45e41-159">Project task dependency relationships</span></span>
<span data-ttu-id="45e41-160">Untuk memastikan peningkatan yang berjaya, perhubungan berikut mesti diselenggara dengan betul:</span><span class="sxs-lookup"><span data-stu-id="45e41-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="45e41-161">Semua tugas projek kebergantungan mestilah berkaitan dengan projek yang sama.</span><span class="sxs-lookup"><span data-stu-id="45e41-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="45e41-162">Satu tugas tidak boleh mempunyai kebergantungan yang sama yang dirujuk lebih daripada sekali.</span><span class="sxs-lookup"><span data-stu-id="45e41-162">A task can't have the same dependency referenced more than once.</span></span>
