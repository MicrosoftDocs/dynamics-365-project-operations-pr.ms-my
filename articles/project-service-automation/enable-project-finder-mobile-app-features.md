---
title: Dayakan ciri-ciri aplikasi Project Finder Mobile
description: Cara untuk mendayakan ciri aplikasi Project Finder Mobile untuk Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 038c5c66-f136-4c7e-88c2-30ada80bbf38
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9265ee78b20899026277e5af8e589112cd9fac74
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753840"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="d837d-103">Dayakan ciri aplikasi Project Finder Mobile (Project Service)</span><span class="sxs-lookup"><span data-stu-id="d837d-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="d837d-104">Sumber anda boleh menggunakan aplikasi Project Finder Mobile pada telefon mereka dengan [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] untuk mencari projek baharu untuk diusahakan dan mengemas kini set kemahiran mereka.</span><span class="sxs-lookup"><span data-stu-id="d837d-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="d837d-105">Aplikasi tersedia untuk [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], telefon [!INCLUDE[tn_android](../includes/tn-android.md)] dan [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span><span class="sxs-lookup"><span data-stu-id="d837d-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="d837d-106">Anda perlu menetapkan beberapa pilihan dalam tetapan parameter untuk unit organisasi anda bagi membolehkan pengguna melihat keperluan sumber projek dan mengemas kini kemahiran mereka.</span><span class="sxs-lookup"><span data-stu-id="d837d-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d837d-107">Aplikasi Project Finder Mobile hanya berfungsi dengan [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], bukan dengan pemasangan di premis.</span><span class="sxs-lookup"><span data-stu-id="d837d-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="d837d-108">Pergi ke **Project Service > Parameter**.</span><span class="sxs-lookup"><span data-stu-id="d837d-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="d837d-109">Klik tetapan parameter yang anda mahu gunakan untuk membolehkan ciri aplikasi Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="d837d-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="d837d-110">Dalam kawasan **Umum**, tetapkan **Keperluan sumber dapat dilihat oleh sumber** kepada **Ya**.</span><span class="sxs-lookup"><span data-stu-id="d837d-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="d837d-111">Tetapkan **Benarkan kemas kini oleh sumber** kepada **Ya**.</span><span class="sxs-lookup"><span data-stu-id="d837d-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="d837d-112">![ProjectService_ProjectFinderEnable](../project-service/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="d837d-112">![ProjectService_ProjectFinderEnable](../project-service/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="d837d-113">Ini adalah tetapan global.</span><span class="sxs-lookup"><span data-stu-id="d837d-113">This is a global setting.</span></span> <span data-ttu-id="d837d-114">Pengurus projek boleh menetapkan sama ada projek individu akan dapat dilihat pada halaman **Pasukan Projek** projek.</span><span class="sxs-lookup"><span data-stu-id="d837d-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="d837d-115">![ProjectService_ProjectTeamVisible](../project-service/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="d837d-115">![ProjectService_ProjectTeamVisible](../project-service/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="d837d-116">Pemberitahuan e-mel</span><span class="sxs-lookup"><span data-stu-id="d837d-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="d837d-117">menghantar e-mel berkenaan permintaan sumber kepada penerima berikut pada masa yang berikut:</span><span class="sxs-lookup"><span data-stu-id="d837d-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="d837d-118">Penerima</span><span class="sxs-lookup"><span data-stu-id="d837d-118">Recipient</span></span>|<span data-ttu-id="d837d-119">Peristiwa</span><span class="sxs-lookup"><span data-stu-id="d837d-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="d837d-120">Pengurus projek</span><span class="sxs-lookup"><span data-stu-id="d837d-120">Project manager</span></span>|<span data-ttu-id="d837d-121">-   Apabila sumber mendaftar untuk projek dengan aplikasi Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="d837d-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="d837d-122">Sumber</span><span class="sxs-lookup"><span data-stu-id="d837d-122">Resource</span></span>|<span data-ttu-id="d837d-123">-   Apabila kerja projek yang sumber telah daftarkan telah dipenuhi oleh sumber lain.</span><span class="sxs-lookup"><span data-stu-id="d837d-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="d837d-124">-   Apabila permintaan kelulusan kemahiran mereka telah diluluskan atau ditolak.</span><span class="sxs-lookup"><span data-stu-id="d837d-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="d837d-125">-   Apabila permintaan pendaftaran projek telah diluluskan atau ditolak.</span><span class="sxs-lookup"><span data-stu-id="d837d-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="d837d-126">Notis privasi</span><span class="sxs-lookup"><span data-stu-id="d837d-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="d837d-127">Lihat Juga</span><span class="sxs-lookup"><span data-stu-id="d837d-127">See Also</span></span>  
 [<span data-ttu-id="d837d-128">Sediakan sumber</span><span class="sxs-lookup"><span data-stu-id="d837d-128">Set up resources</span></span>](../project-service/set-up-resources.md)
