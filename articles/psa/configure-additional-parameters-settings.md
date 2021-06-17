---
title: Konfigurasi tetapan parameter tambahan
description: Cara untuk mengkonfigurasikan tetapan parameter tambahan dalam Project Service
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: f4e883e71beacffb6e2b0b56967046c3f38f7d50
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001122"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="e5d70-103">Konfigurasikan tetapan parameter tambahan (Project Service)</span><span class="sxs-lookup"><span data-stu-id="e5d70-103">Configure additional parameter settings (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="e5d70-104">Sebaik sahaja anda telah mengkonfigurasi item dalam topik yang sebelumnya, anda perlu menetapkan parameter projek tambahan untuk digunakan kepada projek anda.</span><span class="sxs-lookup"><span data-stu-id="e5d70-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="e5d70-105">Ketika pertama kali anda memasang [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], anda mencipta tetapan parameter untuk mencipta dahulu semua rekod yang diperlukan untuk [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] berfungsi.</span><span class="sxs-lookup"><span data-stu-id="e5d70-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="e5d70-106">Kini tiba masanya untuk kembali dan mengkonfigurasi medan tambahan untuk tetapan ini.</span><span class="sxs-lookup"><span data-stu-id="e5d70-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="e5d70-107">Anda perlu mengkonfigurasikan tetapan berikut:</span><span class="sxs-lookup"><span data-stu-id="e5d70-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="e5d70-108">Unit organisasi</span><span class="sxs-lookup"><span data-stu-id="e5d70-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="e5d70-109">Kekerapan invois</span><span class="sxs-lookup"><span data-stu-id="e5d70-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="e5d70-110">Templat waktu kerja</span><span class="sxs-lookup"><span data-stu-id="e5d70-110">Work hours template</span></span>  
  
-   <span data-ttu-id="e5d70-111">Senarai harga</span><span class="sxs-lookup"><span data-stu-id="e5d70-111">Price list</span></span>  
 
<span data-ttu-id="e5d70-112">Dalam langkah ini, anda juga akan menunjukkan jenis peruntukan sumber yang anda mahu:</span><span class="sxs-lookup"><span data-stu-id="e5d70-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="e5d70-113">**Tengah**.</span><span class="sxs-lookup"><span data-stu-id="e5d70-113">**Central**.</span></span> <span data-ttu-id="e5d70-114">Hanya pengurus sumber boleh menguntukkan sumber untuk projek.</span><span class="sxs-lookup"><span data-stu-id="e5d70-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="e5d70-115">**Hibrid**.</span><span class="sxs-lookup"><span data-stu-id="e5d70-115">**Hybrid**.</span></span> <span data-ttu-id="e5d70-116">Pengurus sumber, pengurus projek dan pengurus akaun boleh menguntukkan sumber untuk projek.</span><span class="sxs-lookup"><span data-stu-id="e5d70-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="e5d70-117">Untuk menetapkan parameter projek:</span><span class="sxs-lookup"><span data-stu-id="e5d70-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="e5d70-118">Pergi ke **Project Service > Parameter**.</span><span class="sxs-lookup"><span data-stu-id="e5d70-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="e5d70-119">Klik tetapan parameter yang anda mahu konfigurasikan (tetapan yang anda cipta ketika pertama kali anda memasang [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]) atau klik **Baharu** untuk mencipta tetapan baharu.</span><span class="sxs-lookup"><span data-stu-id="e5d70-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="e5d70-120">Dalam kawasan **Umum**, tetapkan pilihan untuk parameter projek anda.</span><span class="sxs-lookup"><span data-stu-id="e5d70-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="e5d70-121">Dalam kawasan **Senarai Harga**, klik **+** untuk menambah senarai harga dalam senarai juntai bawah **Senarai Harga Parameter Projek** dan kemudian klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="e5d70-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="e5d70-122">Klik butang **Simpan** di sudut kanan bawah skrin.</span><span class="sxs-lookup"><span data-stu-id="e5d70-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="e5d70-123">Rekod parameter projek mesti diselenggara untuk Project Service berfungsi dengan betul.</span><span class="sxs-lookup"><span data-stu-id="e5d70-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="e5d70-124">Rekod ini tidak boleh dipadamkan.</span><span class="sxs-lookup"><span data-stu-id="e5d70-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="e5d70-125">Lihat Juga</span><span class="sxs-lookup"><span data-stu-id="e5d70-125">See Also</span></span>  
 [<span data-ttu-id="e5d70-126">Sediakan sumber</span><span class="sxs-lookup"><span data-stu-id="e5d70-126">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]