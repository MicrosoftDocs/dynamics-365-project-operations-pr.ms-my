---
title: Import anggaran untuk projek pada baris sebut harga berasaskan projek
description: Topik ini menyediakan maklumat tentang cara mengimport anggaran daripada projek kepada baris sebut harga.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75511f0d7ef1d2d1b3bf5cc598a8f51d0c553939
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908403"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Import anggaran untuk projek pada baris sebut harga berasaskan projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_


Jika projek dicipta semasa peringkat prajualan, anda boleh memilih untuk mengimport anggaran kewangan daripada projek kepada baris sebut harga berasaskan projek.

1. Pastikan baris sebut harga berasaskan projek mempunyai maklumat projek dalam medan **Project**.
2. Pada tab **Butiran baris sebut harga**, pilih **Import daripada Anggaran Project**.
3. Pada halaman dialog yang dibuka, pilih salah satu pilihan peringkasan berikut.

  - **Kelas transaksi**
  - **Kategori**
  - **Peranan** 
  - **Tugas projek**

Berdasarkan pemilihan anda, anggaran daripada projek untuk semua kelas urus niaga termasuk pada baris sebut harga ini disalin. Untuk menyemak jenis kelas urus niaga yang disertakan, pilih tab **Umum** pada baris sebut harga berasaskan projek dan semak nilai untuk **Termasuk Masa**, **Termasuk Perbelanjaan** dan **Termasuk Yuran**.

Apabila anda mengimport anggaran, sistem akan melalaikan penetapan harga berdasarkan senarai harga projek yang dilampirkan pada sebut harga dan jenis pengebilan yang ditetapkan pada baris sebut harga berasaskan projek. Jika peranan atau kategori ditetapkan pada baris sebut harga berasaskan projek sebagai tidak boleh dikenakan, baris anggaran yang diimport akan ditetapkan sebagai tidak boleh dikenakan cukai dan tidak akan menambah pada nilai baris sebut harga yang disebut harga.

Apabila baris sebut harga mempunyai butiran baris, medan **Nilai Sebut Harga** dan **Anggaran Cukai** pada baris sebut harga diringkaskan dan tidak boleh diedit.

Apabila pilihan berbilang peringkasan dipilih, peringkasan cuba untuk meringkaskan dengan semua pilihan yang dipilih. Ini bererti bahawa output baris sebut harga yang diimport akan menjadi lebih banyak jika anda memilih hanya satu pilihan peringkasan.

Contohnya, jika projek mempunyai baris anggaran berikut untuk perbelanjaan.

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