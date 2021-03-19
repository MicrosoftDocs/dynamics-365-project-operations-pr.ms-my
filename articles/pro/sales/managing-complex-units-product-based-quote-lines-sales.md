---
title: Mengurus unit kompleks seperti mengikut setiap pengguna, setiap bulan untuk baris sebut harga berasaskan produk - lite
description: Topik ini menyediakan maklumat tentang mengurus unit kompleks untuk baris sebut harga berasaskan projek.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b4a075ae5a7329f241cc31afceab0e085c771f72
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272894"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a><span data-ttu-id="53b4a-103">Mengurus unit kompleks seperti mengikut setiap pengguna, setiap bulan untuk baris sebut harga berasaskan produk - lite</span><span class="sxs-lookup"><span data-stu-id="53b4a-103">Managing complex units such as per-user, per-month for product-based quote lines - lite</span></span>

<span data-ttu-id="53b4a-104">_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_</span><span class="sxs-lookup"><span data-stu-id="53b4a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="53b4a-105">Dynamics 365 Project Operations menggunakan faktor kuantiti untuk menyokong jualan produk berdasarkan langganan.</span><span class="sxs-lookup"><span data-stu-id="53b4a-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="53b4a-106">Untuk produk berasaskan langganan, kuantiti pada sebut harga atau baris kontrak projek dinyatakan sebagai bilangan bulan pengguna.</span><span class="sxs-lookup"><span data-stu-id="53b4a-106">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="53b4a-107">Biasanya, harga perisian langganan disimpan dalam katalog sebagai harga bagi setiap pengguna setiap bulan.</span><span class="sxs-lookup"><span data-stu-id="53b4a-107">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="53b4a-108">Semasa proses jualan, harga pada baris sebut harga biasanya adalah harga bagi setiap pengguna, setiap bulan yang telah dirundingkan dan terdiskaun oleh ejen jualan IT.</span><span class="sxs-lookup"><span data-stu-id="53b4a-108">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="53b4a-109">Setiap urusan mempunyai bilangan pengguna yang berbeza dan bilangan bulan langganan yang berbeza.</span><span class="sxs-lookup"><span data-stu-id="53b4a-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="53b4a-110">Kuantiti yang digunakan untuk mengira baris sebut harga adalah produk bilangan pengguna dan bilangan bulan langganan.</span><span class="sxs-lookup"><span data-stu-id="53b4a-110">The quantity used to compute the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="53b4a-111">Untuk menyokong jenis jualan ini, Project Operations memperkenalkan konsep faktor kuantiti.</span><span class="sxs-lookup"><span data-stu-id="53b4a-111">To support this type of sale, Project Operations introduced the concept of quantity factors.</span></span> <span data-ttu-id="53b4a-112">Faktor kuantiti bergantung pada atribut produk dalam Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="53b4a-112">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="53b4a-113">Apabila anda mengkonfigurasi sifat khusus untuk produk, Project Operations membolehkan anda menandakan subset atau semua sifat tersebut, sebagai faktor kuantiti.</span><span class="sxs-lookup"><span data-stu-id="53b4a-113">When you configure specific properties for a product, Project Operations lets you flag a subset, or all of the properties, as quantity factors.</span></span>

<span data-ttu-id="53b4a-114">Project Operations mengesahkan bahawa hanya sifat angka atau sifat produk yang mempunyai jenis data berangka ditandakan sebagai faktor kuantiti.</span><span class="sxs-lookup"><span data-stu-id="53b4a-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="53b4a-115">Apabila anda menambah produk dengan faktor kuantiti pada baris sebut harga, medan **Kuantiti** menjadi baca sahaja.</span><span class="sxs-lookup"><span data-stu-id="53b4a-115">When you add a product with quantity factors to a quote line, the **Quantity** field becomes read-only.</span></span> <span data-ttu-id="53b4a-116">Selepas anda memasukkan nilai untuk sifat produk yang merupakan faktor kuantiti, Project Operations mengira kuantiti baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="53b4a-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the quote line.</span></span>

