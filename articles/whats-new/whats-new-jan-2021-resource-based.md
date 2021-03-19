---
title: Perkara baharu Januari 2021 - Project Operations untuk senario berasaskan sumber/bukan stok
description: Topik ini memberikan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran Januari 2021 bagi Project Operations untuk senario berasaskan sumber/bukan stok.
author: sigitac
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e5bfd3c790dac51895cde04e08d1fa62f4457e8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5292080"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Perkara baharu Januari 2021 - Project Operations untuk senario berasaskan sumber/bukan stok

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_


Topik ini digunakan pada komponen dan versi Dynamics 365 Project Operations berikut:

  - Project Operations pada persekitaran Dataverse versi 4.6.0.154
  - Pengurusan projek dan perakaunan dalam persekitaran Dynamics 365 Finance versi 10.0.16

## <a name="quality-updates"></a>Kemas kini kualiti

### <a name="project-operations-on-dataverse"></a>Project Operations pada Dataverse

| **Bahagian Ciri** | **Nombor rujukan** | **Kemas kini kualiti** |
| --- | --- | --- |
| **Pelaksanaan dan konfigurasi** | 2106818 | Tetapkan nama semula sumber web yang menyebabkan isu yang berkaitan dengan menyesuaikan halaman. |
| **Pengebilan dan Penentuan Harga** | 2091908 | Tetapkan kebolehlihatan pilihan **Kunci penetapan harga** dan **Gunakan Penetapan Harga Semasa** pada halaman **Invois** apabila Project Operations dipasang bersama dengan Dynamics 365 Field Service. |
| **Pengebilan dan Penentuan Harga** | 2103058 | **Jumlah Projek** yang disegar semula untuk menangani nilai nol untuk kos sebenar pada tugas. |
| **Pengebilan dan Penentuan Harga** | 2116100 | Mesej ralat yang dipertingkatkan digunakan dengan kefungsian, **Masukan yang betul pada Nilai Sebenar**. |
| **Pengebilan dan Penentuan Harga** | 2116129 | Perbelanjaan yang dipertingkatkan menganggar kebolehlihatan pada tab **Anggaran** pada halaman **Projek**. |
| **Pengebilan dan Penentuan Harga** | 2119112 | Pengagregatan tetap jualan sebenar dan kos sebenar apabila kadar pertukaran yang berbeza digunakan. |
| **Pengebilan dan Penentuan Harga** | 2134705 | Tetapkan ralat, "Tidak boleh baca sifat **getResourceString** tak tertakrif" apabila halaman **Invois** dibuka dan Field Service dipasang. |
| **Pengurusan Peluang** | 2022195 | Grid pengebilan berasaskan tugas pada halaman **Projek** termasuk ikon yang menunjukkan bahawa terdapat kontrak atau baris sebut harga yang berkaitan dengan tugas tersebut. |
| **Pengurusan Peluang** | 2029135 | Tetapkan ralat proses perniagaan yang berlaku apabila pengguna cuba membuka baris invois pada invois yang disahkan yang mempunyai jumlah diinvois awal. |
| **Pengurusan Peluang** | 2040713 | Tetapkan ralat skrip yang berlaku apabila mencipta invois daripada kontrak dan Field Service dipasang. |
| **Perancangan dan Penjejakan Projek** | 2090202 | Peraturan perniagaan bertanda tidak lagi digunakan sebagai **Ditamatkan**. |
| **Masa dan Perbelanjaan** | 2091249 | Ketatkan kawalan supaya pengguna tidak boleh mengubah tugas pada entri masa yang telah diserahkan atau diluluskan. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Pengurusan projek dan perakaunan dalam Dynamics 365 Finance

