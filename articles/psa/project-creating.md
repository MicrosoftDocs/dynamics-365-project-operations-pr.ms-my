---
title: Jadual projek
description: Topik ini memberikan maklumat tentang cara untuk mencipta jadual.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: 9a6b27050a19d8a7f2ed35f74b42bb4f371ad069
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081263"
---
# <a name="project-schedules"></a>Jadual projek 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Jadual projek menyampaikan kerja yang mesti diselesaikan, sumber yang akan melakukan kerja dan jangka masa kerja mesti diselesaikan. Ia menunjukkan semua kerja yang berkaitan dengan penghantaran projek tepat pada masanya. Dalam Dynamics 365 Project Service Automation, anda cipta jadual projek dengan membahagikan kerja kepada tugas boleh diuruskan, menganggarkan masa yang diperlukan untuk melakukan setiap tugas, menetapkan kebergantungan tugas, menetapkan tempoh tugas dan menganggarkan sumber generik yang akan melakukan tugas. Jadual projek dicipta pada tab **Jadual** halaman projek.
 
## <a name="tasks"></a>Tugas

Langkah pertama dalam mencipta jadual projek ialah untuk membahagikan kerja kepada bahagian yang boleh diuruskan. Jadual dalam PSA menyokong ciri yang berikut:

- Nod akar projek
- Tugas ringkas atau bekas
- Tugas nod daun

### <a name="project-root-node"></a>Nod akar projek

Nod akar projek ialah tugas ringkasan peringkat atas bagi projek. Semua tugas projek lain dicipta di bawahnya. Nama nod akar selalunya ditetapkan pada nama projek. Usaha, tarikh dan tempoh nod akar diringkaskan berdasarkan nilai dalam hierarki di bawahnya. Anda tidak boleh mengedit sifat nod akar. Anda juga tidak boleh memadamkan nod akar.

### <a name="summary-or-container-tasks"></a>Tugas ringkas atau bekas 

Tugas ringkasan mempunyai subtugas atau tugas bekas di bawahnya. Ia tidak mempunyai usaha kerja atau kos sendiri. Sebaliknya, usaha kerja dan kos ia ialah gulung atas bagi usaha kerja dan kos tugas bekas ia. Tarikh mula tugas ringkasan ialah tarikh mula tugas bekas dan tarikh tamat ialah tarikh tamat tugas bekas. Nama tugas ringkasan boleh diedit tetapi sifat penjadualan (usaha, tarikh dan tempoh) tidak boleh diedit. Jika anda memadamkan tugas ringkasan, anda juga akan memadamkan semua tugas bekasnya.

### <a name="leaf-node-tasks"></a>Tugas nod daun

Tugas nod daun mewakili kerja yang paling berbutir pada projek itu. Ia mengandungi anggaran usaha, sumber, tarikh mula dan tamat yang dirancang dan tempoh.
 
## <a name="creating-a-task-hierarchy"></a>Mencipta hierarki tugas

Anda boleh mencipta hierarki tugas dengan menggunakan pilihan berikut:

- Butang **Tambah tugas**
- Butang **Tugas engsot**
- Butang **Tugas engsot keluar**
- Butang **Gerak ke atas** dan **Gerak ke bawah**
- Kebolehcapaian dan pintasan papan kekunci

### <a name="add-task"></a>Tambah tugas

Butang **Tambah tugas** membolehkan anda mencipta tugas baharu dalam hierarki. Jika anda tidak memilih kedudukan, tugas dimasukkan di bahagian hujung. 

ID jadual ditugaskan pada setiap tugas. ID jadual mewakili kedalaman dan kedudukan tugas dalam hierarki. Ia menggunakan penomboran rangka. Untuk tugas dalam peringkat pertama di bawah nod akar projek, skema penomboran 1, 2, 3 dan seterusnya, digunakan. Untuk tugas di bawah peringkat pertama, skema penomboran 1.1, 1.2, 1.3 dan seterusnya, digunakan.

### <a name="indent-task"></a>Engsot masuk tugas.

