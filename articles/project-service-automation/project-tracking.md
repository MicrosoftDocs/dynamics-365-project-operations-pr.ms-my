---
title: Kemajuan projek dan penggunaan kos
description: Topik ini memberikan maklumat tentang cara untuk menjejaki kemajuan projek dan penggunaan kos.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753964"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="76714-103">Kemajuan projek dan penggunaan kos</span><span class="sxs-lookup"><span data-stu-id="76714-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="76714-104">Keperluan untuk menjejaki kemajuan terhadap jadual berbeza-beza mengikut industri.</span><span class="sxs-lookup"><span data-stu-id="76714-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="76714-105">Sesetengah industri menjejaki pada tahap butiran, manakala industri lain menjejaki pada tahap yang lebih tinggi.</span><span class="sxs-lookup"><span data-stu-id="76714-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="76714-106">Topik ini menunjukkan cara untuk menjadualkan bagi memenuhi keperluan organisasi anda.</span><span class="sxs-lookup"><span data-stu-id="76714-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="76714-107">Pandangan penjejakan usaha</span><span class="sxs-lookup"><span data-stu-id="76714-107">Effort tracking view</span></span>

<span data-ttu-id="76714-108">Pandangan **Penjejakan usaha** menjejaki kemajuan tugas dalam jadual.</span><span class="sxs-lookup"><span data-stu-id="76714-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="76714-109">Ia membandingkan jam kerja sebenar yang telah diluangkan pada tugas kepada jam kerja yang dirancang bagi tugas itu.</span><span class="sxs-lookup"><span data-stu-id="76714-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="76714-110">PSA menggunakan formula berikut untuk mengira metrik penjejakan:</span><span class="sxs-lookup"><span data-stu-id="76714-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="76714-111">Peratusan kemajuan = Usaha sebenar dihabiskan sehingga kini ÷ Usaha yang dirancang untuk tugas tersebut</span><span class="sxs-lookup"><span data-stu-id="76714-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="76714-112">Anggaran untuk selesai (ETC) = Usaha yang dirancang – Usaha sebenar dihabiskan sehingga kini</span><span class="sxs-lookup"><span data-stu-id="76714-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="76714-113">Anggaran ketika selesai (EAC) = Usaha selebihnya + Usaha sebenar dihabiskan sehingga kini</span><span class="sxs-lookup"><span data-stu-id="76714-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="76714-114">Varians usaha yang diunjurkan = Usaha yang dirancang - EAC</span><span class="sxs-lookup"><span data-stu-id="76714-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="76714-115">PSA menunjukkan unjuran bagi varians usaha pada tugas.</span><span class="sxs-lookup"><span data-stu-id="76714-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="76714-116">Jika EAC adalah lebih daripada usaha yang dirancang, tugas itu diunjurkan mengambil lebih banyak masa daripada yang dirancang pada asalnya.</span><span class="sxs-lookup"><span data-stu-id="76714-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="76714-117">Oleh itu, ia lebih lewat daripada yang dijadualkan.</span><span class="sxs-lookup"><span data-stu-id="76714-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="76714-118">Jika EAC kurang daripada usaha yang dirancang, tugas itu diunjurkan mengambil sedikit masa daripada yang dirancang pada asalnya.</span><span class="sxs-lookup"><span data-stu-id="76714-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="76714-119">Oleh itu, ia lebih awal daripada yang dijadualkan.</span><span class="sxs-lookup"><span data-stu-id="76714-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="76714-120">Usaha mengunjurkan semula</span><span class="sxs-lookup"><span data-stu-id="76714-120">Re-projecting effort</span></span>

