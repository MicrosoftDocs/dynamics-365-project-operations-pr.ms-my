---
title: Gunakan API jadual Projek untuk melaksanakan operasi dengan entiti Penjadualan
description: Topik ini memberikan maklumat dan sampel untuk penggunaan API jadual Projek.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293238"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="dffde-103">Gunakan API jadual Projek untuk melaksanakan operasi dengan entiti Penjadualan</span><span class="sxs-lookup"><span data-stu-id="dffde-103">Use Project schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="dffde-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="dffde-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="dffde-105">Sesetengah atau semua kefungsian yang dinyatakan dalam topik ini tersedia sebagai sebahagian daripada keluaran pratonton.</span><span class="sxs-lookup"><span data-stu-id="dffde-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="dffde-106">Kandungan dan fungsi adalah tertakluk kepada perubahan.</span><span class="sxs-lookup"><span data-stu-id="dffde-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="dffde-107">Entiti penjadualan</span><span class="sxs-lookup"><span data-stu-id="dffde-107">Scheduling entities</span></span>

<span data-ttu-id="dffde-108">API jadual Projek memberikan keupayaan untuk melaksanakan operasi cipta, kemas kini dan padam dengan **Entiti penjadualan**.</span><span class="sxs-lookup"><span data-stu-id="dffde-108">Project schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="dffde-109">Entiti ini diuruskan melalui enjin Penjadualan dalam Projek untuk web.</span><span class="sxs-lookup"><span data-stu-id="dffde-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="dffde-110">Operasi mencipta, mengemas kini dan memadam dengan **Entiti penjadualan** telah dihadkan dalam keluaran Dynamics 365 Project Operations sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="dffde-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="dffde-111">Jadual berikut memberikan senarai lengkap entiti jadual Projek.</span><span class="sxs-lookup"><span data-stu-id="dffde-111">The following table provides a full list of the Project schedule entities.</span></span>

| <span data-ttu-id="dffde-112">Nama entiti</span><span class="sxs-lookup"><span data-stu-id="dffde-112">Entity name</span></span>  | <span data-ttu-id="dffde-113">Nama logik entiti</span><span class="sxs-lookup"><span data-stu-id="dffde-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="dffde-114">Project</span><span class="sxs-lookup"><span data-stu-id="dffde-114">Project</span></span> | <span data-ttu-id="dffde-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="dffde-115">msdyn_project</span></span> |
| <span data-ttu-id="dffde-116">Tugas Projek</span><span class="sxs-lookup"><span data-stu-id="dffde-116">Project Task</span></span>  | <span data-ttu-id="dffde-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="dffde-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="dffde-118">Kebergantungan Tugas Projek</span><span class="sxs-lookup"><span data-stu-id="dffde-118">Project Task Dependency</span></span>  | <span data-ttu-id="dffde-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="dffde-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="dffde-120">Tugasan Sumber</span><span class="sxs-lookup"><span data-stu-id="dffde-120">Resource Assignment</span></span> | <span data-ttu-id="dffde-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="dffde-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="dffde-122">Baldi Projek</span><span class="sxs-lookup"><span data-stu-id="dffde-122">Project Bucket</span></span>  | <span data-ttu-id="dffde-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="dffde-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="dffde-124">Ahli Pasukan Projek</span><span class="sxs-lookup"><span data-stu-id="dffde-124">Project Team Member</span></span> | <span data-ttu-id="dffde-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="dffde-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="dffde-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="dffde-126">OperationSet</span></span>

<span data-ttu-id="dffde-127">OperationSet ialah corak unit kerja yang boleh digunakan apabila beberapa jadual yang mempengaruhi permintaan mesti diproses dalam transaksi.</span><span class="sxs-lookup"><span data-stu-id="dffde-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="project-schedule-apis"></a><span data-ttu-id="dffde-128">API jadual Projek</span><span class="sxs-lookup"><span data-stu-id="dffde-128">Project schedule APIs</span></span>

<span data-ttu-id="dffde-129">Berikut ialah senarai API jadual Projek semasa.</span><span class="sxs-lookup"><span data-stu-id="dffde-129">The following is a list of current Project schedule APIs.</span></span>

- <span data-ttu-id="dffde-130">**msdyn_CreateProjectV1**: API ini boleh digunakan untuk mencipta projek.</span><span class="sxs-lookup"><span data-stu-id="dffde-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="dffde-131">Projek dan baldi projek lalai dicipta dengan serta-merta.</span><span class="sxs-lookup"><span data-stu-id="dffde-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="dffde-132">**msdyn_CreateTeamMemberV1**: API ini boleh digunakan untuk mencipta ahli pasukan projek.</span><span class="sxs-lookup"><span data-stu-id="dffde-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="dffde-133">Rekod ahli pasukan dicipta dengan serta-merta.</span><span class="sxs-lookup"><span data-stu-id="dffde-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="dffde-134">**msdyn_CreateOperationSetV1**: API ini boleh digunakan untuk menjadualkan beberapa permintaan yang mesti dilaksanakan dalam transaksi.</span><span class="sxs-lookup"><span data-stu-id="dffde-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="dffde-135">**msdyn_PSSCreateV1**: API ini boleh digunakan untuk mencipta entiti.</span><span class="sxs-lookup"><span data-stu-id="dffde-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="dffde-136">Entiti boleh menjadi sebarang entiti penjadualan Projek yang menyokong operasi cipta.</span><span class="sxs-lookup"><span data-stu-id="dffde-136">The entity can be any of the Project scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="dffde-137">**msdyn_PSSUpdateV1**: API ini boleh digunakan untuk mengemas kini entiti.</span><span class="sxs-lookup"><span data-stu-id="dffde-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="dffde-138">Entiti boleh menjadi sebarang entiti penjadualan Projek yang menyokong operasi kemas kini.</span><span class="sxs-lookup"><span data-stu-id="dffde-138">The entity can be any of the Project scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="dffde-139">**msdyn_PSSDeleteV1**: API ini boleh digunakan untuk memadamkan entiti.</span><span class="sxs-lookup"><span data-stu-id="dffde-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="dffde-140">Entiti boleh menjadi sebarang entiti penjadualan Projek yang menyokong operasi padam.</span><span class="sxs-lookup"><span data-stu-id="dffde-140">The entity can be any of the Project scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="dffde-141">**msdyn_ExecuteOperationSetV1**: API ini digunakan untuk melaksanakan semua operasi dalam set operasi yang diberikan.</span><span class="sxs-lookup"><span data-stu-id="dffde-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-project-schedule-apis-with-operationset"></a><span data-ttu-id="dffde-142">Menggunakan API jadual Projek dengan OperationSet</span><span class="sxs-lookup"><span data-stu-id="dffde-142">Using Project schedule APIs with OperationSet</span></span>

