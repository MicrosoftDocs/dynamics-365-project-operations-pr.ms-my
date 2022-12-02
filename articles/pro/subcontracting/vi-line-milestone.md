---
title: Baris invois vendor untuk pencapaian
description: Artikel ini menerangkan cara untuk mencipta baris invois vendor untuk pencapaian pada subkontrak.
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

Invois vendor dalam Microsoft Dynamics 365 Project Operations boleh mempunyai baris invois vendor untuk pencapaian yang ditakrifkan pada baris subkontrak. Pengurus projek boleh menggunakan baris invois vendor bagi pencapaian untuk merekodkan kos perkhidmatan yang diperoleh sebagai kos berasaskan pencapaian yang ditanggung pada perkhidmatan atau produk yang diperoleh untuk projek.

Baris invois vendor untuk pencapaian mesti sentiasa merujuk baris subkontrak yang mempunyai kaedah pengebilan harga Tetap. Apabila baris invois vendor untuk pencapaian merujuk baris subkontrak, pengurus projek akan dapat memadankan dan mengesahkan kos tersembunyi bagi masa, perbelanjaan atau bahan yang merujuk baris subkonrak terhadap pencapaian yang sedang diinvois oleh vendor.

Jadual berikut menyediakan maklumat tentang medan pada baris invois vendor untuk pencapaian.

| Medan | Description | Kesan kefungsian |
| --- | --- | --- |
| Nama | Nama baris invois vendor untuk membantu pengenalpastian. | Nama ini akan ditunjukkan sebagai lajur pertama dalam semua carian yang berdasarkan pada baris invois vendor. |
| Description | Penerangan ringkas tentang perkhidmatan yang sedang diinvois oleh vendor pada baris invois vendor. | Tiada |
| Subkontrak | Subkontrak yang perkhidmatan telah dipesan pada asalnya. | Apabila subkontrak dipilih untuk invois vendor, semua baris pada invois vendor akan mewarisi pemilihan tersebut. Invois vendor tidak boleh mempunyai baris invois vendor yang merujuk subkontrak berbeza. |
| Baris subkontrak | Baris subkontrak yang perkhidmatan telah dipesan. Senarai baris subkontrak yang boleh dipilih adalah terhad kepada baris pada subkontrak yang dipilih. | Apabila baris subkontrak dipilih pada baris invois vendor untuk pencapaian, medan **Peranan** dan **Kategori urus niaga** dan medan berkaitan produk, tidak relevan dan tidak tersedia. Mendan **Kuantiti**, **Unit**, dan **Kumpulan unit** juga tidak relevan untuk garis invois vendor berasaskan pencapaian. |
| Tarikh transaksi | Tarikh apabila aktual kos baris invois vendor akan direkodkan pada projek. | Tiada |
| Kelas transaksi | Pilih **Pencapaian** untuk merekodkan invois vendor untuk pencapaian lengkap yang ditakrifkan pada baris subkontrak. | Tiada |
| Pencapaian | Pilih pencapaian yang ditakrifkan pada baris subkontrak berkaitan yang ditandakan sebagai **Tersedia untuk Invois**. | Pencapaian baris subkontrak yang mempunyai status **Tersedia untuk invois** boleh dipilih pada baris invois vendor. |
| Project | Nama projek yang digunakan pada perkhidmatan yang sedang diinvois. | Medan ini diperlukan dan tidak boleh dibiarkan kosong. |
| Tugas | Nama tugas projek yang digunakan pada perkhidmatan yang sedang diinvois. Medan ini tersedia hanya jika projek dipilih. Pemilihan tugas projek adalah opsyenal. | Jika medan ini dibiarkan kosong, pengurus projek boleh memadankan baris invois vendor dengan kelas urus niaga pada baris subkontrak berkaitan yang direkodkan pada sebarang tugas projek. Jika baris invois vendor tidak merujuk baris subkontrak, dan medan ini dibiarkan kosong, aktual kos yang dicipta oleh baris invois vendor tidak akan dipautkan pada sebarang aktual jualan yang tidak dibilkan. Dalam kes ini, jika pengebilan berasaskan tugas ditetapkan, kos mungkin tidak dapat diinvois kepada pelanggan akhir. |
| Jumlah pencapaian | Masukkan nilai pencapaian yang ditakrifkan pada baris subkontrak yang tersedia untuk diinvois. | Tiada |
| Cukai jualan | Masukkan amaun cukai jualan. | Tiada |
| Jumlah amaun | Jumlah amaun baris invois vendor, termasuk cukai. Medan ini dikira sebagai *Jumlah pencapaian* + *Cukai jualan*. | Tiada |

> [!NOTE]
> Apabila baris invois vendor yang merujuk baris pencapaian baris subkontrak dicipta, status pencapaian subkontrak dikemas kini kepada **Invois vendor dicipta**. Kemudian, apabila invois vendor disahkan, status pencapaian baris subkontrak dikemas kini kepada **Invois vendor disahkan**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