Apabila tugas diengsot, ia menjadi anak tugas yang terus berada di atasnya. ID jadual tugas kemudiannya dikira semula supaya ia berdasarkan kepada ID jadual induk barunya dan mengikut skema penomboran rangka. Tugas induk kini ialah tugas ringkasan atau tugas bekas. Oleh itu, ia menjadi gulung atas bagi tugas anaknya.

### <a name="outdent-task"></a>Engsot keluar tugas 

Apabila tugas diengsot keluar, ia tidak lagi menjadi anak kepada tugas yang merupakan induknya. ID jadual kemudian dikira semula supaya ia menunjukkan kedalaman dan kedudukan yang dikemas kini bagi tugas tersebut dalam hierarki. Usaha, kos dan tarikh tugas induk sebelumnya dikira semula supaya ia tidak memasukkan tugas ini.

### <a name="move-up-and-move-down"></a>Gerak ke atas dan Gerak ke bawah. 

Butang **Gerak ke atas** dan **Gerak ke bawah** mengubah kedudukan tugas dalam hierarki induknya. Perubahan jenis ini tidak menjejaskan usaha, kos, tarikh atau tempoh tugas. Hanya ID jadual tugas yang terjejas. ID jadual dikira semula supaya ia menunjukkan kedudukan baharu tugas dalam senarai tugas anak induk.

### <a name="accessibility-and-keyboard-shortcuts"></a>Kebolehcapaian dan pintasan papan kekunci

Grid **Jadual** boleh diakses sepenuhnya dan boleh digunakan dengan pembaca skrin seperti Pencerita, JAWS atau NVDA. Anda boleh bergerak melalui kawasan grid dengan menggunakan kekunci anak panah (seperti dalam Microsoft Excel), anda boleh menggunakan kekunci Tab untuk maju melalui elemen UI interaktif dan anda boleh menggunakan kekunci anak panah Bawah, kekunci Enter atau Bar Ruang untuk memilih dan menggunakan menu ke bawah. Pengepala lajur juga interaktif. Anda boleh sembunyikan dan tunjukkan lajur, gunakan kekunci Tab dan kekunci anak panah untuk bergerak melalui pengepala lajur dan menggunakan butang tindakan pada bar alat. Selain itu, anda boleh menggunakan pintasan papan kekunci berikut:

- **Segar semula** : ALT+SHIFT+F5
- **Tambah** : ALT+SHIFT+Insert
- **Padam** : ALT+SHIFT+Delete
- **Bergerak ke atas/bawah** : ALT+SHIFT+anak panah Atas/Bawah
- **Engsot/Engsot keluar** : ALT_SHIFT+anak panah Kiri/Kanan
- **Kembangkan/Runtuhkan Hierarki** : Alt + Shift +kekunci Tambah/Tolak

## <a name="task-attributes"></a>Atribut tugas

Nama tugas menerangkan kerja yang mesti dilengkapkan. Dalam PSA, atribut yang berkaitan dengan tugas menerangkan jadual tugas dan keperluan kakitangannya.

> ![Atribut tugas](media/project-2.png)
 
### <a name="schedule-attributes"></a>Atribut jadual

Atribut **Usaha** , **Tarikh mula** , **Tarikh tamat** dan **Tempoh** menentukan jadual untuk tugas.

Atribut jadual tambahan termasuk:

- **Jam usaha** : Masukkan anggaran jam yang diperlukan untuk melengkapkan tugas. 
- **Tempoh** : Tentukan bilangan hari kerja yang diperlukan untuk melengkapkan tugas.
- **ID Jadual** : ID yang dijana secara automatik ini digunakan untuk memesan tugas dalam hierarki. Kebergantungan antara tugas menguruskan pesanan sebenar bagi tugas diusahakan di dalamnya.
 
### <a name="staffing-attributes"></a>Atribut kakitangan

Atribut kakitangan diakses melalui medan **Sumber** dalam Jadual. Anda boleh sama ada mencari sumber sedia ada atau klik **Cipta** dan dalam anak tetingkap **Cipta Cepat** , tambah ahli pasukan projek sebagai sumber baharu.

