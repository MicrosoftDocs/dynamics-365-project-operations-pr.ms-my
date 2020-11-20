---
title: Urus unit kompleks untuk baris kontrak berdasarkan produk - lite
description: Topik ini memberikan maklumat mengenai menyokong jualan produk berasaskan langganan.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a58a13c8186f36e6031fe3c6f3c3a57ea920ac9e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177387"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="1ebaa-103">Urus unit kompleks untuk baris kontrak berdasarkan produk - lite</span><span class="sxs-lookup"><span data-stu-id="1ebaa-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="1ebaa-104">_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_</span><span class="sxs-lookup"><span data-stu-id="1ebaa-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1ebaa-105">Dynamics 365 Project Operations menggunakan faktor kuantiti untuk menyokong jualan produk berasaskan langganan.</span><span class="sxs-lookup"><span data-stu-id="1ebaa-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="1ebaa-106">Untuk produk berdasarkan langganan, kuantiti pada kontrak atau baris kontrak projek dinyatakan sebagai bilangan bulan pengguna.</span><span class="sxs-lookup"><span data-stu-id="1ebaa-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="1ebaa-107">Harga perisian langganan disimpan dalam katalog sebagai harga bagi setiap pengguna setiap bulan.</span><span class="sxs-lookup"><span data-stu-id="1ebaa-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="1ebaa-108">Semasa proses jualan, harga pada baris kontrak biasanya adalah harga bagi setiap pengguna, setiap bulan yang telah dirundingkan dan terdiskaun oleh ejen jualan.</span><span class="sxs-lookup"><span data-stu-id="1ebaa-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="1ebaa-109">Setiap urusan mempunyai bilangan pengguna yang berbeza dan bilangan bulan langganan yang berbeza.</span><span class="sxs-lookup"><span data-stu-id="1ebaa-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="1ebaa-110">Kuantiti yang digunakan untuk mengira jumlah baris kontrak adalah produk bilangan pengguna dan bilangan bulan langganan.</span><span class="sxs-lookup"><span data-stu-id="1ebaa-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="1ebaa-111">Untuk menyokong jenis jualan ini, Project Operations menyokong konsep *faktor kuantiti*.</span><span class="sxs-lookup"><span data-stu-id="1ebaa-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="1ebaa-112">Faktor kuantiti bergantung pada atribut produk.</span><span class="sxs-lookup"><span data-stu-id="1ebaa-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="1ebaa-113">Apabila anda mengkonfigurasikan sifat khusus untuk produk, anda boleh menandakan subset sifat itu atau semua sifat itu, sebagai faktor kuantiti.</span><span class="sxs-lookup"><span data-stu-id="1ebaa-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="1ebaa-114">Project Operations mengesahkan bahawa hanya sifat angka atau sifat produk yang mempunyai jenis data berangka ditandakan sebagai faktor kuantiti.</span><span class="sxs-lookup"><span data-stu-id="1ebaa-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="1ebaa-115">Apabila produk yang mempunyai faktor kuantiti yang dikonfigurasikan ditambah pada baris kontrak, medan **Kuantiti** menjadi baca sahaja.</span><span class="sxs-lookup"><span data-stu-id="1ebaa-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="1ebaa-116">Selepas anda memasukkan nilai untuk sifat produk yang merupakan faktor kuantiti, Project Operations mengira kuantiti baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="1ebaa-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="1ebaa-117">Contohnya, Dynamics 365 Sales mungkin mempunyai sifat berikut:</span><span class="sxs-lookup"><span data-stu-id="1ebaa-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="1ebaa-118">**Bilangan pengguna**: Bilangan pengguna.</span><span class="sxs-lookup"><span data-stu-id="1ebaa-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="1ebaa-119">**Bilangan Bulan**: Bilangan bulan langganan.</span><span class="sxs-lookup"><span data-stu-id="1ebaa-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="1ebaa-120">**Produk SKU**: Unit penyimpanan stok (SKU) untuk produk tersebut.</span><span class="sxs-lookup"><span data-stu-id="1ebaa-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="1ebaa-121">Sifat **Bilangan Pengguna** dan **Bilangan Bulan** boleh ditanda sebagai faktor kuantiti dengan mengedit sifat baris produk.</span><span class="sxs-lookup"><span data-stu-id="1ebaa-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="1ebaa-122">Untuk mencipta faktor kuantiti daripada sifat produk, lengkapkan langkah berikut.</span><span class="sxs-lookup"><span data-stu-id="1ebaa-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="1ebaa-123">Pada **Project Operations**, pilih **Produk Jualan**.</span><span class="sxs-lookup"><span data-stu-id="1ebaa-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="1ebaa-124">Buka produk yang anda perlukan untuk menetapkan faktor kuantiti.</span><span class="sxs-lookup"><span data-stu-id="1ebaa-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="1ebaa-125">Pastikan produk mempunyai sifat yang sudah ditetapkan.</span><span class="sxs-lookup"><span data-stu-id="1ebaa-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="1ebaa-126">Pada halaman **Maklumat Projek**, pilih tab **Faktor Kuantiti**.</span><span class="sxs-lookup"><span data-stu-id="1ebaa-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="1ebaa-127">Dalam subgrid, pilih **+ Pengiraan medan baharu**.</span><span class="sxs-lookup"><span data-stu-id="1ebaa-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="1ebaa-128">Masukkan nama **Faktor Kuantiti** dan pilih nilai sifat yang dipetakan kepada pengiraan medan.</span><span class="sxs-lookup"><span data-stu-id="1ebaa-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="1ebaa-129">Simpan dan tutup borang.</span><span class="sxs-lookup"><span data-stu-id="1ebaa-129">Save and close the form.</span></span>
7. <span data-ttu-id="1ebaa-130">Ulangi langkah 2-6 untuk semua sifat yang bersama akan membentuk kuantiti untuk baris kontrak berasaskan produk.</span><span class="sxs-lookup"><span data-stu-id="1ebaa-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="1ebaa-131">Dengan faktor kuantiti yang disediakan, apabila pengguna mencipta baris kontrak untuk produk ini, kuantiti baris kontrak dikunci.</span><span class="sxs-lookup"><span data-stu-id="1ebaa-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="1ebaa-132">Kuantiti kemudian dikira sebagai produk nilai sifat untuk baris kontrak tersebut.</span><span class="sxs-lookup"><span data-stu-id="1ebaa-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>
