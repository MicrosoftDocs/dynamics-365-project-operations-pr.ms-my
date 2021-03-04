---
title: Kemajuan projek dan penggunaan kos
description: Topik ini memberikan maklumat tentang penjejakan kemajuan projek dan penggunaan kos.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0b69cee49e028b98bbb32e4a7e7aedf5479527dc
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148024"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="f2266-103">Kemajuan projek dan penggunaan kos</span><span class="sxs-lookup"><span data-stu-id="f2266-103">Project progress and cost consumption</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f2266-104">Keperluan untuk menjejaki kemajuan terhadap jadual berbeza-beza mengikut industri.</span><span class="sxs-lookup"><span data-stu-id="f2266-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="f2266-105">Sesetengah industri menjejaki pada tahap butiran, manakala industri lain menjejaki pada tahap yang lebih tinggi.</span><span class="sxs-lookup"><span data-stu-id="f2266-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="f2266-106">Topik ini menunjukkan cara untuk menjadualkan bagi memenuhi keperluan organisasi anda.</span><span class="sxs-lookup"><span data-stu-id="f2266-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="f2266-107">Pandangan penjejakan usaha</span><span class="sxs-lookup"><span data-stu-id="f2266-107">Effort tracking view</span></span>

<span data-ttu-id="f2266-108">Pandangan **Penjejakan usaha** menjejaki kemajuan tugas dalam jadual.</span><span class="sxs-lookup"><span data-stu-id="f2266-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="f2266-109">Ia membandingkan jam usaha sebenar yang dihabiskan pada satu tugas dengan jam usaha yang dirancang bagi tugas tersebut.</span><span class="sxs-lookup"><span data-stu-id="f2266-109">It compares the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="f2266-110">Project Service Automation menggunakan formula berikut untuk mengira metrik penjejakan:</span><span class="sxs-lookup"><span data-stu-id="f2266-110">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="f2266-111">Di awal penciptaan tugas: Kos yang dirancang akan ditetapkan kepada Anggaran kos yang lengkap.</span><span class="sxs-lookup"><span data-stu-id="f2266-111">Initially on the task creation: Planned cost will be set to the Estimated cost at complete.</span></span> <span data-ttu-id="f2266-112">Sebaik sahaja Sebenar direkodkan pada tugas, perkara berikut akan menjadi pengiraan pada pandangan Penjejakan untuk Usaha</span><span class="sxs-lookup"><span data-stu-id="f2266-112">Once Actuals are recorded on the task, the following will be calculation on the Tracking view for Effort</span></span>

- <span data-ttu-id="f2266-113">Peratusan kemajuan = Usaha sebenar yang dihabiskan sehingga kini ÷ Anggaran yang lengkap (EAC)</span><span class="sxs-lookup"><span data-stu-id="f2266-113">Progress percentage = Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="f2266-114">Anggaran untuk lengkap (ETC) = Anggaran yang lengkap (EAC) – Usaha sebenar dihabiskan sehingga kini</span><span class="sxs-lookup"><span data-stu-id="f2266-114">Estimate to complete (ETC) = Estimate at complete (EAC)  – Actual effort spent to date</span></span> 
- <span data-ttu-id="f2266-115">EAC = Usaha selebihnya + Usaha sebenar dihabiskan sehingga kini</span><span class="sxs-lookup"><span data-stu-id="f2266-115">EAC = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="f2266-116">Varians usaha yang diunjurkan = Usaha yang dirancang - EAC</span><span class="sxs-lookup"><span data-stu-id="f2266-116">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="f2266-117">Project Service Automation menunjukkan unjuran bagi varians usaha pada tugas.</span><span class="sxs-lookup"><span data-stu-id="f2266-117">Project Service Automation shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="f2266-118">Jika EAC adalah lebih daripada usaha yang dirancang, tugas itu diunjurkan mengambil lebih banyak masa daripada yang dirancang pada asalnya.</span><span class="sxs-lookup"><span data-stu-id="f2266-118">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="f2266-119">Oleh itu, ia lebih lewat daripada yang dijadualkan.</span><span class="sxs-lookup"><span data-stu-id="f2266-119">Therefore, it's behind schedule.</span></span> <span data-ttu-id="f2266-120">Jika EAC kurang daripada usaha yang dirancang, tugas itu diunjurkan mengambil sedikit masa daripada yang dirancang pada asalnya.</span><span class="sxs-lookup"><span data-stu-id="f2266-120">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="f2266-121">Oleh itu, ia lebih awal daripada yang dijadualkan.</span><span class="sxs-lookup"><span data-stu-id="f2266-121">Therefore, it's ahead of schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="f2266-122">Usaha mengunjurkan semula</span><span class="sxs-lookup"><span data-stu-id="f2266-122">Reprojecting effort</span></span>

