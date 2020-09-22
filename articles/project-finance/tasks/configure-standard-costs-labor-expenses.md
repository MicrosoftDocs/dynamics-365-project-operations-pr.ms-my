---
title: Konfigurasikan kos standard untuk buruh dan perbelanjaan
description: Topik ini menerangkan cara menetapkan kos standard untuk buruh dan perbelanjaan untuk projek.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: fa7c024f-4b18-4d29-9fd4-9c430cd83fad
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3e796cc03aeaa28938c56ce37d5075755248dfa
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753997"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="fc2b6-103">Konfigurasikan kos standard untuk buruh dan perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="fc2b6-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fc2b6-104">Topik ini menerangkan cara menetapkan kos standard untuk buruh dan perbelanjaan untuk projek.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="fc2b6-105">Tugas ini menggunakan set data USSI.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="fc2b6-106">Dalam anak tetingkap navigasi, pergi ke **Modul > Pengurusan dan perakaunan projek > Penyediaan > Harga > Harga kos (jam)**.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="fc2b6-107">Pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-107">Select **New**.</span></span>
3. <span data-ttu-id="fc2b6-108">Dalam medan **Tarikh berkuat kuasa**, masukkan tarikh.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="fc2b6-109">Dalam medan **Harga kos**, masukkan nombor.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="fc2b6-110">Anda boleh menetapkan harga kos standard untuk kategori projek, atau anda boleh menetapkan harga kos mengikut ombor pekerja, nombor projek, kategori, tarikh, atau mana-mana kombinasi ini.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="fc2b6-111">Harga kos yang dikenakan ialah harga kos dengan tahap butiran tertinggi.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="fc2b6-112">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-112">Select **Save**.</span></span>
6. <span data-ttu-id="fc2b6-113">Dalam anak tetingkap navigasi, pergi ke **Modul > Pengurusan dan perakaunan projek > Penyediaan > Harga > Harga jualan (jam)**.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="fc2b6-114">Pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-114">Select **New**.</span></span>
8. <span data-ttu-id="fc2b6-115">Dalam medan **Tarikh berkuat kuasa**, masukkan tarikh.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="fc2b6-116">Dalam medan **Sah untuk**, pilih pilihan.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="fc2b6-117">Dalam medan **Penentuan harga**, masukkan nombor.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="fc2b6-118">Anda boleh menetapkan harga jualan standard untuk transaksi jam atau untuk kategori projek.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="fc2b6-119">Anda juga boleh menyediakan harga jualan mengikut nombor pekerja, nombor projek, kategori, tarikh transaksi atau sebarang kombinasi ini.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="fc2b6-120">Harga jualan sebenar, yang diguna pakai apabila pekerja memasukkan transaksi dalam jurnal Jam, adalah harga jualan dengan tahap butiran tertinggi.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="fc2b6-121">Sebagai contoh, jika kedua-dua harga jualan am dan harga jualan pekerja khusus adalah ditetapkan, harga jualan pekerja khusus digunakan.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="fc2b6-122">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-122">Select **Save**.</span></span>
12. <span data-ttu-id="fc2b6-123">Tutup halaman.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-123">Close the page.</span></span>
13. <span data-ttu-id="fc2b6-124">Dalam anak tetingkap navigasi, pergi ke **Modul > Pengurusan dan perakaunan projek > Penyediaan > Harga > Harga kos (perbelanjaan)**.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="fc2b6-125">Pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-125">Select **New**.</span></span>
15. <span data-ttu-id="fc2b6-126">Dalam medan **Tarikh berkuat kuasa**, masukkan tarikh.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="fc2b6-127">Dalam medan **Harga kos**, masukkan nombor.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="fc2b6-128">Berbilang medan boleh diisi, tetapi ini adalah minimum yang diperlukan untuk menyimpan rekod.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="fc2b6-129">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-129">Select **Save**.</span></span>
18. <span data-ttu-id="fc2b6-130">Dalam anak tetingkap navigasi, pergi ke **Modul > Pengurusan dan perakaunan projek > Penyediaan > Harga > Harga jualan (perbelanjaan)**.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="fc2b6-131">Pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-131">Select **New**.</span></span>
20. <span data-ttu-id="fc2b6-132">Dalam medan **Tarikh berkuat kuasa**, masukkan tarikh.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="fc2b6-133">Dalam medan **Sah untuk**, pilih pilihan.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="fc2b6-134">Dalam medan **Penentuan harga**, masukkan nombor.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="fc2b6-135">Harga jualan sebenar, yang diguna pakai apabila pekerja memasukkan transaksi dalam jurnal perbelanjaan, adalah harga jualan dengan tahap butiran tertinggi.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="fc2b6-136">Sebagai contoh, jika kedua-dua harga jualan am dan pekerja khusus adalah ditetapkan, harga jualan pekerja khusus digunakan.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="fc2b6-137">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="fc2b6-137">Select **Save**.</span></span>

