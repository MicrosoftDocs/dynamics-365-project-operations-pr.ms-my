---
title: Semak sumber yang dicadangkan
description: Topik ini memberikan maklumat tentang cara untuk mencadang sumber projek.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 987ea08c77c1824182856c0d52ee0cd15e7029b9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000762"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="c7567-103">Semak sumber yang dicadangkan</span><span class="sxs-lookup"><span data-stu-id="c7567-103">Review proposed resources</span></span>

<span data-ttu-id="c7567-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="c7567-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c7567-105">Pengurus sumber boleh mencadangkan sumber kepada pengurus projek menggunakan permintaan sumber.</span><span class="sxs-lookup"><span data-stu-id="c7567-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="c7567-106">Daripada grid permintaan atau permintaan itu sendiri, pilih **Cari sumber.**</span><span class="sxs-lookup"><span data-stu-id="c7567-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="c7567-107">Pada halaman **Pembantu Jadual** , pilih sumber dan kemudian, dalam anak tetingkap **Cipta Tempahan Sumber** dalam medan status **Status Tempahan**, pilih **Tempah.**</span><span class="sxs-lookup"><span data-stu-id="c7567-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="c7567-108">Kemas kini status berikut berlaku:</span><span class="sxs-lookup"><span data-stu-id="c7567-108">The following status updates occur:</span></span>

- <span data-ttu-id="c7567-109">Pada halaman **Pembantu Jadual**, penunjuk status dikemas kini untuk menunjukkan bahawa penempahan dicadangkan, tidak ditempah cetak.</span><span class="sxs-lookup"><span data-stu-id="c7567-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="c7567-110">Pada permintaan sumber, status ditukar kepada **Keperluan Semakan Semula.**</span><span class="sxs-lookup"><span data-stu-id="c7567-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="c7567-111">Pada tab **Pasukan** projek, permintaan ahli pasukan generik **Status Permintaan** ditukar kepada **Keperluan Semakan Semula.**</span><span class="sxs-lookup"><span data-stu-id="c7567-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="c7567-112">Pengurus projek boleh sama ada menerima atau menolak cadangan itu.</span><span class="sxs-lookup"><span data-stu-id="c7567-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="c7567-113">Apabila pengurus sumber memproses permintaan sumber, mereka boleh menggunakan sebarang pendekatan berikut:</span><span class="sxs-lookup"><span data-stu-id="c7567-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="c7567-114">Mencadangkan berbilang sumber untuk memenuhi permintaan jika tiada sumber tunggal tersedia untuk memenuhi jam yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="c7567-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="c7567-115">Waktu yang dicadangkan kemudian berpecah antara sumber yang boleh memenuhi jam yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="c7567-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="c7567-116">Dalam senario ini, jam tidak boleh bertindan.</span><span class="sxs-lookup"><span data-stu-id="c7567-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="c7567-117">Mencadangkan lebih sedikit sumber daripada keperluan.</span><span class="sxs-lookup"><span data-stu-id="c7567-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="c7567-118">Dalam senario ini, kapasiti sumber yang dicadangkan adalah kurang daripada jam yang diperlukan yang ditentukan oleh peminta.</span><span class="sxs-lookup"><span data-stu-id="c7567-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="c7567-119">Oleh itu, apabila peminta menerima sumber yang dicadangkan, keperluan sumber yang tidak dipatuhi dicipta untuk menawan permintaan yang berbaki.</span><span class="sxs-lookup"><span data-stu-id="c7567-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="c7567-120">Tempah berbilang sumber untuk memenuhi permintaan jika tiada sumber tunggal tersedia untuk menyelesaikan kerja.</span><span class="sxs-lookup"><span data-stu-id="c7567-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="c7567-121">Menempah lebih sedikit sumber daripada keperluan.</span><span class="sxs-lookup"><span data-stu-id="c7567-121">Book fewer resources than are required.</span></span> <span data-ttu-id="c7567-122">Dalam senario ini, masa yang ditempah adalah lebih sedikit daripada jam yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="c7567-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="c7567-123">Sistem ini memberi panduan kepada anda untuk mencadangkan sumber dan bukannya penempahan, supaya peminta boleh mengesahkan dan menjejaki permintaan yang berbaki.</span><span class="sxs-lookup"><span data-stu-id="c7567-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="c7567-124">Ketersediaan sumber</span><span class="sxs-lookup"><span data-stu-id="c7567-124">Resource availability</span></span>

<span data-ttu-id="c7567-125">Adalah penting bahawa pengurus sumber boleh melihat ketersediaan sumber dan kemas kini tempahan.</span><span class="sxs-lookup"><span data-stu-id="c7567-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="c7567-126">Dalam sesetengah kes, tidak ada permintaan formal (permintaan sumber), tetapi pengurus sumber mesti bertindak balas kepada permintaan yang tidak dirancang yang datang melalui saluran seperti e-mel, panggilan telefon atau mesej segera.</span><span class="sxs-lookup"><span data-stu-id="c7567-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="c7567-127">Pengurus sumber menggunakan Papan Jadual untuk mengemas kini sumber dan penempahan.</span><span class="sxs-lookup"><span data-stu-id="c7567-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="c7567-128">Waktu kerja sumber digunakan sebagai asas untuk mengira ketersediaan sumber.</span><span class="sxs-lookup"><span data-stu-id="c7567-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="c7567-129">Tempahan sumber mengambil kapasiti sumber.</span><span class="sxs-lookup"><span data-stu-id="c7567-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="c7567-130">Papan Jadual menggunakan warna dan pembayangan untuk menunjukkan penempahan, ketersediaan dan pilihan berlebihan dan juga status tempahan.</span><span class="sxs-lookup"><span data-stu-id="c7567-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="c7567-131">Tetapan dalam tetapan Papan Jadual membolehkan anda menunjukkan petunjuk.</span><span class="sxs-lookup"><span data-stu-id="c7567-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="c7567-132">Jika anak panah tunjuk sebelah kanan muncul di sebelah sumber boleh ditempah individu pada Papan Jadual, sumber itu dapat dikembangkan untuk menunjukkan butiran kerja yang digunakan oleh sumber tersebut.</span><span class="sxs-lookup"><span data-stu-id="c7567-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="c7567-133">Kerana Dynamics 365 Project Operations menggunakan enjin Universal Resource Scheduling, jika anda juga telah Dynamics 365 Field Service dipasang, anda boleh melihat butiran daripada penempahan sumber untuk projek, pesanan kerja dan sebarang entiti lain yang anda telah melanjutkan penjadualan.</span><span class="sxs-lookup"><span data-stu-id="c7567-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="c7567-134">Untuk melihat lebih banyak butiran mengenai sumber individu, klik kanan padanya untuk membuka kad sumber.</span><span class="sxs-lookup"><span data-stu-id="c7567-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]