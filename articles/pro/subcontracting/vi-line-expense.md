---
title: Baris invois vendor untuk kategori perbelanjaan
description: Artikel ini menerangkan cara merakam baris invois vendor untuk kategori perbelanjaan.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2c3cd2fab87af1cbfccd81e543f2cea0278978f6
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261694"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Baris invois vendor untuk kategori perbelanjaan

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Invois vendor dalam Microsoft Dynamics 365 Project Operations boleh mempunyai baris invois vendor untuk kategori perbelanjaan. Pengurus projek boleh menggunakan talian invois vendor untuk kategori perbelanjaan untuk merekodkan kos perkhidmatan yang diperoleh sebagai kategori perbelanjaan.

Baris invois vendor untuk kategori perbelanjaan mungkin atau mungkin tidak merujuk garis subkontrak untuk kategori perbelanjaan. Jika baris invois vendor untuk kategori perbelanjaan merujuk subkontrak, pengurus projek akan dapat memadankan dan mengesahkan perbelanjaan yang sedang diinvois oleh talian invois vendor terhadap perbelanjaan yang direkodkan pada kategori perbelanjaan ini dan diluluskan oleh pengurus projek pada projek.

Jadual berikut menyediakan maklumat tentang medan pada baris invois vendor untuk kategori perbelanjaan.

| Medan | Description | Kesan kefungsian |
| --- | --- | --- |
| Nama | Nama talian invois vendor, untuk membantu mengenal pasti. | Nama ini akan ditunjukkan sebagai lajur pertama dalam semua carian yang berdasarkan baris invois vendor. |
| Description | Penerangan ringkas mengenai perkhidmatan yang sedang diinvois oleh vendor pada baris invois vendor. | Tiada |
| Subkontrak | Subkontrak yang pada asalnya dipesan oleh perkhidmatan tersebut. | Apabila subkontrak dipilih untuk invois vendor, semua baris pada invois vendor akan mewarisi pemilihan tersebut. Invois vendor tidak boleh mempunyai baris invois vendor yang merujuk subkontrak yang berbeza. |
| Garis subkontrak | Garis subkontrak yang dipesan oleh perkhidmatan tersebut. Senarai garis subkontrak yang boleh dipilih adalah terhad kepada garisan pada subkontrak yang dipilih. | Apabila baris subkontrak dipilih pada baris invois vendor untuk kategori perbelanjaan, nilai lalai untuk **medan kategori** Projek **,** Tugas **dan** Transaksi dimasukkan daripada medan yang sepadan pada baris subkontrak. Jika garis subkontrak terpilih mempunyai nilai dalam **medan kategori** Projek **,** Projek **dan** Transaksi, nilai medan sepadan pada baris invois vendor tidak boleh berbeza daripada nilai tersebut. |
| Tarikh transaksi | Tarikh kos sebenar talian invois vendor akan direkodkan pada projek. |Tiada |
| Kelas transaksi | Pilih **Perbelanjaan** untuk merekodkan invois vendor untuk kategori perbelanjaan. | **Nilai Perbelanjaan** menunjukkan bahawa talian invois vendor sedang digunakan untuk merekodkan jumlah invois untuk perkhidmatan yang diperoleh sebagai kategori perbelanjaan. |
| Project | Nama projek yang perkhidmatan yang sedang diinvois telah digunakan. | Medan ini diperlukan dan tidak boleh dibiarkan kosong. |
| Tugas | Nama tugas projek yang digunakan oleh perkhidmatan yang sedang diinvois. Medan ini tersedia hanya jika projek dipilih. Pemilihan tugas projek adalah pilihan. | Jika medan ini dibiarkan kosong, pengurus projek boleh memadankan talian invois vendor dengan perbelanjaan yang direkodkan pada sebarang tugas projek. Jika baris invois vendor tidak merujuk garis subkontrak, dan medan ini dibiarkan kosong, kos sebenar yang dicipta oleh baris invois vendor tidak akan dipautkan kepada mana-mana jualan sebenar yang belum dibilkan. Dalam kes ini, jika pengebilan berasaskan tugas disediakan, kos mungkin tidak dapat diinvois kepada pelanggan akhir. |
| Kategori transaksi | Kategori transaksi yang sedang diinvois. Kategori perbelanjaan yang sepadan mesti dibuat untuk kategori transaksi yang dipilih. | Gabungan **kategori Transaksi dan** nilai Unit **akan digunakan sebagai nilai lalai atau dikira untuk** medan Harga **Unit pada** baris invois vendor. |
| Kuantiti | Masukkan kuantiti yang sedang diinvois oleh vendor pada baris invois. |Tiada|
| Kumpulan unit | Nilai lalai dimasukkan berdasarkan kumpulan unit kategori transaksi terpilih. | Tiada |
| Unit | Nilai lalai ialah unit asas kumpulan unit yang dipilih. Anda boleh menukar nilai ini untuk membeli dalam mana-mana unit kumpulan unit. | Gabungan **kategori Transaksi dan** nilai Unit **akan digunakan sebagai nilai lalai atau dikira untuk** medan Harga **Unit pada** baris invois vendor. |
| Harga unit | Harga unit lalai menggunakan gabungan **kategori** Transaksi dan **nilai Unit** daripada senarai harga projek yang terpakai pada tarikh transaksi baris invois vendor. | Jika harga untuk senarai harga projek yang berkenaan disediakan dalam unit yang berbeza daripada unit pada baris invois vendor, sistem menggunakan penukaran unit untuk mengira harga seunit. |
| Jumlah kecil | Medan baca sahaja ini dikira sebagai *harga* Unit Kuantiti&times;*·*, jika nilai dimasukkan dalam kedua-dua **medan Kuantiti** dan **medan harga** Unit. Jika satu atau kedua-dua medan tersebut kosong, anda boleh memasukkan nilai dalam medan ini.| Tiada |
| Cukai jualan | Masukkan amaun cukai jualan. | Tiada |
| Jumlah | Jumlah keseluruhan baris invois vendor, termasuk cukai. Medan ini dikira sebagai *cukai* + *Jualan Subjumlah*. | Tiada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
