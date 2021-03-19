---
title: Sediakan aliran kerja untuk pengurusan Perbelanjaan
description: Anda boleh menyediakan proses aliran kerja yang digunakan untuk menyemak dan meluluskan dokumen perjalanan dan perbelanjaan.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e54fca67427e8f3d0e7050563a751b5be354356c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276044"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="68e05-103">Sediakan aliran kerja untuk pengurusan Perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="68e05-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="68e05-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="68e05-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="68e05-105">Anda boleh menyediakan proses aliran kerja untuk menyemak dan meluluskan dokumen perjalanan dan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="68e05-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="68e05-106">Anda boleh menakrifkan aliran kerja untuk laporan perbelanjaan, permintaan perjalanan dan permintaan pendahuluan tunai.</span><span class="sxs-lookup"><span data-stu-id="68e05-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="68e05-107">Aliran kerja mewakili proses perniagaan dan mentakrifkan cara aliran dokumen melalui sistem.</span><span class="sxs-lookup"><span data-stu-id="68e05-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="68e05-108">Aliran kerja juga menunjukkan siapa yang mesti melengkapkan tugas atau meluluskan dokumen.</span><span class="sxs-lookup"><span data-stu-id="68e05-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="68e05-109">Terdapat beberapa faedah menggunakan sistem aliran kerja dalam organisasi anda:</span><span class="sxs-lookup"><span data-stu-id="68e05-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="68e05-110">**Proses konsisten**: Anda boleh menakrifkan proses kelulusan untuk dokumen tertentu seperti permintaan pembelian dan laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="68e05-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="68e05-111">Menggunakan sistem aliran kerja membantu memastikan dokumen diproses dan diluluskan dengan cara yang konsisten dan berkesan.</span><span class="sxs-lookup"><span data-stu-id="68e05-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="68e05-112">**Keterlihatan proses**: Anda boleh menjejak status, sejarah dan metrik prestasi tika aliran kerja tertentu.</span><span class="sxs-lookup"><span data-stu-id="68e05-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="68e05-113">Ini membantu anda menentukan sama ada perubahan harus dibuat pada aliran kerja untuk meningkatkan kecekapan.</span><span class="sxs-lookup"><span data-stu-id="68e05-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="68e05-114">**Senarai kerja berpusat**: Pengguna boleh melihat senarai kerja berpusat untuk melihat tugas aliran kerja dan kelulusan yang ditugaskan kepada mereka.</span><span class="sxs-lookup"><span data-stu-id="68e05-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="68e05-115">Jenis aliran kerja</span><span class="sxs-lookup"><span data-stu-id="68e05-115">Workflow types</span></span>

<span data-ttu-id="68e05-116">Jadual berikut menyenaraikan jenis aliran kerja yang anda boleh cipta dalam **Pengurusan perbelanjaan**.</span><span class="sxs-lookup"><span data-stu-id="68e05-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="68e05-117"><strong>Jenis</strong></span><span class="sxs-lookup"><span data-stu-id="68e05-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="68e05-118"><strong>Gunakan jenis ini untuk</strong></span><span class="sxs-lookup"><span data-stu-id="68e05-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="68e05-119"><strong>Kelulusan automatik laporan perbelanjaan</strong></span><span class="sxs-lookup"><span data-stu-id="68e05-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="68e05-120">Cipta aliran kerja kelulusan untuk laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="68e05-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="68e05-121"><strong>siaran automatik laporan perbelanjaan</strong></span><span class="sxs-lookup"><span data-stu-id="68e05-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="68e05-122">Cipta aliran kerja siaran automatik untuk laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="68e05-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="68e05-123"><strong>Item bari perbelanjaan</strong></span><span class="sxs-lookup"><span data-stu-id="68e05-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="68e05-124">Cipta aliran kerja kelulusan untuk item baris pada laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="68e05-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="68e05-125"><strong>Siaran automatik item baris perbelanjaan</strong></span><span class="sxs-lookup"><span data-stu-id="68e05-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="68e05-126">Cipta aliran kerja Siaran untuk item baris pada laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="68e05-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="68e05-127"><strong>Permintaan perjalanan</strong></span><span class="sxs-lookup"><span data-stu-id="68e05-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="68e05-128">Cipta aliran kelulusan untuk permintaan perjalanan.</span><span class="sxs-lookup"><span data-stu-id="68e05-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="68e05-129"><strong>Permintaan pendahuluan tunai</strong></span><span class="sxs-lookup"><span data-stu-id="68e05-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="68e05-130">Cipta aliran kerja kelulusan untuk permintaan pendahuluan tunai.</span><span class="sxs-lookup"><span data-stu-id="68e05-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="68e05-131"><strong>Pemulihan cukai VAT</strong></span><span class="sxs-lookup"><span data-stu-id="68e05-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="68e05-132">Cipta aliran kerja kelulusan untuk mendapatkan kembali cukai nilai ditambah (VAT).</span><span class="sxs-lookup"><span data-stu-id="68e05-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |


[!INCLUDE[footer-include](../includes/footer-banner.md)]