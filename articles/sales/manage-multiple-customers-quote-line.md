---
title: Urus berbilang pelanggan pada baris sebut harga berasaskan projek
description: Topik ini memberikan maklumat tentang cara mengurus berbilang pelanggan pada baris sebut harga berasaskan projek.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48336af0ad522e9d6aa68fa82ffa7921f09662d4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118574"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines"></a>Urus berbilang pelanggan pada baris sebut harga berasaskan projek

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Baris sebut harga berasaskan projek menyokong senario yang setiap baris sebut harga mempunyai senarai pelanggan yang membayarnya. Senarai pelanggan pada baris sebut harga berasaskan projek boleh sama dengan senarai pelanggan pada sebut harga. Anda juga boleh mengubah senarai pelanggan yang akan berbeza. Untuk mewujudkan kontrak projek akhir apabila sebut harga projek dimenangi, senarai pelanggan pada baris sebut harga projek akan disalin ke baris kontrak berasaskan projek yang sepadan. Pelanggan pada sebut harga berasaskan projek disalin ke kontrak projek.

Apabila anda menginvois kontrak projek akhir, senarai pelanggan pada baris kontrak berasaskan projek mengambil keutamaan melalui senarai pada kontrak projek. Senarai pelanggan pada kontrak projek hanya digunakan untuk melalaikan baris kontrak projek baharu.

Semua pelanggan sebut harga pada tab **Pelanggan** projek dilalaikan sebagai pelanggan baris sebut sebut harga pada mana-mana baris sebut harga berasaskan projek baharu dicipta untuk sebut harga projek. Sebarang baris sebut harga berasaskan projek sedia ada tidak mewarisi rekod pelanggan sebut harga baharu yang dicipta selepasnya.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Cipta, kemas kini atau padam rekod pelanggan baris sebut harga

Anda boleh cipta, kemas kini atau padam pelanggan baris sebut harga pada tab **Pelanggan baris sebut harga** pada halaman **Baris sebut harga berasaskan projek**. Apabila anda menambah pelanggan baharu pada baris sebut harga berasaskan projek, pelanggan juga ditambah kepada sebut harga keseluruhan sebagai pelanggan sebut harga dengan peratusan pecahan pengebilan lalai berasaskan sebut harga keseluruhan sebanyak 0%. Peratusan pecahan pengebilan pada sebut harga keseluruhan disalin ke baris sebut harga baharu dan kontrak projek yang akhir. Walau bagaimanapun, apabila anda menginvois daripada kontrak, peratusan pecahan pengebilan pada peringkat baris sebut harga digunakan bukan peratusan pecahan pengebilan pada keseluruhan peringkat kontrak. 

Jadual berikut menunjukkan medan pada rekod pelanggan baris sebut harga bagi baris sebut harga berasaskan projek.

| Medan | Lokasi | Description dan panduan | Kesan hiliran |
| --- | --- | --- | --- |
| **Akaun** | Grid boleh diedit pada tab **Sebut harga pelanggan**, borang utama dan borang cipta cepat untuk pelanggan baris sebut harga. | Senarai semua akaun aktif. Medan ini dikunci selepas rekod dicipta. Jika anda perlu mengemas kini medan, hapus dan cipta semula rekod. Jika anda merekod sebarang aktual, anda tidak boleh memadam rekod. | Apabila anda memilih akaun daripada senarai induk akaun untuk ditambah, pelanggan baris Sebut Harga juga ditambah sebagai pelanggan Sebut Harga. Pelanggan baris sebut harga disalin ke pelanggan baris kontrak projek apabila sebut harga dimenangi. |
| **Peratusan Pecahan Pengebilan** | Grid boleh diedit pada tab **Sebut harga pelanggan**, borang utama dan borang cipta cepat untuk pelanggan baris sebut harga. | Mewakili peratusan bagi setiap transaksi jualan tidak dibilkan yang akan diatribut dengan pelanggan baris sebut harga ini. | Disalin ke atas pelanggan baris kontrak projek. |
| **Had yang tidak melebihi** | Grid boleh diedit pada tab **Sebut harga pelanggan**, borang utama dan borang cipta cepat untuk pelanggan baris sebut harga. | Menunjukkan sama ada terdapat had atau atas yang dirunding ke jumlah keseluruhan yang akan diinvois kepada pelanggan ini untuk baris yang dipetik ini. | Disalin ke atas pelanggan baris kontrak projek apabila sebut harga dimenangi. |
| **Syarikat pemilikan** | Grid boleh diedit pada tab **Pelanggan baris sebut harga**, borang utama dan borang cipta cepat untuk pelanggan baris sebut harga, | Entiti sah yang disediakan oleh pelanggan dalam modul **Pengurusan projek dan perakaunan**. Medan ini adalah baca sahaja dan ditetapkan kepada syarikat pemilikan sebut harga itu sendiri. Senarai pelanggan untuk ditambah dalam medan **Akaun** sudah ditapis ke senarai daripada syarikat pemilikan dalam modul Project Operations **Pengurusan projek dan perakaunan**. | Syarikat yang dimiliki menyamai konsep entiti undang-undang. Semua kos dan pendapatan yang terakru daripada projek ini diambil kira dalam Lejar Am syarikat pemilik. |
| **adalah pembundaran** | Grid boleh diedit pada tab **Sebut harga pelanggan**, borang utama dan borang cipta cepat untuk pelanggan baris sebut harga. | Menunjukkan sama ada pelanggan ini adalah pelanggan pembundaran lalai untuk baris sebut harga berasaskan projek ini. | Disalin ke atas pelanggan baris kontrak projek apabila sebut harga dimenangi. |

## <a name="edit-billing-split-percentages"></a>Edit peratusan pecahan pengebilan

Anda boleh mengedit peratusan pecahan pengebilan dalam talian. Apabila peratusan pecahan pengebilan tidak berjumlah 100%, ralat berlaku. Selepas anda mengedit peratusan pecahan pengebilan, segar semula halaman baris sebut harga untuk mengalih keluar ralat.

Gunakan tindakan mengedar sama rata pada baris sebut harga pelanggan sub untuk memperuntukkan pecahan pengebilan kepada pelanggan baris sebut harga. Jika terdapat faktor pembundaran yang akan ditambah kepada pelanggan pembundaran. Salah satu pelanggan baris sebut harga sentiasa ditanda sebagai pelanggan pembundaran yang bermaksud rekod sebut harga pelanggan talian itu mempunyai bendera pembundaran yang ditetapkan kepada **Ya**. 
