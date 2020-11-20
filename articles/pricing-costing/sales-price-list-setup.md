---
title: Sediakan senarai harga jualan
description: Topik ini menyediakan maklumat tentang senarai harga jualan untuk penetapan harga projek.
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
ms.openlocfilehash: eb8dfa61a2d17ba644daf1552889cbcde0f1e47a
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176262"
---
# <a name="set-up-a-sales-price-list"></a>Sediakan senarai harga jualan

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Untuk sebut harga projek dan kontrak, senarai harga projek mempunyai corak ganti harga yang berbeza berbanding senarai harga produk. Pada baris sebut harga berdasarkan katalog produk, anda boleh menulis ganti harga kepada peranan dan kategori secara langsung pada baris sebut harga, kerana setiap mata baris sebut harga kepada betul-betul satu item katalog. Walau bagaimanapun, pada baris sebut harga berasaskan projek, anda tidak boleh mengganti harga kepada peranan dan kategori secara langsung pada baris sebut harga. Anda boleh menggunakan senarai harga projek untuk bekerja dengan kedua-dua corak gantian yang berbeza.

> [!NOTE]
> Kami mengesyorkan anda mempunyai senarai harga berasingan untuk sumber projek dan item katalog anda, disebabkan perbezaan tingkah laku antara kedua-dua apabila anda mengganti penetapan harga.

Setiap entiti berikut boleh mempunyai senarai harga jualan yang berkaitan untuk penetapan harga projek:

- Pelanggan (akaun) 
- Peluang 
- Sebut Harga 
- Kontrak Projek

Persatuan entiti ini dengan senarai harga ditunjukkan oleh senarai harga projek. Anda boleh mengaitkan satu atau lebih senarai harga dengan entiti Pelanggan, Peluang, Sebut Harga dan Jualan Kontrak Projek.

Senarai harga projek lalai tidak dimasukkan secara automatik pada rekod pelanggan. Walau bagaimanapun, anda boleh melampirkan senarai harga projek kepada rekod pelanggan secara manual. Walau bagaimanapun, anda akan melampirkan senarai harga projek secara manual hanya apabila anda mempunyai perjanjian penetapan harga tersuai dengan pelanggan. 

Apabila senarai harga projek dilampirkan ke entiti jualan, maklumat berikut disahkan:

- Senarai harga mempunyai konteks **Jualan**. 
- Mata wang senarai harga sepadan dengan mata wang pelanggan. 

Pada kontrak projek, perintah keutamaan berikut digunakan untuk menetapkan senarai harga projek yang berkaitan secara automatik:

1. Sebut Harga
2. Peluang
3. Pelanggan 
4. Tetapan global 

Apabila senarai harga projek dimasukkan secara lalai, sistem mengesahkan bahawa mata wang sepadan dengan mata wang pelanggan dan senarai harga lalai yang telah dimasukkan mempunyai konteks **Jualan**.

Anda boleh mengaitkan senarai harga berbilang projek dengan entiti Pelanggan, Peluang, Sebut Harga dan Jualan Kontrak Projek. Keupayaan ini menyokong harga lalai khusus masa untuk kontrak projek panjang, yang anda mungkin memerlukan lebih daripada satu senarai harga untuk akaun bagi kemas kini harga yang berlaku kerana inflasi. Bagaimanapun, jika senarai harga yang anda kaitkan dengan entiti Pelanggan, Peluang, Sebut Harga atau Kontrak Projek mempunyai keberkesanan tarikh bertindan, harga lalai mungkin salah. Oleh itu, anda perlu memastikan senarai harga projek yang mempunyai keberkesanan tarikh bertindan tidak dikaitkan dengan entiti tersebut.
