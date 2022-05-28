---
title: Asal transaksi - Pautkan sebenarnya ke sumber mereka
description: Topik ini menerangkan bagaimana konsep asal transaksi digunakan untuk memautkan sebenar kepada rekod sumber asal, seperti kemasukan masa, kemasukan perbelanjaan, atau log penggunaan bahan.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 908f78f7d58ec4b18f37d03b6fa7c4e2295491fa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584837"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Asal transaksi - Pautkan sebenarnya ke sumber mereka

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Rekod asal transaksi dicipta untuk memautkan aktual ke sumber mereka, entri masa tersebut, entri perbelanjaan, log penggunaan bahan dan invois projek.

Contoh berikut menunjukkan pemprosesan biasa bagi entri masa dalam kitaran hayat projek Project Operations.

> ![Memproses keseluruhan masa dalam Operasi Projek.](media/basic-guide-17.png)
 
1. Penyerahan entri masa menyebabkan dua baris jurnal dibuat: satu untuk kos dan satu untuk jualan yang tidak dibilkan.
2. Kelulusan akhir kemasukan masa menyebabkan dua aktual dibuat: satu untuk kos dan satu untuk jualan yang tidak dibilkan.
3. Apabila pengguna mencipta invois projek, transaksi baris invois dicipta menggunakan data daripada aktual jualan yang tidak dibilkan.
4. Apabila invois disahkan, dua aktual baharu dicipta: pembalikan jualan yang belum dibilkan dan aktual jualan yang dibilkan.

Setiap peristiwa dalam aliran kerja pemprosesan ini mencetuskan penciptaan rekod dalam entiti asal Transaksi untuk membantu membina jejak hubungan antara rekod ini yang dicipta merentas entri masa, baris jurnal, butiran baris sebenar dan invois.

Jadual berikut menunjukkan rekod dalam entiti asal Transaksi untuk aliran kerja sebelumnya.

| Peristiwa                        | Asal                   | Jenis asal                       | Transaksi                       | Jenis transaksi         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Penyerahan Entri Masa        | GUID Rekod entri masa   | Entri Masa                        | GUID Rekod Garisan Jurnal (kos)   | Garisan Jurnal             |
| GUID Rekod entri masa       | Entri Masa               | GUID Rekod Garisan Jurnal (jualan)  | Garisan Jurnal                      |                          |
| Kelulusan Masa                | GUID Rekod Garisan Jurnal | Garisan Jurnal                      | GUID Rekod Jualan Belum Dibilkan        | Sebenar                   |
| GUID Rekod entri masa       | Entri Masa               | GUID Rekod Jualan Belum Dibilkan        | Sebenar                            |                          |
| GUID Rekod Garisan Jurnal     | Garisan Jurnal             | GUID Rekod Aktual Kos           | Sebenar                            |                          |
| GUID Rekod entri masa       | Entri Masa               | GUID Rekod Aktual Kos           | Sebenar                            |                          |
| Penciptaan Invois             | GUID Rekod entri masa   | Entri Masa                        | GUID Transaksi Baris Invois     | Transaksi Baris Invois |
| GUID Rekod Garisan Jurnal     | Garisan Jurnal             | GUID Transaksi Baris Invois     | Transaksi Baris Invois          |                          |
| Pengesahan Invois         | GUID Baris Invois        | Baris Invois                      | GUID Rekod Jualan Dibilkan          | Sebenar                   |
| GUID Invois                 | Invois                  | GUID Rekod Jualan Dibilkan          | Sebenar                            |                          |
| GUID Butiran Baris Invois     | Butiran Baris Invois      | GUID Rekod Jualan Dibilkan          | Sebenar                            |                          |
| GUID Rekod entri masa       | Entri Masa               | GUID Rekod Jualan Dibilkan          | Sebenar                            |                          |
| GUID Rekod Garisan Jurnal     | Garisan Jurnal             | GUID Rekod Jualan Dibilkan          | Sebenar                            |                          |
| GUID Rekod entri masa       | Entri Masa               | GUID Pembalikan Jualan Belum Dibilkan      | Sebenar                            |                          |
| GUID Rekod Garisan Jurnal     | Garisan Jurnal             | GUID Pembalikan Jualan Belum Dibilkan      | Sebenar                            |                          |
| Pembetulan Invois Draf     | GUID ILD Lama             | Transaksi Baris Invois          | GUID ILD Pembetulan               | Transaksi Baris Invois |
| GUID IL Lama                  | Baris Invois             | GUID ILD Pembetulan               | Transaksi Baris Invois          |                          |
| GUID Invois Lama             | Invois                  | GUID ILD Pembetulan               | Transaksi Baris Invois          |                          |
| GUID Rekod entri masa       | Entri Masa               | GUID ILD Pembetulan               | Transaksi Baris Invois          |                          |
| GUID Rekod Garisan Jurnal     | Garisan Jurnal             | GUID ILD Pembetulan               | Transaksi Baris Invois          |                          |
| Pembetulan invois yang disahkan | GUID ILD Lama             | Transaksi Baris Invois          | GUID Aktual Jualan Dibilkan yang Dibalikkan | Sebenar                   |
| GUID IL Lama                  | Baris Invois             | GUID Aktual Jualan Dibilkan yang Dibalikkan | Sebenar                            |                          |
| GUID Invois Lama             | Invois                  | GUID Aktual Jualan Dibilkan yang Dibalikkan | Sebenar                            |                          |
| GUID Rekod entri masa       | Entri Masa               | GUID Aktual Jualan Dibilkan yang Dibalikkan | Sebenar                            |                          |
| GUID Rekod Garisan Jurnal     | Garisan Jurnal             | GUID Aktual Jualan Dibilkan yang Dibalikkan | Sebenar                            |                          |
| GUID ILD Lama                 | Transaksi Baris Invois | GUID Aktual Jualan Belum Dibilkan Baharu    | Sebenar                            |                          |
| GUID IL Lama                  | Baris Invois             | GUID Aktual Jualan Belum Dibilkan Baharu    | Sebenar                            |                          |
| GUID Invois Lama             | Invois                  | GUID Aktual Jualan Belum Dibilkan Baharu    | Sebenar                            |                          |
| GUID Rekod entri masa       | Entri Masa               | GUID Aktual Jualan Belum Dibilkan Baharu    | Sebenar                            |                          |
| GUID Rekod Garisan Jurnal     | Garisan Jurnal             | GUID Aktual Jualan Belum Dibilkan Baharu    | Sebenar                            |                          |
| GUID ILD Pembetulan          | Transaksi Baris Invois | GUID Aktual Jualan Belum Dibilkan Baharu    | Sebenar                            |                          |
| GUID IL Pembetulan           | Baris Invois             | GUID Aktual Jualan Belum Dibilkan Baharu    | Sebenar                            |                          |
| GUID Invois Pembetulan      | Invois                  | GUID Aktual Jualan Belum Dibilkan Baharu    | Aktual                            |                          |


Ilustrasi berikut menunjukkan pautan yang dicipta antara sebenar dan sumbernya pada pelbagai acara menggunakan contoh entri masa dalam Operasi Projek.

> ![Cara sebenar dipautkan kepada rekod sumber dalam Operasi Projek.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
