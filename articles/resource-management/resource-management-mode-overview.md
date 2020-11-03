---
title: Gambaran keseluruhan mod pengurusan sumber
description: Topik ini menyediakan maklumat tentang kefungsian pengurusan Sumber dalam Operasi Projek Dynamics 365.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081116"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="ad3b0-103">Gambaran keseluruhan mod pengurusan sumber</span><span class="sxs-lookup"><span data-stu-id="ad3b0-103">Resource management modes overview</span></span>

<span data-ttu-id="ad3b0-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="ad3b0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="ad3b0-105">Operasi Projek Dynamics 365 menyokong dua mod dalam pesanan untuk anda melaksanakan aliran penempahan keseluruhan.</span><span class="sxs-lookup"><span data-stu-id="ad3b0-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="ad3b0-106">Mod pengurusan ditakrifkan sebagai parameter projek dan boleh diubah suai jika perniagaan anda perlu berubah.</span><span class="sxs-lookup"><span data-stu-id="ad3b0-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="ad3b0-107">Mod tengah</span><span class="sxs-lookup"><span data-stu-id="ad3b0-107">Central mode</span></span>
<span data-ttu-id="ad3b0-108">Untuk organisasi yang memusatkan peruntukan bagi sumber untuk projek, mod Pusat menyediakan cara untuk memastikan Pengurus Projek boleh mentakrifkan keperluan sumber pada peringkat projek.</span><span class="sxs-lookup"><span data-stu-id="ad3b0-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="ad3b0-109">Pemenuhan keperluan sumber ditugaskan kepada Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="ad3b0-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="ad3b0-110">Pengurus Projek boleh menerima atau menolak sumber yang dicadangkan oleh Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="ad3b0-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Mod Tengah](./media/resource-management-central.png)

<span data-ttu-id="ad3b0-112">Untuk menguruskan sumber dengan Mod Tengah, lihat:</span><span class="sxs-lookup"><span data-stu-id="ad3b0-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="ad3b0-113">Tugaskan sumber boleh ditempah generik kepada tugas dan jana keperluan sumber</span><span class="sxs-lookup"><span data-stu-id="ad3b0-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="ad3b0-114">Tempah sumber dinamakan daripada keperluan sumber</span><span class="sxs-lookup"><span data-stu-id="ad3b0-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="ad3b0-115">Serahkan permintaan sumber</span><span class="sxs-lookup"><span data-stu-id="ad3b0-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="ad3b0-116">Penuhi permintaan sumber</span><span class="sxs-lookup"><span data-stu-id="ad3b0-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="ad3b0-117">Menerima atau menolak sumber projek yang dicadangkan daripada permintaan sumber</span><span class="sxs-lookup"><span data-stu-id="ad3b0-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="ad3b0-118">Mod hibrid</span><span class="sxs-lookup"><span data-stu-id="ad3b0-118">Hybrid mode</span></span>
<span data-ttu-id="ad3b0-119">Untuk organisasi yang memerlukan fleksibiliti dalam peruntukan sumber, mod hibrid membolehkan kedua-dua Pengurus Projek dan Resource Manager keupayaan untuk menempah sumber.</span><span class="sxs-lookup"><span data-stu-id="ad3b0-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Mod Hibrid](./media/resource-management-hybrid.png)

<span data-ttu-id="ad3b0-121">Selain daripada proses mod Pusat yang disokong, lihat topik berikut untuk menguruskan semua aliran penempahan lain yang disokong dalam mod Hibrid:</span><span class="sxs-lookup"><span data-stu-id="ad3b0-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="ad3b0-122">Tempah sumber secara langsung kepada projek:</span><span class="sxs-lookup"><span data-stu-id="ad3b0-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="ad3b0-123">Tempah sumber boleh ditempah dinamakan untuk pasukan projek dan menugaskan tugasan</span><span class="sxs-lookup"><span data-stu-id="ad3b0-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="ad3b0-124">Tempah sumber daripada keperluan sumber:</span><span class="sxs-lookup"><span data-stu-id="ad3b0-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="ad3b0-125">Tugaskan sumber boleh ditempah generik kepada tugas dan jana keperluan sumber</span><span class="sxs-lookup"><span data-stu-id="ad3b0-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="ad3b0-126">Tempah sumber dinamakan daripada keperluan sumber</span><span class="sxs-lookup"><span data-stu-id="ad3b0-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
