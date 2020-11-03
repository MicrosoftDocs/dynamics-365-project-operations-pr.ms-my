---
title: Gunakan Tambahan Project Service untuk merancang kerja anda dalam Microsoft Project | MicrosoftDocs
description: Topik ini memberikan maklumat tentang cara untuk menambah, mengkonfigurasi dan menggunakan tambahan Microsoft Project untuk Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: 1d988419ae5a9d57532902d2553cd7de147e27c1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081358"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="a1e88-103">Gunakan tambahan Project Service Automation untuk merancang kerja anda dalam Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="a1e88-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="a1e88-104">memudahkan anda membuat perancangan projek anda, termasuk anggaran.</span><span class="sxs-lookup"><span data-stu-id="a1e88-104">makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="a1e88-105">Anda boleh mentakrifkan kerja supaya nilai kos, usaha dan jualan jelas seperti cadangan akhir diserahkan.</span><span class="sxs-lookup"><span data-stu-id="a1e88-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="a1e88-106">Anda kini boleh memasang [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] dan melakukan kerja perancangan anda dalam persekitaran [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] yang biasa.</span><span class="sxs-lookup"><span data-stu-id="a1e88-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="a1e88-107">Gunakan keupayaan perancangan dan pengurusan [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] yang kukuh dan kemudian kemas kini rancangan projek anda dalam Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a1e88-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="a1e88-108">Untuk menggunakan pengurusan dokumen SharePoint bagi menyimpan fail [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] anda untuk projek [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], pentadbir [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] anda perlu menghidupkan pengurusan dokumen.</span><span class="sxs-lookup"><span data-stu-id="a1e88-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> 
> - <span data-ttu-id="a1e88-109">[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] adalah satu-satunya yang serasi dengan [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span><span class="sxs-lookup"><span data-stu-id="a1e88-109">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="a1e88-110">Muat turun dan pasang tambahan</span><span class="sxs-lookup"><span data-stu-id="a1e88-110">Download and install the add-in</span></span>  
 <span data-ttu-id="a1e88-111">Pastikan maklumat daftar masuk [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] anda tersedia.</span><span class="sxs-lookup"><span data-stu-id="a1e88-111">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="a1e88-112">Anda akan memerlukan maklumat ini untuk menyambung daripada [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] kepada [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a1e88-112">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="a1e88-113">Daripada Pusat Muat Turun, muat turun tambahan untuk versi Project Service anda yang disokong, sama ada [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) atau [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span><span class="sxs-lookup"><span data-stu-id="a1e88-113">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="a1e88-114">Klik pautan muat turun.</span><span class="sxs-lookup"><span data-stu-id="a1e88-114">Click the download link.</span></span>  

3.  <span data-ttu-id="a1e88-115">Apabila muat turun selesai, klik **Ya** untuk memasang tambahan.</span><span class="sxs-lookup"><span data-stu-id="a1e88-115">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="a1e88-116">Konfigurasikan tambahan</span><span class="sxs-lookup"><span data-stu-id="a1e88-116">Configure the add-in</span></span>  

1. <span data-ttu-id="a1e88-117">Buka [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dan klik tab **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="a1e88-117">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="a1e88-118">Klik **Sambung**.</span><span class="sxs-lookup"><span data-stu-id="a1e88-118">Click **Connect**.</span></span>  

3. <span data-ttu-id="a1e88-119">Masukkan maklumat daftar masuk anda dan kemudian klik **Daftar Masuk**.</span><span class="sxs-lookup"><span data-stu-id="a1e88-119">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="a1e88-120">Anda boleh mula menggunakan tambahan sekarang.</span><span class="sxs-lookup"><span data-stu-id="a1e88-120">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="a1e88-121">Baca daripada templat</span><span class="sxs-lookup"><span data-stu-id="a1e88-121">Read from a template</span></span>  
 <span data-ttu-id="a1e88-122">Baca daripada templat yang anda cipta dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] disalin ke dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] untuk memulakan perancangan projek anda.</span><span class="sxs-lookup"><span data-stu-id="a1e88-122">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="a1e88-123">[Cipta templat projek (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="a1e88-123">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1.  <span data-ttu-id="a1e88-124">Daripada tab **Project Service** , klik **Baca** > **Templat Projek bagi Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="a1e88-124">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="a1e88-125">Pilih templat projek daripada senarai dan kemudian klik **Buka**.</span><span class="sxs-lookup"><span data-stu-id="a1e88-125">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="a1e88-126">Secara lalai, tugas yang disalin daripada templat ke dalam Projek ditetapkan seperti yang dijadualkan secara manual.</span><span class="sxs-lookup"><span data-stu-id="a1e88-126">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="a1e88-127">Untukkan peranan [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kepada sumber projek</span><span class="sxs-lookup"><span data-stu-id="a1e88-127">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="a1e88-128">Buka projek dan klik reben **Tugas**.</span><span class="sxs-lookup"><span data-stu-id="a1e88-128">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="a1e88-129">Klik menu **Carta Gantt** dan kemudian pilih **Helaian Sumber**.</span><span class="sxs-lookup"><span data-stu-id="a1e88-129">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="a1e88-130">Pada Helaian Sumber, klik menu juntai bawah **Peranan Sumber Project Service** dan pilih peranan Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a1e88-130">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="a1e88-131">Tetapkan sumber untuk projek anda</span><span class="sxs-lookup"><span data-stu-id="a1e88-131">Staff your project with resources</span></span>  

1.  <span data-ttu-id="a1e88-132">Daripada tab Project Service, pilih baris dan klik **Cari Sumber**.</span><span class="sxs-lookup"><span data-stu-id="a1e88-132">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="a1e88-133">Pada skrin **Tempah Sumber** , pilih sumber yang anda mahu gunakan untuk projek.</span><span class="sxs-lookup"><span data-stu-id="a1e88-133">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="a1e88-134">Klik **Tempah** dan kemudian klik **OK**.</span><span class="sxs-lookup"><span data-stu-id="a1e88-134">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="a1e88-135">Terbitkan projek anda</span><span class="sxs-lookup"><span data-stu-id="a1e88-135">Publish your project</span></span>  
<span data-ttu-id="a1e88-136">Apabila perancangan projek anda selesai, langkah seterusnya adalah untuk mengimport dan menerbitkan projek ke dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a1e88-136">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="a1e88-137">Projek akan mengimport ke dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a1e88-137">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="a1e88-138">Proses penjanaan harga dan pasukan diguna pakai.</span><span class="sxs-lookup"><span data-stu-id="a1e88-138">The pricing and team generation process are applied.</span></span> <span data-ttu-id="a1e88-139">Buka projek dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] untuk melihat bahawa pasukan, anggaran projek dan struktur pecahan kerja telah dijanakan.</span><span class="sxs-lookup"><span data-stu-id="a1e88-139">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="a1e88-140">Jadual berikut menunjukkan tempat untuk mencari hasil:</span><span class="sxs-lookup"><span data-stu-id="a1e88-140">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="a1e88-141">**Carta Gantt**</span><span class="sxs-lookup"><span data-stu-id="a1e88-141">**Gantt Chart**</span></span>   | <span data-ttu-id="a1e88-142">Mengimport ke dalam skrin **Struktur Pecahan Kerja** [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a1e88-142">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="a1e88-143">**Lembaran Sumber**</span><span class="sxs-lookup"><span data-stu-id="a1e88-143">**Resource Sheet**</span></span> |   <span data-ttu-id="a1e88-144">Mengimport ke dalam skrin **Ahli Pasukan Projek** [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] .</span><span class="sxs-lookup"><span data-stu-id="a1e88-144">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="a1e88-145">**Gunakan Penggunaan**</span><span class="sxs-lookup"><span data-stu-id="a1e88-145">**Use Usage**</span></span>    |    <span data-ttu-id="a1e88-146">Mengimport ke dalam skrin **Anggaran Projek** [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a1e88-146">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="a1e88-147">**Untuk mengimport dan menerbitkan projek anda**</span><span class="sxs-lookup"><span data-stu-id="a1e88-147">**To import and publish your project**</span></span>  
1. <span data-ttu-id="a1e88-148">Daripada tab **Project Service** , klik **Terbitkan** > **Projek Project Service Automation Baharu**.</span><span class="sxs-lookup"><span data-stu-id="a1e88-148">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="a1e88-149">Pada kotak dialog **Terbitkan pada projek baharu dalam Project Service** , masukkan **Nama Projek** dan pilih **Pelanggan**.</span><span class="sxs-lookup"><span data-stu-id="a1e88-149">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="a1e88-150">Secara pilihan, semak **Pautkan rancangan projek kepada Project Service Automation** untuk memautkan fail Projek rancangan kepada Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a1e88-150">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="a1e88-151">Klik **Terbitkan**.</span><span class="sxs-lookup"><span data-stu-id="a1e88-151">Click **Publish**.</span></span>  

   <span data-ttu-id="a1e88-152">Memautkan fail Projek kepada [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] menjadikan fail Projek sebagai fail induk dan menetapkan struktur pecahan kerja dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kepada baca sahaja.</span><span class="sxs-lookup"><span data-stu-id="a1e88-152">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="a1e88-153">Untuk membuat perubahan kepada rancangan projek, anda perlu membuatnya dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dan menerbitkannya sebagai kemas kini untuk [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a1e88-153">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="a1e88-154">Edit projek yang telah diimport</span><span class="sxs-lookup"><span data-stu-id="a1e88-154">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="a1e88-155">Untuk membuat perubahan kepada rancangan projek yang diimport ke dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], anda mempunyai dua pilihan:</span><span class="sxs-lookup"><span data-stu-id="a1e88-155">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="a1e88-156">Buka fail induk dan edit ia dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="a1e88-156">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="a1e88-157">Nyahpaut fail dan edit ia secara terus dalam Project Service.</span><span class="sxs-lookup"><span data-stu-id="a1e88-157">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="a1e88-158">Secara lalai, projek yang telah dimuat naik daripada [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dikunci dan hanya boleh diedit dalam Projek.</span><span class="sxs-lookup"><span data-stu-id="a1e88-158">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="a1e88-159">Untuk mengedit fail dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], fail perlu dinyahpautkan.</span><span class="sxs-lookup"><span data-stu-id="a1e88-159">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="a1e88-160">Edit dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="a1e88-160">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="a1e88-161">Daripada menu utama, klik **Project Service** > **Projek**.</span><span class="sxs-lookup"><span data-stu-id="a1e88-161">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="a1e88-162">Daripada senarai projek, buka projek yang anda cipta dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="a1e88-162">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="a1e88-163">Klik **Buka dalam MS Project** daripada reben.</span><span class="sxs-lookup"><span data-stu-id="a1e88-163">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="a1e88-164">Ini akan membuka fail induk yang dipautkan dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="a1e88-164">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="a1e88-165">Nyahpautkan fail dan edit ia dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span><span class="sxs-lookup"><span data-stu-id="a1e88-165">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="a1e88-166">Daripada menu utama, klik **Project Service** > **Projek**.</span><span class="sxs-lookup"><span data-stu-id="a1e88-166">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="a1e88-167">Daripada senarai projek, buka projek yang anda cipta dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="a1e88-167">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="a1e88-168">Klik **Nyahpaut daripada MS Project** daripada reben.</span><span class="sxs-lookup"><span data-stu-id="a1e88-168">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="a1e88-169">Muat naik fail Projek ke SharePoint atau Kumpulan Office</span><span class="sxs-lookup"><span data-stu-id="a1e88-169">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="a1e88-170">Anda boleh memuat naik fail Projek anda ke SharePoint dan menemuinya di bawah Dokumen Berkaitan untuk projek [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] anda.</span><span class="sxs-lookup"><span data-stu-id="a1e88-170">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="a1e88-171">Anda perlu meminta pentadbir anda mengkonfigurasikan pengurusan dokumen SharePoint dan menghidupkannya untuk entiti Projek.</span><span class="sxs-lookup"><span data-stu-id="a1e88-171">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> 

 <span data-ttu-id="a1e88-172">Anda juga boleh memuat naik fail Projek anda kepada [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] jika anda telah menyediakan Kumpulan Office.</span><span class="sxs-lookup"><span data-stu-id="a1e88-172">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span>

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="a1e88-173">Muat naik fail untuk SharePoint</span><span class="sxs-lookup"><span data-stu-id="a1e88-173">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="a1e88-174">Daripada menu utama, klik **Project Service** > **Muat Naik**.</span><span class="sxs-lookup"><span data-stu-id="a1e88-174">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="a1e88-175">Pilih **Ke Dokumen Projek Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="a1e88-175">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="a1e88-176">Pada dialog **Dayakan Buka dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** , pilih **Ya** atau **Tidak**.</span><span class="sxs-lookup"><span data-stu-id="a1e88-176">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="a1e88-177">Jika anda klik **Ya** , anda akan dapat memilih butang **Buka dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dalam Project Service Automation, melancarkan [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dan memuatkan fail Projek daripada pustaka dokumen SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a1e88-177">If you click **Yes** , you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="a1e88-178">Jika anda klik **Tidak** , pautan untuk butang **Buka dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** tidak akan berfungsi.</span><span class="sxs-lookup"><span data-stu-id="a1e88-178">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="a1e88-179">Fail [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] boleh ditemui dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] di bawah **Dokumen** untuk projek [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] tertentu.</span><span class="sxs-lookup"><span data-stu-id="a1e88-179">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="a1e88-180">Muat naik fail untuk Kumpulan Office</span><span class="sxs-lookup"><span data-stu-id="a1e88-180">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="a1e88-181">Daripada menu utama, klik **Project Service** > **Muat Naik**.</span><span class="sxs-lookup"><span data-stu-id="a1e88-181">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="a1e88-182">Pilih **Ke Dokumen Projek Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="a1e88-182">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="a1e88-183">Pada dialog **Dayakan Buka dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** , pilih **Ya** atau **Tidak**.</span><span class="sxs-lookup"><span data-stu-id="a1e88-183">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="a1e88-184">Jika anda klik **Ya** , anda akan dapat memilih butang **Buka dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dalam Project Service Automation, melancarkan [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dan memuatkan fail Projek daripada pustaka dokumen SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a1e88-184">If you click **Yes** , you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="a1e88-185">Jika anda klik **Tidak** , pautan untuk butang **Buka dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** tidak akan berfungsi.</span><span class="sxs-lookup"><span data-stu-id="a1e88-185">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="a1e88-186">Fail [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] boleh ditemui dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] di bawah **Dokumen** untuk projek [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] tertentu.</span><span class="sxs-lookup"><span data-stu-id="a1e88-186">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="a1e88-187">Terbitkan projek anda sebagai templat</span><span class="sxs-lookup"><span data-stu-id="a1e88-187">Publish  your project as a template</span></span>  
 <span data-ttu-id="a1e88-188">Anda boleh menyimpan projek anda dan menggunakannya semula dengan menyimpannya sebagai templat projek dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a1e88-188">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="a1e88-189">Templat projek ialah rancangan projek yang boleh digunakan semula dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a1e88-189">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="a1e88-190">[Cipta templat projek (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="a1e88-190">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1. <span data-ttu-id="a1e88-191">Daripada tab **Project Service** , klik **Terbitkan** > **Templat Projek bagi Project Service Automation Baharu**.</span><span class="sxs-lookup"><span data-stu-id="a1e88-191">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="a1e88-192">Pada kotak dialog **Terbitkan ke projek baharu dalam templat Project Service** , masukkan **Nama templat projek**.</span><span class="sxs-lookup"><span data-stu-id="a1e88-192">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="a1e88-193">Secara pilihan, semak **Pautkan rancangan projek kepada Project Service Automation** untuk memautkan fail Projek kepada [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a1e88-193">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="a1e88-194">Klik **Terbitkan**.</span><span class="sxs-lookup"><span data-stu-id="a1e88-194">Click **Publish**.</span></span>  

<span data-ttu-id="a1e88-195">Memautkan fail Projek kepada [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] menjadikan fail Projek sebagai fail induk dan menetapkan struktur pecahan kerja dalam templat [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kepada baca sahaja.</span><span class="sxs-lookup"><span data-stu-id="a1e88-195">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="a1e88-196">Untuk membuat perubahan kepada rancangan projek, anda perlu membuatnya dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dan menerbitkannya sebagai kemas kini untuk [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a1e88-196">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="a1e88-197">Lihat Juga</span><span class="sxs-lookup"><span data-stu-id="a1e88-197">See Also</span></span>  
 [<span data-ttu-id="a1e88-198">Panduan Pengurus Projek</span><span class="sxs-lookup"><span data-stu-id="a1e88-198">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
