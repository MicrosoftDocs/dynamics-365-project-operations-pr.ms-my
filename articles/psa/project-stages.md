---
title: Jenis peringkat projek
description: Topik ini memberikan maklumat tentang peringkat projek.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: aa423979a794b07a8bd27440f47a29480b74b518
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123073"
---
# <a name="project-stage-types"></a><span data-ttu-id="01aac-103">Jenis peringkat projek</span><span class="sxs-lookup"><span data-stu-id="01aac-103">Project stage types</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="01aac-104">Peringkat projek direka bentuk untuk menggambarkan keadaan projek semasa ia berjalan.</span><span class="sxs-lookup"><span data-stu-id="01aac-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="01aac-105">Penyesuaian boleh digunakan untuk mengemas kini peringkat secara automatik dengan aliran proses perniagaan, Power Automate atau sambungan pasang masuk.</span><span class="sxs-lookup"><span data-stu-id="01aac-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="01aac-106">Peringkat berikut ditakrifkan dalam BPF lalai:</span><span class="sxs-lookup"><span data-stu-id="01aac-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="01aac-107">Baru</span><span class="sxs-lookup"><span data-stu-id="01aac-107">New</span></span>
- <span data-ttu-id="01aac-108">Sebut Harga</span><span class="sxs-lookup"><span data-stu-id="01aac-108">Quote</span></span>
- <span data-ttu-id="01aac-109">Pelan</span><span class="sxs-lookup"><span data-stu-id="01aac-109">Plan</span></span>
- <span data-ttu-id="01aac-110">Hantar</span><span class="sxs-lookup"><span data-stu-id="01aac-110">Deliver</span></span>
- <span data-ttu-id="01aac-111">Selesai</span><span class="sxs-lookup"><span data-stu-id="01aac-111">Complete</span></span>
- <span data-ttu-id="01aac-112">Tutup</span><span class="sxs-lookup"><span data-stu-id="01aac-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="01aac-113">Baharu</span><span class="sxs-lookup"><span data-stu-id="01aac-113">New</span></span>

<span data-ttu-id="01aac-114">Apabila anda mencipta projek, peringkat projek ditetapkan kepada **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="01aac-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="01aac-115">Jika projek dicipta daripada templat, ia mungkin mempunyai jadual, anggaran dan data pasukan.</span><span class="sxs-lookup"><span data-stu-id="01aac-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="01aac-116">Jika tidak, ia hanya satu garis panduan projek dan komponen yang selebihnya mesti dimasukkan.</span><span class="sxs-lookup"><span data-stu-id="01aac-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="01aac-117">Sebut Harga</span><span class="sxs-lookup"><span data-stu-id="01aac-117">Quote</span></span>

<span data-ttu-id="01aac-118">Apabila anda mengaitkan projek dengan sebut harga atau apabila anda mencipta projek daripada sebut harga, peringkat projek ditetapkan kepada **Sebut Harga** dan anggaran tarikh mula dan tamat dikemas kini.</span><span class="sxs-lookup"><span data-stu-id="01aac-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="01aac-119">Semasa projek berada dalam peringkat **Sebut harga**, tab **Jualan** pada halaman **Entiti Projek** menunjukkan butiran sebut harga tersebut.</span><span class="sxs-lookup"><span data-stu-id="01aac-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="01aac-120">Pelan</span><span class="sxs-lookup"><span data-stu-id="01aac-120">Plan</span></span>

<span data-ttu-id="01aac-121">Apabila anda menang sebut harga yang dikaitkan dengan sesuatu projek dan projek tersebut beralih ke peringkat **Kontrak**, peringkat projek dikemas kini kepada **Pelan**.</span><span class="sxs-lookup"><span data-stu-id="01aac-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="01aac-122">Semasa projek berada dalam peringkat **Pelan**, halaman **Entiti Projek** menunjukkan butiran kontrak tersebut.</span><span class="sxs-lookup"><span data-stu-id="01aac-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="01aac-123">Hantar</span><span class="sxs-lookup"><span data-stu-id="01aac-123">Deliver</span></span>

<span data-ttu-id="01aac-124">Apabila pelan projek selesai dan anda bersedia untuk memulakan projek, pengurus projek harus mengemas kini peringkat projek kepada **Hantar** untuk menunjukkan yang projek telah dimulakan.</span><span class="sxs-lookup"><span data-stu-id="01aac-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="01aac-125">Selesai</span><span class="sxs-lookup"><span data-stu-id="01aac-125">Complete</span></span> 

<span data-ttu-id="01aac-126">Apabila kerja untuk projek selesai, pengurus projek boleh mengemas kini peringkat kepada **Selesai**.</span><span class="sxs-lookup"><span data-stu-id="01aac-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="01aac-127">Dengan mengemas kini peringkat projek kepada **Selesai**, pengurus projek menunjukkan bahawa kerja tersebut telah 100 peratus selesai, tetapi projek itu dibiarkan terbuka supaya sebarang masa atau perbelanjaan yang tertangguh boleh direkodkan.</span><span class="sxs-lookup"><span data-stu-id="01aac-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="01aac-128">Tutup</span><span class="sxs-lookup"><span data-stu-id="01aac-128">Close</span></span>

<span data-ttu-id="01aac-129">Apabila semua transaksi direkodkan untuk projek, pengurus projek boleh mengemas kini peringkat kepada **Tutup**.</span><span class="sxs-lookup"><span data-stu-id="01aac-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="01aac-130">Pada ketika itu, tiada transaksi boleh direkodkan dan projek itu ditetapkan kepada baca sahaja.</span><span class="sxs-lookup"><span data-stu-id="01aac-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
