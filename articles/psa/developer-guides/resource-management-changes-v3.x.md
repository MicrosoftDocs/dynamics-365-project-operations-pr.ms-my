---
title: Perubahan pengurusan sumber (Project Service Automation 3.x)
description: Topik ini memberikan maklumat tentang perubahan pada kawasan pengurusan Sumber.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5f88d7309a5e1171629a72e749bfc01abb64c62a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284774"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="ff583-103">Perubahan pengurusan sumber (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="ff583-103">Resource management changes (Project Service Automation 3.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

<span data-ttu-id="ff583-104">Bahagian topik ini menyediakan maklumat mengenai perubahan yang telah dibuat ke kawasan pengurusan Sumber Dynamics 365 Project Service Automation versi 3. x.</span><span class="sxs-lookup"><span data-stu-id="ff583-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="ff583-105">Anggaran projek</span><span class="sxs-lookup"><span data-stu-id="ff583-105">Project estimates</span></span>

<span data-ttu-id="ff583-106">Selain daripada yang berasaskan entiti **msdyn\_projecttask** (**Tugas Projek**), anggaran projek adalah berdasarkan kepada entiti **msdyn\_resourceassignment** (**Tugasan sumber**).</span><span class="sxs-lookup"><span data-stu-id="ff583-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="ff583-107">Tugasan sumber telah menjadi "sumber kebenaran" untuk penjadualan tugas dan penetapan harga.</span><span class="sxs-lookup"><span data-stu-id="ff583-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="ff583-108">Tugas talian</span><span class="sxs-lookup"><span data-stu-id="ff583-108">Line tasks</span></span>

<span data-ttu-id="ff583-109">Dalam PSA 3. x, tugas talian adalah usang (ditamatkan).</span><span class="sxs-lookup"><span data-stu-id="ff583-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="ff583-110">Tugasan sekarang menunjuk ke tugas keseluruhan bukan tugas talian.</span><span class="sxs-lookup"><span data-stu-id="ff583-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="ff583-111">Contoh berikut menunjukkan cara tugas yang dinamakan "Tugas Ujian" ditugaskan kepada ahli pasukan A dan B dalam versi awal PSA dan dalam PSA 3. x.</span><span class="sxs-lookup"><span data-stu-id="ff583-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="ff583-112">**Sebelum PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="ff583-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="ff583-113">Tugas ujian</span><span class="sxs-lookup"><span data-stu-id="ff583-113">Test task</span></span>

        - <span data-ttu-id="ff583-114">Tugas ujian – Tugas talian 1</span><span class="sxs-lookup"><span data-stu-id="ff583-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="ff583-115">Tugasan ke A</span><span class="sxs-lookup"><span data-stu-id="ff583-115">Assignment to A</span></span>

        - <span data-ttu-id="ff583-116">Tugas ujian – Tugas talian 2</span><span class="sxs-lookup"><span data-stu-id="ff583-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="ff583-117">Tugasan ke B</span><span class="sxs-lookup"><span data-stu-id="ff583-117">Assignment to B</span></span>

- <span data-ttu-id="ff583-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="ff583-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="ff583-119">Tugas ujian</span><span class="sxs-lookup"><span data-stu-id="ff583-119">Test task</span></span>

        - <span data-ttu-id="ff583-120">Tugasan ke A</span><span class="sxs-lookup"><span data-stu-id="ff583-120">Assignment to A</span></span>
        - <span data-ttu-id="ff583-121">Tugasan ke B</span><span class="sxs-lookup"><span data-stu-id="ff583-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="ff583-122">Tugasan yang tidak ditugaskan</span><span class="sxs-lookup"><span data-stu-id="ff583-122">Unassigned assignment</span></span>

