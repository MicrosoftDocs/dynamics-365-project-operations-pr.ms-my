---
title: Terima item pada pesanan pembelian daripada keperluan item
description: Topik ini menerangkan cara untuk menerima item pada pesanan pembelian daripada keperluan item.
author: Yowelle
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e0c4a75f1d86538cc773af1f7c0ae3c83ef0ad5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011697"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="d736d-103">Terima item pada pesanan pembelian daripada keperluan item</span><span class="sxs-lookup"><span data-stu-id="d736d-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d736d-104">Topik ini menerangkan cara untuk menerima item pada pesanan pembelian daripada keperluan item.</span><span class="sxs-lookup"><span data-stu-id="d736d-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="d736d-105">Dengan menggunakan keperluan item berbanding transaksi item, anda boleh merancang untuk penghantaran hanya sebelum item itu sebenarnya digunakan, cipta pesanan pembelian, termasuk item dalam rangka kerja perjanjian perdagangan dan termasuk keperluan item dalam perancangan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="d736d-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="d736d-106">Tugas ini menggunakan set data USSI.</span><span class="sxs-lookup"><span data-stu-id="d736d-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="d736d-107">Dalam anak tetingkap navigasi, pergi ke **Modul > Pengurusan dan perakaunan projek > Projek > Semua projek**.</span><span class="sxs-lookup"><span data-stu-id="d736d-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="d736d-108">Dalam senarai, pilih pautan dalam baris yang dikehendaki.</span><span class="sxs-lookup"><span data-stu-id="d736d-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="d736d-109">Pada Anak Tetingkap Tindakan, pilih **Pelan**.</span><span class="sxs-lookup"><span data-stu-id="d736d-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="d736d-110">Pilih **Keperluan item**.</span><span class="sxs-lookup"><span data-stu-id="d736d-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="d736d-111">Pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="d736d-111">Select **New**.</span></span>
6. <span data-ttu-id="d736d-112">Dalam baris baharu, masukkan atau pilih nilai dalam medan **Nombor item**.</span><span class="sxs-lookup"><span data-stu-id="d736d-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="d736d-113">Dalam medan **Kuantiti**, masukkan nombor.</span><span class="sxs-lookup"><span data-stu-id="d736d-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="d736d-114">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="d736d-114">Select **Save**.</span></span>
9. <span data-ttu-id="d736d-115">Pada Anak Tetingkap Tindakan, pilih **Urus**.</span><span class="sxs-lookup"><span data-stu-id="d736d-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="d736d-116">Pilih **Fungsi**.</span><span class="sxs-lookup"><span data-stu-id="d736d-116">Select **Functions**.</span></span>
11. <span data-ttu-id="d736d-117">Pilih **Cipta pesanan pembelian**.</span><span class="sxs-lookup"><span data-stu-id="d736d-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="d736d-118">Pilih kotak semak **Masukkan semua**.</span><span class="sxs-lookup"><span data-stu-id="d736d-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="d736d-119">Dalam medan **Akaun vendor**, masukkan atau pilih nilai.</span><span class="sxs-lookup"><span data-stu-id="d736d-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="d736d-120">Pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="d736d-120">Select **OK**.</span></span>
15. <span data-ttu-id="d736d-121">Dalam anak tetingkap navigasi, pergi ke **Modul > Akaun belum dibayar > Pesanan pembelian > Semua pesanan pembelian**.</span><span class="sxs-lookup"><span data-stu-id="d736d-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="d736d-122">Dalam senarai, pilih pautan dalam baris yang dikehendaki.</span><span class="sxs-lookup"><span data-stu-id="d736d-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="d736d-123">Pada Anak Tetingkap Tindakan, pilih **Beli**.</span><span class="sxs-lookup"><span data-stu-id="d736d-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="d736d-124">Pilih **Sahkan**.</span><span class="sxs-lookup"><span data-stu-id="d736d-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="d736d-125">Pada Anak Tetingkap Tindakan, pilih **Terima**.</span><span class="sxs-lookup"><span data-stu-id="d736d-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="d736d-126">Pilih **Resit produk**.</span><span class="sxs-lookup"><span data-stu-id="d736d-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="d736d-127">Dalam medan **Resit produk**, taipkan nilai.</span><span class="sxs-lookup"><span data-stu-id="d736d-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="d736d-128">Pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="d736d-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]