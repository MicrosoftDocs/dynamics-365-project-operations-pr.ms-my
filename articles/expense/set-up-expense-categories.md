---
title: Sediakan kategori perbelanjaan
description: Topik ini memberikan maklumat tentang cara menyediakan kategori perbelanjaan dan kategori dikongsi untuk laporan perbelanjaan.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081118"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="be70c-103">Sediakan kategori perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="be70c-103">Set up expense categories</span></span>

<span data-ttu-id="be70c-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="be70c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="be70c-105">Apabila pekerja cipta laporan perbelanjaan, setiap perbelanjaan yang mereka rekod mesti dikaitkan dengan kategori perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="be70c-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="be70c-106">Kategori perbelanjaan diperoleh daripada kategori dikongsi yang boleh dikongsi merentasi entiti yang sah dalam organisasi anda.</span><span class="sxs-lookup"><span data-stu-id="be70c-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="be70c-107">Bergantung pada cara organisasi anda ditakrifkan, kategori perbelanjaan ini juga boleh dikongsi di kawasan lain.</span><span class="sxs-lookup"><span data-stu-id="be70c-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="be70c-108">Berdasarkan definisi organisasi dan panduan anda daripada pasukan pelaksanaan, anda mesti menentukan sama ada kategori yang digunakan dalam Pengurusan perbelanjaan akan digunakan hanya dalam Pengurusan perbelanjaan atau harus dikongsi di kawasan lain.</span><span class="sxs-lookup"><span data-stu-id="be70c-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="be70c-109">Kategori ini boleh dikongsi di antara Pengurusan projek dan perakaunan dan Pengurusan perbelanjaan, atau antara Pengurusan projek dan perakaunan dan Pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="be70c-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="be70c-110">Walau bagaimanapun, ia tidak boleh dikongsi antara Pengurusan perbelanjaan dan Pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="be70c-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="be70c-111">Sebelum anda boleh memulakan proses persediaan, keputusan berikut mesti dibuat untuk setiap kategori perbelanjaan:</span><span class="sxs-lookup"><span data-stu-id="be70c-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="be70c-112">Apakah itu kategori perbelanjaan?</span><span class="sxs-lookup"><span data-stu-id="be70c-112">What is the expense category?</span></span> <span data-ttu-id="be70c-113">Contohnya termasuk kategori untuk penerbangan, hotel, atau perbatuan.</span><span class="sxs-lookup"><span data-stu-id="be70c-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="be70c-114">Bolehkah kategori perbelanjaan juga digunakan dalam Pengurusan projek dan perakaunan?</span><span class="sxs-lookup"><span data-stu-id="be70c-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="be70c-115">Jika ia boleh, anda juga mesti membuat keputusan berikut:</span><span class="sxs-lookup"><span data-stu-id="be70c-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="be70c-116">Akaun kos manakah akan digunakan untuk perbelanjaan yang berikut?</span><span class="sxs-lookup"><span data-stu-id="be70c-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="be70c-117">Kos</span><span class="sxs-lookup"><span data-stu-id="be70c-117">Cost</span></span>
        - <span data-ttu-id="be70c-118">Peruntukan gaji</span><span class="sxs-lookup"><span data-stu-id="be70c-118">Payroll allocation</span></span>
        - <span data-ttu-id="be70c-119">WIP-nilai kos</span><span class="sxs-lookup"><span data-stu-id="be70c-119">WIP-cost value</span></span>
        - <span data-ttu-id="be70c-120">Kos-item</span><span class="sxs-lookup"><span data-stu-id="be70c-120">Cost-item</span></span>
        - <span data-ttu-id="be70c-121">WIP-nilai kos-item</span><span class="sxs-lookup"><span data-stu-id="be70c-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="be70c-122">Kerugian terakru</span><span class="sxs-lookup"><span data-stu-id="be70c-122">Accrued loss</span></span>
        - <span data-ttu-id="be70c-123">WIP-kerugian terakru</span><span class="sxs-lookup"><span data-stu-id="be70c-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="be70c-124">Akaun hasil manakah yang akan digunakan untuk sumber hasil berikut?</span><span class="sxs-lookup"><span data-stu-id="be70c-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="be70c-125">Hasil diinvois</span><span class="sxs-lookup"><span data-stu-id="be70c-125">Invoiced revenue</span></span>
        - <span data-ttu-id="be70c-126">Hasil terakru-nilai jualan</span><span class="sxs-lookup"><span data-stu-id="be70c-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="be70c-127">WIP-nilai jualan</span><span class="sxs-lookup"><span data-stu-id="be70c-127">WIP-sales value</span></span>
        - <span data-ttu-id="be70c-128">Hasil terakru-pengeluaran</span><span class="sxs-lookup"><span data-stu-id="be70c-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="be70c-129">WIP-pengeluaran</span><span class="sxs-lookup"><span data-stu-id="be70c-129">WIP-production</span></span>
        - <span data-ttu-id="be70c-130">Hasil terakru-keuntungan</span><span class="sxs-lookup"><span data-stu-id="be70c-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="be70c-131">WIP-keuntungan</span><span class="sxs-lookup"><span data-stu-id="be70c-131">WIP-profit</span></span>
        - <span data-ttu-id="be70c-132">Hasil terakru-langganan</span><span class="sxs-lookup"><span data-stu-id="be70c-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="be70c-133">WIP-langganan</span><span class="sxs-lookup"><span data-stu-id="be70c-133">WIP-subscription</span></span>

- <span data-ttu-id="be70c-134">Apakah itu jenis perbelanjaan?</span><span class="sxs-lookup"><span data-stu-id="be70c-134">What is the expense type?</span></span>
- <span data-ttu-id="be70c-135">Apakah itu kaedah pembayaran lalai untuk kategori perbelanjaan?</span><span class="sxs-lookup"><span data-stu-id="be70c-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="be70c-136">Adakah perbelanjaan dalam kategori perbelanjaan perlu diperincikan?</span><span class="sxs-lookup"><span data-stu-id="be70c-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="be70c-137">Apakah itu akaun lalai utama untuk kategori perbelanjaan?</span><span class="sxs-lookup"><span data-stu-id="be70c-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="be70c-138">Apakah itu kumpulan cukai jualan item lalai untuk kategori perbelanjaan?</span><span class="sxs-lookup"><span data-stu-id="be70c-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="be70c-139">Adakah kaedah pembayaran tambahan dibenarkan untuk kategori perbelanjaan?</span><span class="sxs-lookup"><span data-stu-id="be70c-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="be70c-140">Jika ya, apakah itu?</span><span class="sxs-lookup"><span data-stu-id="be70c-140">If so, what are they?</span></span>
- <span data-ttu-id="be70c-141">Adakah terdapat subkategori dalam kategori perbelanjaan ini?</span><span class="sxs-lookup"><span data-stu-id="be70c-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="be70c-142">Jika terdapat subkategori, anda juga mesti membuat keputusan berikut:</span><span class="sxs-lookup"><span data-stu-id="be70c-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="be70c-143">Adakah sebarang subkategori dikecualikan daripada pemulihan cukai?</span><span class="sxs-lookup"><span data-stu-id="be70c-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="be70c-144">Apakah itu kumpulan cukai jualan item subkategori?</span><span class="sxs-lookup"><span data-stu-id="be70c-144">What is the item sales tax group of the subcategories?</span></span>
