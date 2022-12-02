---
title: Urus cadangan invois projek
description: Artikel ini memberikan butiran tentang pemprosesan invois yang menghadap pelanggan dengan Project Operations untuk senario berasaskan sumber/bukan stok.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ef6003499f1372a51d7d1606db6f5bf9722a369d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927845"
---
# <a name="manage-project-invoice-proposals"></a>Urus cadangan invois projek

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Cadangan invois projek boleh diproses oleh jabatan pengebilan anda apabila dua syarat berikut dipenuhi:

  - Pengurus Projek mengesahkan invois proforma dalam Microsoft Dataverse.
  - Semua transaksi jualan yang tidak dibilkan untuk masa dan bahan yang disertakan dalam invois proforma disiar menggunakan jurnal **Integrasi Project Operations** Dynamics 365.

Gunakan langkah berikut untuk melengkapkan cadangan invois projek dalam Dynamics 365 Finance.

1. Menyemak maklumat pengebilan untuk transaksi masa dan bahan dan siarkan jurnal **Integrasi Project Operations**.
2. Semak maklumat pengebilan untuk pencapaian pengebilan harga tetap.
3. Semak dan formatkan cadangan invois projek.
4. Siar dan cetak invois projek.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Urus maklumat pengebilan dalam jurnal Integrasi Project Operations

Aktual projek dicipta dalam Dataverse disemak semula dan disiarkan dalam Kewangan oleh akauntan Projek. Untuk maklumat lanjut tentang bekerja dengan jurnal Integrasi, lihat [Jurnal Integrasi dalam Project Operations](../project-accounting/project-operations-integration-journal.md).

Aktual kos dan aktual jualan yang belum dibilkan ditambah ke jurnal Integrasi sebagai baris berasingan:

  - Unit harga kos dan jumlah kos ke atas aktual Kos lalai daripada transaksi kos sebenar projek dalam Dataverse.
  - Harga unit jualan dan jumlah jualan pada transaksi jualan Tidak dibilkan lalai daripada transaksi jualan tidak dibilkan aktual projek dalam Dataverse.

### <a name="billing-sales-tax"></a>Cukai jualan pengebilan

Pengiraan cukai jualan untuk pengebilan ditentukan oleh medan **Kumpulan cukai jualan pengebilan** dan **Kumpulan cukai jualan item pengebilan** pada rekod jualan belum dibilkan pada baris jurnal **Integrasi Project Operations**. Sistem melalaikan nilai medan ini berdasarkan pada tetapan pada tab **Kewangan** pada halaman **Pengurusan projek dan parameter perakaunan**.

- **Kaedah kumpulan cukai jualan** menentukan logik menlalaikan kumpulan cukai jualan pengebilan:
  
  - **Projek**: Akan sentiasa melalaikan kumpulan cukai jualan pengebilan daripada projek. Anda boleh menyemak atau mengubah kumpulan cukai jualan pengebilan lalai pada projek dengan memilih **Tunjukkan perakaunan lalai** pada halaman **Semua Projek**.
  - **Kontrak projek**: Akan sentiasa melalaikan kumpulan cukai jualan pengebilan daripada kontrak. Anda boleh menyemak atau mengubah kumpulan cukai jualan lalai pada kontrak projek dengan memilih **Tunjukkan perakaunan lalai** pada halaman **Kontrak projek**.
  - **Pelanggan**: Akan sentiasa melalaikan kumpulan cukai jualan pengebilan daripada pelanggan.
  - **Cari**: Akan mencari merentasi semua entiti di atas dan memilih nilai pertama yang tersedia. Carian bermula dengan entiti **Projek**, kemudian entiti **Kontrak projek** dan akhirnya entiti **Pelanggan**.

- **Kaedah kumpulan cukai jualan item** menentukan logik menlalaikan kumpulan cukai jualan item pengebilan:
  
  - Untuk jenis masa, perbelanjaan dan transaksi yuran, kumpulan cukai jualan item pengebilan akan sentiasa lalai daripada entiti **Kategori projek**.
  - Untuk jenis transaksi bahan, kumpulan cukai jualan item pengebilan lalai berdasarkan pada tetapan **Kaedah kumpulan cukai jualan item** dalam **Parameter pengurusan projek dan perakaunan**. Nombor item melalaikan kumpulan cukai jualan item daripada entiti **Produk yang dilepaskan**. Kategori melalaikan kumpulan cukai jualan item daripada entiti **Kategori produk**.

### <a name="financial-dimensions"></a>Dimensi kewangan

Dimensi kewangan bagi rekod jualan yang tidak dibilkan dalam jurnal **Integrasi Project Operations** lalai daripada entiti **Projek**. Dimensi kewangan boleh disemak dan dilaraskan dengan memilih **Mengedarkan Jumlah**. Jika anda perlu mengubah dimensi kewangan bagi rekod jualan yang tidak dibilkan selepas jurnal Integrasi disiarkan tetapi sebelum invois Proforma disahkan, pergi ke **Semua Projek** > **Urus** > **Transaksi yang telah disiarkan**, pilih transaksi, dan kemudian pilih **Proses** > **Laraskan perakaunan**.

