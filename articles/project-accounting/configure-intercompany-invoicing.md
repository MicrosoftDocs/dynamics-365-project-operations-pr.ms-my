---
title: Konfigurasikan penginvoisan antara syarikat
description: Artikel ini memberikan maklumat dan contoh mengenai mengkonfigurasi invois antara syarikat untuk projek.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ae0c2662bb6b2789ab520f08c7c21935b651ced5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929409"
---
# <a name="configure-intercompany-invoicing"></a>Konfigurasikan penginvoisan antara syarikat

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Lengkapkan langkah berikut untuk menyediakan penginvoisan antara Syarikat untuk projek dalam Dynamics 365 Project Operations. Transaksi antara syarikat ialah transaksi masa dan perbelanjaan daripada kontrak projek yang dimiliki oleh satu syarikat atau unit organisasi, sementara sumber pada kontrak projek adalah sebahagian daripada syarikat atau unit organisasi yang berbeza.

## <a name="example-configure-intercompany-invoicing"></a>Contoh: Konfigurasikan penginvoisan antara syarikat

Dalam contoh berikut, Contoso Robotics Amerika Syarikat (USPM) ialah entiti sah pinjaman dan Contoso Robotics UK (GBPM) ialah entiti sah pinjaman. 

1. **Konfigurasikan perakaunan antara syarikat antara entiti sah**. Setiap pasangan entiti sah pinjaman mesti dikonfigurasikan pada Lejar umum halaman [Perakaunan antara syarikat](/dynamics365/finance/general-ledger/intercompany-accounting-setup).
    
    1. Dalam Dynamics 365 Finance, pergi ke **General Ledger** > **Posting persediaan** > **Perakaunan antara syarikat**. Cipta rekod dengan maklumat berikut:

        - **Syarikat asal** = **GBPM**
        - **Syarikat destinasi** = **USPM**

2. **Konfigurasikan hubungan jualan antara entiti sah**. Rekod pelanggan yang mewakili entiti sah pinjaman mesti dicipta dalam entiti sah pinjaman. Rekod vendor yang mewakili entiti sah pinjaman mesti dicipta dalam entiti sah pinjaman.

     1. Dalam Kewangan, pilih entiti sah **GBPM**.
     2. Pergi ke **Akaun belum terima** > **Pelanggan** > **Semua pelanggan**. Cipta rekod baharu untuk entiti sah, **USPM**.
     3. Kembangkan **Nama**, tapis rekod mengikut **Jenis** dan pilih **Entiti sah**. 
     4. Cari dan pilih rekod pelanggan untuk **Contoso Robotics Amerika Syarikat (USPM)**.
     5. Pilih **Gunakan padanan**. 
     6. Pilih kumpulan pelanggan **50 - Pelanggan antara syarikat** dan kemudian simpan rekod.
     7. Pilih entiti sah **USPM**.
     8. Pergi ke **Akaun belum bayar** > **Vendor** > **Semua vendor**. Cipta rekod baharu untuk entiti sah, **GBPM**.
     9. Kembangkan **Nama**, tapis rekod mengikut **Jenis** dan pilih **Entiti sah**. 
     10. Cari dan pilih rekod pelanggan untuk **Contoso Robotics UK (GBPM)**.
     11. Pilih **Gunakan padanan**, pilih kumpulan vendor dan kemudian simpan rekod.
     12. Dalam rekod vendor, pilih **Umum** > **Sediakan** > **Antara Syarikat**.
     13. Pada tab **Hubungan jualan**, tetapkan **Aktif** kepada **Ya**.
     14. Tetapkan medan **Syarikat pelanggan** ke **GBPM** dan dalam **Rekod akaun saya**, pilih rekod pelanggan yang anda cipta lebih awal dalam prosedur..

3. **Konfigurasikan tetapan antara syarikat dalam Parameter pengurusan projek dan perakaunan**. 

    1. Pilih entiti sah **USPM** dan pergi ke **Pengurusan projek dan perakaunan** > **Persediaan** > **Parameter pengurusan projek dan perakaunan**.
    2. Pada tab **Antara Syarikat**, pilih kategori pemerolehan untuk dipadankan dengan invois vendor yang dijana secara automatik.
    3. Dalam **Kategori lalai**, pilih **Sumber antara syarikat**.
    4. Pilih entiti sah **GBPM** dan pergi ke **Pengurusan projek dan perakaunan** > **Persediaan** > **Parameter pengurusan projek dan perakaunan**.
    5. Pada tab **Antara Syarikat**, pilih kategori projek lalai untuk setiap jenis transaksi. Kategori projek digunakan untuk konfigurasi cukai apabila kategori diinvois dalam transaksi antara syarikat wujud hanya dalam entiti undang-undang peminjaman. Anda boleh memilih untuk mengakru hasil bagi transaksi antara syarikat. Akruan berlaku apabila transaksi disiarkan melalui jurnal Integrasi Project Operations dalam entiti sah pinjaman. Jurnal ini akan diterbalikkan apabila invois antara syarikat disiarkan.
    6. Dalam kumpulan **Sumber apabila meminjam**, pilih **...** > **Baharu**. 
    7. Dalam grid, pilih maklumat berikut:

          - **Entiti sah pinjaman** = **USPM**
          - **Hasil terakru** = **Ya**
          - **Kategori lembaran masa lalai** = **Lalai – Jam**
          - **Kategori perbelanjaan lalai** = **Lalai – perbelanjaan**

