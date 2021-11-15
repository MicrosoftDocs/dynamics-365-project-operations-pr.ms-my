---
title: Cipta struktur pecahan kerja
description: Topik ini menerangkan cara untuk mencipta struktur pecahan kerja (WBS) termasuk kawalan asas dalam antara muka penjadualan baru.
author: ruhercul
ms.date: 06/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f77450d0d754606dd336072248012fea462510a4
ms.sourcegitcommit: a12d21c7cab296f5b6a3181d76a06f57dee1267c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/19/2021
ms.locfileid: "7655428"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>Cipta struktur pecahan kerja (WBS)

Jadual projek menyampaikan kerja yang mesti diselesaikan, sumber yang akan melakukan kerja dan jangka masa kerja mesti diselesaikan. Jadual menunjukkan semua kerja yang berkaitan dengan penghantaran projek pada masanya. Dalam Dynamics 365 Project Operations, anda mencipta jadual projek dengan:

  - Memecahkan kerja kepada tugas yang boleh diuruskan.
  - Menganggarkan masa yang diperlukan untuk melakukan setiap tugas.
  - Menetapkan kebergantungan tugas.
  - Menetapkan tempoh tugas.
  - Menganggarkan sumber generik yang akan melakukan tugas. 

Jadual projek dicipta pada tab **Jadual** pada halaman **Projek**.

## <a name="tasks"></a>Tugas

Langkah pertama dalam mencipta jadual projek ialah untuk membahagikan kerja kepada bahagian yang boleh diuruskan. Jadual dalam Project Operations menyokong ciri yang berikut:

- Tugas ringkas atau bekas
- Tugas nod daun

### <a name="summary-tasks"></a>Tugas ringkasan

Tugas ringkasan boleh menyimpan tugas ringkasan lain atau tugas nod daun. Ia tidak mempunyai usaha kerja atau kos sendiri. Sebaliknya, usaha kerja dan kos ia ialah gulung atas bagi usaha kerja dan kos tugas bekas ia. Tarikh mula tugas ringkasan ialah tarikh mula tugas bekas dan tarikh tamat ialah tarikh tamat tugas bekas. Nama tugas ringkasan boleh diedit tetapi sifat penjadualan, termasuk usaha, tarikh dan tempoh, tidak boleh diedit. Jika anda memadamkan tugas ringkasan, anda juga akan memadamkan semua tugas bekasnya.

### <a name="leaf-node-tasks"></a>Tugas nod daun

Tugas nod daun mewakili kerja yang paling berbutir pada projek itu. Ia mengandungi anggaran usaha, sumber, tarikh mula dan tamat yang dirancang dan tempoh.

## <a name="create-a-task-hierarchy"></a>Ccipta hierarki tugas

### <a name="add-a-task"></a>Tambah tugas

Lengkapkan langkah berikut untuk menambah satu atau lebih tugas.

1. Pergi ke **Projek** dan pilih dan buka rekod projek untuk yang anda mahu cipta jadual. 
2. Pilih tab **Tugasan**. 
3. Pilih **Tambah tugas baharu**, masukkan nama untuk tugas, dan kemudian tekan Enter.
2. Masukkan nama tugas lain dan tekan Enter lagi sehingga anda mempunyai senarai penuh tugas.

### <a name="manage-hierarchy-of-a-task"></a>Uruskan hierarki tugas

Apabila tugas diengsot, ia menjadi anak tugas yang terus berada di atasnya. ID jadual tugas kemudiannya dikira semula supaya ia berdasarkan kepada ID jadual induk barunya dan mengikut skema penomboran rangka. Tugas induk kini merupakan tugas ringkas. Oleh itu, ia menjadi gulung atas bagi tugas anaknya. Apabila tugas dipromosikan, ia tidak lagi menjadi anak kepada tugas yang merupakan induknya. ID jadual kemudian dikira semula supaya ia menunjukkan kedalaman dan kedudukan yang dikemas kini bagi tugas tersebut dalam hierarki. Usaha, kos dan tarikh tugas induk sebelumnya dikira semula supaya ia tidak memasukkan tugas ini.

Lengkapkan langkah berikut untuk inden atau promosikan tugas.

1. Pada halaman **Projek**, pada tab **Tugas**, di bawah **Tugas ringkasan**, pilih tiga titik menegak dengan nama tugas dan kemudian pilih **Buat subtugas**. 
2. Pilih tugas untuk inden atau mempromosikan. Untuk memilih lebih daripada satu tugas, pilih tugas, tekan dan tahan Ctrl dan kemudian pilih tugas tambahan.
2. Pilih **Inden** atau **Promosikan subtugas**  untuk menggerakkan tugas di bawah atau keluar daripada tugas ringkasan.

### <a name="move-tasks-up-and-down"></a>Gerakkan tugas ke atas dan ke bawah

Tugas boleh dipindahkan ke mana-mana tahap dalam struktur pecahan kerja dalam salah satu daripada dua cara:

- Pilih satu lagi tugas dan seretnya ke lokasi yang dikehendaki.
- Pilih satu atau lebih tugas, klik kanan dan pilih **Potong**, pilih sel destinasi dalam jadual, dan kemudian klik kanan dan pilih **Tampal**.

## <a name="task-attributes"></a>Atribut tugas

Nama tugas menerangkan kerja yang mesti dilengkapkan. Dalam Project Operations, atribut yang dikaitkan dengan tugas menerangkan jadual tugas dan keperluan kakitangannya.

## <a name="schedule-attributes"></a>Atribut jadual

Atribut **Usaha**, **Tarikh mula**, **Tarikh tamat** dan **Tempoh** menentukan jadual untuk tugas.

