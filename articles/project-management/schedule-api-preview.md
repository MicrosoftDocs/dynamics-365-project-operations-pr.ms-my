---
title: Gunakan API jadual untuk melaksanakan operasi dengan entiti Penjadualan
description: Topik ini menyediakan maklumat dan sampel untuk menggunakan API Jadual.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e03f4e6c49a835206b23cade3fabe3fd26693441
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950815"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="36694-103">Gunakan API jadual untuk melaksanakan operasi dengan entiti Penjadualan</span><span class="sxs-lookup"><span data-stu-id="36694-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="36694-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="36694-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="36694-105">Sesetengah atau semua kefungsian yang dinyatakan dalam topik ini tersedia sebagai sebahagian daripada keluaran pratonton.</span><span class="sxs-lookup"><span data-stu-id="36694-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="36694-106">Kandungan dan fungsi adalah tertakluk kepada perubahan.</span><span class="sxs-lookup"><span data-stu-id="36694-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="36694-107">Entiti penjadualan</span><span class="sxs-lookup"><span data-stu-id="36694-107">Scheduling entities</span></span>

<span data-ttu-id="36694-108">Api Jadual menyediakan keupayaan untuk melaksanakan operasi mencipta, mengemas kini dan memadam dengan **Entiti penjadualan**.</span><span class="sxs-lookup"><span data-stu-id="36694-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="36694-109">Entiti ini diuruskan melalui enjin Penjadualan dalam Projek untuk web.</span><span class="sxs-lookup"><span data-stu-id="36694-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="36694-110">Operasi mencipta, mengemas kini dan memadam dengan **Entiti penjadualan** telah dihadkan dalam keluaran Dynamics 365 Project Operations sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="36694-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="36694-111">Jadual berikut menyediakan senarai lengkap **Entiti penjadualan**.</span><span class="sxs-lookup"><span data-stu-id="36694-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="36694-112">Nama entiti</span><span class="sxs-lookup"><span data-stu-id="36694-112">Entity name</span></span>  | <span data-ttu-id="36694-113">Nama logik entiti</span><span class="sxs-lookup"><span data-stu-id="36694-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="36694-114">Project</span><span class="sxs-lookup"><span data-stu-id="36694-114">Project</span></span> | <span data-ttu-id="36694-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="36694-115">msdyn_project</span></span> |
| <span data-ttu-id="36694-116">Tugas Projek</span><span class="sxs-lookup"><span data-stu-id="36694-116">Project Task</span></span>  | <span data-ttu-id="36694-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="36694-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="36694-118">Kebergantungan Tugas Projek</span><span class="sxs-lookup"><span data-stu-id="36694-118">Project Task Dependency</span></span>  | <span data-ttu-id="36694-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="36694-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="36694-120">Tugasan Sumber</span><span class="sxs-lookup"><span data-stu-id="36694-120">Resource Assignment</span></span> | <span data-ttu-id="36694-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="36694-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="36694-122">Baldi Projek</span><span class="sxs-lookup"><span data-stu-id="36694-122">Project Bucket</span></span>  | <span data-ttu-id="36694-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="36694-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="36694-124">Ahli Pasukan Projek</span><span class="sxs-lookup"><span data-stu-id="36694-124">Project Team Member</span></span> | <span data-ttu-id="36694-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="36694-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="36694-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="36694-126">OperationSet</span></span>

<span data-ttu-id="36694-127">OperationSet ialah corak unit kerja yang boleh digunakan apabila beberapa jadual yang mempengaruhi permintaan mesti diproses dalam transaksi.</span><span class="sxs-lookup"><span data-stu-id="36694-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="36694-128">API Jadual</span><span class="sxs-lookup"><span data-stu-id="36694-128">Schedule APIs</span></span>

<span data-ttu-id="36694-129">Berikut ialah senarai API Jadual semasa.</span><span class="sxs-lookup"><span data-stu-id="36694-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="36694-130">**msdyn_CreateProjectV1**: API ini boleh digunakan untuk mencipta projek.</span><span class="sxs-lookup"><span data-stu-id="36694-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="36694-131">Projek dan baldi projek lalai dicipta dengan serta-merta.</span><span class="sxs-lookup"><span data-stu-id="36694-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="36694-132">**msdyn_CreateTeamMemberV1**: API ini boleh digunakan untuk mencipta ahli pasukan projek.</span><span class="sxs-lookup"><span data-stu-id="36694-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="36694-133">Rekod ahli pasukan dicipta dengan serta-merta.</span><span class="sxs-lookup"><span data-stu-id="36694-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="36694-134">**msdyn_CreateOperationSetV1**: API ini boleh digunakan untuk menjadualkan beberapa permintaan yang mesti dilaksanakan dalam transaksi.</span><span class="sxs-lookup"><span data-stu-id="36694-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="36694-135">**msdyn_PSSCreateV1**: API ini boleh digunakan untuk mencipta entiti.</span><span class="sxs-lookup"><span data-stu-id="36694-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="36694-136">Entiti boleh jadi sebarang entiti Penjadualan yang menyokong penciptaan operasi.</span><span class="sxs-lookup"><span data-stu-id="36694-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="36694-137">**msdyn_PSSUpdateV1**: API ini boleh digunakan untuk mengemas kini entiti.</span><span class="sxs-lookup"><span data-stu-id="36694-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="36694-138">Entiti boleh jadi sebarang entiti Penjadualan yang menyokong kemas kini operasi.</span><span class="sxs-lookup"><span data-stu-id="36694-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="36694-139">**msdyn_PSSDeleteV1**: API ini boleh digunakan untuk memadamkan entiti.</span><span class="sxs-lookup"><span data-stu-id="36694-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="36694-140">Entiti boleh jadi sebarang entiti Penjadualan yang menyokong pemadaman operasi.</span><span class="sxs-lookup"><span data-stu-id="36694-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="36694-141">**msdyn_ExecuteOperationSetV1**: API ini digunakan untuk melaksanakan semua operasi dalam set operasi yang diberikan.</span><span class="sxs-lookup"><span data-stu-id="36694-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="36694-142">Menggunakan API Jadual dengan OperationSet</span><span class="sxs-lookup"><span data-stu-id="36694-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="36694-143">Kerana rekod dengan kedua-dua **CreateProjectV1** dan **CreateTeamMemberV1** dicipta dengan serta-merta, API ini tidak boleh digunakan dalam **OperationSet** secara langsung.</span><span class="sxs-lookup"><span data-stu-id="36694-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="36694-144">Walau bagaimanapun, anda boleh menggunakan API untuk mencipta rekod yang diperlukan, cipta **OperationSet** dan kemudian gunakan rekod yang dipracipta dalam **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="36694-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="36694-145">Operasi yang disokong</span><span class="sxs-lookup"><span data-stu-id="36694-145">Supported operations</span></span>

