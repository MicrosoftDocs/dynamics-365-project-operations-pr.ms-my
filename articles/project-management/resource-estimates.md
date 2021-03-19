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
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286529"
---
# <a name="resource-estimates"></a><span data-ttu-id="abf84-103">Anggaran sumber</span><span class="sxs-lookup"><span data-stu-id="abf84-103">Resource estimates</span></span>

<span data-ttu-id="abf84-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="abf84-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="abf84-105">Anggaran sumber datang dari usaha jangka masa yang ditakrifkan dalam struktur pecahan kerja berserta dengan dimensi harga yang berkenaan.</span><span class="sxs-lookup"><span data-stu-id="abf84-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="abf84-106">Lazimnya, pengiraan adalah **kadar/jam untuk setiap peranan x jam.**</span><span class="sxs-lookup"><span data-stu-id="abf84-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="abf84-107">Usaha berfasa masa untuk setiap sumber disimpan dalam rekod tugas sumber.</span><span class="sxs-lookup"><span data-stu-id="abf84-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="abf84-108">Harga disimpan dalam senarai harga pratakrif.</span><span class="sxs-lookup"><span data-stu-id="abf84-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="abf84-109">Unit penukaran digunakan berdasarkan senarai harga yang berkenaan.</span><span class="sxs-lookup"><span data-stu-id="abf84-109">Unit conversion is applied based on the applicable price list.</span></span>

![Anggaran Sumber](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="abf84-111">Harga kos dan mata wang kos lalai</span><span class="sxs-lookup"><span data-stu-id="abf84-111">Default cost price and cost currency</span></span>

<span data-ttu-id="abf84-112">Harga kos dilalaikan daripada Unit Organisasi.</span><span class="sxs-lookup"><span data-stu-id="abf84-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="abf84-113">Kadar bil dan mata wang jualan lalai</span><span class="sxs-lookup"><span data-stu-id="abf84-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="abf84-114">Harga jualan digunakan sekali setiap urusan.</span><span class="sxs-lookup"><span data-stu-id="abf84-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="abf84-115">Hierarki untuk senarai harga jualan yang ingkar adalah seperti berikut:</span><span class="sxs-lookup"><span data-stu-id="abf84-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="abf84-116">Organisasi</span><span class="sxs-lookup"><span data-stu-id="abf84-116">Organization</span></span>
2. <span data-ttu-id="abf84-117">Pelanggan</span><span class="sxs-lookup"><span data-stu-id="abf84-117">Customer</span></span>
3. <span data-ttu-id="abf84-118">Sebut harga/kontrak</span><span class="sxs-lookup"><span data-stu-id="abf84-118">Quote/contract</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]