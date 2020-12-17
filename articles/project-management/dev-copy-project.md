---
title: Bangunkan templat projek dengan Salin Projek
description: Topik ini menyediakan maklumat tentang cara untuk mencipta templat projek menggunakan tindakan tersuai Salin Projek.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 22976730ef3c8c22ea028b27a6eb5f14fb88993e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642419"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="ac799-103">Bangunkan templat projek dengan Salin Projek</span><span class="sxs-lookup"><span data-stu-id="ac799-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="ac799-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="ac799-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ac799-105">Dynamics 365 Project Operations menyokong keupayaan untuk menyalin projek dan mengembalikan sebarang tugasan kembali ke sumber generik yang mewakili peranan.</span><span class="sxs-lookup"><span data-stu-id="ac799-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="ac799-106">Pelanggan boleh menggunakan kefungsian ini untuk membina templat projek asas.</span><span class="sxs-lookup"><span data-stu-id="ac799-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="ac799-107">Apabila anda memilih **Salin Projek**, status projek sasaran akan dikemas kini.</span><span class="sxs-lookup"><span data-stu-id="ac799-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="ac799-108">Gunakan **Sebab Status** untuk menentukan apabila tindakan salin selesai.</span><span class="sxs-lookup"><span data-stu-id="ac799-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="ac799-109">Memilih **Salin Projek** juga mengemas kini tarikh mula projek kepada tarikh mula semasa jika tiada tarikh sasaran dikesan dalam entiti projek sasaran.</span><span class="sxs-lookup"><span data-stu-id="ac799-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="ac799-110">Tindakan tersuai Salin Projek</span><span class="sxs-lookup"><span data-stu-id="ac799-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="ac799-111">Nama</span><span class="sxs-lookup"><span data-stu-id="ac799-111">Name</span></span> 

<span data-ttu-id="ac799-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="ac799-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="ac799-113">Parameter input</span><span class="sxs-lookup"><span data-stu-id="ac799-113">Input parameters</span></span>
<span data-ttu-id="ac799-114">Terdapat tiga parameter input:</span><span class="sxs-lookup"><span data-stu-id="ac799-114">There are three input parameters:</span></span>

| <span data-ttu-id="ac799-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac799-115">Parameter</span></span>          | <span data-ttu-id="ac799-116">Jenis</span><span class="sxs-lookup"><span data-stu-id="ac799-116">Type</span></span>   | <span data-ttu-id="ac799-117">Nilai</span><span class="sxs-lookup"><span data-stu-id="ac799-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="ac799-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="ac799-118">ProjectCopyOption</span></span>  | <span data-ttu-id="ac799-119">Jalur</span><span class="sxs-lookup"><span data-stu-id="ac799-119">String</span></span> | <span data-ttu-id="ac799-120">**{"removeNamedResources":true}** atau **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="ac799-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="ac799-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="ac799-121">SourceProject</span></span>      | <span data-ttu-id="ac799-122">Rujukan Entiti</span><span class="sxs-lookup"><span data-stu-id="ac799-122">Entity Reference</span></span> | <span data-ttu-id="ac799-123">Projek Sumber</span><span class="sxs-lookup"><span data-stu-id="ac799-123">Source Project</span></span> |
| <span data-ttu-id="ac799-124">Sasaran</span><span class="sxs-lookup"><span data-stu-id="ac799-124">Target</span></span>             | <span data-ttu-id="ac799-125">Rujukan Entiti</span><span class="sxs-lookup"><span data-stu-id="ac799-125">Entity Reference</span></span> | <span data-ttu-id="ac799-126">Projek Sasaran</span><span class="sxs-lookup"><span data-stu-id="ac799-126">Target Project</span></span> |


- <span data-ttu-id="ac799-127">**{"clearTeamsAndAssignments":true}**: Tingkah laku lalai untuk Projek untuk Web dan akan mengalih keluar semua tugasan dan ahli pasukan.</span><span class="sxs-lookup"><span data-stu-id="ac799-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="ac799-128">**{"removeNamedResources":true}** Tingkah laku lalai untuk Project Operations dan akan menukar tugasan kembali kepada sumber generik.</span><span class="sxs-lookup"><span data-stu-id="ac799-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="ac799-129">Untuk mendapatkan lebih banyak lalai pada tindakan, lihat [Gunakan tindakan API Web](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="ac799-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="ac799-130">Tentukan medan untuk disalin</span><span class="sxs-lookup"><span data-stu-id="ac799-130">Specify fields to copy</span></span> 
<span data-ttu-id="ac799-131">Apabila tindakan dipanggil, **Salin Projek** akan melihat pandangan projek **Lajur Salin Projek** untuk menentukan medan untuk disalin apabila projek dicipta.</span><span class="sxs-lookup"><span data-stu-id="ac799-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
