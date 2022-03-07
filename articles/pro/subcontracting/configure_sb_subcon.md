---
title: Mengkonfigurasikan Lembaga Jadual untuk menunjukkan pekerja kontrak dan kapasiti subkontrak
description: Topik ini menerangkan cara mengkonfigurasikan Papan Jadual dalam Microsoft Dynamics 365 Project Operations untuk menunjukkan kapasiti sumber subkontrak apabila kakitangan keperluan sumber projek.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d645dee741a45dcb0219e4e4f58a329b7b873e10
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903067"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Mengkonfigurasikan Lembaga Jadual untuk menunjukkan pekerja kontrak dan kapasiti subkontrak 

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Papan Jadual dalam Microsoft Dynamics 365 Project Operations boleh digunakan untuk mencari sumber dalam dua cara:

- Carian sumber am tanpa konteks sebarang keperluan sumber berasaskan projek tertentu.
- Carian sumber khusus keperluan di mana keperluan projek akan menyediakan konteks untuk sumber yang dicadangkan.

Untuk memberitahu lembaga jadual kapasiti sumber subkontrak dan pekerja kontrak, anda perlu membuat kemas kini kepada tetapan Lembaga Jadual. Kemas kini ini termasuk: 
- Kemas kini Jadualkan Tetapan Papan untuk carian sumber am.
- Kemas kini Jadualkan seting Papan untuk carian sumber berasaskan keperluan.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Kemas kini seting Papan Jadual untuk carian sumber am
### <a name="update-filters-for-general-resource-search"></a>Kemas kini penapis untuk carian sumber am
Apabila anda mencari sumber, penapis yang tersedia pada papan jadual perlu dikemas kini supaya anda juga boleh mencari sumber luaran dengan menentukan mana-mana atau semua yang berikut:
  - Jenis pekerja, sama ada sumber yang ditunjukkan mestilah pekerja kontrak atau pekerja.
  - Syarikat vendor yang mana sumber harus dimiliki.
  - Sumber yang tergolong dalam subkontrak atau garis subkontrak tertentu.
    
### <a name="update-retrieve-resource-query"></a>Kemas kini mendapatkan semula pertanyaan sumber
Pertanyaan yang digunakan untuk carian juga perlu dikemas kini untuk menggunakan atribut penapis tambahan ini. Gunakan langkah berikut untuk mengemas kini konfigurasi Papan Jadual untuk carian sumber umum:  
1. Buka **Seting Papan Jadual untuk Papan Jadual** tertentu.
2. Buka **tab Seting Umum** dan skrol ke **Seting lain**.
3. Dalam senarai seting dalam seksyen ini, kemas kini **Susun Atur Penapis ke Susun Atur Penapis Lalai untuk Operasi Projek Lite** **·**.
4. Kemas kini **Dapatkan Semula Pertanyaan Sumber untuk Pertanyaan Sumber Ambil Semula Lalai untuk Operasi Projek Lite** **·**.

![Kemas kini seting Papan Jadual untuk carian sumber am](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Kemas kini seting Papan Jadual untuk carian sumber berasaskan keperluan
### <a name="update-filters-for-requirement-specific-resource-search"></a>Kemas kini penapis untuk carian sumber khusus keperluan 
Apabila anda mencari sumber, penapis yang tersedia pada papan jadual perlu dikemas kini supaya anda juga boleh mencari sumber luaran dengan menentukan mana-mana atau semua yang berikut:
 - Jenis pekerja, sama ada sumber yang ditunjukkan mestilah pekerja kontrak atau pekerja.
 - Syarikat vendor yang mana sumber harus dimiliki.
 - Sumber yang tergolong dalam subkontrak atau garis subkontrak tertentu.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Kemas kini mendapatkan semula pertanyaan sumber untuk carian sumber khusus keperluan 
Pertanyaan yang digunakan untuk carian juga perlu dikemas kini untuk menggunakan atribut penapis tambahan ini. Gunakan langkah berikut untuk mengemas kini konfigurasi Papan Jadual untuk carian sumber berasaskan keperluan:

1. Buka **Seting Papan Jadual untuk Papan Jadual tertentu kemudian pilih Buka seting Lalai untuk membuka seting untuk** carian khusus **keperluan**.
2. Buka **tab Seting Umum** dan skrol ke **Seting lain**.
3. Dalam senarai seting dalam seksyen ini, kemas kini **Susun Atur Penapis ke Susun Atur Penapis Lalai untuk Operasi Projek Lite** **·**.
4. Kemas kini **Dapatkan Semula Pertanyaan Sumber untuk Pertanyaan Sumber Ambil Semula Lalai untuk Operasi Projek Lite** **·**.
5. Buka **tab Jenis Jadual** dan pergi ke **Projek**.
6. Di bawah seting untuk **Projek**, kemas kini **Jadual Pembantu Mendapatkan Semula Sumber Pertanyaan untuk Lalai Mendapatkan Sumber Pertanyaan untuk Operasi Projek Lite dan** kemas kini Jadual Pembantu Dapatkan Semula **Pertanyaan** **Kekangan** untuk Lalai Mendapatkan **Semula Kekangan Pertanyaan untuk Operasi Projek Lite**.

![Kemas kini seting Papan Jadual untuk carian sumber berasaskan keperluan](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
