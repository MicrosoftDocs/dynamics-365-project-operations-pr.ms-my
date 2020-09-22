---
title: Konfigurasi tetapan parameter tambahan
description: Cara untuk mengkonfigurasikan tetapan parameter tambahan dalam Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: de2fe830-4313-4711-b03b-76d56bf56cb6
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: f3e110163088f8e3b78da9f273113d74775bf24c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753999"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="01613-103">Konfigurasikan tetapan parameter tambahan (Project Service)</span><span class="sxs-lookup"><span data-stu-id="01613-103">Configure additional parameter settings (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="01613-104">Sebaik sahaja anda telah mengkonfigurasi item dalam topik yang sebelumnya, anda perlu menetapkan parameter projek tambahan untuk digunakan kepada projek anda.</span><span class="sxs-lookup"><span data-stu-id="01613-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="01613-105">Ketika pertama kali anda memasang [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], anda mencipta tetapan parameter untuk mencipta dahulu semua rekod yang diperlukan untuk [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] berfungsi.</span><span class="sxs-lookup"><span data-stu-id="01613-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="01613-106">Kini tiba masanya untuk kembali dan mengkonfigurasi medan tambahan untuk tetapan ini.</span><span class="sxs-lookup"><span data-stu-id="01613-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="01613-107">Anda perlu mengkonfigurasikan tetapan berikut:</span><span class="sxs-lookup"><span data-stu-id="01613-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="01613-108">Unit organisasi</span><span class="sxs-lookup"><span data-stu-id="01613-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="01613-109">Kekerapan invois</span><span class="sxs-lookup"><span data-stu-id="01613-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="01613-110">Templat waktu kerja</span><span class="sxs-lookup"><span data-stu-id="01613-110">Work hours template</span></span>  
  
-   <span data-ttu-id="01613-111">Senarai harga</span><span class="sxs-lookup"><span data-stu-id="01613-111">Price list</span></span>  
 
<span data-ttu-id="01613-112">Dalam langkah ini, anda juga akan menunjukkan jenis peruntukan sumber yang anda mahu:</span><span class="sxs-lookup"><span data-stu-id="01613-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="01613-113">**Tengah**.</span><span class="sxs-lookup"><span data-stu-id="01613-113">**Central**.</span></span> <span data-ttu-id="01613-114">Hanya pengurus sumber boleh menguntukkan sumber untuk projek.</span><span class="sxs-lookup"><span data-stu-id="01613-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="01613-115">**Hibrid**.</span><span class="sxs-lookup"><span data-stu-id="01613-115">**Hybrid**.</span></span> <span data-ttu-id="01613-116">Pengurus sumber, pengurus projek dan pengurus akaun boleh menguntukkan sumber untuk projek.</span><span class="sxs-lookup"><span data-stu-id="01613-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="01613-117">Untuk menetapkan parameter projek:</span><span class="sxs-lookup"><span data-stu-id="01613-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="01613-118">Pergi ke **Project Service > Parameter**.</span><span class="sxs-lookup"><span data-stu-id="01613-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="01613-119">Klik tetapan parameter yang anda mahu konfigurasikan (tetapan yang anda cipta ketika pertama kali anda memasang [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]) atau klik **Baharu** untuk mencipta tetapan baharu.</span><span class="sxs-lookup"><span data-stu-id="01613-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="01613-120">Dalam kawasan **Umum**, tetapkan pilihan untuk parameter projek anda.</span><span class="sxs-lookup"><span data-stu-id="01613-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="01613-121">Dalam kawasan **Senarai Harga**, klik **+** untuk menambah senarai harga dalam senarai juntai bawah **Senarai Harga Parameter Projek** dan kemudian klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="01613-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="01613-122">Klik butang **Simpan** di sudut kanan bawah skrin.</span><span class="sxs-lookup"><span data-stu-id="01613-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="01613-123">Rekod parameter projek mesti diselenggara untuk Project Service berfungsi dengan betul.</span><span class="sxs-lookup"><span data-stu-id="01613-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="01613-124">Rekod ini tidak boleh dipadamkan.</span><span class="sxs-lookup"><span data-stu-id="01613-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="01613-125">Lihat Juga</span><span class="sxs-lookup"><span data-stu-id="01613-125">See Also</span></span>  
 [<span data-ttu-id="01613-126">Sediakan sumber</span><span class="sxs-lookup"><span data-stu-id="01613-126">Set up resources</span></span>](../project-service/set-up-resources.md)
