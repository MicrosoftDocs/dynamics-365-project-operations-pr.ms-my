---
title: Kemas kini projek
description: Topik ini menyediakan maklumat tentang mengemas kini projek dalam Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081083"
---
# <a name="update-a-project"></a><span data-ttu-id="53c2f-103">Kemas kini projek</span><span class="sxs-lookup"><span data-stu-id="53c2f-103">Update a project</span></span>

<span data-ttu-id="53c2f-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="53c2f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="53c2f-105">Di bawah adalah ringkasan medan yang boleh dikemas kini pada projek selepas ia telah dicipta dan sebarang implikasi yang berkenaan dengan kemas kini.</span><span class="sxs-lookup"><span data-stu-id="53c2f-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="53c2f-106">Medan butiran projek</span><span class="sxs-lookup"><span data-stu-id="53c2f-106">Project detail fields</span></span>

- <span data-ttu-id="53c2f-107">**Nama** : Tajuk projek.</span><span class="sxs-lookup"><span data-stu-id="53c2f-107">**Name** : The title of the project.</span></span>
- <span data-ttu-id="53c2f-108">**Perihalan** : Gambaran keseluruhan projek.</span><span class="sxs-lookup"><span data-stu-id="53c2f-108">**Description** : An overview of the project.</span></span>
- <span data-ttu-id="53c2f-109">**Pelanggan** : Syarikat projek itu akan dihantar kepada.</span><span class="sxs-lookup"><span data-stu-id="53c2f-109">**Customer** : The company the project will be delivered to.</span></span>
- <span data-ttu-id="53c2f-110">**Templat kalendar** : Waktu kerja projek.</span><span class="sxs-lookup"><span data-stu-id="53c2f-110">**Calendar template** : The working hours of the project.</span></span> <span data-ttu-id="53c2f-111">Apabila medan ditukar, keseluruhan jadual dikira semula.</span><span class="sxs-lookup"><span data-stu-id="53c2f-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="53c2f-112">**Mata Wang** : Mata wang untuk projek.</span><span class="sxs-lookup"><span data-stu-id="53c2f-112">**Currency** : The currency for the project.</span></span> <span data-ttu-id="53c2f-113">Medan lalai ini adalah berdasarkan pada mata wang yang ditakrifkan dalam unit kontrak.</span><span class="sxs-lookup"><span data-stu-id="53c2f-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="53c2f-114">Apabila unit kontrak dikemas kini, medan juga dikemas kini.</span><span class="sxs-lookup"><span data-stu-id="53c2f-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="53c2f-115">**Unit Kontrak** : Unit organisasi yang mewakili kumpulan atau bahagian syarikat yang bertanggungjawab terutamanya untuk memenangi jualan dan menguruskan penyampaian kerja dan perkhidmatan kepada pelanggan.</span><span class="sxs-lookup"><span data-stu-id="53c2f-115">**Contracting Unit** : The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="53c2f-116">**Pengurus Projek** : Ahli pasukan projek yang mempunyai kuasa untuk menyemak dan meluluskan entri masa dan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="53c2f-116">**Project Manager** : The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="53c2f-117">Anggaran medan</span><span class="sxs-lookup"><span data-stu-id="53c2f-117">Estimate fields</span></span>

- <span data-ttu-id="53c2f-118">**Anggaran Tarikh Mula** : Tarikh projek akan bermula.</span><span class="sxs-lookup"><span data-stu-id="53c2f-118">**Estimated Start Date** : The date that the project will begin.</span></span> <span data-ttu-id="53c2f-119">Apabila medan ini dikemas kini, sebarang tugas pada projek akan mengalih secara berkadaran dengan tarikh mula yang baharu.</span><span class="sxs-lookup"><span data-stu-id="53c2f-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="53c2f-120">**Tarikh Selesai** : Tarikh projek itu dijadualkan untuk berakhir.</span><span class="sxs-lookup"><span data-stu-id="53c2f-120">**Finish Date** : The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="53c2f-121">**Usaha** : Anggaran usaha projek.</span><span class="sxs-lookup"><span data-stu-id="53c2f-121">**Effort** : The estimated effort of the project.</span></span> <span data-ttu-id="53c2f-122">Apabila tugas ditambahkan kepada projek, medan ini tidak boleh diedit lagi.</span><span class="sxs-lookup"><span data-stu-id="53c2f-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="53c2f-123">**Anggaran Kos Buruh** : Anggaran kos buruh projek.</span><span class="sxs-lookup"><span data-stu-id="53c2f-123">**Estimated Labor Cost** : The estimated labor cost of the project.</span></span> <span data-ttu-id="53c2f-124">Apabila kos buruh ditambahkan kepada projek, medan ini tidak boleh diedit lagi.</span><span class="sxs-lookup"><span data-stu-id="53c2f-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="53c2f-125">**Anggaran Perbelanjaan** : Anggaran perbelanjaan projek.</span><span class="sxs-lookup"><span data-stu-id="53c2f-125">**Estimated Expenses** : The estimated expenses of the project.</span></span> <span data-ttu-id="53c2f-126">Apabila perbelanjaan ditambahkan kepada projek, medan ini tidak boleh diedit lagi.</span><span class="sxs-lookup"><span data-stu-id="53c2f-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="53c2f-127">Medan sebenar projek</span><span class="sxs-lookup"><span data-stu-id="53c2f-127">Project actual fields</span></span>
- <span data-ttu-id="53c2f-128">**Mula Sebenar** : Tarikh projek dimulakan.</span><span class="sxs-lookup"><span data-stu-id="53c2f-128">**Actual Start** : The date that the project started.</span></span>
- <span data-ttu-id="53c2f-129">**Selesai Sebenar** : Untuk dikemas kini apabila projek telah selesai.</span><span class="sxs-lookup"><span data-stu-id="53c2f-129">**Actual Finish** : To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="53c2f-130">Medan status projek</span><span class="sxs-lookup"><span data-stu-id="53c2f-130">Project status fields</span></span>

- <span data-ttu-id="53c2f-131">**Status Projek Keseluruhan** : Kesihatan projek secara keseluruhan yang disediakan oleh Pengurus projek.</span><span class="sxs-lookup"><span data-stu-id="53c2f-131">**Overall Project Status** : The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="53c2f-132">**Komen** : Naratif mengenai kesihatan semasa projek yang disediakan oleh Pengurus projek.</span><span class="sxs-lookup"><span data-stu-id="53c2f-132">**Comments** : A narrative regarding the current health of the project provided by the Project manager.</span></span>

