---
title: Senario berbilang mata wang (versi 3.x)
description: Topik ini menyediakan maklumat tentang senario berbilang mata wang.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4b589142-952d-4121-ab5c-3aa7a85690e2
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d9dbd7755e2dc4bd33f264feb7d8bf9f2a4a0787
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753868"
---
# <a name="multiple-currency-scenarios"></a>Senario berbilang mata wang

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 mempunyai dua konsep mata wang:

- **Mata wang transaksi** - Mata wang yang berlaku pada transaksi. 
- **Mata wang asas** - Mata wang tika Dynamics 365. Mata wang ini ditetapkan apabila tika Dynamics 365 diperuntukkan. Ia tidak boleh ditukar.

Sebagai contoh, Contoso AS telah menjual 100 kemeja-T kepada pelanggan di UK untuk 15 paun sterling (GBP) setiap satu. Jadual berikut menunjukkan cara transaksi ini direkodkan dalam entiti Produk Pesanan.

| Produk | Kuantiti | Harga seunit | Mata Wang | Amaun | Kadar pertukaran | Harga setiap unit (Asas)| Amaun (Asas)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| Kemeja-T | 100      | 15             | GBP      | 1500   | 0.94          | $17.25               | $1,725       |

Lajur **Mata wang** menunjukkan mata wang transaksi, yang merupakan mata wang yang jualan tersebut berlaku. Lajur **Kadar pertukaran** ialah kadar pertukaran antara mata wang transaksi dan mata wang asas. Mata wang asas ialah dolar AS (USD). Mata wang asas ini telah ditetapkan apabila tika Dynamics 365 telah diperuntukkan.
Seperti yang jadual tunjukkan, setiap transaksi direkodkan dalam kedua-dua mata wang transaksi dan mata wang asas. Dynamics 365 menggunakan kadar pertukaran mata wang untuk mengira jumlah mata wang asas.

## <a name="project-service-automation-extensions"></a>Pelanjutan Project Service Automation

Dynamics 365 Project Service Automation mempengaruhi mata wang transaksi, kerana transaksi perniagaan biasanya mempunyai dua aspek: kos dan jualan.

Entiti berikut dikira sebagai transaksi perniagaan:

- Butiran baris sebut harga
- Butiran baris kontrak projek
- Garisan anggaran
- Garisan jurnal
- Butiran baris invois
- Sebenar

Dalam setiap entiti ini, terdapat rekod yang mewakili jumlah kos atau jumlah jualan. Bagi mana-mana entiti Dynamics 365 yang mempunyai medan **Amaun**, setiap rekod termasuk jumlah dalam kedua-dua mata wang transaksi dan mata wang asas. 

PSA meluaskan konsep mata wang urus niaga untuk kos dan jualan dengan cara berikut:

- Mata wang transaksi kos untuk transaksi masa sentiasa datang daripada mata wang unit organisasi yang memiliki atau menguruskan projek. Unit organisasi ini dikenali sebagai unit kontrak.
- Mata wang transaksi jualan untuk masa dan transaksi perbelanjaan sentiada datang daripada mata wang kontrak projek.
- Mata wang transaksi kos untuk perbelanjaan datang dari mata wang yang kemasukan perbelanjaan telah dicipta.

## <a name="multiple-currency-scenario"></a>Senario berbilang mata wang

Bahagian ini menerangkan contoh projek yang Contoso UK sampaikan untuk pelanggan yang bernama Fabrikam, Jepun. Berikut ialah cara senario yang telah disediakan:

