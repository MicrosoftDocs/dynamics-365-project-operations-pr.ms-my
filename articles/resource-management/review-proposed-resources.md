---
title: Semak sumber yang dicadangkan
description: Topik ini memberikan maklumat tentang cara untuk mencadang sumber projek.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 212b80a7fde8368eedd7572dd5f9278cc53fae98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897372"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="91eff-103">Semak sumber yang dicadangkan</span><span class="sxs-lookup"><span data-stu-id="91eff-103">Review proposed resources</span></span>

<span data-ttu-id="91eff-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="91eff-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="91eff-105">Pengurus sumber boleh mencadangkan sumber kepada pengurus projek menggunakan permintaan sumber.</span><span class="sxs-lookup"><span data-stu-id="91eff-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="91eff-106">Daripada grid permintaan atau permintaan itu sendiri, pilih **Cari sumber.**</span><span class="sxs-lookup"><span data-stu-id="91eff-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="91eff-107">Pada halaman **Pembantu Jadual** , pilih sumber dan kemudian, dalam anak tetingkap **Cipta Tempahan Sumber** dalam medan status **Status Tempahan**, pilih **Tempah.**</span><span class="sxs-lookup"><span data-stu-id="91eff-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="91eff-108">Kemas kini status berikut berlaku:</span><span class="sxs-lookup"><span data-stu-id="91eff-108">The following status updates occur:</span></span>

- <span data-ttu-id="91eff-109">Pada halaman **Pembantu Jadual**, penunjuk status dikemas kini untuk menunjukkan bahawa penempahan dicadangkan, tidak ditempah cetak.</span><span class="sxs-lookup"><span data-stu-id="91eff-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="91eff-110">Pada permintaan sumber, status ditukar kepada **Keperluan Semakan Semula.**</span><span class="sxs-lookup"><span data-stu-id="91eff-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="91eff-111">Pada tab **Pasukan** projek, permintaan ahli pasukan generik **Status Permintaan** ditukar kepada **Keperluan Semakan Semula.**</span><span class="sxs-lookup"><span data-stu-id="91eff-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="91eff-112">Pengurus projek boleh sama ada menerima atau menolak cadangan itu.</span><span class="sxs-lookup"><span data-stu-id="91eff-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="91eff-113">Apabila pengurus sumber memproses permintaan sumber, mereka boleh menggunakan sebarang pendekatan berikut:</span><span class="sxs-lookup"><span data-stu-id="91eff-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="91eff-114">Mencadangkan berbilang sumber untuk memenuhi permintaan jika tiada sumber tunggal tersedia untuk memenuhi jam yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="91eff-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="91eff-115">Waktu yang dicadangkan kemudian berpecah antara sumber yang boleh memenuhi jam yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="91eff-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="91eff-116">Dalam senario ini, jam tidak boleh bertindan.</span><span class="sxs-lookup"><span data-stu-id="91eff-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="91eff-117">Mencadangkan lebih sedikit sumber daripada keperluan.</span><span class="sxs-lookup"><span data-stu-id="91eff-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="91eff-118">Dalam senario ini, kapasiti sumber yang dicadangkan adalah kurang daripada jam yang diperlukan yang ditentukan oleh peminta.</span><span class="sxs-lookup"><span data-stu-id="91eff-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="91eff-119">Oleh itu, apabila peminta menerima sumber yang dicadangkan, keperluan sumber yang tidak dipatuhi dicipta untuk menawan permintaan yang berbaki.</span><span class="sxs-lookup"><span data-stu-id="91eff-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="91eff-120">Tempah berbilang sumber untuk memenuhi permintaan jika tiada sumber tunggal tersedia untuk menyelesaikan kerja.</span><span class="sxs-lookup"><span data-stu-id="91eff-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="91eff-121">Menempah lebih sedikit sumber daripada keperluan.</span><span class="sxs-lookup"><span data-stu-id="91eff-121">Book fewer resources than are required.</span></span> <span data-ttu-id="91eff-122">Dalam senario ini, masa yang ditempah adalah lebih sedikit daripada jam yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="91eff-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="91eff-123">Sistem ini memberi panduan kepada anda untuk mencadangkan sumber dan bukannya penempahan, supaya peminta boleh mengesahkan dan menjejaki permintaan yang berbaki.</span><span class="sxs-lookup"><span data-stu-id="91eff-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="91eff-124">Penggunaan boleh dibilkan</span><span class="sxs-lookup"><span data-stu-id="91eff-124">Billable utilization</span></span>

