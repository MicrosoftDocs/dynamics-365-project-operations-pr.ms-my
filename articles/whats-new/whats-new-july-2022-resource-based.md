---
title: Ciri baharu Julai 2022 - Project Operations untuk senario berdasarkan sumber/tidak distok
description: Artikel ini memberikan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran Julai 2022 bagi Microsoft Dynamics 365 Project Operations untuk senario berasaskan sumber/bukan stok.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: e63b29741dbaa400a2176ff8b4c35c6d64dfeab4
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403963"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Ciri baharu Julai 2022 - Project Operations untuk senario berdasarkan sumber/tidak distok

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Artikel ini digunakan pada komponen dan versi Microsoft Dynamics 365 Project Operations berikut:

- Project Operations dalam persekitaran Dataverse versi 4.44.0.22
- Pengurusan projek dan perakaunan dalam persekitaran Dynamics 365 Finance versi 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Kemas kini peta dwi tulis Project Operations

Tiada kemas kini untuk peta dwi tulis Project Operations dalam keluaran ini. Untuk senarai semasa dan versi peta dwi tulis Project Operations, lihat [Versi peta dwi tulis Project Operations](../environment/resource-dual-write-maps.md).

Sentiasa menjalankan versi terkini peta dalam persekitaran anda, dan mendayakan semua peta jadual berkaitan ketika anda mengemas kini versi penyelesaian Project Operations Dataverse dan penyelesaian Kewangan anda. Sesetengah ciri dan keupayaan mungkin tidak berfungsi dengan betul jika versi terkini peta tidak diaktifkan. Anda boleh melihat versi aktif peta dalam lajur **Versi** pada halaman **Dwi tulis**. Untuk mengaktifkan versi baharu peta dengan, pilih **Versi peta jadual**, pilih versi terkini dan kemudian simpan versi yang dipilih. Jika anda sudah mempunyai peta jadual luar kotak tersuai, mohon semula perubahan. Untuk maklumat lanjut, lihat [Pengurusan kitaran hayat Aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika anda mengalami isu semasa anda memulakan peta, ikut arahan dalam bahagian [Isu lajur jadual yang hilang pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) bagi panduan penyelesaian masalah Dwi tulis.

## <a name="quality-updates"></a>Kemas kini kualiti

### <a name="project-operations-on-dataverse"></a>Project Operations pada Dataverse

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Pelaksanaan dan Konfigurasi | 2761472 | Ralat pemasangan Project Operations akan dikendalikan. |
| Pengebilan dan Penentuan Harga | 2746940 | Nama baris subkontrak mesti mempunyai panjang maksimum sebanyak 100 aksara. |
| Pengebilan dan Penentuan Harga | 2739162 | Pelanggan mesti dapat melihat butang Reben dalam pandangan grid aktual. |
| Perancangan dan Penjejakan Projek | 2730318 | Pengesahan yang dikemas kini untuk aksara yang tidak disokong dalam subjek projek. |
| Pengebilan dan Penentuan Harga | 2705361 | Aktual jualan dibilkan pencapaian mesti termasuk dalam medan penjejakan projek. |
| Pengebilan dan Penentuan Harga | 2675880 | Mencegah projek daripada dikaitkan dengan baris kontrak yang tidak berasaskan kerja. |
| Pengebilan dan Penentuan Harga | 2664396 | Jika senarai sebut harga disimpan tanpa sebut harga, mesti ada ralat yang menyatakan bahawa sebut harga tersebut tidak boleh kosong. |
| Pengebilan dan Penentuan Harga | 2184019 | Tab **Pengebilan berasaskan tugas** tidak boleh ditunjukkan untuk projek yang tidak mempunyai kontrak atau sebut harga sandaran. |
| Masa dan Perbelanjaan | 2754459 | Apabila aliran awan penjadualan berulang tidak aktif, tunjukkan pemprosesan tak segerak sepanduk dan pintasan. |
| Pengebilan dan Penentuan Harga | 2724391 | Pengecualian salah telah dibuang apabila peraturan pengebilan pecahan kontrak projek tiada nilai pelanggan. |
| Pengebilan dan Penentuan Harga | 2708638 | Rekod tidak ditemui ketika mencari menggunakan grid carian dalam Penggunaan Bahan dan Kelulusan untuk Penggunaan Bahan.|
| Pengebilan dan Penentuan Harga | 2686977 | Elakkan pengesahan untuk baris invois semasa penciptaan invois. |
| Pengebilan dan Penentuan Harga | 2683032 | Penyalinan peranan dan kategori boleh dikenakan caj tidak mempunyai skala melebihi 5000 rekod.|
| Pengebilan dan Penentuan Harga | 2673363 | Penggunaan Kos % pada Projek rosak apabila kedua-dua Usaha dan anggaran Perbelanjaan dan aktual wujud untuk projek. |

### <a name="project-management-and-accounting-in-finance"></a>Pengurusan projek dan perakaunan dalam Kewangan

Untuk maklumat tentang pembetulan pepijat yang termasuk dalam kemas kini ini, daftar masuk ke Microsoft Dynamics Lifecycle Services (LCS), dan lihat [artikel KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Ciri dihidupkan secara lalai dalam keluaran yang akan datang

Jadual berikut menyenaraikan ciri yang dihidupkan secara lalai dalam versi 10.0.29. Kebanyakan ciri yang dihidupkan secara automatik boleh dimatikan dalam [Pengurusan ciri](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Pada masa hadapan, sesetengah ciri yang dihidupkan secara automatik mungkin akan dialih keluar daripada pengurusan Ciri dan menjadi mandatori. Perubahan ini memastikan bahawa pelanggan menggunakan kefungsian semasa, supaya peningkatan boleh dibina pada kefungsian semasa apabila ditambahkan. Ciri tidak akan didayakan secara automatik dalam masa kurang dari satu tahun, melainkan ciri tersebut dianggap penting.

| Nama ciri | Dayakan tarikh | Ciri ditambahkan | Keadaan ciri | Modul |
| --- | --- | --- |--- |--- |
| Dayakan pelarasan urus niaga jam berdasarkan perubahan dalam peruntukan peraturan pembiayaan | 16 September 2022 | 7 Oktober 2020 | Dihidupkan secara lalai | Pengurusan projek dan perakaunan |
| Ciri pembalikan invois prabayaran pesanan belian projek | 16 September 2022 | 6 Oktober 2021 | Dihidupkan secara lalai | Pengurusan projek dan perakaunan |
| Padamkan baris cadangan invois semasa menggunakan Project Operations untuk senario berasaskan sumber/bukan stok | 16 September 2022 | 6 Oktober 2021 | Dihidupkan secara lalai | Pengurusan projek dan perakaunan |
| Laraskan perakaunan pada urus niaga projek yang telah disiarkan | 16 September 2022 | 10 Mei 2020 | Dihidupkan secara lalai | Pengurusan projek dan perakaunan |
| Dayakan persediaan perakaunan lalai untuk projek | 16 September 2022 | 19 Februari 2020 | Dihidupkan secara lalai | Pengurusan projek dan perakaunan |
| Dayakan berbilang baris kontrak untuk projek | 16 September 2022 | 29 Jun 2020 | Dihidupkan secara lalai | Pengurusan projek dan perakaunan |
| Jadikan jurnal Jam Projek baca sahaja jika status kelulusan semasa tidak membenarkan pengeditan | 16 September 2022 | 6 Oktober 2021 | Dihidupkan secara lalai | Pengurusan projek dan perakaunan |
| Dayakan baris jualan penyegerakan daripada baris pembelian apabila baris pembelian dikemas kini dan parameter pembelian pengurusan perubahan pesanan belian dihidupkan | 16 September 2022 | 7 Oktober 2020 | Dihidupkan secara lalai | Pengurusan projek dan perakaunan |
| Dayakan Project Operations pada Dynamics 365 Customer Engagement | 16 September 2022 | 29 Jun 2020 | Dihidupkan secara lalai | Pengurusan projek dan perakaunan |
| Ciri pembetulan pembalikan urus niaga projek | 16 September 2022 | 13 Julai 2020 | Dihidupkan secara lalai | Pengurusan projek dan perakaunan |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Ciri yang menjadi mandatori dalam keluaran yang akan datang

Jadual berikut menyenaraikan ciri yang mandatori daripada versi 10.0.29 ke atas.

| Nama ciri | Dayakan tarikh | Ciri ditambahkan | Keadaan ciri | Modul |
| --- | --- | --- | --- | --- |
| Kira nilai komited pada sumber pembiayaan tanpa dibundarkan kadar pertukaran | 16 September 2022 | 14 Jun 2020 | Mandatori | Pengurusan projek dan perakaunan |
| Dayakan penyiaran pelarasan projek dengan akaun lejar yang sama seperti urus niaga asal | 16 September 2022 | 14 Jun 2020 | Mandatori | Pengurusan projek dan perakaunan |
| Butiran jumlah komited kontrak projek | 16 September 2022 | 31 Ogos 2019 | Mandatori | Pengurusan projek dan perakaunan |
| Dayakan pengisihan mengikut penciptaan cadangan invois projek | 16 September 2022 | 31 Ogos 2019 | Mandatori | Pengurusan projek dan perakaunan |