### <a name="exchange-rates"></a>Kadar pertukaran

Mata wang transaksi tidak dibilkan dalam Dataverse digunakan sebagai mata wang transaksi dalam Kewangan dan ditukar kepada mata wang perakaunan syarikat dengan menggunakan kadar pertukaran yang ditakrifkan dalam Kewangan.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>Urus atribut kewangan pencapaian pengebilan 

Baris kontrak projek menggunakan kaedah pengebilan harga tetap adalah diinvois melalui [Pencapaian harga tetap](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line). Pihak akauntan Projek boleh menyemak semula pencapaian pengebilan dalam Kewangan dengan pergi ke **Pengurusan projek dan perakaunan** > **Semua projek** > **Urus** > **Transaksi dalam akaun**.

### <a name="billing-sales-tax"></a>Cukai jualan pengebilan

Nilai **Kumpulan cukai jualan** dan **Kumpulan cukai jualan item**  lalai daripada tetapan apabila pencapaian pengebilan baharu dicipta dalam Dataverse. Sistem melalaikan nilai kepada medan ini berdasarkan pada tetapan pada tab **Kewangan** pada halaman **Pengurusan projek dan parameter perakaunan**.

- **Kaedah kumpulan cukai jualan** menentukan logik menlalaikan **Kumpulan cukai jualan pengebilan**:

    - **Projek** akan sentiasa melalaikan kumpulan cukai jualan pengebilan daripada projek. Anda boleh menyemak atau mengubah kumpulan cukai jualan lalai pada projek dengan memilih **Tunjukkan perakaunan lalai** pada halaman **Semua Projek**.
    - **Kontrak projek** akan sentiasa melalaikan kumpulan cukai jualan pengebilan daripada kontrak. Anda boleh menyemak atau mengubah kumpulan cukai jualan lalai pada kontrak projek dengan memilih **Tunjukkan perakaunan lalai** pada halaman **Kontrak projek**.
    - **Pelanggan** akan sentiasa melalaikan kumpulan cukai jualan pengebilan daripada pelanggan.
    - **Cari** akan mencari merentasi semua entiti dalam senarai ini dan memilih nilai pertama yang tersedia. Carian bermula dengan entiti **Projek**, kemudian entiti **Kontrak projek** dan kemudian entiti **Pelanggan**.

- **Kumpulan cukai jualan item pencapaian harga tetap** digunakan sebagai nilai lalai dalam medan **kumpulan cukai jualan item** untuk pencapaian pengebilan. Akauntan boleh menyemak semula dan mengubah suai nilai ini pada halaman **Transaksi pada akaun**. Sistem menggunakan nilai daripada transaksi pada akaun apabila mencipta baris cadangan invois projek.
 

### <a name="financial-dimensions"></a>Dimensi kewangan

Dimensi kewangan lalai untuk pencapaian pengebilan harga tetap ditetapkan pada baris kontrak Projek. Pergi ke **Kontrak projek** > **Tunjukkan perakaunan lalai** dan pada tab **Baris kontrak**, pilih **baris kontrak harga**, kemudian tetapkan nilai dimensi kewangan yang anda mahu gunakan sebagai lalai.

Akauntan Projek boleh mengedit cukai jualan dan dimensi kewangan maklumat pada pencapaian invois sehingga cadangan invois Projek dicipta.


## <a name="create-project-invoice-proposals"></a>Cipta cadangan invois projek

Cadangan invois projek boleh disemak semula dalam modul **Pengurusan projek dan perakaunan** dengan pergi ke **Invois projek** > **Cadangan invois projek**.

Pengepala cadangan invois Projek dicipta dalam Kewangan apabila invois Proforma disahkan dalam Dataverse. Untuk penyesuaian lebih mudah, sistem menetapkan nombor cadangan invois Projek dalam kewangan kepada nombor yang sama dengan ID invois Proforma dalam Dataverse. Kerana invois Proforma tidak semestinya disahkan dalam susunan yang sama ia dicipta, urutan nombor cadangan invois Projek dalam Kewangan mesti membenarkan perubahan pada nombor yang lebih rendah dan lebih tinggi. Konfigurasikan urutan nombor menggunakan langkah-langkah berikut:

1. Dalam Kewangan, pergi ke **Pentadbiran Organisasi** > **Urutan nombor** > **Urutan nombor**.
2. Dalam penapis **Kawasan**, pilih **Projek**.
3. Dalam penapis **Rujukan**, pilih **Cadangan invois**.
4. Gunakan medan **Syarikat** untuk menapis setiap entiti sah dengan integrasi Project Operations Dataverse didayakan.
5. Buka **Butiran Urutan Nombor** dan pada tab **Umum** tetapkan:

    - **Benarkan perubahan pengguna: Kepada nombor yang lebih rendah** = **Ya**
    - **Benarkan perubahan pengguna: Kepada nombor yang lebih tinggi** = **Ya**

