---
title: Baris invois vendor untuk kategori perbelanjaan
description: Artikel ini menerangkan cara merakam baris invois vendor untuk kategori perbelanjaan.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3ffad20b53344221ead9b6850ecdc1efd48d5b13
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925897"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Baris invois vendor untuk kategori perbelanjaan

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Invois vendor dalam Microsoft Dynamics 365 Project Operations boleh mempunyai baris invois vendor untuk kategori perbelanjaan. Pengurus projek boleh menggunakan baris invois vendor untuk kategori perbelanjaan untuk merekodkan kos perkhidmatan yang diperoleh sebagai kategori perbelanjaan.

Baris invois vendor untuk kategori perbelanjaan mungkin atau mungkin tidak merujuk baris subkontrak untuk kategori perbelanjaan. Jika baris invois vendor untuk kategori perbelanjaan merujuk subkontrak, pengurus projek akan dapat memadankan dan mengesahkan perbelanjaan yang diinvois oleh baris invois vendor terhadap perbelanjaan yang direkodkan pada kategori perbelanjaan ini dan diluluskan oleh pengurus projek pada projek.

Jadual berikut memberikan maklumat tentang medan pada baris invois vendor untuk kategori perbelanjaan.

| Medan | Description | Kesan kefungsian |
| --- | --- | --- |
| Nama | Nama baris invois vendor, untuk membantu pengenalan. | Nama ini akan ditunjukkan sebagai lajur pertama dalam semua carian yang berdasarkan baris invois vendor. |
| Description | Penerangan ringkas tentang perkhidmatan yang sedang diinvois oleh vendor pada baris invois vendor. | Tiada |
| Subkontrak | Subkontrak bahawa perkhidmatan pada asalnya diperintahkan. | Apabila subkontrak dipilih untuk invois vendor, semua baris pada invois vendor akan mewarisi pemilihan tersebut. Invois vendor tidak boleh mempunyai baris invois vendor yang merujuk subkontrak yang berbeza. |
| Garis subkontrak | Garis subkontrak yang mana perkhidmatan telah dipesan. Senarai baris subkontrak yang boleh dipilih adalah terhad kepada baris pada subkontrak yang dipilih. | Apabila baris subkontrak dipilih pada baris invois vendor untuk kategori perbelanjaan, nilai lalai untuk **medan kategori** Projek **,** Tugas **dan** Transaksi dimasukkan daripada medan yang sepadan pada baris subkontrak. Jika baris subkontrak yang dipilih mempunyai nilai dalam **medan Projek**, **Tugas** Projek dan **kategori** Transaksi, nilai medan yang sepadan pada baris invois vendor tidak boleh berbeza daripada nilai tersebut. |
| Tarikh transaksi | Tarikh apabila kos sebenar baris invois vendor akan direkodkan pada projek. |Tiada |
| Kelas transaksi | Pilih **Perbelanjaan** untuk merakam invois vendor untuk kategori perbelanjaan. | Nilai **Perbelanjaan** menunjukkan bahawa baris invois vendor digunakan untuk merekodkan jumlah invois untuk perkhidmatan yang diperoleh sebagai kategori perbelanjaan. |
| Project | Nama projek yang digunakan oleh perkhidmatan yang diinvois telah digunakan. | Medan ini diperlukan dan tidak boleh dibiarkan kosong. |
| Tugas | Nama tugas projek yang sedang diinvois oleh perkhidmatan yang sedang diinvois telah digunakan. Medan ini hanya tersedia jika projek dipilih. Pemilihan tugas projek adalah pilihan. | Jika medan ini dibiarkan kosong, pengurus projek boleh memadankan baris invois vendor dengan perbelanjaan yang direkodkan pada sebarang tugas projek. Jika baris invois vendor tidak merujuk baris subkontrak dan medan ini dibiarkan kosong, kos sebenar yang dicipta oleh baris invois vendor tidak akan dipautkan kepada sebarang real jualan yang tidak dibilkan. Dalam kes ini, jika pengebilan berasaskan tugas disediakan, kos mungkin tidak dapat diinvois kepada pelanggan akhir. |
| Kategori transaksi | Kategori transaksi yang sedang diinvois. Kategori perbelanjaan yang sepadan mesti dibuat untuk kategori transaksi yang dipilih. | Gabungan **kategori Transaksi dan** Nilai Unit **akan digunakan sebagai nilai lalai atau dikira untuk** medan Harga **unit pada** baris invois vendor. |
| Kuantiti | Masukkan kuantiti yang diinvois oleh vendor pada baris invois. |Tiada|
| Kumpulan unit | Nilai lalai dimasukkan berdasarkan kumpulan unit kategori transaksi yang dipilih. | Tiada |
| Unit | Nilai lalai ialah unit asas kumpulan unit yang dipilih. Anda boleh menukar nilai ini untuk membeli dalam mana-mana unit kumpulan unit. | Gabungan **kategori Transaksi dan** Nilai Unit **akan digunakan sebagai nilai lalai atau dikira untuk** medan Harga **unit pada** baris invois vendor. |
| Harga unit | Harga unit lalai menggunakan gabungan **kategori** Transaksi dan **nilai Unit** daripada senarai harga projek yang boleh digunakan pada tarikh transaksi baris invois vendor. | Jika harga untuk senarai harga projek yang berkenaan disediakan dalam unit yang berbeza daripada unit pada baris invois vendor, sistem menggunakan penukaran unit untuk mengira harga setiap unit. |
| Jumlah kecil | Medan baca sahaja ini dikira sebagai *harga* Unit Kuantiti&times;*·*, jika nilai dimasukkan dalam kedua-dua **medan Kuantiti** dan **medan Harga** unit. Jika satu atau kedua-dua medan tersebut kosong, anda boleh memasukkan nilai dalam medan ini.| Tiada |
| Cukai jualan | Masukkan amaun cukai jualan. | Tiada |
| Jumlah | Jumlah keseluruhan baris invois vendor, termasuk cukai. Medan ini dikira sebagai *cukai Jualan Subjumlah* + *·*. | Tiada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
