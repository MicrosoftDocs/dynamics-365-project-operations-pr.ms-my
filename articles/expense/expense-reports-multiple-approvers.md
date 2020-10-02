---
title: Laporan perbelanjaan dan berbilang pelulus
description: Topik ini menyediakan maklumat tentang laporan perbelanjaan yang memerlukan kelulusan oleh lebih daripada satu orang.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 818092dd631d07cc0a7d63c9eec51eeff4f67ffe
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897102"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="e3cbe-103">Laporan perbelanjaan dan berbilang pelulus</span><span class="sxs-lookup"><span data-stu-id="e3cbe-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="e3cbe-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="e3cbe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e3cbe-105">Bergantung pada dasar kelulusan perbelanjaan organisasi anda, lebih daripada satu orang mungkin perlu meluluskan laporan perbelanjaan yang diserahkan.</span><span class="sxs-lookup"><span data-stu-id="e3cbe-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="e3cbe-106">Apabila anda menyediakan proses aliran kerja untuk kelulusan laporan perbelanjaan, anda boleh menambah elemen aliran kerja yang termasuk tugas atau langkah untuk satu atau lebih laporan pelulus.</span><span class="sxs-lookup"><span data-stu-id="e3cbe-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="e3cbe-107">Contohnya, anda mungkin memerlukan semua laporan perbelanjaan yang diluluskan oleh dua orang berasingan, pengurus pekerja yang menyerahkan laporan dan Penyelaras Akaun belum bayar.</span><span class="sxs-lookup"><span data-stu-id="e3cbe-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="e3cbe-108">Jika anda memutuskan untuk memerlukan berbilang pelulus laporan perbelanjaan, anda boleh menambah elemen aliran kerja dalam mana-mana cara berikut:</span><span class="sxs-lookup"><span data-stu-id="e3cbe-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="e3cbe-109">Tambah satu elemen kelulusan yang mempunyai satu langkah.</span><span class="sxs-lookup"><span data-stu-id="e3cbe-109">Add one approval element that has one step.</span></span> <span data-ttu-id="e3cbe-110">Contohnya, langkah mungkin memerlukan laporan perbelanjaan ditugaskan kepada kumpulan pengguna dan ia akan diluluskan oleh 50 peratus daripada ahli kumpulan pengguna.</span><span class="sxs-lookup"><span data-stu-id="e3cbe-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="e3cbe-111">Tambah satu elemen kelulusan yang mempunyai berbilang langkah.</span><span class="sxs-lookup"><span data-stu-id="e3cbe-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="e3cbe-112">Contohnya, elemen kelulusan mungkin mempunyai langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="e3cbe-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="e3cbe-113">Pengurus pekerja yang menyerahkan laporan perbelanjaan meluluskannya.</span><span class="sxs-lookup"><span data-stu-id="e3cbe-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="e3cbe-114">Kerani akaun belum bayar mengesahkan resit dan item laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="e3cbe-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="e3cbe-115">Pemilik bajet meluluskan laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="e3cbe-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="e3cbe-116">Tambah berbilang elemen kelulusan, setiap satunya mempunyai satu langkah.</span><span class="sxs-lookup"><span data-stu-id="e3cbe-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="e3cbe-117">Contohnya, anda mungkin menambahkan elemen kelulusan berasingan bagi setiap langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="e3cbe-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="e3cbe-118">Pengurus pekerja akan meluluskan laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="e3cbe-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="e3cbe-119">Pemilik bajet meluluskan laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="e3cbe-119">The budget owner approves the expense report.</span></span>
