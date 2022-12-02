---
title: Senarai harga lalai
description: Artikel ini menyediakan maklumat tentang senarai harga jualan dan kos lalai dalam Project Operations.
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
1. Jika tiada senarai harga projek yang dilampirkan pada rekod akaun, sistem akan melihat senarai harga jualan yang dilampirkan pada parameter projek yang sepadan dengan mata wang sebut harga projek.
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

Senarai harga kos tidak dijadikan lalai kepada mana-mana entiti dalam Project Operations. Menentukan senarai harga kos untuk digunakan bagi kos projek sentiasa dilakukan berasaskan setiap transaksi. Sistem akan melengkapkan proses berikut untuk menentukan senarai harga untuk digunakan untuk kos projek:

1. Sistem melihat senarai harga yang dilampirkan pada unit organisasi kontrak projek.
1. Seterusnya, sistem melihat tarikh kuat kuasa senarai harga yang sepadan dengan tarikh konteks anggaran atau konteks aktual akan datang.

    - *Konteks anggaran* merujuk kepada mana-mana daripada tiga konteks anggaran dalam Project Operations:

        - Baris anggaran projek
        - Butiran baris sebut harga
        - Butiran baris kontrak

    - *Konteks aktual* merujuk kepada mana-mana daripada tiga sumber bagi aktual dalam Project Operations:

       - Garisan jurnal entri yang dicipta secara manual atau garisan jurnal pembetulan yang dicipta dalam jurnal pembetulan
       - Garisan jurnal yang dicipta semasa penyerahan masa, perbelanjaan atau log penggunaan bahan
       - Butiran baris invois

    Apabila Project Operations sepadan dengan tarikh kuat kuasa butiran garisan jurnal atau baris invois akan datang dalam *konteks aktual*, ia menggunakan medan **Tarikh transaksi**.

    - Jika berbilang senarai harga berkuat kuasa untuk tarikh konteks anggaran atau konteks aktual akan datang, senarai harga yang paling baru dicipta akan dipilih.
    - Jika tiada senarai harga dilampirkan pada unit organisasi kontrak projek, sistem akan melihat senarai harga jualan yang dilampirkan pada parameter projek yang sepadan dengan mata wang projek.

## <a name="enable-multi-currency-cost-price-list"></a>Dayakan berbilang mata wang senarai harga kos

Tetapan ini boleh ditemukan pada **Tetapan** \> **Parameter**. Nilai lalai ialah **Tidak**.

Apabila tetapan ini didayakan (iaitu, nilai ditetapkan kepada **Ya**), sistem berkelakuan seperti berikut:

- Ia membenarkan senarai harga kos dalam apa-apa mata wang dikaitkan dengan unit organisasi. Contohnya, senarai harga kos dalam mata wang EUR boleh dilampirkan kepada unit organisasi dalam mata wang USD. Sistem akan terus mengesahkan bahawa senarai harga kos yang dilampirkan pada unit organisasi tidak mempunyai tarikh kuat kuasa yang bertindan.
- Ia mengesahkan bahawa senarai harga kos yang dilampirkan pada parameter projek tidak mempunyai tarikh kuat kuasa yang bertindan, walaupun mempunyai mata wang yang berbeza. Tingkah laku ini berbeza daripada tingkah laku lalai (iaitu, tingkah laku apabila nilai ditetapkan kepada **Tidak**). Dalam tingkah laku lalai, hanya senarai harga kos yang mempunyai mata wang yang **sama** disahkan untuk tarikh kuat kuasa yang tidak bertindan.
- Untuk konteks transaksi yang akan datang, ia menentukan senarai harga kos berdasarkan pada tarikh kuat kuasa sahaja. Tingkah laku ini berbeza daripada tingkah laku lalai, iaitu sistem memilih senarai harga kos yang sepadan dengan kedua-dua mata wang projek dan tarikh kuat kuasa.

Disebabkan perubahan dalam tingkah laku ini, pelanggan Project Operations akan dapat mengekalkan senarai harga kos global yang akan berkaitan untuk seluruh syarikat. Mereka tidak perlu mempunyai senarai harga dalam setiap mata wang operasi. Senarai harga global akan mempunyai tarikh kuat kuasa dan akan membolehkan kadar kos untuk ditetapkan dalam apa-apa mata wang untuk kombinasi khusus nilai dimensi penetapan harga. Mata wang senarai harga kos digunakan hanya untuk memasukkan nilai lalai apabila rekod item **Harga peranan**, **Harga kategori** dan **Senarai harga** dicipta. Ia tidak akan digunakan untuk menentukan senarai harga.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
