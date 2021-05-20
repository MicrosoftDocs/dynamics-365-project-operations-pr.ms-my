---
title: Mod penjadualan
description: Topik ini memberikan maklumat tentang mod penjadualan.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981446"
---
# <a name="scheduling-modes"></a><span data-ttu-id="1ecc4-103">Mod penjadualan</span><span class="sxs-lookup"><span data-stu-id="1ecc4-103">Scheduling modes</span></span>

<span data-ttu-id="1ecc4-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="1ecc4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="1ecc4-105">Dynamics 365 Project Operations menyediakan keupayaan untuk organisasi mentakrifkan cara mereka mengurus perubahan ke pemboleh ubah utama dalam tugas dalam struktur pecahan kerja.</span><span class="sxs-lookup"><span data-stu-id="1ecc4-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="1ecc4-106">Berdasarkan pada keperluan khusus organisasi, Pengurus Projek boleh membuat perubahan pada mod penjadualan apabila projek dicipta.</span><span class="sxs-lookup"><span data-stu-id="1ecc4-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="1ecc4-107">Terdapat tiga mod penjadualan yang tersedia dalam Project Operations:</span><span class="sxs-lookup"><span data-stu-id="1ecc4-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="1ecc4-108">Tempoh tetap (ini adalah mod lalai)</span><span class="sxs-lookup"><span data-stu-id="1ecc4-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="1ecc4-109">Kerja ditetapkan</span><span class="sxs-lookup"><span data-stu-id="1ecc4-109">Fixed work</span></span>
  - <span data-ttu-id="1ecc4-110">Unit ditetapkan</span><span class="sxs-lookup"><span data-stu-id="1ecc4-110">Fixed units</span></span>

<span data-ttu-id="1ecc4-111">Nilai yang terjejas dengan definisi mod penjadualan tertentu ditentukan oleh formula berikut:</span><span class="sxs-lookup"><span data-stu-id="1ecc4-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="1ecc4-112">Usaha (*Kerja*) = Tempoh x Unit</span><span class="sxs-lookup"><span data-stu-id="1ecc4-112">Effort (*Work*) = Duration x Units</span></span>

<span data-ttu-id="1ecc4-113">Apabila anda mentakrifkan mod penjadualan projek, anda menetapkan salah satu daripada nilai ini yang kemudian tidak boleh ditukar.</span><span class="sxs-lookup"><span data-stu-id="1ecc4-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="1ecc4-114">Memegang nilai ini sebagai pemalar meletakkan keutamaan pada nilai itu yang memberitahu sistem untuk tidak mengubahnya apabila dua nilai lain berubah.</span><span class="sxs-lookup"><span data-stu-id="1ecc4-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="1ecc4-115">Jadual berikut memberikan maklumat tentang kesan pemilihan mod tertentu.</span><span class="sxs-lookup"><span data-stu-id="1ecc4-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="1ecc4-116">**Dalam tugas ini**</span><span class="sxs-lookup"><span data-stu-id="1ecc4-116">**In this task**</span></span>             | <span data-ttu-id="1ecc4-117">**Jika anda menyemak semula unit**</span><span class="sxs-lookup"><span data-stu-id="1ecc4-117">**If you revise units**</span></span>   | <span data-ttu-id="1ecc4-118">**Jika anda menyemak semula tempoh**</span><span class="sxs-lookup"><span data-stu-id="1ecc4-118">**If you revise duration**</span></span> | <span data-ttu-id="1ecc4-119">**Jika anda menyemak semula usaha**</span><span class="sxs-lookup"><span data-stu-id="1ecc4-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="1ecc4-120">Tugas unit tetap</span><span class="sxs-lookup"><span data-stu-id="1ecc4-120">Fixed units task</span></span>     | <span data-ttu-id="1ecc4-121">Tempoh dikira semula.</span><span class="sxs-lookup"><span data-stu-id="1ecc4-121">Duration is recalculated.</span></span> | <span data-ttu-id="1ecc4-122">Usaha dikira semula.</span><span class="sxs-lookup"><span data-stu-id="1ecc4-122">Effort is recalculated.</span></span>    | <span data-ttu-id="1ecc4-123">Tempoh dikira semula.</span><span class="sxs-lookup"><span data-stu-id="1ecc4-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="1ecc4-124">Tugas usaha tetap</span><span class="sxs-lookup"><span data-stu-id="1ecc4-124">Fixed effort task</span></span>    | <span data-ttu-id="1ecc4-125">Tempoh dikira semula.</span><span class="sxs-lookup"><span data-stu-id="1ecc4-125">Duration is recalculated.</span></span> | <span data-ttu-id="1ecc4-126">Unit dikira semula.</span><span class="sxs-lookup"><span data-stu-id="1ecc4-126">Units are recalculated.</span></span>    | <span data-ttu-id="1ecc4-127">Tempoh dikira semula.</span><span class="sxs-lookup"><span data-stu-id="1ecc4-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="1ecc4-128">Tugas tempoh tetap</span><span class="sxs-lookup"><span data-stu-id="1ecc4-128">Fixed duration task</span></span>  | <span data-ttu-id="1ecc4-129">Usaha dikira semula.</span><span class="sxs-lookup"><span data-stu-id="1ecc4-129">Effort is recalculated.</span></span>   | <span data-ttu-id="1ecc4-130">Usaha dikira semula.</span><span class="sxs-lookup"><span data-stu-id="1ecc4-130">Effort is recalculated.</span></span>    | <span data-ttu-id="1ecc4-131">Unit dikira semula.</span><span class="sxs-lookup"><span data-stu-id="1ecc4-131">Units are recalculated.</span></span>   |

