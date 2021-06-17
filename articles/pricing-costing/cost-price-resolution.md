---
title: Menyelesaikan harga kos untuk anggaran dan aktual
description: Topik ini menyediakan maklumat tentang cara harga kos untuk anggaran dan aktual diselesaikan.
author: rumant
ms.date: 04/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d81b521acbfd97127cf056bd41a3249c01108374
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001392"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Menyelesaikan harga kos untuk anggaran dan aktual

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Untuk menyelesaikan harga kos dan senarai harga kos bagi anggaran dan aktual, sistem ini menggunakan maklumat dalam medan **Tarikh**, **Mata Wang** dan **Unit Kontrak** untuk projek berkaitan. Selepas senarai harga kos diselesaikan, aplikasi ini menyelesaikan kadar kos.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Menyelesaikan kadar kos pada baris aktual dan anggaran untuk Masa

Baris anggaran untuk Masa merujuk kepada butiran sebut harga dan baris kontrak bagi tugasan masa dan sumber pada projek.

Selepas senarai harga kos diselesaikan, sistem menggunakan medan **Peranan**, **Syarikat Sumber** dan **Unit Sumber** pada baris anggaran untuk Masa bagi pemadanan terhadap baris harga peranan dalam senarai harga. Pemadanan ini menganggap anda menggunakan dimensi penetapan harga luar kotak untuk kos buruh. Sebaliknya jika anda mengkonfigurasikan sistem untuk memadankan medan atau sebagai tambahan kepada **Peranan**, **Syarikat Sumber** dan **Unit Sumber** maka kombinasi berbeza akan digunakan untuk mendapatkan baris harga peranan pemadanan. Jika aplikasi mencari baris harga peranan yang mempunyai kadar kos untuk kombinasi **Peranan**, **Syarikat Sumber** dan **Unit Sumber** iaitu kadar kos lalai. Jika aplikasi tidak boleh betul-betul sepadan dengan kombinasi nilai **Peranan**, **Syarikat Sumber** dan **Unit Sumber**, ia akan mendapatkan kembali baris harga peranan dengan nilai peranan sepadan, tetapi mempunyai nilai nol untuk **Unit Sumber** dan **Syarikat Sumber**. Selepas rekod harga peranan sepadan dengan nilai harga peranan sepadan ditemukan, kadar kos ditetapkan lalai daripada rekod tersebut. 

> [!NOTE]
> Jika anda mengkonfigurasikan keutamaan yang berbeza **Peranan**, **Syarikat Sumber** dan **Unit Sumber** atau jika anda mempunyai dimensi lain yang mempunyai keutamaan lebih tinggi, tingkah laku ini akan berubah sewajarnya. Sistem ini mendapatkan kembali rekod harga peranan dengan nilai yang sepadan bagi setiap nilai dimensi penetapan harga dalam urutan keutamaan dengan baris yang mempunyai nilai nol untuk dimensi tersebut muncul terakhir dalam urutan keutamaan.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Menyelesaikan kadar kos pada baris aktual dan anggaran untuk Perbelanjaan

Baris anggaran untuk Perbelanjaan merujuk kepada butiran sebut harga dan baris kontrak bagi perbelanjaan dan baris anggaran perbelanjaan pada projek.

Selepas senarai harga kos diselesaikan, sistem menggunakan kombinasi medan **Kategori** dan **Unit** pada baris anggaran untuk Perbelanjaan bagi pemadanan terhadap baris **Harga Kategori** pada senarai harga diselesaikan. Jika sistem mencari baris harga kategori yang mempunyai kadar kos untuk kombinasi **Kategori** dan **Unit**, kadar kos dilalaikan. Jika sistem tidak boleh memadankan nilai **Kategori** dan **Unit**, atau jika sistem berupaya mencari baris harga kategori yang berpadanan tetapi kaedah penetapan harga bukan **Unit Setiap Harga**, kadar kos dilalaikan ke kosong(0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Menyelesaikan kadar kos pada baris aktual dan anggaran untuk bahan

Baris anggaran untuk bahan merujuk kepada butiran sebut harga dan baris kontrak untuk bahan dan baris anggaran bahan pada projek.

Selepas senarai harga kos diselesaikan, sistem menggunakan gabungan medan **Produk** dan **Unit** pada baris anggaran bagi anggaran bahan untuk dipadankan dengan baris **Item Senarai Harga** pada senarai harga yang diselesaikan. Jika sistem mendapati barisan harga produk yang mempunyai kadar kos untuk gabungan medan **Produk** dan **Unit**, kadar kos ditetapkan lalai. Jika sistem tidak dapat memadankan nilai **Produk** dan **Unit**, kos unit ditetapkan lalai kepada sifar. Tetapan lalai ini juga akan berlaku jika terdapat baris item senarai harga sepadan, tetapi kaedah penetapan harga adalah berdasarkan kos standard atau kos semasa yang tidak ditakrifkan dalam produk.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
