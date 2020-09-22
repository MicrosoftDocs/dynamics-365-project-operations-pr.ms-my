---
title: Tentukan kos projek dan anggaran hasil
description: Cara untuk menentukan kos projek dan anggaran hasil dalam Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: cfa3c0c6-a57d-4d50-90dd-9a517d380257
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2fd581cdb84a3a1c0dbbd1b9b27d87ddd959f883
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753871"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Tentukan kos projek dan anggaran hasil 

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Anggaran projek memberikan pandangan kewangan untuk kerja anggaran dan dijadualkan dalam struktur pecahan kerja projek. Pandangan anggaran memberitahu anda kesan kos dan hasil kerja yang dirancang. Pandangan anggaran menyediakan alat untuk melihat maklumat pada beberapa dimensi yang ditakrif lebih awal untuk memaklumkan anda kesan kewangan projek sebaiknya.  
  
## <a name="cost-and-sales-value-of-the-project"></a>Kos dan nilai jualan projek  
Senrai harga [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] mentakrifkan kadar kos dan bil untuk kegunaan projek peranan. Berdasarkan peranan yang dikaitkan dengan tugas dalam struktur pecahan kerja projek, anda boleh menentukan kesan kos dan hasil kerja yang terlibat.  
  
## <a name="cost-price-defaulting"></a>Penetapan nilai lalai harga kos  
Setiap projek dimiliki oleh organisasi (ditunjukkan dalam **Unit Pemilikan** dalam projek). Senarai harga yang berkaitan dengan unit organisasi pemilikan menentukan harga kos unit. [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] menentukan harga kos untuk peranan dengan mencari gabungan peranan, unit dan unit organisasi dalam senarai harga kos untuk mendapatkan harga kos yang betul untuk tarikh berkuat kuasa pada garisan anggaran.  
  
Jika gabungan peranan, unit dan unit organisasi tidak menghasilkan harga kos daripada senarai harga unit pemilikan, unit tidak diambil kira dalam gabungan peranan dan unit organisasi. Jika terdapat harga kos, harga ini ditukar kepada unit yang anda pilih pada garisan anggaran.  
  
Jika gabungan peranan dan unit organisasi tidak menghasilkan harga kos, unit organisasi tidak diambil kira dalam gabungan peranan dan unit serta harga ditetapkan kepada nilai lalai selepas menggunakan sebarang pertukaran, jika perlu.  
  
 Jika tiada harga untuk peranan, maka harga kos menjadi lalai kepada 0.00 pada garisan anggaran.  
  
 Semua amaun kos pada garisan anggaran kos projek berada dalam mata wang unit organisasi pemilikan.  
  
## <a name="sales-price-defaulting"></a>Penetapan nilai lalai harga jualan  
Senarai harga jualan adalah berdasarkan entiti jualan yang dilampirkan pada projek. Senarai harga jualan yang berkaitan dengan sebut harga atau kontrak menentukan harga jualan unit. Jika sebut harga atau kontrak mempunyai senarai harga tersuai, ini akan menjadi senarai harga jualan lalai untuk anggaran projek. Jika tiada kaitan dengan entiti jualan, maka senarai harga jualan lalai yang dikonfigurasikan dalam tetapan parameter akan menjadi senarai harga jualan lalai bagi projek tersebut. Setiap garisan anggaran mempunyai unit organisasi sumber yang berkaitan untuk menunjukkan unit organisasi bagi sumber yang akan ditempah untuk melengkapkan tugas. Harga jualan untuk peranan berkaitan ditentukan dengan mencari gabungan peranan, unit dan unit organisasi sumber dalam senarai harga jualan untuk mendapatkan harga jualan yang betul untuk tarikh berkuat kuasa pada garisan anggaran.  
  
Jika gabungan peranan, unit dan unit organisasi sumber tidak menghasilkan harga jualan daripada senarai harga jualan, sistem akan mengabaikan unit dan mencari gabungan peranan dan unit organisasi sumber. Jika harga jualan ditemui, ini akan ditukar kepada unit yang anda pilih pada garisan anggaran jualan.  
  
Jika sistem tidak menemui harga untuk peranan, maka harga jualan mesti menjadi lalai kepada 0.00 pada garisan anggaran.  
  
Pandangan anggaran mempunyai pandangan grid y ang memaparkan grid rata garisan anggaran dengan unit dan jumlah kos serta harga jualan.  
  
