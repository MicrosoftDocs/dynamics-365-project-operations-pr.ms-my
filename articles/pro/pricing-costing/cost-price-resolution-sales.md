---
title: Tentukan kadar kos untuk anggaran dan aktual projek
description: Artikel ini memberikan maklumat tentang cara kadar kos untuk anggaran dan aktual projek ditentukan.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c2295174df1ce766c6d1304f4e9c55d32d5c4775
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475243"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Tentukan kadar kos untuk anggaran dan aktual projek

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Untuk menentukan kadar kos bagi anggaran dan aktual dalam Microsoft Dynamics 365 Project Operations, sistem menggunakan tarikh dan mata wang dalam konteks anggaran atau aktual akan datang terlebih dahulu untuk menentukan senarai harga kos. Dalam konteks aktual khususnya, sistem menggunakan medan **Tarikh transaksi** untuk menentukan senarai harga yang boleh digunakan. Nilai **Tarikh transaksi** bagi anggaran atau aktual akan datang dibandingkan dengan nilai **Mula Berkuat Kuasa (Bebas zon waktu)** dan **Tamat Berkuat Kuasa (Bebas zon waktu)** pada senarai harga. Selepas senarai harga kos ditentukan, sistem menentukan kadar kos. 

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Menentukan kadar kos dalam konteks anggaran dan aktual untuk Masa

Konteks anggaran untuk **Masa** merujuk kepada:

- Butiran baris sebut harga untuk **Masa**.
- Butiran baris kontrak untuk **Masa**.
- Penugasan sumber pada projek.

Konteks aktual untuk **Masa** merujuk kepada:

- Garisan jurnal Entri dan Pembetulan untuk **Masa**.
- Garisan jurnal yang dicipta apabila entri masa diserahkan.

Setelah senarai harga kos ditentukan, sistem melengkapkan langkah-langkah berikut untuk memasukkan kadar kos lalai.

1. Sistem memadankan kombinasi medan **Peranan** dan **Unit Penyumberan** dalam konteks anggaran atau aktual untuk **Masa** dengan baris harga peranan pada senarai harga. Pemadanan ini menganggap anda menggunakan dimensi penetapan harga standard untuk kos buruh. Jika anda telah mengkonfigurasikan sistem untuk sepadan dengan medan selain daripada atau sebagai tambahan kepada **Peranan** dan **Unit Penyumberan**, kombinasi berbeza digunakan untuk mendapatkan baris harga peranan yang berpadanan.
1. Jika sistem menemukan baris harga peranan yang mempunyai kadar kos untuk kombinasi **Peranan** dan **Unit Penyumberan**, kadar kos itu digunakan sebagai nilai kadar kos lalai.
1. Jika sistem tidak dapat memadankan nilai **Peranan** dan **Unit Penyumberan**, maka ia akan mendapatkan baris harga peranan yang mempunyai nilai yang sepadan untuk medan **Peranan** tetapi nilai nol untuk medan **Unit Penyumberan**. Setelah sistem mempunyai rekod harga peranan yang sepadan, kadar kos daripada rekod tersebut akan digunakan sebagai kadar kos lalai.

> [!NOTE]
> Jika anda mengkonfigurasi keutamaan yang berbeza bagi medan **Peranan** dan **Unit Penyumberan** atau jika anda mempunyai dimensi lain yang mempunyai keutamaan lebih tinggi, tingkah laku sebelumnya akan berubah sewajarnya. Sistem mendapatkan rekod harga peranan yang mempunyai nilai yang sepadan dengan nilai dimensi penetapan harga mengikut keutamaan. Rekod dengan baris yang mempunyai nilai nol bagi dimensi akan didapatkan terakhir.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Menentukan kadar kos pada baris anggaran dan aktual untuk Perbelanjaan

Konteks anggaran untuk **Perbelanjaan** merujuk kepada:

- Butiran baris sebut harga untuk **Perbelanjaan**.
- Butiran baris kontrak harga untuk **Perbelanjaan**.
- Anggaran perbelanjaan pada projek.

Konteks aktual untuk **Perbelanjaan** merujuk kepada:

- Garisan jurnal Entri dan Pembetulan untuk **Perbelanjaan**.
- Garisan jurnal yang dicipta apabila entri perbelanjaan diserahkan.

Setelah senarai harga kos ditentukan, sistem melengkapkan langkah-langkah berikut untuk memasukkan kadar kos lalai.

1. Sistem memadankan kombinasi medan **Kategori** dan **Unit** dalam konteks anggaran atau aktual untuk **Perbelanjaan** dengan baris harga kategori pada senarai harga.
1. Jika sistem mencari baris harga kategori yang mempunyai kadar kos untuk kombinasi **Kategori** dan **Unit**, kadar kos tersebut digunakan sebagai kadar kos lalai.
1. Jika sistem tidak dapat memadankan nilai **Kategori** dan **Unit**, harga ditetapkan kepada **0** (sifar) secara lalai.
1. Dalam konteks anggaran, jika sistem tidak dapat menemukan baris harga kategori yang sepadan, tetapi kaedah penetapan harga bukan **Harga Setiap Unit**, kadar kos ditetapkan kepada **0** (sifar) secara lalai.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Menentukan kadar kos pada baris aktual dan anggaran untuk Bahan

Konteks anggaran untuk **Bahan** merujuk kepada:

- Butiran baris sebut harga untuk **Bahan**.
- Butiran baris kontrak harga untuk **Bahan**.
- Anggaran bahan pada projek.

Konteks aktual untuk **Bahan** merujuk kepada:

- Garisan jurnal Entri dan Pembetulan untuk **Bahan**.
- Garisan jurnal yang dicipta apabila log penggunaan Bahan diserahkan.

Setelah senarai harga kos ditentukan, sistem melengkapkan langkah-langkah berikut untuk memasukkan kadar kos lalai.

1. Sistem menggunakan kombinasi medan **Produk** dan **Unit** dalam konteks anggaran atau aktual untuk **Bahan** berbanding baris item senarai harga pada senarai harga.
1. Jika sistem menemukan baris item senarai harga yang mempunyai kadar kos untuk kombinasi **Produk** dan **Unit**, kadar kos tersebut digunakan sebagai kadar kos lalai.
1. Jika sistem tidak dapat memadankan nilai **Produk** dan **Unit**, kos unit ditetapkan kepada **0** (sifar) secara lalai.
1. Dalam konteks anggaran atau aktual, jika sistem tidak dapat menemukan baris item senarai harga yang sepadan, tetapi kaedah penetapan harga bukan **Amaun mata wang**, kos unit ditetapkan kepada **0** secara lalai. Tingkah laku ini berlaku kerana Project Operations hanya menyokong kaedah penetapan harga **Amaun mata wang** untuk bahan yang digunakan pada projek.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
