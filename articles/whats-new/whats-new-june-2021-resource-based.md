---
title: Ciri baharu Jun 2021 - Project Operations untuk senario berdasarkan sumber/tidak distok
description: Artikel ini memberikan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran Operasi Projek Jun 2021 untuk senario berasaskan sumber /tidak berstok.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fd745107fa6d50882ebea302d3d2ae0de21b79ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028257"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Ciri baharu Jun 2021 - Project Operations untuk senario berdasarkan sumber/tidak distok

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Artikel ini terpakai kepada komponen dan versi berikut Dynamics 365 Project Operations:

- Project Operations dalam persekitaran Dynamics 365 Dataverse versi 4.11.0.156 atau 4.11.0.164.
- Pengurusan projek dan perakaunan dalam persekitaran aplikasi kewangan dan operasi versi 10.0.19.

## <a name="features-included-in-this-release"></a>Ciri yang disertakan dalam keluaran ini

Ciri berikut disertakan dalam keluaran ini:

- Keupayaan untuk memadamkan [Baris cadangan invois projek untuk senario pelarasan](../invoicing/correct-project-invoice-proposals.md).
- Baris perbelanjaan terbutir menunjukkan nama subkategori dalam laporan perbelanjaan [Laporan Perbelanjaan Digambarkan Semula-Ciri Baharu](../expense/expense-reports-reimagined.md#new-features).
- Kaedah pembayaran tersedia dalam anak tetingkap perbelanjaan baharu apabila mencipta perbelanjaan baharu.
- Ketersediaan umum API jadual Projek. Kefungsian baharu ini membolehkan pelanggan untuk melakukan, mencipta, mengemas kini dan memadamkan operasi secara berprogram pada tugas projek, tugasan sumber, kebergantungan tugas dan rekod ahli pasukan projek. Untuk mendapatkan maklumat lanjut, lihat [Gunakan API jadual Projek untuk melakukan operasi dengan entiti Penjadualan](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Kemas kini peta dwi tulis Project Operations

Tiada kemas kini untuk peta dwi tulis Project Operations dalam keluaran ini. 

Untuk senarai semasa dan versi peta dwi tulis Project Operations, lihat [Versi peta dwi tulis Project Operations](../environment/resource-dual-write-maps.md).

Sentiasa jalankan versi terkini peta dalam persekitaran anda dan dayakan semua peta jadual yang berkaitan semasa anda mengemas kini penyelesaian Operasi Dataverse Projek anda dan versi penyelesaian aplikasi kewangan dan operasi. Ciri dan keupayaan tertentu mungkin tidak berfungsi dengan betul jika versi terkini peta tidak diaktifkan. Anda boleh melihat versi aktif peta pada halaman **dwi tulis** dalam lajur **Versi**. Aktifkan versi baharu peta dengan memilih **Versi peta jadual**, memilih versi terkini dan kemudian menyimpan versi yang dipilih. Jika anda mempunyai peta jadual luar kotak tersuai, mohon semula perubahan. Untuk maklumat lanjut, lihat [Pengurusan kitaran hayat Aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika anda menghadapi isu memulakan peta, ikuti arahan dalam bahagian [Isu lajur jadual yang tidak ditemui pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) bagi Panduan penyelesaian masalah dwi tulis

## <a name="quality-updates"></a>Kemas kini kualiti

### <a name="project-operations-on-dataverse"></a>Project Operations pada Dataverse

| **Bahagian ciri** | **Nombor rujukan** | **Kemas kini kualiti** |
| --- | --- | --- |
| Pengebilan dan Penentuan Harga | 2281417 | Telah menetapkan isu berkenaan kegagalan tindakan penciptaan invois automatik melalui jadual invois. |
| Pengebilan dan Penentuan Harga | 2287835 | Prestasi pengesahan invois yang ditambah baik. |
| Pengurusan Peluang | 2222555 | Kebolehtuntutan anggaran bahan mestilah disalin dengan betul kepada butiran baris sebut harga apabila menggunakan **Import daripada Anggaran Projek**. |
| Pengurusan Peluang | 2223427 | Penyesuaian kini dibenarkan untuk tindakan, **GenerateRetainersFromRetainerScheduleOptions**. |
| Pengurusan Peluang | 2277528 | Pengiraan nilai pencapaian pengebilan tetap untuk baris kontrak projek dengan berbilang pelanggan. |
| Perancangan dan Penjejakan Projek | 2226110 | Telah menetapkan isu berkala dengan fungsi **Jana Keperluan** dalam grid **Pasukan projek**. |
| Perancangan dan Penjejakan Projek | 2208109 | Pengguna tidak boleh mencipta projek dalam satu mata wang dengan tugas yang berkaitan dalam mata wang lain. |
| Perancangan dan Penjejakan Projek | 2258228 | Senarai medan yang dibenarkan untuk mengubah suai dengan entiti **Penjadualan** menggunakan API Jadual telah dikemas kini. |
| Perancangan dan Penjejakan Projek | 2293989 | Tetapan bahasa dan serantau yang betul mestilah dihantar ke grid **Tugas Projek**. |
| Pengurusan Sumber | 2220493 | Telah menetapkan pengalaman pengguna dalam grid **Tugas** apabila menandakan dengan cepat permintaan sumber sebagai selesai. |
| Pengurusan Sumber | 2330496 | Telah menetapkan isu pemuatan **Papan Jadual**. (Kemas kini kualiti tersedia dalam versi 4.11.0.164) |
| Masa dan Perbelanjaan | 2194431 | Grid **Entri masa** mesti menghormati permulaan minggu seperti yang ditetapkan dalam **Tetapan sistem**. |
| Masa dan Perbelanjaan | 2277311 | Selepas anda memadamkan nilai dalam sel dalam grid **Entri masa**, kursor kekal dalam grid. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Pengurusan projek dan perakaunan pada Dynamics 365 Finance

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Pengurusan projek dan perakaunan | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Nota borang** dan **Persediaan borang** tidak boleh dilihat di bawah **Persediaan pengurusan projek** dalam entiti sah Finance yang berintegrasi dengan Project Operations. |
| Pengurusan projek dan perakaunan | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | Perihalan lalai untuk VAT kosong apabila **Jenis penyiaran** = **Cukai jualan** untuk baucar invois projek. |
| Pengurusan projek dan perakaunan | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Transaksi berganda disiarkan apabila pengebilan berdasarkan tugas digunakan dalam Dataverse dengan integrasi Project Operations. |
| Pengurusan projek dan perakaunan | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Peratusan selesai dalam pengecaman hasil tidak betul ketika menggunakan integrasi Project Operations. |
| Pengurusan projek dan perakaunan | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | Akruan hasil berganda dalam invois vendor belum selesai dalam senario berintegrasi Project Operations. |
| Pengurusan projek dan perakaunan | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Tidak dapat menyiarkan jurnal integrasi apabila peraturan profil hasil ditetapkan kepada persediaan **Kumpulan**. |
| Pengurusan projek dan perakaunan | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | Invois pembelian tidak boleh disiarkan untuk pesanan pembelian projek yang mempunyai baris dengan berbilang unit ukuran. |
| Pengurusan projek dan perakaunan | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | Dimensi kewangan lalai dalam projek tidak boleh dikemas kini menggunakan entiti data projek **V2**. |
| Pengurusan projek dan perakaunan | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | Proses kelompok untuk mencipta anggaran projek mengambil masa yang terlalu lama untuk selesai. |
| Pengurusan projek dan perakaunan | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Pemadaman kontrak juga memadamkan alamat berkaitan dengan pelanggan. |
| Perjalanan dan perbelanjaan | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | Syarat aliran kerja kelulusan laporan perbelanjaan tidak dinilai dengan betul. |
| Perjalanan dan perbelanjaan | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | Dasar laporan perbelanjaan tidak menilai dengan betul ID projek. |
| Perjalanan dan perbelanjaan | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | Tindakan, **Pisah kepada peribadi untuk transaksi perbelanjaan antara syarikat** tidak berfungsi dengan betul. |
| Perjalanan dan perbelanjaan | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Justifikasi baris laporan perbelanjaan dipadamkan secara tidak sengaja apabila permintaan perjalanan tertentu dipadamkan. Ini berlaku apabila recID laporan perbelanjaan dan permintaan perjalanan adalah sama. |
| Perjalanan dan perbelanjaan | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Terdapat isu dalam aplikasi mudah alih Perbelanjaan apabila medan **ID Projek** diperlukan dalam dasar laporan perbelanjaan. |
| Perjalanan dan perbelanjaan | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Perbelanjaan antara syarikat yang berkaitan dengan projek tidak boleh diedit. Sebaliknya, mesej ralat berikut memaparkan, "Rujukan objek rujukan tidak ditetapkan kepada tika objek." |
| Perjalanan dan perbelanjaan | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Selepas laporan perbelanjaan disiarkan, mata wang dan amaun yang salah disenaraikan dalam sublejar bank. |
| Perjalanan dan perbelanjaan | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Penambahbaikan telah dibuat kepada ciri, *Padam transaksi kad kredit*.  |
| Perjalanan dan perbelanjaan | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | Cukai jualan yang disertakan dalam laporan perbelanjaan tidak dikira secara konsisten apabila mata wang pelaporan yang berbeza ditentukan dalam entiti sah. |
| Perjalanan dan perbelanjaan | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | Prestasi terjejas apabila menambahkan perbelanjaan perjalanan tunai baharu. |
| Perjalanan dan perbelanjaan | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Peraturan dasar perbelanjaan tidak dicetuskan pada laporan perbelanjaan. |
| Perjalanan dan perbelanjaan | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Memuat naik kategori dikongsi baharu dengan menggunakan Rangka Kerja Pengurusan Data akan mengalih keluar semua subkategori untuk semua kategori dikongsi. |
| Perjalanan dan perbelanjaan | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Apabila anda mencipta baris perbelanjaan dan kemudian memilih kategori, mesej ralat berikut memaparkan, "Gabungan Kumpulan cukai jualan DOM dan Kumpulan cukai jualan item STD tidak sah." |
| Perjalanan dan perbelanjaan | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Terdapat isu penyegerakan dalam aplikasi mudah alih Perbelanjaan. |
