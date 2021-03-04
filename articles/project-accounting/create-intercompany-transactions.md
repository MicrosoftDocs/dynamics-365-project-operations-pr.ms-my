---
title: Cipta transaksi antara syarikat
description: Topik ini menyediakan maklumat tentang cara mencipta transaksi antara syarikat.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0a9d34d69ff59f0cb470bb852d8a80ecaedf6544
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595521"
---
# <a name="create-intercompany-transactions"></a>Cipta transaksi antara syarikat

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Transaksi antara syarikat ialah transaksi masa dan perbelanjaan daripada kontrak projek yang dimiliki oleh satu syarikat atau unit organisasi, sementara sumber pada kontrak projek adalah sebahagian daripada syarikat atau unit organisasi yang berbeza.

Apabila transaksi antara syarikat diluluskan, transaksi sebenar berikut dicipta

| **Jenis transaksi** | **Senarai harga digunakan** | **Mata wang transaksi** |
| --- | --- | --- |
| Kos | Senarai harga kos unit kontrak | Mata wang pada baris harga |
| Jualan belum dibilkan. Ini dicipta hanya untuk aktual yang berkaitan dengan baris kontrak dengan jenis pengebilan, masa dan bahan. | Senarai harga jualan projek kontrak | Mata wang kontrak |
| Kos unit persumberan | Senarai harga kos unit sumber | Mata wang pada baris harga |
| Jualan unit antara organisasi | Senarai harga kos unit kontrak | Mata wang pada baris harga |

Kos, kos unit sumber dan penentuan harga transaksi jualan antara organisasi dan mata wang didorong oleh **unit organisasi**. Penting untuk diingati apabila menentukan cara untuk menstrukturkan syarikat dan unit organisasi dalam pelaksanaan anda.

Apabila anda mencipta peluang, sebut harga, kontrak projek dan rekod projek, sistem mengesahkan bahawa mata wang unit kontrak sepadan dengan mata wang perakaunan syarikat kontrak. Apabila tidak sama, rekod ini tidak boleh dicipta. Mata wang unit organisasi ditakrifkan dalam Dynamics 365 Project Operations dengan pergi ke **Dataverse** > **Tetapan** > **Unit organisasi**. Mata wang perakaunan syarikat ditakrifkan dalam Dynamics 365 Finance dengan pergi ke **Lejar umum** > **Persediaan lejar** > **Lejar**. Mata wang disegerakkan dengan persekitaran Dataverse anda dengan menggunakan peta Dwitulis Lejar.

Sistem mencipta kos unit sumber dan aktual jualan unit antara organisasi dalam situasi berikut:

  - Apabila unit sumber berbeza daripada unit kontrak
  - Apabila unit sumber berbeza daripada syarikat kontrak

Walau bagaimanapun, hanya transaksi yang mempunyai syarikat sumber yang berbeza daripada syarikat kontrak akan dipindahkan ke persekitaran Dynamics 365 Finance untuk perakaunan tambahan.

Perakaunan untuk aktual projek direkodkan dalam jurnal integrasi Project Operations dalam Kewangan. Sistem mencipta garisan jurnal berikut.

| **Jenis transaksi** | **Entiti yang sah** | **Cipta transaksi projek pada siaran** | **Dimensi kewangan lalai daripada** | **Kumpulan cukai jualan pengebilan dan kumpulan cukai jualan item pengebilan lalai** |
| --- | --- | --- | --- | --- |
| Kos | Tidak ditambah ke jurnal integrasi | T\A | T\A | T\A |
| Jualan belum dibilkan | Jurnal integrasi entiti sah pinjaman | Ya | Project | **Kumpulan cukai jualan pengebilan**: Berdasarkan **pelanggan kontrak** <br/> **Kumpulan cukai jualan item pengebilan**: Daripada kategori projek entiti sah semasa pada garisan jurnal |
| Kos unit persumberan | Jurnal integrasi entiti sah pinjaman | Tidak | Pelanggan antara syarikat | **Kumpulan cukai jualan pengebilan**: Berdasarkan **pelanggan antara syarikat** <br/> **Kumpulan cukai jualan item pengebilan**: Daripada kategori projek entiti sah semasa pada garisan jurnal |
| Jualan antara organisasi | Jurnal integrasi entiti sah pinjaman | Tidak | Pelanggan antara syarikat | **Kumpulan cukai jualan pengebilan**: Berdasarkan **pelanggan antara syarikat** <br/> **Kumpulan cukai jualan item pengebilan**: Daripada kategori projek entiti sah semasa pada garisan jurnal |

### <a name="example-intercompany-transactions"></a>Contoh: Transaksi antara syarikat

Siti Fatimah Samsuddin, pembangun yang digunakan dalam GBPM merekodkan 10 jam bekerja bagi projek Adventure Works USPM, yang diluluskan oleh pengurus projek. Kos pembangun dalam GBPM ialah 88 GBP sejam. GBPM akan mengebil USPM sebanyak 120 USD bagi setiap jam pembangun. USPM akan mengebil Adventure Works pelanggan, sebanyak 200 USD untuk kerja yang dilakukan oleh sumber GBPM. Untuk mendapatkan maklumat lanjut, lihat [Konfigurasikan penginvoisan antara syarikat](configure-intercompany-invoicing.md).

