---
title: Baris invois vendor untuk produk
description: Artikel ini menerangkan cara merekodkan baris invois vendor untuk produk dan menggunakan medan berbeza untuk merekodkan pembelian produk daripada vendor.
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

Invois vendor dalam Microsoft Dynamics 365 Project Operations boleh mempunyai baris invois vendor untuk produk (juga dirujuk sebagai bahan). Pengurus projek boleh menggunakan baris invois vendor bagi produk untuk merekodkan kos produk yang telah dibeli pada projek.

Baris invois vendor untuk produk mungkin atau mungkin tidak merujuk baris subkontrak untuk bahan. Jika baris invois vendor untuk produk merujuk subkontrak, pengurus projek akan dapat memadankan dan mengesahkan produk yang sebagai diinvois oleh baris invois vendor terhadap penggunaan pembelian produk yang direkodkan dan diluluskan oleh pengurus projek.

Jadual berikut menyediakan maklumat tentang medan pada baris invois vendor untuk produk.

| Medan | Description | Kesan kefungsian |
| --- | --- | --- |
| Nama | Nama baris invois vendor untuk membantu pengenalpastian. | Nama ini akan ditunjukkan sebagai lajur pertama dalam semua carian yang berdasarkan pada baris invois vendor. |
| Description | Penerangan ringkas tentang produk yang sedang diinvois oleh vendor pada baris invois vendor. | Tiada |
| Subkontrak | Subkontrak yang produk telah dipesan pada asalnya. | Apabila subkontrak dipilih untuk invois vendor, semua baris pada invois vendor akan mewarisi pemilihan tersebut. Invois vendor tidak boleh mempunyai baris invois vendor yang merujuk subkontrak berbeza. |
| Baris subkontrak | Baris subkontrak yang produk telah dipesan. Senarai baris subkontrak yang boleh dipilih adalah terhad kepada baris pada subkontrak yang dipilih. | Apabila baris subkontrak dipilih pada baris invois vendor untuk produk, nilai lalai untuk medan **Projek**, **Tugas**, dan **Produk** akan dimasukkan daripada medan berkenaan pada baris subkontrak. Jika baris subkontrak yang dipilih mempunyai nilai dalam medan **Projek**, **Tugas**, dan **Produk**, nilai medan berkenaan pada baris invois vendor tidak boleh berbeza daripada nilai tersebut. |
| Tarikh transaksi | Tarikh apabila aktual kos baris invois vendor akan direkodkan pada projek. | Tiada|
| Kelas transaksi | Apabila produk diinvois, medan ini harus ditetapkan kepada **Bahan**. | Nilai **Bahan** akan menunjukkan bahawa baris invois vendor sedang digunakan untuk merekodkan jumlah invois bagi bahan yang dibeli. |
| Project | Nama projek yang digunakan pada produk yang sedang diinvois. | Medan ini diperlukan dan tidak boleh dibiarkan kosong. |
| Tugas | Nama tugas projek yang digunakan pada produk yang sedang diinvois. Medan ini tersedia hanya jika projek dipilih. Pemilihan tugas projek adalah opsyenal. | Jika medan ini dibiarkan kosong, pengurus projek boleh memadankan baris invois vendor dengan pembelian produk yang digunakan pada sebarang tugas projek. Jika baris invois vendor tidak merujuk baris subkontrak, dan medan ini dibiarkan kosong, aktual kos yang dicipta oleh baris invois vendor tidak akan dipautkan pada sebarang aktual jualan yang tidak dibilkan. Dalam kes ini, jika pengebilan berasaskan tugas ditetapkan, kos mungkin tidak dapat diinvois kepada pelanggan akhir. |
| Pilih produk | Pilih sama ada produk yang sedang diinvois ialah produk sedia ada daripada produk katalog atau produk masukan manual. | Nilai lalai dimasukkan daripada baris subkontrak apabila baris subkontrak dipilih. |
| Produk | Pilih produk daripada katalog. Jika produk ialah produk masukan manual, masukkan nama produk. | Medan ini digunakan untuk memasukkan harga pembelian lalai bagi produk sedia ada. |
| Kuantiti | Masukkan kuantiti bahan yang sedang diinvois oleh vendor pada baris invois ini. | Tiada |
| Kumpulan unit | Pilih kumpulan unit bagi unit yang dijelaskan dalam kuantiti yang sedang diinvois. | Tiada |
| Unit | Nilai lalai ialah unit asas kumpulan unit yang dipilih. Anda boleh mengubah nilai ini untuk membayar dalam apa-apa unit daripada kumpulan unit yang dipilih. | Kombinasi **Produk** dan nilai **Unit** akan digunakan sebagai lalai atau nilai yang dikira untuk medan **Harga unit** pada baris invois vendor. |
| Harga unit | Harga unit lalai menggunakan kombinasi **Produk** dan nilai **Unit** daripada senarai harga projek yang terpakai untuk tarikh urus niaga baris invois vendor. | Tiada |
| Jumlah kecil | Medan baca sahaja ini dikira sebagai *Kuantiti* &times; *Harga unit*, jika nilai dimasukkan dalam kedua-dua medan **Kuantiti** dan medan **Harga unit**. Jika salah satu atau kedua-dua medan adalah kosong, anda boleh memasukkan nilai dalam medan ini. | Tiada |
| Cukai jualan | Masukkan amaun cukai jualan. | Tiada |
| Jumlah amaun | Jumlah amaun baris invois vendor, termasuk cukai. Medan ini dikira sebagai *Subjumlah* + *Cukai jualan*. | Tiada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
