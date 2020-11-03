---
title: Mencadangkan sumber projek
description: Topik ini memberikan maklumat tentang cadangan sumber projek.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 18d7dcd95806841c952ea621ec65b513ef614958
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081447"
---
# <a name="propose-project-resources"></a><span data-ttu-id="463cb-103">Mencadangkan sumber projek</span><span class="sxs-lookup"><span data-stu-id="463cb-103">Propose project resources</span></span>

<span data-ttu-id="463cb-104">Pengurus sumber boleh mencadangkan sumber kepada pengurus projek menggunakan permintaan sumber.</span><span class="sxs-lookup"><span data-stu-id="463cb-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="463cb-105">Daripada grid permintaan atau permintaan itu sendiri, pilih **Cari sumber.**</span><span class="sxs-lookup"><span data-stu-id="463cb-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="463cb-106">Pada halaman **Pembantu Jadual** , pilih sumber dan kemudian, dalam anak tetingkap **Cipta Tempahan Sumber** dalam medan status **Status Tempahan** , pilih **Tempah.**</span><span class="sxs-lookup"><span data-stu-id="463cb-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![Sumber terpilih yang dicadangkan.](media/Resource-Management-image62.png)

<span data-ttu-id="463cb-108">Kemas kini status berikut berlaku:</span><span class="sxs-lookup"><span data-stu-id="463cb-108">The following status updates occur:</span></span>

- <span data-ttu-id="463cb-109">Pada halaman **Pembantu Jadual** , penunjuk status dikemas kini untuk menunjukkan bahawa penempahan dicadangkan, tidak ditempah cetak.</span><span class="sxs-lookup"><span data-stu-id="463cb-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![Petunjuk status untuk tempahan yang dicadangkan pada halaman Pembantu Jadual](media/Resource-Management-image63.png)

- <span data-ttu-id="463cb-111">Pada permintaan sumber, status ditukar kepada **Keperluan Semakan Semula.**</span><span class="sxs-lookup"><span data-stu-id="463cb-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![Status permintaan sumber ditukar kepada Keperluan Semakan Semula](media/Resource-Management-image64.png)

- <span data-ttu-id="463cb-113">Pada tab **Pasukan** projek, permintaan ahli pasukan generik **Status Permintaan** ditukar kepada **Keperluan Semakan Semula.**</span><span class="sxs-lookup"><span data-stu-id="463cb-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![Status permintaan ahli pasukan generik ditukar kepada Keperluan Semakan Semula pada tab Pasukan.](media/Resource-Management-image48.png)

<span data-ttu-id="463cb-115">Pengurus projek boleh sama ada menerima atau menolak cadangan itu.</span><span class="sxs-lookup"><span data-stu-id="463cb-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="463cb-116">Apabila pengurus sumber memproses permintaan sumber, mereka boleh menggunakan sebarang pendekatan berikut:</span><span class="sxs-lookup"><span data-stu-id="463cb-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="463cb-117">Mencadangkan berbilang sumber untuk memenuhi permintaan jika tiada sumber tunggal tersedia untuk memenuhi jam yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="463cb-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="463cb-118">Waktu yang dicadangkan kemudian berpecah antara sumber yang boleh memenuhi jam yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="463cb-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="463cb-119">Dalam senario ini, jam tidak boleh bertindan.</span><span class="sxs-lookup"><span data-stu-id="463cb-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="463cb-120">Mencadangkan lebih sedikit sumber daripada keperluan.</span><span class="sxs-lookup"><span data-stu-id="463cb-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="463cb-121">Dalam senario ini, kapasiti sumber yang dicadangkan adalah kurang daripada jam yang diperlukan yang ditentukan oleh peminta.</span><span class="sxs-lookup"><span data-stu-id="463cb-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="463cb-122">Oleh itu, apabila peminta menerima sumber yang dicadangkan, keperluan sumber yang tidak dipatuhi dicipta untuk menawan permintaan yang berbaki.</span><span class="sxs-lookup"><span data-stu-id="463cb-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="463cb-123">Tempah berbilang sumber untuk memenuhi permintaan jika tiada sumber tunggal tersedia untuk menyelesaikan kerja.</span><span class="sxs-lookup"><span data-stu-id="463cb-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="463cb-124">Menempah lebih sedikit sumber daripada keperluan.</span><span class="sxs-lookup"><span data-stu-id="463cb-124">Book fewer resources than are required.</span></span> <span data-ttu-id="463cb-125">Dalam senario ini, masa yang ditempah adalah lebih sedikit daripada jam yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="463cb-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="463cb-126">Sistem ini memberi panduan kepada anda untuk mencadangkan sumber dan bukannya penempahan, supaya peminta boleh mengesahkan dan menjejaki permintaan yang berbaki.</span><span class="sxs-lookup"><span data-stu-id="463cb-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="463cb-127">Penggunaan boleh dibilkan</span><span class="sxs-lookup"><span data-stu-id="463cb-127">Billable utilization</span></span>

