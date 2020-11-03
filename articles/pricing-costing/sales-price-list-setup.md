---
title: Penyediaan senarai harga jualan
description: Topik ini menyediakan maklumat tentang senarai harga jualan untuk penetapan harga projek.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 1d2c797b72666123eb0a18d2d0c1df9fe3d207f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081283"
---
# <a name="sales-price-list-setup"></a><span data-ttu-id="7867a-103">Penyediaan senarai harga jualan</span><span class="sxs-lookup"><span data-stu-id="7867a-103">Sales price list setup</span></span>

<span data-ttu-id="7867a-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="7867a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7867a-105">Untuk sebut harga projek dan kontrak, senarai harga projek mempunyai corak ganti harga yang berbeza berbanding senarai harga produk.</span><span class="sxs-lookup"><span data-stu-id="7867a-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="7867a-106">Pada baris sebut harga berdasarkan katalog produk, anda boleh menulis ganti harga kepada peranan dan kategori secara langsung pada baris sebut harga, kerana setiap mata baris sebut harga kepada betul-betul satu item katalog.</span><span class="sxs-lookup"><span data-stu-id="7867a-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="7867a-107">Walau bagaimanapun, pada baris sebut harga berasaskan projek, anda tidak boleh mengganti harga kepada peranan dan kategori secara langsung pada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="7867a-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="7867a-108">Anda boleh menggunakan senarai harga projek untuk bekerja dengan kedua-dua corak gantian yang berbeza.</span><span class="sxs-lookup"><span data-stu-id="7867a-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="7867a-109">Kami mengesyorkan anda mempunyai senarai harga berasingan untuk sumber projek dan item katalog anda, disebabkan perbezaan tingkah laku antara kedua-dua apabila anda mengganti penetapan harga.</span><span class="sxs-lookup"><span data-stu-id="7867a-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="7867a-110">Setiap entiti berikut boleh mempunyai senarai harga jualan yang berkaitan untuk penetapan harga projek:</span><span class="sxs-lookup"><span data-stu-id="7867a-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="7867a-111">Pelanggan (akaun)</span><span class="sxs-lookup"><span data-stu-id="7867a-111">Customer (account)</span></span> 
- <span data-ttu-id="7867a-112">Peluang</span><span class="sxs-lookup"><span data-stu-id="7867a-112">Opportunity</span></span> 
- <span data-ttu-id="7867a-113">Sebut Harga</span><span class="sxs-lookup"><span data-stu-id="7867a-113">Quote</span></span> 
- <span data-ttu-id="7867a-114">Kontrak Projek</span><span class="sxs-lookup"><span data-stu-id="7867a-114">Project Contract</span></span>

<span data-ttu-id="7867a-115">Persatuan entiti ini dengan senarai harga ditunjukkan oleh senarai harga projek.</span><span class="sxs-lookup"><span data-stu-id="7867a-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="7867a-116">Anda boleh mengaitkan satu atau lebih senarai harga dengan entiti Pelanggan, Peluang, Sebut Harga dan Jualan Kontrak Projek.</span><span class="sxs-lookup"><span data-stu-id="7867a-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="7867a-117">Senarai harga projek lalai tidak dimasukkan secara automatik pada rekod pelanggan.</span><span class="sxs-lookup"><span data-stu-id="7867a-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="7867a-118">Walau bagaimanapun, anda boleh melampirkan senarai harga projek kepada rekod pelanggan secara manual.</span><span class="sxs-lookup"><span data-stu-id="7867a-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="7867a-119">Walau bagaimanapun, anda akan melampirkan senarai harga projek secara manual hanya apabila anda mempunyai perjanjian penetapan harga tersuai dengan pelanggan.</span><span class="sxs-lookup"><span data-stu-id="7867a-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="7867a-120">Apabila senarai harga projek dilampirkan ke entiti jualan, maklumat berikut disahkan:</span><span class="sxs-lookup"><span data-stu-id="7867a-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="7867a-121">Senarai harga mempunyai konteks **Jualan**.</span><span class="sxs-lookup"><span data-stu-id="7867a-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="7867a-122">Mata wang senarai harga sepadan dengan mata wang pelanggan.</span><span class="sxs-lookup"><span data-stu-id="7867a-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="7867a-123">Pada kontrak projek, perintah keutamaan berikut digunakan untuk menetapkan senarai harga projek yang berkaitan secara automatik:</span><span class="sxs-lookup"><span data-stu-id="7867a-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="7867a-124">Sebut Harga</span><span class="sxs-lookup"><span data-stu-id="7867a-124">Quote</span></span>
2. <span data-ttu-id="7867a-125">Peluang</span><span class="sxs-lookup"><span data-stu-id="7867a-125">Opportunity</span></span>
3. <span data-ttu-id="7867a-126">Pelanggan</span><span class="sxs-lookup"><span data-stu-id="7867a-126">Customer</span></span> 
4. <span data-ttu-id="7867a-127">Tetapan global</span><span class="sxs-lookup"><span data-stu-id="7867a-127">Global settings</span></span> 

<span data-ttu-id="7867a-128">Apabila senarai harga projek dimasukkan secara lalai, sistem mengesahkan bahawa mata wang sepadan dengan mata wang pelanggan dan senarai harga lalai yang telah dimasukkan mempunyai konteks **Jualan**.</span><span class="sxs-lookup"><span data-stu-id="7867a-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="7867a-129">Anda boleh mengaitkan senarai harga berbilang projek dengan entiti Pelanggan, Peluang, Sebut Harga dan Jualan Kontrak Projek.</span><span class="sxs-lookup"><span data-stu-id="7867a-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="7867a-130">Keupayaan ini menyokong harga lalai khusus masa untuk kontrak projek panjang, yang anda mungkin memerlukan lebih daripada satu senarai harga untuk akaun bagi kemas kini harga yang berlaku kerana inflasi.</span><span class="sxs-lookup"><span data-stu-id="7867a-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="7867a-131">Bagaimanapun, jika senarai harga yang anda kaitkan dengan entiti Pelanggan, Peluang, Sebut Harga atau Kontrak Projek mempunyai keberkesanan tarikh bertindan, harga lalai mungkin salah.</span><span class="sxs-lookup"><span data-stu-id="7867a-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="7867a-132">Oleh itu, anda perlu memastikan senarai harga projek yang mempunyai keberkesanan tarikh bertindan tidak dikaitkan dengan entiti tersebut.</span><span class="sxs-lookup"><span data-stu-id="7867a-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>
