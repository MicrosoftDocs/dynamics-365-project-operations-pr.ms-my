---
title: Sediakan dasar perbelanjaan
description: Anda boleh menyediakan dasar perbelanjaan yang mesti dipatuhi oleh pekerja anda apabila memasukkan dan menyerahkan laporan perbelanjaan dan permintaan perjalanan dalam Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab99c0ec769eb2e0914fc7d993f83d20e2c327f6
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960708"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="509ca-103">Sediakan dasar perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="509ca-103">Set up expense policies</span></span>

<span data-ttu-id="509ca-104">Anda boleh menakrifkan dasar yang mesti dipatuhi oleh pekerja apabila memasukkan dan menyerahkan laporan perbelanjaan dan permintaan perjalanan.</span><span class="sxs-lookup"><span data-stu-id="509ca-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="509ca-105">Pelaksanaan dasar perbelanjaan boleh membantu anda mengurus perbelanjaan secara berkesan.</span><span class="sxs-lookup"><span data-stu-id="509ca-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="509ca-106">Contohnya, anda boleh menetapkan dasar untuk perbelanjaan Hotel di New York City yang menyatakan bahawa perbelanjaan bagi setiap malam tidak boleh melebihi USD 250.</span><span class="sxs-lookup"><span data-stu-id="509ca-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="509ca-107">Jika pekerja menyerahkan laporan perbelanjaan atau permintaan perjalanan yang kadar bilik melebihi amaun ini, sistem akan memberitahu</span><span class="sxs-lookup"><span data-stu-id="509ca-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="509ca-108">pekerja bahawa amaun dasar untuk perbelanjaan telah melebihi.</span><span class="sxs-lookup"><span data-stu-id="509ca-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="509ca-109">Anda boleh mengkonfigurasi message yang akan diterima oleh pekerja apabila anda</span><span class="sxs-lookup"><span data-stu-id="509ca-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="509ca-110">menakrifkan dasar.</span><span class="sxs-lookup"><span data-stu-id="509ca-110">define the policy.</span></span>      
        
<span data-ttu-id="509ca-111">Anda boleh menakrifkan tiga jenis dasar:</span><span class="sxs-lookup"><span data-stu-id="509ca-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="509ca-112">Amaran – Membenarkan pekerja menyerahkan laporan perbelanjaan atau permintaan perjalanan tetapi perbelanjaan akan ditandakan untuk semua pelulus dan</span><span class="sxs-lookup"><span data-stu-id="509ca-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="509ca-113">untuk pelaporan kemudian.</span><span class="sxs-lookup"><span data-stu-id="509ca-113">for later reporting.</span></span>        

- <span data-ttu-id="509ca-114">Ralat – Memerlukan pekerja menyemak semula perbelanjaan untuk mematuhi dasar sebelum menyerahkan laporan perbelanjaan atau permintaan perjalanan.</span><span class="sxs-lookup"><span data-stu-id="509ca-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="509ca-115">Justifikasi – Memerlukan pekerja atau pengurus memasukkan justifikasi amaun melebihi jumlah dasar sebelum menyerahkan laporan perbelanjaan atau permintaan perjalanan.</span><span class="sxs-lookup"><span data-stu-id="509ca-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="509ca-116">Tips dasar</span><span class="sxs-lookup"><span data-stu-id="509ca-116">Policy tips</span></span>
<span data-ttu-id="509ca-117">Berikut adalah beberapa cadangan yang dapat membantu anda semasa mencipta dasar baharu untuk pengurusan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="509ca-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="509ca-118">Dasar adalah tarikh kuat kuasa dan tidak akan berkuat kuasa jika dasar dicipta dengan tarikh selepas tarikh perbelanjaan itu berlaku.</span><span class="sxs-lookup"><span data-stu-id="509ca-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="509ca-119">Sebagai contoh, jika anda mencipta dasar baharu hari ini untuk menguatkuasakan perbelanjaan makan maksimum sebanyak $50 berbanding sebarang perbelanjaan sedia ada yang dimasukkan semalam tidak akan disemak terhadap dasar ini.</span><span class="sxs-lookup"><span data-stu-id="509ca-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="509ca-120">Apabila mencipta dasar untuk kategori perbelanjaan yang boleh diperincikan, pertimbangkan untuk menambah syarat bagi jenis baris perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="509ca-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="509ca-121">Sesetengah dasar seperti yang memerlukan resit mungkin tidak masuk akal untuk baris yang diperincikan dan sepatutnya digunakan untuk baris pengepala atau baris yang tidak diperincikan.</span><span class="sxs-lookup"><span data-stu-id="509ca-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="509ca-122">Dasar pengurusan perbelanjaan dinilai berdasarkan entiti sumber secara lalai.</span><span class="sxs-lookup"><span data-stu-id="509ca-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="509ca-123">Untuk senario antara syarikat, sebaliknya anda boleh menetapkan dasar untuk dinilai berdasarkan entiti destinasi (entiti pinjaman).</span><span class="sxs-lookup"><span data-stu-id="509ca-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="509ca-124">Untuk menjalankan dasar terhadap entiti destinasi, hidupkan ciri "Nilaikan dasar Perbelanjaan terhadap peminjaman entiti undang-undang" dalam ruang kerja **Pengurusan Ciri**.</span><span class="sxs-lookup"><span data-stu-id="509ca-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="509ca-125">Bila untuk menilai dasar</span><span class="sxs-lookup"><span data-stu-id="509ca-125">When to evaluate policies</span></span>

<span data-ttu-id="509ca-126">Dalam parameter pengurusan perbelanjaan, terdapat pilihan untuk sama ada menilai dasar pengurusan perbelanjaan apabila baris disimpan atau apabila laporan perbelanjaan diserahkan.</span><span class="sxs-lookup"><span data-stu-id="509ca-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="509ca-127">Jika anda memilih untuk menilai apabila baris disimpan ini memastikan pengguna mempunyai keterlihatan awal kepada perkara yang mereka perlu lakukan untuk melengkapkan laporan perbelanjaan mereka sekaligus.</span><span class="sxs-lookup"><span data-stu-id="509ca-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="509ca-128">Jika tidak, anda boleh melambatkan penilaian dasar dan menjimatkan masa jika anda mempunyai pengesahan terjadi di akhir, semasa penyerahan aliran kerja.</span><span class="sxs-lookup"><span data-stu-id="509ca-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
