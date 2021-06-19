---
title: Salin projek
description: Topik ini menyediakan maklumat tentang menyalin projek dalam Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091265"
---
# <a name="copy-a-project"></a><span data-ttu-id="c7bee-103">Salin projek</span><span class="sxs-lookup"><span data-stu-id="c7bee-103">Copy a project</span></span>

<span data-ttu-id="c7bee-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="c7bee-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c7bee-105">Dengan Dynamics 365 Project Operations, anda boleh dengan cepat membina projek baru dengan memilih **Salin Projek** pada borang **Projek**.</span><span class="sxs-lookup"><span data-stu-id="c7bee-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="c7bee-106">Untuk menyalin projek, buka projek yang anda mahu salin dan kemudian pilih **Salin projek**.</span><span class="sxs-lookup"><span data-stu-id="c7bee-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="c7bee-107">Tindakan akan menyalin yang berikut:</span><span class="sxs-lookup"><span data-stu-id="c7bee-107">The action will copy the following:</span></span>

- <span data-ttu-id="c7bee-108">Sifat projek</span><span class="sxs-lookup"><span data-stu-id="c7bee-108">Project properties</span></span> 
- <span data-ttu-id="c7bee-109">Struktur pecahan kerja</span><span class="sxs-lookup"><span data-stu-id="c7bee-109">Work breakdown structure</span></span>
- <span data-ttu-id="c7bee-110">Ahli pasukan projek</span><span class="sxs-lookup"><span data-stu-id="c7bee-110">Project team members</span></span>
- <span data-ttu-id="c7bee-111">Anggaran projek</span><span class="sxs-lookup"><span data-stu-id="c7bee-111">Project estimates</span></span>
- <span data-ttu-id="c7bee-112">Anggaran perbelanjaan projek</span><span class="sxs-lookup"><span data-stu-id="c7bee-112">Project expense estimates</span></span>
- <span data-ttu-id="c7bee-113">Anggaran bahan projek</span><span class="sxs-lookup"><span data-stu-id="c7bee-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="c7bee-114">Sifat projek</span><span class="sxs-lookup"><span data-stu-id="c7bee-114">Project properties</span></span>

