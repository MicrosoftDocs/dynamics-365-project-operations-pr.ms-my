---
title: Sambungan transaksi - Pautkan aktual jenis transaksi yang berbeza
description: Topik ini menerangkan bagaimana sambungan transaksi digunakan untuk menghubungkan sebenar jenis yang berbeza untuk membantu mengesan keuntungan, tunggakan pengebilan, dan dibilkan berbanding pengiraan hasil yang belum dibilkan.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2e8d75a69e27619e6a21f0fe61e2c656e94017b0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580789"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Sambungan transaksi - Pautkan aktual jenis transaksi yang berbeza

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Rekod sambungan transaksi dicipta untuk memautkan aktual jenis yang berbeza apabila masa, perbelanjaan atau penggunaan bahan bergerak dalam kitaran hayatnya daripada peringkat sebut harga atau pra-jualan ke peringkat kontrak, kelulusan dan/atau penarikan balik, invois dan potensi penginvoisan kredit atau pembetulan.

Contoh berikut menunjukkan pemprosesan biasa bagi entri masa dalam kitaran hayat projek Project Operations.

> ![Memproses entri masa dalam Operasi Projek.](media/basic-guide-17.png)

Pemprosesan entri masa dalam kitaran hayat projek Project Operations mengikuti langkah-langkah berikut: 

1. Penyerahan entri masa menyebabkan dua baris jurnal dibuat: satu untuk kos dan satu untuk jualan yang tidak dibilkan. 
2. Kelulusan akhir kemasukan masa menyebabkan dua aktual dibuat: satu untuk kos dan satu untuk jualan yang tidak dibilkan. 2 sebenar ini dihubungkan menggunakan sambungan transaksi.
3. Apabila pengguna mencipta invois projek, transaksi baris invois dicipta menggunakan data daripada aktual jualan yang tidak dibilkan.
4. Apabila invois disahkan, ini mencipta dua sebenar baharu: pembalikan jualan yang tidak dibilkan dan sebenar jualan yang dibilkan. Pembalikan jualan yang tidak dibilkan dan jualan asal yang belum dibilkan sebenarnya disambungkan menggunakan sambungan transaksi terbalik. Jualan yang dibilkan dan sebenar jualan asal yang belum dibilkan juga dihubungkan untuk menunjukkan hubungan antara apa yang pernah tertunggak atau hasil kerja yang sedang berjalan (WIP) dengan apa yang kini dibilkan pendapatan.   

Setiap peristiwa dalam aliran kerja pemprosesan mencetuskan penciptaan rekod dalam **jadual sambungan** Transaksi. Ini membantu membina jejak hubungan antara rekod yang dicipta merentasi entri masa, baris jurnal, butiran baris sebenar dan invois.

Jadual berikut menunjukkan rekod dalam **entiti sambungan** Transaksi untuk aliran kerja sebelumnya.

|Peristiwa                   |Transaksi 1                 |Peranan Transaksi 1 |Jenis Transaksi 1       |Transaksi 2          |Peranan Transaksi 2 |Jenis Transaksi 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Penyerahan Entri Masa   |GUID Garisan Jurnal (Jualan)     |Jualan Belum Dibilkan |msdyn_journalline            |GUID Garisan Jurnal (kos)     |Kos            |msdyn_journalline  |
|Kelulusan Masa           |GUID Aktual Belum Dibilkan (Jualan)  |Jualan Belum Dibilkan |msdyn_actual                 |GUID Aktual Kos (kos)       |Kos            |msdyn_actual       |
|Penciptaan Invois        |GUID Butiran Baris Invois      |Jualan Dibilkan   |msdyn_invoicelinetransaction |GUID Aktual Jualan Belum Dibilkan   |Jualan Belum Dibilkan  |msdyn_actual       |
|Pengesahan Invois    |Menterbalikkan GUID Aktual         |Menterbalikkan      |msdyn_actual                 |GUID jualan belum dibilkan asal |Asal        |msdyn_actual       |
|                        |GUID Jualan Dibilkan             |Jualan Dibilkan   |msdyn_actual                 |GUID Aktual Jualan Belum Dibilkan   |Jualan Belum Dibilkan  |msdyn_actual       |
|Pembetulan Invois Draf |GUID Transaksi Baris Invois|Menggantikannya      |msdyn_invoicelinetransaction |GUID Jualan Dibilkan            |Asal        |msdyn_actual       |
|Sahkan Pembetulan Invois|GUID Pembalikan Jualan Dibilkan  |Menterbalikkan      |msdyn_actual                 |GUID Jualan Dibilkan            |Asal        |msdyn_actual       |
|                        |GUID Jualan Belum Dibilkan Baru |Menggantikannya            |msdyn_actual                 |GUID Jualan Dibilkan            |Asal        |msdyn_actual       |


Ilustrasi berikut menunjukkan pautan yang dicipta antara pelbagai jenis sebenar pada pelbagai acara menggunakan contoh entri masa dalam Operasi Projek.

> ![Bagaimana sebenar jenis yang berbeza dipautkan antara satu sama lain dalam Operasi Projek.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