<span data-ttu-id="76714-121">Ia adalah perkara biasa bagi pengurus projek untuk menyemak semula anggaran asal pada tugas.</span><span class="sxs-lookup"><span data-stu-id="76714-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="76714-122">Unjuran semula projek ialah persepsi pengurus projek mengenai anggaran, memandangkan keadaan projek semasa.</span><span class="sxs-lookup"><span data-stu-id="76714-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="76714-123">Walau bagaimanapun, kami tidak mengesyorkan agar pengurus projek mengubah nombor garis dasar, kerana garis dasar projek mewakili sumber kebenaran yang sudah mantap bagi jadual dan anggaran kos projek, dan semua pemegang amanah projek telah bersetuju dengannya.</span><span class="sxs-lookup"><span data-stu-id="76714-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="76714-124">Terdapat dua cara pengurus projek boleh mengunjurkan semula usaha pada tugas:</span><span class="sxs-lookup"><span data-stu-id="76714-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="76714-125">Ganti ETC lalai dengan anggaran baharu bagi usaha sebenar yang masih tinggal pada tugas.</span><span class="sxs-lookup"><span data-stu-id="76714-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="76714-126">Ganti peratusan kemajuan lalai dengan anggaran baharu bagi kemajuan sebenar tugas.</span><span class="sxs-lookup"><span data-stu-id="76714-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="76714-127">Setiap pendekatan ini menyebabkan pengiraan semula ETC, EAC dan peratusan kemajuan tugas, serta varians usaha yang diunjurkan pada tugas.</span><span class="sxs-lookup"><span data-stu-id="76714-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="76714-128">EAC, ETC dan peratusan kemajuan pada tugas ringkasan juga dikira semula, dan menghasilkan unjuran baharu varians usaha.</span><span class="sxs-lookup"><span data-stu-id="76714-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="76714-129">Unjuran semula usaha pada tugas ringkasan</span><span class="sxs-lookup"><span data-stu-id="76714-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="76714-130">Usaha pada tugas ringkasan atau tugas bekas boleh diunjurkan semula.</span><span class="sxs-lookup"><span data-stu-id="76714-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="76714-131">Tidak kira sama ada pengguna mengunjurkan semula dengan menggunakan usaha yang masih tinggal atau peratusan kemajuan pada tugas ringkasan, set pengiraan berikut bermula:</span><span class="sxs-lookup"><span data-stu-id="76714-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="76714-132">EAC, ETC dan peratusan kemajuan pada tugas dikira.</span><span class="sxs-lookup"><span data-stu-id="76714-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="76714-133">EAC yang baharu diagihkan sehingga ke tugas anak dalam perkadaran yang sama dengan EAC asal pada tugas tersebut.</span><span class="sxs-lookup"><span data-stu-id="76714-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="76714-134">EAC baharu pada setiap tugas individu sehingga ke tugas nod daun dikira.</span><span class="sxs-lookup"><span data-stu-id="76714-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="76714-135">Tugas anak yang terjejas sehingga ke nod daun, ETC dan peratusan kemajuan ia dikira semula berdasarkan pada nilai EAC.</span><span class="sxs-lookup"><span data-stu-id="76714-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="76714-136">Ini menghasilkan unjuran baharu bagi varians usaha tugas tersebut.</span><span class="sxs-lookup"><span data-stu-id="76714-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="76714-137">EAC tugas ringkasan sehingga ke nod akar dikira semula.</span><span class="sxs-lookup"><span data-stu-id="76714-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="76714-138">Pandangan penjejakan kos</span><span class="sxs-lookup"><span data-stu-id="76714-138">Cost tracking view</span></span> 

