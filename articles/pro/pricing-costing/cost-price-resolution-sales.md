---
title: Selesaikan harga kos untuk anggaran dan aktual projek
description: Topik ini memberikan maklumat tentang cara harga kos untuk anggaran dan aktual projek diselesaikan.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a2a2df7672118a4a4d7748795174e8e8238dd7618a48437185879e06a253a381
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997572"
---
# <a name="resolve-cost-prices-on-project-estimates-and-actuals"></a>Selesaikan harga kos untuk anggaran dan aktual projek 

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Untuk menyelesaikan harga kos dan senarai harga kos bagi anggaran dan aktual, sistem ini menggunakan maklumat dalam medan **Tarikh**, **Mata Wang** dan **Unit Kontrak** untuk projek berkaitan. Selepas senarai harga kos diselesaikan, aplikasi ini menyelesaikan kadar kos.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Menyelesaikan kadar kos pada baris aktual dan anggaran untuk Masa

Baris anggaran untuk Masa merujuk kepada butiran sebut harga dan baris kontrak bagi tugasan masa dan sumber pada projek.

Selepas senarai harga kos diselesaikan, medan **Peranan** dan **Unit Sumber** pada baris anggaran untuk Masa dipadankan dengan baris harga peranan dalam senarai harga. Padanan ini menganggap anda menggunakan dimensi penetapan harga standard untuk kos buruh. Jika anda mengkonfigurasi sistem untuk sepadan dengan bidang bukan atau sebagai tambahan **Peranan** dan **Unit Sumber** kemudian kombinasi berbeza akan digunakan untuk mendapatkan baris harga peranan yang berpadanan. Jika aplikasi mencari baris harga peranan yang mempunyai kadar kos untuk kombinasi **Peranan** dan **Unit Sumber** yang merupakan kadar kos lalai. Jika aplikasi tidak boleh memadankan nilai **Peranan** dan **Unit Sumber** kemudian ia akan mendapatkan baris harga peranan dengan peranan yang berpadan tetapi nilai nol **Unit Sumber**. Selepas aplikasi mendapat rekod harga peranan yang sepadan, kadar kos lalai daripada rekod itu. 

> [!NOTE]
> Jika anda mengkonfigurasi keutamaan **Peranan** dan **Unit Sumber** yang berbeza atau jika anda mempunyai dimensi lain yang mempunyai keutamaan lebih tinggi, tingkah laku ini akan berubah sewajarnya. Sistem akan mendapatkan rekod harga peranan dengan nilai yang sepadan dengan setiap nilai dimensi penetapan harga mengikut urutan keutamaan dengan baris yang mempunyai nilai nol bagi dimensi yang terakhir.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Menyelesaikan kadar kos pada baris aktual dan anggaran untuk Perbelanjaan

Baris anggaran untuk Perbelanjaan merujuk kepada butiran sebut harga dan baris kontrak bagi perbelanjaan dan baris anggaran perbelanjaan pada projek.

Selepas senarai harga kos diselesaikan, sistem menggunakan kombinasi medan **Kategori** dan **Unit** pada baris anggaran perbelanjaan untuk dipadankan dengan baris **Harga Kategori** pada senarai harga yang diselesaikan. Jika sistem mencari baris harga kategori yang mempunyai kadar kos untuk kombinasi **Kategori** dan **Unit**, kadar kos dilalaikan. Jika sistem tidak dapat sepadan dengan nilai **Kategori** dan **Unit**, atau jika ia dapat mencari baris harga kategori yang sepadan tetapi kaedah penetapan harga bukan **Harga Seunit**, kadar kos lalai kepada sifar (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Menyelesaikan kadar kos pada baris aktual dan anggaran untuk bahan

Baris anggaran untuk Bahan merujuk kepada butiran sebut harga dan baris kontrak untuk bahan dan baris anggaran bahan pada projek.

Selepas senarai harga kos diselesaikan, sistem menggunakan gabungan medan **Produk** dan **Unit** pada baris anggaran bagi anggaran bahan untuk dipadankan dengan baris **Item Senarai Harga** pada senarai harga yang diselesaikan. Jika sistem mendapati barisan harga produk yang mempunyai kadar kos untuk gabungan medan **Produk** dan **Unit**, kadar kos ditetapkan lalai. Jika sistem tidak boleh sepadan dengan nilai **Produk** dan **Unit** atau jika ia dapat mencari baris item senarai harga yang sepadan tetapi kaedah penetapan harga adalah berdasarkan Kos standard atau Kos semasa dan tidak ditakrifkan untuk produk, kos unit ditetapkan lalai kepada sifar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
