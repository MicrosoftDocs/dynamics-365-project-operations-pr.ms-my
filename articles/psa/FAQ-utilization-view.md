---
title: Lihat penggunaan boleh caj untuk sumber
description: Topik ini memberikan maklumat tentang pandangan penggunaan sumber.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: a1d1db532c65b2a13f3cf4e1281a5987490b96df
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122174"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="67eae-103">Lihat penggunaan boleh caj untuk sumber</span><span class="sxs-lookup"><span data-stu-id="67eae-103">View chargeable utilization for resources</span></span>
 
<span data-ttu-id="67eae-104">**Pandangan Penggunaan** pada halaman **Penggunaan Sumber Project Service** menunjukkan penggunaan boleh caj untuk setiap sumber boleh ditempah.</span><span class="sxs-lookup"><span data-stu-id="67eae-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="67eae-105">Disebabkan pandangan adalah berdasarkan papan jadual, anda akan mendapati banyak fungsi sama.</span><span class="sxs-lookup"><span data-stu-id="67eae-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Petikan skrin Pandangan Penggunaan](media/FAQ-utilization-1.png)
 

<span data-ttu-id="67eae-107">Pengiraan penggunaan boleh dituntut berfungsi seperti berikut:</span><span class="sxs-lookup"><span data-stu-id="67eae-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="67eae-108">Pengguna boleh caj = (Jam sebenar boleh caj) / (kapasiti sumber)</span><span class="sxs-lookup"><span data-stu-id="67eae-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="67eae-109">Sel mewakili penggunaan boleh dicaj dikira untuk tempoh tertentu (hari, minggu, atau bulan).</span><span class="sxs-lookup"><span data-stu-id="67eae-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="67eae-110">Warna dalam setiap sel menunjukkan penggunaan boleh dituntut untuk sumber berbanding dengan penggunaan boleh dituntut sasaran mereka.</span><span class="sxs-lookup"><span data-stu-id="67eae-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="67eae-111">Penggunaan sasaran boleh ditetapkan atas peranan lalai sumber atau atas sumber individu itu sendiri.</span><span class="sxs-lookup"><span data-stu-id="67eae-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="67eae-112">Pengiraan melihat kepada individu untuk sasaran dahulu, kemudian kepada peranan lalai sumber.</span><span class="sxs-lookup"><span data-stu-id="67eae-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="67eae-113">Tetapkan sasaran pada sumber</span><span class="sxs-lookup"><span data-stu-id="67eae-113">Set target on a resource</span></span>

1. <span data-ttu-id="67eae-114">Pergi ke **Sumber** \> **Sumber**.</span><span class="sxs-lookup"><span data-stu-id="67eae-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="67eae-115">Pilih sumber untuk membuka rekod.</span><span class="sxs-lookup"><span data-stu-id="67eae-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="67eae-116">Pada tab **Project Service**, anda boleh menetapkan penggunaan sasaran sumber.</span><span class="sxs-lookup"><span data-stu-id="67eae-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Petikan skrin menggunakan tab Project Service untuk menetapkan penggunaan sasaran](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="67eae-118">Tetapkan penggunaan pada peranan</span><span class="sxs-lookup"><span data-stu-id="67eae-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="67eae-119">Pergi ke **Sumber** \> **Peranan Sumber**.</span><span class="sxs-lookup"><span data-stu-id="67eae-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="67eae-120">Pilih peranan untuk membuka rekod.</span><span class="sxs-lookup"><span data-stu-id="67eae-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="67eae-121">Tetapkan penggunaan sasaran untuk peranan.</span><span class="sxs-lookup"><span data-stu-id="67eae-121">Set the target utilization for the role.</span></span>

