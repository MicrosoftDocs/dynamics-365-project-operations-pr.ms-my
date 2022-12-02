---
title: Perkara baharu April 2022 - Project Operations untuk senario berdasarkan sumber/bukan stok
description: Artikel ini memberikan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran April 2022 bagi Microsoft Dynamics 365 Project Operations untuk senario berasaskan sumber/bukan stok.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 999006b2c2fe2b31d6e47910a3f1a55cab415f0e
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110895"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Perkara baharu April 2022 - Project Operations untuk senario berdasarkan sumber/bukan stok

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Artikel ini digunakan pada komponen dan versi Microsoft Dynamics 365 Project Operations berikut:

- Project Operations dalam persekitaran Dataverse versi 4.41.0.45
- Pengurusan projek dan perakaunan dalam persekitaran Dynamics 365 Finance versi 10.0.26

## <a name="features-included-in-this-release"></a>Ciri yang disertakan dalam keluaran ini

Kategori perolehan boleh digunakan dalam pesanan belian projek dan invois vendor yang belum selesai. Untuk maklumat lajut, lihat [Gunakan kategori perolehan dengan pesanan belian projek dan invois vendor yang belum selesai](../procurement/configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Kemas kini peta dwi tulis Project Operations

Jadual berikut menunjukkan peta dwi tulis yang telah diubah suai atau ditambahkan dalam keluaran Mac 2022 Project Operations.

| Peta entiti | Versi dikemas kini | Komen |
| -------------- | ------------------- | ------------|
| Entiti eksport baris invois vendor projek penyepaduan Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.4 | Peta ini menyokong penggunaan kategori perolehan dengan pesanan belian projek dan invois vendor yang belum selesai. |

Sentiasa menjalankan versi terkini peta dalam persekitaran anda, dan mendayakan semua peta jadual berkaitan ketika anda mengemas kini versi penyelesaian Project Operations Dataverse dan penyelesaian Kewangan anda. Sesetengah ciri dan keupayaan mungkin tidak berfungsi dengan betul jika versi terkini peta tidak diaktifkan. Anda boleh melihat versi aktif peta dalam lajur **Versi** pada halaman **Dwi tulis**. Untuk mengaktifkan versi baharu peta dengan, pilih **Versi peta jadual**, pilih versi terkini dan kemudian simpan versi yang dipilih. Jika anda sudah mempunyai peta jadual luar kotak tersuai, mohon semula perubahan. Untuk maklumat lanjut, lihat [Pengurusan kitaran hayat Aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika anda mengalami isu semasa anda memulakan peta, ikut arahan dalam bahagian [Isu lajur jadual yang hilang pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) bagi panduan penyelesaian masalah Dwi tulis.

## <a name="quality-updates"></a>Kemas kini kualiti

### <a name="project-operations-on-dataverse"></a>Project Operations pada Dataverse

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| ------------ | ---------------- | -------------- |
| Masa dan perbelanjaan | 2573900 | Ciri **Kelulusan Moden** mesti didayakan secara lalai. |
| Pengebilan dan harga | 2603313 | Memperbaiki ralat rekod duplikasi yang menghalang sebut harga dan baris kontrak yang mempunyai produk daripada ditambahkan. |
| Pelaksanaan dan konfigurasi | 2611368 | Pelanggan mesti dapat menambah sehingga lima entiti tersuai pada penyelesaian menggunakan pereka bentuk aplikasi moden. |
| Masa dan perbelanjaan | 2628285 | Memperbaiki isu yang menjejaskan keupayaan untuk menetapkan kategori sumber betul semasa import entri masa. |
| Pengurusan peluang| 2628815 | Kemas kini had aksara bagi perihalan butiran baris sebut harga untuk dipadankan dengan had aksara bagi subjek tugas, supaya import berjaya untuk tugas yang subjek lebih panjang daripada 100 aksara. |
| Masa dan perbelanjaan| 2629547 | Medan **Diserahkan Oleh** kelulusan projek mesti menunjukkan kepada pengguna yang menyerahkan rekod. |
| Masa dan perbelanjaan| 2629865 | Medan **Salin kategori** pada tugas apabila projek disalin. |
| Masa dan perbelanjaan| 2636463 | Memperbaiki penapis pada kelulusan dalam borang kelulusan moden. |
| Perancangan dan penjejakan projek | 2648300 | Memperbaiki isu yang menghalang pemilik projek daripada ditukar. |
| Pengebilan dan harga | 2563000 | Garisan jurnal untuk jualan belum dibilkan yang mata wang berbeza daripada mata wang kontrak tidak boleh dibenarkan. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Pengurusan projek dan perakaunan dalam Dynamics 365 Finance

Untuk maklumat tentang pembetulan pepijat yang termasuk dalam kemas kini ini, daftar masuk ke Microsoft Dynamics Lifecycle Services (LCS), dan lihat [artikel KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
