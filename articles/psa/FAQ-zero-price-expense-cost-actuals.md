---
title: Mengapakah harga ditetapkan lalai kepada sifar pada kos perbelanjaan sebenar?
description: Penyelesaian masalah sebab harga ditetapkan lalai kepada 0 pada kos perbelanjaan sebenar.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 306f169ee25d42ac3c9e63fa70956b9c50315829
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122129"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="bd295-103">Mengapakah harga ditetapkan lalai kepada sifar pada kos perbelanjaan sebenar?</span><span class="sxs-lookup"><span data-stu-id="bd295-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="bd295-104">Soalan lazim (FAQ) ini digunakan untuk perbelanjaan sebenar yang mana kelas transaksi ditetapkan kepada Perbelanjaan dan jenis transaksi ialah Kos.</span><span class="sxs-lookup"><span data-stu-id="bd295-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="bd295-105">Kadar kos penyelesaian masalah pada kos perbelanjaan sebenar</span><span class="sxs-lookup"><span data-stu-id="bd295-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="bd295-106">Pergi ke entri perbelanjaan yang berkaitan dan pastikan terdapat jumlah dalam medan enti perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="bd295-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="bd295-107">Jika entri perbelanjaan asal tidak mempunyai jumlah medan yang dipenuhi, maka anda telah mengasingkan masalah tersebut.</span><span class="sxs-lookup"><span data-stu-id="bd295-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="bd295-108">Untuk menyelesaikan masalah ini, cipta semula entri perbelanjaan dengan jumlah yang sah dan luluskannya.</span><span class="sxs-lookup"><span data-stu-id="bd295-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
