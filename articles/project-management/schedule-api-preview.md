---
title: Gunakan API jadual untuk melaksanakan operasi dengan entiti Penjadualan
description: Topik ini menyediakan maklumat dan sampel untuk menggunakan API Jadual.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868140"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="d45b9-103">Gunakan API jadual untuk melaksanakan operasi dengan entiti Penjadualan</span><span class="sxs-lookup"><span data-stu-id="d45b9-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="d45b9-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="d45b9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="d45b9-105">Sesetengah atau semua kefungsian yang dinyatakan dalam topik ini tersedia sebagai sebahagian daripada keluaran pratonton.</span><span class="sxs-lookup"><span data-stu-id="d45b9-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="d45b9-106">Kandungan dan fungsi adalah tertakluk kepada perubahan.</span><span class="sxs-lookup"><span data-stu-id="d45b9-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="d45b9-107">Entiti penjadualan</span><span class="sxs-lookup"><span data-stu-id="d45b9-107">Scheduling entities</span></span>

<span data-ttu-id="d45b9-108">Api Jadual menyediakan keupayaan untuk melaksanakan operasi mencipta, mengemas kini dan memadam dengan **Entiti penjadualan**.</span><span class="sxs-lookup"><span data-stu-id="d45b9-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="d45b9-109">Entiti ini diuruskan melalui enjin Penjadualan dalam Projek untuk web.</span><span class="sxs-lookup"><span data-stu-id="d45b9-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="d45b9-110">Operasi mencipta, mengemas kini dan memadam dengan **Entiti penjadualan** telah dihadkan dalam keluaran Dynamics 365 Project Operations sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="d45b9-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="d45b9-111">Jadual berikut menyediakan senarai lengkap **Entiti penjadualan**.</span><span class="sxs-lookup"><span data-stu-id="d45b9-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="d45b9-112">Nama entiti</span><span class="sxs-lookup"><span data-stu-id="d45b9-112">Entity name</span></span>  | <span data-ttu-id="d45b9-113">Nama logik entiti</span><span class="sxs-lookup"><span data-stu-id="d45b9-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="d45b9-114">Project</span><span class="sxs-lookup"><span data-stu-id="d45b9-114">Project</span></span> | <span data-ttu-id="d45b9-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="d45b9-115">msdyn_project</span></span> |
| <span data-ttu-id="d45b9-116">Tugas Projek</span><span class="sxs-lookup"><span data-stu-id="d45b9-116">Project Task</span></span>  | <span data-ttu-id="d45b9-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="d45b9-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="d45b9-118">Kebergantungan Tugas Projek</span><span class="sxs-lookup"><span data-stu-id="d45b9-118">Project Task Dependency</span></span>  | <span data-ttu-id="d45b9-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="d45b9-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="d45b9-120">Tugasan Sumber</span><span class="sxs-lookup"><span data-stu-id="d45b9-120">Resource Assignment</span></span> | <span data-ttu-id="d45b9-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="d45b9-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="d45b9-122">Baldi Projek</span><span class="sxs-lookup"><span data-stu-id="d45b9-122">Project Bucket</span></span>  | <span data-ttu-id="d45b9-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="d45b9-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="d45b9-124">Ahli Pasukan Projek</span><span class="sxs-lookup"><span data-stu-id="d45b9-124">Project Team Member</span></span> | <span data-ttu-id="d45b9-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="d45b9-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="d45b9-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="d45b9-126">OperationSet</span></span>

<span data-ttu-id="d45b9-127">OperationSet ialah corak unit kerja yang boleh digunakan apabila beberapa jadual yang mempengaruhi permintaan mesti diproses dalam transaksi.</span><span class="sxs-lookup"><span data-stu-id="d45b9-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="d45b9-128">API Jadual</span><span class="sxs-lookup"><span data-stu-id="d45b9-128">Schedule APIs</span></span>

