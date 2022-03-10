---
title: Gambaran keseluruhan baris kontrak berasaskan produk - lite
description: Topik ini memberikan maklumat tentang baris kontrak berdasarkan produk.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 79b4f6355afb7472f843eda06bf33a3fe732274d6f2566bd23000aa11cbfdce1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007562"
---
# <a name="product-based-contract-lines-overview---lite"></a>Gambaran keseluruhan baris kontrak berasaskan produk - lite

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

Jika anda menetapkan medan **Harga** kepada **Harga ganti**, harga lalai tidak ditetapkan. Masukkan harga untuk produk pada baris kontrak. Jika anda menetapkan medan kepada **Gunakan lalai**, harga jualan lalai digunakan dan medan tidak boleh diedit.

Selepas anda memasang Project Operations, harga jualan lalai dimasukkan pada baris berdasarkan produk pada kontrak. Medan **Harga** ditetapkan kepada **Ganti harga** supaya anda boleh mengedit harga lalai pada baris kontrak. Ini adalah ganti khusus Project Operations kepada tingkah laku baris berdasarkan produk dalam Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]