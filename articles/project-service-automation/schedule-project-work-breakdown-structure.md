---
title: Jadualkan projek dengan struktur pecahan kerja
description: Cara untuk menjadualkan projek dengan struktur pecahan kerja dalam Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ca9b899c-7791-4990-b02e-cdff7f652621
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 003a1c543163b7ef1df1221d0b633a078e6619cf
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753954"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>Jadualkan projek dengan struktur pecahan kerja (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Jadual projek menyampaikan kerja yang perlu dilaksanakan, sumber yang akan melaksanakan kerja dan jangka masa kerja perlu dilengkapkan. Jadual projek menunjukkan semua kerja yang berkaitan dengan penghantaran projek pada masanya. Salah satu langkah pertama dalam fasa permulaan projek adalah untuk muncul dengan jadual projek. Untuk mewujudkan jadual projek, anda perlu mencipta struktur pecahan kerja.  
  
 Cipta struktur projek dengan struktur pecahan kerja yang membantu anda:  
  
- Pecahkan kerja kepada tugas boleh diuruskan  
  
- Anggarkan masa yang diperlukan untuk melengkapkan tugas  
  
- Tetapkan kebergantungan tugas dan tempoh tugas  
  
- Tentukan peranan yang diperlukan untuk melengkapkan setiap tugas  
  
  Jadual projek dalam struktur pecahan kerja mempunyai penampilan dan suasana yang biasa, lengkap dengan carta Gantt yang interaktif.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Cipta struktur pecahan kerja untuk projek  
 Cipta struktur pecahan kerja untuk menunjukkan urutan tugas dalam projek. Struktur pecahan kerja merangkumi tugas, keperluan untuk setiap tugas serta maklumat hasil dan kos. Dalam struktur pecahan kerja anda, anda boleh menambah:  
  
-   Urutan tugas dalam hierarki  
  
-   Tugas lain, jika ada, yang mesti dilengkapkan sebelum tugas boleh dimulakan  
  
-   Tarikh mula, tarikh tamat dan tempoh tugas  
  
-   Bilangan jam yang diperlukan untuk tugas  
  
-   Sebarang kemahiran dan pendidikan pekerja yang diperlukan  
  
-   Pekerja yang ditugaskan kepada tugas  
  
-   Anggaran hasil dan kos  
  
## <a name="task-types"></a>Jenis tugas  
Anda akan menggunakan jenis tugas berikut ketika mencipta struktur pecahan kerja anda:  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Nod akar projek** | Tugas ringkas peringkat atas untuk projek. Semua tugas projek lain dicipta di bawahnya. Nama tugas akar ialah nama projek. Usaha, tarikh dan tempoh nod akar adalah berdasarkan nilai dalam hierarki di bawahnya. Anda tidak boleh mengedit sifat nod akar atau memadan nod akar. | 
| **Tugas ringkas atau bekas** | Tugas ringkas ialah tugas yang mempunyai sub tugas di bawahnya. Tugas ringkas tidak mempunyai sebarang usaha kerja atau kosnya sendiri. Usaha kerja dan kosnya adalah himpunan sub tugasnya. Anda boleh mengubah nama tugas ringkas tetapi anda tidak boleh mengubah usaha, tarikh atau tempoh kerana ia dikira secara automatik. Tindakan memadam tugas ringkas akan memadam tugas dan semua sub tugasnya.|  
| **Tugas nod daun** | Tugas nod daun menunjukkan kerja paling terperinci dalam projek. Ia mengandungi anggaran usaha, bilangan sumber yang dirancang, tarikh mula dan tamat yang dirancang dan tempoh.|

  
## <a name="task-hierarchy"></a>Hierarki tugas  
 Anda mempunyai pilihan berikut ketika mencipta hierarki tugas:  
  
- **Tambah tugas**.   Anda boleh menambah tugas pada kedudukan yang anda pilih dalam hierarki tugas. Jika anda tidak memilih kedudukan, tugas baharu anda muncul di bahagian hujung.  
  
- **Engsot masuk tugas**.   Engsot masuk tugas untuk menjadikannya anak kepada tugas yang berada secara terus di atasnya.  
  
- **Engsot keluar tugas**.   Engsot keluar tugas untuk menjadikannya bukan lagi sub tugas bagi tugas induk asalnya.  
  
- **Alih ke atas dan Alih ke bawah**.   Alihkan tugas ke atas dan ke bawah dalam hierarki tugas induknya. Mengalihkan tugas ke atas dan ke bawah tidak memberi kesan kepada usaha, kos, tarikh dan tempohnya.  
  
## <a name="task-attributes"></a>Atribut tugas  
 Nama tugas menerangkan kerja yang perlu dilengkapkan. Anda menggunakan pelbagai atribut tugas untuk menghuraikan keperluan jadual dan kakitangan untuk tugas.  
  
### <a name="schedule-attributes"></a>Atribut jadual

 - Tetapkan nilai untuk **Jam usaha**, **Bilangan sumber**, **Tarikh mula**, **Tarikh tamat** dan **Tempoh** untuk menentukan jadual untuk tugas. 
 - **Usaha** ialah anggaran jam yang diperlukan untuk melengkapkan tugas.
 - **Bilangan sumber** ialah anggaran yang pengurus projek letak dalam tugas untuk membantu menghasilkan jadual yang sebaik mungkin. 
 - **Tempoh** (dalam hari) menunjukkan bilangan hari bekerja yang diperlukan untuk melengkapkan tugas.  
  