| <span data-ttu-id="36694-146">Entiti penjadualan</span><span class="sxs-lookup"><span data-stu-id="36694-146">Scheduling entity</span></span> | <span data-ttu-id="36694-147">Cipta</span><span class="sxs-lookup"><span data-stu-id="36694-147">Create</span></span> | <span data-ttu-id="36694-148">Kemas kini </span><span class="sxs-lookup"><span data-stu-id="36694-148">Update</span></span> | <span data-ttu-id="36694-149">Delete</span><span class="sxs-lookup"><span data-stu-id="36694-149">Delete</span></span> | <span data-ttu-id="36694-150">Pertimbangan penting</span><span class="sxs-lookup"><span data-stu-id="36694-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="36694-151">Tugas projek</span><span class="sxs-lookup"><span data-stu-id="36694-151">Project task</span></span> | <span data-ttu-id="36694-152">Ya</span><span class="sxs-lookup"><span data-stu-id="36694-152">Yes</span></span> | <span data-ttu-id="36694-153">Ya</span><span class="sxs-lookup"><span data-stu-id="36694-153">Yes</span></span> | <span data-ttu-id="36694-154">Ya</span><span class="sxs-lookup"><span data-stu-id="36694-154">Yes</span></span> | <span data-ttu-id="36694-155">Tiada</span><span class="sxs-lookup"><span data-stu-id="36694-155">None</span></span> |
| <span data-ttu-id="36694-156">Pergantungan tugas projek</span><span class="sxs-lookup"><span data-stu-id="36694-156">Project task dependency</span></span> | <span data-ttu-id="36694-157">Ya</span><span class="sxs-lookup"><span data-stu-id="36694-157">Yes</span></span> | <span data-ttu-id="36694-158">Ya</span><span class="sxs-lookup"><span data-stu-id="36694-158">Yes</span></span> | | <span data-ttu-id="36694-159">Rekod pergantungan tugas projek tidak dikemas kini.</span><span class="sxs-lookup"><span data-stu-id="36694-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="36694-160">Sebaliknya, rekod lama boleh dipadamkan dan rekod baharu boleh dicipta.</span><span class="sxs-lookup"><span data-stu-id="36694-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="36694-161">Penugasan sumber</span><span class="sxs-lookup"><span data-stu-id="36694-161">Resource assignment</span></span> | <span data-ttu-id="36694-162">Ya</span><span class="sxs-lookup"><span data-stu-id="36694-162">Yes</span></span> | <span data-ttu-id="36694-163">Ya</span><span class="sxs-lookup"><span data-stu-id="36694-163">Yes</span></span> | | <span data-ttu-id="36694-164">Operasi dengan medan berikut tidak disokong: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** dan **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="36694-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="36694-165">Rekod penugasan sumber tidak dikemas kini.</span><span class="sxs-lookup"><span data-stu-id="36694-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="36694-166">Sebaliknya, rekod lama boleh dipadamkan dan rekod baharu boleh dicipta.</span><span class="sxs-lookup"><span data-stu-id="36694-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="36694-167">Baldi projek</span><span class="sxs-lookup"><span data-stu-id="36694-167">Project bucket</span></span> | <span data-ttu-id="36694-168">T/B</span><span class="sxs-lookup"><span data-stu-id="36694-168">N/A</span></span> | <span data-ttu-id="36694-169">T/B</span><span class="sxs-lookup"><span data-stu-id="36694-169">N/A</span></span> | <span data-ttu-id="36694-170">T/B</span><span class="sxs-lookup"><span data-stu-id="36694-170">N/A</span></span> | <span data-ttu-id="36694-171">Baldi lalai dicipta menggunakan API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="36694-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="36694-172">Ahli pasukan projek</span><span class="sxs-lookup"><span data-stu-id="36694-172">Project team member</span></span> | <span data-ttu-id="36694-173">Ya</span><span class="sxs-lookup"><span data-stu-id="36694-173">Yes</span></span> | <span data-ttu-id="36694-174">Ya</span><span class="sxs-lookup"><span data-stu-id="36694-174">Yes</span></span> | <span data-ttu-id="36694-175">Ya</span><span class="sxs-lookup"><span data-stu-id="36694-175">Yes</span></span> | <span data-ttu-id="36694-176">Untuk mencipta operasi, gunakan API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="36694-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="36694-177">Project</span><span class="sxs-lookup"><span data-stu-id="36694-177">Project</span></span> | <span data-ttu-id="36694-178">Ya</span><span class="sxs-lookup"><span data-stu-id="36694-178">Yes</span></span> | <span data-ttu-id="36694-179">Ya</span><span class="sxs-lookup"><span data-stu-id="36694-179">Yes</span></span> | <span data-ttu-id="36694-180">T/B</span><span class="sxs-lookup"><span data-stu-id="36694-180">N/A</span></span> | <span data-ttu-id="36694-181">Operasi dengan medan berikut tidak disokong: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** dan **Duration**.</span><span class="sxs-lookup"><span data-stu-id="36694-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="36694-182">Api ini boleh dipanggil dengan objek entiti yang termasuk medan tersuai.</span><span class="sxs-lookup"><span data-stu-id="36694-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="36694-183">Sifat ID adalah pilihan.</span><span class="sxs-lookup"><span data-stu-id="36694-183">The ID property is optional.</span></span> <span data-ttu-id="36694-184">Jika ia disediakan, sistem cuba untuk menggunakannya dan memberikan pengecualian jika ia tidak boleh digunakan.</span><span class="sxs-lookup"><span data-stu-id="36694-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="36694-185">Jika ia tidak disediakan, sistem akan menjananya.</span><span class="sxs-lookup"><span data-stu-id="36694-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="36694-186">Medan terhad</span><span class="sxs-lookup"><span data-stu-id="36694-186">Restricted fields</span></span>