<span data-ttu-id="91eff-125">Sumber boleh mempunyai sasaran penggunaan boleh dibilkan.</span><span class="sxs-lookup"><span data-stu-id="91eff-125">Resources can have a target billable utilization.</span></span> <span data-ttu-id="91eff-126">Penggunaan sasaran ini sama ada ditakrifkan sebagai atribut pada peranan lalai sumber atau ditetapkan pada rekod sumber boleh ditempah individu.</span><span class="sxs-lookup"><span data-stu-id="91eff-126">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="91eff-127">Pengiraan penggunaan adalah berdasarkan masa sebenar bahawa sumber telah dilaporkan dengan menggunakan kemasukan penyertaan yang diluluskan.</span><span class="sxs-lookup"><span data-stu-id="91eff-127">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="91eff-128">Formula berikut digunakan untuk mengira penggunaan:</span><span class="sxs-lookup"><span data-stu-id="91eff-128">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="91eff-129">Penggunaan boleh dibilkan = Jam sebenar ÷ Kapasiti sumber boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="91eff-129">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="91eff-130">Penggunaan tidak boleh dibilkan = Masa sebenar dengan ID jenis bil = Tidak dikenakan caj, Pelengkap atau Tidak tersedia yang boleh ÷ Kapasiti sumber</span><span class="sxs-lookup"><span data-stu-id="91eff-130">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="91eff-131">Dalaman = Masa sebenar dengan tiada kontrak jualan ÷ Kapasiti sumber</span><span class="sxs-lookup"><span data-stu-id="91eff-131">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="91eff-132">Kapasiti sumber = Waktu kerja sumber – Keluar dari pejabat – Hari tidak bekerja</span><span class="sxs-lookup"><span data-stu-id="91eff-132">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="91eff-133">Anda boleh mencari pandangan **Penggunaan Sumber** dalam anak tetingkap **Sumber**.</span><span class="sxs-lookup"><span data-stu-id="91eff-133">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="91eff-134">Setiap sel dalam grid mewakili peratusan penggunaan boleh dibilkan bagi sumber dalam tempoh, seperti hari, minggu atau bulan.</span><span class="sxs-lookup"><span data-stu-id="91eff-134">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="91eff-135">Formula berikut digunakan untuk mewarnakan sel:</span><span class="sxs-lookup"><span data-stu-id="91eff-135">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="91eff-136">**Hijau:** Penggunaan boleh dibilkan \>= Penggunaan sasaran sumber</span><span class="sxs-lookup"><span data-stu-id="91eff-136">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="91eff-137">**Kuning:** Penggunaan sasaran – 20 \<= Penggunaan boleh dibilkan \< Penggunaan sasaran</span><span class="sxs-lookup"><span data-stu-id="91eff-137">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="91eff-138">**Merah:** Penggunaan boleh dibilkan \< Penggunaan sasaran – 20</span><span class="sxs-lookup"><span data-stu-id="91eff-138">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="91eff-139">Oleh kerana pandangan **Penggunaan Sumber** adalah berdasarkan Papan Jadual, anda boleh menggunakan keupayaan penapisan Papan Jadual untuk menapis hasil anda.</span><span class="sxs-lookup"><span data-stu-id="91eff-139">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="91eff-140">Grid memerlukan anda menetapkan penggunaan sasaran pada sama ada peranan atau sumber individu.</span><span class="sxs-lookup"><span data-stu-id="91eff-140">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="91eff-141">Untuk melakukan persediaan ini, pergi ke **Peranan** \> **Peranan sumber**.</span><span class="sxs-lookup"><span data-stu-id="91eff-141">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="91eff-142">Selain itu, peranan lalai mesti ditugaskan kepada setiap sumber boleh ditempah.</span><span class="sxs-lookup"><span data-stu-id="91eff-142">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="91eff-143">Pergi ke **Sumber** \> **Sumber**.</span><span class="sxs-lookup"><span data-stu-id="91eff-143">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="91eff-144">Pada tab **Project Service** sahkan peranan sumber ditakrifkan dan medan **Adalah Lalai** untuk ia disetkan kepada **Ya.**</span><span class="sxs-lookup"><span data-stu-id="91eff-144">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="91eff-145">Anda boleh menambah peranan tambahan di mana **Adalah Lalai = No**.</span><span class="sxs-lookup"><span data-stu-id="91eff-145">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="91eff-146">Peranan di mana **Adalah Lalai = Ya** digunakan untuk menilai penggunaan sumber terhadap sasaran untuk peranan tersebut.</span><span class="sxs-lookup"><span data-stu-id="91eff-146">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="91eff-147">Pada tab **Project Service**, anda juga boleh menetapkan penggunaan sasaran individu untuk sumber.</span><span class="sxs-lookup"><span data-stu-id="91eff-147">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="91eff-148">Pengiraan penggunaan ini kemudian menggunakan penggunaan sasaran yang akan menilai sasaran sumber bukan sasaran peranan lalai sumber.</span><span class="sxs-lookup"><span data-stu-id="91eff-148">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="91eff-149">Penggunaan ditunjukkan untuk sumber hanya jika sumber tersebut telah diluluskan dan masa boleh dikenakan dalam tempoh yang ditunjukkan dalam grid.</span><span class="sxs-lookup"><span data-stu-id="91eff-149">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="91eff-150">Ketersediaan sumber</span><span class="sxs-lookup"><span data-stu-id="91eff-150">Resource availability</span></span>

