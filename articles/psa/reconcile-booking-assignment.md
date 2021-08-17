---
title: Menyelaraskan tempahan dan tugasan
description: Topik ini memberikan maklumat tentang aktual.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
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
ms.openlocfilehash: 264271a5be63cb2e51f175595a48bef5fbff0a42a37795c85dd5b4725deec35e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995142"
---
# <a name="reconcile-bookings-and-assignments"></a>Menyelaraskan tempahan dan tugasan

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Tempahan projek ahli pasukan projek dan tugasan tugas projek adalah digandingkan secara longgar. Oleh itu, sumber boleh mempunyai tugasan tugas yang tidak sepadan dengan tempahan dan tempahan yang tidak sepadan dengan tugasan tugas. Sebaik-baiknya, tempahan dan tugasan projek disejajarkan, supaya sumber mempunyai kapasiti terikat untuk melaksanakan tugasan tugas mereka. Walau bagaimanapun, realitinya ialah tempahan boleh berlaku berdasarkan ketersediaan dan masa tugas boleh berubah apabila projek meneruskan melalui kitaran hayatnya. Oleh itu, gandingan longgar membolehkan fleksibiliti.

Oleh sebab gandingan longgar penempahan projek dan tugasan tugas, tab **Penyelarasan** dimasukkan pada entiti Projek. Tab ini membantu pengurus projek menyelaraskan tempahan ahli pasukan dan tugasan mereka untuk pasukan projek mereka.

Bagi setiap ahli pasukan yang dinamakan, tab **Penyesuaian** menunjukkan penempahan dan tugasan sehingga kepada tugasan tugas individu. Ia menunjukkan jam dalam sel yang boleh mewakili tempoh dari bulan hingga ke hari.

Dalam medan **Skala masa**, anda boleh pilih **Bulan**, **Minggu** atau **hari.** Secara lalai, **Minggu** dipilih. Walau bagaimanapun, anda boleh mengubah nilai lalai tersebut dengan memilih butang **Tetapan**. Apabila tab **Penyesuaian** dibuka, ia menunjukkan tarikh semasa, tetapi anda boleh menggunakan kawalan kalendar untuk bergerak ke hadapan atau ke belakang dalam masa. Apabila projek mempunyai tarikh mula yang berada pada masa hadapan, tab menunjukkan tarikh tersebut apabila ia dibuka. Kawalan kalendar juga mempunyai pilihan yang membolehkan anda bergerak ke tarikh mula dan tamat projek.

Anda boleh menggunakan kawalan pengembang pada setiap sumber untuk menunjukkan butiran bagi penempahan sumber tersebut. Anda juga boleh mengembangkan tugasan setiap sumber ke peringkat tugas individu.

Bahagian bawah tab **Penyesuaian** menunjukkan keseluruhan jumlah bersih bagi projek, dan tab tersebut juga menyertakan jumlah lajur. Bagi setiap sumber, tab tersebut mengambil perbezaan antara penempahan ahli pasukan pada projek dan gulung atas tugasan tugas ahli pasukan tersebut. Secara idealnya, perbezaannya ialah 0 (sifar). Dengan kata lain, tidak ada perbezaan antara tempahan sumber dan tugasan tugasnya. Sebarang perbezaan ditunjukkan dengan warna dan pembayang untuk memanggil dua syarat:

- **Kekurangan tempahan** – Kekurangan tempahan berlaku apabila sumber mempunyai lebih banyak tugasan daripada tempahan. Disebabkan kapasiti ini belum ditempah, pengurus projek boleh membetulkan keadaan ini dengan melanjutkan tempahan sumber untuk menampung kekurangan tersebut.
- **Tempahan berlebihan** – Tempahan berlebihan berlaku apabila sumber telah ditempah kepada projek tetapi belum ditugaskan kepada tugas. Keadaan ini mungkin boleh diterima jika, sebagai contoh, sumber itu telah ditempah sebelum tugasan tugas berlaku. Walau bagaimanapun, dalam kes lain, sumber mungkin tidak dirancang untuk ditugaskan. Dalam kes ini, pengurus projek perlu mempertimbangkan untuk membatalkan penempahan sumber, supaya kapasiti boleh digunakan untuk projek lain.

> [!NOTE]
> Petunjuk bagi keadaan ini mungkin tersembunyi untuk meninggalkan lebih banyak ruang untuk grid. Dalam kes ini, anda boleh menjadikan petunjuk dapat dilihat dengan memilih butang **Tetapan**.

Dalam sesetengah kes, apabila medan **Skala masa** ditetapkan kepada peringkat yang lebih tinggi daripada **Hari**, perbezaan mungkin dikira sebagai 0 (sifar). Sebagai contoh, pada peringkat **Bulan**, perbezaan bersih bagi sumber mungkin 0 (sifar) untuk menunjukkan bahawa tempahan adalah sama dengan tugasan. Walau bagaimanapun, jika anda melihat pada peringkat **Minggu**, anda mungkin melihat bahawa terdapat tugasan 0 (sifar) jam dan penempahan 40 jam pada minggu pertama bulan ini serta tugasan 40 jam dan tempahan 0 (sifar) jam pada minggu kedua bulan tersebut. Walaupun jumlah tempahan dan tugasan untuk bulan tersebut adalah sama, ia berbeza mengikut minggu.

Apabila anda melihat tahap masa yang lebih tinggi, tab **Penyesuaian** menunjukkan penunjuk sel untuk memberitahu anda bahawa terdapat perbezaan pada tahap masa yang lebih rendah. Sebagai contoh, dalam ilustrasi berikut, penunjuk sel muncul dalam sel untuk bulan Oktober 2018 bagi sumber yang dinamakan Faziah Karim. Oleh itu, anda boleh melihat bahawa, walaupun tempahan sumber dan tugasan adalah sama apabila ia diagregat pada peringkat **Bulan**, ia tidak sepadan pada peringkat yang lebih rendah.

