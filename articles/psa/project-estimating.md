---
title: Kos dan hasil projek
description: Topik ini memberikan maklumat tentang menganggarkan kos dan hasil projek.
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
ms.openlocfilehash: 282950c0ee21f430a2f20b21128830891c76c84a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127979"
---
# <a name="project-costs-and-revenue"></a>Kos dan hasil projek

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Anggaran projek memberikan pandangan kewangan untuk kerja yang dianggarkan dan dijadualkan dalam jadual projek. Tab **Anggaran** pada halaman **Projek** menunjukkan kesan kos dan hasil bagi kerja yang anda rancang. Ia juga menyediakan maklumat tentang banyak dimensi pratakrif. 

> ![Tab anggaran](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>Nilai kos dan jualan projek

Senarai harga menentukan kadar kos dan bil untuk peranan dalam projek. Anda boleh menentukan kesan kos dan hasil kerja, berdasarkan peranan yang berkaitan dengan nama kedudukan dan sumber yang dinamakan yang ditugaskan kepada tugas. Jika terdapat tugas yang tidak mempunyai sebarang tugasan (generik atau dinamakan), anda tidak boleh mendapatkan anggaran kos atau jualan. Nilai kos dan jualan pertimbangkan tarikh yang ditakrifkan dalam senarai harga.

### <a name="default-cost-price"></a>Harga kos lalai  

Setiap projek milik organisasi. Organisasi ini ditunjukkan dalam medan **Unit Kontrak** dalam projek. Senarai harga yang dikaitkan dengan unit kontrak ini digunakan untuk menentukan harga kos unit. Untuk menentukan harga kos yang betul pada peranan bagi tarikh yang ditakrifkan pada baris anggaran, cari gabungan peranan, unit dan unit organisasi dalam senarai harga kos. 

Supaya harga kos ia boleh dikira, semua tugas mesti ditugaskan kepada sumber. Sebarang tugas yang tidak ditugaskan akan mempunyai harga kos 0.00.

Jika gabungan peranan, unit dan unit organisasi tidak memulangkan harga kos dari senarai harga unit kontrak, sistem mengabaikan unit tersebut. Sebaliknya, ia mencari gabungan peranan dan unit organisasi sahaja. Jika harga kos ditemui, faktor penukaran digunakan untuk menukarnya kepada unit yang anda pilih pada baris anggaran.

Jika gabungan peranan dan unit organisasi tidak mengembalikan harga kos, sistem mengabaikan unit organisasi tersebut. Sebaliknya, ia mencari gabungan peranan dan unit untuk menetapkan harga lalai (selepas sebarang penukaran digunakan).

Jika sistem tidak menemui harga untuk peranan, harga kos pada baris anggaran ditetapkan kepada nilai lalai **0.00**. Semua jumlah kos pada baris anggaran kos projek direkodkan dalam mata wang unit kontrak.

> [!NOTE]
> Secara lalai, Microsoft Dynamics 365 menyimpan jumlah kos dalam mata wang asas anda. Walau bagaimanapun, jumlah kos yang ditunjukkan pada tab **Anggaran** adalah dalam mata wang unit kontrak.  

### <a name="default-sales-price"></a>Harga jualan lalai 

Senarai harga jualan ditentukan sama ada oleh entiti jualan yang projek tersebut dilampirkan atau pelanggan projek. Apabila entiti jualan, seperti peluang, kutipan atau kontrak, dikaitkan dengan projek itu, harga jualan entiti jualan ditentukan oleh senarai harga yang dikaitkan dengan sebut harga atau kontrak. Jika sebut harga atau kontrak mempunyai senarai harga tersuai, senarai harga itu digunakan sebagai senarai harga lalai untuk anggaran projek. Jika tiada perkaitan dengan entiti jualan, senarai harga jualan lalai daripada parameter digunakan sebagai senarai harga jualan lalai projek yang dipadankan dengan mata wang pelanggan yang ditakrifkan pada projek.

Setiap baris anggaran mempunyai unit sumber yang dikaitkan dengannya. Unit sumber menunjukkan unit organisasi yang sumber ditempah darinya untuk menyelesaikan tugas. Untuk menentukan harga jualan bagi peranan yang berkaitan, cari gabungan peranan, unit dan unit sumber dalam senarai harga jualan. Jika tiada tugasan pada tugas, harga jualan bagi tugas ialah 0.00.

Jika gabungan peranan, unit dan unit sumber tidak memulangkan harga jualan dari senarai harga jualan, sistem ini mengabaikan unit tersebut. Sebaliknya, ia mencari gabungan peranan dan unit sumber sahaja. Jika harga kos ditemui, faktor penukaran digunakan untuk menukarnya kepada unit yang anda pilih pada baris anggaran jualan. 

Jika gabungan peranan dan unit sumber tidak memulangkan harga jualan dari senarai harga jualan, sistem ini mengabaikan unit sumber tersebut. Sebaliknya, ia mencari gabungan peranan dan unit untuk menetapkan harga lalai (selepas sebarang penukaran digunakan).

Jika sistem tidak menemui harga untuk peranan, harga jualan pada baris anggaran ditetapkan kepada nilai lalai **0.00**.

Tab **Anggaran** mempunyai pandangan grid yang menunjukkan baris anggaran. Grid termasuk lajur untuk unit, jumlah harga kos dan jumlah harga jualan seperti yang ditunjukkan dalam ilustrasi berikut. 

> ![Pandangan grid pada tab Anggaran](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>Pandangan anggaran projek berfasa masa

Pandangan berfasa masa bagi anggaran projek menunjukkan data anggaran daripada paparan grid merentasi garis masa, dalam skala masa yang anda pilih. Secara lalai, data anggaran dipangsikan pada dimensi **Peranan**.

> ![Pandangan berfasa masa untuk anggaran projek](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>Peruntukkan usaha anggaran berdasarkan pada mod tugas

Dalam pandangan berfasa masa, anda mengedarkan jumlah usaha yang dianggarkan untuk tugas dengan memperuntukkan jam usaha bagi setiap tempoh masa unit dalam skala masa yang dipilih. Mod tugas menentukan cara usaha diperuntukkan merentasi tempoh tugas. Dua jenis peruntukan ialah peruntukan **Sekata** dan **Berasaskan jam kerja**.

### <a name="work-hours-based-allocation"></a>Peruntukan berasaskan jam kerja
 
Dalam mod tugas penjadualan automatik, jam lalai harian untuk sumber tugas ditetapkan pada kadar jam kerja penuh. Tingkah laku ini digunakan apabila usaha diperuntukkan dengan memisahkannya merentasi tempoh tugas dalam berfasa masa. Contohnya, jika anda anggarkan yang tugas akan diselesaikan oleh satu sumber dalam skala masa **Hari**, usaha yang diperuntukkan bagi setiap hari tidak akan melebihi jam kerja bagi setiap hari yang ditakrifkan dalam kalendar projek. Oleh itu, peruntukan usaha sentiasa memastikan bahawa sumber dianggarkan untuk digunakan bagi sepanjang hari.

### <a name="even-allocation"></a>Peruntukan sama rata

Dalam mod tugas yang dijadualkan secara manual, masa kerja dari kalendar projek tidak digunakan. Sebaliknya, jadual tugas adalah berdasarkan input pengguna. Untuk tugas ini, peruntukan usaha bagi setiap tempoh masa unit dalam skala masa yang dipilih tidak mempunyai sebarang faktor pengehadan. Jumlah usaha pada tugas dipisahkan dengan sama rata dan diperuntukkan untuk setiap tempoh masa unit dalam skala masa yang dipilih. Oleh itu, mod tugas yang ditakrifkan pada tugas menentukan pengagihan usaha, atau peruntukan usaha bagi setiap tempoh masa unit dalam anggaran yang berfasa masa.

## <a name="grouping-and-time-phasing-options"></a>Pengumpulan dan pilihan pemfasaan masa

Pandangan berfasa masa menunjukkan pengagihan usaha, kos dan anggaran jualan secara harian, mingguan, bulanan atau tahunan. Secara lalai, data anggaran dipangsikan pada dimensi **Peranan**. Walau bagaimanapun, anda boleh menggunakan pilihan **Kumpulan Mengikut** untuk membuat pangsi pada dua dimensi lain: **Kategori** dan **Sumber**.

Dalam pandangan grid dan pandangan berfasa masa, anda boleh memilih medan yang ditunjukkan. Jumlah untuk setiap blok masa ditunjukkan di bahagian bawah projek. Mereka menunjukkan jumlah anggaran usaha, kos dan jualan untuk hari, minggu, bulan atau tahun. Harga kos lalai dan harga jualan adalah berkesan tarikh. Dalam erti kata lain, ia berubah bagi setiap sumber, berdasarkan pandangan berfasa masa yang anda pilih.

## <a name="expense-estimates"></a>Anggaran perbelanjaan

Butang **Tambah Anggaran Perbelanjaan Baharu** dalam paparan grid membolehkan anda merekodkan sebarang perbelanjaan yang ditanggung dalam projek itu, tetapi itu tidak berkaitan secara langsung dengan buruh. Anda boleh merekodkan anggaran perbelanjaan untuk tugas tertentu atau untuk keseluruhan projek. Pilih kategori perbelanjaan dan tarikh tentatif apabila anda menjangka untuk menanggung perbelanjaan tersebut. Jika senarai harga kos dan senarai harga jualan yang berkaitan mempunyai harga lalai (atau jika peratusan tokokan ditakrifkan untuk kategori perbelanjaan), ia akan dimasukkan secara automatik pada baris anggaran apabila perkaitan berlaku.
