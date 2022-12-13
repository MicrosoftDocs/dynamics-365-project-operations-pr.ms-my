---
title: Sediakan penukaran mata wang untuk mengira harga jualan daripada kadar kos
description: Artikel ini menerangkan cara mengkonfigurasi tingkah laku penukaran mata wang yang akan digunakan dalam Microsoft Dynamics 365 Project Operations apabila transaksi jualan dijana daripada transaksi kos.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816696"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Sediakan penukaran mata wang untuk mengira harga jualan daripada kadar kos

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Di Microsoft Dynamics 365 Project Operations, harga jualan untuk kategori perbelanjaan boleh disediakan sebagai nilai angka atau ia boleh disediakan supaya ia dikira berdasarkan kos yang ditanggung.

Apabila ia disediakan untuk dikira berdasarkan kos yang ditanggung, pilihan berikut tersedia:

- Pada kos
- Tandakan peratusan berbanding kos

Dalam senario di mana kos perbelanjaan ditanggung dalam mata wang yang berbeza daripada mata wang jualan untuk kontrak projek, penukaran mata wang diperlukan untuk mengira harga jualan berdasarkan kos.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Tingkah laku penukaran mata wang yang menggunakan kadar pertukaran asli Dataverse 

Secara lalai, Project Operations menggunakan kadar pertukaran mata wang yang disimpan dalam jadual Mata Wang Dataverse. Untuk mengkonfigurasi Operasi Projek untuk menggunakan kadar pertukaran asli untuk mengira harga jualan daripada kos, ikuti langkah-langkah ini.

1. Pergi ke **Parameter Tetapan \> Operasi \> Projek**.
1.  **Buka halaman butiran Parameter** Projek.
1. Setkan **medan logik** penukaran Mata Wang kepada nilai kosong.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>Kelakuan penukaran mata wang yang menggunakan kadar pertukaran daripada aplikasi kewangan dan operasi

Kadar pertukaran dalam jadual Mata Wang yang tersedia secara asli tidak Dataverse tarikh berkuat kuasa. Oleh itu, mereka mungkin tidak selalu diskalakan kepada keperluan yang anda miliki untuk pengiraan harga jualan dari kadar kos.

Anda boleh menggunakan kadar pertukaran dari persekitaran kewangan dan operasi untuk mengira harga jualan dalam mata wang jualan dari kadar kos dalam mata wang kos. Untuk mengkonfigurasi tingkah laku penukaran mata wang ini, ikuti langkah ini.

1.  **Pada halaman Parameter** projek, tambahkan **medan logik** penukaran Mata Wang. Kemudian simpan dan terbitkan penyesuaian.
1. Pergi ke **Parameter Tetapan \> Operasi \> Projek**.
1.  **Buka halaman butiran Parameter** Projek. 
1. Setkan **medan Kelakuan** penukaran Mata Wang kepada Dilanjutkan dengan sandaran balik kepada **lalai**.
1.  **Berikan pengguna aplikasi dwi-tulis peranan keselamatan**  **Pengguna aplikasi**  Global Baca kebenaran kepada jadual berikut:

    - MSDYN\_ CurrencyExchangerates
    - MSDYN\_ CurrencyExchangeratePairs
    - Msdyn\_ Exchangeratetypes

1. Dalam persekitaran kewangan dan operasi anda, jalankan peta dwi-tulis berikut dengan penyegerakan awal:

    - Jenis kadar pertukaran (msdyn\_ exchangeratetypes)
    - Pasangan mata wang kadar pertukaran (msdyn\_ currencyexchangeratepairs)
    - Kadar Pertukaran CDS (msdyn\_ currencyexchangerates)

Selepas perubahan ini selesai, dwi-tulis akan membuat kadar pertukaran dari persekitaran kewangan dan operasi yang terdapat di. Dataverse Operasi Projek kemudiannya akan menggunakan kadar pertukaran tersebut untuk menukar kadar kos ke dalam mata wang jualan kontrak.

> [!NOTE]
> Tingkah laku penukaran mata wang ini hanya terpakai kepada pengiraan harga jualan dari kadar kos. Ia tidak akan digunakan untuk mengira nilai mata wang asas secara generik. Nilai mata wang asas akan sentiasa menggunakan kadar pertukaran asli Dataverse , tidak kira sama ada anda melengkapkan prosedur ini.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
