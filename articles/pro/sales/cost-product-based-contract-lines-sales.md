---
title: Kos baris kontrak berasaskan produk - ringan
description: Topik ini menyediakan maklumat tentang penciptaan
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 001b0b54abcdd5fcd1eca7f3271cc78392f68860
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273704"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="061b5-103">Kos baris kontrak berasaskan produk - ringan</span><span class="sxs-lookup"><span data-stu-id="061b5-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="061b5-104">_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_</span><span class="sxs-lookup"><span data-stu-id="061b5-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="061b5-105">Baris kontrak berdasarkan produk dalam Dynamics 365 Project Operations termasuk medan **Harga Kos**, yang menyimpan harga kos bagi produk untuk pengiraan keuntungan hiliran.</span><span class="sxs-lookup"><span data-stu-id="061b5-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="061b5-106">Apabila baris kontrak berdasarkan produk dicipta untuk produk katalog, kos baris lalai daripada medan **Kos Standard** dalam katalog produk.</span><span class="sxs-lookup"><span data-stu-id="061b5-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="061b5-107">Medan **Kos Standard** dalam katalog produk ditetapkan dalam mata wang asas Organisasi.</span><span class="sxs-lookup"><span data-stu-id="061b5-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="061b5-108">Apabila unit kos lalai pada baris kontrak, ia ditukar ke dalam mata wang jualan pada kontrak.</span><span class="sxs-lookup"><span data-stu-id="061b5-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="061b5-109">Kos unit pada barisan kontrak berasaskan produk</span><span class="sxs-lookup"><span data-stu-id="061b5-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="061b5-110">Mempunyai kos unit pada baris kontrak berasaskan produk membenarkan untuk kos produk yang berbeza bagi setiap jualan.</span><span class="sxs-lookup"><span data-stu-id="061b5-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="061b5-111">Walaupun tidak semestinya perlu, terdapat senario tertentu yang kos produk mungkin didiskaunkan kepada pelanggan oleh pembekal.</span><span class="sxs-lookup"><span data-stu-id="061b5-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="061b5-112">Pertimbangkan senario yang berikut:</span><span class="sxs-lookup"><span data-stu-id="061b5-112">Consider the following scenario:</span></span>

<span data-ttu-id="061b5-113">Fabrikam Robotics sedang memasang lengan robotik pada barisan pemasangan Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="061b5-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="061b5-114">Fabrikam menyediakan perkhidmatan pemasangan tetapi lengan robot adalah daripada Trey Reserarch.</span><span class="sxs-lookup"><span data-stu-id="061b5-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="061b5-115">Jika pemasangan lengan robotik di Adatum Corporation membuka industri menegak baharu bagi Trey Research, ia boleh menawarkan diskaun istimewa untuk urusan ini kepada Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="061b5-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="061b5-116">Dalam hal ini, Fabrikam mencipta baris kontrak berdasarkan produk untuk Lengan Robot.</span><span class="sxs-lookup"><span data-stu-id="061b5-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="061b5-117">Kos seunit dimasukkan untuk kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="061b5-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="061b5-118">Kos adalah berbeza daripada kos lengan robot daripada Trey Research.</span><span class="sxs-lookup"><span data-stu-id="061b5-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]