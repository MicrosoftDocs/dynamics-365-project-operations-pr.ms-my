---
title: Analisis sebut harga projek
description: Topik ini memberikan maklumat mengenai analisis sebut harga projek.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
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
ms.openlocfilehash: 0d9cefafcce33297146cae81d9ba7e68ab79aeb6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081344"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="76bb9-103">Analisis sebut harga projek</span><span class="sxs-lookup"><span data-stu-id="76bb9-103">Analysis of project quotes</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="76bb9-104">Dynamics 365 Project Service Automation menganalisa sebut harga projek untuk menganggarkan keuntungan.</span><span class="sxs-lookup"><span data-stu-id="76bb9-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="76bb9-105">Ia juga menganalisis seberapa baik sebut harga itu sejajar dengan jangkaan pelanggan mengenai tarikh penghantaran atau tarikh siap dan tentang belanjawan.</span><span class="sxs-lookup"><span data-stu-id="76bb9-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="76bb9-106">Analisis keuntungan</span><span class="sxs-lookup"><span data-stu-id="76bb9-106">Profitability analysis</span></span>

<span data-ttu-id="76bb9-107">Project Service Automation menganalisis keuntungan dengan menggunakan margin kasar dan margin kasar yang dilaraskan.</span><span class="sxs-lookup"><span data-stu-id="76bb9-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="76bb9-108">Margin kasar dikira menggunakan formula berikut:</span><span class="sxs-lookup"><span data-stu-id="76bb9-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="76bb9-109">Margin kasar yang dilaraskan dikira menggunakan formula berikut:</span><span class="sxs-lookup"><span data-stu-id="76bb9-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="76bb9-110">Jika nilai untuk margin kasar dan margin kasar dilaraskan berbeza mengikut luas margin, kebanyakan kerja dalam sebut harga dikelaskan sebagai tidak boleh dikenakan cukai.</span><span class="sxs-lookup"><span data-stu-id="76bb9-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="76bb9-111">Analisis jangkaan pelanggan</span><span class="sxs-lookup"><span data-stu-id="76bb9-111">Analysis of customer expectations</span></span>

<span data-ttu-id="76bb9-112">Anda boleh menganalisis sebut harga dan menjana carta untuk jangkaan pelanggan mengenai jadual dan belanjawan jika anda memasukkan nilai untuk medan berikut:</span><span class="sxs-lookup"><span data-stu-id="76bb9-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="76bb9-113">Medan **Tarikh penghantaran yang diminta** pada pengepala sebut harga.</span><span class="sxs-lookup"><span data-stu-id="76bb9-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="76bb9-114">Medan **Belanjawan pelanggan** bagi setiap baris sebut harga (untuk baris berasaskan projek dan baris berasaskan produk).</span><span class="sxs-lookup"><span data-stu-id="76bb9-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="76bb9-115">Analisis jangkaan pelanggan mengenai jadual dilakukan dengan membandingkan tarikh akhir baris sebut harga terperinci dengan tarikh penghantaran yang diminta merentasi semua baris sebut harga dalam sebut harga.</span><span class="sxs-lookup"><span data-stu-id="76bb9-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="76bb9-116">Analisis jangkaan pelanggan mengenai belanjawan dilakukan dengan membandingkan jumlah bagi jumlah belanjawan pelanggan dengan amaun disebut merentasi semua baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="76bb9-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>
