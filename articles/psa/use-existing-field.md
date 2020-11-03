---
title: Gunakan medan sedia ada dalam Project Service sebagai dimensi penentuan harga
description: Topik ini menyediakan maklumat tentang penggunaan medan Project Service sedia ada sebagai dimensi penentuan harga.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 415e346f88e60cb064f3327bfb35e21bd1c89014
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081306"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="8626e-103">Gunakan medan sedia ada dalam Project Service sebagai dimensi penentuan harga</span><span class="sxs-lookup"><span data-stu-id="8626e-103">Use an existing field in Project Service as a pricing dimension</span></span>

<span data-ttu-id="8626e-104">Project Service Automation (PSA) mempunyai banyak medan pada entiti **Aktual** yang boleh digunakan sebagai dimensi penentuan harga untuk penentuan harga berasaskan sumber dalam organisasi projek.</span><span class="sxs-lookup"><span data-stu-id="8626e-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="8626e-105">Contohnya, satu medan biasa ialah **Sumber Boleh Ditempah**.</span><span class="sxs-lookup"><span data-stu-id="8626e-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="8626e-106">Syarikat yang lebih kecil yang mempunyai kurang daripada 20-30 sumber boleh dibilkan mungkin mendapati bahawa mempunyai bil dan kadar kos khusus untuk setiap sumber adalah pendekatan yang lebih mudah.</span><span class="sxs-lookup"><span data-stu-id="8626e-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="8626e-107">Walau bagaimanapun, apabila tenaga kerja berkembang, ini boleh menjadi tidak realistik untuk dikekalkan sebagai kos sumber dan kadar bil mula berubah apabila sumber dipromosikan, mendapat lebih banyak pengalaman atau memperoleh set kemahiran yang berbeza.</span><span class="sxs-lookup"><span data-stu-id="8626e-107">However, as the billable workforce grows, this could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill sets.</span></span> <span data-ttu-id="8626e-108">Oleh sebab pendekatan ini masih berfungsi untuk syarikat saiz tertentu, lihat topik, [Gunakan sumber boleh ditempah sebagai dimensi penentuan harga](bookable-resource-pricing-dimension.md) untuk memahami cara medan Project Service sedia ada boleh digunakan sebagai dimensi penentuan harga.</span><span class="sxs-lookup"><span data-stu-id="8626e-108">Because this approach still works for companies of a certain size, see the topic, [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="8626e-109">Satu lagi contoh ialah kategori transaksi.</span><span class="sxs-lookup"><span data-stu-id="8626e-109">Another example is that of transaction category.</span></span> <span data-ttu-id="8626e-110">Pelanggan dan Pelaksana telah menggunakan kategori transaksi dalam PSA untuk mengklasifikasikan kerja dan menggunakan medan harga dan kos berdasarkan pada kategori kerja.</span><span class="sxs-lookup"><span data-stu-id="8626e-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="8626e-111">Untuk maklumat lanjut, lihat [Gunakan kategori transaksi sebagai dimensi penentuan harga](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="8626e-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>
