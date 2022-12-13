---
title: Garis peluang projek
description: Artikel ini memberikan maklumat tentang baris peluang berdasarkan projek. (Pro)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e4f67bd9b7d51559e2942e9005b8f5f9187b1f78
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824967"
---
# <a name="project-opportunity-lines"></a>Garis peluang projek 

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Garis peluang projek hanya tersedia dalam peluang berasaskan projek. Rekod peluang berdasarkan projek mempunyai nilai medan **Jenis** ditetapkan kepada **Berdasarkan kerja**.

Garis peluang projek adalah item baris yang akan dihantar kepada pelanggan menggunakan projek. Walau bagaimanapun, projek tidak boleh terikat kepada baris peluang berdasarkan projek. Projek boleh diikat kepada item baris daripada peringkat **Sebut Harga** dan ke hadapan kerana biasanya peluang berlaku di peringkat awal dalam kitaran hayat urus niaga. Penentuan jumlah projek yang akan digunakan untuk menyampaikan kerja untuk pelanggan ialah keputusan yang dibuat kemudian dalam fasa jualan. Anda boleh menggunakan fasa peluang untuk mengenal pasti komponen penghantaran diskret untuk pelanggan. Keputusan yang melingkungi jumlah projek sebenar yang digunakan untuk menyampaikan komponen ini boleh ditolak keluar sehingga lebih banyak maklumat diketahui tentang kerja itu sendiri.

Berikut adalah bidang pada garis peluang projek:

| **Medan** | **Location** | **Penerangan** | **Kesan hiliran** |
| --- | --- | --- | --- |
| Jenis Produk | Tab umum (tersembunyi) | Anda boleh memilih satu daripada pilihan yang berikut:</br>- Perkhidmatan berasaskan projek (hanya tersedia apabila Dynamics 365 Project Operations dipasang)</br>- Produk (tersedia hanya apabila Project Operations dan Dynamics 365 Sales dipasang) | Nilai medan ini ditetapkan kepada **Peluang berdasarkan projek** apabila anda mencipta baris peluang berdasarkan projek daripada grid baris berdasarkan projek pada Peluang. <br> Jika anda mengubah atau menulis ganti nilai ini, kefungsian projek tidak akan didayakan pada item baris berdasarkan projek anda. |
| Peluang | Tab umum | Medan ini ialah baca sahaja dan rujukan rekod Peluang induk yang item baris ini digolongkan. | Tiada kesan hiliran daripada medan ini. |
| Nama | Tab umum | Medan teks boleh diedit ini boleh digunakan untuk memberikan identiti ringkas kepada item baris. | Nilai ini dibawa ke dalam baris sebut harga apabila anda mencipta sebut harga daripada peluang ini. |
| Belanjawan Pelanggan | Tab umum | Medan mata wang boleh diedit ini boleh digunakan untuk menjejaki amaun yang pelanggan sanggup belanja untuk item baris ini. | Nilai ini dibawa ke dalam medan yang sepadan pada baris sebut harga apabila anda mencipta sebut harga daripada peluang ini. |
| Kaedah Pengebilan | Tab umum | Medan boleh diedit ini mempunyai nilai yang berikut:</br>- Masa dan Bahan</br>- Harga Tetap | Nilai ini dibawa ke dalam medan yang sepadan pada baris sebut harga apabila anda mencipta sebut harga daripada peluang ini. Selepas baris sebut harga dicipta, medan dikunci dan tidak boleh diubah. Peruntukkan nilai medan ini setepat yang mungkin. Jika anda perlu mengubah nilai medan ini pada baris sebut harga, padamkan dan cipta semula baris sebut harga. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
