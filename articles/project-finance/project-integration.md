---
title: Integrasi Microsoft Project Client
description: Merancang dan menyelenggara jadual projek boleh menjadi proses yang rumit, oleh itu, pengurus projek perlu menggunakan alat yang membantu mereka menguruskan tugas ini. Integrasi dengan Microsoft Project Client menyediakan sokongan untuk membuka dan menguruskan struktur pecahan kerja projek.
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: c6478e05-50ee-4993-87f4-6ce9cb78f076
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e35e1e54bad659d1329c333479830b680a17cbb0
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753966"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="b8ad2-104">Integrasi Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="b8ad2-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b8ad2-105">Merancang dan menyelenggara jadual projek boleh menjadi proses yang rumit, oleh itu, pengurus projek perlu menggunakan alat yang membantu mereka menguruskan tugas ini.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="b8ad2-106">Integrasi dengan Microsoft Project Client menyediakan sokongan untuk membuka dan menguruskan struktur pecahan kerja projek.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="b8ad2-107">Pengurus projek boleh menerbitkan apa-apa perubahan kembali kepada struktur pecahan kerja projek Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="b8ad2-108">Jika anda menggunakan versi kemas kini Julai (versi 10.0.4), anda mesti memasang KB 4054797 dan 4055884.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="b8ad2-109">Konfigurasikan tambahan Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="b8ad2-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="b8ad2-110">Untuk mendayakan integrasi dengan Microsoft Project Client, tambahan Microsoft Dynamics 365 diperlukan untuk dipasang dalam aplikasi Microsoft Project klien pengguna.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="b8ad2-111">Ini boleh dilakukan dengan membuka **Ruang kerja pengurusan projek**.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="b8ad2-112">•   Klik **Konfigurasikan tambahan klien projek** daripada **Pautan** > **bahagian Persediaan** ruang kerja.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="b8ad2-113">•   Klik **Buka**, kemudian klik **Jalankan** apabila digesa.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="b8ad2-114">Buka dan edit struktur pecahan kerja draf yang sedia ada dalam Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="b8ad2-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="b8ad2-115">Jika projek dalam Dynamics 365 Finance sudah pun mempunyai struktur pecahan kerja yang dicipta, struktur pecahan kerja boleh dibuka dalam aplikasi Microsoft Project Client jika struktur pecahan kerja berada dalam status draf.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="b8ad2-116">Untuk membuka daripada halaman **Projek**, klik pautan **Buka dalam Microsoft Project** daripada tab **Pelan**. Halaman ini juga boleh dibuka dari dalam aplikasi Microsoft Project Client dengan mengklik **Buka** dalam tab **Microsoft Dynamics 365**. Pilih **Entiti undang-undang** dan **Projek** daripada senarai.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="b8ad2-117">Jika anda menggunakan Internet Explorer sebagai pelayar anda, anda akan perlu klik **Simpan** untuk membuka secara manual dari lokasi yang fail itu dimuat turun.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="b8ad2-118">Atau, klik **Simpan dan buka** untuk membuka fail dalam Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="b8ad2-119">Jangan namakan semula nama fail semasa menyimpan.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="b8ad2-120">Sebelum membuat apa-apa pengeditan pada fail dengan menggunakan Microsoft Project Client, anda perlu mendaftar keluar fail. Klik **Daftar keluar** dalam tab **Microsoft Dynamics 365**. Ini akan mengelakkan pengguna lain daripada mengedit struktur pecahan kerja dari dalam Kewangan pada masa yang sama.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="b8ad2-121">Untuk menerbitkan struktur pecahan kerja selepas menyelesaikan apa-apa pengeditan, klik **Daftar masuk** pada tab **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="b8ad2-122">Jika pasukan projek sudah ditambah pada projek dalam Kewangan, senarai sumber akan diisi dengan ahli pasukan.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="b8ad2-123">Jika pasukan projek belum lagi ditambah pada projek, anda boleh memilih sumber dan membina pasukan dalam Microsoft Project Client dengan mengklik butang **Sumber** pada tab **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="b8ad2-124">Data berikut akan disegerakkan kembali kepada Kewangan sebagai sebahagian daripada proses daftar masuk:</span><span class="sxs-lookup"><span data-stu-id="b8ad2-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="b8ad2-125">•   Nama tugas</span><span class="sxs-lookup"><span data-stu-id="b8ad2-125">•   Task name</span></span>

