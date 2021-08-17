---
title: Transaksi perniagaan
description: Topik ini menyediakan maklumat mengenai transaksi perniagaan.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 28555f29e65c11255c8966f3d4b900512aa01c30fef0a9cef3a3794edaf92a0b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987537"
---
# <a name="business-transactions"></a>Transaksi perniagaan

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dalam Dynamics 365 Project Service Automation, *transaksi perniagaan* ialah konsep abstrak yang tidak diwakili oleh sebarang entiti. Walau bagaimanapun, beberapa medan dan proses biasa pada entiti direka bentuk untuk menggunakan konsep transaksi perniagaan. Entiti berikut menggunakan pengabstrakan ini:

- Butiran baris sebut harga
- Butiran baris kontrak
- Garisan anggaran
- Garisan jurnal
- Sebenar

Bagi entiti ini, butiran baris Sebut Harga, butiran baris Kontrak dan baris Anggaran dipetakan ke fasa anggaran dalam kitaran hayat projek. Barisan Jurnal dan entiti Aktual dipetakan ke fasa pelaksanaan dalam kitaran hayat projek.

PSA melayan rekod dalam lima entiti ini sebagai transaksi perniagaan. Satu-satunya perbezaan adalah bahawa rekod dalam entiti yang dipetakan ke fasa anggaran dianggap ramalan kewangan, manakala rekod dalam entiti yang dipetakan ke fasa pelaksanaan dianggap sebagai fakta kewangan yang telah berlaku.

