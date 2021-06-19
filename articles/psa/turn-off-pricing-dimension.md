---
title: Padamkan dimensi penetapan harga
description: Topik ini menunjukkan cara menyediakan dimensi penetapan harga dalam penyelesaian Project Service.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: da8615fa147838d9088c639039d5a2534e662e82
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014307"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="d8e08-103">Padamkan dimensi penetapan harga</span><span class="sxs-lookup"><span data-stu-id="d8e08-103">Turn off a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d8e08-104">Anda mungkin perlu menyemak semula dan mengemas kini strategi penetapan harga setiap beberapa tahun.</span><span class="sxs-lookup"><span data-stu-id="d8e08-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="d8e08-105">Sebarang kemas kini yang anda lakukan mungkin memerlukan anda memadamkan dimensi penetapan harga yang sedia ada dan mencipta satu yang baharu.</span><span class="sxs-lookup"><span data-stu-id="d8e08-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="d8e08-106">Sebagai contoh, anda mungkin telah memilih lebih banyak **Peranan** tetapi kini anda telah memutuskan harga mengikut **Pengalaman Kerja**.</span><span class="sxs-lookup"><span data-stu-id="d8e08-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="d8e08-107">Ini mungkin memerlukan anda **Peranan** sebagai dimensi penetapan harga dan mencipta **Pengalaman Kerja** sebagai dimensi penetapan harga baharu.</span><span class="sxs-lookup"><span data-stu-id="d8e08-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="d8e08-108">Mematikan dimensi penetapan harga, tanpa mengira jika ia di luar kotak atau tersuai, boleh dilakukan dengan menetapkan medan **Digunakan pada Kos** dan **Diguna pada Jualan** Dimensi Penetapan Harga ke **Tidak**.</span><span class="sxs-lookup"><span data-stu-id="d8e08-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="d8e08-109">Walau bagaimanapun, apabila anda lakukan ini, anda mungkin menerima mesej ralat berikut.</span><span class="sxs-lookup"><span data-stu-id="d8e08-109">However, when you do this, you might receive the following error message.</span></span>

![Ralat Proses Perniagaan mungkin apabila memadamkan dimensi penetapan harga](media/Business-Process-Error.png)


<span data-ttu-id="d8e08-111">Mesej ralat ini menunjukkan bahawa terdapat rekod harga yang ditetapkan sebelum ini untuk dimensi yang sedang dipadamkan.</span><span class="sxs-lookup"><span data-stu-id="d8e08-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="d8e08-112">Semua **Harga Peranan** dan **Tokokan Harga Peranan** yang merujuk kepada dimensi mesti dipadamkan sebelum kebolehgunaan dimensi boleh ditetapkan ke **Tidak**.</span><span class="sxs-lookup"><span data-stu-id="d8e08-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="d8e08-113">Peraturan ini diguna pakai untuk kedua-dua dimensi penetapan harga luar kotak dan sebarang dimensi penetapan harga tersuai yang anda telah cipta.</span><span class="sxs-lookup"><span data-stu-id="d8e08-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="d8e08-114">Sebab untuk pengesahan ini adalah kerana Project Service mempunyai kekangan bahawa setiap rekod **Harga Peranan** mesti mempunyai kombinasi unik dimensi.</span><span class="sxs-lookup"><span data-stu-id="d8e08-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="d8e08-115">Sebagai contoh, pada senarai harga yang dipanggil **Kadar Kos 2018 AS**, anda mempunyai baris harga **Peranan harga**.</span><span class="sxs-lookup"><span data-stu-id="d8e08-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="d8e08-116">Tajuk Standard</span><span class="sxs-lookup"><span data-stu-id="d8e08-116">Standard Title</span></span>         | <span data-ttu-id="d8e08-117">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="d8e08-117">Org Unit</span></span>    |<span data-ttu-id="d8e08-118">Unit</span><span class="sxs-lookup"><span data-stu-id="d8e08-118">Unit</span></span>   |<span data-ttu-id="d8e08-119">Harga</span><span class="sxs-lookup"><span data-stu-id="d8e08-119">Price</span></span>  |<span data-ttu-id="d8e08-120">Mata wang</span><span class="sxs-lookup"><span data-stu-id="d8e08-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="d8e08-121">Jurutera sistem</span><span class="sxs-lookup"><span data-stu-id="d8e08-121">Systems Engineer</span></span>|<span data-ttu-id="d8e08-122">Contoso AS</span><span class="sxs-lookup"><span data-stu-id="d8e08-122">Contoso US</span></span>|<span data-ttu-id="d8e08-123">Jam</span><span class="sxs-lookup"><span data-stu-id="d8e08-123">Hour</span></span>| <span data-ttu-id="d8e08-124">100</span><span class="sxs-lookup"><span data-stu-id="d8e08-124">100</span></span>|<span data-ttu-id="d8e08-125">USD</span><span class="sxs-lookup"><span data-stu-id="d8e08-125">USD</span></span>|
| <span data-ttu-id="d8e08-126">Jurutera Sistem Senior</span><span class="sxs-lookup"><span data-stu-id="d8e08-126">Senior Systems Engineer</span></span>|<span data-ttu-id="d8e08-127">Contoso AS</span><span class="sxs-lookup"><span data-stu-id="d8e08-127">Contoso US</span></span>|<span data-ttu-id="d8e08-128">Jam</span><span class="sxs-lookup"><span data-stu-id="d8e08-128">Hour</span></span>| <span data-ttu-id="d8e08-129">150</span><span class="sxs-lookup"><span data-stu-id="d8e08-129">150</span></span>| <span data-ttu-id="d8e08-130">USD</span><span class="sxs-lookup"><span data-stu-id="d8e08-130">USD</span></span>|


<span data-ttu-id="d8e08-131">Apabila anda memadamkan **Tajuk Standard** sebagai dimensi penetapan harga dan enjin penetapan harga Project Service mencari untuk harga, ia hanya akan menggunakan nilai **Unit Harga** daripada konteks input.</span><span class="sxs-lookup"><span data-stu-id="d8e08-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="d8e08-132">Jika **Unit Organisasi** konteks input ialah "Contoso AS", hasilnya tidak akan ditentukan kerana kedua-dua baris akan sepadan.</span><span class="sxs-lookup"><span data-stu-id="d8e08-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="d8e08-133">Untuk mengelakkan senario ini, apabila anda mencipta **Harga Peranan** Project Service mengesahkan bahawa kombinasi dimensi adalah unik.</span><span class="sxs-lookup"><span data-stu-id="d8e08-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="d8e08-134">Jika dimensi telah dimatikan selepas rekod **Peranan Harga** dicipta, kekangan ini boleh dilanggar.</span><span class="sxs-lookup"><span data-stu-id="d8e08-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="d8e08-135">Oleh itu, ia adalah diperlukan bahawa sebelum anda mematikan dimensi, anda memadamkan **Peranan Harga** dan **Tokokan Harga Peranan** yang mempunyai nilai dimensi yang diisi.</span><span class="sxs-lookup"><span data-stu-id="d8e08-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]