<span data-ttu-id="ff583-123">Dalam PSA 3.x, tugasan yang tidak ditugaskan ialah tugasan yang ditugaskan kepada ahli pasukan yang **TIDAK** batal dan sumber **TIDAK**.</span><span class="sxs-lookup"><span data-stu-id="ff583-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="ff583-124">Tugasan yang tidak ditugaskan boleh berlaku dalam beberapa senario:</span><span class="sxs-lookup"><span data-stu-id="ff583-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="ff583-125">Jika tugas telah dicipta tetapi belum ditugaskan kepada mana-mana ahli pasukan, penyerahan tugas yang tidak ditugaskan sentiasa dicipta.</span><span class="sxs-lookup"><span data-stu-id="ff583-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="ff583-126">Jika semua penugas pada tugas dikeluarkan, tugasan yang tidak ditugaskan telah dicipta semula untuk tugas tersebut.</span><span class="sxs-lookup"><span data-stu-id="ff583-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="ff583-127">Medan penjadualan pada entiti Tugas Projek</span><span class="sxs-lookup"><span data-stu-id="ff583-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="ff583-128">Medan pada **entiti msdyn\_projecttask** telah ditamatkan atau dipindahkan ke entiti **msdyn\_resourceassignment** atau ia kini dirujuk daripada entiti **msdyn\_projectteam**(**Ahli Pasukan Projek**).</span><span class="sxs-lookup"><span data-stu-id="ff583-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="ff583-129">Medan ditamatkan pada msdyn\_projecttask (Tugas projek)</span><span class="sxs-lookup"><span data-stu-id="ff583-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="ff583-130">Medan baharu tentang msdyn\_resourceassignment (Tugasan Sumber)</span><span class="sxs-lookup"><span data-stu-id="ff583-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="ff583-131">Komen</span><span class="sxs-lookup"><span data-stu-id="ff583-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="ff583-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="ff583-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="ff583-133">Tiada</span><span class="sxs-lookup"><span data-stu-id="ff583-133">None</span></span> | |
| <span data-ttu-id="ff583-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="ff583-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="ff583-135">Tiada</span><span class="sxs-lookup"><span data-stu-id="ff583-135">None</span></span> | |
| <span data-ttu-id="ff583-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="ff583-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="ff583-137">Tiada</span><span class="sxs-lookup"><span data-stu-id="ff583-137">None</span></span> | |
| <span data-ttu-id="ff583-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="ff583-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="ff583-139">Tiada</span><span class="sxs-lookup"><span data-stu-id="ff583-139">None</span></span> | |
| <span data-ttu-id="ff583-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="ff583-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="ff583-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="ff583-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="ff583-142">Format struktur data Nota Objek JavaScript (JSON) yang disimpan dalam medan telah ditukar.</span><span class="sxs-lookup"><span data-stu-id="ff583-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="ff583-143">Jadual kontur</span><span class="sxs-lookup"><span data-stu-id="ff583-143">Schedule contour</span></span>

<span data-ttu-id="ff583-144">Kontur jadual tersebut disimpan dalam medan **Kerja Terancang** (**msdyn\_plannedwork**) bagi setiap entiti **Tugasan Sumber**(**msdyn\_sumber**).</span><span class="sxs-lookup"><span data-stu-id="ff583-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="ff583-145">Struktur</span><span class="sxs-lookup"><span data-stu-id="ff583-145">Structure</span></span>

<span data-ttu-id="ff583-146">Struktur baharu jadual kontur terdiri daripada hirisan masa fleksibel yang ditakrifkan untuk setiap hari jadual.</span><span class="sxs-lookup"><span data-stu-id="ff583-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="ff583-147">Setiap hirisan masa mempunyai sifat berikut:</span><span class="sxs-lookup"><span data-stu-id="ff583-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="ff583-148">**Mulakan** – Bermulanya waktu kerja untuk hari tersebut, mengikut kalendar projek.</span><span class="sxs-lookup"><span data-stu-id="ff583-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="ff583-149">**Akhir** – Berakhirnya waktu kerja untuk hari tersebut, mengikut kalendar projek.</span><span class="sxs-lookup"><span data-stu-id="ff583-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="ff583-150">**Jam** – Bilangan jam yang ditugaskan pada hari tersebut.</span><span class="sxs-lookup"><span data-stu-id="ff583-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="ff583-151">**Contoh**</span><span class="sxs-lookup"><span data-stu-id="ff583-151">**Example**</span></span>

<span data-ttu-id="ff583-152">Contoh ini menggunakan kalendar projek di mana hari kerja adalah dari jam 9 pagi hingga 5 petang dalam zon waktu UTC-8.</span><span class="sxs-lookup"><span data-stu-id="ff583-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="ff583-153">Penjadualan automatik dan penjadualan manual</span><span class="sxs-lookup"><span data-stu-id="ff583-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="ff583-154">Jika tugas dijadualkan secara automatik, waktu yang dimuatkan depan dan tempoh tugas mungkin dikurangkan.</span><span class="sxs-lookup"><span data-stu-id="ff583-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="ff583-155">**Contoh**</span><span class="sxs-lookup"><span data-stu-id="ff583-155">**Example**</span></span>

