---
title: Berbilang pelulus pada laporan perbelanjaan
description: Topik ini menyediakan maklumat tentang laporan perbelanjaan yang memerlukan kelulusan oleh berbilang orang.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0fbe1c93c5359a6be493e3c4e1b27b06dbb48002
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271724"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="2b2ab-103">Berbilang pelulus pada laporan perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="2b2ab-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="2b2ab-104">Bergantung pada dasar kelulusan perbelanjaan organisasi anda, lebih daripada satu orang mungkin perlu meluluskan laporan perbelanjaan yang diserahkan oleh pekerja.</span><span class="sxs-lookup"><span data-stu-id="2b2ab-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="2b2ab-105">Apabila anda menyediakan proses aliran kerja untuk kelulusan laporan perbelanjaan, anda boleh menambah elemen aliran kerja yang termasuk tugas atau langkah untuk satu atau lebih laporan pelulus.</span><span class="sxs-lookup"><span data-stu-id="2b2ab-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="2b2ab-106">Contohnya, anda mungkin mengkehendaki semua laporan perbelanjaan diluluskan dahulu oleh pengurus pekerja yang menyerahkan laporan dan kemudian diluluskan oleh Penyelaras akaun belum bayar.</span><span class="sxs-lookup"><span data-stu-id="2b2ab-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="2b2ab-107">Jika anda memutuskan untuk memerlukan berbilang pelulus laporan perbelanjaan, anda boleh menambah elemen aliran kerja dalam mana-mana cara berikut:</span><span class="sxs-lookup"><span data-stu-id="2b2ab-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="2b2ab-108">Tambah satu elemen kelulusan yang mempunyai satu langkah.</span><span class="sxs-lookup"><span data-stu-id="2b2ab-108">Add one approval element that has one step.</span></span> <span data-ttu-id="2b2ab-109">Contohnya, langkah mungkin memerlukan laporan perbelanjaan ditugaskan kepada kumpulan pengguna dan ia akan diluluskan oleh 50 peratus daripada ahli kumpulan pengguna.</span><span class="sxs-lookup"><span data-stu-id="2b2ab-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="2b2ab-110">Tambah satu elemen kelulusan yang mempunyai berbilang langkah.</span><span class="sxs-lookup"><span data-stu-id="2b2ab-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="2b2ab-111">Contohnya, elemen kelulusan mungkin mempunyai langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="2b2ab-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="2b2ab-112">Pengurus pekerja yang menyerahkan laporan perbelanjaan meluluskannya.</span><span class="sxs-lookup"><span data-stu-id="2b2ab-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="2b2ab-113">Kerani akaun belum bayar mengesahkan resit dan item laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="2b2ab-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="2b2ab-114">Pemilik bajet meluluskan laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="2b2ab-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="2b2ab-115">Tambah berbilang elemen kelulusan, setiap satunya mempunyai satu langkah.</span><span class="sxs-lookup"><span data-stu-id="2b2ab-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="2b2ab-116">Contohnya, anda mungkin menambahkan elemen kelulusan berasingan bagi setiap langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="2b2ab-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="2b2ab-117">Pengurus pekerja akan meluluskan laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="2b2ab-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="2b2ab-118">Pemilik bajet meluluskan laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="2b2ab-118">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]