---
title: Mengimport anggaran kepada baris kontrak berasaskan projek
description: Topik ini menyediakan maklumat tentang cara mengimport anggaran kewangan daripada projek kepada baris kontrak.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9ac367baba4529e86a42d812b7d9b2550812e297
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/20/2020
ms.locfileid: "4081461"
---
# <a name="importing-an-estimate-to-a-project-based-contract-line"></a>Mengimport anggaran kepada baris kontrak berasaskan projek

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Dalam Dynamics 365 Project Operations, anda boleh mengimport anggaran daripada projek kepada baris kontrak berasaskan projek.

1. Sahkan bahawa medan **Projek** pada baris kontrak berasaskan projek telah diisi.
2. Pada tab **Butiran Baris Kontrak** , pada subgrid, pilih **Import daripada Anggaran Projek**. Halaman dialog dengan pilihan perumusan terbuka. Pilihan perumusan yang tersedia ialah **Kelas Transaksi** , **Kategori** , **Peranan** , dan **Tugas Projek**.
3. Berdasarkan pemilihan rumusan, anggaran daripada projek untuk semua kelas transaksi dan tugas yang dirangkumkan pada baris kontrak ini akan disalin. Untuk melihat rangkuman kelas transaksi, pada tab **Umum** pada baris kontrak berasaskan projek, semak nilai dalam medan **Termasuk Masa** , **Termasuk Perbelanjaan** , dan **Termasuk Yuran**. 
4. Untuk melihat rangkuman tugas, pilih tab **Tugas Boleh Dicaj** pada baris kontrak. Berdasarkan tugas berkaitan yang mempunyai medan **Termasuk Kelas Transaksi** ditetapkan kepada **Ya** , semua anggaran untuk gabungan tugas dan kelas transaksi tersebut akan diimport kepada baris kontrak.

Apabila anda mengimport anggaran, sistem akan melalaikan penetapan harga berdasarkan senarai harga projek yang dilampirkan pada persediaan kontrak dan jenis pengebilan pada baris kontrak. Jika tugas, peranan atau kategori disediakan pada baris kontrak sebagai tidak boleh dicaj, baris anggaran yang diimport akan menjadi tidak boleh dicaj dan tidak akan ditambahkan pada nilai kontrak baris kontrak.

Apabila baris kontrak mempunyai butiran baris, medan **Nilai Kontrak** dan **Cukai Anggaran** pada baris kontrak dirumuskan dan tidak boleh diedit.

Apabila berbilang pilihan perumusan dipilih, sistem cuba merumuskan mengikut semua pilihan yang dipilih. Hasil output perumusan menghasilkan lebih banyak baris kontrak yang diimport berbanding dengan jika anda hanya memilih satu pilihan perumusan.

Contohnya, jika projek mempunyai baris anggaran berikut untuk perbelanjaan:

| Tugas | Kategori | Tarikh | Kuantiti | Harga unit | Amaun |
| --- | --- | --- | --- | --- | --- |
| Tugas A | Tambang penerbangan | 10/1/2020 | 4 | 400 | 1600 |
| Tugas B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Tugas C | Hotel | 11/1/2020 | 2 | 200 | 400 |

Apabila pengguna memilih untuk merumuskan mengikut **Kelas Transaksi** , maklumat berikut akan diimport:

| Tugas | Kategori | Tarikh | Kuantiti | Harga unit | Amaun |
| --- | --- | --- | --- | --- | --- |
| &nbsp; | &nbsp; | 10/1/2020 | 3.34 | 840 | 2800 |

Apabila pengguna memilih untuk merumuskan mengikut **Kelas Transaksi** dan **Kategori** , maklumat berikut akan diimport:

| Tugas | Kategori | Tarikh | Kuantiti | Harga unit | Amaun |
| --- | --- | --- | --- | --- | --- |
| Tugas A | Tambang penerbangan | 10/1/2020 | 4 | 400 | 1600 |
| &nbsp;| Hotel | 10/1/2020 | 6 | 200 | 1200 |

Apabila pengguna memilih untuk merumuskan mengikut **Kelas Transaksi** , **Kategori** , dan **Tugas Nod Daun** , yang berikut akan diimport. Ambil perhatian bahawa hasil ini ialah sama dengan hasil pada projek:

| Tugas | Kategori | Tarikh | Kuantiti | Harga unit | Amaun |
| --- | --- | --- | --- | --- | --- |
| Tugas A | Tambang penerbangan | 10/1/2020 | 4 | 400 | 1600 |
| Tugas B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Tugas C | Hotel | 11/1/2020 | 2 | 200 | 400 |