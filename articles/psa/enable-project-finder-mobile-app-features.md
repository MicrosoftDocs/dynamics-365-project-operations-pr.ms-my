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
ms.openlocfilehash: 749c5682dc2e639843a0a8a085fe8af65502d433
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081235"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Dayakan ciri aplikasi Project Finder Mobile (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Sumber anda boleh menggunakan aplikasi Project Finder Mobile pada telefon mereka dengan [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] untuk mencari projek baharu untuk diusahakan dan mengemas kini set kemahiran mereka.  
  
 Aplikasi tersedia untuk [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], telefon [!INCLUDE[tn_android](../includes/tn-android.md)] dan [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
  
 Anda perlu menetapkan beberapa pilihan dalam tetapan parameter untuk unit organisasi anda bagi membolehkan pengguna melihat keperluan sumber projek dan mengemas kini kemahiran mereka.  
  
> [!NOTE]
>  Aplikasi Project Finder Mobile hanya berfungsi dengan [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], bukan dengan pemasangan di premis.  
  
1. Pergi ke **Project Service > Parameter**.  
  
2. Klik tetapan parameter yang anda mahu gunakan untuk membolehkan ciri aplikasi Project Finder Mobile.  
  
3. Dalam kawasan **Umum** , tetapkan **Keperluan sumber dapat dilihat oleh sumber** kepada **Ya**.  
  
4. Tetapkan **Benarkan kemas kini oleh sumber** kepada **Ya**.  
  
   ![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Ini adalah tetapan global. Pengurus projek boleh menetapkan sama ada projek individu akan dapat dilihat pada halaman **Pasukan Projek** projek.  
  
   ![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>Pemberitahuan e-mel  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] menghantar e-mel berkenaan permintaan sumber kepada penerima berikut pada masa yang berikut:  
  
|Penerima|Peristiwa|  
|---------------|-----------|  
|Pengurus projek|-   Apabila sumber mendaftar untuk projek dengan aplikasi Project Finder Mobile.|  
|Sumber|-   Apabila kerja projek yang sumber telah daftarkan telah dipenuhi oleh sumber lain.<br />-   Apabila permintaan kelulusan kemahiran mereka telah diluluskan atau ditolak.<br />-   Apabila permintaan pendaftaran projek telah diluluskan atau ditolak.|  
  
## <a name="privacy-notice"></a>Notis privasi  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Lihat Juga  
 [Sediakan sumber](../psa/set-up-resources.md)
