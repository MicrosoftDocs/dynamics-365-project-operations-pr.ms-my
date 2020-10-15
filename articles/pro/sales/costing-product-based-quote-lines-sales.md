---
title: Penetapan kos baris sebut harga berdasarkan produk
description: Topik ini memberikan maklumat tentang penerapan harga kos pada sebut harga berdasarkan produk.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 17b377eab5bcbc1a2327cb3ff87cc75d8de40953
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906262"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="6f886-103">Penetapan kos baris sebut harga berdasarkan produk</span><span class="sxs-lookup"><span data-stu-id="6f886-103">Costing product-based quote lines</span></span>

<span data-ttu-id="6f886-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="6f886-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="6f886-105">Baris sebut harga berasaskan produk dalam Operasi Projek Dynamics 365 juga mempunyai medan **Harga Kos**.</span><span class="sxs-lookup"><span data-stu-id="6f886-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="6f886-106">Medan ini digunakan untuk menjejaki harga kos untuk produk pada baris sebut harga dan untuk pengiraan keuntungan hiliran.</span><span class="sxs-lookup"><span data-stu-id="6f886-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="6f886-107">Apabila baris sebut harga berdasarkan produk dicipta untuk produk katalog, kos baris sebut harga berdasarkan produk ditetapkan daripada medan **Kos Standard** dalam katalog produk.</span><span class="sxs-lookup"><span data-stu-id="6f886-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="6f886-108">Medan kos standard dalam katalog produk ditetapkan dalam mata wang asas Organisasi.</span><span class="sxs-lookup"><span data-stu-id="6f886-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="6f886-109">Kos unit lalai pada baris sebut harga berasaskan produk ditukar kepada mata wang jualan pada sebut harga.</span><span class="sxs-lookup"><span data-stu-id="6f886-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="6f886-110">Kos unit pada barisan sebut harga berasaskan produk</span><span class="sxs-lookup"><span data-stu-id="6f886-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="6f886-111">Tujuan mempunyai kos unit pada baris sebut harga berasaskan produk ialah untuk membolehkan kos yang berbeza untuk produk untuk setiap jualan.</span><span class="sxs-lookup"><span data-stu-id="6f886-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="6f886-112">Ini bukan senario biasa, tetapi kadangkala kos produk mungkin didiskaunkan oleh pembekal bergantung pada pelanggan jualan akhir.</span><span class="sxs-lookup"><span data-stu-id="6f886-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="6f886-113">Contohnya:</span><span class="sxs-lookup"><span data-stu-id="6f886-113">For example:</span></span>

<span data-ttu-id="6f886-114">Fabrikam Robotics sedang memasang lengan robot pada barisan pemasangan Datum Corporation.</span><span class="sxs-lookup"><span data-stu-id="6f886-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="6f886-115">Fabrikam menyediakan perkhidmatan pemasangan tetapi lengan robot diperolehi daripada Trey robotics.</span><span class="sxs-lookup"><span data-stu-id="6f886-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="6f886-116">Jika pemasangan senjata robot di sebuah Datum Corporation membuka industri baru menegak untuk lengan robot Trey, Trey boleh memberikan diskaun khas untuk urusan ini ke Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="6f886-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="6f886-117">Dalam kes ini, Fabrikam akan mencipta talian sebut harga berdasarkan produk untuk Senjata Robot dan masukkan kos khas bagi setiap unit untuk sebut harga ini.</span><span class="sxs-lookup"><span data-stu-id="6f886-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="6f886-118">Kos ini berbeza daripada kos Standard Lengan Robot Trey.</span><span class="sxs-lookup"><span data-stu-id="6f886-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>
