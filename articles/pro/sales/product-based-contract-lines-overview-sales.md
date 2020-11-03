---
title: Gambaran keseluruhan baris kontrak berdasarkan produk
description: Topik ini memberikan maklumat tentang baris kontrak berdasarkan produk.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 794a80b0dd6b8717b43e712b96b9ac077517c226
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081155"
---
# <a name="product-based-contract-lines-overview"></a><span data-ttu-id="452e5-103">Gambaran keseluruhan baris kontrak berdasarkan produk</span><span class="sxs-lookup"><span data-stu-id="452e5-103">Product-based contract lines overview</span></span>

<span data-ttu-id="452e5-104">_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_</span><span class="sxs-lookup"><span data-stu-id="452e5-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="452e5-105">Anda boleh mencipta baris kontrak berdasarkan produk dalam Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="452e5-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="452e5-106">Baris kontrak berdasarkan produk boleh dicipta baris secara manual, atau ia boleh menjadi item daripada katalog produk.</span><span class="sxs-lookup"><span data-stu-id="452e5-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="452e5-107">Katalog produk</span><span class="sxs-lookup"><span data-stu-id="452e5-107">Product catalog</span></span>

<span data-ttu-id="452e5-108">Produk dalam katalog produk mempunyai unit lalai dan kumpulan unit.</span><span class="sxs-lookup"><span data-stu-id="452e5-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="452e5-109">Jika beberapa produk berkongsi set atribut yang sama, anda boleh mencipta keluarga produk yang juga mempunyai atribut tersebut.</span><span class="sxs-lookup"><span data-stu-id="452e5-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="452e5-110">Semua produk dalam satu keluarga produk mewarisi set atribut yang sama.</span><span class="sxs-lookup"><span data-stu-id="452e5-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="452e5-111">Contohnya, sebuah syarikat menjual lesen langganan untuk pelbagai jenis perisian.</span><span class="sxs-lookup"><span data-stu-id="452e5-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="452e5-112">Semua perisian langganan mempunyai dua atribut berikut:</span><span class="sxs-lookup"><span data-stu-id="452e5-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="452e5-113">Bilangan pengguna</span><span class="sxs-lookup"><span data-stu-id="452e5-113">Number of users</span></span>
- <span data-ttu-id="452e5-114">Tempoh langganan (dalam bulan)</span><span class="sxs-lookup"><span data-stu-id="452e5-114">Subscription duration (in months)</span></span>

<span data-ttu-id="452e5-115">Untuk mengekalkan jenis katalog ini, cipta keluarga produk yang dinamakan **Perisian Langganan**.</span><span class="sxs-lookup"><span data-stu-id="452e5-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="452e5-116">Tambah atribut, **Bilangan pengguna** dan **Tempoh langganan** kepada keluarga produk.</span><span class="sxs-lookup"><span data-stu-id="452e5-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="452e5-117">Kemudian, tambah produk individu ke keluarga produk **Perisian Langganan**.</span><span class="sxs-lookup"><span data-stu-id="452e5-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="452e5-118">Tambah item katalog produk ke Kontrak projek</span><span class="sxs-lookup"><span data-stu-id="452e5-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="452e5-119">Kontrak projek mempunyai bahagian untuk dua jenis baris, berdasarkan projek dan berdasarkan produk.</span><span class="sxs-lookup"><span data-stu-id="452e5-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="452e5-120">Baris berdasarkan produk termasuk semua produk dan unit dalam senarai harga produk pada kontrak.</span><span class="sxs-lookup"><span data-stu-id="452e5-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="452e5-121">Produk yang bukan merupakan sebahagian daripada senarai harga produk kontrak boleh ditambahkan.</span><span class="sxs-lookup"><span data-stu-id="452e5-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="452e5-122">Anda boleh memilih produk daripada senarai harga lain, atau secara langsung daripada katalog produk.</span><span class="sxs-lookup"><span data-stu-id="452e5-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="452e5-123">Apabila anda memilih produk secara langsung daripada katalog produk, senarai harga lalai produk tersebut digunakan untuk harga jualan produk.</span><span class="sxs-lookup"><span data-stu-id="452e5-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="452e5-124">Jika senarai harga lalai tidak ditetapkan, harga ditetapkan kepada 0 (sifar).</span><span class="sxs-lookup"><span data-stu-id="452e5-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="452e5-125">Jika baris kontrak adalah berdasarkan pada katalog produk, anda boleh ganti harga jualan secara langsung pada baris.</span><span class="sxs-lookup"><span data-stu-id="452e5-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="452e5-126">Baris kontrak mempunyai medan **Harga** dengan dua nilai:</span><span class="sxs-lookup"><span data-stu-id="452e5-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="452e5-127">**Ganti penetapan harga**</span><span class="sxs-lookup"><span data-stu-id="452e5-127">**Override pricing**</span></span>
- <span data-ttu-id="452e5-128">**Gunakan lalai**</span><span class="sxs-lookup"><span data-stu-id="452e5-128">**Use default**</span></span>

<span data-ttu-id="452e5-129">Jika anda menetapkan medan **Harga** kepada **Harga ganti** , harga lalai tidak ditetapkan.</span><span class="sxs-lookup"><span data-stu-id="452e5-129">If you set the **Pricing** field to **Override pricing** , the default price isn't set.</span></span> <span data-ttu-id="452e5-130">Masukkan harga untuk produk pada baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="452e5-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="452e5-131">Jika anda menetapkan medan kepada **Gunakan lalai** , harga jualan lalai digunakan dan medan tidak boleh diedit.</span><span class="sxs-lookup"><span data-stu-id="452e5-131">If you set the field to **Use default** , the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="452e5-132">Selepas anda memasang Project Operations, harga jualan lalai dimasukkan pada baris berdasarkan produk pada kontrak.</span><span class="sxs-lookup"><span data-stu-id="452e5-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="452e5-133">Medan **Harga** ditetapkan kepada **Ganti harga** supaya anda boleh mengedit harga lalai pada baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="452e5-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="452e5-134">Ini adalah ganti khusus Project Operations kepada tingkah laku baris berdasarkan produk dalam Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="452e5-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>
