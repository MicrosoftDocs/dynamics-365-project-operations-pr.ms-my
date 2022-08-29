---
title: Baris invois vendor untuk produk
description: Artikel ini menerangkan cara merakam baris invois vendor untuk produk dan menggunakan medan yang berbeza untuk merakam pembelian produk daripada vendor.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d38a447c576c095a7bbe2f5ed84342a88bf69a9b
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261570"
---
# <a name="vendor-invoice-lines-for-products"></a>Baris invois vendor untuk produk

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Invois vendor dalam Microsoft Dynamics 365 Project Operations boleh mempunyai talian invois vendor untuk produk (juga dirujuk sebagai bahan). Pengurus projek boleh menggunakan talian invois vendor untuk produk untuk merekodkan kos produk yang dibeli pada projek.

Baris invois vendor untuk produk mungkin atau mungkin tidak merujuk garis subkontrak untuk bahan. Jika baris invois vendor untuk rujukan produk sebagai subkontrak, pengurus projek akan dapat memadankan dan mengesahkan produk yang sedang diinvois oleh baris invois vendor terhadap penggunaan produk yang dibeli yang direkodkan dan diluluskan oleh pengurus projek.

Jadual berikut menyediakan maklumat tentang medan pada baris invois vendor untuk produk.

| Medan | Description | Kesan kefungsian |
| --- | --- | --- |
| Nama | Nama talian invois vendor, untuk membantu mengenal pasti. | Nama ini akan ditunjukkan sebagai lajur pertama dalam semua carian yang berdasarkan baris invois vendor. |
| Description | Penerangan ringkas mengenai produk yang sedang diinvois oleh vendor pada baris invois vendor. | Tiada |
| Subkontrak | Subkontrak yang produk pada asalnya dipesan. | Apabila subkontrak dipilih untuk invois vendor, semua baris pada invois vendor akan mewarisi pemilihan tersebut. Invois vendor tidak boleh mempunyai baris invois vendor yang merujuk subkontrak yang berbeza. |
| Garis subkontrak | Garis subkontrak yang dipesan oleh produk. Senarai garis subkontrak yang boleh dipilih adalah terhad kepada garisan pada subkontrak yang dipilih. | Apabila baris subkontrak dipilih pada baris invois vendor untuk produk, nilai lalai untuk **medan Projek**, **Tugas** dan **Produk** dimasukkan daripada medan yang sepadan pada baris subkontrak. Jika garis subkontrak terpilih mempunyai nilai dalam **medan Projek**, **Tugas** dan **Produk**, nilai medan sepadan pada baris invois vendor tidak boleh berbeza daripada nilai tersebut. |
| Tarikh transaksi | Tarikh kos sebenar talian invois vendor akan direkodkan pada projek. | Tiada|
| Kelas transaksi | Apabila produk diinvois, medan ini hendaklah ditetapkan kepada **Bahan**. | Bahan **nilai** menunjukkan bahawa talian invois vendor sedang digunakan untuk merekodkan jumlah invois untuk bahan yang dibeli. |
| Project | Nama projek yang produk yang sedang diinvois telah digunakan. | Medan ini diperlukan dan tidak boleh dibiarkan kosong. |
| Tugas | Nama tugas projek yang produk yang sedang diinvois telah digunakan. Medan ini tersedia hanya jika projek dipilih. Pemilihan tugas projek adalah pilihan. | Jika medan ini dibiarkan kosong, pengurus projek boleh memadankan baris invois vendor dengan produk yang dibeli yang digunakan pada sebarang tugas projek. Jika baris invois vendor tidak merujuk garis subkontrak, dan medan ini dibiarkan kosong, kos sebenar yang dicipta oleh baris invois vendor tidak akan dipautkan kepada mana-mana jualan sebenar yang belum dibilkan. Dalam kes ini, jika pengebilan berasaskan tugas disediakan, kos tidak akan dapat diinvois kepada pelanggan akhir. |
| Pilih produk | Pilih sama ada produk yang sedang diinvois ialah produk sedia ada daripada katalog atau produk tulis. | Nilai lalai dimasukkan daripada garis subkontrak apabila garis subkontrak dipilih. |
| Produk | Pilih produk daripada katalog. Jika produk adalah produk tulis, masukkan nama produk. | Medan ini digunakan untuk memasukkan harga pembelian lalai untuk produk sedia ada. |
| Kuantiti | Masukkan kuantiti bahan yang sedang diinvois oleh vendor pada baris invois ini. | Tiada |
| Kumpulan unit | Pilih kumpulan unit unit yang kuantiti yang sedang diinvois dinyatakan. | Tiada |
| Unit | Nilai lalai ialah unit asas kumpulan unit yang dipilih. Anda boleh menukar nilai ini untuk membayar dalam mana-mana unit kumpulan unit yang dipilih. | Gabungan **nilai Produk** dan **Unit** akan digunakan sebagai nilai lalai atau dikira untuk **medan Harga** unit pada baris invois vendor. |
| Harga unit | Harga unit lalai menggunakan gabungan **nilai Produk** dan **Unit** daripada senarai harga projek yang boleh digunakan pada tarikh transaksi baris invois vendor. | Tiada |
| Jumlah kecil | Medan baca sahaja ini dikira sebagai *harga* Unit Kuantiti&times;*·*, jika nilai dimasukkan dalam kedua-dua **medan Kuantiti** dan **medan harga** Unit. Jika satu atau kedua-dua medan tersebut kosong, anda boleh memasukkan nilai dalam medan ini. | Tiada |
| Cukai jualan | Masukkan amaun cukai jualan. | Tiada |
| Jumlah | Jumlah keseluruhan baris invois vendor, termasuk cukai. Medan ini dikira sebagai *cukai* + *Jualan Subjumlah*. | Tiada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
