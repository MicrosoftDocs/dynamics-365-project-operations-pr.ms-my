---
title: Perkara baharu April 2022 - Project Operations untuk senario berdasarkan sumber/bukan stok
description: Topik ini memberikan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran April 2022 Microsoft Dynamics 365 Project Operations untuk senario berasaskan sumber/bukan stok.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc713e7a0dd6993e38ce3e3b2ba19f796a6f4773
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613355"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Perkara baharu April 2022 - Project Operations untuk senario berdasarkan sumber/bukan stok

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Topik ini terpakai kepada komponen dan versi Microsoft Dynamics 365 Project Operations berikut :

- Operasi Projek dalam versi persekitaran 4.41.0.45 Dataverse
- Pengurusan projek dan perakaunan dalam persekitaran Dynamics 365 Finance versi 10.0.26

## <a name="features-included-in-this-release"></a>Ciri yang disertakan dalam keluaran ini

Kategori perolehan boleh digunakan dalam pesanan pembelian projek dan invois vendor yang belum selesai. Untuk maklumat lanjut, lihat [Gunakan kategori perolehan dengan pesanan pembelian projek dan invois vendor yang belum selesai](configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Kemas kini peta dwi tulis Project Operations

Jadual berikut menunjukkan peta dwi-tulis yang telah diubah suai atau ditambah dalam keluaran Operasi Projek Mac 2022.

| Peta entiti | Versi dikemas kini | Komen |
| -------------- | ------------------- | ------------|
| Project Operations integrasi projek vendor invois talian export entity msdyn\_ projectvendorinvoicelines | 1.0.0.4 | Peta ini menyokong penggunaan kategori perolehan dengan pesanan pembelian dan invois vendor yang belum selesai. |

Sentiasa jalankan versi terkini peta dalam persekitaran anda dan dayakan semua peta jadual yang berkaitan semasa anda mengemas kini penyelesaian Operasi Dataverse Projek dan versi penyelesaian Kewangan anda. Sesetengah ciri dan keupayaan mungkin tidak berfungsi dengan betul jika versi terkini peta tidak diaktifkan. Anda boleh melihat versi aktif peta dalam lajur **Versi** pada halaman **Dwi tulis**. Untuk mengaktifkan versi baharu peta dengan, pilih **Versi peta jadual**, pilih versi terkini dan kemudian simpan versi yang dipilih. Jika anda telah menyesuaikan peta jadual di luar kotak, gunakan semula perubahan. Untuk maklumat lanjut, lihat [Pengurusan kitaran hayat Aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika anda menghadapi isu apabila anda memulakan peta, ikut arahan dalam [isu lajur jadual hilang pada bahagian peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) panduan penyelesaian masalah Dwi-tulis.

## <a name="quality-updates"></a>Kemas kini kualiti

### <a name="project-operations-on-dataverse"></a>Project Operations pada Dataverse

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| ------------ | ---------------- | -------------- |
| Masa dan perbelanjaan | 2573900 | Ciri **Kelulusan** Moden mesti didayakan secara lalai. |
| Pengebilan dan harga | 2603313 | Membaiki ralat rekod pendua yang menghalang sebut harga dan baris kontrak yang mempunyai produk daripada ditambah. |
| Penggunaan dan konfigurasi | 2611368 | Pelanggan mesti dapat menambah sehingga lima entiti tersuai kepada penyelesaian dengan menggunakan pereka bentuk aplikasi moden. |
| Masa dan perbelanjaan | 2628285 | Membaiki isu yang menjejaskan keupayaan untuk menetapkan kategori sumber yang betul semasa import kemasukan masa. |
| Pengurusan peluang| 2628815 | Kemas kini had aksara perihalan butiran baris petikan agar sepadan dengan had aksara subjek tugas, supaya import berjaya untuk tugas di mana subjek lebih panjang daripada 100 aksara. |
| Masa dan perbelanjaan| 2629547 | Medan **Dihantar Mengikut** kelulusan projek mesti menuding kepada pengguna yang menyerahkan rekod. |
| Masa dan perbelanjaan| 2629865 | Medan **Salin kategori** pada tugas apabila projek disalin. |
| Masa dan perbelanjaan| 2636463 | Menetapkan penapis pada kelulusan dalam borang kelulusan moden. |
| Perancangan dan penjejakan projek | 2648300 | Membaiki isu yang menghalang pemilik projek daripada diubah. |
| Pengebilan dan harga | 2563000 | Garis jurnal untuk jualan yang tidak dibilkan di mana mata wang berbeza daripada mata wang kontrak tidak boleh dibenarkan. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Pengurusan projek dan perakaunan di Dynamics 365 Finance

Untuk maklumat tentang pembetulan pepijat yang disertakan dalam kemas kini ini, log masuk ke Microsoft Dynamics Perkhidmatan Kitaran Hayat (LCS) dan lihat [artikel KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
