---
title: Senarai harga lalai
description: Artikel ini menyediakan maklumat tentang jualan lalai dan senarai harga kos dalam Operasi Projek.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410274"
---
# <a name="default-price-lists"></a>Senarai harga lalai

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

## <a name="sales-price-lists"></a>Senarai harga jualan

Setiap sebut harga projek dan kontrak dalam Dynamics 365 Project Operations mengandungi senarai harga jualan lalai. 

### <a name="price-list-default-on-project-quotes"></a>Senarai harga dijadikan lalai pada sebut harga projek
Sistem akan melengkapkan proses berikut untuk menentukan senarai harga untuk dijadikan lalai pada sebut harga projek:

1. Sistem melihat senarai harga yang dilampirkan pada senarai harga projek akaun. 
1. Sekiranya tidak ada senarai harga projek yang dilampirkan pada rekod akaun, sistem melihat senarai harga jualan yang dilampirkan pada parameter projek yang sepadan dengan mata wang sebut harga projek.
1. Seterusnya, sistem akan menyemak tempoh kuat kuasa tarikh senarai harga yang sepadan dengan julat tarikh sebut harga projek. Khususnya, tarikh yang sebut harga dicipta.
1. Jika terdapat berbilang senarai harga yang berkuat kuasa untuk tarikh sebut harga projek, semua senarai harga dijadikan lalai pada sebut harga projek.
1. Jika tiada senarai harga yang berkuat kuasa untuk tarikh sebut harga projek, tidak akan ada senarai harga projek dijadikan lalai pada sebut harga projek. Mesej amaran akan muncul pada sebut harga projek. Mesej menyatakan bahawa nilai sebenar dan anggaran pada projek tidak akan diberikan harga kerana tiada senarai harga projek dilampirkan.

### <a name="price-list-default-on-project-contracts"></a>Senarai harga yang dijadikan lalai pada kontrak projek 
Sistem akan melengkapkan proses berikut untuk menentukan senarai harga untuk dijadikan lalai pada kontrak projek:

1. Jika kontrak dicipta daripada sebut harga, senarai harga projek pada sebut harga disalin secara berasingan dan dilampirkan pada kontrak projek.
1. Jika kontrak dicipta daripada kosong, sistem akan melihat senarai harga yang dilampirkan pada senarai harga projek akaun. Jika tiada senarai harga projek yang dilampirkan pada rekod akaun, sistem akan mencari senarai harga jualan yang dilampirkan pada parameter projek yang sepadan dengan mata wang kontrak projek.
1. Seterusnya, sistem akan menyemak tempoh kuat kuasa tarikh senarai harga yang sepadan dengan julat tarikh kontrak projek. Khususnya, tarikh yang kontrak dicipta.
1. Jika terdapat berbilang senarai harga yang berkuat kuasa untuk tarikh kontrak, semua senarai harga dijadikan lalai pada kontrak.
1. Jika tiada senarai harga yang berkuat kuasa untuk tarikh kontrak, tidak akan ada senarai harga projek dijadikan lalai pada kontrak. Mesej amaran akan muncul pada kontrak projek. Mesej menyatakan bahawa nilai sebenar dan anggaran pada projek tidak akan diberikan harga kerana tiada senarai harga projek dilampirkan.

## <a name="cost-price-lists"></a>Senarai harga kos

Senarai harga kos tidak dijadikan lalai kepada mana-mana entiti dalam Project Operations. Menentukan senarai harga kos untuk digunakan untuk kos projek sentiasa dilakukan berdasarkan setiap transaksi. Sistem akan melengkapkan proses berikut untuk menentukan senarai harga untuk digunakan untuk kos projek:

1. Sistem ini melihat senarai harga yang dilampirkan pada unit organisasi kontrak projek.
1. Seterusnya, sistem melihat kesan tarikh senarai harga yang sepadan dengan tarikh konteks anggaran masuk atau konteks sebenar.

    - *Konteks anggaran* merujuk kepada mana-mana tiga konteks anggaran dalam Operasi Projek:

        - Baris anggaran projek
        - Butiran baris sebut harga
        - Butiran baris kontrak

    - *Konteks sebenar* merujuk kepada mana-mana tiga sumber untuk sebenar dalam Operasi Projek:

       - Baris jurnal entri yang dicipta secara manual, atau garis jurnal pembetulan yang dicipta dalam jurnal pembetulan
       - Baris jurnal yang dicipta semasa penyerahan masa, perbelanjaan, atau log penggunaan bahan
       - Butiran baris invois

    Apabila Operasi Projek sepadan dengan keberkesanan tarikh baris jurnal yang masuk atau butiran baris invois dalam *konteks* sebenar, ia menggunakan **medan Tarikh** transaksi.

    - Jika berbilang senarai harga berkuat kuasa untuk tarikh konteks anggaran masuk atau konteks sebenar, senarai harga yang paling baru dibuat dipilih.
    - Sekiranya tiada senarai harga dilampirkan pada unit organisasi kontrak projek, sistem melihat senarai harga kos yang dilampirkan pada parameter projek yang sepadan dengan mata wang projek.

## <a name="enable-multi-currency-cost-price-list"></a>Dayakan berbilang mata wang senarai harga kos

Tetapan ini boleh didapati di **Parameter** Tetapan \>**·**. Nilai lalai ialah **Tidak**.

Apabila seting ini didayakan (iaitu nilai disetkan kepada **Ya**), sistem berkelakuan dengan cara berikut:

- Ia membolehkan senarai harga kos dalam mana-mana mata wang dikaitkan dengan unit organisasi. Sebagai contoh, senarai harga kos dalam mata wang EUR boleh dilampirkan pada unit organisasi dalam mata wang USD. Sistem ini akan terus mengesahkan bahawa senarai harga kos yang dilampirkan pada unit organisasi tidak mempunyai kesan tarikh bertindih.
- Ia mengesahkan bahawa senarai harga kos yang dilampirkan pada parameter projek tidak mempunyai kesan tarikh bertindih, walaupun mereka mempunyai mata wang yang berbeza. Kelakuan ini berbeza daripada kelakuan lalai (iaitu, kelakuan apabila nilai disetkan kepada **Tidak**). Dalam kelakuan lalai, hanya senarai harga kos yang mempunyai **mata wang yang sama** disahkan untuk kesan tarikh yang tidak bertindih.
- Untuk konteks transaksi yang masuk, ia menentukan senarai harga kos berdasarkan kesan tarikh sahaja. Tingkah laku ini berbeza daripada tingkah laku lalai, di mana sistem memilih senarai harga kos yang sepadan dengan kedua-dua mata wang projek dan kesan tarikh.

Oleh kerana perubahan tingkah laku ini, pelanggan Operasi Projek akan dapat mengekalkan senarai harga kos global yang relevan untuk seluruh syarikat. Mereka tidak perlu mempunyai senarai harga dalam setiap mata wang operasi. Senarai harga global akan mempunyai kesan tarikh dan akan membolehkan kadar kos ditetapkan dalam mana-mana mata wang untuk gabungan nilai dimensi harga tertentu. Mata wang senarai harga kos hanya digunakan untuk memasukkan nilai lalai apabila **Harga peranan**, **harga** Kategori dan **rekod item senarai** harga dicipta. Ia tidak akan digunakan untuk menentukan senarai harga.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