4. **Tetapkan akaun kos dan hasil antara syarikat dalam Persediaan penyiaran lejar**. Akaun hasil antara syarikat dikreditkan apabila invois pelanggan Antara Syarikat disiarkan dalam entiti sah pinjaman. Akaun kos antara syarikat didebitkan apabila padanan invois vendor yang belum selesai disiarkan dalam entiti sah pinjaman. Akaun ini disediakan dalam entiti sah yang berkaitan. 
      
     1. Dalam Kewangan, pilih entiti sah pinjaman **USPM**. 
     2. Pergi ke **Pengurusan projek dan perakaunan** > **Persediaan** > **Penyiaran** > **Persediaan penyiaran lejar**. 
     3. Pada tab **Akaun kos**, dalam **Jenis akaun lejar**, pilih **Kos antara syarikat**. Cipta rekod baharu dengan maklumat berikut:
      
        - **Entiti sah pinjaman** = **GBPM**
        - **Akaun utama** = Pilih akaun utama untuk kos antara syarikat. Persediaan ini diperlukan. Persediaan digunakan untuk aliran antara syarikat dalam Kewangan tetapi tidak dalam aliran antara syarikat berkaitan projek. Pemilihan ini tidak mempunyai kesan hiliran. 
        
     4. Pilih entiti sah pinjaman, **GBPM**. 
     5. Pergi ke **Pengurusan projek dan perakaunan** > **Persediaan** > **Penyiaran** > **Persediaan penyiaran lejar**. 
     6. Pada tab **Akaun hasil**, dalam **Jenis akaun lejar**, pilih **Hasil antara syarikat**. Cipta rekod baharu dengan maklumat berikut:

        - **Entiti sah pinjaman** = **USPM**
        - **Akaun utama** = Pilih akaun utama untuk hasil antara syarikat. Persediaan ini diperlukan. Persediaan digunakan untuk aliran antara syarikat dalam Kewangan tetapi tidak dalam aliran antara syarikat berkaitan projek. Pemilihan ini tidak mempunyai kesan hiliran. 

5. **Sediakan penentuan harga pindahan untuk buruh**. Penentuan harga pindahan antara syarikat dikonfigurasikan dalam Project Operations pada Dataverse. Konfigurasikan [kadar kos buruh](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) dan [kadar bil buruh](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) untuk penginvoisan antara syarikat. Penentuan harga pindahan tidak disokong untuk transaksi perbelanjaan antara syarikat. Harga jualan unit antara organisasi akan sentiasa ditetapkan kepada nilai yang sama dengan harga unit sumber.

      Kos sumber pembangun dalam Contoso Robotics UK ialah 88 GBP sejam. Contoso Robotics UK akan mengebil Contoso Robotics Amerika Syarikat sebanyak 120 USD untuk setiap jam sumber ini bekerja pada projek AS. Contoso Robotics Amerika Syarikat akan mengebil Adventure Works pelanggan sebanyak 200 USD untuk kerja yang dilakukan oleh sumber pembangun Contoso Robotics UK.

      1. Dalam Project Operations pada Dataverse, pergi ke **Jualan** > **Senarai harga**. Cipta senarai harga kos baharu yang dipanggil **kadar kos Contoso Robotics UK.** 
      2. Dalam senarai harga kos, cipta rekod dengan maklumat berikut:
         - **Peranan** = **Pembangun**
         - **Kos** = **88 GBP**
      3. Pergi ke **Tetapan** > **Unit organisasi** dan lampirkan senarai harga kos ini kepada unit organisasi **Contoso Robotics UK**.
      4. Pergi ke **Jualan** > **Senarai harga**. Cipta senarai harga kos yang dipanggil **kadar kos Contoso Robotics Amerika Syarikat**. 
      5. Dalam senarai harga kos, cipta rekod dengan maklumat berikut:
          - **Peranan** = **Pembangun**
          - **Syarikat sumber** = **Contoso Robotics UK**
          - **Kos** = **120 USD**
      6. Pergi ke **Tetapan** > **Unit organisasi** dan lampirkan senarai harga kos **kadar kos Contoso Robotics Amerika Syarikat** kepada unit organisasi **Contoso Robotics Amerika Syarikat**.
      7. Pergi ke **Jualan** > **Senarai harga**. Cipta senarai harga jualan yang dipanggil **kadar bil Adventure Works**. 
      8. Dalam senarai harga jualan, cipta rekod dengan maklumat berikut:
          - **Peranan** = **Pembangun**
          - **Syarikat sumber** = **Contoso Robotics UK**
          - **Kadar bil** = **200 USD**
      9. Pergi ke **Jualan** > **Kontrak projek** dan lampirkan senarai harga **kadar bil Adventure Works** kepada senarai harga projek Adventure Works bagi kontrak projek.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
