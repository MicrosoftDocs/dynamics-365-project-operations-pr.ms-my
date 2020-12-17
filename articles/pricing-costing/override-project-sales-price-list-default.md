---
title: Ganti senarai harga jualan projek
description: Topik ini menyediakan maklumat tentang mencipta senarai harga jualan tersuai.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: af9baca540d89f4e5e616bdfdd6111bef29abe28
ms.sourcegitcommit: 656a9d03f260c29e988e2ff05b6e07ae0365d6d0
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672242"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="075ba-103">Ganti senarai harga jualan projek</span><span class="sxs-lookup"><span data-stu-id="075ba-103">Override project sales price lists</span></span>

<span data-ttu-id="075ba-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="075ba-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="075ba-105">Senarai harga projek khusus pelanggan</span><span class="sxs-lookup"><span data-stu-id="075ba-105">Customer-specific project price lists</span></span>

<span data-ttu-id="075ba-106">Perjanjian harga khusus pelanggan boleh ditetapkan sebagai senarai harga projek pada rekod akaun dalam Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="075ba-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="075ba-107">Untuk menyediakan senarai harga projek khusus pelanggan, dalam kawasan **Jualan**, navigasi ke rekod akaun.</span><span class="sxs-lookup"><span data-stu-id="075ba-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="075ba-108">Buka halaman senarai **Akaun**.</span><span class="sxs-lookup"><span data-stu-id="075ba-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="075ba-109">Cari dan klik dua kali rekod pelanggan untuk membuka halaman butiran **Akaun**.</span><span class="sxs-lookup"><span data-stu-id="075ba-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="075ba-110">Pada tab **Senarai Harga Projek**, pilih **+ Senarai Harga Projek Baharu**.</span><span class="sxs-lookup"><span data-stu-id="075ba-110">On the **Project Price lists** tab, select **+ New Project Price List**.</span></span>
4. <span data-ttu-id="075ba-111">Pada halaman **Senarai Harga Projek Baharu**, pilih senarai harga daripada juntai bawah.</span><span class="sxs-lookup"><span data-stu-id="075ba-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="075ba-112">Hanya senarai harga yang mempunyai konteks ditetapkan ke **Jualan** dan mata wang yang sepadan dengan mata wang akaun dimasukkan.</span><span class="sxs-lookup"><span data-stu-id="075ba-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="075ba-113">Namakan perkaitan dan kemudian pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="075ba-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="075ba-114">Senarai harga projek khusus pelanggan dicipta.</span><span class="sxs-lookup"><span data-stu-id="075ba-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="075ba-115">Senarai harga ini akan digunakan untuk harga projek lalai pada sebut harga projek atau kontrak yang dicipta untuk pelanggan ini dengan tarikh sebut harga atau kontrak projek yang dicipta berada dalam penguatkuasaan tarikh senarai harga.</span><span class="sxs-lookup"><span data-stu-id="075ba-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="075ba-116">Penetapan harga tersuai pada sebut harga projek</span><span class="sxs-lookup"><span data-stu-id="075ba-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="075ba-117">Pada sebut harga projek, anda boleh mempunyai penetapan harga projek yang bermula dengan senarai harga standard lalai yang dilalaikan daripada pelanggan atau daripada parameter projek.</span><span class="sxs-lookup"><span data-stu-id="075ba-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="075ba-118">Apabila anda memerlukan penetapan harga tersuai untuk kerja berkaitan projek pada sebut harga tertentu, anda boleh mendapatkannya daripada senarai harga projek entiti berkaitan.</span><span class="sxs-lookup"><span data-stu-id="075ba-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="075ba-119">Lengkapkan langkah berikut untuk menyediakan penetapan harga projek khusus sebut harga.</span><span class="sxs-lookup"><span data-stu-id="075ba-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="075ba-120">Buka sebut harga projek dan pilih tab **Senarai Harga Projek**.</span><span class="sxs-lookup"><span data-stu-id="075ba-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="075ba-121">Dalam sub grid, pilih **Cipta penetapan harga tersuai**.</span><span class="sxs-lookup"><span data-stu-id="075ba-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="075ba-122">Semua senarai harga projek yang dilampirkan pada sebut harga disalin ke senarai harga baharu.</span><span class="sxs-lookup"><span data-stu-id="075ba-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="075ba-123">Nama senarai harga baharu menunjukkan nama sebut harga dengan cap masa tarikh untuk apabila senarai harga ini dicipta.</span><span class="sxs-lookup"><span data-stu-id="075ba-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="075ba-124">Anda boleh menggunakan setiap senarai harga itu dan membuat kemas kini untuk harga buruh (harga peranan) dan perbelanjaan (harga kategori).</span><span class="sxs-lookup"><span data-stu-id="075ba-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="075ba-125">Harga ini hanya akan digunakan untuk sebut harga projek ini.</span><span class="sxs-lookup"><span data-stu-id="075ba-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="075ba-126">Senarai harga pada kontrak projek</span><span class="sxs-lookup"><span data-stu-id="075ba-126">Price lists on a project contract</span></span>

<span data-ttu-id="075ba-127">Pada kontrak projek, penetapan harga projek sentiasa lalai sebagai senarai harga tersuai dengan nama kontrak dan cap masa tarikh dicipta ditambah kepada nama.</span><span class="sxs-lookup"><span data-stu-id="075ba-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="075ba-128">Ini adalah benar sama ada kontrak dicipta apabila sebut harga dimenangi atau jika kontrak dicipta daripada awal.</span><span class="sxs-lookup"><span data-stu-id="075ba-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="075ba-129">Jika perlu, anda boleh mengalih keluar perkaitan ini ke senarai harga tersuai dan mengaitkan senarai harga standard kepada kontrak projek.</span><span class="sxs-lookup"><span data-stu-id="075ba-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="075ba-130">Apabila anda mengaitkan senarai harga standard ke senarai harga projek pada sebut harga atau kontrak, sebarang perubahan yang dibuat pada harga dalam senarai harga akan memberi kesan kepada semua sebut harga dan kontrak yang menggunakan senarai harga.</span><span class="sxs-lookup"><span data-stu-id="075ba-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>
