---
title: Konfigurasikan penginvoisan projek antara syarikat
description: Topik ini menunjukkan cara menyediakan penginvoisan projek antara dua syarikat dalam organisasi anda.
author: Yowelle
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9df15cb3712356a164de3507f5dbc17a9ff9a652
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288390"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="c5fd6-103">Konfigurasikan penginvoisan projek antara syarikat</span><span class="sxs-lookup"><span data-stu-id="c5fd6-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c5fd6-104">Topik ini menunjukkan cara menyediakan penginvoisan projek antara dua syarikat dalam organisasi anda.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="c5fd6-105">Tugas ini menggunakan set data USSI.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="c5fd6-106">Dalam anak tetingkap navigasi, pergi ke **Modul > Akaun belum bayar > Vendor > Semua vendor**.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="c5fd6-107">Dalam senarai **Semua vendor**, cari dan pilih rekod yang dikehendaki.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="c5fd6-108">Pada Anak Tetingkap Tindakan, pilih **Umum**.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="c5fd6-109">Pilih **Antara Syarikat**.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="c5fd6-110">Tetapkan **Aktif** kepada **Ya** untuk mendayakan perdagangan antara syarikat.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="c5fd6-111">Dalam medan **Syarikat pelanggan**, masukkan atau pilih nilai.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="c5fd6-112">Dalam medan **Akaun saya**, masukkan atau pilih nilai.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="c5fd6-113">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-113">Select **Save**.</span></span>
9. <span data-ttu-id="c5fd6-114">Tutup halaman untuk kembali ke halaman utama.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="c5fd6-115">Dalam anak tetingkap navigasi, pergi ke **Modul > Pengurusan dan perakaunan projek > Penyediaan > Pengurusan projek dan parameter perakaunan**.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="c5fd6-116">Pilih tab **Antara syarikat**.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="c5fd6-117">Gerakkan gelangsar ke **Ya** untuk mendayakan penjadualan sumber antara syarikat dan lembaran masa.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="c5fd6-118">Dalam senarai, tandakan baris yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="c5fd6-119">Pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-119">Select **New**.</span></span>
15. <span data-ttu-id="c5fd6-120">Dalam medan **Meminjam entiti undang-undang**, masukkan atau pilih nilai.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="c5fd6-121">Pilih kotak semak **Hasil terakru**.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="c5fd6-122">Dalam medan **Kategori lembaran masa lalai**, masukkan atau pilih nilai.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="c5fd6-123">Dalam medan **Kategori perbelanjaan lalai**, masukkan atau pilih nilai.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="c5fd6-124">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-124">Select **Save**.</span></span>
20. <span data-ttu-id="c5fd6-125">Tutup halaman.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-125">Close the page.</span></span>
21. <span data-ttu-id="c5fd6-126">Dalam anak tetingkap navigasi, pergi ke **Modul > Pengurusan dan perakaunan projek > Penyediaan > Penyiaran > Penyediaan penyiaran lejar**.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="c5fd6-127">Dalam medan **Jenis akaun Lejar**, pilih pilihan.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="c5fd6-128">Pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-128">Select **New**.</span></span>
24. <span data-ttu-id="c5fd6-129">Dalam medan **Akaun utama** baris baharu, tentukan nilai yang dikehendaki.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="c5fd6-130">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-130">Select **Save**.</span></span>
26. <span data-ttu-id="c5fd6-131">Tutup halaman.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-131">Close the page.</span></span>
27. <span data-ttu-id="c5fd6-132">Dalam anak tetingkap navigasi, pergi ke **Modul > Pengurusan dan perakaunan projek > Penyediaan > Harga > Pindahkan harga**.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="c5fd6-133">Pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-133">Select **New**.</span></span>
29. <span data-ttu-id="c5fd6-134">Dalam medan **Tarikh berkuat kuasa**, masukkan tarikh.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="c5fd6-135">Dalam medan **Meminjam entiti undang-undang**, masukkan atau pilih nilai.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="c5fd6-136">Dalam medan **Pindahkan model harga**, pilih pilihan.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="c5fd6-137">Dalam medan **Penentuan harga**, masukkan nombor.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="c5fd6-138">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="c5fd6-138">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]