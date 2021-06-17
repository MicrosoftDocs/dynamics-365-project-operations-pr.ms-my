---
title: Baris sebut harga berdasarkan produk
description: Topik ini memberikan maklumat tentang baris sebut harga berdasarkan produk.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1bd789f4ee4d5b4603093be24aa25addafa9e8e8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998512"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="961fa-103">Baris sebut harga berdasarkan produk</span><span class="sxs-lookup"><span data-stu-id="961fa-103">Product-based quote lines</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="961fa-104">Anda boleh mencipta baris sebut harga berdasarkan produk dalam Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="961fa-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="961fa-105">Baris sebut harga berdasarkan produk boleh menjadi baris "tulis masuk" atau ia boleh menjadi item daripada katalog produk.</span><span class="sxs-lookup"><span data-stu-id="961fa-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="961fa-106">Katalog produk</span><span class="sxs-lookup"><span data-stu-id="961fa-106">Product catalog</span></span>

<span data-ttu-id="961fa-107">Produk dalam katalog produk Dynamics 365 mempunyai unit lalai dan kumpulan unit.</span><span class="sxs-lookup"><span data-stu-id="961fa-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="961fa-108">Jika beberapa produk berkongsi set atribut yang sama, anda boleh mencipta keluarga produk yang juga mempunyai atribut tersebut.</span><span class="sxs-lookup"><span data-stu-id="961fa-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="961fa-109">Semua produk dalam satu keluarga produk mewarisi set atribut yang sama.</span><span class="sxs-lookup"><span data-stu-id="961fa-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="961fa-110">Sebagai contoh, sebuah syarikat menjual lesen langganan untuk pelbagai perisian.</span><span class="sxs-lookup"><span data-stu-id="961fa-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="961fa-111">Semua perisian langganan mempunyai dua atribut berikut:</span><span class="sxs-lookup"><span data-stu-id="961fa-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="961fa-112">Bilangan pengguna</span><span class="sxs-lookup"><span data-stu-id="961fa-112">Number of users</span></span> 
- <span data-ttu-id="961fa-113">Tempoh langganan (dalam bulan)</span><span class="sxs-lookup"><span data-stu-id="961fa-113">Subscription duration (in months)</span></span>

<span data-ttu-id="961fa-114">Cara yang baik untuk mengekalkan jenis katalog ini adalah untuk mencipta keluarga produk yang dinamakan **Perisian Langganan** dan yang mempunyai **Bilangan pengguna** dan **Tempoh langganan** sebagai atribut.</span><span class="sxs-lookup"><span data-stu-id="961fa-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="961fa-115">Anda kemudian boleh menambah produk individu, seperti **Dynamics 365 Sales** atau **Dynamics 365 Field Service** kepada keluarga produk **Perisian Langganan**.</span><span class="sxs-lookup"><span data-stu-id="961fa-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="961fa-116">Menambahkan item katalog produk kepada sebut harga projek</span><span class="sxs-lookup"><span data-stu-id="961fa-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="961fa-117">Sebut harga projek dan halaman kontrak projek mempunyai bahagian untuk dua jenis baris: Baris berdasarkan projek dan baris berdasarkan produk.</span><span class="sxs-lookup"><span data-stu-id="961fa-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="961fa-118">Untuk baris berdasarkan produk, Dynamics 365 digunakan untuk menambah item daripada katalog produk kepada sebut harga.</span><span class="sxs-lookup"><span data-stu-id="961fa-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="961fa-119">Senarai ke bawah pada baris sebut harga atau baris kontrak projek menyertakan semua produk dan unit dalam senarai harga produk yang dilampirkan pada sebut harga atau kontrak projek.</span><span class="sxs-lookup"><span data-stu-id="961fa-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="961fa-120">Anda juga boleh menambah produk yang bukan sebahagian daripada senarai harga produk sebut harga.</span><span class="sxs-lookup"><span data-stu-id="961fa-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="961fa-121">Selain itu, anda boleh memilih produk daripada senarai harga lain atau anda boleh memilih produk secara langsung daripada katalog produk.</span><span class="sxs-lookup"><span data-stu-id="961fa-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="961fa-122">Apabila anda memilih produk secara langsung daripada katalog produk, senarai harga lalai produk tersebut digunakan untuk mendapatkan harga jualan produk tersebut.</span><span class="sxs-lookup"><span data-stu-id="961fa-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="961fa-123">Jika senarai harga lalai tidak ditetapkan, harga ditetapkan kepada 0 (sifar).</span><span class="sxs-lookup"><span data-stu-id="961fa-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="961fa-124">Jika baris sebut harga adalah berdasarkan katalog produk, anda boleh ganti harga jualan secara langsung pada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="961fa-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="961fa-125">Ambil perhatian bahawa baris sebut harga dalam Dynamics 365 mempunyai medan **Penetapan harga**.</span><span class="sxs-lookup"><span data-stu-id="961fa-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="961fa-126">Dua nilai tersedia:</span><span class="sxs-lookup"><span data-stu-id="961fa-126">Two values are available:</span></span>