<span data-ttu-id="c7bee-115">Apabila projek disalin, nilai dalam medan berikut disalin:</span><span class="sxs-lookup"><span data-stu-id="c7bee-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="c7bee-116">Nama</span><span class="sxs-lookup"><span data-stu-id="c7bee-116">Name</span></span>
- <span data-ttu-id="c7bee-117">Penerangan </span><span class="sxs-lookup"><span data-stu-id="c7bee-117">Description</span></span>
- <span data-ttu-id="c7bee-118">Pelanggan</span><span class="sxs-lookup"><span data-stu-id="c7bee-118">Customer</span></span>
- <span data-ttu-id="c7bee-119">Templat Kalendar</span><span class="sxs-lookup"><span data-stu-id="c7bee-119">Calendar Template</span></span>
- <span data-ttu-id="c7bee-120">Mata wang</span><span class="sxs-lookup"><span data-stu-id="c7bee-120">Currency</span></span>
- <span data-ttu-id="c7bee-121">Unit Pengkontrakan</span><span class="sxs-lookup"><span data-stu-id="c7bee-121">Contracting Unit</span></span>
- <span data-ttu-id="c7bee-122">Pengurus Projek</span><span class="sxs-lookup"><span data-stu-id="c7bee-122">Project Manager</span></span>
- <span data-ttu-id="c7bee-123">Status</span><span class="sxs-lookup"><span data-stu-id="c7bee-123">Status</span></span>
- <span data-ttu-id="c7bee-124">Keseluruhan Status Projek</span><span class="sxs-lookup"><span data-stu-id="c7bee-124">Overall Project Status</span></span>
- <span data-ttu-id="c7bee-125">Komen</span><span class="sxs-lookup"><span data-stu-id="c7bee-125">Comments</span></span>
- <span data-ttu-id="c7bee-126">Anggaran</span><span class="sxs-lookup"><span data-stu-id="c7bee-126">Estimates</span></span>
- <span data-ttu-id="c7bee-127">Anggaran Tarikh Mula: Ini ialah tarikh projek yang dicipta daripada salinan.</span><span class="sxs-lookup"><span data-stu-id="c7bee-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="c7bee-128">Anggaran Tarikh Tamat: Tarikh ini dilaraskan berdasarkan tarikh mula projek baharu yang telah dibuat daripada salinan.</span><span class="sxs-lookup"><span data-stu-id="c7bee-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="c7bee-129">Usaha (Jam)</span><span class="sxs-lookup"><span data-stu-id="c7bee-129">Effort (Hours)</span></span>
- <span data-ttu-id="c7bee-130">Kos Buruh yang Dianggarkan</span><span class="sxs-lookup"><span data-stu-id="c7bee-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="c7bee-131">Kos Perbelanjaan yang Dianggarkan</span><span class="sxs-lookup"><span data-stu-id="c7bee-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="c7bee-132">Kos Bahan yang Dianggarkan</span><span class="sxs-lookup"><span data-stu-id="c7bee-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="c7bee-133">Salin projek adalah operasi yang panjang berjalan.</span><span class="sxs-lookup"><span data-stu-id="c7bee-133">Copy project is a long running operation.</span></span> <span data-ttu-id="c7bee-134">Rekod projek, atribut yang berkaitan dan banyak entiti berkaitan juga boleh disalin.</span><span class="sxs-lookup"><span data-stu-id="c7bee-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="c7bee-135">Disebabkan oleh sifat jangka panjang operasi, selepas salinan dimulakan, halaman projek sasaran dikunci untuk pengeditan sehingga operasi salinan selesai.</span><span class="sxs-lookup"><span data-stu-id="c7bee-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="c7bee-136">Struktur pecahan kerja</span><span class="sxs-lookup"><span data-stu-id="c7bee-136">Work breakdown structure</span></span>

<span data-ttu-id="c7bee-137">Apabila projek disalin, keseluruhan struktur pecahan kerja yang dimuatkan oleh sumber akan disalin.</span><span class="sxs-lookup"><span data-stu-id="c7bee-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="c7bee-138">Sumber yang dinamakan digantikan dengan sumber yang generik.</span><span class="sxs-lookup"><span data-stu-id="c7bee-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="c7bee-139">Jika sumber yang dinamakan tidak mempunyai masa kerja yang sama dengan sumber generik, jadual akan dikira semula dan tempoh tugas mungkin berubah.</span><span class="sxs-lookup"><span data-stu-id="c7bee-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="c7bee-140">Ahli pasukan projek</span><span class="sxs-lookup"><span data-stu-id="c7bee-140">Project team members</span></span>

<span data-ttu-id="c7bee-141">Apabila pasukan projek disalin daripada projek sumber, sumber generik akan disalin.</span><span class="sxs-lookup"><span data-stu-id="c7bee-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="c7bee-142">Tugasan sumber generik juga dikekalkan sebagai mana ia di dalam projek sumber.</span><span class="sxs-lookup"><span data-stu-id="c7bee-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="c7bee-143">Sumber yang dinamakan akan ditukar kepada ahli pasukan generik.</span><span class="sxs-lookup"><span data-stu-id="c7bee-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="c7bee-144">Anggaran</span><span class="sxs-lookup"><span data-stu-id="c7bee-144">Estimates</span></span>

<span data-ttu-id="c7bee-145">Apabila projek disalin, sumber, perbelanjaan dan baris anggaran bahan akan disalin daripada projek sumber.</span><span class="sxs-lookup"><span data-stu-id="c7bee-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="c7bee-146">Untuk maklumat tentang cara mengakses Salin Projek secara programatik, lihat [Membangun templat projek dengan Salin Projek](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="c7bee-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