<span data-ttu-id="b8ad2-126">•   Tarikh mula</span><span class="sxs-lookup"><span data-stu-id="b8ad2-126">•   Start date</span></span>

<span data-ttu-id="b8ad2-127">•   Tarikh siap</span><span class="sxs-lookup"><span data-stu-id="b8ad2-127">•   Finish date</span></span>

<span data-ttu-id="b8ad2-128">•   Terdahulu</span><span class="sxs-lookup"><span data-stu-id="b8ad2-128">•   Predecessors</span></span>

<span data-ttu-id="b8ad2-129">•   Nama sumber</span><span class="sxs-lookup"><span data-stu-id="b8ad2-129">•   Resource names</span></span>

<span data-ttu-id="b8ad2-130">•   Kategori</span><span class="sxs-lookup"><span data-stu-id="b8ad2-130">•   Category</span></span>

<span data-ttu-id="b8ad2-131">•   Kategori sumber</span><span class="sxs-lookup"><span data-stu-id="b8ad2-131">•   Resource category</span></span>

<span data-ttu-id="b8ad2-132">•   Jam kerja</span><span class="sxs-lookup"><span data-stu-id="b8ad2-132">•   Work hours</span></span>

<span data-ttu-id="b8ad2-133">•   Nota</span><span class="sxs-lookup"><span data-stu-id="b8ad2-133">•   Notes</span></span>

<span data-ttu-id="b8ad2-134">•   Keutamaan</span><span class="sxs-lookup"><span data-stu-id="b8ad2-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="b8ad2-135">Jika anda menambah apa-apa lajur lain pada fail Microsoft Project Client anda, lajur tersebut tidak akan disimpan pada fail dan tidak akan dipaparkan apabila fail dibuka semula.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="b8ad2-136">Cipta struktur pecahan kerja untuk projek yang sedia ada menggunakan Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="b8ad2-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="b8ad2-137">Untuk mencipta struktur pecahan kerja baharu dengan menggunakan Microsoft Project Client, ikut langkah ini:</span><span class="sxs-lookup"><span data-stu-id="b8ad2-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="b8ad2-138">Buka Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="b8ad2-139">Pada tab **Microsoft Dynamics 365**, klik **Buka**.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="b8ad2-140">Pilih **Entiti undang-undang** untuk projek.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="b8ad2-141">Pilih **Projek**.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="b8ad2-142">Klik **Daftar keluar** pada tab **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="b8ad2-143">Apabila anda sedia untuk menerbitkan kepada Kewangan, klik **Daftar masuk** pada tab **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="b8ad2-144">Gantikan struktur pecahan kerja yang sedia ada untuk projek sedia ada menggunakan Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="b8ad2-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="b8ad2-145">Untuk mencipta struktur pecahan kerja baharu dengan menggunakan Microsoft Project Client dan menggantikan struktur pecahan kerja yang sedia ada untuk projek sedia ada, ikut langkah ini:</span><span class="sxs-lookup"><span data-stu-id="b8ad2-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="b8ad2-146">Buka Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="b8ad2-147">CIpta jadual dalam Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="b8ad2-148">Pada tab **Microsoft Dynamics 365**, klik **Simpan perubahan** > **Gantikan projek sedia ada**.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="b8ad2-149">Pilih **Entiti undang-undang** untuk projek.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="b8ad2-150">Pilih **Projek**.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="b8ad2-151">Klik **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="b8ad2-152">Cipta projek baharu dari dalam Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="b8ad2-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="b8ad2-153">Buka Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="b8ad2-154">CIpta jadual dalam Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="b8ad2-155">Pada tab **Microsoft Dynamics 365**, klik **Simpan perubahan** > **Simpan pada Projek baharu**.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="b8ad2-156">Pilih **Entiti undang-undang** untuk projek.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="b8ad2-157">Masukkan **ID projek**, jika perlu.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="b8ad2-158">Masukkan **Nama projek**.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="b8ad2-159">Pilih **Jenis projek**, **Kumpulan projek** dan **ID kontrak projek**.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="b8ad2-160">Sebagai alternatif, anda boleh mencipta kontrak projek baharu dengan mengklik **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="b8ad2-161">Pilih **Kalendar** untuk digunakan untuk penyumberan.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="b8ad2-162">Klik **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8ad2-162">Click **OK**.</span></span>