| **Bahagian Ciri** | **Nombor rujukan** | **Kemas kini kualiti** |
| --- | --- | --- |
| **Pengurusan projek dan perakaunan** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Jumlah kontrak yang salah pada halaman **Pada akaun** untuk projek harga tetap dengan berbilang sumber penandaan. |
| **Pengurusan projek dan perakaunan** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | Ruang letak **Invoiceproposal.PSAnfRefProjId** tidak memaparkan ID Projek untuk aliran kerja, **Semak semula cadangan invois projek**. |
| **Pengurusan projek dan perakaunan** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | Tarikh diskaun tunai yang salah digunakan apabila menyiarkan cadangan invois projek. |
| **Pengurusan projek dan perakaunan** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | Mengalih keluar dan membaca tugasan sumber dalam Project Operations menggandakan entri ramalan projek dalam Kewangan. |
| **Pengurusan projek dan perakaunan** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | Dalam Project Operations, anda tidak boleh mencipta anggaran projek dalam Dataverse tanpa mempunyai baris kontrak pada projek. |
| **Pengurusan projek dan perakaunan** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | Dimensi kewangan bagi transaksi perbelanjaan projek tidak disegerakkan dengan baucar berkaitan dan pengedaran perakaunan bagi laporan perbelanjaan apabila kos disiarkan ke Baki. |
| **Pengurusan projek dan perakaunan** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | Penapis **Status invois** untuk transaksi projek yang disiarkan bagi projek harga tetap tidak berfungsi. |
| **Pengurusan projek dan perakaunan** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Penyingkiran anggaran pembalikan tidak berfungsi dalam bahagian **Berkala**. |
| **Pengurusan projek dan perakaunan** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | Baris cadangan invois boleh dipadam dalam Project Operations apabila diintegrasikan dengan Dataverse. |
| **Pengurusan projek dan perakaunan** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Menghalang pendayaan berbilang ciri baris kontrak tanpa integrasi Dataverse. |
| **Pengurusan projek dan perakaunan** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | Apabila penginvoisan pada akaun adalah bersamaan dengan keuntungan dan kerugian, hasil diinvois disenaraikan sebagai sifar pada halaman Anggaran. |
| **Pengurusan projek dan perakaunan** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | Pembetulan invois tidak berfungsi dalam persekitaran bersepadu. |
| **Pengurusan projek dan perakaunan** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Apabila menyiarkan WIP - nilai jualan dalam penginvoisan projek antara syarikat, akaun yang salah dipilih. |
| **Pengurusan projek dan perakaunan** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | Dalam Project Operations, kebergantungan pada tugas anggaran dalam Dataverse tidak boleh dikemas kini. |
| **Pengurusan projek dan perakaunan** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | Berulang kali memadamkan jurnal integrasi Project Operations dalam Kewangan membawa kepada kehilangan data. |
| **Pengurusan projek dan perakaunan** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | Ralat berikut berlaku semasa menyiarkan cadangan invois projek, "Transaksi tidak seimbang pada mata wang pelaporan apabila invois lanjutan yang ditolak ditambah". |
| **Pengurusan projek dan perakaunan** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | ID Projek yang salah dimasukkan pada potongan selepas kontrak projek lalai dikemas kini dalam Project Operations. |
| **Pengurusan projek dan perakaunan** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | Pengiktirafan anggaran dan hasil tidak boleh diselesaikan apabila Project Operations didayakan. |
| **Pengurusan projek dan perakaunan** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Dalam Project Operations, mengalih keluar projek daripada kontrak tidak menetapkan semula projek lalai pada kontrak. |
| **Pengurusan projek dan perakaunan** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | Dalam Project Operations, pada invois antara syarikat, baris perbelanjaan yang salah ditunjukkan dalam senarai **Tambah baris**. |
| **Perjalanan dan Perbelanjaan** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | Baris perbelanjaan tidak boleh disiarkan kerana persediaan jam hilang pada baris kontrak. |
| **Perjalanan dan Perbelanjaan** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | Apabila pengesahan projek/kategori adalah mandatori, kategori perbelanjaan yang berkaitan dengan projek tidak boleh dilihat dalam laporan perbelanjaan. |
| **Perjalanan dan Perbelanjaan** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Baki pendahuluan tunai tidak dikemas kini apabila laporan perbelanjaan disiarkan mengikut baris. |
| **Perjalanan dan Perbelanjaan** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | Kerja **Kemas kini maklumat pembayaran** gagal selepas membalikkan penyelesaian yang invois diselesaikan dengan dua atau lebih transaksi pembayaran. |
| **Perjalanan dan Perbelanjaan** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Terdapat isu dengan pengiraan pengurangan hidangan hari terakhir untuk kategori perbelanjaan setiap hari. |
| **Perjalanan dan Perbelanjaan** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | Laporan **Jenis perbelanjaan mengikut pekerja** tidak akan menunjukkan perbelanjaan terperinci jika sambungan pertama pengguna adalah dalam bahasa es-MX. |
| **Perjalanan dan Perbelanjaan** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | Pembayaran vendor untuk invois laporan perbelanjaan menggunakan akaun ringkasan yang salah bagi penyiaran penyelesaian. |
| **Perjalanan dan Perbelanjaan** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | Apabila laporan perbelanjaan yang disiarkan dengan **Membenarkan pengumpulan transaksi berdasarkan akaun pembayaran ofset** dan **Membetulkan Tarikh Perakaunan pada siaran** didayakan, tarikh perakaunan tidak dikumpulkan dalam jadual **Pengedaran perakaunan** yang memberi kesan kepada rekod cukai jualan. |
| **Perjalanan dan Perbelanjaan** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | Pemetaan subkategori perbelanjaan dialih keluar apabila kotak semak Gunakan dalam perbelanjaan telah dikosongkan dan kemudian pilih semula. |
| **Perjalanan dan Perbelanjaan** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | Laporan perbelanjaan antara syarikat tidak dapat dicipta jika ID Projek ditambah pada peringkat pengepala. |
| **Perjalanan dan Perbelanjaan** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Terdapat isu dengan pembayaran perbelanjaan apabila amaun perbelanjaan lebih daripada amaun pendahuluan tunai. |
| **Perjalanan dan Perbelanjaan** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | Medan **ID Projek** pada laporan perbelanjaan antara syarikat adalah kosong jika peranan pengguna ditugaskan kepada organisasi tertentu. |
| **Perjalanan dan Perbelanjaan** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Kategori perbelanjaan dikunci apabila menambah baris perbelanjaan baharu. |
| **Perjalanan dan Perbelanjaan** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Memperincikan baris laporan perbelanjaan yang telah terbahagi menghasilkan Akaun belum dibayar \baucar lejar Am yang belum lengkap. Disebabkan duplikasi **TRVEXPTRANS.SOURCEDOCUMENTLINE**, Peneroka Sumber Perakaunan juga rosak. |
| **Perjalanan dan Perbelanjaan** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | Indeks ditambah pada jadual **TRVREQUISITIONLINE** yang mana pelanggan mempunyai pendua, mengakibatkan ralat semasa naik taraf. |
| **Perjalanan dan Perbelanjaan** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | Dalam Project Operations, masa dengan tugas antara syarikat dalam Dataverse tidak boleh dicipta atau diluluskan. |

## <a name="regulatory-updates"></a>Kemas kini kawal selia

Untuk mendapatkan maklumat tentang kemas kini kawal selia untuk aplikasi Finance and Operations, lihat [Kemas kini kawal selia](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Anda juga boleh mendaftar masuk ke LCS dan melihat kemas kini kawal selia yang dirancang dengan menggunakan alat carian isu. Carian isu membolehkan anda membuat carian mengikut negara, jenis ciri dan keluaran.


[!INCLUDE[footer-include](../includes/footer-banner.md)]