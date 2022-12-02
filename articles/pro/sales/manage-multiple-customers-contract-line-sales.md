---
title: Urus berbilang pelanggan pada baris kontrak berasaskan projek - ringan
description: Artikel ini menyediakan maklumat tentang pengurusan berbilang pelanggan pada baris kontrak berasaskan projek.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f7648c7ef7ec6ffb68932552a0c25b79f1f93733
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922141"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines---lite"></a>Urus berbilang pelanggan pada baris kontrak berasaskan projek - ringan

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Baris kontrak berasaskan projek boleh memasukkan senarai pelanggan yang bertanggungjawab untuk pembayaran. Senarai pelanggan pada baris kontrak berasaskan projek ini boleh sama dengan senarai pelanggan pada kontrak, tetapi tidak diperlukan. Apabila sebut harga projek dimenangi dan kontrak projek dicipta, senarai pelanggan pada baris sebut harga disalin ke baris kontrak yang sepadan. Pelanggan pada sebut harga disalin ke kontrak.

Apabila kontrak projek diinvois, senarai pelanggan pada baris kontrak berasaskan projek diutamakan daripada senarai pelanggan pada kontrak. Senarai pelanggan pada kontrak projek hanya digunakan untuk baris kontrak baharu lalai.

Semua pelanggan kontrak pada tab **Pelanggan** kontrak projek adalah lalai kerana pelanggan baris kontrak pada mana-mana baris kontrak baharu dicipta untuk kontrak projek. Mana-mana baris kontrak yang sedia ada tidak akan mewarisi rekod pelanggan kontrak baharu yang dicipta selepas itu.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Cipta, kemas kini atau padamkan rekod pelanggan baris kontrak

Anda boleh mencipta, mengemas kini atau memadamkan pelanggan baris kontrak daripada tab Pelanggan Baris Kontrak pada halaman Baris Kontrak berasaskan Projek. Apabila pelanggan baharu ditambah pada baris kontrak berasaskan projek, mereka juga ditambah pada keseluruhan kontrak sebagai pelanggan kontrak dengan peratusan pecahan bil lalai sebanyak kosong peratus. Peratusan pecahan bil pada keseluruhan kontrak disalin ke baris kontrak baharu dan ke kontrak projek akhir. Walau bagaimanapun, apabila invois daripada kontrak, invois itu ialah peratusan pecahan bil pada peringkat baris kontrak yang digunakan dan bukan peratusan pecahan bil pada peringkat keseluruhan kontrak.

Berikut ialah medan pada rekod pelanggan baris **Kontrak** bagi baris kontrak berasaskan projek yang perlu diingat ketika anda bekerja dengan baris tersebut:

| Medan | Lokasi | Penerangan | Kesan hiliran |
| --- | --- | --- | --- |
| **Akaun** | Grid boleh diedit pada tab **Pelanggan Kontrak** dan borang **Utama** dan **Cipta Cepat** untuk pelanggan kontrak. | Semua akaun aktif. Medan ini dikunci selepas rekod dicipta. Untuk mengemas kini medan, padamkan rekod dan cipta rekod baharu. Jika anda telah merekodkan sebarang aktual, anda tidak boleh memadamkan rekod tersebut. Walau bagaimanapun, anda boleh menandakan peratusan pecahan bil sebagai sifar untuk akaun tersebut. Apabila rekod ditandakan sebagai sifar, mana-mana kos masa depan dan aktual hasil yang diatribut atau dipecahkan kepada pelanggan ini akan terjejas. | Apabila anda memilih akaun daripada senarai induk akaun untuk menambah dan menyimpan akaun tersebut, pelanggan baris kontrak juga ditambah sebagai pelanggan kontrak. Pelanggan baris kontrak digunakan apabila invois dijana. |
| **Peratus Pecahan Bil** | Grid boleh diedit pada tab **Pelanggan Kontrak** dan borang **Utama** dan **Cipta Cepat** untuk pelanggan kontrak. | Medan ini mewakili peratusan setiap transaksi jualan belum dibilkan yang akan diatribut kepada pelanggan baris kontrak ini. | Pelanggan baris kontrak dan peratusan pecahan bil digunakan apabila aktual dicipta selepas mendapat kelulusan dan apabila invois dijana. |
| **Had Tidak Boleh Dilebihi** | Grid boleh diedit pada tab **Pelanggan Kontrak** dan borang **Utama** dan **Cipta Cepat** untuk pelanggan kontrak. | Menunjukkan jika terdapat had yang dirundingkan atau had kepada jumlah keseluruhan yang akan diinvoiskan kepada pelanggan ini untuk baris kontrak. | Had tidak-boleh dilebihi untuk pelanggan baris kontrak digunakan apabila aktual dicipta dan invois dijana. |
| **Adakah Pembundaran** | Grid boleh diedit pada tab **Pelanggan Kontrak** dan borang **Utama** dan **Cipta Cepat** untuk pelanggan baris kontrak. | Medan ini menunjukkan jika pelanggan ini ialah pelanggan pembundaran lalai untuk baris kontrak berasaskan projek ini. | Apabila anda menjana aktual mengikut peratusan pecahan bil, mungkin terdapat beberapa perbezaan pembundaran. Pelanggan ini diatribut dengan perbezaan pembundaran dalam situasi ini. |

## <a name="edit-billing-split-percentages"></a>Edit peratusan pecahan pengebilan

Peratusan pecahan bil boleh diedit dalam grid. Apabila peratusan pecahan bil tidak berjumlah 100 peratus, ralat akan berlaku. Selepas anda mengedit peratusan pecahan bil, segar semula halaman untuk mengeluarkan ralat.

Anda juga boleh memilih **Agihkan Secara Sekata** pada subgrid pelanggan baris kontrak. Tindakan ini menguntukkan pecahan bil kepada semua pelanggan baris kontrak secara sekata. Jika terdapat mana-mana faktor pembundaran, faktor itu akan ditambah kepada pelanggan pembundaran. Seorang pelanggan baris kontrak sentiasa ditandakan sebagai pelanggan **Pembundaran** dengan bendera **Pembundaran** ditetapkan kepada **Ya**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]