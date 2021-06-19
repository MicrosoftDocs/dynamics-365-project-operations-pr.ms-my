---
title: Tempah sumber nama daripada keperluan sumber.
description: Topik ini memberikan maklumat tentang menempah sumber bernama untuk keperluan sumber generik.
author: JohnPBurrows
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
ms.openlocfilehash: c2f97107de938975491770ab4e2ed18a3145d0e3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013407"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="e7074-103">Tempah sumber nama daripada keperluan sumber.</span><span class="sxs-lookup"><span data-stu-id="e7074-103">Book named resources from resource requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e7074-104">Anda boleh menempah sumber bernama untuk menggantikan sumber generik yang mempunyai keperluan sumber.</span><span class="sxs-lookup"><span data-stu-id="e7074-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="e7074-105">Dalam Project Service Automation (PSA), pada halaman **Projek**, klik tab **Pasukan**.</span><span class="sxs-lookup"><span data-stu-id="e7074-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="e7074-106">Pilih sumber generik yang mempunyai keperluan sumber daripada senarai dan kemudian klik **Tempah**.</span><span class="sxs-lookup"><span data-stu-id="e7074-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="e7074-107">Atau, buka keperluan sumber dan kemudian klik **Tempah**.</span><span class="sxs-lookup"><span data-stu-id="e7074-107">Or, open the resource requirement and then click **Book**.</span></span>


![Menempah ahli pasukan generik](media/RM-how-to-14.png)


3. <span data-ttu-id="e7074-109">Pada halaman **Pembantu Jadual**, pilih sumber bernama untuk menempah ke dalam pasukan projek anda dan kemudian klik **Tempah**.</span><span class="sxs-lookup"><span data-stu-id="e7074-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Menempah ahli pasukan generik menggunakan pembantu jadual](media/RM-how-to-15.png)

<span data-ttu-id="e7074-111">Apabila tempahan selesai dan diisi dengan sumber bernama, sumber generik digantikan dengan sumber bernama.</span><span class="sxs-lookup"><span data-stu-id="e7074-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Ahli pasukan bernama menggantikan ahli pasukan generik](media/RM-how-to-16.png)

<span data-ttu-id="e7074-113">Tugasan ke atas jadual dikemas kini dengan sumber bernama juga.</span><span class="sxs-lookup"><span data-stu-id="e7074-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Ahli pasukan bernama ditugaskan kepada tugas projek](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="e7074-115">Isi sumber generik dengan berbilang sumber bernama</span><span class="sxs-lookup"><span data-stu-id="e7074-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="e7074-116">Mengisi keperluan untuk sumber generik dengan berbilang sumber bernama adalah serupa dengan menugaskan sumber bernama tunggal.</span><span class="sxs-lookup"><span data-stu-id="e7074-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="e7074-117">Contohnya, terdapat tugas yang mempunyai tempoh lima hari dan 120 jam usaha.</span><span class="sxs-lookup"><span data-stu-id="e7074-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="e7074-118">Tugas ini tidak boleh diselesaikan oleh satu sumber yang bekerja 8 jam sehari selama lima hari seminggu yang biasa.</span><span class="sxs-lookup"><span data-stu-id="e7074-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![Tugas yang memerlukan 120 jam usaha selama lima hari](media/RM-how-to-21.png)

<span data-ttu-id="e7074-120">Keperluan adalah untuk 120 jam bagi kejuruteraan robotik selama lima hari, yang mana 24 jam sehari.</span><span class="sxs-lookup"><span data-stu-id="e7074-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Keperluan setiap hari](media/RM-how-to-22.png)

<span data-ttu-id="e7074-122">Ini adalah contoh ketika sumber berbilang diperlukan untuk mengisi permintaan sumber generik.</span><span class="sxs-lookup"><span data-stu-id="e7074-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="e7074-123">Anda perlu menempah berbilang sumber untuk mengisi keperluan.</span><span class="sxs-lookup"><span data-stu-id="e7074-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Menempah berbilang sumber untuk mengisi keperluan](media/RM-how-to-23.png)

<span data-ttu-id="e7074-125">Perbezaan utama dalam senario ini ialah bahawa sumber generik kekal dalam pasukan yang ditugaskan kepada tugas, dan ahli pasukan sumber bernama yang ditempah tidak ditugaskan sebagai sebahagian daripada kedudukan tersebut.</span><span class="sxs-lookup"><span data-stu-id="e7074-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="e7074-126">Pengurus projek boleh menugaskan kerja sebagai sesuai kepada sumber bernama.</span><span class="sxs-lookup"><span data-stu-id="e7074-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="e7074-127">Pandangan **Penyesuaian** boleh membantu pengurus projek dalam memecahkan tempahan di semua berbilang sumber untuk menugaskan tugasan.</span><span class="sxs-lookup"><span data-stu-id="e7074-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="e7074-128">Ini tidak dilakukan secara automatik kerana dalam mana-mana senario yang lebih rumit daripada contoh mudah di atas, seperti di mana anda mempunyai tugas yang memenuhi keperluan, niat tentang cara pengurus projek mahu menugaskan, perlu disangka oleh sistem.</span><span class="sxs-lookup"><span data-stu-id="e7074-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="e7074-129">Disebabkan sistem tidak boleh memahami niat, peluang adalah bahawa sangkaan akan berbeza daripada yang diniatkan, dan hasil yang tidak betul atau tidak dijangka akan berlaku.</span><span class="sxs-lookup"><span data-stu-id="e7074-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="e7074-130">Hasil yang boleh dijangka ialah sumber generik kekal ditugaskan sehingga pengurus projek secara sengaja mencipta tugasan, dengan bantuan pandangan **Penyesuaian**.</span><span class="sxs-lookup"><span data-stu-id="e7074-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]