<span data-ttu-id="36694-187">Jadual berikut mentakrifkan medan yang terhad daripada **Cipta** dan **Edit.**</span><span class="sxs-lookup"><span data-stu-id="36694-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="36694-188">Tugas projek</span><span class="sxs-lookup"><span data-stu-id="36694-188">Project task</span></span>

| <span data-ttu-id="36694-189">**Nama logik**</span><span class="sxs-lookup"><span data-stu-id="36694-189">**Logical name**</span></span>                       | <span data-ttu-id="36694-190">**Boleh cipta**</span><span class="sxs-lookup"><span data-stu-id="36694-190">**Can create**</span></span> | <span data-ttu-id="36694-191">**Boleh edit**</span><span class="sxs-lookup"><span data-stu-id="36694-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="36694-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="36694-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="36694-193">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-193">no</span></span>             | <span data-ttu-id="36694-194">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-194">no</span></span>               |
| <span data-ttu-id="36694-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="36694-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="36694-196">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-196">no</span></span>             | <span data-ttu-id="36694-197">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-197">no</span></span>               |
| <span data-ttu-id="36694-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="36694-198">msdyn_actualend</span></span>                        | <span data-ttu-id="36694-199">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-199">no</span></span>             | <span data-ttu-id="36694-200">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-200">no</span></span>               |
| <span data-ttu-id="36694-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="36694-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="36694-202">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-202">no</span></span>             | <span data-ttu-id="36694-203">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-203">no</span></span>               |
| <span data-ttu-id="36694-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="36694-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="36694-205">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-205">no</span></span>             | <span data-ttu-id="36694-206">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-206">no</span></span>               |
| <span data-ttu-id="36694-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="36694-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="36694-208">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-208">no</span></span>             | <span data-ttu-id="36694-209">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-209">no</span></span>               |
| <span data-ttu-id="36694-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="36694-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="36694-211">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-211">no</span></span>             | <span data-ttu-id="36694-212">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-212">no</span></span>               |
| <span data-ttu-id="36694-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="36694-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="36694-214">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-214">no</span></span>             | <span data-ttu-id="36694-215">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-215">no</span></span>               |
| <span data-ttu-id="36694-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="36694-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="36694-217">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-217">no</span></span>             | <span data-ttu-id="36694-218">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-218">no</span></span>               |
| <span data-ttu-id="36694-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="36694-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="36694-220">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-220">no</span></span>             | <span data-ttu-id="36694-221">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-221">no</span></span>               |
| <span data-ttu-id="36694-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="36694-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="36694-223">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-223">no</span></span>             | <span data-ttu-id="36694-224">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-224">no</span></span>               |
| <span data-ttu-id="36694-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="36694-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="36694-226">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-226">no</span></span>             | <span data-ttu-id="36694-227">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-227">no</span></span>               |
| <span data-ttu-id="36694-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="36694-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="36694-229">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-229">no</span></span>             | <span data-ttu-id="36694-230">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-230">no</span></span>               |
| <span data-ttu-id="36694-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="36694-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="36694-232">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-232">no</span></span>             | <span data-ttu-id="36694-233">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-233">no</span></span>               |
| <span data-ttu-id="36694-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="36694-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="36694-235">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-235">no</span></span>             | <span data-ttu-id="36694-236">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-236">no</span></span>               |
| <span data-ttu-id="36694-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="36694-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="36694-238">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-238">no</span></span>             | <span data-ttu-id="36694-239">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-239">no</span></span>               |
| <span data-ttu-id="36694-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="36694-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="36694-241">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-241">no</span></span>             | <span data-ttu-id="36694-242">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-242">no</span></span>               |
| <span data-ttu-id="36694-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="36694-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="36694-244">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-244">no</span></span>             | <span data-ttu-id="36694-245">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-245">no</span></span>               |
| <span data-ttu-id="36694-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="36694-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="36694-247">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-247">no</span></span>             | <span data-ttu-id="36694-248">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-248">no</span></span>               |
| <span data-ttu-id="36694-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="36694-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="36694-250">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-250">no</span></span>             | <span data-ttu-id="36694-251">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-251">no</span></span>               |
| <span data-ttu-id="36694-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="36694-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="36694-253">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-253">no</span></span>             | <span data-ttu-id="36694-254">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-254">no</span></span>               |
| <span data-ttu-id="36694-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="36694-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="36694-256">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-256">no</span></span>             | <span data-ttu-id="36694-257">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-257">no</span></span>               |
| <span data-ttu-id="36694-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="36694-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="36694-259">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-259">no</span></span>             | <span data-ttu-id="36694-260">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-260">no</span></span>               |
| <span data-ttu-id="36694-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="36694-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="36694-262">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-262">no</span></span>             | <span data-ttu-id="36694-263">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-263">no</span></span>               |
| <span data-ttu-id="36694-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="36694-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="36694-265">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-265">no</span></span>             | <span data-ttu-id="36694-266">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-266">no</span></span>               |
| <span data-ttu-id="36694-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="36694-267">msdyn_progress</span></span>                         | <span data-ttu-id="36694-268">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-268">no</span></span>             | <span data-ttu-id="36694-269">tidak (ya untuk P4W)</span><span class="sxs-lookup"><span data-stu-id="36694-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="36694-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="36694-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="36694-271">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-271">no</span></span>             | <span data-ttu-id="36694-272">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-272">no</span></span>               |
| <span data-ttu-id="36694-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="36694-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="36694-274">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-274">no</span></span>             | <span data-ttu-id="36694-275">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-275">no</span></span>               |
| <span data-ttu-id="36694-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="36694-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="36694-277">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-277">no</span></span>             | <span data-ttu-id="36694-278">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-278">no</span></span>               |
| <span data-ttu-id="36694-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="36694-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="36694-280">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-280">no</span></span>             | <span data-ttu-id="36694-281">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-281">no</span></span>               |
| <span data-ttu-id="36694-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="36694-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="36694-283">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-283">no</span></span>             | <span data-ttu-id="36694-284">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-284">no</span></span>               |
| <span data-ttu-id="36694-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="36694-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="36694-286">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-286">no</span></span>             | <span data-ttu-id="36694-287">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-287">no</span></span>               |
| <span data-ttu-id="36694-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="36694-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="36694-289">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-289">no</span></span>             | <span data-ttu-id="36694-290">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-290">no</span></span>               |
| <span data-ttu-id="36694-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="36694-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="36694-292">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-292">no</span></span>             | <span data-ttu-id="36694-293">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-293">no</span></span>               |
| <span data-ttu-id="36694-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="36694-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="36694-295">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-295">no</span></span>             | <span data-ttu-id="36694-296">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-296">no</span></span>               |
| <span data-ttu-id="36694-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="36694-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="36694-298">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-298">no</span></span>             | <span data-ttu-id="36694-299">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-299">no</span></span>               |
| <span data-ttu-id="36694-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="36694-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="36694-301">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-301">no</span></span>             | <span data-ttu-id="36694-302">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-302">no</span></span>               |
| <span data-ttu-id="36694-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="36694-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="36694-304">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-304">no</span></span>             | <span data-ttu-id="36694-305">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-305">no</span></span>               |
| <span data-ttu-id="36694-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="36694-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="36694-307">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-307">no</span></span>             | <span data-ttu-id="36694-308">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-308">no</span></span>               |
| <span data-ttu-id="36694-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="36694-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="36694-310">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-310">no</span></span>             | <span data-ttu-id="36694-311">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-311">no</span></span>               |
| <span data-ttu-id="36694-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="36694-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="36694-313">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-313">no</span></span>             | <span data-ttu-id="36694-314">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-314">no</span></span>               |
| <span data-ttu-id="36694-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="36694-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="36694-316">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-316">no</span></span>             | <span data-ttu-id="36694-317">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-317">no</span></span>               |
| <span data-ttu-id="36694-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="36694-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="36694-319">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-319">no</span></span>             | <span data-ttu-id="36694-320">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-320">no</span></span>               |
| <span data-ttu-id="36694-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="36694-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="36694-322">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-322">no</span></span>             | <span data-ttu-id="36694-323">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-323">no</span></span>               |
| <span data-ttu-id="36694-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="36694-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="36694-325">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-325">no</span></span>             | <span data-ttu-id="36694-326">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-326">no</span></span>               |
| <span data-ttu-id="36694-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="36694-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="36694-328">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-328">no</span></span>             | <span data-ttu-id="36694-329">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-329">no</span></span>               |
| <span data-ttu-id="36694-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="36694-330">msdyn_summary</span></span>                          | <span data-ttu-id="36694-331">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-331">no</span></span>             | <span data-ttu-id="36694-332">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-332">no</span></span>               |
| <span data-ttu-id="36694-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="36694-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="36694-334">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-334">no</span></span>             | <span data-ttu-id="36694-335">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-335">no</span></span>               |
| <span data-ttu-id="36694-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="36694-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="36694-337">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-337">no</span></span>             | <span data-ttu-id="36694-338">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="36694-339">Pergantungan tugas projek</span><span class="sxs-lookup"><span data-stu-id="36694-339">Project task dependency</span></span>

