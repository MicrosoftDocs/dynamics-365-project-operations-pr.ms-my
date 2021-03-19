---
title: Sediakan aliran kerja Pengurusan perbelanjaan
description: Anda boleh menyediakan proses aliran kerja untuk menyemak dan meluluskan dokumen perjalanan dan perbelanjaan.
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
ms.openlocfilehash: 36ab1edc4769013684fa9248e6c5eac025637bbd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271634"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="ec60d-103">Sediakan aliran kerja Pengurusan perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="ec60d-103">Set up Expense management workflows</span></span>

<span data-ttu-id="ec60d-104">Anda boleh menyediakan proses aliran kerja yang digunakan untuk menyemak dan meluluskan dokumen perjalanan dan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="ec60d-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="ec60d-105">Dokumen yang aliran kerja boleh ditakrifkan termasuk laporan perbelanjaan, permintaan perjalanan dan permintaan pendahuluan tunai.</span><span class="sxs-lookup"><span data-stu-id="ec60d-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="ec60d-106">Aliran kerja mewakili proses perniagaan.</span><span class="sxs-lookup"><span data-stu-id="ec60d-106">A workflow represents a business process.</span></span> <span data-ttu-id="ec60d-107">Ia menentukan cara dokumen dialirkan melalui sistem dan menandakan orang yang harus melengkapkan tugas atau meluluskan dokumen.</span><span class="sxs-lookup"><span data-stu-id="ec60d-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="ec60d-108">Terdapat beberapa faedah menggunakan sistem aliran kerja dalam organisasi anda:</span><span class="sxs-lookup"><span data-stu-id="ec60d-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="ec60d-109">**Proses konsisten**: — Anda boleh menentukan proses kelulusan untuk dokumen tertentu seperti permintaan pembelian dan laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="ec60d-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="ec60d-110">Menggunakan sistem aliran kerja membantu anda memastikan dokumen diproses dan diluluskan dengan cara yang konsisten dan berkesan.</span><span class="sxs-lookup"><span data-stu-id="ec60d-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="ec60d-111">Keterlihatan proses: — Anda boleh menjejak status, sejarah dan metrik prestasi tika aliran kerja tertentu.</span><span class="sxs-lookup"><span data-stu-id="ec60d-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="ec60d-112">Ini membantu anda menentukan sama ada perubahan harus dibuat pada aliran kerja untuk meningkatkan kecekapan.</span><span class="sxs-lookup"><span data-stu-id="ec60d-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="ec60d-113">Senarai kerja terpusat: — Pengguna boleh melihat senarai kerja terpusat untuk melihat tugas aliran kerja dan kelulusan yang ditugaskan kepada mereka.</span><span class="sxs-lookup"><span data-stu-id="ec60d-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="ec60d-114">**Jenis aliran kerja yang boleh anda cipta**</span><span class="sxs-lookup"><span data-stu-id="ec60d-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="ec60d-115">Jadual berikut menyenaraikan jenis aliran kerja yang boleh anda cipta dalam **Perbelanjaan**.</span><span class="sxs-lookup"><span data-stu-id="ec60d-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="ec60d-116"><strong>Jenis</strong></span><span class="sxs-lookup"><span data-stu-id="ec60d-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="ec60d-117"><strong>Gunakan jenis ini untuk</strong></span><span class="sxs-lookup"><span data-stu-id="ec60d-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="ec60d-118"><strong>Laporan perbelanjaan</strong></span><span class="sxs-lookup"><span data-stu-id="ec60d-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="ec60d-119">Cipta aliran kerja kelulusan untuk laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="ec60d-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="ec60d-120"><strong>siaran automatik laporan perbelanjaan</strong></span><span class="sxs-lookup"><span data-stu-id="ec60d-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="ec60d-121">Cipta aliran kerja siaran automatik untuk laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="ec60d-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="ec60d-122"><strong>Item bari perbelanjaan</strong></span><span class="sxs-lookup"><span data-stu-id="ec60d-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="ec60d-123">Cipta aliran kerja kelulusan untuk item baris pada laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="ec60d-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="ec60d-124"><strong>Siaran automatik item baris perbelanjaan</strong></span><span class="sxs-lookup"><span data-stu-id="ec60d-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="ec60d-125">Cipta aliran kerja Siaran untuk item baris pada laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="ec60d-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="ec60d-126"><strong>Permintaan perjalanan</strong></span><span class="sxs-lookup"><span data-stu-id="ec60d-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="ec60d-127">Cipta aliran kelulusan untuk permintaan perjalanan.</span><span class="sxs-lookup"><span data-stu-id="ec60d-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="ec60d-128"><strong>Permintaan pendahuluan tunai</strong></span><span class="sxs-lookup"><span data-stu-id="ec60d-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="ec60d-129">Cipta aliran kerja kelulusan untuk permintaan pendahuluan tunai.</span><span class="sxs-lookup"><span data-stu-id="ec60d-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="ec60d-130"><strong>Pemulihan cukai VAT</strong></span><span class="sxs-lookup"><span data-stu-id="ec60d-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="ec60d-131">Cipta aliran kerja kelulusan untuk mendapatkan kembali cukai nilai ditambah (VAT).</span><span class="sxs-lookup"><span data-stu-id="ec60d-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]