<span data-ttu-id="f2266-123">Ia adalah perkara biasa bagi pengurus projek untuk menyemak semula anggaran asal pada tugas.</span><span class="sxs-lookup"><span data-stu-id="f2266-123">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="f2266-124">Unjuran semula projek ialah persepsi pengurus projek berkenaan anggaran, memandangkan keadaan projek semasa.</span><span class="sxs-lookup"><span data-stu-id="f2266-124">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="f2266-125">Walau bagaimanapun, kami tidak mengesyorkan agar pengurus projek mengubah nombor garis dasar, kerana garis dasar projek mewakili sumber kebenaran yang sudah mantap bagi jadual dan anggaran kos projek, dan semua pemegang amanah projek telah bersetuju dengannya.</span><span class="sxs-lookup"><span data-stu-id="f2266-125">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="f2266-126">Terdapat dua cara pengurus projek boleh mengunjurkan semula usaha pada tugas:</span><span class="sxs-lookup"><span data-stu-id="f2266-126">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="f2266-127">Ganti ETC lalai dengan anggaran baharu bagi usaha sebenar yang masih tinggal pada tugas.</span><span class="sxs-lookup"><span data-stu-id="f2266-127">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="f2266-128">Ganti peratusan kemajuan lalai dengan anggaran baharu bagi kemajuan sebenar tugas.</span><span class="sxs-lookup"><span data-stu-id="f2266-128">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="f2266-129">Setiap pendekatan ini menyebabkan pengiraan semula ETC, EAC dan peratusan kemajuan tugas, serta varians usaha yang diunjurkan pada tugas.</span><span class="sxs-lookup"><span data-stu-id="f2266-129">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="f2266-130">EAC, ETC dan peratusan kemajuan pada tugas ringkasan juga dikira semula, dan menghasilkan unjuran baharu varians usaha.</span><span class="sxs-lookup"><span data-stu-id="f2266-130">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="f2266-131">Unjuran semula usaha pada tugas ringkasan</span><span class="sxs-lookup"><span data-stu-id="f2266-131">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="f2266-132">Usaha pada tugas ringkasan atau tugas bekas boleh diunjurkan semula.</span><span class="sxs-lookup"><span data-stu-id="f2266-132">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="f2266-133">Tidak kira sama ada pengguna mengunjurkan semula dengan menggunakan usaha yang masih tinggal atau peratusan kemajuan pada tugas ringkasan, set pengiraan berikut bermula:</span><span class="sxs-lookup"><span data-stu-id="f2266-133">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="f2266-134">EAC, ETC dan peratusan kemajuan pada tugas dikira.</span><span class="sxs-lookup"><span data-stu-id="f2266-134">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="f2266-135">EAC yang baharu diagihkan sehingga ke tugas anak dalam perkadaran yang sama dengan EAC asal pada tugas tersebut.</span><span class="sxs-lookup"><span data-stu-id="f2266-135">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="f2266-136">EAC baharu pada setiap tugas individu sehingga ke tugas nod daun dikira.</span><span class="sxs-lookup"><span data-stu-id="f2266-136">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="f2266-137">Tugas anak yang terjejas sehingga ke nod daun, ETC dan peratusan kemajuan ia dikira semula berdasarkan pada nilai EAC.</span><span class="sxs-lookup"><span data-stu-id="f2266-137">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="f2266-138">Ini menghasilkan unjuran baharu bagi varians usaha tugas tersebut.</span><span class="sxs-lookup"><span data-stu-id="f2266-138">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="f2266-139">EAC tugas ringkasan sehingga ke nod akar dikira semula.</span><span class="sxs-lookup"><span data-stu-id="f2266-139">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="f2266-140">Pandangan penjejakan kos</span><span class="sxs-lookup"><span data-stu-id="f2266-140">Cost tracking view</span></span> 

<span data-ttu-id="f2266-141">Pandangan **Penjejakan kos** membandingkan kos sebenar yang dibelanjakan pada tugas dengan kos yang dirancang.</span><span class="sxs-lookup"><span data-stu-id="f2266-141">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost.</span></span> 

> [!NOTE]
> <span data-ttu-id="f2266-142">Pandangan ini hanya menunjukkan kos buruh dan tidak termasuk kos daripada anggaran perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="f2266-142">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="f2266-143">Project Service Automation menggunakan formula berikut untuk mengira metrik penjejakan:</span><span class="sxs-lookup"><span data-stu-id="f2266-143">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="f2266-144">Apabila tugas dicipta, kos yang dirancang sama dengan anggaran kos yang lengkap.</span><span class="sxs-lookup"><span data-stu-id="f2266-144">When a task is created, the planned cost is equal to the estimated cost at complete.</span></span> <span data-ttu-id="f2266-145">Selepas sebenar direkodkan pada tugas, perkara berikut dikira pada pandangan **Penjejakan** untuk kos:</span><span class="sxs-lookup"><span data-stu-id="f2266-145">After actuals are recorded on the task, the following is calculated on the **Tracking** view for cost:</span></span>

 - <span data-ttu-id="f2266-146">Peratusan kos yang digunakan = Kos sebenar yang dibelanjakan sehingga kini ÷ Anggaran kos yang lengkap untuk tugas</span><span class="sxs-lookup"><span data-stu-id="f2266-146">Percentage of cost consumed = Actual cost spent to date ÷ Estimated cost at complete for the task</span></span>
 - <span data-ttu-id="f2266-147">Kos untuk lengkap (CTC) = Anggaran kos yang lengkap – Kos sebenar yang dibelanjakan sehingga kini</span><span class="sxs-lookup"><span data-stu-id="f2266-147">Cost to complete (CTC) = Estimated cost at complete – Actual cost spent to date</span></span>
 - <span data-ttu-id="f2266-148">Anggaran kos yang lengkap = Anggaran kos yang lengkap CTC + Kos sebenar yang dibelanjakan sehingga kini</span><span class="sxs-lookup"><span data-stu-id="f2266-148">Estimated cost at complete = CTC + Actual cost spent to date</span></span>
 - <span data-ttu-id="f2266-149">Varians kos yang unjuran = Kos yang dirancang – Anggaran kos yang lengkap</span><span class="sxs-lookup"><span data-stu-id="f2266-149">Projected cost variance = Planned cost – Estimated cost at complete</span></span>

