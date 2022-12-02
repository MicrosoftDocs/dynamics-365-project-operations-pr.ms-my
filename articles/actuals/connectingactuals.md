---
title: Sambungan urus niaga - Pautan aktual bagi jenis urus niaga yang berbeza
description: Artikel ini menjelaskan cara sambungan transaksi digunakan untuk memautkan aktual jenis yang berbeza untuk membantu dalam menjejaki keberuntungan, tunggakan pengebilan dan pengiraan hasil dibilkan berbanding yang belum dibilkan.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 19a78336099f54c5d6b36a963a90b9fd77e3d0af
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926097"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Sambungan urus niaga - Pautan aktual bagi jenis urus niaga yang berbeza

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Rekod sambungan transaksi dicipta untuk memautkan aktual jenis yang berbeza apabila masa, perbelanjaan atau penggunaan bahan bergerak dalam kitaran hayatnya daripada peringkat sebut harga atau prajualan kepada peringkat kontrak, kelulusan dan/atau panggilan balik, penginvoisan dan berpotensi kredit atau pembetulan penginvoisan.

Contoh berikut menunjukkan pemprosesan biasa bagi entri masa dalam kitaran hayat projek Project Operations.

> ![Memproses entri masa dalam Project Operations.](media/basic-guide-17.png)

Pemprosesan entri masa dalam kitaran hayat projek Project Operations mengikuti langkah ini: 

1. Penyerahan entri masa menyebabkan dua garisan jurnal dicipta: satu untuk kos dan satu untuk jualan yang belum dibilkan. 
2. Pelulus akhir bagi entri masa menyebabkan dua aktual dicipta: satu untuk kos dan satu untuk jualan yang belum dibilkan. 2 aktual ini dipautkan dengan menggunakan sambungan transaksi.
3. Apabila pengguna mencipta invois projek, transaksi baris invois dicipta menggunakan data daripada aktual jualan yang tidak dibilkan.
4. Apabila invois disahkan, ini mencipta dua aktual baharu: pembalikan jualan yang belum dibilkan dan aktual jualan yang dibilkan. Pembalikan jualan yang belum dibilkan dan aktual jualan yang belum dibilkan asal disambungkan menggunakan sambungan transaksi yang membalikkan. Aktual jualan yang dibilkan dan jualan yang belum dibilkan asal juga disambungkan untuk menunjukkan pautan antara perkara yang pernah menjadi hasil tunggakan atau kerja yang sedang berjalan (WIP) kepada hasil yang dibilkan sekarang.   

Setiap peristiwa dalam aliran kerja pemprosesan mencetuskan penciptaan rekod dalam jadual **Sambungan transaksi**. Ini membantu untuk membina jejak hubungan antara rekod yang dicipta merentasi butiran entri masa, garisan jurnal, aktual dan baris invois.

Jadual berikut menunjukkan rekod dalam entiti **Pembetulan transaksi** untuk aliran kerja sebelumnya.

|Peristiwa                   |Transaksi 1                 |Peranan Transaksi 1 |Jenis Transaksi 1       |Transaksi 2          |Peranan Transaksi 2 |Jenis Transaksi 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Penyerahan Entri Masa   |GUID Garisan Jurnal (Jualan)     |Jualan Belum Dibilkan |msdyn_journalline            |GUID Garisan Jurnal (kos)     |Kos            |msdyn_journalline  |
|Kelulusan Masa           |GUID Aktual Belum Dibilkan (Jualan)  |Jualan Belum Dibilkan |msdyn_actual                 |GUID Aktual Kos (kos)       |Kos            |msdyn_actual       |
|Penciptaan Invois        |GUID Butiran Baris Invois      |Jualan Dibilkan   |msdyn_invoicelinetransaction |GUID Aktual Jualan Belum Dibilkan   |Jualan Belum Dibilkan  |msdyn_actual       |
|Pengesahan Invois    |Menterbalikkan GUID Aktual         |Menterbalikkan      |msdyn_actual                 |GUID jualan belum dibilkan asal |Asal        |msdyn_actual       |
|                        |GUID Jualan Dibilkan             |Jualan Dibilkan   |msdyn_actual                 |GUID Aktual Jualan Belum Dibilkan   |Jualan Belum Dibilkan  |msdyn_actual       |
|Pembetulan Invois Draf |GUID Transaksi Baris Invois|Menggantikannya      |msdyn_invoicelinetransaction |GUID Jualan Dibilkan            |Asal        |msdyn_actual       |
|Sahkan Pembetulan Invois|GUID Pembalikan Jualan Dibilkan  |Menterbalikkan      |msdyn_actual                 |GUID Jualan Dibilkan            |Asal        |msdyn_actual       |
|                        |GUID Jualan Belum Dibilkan Baharu |Menggantikannya            |msdyn_actual                 |GUID Jualan Dibilkan            |Asal        |msdyn_actual       |


Ilustrasi berikut menunjukkan pautan yang dicipta antara jenis aktual yang berbeza pada pelbagai peristiwa menggunakan contoh entri masa dalam Project Operations.

> ![Cara aktual jenis yang berbeza dipautkan antara satu sama lain dalam Project Operations.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
