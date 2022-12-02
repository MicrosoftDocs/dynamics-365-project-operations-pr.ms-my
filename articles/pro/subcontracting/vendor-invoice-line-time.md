---
title: Baris invois vendor untuk masa
description: Artikel ini menerangkan cara merekodkan baris invois vendor untuk kos masa yang dimasukkan oleh subkontraktor.
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

Invois vendor dalam Microsoft Dynamics 365 Project Operations boleh mempunyai baris invois vendor untuk masa. Pengurus projek boleh menggunakan baris invois vendor bagi masa untuk merekodkan kos masa subkontraktor pada projek.

Baris invois vendor untuk masa mungkin atau mungkin tidak merujuk baris subkontrak untuk masa. Jika baris invois vendor untuk masa merujuk subkontrak, pengurus projek akan dapat memadankan dan mengesahkan masa yang sebagai diinvois oleh baris invois vendor terhadap masa yang direkodkan dan diluluskan oleh pengurus projek pada projek.

Jadual berikut menyediakan maklumat tentang medan pada baris invois vendor untuk masa.

| Medan | Description | Kesan kefungsian |
| --- | --- | --- |
| Nama | Nama baris invois vendor untuk membantu pengenalpastian. | Nama ini akan ditunjukkan sebagai lajur pertama dalam semua carian yang berdasarkan pada baris invois vendor. |
| Description | Penerangan ringkas tentang perkhidmatan yang sedang diinvois oleh vendor pada baris invois vendor. | Tiada |
| Subkontrak | Subkontrak yang perkhidmatan telah dipesan pada asalnya. | Apabila subkontrak dipilih untuk invois vendor, semua baris pada invois vendor akan mewarisi pemilihan tersebut. Invois vendor tidak boleh mempunyai baris invois vendor yang merujuk subkontrak berbeza. |
| Baris subkontrak | Baris subkontrak yang perkhidmatan telah dipesan. Senarai baris subkontrak yang boleh dipilih adalah terhad kepada baris pada subkontrak yang dipilih. | Apabila baris subkontrak dipilih pada baris invois vendor untuk masa, nilai lalai untuk medan **Projek**, **Peranan**, dan **Sumber boleh ditempah** akan dimasukkan daripada medan berkenaan pada baris subkontrak. Jika baris subkontrak yang dipilih mempunyai nilai dalam medan **Peranan**, **Boleh Ditempah**, dan **Produk**, nilai medan berkenaan pada baris invois vendor tidak boleh berbeza daripada nilai tersebut. |
| Tarikh transaksi | Tarikh apabila aktual kos baris invois vendor akan direkodkan pada projek. | Tiada |
| Kelas transaksi | Nilai lalai ialah **Masa**. | Nilai **Masa** akan menunjukkan bahawa baris invois vendor sedang digunakan untuk merekodkan jumlah invois bagi masa subkontraktor. |
| Project | Nama projek yang digunakan pada perkhidmatan yang sedang diinvois. | Medan ini diperlukan dan tidak boleh dibiarkan kosong. |
| Tugas | Nama tugas projek yang digunakan pada perkhidmatan yang sedang diinvois. Medan ini tersedia hanya jika projek dipilih. Pemilihan tugas projek adalah opsyenal. | Jika medan ini dibiarkan kosong, pengurus projek boleh memadankan baris invois vendor dengan masa yang direkodkan oleh sumber subkontraktor pada sebarang tugas projek. Jika baris invois vendor tidak merujuk baris subkontrak, dan medan ini dibiarkan kosong, aktual kos yang dicipta oleh baris invois vendor tidak akan dipautkan pada sebarang aktual jualan yang tidak dibilkan. Dalam kes ini, jika pengebilan berasaskan tugas ditetapkan, kos mungkin tidak dapat diinvois kepada pelanggan akhir. |
| Peranan | Peranan sumber subkontrak yang masanya sedang diinvois. | Medan ini menentukan peranan yang dilakukan oleh sumber subkontrak yang masanya diinvois pada invois vendor. |
| Sumber boleh ditempah | Nama subkontrak yang masanya sedang diinvois. Pemilihan sumber boleh ditempah adalah opsyenal. | Jika medan ini dibiarkan kosong, pengurus projek boleh memadankan baris invois vendor dengan masa yang direkodkan oleh sebarang sumber yang dimiliki oleh vendor pada baris invois vendor. |
| Kuantiti | Masukkan bilangan jam masa yang sedang diinvois oleh vendor pada baris invois. |Tiada |
| Kumpulan unit | Nilai lalai ialah **Kumpulan unit masa** dan tidak boleh diubah. | Tiada |
| Unit | Nilai lalai ialah unit asas jam daripada kumpulan unit masa. Anda boleh mengubah nilai ini untuk membeli apa-apa unit daripada kumpulan unit masa, seperti hari atau minggu. | Kombinasi **Peranan** dan nilai **Unit** akan digunakan sebagai lalai atau nilai yang dikira untuk medan **Harga unit** pada baris invois vendor. |
| Harga unit | Harga unit lalai menggunakan kombinasi **Peranan** dan nilai **Unit** daripada senarai harga projek yang terpakai untuk tarikh urus niaga baris invois vendor. | Jika harga untuk senarai harga projek terpakai ditetapkan dalam unit yang berbeza daripada unit pada baris invois vendor, sistem menggunakan penukaran unit untuk mengira harga seunit. |
| Jumlah kecil | Medan baca sahaja ini dikira sebagai *Kuantiti* &times; *Harga unit*, jika nilai dimasukkan dalam kedua-dua medan **Kuantiti** dan medan **Harga unit**. Jika salah satu atau kedua-dua medan adalah kosong, anda boleh memasukkan nilai dalam medan ini. | Tiada |
| Cukai jualan | Masukkan amaun cukai jualan. | Tiada |
| Jumlah amaun | Jumlah amaun baris invois vendor, termasuk cukai. Medan ini dikira sebagai *Subjumlah* + *Cukai jualan*. | Tiada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
