---
title: Sediakan sumber projek
description: Topik ini memberikan maklumat tentang menyediakan atau memohon sumber projek.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bf146c3bfb2fd558c471d8a9e980834cb1b87df
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288750"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="de385-103">Sediakan sumber projek</span><span class="sxs-lookup"><span data-stu-id="de385-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="de385-104">Anda mesti menyediakan kalendar dan kaitkannya dengan pekerja atau pekerja.</span><span class="sxs-lookup"><span data-stu-id="de385-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="de385-105">Kalendar digunakan untuk menjadualkan projek dan masa kerja sumber yang diperuntukkan untuk projek.</span><span class="sxs-lookup"><span data-stu-id="de385-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="de385-106">Semasa persediaan kalendar, pengurus projek boleh lakukan pelarasan sumber sebagai sebahagian daripada pengoptimuman sumber.</span><span class="sxs-lookup"><span data-stu-id="de385-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="de385-107">Berdasarkan jadual kalendar, sekatan boleh diletakkan pada sumber.</span><span class="sxs-lookup"><span data-stu-id="de385-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="de385-108">Anda boleh menyediakan kalendar pada halaman **Kalendar**.</span><span class="sxs-lookup"><span data-stu-id="de385-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="de385-109">Apabila anda menyediakan pekerja sebagai sumber projek, anda boleh memilih daripada pekerja yang bekerja dalam syarikat tempat anda menyediakan sumber.</span><span class="sxs-lookup"><span data-stu-id="de385-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="de385-110">Secara alternatif, anda boleh memilih pekerja daripada syarikat lain dalam organisasi anda.</span><span class="sxs-lookup"><span data-stu-id="de385-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="de385-111">Pekerja ini dikenali sebagai sumber antara syarikat.</span><span class="sxs-lookup"><span data-stu-id="de385-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="de385-112">Prosedur berikut menerangkan cara untuk menyediakan pekerja sebagai sumber projek dalam syarikat anda dan cara untuk menyediakan sumber projek antara syarikat.</span><span class="sxs-lookup"><span data-stu-id="de385-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="de385-113">Sediakan pekerja sebagai sumber projek</span><span class="sxs-lookup"><span data-stu-id="de385-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="de385-114">Pada halaman **Pekerja**, dalam senarai **Pekerja**, pilih pekerja yang anda tambah sebagai sumber projek dan buka rekod pekerja.</span><span class="sxs-lookup"><span data-stu-id="de385-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="de385-115">Pada Anak Tetingkap Tindakan, pilih **Projek** &gt; **Persediaan** &gt; **Persediaan projek**.</span><span class="sxs-lookup"><span data-stu-id="de385-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="de385-116">Pilih kalendar, dan kemudian tutup halaman.</span><span class="sxs-lookup"><span data-stu-id="de385-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="de385-117">Anda juga boleh menentukan projek lalai untuk sumber sebagai jenis pra-tugasan.</span><span class="sxs-lookup"><span data-stu-id="de385-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="de385-118">Pra-tugasan boleh digunakan apabila pengurus sumber atau pengurus projek mengetahui projek sumber yang mana akan berjalan terlebih dahulu.</span><span class="sxs-lookup"><span data-stu-id="de385-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="de385-119">Pra-tugasan juga boleh berdasarkan kepada permintaan penaja projek atau pelanggan.</span><span class="sxs-lookup"><span data-stu-id="de385-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="de385-120">Untuk membuat pra-tugaskan projek, pada halaman **Tugaskan projek**, pada tab **Projek**, dalam senarai **Baki projek**, pilih projek yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="de385-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="de385-121">Sediakan sumber antara syarikat</span><span class="sxs-lookup"><span data-stu-id="de385-121">Set up an intercompany resource</span></span>

<span data-ttu-id="de385-122">Apabila anda menyediakan pekerja sebagai sumber antara syarikat, anda mesti melengkapkan persediaan dalam kedua-dua syarikat pinjaman dan syarikat peminjaman.</span><span class="sxs-lookup"><span data-stu-id="de385-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="de385-123">Dalam syarikat pinjaman</span><span class="sxs-lookup"><span data-stu-id="de385-123">In the lending company</span></span>