<span data-ttu-id="d45b9-129">Berikut ialah senarai API Jadual semasa.</span><span class="sxs-lookup"><span data-stu-id="d45b9-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="d45b9-130">**msdyn_CreateProjectV1**: API ini boleh digunakan untuk mencipta projek.</span><span class="sxs-lookup"><span data-stu-id="d45b9-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="d45b9-131">Projek dan baldi projek lalai dicipta dengan serta-merta.</span><span class="sxs-lookup"><span data-stu-id="d45b9-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="d45b9-132">**msdyn_CreateTeamMemberV1**: API ini boleh digunakan untuk mencipta ahli pasukan projek.</span><span class="sxs-lookup"><span data-stu-id="d45b9-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="d45b9-133">Rekod ahli pasukan dicipta dengan serta-merta.</span><span class="sxs-lookup"><span data-stu-id="d45b9-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="d45b9-134">**msdyn_CreateOperationSetV1**: API ini boleh digunakan untuk menjadualkan beberapa permintaan yang mesti dilaksanakan dalam transaksi.</span><span class="sxs-lookup"><span data-stu-id="d45b9-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="d45b9-135">**msdyn_PSSCreateV1**: API ini boleh digunakan untuk mencipta entiti.</span><span class="sxs-lookup"><span data-stu-id="d45b9-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="d45b9-136">Entiti boleh jadi sebarang entiti Penjadualan yang menyokong penciptaan operasi.</span><span class="sxs-lookup"><span data-stu-id="d45b9-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="d45b9-137">**msdyn_PSSUpdateV1**: API ini boleh digunakan untuk mengemas kini entiti.</span><span class="sxs-lookup"><span data-stu-id="d45b9-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="d45b9-138">Entiti boleh jadi sebarang entiti Penjadualan yang menyokong kemas kini operasi.</span><span class="sxs-lookup"><span data-stu-id="d45b9-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="d45b9-139">**msdyn_PSSDeleteV1**: API ini boleh digunakan untuk memadamkan entiti.</span><span class="sxs-lookup"><span data-stu-id="d45b9-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="d45b9-140">Entiti boleh jadi sebarang entiti Penjadualan yang menyokong pemadaman operasi.</span><span class="sxs-lookup"><span data-stu-id="d45b9-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="d45b9-141">**msdyn_ExecuteOperationSetV1**: API ini digunakan untuk melaksanakan semua operasi dalam set operasi yang diberikan.</span><span class="sxs-lookup"><span data-stu-id="d45b9-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="d45b9-142">Menggunakan API Jadual dengan OperationSet</span><span class="sxs-lookup"><span data-stu-id="d45b9-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="d45b9-143">Kerana rekod dengan kedua-dua **CreateProjectV1** dan **CreateTeamMemberV1** dicipta dengan serta-merta, API ini tidak boleh digunakan dalam **OperationSet** secara langsung.</span><span class="sxs-lookup"><span data-stu-id="d45b9-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="d45b9-144">Walau bagaimanapun, anda boleh menggunakan API untuk mencipta rekod yang diperlukan, cipta **OperationSet** dan kemudian gunakan rekod yang dipracipta dalam **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="d45b9-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="d45b9-145">Operasi yang disokong</span><span class="sxs-lookup"><span data-stu-id="d45b9-145">Supported operations</span></span>

