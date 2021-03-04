---
title: Templat projek
description: Topik ini memberikan maklumat tentang cara untuk menggunakan templat projek untuk persediaan projek pantas.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: db42c9ea7280274cdc9cc90f1487f27e08f892e5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148069"
---
# <a name="project-templates"></a><span data-ttu-id="5efcb-103">Templat projek</span><span class="sxs-lookup"><span data-stu-id="5efcb-103">Project templates</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5efcb-104">Templat projek adalah rangka kerja pratakrif yang membantu anda memulakan projek dengan cepat dan mudah.</span><span class="sxs-lookup"><span data-stu-id="5efcb-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="5efcb-105">Anda boleh menggunakan templat pratakrif untuk mencipta projek baharu dengan satu klik.</span><span class="sxs-lookup"><span data-stu-id="5efcb-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="5efcb-106">Bagi projek, anda mesti mentakrifkan prasyarat untuk templat projek.</span><span class="sxs-lookup"><span data-stu-id="5efcb-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="5efcb-107">Anda mesti mentakrifkan kalendar projek untuk setiap templat projek serta senarai peranan dan harga mesti ditetapkan dalam organisasi, supaya komponen templat mempunyai data berguna.</span><span class="sxs-lookup"><span data-stu-id="5efcb-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="5efcb-108">Templat projek terdiri daripada tiga komponen: jadual, anggaran projek dan ahli pasukan projek.</span><span class="sxs-lookup"><span data-stu-id="5efcb-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="5efcb-109">Jadual</span><span class="sxs-lookup"><span data-stu-id="5efcb-109">Schedule</span></span>

<span data-ttu-id="5efcb-110">Jadual dalam templat projek mempunyai set elemen yang sama dengan jadual dalam projek.</span><span class="sxs-lookup"><span data-stu-id="5efcb-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="5efcb-111">Anda boleh mencipta hierarki tugas, mengaitkan peranan dengan tugas, mentakrifkan atribut jadual dan kebergantungan set.</span><span class="sxs-lookup"><span data-stu-id="5efcb-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="5efcb-112">Jadual dalam templat projek juga menyokong mod tugas untuk setiap tugas.</span><span class="sxs-lookup"><span data-stu-id="5efcb-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="5efcb-113">Oleh itu, ia menyokong enjin penjadualan.</span><span class="sxs-lookup"><span data-stu-id="5efcb-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="5efcb-114">Anda mesti mengaitkan kalendar projek dengan projek tersebut.</span><span class="sxs-lookup"><span data-stu-id="5efcb-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="5efcb-115">Apabila anda mencipta jadual kerja, tidak ada perbezaan antara template projek dan projek.</span><span class="sxs-lookup"><span data-stu-id="5efcb-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="5efcb-116">Anggaran projek</span><span class="sxs-lookup"><span data-stu-id="5efcb-116">Project estimates</span></span>

<span data-ttu-id="5efcb-117">Anggaran projek dalam templat projek berfungsi dengan cara yang sama seperti anggaran projek dalam projek.</span><span class="sxs-lookup"><span data-stu-id="5efcb-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="5efcb-118">Walau bagaimanapun, harga kos dan jualan dikeluarkan daripada senarai kos dan harga jualan lalai yang ditakrifkan dalam parameter.</span><span class="sxs-lookup"><span data-stu-id="5efcb-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="5efcb-119">Mencipta projek daripada templat</span><span class="sxs-lookup"><span data-stu-id="5efcb-119">Creating a project from a template</span></span>
 
<span data-ttu-id="5efcb-120">Terdapat beberapa cara untuk mencipta projek daripada templat projek:</span><span class="sxs-lookup"><span data-stu-id="5efcb-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="5efcb-121">Apabila anda mencipta projek daripada sebut harga, anda boleh memilih templat projek dalam kotak dialog **Cipta Pantas: Projek**.</span><span class="sxs-lookup"><span data-stu-id="5efcb-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Kotak dialog Cipta Pantas: Projek](media/project-11.png)