| <span data-ttu-id="36694-340">**Nama logik**</span><span class="sxs-lookup"><span data-stu-id="36694-340">**Logical name**</span></span>              | <span data-ttu-id="36694-341">**Boleh cipta**</span><span class="sxs-lookup"><span data-stu-id="36694-341">**Can create**</span></span> | <span data-ttu-id="36694-342">**Boleh edit**</span><span class="sxs-lookup"><span data-stu-id="36694-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="36694-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="36694-343">msdyn_linktype</span></span>                | <span data-ttu-id="36694-344">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-344">no</span></span>             | <span data-ttu-id="36694-345">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-345">no</span></span>           |
| <span data-ttu-id="36694-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="36694-346">msdyn_linktypename</span></span>            | <span data-ttu-id="36694-347">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-347">no</span></span>             | <span data-ttu-id="36694-348">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-348">no</span></span>           |
| <span data-ttu-id="36694-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="36694-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="36694-350">ya</span><span class="sxs-lookup"><span data-stu-id="36694-350">yes</span></span>            | <span data-ttu-id="36694-351">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-351">no</span></span>           |
| <span data-ttu-id="36694-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="36694-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="36694-353">ya</span><span class="sxs-lookup"><span data-stu-id="36694-353">yes</span></span>            | <span data-ttu-id="36694-354">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-354">no</span></span>           |
| <span data-ttu-id="36694-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="36694-355">msdyn_project</span></span>                 | <span data-ttu-id="36694-356">ya</span><span class="sxs-lookup"><span data-stu-id="36694-356">yes</span></span>            | <span data-ttu-id="36694-357">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-357">no</span></span>           |
| <span data-ttu-id="36694-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="36694-358">msdyn_projectname</span></span>             | <span data-ttu-id="36694-359">ya</span><span class="sxs-lookup"><span data-stu-id="36694-359">yes</span></span>            | <span data-ttu-id="36694-360">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-360">no</span></span>           |
| <span data-ttu-id="36694-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="36694-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="36694-362">ya</span><span class="sxs-lookup"><span data-stu-id="36694-362">yes</span></span>            | <span data-ttu-id="36694-363">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-363">no</span></span>           |
| <span data-ttu-id="36694-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="36694-364">msdyn_successortask</span></span>           | <span data-ttu-id="36694-365">ya</span><span class="sxs-lookup"><span data-stu-id="36694-365">yes</span></span>            | <span data-ttu-id="36694-366">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-366">no</span></span>           |
| <span data-ttu-id="36694-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="36694-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="36694-368">ya</span><span class="sxs-lookup"><span data-stu-id="36694-368">yes</span></span>            | <span data-ttu-id="36694-369">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="36694-370">Penugasan sumber</span><span class="sxs-lookup"><span data-stu-id="36694-370">Resource assignment</span></span>

