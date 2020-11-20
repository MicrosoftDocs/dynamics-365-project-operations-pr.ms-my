---
title: Entri perbelanjaan (ringan)
description: Topik ini memberikan maklumat tentang cara untuk bekerja dengan entri perbelanjaan dalam pelaksanaan ringan.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 536c961593599df8e7e2986f92259b0e690eae8b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121094"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="dd1d9-103">Entri perbelanjaan (ringan)</span><span class="sxs-lookup"><span data-stu-id="dd1d9-103">Expense entry (lite)</span></span>

<span data-ttu-id="dd1d9-104">_**Gunakan pada:** Pelaksanaan ringan - urusan dengan invois proforma_</span><span class="sxs-lookup"><span data-stu-id="dd1d9-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dd1d9-105">Asas, atau ringan, pengurusan perbelanjaan ialah keupayaan untuk merekodkan perbelanjaan mudah.</span><span class="sxs-lookup"><span data-stu-id="dd1d9-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="dd1d9-106">Anda boleh merekodkan perbelanjaan terhadap projek, dan kemudian pelulus projek akan menyemak dan meluluskannya.</span><span class="sxs-lookup"><span data-stu-id="dd1d9-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="dd1d9-107">Untuk mendapatkan maklumat lanjut tentang keupayaan perbelanjaan dalam Dynamics 365 Project Operations, lihat [Gambaran keseluruhan perbelanjaan](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="dd1d9-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="dd1d9-108">Merekodkan perbelanjaan asas</span><span class="sxs-lookup"><span data-stu-id="dd1d9-108">Capture a basic expense</span></span>

<span data-ttu-id="dd1d9-109">Anda boleh merekodkan perbelanjaan anda supaya anda boleh menyerahkannya kepada pelulus.</span><span class="sxs-lookup"><span data-stu-id="dd1d9-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="dd1d9-110">Pergi ke **Perbelanjaan** dan pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="dd1d9-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="dd1d9-111">Pada halaman **Perbelanjaan Baharu**, masukkan maklumat perbelanjaan yang diperlukan dan kemudian pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="dd1d9-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="dd1d9-112">Menyerahkan perbelanjaan asas</span><span class="sxs-lookup"><span data-stu-id="dd1d9-112">Submit a basic expense</span></span>

<span data-ttu-id="dd1d9-113">Selepas anda selesai merekodkan semua perbelanjaan anda, dan anda bersedia untuk mendapatkan kelulusan untuknya, anda mesti menyerahkannya.</span><span class="sxs-lookup"><span data-stu-id="dd1d9-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="dd1d9-114">Pergi ke **Perbelanjaan** dan pilih perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="dd1d9-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="dd1d9-115">Atau, pilih semua perbelanjaan dengan menggunakan kotak semak pada pengepala.</span><span class="sxs-lookup"><span data-stu-id="dd1d9-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="dd1d9-116">Pilih **Serahkan**.</span><span class="sxs-lookup"><span data-stu-id="dd1d9-116">Select **Submit**.</span></span> <span data-ttu-id="dd1d9-117">Sistem memproses entri yang dipilih dan kemudian mencipta permintaan kelulusan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="dd1d9-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="dd1d9-118">Tarik balik perbelanjaan asas</span><span class="sxs-lookup"><span data-stu-id="dd1d9-118">Recall a basic expense</span></span>

<span data-ttu-id="dd1d9-119">Apabila anda menyerahkan perbelanjaan dengan tidak sengaja, anda boleh menariknya balik.</span><span class="sxs-lookup"><span data-stu-id="dd1d9-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="dd1d9-120">Masa yang diperlukan untuk menarik balik entri perbelanjaan bergantung pada peringkat kelulusannya.</span><span class="sxs-lookup"><span data-stu-id="dd1d9-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="dd1d9-121">Jika pelulus belum meluluskan entri itu, tarik balik boleh berlaku dengan serta-merta.</span><span class="sxs-lookup"><span data-stu-id="dd1d9-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="dd1d9-122">Walau bagaimanapun, jika entri telah diluluskan, pelulus diminta untuk meluluskan tarik balik dan membalikkan transaksi tersebut.</span><span class="sxs-lookup"><span data-stu-id="dd1d9-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="dd1d9-123">Pergi ke **Perbelanjaan**, dan kemudian, dalam senarai perbelanjaan, pilih perbelanjaan untuk ditarik balik.</span><span class="sxs-lookup"><span data-stu-id="dd1d9-123">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="dd1d9-124">Pilih **Tarik balik**.</span><span class="sxs-lookup"><span data-stu-id="dd1d9-124">Select **Recall**.</span></span> <span data-ttu-id="dd1d9-125">Jika entri perbelanjaan belum lagi diluluskan, sistem menarik balik ia dengan segera.</span><span class="sxs-lookup"><span data-stu-id="dd1d9-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="dd1d9-126">Jika entri perbelanjaan telah diluluskan, permintaan tarik balik dibuat untuk memberitahu pelulus yang anda mahu membalikkan perbelanjaan itu.</span><span class="sxs-lookup"><span data-stu-id="dd1d9-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="dd1d9-127">Pelulus akan mengesahkan yang pembalikan boleh dilakukan dan entri akan dikembalikan.</span><span class="sxs-lookup"><span data-stu-id="dd1d9-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="dd1d9-128">Padamkan perbelanjaan asas</span><span class="sxs-lookup"><span data-stu-id="dd1d9-128">Delete a basic expense</span></span>

<span data-ttu-id="dd1d9-129">Perbelanjaan yang belum diserahkan boleh dipadamkan.</span><span class="sxs-lookup"><span data-stu-id="dd1d9-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="dd1d9-130">Untuk memadamkan perbelanjaan yang telah diserahkan, anda mesti menarik balik perbelanjaan itu terlebih dahulu.</span><span class="sxs-lookup"><span data-stu-id="dd1d9-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="dd1d9-131">Lihat juga</span><span class="sxs-lookup"><span data-stu-id="dd1d9-131">See also</span></span>

- [<span data-ttu-id="dd1d9-132">Gambaran keseluruhan kelulusan</span><span class="sxs-lookup"><span data-stu-id="dd1d9-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