<span data-ttu-id="1ecc4-132">Untuk maklumat lanjut tentang implikasi mod diberikan, lihat [Tukar jenis tugas untuk penjadualan yang lebih tepat](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="1ecc4-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="1ecc4-133">Dalam topik, istilah **Kerja** digunakan berbanding **Usaha**.</span><span class="sxs-lookup"><span data-stu-id="1ecc4-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="1ecc4-134">Tukar mod penjadualan organisasi</span><span class="sxs-lookup"><span data-stu-id="1ecc4-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="1ecc4-135">Lengkapkan langkah berikut untuk mentakrifkan mod penjadualan organisasi.</span><span class="sxs-lookup"><span data-stu-id="1ecc4-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="1ecc4-136">Pergi ke **Tetapan** \> **Umum** \> **Parameter** dan kemudian pilih parameter projek.</span><span class="sxs-lookup"><span data-stu-id="1ecc4-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="1ecc4-137">Pada halaman **Parameter Projek**, pilih mod penjadualan lalai untuk organisasi dan kemudian takrifkan keupayaan untuk pengurus Projek mengganti tetapan apabila mencipta projek baharu.</span><span class="sxs-lookup"><span data-stu-id="1ecc4-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="1ecc4-138">Tukar tetapan mod penjadualan pada projek</span><span class="sxs-lookup"><span data-stu-id="1ecc4-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="1ecc4-139">Jika organisasi membenarkan pengurus Projek mengganti mod penjadualan lalai, pengurus Projek boleh membuat perubahan itu apabila mereka mencipta projek baharu.</span><span class="sxs-lookup"><span data-stu-id="1ecc4-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="1ecc4-140">Walau bagaimanapun selepas projek telah disimpan, mod penjadualan tidak boleh ditukar.</span><span class="sxs-lookup"><span data-stu-id="1ecc4-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="1ecc4-141">Projek disalin</span><span class="sxs-lookup"><span data-stu-id="1ecc4-141">Copied projects</span></span>

<span data-ttu-id="1ecc4-142">Oleh kerana projek dicipta apabila salinan tindakan projek diambil, pengurus Projek tidak boleh menetapkan mod penjadualan.</span><span class="sxs-lookup"><span data-stu-id="1ecc4-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="1ecc4-143">Projek destinasi akan sentiasa lalai dengan mod yang ditakrifkan pada peringkat organisasi.</span><span class="sxs-lookup"><span data-stu-id="1ecc4-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="1ecc4-144">Tugas yang disalin</span><span class="sxs-lookup"><span data-stu-id="1ecc4-144">Copied tasks</span></span>

<span data-ttu-id="1ecc4-145">Apabila tugas disalin daripada satu projek ke yang lain, tugas mewarisi mod penjadualan projek destinasi.</span><span class="sxs-lookup"><span data-stu-id="1ecc4-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>