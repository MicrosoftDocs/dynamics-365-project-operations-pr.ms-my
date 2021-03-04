---
title: Penginvoisan antara syarikat
description: Artikel ini menyediakan maklumat dan contoh tentang penginvoisan antara syarikat untuk projek.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4604708dbd7c835c8df1cf48f67e645952f49774
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081254"
---
# <a name="intercompany-invoicing"></a>Penginvoisan antara syarikat

[!include [banner](../includes/banner.md)]

Artikel ini menyediakan maklumat dan contoh tentang penginvoisan antara syarikat untuk projek.

Organisasi anda mungkin mempunyai berbilang divisyen, subsidiari dan entiti undang-undang lain yang memindahkan produk dan perkhidmatan kepada satu sama lain untuk projek. Entiti undang-undang yang menyediakan perkhidmatan atau produk dipanggil *entiti undang-undang pemberi pinjaman* dan entiti undang-undang yang menerima perkhidmatan atau produk dipanggil *entiti undang-undang peminjaman*. 

Ilustrasi berikut menunjukkan senario biasa di mana dua entiti undang-undang, SI FR (entiti undang-undang peminjaman) dan SI USA (entiti undang-undang pemberi pinjaman) berkongsi sumber untuk menyampaikan projek bagi pelanggan A. Untuk senario ini, SI FR dikontrak untuk menyampaikan kerja kepada pelanggan A. 