<span data-ttu-id="463cb-128">Sumber boleh mempunyai sasaran penggunaan boleh dibilkan.</span><span class="sxs-lookup"><span data-stu-id="463cb-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="463cb-129">Penggunaan sasaran ini sama ada ditakrifkan sebagai atribut pada peranan lalai sumber atau ditetapkan pada rekod sumber boleh ditempah individu.</span><span class="sxs-lookup"><span data-stu-id="463cb-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="463cb-130">Pengiraan penggunaan adalah berdasarkan masa sebenar bahawa sumber telah dilaporkan dengan menggunakan kemasukan penyertaan yang diluluskan.</span><span class="sxs-lookup"><span data-stu-id="463cb-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="463cb-131">Formula berikut digunakan untuk mengira penggunaan:</span><span class="sxs-lookup"><span data-stu-id="463cb-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="463cb-132">Penggunaan boleh dibilkan = Jam sebenar ÷ Kapasiti sumber boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="463cb-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="463cb-133">Penggunaan tidak boleh dibilkan = Masa sebenar dengan ID jenis bil = Tidak dikenakan caj, Pelengkap atau Tidak tersedia yang boleh ÷ Kapasiti sumber</span><span class="sxs-lookup"><span data-stu-id="463cb-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="463cb-134">Dalaman = Masa sebenar dengan tiada kontrak jualan ÷ Kapasiti sumber</span><span class="sxs-lookup"><span data-stu-id="463cb-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="463cb-135">Kapasiti sumber = Waktu kerja sumber – Keluar dari pejabat – Hari tidak bekerja</span><span class="sxs-lookup"><span data-stu-id="463cb-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="463cb-136">Anda boleh mencari pandangan **Penggunaan Sumber** dalam anak tetingkap **Sumber**.</span><span class="sxs-lookup"><span data-stu-id="463cb-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![Pandangan Penggunaan sumber](media/Resource-Management-image65.png)

<span data-ttu-id="463cb-138">Setiap sel dalam grid mewakili peratusan penggunaan boleh dibilkan bagi sumber dalam tempoh, seperti hari, minggu atau bulan.</span><span class="sxs-lookup"><span data-stu-id="463cb-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="463cb-139">Formula berikut digunakan untuk mewarnakan sel:</span><span class="sxs-lookup"><span data-stu-id="463cb-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="463cb-140">**Hijau:** Penggunaan boleh dibilkan \>= Penggunaan sasaran sumber</span><span class="sxs-lookup"><span data-stu-id="463cb-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="463cb-141">**Kuning:** Penggunaan sasaran – 20 \<= Penggunaan boleh dibilkan \< Penggunaan sasaran</span><span class="sxs-lookup"><span data-stu-id="463cb-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="463cb-142">**Merah:** Penggunaan boleh dibilkan \< Penggunaan sasaran – 20</span><span class="sxs-lookup"><span data-stu-id="463cb-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="463cb-143">Oleh kerana pandangan **Penggunaan Sumber** adalah berdasarkan Papan Jadual, anda boleh menggunakan keupayaan penapisan Papan Jadual untuk menapis hasil anda.</span><span class="sxs-lookup"><span data-stu-id="463cb-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="463cb-144">Grid memerlukan anda menetapkan penggunaan sasaran pada sama ada peranan atau sumber individu.</span><span class="sxs-lookup"><span data-stu-id="463cb-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="463cb-145">Untuk melakukan persediaan ini, pergi ke **Peranan** \> **Peranan sumber**.</span><span class="sxs-lookup"><span data-stu-id="463cb-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="463cb-146">Selain itu, peranan lalai mesti ditugaskan kepada setiap sumber boleh ditempah.</span><span class="sxs-lookup"><span data-stu-id="463cb-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="463cb-147">Pergi ke **Sumber** \> **Sumber**.</span><span class="sxs-lookup"><span data-stu-id="463cb-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="463cb-148">Pada tab **Project Service** sahkan peranan sumber ditakrifkan dan medan **Adalah Lalai** untuk ia disetkan kepada **Ya.**</span><span class="sxs-lookup"><span data-stu-id="463cb-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="463cb-149">Anda boleh menambah peranan tambahan di mana **Adalah Lalai = No**.</span><span class="sxs-lookup"><span data-stu-id="463cb-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="463cb-150">Peranan di mana **Adalah Lalai = Ya** digunakan untuk menilai penggunaan sumber terhadap sasaran untuk peranan tersebut.</span><span class="sxs-lookup"><span data-stu-id="463cb-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![Peranan lalai ditetapkan](media/Resource-Management-image67.png)

