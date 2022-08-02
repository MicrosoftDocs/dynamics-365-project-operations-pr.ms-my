---
title: Senarai harga lalai
description: Artikel ini menyediakan maklumat tentang jualan lalai dan senarai harga kos dalam Operasi Projek.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 99af12577abeb0b77dc5d8a117d1e3b292bf0b80
ms.sourcegitcommit: 260368e1d0751db713da073a641c63c04876fcdf
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/22/2022
ms.locfileid: "9036422"
---
# <a name="default-price-lists"></a>Senarai harga lalai

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

## <a name="sales-price-lists"></a>Senarai harga jualan

Setiap sebut harga projek dan kontrak dalam Dynamics 365 Project Operations mengandungi senarai harga jualan lalai. 

### <a name="price-list-default-on-project-quotes"></a>Senarai harga dijadikan lalai pada sebut harga projek
Sistem akan melengkapkan proses berikut untuk menentukan senarai harga untuk dijadikan lalai pada sebut harga projek:

1. Sistem melihat senarai harga yang dilampirkan pada senarai harga projek akaun. 
2. Sekiranya tidak ada senarai harga projek yang dilampirkan pada rekod akaun, sistem melihat senarai harga jualan yang dilampirkan pada parameter projek yang sepadan dengan mata wang sebut harga projek.
3. Seterusnya, sistem akan menyemak tempoh kuat kuasa tarikh senarai harga yang sepadan dengan julat tarikh sebut harga projek. Khususnya, tarikh yang sebut harga dicipta.
4. Jika terdapat berbilang senarai harga yang berkuat kuasa untuk tarikh sebut harga projek, semua senarai harga dijadikan lalai pada sebut harga projek.
5. Jika tiada senarai harga yang berkuat kuasa untuk tarikh sebut harga projek, tidak akan ada senarai harga projek dijadikan lalai pada sebut harga projek. Mesej amaran akan muncul pada sebut harga projek. Mesej menyatakan bahawa nilai sebenar dan anggaran pada projek tidak akan diberikan harga kerana tiada senarai harga projek dilampirkan.

### <a name="price-list-default-on-project-contracts"></a>Senarai harga yang dijadikan lalai pada kontrak projek 
Sistem akan melengkapkan proses berikut untuk menentukan senarai harga untuk dijadikan lalai pada kontrak projek:

1. Jika kontrak dicipta daripada sebut harga, senarai harga projek pada sebut harga disalin secara berasingan dan dilampirkan pada kontrak projek.
2. Jika kontrak dicipta daripada kosong, sistem akan melihat senarai harga yang dilampirkan pada senarai harga projek akaun. Jika tiada senarai harga projek yang dilampirkan pada rekod akaun, sistem akan mencari senarai harga jualan yang dilampirkan pada parameter projek yang sepadan dengan mata wang kontrak projek.
4. Seterusnya, sistem akan menyemak tempoh kuat kuasa tarikh senarai harga yang sepadan dengan julat tarikh kontrak projek. Khususnya, tarikh yang kontrak dicipta.
5. Jika terdapat berbilang senarai harga yang berkuat kuasa untuk tarikh kontrak, semua senarai harga dijadikan lalai pada kontrak.
6. Jika tiada senarai harga yang berkuat kuasa untuk tarikh kontrak, tidak akan ada senarai harga projek dijadikan lalai pada kontrak. Mesej amaran akan muncul pada kontrak projek. Mesej menyatakan bahawa nilai sebenar dan anggaran pada projek tidak akan diberikan harga kerana tiada senarai harga projek dilampirkan.

## <a name="cost-price-lists"></a>Senarai harga kos

Senarai harga kos tidak dijadikan lalai kepada mana-mana entiti dalam Project Operations. Menentukan senarai harga kos untuk digunakan untuk kos projek sentiasa dilakukan pada masa ini. Sistem akan melengkapkan proses berikut untuk menentukan senarai harga untuk digunakan untuk kos projek:

1. Pertama sekali, sistem akan melihat senarai harga yang dilampirkan pada unit organisasi kontrak projek.
2. Sistem kemudian akan melihat pada tarikh kuat kuasa senarai harga yang sepadan dengan tarikh anggaran masuk atau baris sebenar. Dalam situasi ini, *baris anggaran* merujuk kepada ketiga-tiga konteks anggaran dalam Project Operations:

    - Baris anggaran projek
    - Butiran baris sebut harga
    - Butiran baris kontrak
  
3. Jika terdapat berbilang senarai harga yang berkuat kuasa untuk tarikh pada anggaran masuk atau sebenar, senarai harga yang paling baru dicipta akan dipilih.
4. Jika tiada senarai harga dilampirkan pada unit organisasi kontrak projek, sistem akan melihat senarai harga jualan yang dilampirkan pada parameter projek yang sepadan dengan mata wang projek.
5. Seterusnya, sistem akan melihat tarikh kuat kuasa senarai harga yang sepadan dengan tarikh anggaran masuk atau baris sebenar. 
6. Jika terdapat berbilang senarai harga yang berkuat kuasa untuk tarikh pada anggaran masuk atau sebenar, senarai harga yang paling baru dicipta akan dipilih.
7. Jika tiada senarai harga kos yang dilampirkan pada parameter projek yang sepadan dengan mata wang dan tarikh kuat kuasa, sistem membuat kadar kos kepada sifar (0) pada anggaran masuk atau baris sebenar secara lalai.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