[![Contoh penginvoisan antara syarikat](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Matlamat adalah untuk membuat kawalan kos, pengiktirafan hasil, cukai dan pemindahan harga untuk tansaksi projek antara syarikat lebih fleksibel dan berkuasa. Di samping itu, keupayaan berikut adalah disediakan:

-   Cipta invois pelanggan terhadap projek dalam entiti undang-undang peminjaman dengan menggunakan lembaran masa antara syarikat, perbelanjaan dan invois vendor dalam entiti undang-undang pemberian pinjaman.
-   Menyokong pengiraan cukai dan kos tidak langsung.
-   Menangguhkan pengiktirafan hasil dalam entiti undang-undang peminjaman dan apabila entiti undang-undang peminjaman perlu mengiktiraf kos.
-   Kerja terakru dalam hasil (WIP) proses dalam entiti undang-undang peminjaman.
-   Tetapkan pemindahan harga yang boleh berasaskan pada pelbagai model. Berikut adalah beberapa contoh:
    -   **Kuantiti** – Amaun yang anda masukkan dalam medan **Penentuan Harga** adalah kos sebenar mengikut kuantiti atau unit.
    -   **Amaun caj** – Harga/kos mengikut transaksi tambah amaun caj yang anda masukkan dalam medan **Penentuan Harga**.
    -   **Peratusan caj** – Harga pemindahan adalah harga/kos mengikut transaksi didarabkan dengan peratusan caj yang anda masukkan dalam medan **Penentuan Harga**.
    -   **Peratusan harga jualan** – Peratusan harga jualan yang dipindahkan ke entiti undang-undang pemberi pinjaman.
    -   **Amaun di bawah harga jualan** – Amaun yang ditahan oleh entiti undang-undang peminjaman daripada harga jualan sebelum dipindah ke entiti undang-undang pemberi pinjaman.
    -   **Nisbah sumbangan** – Nombor yang anda masukkan dalam medan **Penentuan Harga** adalah nisbah sumbangan yang diungkapkan sebagai peratusan harga jualan..

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Contoh 1: Tetapkan parameter untuk penginvoisan antara syarikat
Dalam contoh ini, USSI adalah entiti undang-undang pemberi pinjaman dan sumbernya adalah masa pelaporan terhadap entiti undang-undang peminjaman, FRSI yang memiliki kontrak dengan pelanggan akhir. Jam dan perbelanjaan yang dilaporkan oleh pekerja USSI boleh dimasukkan dalam invois projek yang dijana oleh FRSI. Di samping itu, terdapat sumber transaksi ketiga yang berasal daripada entiti undang-undang pemberi pinjaman (dalam contoh ini USSI) apabila ianya menyediakan perkhidmatan vendor dikongsi (seperti FRSI) dan kemudian menyerahkan kos itu kepada projek dalam subsidiari itu. Semua dokumen invois dan pengiraan cukai yang sepadan adalah dilengkapkan oleh Kewangan. 

Untuk contoh ini, FRSI mesti pelanggan dalam entiti undang-undang USSI dan USSI mesti vendor dalam entiti undang-undang FRSI. Anda kemudian boleh menyediakan perhubungan antara syarikat di antara dua entiti undang-undang. Prosedur berikut menunjukkan cara menyediakan parameter supaya kedua-dua entiti undang-undang boleh menyertai dalam penginvoisan antara syarikat.

1. Sediakan FRSI sebagai pelanggan dalam entiti undang-undang USSI dan sediakan USSI sebagai vendor dalam entiti undang-undang FRSI. Terdapat tiga titik entri untuk langkah yang diperlukan bagi tugas ini.

   | Langkah |                                                       Titik entri                                                        |                                                                                                                                                                                               Penerangan                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | Dalam USSI, klik <strong>Akaun belum terima</strong> &gt; <strong>Pelanggan</strong> &gt; <strong>Semua Pelanggan</strong>. |                                                                                                                                                                  Cipta rekod pelanggan baharu untuk FRSI dan pilih kumpulan pelanggan.                                                                                                                                                                  |
   |  B   |    Dalam FRSI, klik <strong>Akaun belum bayar</strong> &gt; <strong>Vendor</strong> &gt; <strong>Semua vendor</strong>.     |                                                                                                                                                                    Cipta rekod vendor baharu untuk USSI dan pilih kumpulan vendor.                                                                                                                                                                    |
   |  C   |                                  Dalam FRSI, buka rekod vendor yang baharu sahaja anda cipta.                                  | Pada Anak Tetingkap Tindakan, pada tab <strong>Umum</strong>, dalam kumpulan <strong>Sediakan</strong>, klik <strong>Antara syarikat</strong>. Pada halaman <strong>Antara syarikat</strong>, pada tab <strong>Hubungan perdagangan</strong>, tetapkan gelangsar <strong>Aktif</strong> ke <strong>Ya</strong>. Dalam medan <strong>Syarikat pelanggan</strong>, pilih rekod pelanggan yang anda cipta dalam langkah A. |


2. Klik **Pengurusan projek dan perakaunan** &gt; **Sediakan** &gt; **Parameter pengurusan projek dan perakaunan** dan kemudian klik tab **Antara syarikat**. Cara anda menyediakan parameter bergantung pada sama ada anda adalah entiti undang-undang peminjaman atau entiti undang-undang pemberi pinjaman.
   -   Jika anda adalah entiti undang-undang peminjaman, pilih kategori perolehan yang perlu digunakan untuk memadankan invois vendor yang dijana secara automatik.
   -   Jika anda adalah entiti undang-undang pemberi pinjaman, untuk setiap entiti peminjaman, pilih kategori projek lalai untuk setiap jenis transaksi. Kategori projek digunakan untuk konfigurasi cukai apabila kategori diinvois dalam transaksi antara syarikat wujud hanya dalam entiti undang-undang peminjaman. Anda boleh memilih untuk mengakru hasil bagi transaksi antara syarikat. Akruan ini dilakukan apabila transaksi disiarkan dan ianya kemudian diterbalikkan apabila invois antara syarikat disiarkan.

3. Klik **Pengurusan projek dan perakaunan** &gt; **Sediakan** &gt; **Harga** &gt; **Harga pemindahan**.
4. Pilih mata wang, jenis transaksi dan model harga pemindahan. Mata wang yang digunakan pada invois adalah mata wang yang dikonfigurasi dalam rekod pelanggan untuk entiti undang-undang peminjaman dalam entiti undang-undang pemberi pinjaman. Mata wang digunakan untuk memadankan entri dalam jadual harga pemindahan.
5. Klik **Lejar umum** &gt; **Sediakan penyiaran** &gt; **Perakaunan antara syarikat** dan sediakan perhubungan USSI dan FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Contoh 2: Cipta dan siarkan lembaran masa antara syarikat
USSI, entiti undang-undang pemberi pinjaman mesti mencipta dan menyiarkan lembaran masa untuk projek daripada FRSI, entiti undang-undang peminjaman. Terdapat dua titik entri untuk langkah yang diperlukan bagi tugas ini.

| Langkah | Titik entri                                                                       | Penerangan                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Pengurusan projek dan perakaunan** &gt; **Lembaran masa** &gt; **Semua lembaran masa** | Cipta lembaran masa baharu. Pada baris lembaran masa dalam medan **Entiti undang-undang** , pilih **FRSI**. Dalam medan **ID Projek** pilih projek dalam FRSI. Masukkan jam untuk setiap hari bagi minggu. |
| B    | Halaman **Lembaran masa**                                                                | Selepas aliran kerja berjalan, siarkan lembaran masa dan buat nota nombor baucer.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Contoh 3: Cipta dan siarkan invois vendor antara syarikat
USSI, entiti undang-undang pemberi pinjaman mesti mencipta dan menyiarkan invois vendor antara syarikat untuk projek daripada FRSI, entiti undang-undang peminjaman. Invois vendor mewakili tenaga kerja luar dan perbelanjaan yang dilakukan oleh vendor yang dibayar oleh USSI. Terdapat dua titik entri untuk langkah yang diperlukan bagi tugas ini.

| Langkah | Titik entri                                                                                      | Penerangan                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Akaun belum bayar** &gt; **Invois** &gt; **Invois vendor terbuka** &gt; **Invois vendor baharu** | Cipta invois vendor baharu dan masukkan perkhidmatan yang diperoleh bagi pihak projek FRSI.                                                                                                                                                                                  |
| B    | Halaman **Invois vendor**                                                                      | Masukkan garisan yang mewakili perkhidmatan luar bagi pihak FRSI. Pada FastTab **Butiran garisan** , pada tab **Projek** untuk invois garisan, dalam medan **Syarikat projek** , masukkan **FRSI**. Masukkan projek dan maklumat yang berpadanan. Kemudian siarkan invois vendor. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Contoh 4: Cipta dan siarkan invois antara syarikat
USSI, entiti undang-undang pemberi pinjaman mesti mencipta dan menyiarkan invois antara syarikat. Terdapat dua titik entri untuk langkah yang diperlukan bagi tugas ini.

| Langkah | Titik entri                                                                                             | Penerangan                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Pengurusan projek dan perakaunan** &gt; **Invois projek** &gt; **Invois pelanggan antara syarikat**  | Klik **Baharu** untuk membuka halaman **Cipta invois antara syarikat**.                                                                                  |
| B    | **Pengurusan projek dan perakaunan** &gt; **Invois projek** &gt; **Invois pelanggan antara syarikat** | Pada halaman **Cipta invois antara syarikat** , masukkan entiti undang-undang, tentukan transaksi yang perlu dimasukkan dan kemudian pilih **Carian**. |
| C    | **Pengurusan projek dan perakaunan** &gt; **Invois projek** &gt; **Invois pelanggan antara syarikat** | Pilih transaksi untuk invois atau klik **Pilih semua** untuk menginvois semua transaksi dalam senarai dan kemudian klik **OK**.                  |
| D    | Halaman **Invois antara syarikat**                                                                       | Cadangan invois pelanggan antara syarikat ditunjukkan.                                                                                             |
| E    | Halaman **Invois antara syarikat**                                                                       | Klik **Siarkan**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Contoh 5: Siarkan invois vendor dan invoiskan pelanggan
Apabila entiti pemberi pinjaman, USSI, menyiarkan invois pelanggan antara syarikat, invois vendor belum selesai yang sepadan dicipta dalam entiti undang-undang peminjaman, FRSI. Selepas invois vendor disiarkan, FRSI juga akan menginvois pelanggan projek untuk jam yang dimasukkan oleh USSI. Terdapat tiga titik entri untuk langkah yang diperlukan bagi tugas ini.

| Langkah | Titik entri                                                                                        | Penerangan                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Akaun belum bayar** &gt; **Invois** &gt; **Invois vendor belum selesai**                            | Semak invois untuk mengesahkan nilai lembaran masa yang dimasukkan dan kemudian siarkan invois vendor.                  |
| B    | **Pengurusan projek dan perakaunan** &gt; **Invois projek** &gt; **Cadangan invois projek** | Cipta invois projek baharu untuk projek dan sahkan jam transaksi yang disiarkan dipaparkan.            |
| C    | Halaman **Invois projek**                                                                       | Pilih invois projek dan kemudian klik **Lihat butiran** untuk menyemak amaun kos dan jualan. Kemudian siarkan invois. |


Untuk maklumat lanjut, lihat [Konfigurasi penginvoisan projek antara syarikat](tasks/configure-intercompany-project-invoicing.md).




[!INCLUDE[footer-include](../includes/footer-banner.md)]