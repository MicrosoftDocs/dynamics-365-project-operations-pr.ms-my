---
title: Selesaikan harga jualan untuk anggaran dan sebenar
description: Topik ini memberikan maklumat tentang cara menyelesaikan kadar jualan untuk anggaran dan sebenar.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b78d0f970f942513ecb6911d64fcffa629567f93f1a763eef20ca168080e4d02
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986277"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals"></a>Selesaikan harga jualan untuk anggaran dan sebenar

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Apabila harga jualan pada anggaran dan sebenar diselesaikan dalam Dynamics 365 Project Operations, sistem mula-mula menggunakan tarikh dan mata wang sebut harga projek atau kontrak yang berkaitan untuk menyelesaikan senarai harga jualan. Setelah senarai harga jualan diselesaikan, sistem menyelesaikan kadar jualan atau bil.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Selesaikan kadar jualan pada baris sebenar dan anggaran untuk masa

Dalam Operasi Projek, baris anggaran bagi masa digunakan untuk menandakan butiran baris sebut harga dan baris kontrak untuk masa dan tugasan sumber pada projek.

Setelah senarai harga untuk jualan diselesaikan, sistem melengkapkan langkah-langkah berikut untuk menetapkan kadar bil lalai.

1. Sistem menggunakan medan **Peranan**, **Syarikat Sumber** dan **Unit Sumber** pada baris anggaran bagi masa, untuk dipadankan dengan baris harga peranan dalam senarai harga yang diselesaikan. Pemadanan ini menganggap bahawa dimensi penetapan harga luar kotak untuk kadar bil sedang digunakan. Jika anda mengkonfigurasi penetapan harga berdasarkan sebarang medan lain atau sebagai tambahan kepada **Peranan**, **Syarikat Sumber** dan **Unit Sumber**, maka gabungan tersebut akan digunakan untuk mendapatkan baris harga peranan yang sepadan.
2. Jika sistem mendapati baris harga peranan yang mempunyai kadar bil untuk gabungan medan **Peranan**, **Syarikat Sumber** dan **Unit SUmber**, maka kadar bil tersebut dilalaikan.
3. Jika sistem tidak dapat memadankan nilai medan **Peranan**, **Syarikat Sumber** dan **Unit Sumber**, maka ia akan mendapatkan baris harga peranan dengan peranan yang sepadan tetapi nilai nol **Unit SUmber**. Setelah sistem menemukan rekod harga peranan yang sepadan, ia akan menetapkan kadar bil daripada rekod tersebut. Pemadanan ini menganggap konfigurasi luar kotak untuk keutamaan relatif **Peranan** berbanding **Unit Sumber** sebagai dimensi penetapan harga jualan.

> [!NOTE]
> Jika anda mengkonfigurasi keutamaan **Peranan**, **Syarikat Sumber** dan **Unit Sumber** yang berbeza atau jika anda mempunyai dimensi lain yang keutamaannya lebih tinggi, kelakuan ini akan berubah dengan sewajarnya. Sistem akan mendapatkan rekod harga peranan dengan nilai yang sepadan daripada setiap nilai dimensi penetapan harga mengikut urutan keutamaan dengan baris yang mempunyai nilai nol untuk dimensi merupakan yang terakhir.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Selesaikan kadar jualan pada baris sebenar dan anggaran untuk perbelanjaan

Dalam Operasi Projek, baris anggaran untuk perbelanjaan digunakan bagi menandakan butiran baris sebut harga dan baris kontrak untuk perbelanjaan dan baris anggaran perbelanjaan pada projek.

Setelah senarai harga untuk jualan diselesaikan, sistem melengkapkan langkah-langkah berikut untuk menetapkan harga jualan unit lalai.

1. Sistem menggunakan gabungan medan **Kategori** dan **Unit** pada baris anggaran bagi perbelanjaan untuk dipadankan dengan baris harga kategori dalam senarai harga yang telah diselesaikan.
2. Jika sistem mendapati baris harga kategori yang mempunyai kadar jualan untuk kombinasi medan **Kategori** dan **Unit**, maka kadar jualan tersebut dilalaikan.
3. Jika sistem mendapati baris harga kategori yang sepadan, kaedah penetapan harga boleh digunakan untuk menetapkan harga jualan lalai. Jadual di bawah menunjukkan kelakuan penetapan lalai harga perbelanjaan dalam Operasi Projek.

    | Konteks | Kaedah penetapan harga | Harga dilalaikan |
    | --- | --- | --- |
    | Anggaran | Harga seunit | Berdasarkan baris harga kategori |
    | &nbsp; | Pada kos | 0.00 |
    | &nbsp; | Tokokan terhadap kos | 0.00 |
    | Sebenar | Harga seunit | Berdasarkan baris harga kategori |
    | &nbsp; | Pada kos | Berdasarkan kos sebenar yang berkaitan |
    | &nbsp; | Tokokan terhadap kos | Dengan menggunakan tokokan seperti yang ditakrifkan oleh baris harga kategori pada kadar kos unit daripada kos berkaitan yang sebenar |

4. Jika sistem tidak dapat memadankan nilai medan **Kategori** dan **Unit**, kadar jualan ditetapkan lalai kepada sifar(0).

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-material"></a>Selesaikan kadar jualan pada baris aktual dan anggaran untuk bahan

Dalam Project Operations, baris anggaran untuk bahan digunakan untuk menandakan butiran baris sebut harga dan baris kontrak untuk bahan dan baris anggaran bahan pada projek.

Setelah senarai harga untuk jualan diselesaikan, sistem melengkapkan langkah-langkah berikut untuk menetapkan harga jualan unit lalai.

1. Sistem menggunakan gabungan medan **Produk** dan **Unit** pada baris anggaran bagi bahan untuk dipadankan dengan baris item senarai harga dalam senarai harga yang telah diselesaikan.
2. Jika sistem mendapati baris item senarai harga yang mempunyai kadar jualan untuk gabungan medan **Produk** dan **Unit** serta kaedah penetapan harga ialah **Amaun mata wang**, harga jualan yang ditentukan pada baris senarai harga digunakan.
3. Jika nilai medan **Produk** dan **Unit** tidak sepadan, kadar jualan ditetapkan lalai kepada sifar.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
