---
title: Konfigurasi penciptaan invois automatik
description: Topik ini menyediakan maklumat tentang cara mengkonfigurasi sistem untuk menjana invois secara automatik.
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
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898137"
---
# <a name="configure-automated-invoice-creation"></a><span data-ttu-id="83a81-103">Konfigurasi penciptaan invois automatik</span><span class="sxs-lookup"><span data-stu-id="83a81-103">Configure automated invoice creation</span></span>

<span data-ttu-id="83a81-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="83a81-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="83a81-105">Lengkapkan langkah berikut untuk mengkonfigurasi jalanan invois automatik dalam Project operations.</span><span class="sxs-lookup"><span data-stu-id="83a81-105">Complete the following steps to configure an automated invoice run in Project operations.</span></span>

1. <span data-ttu-id="83a81-106">Pergi ke **Tetapan** \> **Kerja Kelompok**.</span><span class="sxs-lookup"><span data-stu-id="83a81-106">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="83a81-107">Cipta kerja kelompok dan namakannya **Project operations mencipta invois**.</span><span class="sxs-lookup"><span data-stu-id="83a81-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="83a81-108">Nama kerja kelompok mesti memasukkan terma "cipta invois."</span><span class="sxs-lookup"><span data-stu-id="83a81-108">The name of the batch job must include the term "create invoices."</span></span>
3. <span data-ttu-id="83a81-109">Dalam medan **Jenis kerja**, pilih **Tiada**.</span><span class="sxs-lookup"><span data-stu-id="83a81-109">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="83a81-110">Secara lalai, **Kekerapan Harian** dan pilihan **Adalah Aktif** ditetapkan kepada **Ya**.</span><span class="sxs-lookup"><span data-stu-id="83a81-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="83a81-111">Pilih **Jalankan Aliran Kerja**.</span><span class="sxs-lookup"><span data-stu-id="83a81-111">Select **Run Workflow**.</span></span> <span data-ttu-id="83a81-112">Dalam kotak dialog **Cari Rekod**, anda akan melihat tiga aliran tugas:</span><span class="sxs-lookup"><span data-stu-id="83a81-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="83a81-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="83a81-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="83a81-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="83a81-114">ProcessRunner</span></span>
    - <span data-ttu-id="83a81-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="83a81-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="83a81-116">Pilih **ProcessRunCaller**, kemudian pilih **Tambah**.</span><span class="sxs-lookup"><span data-stu-id="83a81-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="83a81-117">Dalam kotak dialog seterusnya, pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="83a81-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="83a81-118">Aliran tugas **Tidur** diikuti dengan aliran tugas **Proses**.</span><span class="sxs-lookup"><span data-stu-id="83a81-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="83a81-119">Anda juga boleh memilih **ProcessRunner** dalam langkah 5.</span><span class="sxs-lookup"><span data-stu-id="83a81-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="83a81-120">Kemudian, apabila anda pilih **OK**, aliran tugas **Proses** diikuti oleh aliran kerja **Tidur**.</span><span class="sxs-lookup"><span data-stu-id="83a81-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="83a81-121">Aliran kerja **ProcessRunCaller** dan **ProcessRunner** mencipta invois.</span><span class="sxs-lookup"><span data-stu-id="83a81-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="83a81-122">**ProcessRunCaller** memanggil **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="83a81-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="83a81-123">**ProcessRunner** ialah aliran kerja yang sebenarnya mencipta invois.</span><span class="sxs-lookup"><span data-stu-id="83a81-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="83a81-124">Ia merangkumi semua baris kontrak yang perlu dicipta invois, dan ia mencipta invois untuk baris tersebut.</span><span class="sxs-lookup"><span data-stu-id="83a81-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="83a81-125">Untuk menentukan baris kontrak yang perlu dicipta invois, kerja dilihat pada tarikh jalanan invois untuk baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="83a81-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="83a81-126">Jika baris kontrak milik satu kontrak yang mempunyai tarikh jalanan invois sama, transaksi digabungkan ke dalam satu invois yang mempunyai dua baris invois.</span><span class="sxs-lookup"><span data-stu-id="83a81-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="83a81-127">Jika tiada transaksi untuk dicipta invois, kerja melangkau penciptaan invois.</span><span class="sxs-lookup"><span data-stu-id="83a81-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="83a81-128">Selepas **ProcessRunner** selesai berjalan, ia memanggil **ProcessRunCaller**, memberikan masa akhir, dan ditutup.</span><span class="sxs-lookup"><span data-stu-id="83a81-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="83a81-129">**ProcessRunCaller** kemudian memulakan pemasa yang berjalan 24 jam dari tarikh akhir khusus.</span><span class="sxs-lookup"><span data-stu-id="83a81-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="83a81-130">Pada penghujung pemasa, **ProcessRunCaller** ditutup.</span><span class="sxs-lookup"><span data-stu-id="83a81-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="83a81-131">Kerja proses kelompok untuk mencipta invois adalah kerja berulang.</span><span class="sxs-lookup"><span data-stu-id="83a81-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="83a81-132">Jika proses kelompok ini berjalan banyak kali, berbilang tika kerja dicipta dan menyebabkan ralat.</span><span class="sxs-lookup"><span data-stu-id="83a81-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="83a81-133">Maka, anda perlu memulakan proses kelompol hanya satu kali, dan anda hendaklah mulakan semula jika ia berhenti berjalan.</span><span class="sxs-lookup"><span data-stu-id="83a81-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="83a81-134">Penginvoisan kelompok hanya berjalan untuk baris kontrak projek yang dikonfigurasikan oleh jadual invois.</span><span class="sxs-lookup"><span data-stu-id="83a81-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="83a81-135">Baris kontrak dengan kaedah pengebilan harga tetap mesti mempunyai pencapaian yang dikonfigurasikan.</span><span class="sxs-lookup"><span data-stu-id="83a81-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="83a81-136">Baris kontrak projek dengan kaedah pengebilan masa dan bahan akan memerlukan persediaan jadual invois berdasarkan tarikh.</span><span class="sxs-lookup"><span data-stu-id="83a81-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="83a81-137">Perkara yang sama digunakan pada baris kontrak berasaskan projek.</span><span class="sxs-lookup"><span data-stu-id="83a81-137">The same applies to a project-based contract line.</span></span>     