1. Dalam Project Operations, pergi ke **Sumber** dan pilih **Siti Fatimah Samsuddin** daripada senarai. Dalam tab **Penjadualan** dalam medan **Syarikat**, pilih **GBPM**.
2. Pergi ke **Jualan** > **Pelanggan** dan pilih **Baharu** untuk mencipta rekod pelanggan baharu untuk Adventure Works.
    1. Tetapkan syarikat kepada **USPM**.
    2. Tetapkan **Jenis hubungan** kepada **Pelanggan**.
    3. Pilih **Kumpulan pelanggan 10 – Domestik**.
    4. Tetapkan mata wang kepada **USD**.
    5. Simpan rekod.
3. Pergi ke **Jualan** > **Kontrak projek** dan cipta kontrak projek baharu untuk Adventure Works.
    1. Tetapkan syarikat pemilikan kepada **USPM** dan unit kontrak kepada **Contoso Robotics Amerika Syarikat**.
    2. Pilih Adventure Works sebagai pelanggan.
    3. Pilih senarai harga produk dan simpan rekod.
    4. Pada tab **Baris kontrak**, cipta baris kontrak baharu. Tetapkan sebarang nama dan pilih **Masa dan bahan** sebagai kaedah pengebilan.
    5. Cipta projek baharu dan kaitkan dengan baris kontrak ini.
4. Daftar masuk sebagai sumber, **Siti Fatimah Samsuddin**. Pergi ke **Projek** > **Entri masa** dan cipta entri masa untuk projek Adventure Works.
5. Daftar masuk sebagai Pengurus Projek. Pergi ke **Projek** > **Kelulusan** dan luluskan transaksi entri masa yang dilog oleh Siti Fatimah Samsuddin.
6. Navigasi ke projek Adventure Works dan pilih **Berkaitan** > **Aktual**. Transaksi aktual berikut dicipta.

| **Jenis transaksi** | **Harga** | **Mata wang transaksi** | **Amaun** |
| --- | --- | --- | --- |
| Kos | 120 | USD | 1200 |
| Jualan belum dibilkan | 200 | USD | 2000 |
| Kos unit persumberan | 88 | GBP | 880 |
| Jualan unit antara organisasi | 120 | USD | 1200 |

7. Daftar masuk sebagai akauntan USPM. Buka tika Kewangan Project Operations dan pilih syarikat **USPM**. 
8. Pergi ke **Pengurusan projek dan perakaunan** > **Berkala** > **Project Operations pada Customer Engagement** > **Import daripada pemeringkatan** dan pilih untuk menjalankan proses berkala. Proses berkala ini akan mengisi jurnal Integrasi Project Operations.
9. Pergi ke **Pengurusan projek dan perakaunan** > **Jurnal** > **Jurnal integrasi Project Operations** dan semak garisan jurnal. Sistem mencipta baris berikut.

    | **Jenis transaksi** | **Harga** | **Mata wang transaksi** | **Amaun** |
    | --- | --- | --- | --- |
    | Jualan belum dibilkan | 200 | USD | 2000 |

    Jika sistem disediakan untuk mengakru hasil untuk projek ini, perkara berikut disiarkan:

    - Debit: Projek – nilai jualan WIP sebanyak 200 USD
    - Kredit: Projek – Hasil Terakru sebanyak 200 USD

    Jualan belum dibilkan ini kini bersedia untuk penginvoisan. Invois untuk Adventure Works pelanggan boleh disiarkan dari segi kewangan apabila diperlukan.

10. Daftar masuk sebagai akauntan **GBPM**. Buka tika Kewangan Project Operations dan buka syarikat, **GBPM**. 
11. Pergi ke **Pengurusan projek dan perakaunan** > **Berkala** > **Project Operations pada Customer Engagement** > **Import daripada pemeringkatan** dan menjalankan proses berkala untuk mengisi jurnal Integrasi Project Operations.
12. Pergi ke **Pengurusan projek dan perakaunan** > **Jurnal** > **Jurnal integrasi Project Operations** dan semak baris. Sistem mencipta baris berikut.

    | **Jenis transaksi** | **Harga** | **Mata wang transaksi** | **Amaun** |
    | --- | --- | --- | --- |
    | Kos unit persumberan | 88 | GBP | 880 |
    | Jualan unit antara organisasi | 120 | USD | 1200 |

    Menyiar keputusan rekod ini dalam transaksi baucar berikut:

    - Debit: Kos projek sebanyak 88 GBP
    - Kredit: Peruntukan gaji sebanyak 88 GBP

    Jika sistem disediakan untuk mengakru hasil antara syarikat, perkara berikut disiarkan:

    - Debit: Projek – nilai jualan WIP sebanyak 120 USD
    - Kredit: Projek – Hasil Terakru sebanyak 120 USD

    Sistem kini bersedia untuk mencipta invois pelanggan antara syarikat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]