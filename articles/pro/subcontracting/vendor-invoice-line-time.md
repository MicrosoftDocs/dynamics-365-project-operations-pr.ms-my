---
title: Baris invois vendor untuk masa
description: Artikel ini menerangkan cara merakam baris invois vendor untuk kos masa yang dimasukkan oleh subkontraktor.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0b81d2884580e9054457906627c1f9101f435524
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927557"
---
# <a name="vendor-invoice-lines-for-time"></a>Baris invois vendor untuk masa

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Invois vendor dalam Microsoft Dynamics 365 Project Operations boleh mempunyai baris invois vendor untuk masa. Pengurus projek boleh menggunakan baris invois vendor untuk masa untuk masa untuk merekodkan kos masa subkontraktor pada projek.

Baris invois vendor untuk masa mungkin atau mungkin tidak merujuk baris subkontrak untuk masa. Jika baris invois vendor untuk rujukan masa subkontrak, pengurus projek akan dapat memadankan dan mengesahkan masa yang diinvois oleh baris invois vendor terhadap masa yang direkodkan oleh subkontraktor dan diluluskan oleh pengurus projek pada projek.

Jadual berikut memberikan maklumat tentang medan pada baris invois vendor untuk masa.

| Medan | Description | Kesan kefungsian |
| --- | --- | --- |
| Nama | Nama baris invois vendor, untuk membantu pengenalan. | Nama ini akan ditunjukkan sebagai lajur pertama dalam semua carian yang berdasarkan baris invois vendor. |
| Description | Penerangan ringkas tentang perkhidmatan yang sedang diinvois oleh vendor pada baris invois vendor. | Tiada |
| Subkontrak | Subkontrak bahawa perkhidmatan pada asalnya diperintahkan. | Apabila subkontrak dipilih untuk invois vendor, semua baris pada invois vendor akan mewarisi pemilihan tersebut. Invois vendor tidak boleh mempunyai baris invois vendor yang merujuk subkontrak yang berbeza. |
| Garis subkontrak | Garis subkontrak yang mana perkhidmatan telah dipesan. Senarai baris subkontrak yang boleh dipilih adalah terhad kepada baris pada subkontrak yang dipilih. | Apabila baris subkontrak dipilih pada baris invois vendor untuk masa, nilai lalai untuk **medan Projek**, **Peranan** dan **Sumber** Boleh Ditempah dimasukkan daripada medan yang sepadan pada baris subkontrak. Jika baris subkontrak yang dipilih mempunyai nilai dalam **medan Projek**, **Peranan** dan **Boleh Ditempah, nilai medan yang** sepadan pada baris invois vendor tidak boleh berbeza daripada nilai tersebut. |
| Tarikh transaksi | Tarikh apabila kos sebenar baris invois vendor akan direkodkan pada projek. | Tiada |
| Kelas transaksi | Nilai lalai ialah **Masa**. | Nilai **Masa** menunjukkan bahawa baris invois vendor digunakan untuk merekodkan jumlah invois masa subkontraktor. |
| Project | Nama projek yang digunakan oleh perkhidmatan yang diinvois telah digunakan. | Medan ini diperlukan dan tidak boleh dibiarkan kosong. |
| Tugas | Nama tugas projek yang sedang diinvois oleh perkhidmatan yang sedang diinvois telah digunakan. Medan ini hanya tersedia jika projek dipilih. Pemilihan tugas projek adalah pilihan. | Jika medan ini dibiarkan kosong, pengurus projek boleh memadankan baris invois vendor dengan masa yang direkodkan oleh sumber subkontraktor pada sebarang tugas projek. Jika baris invois vendor tidak merujuk baris subkontrak dan medan ini dibiarkan kosong, kos sebenar yang dicipta oleh baris invois vendor tidak akan dipautkan kepada sebarang real jualan yang tidak dibilkan. Dalam kes ini, jika pengebilan berasaskan tugas disediakan, kos mungkin tidak dapat diinvois kepada pelanggan akhir. |
| Peranan | Peranan sumber subkontrak yang masa sedang diinvois. | Medan ini menentukan peranan yang dilakukan oleh sumber subkontrak yang masa diinvois pada invois vendor. |
| Sumber boleh ditempah | Nama subkontraktor yang masa sedang diinvois. Pemilihan sumber yang boleh ditempah adalah pilihan. | Jika medan ini dibiarkan kosong, pengurus projek boleh memadankan baris invois vendor dengan masa yang direkodkan oleh mana-mana sumber yang dimiliki oleh vendor pada baris invois vendor. |
| Kuantiti | Masukkan bilangan jam masa yang diinvois oleh vendor pada baris invois. |Tiada |
| Kumpulan unit | Nilai lalai ialah **kumpulan** unit masa dan tidak boleh diubah. | Tiada |
| Unit | Nilai lalai ialah unit asas jam daripada kumpulan unit masa. Anda boleh menukar nilai ini untuk membeli dalam mana-mana unit kumpulan unit masa, seperti hari atau minggu. | Gabungan **nilai Peranan** dan **Unit** akan digunakan sebagai nilai lalai atau dikira untuk **medan Harga** unit pada baris invois vendor. |
| Harga unit | Harga unit lalai menggunakan gabungan **nilai Peranan** dan **Unit** daripada senarai harga projek yang boleh digunakan pada tarikh transaksi baris invois vendor. | Jika harga untuk senarai harga projek yang berkenaan disediakan dalam unit yang berbeza daripada unit pada baris invois vendor, sistem menggunakan penukaran unit untuk mengira harga setiap unit. |
| Jumlah kecil | Medan baca sahaja ini dikira sebagai *harga* Unit Kuantiti&times;*·*, jika nilai dimasukkan dalam kedua-dua **medan Kuantiti** dan **medan Harga** unit. Jika satu atau kedua-dua medan tersebut kosong, anda boleh memasukkan nilai dalam medan ini. | Tiada |
| Cukai jualan | Masukkan amaun cukai jualan. | Tiada |
| Jumlah | Jumlah keseluruhan baris invois vendor, termasuk cukai. Medan ini dikira sebagai *cukai Jualan Subjumlah* + *·*. | Tiada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
