---
title: Mengimport anggaran untuk projek kepada baris sebut harga berasaskan projek
description: Topik ini menyediakan maklumat tentang cara mengimport anggaran daripada projek kepada baris sebut harga.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 224c2265cfcc38dfc2ed74664d38c095feefaca7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081130"
---
# <a name="importing-estimates-for-a-project-to-a-project-based-quote-line"></a>Mengimport anggaran untuk projek kepada baris sebut harga berasaskan projek

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Jika projek dicipta semasa peringkat prajualan, anda boleh memilih untuk mengimport anggaran kewangan daripada projek kepada baris sebut harga berasaskan projek.

1. Pastikan baris sebut harga berasaskan projek mempunyai maklumat projek dalam medan **Project**.
2. Pada tab **Butiran baris sebut harga** , pilih **Import daripada Anggaran Project**.
3. Pada halaman dialog yang dibuka, pilih salah satu pilihan peringkasan berikut.

  - **Kelas transaksi**
  - **Kategori**
  - **Peranan** 
  - **Tugas projek**

Berdasarkan pemilihan anda, anggaran daripada projek untuk semua kelas urus niaga termasuk pada baris sebut harga ini disalin. Untuk menyemak jenis kelas urus niaga yang disertakan, pilih tab **Umum** pada baris sebut harga berasaskan projek dan semak nilai untuk **Termasuk Masa** , **Termasuk Perbelanjaan** dan **Termasuk Yuran**.  Untuk menyemak rangkuman tugas, pilih tab **Tugas Boleh Dicaj** pada baris sebut harga.

Bergantung pada Tugas yang dikaitkan dan Rangkuman kelas transaksi, anggaran untuk gabungan tugas dan kelas transaksi tersebut diimport kepada baris sebut harga.

Apabila anda mengimport anggaran, sistem akan melalaikan penetapan harga berdasarkan senarai harga projek yang dilampirkan pada sebut harga dan jenis pengebilan yang ditetapkan pada baris sebut harga berasaskan projek. Jika tugas, peranan atau kategori disediakan pada baris sebut harga berasaskan projek sebagai tidak boleh dicaj, baris anggaran yang diimport akan ditetapkan sebagai tidak boleh dicaj dan tidak akan ditambahkan pada nilai baris sebut harga yang diberikan sebut harga.

Apabila baris sebut harga mempunyai butiran baris, medan **Nilai Sebut Harga** dan **Anggaran Cukai** pada baris sebut harga diringkaskan dan tidak boleh diedit.

Apabila berbilang pilihan perumusan dipilih, sistem akan cuba merumuskan mengikut semua pilihan yang dipilih. Hasilnya adalah bahawa output baris sebut harga yang diimport akan menjadi lebih banyak berbanding dengan jika anda memilih hanya satu pilihan perumusan.

Contohnya, jika projek mempunyai baris anggaran berikut untuk perbelanjaan.

| Tugas | Kategori | Tarikh | Kuantiti | Harga unit | Amaun |
| --- | --- | --- | --- | --- | --- |
| Tugas A | Tambang penerbangan | 10/1/2020 | 4 | 400 | 1600 |
| Tugas B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Tugas C | Hotel | 11/1/2020 | 2 | 200 | 400 |

Apabila pengguna memilih untuk meringkaskan dengan kelas Urus Niaga, maklumat berikut akan diimport.

| Tugas | Kategori | Tarikh | Kuantiti | Harga unit | Amaun |
| --- | --- | --- | --- | --- | --- |
|||10/1/2020 | 3.34 | 840 | 2800 |

Apabila pengguna memilih untuk meringkaskan dengan kelas Urus Niaga dan Kategori, maklumat berikut akan diimport.

| Tugas | Kategori | Tarikh | Kuantiti | Harga unit | Amaun |
| --- | --- | --- | --- | --- | --- |
| Tugas A | Tambang penerbangan | 10/1/2020 | 4 | 400 | 1600 |
| | Hotel | 10/1/2020 | 6 | 200 | 1200 |

Apabila pengguna memilih untuk merumuskan mengikut Kelas Transaksi, Kategori dan Tugas Nod Daun, maklumat berikut akan diimport. Perhatikan bahawa keputusan ini adalah sama seperti apa yang ada pada projek.

| Tugas | Kategori | Tarikh | Kuantiti | Harga unit | Amaun |
| --- | --- | --- | --- | --- | --- |
| Tugas A | Tambang penerbangan | 10/1/2020 | 4 | 400 | 1600 |
| Tugas B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Tugas C | Hotel | 11/1/2020 | 2 | 200 | 400 |