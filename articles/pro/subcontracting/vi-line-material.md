---
title: Barisan invois vendor untuk produk
description: Topik ini menerangkan cara merakam baris invois vendor untuk produk dan menggunakan medan yang berbeza untuk merakam pembelian produk daripada vendor.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: af078cd4392f8353b509db2dc48dc5237b8ee275
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599189"
---
# <a name="vendor-invoice-lines-for-products"></a>Barisan invois vendor untuk produk

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Invois vendor dalam Microsoft Dynamics 365 Project Operations boleh mempunyai baris invois vendor untuk produk (juga dirujuk sebagai bahan). Pengurus projek boleh menggunakan baris invois vendor untuk produk untuk merekodkan kos produk yang dibeli pada projek.

Baris invois vendor untuk produk mungkin atau mungkin tidak merujuk baris subkontrak untuk bahan. Jika baris invois vendor untuk produk merujuk subkontrak, pengurus projek akan dapat memadankan dan mengesahkan produk yang diinvois oleh baris invois vendor terhadap penggunaan produk yang dibeli yang direkodkan dan diluluskan oleh pengurus projek.

Jadual berikut memberikan maklumat tentang medan pada baris invois vendor untuk produk.

| Medan | Description | Kesan kefungsian |
| --- | --- | --- |
| Nama | Nama baris invois vendor, untuk membantu pengenalan. | Nama ini akan ditunjukkan sebagai lajur pertama dalam semua carian yang berdasarkan baris invois vendor. |
| Description | Penerangan ringkas tentang produk yang sedang diinvois oleh vendor pada baris invois vendor. | Tiada |
| Subkontrak | Subkontrak bahawa produk pada asalnya dipesan. | Apabila subkontrak dipilih untuk invois vendor, semua baris pada invois vendor akan mewarisi pemilihan tersebut. Invois vendor tidak boleh mempunyai baris invois vendor yang merujuk subkontrak yang berbeza. |
| Garis subkontrak | Barisan subkontrak bahawa produk telah dipesan. Senarai baris subkontrak yang boleh dipilih adalah terhad kepada baris pada subkontrak yang dipilih. | Apabila baris subkontrak dipilih pada baris invois vendor untuk produk, nilai lalai untuk **medan Projek**, **Tugas** dan **Produk** dimasukkan daripada medan yang sepadan pada baris subkontrak. Jika baris subkontrak yang dipilih mempunyai nilai dalam **medan Projek**, **Tugas** dan **Produk**, nilai medan yang sepadan pada baris invois vendor tidak boleh berbeza daripada nilai tersebut. |
| Tarikh transaksi | Tarikh apabila kos sebenar baris invois vendor akan direkodkan pada projek. | Tiada|
| Kelas transaksi | Apabila produk diinvois, medan ini harus ditetapkan kepada **Bahan**. | Nilai **Bahan** menunjukkan bahawa baris invois vendor digunakan untuk merekodkan jumlah invois untuk bahan yang dibeli. |
| Project | Nama projek bahawa produk yang diinvois telah digunakan. | Medan ini diperlukan dan tidak boleh dibiarkan kosong. |
| Tugas | Nama tugas projek yang sedang diinvois produk yang sedang diinvois telah digunakan. Medan ini hanya tersedia jika projek dipilih. Pemilihan tugas projek adalah pilihan. | Jika medan ini dibiarkan kosong, pengurus projek boleh memadankan baris invois vendor dengan produk yang dibeli yang digunakan pada sebarang tugas projek. Jika baris invois vendor tidak merujuk baris subkontrak dan medan ini dibiarkan kosong, kos sebenar yang dicipta oleh baris invois vendor tidak akan dipautkan kepada sebarang real jualan yang tidak dibilkan. Dalam kes ini, jika pengebilan berasaskan tugas disediakan, kos tidak akan dapat diinvois kepada pelanggan akhir. |
| Pilih produk | Pilih sama ada produk yang sedang diinvois adalah produk sedia ada daripada katalog atau produk tulis masuk. | Nilai lalai dimasukkan dari baris subkontrak apabila baris subkontrak dipilih. |
| Produk | Pilih produk daripada katalog. Jika produk adalah produk tulis, masukkan nama produk. | Medan ini digunakan untuk memasukkan harga belian lalai untuk produk sedia ada. |
| Kuantiti | Masukkan kuantiti bahan yang diinvois oleh vendor pada baris invois ini. | Tiada |
| Kumpulan unit | Pilih kumpulan unit unit yang kuantiti yang diinvois dinyatakan. | Tiada |
| Unit | Nilai lalai ialah unit asas kumpulan unit yang dipilih. Anda boleh menukar nilai ini untuk membayar dalam mana-mana unit kumpulan unit yang dipilih. | Gabungan nilai **Produk** dan **Unit** akan digunakan sebagai nilai lalai atau dikira untuk **medan Harga** unit pada baris invois vendor. |
| Harga unit | Harga unit lalai menggunakan gabungan **nilai Produk** dan **Unit** dari senarai harga projek yang berlaku pada tarikh transaksi baris invois vendor. | Tiada |
| Jumlah kecil | Medan baca sahaja ini dikira sebagai *harga* Unit Kuantiti&times;*·*, jika nilai dimasukkan dalam kedua-dua **medan Kuantiti** dan **medan Harga** unit. Jika satu atau kedua-dua medan tersebut kosong, anda boleh memasukkan nilai dalam medan ini. | Tiada |
| Cukai jualan | Masukkan amaun cukai jualan. | Tiada |
| Jumlah | Jumlah keseluruhan baris invois vendor, termasuk cukai. Medan ini dikira sebagai *cukai Jualan Subjumlah* + *·*. | Tiada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
