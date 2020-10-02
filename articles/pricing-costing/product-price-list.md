---
title: Senarai harga produk
description: Topik ini menyediakan maklumat tentang senarai harga dalam penetapan harga katalog yang digunakan untuk sebut harga dan kontrak projek.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 3570aeb78804e9b267caa55a27e02d6c8df9a5c6
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898182"
---
# <a name="product-price-lists"></a><span data-ttu-id="85b2e-103">Senarai harga produk</span><span class="sxs-lookup"><span data-stu-id="85b2e-103">Product price lists</span></span>

<span data-ttu-id="85b2e-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="85b2e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="85b2e-105">Senarai harga dan entiti item senarai harga menyokong penetapan harga katalog produk.</span><span class="sxs-lookup"><span data-stu-id="85b2e-105">Price lists and price list item entities support product catalog pricing.</span></span> <span data-ttu-id="85b2e-106">Bagi sebahagian besar, fungsi ini digunakan untuk baris berdasarkan katalog pada sebut harga projek dan kontrak projek.</span><span class="sxs-lookup"><span data-stu-id="85b2e-106">For the most part, this functionality is used for catalog-based lines on project quotes and project contracts.</span></span>

<span data-ttu-id="85b2e-107">Bagi baris berdasarkan projek, kontrak mewakili urusan selepas ia dimenangi.</span><span class="sxs-lookup"><span data-stu-id="85b2e-107">For project-based lines, a contract represents the deal after it was won.</span></span> <span data-ttu-id="85b2e-108">Oleh sebab proses rundingan biasanya mendahului kemenangan tersebut, harga yang dilampirkan pada sebut harga sentiasa disalin seadanya pada senarai harga baharu dan dilampirkan pada kontrak.</span><span class="sxs-lookup"><span data-stu-id="85b2e-108">Because the process of negotiation usually precedes the win, the pricing that is attached to the quote is always copied as-is to a new price list and attached to the contract.</span></span> <span data-ttu-id="85b2e-109">Senarai harga baharu ini tidak boleh ditukar di luar skop kontrak.</span><span class="sxs-lookup"><span data-stu-id="85b2e-109">This new price list can't be changed outside the scope of the contract.</span></span> <span data-ttu-id="85b2e-110">Pengehadan ini membantu melindungi kad kadar yang telah dirunding daripada sebarang perubahan harga yang berlaku dalam senarai harga induk.</span><span class="sxs-lookup"><span data-stu-id="85b2e-110">This limitation helps protect the rate card that was negotiated from any price changes that occur in the master price list.</span></span>

<span data-ttu-id="85b2e-111">Produk perlu disediakan supaya ia mempunyai kos lalai dan senarai harga dalam katalog produk.</span><span class="sxs-lookup"><span data-stu-id="85b2e-111">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="85b2e-112">Gunakan senarai harga, kos kos standard dan kos semasa untuk mengkonfigurasi kos lalai dan harga senarai.</span><span class="sxs-lookup"><span data-stu-id="85b2e-112">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="85b2e-113">Harga senarai lalai digunakan pada baris sebut harga atau baris kontrak projek hanya apabila sistem tidak dapat mencari baris senarai harga untuk produk tersebut dalam senarai harga produk untuk sebut harga atau kontrak projek.</span><span class="sxs-lookup"><span data-stu-id="85b2e-113">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="85b2e-114">Harga kos baris katalog produk boleh ditukar antara sebut harga.</span><span class="sxs-lookup"><span data-stu-id="85b2e-114">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="85b2e-115">Keupayaan ini penting kerana jika anda tidak menjejak kos dengan tepat, anda tidak boleh menentukan keuntungan operasi pada penglibatan projek.</span><span class="sxs-lookup"><span data-stu-id="85b2e-115">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="85b2e-116">Secara lalai, kos standard produk digunakan sebagai harga kos.</span><span class="sxs-lookup"><span data-stu-id="85b2e-116">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="85b2e-117">Walau bagaimanapun, harga kos lalai boleh dikemas kini pada baris sebut harga jika terdapat harga kos yang berbeza untuk sebut harga itu.</span><span class="sxs-lookup"><span data-stu-id="85b2e-117">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="85b2e-118">Item senarai harga</span><span class="sxs-lookup"><span data-stu-id="85b2e-118">Price list items</span></span>

<span data-ttu-id="85b2e-119">Anda boleh menambah produk daripada katalog produk kepada senarai harga yang berbeza.</span><span class="sxs-lookup"><span data-stu-id="85b2e-119">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="85b2e-120">Baris senarai harga untuk produk sentiasa merujuk kepada unit tertentu.</span><span class="sxs-lookup"><span data-stu-id="85b2e-120">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="85b2e-121">Penetapan harga untuk produk pada item senarai harga boleh dikonfigurasikan sebagai jumlah mata wang.</span><span class="sxs-lookup"><span data-stu-id="85b2e-121">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="85b2e-122">Sebagai alternatif, ia boleh dikonfigurasikan sebagai fungsi harga senarai, kos semasa, atau kos standard.</span><span class="sxs-lookup"><span data-stu-id="85b2e-122">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="85b2e-123">PSA menyokong pelbagai pilihan pembundaran apabila harga dikonfigurasikan sebagai fungsi harga senarai, kos standard atau kos semasa.</span><span class="sxs-lookup"><span data-stu-id="85b2e-123">PSA supports various rounding options when prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="85b2e-124">Selain mengambil kesempatan daripada pelbagai kaedah penetapan harga dan pilihan pembundaran, anda boleh mengaitkan senarai diskaun dengan item senarai harga.</span><span class="sxs-lookup"><span data-stu-id="85b2e-124">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