| <span data-ttu-id="36694-371">**Nama logik**</span><span class="sxs-lookup"><span data-stu-id="36694-371">**Logical name**</span></span>             | <span data-ttu-id="36694-372">**Boleh cipta**</span><span class="sxs-lookup"><span data-stu-id="36694-372">**Can create**</span></span> | <span data-ttu-id="36694-373">**Boleh edit**</span><span class="sxs-lookup"><span data-stu-id="36694-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="36694-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="36694-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="36694-375">ya</span><span class="sxs-lookup"><span data-stu-id="36694-375">yes</span></span>            | <span data-ttu-id="36694-376">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-376">no</span></span>           |
| <span data-ttu-id="36694-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="36694-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="36694-378">ya</span><span class="sxs-lookup"><span data-stu-id="36694-378">yes</span></span>            | <span data-ttu-id="36694-379">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-379">no</span></span>           |
| <span data-ttu-id="36694-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="36694-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="36694-381">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-381">no</span></span>             | <span data-ttu-id="36694-382">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-382">no</span></span>           |
| <span data-ttu-id="36694-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="36694-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="36694-384">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-384">no</span></span>             | <span data-ttu-id="36694-385">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-385">no</span></span>           |
| <span data-ttu-id="36694-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="36694-386">msdyn_committype</span></span>             | <span data-ttu-id="36694-387">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-387">no</span></span>             | <span data-ttu-id="36694-388">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-388">no</span></span>           |
| <span data-ttu-id="36694-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="36694-389">msdyn_committypename</span></span>         | <span data-ttu-id="36694-390">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-390">no</span></span>             | <span data-ttu-id="36694-391">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-391">no</span></span>           |
| <span data-ttu-id="36694-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="36694-392">msdyn_effort</span></span>                 | <span data-ttu-id="36694-393">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-393">no</span></span>             | <span data-ttu-id="36694-394">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-394">no</span></span>           |
| <span data-ttu-id="36694-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="36694-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="36694-396">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-396">no</span></span>             | <span data-ttu-id="36694-397">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-397">no</span></span>           |
| <span data-ttu-id="36694-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="36694-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="36694-399">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-399">no</span></span>             | <span data-ttu-id="36694-400">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-400">no</span></span>           |
| <span data-ttu-id="36694-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="36694-401">msdyn_finish</span></span>                 | <span data-ttu-id="36694-402">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-402">no</span></span>             | <span data-ttu-id="36694-403">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-403">no</span></span>           |
| <span data-ttu-id="36694-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="36694-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="36694-405">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-405">no</span></span>             | <span data-ttu-id="36694-406">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-406">no</span></span>           |
| <span data-ttu-id="36694-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="36694-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="36694-408">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-408">no</span></span>             | <span data-ttu-id="36694-409">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-409">no</span></span>           |
| <span data-ttu-id="36694-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="36694-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="36694-411">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-411">no</span></span>             | <span data-ttu-id="36694-412">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-412">no</span></span>           |
| <span data-ttu-id="36694-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="36694-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="36694-414">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-414">no</span></span>             | <span data-ttu-id="36694-415">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-415">no</span></span>           |
| <span data-ttu-id="36694-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="36694-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="36694-417">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-417">no</span></span>             | <span data-ttu-id="36694-418">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-418">no</span></span>           |
| <span data-ttu-id="36694-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="36694-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="36694-420">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-420">no</span></span>             | <span data-ttu-id="36694-421">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-421">no</span></span>           |
| <span data-ttu-id="36694-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="36694-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="36694-423">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-423">no</span></span>             | <span data-ttu-id="36694-424">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-424">no</span></span>           |
| <span data-ttu-id="36694-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="36694-425">msdyn_projectid</span></span>              | <span data-ttu-id="36694-426">ya</span><span class="sxs-lookup"><span data-stu-id="36694-426">yes</span></span>            | <span data-ttu-id="36694-427">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-427">no</span></span>           |
| <span data-ttu-id="36694-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="36694-428">msdyn_projectidname</span></span>          | <span data-ttu-id="36694-429">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-429">no</span></span>             | <span data-ttu-id="36694-430">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-430">no</span></span>           |
| <span data-ttu-id="36694-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="36694-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="36694-432">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-432">no</span></span>             | <span data-ttu-id="36694-433">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-433">no</span></span>           |
| <span data-ttu-id="36694-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="36694-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="36694-435">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-435">no</span></span>             | <span data-ttu-id="36694-436">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-436">no</span></span>           |
| <span data-ttu-id="36694-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="36694-437">msdyn_start</span></span>                  | <span data-ttu-id="36694-438">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-438">no</span></span>             | <span data-ttu-id="36694-439">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-439">no</span></span>           |
| <span data-ttu-id="36694-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="36694-440">msdyn_taskid</span></span>                 | <span data-ttu-id="36694-441">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-441">no</span></span>             | <span data-ttu-id="36694-442">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-442">no</span></span>           |
| <span data-ttu-id="36694-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="36694-443">msdyn_taskidname</span></span>             | <span data-ttu-id="36694-444">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-444">no</span></span>             | <span data-ttu-id="36694-445">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-445">no</span></span>           |
| <span data-ttu-id="36694-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="36694-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="36694-447">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-447">no</span></span>             | <span data-ttu-id="36694-448">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="36694-449">Ahli pasukan projek</span><span class="sxs-lookup"><span data-stu-id="36694-449">Project team member</span></span>

