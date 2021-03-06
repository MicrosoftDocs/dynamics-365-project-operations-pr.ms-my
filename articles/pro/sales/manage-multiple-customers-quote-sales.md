---
title: Mengurus berbilang pelanggan pada sebut harga projek
description: Topik ini memberikan maklumat tentang bekerja pada sebut harga dengan berbilang pelanggan yang akan membiayai projek itu. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 656418ab99db46455195f70c38b6f5fa13c30755
ms.sourcegitcommit: f6509f7d50de4d4ebb92c1bf2cfcdf09f17458eb
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/06/2020
ms.locfileid: "3966830"
---
# <a name="managing-multiple-customers-on-project-quotes-sales"></a>Mengurus berbilang pelanggan pada sebut harga projek (Jualan)

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Sebut harga projek menyokong senario bagi cadangan melibatkan berbilang pelanggan yang akan membiayai urusan itu. Tab **Ringkasan** Sebut Harga mempunyai medan **Pelanggan berpotensi** yang mengenal pasti pelanggan utama urusan. Pelanggan lain untuk urusan boleh ditetapkan pada tab **Pelanggan** sebut harga projek.

Semua pelanggan sebut harga pada tab **Pelanggan** sebut harga projek dilalaikan sebagai pelanggan baris sebut harga pada sebarang baris sebut harga berasaskan projek **baharu** yang dicipta untuk sebut harga. Sebarang baris sebut harga berasaskan projek sedia ada tidak akan mewarisi rekod pelanggan sebut harga baharu yang dicipta selepasnya.

Baris sebut harga berasaskan produk akan secara automatik dikaitkan kepada pelanggan utama yang juga pelanggan dalam medan **Pelanggan Berpotensi** pada tab **Ringkasan** sebut harga.

Pelanggan sebut harga dan pelanggan baris sebut harga boleh ditambah, dikemas kini atau dipadam pada bila-bila masa sebelum sebut harga dimenangi.

## <a name="concept-of-a-primary-customer"></a>Konsep pelanggan utama

Pelanggan yang disenaraikan pada tab ringkasan projek sebut harga sebagai pelanggan berpotensi adalah pelanggan utama sebut harga. Apabila anda cuba memadam pelanggan utama daripada senarai pelanggan pada sebut harga, anda akan melihat ralat yang rekod pelanggan utama pada sebut harga tidak boleh dipadamkan.

Pelanggan utama tidak boleh dikemas kini daripada senarai pelanggan pada sebut harga. Walau bagaimanapun, anda boleh mempengaruhi pelanggan utama dengan mengubah pelanggan berpotensi pada tab **Ringkasan** sebut harga. Apabila medan ini dikemas kini pada tab **Ringkasan Sebut Harga**, pelanggan berpotensi yang terpilih ditambah sebagai pelanggan sebut harga baharu dengan set bendera **Utama**. Pelanggan berpotensi lama masih akan menjadi pelanggan pada sebut harga.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Cipta, Kemas kini atau Padam rekod pelanggan baris sebut harga

Pelanggan sebut harga boleh dicipta, dikemas kini atau dipadam daripada tab **Pelanggan sebut harga** pada halaman **Sebut Harga**. Medan yang disenaraikan dalam jadual berikut adalah pada rekod pelanggan sebut harga bagi sebut harga projek.