1. GBP dan Yen Jepun (JPY) disediakan dibawah **Tetapan** \> **Pengurusan Perniagaan** \> **Mata Wang**. 
2. Akaun pelanggan yang dinamakan **Fabrikam - Japan** disediakan dan JPY dipilih sebagai mata wang pada akaun.
3. Unit organisasi yang dinamakan **Contoso UK** ditetapkan, dan GBP dipilih sebagai mata wang.
4. Kontrak projek dicipta, yang **Contoso UK** ditetapkan sebagai unit kontrak dan **Fabrikam – Japan** ditetapkan sebagai pelanggan.
5. Baris kontrak projek dicipta, berdasarkan susunan pengebilan untuk pelbagai kelas transaksi pada projek, seperti pengebilan untuk masa berbanding pengebilan untuk perbelanjaan.
6. Projek dicipta di mana **Contoso UK** ditetapkan sebagai unit kontrak. Projek ini dicipta dan dipetakan ke baris kontrak projek.


Semasa anggaran yang menggunakan butiran baris sebut harga, butiran baris kontrak projek, atau pada baris anggaran jadual, dua rekod sentiasa dicipta dalam entiti. Satu rekod ialah untuk kos, dan rekod lain ialah untuk jualan.

- Secara lalai, mata wang transaksi ke atas rekod kos ditetapkan kepada mata wang bagi unit kontrak projek. Dalam contoh ini, mata wang ialah GBP.
- Secara lalai, mata wang transaksi ke atas rekod jualan ditetapkan kepada mata wang bagi kontrak projek. Dalam contoh ini, mata wang ialah JPY.

Apabila aktual dicipta untuk masa menggunakan entri masa atau baris jurnal, tingkah laku berikut berlaku:

- Secara lalai, mata wang transaksi ke atas rekod kos ditetapkan kepada mata wang bagi unit kontrak projek.
- Secara lalai, mata wang transaksi ke atas rekod jualan ditetapkan kepada mata wang bagi kontrak projek.

Apabila aktual dicipta untuk perbelanjaan mengiut entri perbelanjaan atau baris jurnal, tingkah laku berikut berlaku:

- Anda boleh merakam jumlah perbelanjaan dalam sebarang mata wang. Pilih mata wang dengan menggunakan pemilih mata wang pada halaman **Entri Perbelanjaan** atau halaman **Garisan Jurnal**. Secara lalai, mata wang transaksi untuk rekod kos ditetapkan kepada mata wang ke atas entri perbelanjaan. 
- Secara lalai, mata wang transaksi untuk rekod jualan ialah mata wang bagi kontrak projek. Untuk menetapkan mata wang ini, sistem terlebih dahulu menukar jumlah transaksi dalam mata wang yang dimasukkan ke mata wang asas. Ia kemudian menukar jumlah untuk mata wang kontrak projek. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Gulung atas pengkomputeran apabila aktual projek direkodkan dalam mata wang transaksi berbilang

Dynamics 365 secara automatik mengendalikan gulung atas jumlah dalam mata wang yang berbeza. Berikut ialah contoh.

| Kelas transaksi | Jenis transaksi| Date   | Sumber | Kategori transaksi | Kuantiti | Harga unit | Amaun      | Kadar pertukaran | Amaun dalam asas |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Time              | Jualan belum dibilkan   | 14-Jun | Abu Talib  |                      | 8 jam    | 20,000 JPY    | 160,000 JPY | 123           | 1,300.81 USD    |
| Time              | Jualan belum dibilkan   | 15-Jun | Abu Talib  |                      | 8 jam    | 20,000 JPY    | 160,000 JPY | 123           | 1,300.81 USD    |
| Perbelanjaan           | Jualan belum dibilkan   | 16-Jun | Abu Talib  | Hotel                | 1 setiap satu     | 250 EUR      | 250 EUR     | 0.94          | 265.95 USD     |
| Perbelanjaan           | Jualan belum dibilkan   | 17-Jun | Abu Talib  | Sewa Kereta           | 1 setiap satu     | 150 EUR      | 150 EUR     | 0.94          | 159.57 USD     |

Untuk mengira jumlah nilai jualan belum dibilkan ke atas projek, anda boleh mencipta medan gulung atas untuk medan **Amaun** pada semua aktual jualan tidak dibilkan yang berkaitan. Medan gulung atas adalah pembinaan Dynamics 365 yang membolehkan untuk formula pantas pada rekod yang berkaitan.
