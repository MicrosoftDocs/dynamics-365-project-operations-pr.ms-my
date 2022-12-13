---
title: Import anggaran daripada projek kepada baris kontrak projek
description: Artikel ini menyediakan maklumat tentang cara mengimport anggaran kewangan daripada projek kepada baris kontrak.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 73ae0ccbb5372c9dfbc28ac154094c89add0913d
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824686"
---
# <a name="import-estimates-from-a-project-to-a-project-contract-line"></a>Import anggaran daripada projek kepada baris kontrak projek

_**Digunakan untuk:** Penggunaan Lite - berurusan dengan invois proforma, Operasi Projek untuk senario_ berasaskan sumber/bukan stok_

Dalam Dynamics 365 Project Operations, anda boleh mengimport anggaran daripada projek kepada baris kontrak berasaskan projek.

1. Sahkan bahawa medan **Projek** pada baris kontrak berasaskan projek telah diisi.
2. Pada tab **Butiran Baris Kontrak**, pada subgrid, pilih **Import daripada Anggaran Projek**. Halaman dialog dengan pilihan perumusan terbuka. Pilihan perumusan yang tersedia ialah **Kelas Transaksi**, **Kategori**, **Peranan**, dan **Tugas Projek**.
3. Berdasarkan pemilihan rumusan, anggaran daripada projek untuk semua kelas transaksi dan tugas yang dirangkumkan pada baris kontrak ini akan disalin. Untuk melihat rangkuman kelas transaksi, pada tab **Umum** pada baris kontrak berasaskan projek, semak nilai dalam medan **Termasuk Masa**, **Termasuk Perbelanjaan**, dan **Termasuk Yuran**. 
4. Untuk melihat rangkuman tugas, pilih tab **Tugas Boleh Dicaj** pada baris kontrak. Berdasarkan tugas berkaitan yang mempunyai medan **Termasuk Kelas Transaksi** ditetapkan kepada **Ya**, semua anggaran untuk gabungan tugas dan kelas transaksi tersebut akan diimport kepada baris kontrak.

Apabila anda mengimport anggaran, sistem akan melalaikan penetapan harga berdasarkan senarai harga projek yang dilampirkan pada persediaan kontrak dan jenis pengebilan pada baris kontrak. Jika tugas, peranan atau kategori disediakan pada baris kontrak sebagai tidak boleh dicaj, baris anggaran yang diimport akan menjadi tidak boleh dicaj dan tidak akan ditambahkan pada nilai kontrak baris kontrak.

Apabila baris kontrak mempunyai butiran baris, medan **Nilai Kontrak** dan **Cukai Anggaran** pada baris kontrak dirumuskan dan tidak boleh diedit.

Apabila berbilang pilihan perumusan dipilih, sistem cuba merumuskan mengikut semua pilihan yang dipilih. Hasil output perumusan menghasilkan lebih banyak baris kontrak yang diimport berbanding dengan jika anda hanya memilih satu pilihan perumusan.

Contohnya, jika projek mempunyai baris anggaran berikut untuk perbelanjaan:

| Tugas | Kategori | Tarikh | Kuantiti | Harga unit | Amaun |
| --- | --- | --- | --- | --- | --- |
| Tugas A | Tambang penerbangan | 10/1/2020 | 4 | 400 | 1600 |
| Tugas B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Tugas C | Hotel | 11/1/2020 | 2 | 200 | 400 |

Apabila pengguna memilih untuk merumuskan mengikut **Kelas Transaksi**, maklumat berikut akan diimport:

| Tugas | Kategori | Tarikh | Kuantiti | Harga unit | Amaun |
| --- | --- | --- | --- | --- | --- |
| &nbsp; | &nbsp; | 10/1/2020 | 3.34 | 840 | 2800 |

Apabila pengguna memilih untuk merumuskan mengikut **Kelas Transaksi** dan **Kategori**, maklumat berikut akan diimport:

| Tugas | Kategori | Tarikh | Kuantiti | Harga unit | Amaun |
| --- | --- | --- | --- | --- | --- |
| Tugas A | Tambang penerbangan | 10/1/2020 | 4 | 400 | 1600 |
| &nbsp;| Hotel | 10/1/2020 | 6 | 200 | 1200 |

Apabila pengguna memilih untuk merumuskan mengikut **Kelas Transaksi**, **Kategori**, dan **Tugas Nod Daun**, yang berikut akan diimport. Ambil perhatian bahawa hasil ini ialah sama dengan hasil pada projek:

| Tugas | Kategori | Tarikh | Kuantiti | Harga unit | Amaun |
| --- | --- | --- | --- | --- | --- |
| Tugas A | Tambang penerbangan | 10/1/2020 | 4 | 400 | 1600 |
| Tugas B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Tugas C | Hotel | 11/1/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
