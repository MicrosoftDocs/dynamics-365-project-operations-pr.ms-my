---
title: Tugaskan sumber boleh ditempah generik kepada tugas dan pasukan projek
description: Topik ini memberikan maklumat tentang tempahan sumber generik kepada tugasan dan pasukan projek.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f461fbd3-1fce-4aeb-a896-a6d14453a5a4
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 82478e2cf97ab03e80e9f5fbb662b3603d5905b9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754001"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="39e1d-103">Tugaskan sumber boleh ditempah generik kepada tugas dan menjana keperluan sumber</span><span class="sxs-lookup"><span data-stu-id="39e1d-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="39e1d-104">Selain membuat tempahan dan menugaskan sumber yang dinamakan atau sebenar kepada projek anda, anda boleh menugaskan sumber generik kepada tugas projek.</span><span class="sxs-lookup"><span data-stu-id="39e1d-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="39e1d-105">Sumber ini boleh menjadi pemilik tempat untuk sumber yang dinamakan sehingga anda bersedia untuk menyediakan kakitangan projek anda dengan sumber yang dinamakan.</span><span class="sxs-lookup"><span data-stu-id="39e1d-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="39e1d-106">Dalam Project Service Automation (PSA), buka halaman **Projek** dan pada tab **Jadual**, masukkan nama kedudukan sumber generik dalam sel **Sumber** jadual.</span><span class="sxs-lookup"><span data-stu-id="39e1d-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="39e1d-107">Atau, klik ikon **Sumber** dalam sel untuk membuka pemilih sumber dan kemudian masukkan nama sumber generik yang anda ingin cipta.</span><span class="sxs-lookup"><span data-stu-id="39e1d-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Mencipta dan menugaskan ahli pasukan generik](media/RM-how-to-9.png)

<span data-ttu-id="39e1d-109">Ini akan membuka panel **Cipta Pantas: Ahli Pasukan Projek**.</span><span class="sxs-lookup"><span data-stu-id="39e1d-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="39e1d-110">Masukkan peranan dan unit organisasi bagi ahli pasukan sumber generik dan kemudian klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="39e1d-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Cipta pantas ahli pasukan generik](media/RM-how-to-10.png)

3. <span data-ttu-id="39e1d-112">Selepas anda telah mencipta ahli pasukan sumber generik yang baharu, ia ditugaskan kepada tugas.</span><span class="sxs-lookup"><span data-stu-id="39e1d-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="39e1d-113">Anda boleh terus menugaskan sumber generik itu kepada tugas lain dalam jadual tugas.</span><span class="sxs-lookup"><span data-stu-id="39e1d-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Menugaskan ahli pasukan generik sedia ada kepada tugasan](media/RM-how-to-11.png)

4. <span data-ttu-id="39e1d-115">Selepas anda telah menugaskan sumber generik, anda boleh menjana keperluan sumber dan melaksanakannya dengan menempah secara langsung atau menyerahkan permintaan sumber kepada pengurus sumber.</span><span class="sxs-lookup"><span data-stu-id="39e1d-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Menjana keperluan untuk ahli pasukan generik](media/RM-how-to-12.png)

<span data-ttu-id="39e1d-117">Pada grid ahli pasukan, selain daripada boleh menggunakan pemilih sumber seperti yang dinyatakan di atas, anda boleh menambah sumber generik secara langsung.</span><span class="sxs-lookup"><span data-stu-id="39e1d-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="39e1d-118">Sumber ditambah dengan keperluan sumber yang berdasarkan pada tarikh mula/tamat dan kaedah peruntukan yang ditetapkan dalam panel **Cipta Pantas: Ahli Pasukan**.</span><span class="sxs-lookup"><span data-stu-id="39e1d-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="39e1d-119">Anda boleh melihat perbezaan jika anda menambah ahli pasukan generik secara langsung dan kemudian menugaskan lebih banyak tugas kepada sumber generik berbanding mereka memerlukan waktu untuk meliputi.</span><span class="sxs-lookup"><span data-stu-id="39e1d-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="39e1d-120">Klik **Jana Keperluan** untuk menjana semula keperluan untuk mengimbangkan jam yang diperlukan terhadap tugasan.</span><span class="sxs-lookup"><span data-stu-id="39e1d-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="39e1d-121">Anda juga boleh mengklik pautan **Keperluan sumber** dalam grid pasukan untuk membuka keperluan dan menambah kemahiran, sumber pilihan dll.</span><span class="sxs-lookup"><span data-stu-id="39e1d-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Keperluan sumber](media/RM-how-to-13.png)

