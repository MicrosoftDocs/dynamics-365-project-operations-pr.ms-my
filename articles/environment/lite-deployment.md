---
title: Laksanakan Project Operations - lite
description: Topik ini memberikan maklumat mengenai cara untuk memasang pelaksanaan Lite Project Operations - urusan untuk penginvoisan proforma.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0af8067fc0673890a317ac6f4e62d74b7f4eebca
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290100"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="2aaa5-103">Laksanakan Project Operations - lite</span><span class="sxs-lookup"><span data-stu-id="2aaa5-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="2aaa5-104">_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_</span><span class="sxs-lookup"><span data-stu-id="2aaa5-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2aaa5-105">Project Operations menyokong berbilang model pelaksanaan.</span><span class="sxs-lookup"><span data-stu-id="2aaa5-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="2aaa5-106">Untuk menentukan model pelaksanaan terbaik, lihat [Jenis pelaksanaan](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="2aaa5-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="2aaa5-107">Pelaksanaan ini, pelaksanaan Lite – urusan untuk penginvoisan proforma, keputusan dalam **Common Data Service satu-satunya pelaksanaan Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="2aaa5-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="2aaa5-108">Pasang Project Operations ke dalam persekitaran CDS baharu</span><span class="sxs-lookup"><span data-stu-id="2aaa5-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="2aaa5-109">Pasang ke dalam persekitaran CDS sedia ada</span><span class="sxs-lookup"><span data-stu-id="2aaa5-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="2aaa5-110">Pasang Project Operations ke dalam persekitaran CDS baharu</span><span class="sxs-lookup"><span data-stu-id="2aaa5-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="2aaa5-111">Sebagai [Pentadbir global atau Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) dengan lesen Project Operations, cipta persekitaran CD baharu dalam [pusat pentadbir Power Platform](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="2aaa5-111">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="2aaa5-112">Pastikan **pangkalan data CDS** dan **Aplikasi Dynamics 365** didayakan.</span><span class="sxs-lookup"><span data-stu-id="2aaa5-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="2aaa5-113">Untuk mendapatkan maklumat lanjut, lihat [Cipta dan urus persekitaran dalam pusat pentadbir Power Platform](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="2aaa5-113">For more information, see [Create and manage environments in the Power Platform admin center](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="2aaa5-114">Pilih **Microsoft Dynamics 365 Project Operations** daripada senarai pelaksanaan aplikasi Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="2aaa5-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="2aaa5-115">Pasang Project Operations ke dalam persekitaran CDS sedia ada</span><span class="sxs-lookup"><span data-stu-id="2aaa5-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="2aaa5-116">Sebagai [Pentadbir global atau Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) dengan lesen Project Operations, cari persekitaran dalam [Pusat pentadbir Power Platform](https://admin.powerplatform.com) di tempat anda mahu memasang Project Operations.</span><span class="sxs-lookup"><span data-stu-id="2aaa5-116">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="2aaa5-117">Pasang **Microsoft Dynamics 365 Project Operations** daripada senarai pelaksanaan aplikasi Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="2aaa5-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="2aaa5-118">Untuk mendapatkan maklumat lanjut, lihat [Urus aplikasi Dynamics 365](https://docs.microsoft.com/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="2aaa5-118">For more information, see [Manage Dynamics 365 apps](https://docs.microsoft.com/power-platform/admin/manage-apps).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]