<span data-ttu-id="dffde-143">Kerana rekod dengan kedua-dua **CreateProjectV1** dan **CreateTeamMemberV1** dicipta dengan serta-merta, API ini tidak boleh digunakan dalam **OperationSet** secara langsung.</span><span class="sxs-lookup"><span data-stu-id="dffde-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="dffde-144">Walau bagaimanapun, anda boleh menggunakan API untuk mencipta rekod yang diperlukan, cipta **OperationSet** dan kemudian gunakan rekod yang dipracipta dalam **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="dffde-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="dffde-145">Operasi yang disokong</span><span class="sxs-lookup"><span data-stu-id="dffde-145">Supported operations</span></span>

| <span data-ttu-id="dffde-146">Entiti penjadualan</span><span class="sxs-lookup"><span data-stu-id="dffde-146">Scheduling entity</span></span> | <span data-ttu-id="dffde-147">Cipta</span><span class="sxs-lookup"><span data-stu-id="dffde-147">Create</span></span> | <span data-ttu-id="dffde-148">Kemas kini </span><span class="sxs-lookup"><span data-stu-id="dffde-148">Update</span></span> | <span data-ttu-id="dffde-149">Delete</span><span class="sxs-lookup"><span data-stu-id="dffde-149">Delete</span></span> | <span data-ttu-id="dffde-150">Pertimbangan penting</span><span class="sxs-lookup"><span data-stu-id="dffde-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="dffde-151">Tugas projek</span><span class="sxs-lookup"><span data-stu-id="dffde-151">Project task</span></span> | <span data-ttu-id="dffde-152">Ya</span><span class="sxs-lookup"><span data-stu-id="dffde-152">Yes</span></span> | <span data-ttu-id="dffde-153">Ya</span><span class="sxs-lookup"><span data-stu-id="dffde-153">Yes</span></span> | <span data-ttu-id="dffde-154">Ya</span><span class="sxs-lookup"><span data-stu-id="dffde-154">Yes</span></span> | <span data-ttu-id="dffde-155">Tiada</span><span class="sxs-lookup"><span data-stu-id="dffde-155">None</span></span> |
| <span data-ttu-id="dffde-156">Pergantungan tugas projek</span><span class="sxs-lookup"><span data-stu-id="dffde-156">Project task dependency</span></span> | <span data-ttu-id="dffde-157">Ya</span><span class="sxs-lookup"><span data-stu-id="dffde-157">Yes</span></span> | <span data-ttu-id="dffde-158">Ya</span><span class="sxs-lookup"><span data-stu-id="dffde-158">Yes</span></span> | | <span data-ttu-id="dffde-159">Rekod pergantungan tugas projek tidak dikemas kini.</span><span class="sxs-lookup"><span data-stu-id="dffde-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="dffde-160">Sebaliknya, rekod lama boleh dipadamkan dan rekod baharu boleh dicipta.</span><span class="sxs-lookup"><span data-stu-id="dffde-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="dffde-161">Penugasan sumber</span><span class="sxs-lookup"><span data-stu-id="dffde-161">Resource assignment</span></span> | <span data-ttu-id="dffde-162">Ya</span><span class="sxs-lookup"><span data-stu-id="dffde-162">Yes</span></span> | <span data-ttu-id="dffde-163">Ya</span><span class="sxs-lookup"><span data-stu-id="dffde-163">Yes</span></span> | | <span data-ttu-id="dffde-164">Operasi dengan medan berikut tidak disokong: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** dan **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="dffde-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="dffde-165">Rekod penugasan sumber tidak dikemas kini.</span><span class="sxs-lookup"><span data-stu-id="dffde-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="dffde-166">Sebaliknya, rekod lama boleh dipadamkan dan rekod baharu boleh dicipta.</span><span class="sxs-lookup"><span data-stu-id="dffde-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="dffde-167">Baldi projek</span><span class="sxs-lookup"><span data-stu-id="dffde-167">Project bucket</span></span> | <span data-ttu-id="dffde-168">T/B</span><span class="sxs-lookup"><span data-stu-id="dffde-168">N/A</span></span> | <span data-ttu-id="dffde-169">T/B</span><span class="sxs-lookup"><span data-stu-id="dffde-169">N/A</span></span> | <span data-ttu-id="dffde-170">T/B</span><span class="sxs-lookup"><span data-stu-id="dffde-170">N/A</span></span> | <span data-ttu-id="dffde-171">Baldi lalai dicipta menggunakan API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="dffde-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="dffde-172">Ahli pasukan projek</span><span class="sxs-lookup"><span data-stu-id="dffde-172">Project team member</span></span> | <span data-ttu-id="dffde-173">Ya</span><span class="sxs-lookup"><span data-stu-id="dffde-173">Yes</span></span> | <span data-ttu-id="dffde-174">Ya</span><span class="sxs-lookup"><span data-stu-id="dffde-174">Yes</span></span> | <span data-ttu-id="dffde-175">Ya</span><span class="sxs-lookup"><span data-stu-id="dffde-175">Yes</span></span> | <span data-ttu-id="dffde-176">Untuk mencipta operasi, gunakan API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="dffde-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="dffde-177">Project</span><span class="sxs-lookup"><span data-stu-id="dffde-177">Project</span></span> | <span data-ttu-id="dffde-178">Ya</span><span class="sxs-lookup"><span data-stu-id="dffde-178">Yes</span></span> | <span data-ttu-id="dffde-179">Ya</span><span class="sxs-lookup"><span data-stu-id="dffde-179">Yes</span></span> | <span data-ttu-id="dffde-180">T/B</span><span class="sxs-lookup"><span data-stu-id="dffde-180">N/A</span></span> | <span data-ttu-id="dffde-181">Operasi dengan medan berikut tidak disokong: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** dan **Duration**.</span><span class="sxs-lookup"><span data-stu-id="dffde-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="dffde-182">Api ini boleh dipanggil dengan objek entiti yang termasuk medan tersuai.</span><span class="sxs-lookup"><span data-stu-id="dffde-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="dffde-183">Sifat ID adalah pilihan.</span><span class="sxs-lookup"><span data-stu-id="dffde-183">The ID property is optional.</span></span> <span data-ttu-id="dffde-184">Jika ia disediakan, sistem cuba untuk menggunakannya dan memberikan pengecualian jika ia tidak boleh digunakan.</span><span class="sxs-lookup"><span data-stu-id="dffde-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="dffde-185">Jika ia tidak disediakan, sistem akan menjananya.</span><span class="sxs-lookup"><span data-stu-id="dffde-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="dffde-186">Medan terhad</span><span class="sxs-lookup"><span data-stu-id="dffde-186">Restricted fields</span></span>

