---
title: Gambaran keseluruhan penginvoisan antara syarikat
description: Topik ini memberikan maklumat dan contoh tentang penginvoisan antara syarikat untuk projek.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42af89105f8325f1c94df6d2133d2c329facf2b3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002652"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="8c7b5-103">Gambaran keseluruhan penginvoisan antara syarikat</span><span class="sxs-lookup"><span data-stu-id="8c7b5-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="8c7b5-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="8c7b5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8c7b5-105">Organisasi anda mungkin mempunyai berbilang divisyen, subsidiari dan entiti undang-undang lain yang memindahkan produk dan perkhidmatan kepada satu sama lain untuk projek.</span><span class="sxs-lookup"><span data-stu-id="8c7b5-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="8c7b5-106">Entiti undang-undang yang menyediakan perkhidmatan atau produk tersebut dipanggil *entiti undang-undang yang memberi pinjaman*.</span><span class="sxs-lookup"><span data-stu-id="8c7b5-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="8c7b5-107">Entiti undang-undang yang menerima perkhidmatan atau produk tersebut dipanggil *entiti undang-undang yang menerima pinjaman*.</span><span class="sxs-lookup"><span data-stu-id="8c7b5-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="8c7b5-108">Ilustrasi berikut menunjukkan senario biasa di mana dua entiti sah, Contoso Robotics USA (entiti sah pinjaman) dan Contoso Robotics UK (entiti sah pinjaman) berkongsi sumber untuk menyampaikan projek untuk pelanggan, Adventure works.</span><span class="sxs-lookup"><span data-stu-id="8c7b5-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="8c7b5-109">Untuk senario ini, Contoso Robotics USA dikontrakkan untuk menyampaikan kerja kepada Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="8c7b5-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Penginvoisan antara syarikat](./media/IntercompanyScenario.png) 

<span data-ttu-id="8c7b5-111">Dynamics 365 Project Operations menggunakan aliran berikut untuk memproses transaksi antara syarikat:</span><span class="sxs-lookup"><span data-stu-id="8c7b5-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="8c7b5-112">Sumber daripada entiti undang-undang yang memberi pinjaman merekod transaksi perbelanjaan atau masa antara syarikat mengikut masa tempahan dan perbelanjaan terhadap projek dalam entiti undang-undang yang menerima pinjaman.</span><span class="sxs-lookup"><span data-stu-id="8c7b5-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="8c7b5-113">Kos masa dan perbelanjaan direkodkan dalam syarikat yang memberi pinjaman dengan menggunakan senarai harga kos unit syarikat yang menerima pinjaman.</span><span class="sxs-lookup"><span data-stu-id="8c7b5-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="8c7b5-114">Transaksi jualan tidak dibilkan antara syarikat direkodkan dalam syarikat yang memberi pinjaman dengan menggunakan senarai harga kos unit syarikat yang menerima pinjaman.</span><span class="sxs-lookup"><span data-stu-id="8c7b5-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="8c7b5-115">Pendapatan yang tidak dibilkan direkodkan dalam syarikat yang menerima pinjaman menggunakan senarai harga jualan kontrak projek.</span><span class="sxs-lookup"><span data-stu-id="8c7b5-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="8c7b5-116">Pelanggan boleh dibilkan apabila hasil tidak dibilkan direkodkan.</span><span class="sxs-lookup"><span data-stu-id="8c7b5-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="8c7b5-117">Pelanggan tidak perlu menunggu sehingga pemprosesan invois antara syarikat selesai.</span><span class="sxs-lookup"><span data-stu-id="8c7b5-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="8c7b5-118">Invois pelanggan antara syarikat dibuat secara berkala dalam syarikat yang memberi pinjaman.</span><span class="sxs-lookup"><span data-stu-id="8c7b5-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="8c7b5-119">Invois dicipta secara manual atau dengan menggunakan proses automatik berkala.</span><span class="sxs-lookup"><span data-stu-id="8c7b5-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="8c7b5-120">Invois tunggal boleh dicipta untuk setiap entiti undang-undang yang memberi pinham atau invois berasingan boleh dicipta mengikut projek.</span><span class="sxs-lookup"><span data-stu-id="8c7b5-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="8c7b5-121">Apabila invois pelanggan antara syarikat disiarkan dalam entiti undang-undang yang memberi pinjaman, invois vendor yang belum selesai dibuat dalam entiti undang-undang yang menerima pinjaman.</span><span class="sxs-lookup"><span data-stu-id="8c7b5-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="8c7b5-122">Kos dalam invois vendor yang belum selesai akan direkodkan kepada sublejar projek apabila invois disiarkan.</span><span class="sxs-lookup"><span data-stu-id="8c7b5-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="8c7b5-123">Gambar rajah berikut menunjukkan penginvoisan antara syarikat kerana ia berkaitan dengan peristiwa perakaunan dan penyiaran yang dijangka kepada lejar umum.</span><span class="sxs-lookup"><span data-stu-id="8c7b5-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Aliran antara syarikat](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="8c7b5-125">Sumber tambahan</span><span class="sxs-lookup"><span data-stu-id="8c7b5-125">Additional resources</span></span>

- [<span data-ttu-id="8c7b5-126">Konfigurasikan penginvoisan antara syarikat</span><span class="sxs-lookup"><span data-stu-id="8c7b5-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="8c7b5-127">Rekodkan transaksi antara syarikat</span><span class="sxs-lookup"><span data-stu-id="8c7b5-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="8c7b5-128">Cipta invois pelanggan dan vendor antara syarikat</span><span class="sxs-lookup"><span data-stu-id="8c7b5-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]