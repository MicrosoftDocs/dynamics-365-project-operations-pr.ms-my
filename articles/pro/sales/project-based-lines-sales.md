---
title: Baris peluang berdasarkan projek (Pro)
description: Topik ini memberikan maklumat tentang baris peluang berdasarkan projek. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a688b9bed5a38e7b5947cbcee1e3cb8ab211e98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896382"
---
# <a name="project-based-opportunity-lines-pro"></a>Baris peluang berdasarkan projek (Pro)

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Baris peluang berdasarkan projek hanya tersedia dalam peluang berdasarkan projek. Rekod peluang berdasarkan projek mempunyai nilai medan **Jenis** ditetapkan kepada **Berdasarkan kerja**.

Baris peluang berdasarkan projek ialah item baris yang akan disampaikan kepada pelanggan menggunakan projek. Walau bagaimanapun, projek tidak boleh terikat kepada baris peluang berdasarkan projek. Projek boleh diikat kepada item baris daripada peringkat **Sebut Harga** dan ke hadapan kerana biasanya peluang berlaku di peringkat awal dalam kitaran hayat urus niaga. Penentuan jumlah projek yang akan digunakan untuk menyampaikan kerja untuk pelanggan ialah keputusan yang dibuat kemudian dalam fasa jualan. Anda boleh menggunakan fasa peluang untuk mengenal pasti komponen penghantaran diskret untuk pelanggan. Keputusan yang melingkungi jumlah projek sebenar yang digunakan untuk menyampaikan komponen ini boleh ditolak keluar sehingga lebih banyak maklumat diketahui tentang kerja itu sendiri.

Di bawah ialah medan pada baris peluang berdasarkan projek:

| **Medan** | **Lokasi** | **Keterkaitan, tujuan dan panduan** | **Kesan hiliran** |
| --- | --- | --- | --- |
| Jenis Produk | Tab umum (tersembunyi) | Anda boleh memilih satu daripada pilihan yang berikut:</br>- Perkhidmatan berdasarkan projek (tersedia hanya apabila Dynamics 365 Project Operations dipasang)</br>- Produk (tersedia hanya apabila Project Operations dan Dynamics 365 Sales dipasang) | Nilai medan ini ditetapkan kepada **Peluang berdasarkan projek** apabila anda mencipta baris peluang berdasarkan projek daripada grid baris berdasarkan projek pada Peluang. <br> Jika anda mengubah atau menulis ganti nilai ini, kefungsian projek tidak akan didayakan pada item baris berdasarkan projek anda. |
| Peluang | Tab umum | Medan ini ialah baca sahaja dan rujukan rekod Peluang induk yang item baris ini digolongkan. | Tiada kesan hiliran daripada medan ini. |
| Nama | Tab umum | Medan teks boleh diedit ini boleh digunakan untuk memberikan identiti ringkas kepada item baris. | Nilai ini dibawa ke dalam baris sebut harga apabila anda mencipta sebut harga daripada peluang ini. |
| Belanjawan Pelanggan | Tab umum | Medan mata wang boleh diedit ini boleh digunakan untuk menjejaki amaun yang pelanggan sanggup belanja untuk item baris ini. | Nilai ini dibawa ke dalam medan yang sepadan pada baris sebut harga apabila anda mencipta sebut harga daripada peluang ini. |
| Kaedah Pengebilan | Tab umum | Medan boleh diedit ini mempunyai nilai yang berikut:</br>- Masa dan Bahan</br>- Harga Tetap | Nilai ini dibawa ke dalam medan yang sepadan pada baris sebut harga apabila anda mencipta sebut harga daripada peluang ini. Selepas baris sebut harga dicipta, medan dikunci dan tidak boleh diubah. Peruntukkan nilai medan ini setepat yang mungkin. Jika anda perlu mengubah nilai medan ini pada baris sebut harga, padamkan dan cipta semula baris sebut harga. |