| <span data-ttu-id="36694-450">**Nama logik**</span><span class="sxs-lookup"><span data-stu-id="36694-450">**Logical name**</span></span>                                 | <span data-ttu-id="36694-451">**Boleh cipta**</span><span class="sxs-lookup"><span data-stu-id="36694-451">**Can create**</span></span> | <span data-ttu-id="36694-452">**Boleh edit**</span><span class="sxs-lookup"><span data-stu-id="36694-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="36694-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="36694-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="36694-454">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-454">no</span></span>             | <span data-ttu-id="36694-455">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-455">no</span></span>           |
| <span data-ttu-id="36694-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="36694-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="36694-457">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-457">no</span></span>             | <span data-ttu-id="36694-458">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-458">no</span></span>           |
| <span data-ttu-id="36694-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="36694-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="36694-460">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-460">no</span></span>             | <span data-ttu-id="36694-461">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-461">no</span></span>           |
| <span data-ttu-id="36694-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="36694-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="36694-463">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-463">no</span></span>             | <span data-ttu-id="36694-464">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-464">no</span></span>           |
| <span data-ttu-id="36694-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="36694-465">msdyn_effort</span></span>                                     | <span data-ttu-id="36694-466">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-466">no</span></span>             | <span data-ttu-id="36694-467">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-467">no</span></span>           |
| <span data-ttu-id="36694-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="36694-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="36694-469">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-469">no</span></span>             | <span data-ttu-id="36694-470">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-470">no</span></span>           |
| <span data-ttu-id="36694-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="36694-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="36694-472">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-472">no</span></span>             | <span data-ttu-id="36694-473">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-473">no</span></span>           |
| <span data-ttu-id="36694-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="36694-474">msdyn_finish</span></span>                                     | <span data-ttu-id="36694-475">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-475">no</span></span>             | <span data-ttu-id="36694-476">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-476">no</span></span>           |
| <span data-ttu-id="36694-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="36694-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="36694-478">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-478">no</span></span>             | <span data-ttu-id="36694-479">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-479">no</span></span>           |
| <span data-ttu-id="36694-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="36694-480">msdyn_hours</span></span>                                      | <span data-ttu-id="36694-481">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-481">no</span></span>             | <span data-ttu-id="36694-482">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-482">no</span></span>           |
| <span data-ttu-id="36694-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="36694-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="36694-484">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-484">no</span></span>             | <span data-ttu-id="36694-485">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-485">no</span></span>           |
| <span data-ttu-id="36694-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="36694-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="36694-487">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-487">no</span></span>             | <span data-ttu-id="36694-488">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-488">no</span></span>           |
| <span data-ttu-id="36694-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="36694-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="36694-490">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-490">no</span></span>             | <span data-ttu-id="36694-491">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-491">no</span></span>           |
| <span data-ttu-id="36694-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="36694-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="36694-493">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-493">no</span></span>             | <span data-ttu-id="36694-494">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-494">no</span></span>           |
| <span data-ttu-id="36694-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="36694-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="36694-496">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-496">no</span></span>             | <span data-ttu-id="36694-497">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-497">no</span></span>           |
| <span data-ttu-id="36694-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="36694-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="36694-499">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-499">no</span></span>             | <span data-ttu-id="36694-500">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-500">no</span></span>           |
| <span data-ttu-id="36694-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="36694-501">msdyn_start</span></span>                                      | <span data-ttu-id="36694-502">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-502">no</span></span>             | <span data-ttu-id="36694-503">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="36694-504">Project</span><span class="sxs-lookup"><span data-stu-id="36694-504">Project</span></span>

