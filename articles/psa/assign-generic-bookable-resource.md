---
title: Tugaskan sumber boleh ditempah generik kepada tugas dan pasukan projek
description: Topik ini memberikan maklumat tentang tempahan sumber generik kepada tugasan dan pasukan projek.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 5b4c47513b96310745fd2cdb296988a57df0e966
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291405"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="ebb6b-103">Tugaskan sumber boleh ditempah generik kepada tugas dan menjana keperluan sumber</span><span class="sxs-lookup"><span data-stu-id="ebb6b-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ebb6b-104">Selain membuat tempahan dan menugaskan sumber yang dinamakan atau sebenar kepada projek anda, anda boleh menugaskan sumber generik kepada tugas projek.</span><span class="sxs-lookup"><span data-stu-id="ebb6b-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="ebb6b-105">Sumber ini boleh menjadi pemilik tempat untuk sumber yang dinamakan sehingga anda bersedia untuk menyediakan kakitangan projek anda dengan sumber yang dinamakan.</span><span class="sxs-lookup"><span data-stu-id="ebb6b-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="ebb6b-106">Dalam Project Service Automation (PSA), buka halaman **Projek** dan pada tab **Jadual**, masukkan nama kedudukan sumber generik dalam sel **Sumber** jadual.</span><span class="sxs-lookup"><span data-stu-id="ebb6b-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="ebb6b-107">Atau, klik ikon **Sumber** dalam sel untuk membuka pemilih sumber dan kemudian masukkan nama sumber generik yang anda ingin cipta.</span><span class="sxs-lookup"><span data-stu-id="ebb6b-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Mencipta dan menugaskan ahli pasukan generik](media/RM-how-to-9.png)

<span data-ttu-id="ebb6b-109">Ini akan membuka panel **Cipta Pantas: Ahli Pasukan Projek**.</span><span class="sxs-lookup"><span data-stu-id="ebb6b-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="ebb6b-110">Masukkan peranan dan unit organisasi bagi ahli pasukan sumber generik dan kemudian klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="ebb6b-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Cipta pantas ahli pasukan generik](media/RM-how-to-10.png)

3. <span data-ttu-id="ebb6b-112">Selepas anda telah mencipta ahli pasukan sumber generik yang baharu, ia ditugaskan kepada tugas.</span><span class="sxs-lookup"><span data-stu-id="ebb6b-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="ebb6b-113">Anda boleh terus menugaskan sumber generik itu kepada tugas lain dalam jadual tugas.</span><span class="sxs-lookup"><span data-stu-id="ebb6b-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Menugaskan ahli pasukan generik sedia ada kepada tugasan](media/RM-how-to-11.png)

4. <span data-ttu-id="ebb6b-115">Selepas anda telah menugaskan sumber generik, anda boleh menjana keperluan sumber dan melaksanakannya dengan menempah secara langsung atau menyerahkan permintaan sumber kepada pengurus sumber.</span><span class="sxs-lookup"><span data-stu-id="ebb6b-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Menjana keperluan untuk ahli pasukan generik](media/RM-how-to-12.png)

<span data-ttu-id="ebb6b-117">Pada grid ahli pasukan, selain daripada boleh menggunakan pemilih sumber seperti yang dinyatakan di atas, anda boleh menambah sumber generik secara langsung.</span><span class="sxs-lookup"><span data-stu-id="ebb6b-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="ebb6b-118">Sumber ditambah dengan keperluan sumber yang berdasarkan pada tarikh mula/tamat dan kaedah peruntukan yang ditetapkan dalam panel **Cipta Pantas: Ahli Pasukan**.</span><span class="sxs-lookup"><span data-stu-id="ebb6b-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="ebb6b-119">Anda boleh melihat perbezaan jika anda menambah ahli pasukan generik secara langsung dan kemudian menugaskan lebih banyak tugas kepada sumber generik berbanding mereka memerlukan waktu untuk meliputi.</span><span class="sxs-lookup"><span data-stu-id="ebb6b-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="ebb6b-120">Klik **Jana Keperluan** untuk menjana semula keperluan untuk mengimbangkan jam yang diperlukan terhadap tugasan.</span><span class="sxs-lookup"><span data-stu-id="ebb6b-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="ebb6b-121">Anda juga boleh mengklik pautan **Keperluan sumber** dalam grid pasukan untuk membuka keperluan dan menambah kemahiran, sumber pilihan dll.</span><span class="sxs-lookup"><span data-stu-id="ebb6b-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Keperluan sumber](media/RM-how-to-13.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]