---
title: Konsep unik untuk Kontrak Berdasarkan Projek
description: Artikel ini menyediakan maklumat tentang konsep utama untuk kontrak projek dalam Project Operations.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 48053bf6209d0a997e4e8766e29d77f994da06b4
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825858"
---
# <a name="concepts-unique-to-project-based-contracts"></a>Konsep unik untuk Kontrak Berdasarkan Projek

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_



Artikel ini memberikan konsep utama untuk diketahui sebelum anda mula menggunakan kontrak Projek dalam Dynamics 365 Project Operations:

## <a name="owning-company"></a>Syarikat Pemilikan

Syarikat pemilikan ialah entiti yang sah daripada modul **Pengurusan projek dan perakaunan** untuk Project Operations daripada Dynamics 365 Finance. Syarikat pemilikan mewakili entiti yang sah yang akan mengambil kira kos dan hasil yang terakru daripada perjanjian.

## <a name="contracting-unit"></a>Unit Pengkontrakan

Unit kontrak mewakili divisyen atau amalan yang memiliki penghantaran projek. Anda boleh menyediakan kos sumber untuk setiap unit pengkontrakan. Apabila anda menentukan kos sumber untuk sumber, anda juga akan boleh menyediakan kadar kos berbeza untuk sumber. Unit kontrak ini meminjam sumber ini daripada divisyen atau amalan lain dalam perusahaan. Kadar kos untuk sumber dirujuk sebagai harga pemindahan, peminjaman sumber atau harga pertukaran. Apabila anda menyediakan kadar kos untuk meminjam sumber daripada divisyen lain, gunakan mata wang divisyen pinjaman.

## <a name="cost-currency"></a>Mata Wang Kos

Mata wang kos adalah mata wang yang dilaporkan pada skrin. Mata wang ini diperoleh daripada mata wang yang dilampirkan ke medan **Unit Kontrak** pada kontrak dan projek. Kos boleh dilog dalam sebarang mata wang terhadap projek. Walau bagaimanapun, terdapat pertukaran mata wang daripada mata wang kos yang telah direkodkan kepada mata wang kos projek apabila ditunjukkan pada skrin.

Disebabkan oleh kadar pertukaran dalam platform CDS Common Data Service tidak boleh menjadi tarikh berkuat kuasa, jumlah pada skrin untuk kos mungkin berubah dari masa ke masa jika anda mengemas kini kadar pertukaran mata wang. Walau bagaimanapun, kos yang direkodkan dalam pangkalan data kekal tidak berubah kerana amaun disimpan dalam mata wang yang dikenakan kepadanya.

## <a name="sales-currency"></a>Mata Wang Jualan

Mata wang jualan dalam Project Operations ialah mata wang yang digunakan dalam amaun jualan anggaran dan sebenar yang direkodkan dan ditunjukkan. Mata wang jualan juga merupakan mata wang yang digunakan untuk menginvois urus niaga dengan pelanggan. Pada kontrak projek, mata wang jualan lalai daripada rekod pelanggan atau akaun dan boleh diubah semasa kontrak dicipta. Apabila kontrak dicipta dengan menutup sebut harga sebagai menang, mata wang pada kontrak dilalaikan daripada mata wang pada sebut harga.

Apabila anda mencipta kontrak projek daripada mula, medan **Mata Wang Jualan** tidak boleh diedit. Senarai harga produk dan projek lalai berasaskan pada mata wang ini pada kontrak.

Tidak seperti kos, nilai jualan hanya boleh direkodkan dalam mata wang jualan.

## <a name="billing-method"></a>Kaedah Pengebilan

Kebiasaannya terdapat dua jenis model kontrak untuk projek, yuran tetap dan berdasarkan penggunaan. Model ini diwakili dalam Project Operations sebagai kaedah pengebilan dengan dua nilai yang mungkin:

