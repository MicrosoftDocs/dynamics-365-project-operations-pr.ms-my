---
title: Cipta projek baharu
description: Topik ini memberikan maklumat tentang cara untuk mencipta projek baharu.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 727d287c571b2a64bf10b2393a87567093a420d2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081363"
---
# <a name="create-a-new-project"></a><span data-ttu-id="6c859-103">Cipta projek baharu</span><span class="sxs-lookup"><span data-stu-id="6c859-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c859-104">Lengkapkan langkah berikut untuk mencipta projek baharu.</span><span class="sxs-lookup"><span data-stu-id="6c859-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="6c859-105">Pada halaman **Pengurusan projek** , pilih **Projek baharu** , dan masukkan nilai berikut:</span><span class="sxs-lookup"><span data-stu-id="6c859-105">On the **Project management** page, select **New project** , and enter the following values:</span></span>

    - <span data-ttu-id="6c859-106">**Jenis projek:** Masa dan bahan</span><span class="sxs-lookup"><span data-stu-id="6c859-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="6c859-107">**Nama projek:** Naik taraf XYZ Fasa 2</span><span class="sxs-lookup"><span data-stu-id="6c859-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="6c859-108">**Kumpulan projek:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="6c859-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="6c859-109">**ID kontrak projek:** 00000002</span><span class="sxs-lookup"><span data-stu-id="6c859-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="6c859-110">Pilih **Cipta projek**.</span><span class="sxs-lookup"><span data-stu-id="6c859-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="6c859-111">Tugaskan sumber kepada projek</span><span class="sxs-lookup"><span data-stu-id="6c859-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="6c859-112">Pada halaman **Pekerja** , dalam senarai **Pekerja** , pilih rekod untuk pekerja yang sebelum ini anda sediakan kecekapan, dan buka rekod pekerja.</span><span class="sxs-lookup"><span data-stu-id="6c859-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="6c859-113">Pada Anak Tetingkap Tindakan, pada tab **Projek** , dalam kumpulan **Persediaan** , pilih **Tugaskan projek**.</span><span class="sxs-lookup"><span data-stu-id="6c859-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="6c859-114">Pada halaman **Tugasan projek pengesahan sumber** , pada tab **Projek** , dalam medan **Tambah projek ke projek dipilih** , tapis pada projek **Naik taraf XYZ Fasa 2**.</span><span class="sxs-lookup"><span data-stu-id="6c859-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="6c859-115">Dalam anak tetingkap **Baki projek** , pilih projek, dan kemudian pilih butang anak panah untuk menambahnya ke anak tetingkap **Projek dipilih**.</span><span class="sxs-lookup"><span data-stu-id="6c859-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="6c859-116">Anda juga boleh tugaskan kategori untuk sumber yang anda perlukan.</span><span class="sxs-lookup"><span data-stu-id="6c859-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="6c859-117">Jenis kategori ialah sama ada **Kos** atau **Hasil**.</span><span class="sxs-lookup"><span data-stu-id="6c859-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="6c859-118">Jenis kategori adalah ditentukan oleh organisasi anda.</span><span class="sxs-lookup"><span data-stu-id="6c859-118">The category type is determined by your organization.</span></span> <span data-ttu-id="6c859-119">Jika tiada kategori ditugaskan untuk sumber, Kewangan mencari kategori lalai pada harga jam bagi kos dan hasil.</span><span class="sxs-lookup"><span data-stu-id="6c859-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="6c859-120">Sediakan sumber projek dan ciri peranan</span><span class="sxs-lookup"><span data-stu-id="6c859-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="6c859-121">Pengurus projek boleh menggunakan kefungsian penyumberan projek untuk mencipta peranan yang diperlukan untuk projek.</span><span class="sxs-lookup"><span data-stu-id="6c859-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="6c859-122">Peranan boleh digunakan jika sumber yang disahkan masih tidak diketahui apabila sumber diperuntukkan.</span><span class="sxs-lookup"><span data-stu-id="6c859-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="6c859-123">Peranan boleh diperuntukkan sementara sebagai sumber yang dirancang, supaya anda boleh meneruskan peringkat perancangan projek.</span><span class="sxs-lookup"><span data-stu-id="6c859-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="6c859-124">[![Contoh peranan](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="6c859-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="6c859-125">**Senario:** Ariffin diupah untuk melengkapkan Projek masa dan bahan yang mempunyai piagam projek yang diluluskan.</span><span class="sxs-lookup"><span data-stu-id="6c859-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="6c859-126">Pengurus projek muda masih melengkapkan skop projek.</span><span class="sxs-lookup"><span data-stu-id="6c859-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="6c859-127">Resource manager pada masa ini sedang mengenal pasti sumber tertentu yang akan diperuntukkan untuk bekerja pada projek baharu.</span><span class="sxs-lookup"><span data-stu-id="6c859-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="6c859-128">Oleh kerana sifat kritikal projek itu, penaja projek meminta Pengurus projek kanan sebagai salah satu peranan.</span><span class="sxs-lookup"><span data-stu-id="6c859-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="6c859-129">Resource manager mesti mendapatkan sumber baharu dan mentakrifkan peranan dalam sistem sekiranya pengurus projek muda memerlukan maklumat sumber semasa perancangan projek.</span><span class="sxs-lookup"><span data-stu-id="6c859-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="6c859-130">Langkah berikut menunjukkan cara resource manager boleh menyediakan peranan Pengurus projek kanan dan kaitkan ciri sumber dengannya.</span><span class="sxs-lookup"><span data-stu-id="6c859-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="6c859-131">Kemudian, peranan boleh digunakan untuk carian sumber tersedia yang sepadan dengan kecekapan sumber yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="6c859-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="6c859-132">Pada halaman **Peranan persediaan** , pilih **Baharu** , dan masukkan nilai berikut:</span><span class="sxs-lookup"><span data-stu-id="6c859-132">On the **Setup roles** page, select **New** , and enter the following values:</span></span>

    - <span data-ttu-id="6c859-133">**ID peranan:** Pengurus Projek Kanan</span><span class="sxs-lookup"><span data-stu-id="6c859-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="6c859-134">**Perihalan** Pengurus Projek Kanan</span><span class="sxs-lookup"><span data-stu-id="6c859-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="6c859-135">Pilih **Cipta**.</span><span class="sxs-lookup"><span data-stu-id="6c859-135">Select **Create**.</span></span>
