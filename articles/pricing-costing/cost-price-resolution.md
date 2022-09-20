---
title: Tentukan kadar kos untuk anggaran berasaskan projek dan sebenar
description: Artikel ini menyediakan maklumat tentang cara kadar kos untuk anggaran berasaskan projek dan sebenar ditentukan.
author: rumant
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 822a7bd8ae87d4fd4044d8b46347bfe1b4ca13ca
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475290"
---
# <a name="determine-cost-rates-for-project-based-estimates-and-actuals"></a>Tentukan kadar kos untuk anggaran berasaskan projek dan sebenar

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Untuk menentukan harga kos pada anggaran dan sebenar dalam Microsoft Dynamics 365 Project Operations, sistem mula-mula menggunakan tarikh dan mata wang dalam anggaran masuk atau konteks sebenar untuk menentukan senarai harga jualan. Dalam konteks sebenar secara khusus, sistem menggunakan **medan Tarikh** Transaksi untuk menentukan senarai harga yang boleh digunakan. Nilai **tarikh** Transaksi bagi anggaran masuk atau sebenar dibandingkan dengan **nilai Effective Start (Timezone independent)** dan **Effective End (Timezone independent)** pada senarai harga. Selepas senarai harga kos ditentukan, sistem menentukan kadar kos.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Menentukan kadar kos dalam anggaran dan konteks sebenar untuk Masa

Konteks anggaran untuk **Masa** merujuk kepada:

- Petikan butiran baris untuk **Masa**.
- Butiran talian kontrak untuk **Masa**.
- Tugasan sumber pada projek.

Konteks sebenar untuk **Masa** merujuk kepada:

- Baris jurnal Kemasukan dan Pembetulan untuk **Masa**.
- Baris jurnal yang dicipta apabila entri masa dihantar.

Selepas senarai harga kos ditentukan, sistem melengkapkan langkah-langkah berikut untuk memasukkan kadar kos lalai.

1. Sistem ini sepadan dengan gabungan **medan Peranan**, **Syarikat** Resourcing, dan **Unit** Resourcing dalam anggaran atau konteks sebenar untuk **Masa** terhadap garis harga peranan dalam senarai harga. Padanan ini menganggap bahawa anda menggunakan dimensi harga standard untuk kos buruh. Jika anda telah mengkonfigurasikan sistem untuk memadankan medan selain daripada atau sebagai tambahan kepada **Peranan**, **Syarikat** Resourcing dan **Unit** Resourcing, gabungan yang berbeza digunakan untuk mendapatkan semula garis harga peranan yang sepadan.
1. Jika sistem mendapati garis harga peranan yang mempunyai kadar kos untuk **Gabungan Peranan**, **Syarikat** Resourcing dan **Unit** Resourcing, kadar kos tersebut digunakan sebagai kadar kos lalai.
1. Sekiranya sistem tidak dapat menandingi **nilai Peranan**, **Syarikat** Resourcing, dan **Unit** Resourcing, ia menurunkan dimensi yang mempunyai keutamaan terendah, mencari garis harga peranan yang mempunyai padanan untuk dua nilai dimensi yang lain, dan terus menurunkan dimensi secara progresif sehingga baris harga peranan yang sepadan dijumpai. Kadar kos dari rekod itu akan digunakan sebagai kadar kos lalai. Jika sistem tidak menemui baris harga peranan yang sepadan, harga akan ditetapkan kepada **0** (sifar) secara lalai.

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

[!INCLUDE[footer-include](../includes/footer-banner.md)]
