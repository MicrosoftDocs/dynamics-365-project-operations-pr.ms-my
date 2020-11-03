---
title: Lihat penggunaan boleh caj untuk sumber
description: Topik ini memberikan maklumat tentang pandangan penggunaan sumber.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 6daa6cfa1c6a237d8a1685123f7c1a6926418bfe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081250"
---
# <a name="view-chargeable-utilization-for-resources"></a>Lihat penggunaan boleh caj untuk sumber
 
**Pandangan Penggunaan** pada halaman **Penggunaan Sumber Project Service** menunjukkan penggunaan boleh caj untuk setiap sumber boleh ditempah. Disebabkan pandangan adalah berdasarkan papan jadual, anda akan mendapati banyak fungsi sama.

> ![Petikan skrin Pandangan Penggunaan](media/FAQ-utilization-1.png)
 

Pengiraan penggunaan boleh dituntut berfungsi seperti berikut:

   Pengguna boleh caj = (Jam sebenar boleh caj) / (kapasiti sumber)

Sel mewakili penggunaan boleh dicaj dikira untuk tempoh tertentu (hari, minggu, atau bulan).

Warna dalam setiap sel menunjukkan penggunaan boleh dituntut untuk sumber berbanding dengan penggunaan boleh dituntut sasaran mereka. 

Penggunaan sasaran boleh ditetapkan atas peranan lalai sumber atau atas sumber individu itu sendiri. Pengiraan melihat kepada individu untuk sasaran dahulu, kemudian kepada peranan lalai sumber.

## <a name="set-target-on-a-resource"></a>Tetapkan sasaran pada sumber

1. Pergi ke **Sumber** \> **Sumber**. 
2. Pilih sumber untuk membuka rekod. 
3. Pada tab **Project Service** , anda boleh menetapkan penggunaan sasaran sumber.

> ![Petikan skrin menggunakan tab Project Service untuk menetapkan penggunaan sasaran](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Tetapkan penggunaan pada peranan

1. Pergi ke **Sumber** \> **Peranan Sumber**. 
2. Pilih peranan untuk membuka rekod. 
3. Tetapkan penggunaan sasaran untuk peranan.

> ![Petikan skrin menggunakan Peranan Sumber untuk menetapkan penggunaan sasaran](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>Kira penggunaan boleh caj untuk sumber

Untuk mengira penggunaan boleh caj untuk sumber, anda perlu melengkapkan pra-syarat tertentu. 

### <a name="set-default-role-for-individual-resource"></a>Tetapkan peranan lalai untuk sumber individu

Pertama, penggunaan sasaran mestilah ditetapkan kepada sama ada sumber individu atau pada peranan sumber. Jika anda menggunakan peranan sumber untuk sasaran, setiap sumber individu mesti mempunyai peranan lalai. 

1. Untuk tetapkan ini, pergi ke **Sumber** \> **Sumber**. 
2. Pilih sumber, buka rekod, kemudian pilih tab **Project Service**. 
3. Dalam grid **Peranan Sumber** , pastikan terdapat satu peranan untuk sumber dan **Adalah Lalai** ditetapkan kepada **Ya**.
 
### <a name="change-billing-type-for-resource-role"></a>Ubah pengebilan untuk peranan sumber

Peranan sumber mestilah ditetapkan kepada jenis pengebilan **Boleh caj**. 

1. Pergi ke **Sumber** \> **Peranan Sumber**. 
2. Buka rekod yang anda mahu kemas kini, kemudian tetapkan lalai jenis pengebilan kepada **Boleh caj**.

### <a name="set-working-hours-for-resource-role"></a>Tetapkan waktu bekerja untuk peranan sumber
 
Sumber mesti mempunyai jam kerja untuk pengiraan kapasiti. 

1. Pergi ke **Sumber** \> **Sumber**. 
2. Pilih sumber untuk membuka rekod, kemudian pilih **Tunjukkan Waktu Bekerja**. 
3. Anda boleh kemas kini pukal senarai sumber dengan mengggunakan **Templat Waktu Bekerja** daripada pandangan **Senarai Sumber**.

## <a name="troubleshooting-chargeable-actual-hours"></a>Menyelesaikan masalah jam sebenar boleh caj

Jam sebenar boleh caj adalah bersumber daripada entiti **Aktual**. Aktual dengan jenis pengebilan **Boleh Caj** adalah termasuk dalam pengiraan, dan atas sebab ini, anda mesti mempunyai projek di mana aktual adalah boleh caj.

Jika anda tidak melihat penggunaan boleh dituntut, berikut adalah beberapa perkara yang anda boleh semak:

- Sumber mempunyai jam kerja ditakrifkan untuk kapasiti.
- Sumber sama ada mempunyai sasaran penggunaan ditakrifkan secara individu atau mempunyai peranan lalai yang ditugaskan kepadanya. Peranan ini mempunyai sasaran penggunaan ditakrifkan untuknya.
- Aktual mempunyai jenis pengebilan **Boleh Caj** untuk tempoh yang anda jangkakan pengiraan penggunaan. Semak perkara berikut jika anda melihat aktual yang mempunyai jenis pengebilan selain daripada boleh caj:

  - Peranan yang digunakan sebenarnya mempunyai jenis pengebilan lalai bagi sesuatu selain daripada boleh dituntut.
  - Peranan pada baris kontrak projek yang menyokong projek telah ditetapkan kepada tidak boleh dituntut.
  - Projek ini tidak mempunyai baris kontrak yang berkaitan.

