---
title: Ciri baharu Julai 2022 - Project Operations untuk senario berdasarkan sumber/tidak distok
description: Artikel ini memberikan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran Microsoft Dynamics 365 Project Operations Julai 2022 untuk senario berasaskan sumber/bukan stok.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: cbee9281d2fae485a3ebcd38bb884a2b2322f8d1
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183921"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Ciri baharu Julai 2022 - Project Operations untuk senario berdasarkan sumber/tidak distok

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Artikel ini terpakai kepada komponen dan versi Microsoft Dynamics 365 Project Operations berikut :

- Operasi Projek dalam versi persekitaran 4.44.0.22 Dataverse
- Pengurusan projek dan perakaunan dalam persekitaran Dynamics 365 Finance versi 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Kemas kini peta dwi tulis Project Operations

Tiada kemas kini untuk peta dwi tulis Project Operations dalam keluaran ini. Untuk senarai semasa dan versi peta dwi tulis Project Operations, lihat [Versi peta dwi tulis Project Operations](../environment/resource-dual-write-maps.md).

Sentiasa jalankan versi terkini peta dalam persekitaran anda dan dayakan semua peta jadual yang berkaitan semasa anda mengemas kini penyelesaian Operasi Dataverse Projek dan versi penyelesaian Kewangan anda. Sesetengah ciri dan keupayaan mungkin tidak berfungsi dengan betul jika versi terkini peta tidak diaktifkan. Anda boleh melihat versi aktif peta dalam lajur **Versi** pada halaman **Dwi tulis**. Untuk mengaktifkan versi baharu peta dengan, pilih **Versi peta jadual**, pilih versi terkini dan kemudian simpan versi yang dipilih. Jika anda telah menyesuaikan peta jadual di luar kotak, gunakan semula perubahan. Untuk maklumat lanjut, lihat [Pengurusan kitaran hayat Aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika anda menghadapi isu apabila anda memulakan peta, ikut arahan dalam [isu lajur jadual hilang pada bahagian peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) panduan penyelesaian masalah Dwi-tulis.

## <a name="quality-updates"></a>Kemas kini kualiti

### <a name="project-operations-on-dataverse"></a>Project Operations pada Dataverse

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Pelaksanaan dan Konfigurasi | 2761472 | Ralat pemasangan Project Operations dikendalikan. |
| Pengebilan dan Penentuan Harga | 2746940 | Nama baris subkontrak sepatutnya mempunyai panjang maksimum 100 aksara. |
| Pengebilan dan Penentuan Harga | 2739162 | Pelanggan mesti dapat melihat butang reben dalam paparan grid sebenar. |
| Perancangan dan Penjejakan Projek | 2730318 | Pengesahihan dikemaskini untuk aksara yang tidak disokong dalam subjek projek. |
| Pengebilan dan Penentuan Harga | 2705361 | Sebenar jualan yang dibilkan milestone mesti disertakan dalam medan penjejakan projek. |
| Pengebilan dan Penentuan Harga | 2675880 | Halang projek daripada dipautkan kepada garis kontrak yang tidak berasaskan kerja. |
| Pengebilan dan Penentuan Harga | 2664396 | Jika senarai harga sebut harga disimpan tanpa sebut harga, mesti ada ralat yang menyatakan bahawa sebut harga tidak boleh kosong. |
| Pengebilan dan Penentuan Harga | 2184019 | Tab **Pengebilan** Berasaskan Tugas tidak boleh ditunjukkan untuk projek yang tidak mempunyai kontrak sokongan atau sebut harga. |

### <a name="project-management-and-accounting-in-finance"></a>Pengurusan projek dan perakaunan dalam Kewangan

Untuk maklumat tentang pembetulan pepijat yang disertakan dalam kemas kini ini, log masuk ke Microsoft Dynamics Perkhidmatan Kitaran Hayat (LCS) dan lihat [artikel KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Ciri dihidupkan secara lalai dalam keluaran akan datang

Jadual berikut menyenaraikan ciri yang dihidupkan secara lalai dalam versi 10.0.29. Kebanyakan ciri yang telah dihidupkan secara automatik boleh dimatikan dalam [pengurusan Ciri](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Pada masa akan datang, sesetengah ciri yang telah dihidupkan secara automatik mungkin dialih keluar daripada pengurusan Ciri dan menjadi wajib. Perubahan ini memastikan bahawa pelanggan menggunakan fungsi semasa, supaya peningkatan dapat membina fungsi semasa semasa mereka ditambahkan. Ciri tidak akan didayakan secara automatik dalam masa kurang dari satu tahun, melainkan ia ditentukan untuk menjadi penting.

| Nama ciri | Benarkan tarikh | Ciri ditambah | Keadaan ciri | Modul |
| --- | --- | --- |--- |--- |
| Membolehkan pelarasan transaksi jam berdasarkan perubahan dalam peruntukan peraturan pembiayaan | 16 September 2022 | 7 Oktober 2020 | Hidupkan secara lalai | Pengurusan projek dan perakaunan |
| Ciri pembalikan invois prabayar pesanan pembelian projek | 16 September 2022 | 6 Oktober 2021 | Hidupkan secara lalai | Pengurusan projek dan perakaunan |
| Padamkan baris cadangan invois apabila menggunakan Operasi Projek untuk senario berasaskan sumber/ bukan stok | 16 September 2022 | 6 Oktober 2021 | Hidupkan secara lalai | Pengurusan projek dan perakaunan |
| Laraskan perakaunan pada transaksi projek yang disiarkan | 16 September 2022 | 10 Mei 2020 | Hidupkan secara lalai | Pengurusan projek dan perakaunan |
| Mendayakan persediaan perakaunan lalai untuk projek | 16 September 2022 | 19 Februari 2020 | Hidupkan secara lalai | Pengurusan projek dan perakaunan |
| Dayakan berbilang baris kontrak untuk projek | 16 September 2022 | 29 Jun 2020 | Hidupkan secara lalai | Pengurusan projek dan perakaunan |
| Jadikan jurnal Project Hour baca sahaja jika status kelulusan semasa tidak membenarkan pengeditan | 16 September 2022 | 6 Oktober 2021 | Hidupkan secara lalai | Pengurusan projek dan perakaunan |
| Dayakan baris jualan segerak dari baris pembelian apabila talian pembelian dikemas kini dan parameter pengurusan perubahan pesanan pembelian dihidupkan | 16 September 2022 | 7 Oktober 2020 | Hidupkan secara lalai | Pengurusan projek dan perakaunan |
| Mendayakan Operasi Projek pada Dynamics 365 Customer Engagement | 16 September 2022 | 29 Jun 2020 | Hidupkan secara lalai | Pengurusan projek dan perakaunan |
| Ciri pembetulan pembalikan transaksi projek | 16 September 2022 | 13 Julai 2020 | Hidupkan secara lalai | Pengurusan projek dan perakaunan |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Ciri-ciri yang menjadi wajib dalam keluaran yang akan datang

Jadual berikut menyenaraikan ciri yang wajib daripada versi 10.0.29 dan seterusnya.

| Nama ciri | Benarkan tarikh | Ciri ditambah | Keadaan ciri | Modul |
| --- | --- | --- | --- | --- |
| Kira nilai komited pada sumber pembiayaan tanpa membundarkan kadar pertukaran | 16 September 2022 | 14 Jun 2020 | Mandatori | Pengurusan projek dan perakaunan |
| Mendayakan pengeposan pelarasan projek dengan akaun lejar yang sama seperti transaksi asal | 16 September 2022 | 14 Jun 2020 | Mandatori | Pengurusan projek dan perakaunan |
| Kontrak projek komited jumlah terperinci | 16 September 2022 | 31 Ogos 2019 | Mandatori | Pengurusan projek dan perakaunan |
| Mendayakan pengisihan mengikut sumber semasa penciptaan cadangan invois projek | 16 September 2022 | 31 Ogos 2019 | Mandatori | Pengurusan projek dan perakaunan |
