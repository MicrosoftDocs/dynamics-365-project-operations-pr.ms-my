---
title: Medan Project Operations sebagai dimensi penetapan harga
description: Topik ini memberikan maklumat yang menggunakan medan sebagai dimensi penetapan harga dalam Dynamics 365 Project Operations.
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
ms.openlocfilehash: 04b823e8237590a294ed0706e64d0ecb9d2cf56f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274649"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="5ab4c-103">Medan Project Operations sebagai dimensi penentuan harga</span><span class="sxs-lookup"><span data-stu-id="5ab4c-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="5ab4c-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="5ab4c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5ab4c-105">Entiti **Aktual** mempunyai banyak medan yang boleh digunakan sebagai dimensi penetapan harga bagi penetapan harga berasaskan sumber.</span><span class="sxs-lookup"><span data-stu-id="5ab4c-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="5ab4c-106">Contohnya, satu medan biasa ialah **Sumber Boleh Ditempah**.</span><span class="sxs-lookup"><span data-stu-id="5ab4c-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="5ab4c-107">Syarikat yang lebih kecil yang mempunyai kurang daripada 20-30 sumber boleh dibilkan mungkin mendapati bahawa mempunyai bil dan kadar kos khusus untuk setiap sumber adalah pendekatan yang lebih mudah.</span><span class="sxs-lookup"><span data-stu-id="5ab4c-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="5ab4c-108">Walau bagaimanapun, apabila tenaga kerja boleh dibil bertambah, kadar sumber tertentu boleh menjadi tidak realistik untuk dikekalkan.</span><span class="sxs-lookup"><span data-stu-id="5ab4c-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="5ab4c-109">Kos sumber dan kadar bil mulai berbeza ketika sumber dipromosikan, memperoleh lebih banyak pengalaman atau memperoleh pelbagai kemahiran.</span><span class="sxs-lookup"><span data-stu-id="5ab4c-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="5ab4c-110">Satu lagi contoh ialah kategori transaksi.</span><span class="sxs-lookup"><span data-stu-id="5ab4c-110">Another example is that of transaction category.</span></span> <span data-ttu-id="5ab4c-111">Pelanggan dan pelaksana telah menggunakan kategori transaksi untuk mengklasifikasikan kerja dan menggunakan medan untuk harga dan kos berdasarkan pada kategori kerja.</span><span class="sxs-lookup"><span data-stu-id="5ab4c-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]