<span data-ttu-id="f2266-150">Unjuran varians kos ditunjukkan pada tugas.</span><span class="sxs-lookup"><span data-stu-id="f2266-150">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="f2266-151">Jika anggaran kos yang lengkap adalah lebih daripada kos yang dirancang, tugas itu diunjurkan menelan belanja lebih daripada yang dirancang pada asalnya.</span><span class="sxs-lookup"><span data-stu-id="f2266-151">If the estimated cost at complete is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="f2266-152">Oleh itu, ia akan berkembang melebihi belanjawan.</span><span class="sxs-lookup"><span data-stu-id="f2266-152">Therefore, it's trending over budget.</span></span> <span data-ttu-id="f2266-153">Jika Anggaran kos yang lengkap adalah kurang daripada kos yang dirancang, tugas itu diunjurkan menelan belanja kurang daripada yang dirancang pada asalnya dan mengalir di bawah belanjawan.</span><span class="sxs-lookup"><span data-stu-id="f2266-153">If the Estimated cost at complete is less than the planned cost, the task is projected to cost less than was originally planned and is trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="f2266-154">Unjuran semula kos pengurus projek</span><span class="sxs-lookup"><span data-stu-id="f2266-154">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="f2266-155">Apabila usaha diunjurkan semula, CTC, Anggaran kos yang lengkap, peratusan kos yang digunakan dan varians kos unjuran semuanya dikira semula dalam pandangan **Penjejakan kos**.</span><span class="sxs-lookup"><span data-stu-id="f2266-155">When effort is reprojected, the CTC, Estimated cost at complete, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="f2266-156">Ringkasan status projek</span><span class="sxs-lookup"><span data-stu-id="f2266-156">Project status summary</span></span>

<span data-ttu-id="f2266-157">Data penjejakan dalam pandangan **Penjejakan usaha** dan **Penjejakan kos** menunjukkan kemajuan dan penggunaan kos pada nod akar projek, tugas ringkasan dan tahap tugas nod daun.</span><span class="sxs-lookup"><span data-stu-id="f2266-157">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="f2266-158">Bahagian **Status** pada halaman **Entiti projek** menunjukkan ringkasan status peringkat projek.</span><span class="sxs-lookup"><span data-stu-id="f2266-158">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="f2266-159">Medan ringkasan status</span><span class="sxs-lookup"><span data-stu-id="f2266-159">Status summary fields</span></span>

<span data-ttu-id="f2266-160">Medan **Status keseluruhan projek** ialah medan boleh diedit yang menunjukkan status keseluruhan projek.</span><span class="sxs-lookup"><span data-stu-id="f2266-160">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="f2266-161">Ia menggunakan pengekodan warna, seperti hijau, kuning dan merah untuk menunjukkan peningkatan risiko.</span><span class="sxs-lookup"><span data-stu-id="f2266-161">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="f2266-162">Medan **Komen** membolehkan pengurus projek memasukkan komen khusus tentang status.</span><span class="sxs-lookup"><span data-stu-id="f2266-162">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="f2266-163">Medan **Status dikemas kini pada** tidak boleh diedit dan nilainya ialah cap masa yang menunjukkan masa status tersebut dikemas kini kali terakhir.</span><span class="sxs-lookup"><span data-stu-id="f2266-163">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="f2266-164">Medan **Prestasi jadual** dan **Prestasi kos** ditetapkan dari tarikh penjejakan.</span><span class="sxs-lookup"><span data-stu-id="f2266-164">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="f2266-165">Apabila jadual dan varians kos untuk nod akar dalam pandangan **Penjejakan usaha** adalah positif, anda boleh menetapkan medan ini kepada **Di Hadapan.**</span><span class="sxs-lookup"><span data-stu-id="f2266-165">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="f2266-166">Apabila jadual dan varians kos untuk nod akar adalah negatif, anda boleh menetapkan ia kepada **Di Belakang**.</span><span class="sxs-lookup"><span data-stu-id="f2266-166">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