![Tempahan salah padan dan tugasan pada peringkat bulanan.](media/reconcile-assignments-01.JPG)

Klik dua kali sel untuk mengezum ke tahap bawah seterusnya dan lihat perbezaannya. Sebagai contoh, jika anda klik dua kali perbezaan pada Oktober 2018 bagi Faziah Karim, anda akan gerudi bawah peringkat **Minggu**. Anda kemudian boleh melihat bahawa sumber mempunyai tempahan 16 jam tetapi tiada tugasan dalam dua minggu pertama Oktober, dan 16 jam tugasan tetapi tiada tempahan pada minggu ketiga Oktober.

![Tempahan salah padan dan tugasan pada peringkat mingguan.](media/reconcile-assignments-02.JPG)

Anda boleh klik kanan sel untuk zum keluar peringkat lebih tinggi yang seterusnya. Anda juga boleh mematikan penunjuk sel dengan memilih butang **Tetapan**. 

Anda juga boleh menggunakan butang **Sebelumnya** dan **Seterusnya** di atas grid untuk bergerak melalui sebarang perbezaan dalam projek anda. Untuk menggunakan butang ini, anda mesti memilih sumber terlebih dahulu. Pilih **Seterusnya** untuk pergi ke perbezaan seterusnya antara tempahan dan tugasan bagi sumber tersebut. Pilih **Sebelumnya** untuk pergi ke perbezaan sebelumnya.

Dalam situasi apabila anda mempunyai tugasan tugas untuk sumber tetapi tiada tempahan, anda boleh memilih kekurangan tempahan dan kemudian pilih **Lanjutkan tempahan**. Anda kemudian boleh melihat tempahan yang diperlukan untuk menangani kekurangan sumber. Anda juga boleh melihat tempahan sumber pada projek semasa dan projek lain. Pilih **OK** untuk mencipta tempahan bagi sumber tanpa mengambil kira ketersediaan semasa. Pengurus Projek atau pengurus sumber kemudian boleh menggunakan Papan Jadual untuk menguruskan situasi apabila sumber telah menjadi terlebih tempah melebihi kapasiti kerana tempahannya telah dilanjutkan.

## <a name="managing-with-time-zones"></a>Mengurus dengan zon waktu
Untuk memastikan keputusan yang tepat dan boleh diramalkan apabila menggunakan Lanjutkan Tempahan, terdapat dua prasyarat utama yang mesti dipenuhi:  

- Pengguna mesti mengkonfigurasikan zon waktu peranti mereka supaya sepadan dengan zon waktu yang ditakrifkan dalam Tetapan Pemperibadian sistem anda.
 
  ![Tetapan zon waktu dalam Windows 10.](media/reconcile-assignments-03.png)

  ![Tetapan zon waktu dalam tetapan pemperibadian.](media/reconcile-assignments-04.png)
 
- Sumber Boleh Ditempah mesti mempunyai sekurang-kurangnya satu minit daripada masa kerja yang bertindih dengan kontur yang digunakan untuk mentakrifkan sambungan yang diminta. Sebagai contoh, contoh berikut menunjukkan sumber semakan dengan jam kerja yang berada di antara 9:00 PG dan 7:00 MLM. 

  ![Perbandingan kontur sumber.](media/reconcile-assignments-05.png)

Jadual berikut menunjukkan:

- Templat kalendar projek.
- Sumber A: Sumber ini mempunyai kalendar yang sama dan berada dalam zon waktu yang sama seperti projek. Masa mula tempahan ialah 9:00 PG.
- Sumber B: Sumber ini terletak pada zon waktu yang berbeza daripada projek dan oleh itu bermula pada 7:00 PG dalam zon waktu mereka. Walau bagaimanapun, tempahan akan bermula pada 9:00 PG kerana itu adalah masa mula paling awal kontur tugasan.
- Sumber C dan D: Sumber ini juga terletak pada zon waktu yang berbeza, kedua-duanya berbeza antara satu sama lain dan projek dan tempahan ia bermula tidak lebih awal daripada masa mula masing-masing yang tersedia.

|EntitI  |Kalendar  |
|-|-|
|Templat kalendar projek   | ![kalendar projek.](media/reconcile-assignments-06.png) |
|Sumber A  | ![Kalendar Sumber A.](media/reconcile-assignments-06.png) |
|Sumber B  |  ![Kalendar Sumber B.](media/reconcile-assignments-07.png) |
|Sumber C  |  ![Kalendar Sumber C.](media/reconcile-assignments-08.png) |
|Sumber D  | ![Kalendar Sumber D.](media/reconcile-assignments-09.png)  |
 
Apabila anda menavigasi ke pandangan penyesuaian, tugasan sumber dan kekurangan tempahan yang berkaitan akan dipaparkan.
 ![Pandangan penyelarasan sebelum lanjutan.](media/reconcile-assignments-10.png)

Selepas fungsi Lanjutkan Tempahan telah dilaksanakan pada setiap sumber, tempahan berjaya dilanjutkan bagi setiap sumber. Ini kerana setiap jam kerja sumber bertindih dengan kontur kekurangan.
 ![Pandangan penyelarasan selepas lanjutan tempahan.](media/reconcile-assignments-11.png) 

Walau bagaimanapun, pandangan yang lebih dekat pada butiran tempahan menunjukkan perbezaan dalam masa mula tempahan. Tempahan tidak akan bermula lebih awal daripada masa mula kontur tugasan dan tidak lebih awal daripada masa mula sumber yang tersedia.
 ![Tempahan baharu sumber dalam papan jadual.](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]