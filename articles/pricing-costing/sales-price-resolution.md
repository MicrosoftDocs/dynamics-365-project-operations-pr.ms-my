---
title: Tentukan harga jualan untuk anggaran berdasarkan dan aktual
description: Artikel ini memberikan maklumat tentang cara harga jualan untuk anggaran dan aktual berasaskan projek ditentukan.
author: rumant
ms.date: 09/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f0b95c651983230cbf340f2c06089a287b2c8a10
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475381"
---
#  <a name="determine-sales-prices-for-project-based-estimates-and-actuals"></a>Tentukan harga jualan untuk anggaran berdasarkan dan aktual

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Untuk menentukan harga jualan bagi anggaran dan aktual dalam Microsoft Dynamics 365 Project Operations, sistem menggunakan tarikh dan mata wang dalam konteks anggaran atau aktual akan datang terlebih dahulu untuk menentukan senarai harga jualan. Dalam konteks aktual khususnya, sistem menggunakan medan **Tarikh transaksi** untuk menentukan senarai harga yang boleh digunakan. Nilai **Tarikh transaksi** bagi anggaran atau aktual akan datang dibandingkan dengan nilai **Mula Berkuat Kuasa (Bebas zon waktu)** dan **Tamat Berkuat Kuasa (Bebas zon waktu)** pada senarai harga. Setelah senarai harga jualan ditentukan, sistem menentukan kadar jualan atau bil.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Menentukan kadar jualan pada baris aktual dan anggaran untuk Masa

Konteks anggaran untuk **Masa** merujuk kepada:

- Butiran baris sebut harga untuk **Masa**.
- Butiran baris kontrak untuk **Masa**.
- Penugasan sumber pada projek.

Konteks aktual untuk **Masa** merujuk kepada:

- Garisan jurnal Entri dan Pembetulan untuk **Masa**.
- Garisan jurnal yang dicipta apabila entri masa diserahkan.
- Butiran baris invois untuk **Masa**. 

Setelah senarai harga untuk jualan ditentukan, sistem melengkapkan langkah-langkah berikut untuk memasukkan kadar bil lalai.

1. Sistem memadankan kombinasi medan **Peranan** dan **Syarikat Sumber** dan **Unit Sumber** dalam konteks anggaran atau aktual untuk **Masa** dengan baris harga peranan pada senarai harga. Pemadanan ini menganggap bahawa anda menggunakan dimensi harga luar kotak untuk kadar bil. Jika anda mengkonfigurasi penetapan harga supaya berdasarkan medan selain atau sebagai tambahan kepada **Peranan**, **Syarikat Sumber** dan **Unit Sumber**, maka gabungan medan akan digunakan untuk mendapatkan baris harga peranan yang sepadan.
1. Jika sistem mendapati baris harga peranan yang mempunyai kadar bil untuk gabungan medan **Peranan**, **Syarikat Sumber** dan **Unit Sumber**, maka kadar bil digunakan sebagai kadar bil lalai.

> [!NOTE]
> Jika anda mengkonfigurasikan keutamaan yang berbeza bagi medan **Peranan**, **Syarikat Sumber** dan **Unit Sumber** atau jika anda mempunyai dimensi lain yang mempunyai keutamaan lebih tinggi, tingkah laku sebelumnya akan berubah sewajarnya. Sistem mendapatkan rekod harga peranan yang mempunyai nilai yang sepadan dengan nilai dimensi penetapan harga mengikut keutamaan. Rekod dengan baris yang mempunyai nilai nol bagi dimensi akan didapatkan terakhir.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Menentukan kadar jualan pada baris sebenar dan anggaran untuk Perbelanjaan

Konteks anggaran untuk **Perbelanjaan** merujuk kepada:

- Butiran baris sebut harga untuk **Perbelanjaan**.
- Butiran baris kontrak harga untuk **Perbelanjaan**.
- Baris anggaran perbelanjaan pada projek.

Konteks aktual untuk **Perbelanjaan** merujuk kepada:

- Garisan jurnal Entri dan Pembetulan untuk **Perbelanjaan**.
- Garisan jurnal yang dicipta apabila entri perbelanjaan diserahkan.
- Butiran baris invois untuk **Perbelanjaan**. 

Setelah senarai harga untuk jualan ditentukan, sistem melengkapkan langkah-langkah berikut untuk memasukkan harga jualan unit lalai.

1. Sistem memadankan gabungan medan **Kategori** dan **Unit** pada baris anggaran bagi **Perbelanjaan** terhadap baris harga kategori dalam senarai harga.
1. Jika sistem mendapati baris harga kategori yang mempunyai kadar jualan untuk gabungan medan **Kategori** dan **Unit**, maka kadar jualan tersebut digunakan sebagai kadar jualan lalai.
1. Jika sistem mendapati baris harga kategori yang sepadan, kaedah penetapan harga boleh digunakan untuk memasukkan harga jualan lalai. Jadual menunjukkan kelakuan penetapan lalai untuk harga perbelanjaan dalam Project Operations.

    | Konteks | Kaedah penetapan harga | Harga lalai |
    | --- | --- | --- |
    | Anggaran | Harga seunit | Berdasarkan baris harga kategori. |
    |        | Pada kos | 0.00 |
    |        | Tokokan terhadap kos | 0.00 |
    | Aktual | Harga seunit | Berdasarkan baris harga kategori. |
    |        | Pada kos | Berdasarkan kos sebenar yang berkaitan. |
    |        | Tokokan terhadap kos | Tokokan digunakan, seperti yang ditakrifkan oleh baris harga kategori pada kadar kos unit bagi aktual kos yang berkaitan. |

1. Jika sistem tidak dapat memadankan nilai **Kategori** dan **Unit**, kadar jualan ditetapkan kepada **0** (sifar) secara lalai.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Menentukan kadar jualan pada baris aktual dan anggaran untuk Bahan

Konteks anggaran untuk **Bahan** merujuk kepada:

- Butiran baris sebut harga untuk **Bahan**.
- Butiran baris kontrak harga untuk **Bahan**.
- Baris anggaran bahan pada projek.

Konteks aktual untuk **Bahan** merujuk kepada:

- Garisan jurnal Entri dan Pembetulan untuk **Bahan**.
- Garisan jurnal yang dicipta apabila log penggunaan Bahan diserahkan.
- Butiran baris invois untuk **Bahan**. 

Setelah senarai harga untuk jualan ditentukan, sistem melengkapkan langkah-langkah berikut untuk memasukkan harga jualan unit lalai.

1. Sistem memadankan gabungan medan **Produk** dan **Unit** pada baris anggaran bagi **Bahan** terhadap baris item senarai harga pada senarai harga.
1. Jika sistem mendapati baris item senarai harga yang mempunyai kadar jualan untuk gabungan **Produk** dan **Unit**, serta jika kaedah penetapan harga ialah **Amaun mata wang**, harga jualan yang ditentukan pada baris senarai harga digunakan. 
1. Jika nilai medan **Produk** dan **Unit** tidak sepadan, atau jika kaedah penetapan harga merupakan sesuatu selain **Amaun mata wang**, kadar jualan ditetapkan kepada **0** (sifar) secara lalai. Tingkah laku ini berlaku kerana Project Operations hanya menyokong kaedah penetapan harga **Amaun mata wang** untuk bahan yang digunakan pada projek.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
