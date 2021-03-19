---
title: Segerakkan tugas projek secara langsung daripada Project Service Automation kepada Finance and Operations
description: Topik ini menerangkan templat dan tugas dasar yang digunakan untuk segerakkan tugas projek secara langsung daripada Microsoft Dynamics 365 Project Service Automation kepada Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7cc9ee9de576549c132e14c333a1000c22a55236
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288930"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="c8a4e-103">Segerakkan tugas projek secara langsung daripada Project Service Automation kepada Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c8a4e-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c8a4e-104">Topik ini menerangkan templat dan tugas dasar yang digunakan untuk segerakkan tugas projek secara langsung daripada Dynamics 365 Project Service Automation kepada Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="c8a4e-105">Integrasi tugas projek, kategori transaksi perbelanjaan, anggaran jam, anggaran perbelanjaan dan penguncian fungsi tersedia dalam versi 8.0.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="c8a4e-106">Jika anda menggunakan Enterprise Edition 7.3.0, selepas anda memasang KB 4132657 dan KB 4132660, anda akan dapat menggunakan templat untuk mengintegrasikan tugas projek, kategori transaksi perbelanjaan, anggaran jam, anggaran perbelanjaan dan aktual serta untuk mengkonfigurasi fungsi penguncian.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="c8a4e-107">Jika anda mesti tetap semula pengedaran perakaunan, kami mengesyorkan juga anda memasang KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="c8a4e-108">Integrasi aktual tersedia dalam versi 8.0.1 atau kemudian.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="c8a4e-109">Aliran data untuk Project Service Automation kepada Finance</span><span class="sxs-lookup"><span data-stu-id="c8a4e-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="c8a4e-110">Penyelesaian integrasi Project Service Automation kepada Finance menggunakan ciri integrasi Data untuk menyegerakkan data merentasi tika Project Service Automation dan Finance.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="c8a4e-111">Templat penyepaduan yang tersedia dengan ciri penyepaduan Data mendayakan aliran data tentang tugas projek daripada Project Service Automation kepada Kewangan.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="c8a4e-112">Ilustrasi berikut menunjukkan cara data disegerakkan antara Project Service Automation dan Finance.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="c8a4e-113">[![Aliran data untuk penyepaduan Project Service Automation dengan Kewangan](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="c8a4e-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="c8a4e-114">Templat dan tugas</span><span class="sxs-lookup"><span data-stu-id="c8a4e-114">Template and task</span></span>

<span data-ttu-id="c8a4e-115">Untuk mengakses templat, dalam pusat pentadbir Microsoft Power Apps, pilih **Projek** dan kemudian, di sudut kanan atas, pilih **Projek baharu** untuk memilih templat awam.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="c8a4e-116">Templat dan tugas dasar berikut digunakan untuk segerakkan tugas projek daripada Project Service Automation kepada Kewangan:</span><span class="sxs-lookup"><span data-stu-id="c8a4e-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="c8a4e-117">**Nama templat dalam penyepaduan Data:** Tugas projek (PSA kepada Fin dan Ops)</span><span class="sxs-lookup"><span data-stu-id="c8a4e-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="c8a4e-118">**Nama tugas dalam projek:** Tugas projek</span><span class="sxs-lookup"><span data-stu-id="c8a4e-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="c8a4e-119">Sebelum penyegerakan tugas projek boleh berlaku, anda mesti segerakkan kontrak projek dan projek.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="c8a4e-120">Set entiti</span><span class="sxs-lookup"><span data-stu-id="c8a4e-120">Entity set</span></span>

| <span data-ttu-id="c8a4e-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c8a4e-121">Project Service Automation</span></span> | <span data-ttu-id="c8a4e-122">Kewangan</span><span class="sxs-lookup"><span data-stu-id="c8a4e-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="c8a4e-123">Tugas Projek</span><span class="sxs-lookup"><span data-stu-id="c8a4e-123">Project Tasks</span></span>              | <span data-ttu-id="c8a4e-124">Entiti penyepaduan untuk tugas projek</span><span class="sxs-lookup"><span data-stu-id="c8a4e-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="c8a4e-125">Aliran entiti</span><span class="sxs-lookup"><span data-stu-id="c8a4e-125">Entity flow</span></span>

<span data-ttu-id="c8a4e-126">Tugas projek diuruskan dalam Project Service Automation, dan ia disegerakkan kepada Kewangan sebagai aktiviti projek.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="c8a4e-127">Persediaan prasyarat dan pemetaan</span><span class="sxs-lookup"><span data-stu-id="c8a4e-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="c8a4e-128">Sebelum penyegerakan tugas projek boleh berlaku, anda mesti segerakkan kontrak projek dan projek.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="c8a4e-129">Pertanyaan Kuasa</span><span class="sxs-lookup"><span data-stu-id="c8a4e-129">Power Query</span></span>

<span data-ttu-id="c8a4e-130">Anda mesti menggunakan Microsoft Power Query for Excel untuk menapis data jika syarat ini dipenuhi:</span><span class="sxs-lookup"><span data-stu-id="c8a4e-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="c8a4e-131">Anda mempunyai rekod khusus sumber dalam tugas projek.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="c8a4e-132">Jika anda mesti menggunakan Power Query, ikut garis panduan ini:</span><span class="sxs-lookup"><span data-stu-id="c8a4e-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="c8a4e-133">Templat tugas projek (PSA untuk Fin dan Ops) mempunyai penapis lalai yang mengecualikan rekod khusus sumber daripada tugas projek dengan tetapan penapis pada **IsLineTask** kepada **Palsu**.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="c8a4e-134">Jika anda mencipta templat anda sendiri, anda mesti menambahkan penapis ini.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c8a4e-135">Pemetaan tempat dalam integrasi Data</span><span class="sxs-lookup"><span data-stu-id="c8a4e-135">Template mapping in Data integration</span></span>

<span data-ttu-id="c8a4e-136">Ilustrasi berikut menunjukkan contoh pemetaan tugas templat dalam penyepaduan Data.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="c8a4e-137">Pemetaan menunjukkan maklumat medan yang akan disegerakkan daripada Project Service Automation kepada Finance.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="c8a4e-138">[![Pemetaan templat](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="c8a4e-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]