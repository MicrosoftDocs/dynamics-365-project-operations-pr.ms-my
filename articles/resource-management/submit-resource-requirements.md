---
title: Serahkan permintaan sumber
description: Anda boleh menyerahkan keperluan sumber yang dijana sebagai permintaan sumber. Permintaan kemudian dihantar kepada pengurus sumber untuk memenuhi keperluan.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc97af1ec90e60417c502eb329a85004e769e05b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279149"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="d4fa7-104">Serahkan permintaan sumber</span><span class="sxs-lookup"><span data-stu-id="d4fa7-104">Submit a resource request</span></span>

<span data-ttu-id="d4fa7-105">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="d4fa7-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d4fa7-106">Anda boleh menyerahkan keperluan sumber yang dijana sebagai permintaan sumber.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="d4fa7-107">Permintaan kemudian dihantar kepada pengurus sumber untuk memenuhi keperluan.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="d4fa7-108">Dalam Dynamics 365 Project Operations, pada halaman **Projek**, pilih tab **Pasukan** untuk melihat senarai sumber boleh ditempah.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="d4fa7-109">Pilih sumber generik yang mempunyai keperluan sumber daripada senarai, dan kemudian klik **Serahkan Permintaan**.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="d4fa7-110">Status permintaan ahli pasukan generik akan bertukar kepada **Diserahkan.**</span><span class="sxs-lookup"><span data-stu-id="d4fa7-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="d4fa7-111">Selepas permintaan dipenuhi, sumber generik akan digantikan dengan sumber yang dinamakan jika resource manager memenuhi permintaan dengan menempah sumber bernama.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="d4fa7-112">Jika tidak, sekiranya resource manager mencadangkan sumber bernama, sumber generik akan kekal pada pasukan dan status permintaan akan berubah kepada **Keperluan Semakan Semula**.</span><span class="sxs-lookup"><span data-stu-id="d4fa7-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]