- <span data-ttu-id="961fa-127">Ganti penetapan harga</span><span class="sxs-lookup"><span data-stu-id="961fa-127">Override pricing</span></span>  
- <span data-ttu-id="961fa-128">Gunakan lalai</span><span class="sxs-lookup"><span data-stu-id="961fa-128">Use default</span></span>

<span data-ttu-id="961fa-129">Jika anda menetapkan medan ini kepada **Ganti penetapan harga**, Dynamics 365 tidak menetapkan harga lalai.</span><span class="sxs-lookup"><span data-stu-id="961fa-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="961fa-130">Anda mesti masukkan harga untuk produk pada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="961fa-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="961fa-131">Jika anda menetapkan medan ini kepada **Gunakan lalai**, Dynamics 365 menggunakan harga jualan lalai dan mengunci medan tersebut untuk mengelakkan pengeditan.</span><span class="sxs-lookup"><span data-stu-id="961fa-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="961fa-132">Selepas anda memasang PSA, harga jualan lalai dimasukkan pada baris berdasarkan produk pada sebut harga.</span><span class="sxs-lookup"><span data-stu-id="961fa-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="961fa-133">Medan **Penetapan harga** kemudian ditetapkan kepada **Ganti penetapan harga** supaya anda boleh mengedit harga lalai pada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="961fa-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Menetapkan ganti penetapan harga](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="961fa-135">Faktor kuantiti bagi produk</span><span class="sxs-lookup"><span data-stu-id="961fa-135">Quantity factors for products</span></span>

<span data-ttu-id="961fa-136">PSA menggunakan faktor kuantiti untuk menyokong jualan produk berdasarkan langganan.</span><span class="sxs-lookup"><span data-stu-id="961fa-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="961fa-137">Untuk produk berdasarkan langganan, kuantiti pada sebut harga atau baris kontrak projek dinyatakan sebagai bilangan bulan pengguna.</span><span class="sxs-lookup"><span data-stu-id="961fa-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="961fa-138">Biasanya, harga perisian langganan disimpan dalam katalog sebagai harga bagi setiap pengguna setiap bulan.</span><span class="sxs-lookup"><span data-stu-id="961fa-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="961fa-139">Walau bagaimanapun, anda boleh menggunakan perihalan masa lain sebagai ganti.</span><span class="sxs-lookup"><span data-stu-id="961fa-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="961fa-140">Semasa proses jualan, harga pada baris sebut harga biasanya adalah harga bagi setiap pengguna, setiap bulan yang telah dirundingkan dan terdiskaun oleh ejen jualan IT.</span><span class="sxs-lookup"><span data-stu-id="961fa-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="961fa-141">Setiap urusan mempunyai bilangan pengguna yang berbeza dan bilangan bulan langganan yang berbeza.</span><span class="sxs-lookup"><span data-stu-id="961fa-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="961fa-142">Kuantiti yang digunakan untuk mengira jumlah baris sebut harga adalah produk bilangan pengguna dan bilangan bulan langganan.</span><span class="sxs-lookup"><span data-stu-id="961fa-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="961fa-143">Untuk menyokong jenis jualan ini, PSA memperkenalkan konsep faktor kuantiti.</span><span class="sxs-lookup"><span data-stu-id="961fa-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="961fa-144">Faktor kuantiti bergantung pada atribut produk dalam Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="961fa-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="961fa-145">Apabila anda mengkonfigurasikan sifat khusus untuk produk, PSA membolehkan anda menandakan subset sifat tersebut atau semua sifat tersebut, sebagai faktor kuantiti.</span><span class="sxs-lookup"><span data-stu-id="961fa-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="961fa-146">PSA mengesahkan bahawa hanya sifat angka atau sifat produk yang mempunyai jenis data berangka ditandakan sebagai faktor kuantiti.</span><span class="sxs-lookup"><span data-stu-id="961fa-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="961fa-147">Apabila produk yang faktor kuantiti dikonfigurasikan ditambah pada baris sebut harga, medan **Kuantiti** pada baris sebut harga akan menjadi medan baca sahaja.</span><span class="sxs-lookup"><span data-stu-id="961fa-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="961fa-148">Selepas anda memasukkan nilai untuk sifat produk yang merupakan faktor kuantiti, PSA mengira kuantiti baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="961fa-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="961fa-149">Sebagai contoh, Dynamics 365 mungkin mempunyai sifat berikut:</span><span class="sxs-lookup"><span data-stu-id="961fa-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="961fa-150">**Bilangan pengguna** - Bilangan pengguna</span><span class="sxs-lookup"><span data-stu-id="961fa-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="961fa-151">**Bilangan bulan** – Bilangan bulan langganan</span><span class="sxs-lookup"><span data-stu-id="961fa-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="961fa-152">**SKU Produk**</span><span class="sxs-lookup"><span data-stu-id="961fa-152">**Product SKU**</span></span> 

<span data-ttu-id="961fa-153">Sifat **Bilangan Pengguna** dan **Bilangan Bulan** boleh ditandakan sebagai faktor kuantiti dengan mengedit sifat baris produk.</span><span class="sxs-lookup"><span data-stu-id="961fa-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Menandakan Bilangan Pengguna dan Bilangan Bulan sebagai faktor kualiti](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]