---
title: Takrifkan dasar perbelanjaan
description: Anda boleh menakrifkan dasar perbelanjaan yang mesti dipatuhi oleh pekerja apabila memasukkan dan menyerahkan laporan perbelanjaan dan permintaan perjalanan.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fa108db9aa0d2a22c35d2d046917ddae1f3842c1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001887"
---
# <a name="define-expense-policies"></a><span data-ttu-id="ee1c9-103">Takrifkan dasar perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="ee1c9-103">Define expense policies</span></span>

<span data-ttu-id="ee1c9-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="ee1c9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ee1c9-105">Anda boleh menakrifkan dasar yang mesti dipatuhi oleh pekerja apabila memasukkan dan menyerahkan laporan perbelanjaan dan permintaan perjalanan.</span><span class="sxs-lookup"><span data-stu-id="ee1c9-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="ee1c9-106">Pelaksanaan dasar perbelanjaan boleh membantu anda mengurus perbelanjaan secara berkesan.</span><span class="sxs-lookup"><span data-stu-id="ee1c9-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="ee1c9-107">Contohnya, anda boleh menetapkan dasar untuk perbelanjaan Hotel di New York City yang menyatakan bahawa perbelanjaan bagi setiap malam tidak boleh melebihi USD 250.</span><span class="sxs-lookup"><span data-stu-id="ee1c9-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="ee1c9-108">Jika pekerja menyerahkan laporan perbelanjaan atau permintaan perjalanan yang kadar bilik melebihi amaun ini, sistem akan memberitahu</span><span class="sxs-lookup"><span data-stu-id="ee1c9-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="ee1c9-109">pekerja bahawa amaun dasar untuk perbelanjaan telah melebihi.</span><span class="sxs-lookup"><span data-stu-id="ee1c9-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="ee1c9-110">Anda boleh mengkonfigurasi message yang akan diterima oleh pekerja apabila anda</span><span class="sxs-lookup"><span data-stu-id="ee1c9-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="ee1c9-111">menakrifkan dasar.</span><span class="sxs-lookup"><span data-stu-id="ee1c9-111">define the policy.</span></span>      
        
<span data-ttu-id="ee1c9-112">Anda boleh menakrifkan tiga jenis dasar:</span><span class="sxs-lookup"><span data-stu-id="ee1c9-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="ee1c9-113">**Amaran**: Membenarkan pekerja menyerahkan laporan perbelanjaan atau permintaan perjalanan tetapi perbelanjaan akan ditandakan untuk semua pelulus dan</span><span class="sxs-lookup"><span data-stu-id="ee1c9-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="ee1c9-114">untuk pelaporan kemudian.</span><span class="sxs-lookup"><span data-stu-id="ee1c9-114">for later reporting.</span></span>        

- <span data-ttu-id="ee1c9-115">**Ralat**: Memerlukan pekerja menyemak semula perbelanjaan untuk mematuhi dasar sebelum menyerahkan laporan perbelanjaan atau permintaan perjalanan.</span><span class="sxs-lookup"><span data-stu-id="ee1c9-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="ee1c9-116">**Justifikasi**: Memerlukan pekerja atau Pengurus memasukkan justifikasi amaun melebihi jumlah dasar sebelum menyerahkan laporan perbelanjaan atau permintaan perjalanan.</span><span class="sxs-lookup"><span data-stu-id="ee1c9-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="ee1c9-117">Tips dasar</span><span class="sxs-lookup"><span data-stu-id="ee1c9-117">Policy tips</span></span>
<span data-ttu-id="ee1c9-118">Berikut adalah beberapa cadangan yang dapat membantu anda semasa membuat dasar baru untuk pengurusan perbelanjaan:</span><span class="sxs-lookup"><span data-stu-id="ee1c9-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="ee1c9-119">Dasar adalah tarikh berkuatkuasa bermaksud dasar tidak akan berkuatkuasa jika ianya dibuat dengan tarikh selepas tarikh perbelanjaan itu berlaku.</span><span class="sxs-lookup"><span data-stu-id="ee1c9-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="ee1c9-120">Contohnya, anda mencipta dasar baharu hari ini untuk menguatkuasakan perbelanjaan hidangan maksimum sebanyak $50.</span><span class="sxs-lookup"><span data-stu-id="ee1c9-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="ee1c9-121">Sebarang perbelanjaan sedia ada yang dimasukkan pada hari semalam tidak akan disemak berdasarkan dasar ini.</span><span class="sxs-lookup"><span data-stu-id="ee1c9-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="ee1c9-122">Apabila mencipta dasar untuk kategori perbelanjaan yang boleh diperincikan, pertimbangkan untuk menambah syarat bagi jenis baris perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="ee1c9-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="ee1c9-123">Sesetengah dasar seperti yang memerlukan resit mungkin tidak masuk akal untuk baris yang diperincikan.</span><span class="sxs-lookup"><span data-stu-id="ee1c9-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="ee1c9-124">Dalam keadaan ini, dasar hanya digunakan untuk baris pengepala atau baris yang tidak diperincikan.</span><span class="sxs-lookup"><span data-stu-id="ee1c9-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="ee1c9-125">Dasar pengurusan perbelanjaan dinilai berdasarkan entiti sumber secara lalai.</span><span class="sxs-lookup"><span data-stu-id="ee1c9-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="ee1c9-126">Untuk senario antara syarikat, sebaliknya anda boleh menetapkan dasar untuk dinilai berdasarkan entiti destinasi (entiti pinjaman).</span><span class="sxs-lookup"><span data-stu-id="ee1c9-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="ee1c9-127">Untuk menjalankan dasar berdasarkan entiti destinasi, hidupkan ciri **Nilaikan entiti undang-undang peminjaman berdasarkan dasar** dalam ruang kerja **Pengurusan ciri**.</span><span class="sxs-lookup"><span data-stu-id="ee1c9-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="ee1c9-128">Bila untuk menilai dasar</span><span class="sxs-lookup"><span data-stu-id="ee1c9-128">When to evaluate policies</span></span>

<span data-ttu-id="ee1c9-129">Dalam parameter pengurusan perbelanjaan, anda boleh memilih untuk menilai dasar pengurusan perbelanjaan apabila baris disimpan atau apabila laporan perbelanjaan diserahkan.</span><span class="sxs-lookup"><span data-stu-id="ee1c9-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="ee1c9-130">Jika anda memilih untuk menilai apabila baris disimpan, pengguna akan mempunyai keterlihatan awal kepada apa yang mereka perlu lakukan untuk melengkapkan laporan perbelanjaan mereka sekaligus.</span><span class="sxs-lookup"><span data-stu-id="ee1c9-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="ee1c9-131">Jika tidak, anda boleh melambatkan penilaian dasar dan menjimatkan masa dengan mengesahkan di akhir, semasa penyerahan aliran kerja.</span><span class="sxs-lookup"><span data-stu-id="ee1c9-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]