### <a name="staffing-attributes"></a>Atribut kakitangan

 - **Peranan**, **Unit organisasi sumber**, **Bilangan sumber** dan **Sumber** menghuraikan keperluan kakitangan untuk tugas. 
 - **Peranan** menghuraikan jenis sumber yang diperlukan untuk melaksanakan tugas. 
 - **Unit organisasi sumber** menunjukkan unit organisasi dari mana sumber patut diambil bekerja untuk tugas tersebut; ini juga memberi kesan kepada anggaran kos dan jualan tugas, kerana ini diambil kira ketika menentukan harga jualan unit untuk sumber. 
 - **Sumber** mempunyai sumber generik atau sumber bernama apabila ia ditemui.  
  
## <a name="task-dependencies"></a>Pergantungan tugas  
 Anda boleh mencipta perhubungan terdahulu antara satu atau lebih tugas dalam struktur pecahan kerja. Anda boleh menetapkan satu atau lebih nilai untuk medan yang terdahulu pada tugas untuk menunjukkan tugas yang ia akan bergantung padanya. Apabila anda menetapkan nilai terdahulu untuk tugas, ia hanya boleh bermula apabila semua tugas terdahulu telah dilengkapkan. Penetapan pergantungan ini pada tugas akan menghasilkan pengiraan semula tarikh mula tugas yang dirancang sebagai penamat terkini semua tugas terdahulunya. Kesan berkaitan tugas terdahulu pada jadual tidak dihadkan oleh mod tugas yang ditakrifkan pada tugas.  
  
## <a name="task-mode"></a>Mod tugas  
 Mod tugas ialah salah satu faktor penting yang menentukan penjadualan tugas nod daun. Terdapat dua mod tugas bagi setiap tugas: mod penjadualan auto dan mod penjadualan manual.  
  
-   **Penjadualan auto**.   Apabila anda menetapkan mod tugas kepada Dijadualkan Secara Automatik, enjin penjadualan tugas menggunakan peranan penjadualan pada atribut tugas berikut untuk menentukan jadual bagi tugas:  
  
    -   Pendahulu  
  
    -   Usaha  
  
    -   Bilangan sumber  
  
    -   Tarikh mula dan tamat  
  
-   **Peraturan penjadualan**.   Tarikh mula tugas nod daun yang tidak mempunyai lalai pendahuluan untuk tarikh mula penjadualan projek. Tempoh tugas nod daun sentiasa dikira sebagai bilangan hari bekerja antara tarikh mula dan tamatnya. Apabila tugas dijadualkan secara automatik, enjin penjadualan mengikut peraturan di bawah:  
  
    -   Tarikh mula dan tamat tugas mesti sentiasa hari bekerja mengikut kalendar penjadualan projek  
  
    -   Tarikh mula tugas yang mempunyai lalai pendahuluan untuk tarikh tamat terkini pendahuluannya  
  
    -   Usaha = Bilangan orang * Tempoh * jam dalam hari kerja standard bagi kalendar projek  
  
-   **Penjadualan manual**.   Dalam sesetengah kes, anda mungkin mahu menyimpang daripada peraturan ini. Dalam kes ini, anda boleh menetapkan mod tugas untuk tugas dijadualkan secara manual. Ini akan menghentikan enjin penjadualan daripada mengira nilai untuk atribut penjadualan lain. Penetapan tugas terdahulu pada tugas sentiasa memberi kesan kepada tarikh mula tugas yang bergantung.  
  
## <a name="create-a-work-breakdown-structure"></a>Cipta struktur pecahan kerja  
  
1.  Pergi ke **Project Service > Projek**.  
  
2.  Klik program y ang anda mahu kerjakan.  
  
3.  Dalam bar yang merentas bahagian atas skrin, pilih anak panah ke bawah di sebelah nama projek dan kemudian klik Struktur pecahan kerja.  
  
4.  Untuk menambah tugasan, klik **Tambah tugas**. Isikan medan untuk tugas dan kemudian klik **Simpan**.  
  
5.  Teruskan menambah tugas sehingga struktur pecahan kerja anda selesai. Ketika mencipta struktur pecahan kerja anda, anda boleh melakukan perkara berikut untuk mengatur tugas anda:  
  
    -   Pilih tugas dan klik **Engsot masuk** untuk mengalihkannya di bawah tugas lain atau klik Engsot keluar untuk mengalihkannya keluar daripada peringkat.  
  
    -   Pilih tugas dan klik **Alih Ke Atas** atau **Alih Ke Bawah** untuk mengalihkannya ke atas atau ke bawah dalam senarai.  
  
    -   Klik **Sembunyikan Gantt** untuk menyembunyikan carta Gantt dan klik **Tunjukkan Gantt** untuk memaparkannya semula.  
  
    -   Pilih tempoh masa yang berbeza untuk carta Gantt dalam **Skala Masa**.  
  
6.  Untuk menambah peranan yang anda tentukan dalam struktur pecahan kerja anda untuk ahli pasukan projek anda, klik **Janakan Pasukan Projek**.  
  
7.  Klik **Simpan** di sudut kanan bawah skrin apabila anda selesai membuat perubahan.  
  
### <a name="see-also"></a>Lihat Juga  
 [Panduan pengurus projek](../project-service/project-manager-guide.md)
