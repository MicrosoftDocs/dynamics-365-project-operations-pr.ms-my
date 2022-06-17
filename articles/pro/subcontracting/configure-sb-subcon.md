---
title: Konfigurasikan Papan Jadual untuk menunjukkan pekerja kontrak dan kapasiti yang disubkontrak
description: Artikel ini menerangkan cara mengkonfigurasi Papan Jadual dalam Microsoft Dynamics 365 Project Operations untuk menunjukkan kapasiti sumber subkontrak apabila kakitangan keperluan sumber projek.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b965fd5011a575354f50c47081be198ab43248f9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919841"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Konfigurasikan Papan Jadual untuk menunjukkan pekerja kontrak dan kapasiti yang disubkontrak 

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Papan Jadual dalam Microsoft Dynamics 365 Project Operations boleh digunakan untuk mencari sumber dalam dua cara:

- Carian sumber am tanpa konteks sebarang keperluan sumber berasaskan projek tertentu.
- Keperluan - carian sumber khusus di mana keperluan projek akan memberikan konteks untuk sumber yang dicadangkan.

Untuk memberitahu lembaga jadual kapasiti sumber subkontrak dan pekerja kontrak, anda perlu membuat kemas kini pada tetapan Papan Jadual. Kemas kini ini termasuk: 
- Kemas kini tetapan Papan Jadual untuk carian sumber umum.
- Kemas kini tetapan Papan Jadual untuk carian sumber berasaskan keperluan.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Kemas kini seting Papan Jadual untuk carian sumber am
### <a name="update-filters-for-general-resource-search"></a>Kemas kini penapis untuk carian sumber umum
Apabila anda mencari sumber, penapis yang tersedia di papan jadual harus dikemas kini supaya anda juga boleh mencari sumber luaran dengan menentukan mana-mana atau semua yang berikut:
  - Jenis pekerja, sama ada sumber yang ditunjukkan mestilah pekerja kontrak atau pekerja.
  - Syarikat vendor yang mana sumber harus dimiliki.
  - Sumber yang tergolong dalam subkontrak atau subkontrak tertentu.
    
### <a name="update-retrieve-resource-query"></a>Kemas kini pertanyaan sumber ambil semula
Pertanyaan yang digunakan untuk mencari juga harus dikemas kini untuk menggunakan atribut penapis tambahan ini. Gunakan langkah berikut untuk mengemas kini konfigurasi Papan Jadual untuk carian sumber umum:  
1. Buka **Tetapan** Papan Jadual untuk Papan Jadual tertentu.
2. **Buka tab Seting** umum dan skrol ke **Seting lain**.
3. Dalam senarai seting dalam seksyen ini, kemas kini **Tataletak** Penapis Penapis kepada **Tataletak Penapis Lalai untuk Project Operations Lite**.
4. Kemas kini **Dapatkan Pertanyaan** Sumber untuk **Pertanyaan Sumber Lalai untuk Operasi Projek Lite**.

![Kemas kini seting Papan Jadual untuk carian sumber am](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Kemas kini seting Papan Jadual untuk carian sumber berasaskan keperluan
### <a name="update-filters-for-requirement-specific-resource-search"></a>Kemas kini penapis untuk carian sumber khusus keperluan 
Apabila anda mencari sumber, penapis yang tersedia di papan jadual harus dikemas kini supaya anda juga boleh mencari sumber luaran dengan menentukan mana-mana atau semua yang berikut:
 - Jenis pekerja, sama ada sumber yang ditunjukkan mestilah pekerja kontrak atau pekerja.
 - Syarikat vendor yang mana sumber harus dimiliki.
 - Sumber yang tergolong dalam subkontrak atau subkontrak tertentu.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Kemas kini pertanyaan sumber ambil untuk carian sumber khusus keperluan 
Pertanyaan yang digunakan untuk mencari juga harus dikemas kini untuk menggunakan atribut penapis tambahan ini. Gunakan langkah berikut untuk mengemas kini konfigurasi Papan Jadual untuk carian sumber berasaskan keperluan:

1. Buka **Seting** Papan Jadual untuk Papan Jadual tertentu dan kemudian pilih **Buka tetapan** Lalai untuk membuka tetapan untuk carian khusus keperluan.
2. **Buka tab Seting** umum dan skrol ke **Seting lain**.
3. Dalam senarai seting dalam seksyen ini, kemas kini **Tataletak** Penapis Penapis kepada **Tataletak Penapis Lalai untuk Project Operations Lite**.
4. Kemas kini **Dapatkan Pertanyaan** Sumber untuk **Pertanyaan Sumber Lalai untuk Operasi Projek Lite**.
5. **Buka tab Jenis** Jadual dan pergi ke **Projek**.
6. Di bawah seting untuk **Projek, kemas kini** Jadual Penolong Mendapatkan Pertanyaan **Sumber untuk** Pertanyaan Sumber Lalai untuk Operasi Projek Lite **dan kemas kini** Jadual Penolong Mendapatkan Pertanyaan **Kekangan kepada** Pertanyaan Kekangan Pengambilan Lalai untuk Operasi Projek **Lite**.

![Kemas kini seting Papan Jadual untuk carian sumber berasaskan keperluan](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