<span data-ttu-id="dffde-187">Jadual berikut mentakrifkan medan yang terhad daripada **Cipta** dan **Edit.**</span><span class="sxs-lookup"><span data-stu-id="dffde-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="dffde-188">Tugas projek</span><span class="sxs-lookup"><span data-stu-id="dffde-188">Project task</span></span>

| <span data-ttu-id="dffde-189">**Nama logik**</span><span class="sxs-lookup"><span data-stu-id="dffde-189">**Logical name**</span></span>                       | <span data-ttu-id="dffde-190">**Boleh cipta**</span><span class="sxs-lookup"><span data-stu-id="dffde-190">**Can create**</span></span> | <span data-ttu-id="dffde-191">**Boleh edit**</span><span class="sxs-lookup"><span data-stu-id="dffde-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="dffde-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="dffde-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="dffde-193">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-193">no</span></span>             | <span data-ttu-id="dffde-194">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-194">no</span></span>               |
| <span data-ttu-id="dffde-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="dffde-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="dffde-196">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-196">no</span></span>             | <span data-ttu-id="dffde-197">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-197">no</span></span>               |
| <span data-ttu-id="dffde-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="dffde-198">msdyn_actualend</span></span>                        | <span data-ttu-id="dffde-199">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-199">no</span></span>             | <span data-ttu-id="dffde-200">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-200">no</span></span>               |
| <span data-ttu-id="dffde-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="dffde-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="dffde-202">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-202">no</span></span>             | <span data-ttu-id="dffde-203">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-203">no</span></span>               |
| <span data-ttu-id="dffde-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="dffde-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="dffde-205">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-205">no</span></span>             | <span data-ttu-id="dffde-206">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-206">no</span></span>               |
| <span data-ttu-id="dffde-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="dffde-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="dffde-208">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-208">no</span></span>             | <span data-ttu-id="dffde-209">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-209">no</span></span>               |
| <span data-ttu-id="dffde-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="dffde-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="dffde-211">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-211">no</span></span>             | <span data-ttu-id="dffde-212">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-212">no</span></span>               |
| <span data-ttu-id="dffde-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="dffde-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="dffde-214">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-214">no</span></span>             | <span data-ttu-id="dffde-215">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-215">no</span></span>               |
| <span data-ttu-id="dffde-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="dffde-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="dffde-217">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-217">no</span></span>             | <span data-ttu-id="dffde-218">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-218">no</span></span>               |
| <span data-ttu-id="dffde-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="dffde-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="dffde-220">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-220">no</span></span>             | <span data-ttu-id="dffde-221">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-221">no</span></span>               |
| <span data-ttu-id="dffde-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="dffde-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="dffde-223">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-223">no</span></span>             | <span data-ttu-id="dffde-224">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-224">no</span></span>               |
| <span data-ttu-id="dffde-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="dffde-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="dffde-226">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-226">no</span></span>             | <span data-ttu-id="dffde-227">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-227">no</span></span>               |
| <span data-ttu-id="dffde-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="dffde-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="dffde-229">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-229">no</span></span>             | <span data-ttu-id="dffde-230">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-230">no</span></span>               |
| <span data-ttu-id="dffde-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="dffde-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="dffde-232">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-232">no</span></span>             | <span data-ttu-id="dffde-233">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-233">no</span></span>               |
| <span data-ttu-id="dffde-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="dffde-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="dffde-235">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-235">no</span></span>             | <span data-ttu-id="dffde-236">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-236">no</span></span>               |
| <span data-ttu-id="dffde-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="dffde-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="dffde-238">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-238">no</span></span>             | <span data-ttu-id="dffde-239">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-239">no</span></span>               |
| <span data-ttu-id="dffde-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="dffde-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="dffde-241">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-241">no</span></span>             | <span data-ttu-id="dffde-242">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-242">no</span></span>               |
| <span data-ttu-id="dffde-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="dffde-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="dffde-244">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-244">no</span></span>             | <span data-ttu-id="dffde-245">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-245">no</span></span>               |
| <span data-ttu-id="dffde-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="dffde-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="dffde-247">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-247">no</span></span>             | <span data-ttu-id="dffde-248">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-248">no</span></span>               |
| <span data-ttu-id="dffde-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="dffde-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="dffde-250">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-250">no</span></span>             | <span data-ttu-id="dffde-251">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-251">no</span></span>               |
| <span data-ttu-id="dffde-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="dffde-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="dffde-253">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-253">no</span></span>             | <span data-ttu-id="dffde-254">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-254">no</span></span>               |
| <span data-ttu-id="dffde-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="dffde-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="dffde-256">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-256">no</span></span>             | <span data-ttu-id="dffde-257">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-257">no</span></span>               |
| <span data-ttu-id="dffde-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="dffde-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="dffde-259">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-259">no</span></span>             | <span data-ttu-id="dffde-260">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-260">no</span></span>               |
| <span data-ttu-id="dffde-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="dffde-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="dffde-262">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-262">no</span></span>             | <span data-ttu-id="dffde-263">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-263">no</span></span>               |
| <span data-ttu-id="dffde-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="dffde-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="dffde-265">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-265">no</span></span>             | <span data-ttu-id="dffde-266">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-266">no</span></span>               |
| <span data-ttu-id="dffde-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="dffde-267">msdyn_progress</span></span>                         | <span data-ttu-id="dffde-268">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-268">no</span></span>             | <span data-ttu-id="dffde-269">tidak (ya untuk P4W)</span><span class="sxs-lookup"><span data-stu-id="dffde-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="dffde-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="dffde-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="dffde-271">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-271">no</span></span>             | <span data-ttu-id="dffde-272">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-272">no</span></span>               |
| <span data-ttu-id="dffde-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="dffde-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="dffde-274">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-274">no</span></span>             | <span data-ttu-id="dffde-275">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-275">no</span></span>               |
| <span data-ttu-id="dffde-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="dffde-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="dffde-277">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-277">no</span></span>             | <span data-ttu-id="dffde-278">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-278">no</span></span>               |
| <span data-ttu-id="dffde-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="dffde-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="dffde-280">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-280">no</span></span>             | <span data-ttu-id="dffde-281">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-281">no</span></span>               |
| <span data-ttu-id="dffde-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="dffde-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="dffde-283">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-283">no</span></span>             | <span data-ttu-id="dffde-284">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-284">no</span></span>               |
| <span data-ttu-id="dffde-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="dffde-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="dffde-286">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-286">no</span></span>             | <span data-ttu-id="dffde-287">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-287">no</span></span>               |
| <span data-ttu-id="dffde-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="dffde-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="dffde-289">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-289">no</span></span>             | <span data-ttu-id="dffde-290">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-290">no</span></span>               |
| <span data-ttu-id="dffde-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="dffde-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="dffde-292">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-292">no</span></span>             | <span data-ttu-id="dffde-293">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-293">no</span></span>               |
| <span data-ttu-id="dffde-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="dffde-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="dffde-295">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-295">no</span></span>             | <span data-ttu-id="dffde-296">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-296">no</span></span>               |
| <span data-ttu-id="dffde-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="dffde-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="dffde-298">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-298">no</span></span>             | <span data-ttu-id="dffde-299">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-299">no</span></span>               |
| <span data-ttu-id="dffde-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="dffde-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="dffde-301">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-301">no</span></span>             | <span data-ttu-id="dffde-302">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-302">no</span></span>               |
| <span data-ttu-id="dffde-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="dffde-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="dffde-304">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-304">no</span></span>             | <span data-ttu-id="dffde-305">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-305">no</span></span>               |
| <span data-ttu-id="dffde-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="dffde-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="dffde-307">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-307">no</span></span>             | <span data-ttu-id="dffde-308">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-308">no</span></span>               |
| <span data-ttu-id="dffde-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="dffde-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="dffde-310">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-310">no</span></span>             | <span data-ttu-id="dffde-311">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-311">no</span></span>               |
| <span data-ttu-id="dffde-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="dffde-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="dffde-313">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-313">no</span></span>             | <span data-ttu-id="dffde-314">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-314">no</span></span>               |
| <span data-ttu-id="dffde-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="dffde-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="dffde-316">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-316">no</span></span>             | <span data-ttu-id="dffde-317">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-317">no</span></span>               |
| <span data-ttu-id="dffde-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="dffde-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="dffde-319">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-319">no</span></span>             | <span data-ttu-id="dffde-320">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-320">no</span></span>               |
| <span data-ttu-id="dffde-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="dffde-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="dffde-322">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-322">no</span></span>             | <span data-ttu-id="dffde-323">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-323">no</span></span>               |
| <span data-ttu-id="dffde-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="dffde-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="dffde-325">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-325">no</span></span>             | <span data-ttu-id="dffde-326">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-326">no</span></span>               |
| <span data-ttu-id="dffde-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="dffde-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="dffde-328">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-328">no</span></span>             | <span data-ttu-id="dffde-329">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-329">no</span></span>               |
| <span data-ttu-id="dffde-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="dffde-330">msdyn_summary</span></span>                          | <span data-ttu-id="dffde-331">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-331">no</span></span>             | <span data-ttu-id="dffde-332">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-332">no</span></span>               |
| <span data-ttu-id="dffde-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="dffde-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="dffde-334">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-334">no</span></span>             | <span data-ttu-id="dffde-335">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-335">no</span></span>               |
| <span data-ttu-id="dffde-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="dffde-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="dffde-337">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-337">no</span></span>             | <span data-ttu-id="dffde-338">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="dffde-339">Pergantungan tugas projek</span><span class="sxs-lookup"><span data-stu-id="dffde-339">Project task dependency</span></span>

