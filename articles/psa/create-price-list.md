---
title: Cipta senarai harga
description: Cara untuk mencipta senarai harga dalam Project Service
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: bf75286fd1837e27a9b6053ccb21b60771ee197d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081264"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="16e89-103">Cipta senarai harga (Project Service)</span><span class="sxs-lookup"><span data-stu-id="16e89-103">Create a price list (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="16e89-104">Senarai harga menyediakan templat yang pengurus akaun anda boleh gunakan untuk mencipta sebut harga dan projek serta untuk menetapkan kos projek.</span><span class="sxs-lookup"><span data-stu-id="16e89-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="16e89-105">Mereka menyediakan senarai item baris bagi peranan dan perbelanjaan serta harga yang anda akan kenakan untuk setiap satu.</span><span class="sxs-lookup"><span data-stu-id="16e89-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="16e89-106">Anda boleh mencipta berbilang harga senarai agar anda boleh mengekalkan struktur harga berasingan untuk rantau berlainan yang anda menjual produk atau saluran jualan yang berlainan.</span><span class="sxs-lookup"><span data-stu-id="16e89-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="16e89-107">Mencipta sekurang-kurangnya satu senarai harga untuk setiap mata wang yang anda ingin gunakan untuk mengebil pelanggan anda adalah satu idea yang baik.</span><span class="sxs-lookup"><span data-stu-id="16e89-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="16e89-108">Untuk mencipta anggaran kewangan supaya kerja dapat dihantar, pastikan setiap projek mempunyai kos sandaran dan senarai harga jualan.</span><span class="sxs-lookup"><span data-stu-id="16e89-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="16e89-109">Sediakan kos lalai dan senarai harga jualan yang diguna pakai untuk semua projek yang dicipta dalam organisasi anda.</span><span class="sxs-lookup"><span data-stu-id="16e89-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="16e89-110">Senarai harga bergantung pada kategori peranan dan perbelanjaan, jadi sebelum anda mencipta senarai harga, pastikan anda telah mengkonfigurasikan kategori peranan dan perbelanjaan yang anda mahu gunakan ketika mencipta senarai harga.</span><span class="sxs-lookup"><span data-stu-id="16e89-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="16e89-111">Pergi ke **Project Service > Senarai Harga**.</span><span class="sxs-lookup"><span data-stu-id="16e89-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="16e89-112">Klik **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="16e89-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="16e89-113">Dalam **Konteks** , pilih sama ada senarai harga ini adalah untuk **Kos** , **Pembelian** atau **Jualan**.</span><span class="sxs-lookup"><span data-stu-id="16e89-113">In **Context** , select whether this price list is for **Cost** , **Purchase** , or **Sales**.</span></span>  
  
4.  <span data-ttu-id="16e89-114">Dalam **Nama** , masukkan nama untuk senarai harga.</span><span class="sxs-lookup"><span data-stu-id="16e89-114">In **Name** , enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="16e89-115">Dalam **Mata Wang** , pilih mata wang yang akan anda gunakan untuk pengebilan dan pengekosan.</span><span class="sxs-lookup"><span data-stu-id="16e89-115">In **Currency** , select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="16e89-116">Dalam **Unit Masa** , tentukan tempoh masa harga digunakan seperti hari atau jam.</span><span class="sxs-lookup"><span data-stu-id="16e89-116">In **Time Unit** , specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="16e89-117">Isikan **Tarikh Mula** , **Tarikh Tamat** dan **Perihalan** seperti yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="16e89-117">Fill in the **Start Date** , **End Date** , and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="16e89-118">Klik **Simpan** untuk mencipta rekod supaya anda boleh terus mengeditnya.</span><span class="sxs-lookup"><span data-stu-id="16e89-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="16e89-119">Untuk menambah harga peranan pada senarai harga, klik **+** di bawah **Harga peranan**.</span><span class="sxs-lookup"><span data-stu-id="16e89-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="16e89-120">Dalam anak tetingkap **Harga Peranan** , isikan butiran dan kemudian klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="16e89-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="16e89-121">Teruskan menambah harga peranan seperti yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="16e89-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="16e89-122">Apabila anda selesai, klik **Simpan** di sudut kanan bawah skrin.</span><span class="sxs-lookup"><span data-stu-id="16e89-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="16e89-123">Untuk menambah harga kategori perbelanjaan pada senarai harga, klik **+** di bawah **Harga Kategori**.</span><span class="sxs-lookup"><span data-stu-id="16e89-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="16e89-124">Dalam anak tetingkap **Harga Kategori Transaksi** , isikan butiran dan kemudian klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="16e89-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="16e89-125">Teruskan menambah harga kategori seperti yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="16e89-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="16e89-126">Apabila anda selesai, klik **Simpan** di sudut kanan bawah skrin.</span><span class="sxs-lookup"><span data-stu-id="16e89-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="16e89-127">Untuk menambah item senarai harga pada senarai harga, klik **+** di bawah **Item Senarai Harga**.</span><span class="sxs-lookup"><span data-stu-id="16e89-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="16e89-128">Dalam anak tetingkap **Item Senarai Harga** , isikan butiran dan kemudian klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="16e89-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="16e89-129">Teruskan menambah item senarai harga seperti yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="16e89-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="16e89-130">Apabila anda selesai, klik **Simpan** di sudut kanan bawah skrin.</span><span class="sxs-lookup"><span data-stu-id="16e89-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="16e89-131">Untuk menambah perhubungan wilayah pada senarai harga, klik **+** di bawah **Perhubungan Wilayah**.</span><span class="sxs-lookup"><span data-stu-id="16e89-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="16e89-132">Dalam tetingkap **Sambungan Baharu** , isikan butiran dan kemudian klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="16e89-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="16e89-133">Teruskan menambah perhubungan wilayah seperti yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="16e89-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="16e89-134">Apabila anda selesai, klik **Simpan** di sudut kanan bawah skrin.</span><span class="sxs-lookup"><span data-stu-id="16e89-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="16e89-135">Lihat Juga</span><span class="sxs-lookup"><span data-stu-id="16e89-135">See Also</span></span>  
 [<span data-ttu-id="16e89-136">Konfigurasikan Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="16e89-136">Configure Project Service Automation</span></span>](../psa/configure.md)
