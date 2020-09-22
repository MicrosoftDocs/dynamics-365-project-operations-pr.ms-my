---
title: Peringkat projek
description: Topik ini memberikan maklumat tentang peringkat projek.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753880"
---
# <a name="project-stages"></a><span data-ttu-id="b5a16-103">Peringkat projek</span><span class="sxs-lookup"><span data-stu-id="b5a16-103">Project stages</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b5a16-104">Peringkat projek dikemas kini untuk menggambarkan keadaan projek tersebut apabila ia berjalan.</span><span class="sxs-lookup"><span data-stu-id="b5a16-104">Project stages are updated to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="b5a16-105">Aliran proses perniagaan lalai mengemas kini secara automatik beberapa peringkat projek sementara yang lain dikemas kini secara manual oleh pengurus projek.</span><span class="sxs-lookup"><span data-stu-id="b5a16-105">The default business process flow automatically updates some stages of the project while others are manually updated by the project manager.</span></span> 

<span data-ttu-id="b5a16-106">Peringkat berikut ditakrifkan dalam BPF lalai:</span><span class="sxs-lookup"><span data-stu-id="b5a16-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="b5a16-107">Baharu</span><span class="sxs-lookup"><span data-stu-id="b5a16-107">New</span></span>
- <span data-ttu-id="b5a16-108">Sebut Harga</span><span class="sxs-lookup"><span data-stu-id="b5a16-108">Quote</span></span>
- <span data-ttu-id="b5a16-109">Pelan</span><span class="sxs-lookup"><span data-stu-id="b5a16-109">Plan</span></span>
- <span data-ttu-id="b5a16-110">Hantar</span><span class="sxs-lookup"><span data-stu-id="b5a16-110">Deliver</span></span>
- <span data-ttu-id="b5a16-111">Selesai</span><span class="sxs-lookup"><span data-stu-id="b5a16-111">Complete</span></span>
- <span data-ttu-id="b5a16-112">Tutup</span><span class="sxs-lookup"><span data-stu-id="b5a16-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="b5a16-113">Baharu</span><span class="sxs-lookup"><span data-stu-id="b5a16-113">New</span></span>

<span data-ttu-id="b5a16-114">Apabila anda mencipta projek, peringkat projek ditetapkan kepada **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="b5a16-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="b5a16-115">Jika projek dicipta daripada templat, ia mungkin mempunyai jadual, anggaran dan data pasukan.</span><span class="sxs-lookup"><span data-stu-id="b5a16-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="b5a16-116">Jika tidak, ia hanya satu garis panduan projek dan komponen yang selebihnya mesti dimasukkan.</span><span class="sxs-lookup"><span data-stu-id="b5a16-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="b5a16-117">Sebut Harga</span><span class="sxs-lookup"><span data-stu-id="b5a16-117">Quote</span></span>

<span data-ttu-id="b5a16-118">Apabila anda mengaitkan projek dengan sebut harga atau apabila anda mencipta projek daripada sebut harga, peringkat projek ditetapkan kepada **Sebut Harga** dan anggaran tarikh mula dan tamat dikemas kini.</span><span class="sxs-lookup"><span data-stu-id="b5a16-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="b5a16-119">Semasa projek berada dalam peringkat **Sebut harga**, tab **Jualan** pada halaman **Entiti Projek** menunjukkan butiran sebut harga tersebut.</span><span class="sxs-lookup"><span data-stu-id="b5a16-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="b5a16-120">Pelan</span><span class="sxs-lookup"><span data-stu-id="b5a16-120">Plan</span></span>

<span data-ttu-id="b5a16-121">Apabila anda menang sebut harga yang dikaitkan dengan sesuatu projek dan projek tersebut beralih ke peringkat **Kontrak**, peringkat projek dikemas kini kepada **Pelan**.</span><span class="sxs-lookup"><span data-stu-id="b5a16-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="b5a16-122">Semasa projek berada dalam peringkat **Pelan**, halaman **Entiti Projek** menunjukkan butiran kontrak tersebut.</span><span class="sxs-lookup"><span data-stu-id="b5a16-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="b5a16-123">Hantar</span><span class="sxs-lookup"><span data-stu-id="b5a16-123">Deliver</span></span>

<span data-ttu-id="b5a16-124">Apabila pelan projek selesai dan anda bersedia untuk memulakan projek, pengurus projek harus mengemas kini peringkat projek kepada **Hantar** untuk menunjukkan yang projek telah dimulakan.</span><span class="sxs-lookup"><span data-stu-id="b5a16-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="b5a16-125">Selesai</span><span class="sxs-lookup"><span data-stu-id="b5a16-125">Complete</span></span> 

<span data-ttu-id="b5a16-126">Apabila kerja untuk projek selesai, pengurus projek boleh mengemas kini peringkat kepada **Selesai**.</span><span class="sxs-lookup"><span data-stu-id="b5a16-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="b5a16-127">Dengan mengemas kini peringkat projek kepada **Selesai**, pengurus projek menunjukkan bahawa kerja tersebut telah 100 peratus selesai, tetapi projek itu dibiarkan terbuka supaya sebarang masa atau perbelanjaan yang tertangguh boleh direkodkan.</span><span class="sxs-lookup"><span data-stu-id="b5a16-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="b5a16-128">Tutup</span><span class="sxs-lookup"><span data-stu-id="b5a16-128">Close</span></span>

<span data-ttu-id="b5a16-129">Apabila semua transaksi direkodkan untuk projek, pengurus projek boleh mengemas kini peringkat kepada **Tutup**.</span><span class="sxs-lookup"><span data-stu-id="b5a16-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="b5a16-130">Pada ketika itu, tiada transaksi boleh direkodkan dan projek itu ditetapkan kepada baca sahaja.</span><span class="sxs-lookup"><span data-stu-id="b5a16-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