| <span data-ttu-id="36694-505">**Nama logik**</span><span class="sxs-lookup"><span data-stu-id="36694-505">**Logical name**</span></span>                       | <span data-ttu-id="36694-506">**Boleh cipta**</span><span class="sxs-lookup"><span data-stu-id="36694-506">**Can create**</span></span> | <span data-ttu-id="36694-507">**Boleh edit**</span><span class="sxs-lookup"><span data-stu-id="36694-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="36694-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="36694-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="36694-509">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-509">no</span></span>             | <span data-ttu-id="36694-510">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-510">no</span></span>           |
| <span data-ttu-id="36694-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="36694-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="36694-512">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-512">no</span></span>             | <span data-ttu-id="36694-513">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-513">no</span></span>           |
| <span data-ttu-id="36694-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="36694-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="36694-515">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-515">no</span></span>             | <span data-ttu-id="36694-516">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-516">no</span></span>           |
| <span data-ttu-id="36694-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="36694-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="36694-518">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-518">no</span></span>             | <span data-ttu-id="36694-519">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-519">no</span></span>           |
| <span data-ttu-id="36694-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="36694-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="36694-521">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-521">no</span></span>             | <span data-ttu-id="36694-522">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-522">no</span></span>           |
| <span data-ttu-id="36694-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="36694-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="36694-524">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-524">no</span></span>             | <span data-ttu-id="36694-525">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-525">no</span></span>           |
| <span data-ttu-id="36694-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="36694-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="36694-527">ya</span><span class="sxs-lookup"><span data-stu-id="36694-527">yes</span></span>            | <span data-ttu-id="36694-528">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-528">no</span></span>           |
| <span data-ttu-id="36694-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="36694-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="36694-530">ya</span><span class="sxs-lookup"><span data-stu-id="36694-530">yes</span></span>            | <span data-ttu-id="36694-531">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-531">no</span></span>           |
| <span data-ttu-id="36694-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="36694-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="36694-533">ya</span><span class="sxs-lookup"><span data-stu-id="36694-533">yes</span></span>            | <span data-ttu-id="36694-534">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-534">no</span></span>           |
| <span data-ttu-id="36694-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="36694-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="36694-536">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-536">no</span></span>             | <span data-ttu-id="36694-537">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-537">no</span></span>           |
| <span data-ttu-id="36694-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="36694-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="36694-539">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-539">no</span></span>             | <span data-ttu-id="36694-540">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-540">no</span></span>           |
| <span data-ttu-id="36694-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="36694-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="36694-542">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-542">no</span></span>             | <span data-ttu-id="36694-543">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-543">no</span></span>           |
| <span data-ttu-id="36694-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="36694-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="36694-545">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-545">no</span></span>             | <span data-ttu-id="36694-546">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-546">no</span></span>           |
| <span data-ttu-id="36694-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="36694-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="36694-548">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-548">no</span></span>             | <span data-ttu-id="36694-549">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-549">no</span></span>           |
| <span data-ttu-id="36694-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="36694-550">msdyn_duration</span></span>                         | <span data-ttu-id="36694-551">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-551">no</span></span>             | <span data-ttu-id="36694-552">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-552">no</span></span>           |
| <span data-ttu-id="36694-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="36694-553">msdyn_effort</span></span>                           | <span data-ttu-id="36694-554">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-554">no</span></span>             | <span data-ttu-id="36694-555">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-555">no</span></span>           |
| <span data-ttu-id="36694-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="36694-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="36694-557">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-557">no</span></span>             | <span data-ttu-id="36694-558">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-558">no</span></span>           |
| <span data-ttu-id="36694-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="36694-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="36694-560">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-560">no</span></span>             | <span data-ttu-id="36694-561">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-561">no</span></span>           |
| <span data-ttu-id="36694-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="36694-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="36694-563">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-563">no</span></span>             | <span data-ttu-id="36694-564">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-564">no</span></span>           |
| <span data-ttu-id="36694-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="36694-565">msdyn_finish</span></span>                           | <span data-ttu-id="36694-566">ya</span><span class="sxs-lookup"><span data-stu-id="36694-566">yes</span></span>            | <span data-ttu-id="36694-567">ya</span><span class="sxs-lookup"><span data-stu-id="36694-567">yes</span></span>          |
| <span data-ttu-id="36694-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="36694-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="36694-569">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-569">no</span></span>             | <span data-ttu-id="36694-570">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-570">no</span></span>           |
| <span data-ttu-id="36694-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="36694-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="36694-572">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-572">no</span></span>             | <span data-ttu-id="36694-573">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-573">no</span></span>           |
| <span data-ttu-id="36694-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="36694-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="36694-575">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-575">no</span></span>             | <span data-ttu-id="36694-576">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-576">no</span></span>           |
| <span data-ttu-id="36694-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="36694-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="36694-578">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-578">no</span></span>             | <span data-ttu-id="36694-579">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-579">no</span></span>           |
| <span data-ttu-id="36694-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="36694-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="36694-581">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-581">no</span></span>             | <span data-ttu-id="36694-582">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-582">no</span></span>           |
| <span data-ttu-id="36694-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="36694-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="36694-584">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-584">no</span></span>             | <span data-ttu-id="36694-585">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-585">no</span></span>           |
| <span data-ttu-id="36694-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="36694-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="36694-587">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-587">no</span></span>             | <span data-ttu-id="36694-588">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-588">no</span></span>           |
| <span data-ttu-id="36694-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="36694-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="36694-590">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-590">no</span></span>             | <span data-ttu-id="36694-591">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-591">no</span></span>           |
| <span data-ttu-id="36694-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="36694-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="36694-593">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-593">no</span></span>             | <span data-ttu-id="36694-594">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-594">no</span></span>           |
| <span data-ttu-id="36694-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="36694-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="36694-596">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-596">no</span></span>             | <span data-ttu-id="36694-597">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-597">no</span></span>           |
| <span data-ttu-id="36694-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="36694-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="36694-599">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-599">no</span></span>             | <span data-ttu-id="36694-600">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-600">no</span></span>           |
| <span data-ttu-id="36694-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="36694-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="36694-602">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-602">no</span></span>             | <span data-ttu-id="36694-603">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-603">no</span></span>           |
| <span data-ttu-id="36694-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="36694-604">msdyn_progress</span></span>                         | <span data-ttu-id="36694-605">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-605">no</span></span>             | <span data-ttu-id="36694-606">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-606">no</span></span>           |
| <span data-ttu-id="36694-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="36694-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="36694-608">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-608">no</span></span>             | <span data-ttu-id="36694-609">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-609">no</span></span>           |
| <span data-ttu-id="36694-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="36694-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="36694-611">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-611">no</span></span>             | <span data-ttu-id="36694-612">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-612">no</span></span>           |
| <span data-ttu-id="36694-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="36694-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="36694-614">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-614">no</span></span>             | <span data-ttu-id="36694-615">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-615">no</span></span>           |
| <span data-ttu-id="36694-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="36694-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="36694-617">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-617">no</span></span>             | <span data-ttu-id="36694-618">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-618">no</span></span>           |
| <span data-ttu-id="36694-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="36694-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="36694-620">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-620">no</span></span>             | <span data-ttu-id="36694-621">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-621">no</span></span>           |
| <span data-ttu-id="36694-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="36694-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="36694-623">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-623">no</span></span>             | <span data-ttu-id="36694-624">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-624">no</span></span>           |
| <span data-ttu-id="36694-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="36694-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="36694-626">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-626">no</span></span>             | <span data-ttu-id="36694-627">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-627">no</span></span>           |
| <span data-ttu-id="36694-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="36694-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="36694-629">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-629">no</span></span>             | <span data-ttu-id="36694-630">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-630">no</span></span>           |
| <span data-ttu-id="36694-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="36694-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="36694-632">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-632">no</span></span>             | <span data-ttu-id="36694-633">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-633">no</span></span>           |
| <span data-ttu-id="36694-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="36694-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="36694-635">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-635">no</span></span>             | <span data-ttu-id="36694-636">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-636">no</span></span>           |
| <span data-ttu-id="36694-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="36694-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="36694-638">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-638">no</span></span>             | <span data-ttu-id="36694-639">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-639">no</span></span>           |
| <span data-ttu-id="36694-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="36694-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="36694-641">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-641">no</span></span>             | <span data-ttu-id="36694-642">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-642">no</span></span>           |
| <span data-ttu-id="36694-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="36694-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="36694-644">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-644">no</span></span>             | <span data-ttu-id="36694-645">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-645">no</span></span>           |
| <span data-ttu-id="36694-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="36694-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="36694-647">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-647">no</span></span>             | <span data-ttu-id="36694-648">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-648">no</span></span>           |
| <span data-ttu-id="36694-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="36694-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="36694-650">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-650">no</span></span>             | <span data-ttu-id="36694-651">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-651">no</span></span>           |
| <span data-ttu-id="36694-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="36694-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="36694-653">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-653">no</span></span>             | <span data-ttu-id="36694-654">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-654">no</span></span>           |
| <span data-ttu-id="36694-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="36694-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="36694-656">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-656">no</span></span>             | <span data-ttu-id="36694-657">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-657">no</span></span>           |
| <span data-ttu-id="36694-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="36694-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="36694-659">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-659">no</span></span>             | <span data-ttu-id="36694-660">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-660">no</span></span>           |
| <span data-ttu-id="36694-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="36694-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="36694-662">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-662">no</span></span>             | <span data-ttu-id="36694-663">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-663">no</span></span>           |
| <span data-ttu-id="36694-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="36694-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="36694-665">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-665">no</span></span>             | <span data-ttu-id="36694-666">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-666">no</span></span>           |
| <span data-ttu-id="36694-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="36694-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="36694-668">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-668">no</span></span>             | <span data-ttu-id="36694-669">tidak</span><span class="sxs-lookup"><span data-stu-id="36694-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="36694-670">Pengehadan dan isu yang diketahui</span><span class="sxs-lookup"><span data-stu-id="36694-670">Limitations and known issues</span></span>
<span data-ttu-id="36694-671">Berikut ialah senarai pengehadan dan isu yang diketahui:</span><span class="sxs-lookup"><span data-stu-id="36694-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="36694-672">API Jadual hanya boleh digunakan oleh **Pengguna dengan Lesen Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="36694-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="36694-673">Ia tidak boleh digunakan oleh:</span><span class="sxs-lookup"><span data-stu-id="36694-673">They can't be used by:</span></span>
    - <span data-ttu-id="36694-674">Pengguna aplikasi</span><span class="sxs-lookup"><span data-stu-id="36694-674">Application users</span></span>
    - <span data-ttu-id="36694-675">Pengguna sistem</span><span class="sxs-lookup"><span data-stu-id="36694-675">System users</span></span>
    - <span data-ttu-id="36694-676">Pengguna integrasi</span><span class="sxs-lookup"><span data-stu-id="36694-676">Integration users</span></span>
    - <span data-ttu-id="36694-677">Pengguna lain yang tidak mempunyai lesen yang diperlukan</span><span class="sxs-lookup"><span data-stu-id="36694-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="36694-678">Setiap **OperationSet** hanya boleh mempunyai maksimum 100 operasi.</span><span class="sxs-lookup"><span data-stu-id="36694-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="36694-679">Setiap pengguna hanya boleh mempunyai maksimum 10 **OperationSet** terbuka.</span><span class="sxs-lookup"><span data-stu-id="36694-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="36694-680">Project Operations menyokong jumlah maksimum 500 tugas pada sesuatu projek pada masa ini.</span><span class="sxs-lookup"><span data-stu-id="36694-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="36694-681">Status kegagalan **OperationSet** dan log kegagalan tidak tersedia pada masa ini.</span><span class="sxs-lookup"><span data-stu-id="36694-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="36694-682">API Jadual dalam Pratonton awam.</span><span class="sxs-lookup"><span data-stu-id="36694-682">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="36694-683">Penggunaan API ini dalam Persekitaran pengeluaran tidak disokong oleh Microsoft.</span><span class="sxs-lookup"><span data-stu-id="36694-683">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>
