---
title: Ciri baharu Julai 2022 - Project Operations untuk senario berdasarkan sumber/tidak distok
description: Artikel ini menyediakan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran Julai 2022 Microsoft Dynamics 365 Project Operations untuk senario berasaskan sumber/bukan stok.
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

Artikel ini digunakan pada komponen dan versi Microsoft Dynamics 365 Project Operations berikut :

- Operasi Projek dalam Dataverse versi persekitaran 4.44.0.22
- Pengurusan projek dan perakaunan dalam persekitaran Dynamics 365 Finance versi 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Kemas kini peta dwi tulis Project Operations

Tiada kemas kini untuk peta dwi tulis Project Operations dalam keluaran ini. Untuk senarai semasa dan versi peta dwi tulis Project Operations, lihat [Versi peta dwi tulis Project Operations](../environment/resource-dual-write-maps.md).

Sentiasa jalankan versi terkini peta dalam persekitaran anda dan dayakan semua peta jadual yang berkaitan semasa anda mengemas kini penyelesaian Operasi Dataverse Projek dan versi penyelesaian Kewangan anda. Sesetengah ciri dan keupayaan mungkin tidak berfungsi dengan betul jika versi terkini peta tidak diaktifkan. Anda boleh melihat versi aktif peta dalam lajur **Versi** pada halaman **Dwi tulis**. Untuk mengaktifkan versi baharu peta dengan, pilih **Versi peta jadual**, pilih versi terkini dan kemudian simpan versi yang dipilih. Jika anda telah menyesuaikan peta jadual luar kotak, gunakan semula perubahan. Untuk maklumat lanjut, lihat [Pengurusan kitaran hayat Aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika anda menghadapi isu apabila anda memulakan peta, ikuti arahan dalam [seksyen Isu lajur jadual hilang pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) pada panduan Penyelesaian Masalah dwi-tulis.

## <a name="quality-updates"></a>Kemas kini kualiti

### <a name="project-operations-on-dataverse"></a>Project Operations pada Dataverse

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Pelaksanaan dan Konfigurasi | 2761472 | Ralat pemasangan Operasi Projek dikendalikan. |
| Pengebilan dan Penentuan Harga | 2746940 | Nama garis subkontrak harus mempunyai panjang maksimum 100 aksara. |
| Pengebilan dan Penentuan Harga | 2739162 | Pelanggan mesti dapat melihat butang reben dalam pandangan grid sebenar. |
| Perancangan dan Penjejakan Projek | 2730318 | Pengesahihan yang dikemas kini untuk aksara yang tidak disokong dalam subjek projek. |
| Pengebilan dan Penentuan Harga | 2705361 | Sebenar jualan yang dibilkan tonggak mesti dimasukkan dalam bidang penjejakan projek. |
| Pengebilan dan Penentuan Harga | 2675880 | Halang projek daripada dipautkan ke talian kontrak yang tidak berasaskan kerja. |
| Pengebilan dan Penentuan Harga | 2664396 | Jika senarai harga sebut harga disimpan tanpa sebut harga, mesti ada ralat yang menyatakan bahawa sebut harga tidak boleh kosong. |
| Pengebilan dan Penentuan Harga | 2184019 | Tab **Pengebilan** Berasaskan Tugas tidak boleh ditunjukkan untuk projek yang tidak mempunyai kontrak sokongan atau sebut harga. |
| Masa dan Perbelanjaan | 2754459 | Apabila aliran awan penjadualan berulang tidak aktif, tunjukkan sepanduk dan memintas pemprosesan async. |
| Pengebilan dan Penentuan Harga | 2724391 | Pengecualian yang salah dilemparkan apabila peraturan pengebilan pecahan kontrak projek hilang nilai pelanggan. |
| Pengebilan dan Penentuan Harga | 2708638 | Rekod tidak ditemui semasa mencari menggunakan carian grid dalam Penggunaan Bahan dan Kelulusan untuk Penggunaan Bahan.|
| Pengebilan dan Penentuan Harga | 2686977 | Halang pengesahihan untuk baris invois semasa penciptaan invois. |
| Pengebilan dan Penentuan Harga | 2683032 | Penyalinan peranan dan kategori yang dikenakan tidak melebihi 5000 rekod.|
| Pengebilan dan Penentuan Harga | 2673363 | Kos Penggunaan % ke atas Projek rosak apabila kedua-dua anggaran Usaha dan Perbelanjaan dan sebenarnya wujud untuk projek. |

### <a name="project-management-and-accounting-in-finance"></a>Pengurusan projek dan perakaunan dalam Kewangan

Untuk maklumat tentang pembetulan pepijat yang disertakan dalam kemas kini ini, log masuk ke Microsoft Dynamics Perkhidmatan Kitaran Hayat (LCS) dan lihat [artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438) KB.

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Ciri dihidupkan secara lalai dalam keluaran akan datang

Jadual berikut menyenaraikan ciri yang dihidupkan secara lalai dalam versi 10.0.29. Kebanyakan ciri yang telah dihidupkan secara automatik boleh dimatikan dalam [Pengurusan](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) ciri. Pada masa akan datang, sesetengah ciri yang telah dihidupkan secara automatik mungkin dialih keluar daripada pengurusan Ciri dan menjadi mandatori. Perubahan ini memastikan pelanggan menggunakan fungsi semasa, supaya peningkatan dapat membina fungsi semasa semasa ditambahkan. Ciri-ciri tidak akan didayakan secara automatik dalam masa kurang dari satu tahun, melainkan ia ditentukan sebagai penting.

| Nama ciri | Dayakan tarikh | Ciri ditambah | Keadaan ciri | Modul |
| --- | --- | --- |--- |--- |
| Membolehkan pelarasan transaksi jam berdasarkan perubahan dalam peruntukan peraturan pembiayaan | 16 September 2022 | 7 Oktober 2020 | Dihidupkan secara lalai | Pengurusan projek dan perakaunan |
| Ciri pembalikan invois prabayar pesanan pembelian projek | 16 September 2022 | 6 Oktober 2021 | Dihidupkan secara lalai | Pengurusan projek dan perakaunan |
| Padamkan baris cadangan invois apabila menggunakan Operasi Projek untuk senario berasaskan sumber / tidak stok | 16 September 2022 | 6 Oktober 2021 | Dihidupkan secara lalai | Pengurusan projek dan perakaunan |
| Laraskan perakaunan pada transaksi projek yang disiarkan | 16 September 2022 | 10 Mei 2020 | Dihidupkan secara lalai | Pengurusan projek dan perakaunan |
| Dayakan persediaan perakaunan lalai untuk projek | 16 September 2022 | 19 Februari 2020 | Dihidupkan secara lalai | Pengurusan projek dan perakaunan |
| Dayakan berbilang baris kontrak untuk projek | 16 September 2022 | 29 Jun 2020 | Dihidupkan secara lalai | Pengurusan projek dan perakaunan |
| Jadikan jurnal Project Hour baca sahaja jika status kelulusan semasa tidak membenarkan pengeditan | 16 September 2022 | 6 Oktober 2021 | Dihidupkan secara lalai | Pengurusan projek dan perakaunan |
| Dayakan talian jualan penyegerakan daripada talian pembelian apabila talian pembelian dikemas kini dan parameter pengurusan perubahan pesanan beli dihidupkan | 16 September 2022 | 7 Oktober 2020 | Dihidupkan secara lalai | Pengurusan projek dan perakaunan |
| Dayakan Operasi Projek pada Dynamics 365 Customer Engagement | 16 September 2022 | 29 Jun 2020 | Dihidupkan secara lalai | Pengurusan projek dan perakaunan |
| Ciri pembetulan pembalikan transaksi projek | 16 September 2022 | 13 Julai 2020 | Dihidupkan secara lalai | Pengurusan projek dan perakaunan |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Ciri-ciri yang menjadi wajib dalam keluaran yang akan datang

Jadual berikut menyenaraikan ciri yang wajib daripada versi 10.0.29 dan seterusnya.

| Nama ciri | Dayakan tarikh | Ciri ditambah | Keadaan ciri | Modul |
| --- | --- | --- | --- | --- |
| Hitung nilai komited pada sumber pembiayaan tanpa membundarkan kadar pertukaran | 16 September 2022 | 14 Jun 2020 | Mandatori | Pengurusan projek dan perakaunan |
| Dayakan pengeposan pelarasan projek dengan akaun lejar yang sama seperti transaksi asal | 16 September 2022 | 14 Jun 2020 | Mandatori | Pengurusan projek dan perakaunan |
| Kontrak projek komited perincian jumlah | 16 September 2022 | 31 Ogos 2019 | Mandatori | Pengurusan projek dan perakaunan |
| Mendayakan pengisihan mengikut sumber semasa penciptaan cadangan invois projek | 16 September 2022 | 31 Ogos 2019 | Mandatori | Pengurusan projek dan perakaunan |
