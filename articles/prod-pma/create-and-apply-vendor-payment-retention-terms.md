---
title: Cipta dan gunakan terma pengekalan pembayaran vendor
description: Topik ini memberikan maklumat tentang cara menyediakan dan mengekalkan terma pengekalan untuk pembayaran vendor.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 09bb30f55ee8e1f24634e9d8b7dea95bd3dbd24f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006341"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="ee345-103">Cipta dan gunakan terma pengekalan pembayaran vendor</span><span class="sxs-lookup"><span data-stu-id="ee345-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="ee345-104">Menyediakan terma pengekalan pembayaran vendor untuk projek berguna apabila organisasi anda mahu mengekalkan sebahagian daripada pembayaran yang dibuat kepada vendor.</span><span class="sxs-lookup"><span data-stu-id="ee345-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="ee345-105">Contohnya, apabila anda ingin menangguhkan pembayaran kepada vendor sehingga produk yang dihantar memenuhi jangkaan anda.</span><span class="sxs-lookup"><span data-stu-id="ee345-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="ee345-106">Terma pengekalan pembayaran vendor dapat ditentukan semasa anda merundingkan kontrak vendor.</span><span class="sxs-lookup"><span data-stu-id="ee345-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="ee345-107">Cipta terma pengekalan pembayaran vendor</span><span class="sxs-lookup"><span data-stu-id="ee345-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="ee345-108">Anda boleh memasukkan peratusan pembayaran vendor untuk pengekalan dan peratusan jumlah dikekalkan sebelumnya yang akan dikeluarkan.</span><span class="sxs-lookup"><span data-stu-id="ee345-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="ee345-109">Jumlah dikekalkan secara automatik pada invois vendor sehingga kontrak mencapai tahap penyelesaian yang ditentukan.</span><span class="sxs-lookup"><span data-stu-id="ee345-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="ee345-110">Selepas anda menyediakan terma pengekalan, anda boleh menggunakannya pada sebarang projek untuk vendor tersebut.</span><span class="sxs-lookup"><span data-stu-id="ee345-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="ee345-111">Gunakan langkah berikut untuk menyediakan dan mengekalkan terma pengekalan untuk pembayaran vendor.</span><span class="sxs-lookup"><span data-stu-id="ee345-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="ee345-112">Pergi ke **Pengurusan dan perakaunan projek** > **Pengekalan** > **Terma pengekalan pembayaran vendor**.</span><span class="sxs-lookup"><span data-stu-id="ee345-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="ee345-113">Pilih **Baharu** untuk menambah terma pengekalan vendor yang baharu.</span><span class="sxs-lookup"><span data-stu-id="ee345-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="ee345-114">Nilai **ID peraturan** untuk terma baharu akan dimasukkan secara automatik.</span><span class="sxs-lookup"><span data-stu-id="ee345-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="ee345-115">Masukkan perihalan ringkas dalam medan **Perihalan** dan pada FastTab **Terma**, pilih **Tambah baris** untuk memasukkan nilai terma bagi yang berikut:</span><span class="sxs-lookup"><span data-stu-id="ee345-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="ee345-116">**Peratusan unit yang dihantar**: Masukkan peratusan siap untuk terma tersebut.</span><span class="sxs-lookup"><span data-stu-id="ee345-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="ee345-117">Jumlah dikekalkan secara automatik pada invois vendor sehingga peringkat penyiapan projek sama dengan peratusan yang ditentukan.</span><span class="sxs-lookup"><span data-stu-id="ee345-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="ee345-118">Contohnya, jika anda memasukkan 50.00, jumlah dikekalkan sehingga projek tersebut 50 peratus selesai.</span><span class="sxs-lookup"><span data-stu-id="ee345-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="ee345-119">**Peratusan untuk dikekalkan**: Masukkan peratusan jumlah invois vendor untuk dikekalkan.</span><span class="sxs-lookup"><span data-stu-id="ee345-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="ee345-120">Contohnya, jika anda memasukkan 10.00, maka 10 peratus daripada jumlah pada invois vendor dikekalkan sehingga projek mencapai peratusan penyiapan seperti yang ditetapkan dalam **medan Peratusan unit yang dihantar**.</span><span class="sxs-lookup"><span data-stu-id="ee345-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="ee345-121">**Peratusan untuk dikeluarkan**: Pilih **Tambah baris** untuk memasukkan peratusan mana-mana jumlah dikekalkan sebelum ini yang akan dikeluarkan untuk peringkat penyiapan projek yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="ee345-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="ee345-122">Jika anda mempunyai lebih daripada satu pencapaian untuk peringkat penyiapan projek yang berbeza, masukkan baris terma pengekalan vendor yang berasingan bagi setiap peraturan pengekalan.</span><span class="sxs-lookup"><span data-stu-id="ee345-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="ee345-123">Setiap baris boleh menentukan peratusan pengekalan yang berbeza dan peratusan keluaran yang berbeza bagi setiap peringkat penyiapan projek yang ditetapkan.</span><span class="sxs-lookup"><span data-stu-id="ee345-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="ee345-124">Selepas anda mencipta terma pengekalan vendor untuk vendor, anda boleh menggunakan terma tersebut untuk projek.</span><span class="sxs-lookup"><span data-stu-id="ee345-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="ee345-125">Gunakan terma pengekalan vendor pada projek</span><span class="sxs-lookup"><span data-stu-id="ee345-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="ee345-126">Pergi ke **Pengurusan dan perakaunan projek** > **Projek** > **Semua projek** dan buka projek dari halaman senarai projek.</span><span class="sxs-lookup"><span data-stu-id="ee345-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="ee345-127">Pada FastTab **Perjanjian vendor**, pilih **Tambah baris**.</span><span class="sxs-lookup"><span data-stu-id="ee345-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="ee345-128">Dalam **medan Kod akaun**, pilih salah satu daripada pilihan berikut:</span><span class="sxs-lookup"><span data-stu-id="ee345-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="ee345-129">**Jadual**: Terma pengekalan vendor digunakan pada vendor tunggal.</span><span class="sxs-lookup"><span data-stu-id="ee345-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="ee345-130">**Kumpulan**: Terma pengekalan vendor digunakan pada semua vendor dalam kumpulan vendor.</span><span class="sxs-lookup"><span data-stu-id="ee345-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="ee345-131">**Semua**: Terma pengekalan vendor digunakan pada semua vendor.</span><span class="sxs-lookup"><span data-stu-id="ee345-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="ee345-132">Dalam **medan Vendor/Kumpulan vendor**, pilih vendor atau kumpulan vendor yang menggunakan terma pengekalan vendor.</span><span class="sxs-lookup"><span data-stu-id="ee345-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="ee345-133">Jika anda memilih **Semua** dalam langkah sebelumnya, medan ini tidak tersedia.</span><span class="sxs-lookup"><span data-stu-id="ee345-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="ee345-134">Dalam **medan Terma pengekalan vendor**, pilih terma pengekalan yang anda cipta dalam prosedur sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="ee345-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="ee345-135">Jika projek tersebut juga mempunyai terma bayar apabila dibayar (PWP) yang disediakan untuk vendor, masukkan peratusan ambang untuk projek dalam medan **Peratusan ambang PWP**.</span><span class="sxs-lookup"><span data-stu-id="ee345-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="ee345-136">Terma pengekalan vendor juga dipaparkan pada pesanan pembelian yang anda cipta untuk vendor.</span><span class="sxs-lookup"><span data-stu-id="ee345-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]