1. <span data-ttu-id="de385-124">Dalam Kewangan, sahkan bahawa syarikat pinjaman dipilih, dan kemudian lengkapkan prosedur dalam bahagian sebelumnya, "Sediakan pekerja sebagai sumber projek."</span><span class="sxs-lookup"><span data-stu-id="de385-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="de385-125">Pada halaman **Perakaunan antara syarikat**, pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="de385-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="de385-126">Dalam medan **ID entiti undang-undang**, pilih syarikat pinjaman.</span><span class="sxs-lookup"><span data-stu-id="de385-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="de385-127">Isikan medan yang selebihnya mengikut kesesuaian, dan kemudian pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="de385-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="de385-128">Pada halaman **Pemindahan harga**, pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="de385-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="de385-129">Dalam medan **Entiti undang-undang peminjaman**, pilih syarikat yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="de385-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="de385-130">Untuk meminjamkan syarikat peminjaman hanya sumber yang anda cipta pada permulaan bahagian ini, dalam medan **Sumber**, pilih nama sumber yang anda cipta.</span><span class="sxs-lookup"><span data-stu-id="de385-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="de385-131">Untuk menjadikan semua sumber dalam syarikat pinjaman tersedia kepada syarikat peminjaman, sila tinggalkan medan **Sumber** kosong.</span><span class="sxs-lookup"><span data-stu-id="de385-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="de385-132">Pada halaman **Pengurusan projek dan parameter perakaunan**, pada tab **Antara Syarikat**, tetapkan pilihan **Dayakan penjadualan sumber antara syarikat dan lembaran masa** kepada **Ya**.</span><span class="sxs-lookup"><span data-stu-id="de385-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="de385-133">Dalam syarikat peminjaman</span><span class="sxs-lookup"><span data-stu-id="de385-133">In the borrowing company</span></span>

- <span data-ttu-id="de385-134">Pada halaman **Senarai sumber**, dalam penapis carian, masukkan nama sumber yang anda cipta untuk syarikat pinjaman, untuk mengesahkan bahawa nama tersebut disertakan dalam senarai sumber untuk syarikat peminjaman.</span><span class="sxs-lookup"><span data-stu-id="de385-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="de385-135">Permohonan sumber projek</span><span class="sxs-lookup"><span data-stu-id="de385-135">Request project resources</span></span>
<span data-ttu-id="de385-136">Kefungsian untuk penjadualan sumber projek hanya membolehkan pengurus sumber edarkan sumber yang diperlukan dalam penglibatan atau projek.</span><span class="sxs-lookup"><span data-stu-id="de385-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="de385-137">Untuk mendayakan kefungsian ini, lengkapkan tugas berikut, atau sahkan yang telah dilengkapkan:</span><span class="sxs-lookup"><span data-stu-id="de385-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="de385-138">Sediakan jujukan nombor.</span><span class="sxs-lookup"><span data-stu-id="de385-138">Set up number sequences.</span></span>
- <span data-ttu-id="de385-139">Sediakan aliran kerja pengurusan projek dan perakaunan.</span><span class="sxs-lookup"><span data-stu-id="de385-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="de385-140">Dayakan aliran kerja permintaan sumber.</span><span class="sxs-lookup"><span data-stu-id="de385-140">Enable resource request workflows.</span></span>

<span data-ttu-id="de385-141">Selepas tugas sebelum ini dilengkapkan, anda boleh melengkapkan tugas berikut seperti yang anda perlukan:</span><span class="sxs-lookup"><span data-stu-id="de385-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="de385-142">Cipta permintaan sumber daripada sumber diperlukan yang ditempah sementara.</span><span class="sxs-lookup"><span data-stu-id="de385-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="de385-143">Pantau permintaan sumber.</span><span class="sxs-lookup"><span data-stu-id="de385-143">Monitor resource requests.</span></span>
- <span data-ttu-id="de385-144">Penuhi permintaan sumber.</span><span class="sxs-lookup"><span data-stu-id="de385-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="de385-145">Minta sumber yang diperlukan daripada WBS.</span><span class="sxs-lookup"><span data-stu-id="de385-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="de385-146">Tempah sumber untuk projek tanpa mempunyai permintaan untuk sumber yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="de385-146">Book resources to a project without having a request for a staffed resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]