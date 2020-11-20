---
title: Takrifkan kemahiran dan kecekapan
description: Topik ini memberikan maklumat tentang cara menyediakan model kecekapan untuk menaraf sumber.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 8738a4743554704ef76807c81fdefcd74e668e1b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124784"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="19964-103">Takrifkan kemahiran dan kecekapan</span><span class="sxs-lookup"><span data-stu-id="19964-103">Define skills and proficiencies</span></span>

<span data-ttu-id="19964-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="19964-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="19964-105">Kemahiran adalah ciri sumber yang dikongsi antara Dynamics 365 Project Operations dan jika ada, Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="19964-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="19964-106">Untuk mengekalkan repositori kemahiran dalam Project Operations, pergi ke **Sumber** \> **Kemahiran Sumber**.</span><span class="sxs-lookup"><span data-stu-id="19964-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="19964-107">Gunakan model kecekapan kepada sumber kadar</span><span class="sxs-lookup"><span data-stu-id="19964-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="19964-108">Kemahiran untuk sumber dinilai oleh model kecekapan.</span><span class="sxs-lookup"><span data-stu-id="19964-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="19964-109">Pengkadaran individu dalam model kecekapan.</span><span class="sxs-lookup"><span data-stu-id="19964-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="19964-110">Untuk mencipta model kecekapan, pergi ke **Sumber** \> **Model Kecekapan** dan kemudian pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="19964-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="19964-111">Dalam model pengkadaran baharu, tentukan nilai penarafan minimum, nilai penarafan maksimum dan entiti yang akan dikadarkan.</span><span class="sxs-lookup"><span data-stu-id="19964-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="19964-112">Dalam subgrid **Nilai Rating**, anda boleh mentakrifkan nilai rating yang berbeza, daripada minimum kepada maksimum.</span><span class="sxs-lookup"><span data-stu-id="19964-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="19964-113">Nilai pengkadaran ini ditunjukkan pada **Keperluan Sumber**, **Papan Jadual** dan penapis **Pembantu Jadual**.</span><span class="sxs-lookup"><span data-stu-id="19964-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
