---
title: Pautkan aktual pada rekod asal
description: Topik ini menerangkan cara memautkan aktual pada rekod asal seperti entri masa, entri perbelanjaan atau log penggunaan bahan.
author: rumant
manager: tfehr
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 545775c4eae6c3dc689f264e7f662471c17b2340
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852600"
---
# <a name="link-actuals-to-original-records"></a>Pautkan aktual pada rekod asal

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_


Dalam Dynamics 365 Project Operations, *transaksi perniagaan* ialah konsep abstrak yang tidak diwakili oleh entiti. Walau bagaimanapun, beberapa medan dan proses biasa pada entiti direka bentuk untuk menggunakan konsep transaksi perniagaan. Entiti berikut menggunakan konsep ini:

- Butiran baris sebut harga
- Butiran baris kontrak
- Garisan anggaran
- Garisan jurnal
- Sebenar

Daripada entiti ini, **Butiran baris sebut harga**, **Butiran baris kontrak** dan **Baris anggaran** dipetakan ke fasa anggaran dalam kitaran hayat projek. **Garisan jurnal** dan **Entiti aktual** dipetakan ke fasa pelaksanaan dalam kitaran hayat projek.

Project Operations mengecam rekod dalam lima entiti ini sebagai transaksi perniagaan. Satu-satunya perbezaan adalah bahawa rekod dalam entiti yang dipetakan ke fasa anggaran dianggap ramalan kewangan, manakala rekod dalam entiti yang dipetakan ke fasa pelaksanaan dianggap sebagai fakta kewangan yang telah berlaku.

## <a name="concepts-that-are-unique-to-business-transactions"></a>Konsep yang unik untuk transaksi perniagaan
Konsep berikut adalah unik kepada konsep transaksi perniagaan:

- Jenis transaksi
- Kelas transaksi
- Asal transaksi
- Sambungan transaksi

### <a name="transaction-type"></a>Jenis transaksi

Jenis transaksi mewakili masa dan konteks kesan kewangan ke atas projek. Ini diwakili oleh set pilihan yang mempunyai nilai disokong berikut dalam Project Operations:

  - Kos
  - Kontrak projek
  - Jualan belum dibilkan
  - Jualan dibilkan
  - Jualan antara organisasi
  - Kos unit persumberan

### <a name="transaction-class"></a>Kelas transaksi

Kelas transaksi mewakili jenis kos berbeza yang berlaku pada projek. Ini diwakili oleh set pilihan yang mempunyai nilai disokong berikut dalam Project Operations:

  - Masa
  - Perbelanjaan
  - Bahan
  - Yuran
  - Pencapaian
  - Cukai

**Pencapaian** biasanya digunakan oleh logik perniagaan untuk pengebilan harga tetap dalam Project Operations.

### <a name="transaction-origin"></a>Asal transaksi

**Asal transaksi** ialah entiti yang menyimpan asal bagi setiap transaksi perniagaan. Apabila projek sedang berjalan, setiap transaksi perniagaan akan membawa kepada transaksi perniagaan lain yang seterusnya akan mencipta satu lain dan seterusnya. Entiti asal transaksi direka untuk menyimpan data tentang setiap asal transaksi untuk membantu dalam pelaporan dan keupayaan kesan. 

### <a name="transaction-connection"></a>Sambungan transaksi

**Sambungan transaksi** ialah entiti yang menyimpan hubungan antara dua transaksi perniagaan yang serupa, seperti kos dan aktual jualan berkaitan, atau pembalikan transaksi yang dicetuskan oleh aktiviti pengebilan seperti pengesahan invois atau pembetulan invois.

Kedua-dia, **Asal transaksi** dan **Sambungan transaksi** membantu anda menjejaki hubungan antara transaksi perniagaan dan tindakan yang menyebabkan transaksi perniagaan khusus.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Contoh: Cara transaksi asal berfungsi dengan sambungan Transaksi

Contoh berikut menunjukkan pemprosesan biasa bagi entri masa dalam kitaran hayat projek Project Operations.

> ![Pemprosesan entri masa dalam kitaran hayat Project Service](media/basic-guide-17.png)
 
1. Penyerahan entri masa mencipta dua garisan jurnal: satu baris untuk kos dan satu baris untuk jualan belum dibilkan.
2. Akhirnya kelulusan entri masa mencipta dua aktual: satu aktual untuk kos dan satu aktual untuk jualan belum dibilkan.
3. Apabila invois projek baharu dicipta, transaksi baris invois dicipta dengan menggunakan data daripada aktual jualan belum dibilkan. 
4. Apabila invois disahkan, dua aktual baharu dicipta: aktual pembalikan jualan belum dibilkan dan aktual jualan dibilkan.

Setiap peristiwa ini mencipta rekod dalam **Asal transaksi** dan entiti **Sambungan transaksi**. Rekod baharu ini membantu untuk membina sejarah hubungan antara rekod yang dicipta merentasi butiran entri masa, garisan jurnal, aktual dan baris invois.

Jadual berikut menunjukkan rekod dalam entiti **Asal transaksi** untuk aliran kerja.

| Peristiwa                        | Asalan                   | Jenis asal                       | Transaksi                       | Jenis transaksi         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Penyerahan Entri Masa        | GUID Rekod Entri Masa   | Entri Masa                        | GUID Rekod Garisan Jurnal (kos)   | Garisan Jurnal             |
| GUID Rekod entri masa       | Entri Masa               | GUID Rekod Garisan Jurnal (jualan)  | Garisan Jurnal                      |                          |
| Kelulusan Masa                | GUID Rekod Garisan Jurnal | Garisan Jurnal                      | GUID Rekod Jualan Belum Dibilkan        | Sebenar                   |
| GUID Rekod entri masa       | Entri Masa               | GUID Rekod Jualan Belum Dibilkan        | Sebenar                            |                          |
| GUID Rekod Garisan Jurnal     | Garisan Jurnal             | GUID Rekod Aktual Kos           | Sebenar                            |                          |
| GUID Rekod entri masa       | Entri Masa               | GUID Rekod Aktual Kos           | Aktual                            |                          |
| Penciptaan Invois             | GUID Rekod Entri Masa   | Entri Masa                        | GUID Transaksi Baris Invois     | Transaksi Baris Invois |
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

Jadual berikut menunjukkan rekod dalam entiti **Sambungan transaksi** untuk aliran kerja.

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