3. <span data-ttu-id="6c859-136">Pilih peranan **Pengurus Projek Kanan** , dan kemudian pilih **Ciri konfigurasi**.</span><span class="sxs-lookup"><span data-stu-id="6c859-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="6c859-137">Dalam medan **Jenis ciri** , pilih **Kemahiran**.</span><span class="sxs-lookup"><span data-stu-id="6c859-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="6c859-138">Dalam medan **Ciri tersedia** , masukkan kemahiran untuk carian.</span><span class="sxs-lookup"><span data-stu-id="6c859-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="6c859-139">Dalam medan **Jenis ciri** , pilih **Sijil**.</span><span class="sxs-lookup"><span data-stu-id="6c859-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="6c859-140">Dalam medan **Ciri tersedia** , masukkan jenis sijil untuk carian.</span><span class="sxs-lookup"><span data-stu-id="6c859-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="6c859-141">Tugaskan sumber projek kepada projek</span><span class="sxs-lookup"><span data-stu-id="6c859-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="6c859-142">Pada halaman **Semua projek** , pilih projek **Naik taraf XYZ Fasa 2**.</span><span class="sxs-lookup"><span data-stu-id="6c859-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="6c859-143">Pada tab **Pasukan projek dan penjadualan** , pilih **Tambah**.</span><span class="sxs-lookup"><span data-stu-id="6c859-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="6c859-144">Dalam medan **Peranan** , pilih **Ahli pasukan**.</span><span class="sxs-lookup"><span data-stu-id="6c859-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="6c859-145">Pilih **Tempah daripada kalendar**.</span><span class="sxs-lookup"><span data-stu-id="6c859-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="6c859-146">Pada halaman **Ketersediaan sumber** , pilih **Pandangan tetapan**.</span><span class="sxs-lookup"><span data-stu-id="6c859-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="6c859-147">Pada halaman **Laraskan pandangan tetapan** , masukkan nilai berikut:</span><span class="sxs-lookup"><span data-stu-id="6c859-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="6c859-148">**Format untuk tarikh pandangan julat:** Hari</span><span class="sxs-lookup"><span data-stu-id="6c859-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="6c859-149">**Paparan perihalan ketersediaan:** Ya</span><span class="sxs-lookup"><span data-stu-id="6c859-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="6c859-150">**Paparan kapasiti baki:** Ya</span><span class="sxs-lookup"><span data-stu-id="6c859-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="6c859-151">Dalam senarai sumber, pilih sumber.</span><span class="sxs-lookup"><span data-stu-id="6c859-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="6c859-152">Pilih **Tempah Keras** dan **Kapasiti penuh**.</span><span class="sxs-lookup"><span data-stu-id="6c859-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="6c859-153">Tugaskan sumber kepada peranan lalai</span><span class="sxs-lookup"><span data-stu-id="6c859-153">Assign a resource to a default role</span></span>

