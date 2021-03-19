---
title: Senarai harga produk
description: Topik ini menyediakan maklumat tentang senarai harga dalam penetapan harga katalog yang digunakan untuk sebut harga dan kontrak projek.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c0f30bec159254c078024549b7b0dd0c048ef65d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275369"
---
# <a name="product-price-lists"></a>Senarai harga produk

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Senarai harga dan entiti item senarai harga menyokong penetapan harga katalog produk. Bagi sebahagian besar, fungsi ini digunakan untuk baris berdasarkan katalog pada sebut harga projek dan kontrak projek.

Bagi baris berdasarkan projek, kontrak mewakili urusan selepas ia dimenangi. Oleh sebab proses rundingan biasanya mendahului kemenangan tersebut, harga yang dilampirkan pada sebut harga sentiasa disalin seadanya pada senarai harga baharu dan dilampirkan pada kontrak. Senarai harga baharu ini tidak boleh ditukar di luar skop kontrak. Pengehadan ini membantu melindungi kad kadar yang telah dirunding daripada sebarang perubahan harga yang berlaku dalam senarai harga induk.

Produk perlu disediakan supaya ia mempunyai kos lalai dan senarai harga dalam katalog produk. Gunakan senarai harga, kos kos standard dan kos semasa untuk mengkonfigurasi kos lalai dan harga senarai. Harga senarai lalai digunakan pada baris sebut harga atau baris kontrak projek hanya apabila sistem tidak dapat mencari baris senarai harga untuk produk tersebut dalam senarai harga produk untuk sebut harga atau kontrak projek.

Harga kos baris katalog produk boleh ditukar antara sebut harga. Keupayaan ini penting kerana jika anda tidak menjejak kos dengan tepat, anda tidak boleh menentukan keuntungan operasi pada penglibatan projek. Secara lalai, kos standard produk digunakan sebagai harga kos. Walau bagaimanapun, harga kos lalai boleh dikemas kini pada baris sebut harga jika terdapat harga kos yang berbeza untuk sebut harga itu.

## <a name="price-list-items"></a>Item senarai harga

Anda boleh menambah produk daripada katalog produk kepada senarai harga yang berbeza. Baris senarai harga untuk produk sentiasa merujuk kepada unit tertentu. Penetapan harga untuk produk pada item senarai harga boleh dikonfigurasikan sebagai jumlah mata wang. Sebagai alternatif, ia boleh dikonfigurasikan sebagai fungsi harga senarai, kos semasa, atau kos standard.

PSA menyokong pelbagai pilihan pembundaran apabila harga dikonfigurasikan sebagai fungsi harga senarai, kos standard atau kos semasa. Selain mengambil kesempatan daripada pelbagai kaedah penetapan harga dan pilihan pembundaran, anda boleh mengaitkan senarai diskaun dengan item senarai harga. 

Apabila anda mencipta senarai harga tersuai baharu untuk sebut harga dengan memilih **Cipta Penetapan Harga Tersuai** pada halaman **Sebut Harga Projek**, salinan senarai harga dibuat dan medan **Entiti** pada pengepala senarai harga baharu ditetapkan kepada **Entiti Jualan**. Nama senarai harga baharu akan ditambah dengan nama sebut harga dan cap masa. Anda juga boleh menggunakan nama senarai harga baharu dan nama sebut harga dalam aliran kerja tersuai untuk mencetuskan semakan tambahan dan kelulusan untuk sebut harga yang menggunakan penetapan harga tersuai.

 
## <a name="default-product-price-list"></a>Senarai harga produk lalai
Setiap rekod pelanggan mempunyai medan **Senarai Harga Lalai**, tempat anda boleh tentukan senarai harga yang sepadan dengan mata wang pelanggan. Nilai lalai tidak dimasukkan secara automatik dalam medan ini. Apabila perjanjian penetapan harga tersuai dengan pelanggan tertentu wujud, anda boleh menggunakan medan ini untuk mengaitkan senarai harga dengan pelanggan tersebut.

Entiti Peluang, Sebut Harga dan Kontrak Projek menggunakan pesanan berikut untuk memasukkan senarai harga produk lalai. Pesanan yang sama digunakan untuk senarai harga projek.

1.  Sebut Harga
2.  Peluang
3.  Pelanggan
4.  Tetapan global 

Secara lalai, medan **Produk** pada baris sebut harga menyenaraikan semua produk aktif dalam senarai harga produk sebut harga. Jika produk telah dinyahaktifkan atau jika ia merupakan produk draf, ia tidak disenaraikan, walaupun ia ada dalam senarai harga. 

Baris katalog produk ditambahkan sebagai baris invois pada invois pertama yang dicipta untuk kontrak projek. Pada invois draf, baris invois tersebut boleh dipadamkan. Dalam kes tersebut, baris akan muncul pada invois berikutnya sehingga ia diinvoiskan atau sehingga invois dihantar kepada pelanggan. Anda tidak boleh menginvoiskan sebahagian kuantiti baris invois produk. Apabila baris produk daripada kontrak projek diinvoiskan, aktual dicipta. Walau bagaimanapun, aktual tersebut tidak dipautkan kepada entiti projek berkaitan. Dalam erti kata lain, baris kontrak projek berdasarkan produk adalah bebas daripada sebarang penggunaan berdasarkan projek. Penggunaan bahan pada projek tidak dijejak.


[!INCLUDE[footer-include](../includes/footer-banner.md)]