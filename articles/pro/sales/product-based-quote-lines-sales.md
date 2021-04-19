---
title: Gambaran keseluruhan baris sebut harga berasaskan produk - lite
description: Topik ini menyediakan maklumat tentang bekerja dengan baris sebut harga berasaskan produk.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29d82637c6c8bb5b5cde7707d181d5b3d3b235c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272579"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="0bc88-103">Gambaran keseluruhan baris sebut harga berasaskan produk - lite</span><span class="sxs-lookup"><span data-stu-id="0bc88-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="0bc88-104">_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_</span><span class="sxs-lookup"><span data-stu-id="0bc88-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0bc88-105">Anda boleh mencipta baris sebut harga berdasarkan produk dalam Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="0bc88-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="0bc88-106">Baris sebut harga berasaskan produk boleh ditambah secara manual atau boleh menjadi item daripada katalog produk.</span><span class="sxs-lookup"><span data-stu-id="0bc88-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="0bc88-107">Katalog produk</span><span class="sxs-lookup"><span data-stu-id="0bc88-107">Product catalog</span></span>

<span data-ttu-id="0bc88-108">Setiap produk dalam katalog produk mempunyai unit dan kumpulan unit lalai.</span><span class="sxs-lookup"><span data-stu-id="0bc88-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="0bc88-109">Jika berbilang produk berkongsi set atribut yang sama, anda boleh mencipta keluarga produk yang berkongsi atribut itu.</span><span class="sxs-lookup"><span data-stu-id="0bc88-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="0bc88-110">Contohnya, sebuah syarikat menjual lesen langganan untuk pelbagai jenis perisian.</span><span class="sxs-lookup"><span data-stu-id="0bc88-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="0bc88-111">Semua perisian langganan mempunyai dua atribut berikut:</span><span class="sxs-lookup"><span data-stu-id="0bc88-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="0bc88-112">Bilangan pengguna</span><span class="sxs-lookup"><span data-stu-id="0bc88-112">Number of users</span></span>
- <span data-ttu-id="0bc88-113">Tempoh langganan diukur dalam bulan</span><span class="sxs-lookup"><span data-stu-id="0bc88-113">A subscription duration measured in months</span></span>

<span data-ttu-id="0bc88-114">Untuk mengekalkan jenis katalog ini, cipta keluarga produk bernama **Perisian Langganan** dan tambah bilangan pengguna dan tempoh langganan sebagai atribut.</span><span class="sxs-lookup"><span data-stu-id="0bc88-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="0bc88-115">Seterusnya, anda boleh menambah produk individu kepada keluarga produk **Perisian Langganan**.</span><span class="sxs-lookup"><span data-stu-id="0bc88-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="0bc88-116">Tambah item katalog produk kepada sebut harga projek</span><span class="sxs-lookup"><span data-stu-id="0bc88-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="0bc88-117">Halaman **Sebut Harga Projek** dan **Kontrak Projek** mempunyai bahagian untuk baris berasaskan projek dan baris berasaskan produk.</span><span class="sxs-lookup"><span data-stu-id="0bc88-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="0bc88-118">Untuk baris berasaskan produk, senarai juntai bawah pada baris sebut harga atau baris kontrak projek termasuk semua produk dan unit dalam senarai harga produk.</span><span class="sxs-lookup"><span data-stu-id="0bc88-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="0bc88-119">Anda juga boleh menambah produk yang bukan sebahagian daripada senarai harga produk.</span><span class="sxs-lookup"><span data-stu-id="0bc88-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="0bc88-120">Selain itu, anda boleh memilih produk daripada senarai harga yang lain atau secara langsung daripada katalog produk.</span><span class="sxs-lookup"><span data-stu-id="0bc88-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="0bc88-121">Apabila anda memilih produk secara langsung daripada katalog produk, senarai harga lalai produk tersebut digunakan untuk mendapatkan harga jualan produk tersebut.</span><span class="sxs-lookup"><span data-stu-id="0bc88-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="0bc88-122">Jika senarai harga lalai tidak ditetapkan, harga ditetapkan kepada sifar (0).</span><span class="sxs-lookup"><span data-stu-id="0bc88-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="0bc88-123">Apabila baris sebut harga adalah berasaskan pada katalog produk, anda boleh mengganti harga jualan secara langsung pada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="0bc88-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="0bc88-124">Baris sebut harga dalam medan **Penetapan harga** dengan dua nilai tersedia:</span><span class="sxs-lookup"><span data-stu-id="0bc88-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="0bc88-125">**Ganti Penetapan harga**</span><span class="sxs-lookup"><span data-stu-id="0bc88-125">**Override Pricing**</span></span>
- <span data-ttu-id="0bc88-126">**Gunakan Lalai**</span><span class="sxs-lookup"><span data-stu-id="0bc88-126">**Use Default**</span></span>

<span data-ttu-id="0bc88-127">Jika anda memilih **Ganti Penetapan Harga**, harga lalai tidak ditetapkan.</span><span class="sxs-lookup"><span data-stu-id="0bc88-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="0bc88-128">Sebaliknya, anda mesti masukkan harga untuk produk pada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="0bc88-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="0bc88-129">Jika anda memilih **Gunakan Lalai**, harga jualan lalai digunakan dan medan dikunci untuk pengeditan.</span><span class="sxs-lookup"><span data-stu-id="0bc88-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="0bc88-130">Harga jualan lalai dimasukkan pada baris berasaskan produk sebut harga.</span><span class="sxs-lookup"><span data-stu-id="0bc88-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="0bc88-131">Medan **Penetapan harga** kemudian ditetapkan kepada **Ganti Penetapan harga** supaya anda boleh mengedit harga lalai pada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="0bc88-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="0bc88-132">Ini adalah Project Operations ganti khusus untuk tingkah laku berasaskan produk dalam Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="0bc88-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]