| <span data-ttu-id="dffde-340">**Nama logik**</span><span class="sxs-lookup"><span data-stu-id="dffde-340">**Logical name**</span></span>              | <span data-ttu-id="dffde-341">**Boleh cipta**</span><span class="sxs-lookup"><span data-stu-id="dffde-341">**Can create**</span></span> | <span data-ttu-id="dffde-342">**Boleh edit**</span><span class="sxs-lookup"><span data-stu-id="dffde-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="dffde-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="dffde-343">msdyn_linktype</span></span>                | <span data-ttu-id="dffde-344">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-344">no</span></span>             | <span data-ttu-id="dffde-345">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-345">no</span></span>           |
| <span data-ttu-id="dffde-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="dffde-346">msdyn_linktypename</span></span>            | <span data-ttu-id="dffde-347">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-347">no</span></span>             | <span data-ttu-id="dffde-348">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-348">no</span></span>           |
| <span data-ttu-id="dffde-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="dffde-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="dffde-350">ya</span><span class="sxs-lookup"><span data-stu-id="dffde-350">yes</span></span>            | <span data-ttu-id="dffde-351">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-351">no</span></span>           |
| <span data-ttu-id="dffde-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="dffde-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="dffde-353">ya</span><span class="sxs-lookup"><span data-stu-id="dffde-353">yes</span></span>            | <span data-ttu-id="dffde-354">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-354">no</span></span>           |
| <span data-ttu-id="dffde-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="dffde-355">msdyn_project</span></span>                 | <span data-ttu-id="dffde-356">ya</span><span class="sxs-lookup"><span data-stu-id="dffde-356">yes</span></span>            | <span data-ttu-id="dffde-357">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-357">no</span></span>           |
| <span data-ttu-id="dffde-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="dffde-358">msdyn_projectname</span></span>             | <span data-ttu-id="dffde-359">ya</span><span class="sxs-lookup"><span data-stu-id="dffde-359">yes</span></span>            | <span data-ttu-id="dffde-360">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-360">no</span></span>           |
| <span data-ttu-id="dffde-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="dffde-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="dffde-362">ya</span><span class="sxs-lookup"><span data-stu-id="dffde-362">yes</span></span>            | <span data-ttu-id="dffde-363">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-363">no</span></span>           |
| <span data-ttu-id="dffde-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="dffde-364">msdyn_successortask</span></span>           | <span data-ttu-id="dffde-365">ya</span><span class="sxs-lookup"><span data-stu-id="dffde-365">yes</span></span>            | <span data-ttu-id="dffde-366">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-366">no</span></span>           |
| <span data-ttu-id="dffde-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="dffde-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="dffde-368">ya</span><span class="sxs-lookup"><span data-stu-id="dffde-368">yes</span></span>            | <span data-ttu-id="dffde-369">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="dffde-370">Penugasan sumber</span><span class="sxs-lookup"><span data-stu-id="dffde-370">Resource assignment</span></span>

