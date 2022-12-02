---
title: Penjejakan kos projek
description: Artikel ini menyediakan maklumat tentang cara Project Operations menjejak kemajuan berbanding kos buruh dan perbelanjaan pada projek.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c069a28c6dc546e5e632c4dff29686dc7965f23e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923751"
---
# <a name="labor-cost-tracking-on-projects"></a>Penjejakan kos buruh pada projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Dynamics 365 Project Operations menjejaki anggaran buruh dan perbelanjaan dengan butiran terendah yang diperlukan pada pelan projek. Anggaran kewangan kos buruh adalah berdasarkan usaha yang dirancang dan sumber generik atau bernama yang ditugaskan kepada setiap tugas nod daun dalam pelan projek. Apabila projek bermula dan orang mula melaporkan masa untuk pelbagai tugas projek, perbelanjaan aktual untuk buruh diringkaskan yang memulakan pengiraan unjuran.

## <a name="labor-cost-tracking-view"></a>Pandangan Penjejakan Kos Buruh

Pada halaman **Projek**, pada tab **Penjejakan**, anda boleh memilih **Penjejakan** > **Kos** untuk membuka pandangan **Penjejakan Kos** dan melihat kemajuan perbelanjaan buruh pada setiap tugas dalam pelan projek. Pandangan ini juga membandingkan kos buruh aktual yang dibelanjakan untuk tugas kepada kos buruh yang dirancang untuk tugas. Project Operations menggunakan formula berikut untuk mengira metrik kos buruh:

- **Kos yang dirancang**: Kos yang dianggarkan bagi semua tugasan sumber pada setiap tugas nod daun
- **Kos Aktual**: Jumlah semua kos aktual untuk masa yang direkodkan pada tugas
- **Peratusan penggunaan kos**: Kos aktual ÷ Kos anggaran ketika selesai
- **Baki Kos**: Kos anggaran ketika selesai – Kos aktual
- **Kos ketika Selesai**: Baki kos + Kos aktual
- **Varians Kos**: Kos yang dirancang - Kos anggaran ketika selesai

Setiap tugas menunjukkan unjuran varians kos pada tugas. Jika kos anggaran ketika selesai lebih banyak daripada kos yang dirancang, tugas diunjurkan untuk melebihi belanjawan. Jika kos anggaran ketika selesai lebih kurang daripada kos yang dirancang, tugas diunjurkan untuk selesai di bawah belanjawan.

>[!NOTE]
> Project Operations hanya menunjukkan kos buruh pada halaman **Projek** pada tab **Penjejakan**. Walaupun bahan dan perbelanjaan boleh dianggarkan dan dijejaki untuk penggunaan, kos ini tidak disertakan dalam kos yang ditunjukkan pada tab **Penjejakan**. Tab ini direka untuk berfungsi hanya untuk pengunjuran semula kos buruh dengan usaha pengunjuran semula.
Semua amaun kos yang ditunjukkan ditukar kepada mata wang kos projek daripada mata wang harga kos projek yang digunakan untuk menentukan kadar kos. Mata wang kos projek ialah mata wang unit kontrak pada projek. Nilai kos anggaran untuk masa yang ditunjukkan pada tab **Anggaran** pada halaman **Projek** mungkin tidak ditambahkan pada kos yang dirancang pada tab **Penjejakan**. Sebab percanggahan ini adalah kerana perbezaan dalam cara kos dianggarkan diringkaskan pada grid **Anggaran** dan cara kos yang dirancang dikira pada grid **Penjejakan**. 
>
> - Tab **Anggaran** mengira kos yang dianggarkan dengan menggunakan mata wang kadar kos yang sama dalam senarai harga. Kemudian, kos yang dianggarkan dalam mata wang senarai harga ditukarkan kepada kos yang dianggarkan dalam mata wang kos projek. Kos anggaran dalam mata wang projek ditunjukkan dibundarkan kepada 2 tempat perpuluhan. Pada bila-bila masa semasa penukaran ini ketepatan mata wang digunakan. 
> - Pada tab **Penjejakan**, pengiraan kos yang dirancang mengikut urutan pengiraan yang sedikit berbeza yang melibatkan ketepatan mata wang yang digunakan dalam dua peringkat: 
   ><ol>
   ><li>Amaun kos yang dianggarkan dalam mata wang senarai harga ditukarkan kepada mata wang asas (penukaran 1).</li>
   ><li>Amaun kos yang dianggarkan dalam mata wang asas ditukarkan kepada mata wang kos projek (penukaran 2). </li>
   ></ol>
   >Ketepatan mata wang digunakan dalam kedua-dua langkah untuk mendapatkan kos yang dirancang (pada tab **Penjejakan**) yang menyimpang sedikit daripada kos yang dianggarkan (pada pandangan **Masa - berfasa** pada tab **Anggaran**). 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>Kos pengunjuran semula pada tugas nod daun