## <a name="time-phased-view-of-project-estimates"></a>Pandangan anggaran projek berfasa masa  
Dalam pandangan berfasa masa untuk anggaran projek, data anggaran daripada pandangan grid dipangsi secara lalai mengikut peranan dan menunjukkan penyebaran data anggaran merentasi garis masa dalam skala masa yang dipilih.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>Peruntukan anggaran usaha berdasarkan mod tugas  
Dalam pandangan berfasa masa, jumlah anggaran usaha untuk tugas diagihkan dengan memperuntukkan beberapa jam usaha tertentu per tempoh masa unit skala masa yang dipilih. Dalam Project Service, mod tugas menentukan bagaimana usaha diperuntukkan merentasi tempoh tugas. Dua jenis peruntukan ialah peruntukan sekata dan jam kerja berdasarkan peruntukan  
  
## <a name="work-hours-based-allocation"></a>Jam kerja berdasarkan peruntukan  
Penjadualan auto mod tugas bagi tugas mengawal peruntukan tersebut untuk bilangan sumber yang dianggarkan dalam tugas, ia dianggarkan akan digunakan untuk jam kerja penuh setiap hari. Ini digunakan apabila memperuntukkan usaha dengan memisahkannya merentasi tempoh tugas juga dalam pandangan berfasa masa. Contohnya, pada skala masa 'Hari', untuk tugas yang dianggarkan akan dilengkapkan oleh satu sumber, usaha yang diperuntukkan setiap hari tidak akan melebihi jam kerja setiap hari yang ditakrifkan dalam kalendar projek. Oleh itu, peruntukan usaha sentiasa memastikan bahawa sumber dianggarkan akan digunakan untuk sepanjang hari.  
  
## <a name="even-distribution"></a>Pengagihan sekata  
Mod tugas yang dijadualkan secara manual tidak menghormati jam kerja, kalendar projek atau bilangan sumber yang ditakrifkan dalam tugas. Jadual tugas adalah berdasarkan input pengguna. Untuk tugas sedemikian, peruntukan usaha setiap tempoh masa unit skala masa yang dipilih tidak mempunyai sebarang faktor pengehadan. Jumlah usaha dalam tugas dipisahkan dengan sama rata dan diperuntukkan untuk setiap tempoh masa unit pada skala masa yang dipilih.  
  
Dengan cara ini, mod tugas yang ditakrifkan dalam tugas menentukan pengagihan usaha atau peruntukan usaha setiap tempoh masa unit dalam anggaran berfasa masa.  
  
## <a name="grouping-and-time-phasing-options"></a>Pengumpulan dan pilihan pemfasaan masa  
Pandangan ini membantu anda memahami pengagihan usaha, kos dan anggaran jualan berasaskan setiap hari, minggu, bulan atau tahun. Pilihan Himpun Mengikut membenarkan pemangsian data anggaran pada dua dimensi lain: kategori dan sumber. Pada kedua-dua pandangan grid dan pandangan berfasa masa, anda boleh memilih medan untuk dipaparkan. Jumlah untuk setiap blok masa dipaparkan di bahagian bawah yang menunjukkan jumlah usaha, kos dan jualan yang dianggarkan untuk hari, minggu, bulan atau tahun.  
  
Penetapan nilai lalai harga kos dan jualan adalah tarikh berkuat kuasa—apabila kadar untuk peranan berubah, ia akan menjadi lebih telus dalam pandangan berfasa masa ketika memaparkan data anggaran yang dipangsikan pada 'Sumber' dan berfasa masa mengikut minggu.  
  
## <a name="expense-estimates"></a>Anggaran perbelanjaan  
Sebarang perbelanjaan yang akan dikenakan dalam projek yang tidak berkaitan secara terus dengan buruh untuk dibelanjakan boleh direkodkan dalam anggaran projek dalam pandangan grid. Anda boleh melaksanakan ini menggunakan pilihan **Tambah anggaran perbelanjaan** dalam pandangan grid. Anggaran perbelanjaan boleh direkodkan untuk tugas khusus atau untuk keseluruhan projek; anda boleh memilih kategori perbelanjaan pada garisan ini dan memilih tarikh tentatif perbelanjaan dijangka akan ditanggung. Jika senarai harga kos dan jualan yang berkaitan mempunyai harga lalai atau peratusan tokokan yang ditakrifkan untuk kategori perbelanjaan, ia akan ditetapkan kepada nilai lalai pada garisan anggaran dalam perkaitan.  
  
### <a name="see-also"></a>Lihat Juga  
 [Panduan Pengurus Projek](../project-service/project-manager-guide.md)
