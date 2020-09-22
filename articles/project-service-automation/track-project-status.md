---
title: Jejaki status projek
description: Cara untuk menjejaki status projek dalam Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 7610aecb-318c-422b-b626-9106b0736b5f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: e4d53b6235c3b941bce525dca09ee3d647c3d242
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753977"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="8b6cd-103">Jejak status projek (Project Service)</span><span class="sxs-lookup"><span data-stu-id="8b6cd-103">Track a project’s status (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="8b6cd-104">Gunakan [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] untuk menjejaki kemajuan projek klien.</span><span class="sxs-lookup"><span data-stu-id="8b6cd-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="8b6cd-105">Sebagaimana kemajuan penglibatan, peringkat projek dikemas kini untuk menunjukkan peringkat penglibatan:</span><span class="sxs-lookup"><span data-stu-id="8b6cd-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="8b6cd-106">**Baharu**</span><span class="sxs-lookup"><span data-stu-id="8b6cd-106">**New**</span></span>    | <span data-ttu-id="8b6cd-107">Apabila anda mencipta projek, peringkat ditetapkan kepada **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="8b6cd-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="8b6cd-108">Jika anda mencipta projek daripada templat, pada peringkat ini, projek mungkin mempunyai jadual, anggaran dan data pasukan.</span><span class="sxs-lookup"><span data-stu-id="8b6cd-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="8b6cd-109">Sebaliknya, hanya terdapat rangka projek dan anda perlu memasukkan komponen projek yang lain secara manual.</span><span class="sxs-lookup"><span data-stu-id="8b6cd-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="8b6cd-110">**Sebut Harga**</span><span class="sxs-lookup"><span data-stu-id="8b6cd-110">**Quote**</span></span>   |      <span data-ttu-id="8b6cd-111">Apabila anda mengaitkan projek dengan sebut harga atau menciptanya daripada sebut harga, peringkat projek ditetapkan kepada **Sebut Harga** dan anggaran tarikh mula dan tamat juga dikemas kini.</span><span class="sxs-lookup"><span data-stu-id="8b6cd-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="8b6cd-112">Apabila projek berada dalam peringkat sebut harga, butiran sebut harga dipaparkan pada tab **Sales** di halaman **Projek**.</span><span class="sxs-lookup"><span data-stu-id="8b6cd-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="8b6cd-113">**Pelan**</span><span class="sxs-lookup"><span data-stu-id="8b6cd-113">**Plan**</span></span>   |                                     <span data-ttu-id="8b6cd-114">Apabila anda menang sebut harga yang dikaitkan dengan projek dan apabila penglibatan mara ke peringkat kontrak, peringkat projek dikemas kini kepada **Pelan**.</span><span class="sxs-lookup"><span data-stu-id="8b6cd-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="8b6cd-115">Butiran kontrak dipaparkan pada tab **Sales** di halaman **Projek**.</span><span class="sxs-lookup"><span data-stu-id="8b6cd-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="8b6cd-116">**Selesai**</span><span class="sxs-lookup"><span data-stu-id="8b6cd-116">**Complete**</span></span> |                    <span data-ttu-id="8b6cd-117">Apabila kerja projek selesai, anda boleh menukar peringkat kepada **Selesai**.</span><span class="sxs-lookup"><span data-stu-id="8b6cd-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="8b6cd-118">Apabila peringkat projek ditetapkan kepada selesai, difahami bahawa kerja 100% selesai tetapi projek terus dibuka untuk sebarang masa menunggu atau entri perbelanjaan direkodkan.</span><span class="sxs-lookup"><span data-stu-id="8b6cd-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="8b6cd-119">**Tutup**</span><span class="sxs-lookup"><span data-stu-id="8b6cd-119">**Close**</span></span>   |           <span data-ttu-id="8b6cd-120">Apabila semua transaksi telah direkodkan pada projek dan tiada lagi transaksi untuk dilogkan, anda boleh menetapkan peringkat secara manual kepada **Tutup**.</span><span class="sxs-lookup"><span data-stu-id="8b6cd-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="8b6cd-121">Apabila projek ditetapkan kepada **Tutup**, tiada lagi transaksi boleh dilogkan pada projek dan projek akan menjadi baca sahaja.</span><span class="sxs-lookup"><span data-stu-id="8b6cd-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="8b6cd-122">Untuk menjejaki status projek</span><span class="sxs-lookup"><span data-stu-id="8b6cd-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="8b6cd-123">Pergi ke **Project Service > Projek**.</span><span class="sxs-lookup"><span data-stu-id="8b6cd-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="8b6cd-124">Klik program y ang anda mahu kerjakan.</span><span class="sxs-lookup"><span data-stu-id="8b6cd-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="8b6cd-125">Dalam bar yang merentas bahagian atas skrin, pilih anak panah ke bawah di sebelah nama projek dan kemudian klik **Penjejakan Projek**.</span><span class="sxs-lookup"><span data-stu-id="8b6cd-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="8b6cd-126">Pilih **Penjejakan Usaha** atau **Penjejakan Kos** dalam senarai juntai bawah di atas senarai tugas.</span><span class="sxs-lookup"><span data-stu-id="8b6cd-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="8b6cd-127">Dwiklik mana-mana tugas untuk mengeditnya.</span><span class="sxs-lookup"><span data-stu-id="8b6cd-127">Double-click any task to edit it.</span></span> <span data-ttu-id="8b6cd-128">Anda juga boleh mengalihkan atau mengubah saiz bar dalam carta Gantt untuk mengubah masa dan kemajuan untuk tugas.</span><span class="sxs-lookup"><span data-stu-id="8b6cd-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="8b6cd-129">Lihat Juga</span><span class="sxs-lookup"><span data-stu-id="8b6cd-129">See Also</span></span>  
 [<span data-ttu-id="8b6cd-130">Panduan Pengurus Projek</span><span class="sxs-lookup"><span data-stu-id="8b6cd-130">Project Manager Guide</span></span>](../project-service/project-manager-guide.md)
