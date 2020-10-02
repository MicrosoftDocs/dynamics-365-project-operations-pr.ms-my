---
title: Peringkat projek
description: Topik ini memberikan maklumat tentang peringkat projek yang tersedia dalam Microsoft Dynamics Project Operations.
author: ruhercul
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
ms.openlocfilehash: b11c67ebd21fdf423eeae2db8154f26787c2e64f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897957"
---
# <a name="project-stages"></a><span data-ttu-id="b61a9-103">Peringkat projek</span><span class="sxs-lookup"><span data-stu-id="b61a9-103">Project stages</span></span>

<span data-ttu-id="b61a9-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="b61a9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b61a9-105">Peringkat projek direka bentuk untuk menggambarkan keadaan projek semasa ia berjalan.</span><span class="sxs-lookup"><span data-stu-id="b61a9-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="b61a9-106">Penyesuaian boleh digunakan untuk mengemas kini peringkat secara automatik dengan aliran proses perniagaan, Power Automate atau sambungan pasang masuk.</span><span class="sxs-lookup"><span data-stu-id="b61a9-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="b61a9-107">Peringkat berikut ditakrifkan dalam aliran proses perniagaan lalai:</span><span class="sxs-lookup"><span data-stu-id="b61a9-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="b61a9-108">Baru</span><span class="sxs-lookup"><span data-stu-id="b61a9-108">New</span></span>
- <span data-ttu-id="b61a9-109">Sebut Harga</span><span class="sxs-lookup"><span data-stu-id="b61a9-109">Quote</span></span>
- <span data-ttu-id="b61a9-110">Pelan</span><span class="sxs-lookup"><span data-stu-id="b61a9-110">Plan</span></span>
- <span data-ttu-id="b61a9-111">Hantar</span><span class="sxs-lookup"><span data-stu-id="b61a9-111">Deliver</span></span>
- <span data-ttu-id="b61a9-112">Dilengkapkan</span><span class="sxs-lookup"><span data-stu-id="b61a9-112">Complete</span></span>
- <span data-ttu-id="b61a9-113">Tutup</span><span class="sxs-lookup"><span data-stu-id="b61a9-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="b61a9-114">Baru</span><span class="sxs-lookup"><span data-stu-id="b61a9-114">New</span></span>

<span data-ttu-id="b61a9-115">Apabila anda mencipta projek, peringkat projek ditetapkan kepada **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="b61a9-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="b61a9-116">Jika projek dicipta daripada templat, ia mungkin mempunyai jadual, anggaran dan data pasukan.</span><span class="sxs-lookup"><span data-stu-id="b61a9-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="b61a9-117">Sebaliknya, ia adalah satu garis panduan projek dan komponen yang tinggal mesti dimasukkan.</span><span class="sxs-lookup"><span data-stu-id="b61a9-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="b61a9-118">Sebut Harga</span><span class="sxs-lookup"><span data-stu-id="b61a9-118">Quote</span></span>

<span data-ttu-id="b61a9-119">Apabila anda mengaitkan projek dengan sebut harga atau apabila anda mencipta projek daripada sebut harga, peringkat projek ditetapkan kepada **Sebut Harga** dan anggaran tarikh mula dan tamat dikemas kini.</span><span class="sxs-lookup"><span data-stu-id="b61a9-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="b61a9-120">Semasa projek berada dalam peringkat **Sebut harga**, tab **Jualan** pada halaman **Entiti Projek** menunjukkan butiran sebut harga tersebut.</span><span class="sxs-lookup"><span data-stu-id="b61a9-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="b61a9-121">Pelan</span><span class="sxs-lookup"><span data-stu-id="b61a9-121">Plan</span></span>

<span data-ttu-id="b61a9-122">Apabila anda menang sebut harga yang dikaitkan dengan sesuatu projek dan projek tersebut beralih ke peringkat **Kontrak**, peringkat projek dikemas kini kepada **Pelan**.</span><span class="sxs-lookup"><span data-stu-id="b61a9-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="b61a9-123">Semasa projek berada dalam peringkat **Pelan**, halaman **Entiti Projek** menunjukkan butiran kontrak tersebut.</span><span class="sxs-lookup"><span data-stu-id="b61a9-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="b61a9-124">Hantar</span><span class="sxs-lookup"><span data-stu-id="b61a9-124">Deliver</span></span>

<span data-ttu-id="b61a9-125">Apabila pelan projek selesai dan anda bersedia untuk memulakan projek, pengurus projek harus mengemas kini peringkat projek kepada **Hantar** untuk menunjukkan yang projek telah dimulakan.</span><span class="sxs-lookup"><span data-stu-id="b61a9-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="b61a9-126">Selesai</span><span class="sxs-lookup"><span data-stu-id="b61a9-126">Complete</span></span> 

<span data-ttu-id="b61a9-127">Apabila kerja untuk projek selesai, pengurus projek boleh mengemas kini peringkat kepada **Selesai**.</span><span class="sxs-lookup"><span data-stu-id="b61a9-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="b61a9-128">Dengan mengemas kini peringkat projek kepada **Selesai**, pengurus projek menunjukkan bahawa kerja tersebut telah 100 peratus selesai, tetapi projek itu dibiarkan terbuka supaya sebarang masa atau perbelanjaan yang tertangguh boleh direkodkan.</span><span class="sxs-lookup"><span data-stu-id="b61a9-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="b61a9-129">Tutup</span><span class="sxs-lookup"><span data-stu-id="b61a9-129">Close</span></span>

<span data-ttu-id="b61a9-130">Apabila semua transaksi direkodkan untuk projek, pengurus projek boleh mengemas kini peringkat kepada **Tutup**.</span><span class="sxs-lookup"><span data-stu-id="b61a9-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="b61a9-131">Pada ketika itu, tiada transaksi boleh direkodkan dan projek itu ditetapkan kepada baca sahaja.</span><span class="sxs-lookup"><span data-stu-id="b61a9-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>

