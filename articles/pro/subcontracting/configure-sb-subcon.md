---
title: Konfigurasikan Papan Jadual untuk menunjukkan pekerja kontrak dan kapasiti yang disubkontrak
description: Artikel ini menerangkan cara mengkonfigurasi Papan Jadual dalam Microsoft Dynamics 365 Project Operations untuk menunjukkan kapasiti sumber subkontrak apabila mengambil kakitangan keperluan sumber projek.
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

Papan Jadual dalam Microsoft Dynamics 365 Project Operations boleh digunakan untuk carian sumber dalam dua cara:

- Carian sumber umum tanpa konteks apa-apa keperluan sumber berasaskan projek khusus.
- Carian sumber khusus keperluan apabila keperluan projek akan menyediakan konteks untuk sumber yang dicadangkan.

Untuk memberitahu papan jadual tentang kapasiti sumber subkontrak dan pekerja kontrak, anda perlu membuat kemas kini kepada tetapan Papan Jadual. Kemas kini ini termasuklah: 
- Kemas kini tetapan Papan Jadual untuk carian sumber umum.
- Kemas kini tetapan Papan Jadual untuk carian sumber berdasarkan keperluan.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Kemas kini tetapan Papan Jadual untuk carian sumber umum
### <a name="update-filters-for-general-resource-search"></a>Kemas kini penapis untuk carian sumber umum
Apabila anda mencari sumber, penapis yang tersedia pada papan jadual perlu dikemas kini supaya anda boleh mencari sumber luaran juga dengan menentukan mana-mana atau semua perkara berikut:
  - Jenis pekerja, sama ada sumber yang ditunjukkan hendaklah pekerja kontrak atau pekerja.
  - Syarikat vendor yang sumber hendaklah tergolong.
  - Sumber yang tergolong dalam subkontrak atau baris subkontrak khusus.
    
### <a name="update-retrieve-resource-query"></a>Kemas kini pertanyaan dapatkan sumber
Pertanyaan yang digunakan untuk carian juga perlu dikemas kini untuk menggunakan atribut penapis tambahan ini. Gunakan langkah berikut untuk mengemas kini konfigurasi Papan Jadual untuk carian sumber umum:  
1. Buka **Tetapan Papan Jadual** papan Papan Jadual khusus.
2. Buka tab **Tetapan umum** dan tatal ke **Tetapan lain**.
3. Dalam senarai tetapan dalam bahagian ini, kemas kini **Tataletak Penapis** kepada **Tataletak Penapis Lalai untuk Project Operations Lite**.
4. Kemas kini **Pertanyaan Dapatkan Sumber** kepada **Pertanyaan Dapatkan Sumber Lalai untuk Project Operations Lite**.

![Kemas kini tetapan Papan Jadual untuk carian sumber umum](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Kemas kini tetapan Papan Jadual untuk carian sumber berdasarkan keperluan
### <a name="update-filters-for-requirement-specific-resource-search"></a>Kemas kini penapis untuk carian sumber khusus keperluan 
Apabila anda mencari sumber, penapis yang tersedia pada papan jadual perlu dikemas kini supaya anda boleh mencari sumber luaran juga dengan menentukan mana-mana atau semua perkara berikut:
 - Jenis pekerja, sama ada sumber yang ditunjukkan hendaklah pekerja kontrak atau pekerja.
 - Syarikat vendor yang sumber hendaklah tergolong.
 - Sumber yang tergolong dalam subkontrak atau baris subkontrak khusus.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Kemas kini pertanyaan dapatkan sumber untuk carian sumber khusus keperluan 
Pertanyaan yang digunakan untuk carian juga perlu dikemas kini untuk menggunakan atribut penapis tambahan ini. Gunakan langkah berikut untuk mengemas kini konfigurasi Papan Jadual untuk carian sumber khusus keperluan:

1. Buka **Tetapan Papan Jadual** untuk Papan Jadual khusus dan kemudian pilih **Buka Tetapan lalai** untuk membuka tetapan bagi carian khusus keperluan.
2. Buka tab **Tetapan umum** dan tatal ke **Tetapan lain**.
3. Dalam senarai tetapan dalam bahagian ini, kemas kini **Tataletak Penapis** kepada **Tataletak Penapis Lalai untuk Project Operations Lite**.
4. Kemas kini **Pertanyaan Dapatkan Sumber** kepada **Pertanyaan Dapatkan Sumber Lalai untuk Project Operations Lite**.
5. Buka tab **Jenis Jadual** dan pergi ke **Projek**.
6. Di bawah tetapan untuk **Projek**, kemas kini **Dapatkan Pembantu Jadual Pertanyaan Sumber** kepada **Dapatkan Pertanyaan Sumber Lalai untuk Project Operations Lite** dan kemas kini **Dapatkan Pembantu Jadual Pertanyaan Kekangan** untuk **Dapatkan Pertanyaan Kekangan Lalai untuk Project Operations Lite**.

![Kemas kini tetapan Papan Jadual untuk carian sumber berdasarkan keperluan](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