| <span data-ttu-id="d45b9-146">Entiti penjadualan</span><span class="sxs-lookup"><span data-stu-id="d45b9-146">Scheduling entity</span></span> | <span data-ttu-id="d45b9-147">Cipta</span><span class="sxs-lookup"><span data-stu-id="d45b9-147">Create</span></span> | <span data-ttu-id="d45b9-148">Kemas kini </span><span class="sxs-lookup"><span data-stu-id="d45b9-148">Update</span></span> | <span data-ttu-id="d45b9-149">Delete</span><span class="sxs-lookup"><span data-stu-id="d45b9-149">Delete</span></span> | <span data-ttu-id="d45b9-150">Pertimbangan penting</span><span class="sxs-lookup"><span data-stu-id="d45b9-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="d45b9-151">Tugas projek</span><span class="sxs-lookup"><span data-stu-id="d45b9-151">Project task</span></span> | <span data-ttu-id="d45b9-152">Ya</span><span class="sxs-lookup"><span data-stu-id="d45b9-152">Yes</span></span> | <span data-ttu-id="d45b9-153">Ya</span><span class="sxs-lookup"><span data-stu-id="d45b9-153">Yes</span></span> | <span data-ttu-id="d45b9-154">Ya</span><span class="sxs-lookup"><span data-stu-id="d45b9-154">Yes</span></span> | <span data-ttu-id="d45b9-155">Tiada</span><span class="sxs-lookup"><span data-stu-id="d45b9-155">None</span></span> |
| <span data-ttu-id="d45b9-156">Pergantungan tugas projek</span><span class="sxs-lookup"><span data-stu-id="d45b9-156">Project task dependency</span></span> | <span data-ttu-id="d45b9-157">Ya</span><span class="sxs-lookup"><span data-stu-id="d45b9-157">Yes</span></span> | <span data-ttu-id="d45b9-158">Ya</span><span class="sxs-lookup"><span data-stu-id="d45b9-158">Yes</span></span> | | <span data-ttu-id="d45b9-159">Rekod pergantungan tugas projek tidak dikemas kini.</span><span class="sxs-lookup"><span data-stu-id="d45b9-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="d45b9-160">Sebaliknya, rekod lama boleh dipadamkan dan rekod baharu boleh dicipta.</span><span class="sxs-lookup"><span data-stu-id="d45b9-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="d45b9-161">Penugasan sumber</span><span class="sxs-lookup"><span data-stu-id="d45b9-161">Resource assignment</span></span> | <span data-ttu-id="d45b9-162">Ya</span><span class="sxs-lookup"><span data-stu-id="d45b9-162">Yes</span></span> | <span data-ttu-id="d45b9-163">Ya</span><span class="sxs-lookup"><span data-stu-id="d45b9-163">Yes</span></span> | | <span data-ttu-id="d45b9-164">Operasi dengan medan berikut tidak disokong: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** dan **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="d45b9-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="d45b9-165">Rekod penugasan sumber tidak dikemas kini.</span><span class="sxs-lookup"><span data-stu-id="d45b9-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="d45b9-166">Sebaliknya, rekod lama boleh dipadamkan dan rekod baharu boleh dicipta.</span><span class="sxs-lookup"><span data-stu-id="d45b9-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="d45b9-167">Baldi projek</span><span class="sxs-lookup"><span data-stu-id="d45b9-167">Project bucket</span></span> | <span data-ttu-id="d45b9-168">T/B</span><span class="sxs-lookup"><span data-stu-id="d45b9-168">N/A</span></span> | <span data-ttu-id="d45b9-169">T/B</span><span class="sxs-lookup"><span data-stu-id="d45b9-169">N/A</span></span> | <span data-ttu-id="d45b9-170">T/B</span><span class="sxs-lookup"><span data-stu-id="d45b9-170">N/A</span></span> | <span data-ttu-id="d45b9-171">Baldi lalai dicipta menggunakan API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="d45b9-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="d45b9-172">Ahli pasukan projek</span><span class="sxs-lookup"><span data-stu-id="d45b9-172">Project team member</span></span> | <span data-ttu-id="d45b9-173">Ya</span><span class="sxs-lookup"><span data-stu-id="d45b9-173">Yes</span></span> | <span data-ttu-id="d45b9-174">Ya</span><span class="sxs-lookup"><span data-stu-id="d45b9-174">Yes</span></span> | <span data-ttu-id="d45b9-175">Ya</span><span class="sxs-lookup"><span data-stu-id="d45b9-175">Yes</span></span> | <span data-ttu-id="d45b9-176">Untuk mencipta operasi, gunakan API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="d45b9-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="d45b9-177">Project</span><span class="sxs-lookup"><span data-stu-id="d45b9-177">Project</span></span> | <span data-ttu-id="d45b9-178">Ya</span><span class="sxs-lookup"><span data-stu-id="d45b9-178">Yes</span></span> | <span data-ttu-id="d45b9-179">Ya</span><span class="sxs-lookup"><span data-stu-id="d45b9-179">Yes</span></span> | <span data-ttu-id="d45b9-180">T/B</span><span class="sxs-lookup"><span data-stu-id="d45b9-180">N/A</span></span> | <span data-ttu-id="d45b9-181">Operasi dengan medan berikut tidak disokong: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** dan **Duration**.</span><span class="sxs-lookup"><span data-stu-id="d45b9-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="d45b9-182">Api ini boleh dipanggil dengan objek entiti yang termasuk medan tersuai.</span><span class="sxs-lookup"><span data-stu-id="d45b9-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="d45b9-183">Sifat ID adalah pilihan.</span><span class="sxs-lookup"><span data-stu-id="d45b9-183">The ID property is optional.</span></span> <span data-ttu-id="d45b9-184">Jika ia disediakan, sistem cuba untuk menggunakannya dan memberikan pengecualian jika ia tidak boleh digunakan.</span><span class="sxs-lookup"><span data-stu-id="d45b9-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="d45b9-185">Jika ia tidak disediakan, sistem akan menjananya.</span><span class="sxs-lookup"><span data-stu-id="d45b9-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="d45b9-186">Pengehadan dan isu yang diketahui</span><span class="sxs-lookup"><span data-stu-id="d45b9-186">Limitations and known issues</span></span>
<span data-ttu-id="d45b9-187">Berikut ialah senarai pengehadan dan isu yang diketahui:</span><span class="sxs-lookup"><span data-stu-id="d45b9-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="d45b9-188">API Jadual hanya boleh digunakan oleh **Pengguna dengan Lesen Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="d45b9-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="d45b9-189">Ia tidak boleh digunakan oleh:</span><span class="sxs-lookup"><span data-stu-id="d45b9-189">They can't be used by:</span></span>
    - <span data-ttu-id="d45b9-190">Pengguna aplikasi</span><span class="sxs-lookup"><span data-stu-id="d45b9-190">Application users</span></span>
    - <span data-ttu-id="d45b9-191">Pengguna sistem</span><span class="sxs-lookup"><span data-stu-id="d45b9-191">System users</span></span>
    - <span data-ttu-id="d45b9-192">Pengguna integrasi</span><span class="sxs-lookup"><span data-stu-id="d45b9-192">Integration users</span></span>
    - <span data-ttu-id="d45b9-193">Pengguna lain yang tidak mempunyai lesen yang diperlukan</span><span class="sxs-lookup"><span data-stu-id="d45b9-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="d45b9-194">Setiap **OperationSet** hanya boleh mempunyai maksimum 100 operasi.</span><span class="sxs-lookup"><span data-stu-id="d45b9-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="d45b9-195">Setiap pengguna hanya boleh mempunyai maksimum 10 **OperationSet** terbuka.</span><span class="sxs-lookup"><span data-stu-id="d45b9-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="d45b9-196">Project Operations menyokong jumlah maksimum 500 tugas pada sesuatu projek pada masa ini.</span><span class="sxs-lookup"><span data-stu-id="d45b9-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="d45b9-197">Status kegagalan **OperationSet** dan log kegagalan tidak tersedia pada masa ini.</span><span class="sxs-lookup"><span data-stu-id="d45b9-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="d45b9-198">API Jadual dalam Pratonton awam.</span><span class="sxs-lookup"><span data-stu-id="d45b9-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="d45b9-199">Penggunaan API ini dalam Persekitaran pengeluaran tidak disokong oleh Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d45b9-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="d45b9-200">Senario sampel</span><span class="sxs-lookup"><span data-stu-id="d45b9-200">Sample scenario</span></span>

<span data-ttu-id="d45b9-201">Dalam senario ini, anda akan mencipta projek, ahli pasukan, empat tugas dan dua penugasan sumber.</span><span class="sxs-lookup"><span data-stu-id="d45b9-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="d45b9-202">Seterusnya, anda akan mengemas kini satu tugas, mengemas kini projek, memadamkan satu tugas, memadamkan satu penugasan sumber dan mencipta pergantungan tugas.</span><span class="sxs-lookup"><span data-stu-id="d45b9-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```C#
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="d45b9-203">Sampel tambahan</span><span class="sxs-lookup"><span data-stu-id="d45b9-203">Additional samples</span></span>

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };
    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
    return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";
    return project;
}

private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
        task["new_amount"] = 591.34m;
        task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }
    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;
    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);
    return taskDependency;
}

#endregion

#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