<span data-ttu-id="6c859-154">Untuk membantu projek atau pengurus projek boleh gerudi bawah lebih lanjut tentang sumber yang boleh diperuntukkan untuk projek.</span><span class="sxs-lookup"><span data-stu-id="6c859-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="6c859-155">Anda boleh kaitkan peranan lalai dengan sumber sedia ada atau sumber yang baharu diperolehi.</span><span class="sxs-lookup"><span data-stu-id="6c859-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="6c859-156">Contohnya, apabila Daniel diupah, beliau mempunyai pengalaman dan kemahiran untuk mengisi peranan Penganalisis perniagaan.</span><span class="sxs-lookup"><span data-stu-id="6c859-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="6c859-157">Resource manager ditugaskan peranan ini sebagai peranan lalai Daniel.</span><span class="sxs-lookup"><span data-stu-id="6c859-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="6c859-158">Oleh itu, resource manager menambah Daniel kepada himpunan penganalisa perniagaan yang bersedia untuk mengerjakan projek.</span><span class="sxs-lookup"><span data-stu-id="6c859-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="6c859-159">Semasa tempahan sumber, pengurus projek boleh menapis sumber peranan yang tersedia untuk mengerjakan projek.</span><span class="sxs-lookup"><span data-stu-id="6c859-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="6c859-160">Mereka boleh menggunakan maklumat ini sebagai satu kriteria apabila mereka melaksanakan analisis keputusan berbilang kriteria semasa pemenuhan sumber.</span><span class="sxs-lookup"><span data-stu-id="6c859-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="6c859-161">Mereka juga boleh menambah ciri sumber lain kepada penapis untuk carian sumber yang mempunyai kemahiran, pendidikan, dan pengalaman khusus untuk projek yang diberikan.</span><span class="sxs-lookup"><span data-stu-id="6c859-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="6c859-162">**Senario:** Projek yang diluluskan telah dimulakan, dan peranan Pengurus projek kanan telah diperuntukkan sebagai sumber yang dirancang semasa peringkat perancangan projek.</span><span class="sxs-lookup"><span data-stu-id="6c859-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="6c859-163">Resource manager kini telah memperolehi sumber untuk memenuhi peranan Pengurus projek kanan.</span><span class="sxs-lookup"><span data-stu-id="6c859-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="6c859-164">Pada halaman **Senarai sumber** , pilih **Daniel Goldschmidt**.</span><span class="sxs-lookup"><span data-stu-id="6c859-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="6c859-165">Pada halaman **Peranan sumber** , pilih **Baharu** , dan masukkan nilai berikut:</span><span class="sxs-lookup"><span data-stu-id="6c859-165">On the **Resource role** page, select **New** , and enter the following values:</span></span>

    - <span data-ttu-id="6c859-166">**Berkuat kuasa:** Masukkan tarikh semasa.</span><span class="sxs-lookup"><span data-stu-id="6c859-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="6c859-167">**Tamat tempoh:** Masukkan **Jangan sekali-kali**.</span><span class="sxs-lookup"><span data-stu-id="6c859-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="6c859-168">**Peranan:** Masukkan **Pengurus Projek Kanan**.</span><span class="sxs-lookup"><span data-stu-id="6c859-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="6c859-169">Pilih **Simpan** , dan kemudian tutup halaman.</span><span class="sxs-lookup"><span data-stu-id="6c859-169">Select **Save** , and then close the page.</span></span>
4. <span data-ttu-id="6c859-170">Pada tab **Kecekapan** , tambah kemahiran **ProjectMgmt** dan sijil **PMP**.</span><span class="sxs-lookup"><span data-stu-id="6c859-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>
