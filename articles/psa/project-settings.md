---
title: Tetapan projek
description: Topik ini memberikan maklumat tentang tetapan pengurusan projek.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: ca5fc63d56ddd84871949e38f421bcdfe38d478e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148159"
---
# <a name="project-settings"></a>Tetapan projek

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Gunakan tetapan berikut untuk mengakses ciri perancangan projek.

## <a name="work-template"></a>Templat kerja

Untuk mencipta jadual projek, anda cipta templat kalendar projek yang mentakrifkan bilangan jam kerja setiap hari dan sebarang penutupan perniagaan. Untuk mencipta templat kalendar projek, anda kaitkan templat kerja dengan medan **Templat kalendar** untuk projek. Ikuti langkah ini untuk mencipta templat kerja.

1. Dalam PSA, dalam anak tetingkap navigasi kiri, klik **Sumber**. 
2. Pada halaman senarai **Sumber**, buka rekod pengguna dan kemudian pilih **Tunjuk Jam Kerja**.

  > [!NOTE]
  > Pastikan anda membenarkan tetimbul pada halaman pelayar. Ini membenarkan anda melihat jam kerja yang ditetapkan untuk sumber.
  
3. Pada tab **Pandangan Bulanan**, klik **Sediakan**. Satu senarai tiga pilihan muncul: 

  - Jadual Mingguan Baharu
  - Jadual Kerja untuk Satu Hari
  - Masa Rehat

> ![Sediakan pilihan](media/project-13.png)

4. Pilih **Jadual Mingguan Baharu** dan kemudian tetapkan pilihan untuk jadual sumber ini. Anda boleh menetapkan jadual mingguan berulang, parameter jam harian, penutupan perniagaan dan banyak lagi.
5. Tetapkan julat tarikh, pilih **Simpan** dan kemudian klik **Tutup**. 
6. Kembali ke halaman senarai **Sumber** dan pilih sumber yang anda tetapkan jam kerja. 
7. Pilih **Tetapkan Kalendar Sebagai** untuk menetapkan templat kerja. 
8. Dalam kotak dialog **Templat Kerja**, masukkan nama untuk templat kerja dan kemudian pilih **Gunakan**. 

Kini anda boleh mengaitkan templat kerja dengan templat kalendar projek.

## <a name="resource-roles"></a>Peranan sumber

Istilah *peranan sumber* merujuk kepada set kemahiran, kecekapan dan pensijilan yang seseorang mesti ada untuk melakukan satu set tugas tertentu pada projek. PSA membolehkan anda menetapkan kos dan mengebilkan masa sumber berdasarkan peranan yang dikaitkan dengan sumber tersebut. Setiap organisasi mesti menyediakan peranan ini dengan menggunakan navigasi kiri pada menu **Project Service**.

Setiap organisasi mesti menyediakan peranan ini pada halaman **Kategori Sumber Aktif**. Untuk membuka halaman ini, dalam anak tetingkap navigasi kiri, pilih **Peranan Sumber**.

## <a name="price-lists"></a>Senarai harga

Senarai harga membolehkan anda menetapkan kos dan harga jualan untuk peranan sumber, kategori perbelanjaan, produk dan elemen lain dalam organisasi. Sebelum anda menetapkan anggaran kewangan untuk kerja yang mesti dihantar bagi sesuatu projek, anda harus mencipta senarai kos sokongan dan harga jualan. Dalam bahagian parameter, anda juga perlu menyediakan senarai kos dan harga jualan lalai yang digunakan pada semua projek yang dicipta dalam organisasi. Pada halaman **Parameter Projek Aktif**, pastikan anda menyediakan senarai kos dan harga jualan lalai.
