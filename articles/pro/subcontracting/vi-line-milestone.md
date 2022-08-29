---
title: Baris invois vendor untuk pencapaian
description: Artikel ini menerangkan cara membuat baris invois vendor untuk peristiwa penting pada subkontrak.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f066c2ac7377a989a92a9ae2e9a732d3c979a0db
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261039"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Baris invois vendor untuk pencapaian

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Invois vendor dalam Microsoft Dynamics 365 Project Operations boleh mempunyai baris invois vendor untuk peristiwa penting yang ditakrifkan pada garis subkontrak. Pengurus projek boleh menggunakan talian invois vendor untuk peristiwa penting untuk merekodkan kos perkhidmatan yang diperoleh sebagai kos berasaskan tonggak yang ditanggung ke atas perkhidmatan atau produk yang diperoleh untuk projek itu.

Baris invois vendor untuk peristiwa penting mesti sentiasa merujuk garis subkontrak yang mempunyai kaedah pengebilan harga tetap. Apabila baris invois vendor untuk peristiwa penting merujuk garis subkontrak, pengurus projek akan dapat memadankan dan mengesahkan kos asas masa, perbelanjaan atau bahan yang merujuk garis subkontrak terhadap peristiwa penting yang sedang diinvois oleh vendor.

Jadual berikut menyediakan maklumat tentang medan pada baris invois vendor untuk peristiwa penting.

| Medan | Description | Kesan kefungsian |
| --- | --- | --- |
| Nama | Nama talian invois vendor, untuk membantu mengenal pasti. | Nama ini akan ditunjukkan sebagai lajur pertama dalam semua carian yang berdasarkan baris invois vendor. |
| Description | Penerangan ringkas mengenai perkhidmatan yang sedang diinvois oleh vendor pada baris invois vendor. | Tiada |
| Subkontrak | Subkontrak yang pada asalnya dipesan oleh perkhidmatan tersebut. | Apabila subkontrak dipilih untuk invois vendor, semua baris pada invois vendor akan mewarisi pemilihan tersebut. Invois vendor tidak boleh mempunyai baris invois vendor yang merujuk subkontrak yang berbeza. |
| Garis subkontrak | Garis subkontrak yang dipesan oleh perkhidmatan tersebut. Senarai garis subkontrak yang boleh dipilih adalah terhad kepada garisan pada subkontrak yang dipilih. | Apabila baris subkontrak dipilih pada baris invois vendor untuk peristiwa penting, **medan kategori** Peranan **dan** Transaksi serta medan berkaitan produk, adalah tidak relevan dan tidak tersedia. Medan **kumpulan** Kuantiti **·**, Unit **dan** Unit juga tidak relevan untuk baris invois vendor berasaskan tonggak. |
| Tarikh transaksi | Tarikh kos sebenar talian invois vendor akan direkodkan pada projek. | Tiada |
| Kelas transaksi | Pilih **Milestone** untuk merakam invois vendor untuk peristiwa penting yang telah ditakrifkan pada baris subkontrak. | Tiada |
| Pencapaian | Pilih peristiwa penting yang ditakrifkan pada baris subkontrak berkaitan yang ditandakan sebagai **Sedia untuk Invois**. | Pencapaian baris subkontrak yang mempunyai status **Sedia untuk invois** boleh dipilih pada baris invois vendor. |
| Project | Nama projek yang perkhidmatan yang sedang diinvois telah digunakan. | Medan ini diperlukan dan tidak boleh dibiarkan kosong. |
| Tugas | Nama tugas projek yang digunakan oleh perkhidmatan yang sedang diinvois. Medan ini tersedia hanya jika projek dipilih. Pemilihan tugas projek adalah pilihan. | Jika medan ini dibiarkan kosong, pengurus projek boleh memadankan baris invois vendor dengan kelas transaksi pada garis subkontrak berkaitan yang direkodkan pada sebarang tugas projek. Jika baris invois vendor tidak merujuk garis subkontrak, dan medan ini dibiarkan kosong, kos sebenar yang dicipta oleh baris invois vendor tidak akan dipautkan kepada mana-mana jualan sebenar yang belum dibilkan. Dalam kes ini, jika pengebilan berasaskan tugas disediakan, kos mungkin tidak dapat diinvois kepada pelanggan akhir. |
| Jumlah pencapaian | Masukkan nilai peristiwa penting yang ditakrifkan pada baris subkontrak yang sedia untuk diinvois. | Tiada |
| Cukai jualan | Masukkan amaun cukai jualan. | Tiada |
| Jumlah | Jumlah keseluruhan baris invois vendor, termasuk cukai. Medan ini dikira sebagai *Milestone jumlah* + *cukai* Jualan. | Tiada |

> [!NOTE]
> Apabila baris invois vendor yang merujuk peristiwa penting baris subkontrak dicipta, status peristiwa penting subkontrak dikemas kini kepada **invois Vendor yang** dicipta. Kemudian, apabila invois vendor itu disahkan, status peristiwa penting baris subkontrak dikemas kini kepada **invois Vendor disahkan**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
