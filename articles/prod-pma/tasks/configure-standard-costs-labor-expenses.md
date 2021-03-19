---
title: Konfigurasikan kos standard untuk buruh dan perbelanjaan
description: Topik ini menerangkan cara menetapkan kos standard untuk buruh dan perbelanjaan untuk projek.
author: Yowelle
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
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b16ed50584b2b4535d1c61fe7069708182a4820e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288345"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="6eda3-103">Konfigurasikan kos standard untuk buruh dan perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="6eda3-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6eda3-104">Topik ini menerangkan cara menetapkan kos standard untuk buruh dan perbelanjaan untuk projek.</span><span class="sxs-lookup"><span data-stu-id="6eda3-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="6eda3-105">Tugas ini menggunakan set data USSI.</span><span class="sxs-lookup"><span data-stu-id="6eda3-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="6eda3-106">Dalam anak tetingkap navigasi, pergi ke **Modul > Pengurusan dan perakaunan projek > Penyediaan > Harga > Harga kos (jam)**.</span><span class="sxs-lookup"><span data-stu-id="6eda3-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="6eda3-107">Pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="6eda3-107">Select **New**.</span></span>
3. <span data-ttu-id="6eda3-108">Dalam medan **Tarikh berkuat kuasa**, masukkan tarikh.</span><span class="sxs-lookup"><span data-stu-id="6eda3-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="6eda3-109">Dalam medan **Harga kos**, masukkan nombor.</span><span class="sxs-lookup"><span data-stu-id="6eda3-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="6eda3-110">Anda boleh menetapkan harga kos standard untuk kategori projek, atau anda boleh menetapkan harga kos mengikut ombor pekerja, nombor projek, kategori, tarikh, atau mana-mana kombinasi ini.</span><span class="sxs-lookup"><span data-stu-id="6eda3-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="6eda3-111">Harga kos yang dikenakan ialah harga kos dengan tahap butiran tertinggi.</span><span class="sxs-lookup"><span data-stu-id="6eda3-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="6eda3-112">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="6eda3-112">Select **Save**.</span></span>
6. <span data-ttu-id="6eda3-113">Dalam anak tetingkap navigasi, pergi ke **Modul > Pengurusan dan perakaunan projek > Penyediaan > Harga > Harga jualan (jam)**.</span><span class="sxs-lookup"><span data-stu-id="6eda3-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="6eda3-114">Pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="6eda3-114">Select **New**.</span></span>
8. <span data-ttu-id="6eda3-115">Dalam medan **Tarikh berkuat kuasa**, masukkan tarikh.</span><span class="sxs-lookup"><span data-stu-id="6eda3-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="6eda3-116">Dalam medan **Sah untuk**, pilih pilihan.</span><span class="sxs-lookup"><span data-stu-id="6eda3-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="6eda3-117">Dalam medan **Penentuan harga**, masukkan nombor.</span><span class="sxs-lookup"><span data-stu-id="6eda3-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="6eda3-118">Anda boleh menetapkan harga jualan standard untuk transaksi jam atau untuk kategori projek.</span><span class="sxs-lookup"><span data-stu-id="6eda3-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="6eda3-119">Anda juga boleh menyediakan harga jualan mengikut nombor pekerja, nombor projek, kategori, tarikh transaksi atau sebarang kombinasi ini.</span><span class="sxs-lookup"><span data-stu-id="6eda3-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="6eda3-120">Harga jualan sebenar, yang diguna pakai apabila pekerja memasukkan transaksi dalam jurnal Jam, adalah harga jualan dengan tahap butiran tertinggi.</span><span class="sxs-lookup"><span data-stu-id="6eda3-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="6eda3-121">Sebagai contoh, jika kedua-dua harga jualan am dan harga jualan pekerja khusus adalah ditetapkan, harga jualan pekerja khusus digunakan.</span><span class="sxs-lookup"><span data-stu-id="6eda3-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="6eda3-122">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="6eda3-122">Select **Save**.</span></span>
12. <span data-ttu-id="6eda3-123">Tutup halaman.</span><span class="sxs-lookup"><span data-stu-id="6eda3-123">Close the page.</span></span>
13. <span data-ttu-id="6eda3-124">Dalam anak tetingkap navigasi, pergi ke **Modul > Pengurusan dan perakaunan projek > Penyediaan > Harga > Harga kos (perbelanjaan)**.</span><span class="sxs-lookup"><span data-stu-id="6eda3-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="6eda3-125">Pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="6eda3-125">Select **New**.</span></span>
15. <span data-ttu-id="6eda3-126">Dalam medan **Tarikh berkuat kuasa**, masukkan tarikh.</span><span class="sxs-lookup"><span data-stu-id="6eda3-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="6eda3-127">Dalam medan **Harga kos**, masukkan nombor.</span><span class="sxs-lookup"><span data-stu-id="6eda3-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="6eda3-128">Berbilang medan boleh diisi, tetapi ini adalah minimum yang diperlukan untuk menyimpan rekod.</span><span class="sxs-lookup"><span data-stu-id="6eda3-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="6eda3-129">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="6eda3-129">Select **Save**.</span></span>
18. <span data-ttu-id="6eda3-130">Dalam anak tetingkap navigasi, pergi ke **Modul > Pengurusan dan perakaunan projek > Penyediaan > Harga > Harga jualan (perbelanjaan)**.</span><span class="sxs-lookup"><span data-stu-id="6eda3-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="6eda3-131">Pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="6eda3-131">Select **New**.</span></span>
20. <span data-ttu-id="6eda3-132">Dalam medan **Tarikh berkuat kuasa**, masukkan tarikh.</span><span class="sxs-lookup"><span data-stu-id="6eda3-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="6eda3-133">Dalam medan **Sah untuk**, pilih pilihan.</span><span class="sxs-lookup"><span data-stu-id="6eda3-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="6eda3-134">Dalam medan **Penentuan harga**, masukkan nombor.</span><span class="sxs-lookup"><span data-stu-id="6eda3-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="6eda3-135">Harga jualan sebenar, yang diguna pakai apabila pekerja memasukkan transaksi dalam jurnal perbelanjaan, adalah harga jualan dengan tahap butiran tertinggi.</span><span class="sxs-lookup"><span data-stu-id="6eda3-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="6eda3-136">Sebagai contoh, jika kedua-dua harga jualan am dan pekerja khusus adalah ditetapkan, harga jualan pekerja khusus digunakan.</span><span class="sxs-lookup"><span data-stu-id="6eda3-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="6eda3-137">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="6eda3-137">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]