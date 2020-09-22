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
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Dayakan ciri aplikasi Project Finder Mobile (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Sumber anda boleh menggunakan aplikasi Project Finder Mobile pada telefon mereka dengan [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] untuk mencari projek baharu untuk diusahakan dan mengemas kini set kemahiran mereka.  
  
 Aplikasi tersedia untuk [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], telefon [!INCLUDE[tn_android](../includes/tn-android.md)] dan [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
  
 Anda perlu menetapkan beberapa pilihan dalam tetapan parameter untuk unit organisasi anda bagi membolehkan pengguna melihat keperluan sumber projek dan mengemas kini kemahiran mereka.  
  
> [!NOTE]
>  Aplikasi Project Finder Mobile hanya berfungsi dengan [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], bukan dengan pemasangan di premis.  
  
1. Pergi ke **Project Service > Parameter**.  
  
2. Klik tetapan parameter yang anda mahu gunakan untuk membolehkan ciri aplikasi Project Finder Mobile.  
  
3. Dalam kawasan **Umum**, tetapkan **Keperluan sumber dapat dilihat oleh sumber** kepada **Ya**.  
  
4. Tetapkan **Benarkan kemas kini oleh sumber** kepada **Ya**.  
  
   ![ProjectService_ProjectFinderEnable](../project-service/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Ini adalah tetapan global. Pengurus projek boleh menetapkan sama ada projek individu akan dapat dilihat pada halaman **Pasukan Projek** projek.  
  
   ![ProjectService_ProjectTeamVisible](../project-service/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>Pemberitahuan e-mel  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] menghantar e-mel berkenaan permintaan sumber kepada penerima berikut pada masa yang berikut:  
  
|Penerima|Peristiwa|  
|---------------|-----------|  
|Pengurus projek|-   Apabila sumber mendaftar untuk projek dengan aplikasi Project Finder Mobile.|  
|Sumber|-   Apabila kerja projek yang sumber telah daftarkan telah dipenuhi oleh sumber lain.<br />-   Apabila permintaan kelulusan kemahiran mereka telah diluluskan atau ditolak.<br />-   Apabila permintaan pendaftaran projek telah diluluskan atau ditolak.|  
  
## <a name="privacy-notice"></a>Notis privasi  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Lihat Juga  
 [Sediakan sumber](../project-service/set-up-resources.md)
