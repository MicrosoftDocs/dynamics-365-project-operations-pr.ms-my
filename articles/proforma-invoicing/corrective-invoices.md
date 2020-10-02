---
title: Invois yang diperbetulkan
description: Topik ini menyediakan maklumat tentang Invois yang diperbetulkan.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898092"
---
# <a name="corrected-invoices"></a><span data-ttu-id="4c294-103">Invois yang diperbetulkan</span><span class="sxs-lookup"><span data-stu-id="4c294-103">Corrected invoices</span></span>

<span data-ttu-id="4c294-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="4c294-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4c294-105">Invois yang disahkan boleh diedit.</span><span class="sxs-lookup"><span data-stu-id="4c294-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="4c294-106">Apabila anda mengedit invois yang disahkan, draf Invois yang diperbetulkan dicipta.</span><span class="sxs-lookup"><span data-stu-id="4c294-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="4c294-107">Oleh kerana anggapan bahawa anda mahu membalikkan semua transaksi dan kuantiti daripada invois asal, invois yang diperbetulkan memasukkan semua transaksi daripada invois asal dan semua kuantiti padanya adalah 0 (sifar).</span><span class="sxs-lookup"><span data-stu-id="4c294-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="4c294-108">Apabila transaksi tidak memerlukan pembetulan, anda boleh mengalih keluarnya daripada draf invois yang diperbetulkan.</span><span class="sxs-lookup"><span data-stu-id="4c294-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="4c294-109">Untuk membalikkan atau mengembalikan hanya sebahagian kuantiti, anda boleh mengedit medan Kuantiti pada butiran baris.</span><span class="sxs-lookup"><span data-stu-id="4c294-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="4c294-110">Jika anda membuka butiran baris invosi, anda boleh melihat kuantiti invois asal.</span><span class="sxs-lookup"><span data-stu-id="4c294-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="4c294-111">Anda kemudian boleh mengedit kuantiti invois semasa, agar ia kurang daripada atau lebih daripada kuantiti invois asal,</span><span class="sxs-lookup"><span data-stu-id="4c294-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="4c294-112">Apabila anda mengesahkan invois pembetulan, aktual jualan dibilkan asal dibalikkan, dan aktual jualan dibilkan baharu dicipta.</span><span class="sxs-lookup"><span data-stu-id="4c294-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="4c294-113">Jika kuantiti dikurangkan, perbezaan akan menyebabkan aktual jualan belum dibilkan baharu dicipta juga.</span><span class="sxs-lookup"><span data-stu-id="4c294-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="4c294-114">Contohnya, jika jualan dibilkan asal adalah untuk 8 jam dan butiran baris invois yang diperbetulkan mempunyai kuantiti berkurangan sebanyak enam jam, baris jualan dibilkan asal dibalikkan dan dua aktual baharu dicipta:</span><span class="sxs-lookup"><span data-stu-id="4c294-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="4c294-115">Aktual jualan dibilkan untuk enam jam.</span><span class="sxs-lookup"><span data-stu-id="4c294-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="4c294-116">Aktual jualan belum dibilkan untuk baki dua jam.</span><span class="sxs-lookup"><span data-stu-id="4c294-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="4c294-117">Transaksi ini boleh sama ada dibilkan kemudian atau ditanda sebagai bukan boleh dicaj, bergantung pada rundingan dengan pelanggan.</span><span class="sxs-lookup"><span data-stu-id="4c294-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
