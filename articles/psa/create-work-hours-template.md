---
title: Cipta templat waktu kerja
description: Artikel ini menerangkan cara mencipta templat waktu kerja dalam Project Service.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 8f3ac17a29e79f86f7c3ce127edb4b02ca63ea04
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916069"
---
# <a name="create-a-work-hours-template-project-service"></a>Cipta templat waktu kerja (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

Untuk mencipta dan mengurus projek, anda mesti menggunakan templat kalendar ke projek. Templat kalendar mentakrifkan atribut projek berikut:

- Waktu bekerja termasuk masa mula dan masa tamat
- Hari bekerja
- Pengecualian kalendar seperti hari tidak bekerja

Templat kalendar yang digunakan ke projek ialah salinan templat kalendar yang ditakrifkan dalam tetapan organisasi anda.

> [!NOTE]
> Jika anda menukar templat kalendar, perubahan itu tidak tersebar ke waktu kerja projek. Untuk menukar waktu kerja projek, templat baharu mesti digunakan.

Untuk mencipta templat kalendar bagi organisasi anda, terdapat dua keperluan utama:

- Takrifkan waktu kerja yang dikehendaki bagi templat menggunakan sumber boleh ditempah baharu atau sedia ada.
- Cipta templat kalendar baharu dan kaitkan templat dengan sumber oleh ditempah.

**Takrif waktu bekerja bagi templat**

1. Pergi ke **Sumber** \> **Sumber**.
2. Cipta sumber baharu untuk dirujuk dalam templat kalendar atau pilih sumber sedia ada.
3. Pilih tab **Waktu Kerja** bagi sumber dan lengkapkan arahan dalam [Tetapkan waktu kerja untuk sumber](/dynamics365/field-service/set-work-hours-resource) untuk mengkonfigurasikan peraturan kalendar.

**Cipta templat kalendar baharu**

1. Pergi ke **Tetapan** \> **Templat Kalendar**.
2. Pilih **Baharu** dan masukkan nama, perihalan dan sumber templat.


> [!NOTE]
> Apabila sumber dirujuk dalam templat kalendar, salinan kalendar sumber dikaitkan dengan templat kalendar. Jika waktu bekerja bagi templat yang disalin berubah, perubahan itu tidak tersebar ke templat kalendar.


### <a name="see-also"></a>Lihat Juga  
 [Sediakan sumber](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