<span data-ttu-id="ff583-156">Tugas berikut adalah dijadualkan secara automatik selama 18 jam untuk tiga hari (3 Disember, 2018, hingga 5 Disember, 2018).</span><span class="sxs-lookup"><span data-stu-id="ff583-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="ff583-157">Jika sesuatu tugas dijadualkan secara manual, waktu secara sekata diedarkan kepada semua tarikh.</span><span class="sxs-lookup"><span data-stu-id="ff583-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="ff583-158">**Contoh**</span><span class="sxs-lookup"><span data-stu-id="ff583-158">**Example**</span></span>

<span data-ttu-id="ff583-159">Tugas berikut adalah dijadualkan secara manual selama 18 jam untuk tiga hari (3 Disember, 2018, hingga 5 Disember, 2018).</span><span class="sxs-lookup"><span data-stu-id="ff583-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="ff583-160">Unit tugasan</span><span class="sxs-lookup"><span data-stu-id="ff583-160">Assignment unit</span></span>

<span data-ttu-id="ff583-161">Unit tugasan telah ditamatkan dalam PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="ff583-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="ff583-162">Masa kerja kerja kini juga dibahagikan sama rata, setiap hari, antara semua sumber yang ditugaskan.</span><span class="sxs-lookup"><span data-stu-id="ff583-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="ff583-163">**Contoh**</span><span class="sxs-lookup"><span data-stu-id="ff583-163">**Example**</span></span>

<span data-ttu-id="ff583-164">Dalam contoh ini, tugas itu ditugaskan kepada dua sumber dan dijadualkan automatik untuk 36 jam untuk tiga hari (3 Disember, 2018, hingga 5 Disember, 2018).</span><span class="sxs-lookup"><span data-stu-id="ff583-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="ff583-165">Tugasan 1:</span><span class="sxs-lookup"><span data-stu-id="ff583-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="ff583-166">Tugasan 2:</span><span class="sxs-lookup"><span data-stu-id="ff583-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="ff583-167">Dimensi penentuan harga</span><span class="sxs-lookup"><span data-stu-id="ff583-167">Pricing dimensions</span></span>

<span data-ttu-id="ff583-168">Dalam PSA 3.x, medan dimensi penetapan harga khusus (seperti **Peranan** dan **Unit Organisasi**) telah dialih keluar daripada entiti **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="ff583-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="ff583-169">Medan ini kini boleh diambil daripada ahli pasukan projek yang berkaitan (**msdyn\_projectteam**) daripada tugasan sumber (**msdyn\_resourceassignment**) apabila anggaran projek dijana.</span><span class="sxs-lookup"><span data-stu-id="ff583-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="ff583-170">Medan baharu, **msdyn\_organizationalunit**, telah ditambah kepada entiti **msdyn\_projectteam**.</span><span class="sxs-lookup"><span data-stu-id="ff583-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="ff583-171">Medan ditamatkan pada msdyn\_projecttask (Tugas projek)</span><span class="sxs-lookup"><span data-stu-id="ff583-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="ff583-172">Medan daripada msdyn\_projectteam (Ahli Pasukan Projek) yang digunakan sebagai ganti</span><span class="sxs-lookup"><span data-stu-id="ff583-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="ff583-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="ff583-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="ff583-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="ff583-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="ff583-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="ff583-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="ff583-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="ff583-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="ff583-177">Kontur</span><span class="sxs-lookup"><span data-stu-id="ff583-177">Contours</span></span>

<span data-ttu-id="ff583-178">Penetapan harga dan penganggaran medan kontur telah ditamatkan pada entiti **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="ff583-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="ff583-179">Mereka telah dipindahkan ke entiti **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="ff583-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="ff583-180">Medan ditamatkan pada msdyn\_projecttask (Tugas projek)</span><span class="sxs-lookup"><span data-stu-id="ff583-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="ff583-181">Medan baharu tentang msdyn\_resourceassignment (Tugasan Sumber)</span><span class="sxs-lookup"><span data-stu-id="ff583-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="ff583-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="ff583-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="ff583-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="ff583-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="ff583-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="ff583-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="ff583-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="ff583-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="ff583-186">Medan berikut ditambah ke entiti **msdyn\_resourceassignment**:</span><span class="sxs-lookup"><span data-stu-id="ff583-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="ff583-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="ff583-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="ff583-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="ff583-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="ff583-189">Medan berikut untuk dirancang, sebenar dan baki kos dan jualan tidak berubah pada entiti **msdyn\_projecttask**:</span><span class="sxs-lookup"><span data-stu-id="ff583-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="ff583-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="ff583-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="ff583-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="ff583-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="ff583-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="ff583-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="ff583-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="ff583-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="ff583-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="ff583-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="ff583-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="ff583-195">msdyn\_remainingsales</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]