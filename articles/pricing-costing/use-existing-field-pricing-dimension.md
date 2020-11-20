---
title: Medan Project Operations sebagai dimensi penetapan harga
description: Topik ini menyediakan maklumat menggunakan medan sebagai dimensi penetapan harga dalam Dynamics 365 Project Operations.
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
ms.openlocfilehash: 59367b35f15f806b109f606e912edc487d9e7685
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119249"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="481a8-103">Medan Project Operations sebagai dimensi penetapan harga</span><span class="sxs-lookup"><span data-stu-id="481a8-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="481a8-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="481a8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="481a8-105">Entiti **Aktual** mempunyai banyak medan yang boleh digunakan sebagai dimensi penetapan harga bagi penetapan harga berasaskan sumber.</span><span class="sxs-lookup"><span data-stu-id="481a8-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="481a8-106">Contohnya, satu medan biasa ialah **Sumber Boleh Ditempah**.</span><span class="sxs-lookup"><span data-stu-id="481a8-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="481a8-107">Syarikat yang lebih kecil yang mempunyai kurang daripada 20-30 sumber boleh dibilkan mungkin mendapati bahawa mempunyai bil dan kadar kos khusus untuk setiap sumber adalah pendekatan yang lebih mudah.</span><span class="sxs-lookup"><span data-stu-id="481a8-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="481a8-108">Walau bagaimanapun, apabila tenaga kerja boleh dibil bertambah, kadar sumber tertentu boleh menjadi tidak realistik untuk dikekalkan.</span><span class="sxs-lookup"><span data-stu-id="481a8-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="481a8-109">Kos sumber dan kadar bil mulai berbeza ketika sumber dipromosikan, memperoleh lebih banyak pengalaman atau memperoleh pelbagai kemahiran.</span><span class="sxs-lookup"><span data-stu-id="481a8-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="481a8-110">Satu lagi contoh ialah kategori transaksi.</span><span class="sxs-lookup"><span data-stu-id="481a8-110">Another example is that of transaction category.</span></span> <span data-ttu-id="481a8-111">Pelanggan dan pelaksana telah menggunakan kategori transaksi untuk mengklasifikasikan kerja dan menggunakan medan untuk harga dan kos berdasarkan pada kategori kerja.</span><span class="sxs-lookup"><span data-stu-id="481a8-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>
