---
title: Senarai harga produk
description: Topik ini menyediakan maklumat tentang senarai harga dalam penetapan harga katalog yang digunakan untuk sebut harga dan kontrak projek.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
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
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e37f0bf9eef946ab4ebd658cef4e1269cbaf686d
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877501"
---
# <a name="product-price-lists"></a><span data-ttu-id="c001b-103">Senarai harga produk</span><span class="sxs-lookup"><span data-stu-id="c001b-103">Product price lists</span></span>

<span data-ttu-id="c001b-104">_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_</span><span class="sxs-lookup"><span data-stu-id="c001b-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="c001b-105">Dalam Project Operations, **Senarai harga produk** dan entiti item senarai harga yang berkaitan menyokong kefungsian untuk penetapan harga produk pada sebut harga berdasarkan produk dan baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="c001b-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="c001b-106">Untuk produk yang digunakan pada projek, rekod item senarai harga untuk senarai harga projek digunakan.</span><span class="sxs-lookup"><span data-stu-id="c001b-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="c001b-107">Produk perlu disediakan supaya ia mempunyai kos lalai dan senarai harga dalam katalog produk.</span><span class="sxs-lookup"><span data-stu-id="c001b-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="c001b-108">Gunakan senarai harga, kos kos standard dan kos semasa untuk mengkonfigurasi kos lalai dan harga senarai.</span><span class="sxs-lookup"><span data-stu-id="c001b-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="c001b-109">Harga senarai lalai digunakan pada baris sebut harga atau baris kontrak projek hanya apabila sistem tidak dapat mencari baris senarai harga untuk produk tersebut dalam senarai harga produk untuk sebut harga atau kontrak projek.</span><span class="sxs-lookup"><span data-stu-id="c001b-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="c001b-110">Harga kos baris katalog produk boleh ditukar antara sebut harga.</span><span class="sxs-lookup"><span data-stu-id="c001b-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="c001b-111">Keupayaan ini penting kerana jika anda tidak menjejak kos dengan tepat, anda tidak boleh menentukan keuntungan operasi pada penglibatan projek.</span><span class="sxs-lookup"><span data-stu-id="c001b-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="c001b-112">Secara lalai, kos standard produk digunakan sebagai harga kos.</span><span class="sxs-lookup"><span data-stu-id="c001b-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="c001b-113">Walau bagaimanapun, harga kos lalai boleh dikemas kini pada baris sebut harga jika terdapat harga kos yang berbeza untuk sebut harga itu.</span><span class="sxs-lookup"><span data-stu-id="c001b-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="c001b-114">Item senarai harga</span><span class="sxs-lookup"><span data-stu-id="c001b-114">Price list items</span></span>

<span data-ttu-id="c001b-115">Anda boleh menambah produk daripada katalog produk kepada senarai harga yang berbeza.</span><span class="sxs-lookup"><span data-stu-id="c001b-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="c001b-116">Baris senarai harga untuk produk sentiasa merujuk kepada unit tertentu.</span><span class="sxs-lookup"><span data-stu-id="c001b-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="c001b-117">Penetapan harga untuk produk pada item senarai harga boleh dikonfigurasikan sebagai jumlah mata wang.</span><span class="sxs-lookup"><span data-stu-id="c001b-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="c001b-118">Sebagai alternatif, ia boleh dikonfigurasikan sebagai fungsi harga senarai, kos semasa, atau kos standard.</span><span class="sxs-lookup"><span data-stu-id="c001b-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="c001b-119">Kefungsian penetapan harga menyokong pelbagai pilihan pembundaran apabila harga produk dikonfigurasikan sebagai fungsi harga senarai, kos standard atau kos semasa.</span><span class="sxs-lookup"><span data-stu-id="c001b-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="c001b-120">Selain mengambil kesempatan daripada pelbagai kaedah penetapan harga dan pilihan pembundaran, anda boleh mengaitkan senarai diskaun dengan item senarai harga.</span><span class="sxs-lookup"><span data-stu-id="c001b-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="c001b-121">Senarai harga produk lalai</span><span class="sxs-lookup"><span data-stu-id="c001b-121">Default product price list</span></span>
<span data-ttu-id="c001b-122">Setiap rekod pelanggan mempunyai medan **Senarai Harga Lalai**, tempat anda boleh tentukan senarai harga yang sepadan dengan mata wang pelanggan.</span><span class="sxs-lookup"><span data-stu-id="c001b-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="c001b-123">Nilai lalai tidak dimasukkan secara automatik dalam medan ini.</span><span class="sxs-lookup"><span data-stu-id="c001b-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="c001b-124">Apabila perjanjian penetapan harga tersuai dengan pelanggan tertentu wujud, anda boleh menggunakan medan ini untuk mengaitkan senarai harga dengan pelanggan tersebut.</span><span class="sxs-lookup"><span data-stu-id="c001b-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="c001b-125">Entiti Peluang, Sebut Harga dan Kontrak Projek menggunakan pesanan berikut untuk memasukkan senarai harga produk lalai.</span><span class="sxs-lookup"><span data-stu-id="c001b-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="c001b-126">Pesanan yang sama digunakan untuk senarai harga projek.</span><span class="sxs-lookup"><span data-stu-id="c001b-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="c001b-127">Sebut Harga</span><span class="sxs-lookup"><span data-stu-id="c001b-127">Quote</span></span>
2.  <span data-ttu-id="c001b-128">Peluang</span><span class="sxs-lookup"><span data-stu-id="c001b-128">Opportunity</span></span>
3.  <span data-ttu-id="c001b-129">Pelanggan</span><span class="sxs-lookup"><span data-stu-id="c001b-129">Customer</span></span>
4.  <span data-ttu-id="c001b-130">Tetapan global</span><span class="sxs-lookup"><span data-stu-id="c001b-130">Global settings</span></span> 

<span data-ttu-id="c001b-131">Secara lalai, medan **Produk** pada baris sebut harga menyenaraikan semua produk aktif dalam senarai harga produk sebut harga.</span><span class="sxs-lookup"><span data-stu-id="c001b-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="c001b-132">Jika produk telah dinyahaktifkan atau jika ia merupakan produk draf, ia tidak disenaraikan, walaupun ia ada dalam senarai harga.</span><span class="sxs-lookup"><span data-stu-id="c001b-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="c001b-133">Baris katalog produk ditambahkan sebagai baris invois pada invois pertama yang dicipta untuk kontrak projek.</span><span class="sxs-lookup"><span data-stu-id="c001b-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="c001b-134">Pada invois draf, baris invois tersebut boleh dipadamkan.</span><span class="sxs-lookup"><span data-stu-id="c001b-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="c001b-135">Dalam kes tersebut, baris akan muncul pada invois berikutnya sehingga ia diinvoiskan atau sehingga invois dihantar kepada pelanggan.</span><span class="sxs-lookup"><span data-stu-id="c001b-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="c001b-136">Anda tidak boleh menginvoiskan sebahagian kuantiti baris invois produk.</span><span class="sxs-lookup"><span data-stu-id="c001b-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="c001b-137">Apabila baris produk daripada kontrak projek diinvoiskan, aktual dicipta.</span><span class="sxs-lookup"><span data-stu-id="c001b-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="c001b-138">Walau bagaimanapun, aktual tersebut tidak dipautkan kepada entiti projek berkaitan.</span><span class="sxs-lookup"><span data-stu-id="c001b-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="c001b-139">Dalam erti kata lain, baris kontrak projek berdasarkan produk adalah bebas daripada sebarang penggunaan berdasarkan projek.</span><span class="sxs-lookup"><span data-stu-id="c001b-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
