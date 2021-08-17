---
title: Penjejakan jualan projek
description: Topik ini menyediakan maklumat tentang cara Project Operations menjejaki kemajuan berbanding hasil buruh pada projek.
author: rumant
ms.date: 03/24/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 78d7bdaf9f5ca1757273cb81a1303befb0357ba547eb354097786fc3c38962b9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995592"
---
# <a name="project-sales-tracking"></a>Penjejakan jualan projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Dynamics 365 Project Operations menjejaki anggaran dan hasil buruh dengan butiran terendah yang diperlukan pada pelan projek. Anggaran hasil buruh adalah berdasarkan usaha yang dirancang dan sumber generik atau bernama yang ditugaskan kepada setiap tugas nod daun dalam pelan projek. Apabila projek bermula dan orang mula melaporkan masa untuk pelbagai tugas projek, hasil aktual untuk buruh diringkaskan yang memulakan pengiraan unjuran.

## <a name="labor-revenue-tracking-view"></a>Pandangan penjejakan hasil buruh

Pada halaman **Projek**, pada tab **Penjejakan**, anda boleh memilih **Penjejakan** > **Kos** untuk membuka pandangan **Penjejakan Kos**. Atau, anda boleh memilih **Gunakan** > **Kadar Bil** untuk membuka pandangan **Penjejakan Hasil**, yang menunjukkan kemajuan hasil buruh pada setiap tugas dalam pelan projek. Pandangan ini juga membandingkan hasil buruh aktual yang dibelanjakan untuk tugas kepada hasil buruh yang dirancang untuk tugas. Project Operations menggunakan formula berikut untuk mengira metrik hasil buruh:

- **Hasil yang dirancang**: Nilai jualan yang dianggarkan bagi semua tugasan sumber pada setiap tugas nod daun
- **Hasil Aktual**: Jumlah semua aktual jualan belum dibilkan untuk masa yang direkodkan pada tugas
- **Hasil Boleh DiBilkan%** : Hasil aktual ÷ Hasil anggaran ketika selesai
- **Baki Hasil** : Hasil anggaran ketika selesai – Hasil aktual
- **Hasil yang Dianggarkan ketika Selesai** : Baki hasil +Hasil aktual
- **Varians hasil** : Hasil yang Dirancang – Anggaran hasil ketika selesai


> [!NOTE]
> Project Operations hanya menunjukkan hasil buruh pada halaman **Projek** pada tab **Penjejakan**. Walaupun bahan dan perbelanjaan boleh dianggarkan dan dijejaki untuk penggunaan, hasil ini tidak disertakan dalam hasil yang ditunjukkan pada tab **Penjejakan**. Tab ini direka untuk berfungsi hanya untuk pengunjuran semula hasil buruh dengan usaha pengunjuran semula.  
> Semua amaun hasil yang ditunjukkan ditukarkan kepada mata wang kos projek. Mata wang kos projek ialah mata wang unit kontrak pada projek. Bagi projek harga tetap, nombor hasil pada pandangan **Penjejakan hasil buruh** tidak berkaitan kerana aktual jualan belum dibilkan tidak direkodkan pada kelulusan masa.
> Nilai jualan yang dianggarkan untuk masa yang ditunjukkan pada tab **Anggaran** projek tidak boleh ditambahkan kepada nilai hasil yang dirancang pada tab **Penjejakan**. Sumber percanggahan ini adalah disebabkan oleh dua sebab yang mungkin:
><ol>
   ><li> Tab <b>Anggaran</b> menunjukkan hasil yang dianggarkan dalam mata wang jualan, manakala tab <b>Penjejakan</b> menunjukkan hasil yang dirancang ditukarkan kepada mata wang kos. </li>
   ><li> Apabila jualan yang dianggarkan ditukarkan kepada mata wang kontrak seperti yang ditunjukkan pada tab <b>Anggaran</b>, kepada mata wang projek, penukaran melibatkan langkah yang boleh mengakibatkan kehilangan ketepatan: </li>
><ol>
><li> Amaun jualan yang dianggarkan dalam mata wang kontrak ditukarkan kepada mata wang asas terlebih dahulu (penukaran 1).</li>
><li> Amaun jualan yang dianggarkan dalam mata wang asas ditukarkan kepada mata wang kos projek (penukaran 2). </li>
></ol>
></ol>
> Ketepatan mata wang digunakan dalam kedua-dua langkah, yang mengakibatkan penyelewengan hasil yang dirancang dalam mata wang projek daripada jualan yang dirancang dalam mata wang kontrak.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>Hasil pengunjuran semula pada tugas nod daun

