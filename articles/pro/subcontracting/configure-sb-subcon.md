---
title: Konfigurasikan Papan Jadual untuk menunjukkan pekerja kontrak dan kapasiti yang disubkontrak
description: Artikel ini menerangkan cara mengkonfigurasikan Papan Jadual dalam Microsoft Dynamics 365 Project Operations untuk menunjukkan kapasiti sumber yang disubkontrak apabila keperluan sumber projek kakitangan.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 355691b63f437de789afab499369afcdf87e6d3d
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262228"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Konfigurasikan Papan Jadual untuk menunjukkan pekerja kontrak dan kapasiti yang disubkontrak 

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Papan Jadual dalam Microsoft Dynamics 365 Project Operations boleh digunakan untuk mencari sumber dalam dua cara:

- Carian sumber umum tanpa konteks sebarang keperluan sumber berasaskan projek tertentu.
- Keperluan - carian sumber khusus di mana keperluan projek akan memberikan konteks untuk sumber yang dicadangkan.

Untuk memaklumkan papan jadual kapasiti sumber subkontrak dan pekerja kontrak, anda perlu membuat kemas kini kepada tetapan Lembaga Jadual. Kemas kini ini termasuk: 
- Kemas kini tetapan Lembaga Jadual untuk carian sumber umum.
- Kemas kini seting Lembaga Jadual untuk carian sumber berdasarkan keperluan.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Mengemas kini seting Lembaga Jadual untuk carian sumber umum
### <a name="update-filters-for-general-resource-search"></a>Kemas kini penapis untuk carian sumber umum
Apabila anda mencari sumber, penapis yang tersedia pada papan jadual harus dikemas kini supaya anda juga boleh mencari sumber luaran dengan menentukan mana-mana atau semua yang berikut:
  - Jenis pekerja, sama ada sumber yang ditunjukkan mestilah pekerja kontrak atau pekerja.
  - Syarikat vendor yang mana sumber harus dimiliki.
  - Sumber yang tergolong dalam subkontrak atau subkontrak tertentu.
    
### <a name="update-retrieve-resource-query"></a>Mengemas kini semula pertanyaan sumber
Pertanyaan yang digunakan untuk carian juga harus dikemas kini untuk menggunakan atribut penapis tambahan ini. Gunakan langkah berikut untuk mengemas kini konfigurasi Papan Jadual untuk carian sumber umum:  
1. Tetapan **Papan Jadual Terbuka** untuk Papan Jadual tertentu.
2. Buka tab **Seting** am dan skrol ke **seting Lain**.
3. Dalam senarai seting dalam seksyen ini, kemas kini **Tataletak Penapis kepada** Tataletak Penapis Lalai untuk Project Operations **Lite**.
4. Kemas kini **Dapatkan Semula Pertanyaan** Sumber kepada **Pertanyaan Sumber Pulih Lalai untuk Operasi Projek Lite**.

![Mengemas kini seting Lembaga Jadual untuk carian sumber umum](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Kemas kini seting Lembaga Jadual untuk carian sumber berdasarkan keperluan
### <a name="update-filters-for-requirement-specific-resource-search"></a>Kemas kini penapis untuk carian sumber khusus keperluan 
Apabila anda mencari sumber, penapis yang tersedia pada papan jadual harus dikemas kini supaya anda juga boleh mencari sumber luaran dengan menentukan mana-mana atau semua yang berikut:
 - Jenis pekerja, sama ada sumber yang ditunjukkan mestilah pekerja kontrak atau pekerja.
 - Syarikat vendor yang mana sumber harus dimiliki.
 - Sumber yang tergolong dalam subkontrak atau subkontrak tertentu.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Mengemas kini semula pertanyaan sumber untuk carian sumber khusus keperluan 
Pertanyaan yang digunakan untuk carian juga harus dikemas kini untuk menggunakan atribut penapis tambahan ini. Gunakan langkah berikut untuk mengemas kini konfigurasi Lembaga Jadual untuk carian sumber berdasarkan keperluan:

1. Buka **Seting** Papan Jadual untuk Papan Jadual tertentu dan kemudian pilih **Buka seting** Lalai untuk membuka seting untuk carian khusus keperluan.
2. Buka tab **Seting** am dan skrol ke **seting Lain**.
3. Dalam senarai seting dalam seksyen ini, kemas kini **Tataletak Penapis kepada** Tataletak Penapis Lalai untuk Project Operations **Lite**.
4. Kemas kini **Dapatkan Semula Pertanyaan** Sumber kepada **Pertanyaan Sumber Pulih Lalai untuk Operasi Projek Lite**.
5. Buka tab **Jenis** Jadual dan pergi ke **Projek**.
6. Di bawah seting untuk **Project**, kemas kini **Pembantu Jadual Mendapatkan Semula Pertanyaan** Sumber untuk **Mendapatkan Semula Pertanyaan Sumber secara Lalai untuk Operasi Projek Lite** dan kemas kini **Pembantu Jadual Mendapatkan Semula Pertanyaan** Kekangan untuk **Lalai Mendapatkan Semula Pertanyaan Kekangan untuk Operasi Projek Lite**.

![Kemas kini seting Lembaga Jadual untuk carian sumber berdasarkan keperluan](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
