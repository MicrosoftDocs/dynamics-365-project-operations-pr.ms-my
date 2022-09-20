---
title: Tentukan harga jualan untuk anggaran berasaskan projek dan sebenar
description: Artikel ini menyediakan maklumat tentang cara harga jualan untuk anggaran berasaskan projek dan sebenar ditentukan.
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
#  <a name="determine-sales-prices-for-project-based-estimates-and-actuals"></a>Tentukan harga jualan untuk anggaran berasaskan projek dan sebenar

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Untuk menentukan harga jualan pada anggaran dan sebenar dalam Microsoft Dynamics 365 Project Operations, sistem mula-mula menggunakan tarikh dan mata wang dalam anggaran masuk atau konteks sebenar untuk menentukan senarai harga jualan. Dalam konteks sebenar secara khusus, sistem menggunakan **medan Tarikh** Transaksi untuk menentukan senarai harga yang boleh digunakan. Nilai **tarikh** Transaksi bagi anggaran masuk atau sebenar dibandingkan dengan **nilai Effective Start (Timezone independent)** dan **Effective End (Timezone independent)** pada senarai harga. Selepas senarai harga jualan ditentukan, sistem menentukan kadar jualan atau bil.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Menentukan kadar jualan pada baris sebenar dan anggaran untuk Masa

Konteks anggaran untuk **Masa** merujuk kepada:

- Petikan butiran baris untuk **Masa**.
- Butiran talian kontrak untuk **Masa**.
- Tugasan sumber pada projek.

Konteks sebenar untuk **Masa** merujuk kepada:

- Baris jurnal Kemasukan dan Pembetulan untuk **Masa**.
- Baris jurnal yang dicipta apabila entri masa dihantar.
- Butiran baris invois untuk **Masa**. 

Selepas senarai harga untuk jualan ditentukan, sistem melengkapkan langkah-langkah berikut untuk memasukkan kadar bil lalai.

1. Sistem ini sepadan dengan gabungan **medan Peranan**, **Syarikat** Resourcing, dan **Unit** Resourcing dalam anggaran atau konteks sebenar untuk **Masa** terhadap garis harga peranan dalam senarai harga. Padanan ini menganggap bahawa anda menggunakan dimensi harga luar kotak untuk kadar bil. Jika anda telah mengkonfigurasikan harga supaya ia berdasarkan medan selain daripada atau sebagai tambahan kepada **Peranan**, **Syarikat** Resourcing dan **Unit** Resourcing, gabungan medan tersebut digunakan untuk mendapatkan garis harga peranan yang sepadan.
1. Jika sistem menemui garis harga peranan yang mempunyai kadar bil untuk **Gabungan Peranan**, **Syarikat** Resourcing dan **Unit** Resourcing, kadar bil tersebut digunakan sebagai kadar bil lalai.

> [!NOTE]
> Jika anda mengkonfigurasi keutamaan yang berbeza bagi **medan Peranan**, **Syarikat** Resourcing dan **Unit** Resourcing, atau jika anda mempunyai dimensi lain yang mempunyai keutamaan yang lebih tinggi, tingkah laku sebelumnya akan berubah dengan sewajarnya. Sistem ini mengambil rekod harga peranan yang mempunyai nilai yang sepadan dengan setiap nilai dimensi harga mengikut keutamaan. Baris yang mempunyai nilai nol untuk dimensi tersebut menjadi terakhir.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Menentukan kadar jualan pada baris sebenar dan anggaran untuk Perbelanjaan

Konteks anggaran perbelanjaan **merujuk** kepada:

- Sebut harga butiran baris untuk **Perbelanjaan**.
- Butiran talian kontrak untuk **Perbelanjaan**.
- Garis anggaran perbelanjaan pada projek.

Konteks sebenar Perbelanjaan **merujuk** kepada:

- Baris jurnal Kemasukan dan Pembetulan untuk **Perbelanjaan**.
- Baris jurnal yang dicipta apabila kemasukan perbelanjaan dikemukakan.
- Butiran baris invois untuk **Perbelanjaan**. 

Selepas senarai harga untuk jualan ditentukan, sistem melengkapkan langkah-langkah berikut untuk memasukkan harga jualan unit lalai.

1. Sistem ini sepadan dengan gabungan **medan Kategori** dan **Unit** pada baris anggaran perbelanjaan **terhadap** garis harga kategori pada senarai harga.
1. Jika sistem menemui garis harga kategori yang mempunyai kadar jualan untuk **gabungan Kategori** dan **Unit**, kadar jualan tersebut digunakan sebagai kadar jualan lalai.
1. Jika sistem menemui garis harga kategori yang sepadan, kaedah harga mungkin digunakan untuk memasukkan harga jualan lalai. Jadual berikut menunjukkan kelakuan lalai bagi harga perbelanjaan dalam Operasi Projek.

    | Konteks | Kaedah penetapan harga | Harga lalai |
    | --- | --- | --- |
    | Anggaran | Harga seunit | Berdasarkan garis harga kategori. |
    |        | Pada kos | 0.00 |
    |        | Tokokan terhadap kos | 0.00 |
    | Aktual | Harga seunit | Berdasarkan garis harga kategori. |
    |        | Pada kos | Berdasarkan kos yang berkaitan sebenar. |
    |        | Tokokan terhadap kos | Markup digunakan, seperti yang ditakrifkan oleh garis harga kategori, kepada kadar kos unit bagi kos sebenar yang berkaitan. |

1. Jika sistem tidak dapat memadankan **nilai Kategori** dan **Unit**, kadar jualan disetkan kepada **0** (sifar) secara lalai.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Menentukan kadar jualan pada baris sebenar dan anggaran untuk Bahan

Konteks anggaran bahan **merujuk** kepada:

- Butiran baris sebut harga untuk **Bahan**.
- Butiran talian kontrak untuk **Bahan**.
- Garis anggaran bahan pada projek.

Konteks sebenar Bahan **merujuk** kepada:

- Baris jurnal Kemasukan dan Pembetulan untuk **Bahan**.
- Baris jurnal yang dicipta apabila log penggunaan Bahan diserahkan.
- Butiran baris invois untuk **Bahan**. 

Selepas senarai harga untuk jualan ditentukan, sistem melengkapkan langkah-langkah berikut untuk memasukkan harga jualan unit lalai.

1. Sistem ini sepadan dengan gabungan **medan Produk** dan **Unit** pada baris anggaran bahan **terhadap** baris item senarai harga pada senarai harga.
1. Jika sistem menemui baris item senarai harga yang mempunyai kadar jualan untuk **gabungan Produk** dan **Unit**, dan jika kaedah harga adalah **jumlah** Mata Wang, harga jualan yang dinyatakan pada baris senarai harga digunakan. 
1. **Jika nilai medan Produk** dan **Unit** tidak sepadan atau jika kaedah harga adalah sesuatu yang selain daripada **jumlah** Mata Wang, kadar jualan ditetapkan kepada **0** (sifar) secara lalai. Tingkah laku ini berlaku kerana Operasi Projek hanya **menyokong kaedah harga jumlah** Mata Wang untuk bahan yang digunakan pada projek.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