Baris cadangan invois projek ditambah oleh sistem menggunakan proses berkala **Import daripada jadual pementasa** (**Pengurusan projek dan perakaunan** > **Berkala** > **Integrasi Project Operations** > **Import daripada jadual pementasan**). Proses ini boleh dijalankan secara manual atau dengan menggunakan jadual berkala. Sistem tidak akan menambah baris kepada dokumen cadangan invois sehingga semua baris bersedia untuk diinvois. Transaksi masa dan bahan sudah sedia untuk diinvois hanya apabila ia disiarkan menggunakan jurnal **Integrasi Project Operations**.

## <a name="format-and-print-invoice-proposals"></a>Format dan cetak cadangan invois

Akauntan Projek boleh menyesuaikan cetakan invois projek dengan menggunakan halaman **Cadangan invois format** dan keupayaan pengurusan cetak.

### <a name="format-invoice-proposals"></a>Cadangan invois format

Halaman **Cadangan invois format** membenarkan transaksi kumpulan tersuai untuk dipaparkan dalam invois projek pelanggan.

1. Pada halaman **Cadangan invois projek**, pilih **Cetak** > **Cadangan invois format**.
2. Pilih **Baharu** untuk mencipta kumpulan baharu bagi cetakan invois Projek.
3. Dalam medan **Butiran/Ringkasan**, pilih pilihan untuk kumpulan ini:

    - Pilih **Butiran** untuk mencetak butiran transaksi invois pelanggan.
    - Pilih **Ringkasan** untuk mencetak ringkasan transaksi invois pelanggan.

> [!NOTE]
> Pemilihan dalam medan **Butiran/Ringkasan** pada halaman **Cadangan invois format** membatalkan pilihan yang dipilih dalam medan **Format invois** pada halaman **Cadangan invois** untuk mencetak invois terperinci atau invois yang diringkaskan.

- Pilih baris transaksi untuk disertakan dalam bahagian ini pada tab **Transaksi tersedia** dan pilih **Termasuk transaksi** untuk memindahkannya ke tab **Transaksi yang dipilih**.
- Pilih **Bergerak ke atas** dan **Bergerak ke bawah** untuk mengubah urutan bahagian.
- Pilih **Cetak pratonton** untuk pratonton invois yang diformat.

### <a name="print-management"></a>Pengurusan cetak

Pengurusan cetak menggunakan fail laporan yang berbeza untuk mencetak, menentukan destinasi dan menyesuaikan teks pengaki untuk invois. Pengurusan cetak boleh ditetapkan pada peringkat modul, bagaimanapun tetapan ini boleh diganti untuk pelanggan, kontrak atau cadangan invois khusus. Untuk mengakses fungsi ini pada halaman **Cadangan invois projek**, pilih **Cetak** > **Pengurusan cetak**.

Penyediaan pengurusan cetak dipaparkan sebagai pandangan pepohon, di mana setiap peringkat nod memaparkan dokumen yang tersedia untuk dilaraskan. Anda boleh menugaskan cetakan tersuai pada peringkat modul, pelanggan, kontrak atau dokumen cadangan invois. Untuk mengubah suai cetakan dokumen asal, kembangkan nod yang dikehendaki dan pilih **Item asal**. Dalam medan **Format laporan**, pilih format laporan yang akan digunakan untuk mencetak. Anda boleh menggunakan format laporan tersuai dengan menggunakan [Rangka kerja Pengurusan Dokumen Perniagaan](/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).

## <a name="post-invoice-proposals"></a>Siarkan cadangan invois

Selepas invois disemak semula dan diedit, dan baris cadangan invois adalah memuaskan, semak jumlah invois dan cukai jualan. Dalam kumpulan **Butiran**, pilih **Jumlah** dan kemudian pilih **Siarkan** untuk menyiarkan invois.

Untuk melihat invois sebelum menyiarkan, kosongkan kotak semak **Menyiarkan**. **Pro forma** akan dicetak pada invois untuk menandakan ia adalah invois sampel. Untuk mencetak invois, pilih kotak semak **Cetak invois**.

Sebagai tambahan kepada halaman **Cadangan invois**, cadangan invois juga boleh disiarkan dengan menjalankan kerja berkala, **Cadangan selepas invois**. Untuk mencari kerja ini, pergi ke **Pengurusan projek dan perakaunan** > **Berkala** > **Invois projek** > **Cadangan selepas invois**.

Halaman ini menunjukkan semua cadangan invois yang sedia untuk disiarkan. Anda boleh menjadualkan menyiarkan cadangan invois dengan memilih **Kelompok**. Tetapkan **Parameter pemprosesan kelompok** kepada **Ya** dan tetapkan pengulangan pemprosesan kelompok dengan memilih **Pengulangan**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
