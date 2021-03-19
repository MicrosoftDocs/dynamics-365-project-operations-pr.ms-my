---
title: Invois yang diperbetulkan
description: Topik ini menyediakan maklumat tentang Invois yang diperbetulkan.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 734dc01e15339a31ac21f92bb3fb20d634a075ad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287834"
---
# <a name="corrected-invoices"></a><span data-ttu-id="b92b1-103">Invois yang diperbetulkan</span><span class="sxs-lookup"><span data-stu-id="b92b1-103">Corrected invoices</span></span>

<span data-ttu-id="b92b1-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="b92b1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b92b1-105">Invois yang disahkan boleh diedit.</span><span class="sxs-lookup"><span data-stu-id="b92b1-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="b92b1-106">Apabila anda mengedit invois yang disahkan, draf Invois yang diperbetulkan dicipta.</span><span class="sxs-lookup"><span data-stu-id="b92b1-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="b92b1-107">Oleh kerana anggapan bahawa anda mahu membalikkan semua transaksi dan kuantiti daripada invois asal, invois yang diperbetulkan memasukkan semua transaksi daripada invois asal dan semua kuantiti padanya adalah 0 (sifar).</span><span class="sxs-lookup"><span data-stu-id="b92b1-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="b92b1-108">Apabila transaksi tidak memerlukan pembetulan, anda boleh mengalih keluarnya daripada draf invois yang diperbetulkan.</span><span class="sxs-lookup"><span data-stu-id="b92b1-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="b92b1-109">Untuk membalikkan atau mengembalikan hanya sebahagian kuantiti, anda boleh mengedit medan Kuantiti pada butiran baris.</span><span class="sxs-lookup"><span data-stu-id="b92b1-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="b92b1-110">Jika anda membuka butiran baris invosi, anda boleh melihat kuantiti invois asal.</span><span class="sxs-lookup"><span data-stu-id="b92b1-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="b92b1-111">Anda kemudian boleh mengedit kuantiti invois semasa, agar ia kurang daripada atau lebih daripada kuantiti invois asal,</span><span class="sxs-lookup"><span data-stu-id="b92b1-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="b92b1-112">Apabila anda mengesahkan invois pembetulan, aktual jualan dibilkan asal dibalikkan, dan aktual jualan dibilkan baharu dicipta.</span><span class="sxs-lookup"><span data-stu-id="b92b1-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="b92b1-113">Jika kuantiti dikurangkan, perbezaan akan menyebabkan aktual jualan belum dibilkan baharu dicipta juga.</span><span class="sxs-lookup"><span data-stu-id="b92b1-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="b92b1-114">Contohnya, jika jualan dibilkan asal adalah untuk 8 jam dan butiran baris invois yang diperbetulkan mempunyai kuantiti berkurangan sebanyak enam jam, baris jualan dibilkan asal dibalikkan dan dua aktual baharu dicipta:</span><span class="sxs-lookup"><span data-stu-id="b92b1-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="b92b1-115">Aktual jualan dibilkan untuk enam jam.</span><span class="sxs-lookup"><span data-stu-id="b92b1-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="b92b1-116">Aktual jualan belum dibilkan untuk baki dua jam.</span><span class="sxs-lookup"><span data-stu-id="b92b1-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="b92b1-117">Transaksi ini boleh sama ada dibilkan kemudian atau ditanda sebagai bukan boleh dicaj, bergantung pada rundingan dengan pelanggan.</span><span class="sxs-lookup"><span data-stu-id="b92b1-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]