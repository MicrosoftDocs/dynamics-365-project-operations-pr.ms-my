---
title: Selesaikan harga jualan untuk anggaran dan aktual projek
description: Artikel ini memberikan maklumat tentang menyelesaikan harga jualan pada anggaran projek dan sebenar.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9a6a19a866ab3218f2a0fa297b5f6a00ed809d2f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917495"
---
# <a name="resolve-sales-prices-for-project-estimates-and-actuals"></a>Selesaikan harga jualan untuk anggaran dan aktual projek

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Apabila harga jualan pada anggaran dan sebenar diselesaikan dalam Dynamics 365 Project Operations, sistem mula-mula menggunakan tarikh dan mata wang sebut harga projek atau kontrak yang berkaitan untuk menyelesaikan senarai harga jualan. Setelah senarai harga jualan diselesaikan, sistem menyelesaikan kadar jualan atau bil.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Selesaikan kadar jualan pada baris sebenar dan anggaran untuk masa

Dalam Operasi Projek, baris anggaran bagi masa digunakan untuk menandakan butiran baris sebut harga dan baris kontrak untuk masa dan tugasan sumber pada projek.

Setelah senarai harga untuk jualan diselesaikan, sistem melengkapkan langkah-langkah berikut untuk menetapkan kadar bil lalai.

1. Sistem menggunakan medan **Peranan** dan **Unit Sumber** pada baris anggaran bagi masa, untuk dipadankan dengan baris harga peranan dalam senarai harga diselesaikan. Pemadanan ini menganggap bahawa dimensi penetapan harga luar kotak untuk kadar bil sedang digunakan. Jika anda mengkonfigurasi penetapan harga berdasarkan sebarang medan lain atau sebagai tambahan kepada **Peranan** dan **Unit Sumber**, maka gabungan tersebut akan digunakan untuk mendapatkan baris harga peranan yang sepadan.
2. Jika sistem mendapati baris harga peranan yang mempunyai kadar bil untuk gabungan medan **Peranan** dan **Unit Sumber**, maka kadar bil tersebut dilalaikan.
3. Jika sistem tidak dapat memadankan nilai medan **Peranan** dan **Unit Sumber**, maka ia akan mendapatkan baris harga peranan dengan peranan yang sepadan tetapi nilai nol **Unit Sumber**. Setelah sistem menemukan rekod harga peranan yang sepadan, ia akan menetapkan kadar bil daripada rekod tersebut. Pemadanan ini menganggap konfigurasi luar kotak untuk keutamaan relatif **Peranan** berbanding **Unit Sumber** sebagai dimensi penetapan harga jualan.

> [!NOTE]
> Jika anda mengkonfigurasi keutamaan **Peranan** dan **Unit Sumber** yang berbeza atau jika anda mempunyai dimensi lain yang keutamaannya lebih tinggi, tingkah laku ini akan berubah dengan sewajarnya. Sistem akan mendapatkan rekod harga peranan dengan nilai yang sepadan daripada setiap nilai dimensi penetapan harga mengikut urutan keutamaan dengan baris yang mempunyai nilai nol untuk dimensi merupakan yang terakhir.

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
    | &nbsp; | Tokokan terhadap kos | Gunakan tokokan seperti yang ditakrifkan oleh baris harga kategori pada kadar kos unit bagi kos berkaitan yang sebenar |

4. Jika sistem tidak dapat memadankan nilai medan **Kategori** dan **Unit**, kadar jualan ditetapkan lalai kepada sifar(0).

## <a name="resolving-sales-rates-on-actual-and-estimate-lines-for-material"></a>Menyelesaikan kadar jualan pada baris aktual dan anggaran untuk Bahan

Dalam Project Operations, baris anggaran untuk bahan digunakan untuk menandakan butiran baris sebut harga dan baris kontrak untuk bahan dan baris anggaran bahan pada projek.

Setelah senarai harga untuk jualan diselesaikan, sistem melengkapkan langkah-langkah berikut untuk menetapkan harga jualan unit lalai.

1. Sistem menggunakan gabungan medan **Produk** dan **Unit** pada baris anggaran bagi bahan untuk dipadankan dengan baris item senarai harga dalam senarai harga yang telah diselesaikan.
2. Jika sistem mendapati baris item senarai harga yang mempunyai kadar jualan untuk gabungan medan **Produk** dan **Unit** serta kaedah penetapan harga ialah **Amaun mata wang**, harga jualan yang ditentukan pada baris senarai harga digunakan.
3. Jika nilai medan **Produk** dan **Unit** tidak sepadan, kadar jualan ditetapkan lalai kepada sifar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
