---
title: Gambaran keseluruhan pembantu jadual
description: Topik ini memberikan maklumat mengenai kerja dengan Pembantu jadual untuk menempah sumber.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d58f5f45ca54691b6e736dee5aab7b273a8e042
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014127"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="0185e-103">Gambaran keseluruhan pembantu jadual</span><span class="sxs-lookup"><span data-stu-id="0185e-103">Schedule assistant overview</span></span>

<span data-ttu-id="0185e-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="0185e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0185e-105">Pembantu jadual digunakan untuk menempah sumber berdasarkan keperluan yang ditakrifkan oleh Pengurus projek.</span><span class="sxs-lookup"><span data-stu-id="0185e-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="0185e-106">Pembantu jadual bergantung pada parameter yang disediakan dalam keperluan sumber untuk mencari sumber.</span><span class="sxs-lookup"><span data-stu-id="0185e-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="0185e-107">Pembantu jadual mengesyorkan sumber yang sepadan dengan keperluan yang berkaitan, seperti masa windows atau kemahiran yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="0185e-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="0185e-108">Selepas sumber yang sesuai dikenal pasti, Sumber atau Pengurus projek boleh menempah sumber untuk kerja.</span><span class="sxs-lookup"><span data-stu-id="0185e-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0185e-109">Prasyarat</span><span class="sxs-lookup"><span data-stu-id="0185e-109">Prerequisites</span></span>

<span data-ttu-id="0185e-110">Pembantu jadual merupakan sebahagian daripada penyelesaian Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="0185e-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="0185e-111">Penyelesaian ini disertakan dan dipasang dengan Dynamics 365 Project Operations, Dynamics 365 Field Service dan Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="0185e-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="0185e-112">Keperluan sepadan dan sumber</span><span class="sxs-lookup"><span data-stu-id="0185e-112">Matching requirements and resources</span></span>

<span data-ttu-id="0185e-113">Keperluan sumber yang dijana adalah berdasarkan butiran seperti:</span><span class="sxs-lookup"><span data-stu-id="0185e-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="0185e-114">Ciri</span><span class="sxs-lookup"><span data-stu-id="0185e-114">Characteristics</span></span>
-   <span data-ttu-id="0185e-115">Peranan</span><span class="sxs-lookup"><span data-stu-id="0185e-115">Roles</span></span>
-   <span data-ttu-id="0185e-116">Unit perniagaan</span><span class="sxs-lookup"><span data-stu-id="0185e-116">Business units</span></span>
-   <span data-ttu-id="0185e-117">Keutamaan sumber</span><span class="sxs-lookup"><span data-stu-id="0185e-117">Resource preferences</span></span>
-   <span data-ttu-id="0185e-118">Usaha kontur</span><span class="sxs-lookup"><span data-stu-id="0185e-118">Effort contours</span></span>
-   <span data-ttu-id="0185e-119">Zon masa</span><span class="sxs-lookup"><span data-stu-id="0185e-119">Time zone</span></span>

<span data-ttu-id="0185e-120">Pembantu jadual menggunakan butiran ini untuk menapis sumber.</span><span class="sxs-lookup"><span data-stu-id="0185e-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="0185e-121">Lancarkan Pembantu jadual</span><span class="sxs-lookup"><span data-stu-id="0185e-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="0185e-122">Terdapat dua cara di mana pembantu jadual dilancarkan.</span><span class="sxs-lookup"><span data-stu-id="0185e-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="0185e-123">Jika anda menggunakan mod hibrid, dalam grid ahli pasukan anda boleh memilih sebarang ahli pasukan dengan keperluan sumber yang tidak dipatuhi, dan kemudian pilih **Tempah**.</span><span class="sxs-lookup"><span data-stu-id="0185e-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="0185e-124">Jika anda menggunakan mod pusat, Resource manager mencari dan memilih sumber.</span><span class="sxs-lookup"><span data-stu-id="0185e-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="0185e-125">Penapis pembantu jadual</span><span class="sxs-lookup"><span data-stu-id="0185e-125">Schedule assistant filters</span></span>

<span data-ttu-id="0185e-126">Selepas Pembantu jadual berjalan, butiran daripada keperluan sumber dipaparkan sebagai nilai yang ditapis dalam anak tetingkap kiri.</span><span class="sxs-lookup"><span data-stu-id="0185e-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="0185e-127">Resource manager atau Pengurus projek boleh memperhalusi hasil dengan melaraskan penapis untuk memenuhi keperluan penjadualan.</span><span class="sxs-lookup"><span data-stu-id="0185e-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="0185e-128">Anak tetingkap penapis menunjukkan pilihan berkaitan kerja, termasuk:</span><span class="sxs-lookup"><span data-stu-id="0185e-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="0185e-129">Mula dan tamat bekerja</span><span class="sxs-lookup"><span data-stu-id="0185e-129">Work start and end</span></span>
-   <span data-ttu-id="0185e-130">Ciri</span><span class="sxs-lookup"><span data-stu-id="0185e-130">Characteristics</span></span>
-   <span data-ttu-id="0185e-131">Peranan</span><span class="sxs-lookup"><span data-stu-id="0185e-131">Roles</span></span>
-   <span data-ttu-id="0185e-132">Unit organisasi</span><span class="sxs-lookup"><span data-stu-id="0185e-132">Organizational units</span></span>
-   <span data-ttu-id="0185e-133">Syarikat persumberan</span><span class="sxs-lookup"><span data-stu-id="0185e-133">Resourcing company</span></span>
-   <span data-ttu-id="0185e-134">Jenis sumber</span><span class="sxs-lookup"><span data-stu-id="0185e-134">Resource types</span></span>
-   <span data-ttu-id="0185e-135">Sumber diutamakan</span><span class="sxs-lookup"><span data-stu-id="0185e-135">Preferred resources</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]