---
title: Pesanan belian untuk projek
description: Artikel ini menerangkan pelbagai kaedah yang boleh anda gunakan untuk mencipta pesanan belian untuk projek. Kaedah yang anda gunakan bergantung pada tujuan pesanan belian, dan apabila item yang dibeli digunakan dan dikenakan kepada projek.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd891aec5bcab66c5801a5d9ca8abbbf632d662d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081216"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="a545e-104">Pesanan belian untuk projek</span><span class="sxs-lookup"><span data-stu-id="a545e-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a545e-105">Artikel ini menerangkan pelbagai kaedah yang boleh anda gunakan untuk mencipta pesanan belian untuk projek.</span><span class="sxs-lookup"><span data-stu-id="a545e-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="a545e-106">Kaedah yang anda gunakan bergantung pada tujuan pesanan belian, dan apabila item yang dibeli digunakan dan dikenakan kepada projek.</span><span class="sxs-lookup"><span data-stu-id="a545e-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="a545e-107">Kaedah untuk mencipta pesanan belian</span><span class="sxs-lookup"><span data-stu-id="a545e-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="a545e-108">Anda boleh menggunakan salah satu kaedah berikut untuk mencipta pesanan belian dalam Pengurusan projek dan perakaunan.</span><span class="sxs-lookup"><span data-stu-id="a545e-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="a545e-109">Tujuan pesanan belian menentukan apabila pesanan belian digunakan dan oleh itu, apabila item dikenakan caj pada projek.</span><span class="sxs-lookup"><span data-stu-id="a545e-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a545e-110">Kaedah</span><span class="sxs-lookup"><span data-stu-id="a545e-110">Method</span></span></th>
<th><span data-ttu-id="a545e-111">Tujuan</span><span class="sxs-lookup"><span data-stu-id="a545e-111">Purpose</span></span></th>
<th><span data-ttu-id="a545e-112">Penggunaan item</span><span class="sxs-lookup"><span data-stu-id="a545e-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a545e-113">Cipta pesanan belian secara langsung daripada projek.</span><span class="sxs-lookup"><span data-stu-id="a545e-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="a545e-114">Gunakan kaedah ini untuk membeli item daripada vendor luaran untuk penggunaan pada projek.</span><span class="sxs-lookup"><span data-stu-id="a545e-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="a545e-115">Anda boleh mencipta pesanan belian dengan dua cara:</span><span class="sxs-lookup"><span data-stu-id="a545e-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="a545e-116">Daripada projek itu sendiri.</span><span class="sxs-lookup"><span data-stu-id="a545e-116">From the project itself.</span></span> <span data-ttu-id="a545e-117">Dalam kes ini, projek sudah ditetapkan untuk pesanan belian.</span><span class="sxs-lookup"><span data-stu-id="a545e-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="a545e-118">Dengan menavigasi kepada pesanan belian projek.</span><span class="sxs-lookup"><span data-stu-id="a545e-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="a545e-119">Anda mesti memilih vendor dan projek untuk mencipta pesanan belian.</span><span class="sxs-lookup"><span data-stu-id="a545e-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="a545e-120">Item digunakan apabila invois vendor dikemas kini.</span><span class="sxs-lookup"><span data-stu-id="a545e-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a545e-121">Cipta pesanan belian daripada pesanan jualan.</span><span class="sxs-lookup"><span data-stu-id="a545e-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="a545e-122">Gunakan kaedah ini untuk membeli item apabila anda mencipta pesanan jualan daripada projek.</span><span class="sxs-lookup"><span data-stu-id="a545e-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="a545e-123">Item digunakan apabila pesanan jualan diinvoiskan kepada pelanggan.</span><span class="sxs-lookup"><span data-stu-id="a545e-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a545e-124">Cipta pesanan belian daripada keperluan item.</span><span class="sxs-lookup"><span data-stu-id="a545e-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="a545e-125">Gunakan kaedah ini untuk membeli item apabila anda mencipta keperluan item daripada projek.</span><span class="sxs-lookup"><span data-stu-id="a545e-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="a545e-126">Item digunakan apabila slip pembungkusan keperluan item dikemas kini.</span><span class="sxs-lookup"><span data-stu-id="a545e-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="a545e-127">Apabila anda mengemas kini invois vendor atau slip pembungkusan, anda digesa untuk mengemas kini slip pembungkusan pada keperluan item.</span><span class="sxs-lookup"><span data-stu-id="a545e-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="a545e-128">Untuk mendapatkan maklumat lanjut, lihat [Terima item pada pesanan belian daripada keperluan item](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="a545e-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