Kos buruh pada tugas nod daun tidak boleh diunjurkan semula secara langsung pada tab **Penjejakan** pada **Halaman projek**. Walau bagaimanapun, anda boleh menggunakan pandangan **Penjejakan Usaha** untuk mengunjurkan semula baki usaha pada tugas. Ini menyebabkan pengiraan semula baki kos pada tugas. Berikut ialah perihalan tentang cara ini berfungsi.

1. Pengurus projek boleh mengunjurkan semula usaha pada tugas dengan mengemaskini nilai lalai dalam medan **Baki Usaha** dengan anggaran baharu baki usaha pada tugas. Pengunjuran semula menyebabkan pengiraan semula anggaran usaha tugas ketika selesai (EAC), peratusan kemajuan dan varians usaha yang diunjurkan pada tugas. EAC, anggaran untuk selesai (ETC) dan peratusan kemajuan pada tugas ringkasan juga dikira semula dan menghasilkan unjuran baharu varians usaha.
2. Berdasarkan nilai baharu untuk baki usaha pada tugas, sistem mengira baki kos pada pandangan **Penjejakan Kos**. Untuk mengira baki kos berdasarkan baki usaha, sistem mengira kos purata satu jam usaha terlebih dahulu pada tugas seperti kos yang dirancang atau usaha yang dirancang. Kos yang dirancang ialah jumlah kos semua tugasan sumber pada tugas. Kos purata setiap jam digunakan untuk mengira baki kos bagi baki usaha yang diunjurkan baharu pada tugas.
3. Kos ketika selesai dan peratusan penggunaan kos pada tugas nod daun dikira semula.
4. Nilai kos ketika selesai bagi tugas ringkasan sehingga ke nod akar dikira semula.

## <a name="reprojecting-costs-on-summary-tasks"></a>Kos pengunjuran semula pada tugas ringkasan

Anda boleh mengunjurkan semula kos buruh pada tugas ringkasan atau tugas bekas. Walau bagaimanapun, anda boleh mengunjurkan kos buruh secara terus pada tugas projek ringkasan pada tab **Penjejakan** pada halaman **Projek**. Sama seperti tugas nod daun, pengunjuran semula tugas ringkasan dan bekas boleh dilakukan menggunakan pandangan **Penjejakan Usaha**. Dalam pandangan ini, anda boleh mengunjurkan semula baki usaha pada tugas ringkasan yang menyebabkan pengiraan semula baki kos pada tugas ringkasan. Berikut ialah perihalan tentang cara ini berfungsi.

1. Pengurus projek boleh mengunjurkan semula usaha pada tugas ringkasan dengan mengemas kini nilai lalai bagi baki usaha dengan anggaran baharu pada tugas. Pengemaskinian ini menyebabkan pengiraan semula anggaran tugas ringkasan ketika selesai (EAC), peratusan kemajuan dan varians usaha yang diunjurkan pada tugas. EAC, ETC dan peratusan kemajuan pada tugas ringkasan juga dikira semula dan menghasilkan unjuran varians usaha baharu.
2. Berdasarkan nilai baharu untuk baki usaha pada tugas ringkasan, sistem mengira baki kos pada pandangan **Penjejakan Kos**. Untuk mengira baki kos berdasarkan baki usaha, sistem mengira kos purata satu jam usaha terlebih dahulu pada tugas ringkasan seperti kos yang dirancang atau usaha yang dirancang. Kos purata setiap jam digunakan untuk mengira kos bagi baki usaha yang diunjurkan baharu pada tugas ringkasan.
3. Kos ketika selesai dan peratusan penggunaan kos pada tugas ringkasan dikira semula.
4. Kos ketika selesai yang baharu diagihkan sehingga ke tugas anak dalam perkadaran yang sama dengan kos yang dirancang asal pada tugas tersebut.
5. Nilai kos ketika selesai yang baharu pada setiap tugas individu sehingga tugas nod daun dikira. Berdasarkan nilai ini, tugas anak yang terjejas sehingga nod daun akan mempunyai baki kos dan peratusan penggunaan kos dikira semula berdasarkan nilai kos ketika selesai. Nilai ini menghasilkan unjuran baharu bagi varians kos tugas tersebut. 


Medan **Prestasi kos** boleh ditetapkan daripada data penjejakan. Apabila varians kos untuk nod akar dalam pandangan **Penjejakan kos** adalah negatif, anda boleh menetapkan medan ini kepada **Bawah Belanjawan**. Apabila varians kos untuk nod akar adalah positif, anda boleh menetapkan nilai kepada **Melebihi Belanjawan**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
