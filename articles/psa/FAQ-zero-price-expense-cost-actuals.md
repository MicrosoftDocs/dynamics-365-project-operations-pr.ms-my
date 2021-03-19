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
ms.openlocfilehash: 742b0b9c495b4b3ecb4705be3ece5656f0322ca9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285858"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="3f921-103">Mengapakah harga ditetapkan lalai kepada sifar pada kos perbelanjaan sebenar</span><span class="sxs-lookup"><span data-stu-id="3f921-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="3f921-104">Soalan lazim (FAQ) ini digunakan untuk perbelanjaan sebenar yang mana kelas transaksi ditetapkan kepada Perbelanjaan dan jenis transaksi ialah Kos.</span><span class="sxs-lookup"><span data-stu-id="3f921-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="3f921-105">Kadar kos penyelesaian masalah pada kos perbelanjaan sebenar</span><span class="sxs-lookup"><span data-stu-id="3f921-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="3f921-106">Pergi ke entri perbelanjaan yang berkaitan dan pastikan terdapat jumlah dalam medan enti perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="3f921-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="3f921-107">Jika entri perbelanjaan asal tidak mempunyai jumlah medan yang dipenuhi, maka anda telah mengasingkan masalah tersebut.</span><span class="sxs-lookup"><span data-stu-id="3f921-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="3f921-108">Untuk menyelesaikan masalah ini, cipta semula entri perbelanjaan dengan jumlah yang sah dan luluskannya.</span><span class="sxs-lookup"><span data-stu-id="3f921-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]