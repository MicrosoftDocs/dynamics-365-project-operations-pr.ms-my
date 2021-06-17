---
title: Mengapakah harga ditetapkan lalai kepada sifar pada kos perbelanjaan sebenar?
description: Penyelesaian masalah sebab harga ditetapkan lalai kepada 0 pada kos perbelanjaan sebenar.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
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
ms.openlocfilehash: 03c958635dec66b0f243872dfb929eba6a20119b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992797"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="cfc62-103">Mengapakah harga ditetapkan lalai kepada sifar pada kos perbelanjaan sebenar</span><span class="sxs-lookup"><span data-stu-id="cfc62-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="cfc62-104">Soalan lazim (FAQ) ini digunakan untuk perbelanjaan sebenar yang mana kelas transaksi ditetapkan kepada Perbelanjaan dan jenis transaksi ialah Kos.</span><span class="sxs-lookup"><span data-stu-id="cfc62-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="cfc62-105">Kadar kos penyelesaian masalah pada kos perbelanjaan sebenar</span><span class="sxs-lookup"><span data-stu-id="cfc62-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="cfc62-106">Pergi ke entri perbelanjaan yang berkaitan dan pastikan terdapat jumlah dalam medan enti perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="cfc62-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="cfc62-107">Jika entri perbelanjaan asal tidak mempunyai jumlah medan yang dipenuhi, maka anda telah mengasingkan masalah tersebut.</span><span class="sxs-lookup"><span data-stu-id="cfc62-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="cfc62-108">Untuk menyelesaikan masalah ini, cipta semula entri perbelanjaan dengan jumlah yang sah dan luluskannya.</span><span class="sxs-lookup"><span data-stu-id="cfc62-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]