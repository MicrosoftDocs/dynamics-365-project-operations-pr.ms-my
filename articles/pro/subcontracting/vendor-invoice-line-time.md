---
title: Baris invois vendor untuk masa
description: Artikel ini menerangkan cara merakam baris invois vendor untuk kos masa yang dimasukkan oleh subkontraktor.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7f28af3ad76d456dddcfd8e85d968cecb773f8fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262024"
---
# <a name="vendor-invoice-lines-for-time"></a>Baris invois vendor untuk masa

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Invois vendor dalam Microsoft Dynamics 365 Project Operations boleh mempunyai talian invois vendor untuk masa. Pengurus projek boleh menggunakan talian invois vendor untuk masa untuk merekodkan kos masa subkontraktor pada projek.

Baris invois vendor untuk masa mungkin atau mungkin tidak merujuk garis subkontrak untuk masa. Jika baris invois vendor untuk rujukan masa subkontrak, pengurus projek akan dapat memadankan dan mengesahkan masa yang diinvois oleh baris invois vendor terhadap masa yang direkodkan oleh subkontraktor dan diluluskan oleh pengurus projek pada projek.

Jadual berikut menyediakan maklumat tentang medan pada baris invois vendor untuk masa.

| Medan | Description | Kesan kefungsian |
| --- | --- | --- |
| Nama | Nama talian invois vendor, untuk membantu mengenal pasti. | Nama ini akan ditunjukkan sebagai lajur pertama dalam semua carian yang berdasarkan baris invois vendor. |
| Description | Penerangan ringkas mengenai perkhidmatan yang sedang diinvois oleh vendor pada baris invois vendor. | Tiada |
| Subkontrak | Subkontrak yang pada asalnya dipesan oleh perkhidmatan tersebut. | Apabila subkontrak dipilih untuk invois vendor, semua baris pada invois vendor akan mewarisi pemilihan tersebut. Invois vendor tidak boleh mempunyai baris invois vendor yang merujuk subkontrak yang berbeza. |
| Garis subkontrak | Garis subkontrak yang dipesan oleh perkhidmatan tersebut. Senarai garis subkontrak yang boleh dipilih adalah terhad kepada garisan pada subkontrak yang dipilih. | Apabila baris subkontrak dipilih pada baris invois vendor untuk masa, nilai lalai bagi **medan Projek**, **Peranan** dan **Sumber** Boleh Ditempah dimasukkan daripada medan yang sepadan pada baris subkontrak. Jika garis subkontrak terpilih mempunyai nilai dalam **medan Projek**, **Peranan** dan **Boleh** Ditempah, nilai medan yang sepadan pada baris invois vendor tidak boleh berbeza daripada nilai tersebut. |
| Tarikh transaksi | Tarikh kos sebenar talian invois vendor akan direkodkan pada projek. | Tiada |
| Kelas transaksi | Nilai lalai ialah **Masa**. | **Nilai Masa** menunjukkan bahawa baris invois vendor sedang digunakan untuk merekodkan jumlah invois masa subkontraktor. |
| Project | Nama projek yang perkhidmatan yang sedang diinvois telah digunakan. | Medan ini diperlukan dan tidak boleh dibiarkan kosong. |
| Tugas | Nama tugas projek yang digunakan oleh perkhidmatan yang sedang diinvois. Medan ini tersedia hanya jika projek dipilih. Pemilihan tugas projek adalah pilihan. | Jika medan ini dibiarkan kosong, pengurus projek boleh memadankan baris invois vendor kepada masa yang direkodkan oleh sumber subkontraktor pada sebarang tugas projek. Jika baris invois vendor tidak merujuk garis subkontrak, dan medan ini dibiarkan kosong, kos sebenar yang dicipta oleh baris invois vendor tidak akan dipautkan kepada mana-mana jualan sebenar yang belum dibilkan. Dalam kes ini, jika pengebilan berasaskan tugas disediakan, kos mungkin tidak dapat diinvois kepada pelanggan akhir. |
| Peranan | Peranan sumber subkontrak yang masa sedang diinvois. | Medan ini menentukan peranan yang dilakukan oleh sumber subkontrak yang masanya diinvois pada invois vendor. |
| Sumber boleh ditempah | Nama subkontraktor yang masanya sedang diinvois. Pemilihan sumber boleh ditempah adalah pilihan. | Jika medan ini dibiarkan kosong, pengurus projek boleh memadankan baris invois vendor mengikut masa yang direkodkan oleh mana-mana sumber yang dimiliki oleh vendor pada baris invois vendor. |
| Kuantiti | Masukkan bilangan jam masa yang sedang diinvois oleh vendor pada baris invois. |Tiada |
| Kumpulan unit | Nilai lalai ialah **kumpulan** unit Masa dan tidak boleh diubah. | Tiada |
| Unit | Nilai lalai ialah unit asas jam daripada kumpulan unit masa. Anda boleh mengubah nilai ini untuk membeli dalam mana-mana unit masa kumpulan, seperti hari atau minggu. | Gabungan **nilai Peranan** dan **Unit** akan digunakan sebagai nilai lalai atau dikira untuk **medan harga** Unit pada baris invois vendor. |
| Harga unit | Harga unit lalai menggunakan gabungan **nilai Peranan** dan **Unit** daripada senarai harga projek yang boleh digunakan pada tarikh transaksi baris invois vendor. | Jika harga untuk senarai harga projek yang berkenaan disediakan dalam unit yang berbeza daripada unit pada baris invois vendor, sistem menggunakan penukaran unit untuk mengira harga seunit. |
| Jumlah kecil | Medan baca sahaja ini dikira sebagai *harga* Unit Kuantiti&times;*·*, jika nilai dimasukkan dalam kedua-dua **medan Kuantiti** dan **medan harga** Unit. Jika satu atau kedua-dua medan tersebut kosong, anda boleh memasukkan nilai dalam medan ini. | Tiada |
| Cukai jualan | Masukkan amaun cukai jualan. | Tiada |
| Jumlah | Jumlah keseluruhan baris invois vendor, termasuk cukai. Medan ini dikira sebagai *cukai* + *Jualan Subjumlah*. | Tiada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