<span data-ttu-id="91eff-151">Adalah penting bahawa pengurus sumber boleh melihat ketersediaan sumber dan kemas kini tempahan.</span><span class="sxs-lookup"><span data-stu-id="91eff-151">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="91eff-152">Dalam sesetengah kes, tidak ada permintaan formal (permintaan sumber), tetapi pengurus sumber mesti bertindak balas kepada permintaan yang tidak dirancang yang datang melalui saluran seperti e-mel, panggilan telefon atau mesej segera.</span><span class="sxs-lookup"><span data-stu-id="91eff-152">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="91eff-153">Pengurus sumber menggunakan Papan Jadual untuk mengemas kini sumber dan penempahan.</span><span class="sxs-lookup"><span data-stu-id="91eff-153">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="91eff-154">Waktu kerja sumber digunakan sebagai asas untuk mengira ketersediaan sumber.</span><span class="sxs-lookup"><span data-stu-id="91eff-154">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="91eff-155">Tempahan sumber mengambil kapasiti sumber.</span><span class="sxs-lookup"><span data-stu-id="91eff-155">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="91eff-156">Papan Jadual menggunakan warna dan pembayangan untuk menunjukkan penempahan, ketersediaan dan pilihan berlebihan dan juga status tempahan.</span><span class="sxs-lookup"><span data-stu-id="91eff-156">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="91eff-157">Tetapan dalam tetapan Papan Jadual membolehkan anda menunjukkan petunjuk.</span><span class="sxs-lookup"><span data-stu-id="91eff-157">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="91eff-158">Jika anak panah tunjuk sebelah kanan muncul di sebelah sumber boleh ditempah individu pada Papan Jadual, sumber itu dapat dikembangkan untuk menunjukkan butiran kerja yang digunakan oleh sumber tersebut.</span><span class="sxs-lookup"><span data-stu-id="91eff-158">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="91eff-159">Oleh kerana Dynamics 365 Project Operations menggunakan enjin Universal Resource Scheduling, jika anda juga dipasang dengan Dynamics 365 Field Service, anda boleh melihat butiran tempahan sumber untuk projek, pesanan kerja dan sebarang entiti lain yang anda telah lanjutkan penjadualannya.</span><span class="sxs-lookup"><span data-stu-id="91eff-159">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="91eff-160">Untuk melihat lebih banyak butiran mengenai sumber individu, klik kanan padanya untuk membuka kad sumber.</span><span class="sxs-lookup"><span data-stu-id="91eff-160">To view more details about an individual resource, right-click it to open the resource card.</span></span>

