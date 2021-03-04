---
title: Cipta templat projek
description: Cara untuk mencipta templat projek dalam Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: efc404131208e1c971cb091cf174c1f4707552f0
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149374"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="540ac-103">Cipta templat projek (Project Service)</span><span class="sxs-lookup"><span data-stu-id="540ac-103">Create a project template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="540ac-104">Templat projek menjimatkan masa anda jika syarikat anda membida dengan kerap pada jenis produk yang serupa.</span><span class="sxs-lookup"><span data-stu-id="540ac-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="540ac-105">Mereka menyediakan set peranan standard dan anggaran jam untuk jenis projek.</span><span class="sxs-lookup"><span data-stu-id="540ac-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="540ac-106">Pengurus akaun dan pengurus projek boleh mencipta projek berdasarkan templat projek atau mereka boleh menyalin templat dan membuat templat mereka sendiri.</span><span class="sxs-lookup"><span data-stu-id="540ac-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="540ac-107">Komponen templat projek</span><span class="sxs-lookup"><span data-stu-id="540ac-107">Components of project template</span></span>
 <span data-ttu-id="540ac-108">Templat projek terdiri daripada tiga komponen:</span><span class="sxs-lookup"><span data-stu-id="540ac-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="540ac-109">**Struktur pecahan kerja**: Struktur pecahan kerja dalam templat projek mempunyai set elemen yang sama seperti dalam projek.</span><span class="sxs-lookup"><span data-stu-id="540ac-109">**Work breakdown structure**: A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="540ac-110">Anda boleh mencipta hierarki tugas, mengaitkan peranan dengan tugas, mentakrifkan atribut jadual, menetapkan kebergantungan dan melihat semua data dalam Gantt.</span><span class="sxs-lookup"><span data-stu-id="540ac-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="540ac-111">Struktur pecahan kerja dalam templat projek juga menyokong mod tugas untuk setiap tugas.</span><span class="sxs-lookup"><span data-stu-id="540ac-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="540ac-112">Tiada perbezaan antara templat projek dengan projek apabila mencipta jadual kerja.</span><span class="sxs-lookup"><span data-stu-id="540ac-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="540ac-113">**Anggaran projek**: Anggaran projek dalam templat mempunyai fungsi yang sama seperti dalam projek, kecuali senarai harga untuk penetapan lalai kos dan harga jualan sentiasa senarai kos dan harga jualan yang ditakrifkan dalam parameter [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="540ac-113">**Project estimates**: Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="540ac-114">Kefungsian yang lain sama seperti dalam projek.</span><span class="sxs-lookup"><span data-stu-id="540ac-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="540ac-115">**Pembentukan pasukan projek**: Apabila membentuk pasukan projek untuk templat projek, anda tidak boleh menempah sumber bernama dalam templat.</span><span class="sxs-lookup"><span data-stu-id="540ac-115">**Project team formation**: When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="540ac-116">Anda boleh menggunakan **Jana Pasukan Projek** dalam struktur pecahan kerja untuk menjana set sumber generik.</span><span class="sxs-lookup"><span data-stu-id="540ac-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="540ac-117">Anda juga boleh menentukan kemahiran dan kecekapan yang diperlukan untuk sumber generik.</span><span class="sxs-lookup"><span data-stu-id="540ac-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="540ac-118">Anda tidak boleh menggantikan sumber generik dengan sumber yang boleh ditempah dalam templat projek.</span><span class="sxs-lookup"><span data-stu-id="540ac-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="540ac-119">Cipta projek daripada templat</span><span class="sxs-lookup"><span data-stu-id="540ac-119">Create a project from a template</span></span>  
 <span data-ttu-id="540ac-120">Anda boleh mencipta projek daripada templat dengan cara berikut:</span><span class="sxs-lookup"><span data-stu-id="540ac-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="540ac-121">Apabila mencipta projek daripada sebut harga, anda boleh memilih templat projek dalam borang cipta cepat projek.</span><span class="sxs-lookup"><span data-stu-id="540ac-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="540ac-122">Apabila mencipta projek dengan mengklik **Projek Baharu**, borang projek memaparkan sebelum anda menyimpan rekod.</span><span class="sxs-lookup"><span data-stu-id="540ac-122">When creating a project by clicking **New Project**, the project form displays before you save the record.</span></span> <span data-ttu-id="540ac-123">Dari sini, anda boleh klik medan **Pilih templat** untuk memilih daripada templat projek yang ditakrifkan lebih awal dalam organisasi anda.</span><span class="sxs-lookup"><span data-stu-id="540ac-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="540ac-124">Klik **Cipta projek daripada templat** pada halaman **Templat Projek** untuk mencipta projek daripada templat.</span><span class="sxs-lookup"><span data-stu-id="540ac-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="540ac-125">Menyalin komponen templat kepada projek</span><span class="sxs-lookup"><span data-stu-id="540ac-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="540ac-126">Apabila anda menyalin komponen templat ke dalam projek, terdapat beberapa perkara yang perlu anda tahu mengenainya.</span><span class="sxs-lookup"><span data-stu-id="540ac-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="540ac-127">**Menyalin struktur pecahan kerja**: Apabila anda menyalin struktur pecahan kerja daripada templat kerja, jika projek mempunyai kalendar projek yang berbeza daripada templat, waktu kerja daripada kalendar projek akan dikenakan kepada jadual tugas.</span><span class="sxs-lookup"><span data-stu-id="540ac-127">**Copying a work breakdown structure**: When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="540ac-128">Ini menyesuaikan jadual untuk kalendar projek sandaran.</span><span class="sxs-lookup"><span data-stu-id="540ac-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="540ac-129">Begitu juga, tugas pertama pada struktur pecahan kerja mengambil tarikh mula, jadi jadual hierarki tugas lain dikemas kini berdasarkan tempoh dan kebergantungan yang ditentukan dalam struktur pecahan kerja templat.</span><span class="sxs-lookup"><span data-stu-id="540ac-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="540ac-130">**Menyalin anggaran projek**: Apabila anda menyalin merentasi garisan anggaran projek, senarai harga dikemas kini berdasarkan unit pemilikan projek untuk senarai harga kos dan pelanggan untuk senarai harga jualan.</span><span class="sxs-lookup"><span data-stu-id="540ac-130">**Copying project estimates**: When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="540ac-131">Kos unit dan harga jualan ditentukan daripada senarai harga ini pada projek yang dikaitkan dengan entiti jualan.</span><span class="sxs-lookup"><span data-stu-id="540ac-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="540ac-132">**Menyalin pasukan projek**: Apabila anda menyalin pasukan projek daripada templat kepada projek, sumber generik disalin merentasi, bersama dengan kemahiran dan kecekapan yang ditentukan dalam templat.</span><span class="sxs-lookup"><span data-stu-id="540ac-132">**Copying a project team**: When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="540ac-133">Tugasan sumber generik juga dikekalkan sebagai mana dalam templat projek.</span><span class="sxs-lookup"><span data-stu-id="540ac-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="540ac-134">Lihat Juga</span><span class="sxs-lookup"><span data-stu-id="540ac-134">See Also</span></span>  
 [<span data-ttu-id="540ac-135">Panduan Pengurus Projek</span><span class="sxs-lookup"><span data-stu-id="540ac-135">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
