---
title: Senarai harga produk
description: Artikel ini memberikan maklumat mengenai senarai harga dalam harga katalog yang digunakan untuk sebut harga projek dan kontrak.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 68203f5adf7bf41d97e662e335d481ccac959ed6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917633"
---
# <a name="product-price-lists"></a>Senarai harga produk

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

 Dalam Project Operations, **Senarai harga produk** dan entiti item senarai harga yang berkaitan menyokong kefungsian untuk penetapan harga produk pada sebut harga berdasarkan produk dan baris kontrak. Untuk produk yang digunakan pada projek, rekod item senarai harga untuk senarai harga projek digunakan. 

Produk perlu disediakan supaya ia mempunyai kos lalai dan senarai harga dalam katalog produk. Gunakan senarai harga, kos kos standard dan kos semasa untuk mengkonfigurasi kos lalai dan harga senarai. Harga senarai lalai digunakan pada baris sebut harga atau baris kontrak projek hanya apabila sistem tidak dapat mencari baris senarai harga untuk produk tersebut dalam senarai harga produk untuk sebut harga atau kontrak projek.

Harga kos baris katalog produk boleh ditukar antara sebut harga. Keupayaan ini penting kerana jika anda tidak menjejak kos dengan tepat, anda tidak boleh menentukan keuntungan operasi pada penglibatan projek. Secara lalai, kos standard produk digunakan sebagai harga kos. Walau bagaimanapun, harga kos lalai boleh dikemas kini pada baris sebut harga jika terdapat harga kos yang berbeza untuk sebut harga itu.

## <a name="price-list-items"></a>Item senarai harga

Anda boleh menambah produk daripada katalog produk kepada senarai harga yang berbeza. Baris senarai harga untuk produk sentiasa merujuk kepada unit tertentu. Penetapan harga untuk produk pada item senarai harga boleh dikonfigurasikan sebagai jumlah mata wang. Sebagai alternatif, ia boleh dikonfigurasikan sebagai fungsi harga senarai, kos semasa, atau kos standard.

Kefungsian penetapan harga menyokong pelbagai pilihan pembundaran apabila harga produk dikonfigurasikan sebagai fungsi harga senarai, kos standard atau kos semasa. Selain mengambil kesempatan daripada pelbagai kaedah penetapan harga dan pilihan pembundaran, anda boleh mengaitkan senarai diskaun dengan item senarai harga. 

 
## <a name="default-product-price-list"></a>Senarai harga produk lalai
Setiap rekod pelanggan mempunyai medan **Senarai Harga Lalai**, tempat anda boleh tentukan senarai harga yang sepadan dengan mata wang pelanggan. Nilai lalai tidak dimasukkan secara automatik dalam medan ini. Apabila perjanjian penetapan harga tersuai dengan pelanggan tertentu wujud, anda boleh menggunakan medan ini untuk mengaitkan senarai harga dengan pelanggan tersebut.

Entiti Peluang, Sebut Harga dan Kontrak Projek menggunakan pesanan berikut untuk memasukkan senarai harga produk lalai. Pesanan yang sama digunakan untuk senarai harga projek.

1.  Sebut Harga
2.  Peluang
3.  Pelanggan
4.  Tetapan global 

Secara lalai, medan **Produk** pada baris sebut harga menyenaraikan semua produk aktif dalam senarai harga produk sebut harga. Jika produk telah dinyahaktifkan atau jika ia merupakan produk draf, ia tidak disenaraikan, walaupun ia ada dalam senarai harga. 

Baris katalog produk ditambahkan sebagai baris invois pada invois pertama yang dicipta untuk kontrak projek. Pada invois draf, baris invois tersebut boleh dipadamkan. Dalam kes tersebut, baris akan muncul pada invois berikutnya sehingga ia diinvoiskan atau sehingga invois dihantar kepada pelanggan. Anda tidak boleh menginvoiskan sebahagian kuantiti baris invois produk. Apabila baris produk daripada kontrak projek diinvoiskan, aktual dicipta. Walau bagaimanapun, aktual tersebut tidak dipautkan kepada entiti projek berkaitan. Dalam erti kata lain, baris kontrak projek berdasarkan produk adalah bebas daripada sebarang penggunaan berdasarkan projek. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