| **Medan** | **Lokasi** | **Keterkaitan, tujuan dan panduan** | **Kesan hiliran** |
| --- | --- | --- | --- |
| Akaun | Grid boleh diedit pada tab **Pelanggan sebut harga** dan borang **Utama** dan **Cipta Cepat** untuk pelanggan sebut harga. | Senaraikan semua akaun aktif. Medan ini dikunci selepas rekod dicipta. Jika anda mahu mengemaskinikannya, padam rekod dan ciptanya semula. Jika anda telah merekod sebarang aktual atau jika rekod pelanggan sebut harga adalah pelanggan utama, anda akan dibenarkan untuk memadam rekod itu. | Pelanggan sebut harga disalin sebagai pelanggan baris sebut harga apabila baris sebut harga dicipta. Pelanggan sebut harga juga disalin ke pelanggan kontrak projek apabila sebut harga dimenangi. |
| Peratusan Pecahan Pengebilan | Grid boleh diedit pada tab **Pelanggan sebut harga** dan borang **Utama** dan **Cipta Cepat** untuk pelanggan sebut harga. | Mewakili peratusan bagi setiap transaksi jualan tidak dibilkan yang akan diatribut ke pelanggan sebut harga ini. | Disalin ke baris sebut harga baharu dan kepada pelanggan kontrak projek. |
| Bil kepada Nama Kenalan | Grid boleh diedit pada tab **Pelanggan sebut harga** dan borang **Utama** dan **Cipta Cepat** untuk pelanggan sebut harga. | Ini ialah medan teks dan hendaklah digunakan bagi mengenal pasti orang hubungan Invois untuk pelanggan ini. Ini telah dilalaikan daripada rekod akaun yang berkaitan | Disalin ke pelanggan kontrak projek apabila Sebut Harga dimenangi dan seterusnya ke medan nama Bil kepada Kontrak yang dijana untuk pelanggan ini. |
| Bil Kepada Nama | Grid boleh diedit pada tab **Pelanggan sebut harga** dan borang **Utama** dan **Cipta Cepat** untuk pelanggan sebut harga. | Medan teks ini hendaklah digunakan bagi mengenal pasti orang hubungan invois untuk pelanggan ini. | Disalin ke pelanggan kontrak projek apabila sebut harga dimenangi dan seterusnya ke medan **Nama Bil kepada Kontrak** yang dijana untuk pelanggan ini. |
| Terma Pembayaran | Grid boleh diedit pada tab **Pelanggan sebut harga** dan borang **Utama** dan **Cipta Cepat** untuk pelanggan sebut harga. | Ini adalah set pilihan dengan nilai yang lalai daripada rekod akaun yang berkaitan. | Disalin kepada pelanggan kontrak projek apabila sebut harga dimenangi dan seterusnya ke medan **Bil kepada Nama Kontrak** pada invois yang dijana untuk pelanggan ini. |
| Adakah Pembundaran | Grid boleh diedit pada tab **Pelanggan sebut harga** dan borang **Utama** dan **Cipta Cepat** untuk pelanggan sebut harga. | Menunjukkan jika pelanggan ini adalah pelanggan pembundaran lalai untuk urusan ini. | Disalin ke pelanggan kontrak projek apabila sebut harga dimenangi. |
| Had yang tidak boleh melebihi | Grid boleh diedit pada tab **Pelanggan sebut harga** dan borang **Utama** dan **Cipta Cepat** untuk pelanggan sebut harga. | Menunjukkan jika terdapat had atau atas yang dirunding ke jumlah keseluruhan yang akan diinvois kepada pelanggan ini untuk perikatan ini | Disalin ke pelanggan kontrak projek apabila sebut harga dimenangi. |

## <a name="editing-billing-split-percentages"></a>Mengedit peratusan pecahan pengebilan

Anda boleh edit peratusan pecahan pengebilan menggunakan pengalaman edit grid dalam baris. Apabila peratusan pecahan pengebilan tidak berjumlah 100%, ralat akan berlaku. Selepas anda mengemas kini peratusan pecahan pengebilan, segar semula halaman untuk mengalih keluar ralat.

Anda juga boleh cuba memilih **Agihkan Dengan Sekata** pada subgrid sebut harga pelanggan. Tindakan ini memperuntukkan pecahan pengebilan ke semua pelanggan sebut harga. Jika terdapat faktor pembundaran yang akan ditambah ke pelanggan pembundaran. Salah satu pelanggan sebut harga sentiasa ditag sebagai pelanggan pembundaran. Ini bermaksud bahawa rekod pelanggan sebut harga mempunyai bendera **Pembundaran** ditetapkan ke **Ya**. Kebiasaannya ini adalah pelanggan utama sebut harga tetapi yang boleh ditukar.
