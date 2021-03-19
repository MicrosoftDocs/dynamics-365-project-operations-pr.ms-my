---
title: Aliran kerja Pengurusan perbelanjaan
description: Topik ini menerangkan cara anda boleh menggunakan sistem aliran kerja dalam Microsoft Dynamics 365 Finance, untuk menyediakan proses semakan untuk laporan perbelanjaan dalam Pengurusan perbelanjaan.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fde336f53d72e9ddf38c5123d9e774a4c3a22a28
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271679"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="4c89c-103">Aliran kerja Pengurusan perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="4c89c-103">Expense management workflow</span></span>

<span data-ttu-id="4c89c-104">Anda boleh menggunakan sistem aliran kerja untuk menyediakan proses semakan untuk laporan perbelanjaan dalam Pengurusan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="4c89c-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="4c89c-105">Anda boleh menyediakan aliran kerja yang menggunakan kriteria berikut untuk menentukan orang yang meluluskan laporan perbelanjaan:</span><span class="sxs-lookup"><span data-stu-id="4c89c-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="4c89c-106">Hierarki pelaporan pekerja dan had kelulusan yang dipratetapkan</span><span class="sxs-lookup"><span data-stu-id="4c89c-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="4c89c-107">Kelulusan berbilang tahap yang menyokong pelulus interim dan pelulus akhir</span><span class="sxs-lookup"><span data-stu-id="4c89c-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="4c89c-108">Dimensi kewangan dan tanggungjawab projek</span><span class="sxs-lookup"><span data-stu-id="4c89c-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="4c89c-109">Penugasan kepada pengguna atau kumpulan pengguna tertentu</span><span class="sxs-lookup"><span data-stu-id="4c89c-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="4c89c-110">Kelulusan aliran kerja boleh dicipta untuk laporan perbelanjaan, permintaan perjalanan, pendahuluan tunai dan pemulihan cukai nilai tambah (VAT).</span><span class="sxs-lookup"><span data-stu-id="4c89c-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="4c89c-111">**Contoh**</span><span class="sxs-lookup"><span data-stu-id="4c89c-111">**Example**</span></span>

<span data-ttu-id="4c89c-112">Proses berikut ialah contoh aliran kerja pengurusan perbelanjaan untuk laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="4c89c-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="4c89c-113">Pekerja mencipta dan menyimpan laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="4c89c-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="4c89c-114">Pekerja menyerahkan laporan perbelanjaan untuk kelulusan.</span><span class="sxs-lookup"><span data-stu-id="4c89c-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="4c89c-115">Pelulus dikenal pasti berdasarkan peraturan yang ditakrifkan apabila aliran kerja disediakan.</span><span class="sxs-lookup"><span data-stu-id="4c89c-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="4c89c-116">Pelulus menerima pemberitahuan bahawa laporan perbelanjaan sedia untuk kelulusan.</span><span class="sxs-lookup"><span data-stu-id="4c89c-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="4c89c-117">Pelulus menyemak laporan perbelanjaan dan mengesahkan bahawa syarat berikut dipenuhi:</span><span class="sxs-lookup"><span data-stu-id="4c89c-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="4c89c-118">Perbelanjaan tidak melanggar apa-apa dasar perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="4c89c-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="4c89c-119">Jika perbelanjaan melanggar dasar, pelulus mengesahkan bahawa laporan perbelanjaan termasuk justifikasi perniagaan yang sah.</span><span class="sxs-lookup"><span data-stu-id="4c89c-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="4c89c-120">Resit elektronik dilampirkan pada laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="4c89c-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="4c89c-121">Pelulus meluluskan laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="4c89c-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="4c89c-122">Laporan perbelanjaan ditugaskan kepada penyelaras Akaun belum bayar untuk penyiaran.</span><span class="sxs-lookup"><span data-stu-id="4c89c-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="4c89c-123">Salah satu langkah berikut berlaku, bergantung pada sama ada penyiaran automatik dikonfigurasikan:</span><span class="sxs-lookup"><span data-stu-id="4c89c-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="4c89c-124">Jika penyiaran automatik dikonfigurasikan, laporan perbelanjaan diproses untuk pembayaran, dan status laporan perbelanjaan dikemas kini.</span><span class="sxs-lookup"><span data-stu-id="4c89c-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="4c89c-125">Jika penyiaran automatik tidak dikonfigurasikan, penyelaras Akaun belum bayar mengesahkan bahawa semua resit asal telah diserahkan, dan bahawa resit adalah selaras dengan perbelanjaan pada laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="4c89c-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="4c89c-126">Semua kod cukai yang dimasukkan pada laporan perbelanjaan juga mesti disahkan sebagai betul.</span><span class="sxs-lookup"><span data-stu-id="4c89c-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="4c89c-127">Selepas keperluan ini disahkan, laporan perbelanjaan akan disiarkan.</span><span class="sxs-lookup"><span data-stu-id="4c89c-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="4c89c-128">Selepas laporan perbelanjaan disiarkan, pembayaran dibenarkan untuk laporan perbelanjaan, dan pekerja akan dibayar balik.</span><span class="sxs-lookup"><span data-stu-id="4c89c-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]