---
title: Baris peluang berasaskan projek - lite
description: Topik ini memberikan maklumat tentang baris peluang berdasarkan projek. (Pro)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1978b452b84486cabd5b6b4e550261e2c8f76cd89a140709b137ac184c8967c1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999012"
---
# <a name="project-based-opportunity-lines---lite"></a>Baris peluang berasaskan projek - lite

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Baris peluang berdasarkan projek hanya tersedia dalam peluang berdasarkan projek. Rekod peluang berdasarkan projek mempunyai nilai medan **Jenis** ditetapkan kepada **Berdasarkan kerja**.

Baris peluang berdasarkan projek ialah item baris yang akan disampaikan kepada pelanggan menggunakan projek. Walau bagaimanapun, projek tidak boleh terikat kepada baris peluang berdasarkan projek. Projek boleh diikat kepada item baris daripada peringkat **Sebut Harga** dan ke hadapan kerana biasanya peluang berlaku di peringkat awal dalam kitaran hayat urus niaga. Penentuan jumlah projek yang akan digunakan untuk menyampaikan kerja untuk pelanggan ialah keputusan yang dibuat kemudian dalam fasa jualan. Anda boleh menggunakan fasa peluang untuk mengenal pasti komponen penghantaran diskret untuk pelanggan. Keputusan yang melingkungi jumlah projek sebenar yang digunakan untuk menyampaikan komponen ini boleh ditolak keluar sehingga lebih banyak maklumat diketahui tentang kerja itu sendiri.

Di bawah ialah medan pada baris peluang berdasarkan projek:

| **Medan** | **Lokasi** | **Perihalan** | **Kesan hiliran** |
| --- | --- | --- | --- |
| Jenis Produk | Tab umum (tersembunyi) | Anda boleh memilih satu daripada pilihan yang berikut:</br>- Perkhidmatan berasaskan projek (hanya tersedia apabila Dynamics 365 Project Operations dipasang)</br>- Produk (tersedia hanya apabila Project Operations dan Dynamics 365 Sales dipasang) | Nilai medan ini ditetapkan kepada **Peluang berdasarkan projek** apabila anda mencipta baris peluang berdasarkan projek daripada grid baris berdasarkan projek pada Peluang. <br> Jika anda mengubah atau menulis ganti nilai ini, kefungsian projek tidak akan didayakan pada item baris berdasarkan projek anda. |
| Peluang | Tab umum | Medan ini ialah baca sahaja dan rujukan rekod Peluang induk yang item baris ini digolongkan. | Tiada kesan hiliran daripada medan ini. |
| Nama | Tab umum | Medan teks boleh diedit ini boleh digunakan untuk memberikan identiti ringkas kepada item baris. | Nilai ini dibawa ke dalam baris sebut harga apabila anda mencipta sebut harga daripada peluang ini. |
| Belanjawan Pelanggan | Tab umum | Medan mata wang boleh diedit ini boleh digunakan untuk menjejaki amaun yang pelanggan sanggup belanja untuk item baris ini. | Nilai ini dibawa ke dalam medan yang sepadan pada baris sebut harga apabila anda mencipta sebut harga daripada peluang ini. |
| Kaedah Pengebilan | Tab umum | Medan boleh diedit ini mempunyai nilai yang berikut:</br>- Masa dan Bahan</br>- Harga Tetap | Nilai ini dibawa ke dalam medan yang sepadan pada baris sebut harga apabila anda mencipta sebut harga daripada peluang ini. Selepas baris sebut harga dicipta, medan dikunci dan tidak boleh diubah. Peruntukkan nilai medan ini setepat yang mungkin. Jika anda perlu mengubah nilai medan ini pada baris sebut harga, padamkan dan cipta semula baris sebut harga. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]