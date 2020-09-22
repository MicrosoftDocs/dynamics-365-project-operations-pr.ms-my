---
title: Mengapakah harga ditetapkan lalai kepada sifar pada kos perbelanjaan sebenar?
description: Penyelesaian masalah sebab harga ditetapkan lalai kepada 0 pada kos perbelanjaan sebenar.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: bc1ebc58-c733-4310-8435-572ed9a9fef9
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 3fb678822877a61d141de75aea29b7d5cdf292c4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753898"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="d92a7-103">Mengapakah harga ditetapkan lalai kepada sifar pada kos perbelanjaan sebenar?</span><span class="sxs-lookup"><span data-stu-id="d92a7-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d92a7-104">Soalan lazim (FAQ) ini digunakan untuk perbelanjaan sebenar yang mana kelas transaksi ditetapkan kepada Perbelanjaan dan jenis transaksi ialah Kos.</span><span class="sxs-lookup"><span data-stu-id="d92a7-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="d92a7-105">Kadar kos penyelesaian masalah pada kos perbelanjaan sebenar</span><span class="sxs-lookup"><span data-stu-id="d92a7-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="d92a7-106">Pergi ke entri perbelanjaan yang berkaitan dan pastikan terdapat jumlah dalam medan enti perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="d92a7-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="d92a7-107">Jika entri perbelanjaan asal tidak mempunyai jumlah medan yang dipenuhi, maka anda telah mengasingkan masalah tersebut.</span><span class="sxs-lookup"><span data-stu-id="d92a7-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="d92a7-108">Untuk menyelesaikan masalah ini, cipta semula entri perbelanjaan dengan jumlah yang sah dan luluskannya.</span><span class="sxs-lookup"><span data-stu-id="d92a7-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
