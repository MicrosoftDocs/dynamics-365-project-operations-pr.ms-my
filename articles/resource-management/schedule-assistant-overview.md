---
title: Gambaran keseluruhan pembantu jadual
description: Topik ini memberikan maklumat mengenai kerja dengan Pembantu jadual untuk menempah sumber.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e14dbe5abb69a547e2d09ef9e6bcba48e1f89455
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279239"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="5b0f9-103">Gambaran keseluruhan pembantu jadual</span><span class="sxs-lookup"><span data-stu-id="5b0f9-103">Schedule assistant overview</span></span>

<span data-ttu-id="5b0f9-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="5b0f9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5b0f9-105">Pembantu jadual digunakan untuk menempah sumber berdasarkan keperluan yang ditakrifkan oleh Pengurus projek.</span><span class="sxs-lookup"><span data-stu-id="5b0f9-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="5b0f9-106">Pembantu jadual bergantung pada parameter yang disediakan dalam keperluan sumber untuk mencari sumber.</span><span class="sxs-lookup"><span data-stu-id="5b0f9-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="5b0f9-107">Pembantu jadual mengesyorkan sumber yang sepadan dengan keperluan yang berkaitan, seperti masa windows atau kemahiran yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="5b0f9-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="5b0f9-108">Selepas sumber yang sesuai dikenal pasti, Sumber atau Pengurus projek boleh menempah sumber untuk kerja.</span><span class="sxs-lookup"><span data-stu-id="5b0f9-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5b0f9-109">Prasyarat</span><span class="sxs-lookup"><span data-stu-id="5b0f9-109">Prerequisites</span></span>

<span data-ttu-id="5b0f9-110">Pembantu jadual merupakan sebahagian daripada penyelesaian Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="5b0f9-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="5b0f9-111">Penyelesaian ini disertakan dan dipasang dengan Dynamics 365 Project Operations, Dynamics 365 Field Service dan Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="5b0f9-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="5b0f9-112">Keperluan sepadan dan sumber</span><span class="sxs-lookup"><span data-stu-id="5b0f9-112">Matching requirements and resources</span></span>

<span data-ttu-id="5b0f9-113">Keperluan sumber yang dijana adalah berdasarkan butiran seperti:</span><span class="sxs-lookup"><span data-stu-id="5b0f9-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="5b0f9-114">Ciri</span><span class="sxs-lookup"><span data-stu-id="5b0f9-114">Characteristics</span></span>
-   <span data-ttu-id="5b0f9-115">Peranan</span><span class="sxs-lookup"><span data-stu-id="5b0f9-115">Roles</span></span>
-   <span data-ttu-id="5b0f9-116">Unit perniagaan</span><span class="sxs-lookup"><span data-stu-id="5b0f9-116">Business units</span></span>
-   <span data-ttu-id="5b0f9-117">Keutamaan sumber</span><span class="sxs-lookup"><span data-stu-id="5b0f9-117">Resource preferences</span></span>
-   <span data-ttu-id="5b0f9-118">Usaha kontur</span><span class="sxs-lookup"><span data-stu-id="5b0f9-118">Effort contours</span></span>
-   <span data-ttu-id="5b0f9-119">Zon masa</span><span class="sxs-lookup"><span data-stu-id="5b0f9-119">Time zone</span></span>

<span data-ttu-id="5b0f9-120">Pembantu jadual menggunakan butiran ini untuk menapis sumber.</span><span class="sxs-lookup"><span data-stu-id="5b0f9-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="5b0f9-121">Lancarkan Pembantu jadual</span><span class="sxs-lookup"><span data-stu-id="5b0f9-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="5b0f9-122">Terdapat dua cara di mana pembantu jadual dilancarkan.</span><span class="sxs-lookup"><span data-stu-id="5b0f9-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="5b0f9-123">Jika anda menggunakan mod hibrid, dalam grid ahli pasukan anda boleh memilih sebarang ahli pasukan dengan keperluan sumber yang tidak dipatuhi, dan kemudian pilih **Tempah**.</span><span class="sxs-lookup"><span data-stu-id="5b0f9-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="5b0f9-124">Jika anda menggunakan mod pusat, Resource manager mencari dan memilih sumber.</span><span class="sxs-lookup"><span data-stu-id="5b0f9-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="5b0f9-125">Penapis pembantu jadual</span><span class="sxs-lookup"><span data-stu-id="5b0f9-125">Schedule assistant filters</span></span>

<span data-ttu-id="5b0f9-126">Selepas Pembantu jadual berjalan, butiran daripada keperluan sumber dipaparkan sebagai nilai yang ditapis dalam anak tetingkap kiri.</span><span class="sxs-lookup"><span data-stu-id="5b0f9-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="5b0f9-127">Resource manager atau Pengurus projek boleh memperhalusi hasil dengan melaraskan penapis untuk memenuhi keperluan penjadualan.</span><span class="sxs-lookup"><span data-stu-id="5b0f9-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="5b0f9-128">Anak tetingkap penapis menunjukkan pilihan berkaitan kerja, termasuk:</span><span class="sxs-lookup"><span data-stu-id="5b0f9-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="5b0f9-129">Mula dan tamat bekerja</span><span class="sxs-lookup"><span data-stu-id="5b0f9-129">Work start and end</span></span>
-   <span data-ttu-id="5b0f9-130">Ciri</span><span class="sxs-lookup"><span data-stu-id="5b0f9-130">Characteristics</span></span>
-   <span data-ttu-id="5b0f9-131">Peranan</span><span class="sxs-lookup"><span data-stu-id="5b0f9-131">Roles</span></span>
-   <span data-ttu-id="5b0f9-132">Unit organisasi</span><span class="sxs-lookup"><span data-stu-id="5b0f9-132">Organizational units</span></span>
-   <span data-ttu-id="5b0f9-133">Syarikat persumberan</span><span class="sxs-lookup"><span data-stu-id="5b0f9-133">Resourcing company</span></span>
-   <span data-ttu-id="5b0f9-134">Jenis sumber</span><span class="sxs-lookup"><span data-stu-id="5b0f9-134">Resource types</span></span>
-   <span data-ttu-id="5b0f9-135">Sumber diutamakan</span><span class="sxs-lookup"><span data-stu-id="5b0f9-135">Preferred resources</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]