<span data-ttu-id="76714-139">Pandangan **Penjejakan kos** membandingkan kos sebenar yang dibelanjakan pada tugas dengan kos yang dirancang pada tugas.</span><span class="sxs-lookup"><span data-stu-id="76714-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="76714-140">Pandangan ini hanya menunjukkan kos buruh dan tidak termasuk kos daripada anggaran perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="76714-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="76714-141">PSA menggunakan formula berikut untuk mengira metrik penjejakan:</span><span class="sxs-lookup"><span data-stu-id="76714-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="76714-142">Peratusan kos yang digunakan = Kos sebenar yang dibelanjakan sehingga kini ÷ Kos yang dirancang untuk tugas tersebut</span><span class="sxs-lookup"><span data-stu-id="76714-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="76714-143">Kos untuk selesai (CTC) = Kos yang dirancang – Kos sebenar yang dibelanjakan sehingga kini</span><span class="sxs-lookup"><span data-stu-id="76714-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="76714-144">EAC = CTC + Kos sebenar yang dibelanjakan sehingga kini</span><span class="sxs-lookup"><span data-stu-id="76714-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="76714-145">Varians kos unjuran = Kos dirancang – EAC</span><span class="sxs-lookup"><span data-stu-id="76714-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="76714-146">Unjuran varians kos ditunjukkan pada tugas.</span><span class="sxs-lookup"><span data-stu-id="76714-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="76714-147">Jika EAC adalah lebih daripada kos yang dirancang, tugas itu diunjurkan menelan belanja lebih daripada yang dirancang pada asalnya.</span><span class="sxs-lookup"><span data-stu-id="76714-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="76714-148">Oleh itu, ia akan berkembang melebihi belanjawan.</span><span class="sxs-lookup"><span data-stu-id="76714-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="76714-149">Jika EAC adalah kurang daripada kos yang dirancang, tugas itu diunjurkan menelan belanja kurang daripada yang dirancang pada asalnya.</span><span class="sxs-lookup"><span data-stu-id="76714-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="76714-150">Oleh itu, ia berkembang di bawah belanjawan.</span><span class="sxs-lookup"><span data-stu-id="76714-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="76714-151">Unjuran semula kos pengurus projek</span><span class="sxs-lookup"><span data-stu-id="76714-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="76714-152">Apabila usaha diunjurkan semula, CTC, EAC, peratusan kos yang digunakan dan varians kos unjuran semuanya dikira semula dalam pandangan **Penjejakan kos**.</span><span class="sxs-lookup"><span data-stu-id="76714-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="76714-153">Ringkasan status projek</span><span class="sxs-lookup"><span data-stu-id="76714-153">Project status summary</span></span>

<span data-ttu-id="76714-154">Data penjejakan dalam pandangan **Penjejakan usaha** dan **Penjejakan kos** menunjukkan kemajuan dan penggunaan kos pada nod akar projek, tugas ringkasan dan tahap tugas nod daun.</span><span class="sxs-lookup"><span data-stu-id="76714-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="76714-155">Bahagian **Status** pada halaman **Entiti projek** menunjukkan ringkasan status peringkat projek.</span><span class="sxs-lookup"><span data-stu-id="76714-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="76714-156">Medan ringkasan status</span><span class="sxs-lookup"><span data-stu-id="76714-156">Status summary fields</span></span>

<span data-ttu-id="76714-157">Medan **Status keseluruhan projek** ialah medan boleh diedit yang menunjukkan status keseluruhan projek.</span><span class="sxs-lookup"><span data-stu-id="76714-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="76714-158">Ia menggunakan pengekodan warna, seperti hijau, kuning dan merah untuk menunjukkan peningkatan risiko.</span><span class="sxs-lookup"><span data-stu-id="76714-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="76714-159">Medan **Komen** membolehkan pengurus projek memasukkan komen khusus tentang status.</span><span class="sxs-lookup"><span data-stu-id="76714-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="76714-160">Medan **Status dikemas kini pada** tidak boleh diedit dan nilainya ialah cap masa yang menunjukkan masa status tersebut dikemas kini kali terakhir.</span><span class="sxs-lookup"><span data-stu-id="76714-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="76714-161">Medan **Prestasi jadual** dan **Prestasi kos** ditetapkan dari tarikh penjejakan.</span><span class="sxs-lookup"><span data-stu-id="76714-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="76714-162">Apabila jadual dan varians kos untuk nod akar dalam pandangan **Penjejakan usaha** adalah positif, anda boleh menetapkan medan ini kepada **Di Hadapan.**</span><span class="sxs-lookup"><span data-stu-id="76714-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="76714-163">Apabila jadual dan varians kos untuk nod akar adalah negatif, anda boleh menetapkan ia kepada **Di Belakang**.</span><span class="sxs-lookup"><span data-stu-id="76714-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
