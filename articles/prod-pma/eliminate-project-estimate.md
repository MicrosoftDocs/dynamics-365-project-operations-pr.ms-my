---
title: Hapuskan anggaran projek
description: Topik ini menyediakan maklumat tentang cara menghapuskan anggaran projek selepas ia selesai.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 8bda8a7357e883b948449b2a19bea476996dde3c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081281"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="72fb1-103">Hapuskan anggaran projek</span><span class="sxs-lookup"><span data-stu-id="72fb1-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72fb1-104">Anggaran projek memberikan pandangan kewangan untuk kerja yang dianggarkan dan dijadualkan untuk projek.</span><span class="sxs-lookup"><span data-stu-id="72fb1-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="72fb1-105">Untuk menggunakan anggaran untuk projek, anda mesti melampirkan projek kepada projek anggaran.</span><span class="sxs-lookup"><span data-stu-id="72fb1-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="72fb1-106">Projek anggaran sentiasa berdasarkan projek yang sedia ada, namun berbilang projek boleh merujuk kepada satu projek anggaran.</span><span class="sxs-lookup"><span data-stu-id="72fb1-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="72fb1-107">Hanya projek harga tetap dan pelaburan boleh dilampirkan kepada projek anggaran, dan projek tersebut mesti tergolong dalam kumpulan projek yang sama dengan projek anggaran.</span><span class="sxs-lookup"><span data-stu-id="72fb1-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="72fb1-108">Untuk menghapuskan projek anggaran, ia mesti dilengkapkan.</span><span class="sxs-lookup"><span data-stu-id="72fb1-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="72fb1-109">Langkah berikut menerangkan cara untuk menghapuskan anggaran.</span><span class="sxs-lookup"><span data-stu-id="72fb1-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="72fb1-110">Pergi **Pengurusan dan perakaunan projek** > **Semua Projek** dan buka projek.</span><span class="sxs-lookup"><span data-stu-id="72fb1-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="72fb1-111">Pada tab **Uruskan** , pilih **Anggaran** , dan pada halaman **Anggaran** , pilih **Hapuskan**.</span><span class="sxs-lookup"><span data-stu-id="72fb1-111">On the **Manage** tab, select **Estimates** , and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="72fb1-112">Pada halaman **Hapuskan anggaran** pada tab **Umum** , tetapan pilihan berikut:</span><span class="sxs-lookup"><span data-stu-id="72fb1-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="72fb1-113">**Kod tempoh** : Pilih kod tempoh untuk memilih projek anggaran yang sewajarnya.</span><span class="sxs-lookup"><span data-stu-id="72fb1-113">**Period code** : Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="72fb1-114">**Tarikh anggaran** : Pilih tarikh anggaran yang sewajarnya untuk penghapusan.</span><span class="sxs-lookup"><span data-stu-id="72fb1-114">**Estimate date** : Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="72fb1-115">**Hapuskan dengan amaran WIP** : Dayakan pilihan ini untuk memberikan pemberitahuan apabila anggaran yang dikaitkan dengan kerja yang sedang dijalankan (WIP) akan dihapuskan.</span><span class="sxs-lookup"><span data-stu-id="72fb1-115">**Eliminate with WIP warnings** : Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="72fb1-116">Apabila pilihan ini tidak didayakan, penghapusan tidak dapat diteruskan jika mana-mana transaksi bukan anggaran wujud.</span><span class="sxs-lookup"><span data-stu-id="72fb1-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="72fb1-117">Pilihan ini hanya tersedia apabila penghapusan digunakan pada projek anggaran.</span><span class="sxs-lookup"><span data-stu-id="72fb1-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="72fb1-118">Ia tidak tersedia jika anda menggunakan penyiaran berkala.</span><span class="sxs-lookup"><span data-stu-id="72fb1-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="72fb1-119">Tetapan ini berfungsi dengan tetapan pada tab **Anggaran** pada halaman **Parameter projek** , dalam kumpulan medan **Benarkan penghapusan apabila transaksi bukan anggaran wujud**.</span><span class="sxs-lookup"><span data-stu-id="72fb1-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="72fb1-120">**Tetapkan peringkat kepada Selesai** : Dayakan pilihan ini untuk menetapkan peringkat projek anggaran kepada **Selesai** selepas anda menjalankan penghapusan.</span><span class="sxs-lookup"><span data-stu-id="72fb1-120">**Set stage to Finished** : Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="72fb1-121">**Cetak senarai anggaran** : Pilih maklumat yang akan disertakan apabila senarai anggaran dicetak.</span><span class="sxs-lookup"><span data-stu-id="72fb1-121">**Print estimate list** : Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="72fb1-122">**Tunjukkan Log Maklumat** : Dayakan pilihan ini untuk memaparkan Log Maklumat.</span><span class="sxs-lookup"><span data-stu-id="72fb1-122">**Show Infolog** : Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="72fb1-123">**Tarikh penyiaran** : Pilih tarikh penyiaran lejar anggaran.</span><span class="sxs-lookup"><span data-stu-id="72fb1-123">**Posting date** : Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="72fb1-124">Pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="72fb1-124">Select **OK**.</span></span>
5. <span data-ttu-id="72fb1-125">Selepas proses penghapusan selesai, projek anggaran yang dihapuskan akan dipaparkan dengan nilai negatif.</span><span class="sxs-lookup"><span data-stu-id="72fb1-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="72fb1-126">Jika anda tidak berniat untuk menghapuskan anggaran, anda boleh memilih anggaran yang dihapuskan dan pilih **Buat balik penghapusan**.</span><span class="sxs-lookup"><span data-stu-id="72fb1-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   
