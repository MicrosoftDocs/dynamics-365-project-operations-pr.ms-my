---
title: Anggaran sumber
description: Topik ini menyediakan maklumat tentang cara anggaran sumber dikira dalam Operasi Projek.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127382"
---
# <a name="resource-estimates"></a><span data-ttu-id="a67c1-103">Anggaran sumber</span><span class="sxs-lookup"><span data-stu-id="a67c1-103">Resource estimates</span></span>

<span data-ttu-id="a67c1-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="a67c1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a67c1-105">Anggaran sumber datang dari usaha jangka masa yang ditakrifkan dalam struktur pecahan kerja berserta dengan dimensi harga yang berkenaan.</span><span class="sxs-lookup"><span data-stu-id="a67c1-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="a67c1-106">Lazimnya, pengiraan adalah **kadar/jam untuk setiap peranan x jam.**</span><span class="sxs-lookup"><span data-stu-id="a67c1-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="a67c1-107">Usaha berfasa masa untuk setiap sumber disimpan dalam rekod tugas sumber.</span><span class="sxs-lookup"><span data-stu-id="a67c1-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="a67c1-108">Harga disimpan dalam senarai harga pratakrif.</span><span class="sxs-lookup"><span data-stu-id="a67c1-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="a67c1-109">Unit penukaran digunakan berdasarkan senarai harga yang berkenaan.</span><span class="sxs-lookup"><span data-stu-id="a67c1-109">Unit conversion is applied based on the applicable price list.</span></span>

![Anggaran Sumber](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="a67c1-111">Harga kos dan mata wang kos lalai</span><span class="sxs-lookup"><span data-stu-id="a67c1-111">Default cost price and cost currency</span></span>

<span data-ttu-id="a67c1-112">Harga kos dilalaikan daripada Unit Organisasi.</span><span class="sxs-lookup"><span data-stu-id="a67c1-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="a67c1-113">Kadar bil dan mata wang jualan lalai</span><span class="sxs-lookup"><span data-stu-id="a67c1-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="a67c1-114">Harga jualan digunakan sekali setiap urusan.</span><span class="sxs-lookup"><span data-stu-id="a67c1-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="a67c1-115">Hierarki untuk senarai harga jualan yang ingkar adalah seperti berikut:</span><span class="sxs-lookup"><span data-stu-id="a67c1-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="a67c1-116">Organisasi</span><span class="sxs-lookup"><span data-stu-id="a67c1-116">Organization</span></span>
2. <span data-ttu-id="a67c1-117">Pelanggan</span><span class="sxs-lookup"><span data-stu-id="a67c1-117">Customer</span></span>
3. <span data-ttu-id="a67c1-118">Sebut harga/kontrak</span><span class="sxs-lookup"><span data-stu-id="a67c1-118">Quote/contract</span></span>
