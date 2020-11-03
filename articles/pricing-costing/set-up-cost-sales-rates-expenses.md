---
title: Sediakan kadar kos dan jualan untuk perbelanjaan
description: Topik ini memberikan maklumat tentang cara menetapkan kadar kos dan jualan untuk kategori transaksi dan perbelanjaan.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e5a2402a2c1059ff11dbe1a331a028da77958235
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081147"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Sediakan kadar kos dan jualan untuk perbelanjaan

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Anda boleh menetapkan kos dan harga jualan untuk kategori transaksi dalam Dynamics 365 Project Operations. Oleh kerana kos dan harga jualan direka untuk Perbelanjaan, setiap kategori transaksi yang merangkumi kos ini, mesti turut ditetapkan sebagai kategori perbelanjaan. Persediaan ini memastikan ketepatan dalam fungsi hiliran. Kos dan harga jualan untuk kategori transaksi hanya boleh disenaraikan dalam satu mata wang, yang mesti menjadi mata wang pada pengepala senarai harga.

Untuk menyediakan kadar kos dan jualan untuk kategori transaksi, lengkapkan langkah-langkah berikut. 

1. Cipta senarai harga berdasarkan pengepala senarai harga. 
2. Pada **Harga Kategori** , pada menu sub grid, pilih **+ Harga Kategori Baharu**. 
3. Pada halaman **Cipta Pantas** , masukkan kategori transaksi dan unit untuk harga baharu yang anda cipta.

Jadual berikut menyenaraikan medan pada tab **Umum** dan halaman **Cipta Pantas** bagi baris harga kategori yang perlu diingati apabila anda mencipta harga kategori pada senarai harga jualan atau kos.

| Medan | Lokasi | Keterkaitan, tujuan dan panduan | Kesan hiliran |
| --- | --- | --- | --- |
| Kategori Transaksi | Tab **Umum** dan halaman **Cipta Pantas** | Pilih kategori transaksi untuk harga jualan atau kos yang anda cipta. | Kategori transaksi pada anggaran atau sebenar yang masuk untuk Perbelanjaan akan dipadankan dengan baris ini untuk menetapkan kadar kos atau jualan lalai bagi kategori transaksi. |
| Jadual Unit | Tab **Umum** dan halaman **Cipta Pantas** | Jadual unit lalai daripada jadual unit bagi kategori transaksi. | Tiada kesan hiliran daripada medan ini. |
| Unit | Tab **Umum** dan halaman **Cipta Pantas** | Pilih unit yang kadarnya sedang disediakan. | Unit pada anggaran atau sebenar yang masuk dipadankan dengan unit pada baris ini untuk menetapkan kadar lalai pada anggaran atau sebenar perbelanjaan. |
| Kaedah Penetapan Harga | Tab **Umum** dan halaman **Cipta Pantas** | Nilai yang mungkin bagi medan **Kaedah Penetapan Harga** ialah, **Harga Setiap Unit** , **Pada Kos** dan **Tokokan Terhadap Kos**. | Semasa penyediaan harga, memilih **Harga Setiap Unit** mengunci medan **Peratus** pada baris harga kategori. Jika **Pada kos** dipilih, medan **Harga** dan **Peratus** dikunci pada senarai harga jualan. Memilih **Tokokan Terhadap Kos** mengunci medan **Harga** pada senarai harga jualan. Pada baris sebenar masuk untuk perbelanjaan, kaedah penetapan harga **Pada kos** atau **Tokokan Terhadap Kos** menyebabkan baris jualan tidak dibilkan yang berkenaan diberikan harga yang sama dengan harga pada kos sebenar atau dikira sebagai tokokan terhadap harga. |
| Harga | Tab **Umum** dan halaman **Cipta Pantas** | Sediakan kadar setiap unit untuk kategori transaksi dan gabungan unit. Contohnya, kadar untuk perbatuan ialah 10 USD setiap batu dan 8 USD setiap Kilometer. | Kadar perbatuan akan menjadi kadar lalai pada harga atau kos setiap unit baris anggaran atau sebenar yang masuk untuk kelas transaksi perbelanjaan.|
| Peratusan | Tab **Umum** dan halaman **Cipta Pantas** | Sediakan peratus terhadap kos untuk kategori transaksi dan gabungan unit. Contohnya, kadar jualan tambang penerbangan hendaklah ditokok 10 peratus terhadap kos perbelanjaan tambang penerbangan yang ditanggung. | Peratus terhadap kos ini hanya digunakan pada senarai harga jualan apabila kaedah penetapan harga yang dipilih ialah **Tokokan Terhadap Kos**. |
| Mata wang | Tab **Umum** dan halaman **Cipta Pantas** | Secara lalai, nilai ini diperoleh daripada mata wang pada pengepala senarai harga. Untuk penetapan harga kategori transaksi, mata wang tidak boleh ditulis ganti. | Mata wang ini lalai pada harga setiap unit bagi baris masuk sebenar untuk kelas transaksi perbelanjaan kos dan jualan. |

## <a name="pricing-methods-for-expenses"></a>Kaedah penetapan harga untuk perbelanjaan

Apabila anda menyediakan harga kategori yang hanya relevan dalam konteks penetapan harga perbelanjaan, anda boleh menggunakan salah satu daripada tiga kaedah penetapan harga berikut:

- **Harga seunit**
- **Pada kos**
- **Tokokan terhadap kos**

### <a name="price-per-unit"></a>Harga seunit
Apabila kaedah penetapan harga ini dipilih pada baris harga kategori yang dikaitkan dengan senarai harga jualan, harga lalai untuk kategori dan gabungan unit dalam kedua-dua anggaran dan sebenar. Anggaran merujuk kepada baris anggaran projek untuk perbelanjaan, butiran baris sebut harga dan butiran baris kontrak untuk perbelanjaan.

### <a name="at-cost"></a>Pada kos
Apabila kaedah penetapan harga ini dipilih pada baris harga kategori yang dikaitkan dengan senarai harga jualan, harga lalai untuk kategori dan gabungan unit hanya untuk perbelanjaan sebenar. Contohnya, jualan sebenar yang tidak dibilkan untuk kelas transaksi perbelanjaan. Harga unit ditetapkan pada jualan sebenar yang tidak dibilkan daripada harga unit pada kos sebenar untuk perbelanjaan tersebut. Harga ditetapkan lalai berdasarkan kos yang belum selesai pada anggaran projek untuk perbelanjaan atau butiran baris sebut harga dan baris kontrak untuk perbelanjaan.

### <a name="markup-over-cost"></a>Tokokan terhadap kos
Apabila kaedah penetapan harga ini dipilih pada baris harga kategori yang dikaitkan dengan senarai harga jualan, harga lalai untuk kategori dan gabungan unit hanya untuk perbelanjaan sebenar. Contohnya, jualan sebenar yang tidak dibilkan untuk kelas transaksi perbelanjaan. Harga unit ini ditetapkan pada jualan sebenar yang tidak dibilkan kepada nilai yang dikira daripada harga unit pada kos sebenar untuk perbelanjaan itu selepas peratus tokokan yang ditakrifkan tersebut digunakan. Harga ditetapkan lalai berdasarkan kos yang belum selesai pada anggaran projek untuk perbelanjaan atau butiran baris sebut harga dan baris kontrak untuk perbelanjaan.