| <span data-ttu-id="dffde-371">**Nama logik**</span><span class="sxs-lookup"><span data-stu-id="dffde-371">**Logical name**</span></span>             | <span data-ttu-id="dffde-372">**Boleh cipta**</span><span class="sxs-lookup"><span data-stu-id="dffde-372">**Can create**</span></span> | <span data-ttu-id="dffde-373">**Boleh edit**</span><span class="sxs-lookup"><span data-stu-id="dffde-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="dffde-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="dffde-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="dffde-375">ya</span><span class="sxs-lookup"><span data-stu-id="dffde-375">yes</span></span>            | <span data-ttu-id="dffde-376">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-376">no</span></span>           |
| <span data-ttu-id="dffde-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="dffde-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="dffde-378">ya</span><span class="sxs-lookup"><span data-stu-id="dffde-378">yes</span></span>            | <span data-ttu-id="dffde-379">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-379">no</span></span>           |
| <span data-ttu-id="dffde-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="dffde-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="dffde-381">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-381">no</span></span>             | <span data-ttu-id="dffde-382">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-382">no</span></span>           |
| <span data-ttu-id="dffde-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="dffde-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="dffde-384">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-384">no</span></span>             | <span data-ttu-id="dffde-385">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-385">no</span></span>           |
| <span data-ttu-id="dffde-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="dffde-386">msdyn_committype</span></span>             | <span data-ttu-id="dffde-387">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-387">no</span></span>             | <span data-ttu-id="dffde-388">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-388">no</span></span>           |
| <span data-ttu-id="dffde-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="dffde-389">msdyn_committypename</span></span>         | <span data-ttu-id="dffde-390">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-390">no</span></span>             | <span data-ttu-id="dffde-391">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-391">no</span></span>           |
| <span data-ttu-id="dffde-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="dffde-392">msdyn_effort</span></span>                 | <span data-ttu-id="dffde-393">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-393">no</span></span>             | <span data-ttu-id="dffde-394">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-394">no</span></span>           |
| <span data-ttu-id="dffde-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="dffde-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="dffde-396">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-396">no</span></span>             | <span data-ttu-id="dffde-397">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-397">no</span></span>           |
| <span data-ttu-id="dffde-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="dffde-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="dffde-399">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-399">no</span></span>             | <span data-ttu-id="dffde-400">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-400">no</span></span>           |
| <span data-ttu-id="dffde-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="dffde-401">msdyn_finish</span></span>                 | <span data-ttu-id="dffde-402">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-402">no</span></span>             | <span data-ttu-id="dffde-403">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-403">no</span></span>           |
| <span data-ttu-id="dffde-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="dffde-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="dffde-405">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-405">no</span></span>             | <span data-ttu-id="dffde-406">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-406">no</span></span>           |
| <span data-ttu-id="dffde-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="dffde-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="dffde-408">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-408">no</span></span>             | <span data-ttu-id="dffde-409">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-409">no</span></span>           |
| <span data-ttu-id="dffde-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="dffde-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="dffde-411">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-411">no</span></span>             | <span data-ttu-id="dffde-412">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-412">no</span></span>           |
| <span data-ttu-id="dffde-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="dffde-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="dffde-414">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-414">no</span></span>             | <span data-ttu-id="dffde-415">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-415">no</span></span>           |
| <span data-ttu-id="dffde-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="dffde-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="dffde-417">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-417">no</span></span>             | <span data-ttu-id="dffde-418">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-418">no</span></span>           |
| <span data-ttu-id="dffde-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="dffde-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="dffde-420">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-420">no</span></span>             | <span data-ttu-id="dffde-421">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-421">no</span></span>           |
| <span data-ttu-id="dffde-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="dffde-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="dffde-423">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-423">no</span></span>             | <span data-ttu-id="dffde-424">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-424">no</span></span>           |
| <span data-ttu-id="dffde-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="dffde-425">msdyn_projectid</span></span>              | <span data-ttu-id="dffde-426">ya</span><span class="sxs-lookup"><span data-stu-id="dffde-426">yes</span></span>            | <span data-ttu-id="dffde-427">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-427">no</span></span>           |
| <span data-ttu-id="dffde-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="dffde-428">msdyn_projectidname</span></span>          | <span data-ttu-id="dffde-429">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-429">no</span></span>             | <span data-ttu-id="dffde-430">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-430">no</span></span>           |
| <span data-ttu-id="dffde-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="dffde-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="dffde-432">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-432">no</span></span>             | <span data-ttu-id="dffde-433">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-433">no</span></span>           |
| <span data-ttu-id="dffde-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="dffde-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="dffde-435">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-435">no</span></span>             | <span data-ttu-id="dffde-436">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-436">no</span></span>           |
| <span data-ttu-id="dffde-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="dffde-437">msdyn_start</span></span>                  | <span data-ttu-id="dffde-438">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-438">no</span></span>             | <span data-ttu-id="dffde-439">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-439">no</span></span>           |
| <span data-ttu-id="dffde-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="dffde-440">msdyn_taskid</span></span>                 | <span data-ttu-id="dffde-441">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-441">no</span></span>             | <span data-ttu-id="dffde-442">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-442">no</span></span>           |
| <span data-ttu-id="dffde-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="dffde-443">msdyn_taskidname</span></span>             | <span data-ttu-id="dffde-444">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-444">no</span></span>             | <span data-ttu-id="dffde-445">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-445">no</span></span>           |
| <span data-ttu-id="dffde-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="dffde-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="dffde-447">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-447">no</span></span>             | <span data-ttu-id="dffde-448">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="dffde-449">Ahli pasukan projek</span><span class="sxs-lookup"><span data-stu-id="dffde-449">Project team member</span></span>

