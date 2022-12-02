---
title: Baris invois vendor untuk kategori perbelanjaan
description: Artikel ini menerangkan cara merekodkan baris invois vendor untuk kategori perbelanjaan.
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

Invois vendor dalam Microsoft Dynamics 365 Project Operations boleh mempunyai baris invois vendor untuk kategori perbelanjaan. Pengurus Projek boleh menggunakan baris invois vendor bagi kategori perbelanjaan untuk merekodkan kos perkhidmatan yang diperoleh sebagai kategori perbelanjaan.

Baris invois vendor untuk kategori perbelanjaan mungkin atau mungkin tidak merujuk baris subkontrak untuk kategori perbelanjaan. Jika baris invois vendor untuk kategori perbelanjaan merujuk subkontrak, pengurus projek akan dapat memadankan dan mengesahkan perbelanjaan yang sebagai diinvois oleh baris invois vendor terhadap perbelanjaan yang direkodkan pada kategori perbelanjaan ini dan diluluskan oleh pengurus projek pada projek.

Jadual berikut menyediakan maklumat tentang medan pada baris invois vendor untuk kategori perbelanjaan.

| Medan | Description | Kesan kefungsian |
| --- | --- | --- |
| Nama | Nama baris invois vendor untuk membantu pengenalpastian. | Nama ini akan ditunjukkan sebagai lajur pertama dalam semua carian yang berdasarkan pada baris invois vendor. |
| Description | Penerangan ringkas tentang perkhidmatan yang sedang diinvois oleh vendor pada baris invois vendor. | Tiada |
| Subkontrak | Subkontrak yang perkhidmatan telah dipesan pada asalnya. | Apabila subkontrak dipilih untuk invois vendor, semua baris pada invois vendor akan mewarisi pemilihan tersebut. Invois vendor tidak boleh mempunyai baris invois vendor yang merujuk subkontrak berbeza. |
| Baris subkontrak | Baris subkontrak yang perkhidmatan telah dipesan. Senarai baris subkontrak yang boleh dipilih adalah terhad kepada baris pada subkontrak yang dipilih. | Apabila baris subkontrak dipilih pada baris invois vendor untuk kategori perbelanjaan, nilai lalai untuk medan **Projek**, **Tugas**, dan **Kategori urus niaga** akan dimasukkan daripada medan berkenaan pada baris subkontrak. Jika baris subkontrak yang dipilih mempunyai nilai dalam medan **Projek**, **Tugas projek**, dan **Kategori urus niaga**, nilai medan berkenaan pada baris invois vendor tidak boleh berbeza daripada nilai tersebut. |
| Tarikh transaksi | Tarikh apabila aktual kos baris invois vendor akan direkodkan pada projek. |Tiada |
| Kelas transaksi | Pilih **Perbelanjaan** untuk merekodkan invois vendor bagi kategori perbelanjaan. | Nilai **Perbelanjaan** akan menunjukkan bahawa baris invois vendor sedang digunakan untuk merekodkan jumlah invois bagi perkhidmatan yang diperoleh sebagai kategori perbelanjaan. |
| Project | Nama projek yang digunakan pada perkhidmatan yang sedang diinvois. | Medan ini diperlukan dan tidak boleh dibiarkan kosong. |
| Tugas | Nama tugas projek yang digunakan pada perkhidmatan yang sedang diinvois. Medan ini tersedia hanya jika projek dipilih. Pemilihan tugas projek adalah opsyenal. | Jika medan ini dibiarkan kosong, pengurus projek boleh memadankan baris invois vendor dengan perbelanjaan yang direkodkan pada sebarang tugas projek. Jika baris invois vendor tidak merujuk baris subkontrak, dan medan ini dibiarkan kosong, aktual kos yang dicipta oleh baris invois vendor tidak akan dipautkan pada sebarang aktual jualan yang tidak dibilkan. Dalam kes ini, jika pengebilan berasaskan tugas ditetapkan, kos mungkin tidak dapat diinvois kepada pelanggan akhir. |
| Kategori transaksi | Kategori urus niaga yang sedang invois. Kategori perbelanjaan yang berkaitan mesti dicipta untuk kategori urus niaga yang dipilih. | Kombinasi **Kategori urus niaga** dan nilai **Unit** akan digunakan sebagai lalai atau nilai yang dikira untuk medan **Harga unit** pada baris invois vendor. |
| Kuantiti | Masukkan kuantiti yang sedang diinvois oleh vendor pada baris invois. |Tiada|
| Kumpulan unit | Nilai lalai dimasukkan berdasarkan pada kumpulan unit bagi kategori urus niaga yang dipilih. | Tiada |
| Unit | Nilai lalai ialah unit asas kumpulan unit yang dipilih. Anda boleh mengubah nilai ini untuk membeli apa-apa unit daripada kumpulan unit. | Kombinasi **Kategori urus niaga** dan nilai **Unit** akan digunakan sebagai lalai atau nilai yang dikira untuk medan **Harga unit** pada baris invois vendor. |
| Harga unit | Harga unit lalai menggunakan kombinasi **Kategori urus niaga** dan nilai **Unit** daripada senarai harga projek yang terpakai untuk tarikh urus niaga baris invois vendor. | Jika harga untuk senarai harga projek terpakai ditetapkan dalam unit yang berbeza daripada unit pada baris invois vendor, sistem menggunakan penukaran unit untuk mengira harga seunit. |
| Jumlah kecil | Medan baca sahaja ini dikira sebagai *Kuantiti* &times; *Harga unit*, jika nilai dimasukkan dalam kedua-dua medan **Kuantiti** dan medan **Harga unit**. Jika salah satu atau kedua-dua medan adalah kosong, anda boleh memasukkan nilai dalam medan ini.| Tiada |
| Cukai jualan | Masukkan amaun cukai jualan. | Tiada |
| Jumlah amaun | Jumlah amaun baris invois vendor, termasuk cukai. Medan ini dikira sebagai *Subjumlah* + *Cukai jualan*. | Tiada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