Medan **Peranan** , **Unit Sumber** dan **Nama Kedudukan** digunakan untuk menerangkan keperluan kakitangan untuk tugas tersebut. Atribut kakitangan ini berserta dengan jadual tugas digunakan untuk mencari sumber tersedia untuk melakukan tugas ini.

**Peranan** - Tentukan jenis sumber yang diperlukan untuk melakukan tugas.

**Unit sumber** - Tentukan unit yang sumber untuk tugas perlu ditugaskan. Atribut ini memberi kesan kepada anggaran kos dan jualan bagi tugas jika kos dan kadar bil untuk sumber ditetapkan berdasarkan unit sumber.

**Nama kedudukan** – Masukkan nama mesra untuk sumber generik yang berfungsi sebagai ruang letak untuk sumber yang akhirnya akan melakukan kerja.

Medan **Sumber** memegang nama kedudukan bagi sumber generik atau sumber yang dinamakan apabila ia dijumpai.

Medan **Kategori** memegang nilai yang menunjukkan jenis kerja yang lebih luas yang tugas boleh dikumpulkan di dalamnya. Medan ini tidak menjejaskan penjadualan atau pengambilan kakitangan. Ia hanya digunakan untuk pelaporan.

### <a name="task-dependencies"></a>Pergantungan tugas 

Anda boleh menggunakan jadual dalam PSA untuk mencipta perhubungan pendahulu antara tugas. Medan **Pendahulu** di bawah **Tugas** mengambil satu atau lebih nilai untuk menunjukkan tugas yang sesuatu tugas itu bergantung. Apabila nilai pendahulu ditugaskan pada satu tugas, tugasan tersebut boleh bermula hanya selepas semua tugas pendahulu telah selesai. Disebabkan kebergantungan, tarikh mula yang dirancang bagi tugas ditetapkan semula ke tarikh apabila tugas pendahulu telah dilengkapkan.

Mod tugas tidak memberi kesan ke atas kemas kini yang dibuat pada tarikh mula dan tamat tugas pendahulu/bersandar.

## <a name="task-mode"></a>Mod tugas 

Mod tugas menentukan penjadualan bagi tugas nod daun. PSA menyokong dua mod tugas bagi setiap tugas: penjadualan automatik dan penjadualan manual.

### <a name="auto-scheduling"></a>Penjadualan automatik 
 
Apabila mod tugas ditetapkan kepada **Dijadualkan Secara Automatik** bagi satu tugas, enjin penjadualan tugas menggunakan peraturan penjadualan pada atribut tugas untuk menentukan jadual untuk tugas tersebut.

#### <a name="scheduling-rules"></a>Peraturan penjadualan

Secara lalai, jika tugas nod daun tidak mempunyai pendahulu, tarikh mulanya ditetapkan kepada tarikh mula yang dijadualkan bagi projek. Tempoh tugas nod daun sentiasa dikira sebagai bilangan hari bekerja antara tarikh mula dan tamatnya. Apabila tugas dijadualkan secara automatik, enjin penjadualan mengikut peraturan di ini:

- Tarikh mula dan tamat tugas mesti hari bekerja, mengikut kalendar penjadualan projek. 
- Untuk sebarang tugas yang mempunyai tugas pendahulu, tarikh mula ditetapkan secara automatik kepada tarikh tamat terkini pendahulunya.
- Usaha dikira dengan menggunakan formula ini: Bilangan orang × Tempoh × Jam dalam hari kerja standard dalam kalendar projek.

### <a name="manual-scheduling"></a>Penjadualan manual

Jika peraturan penjadualan automatik tidak memenuhi keperluan anda, anda boleh menetapkan mod tugas untuk tugas itu kepada **Dijadualkan Secara Manual**. Tetapan ini menghentikan enjin penjadualan daripada mengira nilai atribut penjadualan yang lain. Tanpa mengira mod tugas, jika anda menetapkan pendahulu pada tugas, anda sentiasa mempengaruhi tarikh mula tugas bersandar.
