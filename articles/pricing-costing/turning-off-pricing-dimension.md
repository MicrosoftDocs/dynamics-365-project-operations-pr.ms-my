---
title: Matikan dimensi penetapan harga
description: Topik ini menyediakan maklumat tentang cara mematikan dimensi penetapan harga.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d2e10c9ce782697fa4cbbe6eb63491ebb573a6f6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274739"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="52e88-103">Matikan dimensi penetapan harga</span><span class="sxs-lookup"><span data-stu-id="52e88-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="52e88-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="52e88-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="52e88-105">Anda mungkin perlu menyemak semula dan mengemas kini strategi penetapan harga setiap beberapa tahun.</span><span class="sxs-lookup"><span data-stu-id="52e88-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="52e88-106">Sebarang kemas kini yang anda lakukan mungkin memerlukan anda memadamkan dimensi penetapan harga yang sedia ada dan mencipta satu yang baharu.</span><span class="sxs-lookup"><span data-stu-id="52e88-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="52e88-107">Sebagai contoh, anda mungkin telah memilih lebih banyak **Peranan** tetapi kini anda telah memutuskan harga mengikut **Pengalaman Kerja**.</span><span class="sxs-lookup"><span data-stu-id="52e88-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="52e88-108">Ini mungkin memerlukan anda mematikan **Peranan** sebagai dimensi penetapan harga dan mencipta **Pengalaman Kerja** sebagai dimensi penetapan harga baharu.</span><span class="sxs-lookup"><span data-stu-id="52e88-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="52e88-109">Mematikan dimensi penetapan harga, tanpa mengira jika ia di luar kotak atau tersuai, boleh dilakukan dengan menetapkan medan **Digunakan pada Kos** dan **Diguna pada Jualan** Dimensi Penetapan Harga ke **Tidak**.</span><span class="sxs-lookup"><span data-stu-id="52e88-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="52e88-110">Walau bagaimanapun, apabila anda melakukannya, anda mungkin menerima message ralat, **Dimensi penetapan harga tidak boleh dikemas kini atau dipadam jika terdapat rekod harga yang berkaitan.**</span><span class="sxs-lookup"><span data-stu-id="52e88-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

![Ralat Proses Perniagaan mungkin apabila memadamkan dimensi penetapan harga](media/Business-Process-Error.png)

<span data-ttu-id="52e88-112">Mesej ralat ini menunjukkan bahawa terdapat rekod harga yang ditetapkan sebelum ini untuk dimensi yang sedang dipadamkan.</span><span class="sxs-lookup"><span data-stu-id="52e88-112">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="52e88-113">Semua **Harga Peranan** dan **Tokokan Harga Peranan** yang merujuk kepada dimensi mesti dipadamkan sebelum kebolehgunaan dimensi boleh ditetapkan ke **Tidak**.</span><span class="sxs-lookup"><span data-stu-id="52e88-113">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="52e88-114">Peraturan ini diguna pakai untuk kedua-dua dimensi penetapan harga luar kotak dan sebarang dimensi penetapan harga tersuai yang anda telah cipta.</span><span class="sxs-lookup"><span data-stu-id="52e88-114">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="52e88-115">Sebab pengesahan ini adalah kerana rekod **Harga Peranan** masing-masing mesti mempunyai kombinasi dimensi yang unik.</span><span class="sxs-lookup"><span data-stu-id="52e88-115">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="52e88-116">Sebagai contoh, pada senarai harga yang dipanggil **Kadar Kos 2018 AS**, anda mempunyai baris harga **Peranan harga**.</span><span class="sxs-lookup"><span data-stu-id="52e88-116">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="52e88-117">Tajuk Standard</span><span class="sxs-lookup"><span data-stu-id="52e88-117">Standard Title</span></span>         | <span data-ttu-id="52e88-118">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="52e88-118">Org Unit</span></span>    |<span data-ttu-id="52e88-119">Unit</span><span class="sxs-lookup"><span data-stu-id="52e88-119">Unit</span></span>   |<span data-ttu-id="52e88-120">Harga</span><span class="sxs-lookup"><span data-stu-id="52e88-120">Price</span></span>  |<span data-ttu-id="52e88-121">Mata Wang</span><span class="sxs-lookup"><span data-stu-id="52e88-121">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="52e88-122">Jurutera sistem</span><span class="sxs-lookup"><span data-stu-id="52e88-122">Systems Engineer</span></span>|<span data-ttu-id="52e88-123">Contoso AS</span><span class="sxs-lookup"><span data-stu-id="52e88-123">Contoso US</span></span>|<span data-ttu-id="52e88-124">Hour</span><span class="sxs-lookup"><span data-stu-id="52e88-124">Hour</span></span>| <span data-ttu-id="52e88-125">100</span><span class="sxs-lookup"><span data-stu-id="52e88-125">100</span></span>|<span data-ttu-id="52e88-126">USD</span><span class="sxs-lookup"><span data-stu-id="52e88-126">USD</span></span>|
| <span data-ttu-id="52e88-127">Jurutera Sistem Senior</span><span class="sxs-lookup"><span data-stu-id="52e88-127">Senior Systems Engineer</span></span>|<span data-ttu-id="52e88-128">Contoso AS</span><span class="sxs-lookup"><span data-stu-id="52e88-128">Contoso US</span></span>|<span data-ttu-id="52e88-129">Hour</span><span class="sxs-lookup"><span data-stu-id="52e88-129">Hour</span></span>| <span data-ttu-id="52e88-130">150</span><span class="sxs-lookup"><span data-stu-id="52e88-130">150</span></span>| <span data-ttu-id="52e88-131">USD</span><span class="sxs-lookup"><span data-stu-id="52e88-131">USD</span></span>|


<span data-ttu-id="52e88-132">Apabila anda mematikan **Tajuk Standard** sebagai dimensi penetapan harga dan enjin penetapan harga mencari harga, ianya akan hanya menggunakan nilai **Unit Organisasi** daripada konteks input.</span><span class="sxs-lookup"><span data-stu-id="52e88-132">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="52e88-133">Jika **Unit Organisasi** konteks input ialah "Contoso US", hasilnya tidak akan ditentukan kerana kedua-dua baris akan dipadankan.</span><span class="sxs-lookup"><span data-stu-id="52e88-133">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="52e88-134">Untuk mengelakkan senario ini, apabila anda mencipta rekod **Harga Peranan**, sistem mengesahkan bahawa kombinasi dimensi adalah unik.</span><span class="sxs-lookup"><span data-stu-id="52e88-134">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="52e88-135">Jika dimensi telah dimatikan selepas rekod **Peranan Harga** dicipta, kekangan ini boleh dilanggar.</span><span class="sxs-lookup"><span data-stu-id="52e88-135">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="52e88-136">Oleh itu, ia adalah diperlukan bahawa sebelum anda mematikan dimensi, anda memadamkan **Peranan Harga** dan **Tokokan Harga Peranan** yang mempunyai nilai dimensi yang diisi.</span><span class="sxs-lookup"><span data-stu-id="52e88-136">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]