> ![Petikan skrin menggunakan Peranan Sumber untuk menetapkan penggunaan sasaran](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="67eae-123">Kira penggunaan boleh caj untuk sumber</span><span class="sxs-lookup"><span data-stu-id="67eae-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="67eae-124">Untuk mengira penggunaan boleh caj untuk sumber, anda perlu melengkapkan pra-syarat tertentu.</span><span class="sxs-lookup"><span data-stu-id="67eae-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="67eae-125">Tetapkan peranan lalai untuk sumber individu</span><span class="sxs-lookup"><span data-stu-id="67eae-125">Set default role for individual resource</span></span>

<span data-ttu-id="67eae-126">Pertama, penggunaan sasaran mestilah ditetapkan kepada sama ada sumber individu atau pada peranan sumber.</span><span class="sxs-lookup"><span data-stu-id="67eae-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="67eae-127">Jika anda menggunakan peranan sumber untuk sasaran, setiap sumber individu mesti mempunyai peranan lalai.</span><span class="sxs-lookup"><span data-stu-id="67eae-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="67eae-128">Untuk tetapkan ini, pergi ke **Sumber** \> **Sumber**.</span><span class="sxs-lookup"><span data-stu-id="67eae-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="67eae-129">Pilih sumber, buka rekod, kemudian pilih tab **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="67eae-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="67eae-130">Dalam grid **Peranan Sumber**, pastikan terdapat satu peranan untuk sumber dan **Adalah Lalai** ditetapkan kepada **Ya**.</span><span class="sxs-lookup"><span data-stu-id="67eae-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="67eae-131">Ubah pengebilan untuk peranan sumber</span><span class="sxs-lookup"><span data-stu-id="67eae-131">Change billing type for resource role</span></span>

<span data-ttu-id="67eae-132">Peranan sumber mestilah ditetapkan kepada jenis pengebilan **Boleh caj**.</span><span class="sxs-lookup"><span data-stu-id="67eae-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="67eae-133">Pergi ke **Sumber** \> **Peranan Sumber**.</span><span class="sxs-lookup"><span data-stu-id="67eae-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="67eae-134">Buka rekod yang anda mahu kemas kini, kemudian tetapkan lalai jenis pengebilan kepada **Boleh caj**.</span><span class="sxs-lookup"><span data-stu-id="67eae-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="67eae-135">Tetapkan waktu bekerja untuk peranan sumber</span><span class="sxs-lookup"><span data-stu-id="67eae-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="67eae-136">Sumber mesti mempunyai jam kerja untuk pengiraan kapasiti.</span><span class="sxs-lookup"><span data-stu-id="67eae-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="67eae-137">Pergi ke **Sumber** \> **Sumber**.</span><span class="sxs-lookup"><span data-stu-id="67eae-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="67eae-138">Pilih sumber untuk membuka rekod, kemudian pilih **Tunjukkan Waktu Bekerja**.</span><span class="sxs-lookup"><span data-stu-id="67eae-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="67eae-139">Anda boleh kemas kini pukal senarai sumber dengan mengggunakan **Templat Waktu Bekerja** daripada pandangan **Senarai Sumber**.</span><span class="sxs-lookup"><span data-stu-id="67eae-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="67eae-140">Menyelesaikan masalah jam sebenar boleh caj</span><span class="sxs-lookup"><span data-stu-id="67eae-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="67eae-141">Jam sebenar boleh caj adalah bersumber daripada entiti **Aktual**.</span><span class="sxs-lookup"><span data-stu-id="67eae-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="67eae-142">Aktual dengan jenis pengebilan **Boleh Caj** adalah termasuk dalam pengiraan, dan atas sebab ini, anda mesti mempunyai projek di mana aktual adalah boleh caj.</span><span class="sxs-lookup"><span data-stu-id="67eae-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="67eae-143">Jika anda tidak melihat penggunaan boleh dituntut, berikut adalah beberapa perkara yang anda boleh semak:</span><span class="sxs-lookup"><span data-stu-id="67eae-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="67eae-144">Sumber mempunyai jam kerja ditakrifkan untuk kapasiti.</span><span class="sxs-lookup"><span data-stu-id="67eae-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="67eae-145">Sumber sama ada mempunyai sasaran penggunaan ditakrifkan secara individu atau mempunyai peranan lalai yang ditugaskan kepadanya.</span><span class="sxs-lookup"><span data-stu-id="67eae-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="67eae-146">Peranan ini mempunyai sasaran penggunaan ditakrifkan untuknya.</span><span class="sxs-lookup"><span data-stu-id="67eae-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="67eae-147">Aktual mempunyai jenis pengebilan **Boleh Caj** untuk tempoh yang anda jangkakan pengiraan penggunaan.</span><span class="sxs-lookup"><span data-stu-id="67eae-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="67eae-148">Semak perkara berikut jika anda melihat aktual yang mempunyai jenis pengebilan selain daripada boleh caj:</span><span class="sxs-lookup"><span data-stu-id="67eae-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="67eae-149">Peranan yang digunakan sebenarnya mempunyai jenis pengebilan lalai bagi sesuatu selain daripada boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="67eae-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="67eae-150">Peranan pada baris kontrak projek yang menyokong projek telah ditetapkan kepada tidak boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="67eae-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="67eae-151">Projek ini tidak mempunyai baris kontrak yang berkaitan.</span><span class="sxs-lookup"><span data-stu-id="67eae-151">The project does not have an associated contract line.</span></span>

