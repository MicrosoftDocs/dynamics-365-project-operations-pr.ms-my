---
title: Baris invois vendor untuk pencapaian
description: Artikel ini menerangkan cara membuat baris invois vendor untuk pencapaian pada subkontrak.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 212d68c32e712ac2349d1670f9e799bcc5144148
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931341"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Baris invois vendor untuk pencapaian

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Invois vendor dalam Microsoft Dynamics 365 Project Operations boleh mempunyai baris invois vendor untuk tonggak yang ditakrifkan pada baris subkontrak. Pengurus projek boleh menggunakan baris invois vendor untuk tonggak untuk merekodkan kos perkhidmatan yang diperoleh sebagai kos berasaskan tonggak yang ditanggung pada perkhidmatan atau produk yang diperoleh untuk projek.

Baris invois vendor untuk tonggak mesti sentiasa merujuk baris subkontrak yang mempunyai kaedah pengebilan harga tetap. Apabila baris invois vendor untuk tonggak merujuk baris subkontrak, pengurus projek akan dapat memadankan dan mengesahkan kos asas masa, perbelanjaan atau bahan yang merujuk garis subkontrak terhadap pencapaian yang sedang diinvois oleh vendor.

Jadual berikut memberikan maklumat tentang medan pada baris invois vendor untuk peristiwa penting.

| Medan | Description | Kesan kefungsian |
| --- | --- | --- |
| Nama | Nama baris invois vendor, untuk membantu pengenalan. | Nama ini akan ditunjukkan sebagai lajur pertama dalam semua carian yang berdasarkan baris invois vendor. |
| Description | Penerangan ringkas tentang perkhidmatan yang sedang diinvois oleh vendor pada baris invois vendor. | Tiada |
| Subkontrak | Subkontrak bahawa perkhidmatan pada asalnya diperintahkan. | Apabila subkontrak dipilih untuk invois vendor, semua baris pada invois vendor akan mewarisi pemilihan tersebut. Invois vendor tidak boleh mempunyai baris invois vendor yang merujuk subkontrak yang berbeza. |
| Garis subkontrak | Garis subkontrak yang mana perkhidmatan telah dipesan. Senarai baris subkontrak yang boleh dipilih adalah terhad kepada baris pada subkontrak yang dipilih. | Apabila baris subkontrak dipilih pada baris invois vendor untuk peristiwa penting, **medan kategori** Peranan **dan** Transaksi serta medan berkaitan produk, tidak relevan dan tidak tersedia. Medan **kumpulan** Kuantiti **·**, Unit **dan** Unit juga tidak relevan untuk baris invois vendor berasaskan tonggak. |
| Tarikh transaksi | Tarikh apabila kos sebenar baris invois vendor akan direkodkan pada projek. | Tiada |
| Kelas transaksi | Pilih **Milestone** untuk merakam invois vendor untuk pencapaian lengkap yang ditakrifkan pada baris subkontrak. | Tiada |
| Pencapaian | Pilih peristiwa penting yang ditakrifkan pada baris subkontrak berkaitan yang ditandakan sebagai **Sedia untuk Invois**. | Tonggak baris subkontrak yang mempunyai status **Sedia untuk invois** boleh dipilih pada baris invois vendor. |
| Project | Nama projek yang digunakan oleh perkhidmatan yang diinvois telah digunakan. | Medan ini diperlukan dan tidak boleh dibiarkan kosong. |
| Tugas | Nama tugas projek yang sedang diinvois oleh perkhidmatan yang sedang diinvois telah digunakan. Medan ini hanya tersedia jika projek dipilih. Pemilihan tugas projek adalah pilihan. | Jika medan ini dibiarkan kosong, pengurus projek boleh memadankan baris invois vendor dengan kelas transaksi pada baris subkontrak berkaitan yang direkodkan pada mana-mana tugas projek. Jika baris invois vendor tidak merujuk baris subkontrak dan medan ini dibiarkan kosong, kos sebenar yang dicipta oleh baris invois vendor tidak akan dipautkan kepada sebarang real jualan yang tidak dibilkan. Dalam kes ini, jika pengebilan berasaskan tugas disediakan, kos mungkin tidak dapat diinvois kepada pelanggan akhir. |
| Jumlah pencapaian | Masukkan nilai peristiwa penting yang ditakrifkan pada baris subkontrak yang sedia untuk diinvois. | Tiada |
| Cukai jualan | Masukkan amaun cukai jualan. | Tiada |
| Jumlah | Jumlah keseluruhan baris invois vendor, termasuk cukai. Medan ini dikira sebagai *jumlah* + *Milestone Cukai jualan*. | Tiada |

> [!NOTE]
> Apabila baris invois vendor yang merujuk tonggak baris subkontrak dicipta, status pencapaian subkontrak dikemas kini kepada **invois Vendor yang dibuat**. Kemudian, apabila invois vendor tersebut disahkan, status pencapaian baris subkontrak dikemas kini kepada **invois Vendor disahkan**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
