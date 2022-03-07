---
title: Urus berbilang pelanggan pada kontrak projek - ringan
description: Topik ini menyediakan maklumat tentang pengurusan berbilang pelanggan pada kontrak projek.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b7010ef75cd71ecdf832abb889db4703baa18fce0adadf3893621c42002fcab9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001757"
---
# <a name="manage-multiple-customers-on-project-contracts---lite"></a>Urus berbilang pelanggan pada kontrak projek - ringan

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Kontrak projek dalam Dynamics 365 Project Operations menyokong senario perjanjian kontrak melibatkan berbilang pelanggan yang membiayai urusan. Tab **Ringkasan** pada halaman **Kontrak Projek** termasuk medan **Pelanggan**. Medan ini mengenal pasti pelanggan utama urusan. Pelanggan lain untuk urusan boleh ditetapkan pada tab **Pelanggan** halaman **Kontrak Projek**.

Semua pelanggan kontrak yang disenaraikan pada kontrak projek lalai sebagai pelanggan baris kontrak pada mana-mana baris kontrak berasaskan projek baharu yang dicipta untuk kontrak projek. Baris kontrak berasaskan projek yang sedia ada tidak mewarisi pelanggan kontrak baharu kerana rekod baharu dicipta.

Baris kontrak berasaskan produk dikaitkan secara automatik kepada pelanggan utama.

Pelanggan kontrak dan pelanggan baris kontrak boleh ditambah, dikemas kini atau dipadamkan pada bila-bila masa sebelum kontrak dimenangi.

## <a name="primary-customer"></a>Pelanggan utama

Pelanggan yang disenaraikan pada tab **Ringkasan** kontrak projek sebagai bakal pelanggan ialah pelanggan utama kontrak. Apabila anda cuba memadamkan pelanggan utama daripada senarai pelanggan pada kontrak, anda akan menerima mesej ralat yang rekod pelanggan utama pada kontrak tidak boleh dipadamkan.

Pelanggan utama tidak boleh dikemas kini daripada senarai pelanggan kontrak. Sebaliknya, tukar bakal pelanggan pada tab **Ringkasan** kontrak. Apabila medan ini dikemas kini pada halaman **Ringkasan Kontrak**, pelanggan baharu ditambahkan sebagai pelanggan kontrak baharu dengan bendera **Utama** ditetapkan. Pelanggan utama sebelumnya masih akan menjadi pelanggan pada kontrak.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Cipta, kemas kini atau padamkan rekod pelanggan kontrak

Pelanggan kontrak boleh dicipta, dikemas kini atau dipadamkan daripada tab **Pelanggan** pada halaman **Kontrak Projek**. Medan dalam jadual berikut adalah pada rekod pelanggan kontrak bagi kontrak projek dan perlu diingat kerana anda bekerja dengan kontrak tersebut.

| Medan | Lokasi | Penerangan | Kesan hiliran |
| --- | --- | --- | --- |
| **Akaun** | Grid boleh diedit pada tab **Pelanggan Kontrak** dan borang **Utama** dan **Cipta Cepat** untuk pelanggan kontrak. | Senaraikan semua akaun aktif. Medan ini dikunci selepas rekod dicipta. Untuk mengemas kini akaun, padamkan rekod dan cipta semula rekod. Jika anda telah merakam sebarang aktual atau rekod pelanggan kontrak ialah pelanggan utama, anda tidak boleh memadamkan rekod. | Pelanggan kontrak disalin sebagai pelanggan baris kontrak apabila baris kontrak dicipta. |
| **Peratus Pecahan Bil** | Grid boleh diedit pada tab **Pelanggan Kontrak** dan borang **Utama** dan **Cipta Cepat** untuk pelanggan kontrak. | Mewakili peratusan setiap transaksi jualan belum dibilkan yang diatribut kepada pelanggan kontrak ini. | Disalin ke baris kontrak baharu dan kepada pelanggan baris kontrak projek pada baris kontrak projek baharu. |
| **Bil kepada Nama Kenalan** | Grid boleh diedit pada tab **Pelanggan Kontrak** dan borang **Utama** dan **Cipta Cepat** untuk pelanggan kontrak. | Medan teks ini hendaklah digunakan bagi mengenal pasti orang hubungan invois untuk pelanggan ini. Medan ini adalah lalai daripada rekod akaun yang berkaitan. | Disalin ke medan **Bil kepada Nama Kontrak** pada invois yang dijana untuk pelanggan ini. |
| **Nama Bil Kepada** | Grid boleh diedit pada tab **Pelanggan Kontrak** dan borang **Utama** dan **Cipta Cepat** untuk pelanggan kontrak | Medan teks ini hendaklah digunakan bagi mengenal pasti orang hubungan invois untuk pelanggan ini. Medan ini adalah lalai daripada rekod akaun yang berkaitan. | Disalin ke medan **Bil kepada Nama Kontrak** pada invois yang dijana untuk pelanggan ini. |
| **Terma Pembayaran** | Grid boleh diedit pada tab **Pelanggan Kontrak** dan borang **Utama** dan **Cipta Cepat** untuk pelanggan kontrak. | Nilai adalah lalai daripada rekod akaun yang berkaitan. | Disalin ke medan **Bil kepada Nama Kontrak** pada invois yang dijana untuk pelanggan ini. |
| **Adakah Pembundaran** | Grid boleh diedit pada tab **Pelanggan Kontrak** dan borang **Utama** dan **Cipta Cepat** untuk pelanggan kontrak. | Menunjukkan jika pelanggan ini adalah pelanggan pembundaran lalai untuk urusan ini. Hanya boleh ada seorang pelanggan pembundaran pada kontrak projek. | Apabila kos dan jualan belum dibilkan berpecah pada kuantiti yang membawa kepada perbezaan pembundaran, perbezaan tersebut dikenakan kepada aktual yang memetakan kepada pelanggan ini. |
| **Had Tidak Boleh Dilebihi** | Grid boleh diedit pada tab **Pelanggan Kontrak** dan borang **Utama** dan **Cipta Cepat** untuk pelanggan kontrak | Menunjukkan jika terdapat had yang dirundingkan atau had kepada jumlah keseluruhan yang akan diinvoiskan kepada pelanggan untuk penglibatan ini. | **Had Tidak Boleh Dilebihi** yang disediakan pada peringkat pelanggan kontrak akan dinilai berdasarkan **Aktual Jualan Belum Dibilkan** yang merujuk kepada pelanggan kontrak ini. |

## <a name="edit-billing-split-percentages"></a>Edit peratusan pecahan pengebilan

Peratusan pecahan bil boleh diedit menggunakan pengalaman edit grid dalam baris. Apabila peratusan pecahan bil tidak berjumlah 100 peratus, anda akan menerima ralat. Selepas anda mengedit peratusan pecahan bil, segar semula halaman untuk menutup ralat.

Anda juga boleh memilih **Agihkan Secara Sekata** pada subgrid **Pelanggan Kontrak** untuk menguntukkan pecahan bil secara sekata kepada semua pelanggan kontrak. Jika terdapat faktor pembundaran, faktor itu akan ditambah kepada pelanggan pembundaran. Salah seorang pelanggan kontrak sentiasa ditag sebagai pelanggan **pembundaran**, yang bermaksud bahawa rekod pelanggan kontrak mempunyai bendera pembundaran yang ditetapkan kepada **Ya**. Biasanya, ini ialah pelanggan utama kontrak, tetapi ia juga boleh ditukar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]