---
title: Import anggaran untuk projek pada baris sebut harga berasaskan projek
description: Topik ini menyediakan maklumat tentang cara mengimport anggaran daripada projek kepada baris sebut harga.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b32ac22188922a56fa13ea67e0ead77b9b045d9f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278339"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Import anggaran untuk projek pada baris sebut harga berasaskan projek

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_


Jika projek dicipta semasa peringkat prajualan, anda boleh memilih untuk mengimport anggaran kewangan daripada projek kepada baris sebut harga berasaskan projek.

1. Pastikan baris sebut harga berasaskan projek mempunyai maklumat projek dalam medan **Project**.
2. Pada tab **Butiran baris sebut harga**, pilih **Import daripada Anggaran Project**.
3. Pada halaman dialog yang terbuka, pilih salah satu pilihan perumusan berikut:

  - **Kelas transaksi**
  - **Kategori**
  - **Peranan** 
  - **Tugas projek**

Berdasarkan pemilihan anda, anggaran daripada projek untuk semua kelas urus niaga termasuk pada baris sebut harga ini disalin. Untuk menyemak jenis kelas urus niaga yang disertakan, pilih tab **Umum** pada baris sebut harga berasaskan projek dan semak nilai untuk **Termasuk Masa**, **Termasuk Perbelanjaan** dan **Termasuk Yuran**.

Apabila anda mengimport anggaran, sistem akan melalaikan penetapan harga berdasarkan senarai harga projek yang dilampirkan pada sebut harga dan jenis pengebilan yang disediakan pada baris sebut harga berasaskan projek. Jika peranan atau kategori ditetapkan pada baris sebut harga berasaskan projek sebagai tidak boleh dikenakan, baris anggaran yang diimport akan ditetapkan sebagai tidak boleh dikenakan cukai dan tidak akan menambah pada nilai baris sebut harga yang disebut harga.

Apabila baris sebut harga mempunyai butiran baris, medan **Nilai Sebut Harga** dan **Anggaran Cukai** pada baris sebut harga diringkaskan dan tidak boleh diedit.

Apabila berbilang pilihan perumusan dipilih, sistem akan cuba merumuskan mengikut semua pilihan yang dipilih. Hasilnya adalah bahawa output baris sebut harga yang diimport akan menjadi lebih banyak berbanding dengan jika anda memilih hanya satu pilihan perumusan.

Contohnya, sama ada projek mempunyai baris anggaran berikut untuk perbelanjaan.

| Tugas | Kategori | Tarikh | Kuantiti | Harga unit | Amaun |
| --- | --- | --- | --- | --- | --- |
| Tugas A | Tambang penerbangan | 10/1/2020 | 4 | 400 | 1600 |
| Tugas B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Tugas C | Hotel | 11/1/2020 | 2 | 200 | 400 |

Apabila pengguna memilih untuk meringkaskan dengan kelas Urus Niaga, maklumat berikut akan diimport.

| Tugas | Kategori | Tarikh | Kuantiti | Harga unit | Amaun |
| --- | --- | --- | --- | --- | --- |
| | | 10/1/2020 | 3.34 | 840 | 2800 |

Apabila pengguna memilih untuk meringkaskan dengan kelas Urus Niaga dan Kategori, maklumat berikut akan diimport.

| Tugas | Kategori | Tarikh | Kuantiti | Harga unit | Amaun |
| --- | --- | --- | --- | --- | --- |
| Tugas A | Tambang penerbangan | 10/1/2020 | 4 | 400 | 1600 |
| | Hotel | 10/1/2020 | 6 | 200 | 1200 |

Apabila pengguna memilih untuk meringkaskan dengan kelas Urus Niaga, Kategori dan Tugas Nod Leaf, maklumat berikut akan diimport. Perhatikan bahawa keputusan ini adalah sama seperti apa yang ada pada projek.

| Tugas | Kategori | Tarikh | Kuantiti | Harga unit | Amaun |
| --- | --- | --- | --- | --- | --- |
| Tugas A | Tambang penerbangan | 10/1/2020 | 4 | 400 | 1600 |
| Tugas B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Tugas C | Hotel | 11/1/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]