---
title: Model kemahiran dan kecekapan
description: Topik ini memberikan maklumat mengenai cara untuk menggunakan model kemahiran dan kecekapan.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 82eeab4c9682e5b777da4e66f6c4f3f1afb3c19b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282974"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="93d32-103">Model kemahiran dan kecekapan</span><span class="sxs-lookup"><span data-stu-id="93d32-103">Skills and proficiency models</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="93d32-104">Kemahiran ialah ciri sumber yang dikongsi antara Dynamics 365 Project Service Automation dan jika ada Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="93d32-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="93d32-105">Untuk mengekalkan repositori kemahiran dalam Project Service Automation, pergi ke **Sumber** \> **Kemahiran Sumber**.</span><span class="sxs-lookup"><span data-stu-id="93d32-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Kemahiran Sumber](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="93d32-107">Gunakan model kecekapan kepada sumber kadar</span><span class="sxs-lookup"><span data-stu-id="93d32-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="93d32-108">Kemahiran untuk sumber dinilai oleh model kecekapan.</span><span class="sxs-lookup"><span data-stu-id="93d32-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="93d32-109">Pengkadaran individu dalam model kecekapan.</span><span class="sxs-lookup"><span data-stu-id="93d32-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="93d32-110">Untuk mencipta model kecekapan, pergi ke **Sumber** \> **Model Kecekapan** dan kemudian pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="93d32-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="93d32-111">Dalam model pengkadaran baharu, tentukan nilai penarafan minimum, nilai penarafan maksimum dan entiti yang akan dikadarkan.</span><span class="sxs-lookup"><span data-stu-id="93d32-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="93d32-112">Dalam subgrid **Nilai Rating**, anda boleh mentakrifkan nilai rating yang berbeza, daripada minimum kepada maksimum.</span><span class="sxs-lookup"><span data-stu-id="93d32-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Pengkadaran minimum dan maksimum ditakrifkan](media/Resource-Management-image85.png)

<span data-ttu-id="93d32-114">Nilai pengkadaran ini ditunjukkan pada **Keperluan Sumber**, **Papan Jadual** dan penapis **Pembantu Jadual**.</span><span class="sxs-lookup"><span data-stu-id="93d32-114">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]