Untuk mendapatkan maklumat lanjut, lihat [Anggaran](estimates.md) dan [Aktual](actuals.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Konsep yang unik untuk transaksi perniagaan
Konsep berikut adalah unik kepada konsep transaksi perniagaan:

- Jenis transaksi
- Kelas transaksi
- Asal transaksi
- Sambungan transaksi

### <a name="transaction-type"></a>Jenis transaksi

Jenis transaksi mewakili masa dan konteks kesan kewangan ke atas projek. Ia diwakili oleh set pilihan yang mempunyai nilai disokong berikut dalam PSA:
- Kos
- Kontrak projek
- Jualan belum dibilkan
- Jualan dibilkan
- Jualan antara organisasi
- Kos unit persumberan

### <a name="transaction-class"></a>Kelas transaksi

Kelas transaksi mewakili jenis kos berbeza yang berlaku pada projek. Ia diwakili oleh set pilihan yang mempunyai nilai disokong berikut dalam PSA:

- Time
- Perbelanjaan
- Bahan
- Yuran
- Pencapaian
- Cukai

Nilai **Pencapaian** biasanya digunakan oleh logik perniagaan untuk pembayaran bil harga tetap dalam PSA.

### <a name="transaction-origin"></a>Asal transaksi

Asal transaksi ialah entiti yang menyimpan asal bagi setiap transaksi perniagaan. Apabila pelaksanaan projek dijalankan, setiap urus niaga perniagaan akan menimbulkan urus niaga perniagaan lain yang akan menghasilkan satu lagi urus niaga perniagaan dan seterusnya. Entiti asal urus niaga direka bentuk untuk menyimpan data tentang setiap asal urus niaga untuk membantu pelaporan dan kebolehjejakan. 

### <a name="transaction-connection"></a>Sambungan transaksi

Sambungan transaksi ialah entiti yang menyimpan hubungan antara dua urus niaga perniagaan yang sama seperti kos dan aktual jualan berkaitan atau pembalikan transaksi yang dicetuskan oleh aktiviti pengebilan seperti pengesahan invois atau pembetulan invois.

Bersama-sama, asal Transaksi dan entiti sambungan Transaksi membantu anda menjejaki perhubungan antara transaksi perniagaan dengan tindakan yang menyebabkan penciptaan transaksi perniagaan khusus.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Contoh: Cara transaksi asal berfungsi dengan sambungan Transaksi

Contoh berikut menunjukkan pemprosesan biasa bagi entri masa dalam kitaran hayat projek PSA.

> ![Pemprosesan entri masa dalam kitaran hayat Project Service.](media/basic-guide-17.png)
 
1. Penyerahan entri masa menyebabkan penciptaan dua baris jurnal: satu untuk kos dan satu untuk jualan yang tidak dibilkan.
2. Pelulus akhir bagi entri masa menyebabkan penciptaan dua aktual: satu untuk kos dan satu untuk jualan yang tidak dibilkan.
3. Apabila pengguna mencipta invois projek, transaksi baris invois dicipta menggunakan data daripada aktual jualan yang tidak dibilkan. 
4. Apabila invois disahkan, dua aktual baharu dicipta: pembalikan jualan yang belum dibilkan dan aktual jualan yang dibilkan.

Setiap peristiwa ini mencetuskan penciptaan rekod dalam asal Transaksi dan entiti sambungan Transaksi untuk membantu membina jejak hubungan antara rekod yang dicipta merentasi entri masa, baris jurnal, aktual dan butiran baris invois.

Jadual berikut menunjukkan rekod dalam entiti asal Transaksi untuk aliran kerja sebelumnya.

| Peristiwa                        | Asal                   | Jenis asal                       | Transaksi                       | Jenis transaksi         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Penyerahan Entri Masa        | GUID Rekod entri masa   | Entri Masa                        | GUID Rekod Garisan Jurnal (kos)   | Garisan Jurnal             |
| GUID Rekod entri masa       | Entri Masa               | GUID Rekod Garisan Jurnal (jualan)  | Garisan Jurnal                      |                          |
| Kelulusan Masa                | GUID Rekod Garisan Jurnal | Garisan Jurnal                      | GUID Rekod Jualan Belum Dibilkan        | Sebenar                   |
| GUID Rekod entri masa       | Entri Masa               | GUID Rekod Jualan Belum Dibilkan        | Sebenar                            |                          |
| GUID Rekod Garisan Jurnal     | Garisan Jurnal             | GUID Rekod Aktual Kos           | Sebenar                            |                          |
| GUID Rekod entri masa       | Entri Masa               | GUID Rekod Aktual Kos           | Sebenar                            |                          |
| Penciptaan Invois             | GUID Rekod entri masa   | Entri Masa                        | GUID Transaksi Baris Invois     | Transaksi Baris Invois |
| GUID Rekod Garisan Jurnal     | Garisan Jurnal             | GUID Transaksi Baris Invois     | Transaksi Baris Invois          |                          |
| Pengesahan Invois         | GUID Baris Invois        | Baris Invois                      | GUID Rekod Jualan Dibilkan          | Sebenar                   |
| GUID Invois                 | Invois                  | GUID Rekod Jualan Dibilkan          | Sebenar                            |                          |
| GUID Butiran Baris Invois     | Butiran Baris Invois      | GUID Rekod Jualan Dibilkan          | Sebenar                            |                          |
| GUID Rekod entri masa       | Entri Masa               | GUID Rekod Jualan Dibilkan          | Sebenar                            |                          |
| GUID Rekod Garisan Jurnal     | Garisan Jurnal             | GUID Rekod Jualan Dibilkan          | Sebenar                            |                          |
| GUID Rekod entri masa       | Entri Masa               | GUID Pembalikan Jualan Belum Dibilkan      | Sebenar                            |                          |
| GUID Rekod Garisan Jurnal     | Garisan Jurnal             | GUID Pembalikan Jualan Belum Dibilkan      | Sebenar                            |                          |
| Pembetulan Invois Draf     | GUID ILD Lama             | Transaksi Baris Invois          | GUID ILD Pembetulan               | Transaksi Baris Invois |
| GUID IL Lama                  | Baris Invois             | GUID ILD Pembetulan               | Transaksi Baris Invois          |                          |
| GUID Invois Lama             | Invois                  | GUID ILD Pembetulan               | Transaksi Baris Invois          |                          |
| GUID Rekod entri masa       | Entri Masa               | GUID ILD Pembetulan               | Transaksi Baris Invois          |                          |
| GUID Rekod Garisan Jurnal     | Garisan Jurnal             | GUID ILD Pembetulan               | Transaksi Baris Invois          |                          |
| Pembetulan invois yang disahkan | GUID ILD Lama             | Transaksi Baris Invois          | GUID Aktual Jualan Dibilkan yang Dibalikkan | Sebenar                   |
| GUID IL Lama                  | Baris Invois             | GUID Aktual Jualan Dibilkan yang Dibalikkan | Sebenar                            |                          |
| GUID Invois Lama             | Invois                  | GUID Aktual Jualan Dibilkan yang Dibalikkan | Sebenar                            |                          |
| GUID Rekod entri masa       | Entri Masa               | GUID Aktual Jualan Dibilkan yang Dibalikkan | Sebenar                            |                          |
| GUID Rekod Garisan Jurnal     | Garisan Jurnal             | GUID Aktual Jualan Dibilkan yang Dibalikkan | Sebenar                            |                          |
| GUID ILD Lama                 | Transaksi Baris Invois | GUID Aktual Jualan Belum Dibilkan Baharu    | Sebenar                            |                          |
| GUID IL Lama                  | Baris Invois             | GUID Aktual Jualan Belum Dibilkan Baharu    | Sebenar                            |                          |
| GUID Invois Lama             | Invois                  | GUID Aktual Jualan Belum Dibilkan Baharu    | Sebenar                            |                          |
| GUID Rekod entri masa       | Entri Masa               | GUID Aktual Jualan Belum Dibilkan Baharu    | Sebenar                            |                          |
| GUID Rekod Garisan Jurnal     | Garisan Jurnal             | GUID Aktual Jualan Belum Dibilkan Baharu    | Sebenar                            |                          |
| GUID ILD Pembetulan          | Transaksi Baris Invois | GUID Aktual Jualan Belum Dibilkan Baharu    | Sebenar                            |                          |
| GUID IL Pembetulan           | Baris Invois             | GUID Aktual Jualan Belum Dibilkan Baharu    | Sebenar                            |                          |
| GUID Invois Pembetulan      | Invois                  | GUID Aktual Jualan Belum Dibilkan Baharu    | Sebenar                            |                          |

Jadual berikut menunjukkan rekod dalam entiti pembetulan Transaksi untuk aliran kerja sebelumnya.

| Peristiwa                          | Transaksi 1                 | Peranan Transaksi 1 | Jenis Transaksi 1           | Transaksi 2                | Peranan Transaksi 2 | Jenis Transaksi 2 |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Penyerahan Entri Masa          | GUID Garisan Jurnal (Jualan)     | Jualan Belum Dibilkan     | msdyn_journalline            | GUID Garisan Jurnal (kos)     | Kos               | msdyn_journalline  |
| Kelulusan Masa                  | GUID Aktual Belum Dibilkan (Jualan)  | Jualan Belum Dibilkan     | msdyn_actual                 | GUID Aktual Kos (kos)       | Kos               | msdyn_actual       |
| Penciptaan Invois               | GUID Butiran Baris Invois      | Jualan Dibilkan       | msdyn_invoicelinetransaction | GUID Aktual Jualan Belum Dibilkan   | Jualan Belum Dibilkan     | msdyn_actual       |
| Pengesahan Invois           | Menterbalikkan GUID Aktual         | Menterbalikkan          | msdyn_actual                 | GUID jualan belum dibilkan asal | Asal           | msdyn_actual       |
| GUID Jualan Dibilkan              | Jualan Dibilkan                  | msdyn_actual       | GUID Aktual Jualan Belum Dibilkan   | Jualan Belum Dibilkan               | msdyn_actual       |                    |
| Pembetulan Invois Draf       | GUID Transaksi Baris Invois | Menggantikannya          | msdyn_invoicelinetransaction | GUID Jualan Dibilkan            | Asal           | msdyn_actual       |
| Sahkan Pembetulan Invois     | GUID Pembalikan Jualan Dibilkan    | Menterbalikkan          | msdyn_actual                 | GUID Jualan Dibilkan            | Asal           | msdyn_actual       |
| GUID Aktual Jualan Belum Dibilkan Baharu | Menggantikan                     | msdyn_actual       | GUID Jualan Dibilkan            | Asal                     | msdyn_actual       |                    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]