<span data-ttu-id="85b2e-125">Apabila anda mencipta senarai harga tersuai baharu untuk sebut harga dengan memilih **Cipta Penetapan Harga Tersuai** pada halaman **Sebut Harga Projek**, salinan senarai harga dibuat dan medan **Entiti** pada pengepala senarai harga baharu ditetapkan kepada **Entiti Jualan**.</span><span class="sxs-lookup"><span data-stu-id="85b2e-125">When you create a new custom price list for a quote by selecting **Create Custom Pricing** on the **Project Quote** page, a copy of the price list is made, and the **Entity** field on the header of the new price list is set to **Sales Entity**.</span></span> <span data-ttu-id="85b2e-126">Nama senarai harga baharu akan ditambah dengan nama sebut harga dan cap masa.</span><span class="sxs-lookup"><span data-stu-id="85b2e-126">The name of the new price list is appended with the name of the quote and a timestamp.</span></span> <span data-ttu-id="85b2e-127">Anda juga boleh menggunakan nama senarai harga baharu dan nama sebut harga dalam aliran kerja tersuai untuk mencetuskan semakan tambahan dan kelulusan untuk sebut harga yang menggunakan penetapan harga tersuai.</span><span class="sxs-lookup"><span data-stu-id="85b2e-127">You also can use the name of the new price list and the name of the quote in custom workflows to trigger additional review and approvals for quotes that use custom pricing.</span></span>

 
## <a name="default-product-price-list"></a><span data-ttu-id="85b2e-128">Senarai harga produk lalai</span><span class="sxs-lookup"><span data-stu-id="85b2e-128">Default product price list</span></span>
<span data-ttu-id="85b2e-129">Setiap rekod pelanggan mempunyai medan **Senarai Harga Lalai**, tempat anda boleh tentukan senarai harga yang sepadan dengan mata wang pelanggan.</span><span class="sxs-lookup"><span data-stu-id="85b2e-129">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="85b2e-130">Nilai lalai tidak dimasukkan secara automatik dalam medan ini.</span><span class="sxs-lookup"><span data-stu-id="85b2e-130">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="85b2e-131">Apabila perjanjian penetapan harga tersuai dengan pelanggan tertentu wujud, anda boleh menggunakan medan ini untuk mengaitkan senarai harga dengan pelanggan tersebut.</span><span class="sxs-lookup"><span data-stu-id="85b2e-131">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="85b2e-132">Entiti Peluang, Sebut Harga dan Kontrak Projek menggunakan pesanan berikut untuk memasukkan senarai harga produk lalai.</span><span class="sxs-lookup"><span data-stu-id="85b2e-132">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="85b2e-133">Pesanan yang sama digunakan untuk senarai harga projek.</span><span class="sxs-lookup"><span data-stu-id="85b2e-133">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="85b2e-134">Sebut Harga</span><span class="sxs-lookup"><span data-stu-id="85b2e-134">Quote</span></span>
2.  <span data-ttu-id="85b2e-135">Peluang</span><span class="sxs-lookup"><span data-stu-id="85b2e-135">Opportunity</span></span>
3.  <span data-ttu-id="85b2e-136">Pelanggan</span><span class="sxs-lookup"><span data-stu-id="85b2e-136">Customer</span></span>
4.  <span data-ttu-id="85b2e-137">Tetapan global</span><span class="sxs-lookup"><span data-stu-id="85b2e-137">Global settings</span></span> 

<span data-ttu-id="85b2e-138">Secara lalai, medan **Produk** pada baris sebut harga menyenaraikan semua produk aktif dalam senarai harga produk sebut harga.</span><span class="sxs-lookup"><span data-stu-id="85b2e-138">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="85b2e-139">Jika produk telah dinyahaktifkan atau jika ia merupakan produk draf, ia tidak disenaraikan, walaupun ia ada dalam senarai harga.</span><span class="sxs-lookup"><span data-stu-id="85b2e-139">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="85b2e-140">Baris katalog produk ditambahkan sebagai baris invois pada invois pertama yang dicipta untuk kontrak projek.</span><span class="sxs-lookup"><span data-stu-id="85b2e-140">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="85b2e-141">Pada invois draf, baris invois tersebut boleh dipadamkan.</span><span class="sxs-lookup"><span data-stu-id="85b2e-141">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="85b2e-142">Dalam kes tersebut, baris akan muncul pada invois berikutnya sehingga ia diinvoiskan atau sehingga invois dihantar kepada pelanggan.</span><span class="sxs-lookup"><span data-stu-id="85b2e-142">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="85b2e-143">Anda tidak boleh menginvoiskan sebahagian kuantiti baris invois produk.</span><span class="sxs-lookup"><span data-stu-id="85b2e-143">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="85b2e-144">Apabila baris produk daripada kontrak projek diinvoiskan, aktual dicipta.</span><span class="sxs-lookup"><span data-stu-id="85b2e-144">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="85b2e-145">Walau bagaimanapun, aktual tersebut tidak dipautkan kepada entiti projek berkaitan.</span><span class="sxs-lookup"><span data-stu-id="85b2e-145">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="85b2e-146">Dalam erti kata lain, baris kontrak projek berdasarkan produk adalah bebas daripada sebarang penggunaan berdasarkan projek.</span><span class="sxs-lookup"><span data-stu-id="85b2e-146">In other words, product-based project contract lines are independent of any project-based use.</span></span> <span data-ttu-id="85b2e-147">Penggunaan bahan pada projek tidak dijejak.</span><span class="sxs-lookup"><span data-stu-id="85b2e-147">Material consumption on projects isn't tracked.</span></span>