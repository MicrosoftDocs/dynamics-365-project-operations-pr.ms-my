---
title: Urus berbilang pelanggan pada baris sebut harga berdasarkan projek - ringan
description: Topik ini menerangkan cara mengurus berbilang pelanggan pada baris sebut harga berasaskan projek.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0fde833ad6b13fc12b733d1aa9f3bba0cfd95b2b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273097"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines---lite"></a>Urus berbilang pelanggan pada baris sebut harga berdasarkan projek - ringan

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Baris sebut harga berasaskan projek menyokong senario yang setiap baris sebut harga mempunyai senarai pelanggan yang membayarnya. Senarai pelanggan pada baris sebut harga berasaskan projek boleh sama dengan senarai pelanggan pada sebut harga. Anda juga boleh mengubah senarai pelanggan yang akan berbeza. Apabila sebut harga projek dimenangi, senarai pelanggan pada baris sebut harga berasaskan projek disalin ke baris kontrak berasaskan projek yang berpadanan untuk akhirnya mencipta kontrak projek. Pelanggan pada sebut harga berasaskan projek disalin ke kontrak projek.

Apabila anda menginvois kontrak projek akhir, senarai pelanggan pada baris kontrak berasaskan projek mengambil keutamaan melalui senarai pada kontrak projek. Senarai pelanggan pada kontrak projek hanya digunakan untuk melalaikan baris kontrak projek baharu.

Semua pelanggan sebut harga pada tab **Pelanggan** projek dilalaikan sebagai pelanggan baris sebut sebut harga pada mana-mana baris sebut harga berasaskan projek baharu dicipta untuk sebut harga projek. Sebarang baris sebut harga berasaskan projek sedia ada tidak mewarisi rekod pelanggan sebut harga baharu yang dicipta selepasnya.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Cipta, kemas kini atau padam rekod pelanggan baris sebut harga

Anda boleh cipta, kemas kini atau padam pelanggan baris sebut harga pada tab **Pelanggan baris sebut harga** pada halaman **Baris sebut harga berasaskan projek**. Apabila anda menambah pelanggan baharu pada baris sebut harga berasaskan projek, pelanggan juga ditambah kepada sebut harga keseluruhan sebagai pelanggan sebut harga dengan peratusan pecahan pengebilan lalai berasaskan sebut harga keseluruhan sebanyak 0%. Peratusan pecahan pengebilan pada sebut harga keseluruhan disalin ke baris sebut harga baharu dan kontrak projek yang akhir. Walau bagaimanapun, apabila anda menginvois daripada kontrak, peratusan pecahan pengebilan pada peringkat baris sebut harga digunakan bukan peratusan pecahan pengebilan pada keseluruhan peringkat kontrak. 

Jadual berikut menunjukkan medan pada rekod pelanggan baris sebut harga bagi baris sebut harga berasaskan projek.

| Medan | Lokasi | Description dan panduan | Kesan hiliran |
| --- | --- | --- | --- |
| **Akaun** | Grid boleh diedit pada tab **Pelanggan baris sebut harga**, borang utama dan borang cipta cepat untuk pelanggan baris sebut harga, | Senarai semua akaun aktif. Medan ini dikunci selepas rekod dicipta. Jika anda perlu mengemas kini medan, hapus dan cipta semula rekod. Jika anda merekod sebarang aktual, anda tidak boleh memadam rekod. | Apabila anda memilih akaun daripada senarai induk akaun untuk ditambah, pelanggan baris sebut harga juga ditambah sebagai pelanggan sebut harga apabila anda menyimpannya. Pelanggan baris sebut harga disalin ke pelanggan baris kontrak projek apabila sebut harga dimenangi. |
| **Peratusan Pecahan Pengebilan** | Grid boleh diedit pada tab **Pelanggan baris sebut harga**, borang utama dan borang cipta cepat untuk pelanggan baris sebut harga, | Mewakili peratusan bagi setiap transaksi jualan tidak dibilkan yang akan diatribut dengan pelanggan baris sebut harga ini. | Disalin ke atas pelanggan baris kontrak projek. |
| **Had yang tidak melebihi** | Grid boleh diedit pada tab **Pelanggan baris sebut harga**, borang utama dan borang cipta cepat untuk pelanggan baris sebut harga, | Menunjukkan sama ada terdapat had atau atas yang dirunding ke jumlah keseluruhan yang akan diinvois kepada pelanggan ini untuk baris yang dipetik ini. | Disalin ke atas pelanggan baris kontrak projek apabila sebut harga dimenangi. |
| **Adalah pembundaran** | Grid boleh diedit pada tab **Pelanggan baris sebut harga**, borang utama dan borang cipta cepat untuk pelanggan baris sebut harga, | Menunjukkan sama ada pelanggan ini adalah pelanggan pembundaran lalai untuk baris sebut harga berasaskan projek ini. | Disalin ke atas pelanggan baris kontrak projek apabila sebut harga dimenangi. |

## <a name="edit-billing-split-percentages"></a>Edit peratusan pecahan pengebilan

Anda boleh mengedit peratusan pecahan pengebilan dalam talian. Apabila peratusan pecahan pengebilan tidak berjumlah 100%, ralat berlaku. Selepas anda mengedit peratusan pecahan pengebilan, segar semula halaman baris sebut harga untuk mengalih keluar ralat.

Gunakan tindakan mengedar sama rata pada baris sebut harga pelanggan sub untuk memperuntukkan pecahan pengebilan kepada pelanggan baris sebut harga. Jika terdapat faktor pembundaran yang akan ditambah kepada pelanggan pembundaran. Salah satu pelanggan baris sebut harga sentiasa ditanda sebagai pelanggan pembundaran yang bermaksud rekod sebut harga pelanggan talian itu mempunyai bendera pembundaran yang ditetapkan kepada **Ya**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]