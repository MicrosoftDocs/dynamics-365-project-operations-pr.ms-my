---
title: Gambaran keseluruhan baris sebut harga berdasarkan produk
description: Artikel ini menyediakan maklumat tentang bekerja dengan baris sebut harga berasaskan produk.
author: rumant
ms.date: 10/30/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a260c0f51cc2d958281dbc6f0f711347cab85a9a
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 12/05/2022
ms.locfileid: "9826234"
---
# <a name="product-based-quote-lines-overview"></a>Gambaran keseluruhan baris sebut harga berdasarkan produk

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Anda boleh mencipta baris sebut harga berdasarkan produk dalam Dynamics 365 Project Operations. Baris sebut harga berasaskan produk boleh ditambah secara manual atau boleh menjadi item daripada katalog produk.

## <a name="product-catalog"></a>Katalog produk

Setiap produk dalam katalog produk mempunyai unit dan kumpulan unit lalai. Jika berbilang produk berkongsi set atribut yang sama, anda boleh mencipta keluarga produk yang berkongsi atribut itu. 

Contohnya, sebuah syarikat menjual lesen langganan untuk pelbagai jenis perisian. Semua perisian langganan mempunyai dua atribut berikut:

- Bilangan pengguna
- Tempoh langganan diukur dalam bulan

Untuk mengekalkan jenis katalog ini, cipta keluarga produk bernama **Perisian Langganan** dan tambah bilangan pengguna dan tempoh langganan sebagai atribut. Seterusnya, anda boleh menambah produk individu kepada keluarga produk **Perisian Langganan**.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Tambah item katalog produk kepada sebut harga projek

Halaman **Sebut Harga Projek** dan **Kontrak Projek** mempunyai bahagian untuk baris berasaskan projek dan baris berasaskan produk. Untuk baris berasaskan produk, senarai juntai bawah pada baris sebut harga atau baris kontrak projek termasuk semua produk dan unit dalam senarai harga produk. Anda juga boleh menambah produk yang bukan sebahagian daripada senarai harga produk.

Selain itu, anda boleh memilih produk daripada senarai harga yang lain atau secara langsung daripada katalog produk. Apabila anda memilih produk secara langsung daripada katalog produk, senarai harga lalai produk tersebut digunakan untuk mendapatkan harga jualan produk tersebut. Jika senarai harga lalai tidak ditetapkan, harga ditetapkan kepada sifar (0).

Apabila baris sebut harga adalah berasaskan pada katalog produk, anda boleh mengganti harga jualan secara langsung pada baris sebut harga. Baris sebut harga dalam medan **Penetapan harga** dengan dua nilai tersedia:

- **Ganti Penetapan harga**
- **Gunakan Lalai**

Jika anda memilih **Ganti Penetapan Harga**, harga lalai tidak ditetapkan. Sebaliknya, anda mesti masukkan harga untuk produk pada baris sebut harga. Jika anda memilih **Gunakan Lalai**, harga jualan lalai digunakan dan medan dikunci untuk pengeditan.

Harga jualan lalai dimasukkan pada baris berasaskan produk sebut harga. Medan **Penetapan harga** kemudian ditetapkan kepada **Ganti Penetapan harga** supaya anda boleh mengedit harga lalai pada baris sebut harga. Ini adalah Project Operations ganti khusus untuk tingkah laku berasaskan produk dalam Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
