---
title: Takrifkan kemahiran dan kecekapan
description: Topik ini memberikan maklumat tentang cara menyediakan model kecekapan untuk menaraf sumber.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9376e0b268a3ab682716da604ceecfa1e878da68
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897642"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="5d394-103">Takrifkan kemahiran dan kecekapan</span><span class="sxs-lookup"><span data-stu-id="5d394-103">Define skills and proficiencies</span></span>

<span data-ttu-id="5d394-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="5d394-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5d394-105">Kemahiran adalah ciri sumber yang dikongsi antara Dynamics 365 Project Operations dan jika ada, Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="5d394-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="5d394-106">Untuk mengekalkan repositori kemahiran dalam Project Operations, pergi ke **Sumber** \> **Kemahiran Sumber**.</span><span class="sxs-lookup"><span data-stu-id="5d394-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="5d394-107">Gunakan model kecekapan kepada sumber kadar</span><span class="sxs-lookup"><span data-stu-id="5d394-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="5d394-108">Kemahiran untuk sumber dinilai oleh model kecekapan.</span><span class="sxs-lookup"><span data-stu-id="5d394-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="5d394-109">Pengkadaran individu dalam model kecekapan.</span><span class="sxs-lookup"><span data-stu-id="5d394-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="5d394-110">Untuk mencipta model kecekapan, pergi ke **Sumber** \> **Model Kecekapan** dan kemudian pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="5d394-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="5d394-111">Dalam model pengkadaran baharu, tentukan nilai penarafan minimum, nilai penarafan maksimum dan entiti yang akan dikadarkan.</span><span class="sxs-lookup"><span data-stu-id="5d394-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="5d394-112">Dalam sub grid **Nilai Pengkadaran** anda boleh mentakrifkan nilai penarafan yang berbeza, daripada minimum kepada maksimum.</span><span class="sxs-lookup"><span data-stu-id="5d394-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="5d394-113">Nilai pengkadaran ini ditunjukkan pada **Keperluan Sumber**, **Papan Jadual** dan penapis **Pembantu Jadual**.</span><span class="sxs-lookup"><span data-stu-id="5d394-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
