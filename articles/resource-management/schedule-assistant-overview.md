---
title: Gambaran keseluruhan pembantu jadual
description: Topik ini memberikan maklumat mengenai kerja dengan Pembantu jadual untuk menempah sumber.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081084"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="0b03d-103">Gambaran keseluruhan pembantu jadual</span><span class="sxs-lookup"><span data-stu-id="0b03d-103">Schedule assistant overview</span></span>

<span data-ttu-id="0b03d-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="0b03d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0b03d-105">Pembantu jadual digunakan untuk menempah sumber berdasarkan keperluan yang ditakrifkan oleh Pengurus projek.</span><span class="sxs-lookup"><span data-stu-id="0b03d-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="0b03d-106">Pembantu jadual bergantung pada parameter yang disediakan dalam keperluan sumber untuk mencari sumber.</span><span class="sxs-lookup"><span data-stu-id="0b03d-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="0b03d-107">Pembantu jadual mengesyorkan sumber yang sepadan dengan keperluan yang berkaitan, seperti masa windows atau kemahiran yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="0b03d-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="0b03d-108">Selepas sumber yang sesuai dikenal pasti, Sumber atau Pengurus projek boleh menempah sumber untuk kerja.</span><span class="sxs-lookup"><span data-stu-id="0b03d-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0b03d-109">Prasyarat</span><span class="sxs-lookup"><span data-stu-id="0b03d-109">Prerequisites</span></span>

<span data-ttu-id="0b03d-110">Pembantu jadual merupakan sebahagian daripada penyelesaian Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="0b03d-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="0b03d-111">Penyelesaian ini disertakan dan dipasang dengan Dynamics 365 Project Operations, Dynamics 365 Field Service, dan Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="0b03d-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="0b03d-112">Keperluan sepadan dan sumber</span><span class="sxs-lookup"><span data-stu-id="0b03d-112">Matching requirements and resources</span></span>

<span data-ttu-id="0b03d-113">Keperluan sumber yang dijana adalah berdasarkan butiran seperti:</span><span class="sxs-lookup"><span data-stu-id="0b03d-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="0b03d-114">Ciri</span><span class="sxs-lookup"><span data-stu-id="0b03d-114">Characteristics</span></span>
-   <span data-ttu-id="0b03d-115">Peranan</span><span class="sxs-lookup"><span data-stu-id="0b03d-115">Roles</span></span>
-   <span data-ttu-id="0b03d-116">Unit perniagaan</span><span class="sxs-lookup"><span data-stu-id="0b03d-116">Business units</span></span>
-   <span data-ttu-id="0b03d-117">Keutamaan sumber</span><span class="sxs-lookup"><span data-stu-id="0b03d-117">Resource preferences</span></span>
-   <span data-ttu-id="0b03d-118">Usaha kontur</span><span class="sxs-lookup"><span data-stu-id="0b03d-118">Effort contours</span></span>
-   <span data-ttu-id="0b03d-119">Zon masa</span><span class="sxs-lookup"><span data-stu-id="0b03d-119">Time zone</span></span>

<span data-ttu-id="0b03d-120">Pembantu jadual menggunakan butiran ini untuk menapis sumber.</span><span class="sxs-lookup"><span data-stu-id="0b03d-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="0b03d-121">Lancarkan Pembantu jadual</span><span class="sxs-lookup"><span data-stu-id="0b03d-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="0b03d-122">Terdapat dua cara di mana pembantu jadual dilancarkan.</span><span class="sxs-lookup"><span data-stu-id="0b03d-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="0b03d-123">Jika anda menggunakan mod hibrid, dalam grid ahli pasukan anda boleh memilih sebarang ahli pasukan dengan keperluan sumber yang tidak dipatuhi, dan kemudian pilih **Tempah**.</span><span class="sxs-lookup"><span data-stu-id="0b03d-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="0b03d-124">Jika anda menggunakan mod pusat, Resource manager mencari dan memilih sumber.</span><span class="sxs-lookup"><span data-stu-id="0b03d-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="0b03d-125">Penapis pembantu jadual</span><span class="sxs-lookup"><span data-stu-id="0b03d-125">Schedule assistant filters</span></span>

<span data-ttu-id="0b03d-126">Selepas Pembantu jadual berjalan, butiran daripada keperluan sumber dipaparkan sebagai nilai yang ditapis dalam anak tetingkap kiri.</span><span class="sxs-lookup"><span data-stu-id="0b03d-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="0b03d-127">Resource manager atau Pengurus projek boleh memperhalusi hasil dengan melaraskan penapis untuk memenuhi keperluan penjadualan.</span><span class="sxs-lookup"><span data-stu-id="0b03d-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="0b03d-128">Anak tetingkap penapis menunjukkan pilihan berkaitan kerja, termasuk:</span><span class="sxs-lookup"><span data-stu-id="0b03d-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="0b03d-129">Mula dan tamat bekerja</span><span class="sxs-lookup"><span data-stu-id="0b03d-129">Work start and end</span></span>
-   <span data-ttu-id="0b03d-130">Ciri</span><span class="sxs-lookup"><span data-stu-id="0b03d-130">Characteristics</span></span>
-   <span data-ttu-id="0b03d-131">Peranan</span><span class="sxs-lookup"><span data-stu-id="0b03d-131">Roles</span></span>
-   <span data-ttu-id="0b03d-132">Unit organisasi</span><span class="sxs-lookup"><span data-stu-id="0b03d-132">Organizational units</span></span>
-   <span data-ttu-id="0b03d-133">Syarikat persumberan</span><span class="sxs-lookup"><span data-stu-id="0b03d-133">Resourcing company</span></span>
-   <span data-ttu-id="0b03d-134">Jenis sumber</span><span class="sxs-lookup"><span data-stu-id="0b03d-134">Resource types</span></span>
-   <span data-ttu-id="0b03d-135">Sumber diutamakan</span><span class="sxs-lookup"><span data-stu-id="0b03d-135">Preferred resources</span></span>