<span data-ttu-id="53b4a-117">Contohnya, Dynamics 365 Sales mungkin mempunyai sifat berikut:</span><span class="sxs-lookup"><span data-stu-id="53b4a-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="53b4a-118">**Bilangan pengguna**: Bilangan pengguna</span><span class="sxs-lookup"><span data-stu-id="53b4a-118">**No of users**: The number of users</span></span>
- <span data-ttu-id="53b4a-119">**Bilangan bulan**: Bilangan bulan langganan</span><span class="sxs-lookup"><span data-stu-id="53b4a-119">**No of Months**: The number of subscription months</span></span>
- <span data-ttu-id="53b4a-120">**SKU Produk**</span><span class="sxs-lookup"><span data-stu-id="53b4a-120">**Product SKU**</span></span>

<span data-ttu-id="53b4a-121">Anda boleh menandakan sifat **Bilangan Pengguna** dan **Bilangan Bulan** sebagai faktor kuantiti dengan mengedit sifat baris produk.</span><span class="sxs-lookup"><span data-stu-id="53b4a-121">You can flag the **No of Users** and **No of Months** properties as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="53b4a-122">Untuk mencipta faktor Kuantiti daripada sifat Produk, ikuti langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="53b4a-122">To create Quantity factors from Product properties, follow these steps:</span></span>

1. <span data-ttu-id="53b4a-123">Pada tetingkap navigasi kiri Project Operations, pergi ke **Jualan** > **Produk**.</span><span class="sxs-lookup"><span data-stu-id="53b4a-123">On the Project Operations left navigation pane, go to **Sales** > **Products**.</span></span>
2. <span data-ttu-id="53b4a-124">Buka produk yang anda perlukan untuk mengkonfigurasi faktor kuantiti.</span><span class="sxs-lookup"><span data-stu-id="53b4a-124">Open the product for which you need to configure quantity factors.</span></span> <span data-ttu-id="53b4a-125">Pastikan produk mempunyai sifat yang telah pun dikonfigurasi.</span><span class="sxs-lookup"><span data-stu-id="53b4a-125">Make sure the product has properties already configured.</span></span>
3. <span data-ttu-id="53b4a-126">Pada halaman **Maklumat Projek** untuk Produk, pilih tab **Faktor Kuantiti**.</span><span class="sxs-lookup"><span data-stu-id="53b4a-126">On the **Project Information** page for the Product, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="53b4a-127">Dalam subgrid, pilih **+ Pengiraan medan baharu**.</span><span class="sxs-lookup"><span data-stu-id="53b4a-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="53b4a-128">Masukkan nama faktor Kuantiti dan pilih nilai sifat yang dipetakan kepada pengiraan medan.</span><span class="sxs-lookup"><span data-stu-id="53b4a-128">Enter the name of the Quantity factor and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="53b4a-129">Simpan dan tutup borang.</span><span class="sxs-lookup"><span data-stu-id="53b4a-129">Save and close the form.</span></span> <span data-ttu-id="53b4a-130">Ulangi langkah ini untuk semua sifat yang digunakan untuk pengkomputeran kuantiti untuk baris sebut harga berasaskan produk.</span><span class="sxs-lookup"><span data-stu-id="53b4a-130">Repeat these steps for all properties to use for computing the quantity for the product-based quote line.</span></span>

<span data-ttu-id="53b4a-131">Apabila anda mencipta baris sebut harga berasaskan produk untuk produk, kuantiti baris sebut harga akan dikunci.</span><span class="sxs-lookup"><span data-stu-id="53b4a-131">When you create a product-based quote line for a product, the quantity of the quote line will be locked.</span></span> <span data-ttu-id="53b4a-132">Kuantiti akan dikira sebagai produk nilai sifat yang anda masukkan untuk baris sebut harga tersebut.</span><span class="sxs-lookup"><span data-stu-id="53b4a-132">The quantity will be computed as a product of the property values that you input for that quote line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]