---
title: Gambaran keseluruhan baris kontrak berdasarkan produk
description: Topik ini memberikan maklumat tentang baris kontrak berdasarkan produk.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 794a80b0dd6b8717b43e712b96b9ac077517c226
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081155"
---
# <a name="product-based-contract-lines-overview"></a>Gambaran keseluruhan baris kontrak berdasarkan produk

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Anda boleh mencipta baris kontrak berdasarkan produk dalam Dynamics 365 Project Operations. Baris kontrak berdasarkan produk boleh dicipta baris secara manual, atau ia boleh menjadi item daripada katalog produk.

## <a name="product-catalog"></a>Katalog produk

Produk dalam katalog produk mempunyai unit lalai dan kumpulan unit. Jika beberapa produk berkongsi set atribut yang sama, anda boleh mencipta keluarga produk yang juga mempunyai atribut tersebut. Semua produk dalam satu keluarga produk mewarisi set atribut yang sama.

Contohnya, sebuah syarikat menjual lesen langganan untuk pelbagai jenis perisian. Semua perisian langganan mempunyai dua atribut berikut:

- Bilangan pengguna
- Tempoh langganan (dalam bulan)

Untuk mengekalkan jenis katalog ini, cipta keluarga produk yang dinamakan **Perisian Langganan**. Tambah atribut, **Bilangan pengguna** dan **Tempoh langganan** kepada keluarga produk. Kemudian, tambah produk individu ke keluarga produk **Perisian Langganan**.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Tambah item katalog produk ke Kontrak projek

Kontrak projek mempunyai bahagian untuk dua jenis baris, berdasarkan projek dan berdasarkan produk. Baris berdasarkan produk termasuk semua produk dan unit dalam senarai harga produk pada kontrak. Produk yang bukan merupakan sebahagian daripada senarai harga produk kontrak boleh ditambahkan.

Anda boleh memilih produk daripada senarai harga lain, atau secara langsung daripada katalog produk. Apabila anda memilih produk secara langsung daripada katalog produk, senarai harga lalai produk tersebut digunakan untuk harga jualan produk. Jika senarai harga lalai tidak ditetapkan, harga ditetapkan kepada 0 (sifar).

Jika baris kontrak adalah berdasarkan pada katalog produk, anda boleh ganti harga jualan secara langsung pada baris. Baris kontrak mempunyai medan **Harga** dengan dua nilai:

- **Ganti penetapan harga**
- **Gunakan lalai**

Jika anda menetapkan medan **Harga** kepada **Harga ganti** , harga lalai tidak ditetapkan. Masukkan harga untuk produk pada baris kontrak. Jika anda menetapkan medan kepada **Gunakan lalai** , harga jualan lalai digunakan dan medan tidak boleh diedit.

Selepas anda memasang Project Operations, harga jualan lalai dimasukkan pada baris berdasarkan produk pada kontrak. Medan **Harga** ditetapkan kepada **Ganti harga** supaya anda boleh mengedit harga lalai pada baris kontrak. Ini adalah ganti khusus Project Operations kepada tingkah laku baris berdasarkan produk dalam Dynamics 365 Sales.