Hasil buruh pada tugas nod daun tidak boleh diunjurkan semula secara langsung pada tab **Penjejakan** pada halaman **Projek**. Walau bagaimanapun, anda boleh menggunakan pandangan **Penjejakan Usaha** untuk mengunjurkan semula baki usaha pada tugas. Ini menyebabkan pengiraan semula baki hasil pada tugas. Berikut ialah perihalan tentang cara ini berfungsi.

1. Pengurus projek boleh mengunjurkan semula usaha pada tugas dengan mengemaskini nilai lalai dalam medan **Baki Usaha** dengan anggaran baharu baki usaha pada tugas. Pengunjuran semula menyebabkan pengiraan semula anggaran usaha tugas ketika selesai (EAC), peratusan kemajuan dan varians usaha yang diunjurkan pada tugas. EAC, anggaran untuk selesai (ETC) dan peratusan kemajuan pada tugas ringkasan juga dikira semula dan menghasilkan unjuran baharu varians usaha.
2. Berdasarkan nilai baharu untuk baki usaha pada tugas, sistem mengira baki hasil pada pandangan **Penjejakan Hasil**. Untuk mengira baki hasil berdasarkan baki usaha, sistem mengira hasil purata satu jam usaha terlebih dahulu pada tugas seperti hasil yang dirancang atau usaha yang dirancang. Hasil yang dirancang ialah jumlah hasil semua tugasan sumber pada tugas. Hasil purata setiap jam digunakan untuk mengira baki hasil bagi baki usaha yang diunjurkan baharu pada tugas.
3. Hasil yang dianggarkan ketika selesai dan peratusan penggunaan hasil pada tugas nod daun dikira semula.
4. Nilai hasil ketika selesai bagi tugas ringkasan sehingga nod akar dikira semula.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Hasil pengunjuran semula pada tugas ringkasan

Anda boleh mengunjurkan semula hasil buruh pada tugas ringkasan atau tugas bekas. Walau bagaimanapun, anda tidak boleh mengunjurkan hasil buruh secara terus pada tugas projek ringkasan pada tab **Penjejakan** pada halaman **Projek**. Sama seperti tugas nod daun, pengunjuran semula tugas ringkasan dan bekas boleh dilakukan menggunakan pandangan **Penjejakan Usaha**. Dalam pandangan ini, anda boleh mengunjurkan semula baki usaha pada tugas ringkasan yang menyebabkan pengiraan semula baki hasil pada tugas ringkasan. Berikut ialah perihalan tentang cara ini berfungsi.

1. Pengurus projek boleh mengunjurkan semula usaha pada tugas dengan mengemas kini nilai lalai dalam medan **Baki Usaha** dengan anggaran baharu **Baki Usaha** pada tugas. Pengunjuran semula menyebabkan pengiraan semula anggaran tugas ketika selesai (EAC), peratusan kemajuan dan varians usaha yang diunjurkan pada tugas. EAC, ETC dan peratusan kemajuan pada tugas ringkasan juga dikira semula dan menghasilkan unjuran varians usaha baharu.
2. Berdasarkan nilai baharu dalam medan **Baki usaha** pada tugas, sistem mengira baki hasil dalam pandangan **Penjejakan Hasil**. Untuk mengira baki hasil berdasarkan baki usaha, sistem mengira hasil purata satu jam usaha terlebih dahulu pada tugas seperti hasil yang dirancang atau usaha yang dirancang. Hasil yang dirancang ialah jumlah hasil semua tugasan sumber pada tugas. Hasil purata setiap jam ini kemudian digunakan untuk mengira hasil bagi baki usaha yang diunjurkan baharu pada tugas.
3. Hasil yang dianggarkan ketika selesai dan peratusan penggunaan hasil pada tugas ringkasan dikira semula.
4. Nilai baharu untuk hasil yang dianggarkan ketika selesai diagihkan sehingga tugas anak dalam perkadaran yang sama dengan hasil yang dirancang asal pada tugas tersebut.
5. Hasil yang dianggarkan ketika selesai yang baharu pada setiap tugas individu sehingga tugas nod daun dikira. Berdasarkan nilai ini, tugas anak yang terjejas sehingga nod daun akan mempunyai baki hasil dan peratusan penggunaan hasil dikira semula berdasarkan nilai hasil ketika selesai. Ini menghasilkan unjuran baharu bagi varians hasil tugas tersebut. 
6. Nilai hasil ketika selesai bagi tugas ringkasan sehingga nod akar dikira semula.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

