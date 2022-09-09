---
title: Tentukan kadar kos untuk anggaran projek dan sebenar
description: Artikel ini menyediakan maklumat tentang cara kadar kos untuk anggaran projek dan sebenar ditentukan.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c7dd264ebbd1da9b2f42d2284fb38988a09aa03f
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410161"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Tentukan kadar kos untuk anggaran projek dan sebenar

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Untuk menentukan senarai harga kos dan kadar kos dalam anggaran dan konteks sebenar, sistem menggunakan maklumat dalam **medan Tarikh**, **Mata Wang**, dan **Unit** Kontrak projek yang berkaitan.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Menentukan kadar kos dalam anggaran dan konteks sebenar untuk Masa

Konteks anggaran untuk **Masa** merujuk kepada:

- Petikan butiran baris untuk **Masa**.
- Butiran talian kontrak untuk **Masa**.
- Tugasan sumber pada projek.

Konteks sebenar untuk **Masa** merujuk kepada:

- Baris jurnal Kemasukan dan Pembetulan untuk **Masa**.
- Baris jurnal yang dicipta apabila entri masa dihantar.

Selepas senarai harga kos ditentukan, sistem melengkapkan langkah-langkah berikut untuk memasukkan kadar kos lalai.

1. Sistem ini sepadan dengan gabungan **medan Unit** Peranan **dan** Resourcing dalam anggaran atau konteks sebenar untuk **Masa** terhadap garis harga peranan pada senarai harga. Padanan ini menganggap bahawa anda menggunakan dimensi harga standard untuk kos buruh. Jika anda telah mengkonfigurasikan sistem untuk memadankan medan selain daripada atau sebagai tambahan kepada **Unit** Peranan **dan** Resourcing, gabungan yang berbeza digunakan untuk mendapatkan semula garis harga peranan yang sepadan.
1. Jika sistem menemui garis harga peranan yang mempunyai kadar kos untuk **gabungan Unit** Peranan **dan** Resourcing, kadar kos tersebut digunakan sebagai kadar kos lalai.
1. Jika sistem tidak dapat memadankan **nilai Unit** Peranan **dan** Resourcing, ia mengambil garis harga peranan yang mempunyai nilai padanan untuk **medan Peranan** tetapi nilai nol untuk **medan Unit** Resourcing. Selepas sistem mempunyai rekod harga peranan yang sepadan, kadar kos dari rekod itu akan digunakan sebagai kadar kos lalai.

> [!NOTE]
> Jika anda mengkonfigurasi keutamaan yang berbeza bagi **medan Unit** Peranan **dan** Resourcing, atau jika anda mempunyai dimensi lain yang mempunyai keutamaan yang lebih tinggi, kelakuan sebelumnya akan berubah dengan sewajarnya. Sistem ini mengambil rekod harga peranan yang mempunyai nilai yang sepadan dengan setiap nilai dimensi harga mengikut keutamaan. Baris yang mempunyai nilai nol untuk dimensi tersebut menjadi terakhir.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Menentukan kadar kos pada baris sebenar dan anggaran untuk Perbelanjaan

Konteks anggaran perbelanjaan **merujuk** kepada:

- Sebut harga butiran baris untuk **Perbelanjaan**.
- Butiran talian kontrak untuk **Perbelanjaan**.
- Anggaran perbelanjaan pada projek.

Konteks sebenar Perbelanjaan **merujuk** kepada:

- Baris jurnal Kemasukan dan Pembetulan untuk **Perbelanjaan**.
- Baris jurnal yang dicipta apabila kemasukan perbelanjaan dikemukakan.

Selepas senarai harga kos ditentukan, sistem melengkapkan langkah-langkah berikut untuk memasukkan kadar kos lalai.

1. Sistem ini sepadan dengan gabungan **medan Kategori** dan **Unit** dalam anggaran atau konteks sebenar untuk **Perbelanjaan** terhadap garis harga kategori pada senarai harga.
1. Jika sistem menemui garis harga kategori yang mempunyai kadar kos untuk **gabungan Kategori** dan **Unit**, kadar kos tersebut digunakan sebagai kadar kos lalai.
1. Jika sistem tidak dapat memadankan **nilai Kategori** dan **Unit**, harga disetkan kepada **0** (sifar) secara lalai.
1. Dalam konteks anggaran, jika sistem dapat mencari garis harga kategori yang sepadan, tetapi kaedah harga adalah sesuatu yang selain daripada **Harga Seunit**, kadar kos ditetapkan kepada **0** (sifar) secara lalai.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Menentukan kadar kos pada baris sebenar dan anggaran untuk Bahan

Konteks anggaran bahan **merujuk** kepada:

- Butiran baris sebut harga untuk **Bahan**.
- Butiran talian kontrak untuk **Bahan**.
- Anggaran bahan pada projek.

Konteks sebenar Bahan **merujuk** kepada:

- Baris jurnal Kemasukan dan Pembetulan untuk **Bahan**.
- Baris jurnal yang dicipta apabila log penggunaan Bahan diserahkan.

Selepas senarai harga kos ditentukan, sistem melengkapkan langkah-langkah berikut untuk memasukkan kadar kos lalai.

1. Sistem ini menggunakan gabungan **medan Produk** dan **Unit** dalam anggaran atau konteks sebenar untuk **Bahan** terhadap baris item senarai harga pada senarai harga.
1. Jika sistem menemui item senarai harga yang mempunyai kadar kos untuk **gabungan Produk** dan **Unit**, kadar kos tersebut digunakan sebagai kadar kos lalai.
1. Jika sistem tidak dapat memadankan **nilai Produk** dan **Unit**, kos unit disetkan kepada **0** (sifar) secara lalai.
1. Dalam anggaran atau konteks sebenar, jika sistem dapat mencari baris item senarai harga yang sepadan, tetapi kaedah harga adalah sesuatu yang lain daripada **jumlah** Mata Wang, kos unit ditetapkan kepada **0** secara lalai. Tingkah laku ini berlaku kerana Operasi Projek hanya **menyokong kaedah harga jumlah** Mata Wang untuk bahan yang digunakan pada projek.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