| <span data-ttu-id="dffde-450">**Nama logik**</span><span class="sxs-lookup"><span data-stu-id="dffde-450">**Logical name**</span></span>                                 | <span data-ttu-id="dffde-451">**Boleh cipta**</span><span class="sxs-lookup"><span data-stu-id="dffde-451">**Can create**</span></span> | <span data-ttu-id="dffde-452">**Boleh edit**</span><span class="sxs-lookup"><span data-stu-id="dffde-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="dffde-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="dffde-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="dffde-454">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-454">no</span></span>             | <span data-ttu-id="dffde-455">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-455">no</span></span>           |
| <span data-ttu-id="dffde-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="dffde-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="dffde-457">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-457">no</span></span>             | <span data-ttu-id="dffde-458">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-458">no</span></span>           |
| <span data-ttu-id="dffde-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="dffde-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="dffde-460">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-460">no</span></span>             | <span data-ttu-id="dffde-461">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-461">no</span></span>           |
| <span data-ttu-id="dffde-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="dffde-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="dffde-463">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-463">no</span></span>             | <span data-ttu-id="dffde-464">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-464">no</span></span>           |
| <span data-ttu-id="dffde-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="dffde-465">msdyn_effort</span></span>                                     | <span data-ttu-id="dffde-466">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-466">no</span></span>             | <span data-ttu-id="dffde-467">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-467">no</span></span>           |
| <span data-ttu-id="dffde-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="dffde-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="dffde-469">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-469">no</span></span>             | <span data-ttu-id="dffde-470">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-470">no</span></span>           |
| <span data-ttu-id="dffde-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="dffde-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="dffde-472">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-472">no</span></span>             | <span data-ttu-id="dffde-473">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-473">no</span></span>           |
| <span data-ttu-id="dffde-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="dffde-474">msdyn_finish</span></span>                                     | <span data-ttu-id="dffde-475">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-475">no</span></span>             | <span data-ttu-id="dffde-476">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-476">no</span></span>           |
| <span data-ttu-id="dffde-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="dffde-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="dffde-478">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-478">no</span></span>             | <span data-ttu-id="dffde-479">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-479">no</span></span>           |
| <span data-ttu-id="dffde-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="dffde-480">msdyn_hours</span></span>                                      | <span data-ttu-id="dffde-481">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-481">no</span></span>             | <span data-ttu-id="dffde-482">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-482">no</span></span>           |
| <span data-ttu-id="dffde-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="dffde-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="dffde-484">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-484">no</span></span>             | <span data-ttu-id="dffde-485">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-485">no</span></span>           |
| <span data-ttu-id="dffde-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="dffde-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="dffde-487">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-487">no</span></span>             | <span data-ttu-id="dffde-488">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-488">no</span></span>           |
| <span data-ttu-id="dffde-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="dffde-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="dffde-490">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-490">no</span></span>             | <span data-ttu-id="dffde-491">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-491">no</span></span>           |
| <span data-ttu-id="dffde-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="dffde-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="dffde-493">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-493">no</span></span>             | <span data-ttu-id="dffde-494">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-494">no</span></span>           |
| <span data-ttu-id="dffde-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="dffde-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="dffde-496">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-496">no</span></span>             | <span data-ttu-id="dffde-497">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-497">no</span></span>           |
| <span data-ttu-id="dffde-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="dffde-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="dffde-499">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-499">no</span></span>             | <span data-ttu-id="dffde-500">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-500">no</span></span>           |
| <span data-ttu-id="dffde-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="dffde-501">msdyn_start</span></span>                                      | <span data-ttu-id="dffde-502">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-502">no</span></span>             | <span data-ttu-id="dffde-503">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="dffde-504">Project</span><span class="sxs-lookup"><span data-stu-id="dffde-504">Project</span></span>

