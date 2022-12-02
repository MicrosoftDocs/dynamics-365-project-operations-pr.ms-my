---
title: Asal transaksi - Pautkan aktual kepada sumbernya
description: Artikel ini menerangkan cara konsep asal transaksi digunakan untuk memautkan aktual kepada rekod sumber asal seperti entri masa, entri perbelanjaan atau log penggunaan bahan.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f1beff392ddd449a930d38016ca6083fea97953b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921313"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Asal transaksi - Pautkan aktual kepada sumbernya

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Rekod asal transaksi dicipta untuk mengaitkan aktual kepada sumber mereka seperti entri masa, entri perbelanjaan, log penggunaan bahan dan invois projek.

Contoh berikut menunjukkan pemprosesan biasa bagi entri masa dalam kitaran hayat projek Project Operations.

> ![Memproses entri masa dalam Project Operations.](media/basic-guide-17.png)
 
1. Penyerahan entri masa menyebabkan dua garisan jurnal dicipta: satu untuk kos dan satu untuk jualan yang belum dibilkan.
2. Pelulus akhir bagi entri masa menyebabkan dua aktual dicipta: satu untuk kos dan satu untuk jualan yang belum dibilkan.
3. Apabila pengguna mencipta invois projek, transaksi baris invois dicipta menggunakan data daripada aktual jualan yang tidak dibilkan.
4. Apabila invois disahkan, dua aktual baharu dicipta: pembalikan jualan yang belum dibilkan dan aktual jualan yang dibilkan.

Setiap peristiwa dalam aliran kerjai pemprosesan ni mencetuskan penciptaan rekod dalam entiti asal Transaksi untuk membantu dalam membina jejak hubungan antara rekod yang dicipta merentasi entri masa, garisan jurnal, aktual dan butiran baris invois.

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


Ilustrasi berikut menunjukkan pautan yang dicipta antara jenis aktual dan sumbernya pada pelbagai peristiwa menggunakan contoh entri masa dalam Project Operations.

> ![Cara aktual dipautkan kepada rekod sumber dalam Project Operations.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