- <span data-ttu-id="5efcb-123">Apabila anda mencipta projek dengan memilih **Projek Baharu**, halaman **Projek** muncul sebelum rekod disimpan.</span><span class="sxs-lookup"><span data-stu-id="5efcb-123">When you create a project by selecting **New Project**, the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="5efcb-124">Dalam medan **Pilih Templat**, pilih salah satu templat projek yang dipratakrif dalam organisasi.</span><span class="sxs-lookup"><span data-stu-id="5efcb-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="5efcb-125">Gunakan **Cipta Projek daripada Templat** pada halaman **Entiti Templat**.</span><span class="sxs-lookup"><span data-stu-id="5efcb-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="5efcb-126">Menyalin komponen templat kepada projek</span><span class="sxs-lookup"><span data-stu-id="5efcb-126">Copying components of template to project</span></span>

<span data-ttu-id="5efcb-127">Apabila anda menyalin komponen templat projek kepada projek, beberapa gantian boleh berlaku, bergantung pada tetapan dalam projek.</span><span class="sxs-lookup"><span data-stu-id="5efcb-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="5efcb-128">Menyalin jadual</span><span class="sxs-lookup"><span data-stu-id="5efcb-128">Copying the schedule</span></span>

<span data-ttu-id="5efcb-129">Apabila anda menyalin jadual daripada templat projek, jika projek tersebut mempunyai kalendar projek yang berbeza daripada templat, jam kerja daripada kalendar projek akan digunakan pada jadual tugas.</span><span class="sxs-lookup"><span data-stu-id="5efcb-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="5efcb-130">Dengan cara ini, jadual diselaraskan supaya sepadan dengan kalendar projek sokongan.</span><span class="sxs-lookup"><span data-stu-id="5efcb-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="5efcb-131">Begitu juga, tugas pertama pada jadual mengambil tarikh mula projek, dan jadual bagi hierarki yang selebihnya dikemas kini berdasarkan tempoh dan kebergantungan yang ditakrifkan dalam templat.</span><span class="sxs-lookup"><span data-stu-id="5efcb-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="5efcb-132">Menyalin anggaran projek</span><span class="sxs-lookup"><span data-stu-id="5efcb-132">Copying project estimates</span></span> 

<span data-ttu-id="5efcb-133">Apabila anda menyalin merentasi baris anggaran projek, senarai harga dikemas kini.</span><span class="sxs-lookup"><span data-stu-id="5efcb-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="5efcb-134">Untuk senarai harga kos, kemas kini ini adalah berdasarkan unit pemilikan projek.</span><span class="sxs-lookup"><span data-stu-id="5efcb-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="5efcb-135">Untuk senarai harga jualan, ia adalah berdasarkan kepada pelanggan.</span><span class="sxs-lookup"><span data-stu-id="5efcb-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="5efcb-136">Bagi projek yang dikaitkan dengan entiti jualan, kos unit dan harga jualan ditentukan berdasarkan pada senarai harga ini.</span><span class="sxs-lookup"><span data-stu-id="5efcb-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="5efcb-137">Menyalin pasukan projek</span><span class="sxs-lookup"><span data-stu-id="5efcb-137">Copying a project team</span></span>

<span data-ttu-id="5efcb-138">Apabila pasukan projek disalin daripada templat projek kepada projek, sumber generik disalin, bersama-sama dengan kemahiran dan kecekapan yang ditakrifkan dalam template.</span><span class="sxs-lookup"><span data-stu-id="5efcb-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="5efcb-139">Tugasan sumber generik juga dikekalkan sebagai mana ia di dalam templat projek.</span><span class="sxs-lookup"><span data-stu-id="5efcb-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="5efcb-140">Sumber yang dinamakan tidak disokong dalam templat projek.</span><span class="sxs-lookup"><span data-stu-id="5efcb-140">Named resources aren't supported in project templates.</span></span>