| <span data-ttu-id="dffde-505">**Nama logik**</span><span class="sxs-lookup"><span data-stu-id="dffde-505">**Logical name**</span></span>                       | <span data-ttu-id="dffde-506">**Boleh cipta**</span><span class="sxs-lookup"><span data-stu-id="dffde-506">**Can create**</span></span> | <span data-ttu-id="dffde-507">**Boleh edit**</span><span class="sxs-lookup"><span data-stu-id="dffde-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="dffde-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="dffde-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="dffde-509">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-509">no</span></span>             | <span data-ttu-id="dffde-510">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-510">no</span></span>           |
| <span data-ttu-id="dffde-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="dffde-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="dffde-512">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-512">no</span></span>             | <span data-ttu-id="dffde-513">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-513">no</span></span>           |
| <span data-ttu-id="dffde-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="dffde-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="dffde-515">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-515">no</span></span>             | <span data-ttu-id="dffde-516">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-516">no</span></span>           |
| <span data-ttu-id="dffde-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="dffde-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="dffde-518">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-518">no</span></span>             | <span data-ttu-id="dffde-519">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-519">no</span></span>           |
| <span data-ttu-id="dffde-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="dffde-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="dffde-521">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-521">no</span></span>             | <span data-ttu-id="dffde-522">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-522">no</span></span>           |
| <span data-ttu-id="dffde-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="dffde-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="dffde-524">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-524">no</span></span>             | <span data-ttu-id="dffde-525">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-525">no</span></span>           |
| <span data-ttu-id="dffde-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="dffde-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="dffde-527">ya</span><span class="sxs-lookup"><span data-stu-id="dffde-527">yes</span></span>            | <span data-ttu-id="dffde-528">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-528">no</span></span>           |
| <span data-ttu-id="dffde-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="dffde-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="dffde-530">ya</span><span class="sxs-lookup"><span data-stu-id="dffde-530">yes</span></span>            | <span data-ttu-id="dffde-531">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-531">no</span></span>           |
| <span data-ttu-id="dffde-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="dffde-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="dffde-533">ya</span><span class="sxs-lookup"><span data-stu-id="dffde-533">yes</span></span>            | <span data-ttu-id="dffde-534">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-534">no</span></span>           |
| <span data-ttu-id="dffde-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="dffde-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="dffde-536">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-536">no</span></span>             | <span data-ttu-id="dffde-537">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-537">no</span></span>           |
| <span data-ttu-id="dffde-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="dffde-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="dffde-539">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-539">no</span></span>             | <span data-ttu-id="dffde-540">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-540">no</span></span>           |
| <span data-ttu-id="dffde-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="dffde-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="dffde-542">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-542">no</span></span>             | <span data-ttu-id="dffde-543">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-543">no</span></span>           |
| <span data-ttu-id="dffde-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="dffde-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="dffde-545">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-545">no</span></span>             | <span data-ttu-id="dffde-546">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-546">no</span></span>           |
| <span data-ttu-id="dffde-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="dffde-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="dffde-548">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-548">no</span></span>             | <span data-ttu-id="dffde-549">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-549">no</span></span>           |
| <span data-ttu-id="dffde-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="dffde-550">msdyn_duration</span></span>                         | <span data-ttu-id="dffde-551">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-551">no</span></span>             | <span data-ttu-id="dffde-552">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-552">no</span></span>           |
| <span data-ttu-id="dffde-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="dffde-553">msdyn_effort</span></span>                           | <span data-ttu-id="dffde-554">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-554">no</span></span>             | <span data-ttu-id="dffde-555">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-555">no</span></span>           |
| <span data-ttu-id="dffde-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="dffde-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="dffde-557">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-557">no</span></span>             | <span data-ttu-id="dffde-558">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-558">no</span></span>           |
| <span data-ttu-id="dffde-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="dffde-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="dffde-560">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-560">no</span></span>             | <span data-ttu-id="dffde-561">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-561">no</span></span>           |
| <span data-ttu-id="dffde-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="dffde-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="dffde-563">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-563">no</span></span>             | <span data-ttu-id="dffde-564">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-564">no</span></span>           |
| <span data-ttu-id="dffde-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="dffde-565">msdyn_finish</span></span>                           | <span data-ttu-id="dffde-566">ya</span><span class="sxs-lookup"><span data-stu-id="dffde-566">yes</span></span>            | <span data-ttu-id="dffde-567">ya</span><span class="sxs-lookup"><span data-stu-id="dffde-567">yes</span></span>          |
| <span data-ttu-id="dffde-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="dffde-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="dffde-569">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-569">no</span></span>             | <span data-ttu-id="dffde-570">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-570">no</span></span>           |
| <span data-ttu-id="dffde-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="dffde-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="dffde-572">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-572">no</span></span>             | <span data-ttu-id="dffde-573">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-573">no</span></span>           |
| <span data-ttu-id="dffde-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="dffde-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="dffde-575">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-575">no</span></span>             | <span data-ttu-id="dffde-576">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-576">no</span></span>           |
| <span data-ttu-id="dffde-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="dffde-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="dffde-578">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-578">no</span></span>             | <span data-ttu-id="dffde-579">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-579">no</span></span>           |
| <span data-ttu-id="dffde-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="dffde-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="dffde-581">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-581">no</span></span>             | <span data-ttu-id="dffde-582">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-582">no</span></span>           |
| <span data-ttu-id="dffde-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="dffde-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="dffde-584">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-584">no</span></span>             | <span data-ttu-id="dffde-585">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-585">no</span></span>           |
| <span data-ttu-id="dffde-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="dffde-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="dffde-587">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-587">no</span></span>             | <span data-ttu-id="dffde-588">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-588">no</span></span>           |
| <span data-ttu-id="dffde-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="dffde-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="dffde-590">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-590">no</span></span>             | <span data-ttu-id="dffde-591">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-591">no</span></span>           |
| <span data-ttu-id="dffde-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="dffde-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="dffde-593">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-593">no</span></span>             | <span data-ttu-id="dffde-594">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-594">no</span></span>           |
| <span data-ttu-id="dffde-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="dffde-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="dffde-596">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-596">no</span></span>             | <span data-ttu-id="dffde-597">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-597">no</span></span>           |
| <span data-ttu-id="dffde-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="dffde-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="dffde-599">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-599">no</span></span>             | <span data-ttu-id="dffde-600">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-600">no</span></span>           |
| <span data-ttu-id="dffde-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="dffde-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="dffde-602">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-602">no</span></span>             | <span data-ttu-id="dffde-603">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-603">no</span></span>           |
| <span data-ttu-id="dffde-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="dffde-604">msdyn_progress</span></span>                         | <span data-ttu-id="dffde-605">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-605">no</span></span>             | <span data-ttu-id="dffde-606">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-606">no</span></span>           |
| <span data-ttu-id="dffde-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="dffde-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="dffde-608">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-608">no</span></span>             | <span data-ttu-id="dffde-609">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-609">no</span></span>           |
| <span data-ttu-id="dffde-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="dffde-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="dffde-611">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-611">no</span></span>             | <span data-ttu-id="dffde-612">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-612">no</span></span>           |
| <span data-ttu-id="dffde-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="dffde-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="dffde-614">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-614">no</span></span>             | <span data-ttu-id="dffde-615">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-615">no</span></span>           |
| <span data-ttu-id="dffde-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="dffde-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="dffde-617">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-617">no</span></span>             | <span data-ttu-id="dffde-618">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-618">no</span></span>           |
| <span data-ttu-id="dffde-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="dffde-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="dffde-620">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-620">no</span></span>             | <span data-ttu-id="dffde-621">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-621">no</span></span>           |
| <span data-ttu-id="dffde-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="dffde-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="dffde-623">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-623">no</span></span>             | <span data-ttu-id="dffde-624">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-624">no</span></span>           |
| <span data-ttu-id="dffde-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="dffde-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="dffde-626">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-626">no</span></span>             | <span data-ttu-id="dffde-627">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-627">no</span></span>           |
| <span data-ttu-id="dffde-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="dffde-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="dffde-629">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-629">no</span></span>             | <span data-ttu-id="dffde-630">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-630">no</span></span>           |
| <span data-ttu-id="dffde-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="dffde-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="dffde-632">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-632">no</span></span>             | <span data-ttu-id="dffde-633">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-633">no</span></span>           |
| <span data-ttu-id="dffde-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="dffde-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="dffde-635">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-635">no</span></span>             | <span data-ttu-id="dffde-636">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-636">no</span></span>           |
| <span data-ttu-id="dffde-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="dffde-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="dffde-638">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-638">no</span></span>             | <span data-ttu-id="dffde-639">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-639">no</span></span>           |
| <span data-ttu-id="dffde-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="dffde-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="dffde-641">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-641">no</span></span>             | <span data-ttu-id="dffde-642">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-642">no</span></span>           |
| <span data-ttu-id="dffde-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="dffde-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="dffde-644">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-644">no</span></span>             | <span data-ttu-id="dffde-645">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-645">no</span></span>           |
| <span data-ttu-id="dffde-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="dffde-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="dffde-647">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-647">no</span></span>             | <span data-ttu-id="dffde-648">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-648">no</span></span>           |
| <span data-ttu-id="dffde-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="dffde-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="dffde-650">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-650">no</span></span>             | <span data-ttu-id="dffde-651">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-651">no</span></span>           |
| <span data-ttu-id="dffde-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="dffde-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="dffde-653">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-653">no</span></span>             | <span data-ttu-id="dffde-654">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-654">no</span></span>           |
| <span data-ttu-id="dffde-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="dffde-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="dffde-656">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-656">no</span></span>             | <span data-ttu-id="dffde-657">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-657">no</span></span>           |
| <span data-ttu-id="dffde-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="dffde-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="dffde-659">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-659">no</span></span>             | <span data-ttu-id="dffde-660">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-660">no</span></span>           |
| <span data-ttu-id="dffde-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="dffde-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="dffde-662">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-662">no</span></span>             | <span data-ttu-id="dffde-663">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-663">no</span></span>           |
| <span data-ttu-id="dffde-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="dffde-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="dffde-665">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-665">no</span></span>             | <span data-ttu-id="dffde-666">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-666">no</span></span>           |
| <span data-ttu-id="dffde-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="dffde-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="dffde-668">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-668">no</span></span>             | <span data-ttu-id="dffde-669">tidak</span><span class="sxs-lookup"><span data-stu-id="dffde-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="dffde-670">Pengehadan dan isu yang diketahui</span><span class="sxs-lookup"><span data-stu-id="dffde-670">Limitations and known issues</span></span>
<span data-ttu-id="dffde-671">Berikut ialah senarai pengehadan dan isu yang diketahui:</span><span class="sxs-lookup"><span data-stu-id="dffde-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="dffde-672">API Jadual Projek hanya boleh digunakan oleh **Pengguna dengan Lesen Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="dffde-672">Project Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="dffde-673">Ia tidak boleh digunakan oleh:</span><span class="sxs-lookup"><span data-stu-id="dffde-673">They can't be used by:</span></span>
    - <span data-ttu-id="dffde-674">Pengguna aplikasi</span><span class="sxs-lookup"><span data-stu-id="dffde-674">Application users</span></span>
    - <span data-ttu-id="dffde-675">Pengguna sistem</span><span class="sxs-lookup"><span data-stu-id="dffde-675">System users</span></span>
    - <span data-ttu-id="dffde-676">Pengguna integrasi</span><span class="sxs-lookup"><span data-stu-id="dffde-676">Integration users</span></span>
    - <span data-ttu-id="dffde-677">Pengguna lain yang tidak mempunyai lesen yang diperlukan</span><span class="sxs-lookup"><span data-stu-id="dffde-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="dffde-678">Setiap **OperationSet** hanya boleh mempunyai maksimum 100 operasi.</span><span class="sxs-lookup"><span data-stu-id="dffde-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="dffde-679">Setiap pengguna hanya boleh mempunyai maksimum 10 **OperationSet** terbuka.</span><span class="sxs-lookup"><span data-stu-id="dffde-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="dffde-680">Project Operations menyokong jumlah maksimum 500 tugas pada sesuatu projek pada masa ini.</span><span class="sxs-lookup"><span data-stu-id="dffde-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="dffde-681">Status kegagalan **OperationSet** dan log kegagalan tidak tersedia pada masa ini.</span><span class="sxs-lookup"><span data-stu-id="dffde-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="dffde-682">Had dan sempadan pada projek dan tugas</span><span class="sxs-lookup"><span data-stu-id="dffde-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="dffde-683">Pengendalian ralat</span><span class="sxs-lookup"><span data-stu-id="dffde-683">Error handling</span></span>

   - <span data-ttu-id="dffde-684">Untuk menyemak ralat yang dijana daripada Set Operasi, pergi ke **Tetapan** \> **Jadualkan Integrasi** \> **Set Operasi**.</span><span class="sxs-lookup"><span data-stu-id="dffde-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="dffde-685">Untuk menyemak ralat yang dijana daripada Perkhidmatan jadual Projek, pergi ke **Tetapan** \> **Integrasi Jadual** \> **Log Ralat PSS**.</span><span class="sxs-lookup"><span data-stu-id="dffde-685">To review errors generated from the Project schedule Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="dffde-686">Senario sampel</span><span class="sxs-lookup"><span data-stu-id="dffde-686">Sample scenario</span></span>

<span data-ttu-id="dffde-687">Dalam senario ini, anda akan mencipta projek, ahli pasukan, empat tugas dan dua penugasan sumber.</span><span class="sxs-lookup"><span data-stu-id="dffde-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="dffde-688">Seterusnya, anda akan mengemas kini satu tugas, mengemas kini projek, memadamkan satu tugas, memadamkan satu penugasan sumber dan mencipta pergantungan tugas.</span><span class="sxs-lookup"><span data-stu-id="dffde-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
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
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="dffde-689">Sampel tambahan</span><span class="sxs-lookup"><span data-stu-id="dffde-689">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
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
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
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
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
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
/// </summary>
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
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
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
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
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