- Masa dan Bahan: Model kontrak berdasarkan penggunaan, setiap kos yang dikenakan disandarkan oleh hasil yang sepadan. Ketika anda menganggarkan atau mengenakan lebih banyak kos, jualan anggaran dan aktual yang sepadan juga akan meningkat. Nyatakan had tidak boleh melebihi pada baris kontrak yang mempunyai kaedah pengebilan ini, yang memberikan hasil aktual. Hasil yang dianggarkan tidak dipengaruhi oleh had tidak boleh melebihi.
- Harga tetap: Model kontrak yuran tetap yang menunjukkan nilai jualan tidak akan bergantung kepada kos yang dikenakan. Nilai jualan adalah tetap dan tidak berubah ketika anda menganggarkan atau mengenakan lebih banyak kos.

## <a name="project-price-lists"></a>Senarai Harga Projek

Senarai harga projek digunakan untuk harga lalai, bukan kadar kos, untuk masa, perbelanjaan dan komponen berkaitan projek yang lain. Terdapat berbilang senarai harga. Setiap senarai harga mempunyai tarikh penguatkuasaan sendiri untuk setiap kontrak projek. Penindihan penguatkuasaan tarikh pada senarai harga projek tidak disokong dalam Project Operations.

Apabila kontrak projek dicipta dengan memenangi sebut harga projek, senarai harga projek disalin dengan nama kontrak dan tarikh disertakan. Penyalinan maklumat ini membentuk penetapan harga tersuai untuk komponen projek pada kontrak projek ini.

## <a name="transaction-classes"></a>Kelas Transaksi

Project Operations menyokong empat jenis kelas transaksi:

- Masa
- Perbelanjaan
- Bahan
- Yuran

Nilai kos dan jualan boleh dianggarkan dan dikenakan pada kelas transaksi Masa, Perbelanjaan dan Bahan. Yuran ialah hanya kelas transaksi hasil sahaja.

## <a name="work-entities-and-billing-entities"></a>Entiti Kerja dan entiti Pengebilan

Entiti yang mewakili kerja ialah projek dan tugas. Entiti yang mewakili aspek pengebilan ialah baris kontrak. Anda boleh mengikat entiti kerja yang berbeza ke pilihan pengebilan dengan mengaitkannya dengan baris kontrak.

## <a name="multi-customer-deals"></a>Urus niaga berbilang pelanggan

Urusan berbilang pelanggan mempunyai lebih daripada satu pelanggan untuk menginvoiskan urusan.. Contoh biasa bagi perkara ini termasuk:

- OEM Enterprise dan rakan kongsinya: Rakan kongsi dan penjual menjual produk dengan beberapa perkhidmatan tambah nilai kebiasaannya melibatkan urusan tertentu dengan pelanggan. OEM menawarkan untuk membiayai sebahagian daripada projek. 

- Projek sektor awam: Berbilang jabatan kerajaan tempatan bersetuju untuk membiayai projek dan diinvoiskan mengikut pecahan yang dipersetujui sebelumnya. Contohnya, daerah sekolah dan kerajaan tempatan bersetuju untuk membiayai pembinaan kolam renang.

## <a name="invoice-schedules"></a>Jadual Invois

Jadual invois adalah khusus untuk setiap baris kontrak dan diperlukan untuk penginvoisan automatik berfungsi. Jadual invois dicipta berdasarkan tarikh mula dan tamat tertentu dan kekerapan invois. Jadual digunakan dalam peringkat kontrak apabila proses penciptaan invois automatik dikonfigurasikan. Apabila kontrak projek dicipta daripada sebut harga, jadual invois disalin ke kontrak projek daripada sebut harga.

## <a name="changes-from-dynamics-365-sales-orders"></a>Perubahan daripada Pesanan Dynamics 365 Sales

Kontrak dalam Project Operations terbina dalam Pesanan dalam Dynamics 365 Sales. Walau bagaimanapun, terdapat beberapa penyelewengan dan perbezaan penting dalam kefungsian. Kontrak mempunyai borang dan elemen UI, peraturan perniagaan, logik perniagaan dalam pasang masuk serta skrip bahagian klien sendiri yang menjadikannya unik daripada Pesanan. Atas sebab ini, jangan gunakan kontrak Pesanan Jualan dan Project Operations secara bergantian.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
