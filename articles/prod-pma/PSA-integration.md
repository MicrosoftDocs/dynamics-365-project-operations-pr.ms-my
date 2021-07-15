---
title: Gambaran Keseluruhan Project Service Automation
description: Topik ini memberikan maklumat mengenai Dynamics 365 Project Service Automation kepada penyelesaian integrasi Dynamics 365 Finance.
author: ruhercul
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c756caec6cd7eda8f891446d3e8309aca3b2482
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369630"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="b8b8d-103">Gambaran Keseluruhan Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b8b8d-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b8b8d-104">Project Service Automation kepada penyelesaian integrasi Kewangan menggunakan ciri integrasi Data untuk menyegerakkan data merentasi tika Dynamics 365 Finance dan Dynamics 365 Project Service Automation melalui Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b8b8d-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="b8b8d-105">Templat integrasi yang tersedia dengan ciri integrasi Data mendayakan aliran projek, kontrak projek, baris kontrak projek, pencapaian baris kontrak projek, tugas projek, kategori transaksi perbelanjaan, anggaran jam dan anggaran perbelanjaan daripada Project Service Automation kepada Kewangan.</span><span class="sxs-lookup"><span data-stu-id="b8b8d-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="b8b8d-106">Jika anda menggunakan versi 7.3.0, anda mesti memasang KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="b8b8d-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="b8b8d-107">Anda kemudian akan dapat mengintegrasikan projek harga tetap.</span><span class="sxs-lookup"><span data-stu-id="b8b8d-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="b8b8d-108">Jika anda menggunakan versi 7.3.0 dan anda sedang membawa transaksi yuran daripada Project Service Automation, anda mesti memasang KB 4345320 untuk memasukkan yuran tersebut dalam invois projek.</span><span class="sxs-lookup"><span data-stu-id="b8b8d-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="b8b8d-109">Jika anda menggunakan versi 8.0, anda akan dapat menggunakan integrasi tugas projek, kategori transaksi perbelanjaan, anggaran jam, anggaran perbelanjaan dan penguncian fungsi.</span><span class="sxs-lookup"><span data-stu-id="b8b8d-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="b8b8d-110">Jika anda menggunakan versi 8.0.1 atau kemudian, anda akan dapat menyegerakkan aktual.</span><span class="sxs-lookup"><span data-stu-id="b8b8d-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="b8b8d-111">Sebelum anda boleh mengintegrasikan kewangan Project Service Automation, anda mesti konfigurasikan parameter integrasi Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b8b8d-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="b8b8d-112">Untuk maklumat lanjut, lihat: [Parameter integrasi Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b8b8d-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="b8b8d-113">Penyelesaian integrasi ini mendayakan penyegerakan langsung dalam senario berikut:</span><span class="sxs-lookup"><span data-stu-id="b8b8d-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="b8b8d-114">Kekalkan kontrak projek dalam Project Service Automation, dan segerakkannya secara langsung daripada Project Service Automation ke Kewangan.</span><span class="sxs-lookup"><span data-stu-id="b8b8d-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="b8b8d-115">Kekalkan projek dalam Project Service Automation, dan segerakkannya secara langsung daripada Project Service Automation ke Kewangan.</span><span class="sxs-lookup"><span data-stu-id="b8b8d-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="b8b8d-116">Kekalkan baris kontrak projek dalam Project Service Automation, dan segerakkannya secara langsung daripada Project Service Automation ke Kewangan.</span><span class="sxs-lookup"><span data-stu-id="b8b8d-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="b8b8d-117">Kekalkan pencapaian baris kontrak projek dalam Project Service Automation, dan segerakkannya secara langsung daripada Project Service Automation ke Kewangan.</span><span class="sxs-lookup"><span data-stu-id="b8b8d-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="b8b8d-118">Kekalkan tugas projek dalam Project Service Automation, dan segerakkannya secara langsung daripada Project Service Automation ke Kewangan.</span><span class="sxs-lookup"><span data-stu-id="b8b8d-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="b8b8d-119">Kekalkan kategori transaksi perbelanjaan dalam Kewangan, dan segerakkannya secara langsung daripada Kewangan ke Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b8b8d-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="b8b8d-120">Cipta anggaran jam projek dalam Project Service Automation, dan segerakkannya secara langsung daripada Project Service Automation ke Kewangan.</span><span class="sxs-lookup"><span data-stu-id="b8b8d-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="b8b8d-121">Cipta anggaran perbelanjaan projek dalam Project Service Automation, dan segerakkannya secara langsung daripada Project Service Automation ke Kewangan.</span><span class="sxs-lookup"><span data-stu-id="b8b8d-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="b8b8d-122">Cipta masa, perbelanjaan dan yuran aktual projek dalam Project Service Automation, dan cipta transaksi projek dalam jurnal integrasi Project Service Automation supaya dapat disiarkan dalam kewangan.</span><span class="sxs-lookup"><span data-stu-id="b8b8d-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="b8b8d-123">Penyegerakan data</span><span class="sxs-lookup"><span data-stu-id="b8b8d-123">Data synchronization</span></span>

<span data-ttu-id="b8b8d-124">Ilustrasi berikut menunjukkan cara data disegerakkan sebagai sebahagian daripada integrasi antara Project Service Automation dan Kewangan.</span><span class="sxs-lookup"><span data-stu-id="b8b8d-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="b8b8d-125">Tidak semua templat kini tersedia.</span><span class="sxs-lookup"><span data-stu-id="b8b8d-125">Not all templates are currently available.</span></span> <span data-ttu-id="b8b8d-126">Templat akan dikeluarkan kerana ia dilengkapkan.</span><span class="sxs-lookup"><span data-stu-id="b8b8d-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="b8b8d-127">[![Integrasi Project Service Automation dengan Kewangan](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="b8b8d-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="b8b8d-128">Keperluan sistem untuk kewangan</span><span class="sxs-lookup"><span data-stu-id="b8b8d-128">System requirements for Finance</span></span>

<span data-ttu-id="b8b8d-129">Untuk menggunakan Project Service Automation kepada penyelesaian integrasi Kewangan, anda mesti memasang Enterprise Edition 7.3 dengan Platform kemas kini 12 atau kemudian.</span><span class="sxs-lookup"><span data-stu-id="b8b8d-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="b8b8d-130">Keperluan sistem untuk Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b8b8d-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="b8b8d-131">Untuk menggunakan Project Service Automation kepada penyelesaian integrasi Kewangan, anda mesti memasang komponen berikut:</span><span class="sxs-lookup"><span data-stu-id="b8b8d-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="b8b8d-132">Dynamics 365 Project Service Automation versi 9.0.0.0 atau lebih terkini</span><span class="sxs-lookup"><span data-stu-id="b8b8d-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="b8b8d-133">Prospek untuk penyelesaian tunai bagi Dynamics 365 Sales, versi 1.14.0.0 (v14) atau kemudian</span><span class="sxs-lookup"><span data-stu-id="b8b8d-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="b8b8d-134">Project Service Automation kepada penyelesaian Kewangan untuk Dynamics 365 Project Service Automation versi 1.0.0.0 atau kemudian</span><span class="sxs-lookup"><span data-stu-id="b8b8d-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="b8b8d-135">Pasang Project Service Automation kepada penyelesaian integrasi Kewangan dalam tika Project Service Automation anda</span><span class="sxs-lookup"><span data-stu-id="b8b8d-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="b8b8d-136">Muat turun Project Service Automation kepada penyelesaian integrasi Kewangan daripada [Pusat Muat Turun Microsoft](https://www.microsoft.com/download/details.aspx?id=57016), dan ikuti arahan yang disertakan dengan penyelesaian.</span><span class="sxs-lookup"><span data-stu-id="b8b8d-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]