---
title: Serahkan permintaan sumber
description: Topik ini memberikan maklumat mengenai mengemukakan permintaan untuk sumber projek.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
author: JohnPBurrows
ms.assetid: 9f4a6315-3905-4b15-8d06-e5dae30ccbb8
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2b706ae25af5ba85647c98353b5950663fafc292
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753951"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="4189f-103">Serahkan permintaan sumber</span><span class="sxs-lookup"><span data-stu-id="4189f-103">Submit a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4189f-104">Anda boleh menyerahkan keperluan sumber yang dijana sebagai permintaan sumber.</span><span class="sxs-lookup"><span data-stu-id="4189f-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="4189f-105">Permintaan kemudian dihantar kepada pengurus sumber untuk memenuhi keperluan.</span><span class="sxs-lookup"><span data-stu-id="4189f-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="4189f-106">Dalam Project Service Automation (PSA) pada halaman **Projek**, klik tab **Pasukan** untuk melihat senarai sumber boleh ditempah.</span><span class="sxs-lookup"><span data-stu-id="4189f-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="4189f-107">Pilih sumber generik yang mempunyai keperluan sumber daripada senarai dan kemudian klik **Serahkan Permintaan.**</span><span class="sxs-lookup"><span data-stu-id="4189f-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Menyerahkan permintaan sumber](media/RM-how-to-18.png)

<span data-ttu-id="4189f-109">Status permintaan ahli pasukan generik akan bertukar kepada **Diserahkan.**</span><span class="sxs-lookup"><span data-stu-id="4189f-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="4189f-110">Selepas permintaan dipenuhi oleh pengurus sumber, sumber generik akan digantikan dengan sumber yang dinamakan jika pengurus sumber memenuhi permintaan dengan tempahan sumber yang dinamakan.</span><span class="sxs-lookup"><span data-stu-id="4189f-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="4189f-111">Jika tidak, sumber generik akan kekal pada pasukan dan status permintaan akan berubah untuk **Keperluan Menyemak Semula**, jika pengurus sumber telah mencadangkan sumber yang dinamakan.</span><span class="sxs-lookup"><span data-stu-id="4189f-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>
