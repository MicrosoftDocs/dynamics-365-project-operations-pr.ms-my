---
title: Prestasi penjadualan sumber projek
description: Topik ini memberikan maklumat mengenai cara untuk menambah baik prestasi penjadualan sumber untuk sebilangan besar projek.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 34c31570778f9b64c23387112cf56fa1139cd0fd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289020"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="5177d-103">Prestasi penjadualan sumber projek</span><span class="sxs-lookup"><span data-stu-id="5177d-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="5177d-104">Isu prestasi yang berkaitan dengan penjadualan sumber boleh berlaku apabila bilangan projek mencapai ke dalam ribuan.</span><span class="sxs-lookup"><span data-stu-id="5177d-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="5177d-105">Untuk meningkatkan prestasi penjadualan sumber, ciri tersedia membenarkan pengguna untuk mengurangkan masa yang diperlukan untuk melancarkan borang ketersediaan sumber.</span><span class="sxs-lookup"><span data-stu-id="5177d-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="5177d-106">Khususnya, ini akan mengalih keluar proses penyegerakan gulungan kapasiti sumber dan menggunakan jadual **SumberProjekRes** untuk mempercepat carian sumber.</span><span class="sxs-lookup"><span data-stu-id="5177d-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="5177d-107">Ambil perhatian jadual **ResRollup** tidak akan digunakan lagi.</span><span class="sxs-lookup"><span data-stu-id="5177d-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5177d-108">Jika terdapat kebergantungan pada sama ada proses penyegerakan gulungan kapasiti sumber atau jadual **SumberProjekRes**, jangan gunakan ciri ini.</span><span class="sxs-lookup"><span data-stu-id="5177d-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="5177d-109">Dayakan peningkatan prestasi penjadualan sumber</span><span class="sxs-lookup"><span data-stu-id="5177d-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="5177d-110">Untuk mendayakan peningkatan prestasi penjadualan sumber, lengkapkan langkah berikut.</span><span class="sxs-lookup"><span data-stu-id="5177d-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="5177d-111">Pergi ke **Pengurusan ciri** > **Semua**, dan dalam senarai ciri, cari **Dayakan ciri peningkatan prestasi penjadualan sumber projek**.</span><span class="sxs-lookup"><span data-stu-id="5177d-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="5177d-112">Pilih **Dayakan sekarang**.</span><span class="sxs-lookup"><span data-stu-id="5177d-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="5177d-113">Jika anda tidak dapat mencari ciri dalam senarai, pilih **Semak untuk kemas kini** untuk segar semula senarai.</span><span class="sxs-lookup"><span data-stu-id="5177d-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="5177d-114">Segar semula pelayar anda, dan kemudian pergi ke **Pengurusan dan perakaunan projek** > **Berkala** > **Sumber projek** > **Segerakkan kapasiti kalendar sumber merentasi semua syarikat**.</span><span class="sxs-lookup"><span data-stu-id="5177d-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="5177d-115">Tetapkan **Alih keluar rekod kapasiti sedia ada** kepada **Ya** untuk mengalih keluar data sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="5177d-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="5177d-116">Jika anda mahu menjana data tambahan, tetapkan ia kepada **Tidak**.</span><span class="sxs-lookup"><span data-stu-id="5177d-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="5177d-117">Dalam medan **Kod tempoh**, pilih tempoh data yang sepatutnya dijana.</span><span class="sxs-lookup"><span data-stu-id="5177d-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="5177d-118">Jika anda memilih kod tempoh, tarikh mula dan tamat tidak perlu ditakrifkan.</span><span class="sxs-lookup"><span data-stu-id="5177d-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="5177d-119">Jika anda membiarkan medan **Kod tempoh** kosong, pilih tarikh mula dan tamat khusus untuk menjana data.</span><span class="sxs-lookup"><span data-stu-id="5177d-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="5177d-120">Pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="5177d-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="5177d-121">Ini akan mengedarkan data umum untuk jadual **KapasitiKalendarRes** merentasi semua syarikat dalam persekitaran anda, jadi kerja kelompok hanya perlu berjalan dalam satu entiti yang sah.</span><span class="sxs-lookup"><span data-stu-id="5177d-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="5177d-122">Data dalam kerja kelompok ini diperlukan untuk mengira kapasiti sumber melalui kalendar berkaitan.</span><span class="sxs-lookup"><span data-stu-id="5177d-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="5177d-123">Pergi ke **Pengurusan dan perakaunan projek** > **Berkala** > **Sumber projek** > **Isikan sumber projek merentasi semua syarikat** dan kemudian pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="5177d-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="5177d-124">Ini adalah skrip naik taraf data untuk data umum dalam **ResProjectResource**, **ResCalendarDateTimeRange**, dan jadual **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="5177d-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="5177d-125">Nilai untuk medan **PSAPRojSchedRole.RootActivity** juga dikemas kini.</span><span class="sxs-lookup"><span data-stu-id="5177d-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="5177d-126">Jika ini tidak berjalan, anda akan menerima amaran apabila anda cuba untuk melaksanakan operasi penjadualan sumber.</span><span class="sxs-lookup"><span data-stu-id="5177d-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="5177d-127">Matikan peningkatan prestasi penjadualan sumber</span><span class="sxs-lookup"><span data-stu-id="5177d-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="5177d-128">Pergi ke **Pengurusan ciri** > **Semua**  dan carian untuk **Dayakan ciri peningkatan prestasi penjadualan sumber projek**.</span><span class="sxs-lookup"><span data-stu-id="5177d-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="5177d-129">Pilih ciri dan kemudian pilih butang **Nyahdaya**.</span><span class="sxs-lookup"><span data-stu-id="5177d-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="5177d-130">Segar semula pelayar anda.</span><span class="sxs-lookup"><span data-stu-id="5177d-130">Refresh your browser.</span></span>
4. <span data-ttu-id="5177d-131">Pergi ke **Pengurusan dan perakaunan projek** > **Berkala** > **Penyegerakan kapasiti** > **Segerakkan gulungan kapasiti sumber**.</span><span class="sxs-lookup"><span data-stu-id="5177d-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="5177d-132">Pada halaman **Penyegerakan gulungan kapasiti**, tetapkan **Alih keluar rekod kapasiti sedia ada** kepada **Ya** untuk mengalih keluar data sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="5177d-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="5177d-133">Jika anda mahu menjana data tambahan, tetapkan ia kepada **Tidak**.</span><span class="sxs-lookup"><span data-stu-id="5177d-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="5177d-134">Dalam medan **Kod tempoh**, pilih tempoh data yang sepatutnya dijana.</span><span class="sxs-lookup"><span data-stu-id="5177d-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="5177d-135">Jika anda memilih kod tempoh, tarikh mula dan tamat tidak perlu ditakrifkan.</span><span class="sxs-lookup"><span data-stu-id="5177d-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="5177d-136">Jika anda membiarkan medan **Kod tempoh** kosong, pilih tarikh mula dan tamat khusus untuk menjana data.</span><span class="sxs-lookup"><span data-stu-id="5177d-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="5177d-137">Pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="5177d-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="5177d-138">Ini akan mengedarkan data umum untuk jadual **ResRollup** merentasi semua syarikat dalam persekitaran anda, jadi kerja kelompok hanya perlu berjalan dalam satu entiti yang sah.</span><span class="sxs-lookup"><span data-stu-id="5177d-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="5177d-139">Kerja kelompok ini diperlukan untuk semua pandangan **Ketersediaan Sumber**.</span><span class="sxs-lookup"><span data-stu-id="5177d-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="5177d-140">Jika kerja kelompok ini tidak berjalan, data **ResRollup** akan dijana pada bila-bila masa, yang boleh mengambil masa.</span><span class="sxs-lookup"><span data-stu-id="5177d-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]