Jadual berikut menunjukkan atribut jadual tambahan.

| **Nama paparan terakhir** | **Perihalan terakhir** |
| --- | --- |
| Usaha Dilengkapkan (Jam) | Kerja dilengkapkan untuk tugas dalam jam. |
| Tempoh | Paparkan tempoh dalam hari untuk transaksi. |
| Jumlah Usaha | Jumlah kerja untuk tugas dalam jam. |
| Siap | Tarikh dan masa tamat. |
| % Selesai | Peratusan tugas yang lengkap. |
| Baldi Projek | Papan tugas boleh dikumpulkan mengikut baldi supaya setiap baldi mempunyai lajur sendiri. |
| Usaha Selebihnya (Jam) | Kerja selebihnya untuk tugas dalam jam. |
| Mulakan | Tarikh dan masa mula. |
| Nama | Nama tugas. |
| ID | ID tugas dalam struktur pecahan kerja. |

Sebagai pentadbir, anda boleh menentukan medan tersuai pada entiti tugas. Walau bagaimanapun, medan tidak boleh dipaparkan pada grid jadual. Untuk melihat medan tersuai anda, tambahkannya pada halaman butiran **Tugas Projek**.

## <a name="staffing-attributes"></a>Atribut kakitangan

Atribut kakitangan diakses melalui medan **Sumber** dalam Jadual. Anda boleh sama ada mencari sumber sedia ada atau pilih **Cipta**, dan dalam anak tetingkap **Cipta Cepat**, tambah ahli pasukan projek sebagai sumber baharu.

Medan **Peranan**, **Unit Sumber** dan **Nama Kedudukan** digunakan untuk menerangkan keperluan kakitangan untuk tugas tersebut. Atribut kakitangan ini, berserta dengan jadual tugas digunakan untuk mencari sumber tersedia untuk melakukan tugas ini.

   - **Peranan**: Tentukan jenis sumber yang diperlukan untuk melakukan tugas.
   - **Unit sumber**: Tentukan unit yang sumber untuk tugas perlu ditugaskan. Atribut ini memberi kesan kepada anggaran kos dan jualan bagi tugas jika kos dan kadar bil untuk sumber ditetapkan berdasarkan unit sumber.
   - **Nama kedudukan**: Masukkan nama mesra untuk sumber generik yang berfungsi sebagai ruang letak untuk sumber yang akhirnya akan melakukan kerja.

Medan **Sumber** memegang nama kedudukan bagi sumber generik atau sumber yang dinamakan apabila ia dijumpai.

Medan **Kategori** memegang nilai yang menunjukkan jenis kerja yang lebih luas yang tugas boleh dikumpulkan di dalamnya. Medan ini tidak menjejaskan penjadualan atau pengambilan kakitangan. Sebaliknya, medan digunakan hanya untuk pelaporan.

## <a name="task-dependencies"></a>Pergantungan tugas

Anda boleh menggunakan jadual dalam Project Operations untuk mencipta perhubungan pendahulu antara tugas. Medan **Pendahulu** menggunakan satu atau lebih nilai untuk menunjukkan tugas yang sesuatu tugas itu bergantung. Apabila nilai pendahulu ditugaskan pada satu tugas, tugasan tersebut boleh bermula hanya selepas semua tugas pendahulu telah selesai. Disebabkan kebergantungan, tarikh mula yang dirancang bagi tugas ditetapkan semula ke tarikh apabila tugas pendahulu telah dilengkapkan.

Mod tugas tidak memberi kesan ke atas kemas kini yang dibuat pada tarikh mula dan tamat tugas pendahulu/bersandar.

## <a name="accessibility-and-keyboard-shortcuts"></a>Kebolehcapaian dan pintasan papan kekunci

Grid **Jadual** boleh diakses sepenuhnya dan boleh digunakan dengan pembaca skrin seperti Pencerita, JAWS atau NVDA. Anda boleh bergerak melalui kawasan grid dengan menggunakan kekunci anak panah (seperti dalam Microsoft Excel), anda boleh menggunakan kekunci Tab untuk maju melalui elemen antaramuka pengguna interaktif dan anda boleh menggunakan kekunci anak panah Bawah, kekunci Enter atau Bar Ruang untuk memilih dan buka menu ke bawah.

## <a name="project-limitations"></a>Batasan projek 
Anda harus sedar batasan berikut jika anda menggunakan struktur pecahan kerja dalam Project Operations. Had ini diguna pakai pada projek dan tugas. Untuk mendapatkan maklumat lanjut, lihat [had dan sempadan Project for the web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

| **Medan**                                          |  **Had**           |
|----------------------------------------------------|----------------------|
| Jumlah tugas maksimum untuk projek                  | 500                  |
| Jumlah tempoh maksimum untuk projek               | 3,650 hari (10 tahun) |
| Jumlah sumber maksimum untuk projek              | 150                  |
| Jumlah pautan maksimum (pengganti sahaja) untuk projek | 600                  |
| Jumlah medan tersuai maksimum untuk projek          | 10                   |

**Batasan tugas**

| **Medan**                               |   **Had**           |
|-----------------------------------------|-----------------------|
| Tahap hierarki maksimum                 | 10 tahap             |
| Pautan maksimum (pengganti + pendahulu) | 20                    |
| Tempoh maksimum tugas daun           | 1250 hari             |
| Tempoh maksimum tugas ringkasan      | 3,650 hari (10 tahun)  |
| Sumber maksimum ditugaskan kepada tugas    | 20 sumber          |
| Julat tarikh yang disokong untuk tugas         | 1/1/2000 - 31/12/2149 |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