- [<span data-ttu-id="36694-684">Had dan sempadan pada projek dan tugas</span><span class="sxs-lookup"><span data-stu-id="36694-684">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="36694-685">Pengendalian ralat</span><span class="sxs-lookup"><span data-stu-id="36694-685">Error handling</span></span>

   - <span data-ttu-id="36694-686">Untuk menyemak ralat yang dijana daripada Set Operasi, pergi ke **Tetapan** \> **Jadualkan Integrasi** \> **Set Operasi**.</span><span class="sxs-lookup"><span data-stu-id="36694-686">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="36694-687">Untuk menyemak ralat yang dijana daripada Perkhidmatan Penjadualan Projek, pergi ke **Tetapan** \> **Jadualkan Integrasi** \> **Log Ralat PSS**.</span><span class="sxs-lookup"><span data-stu-id="36694-687">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="36694-688">Senario sampel</span><span class="sxs-lookup"><span data-stu-id="36694-688">Sample scenario</span></span>

<span data-ttu-id="36694-689">Dalam senario ini, anda akan mencipta projek, ahli pasukan, empat tugas dan dua penugasan sumber.</span><span class="sxs-lookup"><span data-stu-id="36694-689">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="36694-690">Seterusnya, anda akan mengemas kini satu tugas, mengemas kini projek, memadamkan satu tugas, memadamkan satu penugasan sumber dan mencipta pergantungan tugas.</span><span class="sxs-lookup"><span data-stu-id="36694-690">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="36694-691">Sampel tambahan</span><span class="sxs-lookup"><span data-stu-id="36694-691">Additional samples</span></span>

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