<span data-ttu-id="463cb-152">Pada tab **Project Service** , anda juga boleh menetapkan penggunaan sasaran individu untuk sumber.</span><span class="sxs-lookup"><span data-stu-id="463cb-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="463cb-153">Pengiraan penggunaan ini kemudian menggunakan penggunaan sasaran yang akan menilai sasaran sumber bukan sasaran peranan lalai sumber.</span><span class="sxs-lookup"><span data-stu-id="463cb-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="463cb-154">Penggunaan ditunjukkan untuk sumber hanya jika sumber tersebut telah diluluskan dan masa boleh dikenakan dalam tempoh yang ditunjukkan dalam grid.</span><span class="sxs-lookup"><span data-stu-id="463cb-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="463cb-155">Ketersediaan sumber</span><span class="sxs-lookup"><span data-stu-id="463cb-155">Resource availability</span></span>

<span data-ttu-id="463cb-156">Adalah penting bahawa pengurus sumber boleh melihat ketersediaan sumber dan kemas kini tempahan.</span><span class="sxs-lookup"><span data-stu-id="463cb-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="463cb-157">Dalam sesetengah kes, tidak ada permintaan formal (permintaan sumber), tetapi pengurus sumber mesti bertindak balas kepada permintaan yang tidak dirancang yang datang melalui saluran seperti e-mel, panggilan telefon atau mesej segera.</span><span class="sxs-lookup"><span data-stu-id="463cb-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="463cb-158">Pengurus sumber menggunakan Papan Jadual untuk mengemas kini sumber dan penempahan.</span><span class="sxs-lookup"><span data-stu-id="463cb-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="463cb-159">Waktu kerja sumber digunakan sebagai asas untuk mengira ketersediaan sumber.</span><span class="sxs-lookup"><span data-stu-id="463cb-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="463cb-160">Tempahan sumber mengambil kapasiti sumber.</span><span class="sxs-lookup"><span data-stu-id="463cb-160">Resource bookings consume the capacity of the resources.</span></span>

![Papan Jadual](media/Resource-Management-image68.png)

<span data-ttu-id="463cb-162">Papan Jadual menggunakan warna dan pembayangan untuk menunjukkan penempahan, ketersediaan dan pilihan berlebihan dan juga status tempahan.</span><span class="sxs-lookup"><span data-stu-id="463cb-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="463cb-163">Tetapan dalam tetapan Papan Jadual membolehkan anda menunjukkan petunjuk.</span><span class="sxs-lookup"><span data-stu-id="463cb-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="463cb-164">Jika anak panah tunjuk sebelah kanan muncul di sebelah sumber boleh ditempah individu pada Papan Jadual, sumber itu dapat dikembangkan untuk menunjukkan butiran kerja yang digunakan oleh sumber tersebut.</span><span class="sxs-lookup"><span data-stu-id="463cb-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![Sumber boleh ditempah dikembangkan ke Papan Jadual](media/Resource-Management-image69.png)

<span data-ttu-id="463cb-166">Kerana Dynamics 365 Project Service Automation menggunakan enjin Universal Resource Scheduling, jika anda juga telah Dynamics 365 Field Service dipasang, anda boleh melihat butiran daripada penempahan sumber untuk projek, pesanan kerja dan sebarang entiti lain yang anda telah melanjutkan penjadualan.</span><span class="sxs-lookup"><span data-stu-id="463cb-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![Butiran terperinci mengenai tempahan sumber untuk projek dan pesanan kerja](media/Resource-Management-image70.png)

<span data-ttu-id="463cb-168">Untuk melihat lebih banyak butiran mengenai sumber individu, klik kanan padanya untuk membuka kad sumber.</span><span class="sxs-lookup"><span data-stu-id="463cb-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![Kad Sumber](media/Resource-Management-image71.png)
