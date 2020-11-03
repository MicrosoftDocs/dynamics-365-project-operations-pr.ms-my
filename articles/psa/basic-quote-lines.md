---
title: Sebut harga dan baris sebut harga
description: Topik ini memberikan maklumat tentang sebut harga dan baris sebut harga.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: ae48c691fd855e6f22d0642965fc0c1617793368
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081343"
---
# <a name="quotes-and-quote-lines"></a>Sebut harga dan baris sebut harga

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dalam Dynamics 365 Project Service Automation, terdapat dua jenis sebut harga: sebut harga projek dan sebut harga jualan. Dua jenis itu berbeza mengikut cara berikut:

- Pada sebut harga jualan, terdapat hanya satu grid untuk item baris. Pada sebut harga projek, terdapat dua grid untuk item baris: satu untuk baris projek dan satu untuk baris produk.
- Sebut harga jualan menyokong pengaktifan dan semakan. Sebut harga projek tidak menyokong proses tersebut.
- Anda boleh melampirkan berbilang pesanan kepada sebut harga jualan. Anda boleh melampirkan hanya satu kontrak projek kepada sebut harga projek.
- Anda boleh memenangi sebut harga jualan dan menyimpan peluang yang berkaitan dibuka. Selepas sebut harga projek dimenangi, peluang yang berkaitan akan ditutup.
- Sebut harga jualan tidak termasuk beberapa medan dan konsep yang disertakan pada sebut harga projek yang mempunyai medan. Medan termasuk **Unit Kontrak** , **Pengurus Akaun** dan **Bil kepada Nama Kenalan**.  
- Sebut harga jualan dan sebut harga projek juga dikenal pasti oleh medan berasaskan set pilihan yang dinamakan **Jenis**. Untuk sebut harga jualan, medan ini mempunyai nilai **Berasaskan item**. Untuk sebut harga projek, ia mempunyai nilai **Berasaskan kerjas**.

Topik ini akan memberi tumpuan kepada butiran sebut harga projek.

Sebut harga projek dalam PSA boleh mempunyai berbilang baris item atau baris sebut harga. Malah, sebut harga projek mempunyai dua grid untuk item baris. Salah satu grid untuk projek berasaskan baris yang membolehkan anggaran terperinci. Grid lain ialah untuk talian berasaskan produk yang menggunakan harga unit ringkas dan pendekatan berasaskan kuantiti.

- **Berasaskan projek** – Jumlah (nilai disebut harga) ditentukan selepas anda menganggarkan jumlah kerja yang diperlukan. Anda boleh menganggarkan kerja pada peringkat tinggi atau anda boleh menganggarkan secara langsung sebagai butiran baris di bawah setiap baris sebut harga. Akhir sekali, anda boleh menganggarkan kerja berdasarkan anggaran alasan, dengan menggunakan pelan projek dan projek. Baris sebut harga berasaskan projek ditemui hanya dalam sebut harga berasaskan projek yang dicipta menggunakan Project Service Automation. Baris sebut harga jenis ini ialah borang disesuaikan bagi baris sebut harga tulis yang tersedia dalam Microsoft Dynamics 365 Sales.
- **Berasaskan produk** – Jumlah (nilai disebut harga) ditentukan berdasarkan kuantiti unit yang dijual dan harga jualan unit produk. Produk pada baris berasaskan produk boleh datang dari katalog produk dalam Jualan, atau ia boleh menjadi produk yang anda takrifkan. Jenis baris sebut harga ini juga tersedia pada sebut harga projek yang dicipta dengan menggunakan PSA.

Jumlah pada sebut harga ialah jumlah merentas baris berdasarkan produk dan baris berasaskan projek.

> [!NOTE]
> Sebut harga dan baris sebut harga tidak diperlukan dalam PSA. Anda boleh memulakan proses projek dengan kontrak projek (projek yang dijual). Walau bagaimanapun, peluang sentiasa diperlukan, tanpa mengira sama ada anda bermula dengan sebut harga atau kontrak projek.

## <a name="project-based-quote-lines"></a>Baris sebut harga berasarsan projek

Baris sebut harga berasaskan projek dalam PSA mempunyai kaedah pengebilan berikut:

- Masa dan bahan
- Harga tetap

### <a name="time-and-material"></a>Masa dan bahan

Masa dan kaedah pengebilan bahan adalah berdasarkan penggunaan. Apabila anda memilih kaedah pengebilan ini, pelanggan ialah diinvois sebagai kos berlaku projek. Invois dicipta berdasarkan kekerapan berkala berasaskan tarikh. Semasa proses jualan, nilai yang disebut harga bagi komponen masa dan bahan hanya memberikan anggaran kos terakhir kepada pelanggan. Vendor tidak akan melakukannya sendiri untuk melengkapkan projek pada nilai sebut harga yang disebut dengan betul. Komponen masa dan bahan meningkatkan risiko pelanggan. Pelanggan mungkin mahu berunding tambahan kepada klausa tidak melebihi untuk meminimumkan risiko mereka. PSA tidak menyokong tetapan tidak melebihi.

### <a name="fixed-price"></a>Harga tetap

Dalam kaedah pengebilan Harga tetap, vendor melakukan sendiri untuk menyampaikan projek dengan kos tetap kepada pelanggan. Pelanggan dibilkan nilai yang disebut bagi talian sebut harga tetap, tanpa mengira kos yang menyebabkan vendor untuk menyampaikan baris sebut harga tersebut. Nilai baris sebut harga tetap dibilkan dalam salah satu cara berikut: 

- Sebagai jumlah sekaligus pada permulaan atau akhir projek, atau apabila pencapaian projek dicapai. 
- Pada kekerapan berasaskan tarikh ansuran yang sama nilai tetap pada baris sebut harga. Ansuran ini dikenali sebagai pencapaian berkala.
- Pada ansuran yang mempunyai nilai kewangan yang sejajar dengan kemajuan kerja atau pencapaian khusus yang dicapai pada projek. Dalam kes ini, nilai setiap ansuran boleh berbeza, tetapi ia mesti menambah sehingga nilai tetap pada baris sebut harga.

PSA menyokong kesemua tiga jenis jadual invois untuk baris sebut harga tetap.

## <a name="transaction-classification"></a>Pengelasan transaksi

Organisasi perkhidmatan profesional biasanya sebut harga dan invois pelanggan mereka dengan pengelasan kos. Dalam PSA, kos akan diwakili oleh pengelasan transaksi berikut:

- **Masa** – Klasifikasi ini mewakili kos buruh atau masa sumber manusia untuk projek.
- **Perbelanjaan** : – Pengelasan ini mewakili semua jenis perbelanjaan lain pada projek. Kerana perbelanjaan boleh secara umum dikelaskan, kebanyakan organisasi mencipta subkategori, seperti perjalanan, sewa kereta, hotel atau bekalan pejabat.
- **Yuran** – Pengelasan ini mewakili overhed pelbagai, penalti dan barangan lain yang dikenakan kepada pelanggan. 
- **Cukai** – Pengelasan ini mewakili jumlah cukai yang pengguna tambah apabila mereka memasuki perbelanjaan.
- **Transaksi bahan** – Pengelasan ini mewakili aktual daripada barisan produk pada invois projek yang telah disahkan.
- **Pencapaian** – Klasifikasi ini digunakan oleh logik pengebilan harga tetap dalam PSA.

Satu atae lebih pengeleasan transaksi boleh dikaitkan dengan setiap baris sebut harga. Selepas sebut harga dimenangi, pemetaan antara klasifikasi transaksi dan baris sebut harga dipindahkan ke baris kontrak.
 
> ![Tangkapan skrin jenis transaksi pemetaan kepada sebut harga dan baris kontrak](media/basic-guide-5.png)
  
Sebagai contoh, sebut harga mungkin mengandungi dua baris sebut harga berikut: 
- Kerja perundingan yang menggunakan kaedah pengebilan masa dan bahan di mana pengelasan transaksi masa dan yuran dikenakan. Contohnya, semua transaksi masa dan yuran untuk projek contoh **Pelaksanaan Dynamics AX** ialah invois kepada pelanggan berdasarkan masa dan bahan yang digunakan. 
- Perbelanjaan perjalanan berkaitan yang menggunakan kaedah pengebilan harga tetap. Contohnya, semua perbelanjaan perjalanan untuk projek contoh **Pelaksanaan Dynamiscs AX** ialah invois pada nilai wang tetap.

> [!NOTE]
> Gabungan klasifikasi projek dan transaksi **Masa** , **Perbelanjaan** dan **Yuran** yang dikaitkan dengan baris sebut harga atau baris kontrak mesti unik. Jika gabungan projek dan transaksi yang sama kelas yang dikaitkan dengan lebih daripada satu baris kontrak atau baris sebut harga, PSA tidak akan berfungsi dengan betul.

## <a name="billing-types"></a>Jenis pengebilan

Medan **Jenis Pengebilan** mentakrifkan konsep boleh dikenaka cas dalam PSA. Ia ialah set pilihan yang mempunyai nilai mungkin berikut:

- **Boleh dikenakan cas** – Kos yang terakru oleh peranan/kategori ini ialah kos langsung yang mendorong pelaksanaan projek dan pelanggan akan membayar untuk kerja ini. Pembayaran boleh ditadbir sebagai masa dan bahan atau perkiraan harga tetap. Walau bagaimanapun, pekerja yang menghabiskan masa ini akan menerima kredit yang sesuai untuk penggunaan boleh dibilkan beliau.
- **Tidak boleh dikenakan cas** – Kos yang terakru oleh peranan/kategori ini ialah dianggap kos langsung yang mendorong pelaksanaan projek, walaupun pelanggan tidak mengenal pasti fakta ini dan tidak akan membayar untuk kerja ini. Pekerja yang menghabiskan masa ini tidak akan dikreditkan dengan penggunaan yang boleh dibilkan untuk itu.
- **Percuma** – Kos yang terakru oleh peranan/kategori ini ialah dianggap kos langsung yang mendorong pelaksanaan projek dan pelanggan mengenal pasti fakta ini. Pekerja yang menghabiskan masa ini tidak akan dikreditkan untuk penggunaan yang boleh dibilkan untuk itu. Walau bagaimanapun, kos ini tidak dicaj kepada pelanggan.
- **Tidak tersedia** – Kos yang berlaku ke atas projek dalaman yang tidak memerlukan penjejakan pendapatan dijejak dengan menggunakan pilihan ini.

## <a name="invoice-schedule"></a>Jadual invois

Jadual invois ialah siri tarikh apabila penginvoisan bagi projek berlaku. Anda secara pilihan boleh membuat jadual invois pada baris sebut harga dalam PSA. Setiap baris sebut harga boleh mempunyai jadual invois sendiri. Untuk mencipta jadual invois, anda mesti menyediakan nilai atribut berikut:

- Tarikh mula pengebilan 
- Tarikh penghantaran yang mewakili tarikh tamat pengebilan pada projek
- Kekerapan invois

PSA menggunakan tiga nilai atribut untuk menjana set tentatif tarikh untuk menetapkan invois.

## <a name="invoice-frequency"></a>Kekerapan invois

Kekerapan invois ialah entiti yang menyimpan nilai atribut yang membantu menerangkan kekerapan penciptaan invois. Atribut berikut menyatakan atau mentakrifkan entiti kekerapan Invois:

- **Tempoh** - Tempoh bulanan, dua kali seminggu dan mingguan disokong. 
- **Berjalan setiap tempoh** - Untuk tempoh mingguan dan dua kali seminggu, anda boleh mentakrifkan hanya satu jalanan setiap tempoh. Untuk tempoh bulanan, anda boleh mentakrifkan antara satu dan empat jalanan setiap tempoh. 
- **Hari jalanan** – Hari apabila penginvoisan patut dijalankan. Anda boleh mengkonfigurasi atribut ini dalam dua cara yang berbeza:
  - **Hari kerja** - Contohnya, anda boleh menentukan penginvoisan dijalankan setiap Isnin atau Isnin kedua. Pelanggan yang mesti menetapkan penginvoisan untuk dijalankan pada hari kerja mungkin lebih suka konfigurasi jenis ini. 
  - **Hari kalendar** – Contohnya, anda boleh menentukan penginvoisan yang dijalankan pada hari ketujuh dan dua puluh satu setiap bulan. Sesetengah organisasi mungkin lebih suka konfigurasi jenis ini, kerana ia membantu menjamin penginvoisan yang dijalankan pada jadual tetap setiap bulan.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Jadual invois untuk baris sebut harga tetap

Untuk baris sebut harga tetap, anda boleh menggunakan grid **Jadual Invois** untuk mencipta pencapaian pengebilan yang sama dengan nilai baris sebut harga.

- Untuk mencipta peristiwa pengebilan yang sama dibahagikan, pilih kekerapan invois, masukkan tarikh mula pengebilan pada baris sebut harga dan pilih **Tarikh Penyelesaian Diminta** diminta untuk sebut harga dalam bahagian **Ringkasan** bagi pengepala sebut harga. Kemudian pilih **Jana Pencapaian Berkala** berkala untuk mencipta pencapaian yang sama rata berdasarkan kekerapan invois yang dipilih. 
- Untuk mencipta pencapaian pengebilan sekaligus, cipta pencapaian dan kemudian masukkan nilai baris sebut harga sebagai jumlah pencapaian.
- Untuk mencipta pencapaian pengebilan berdasarkan tugas khusus dalam pelan projek, cipta pencapaian dan petakannya kepada elemen jadual projek dalam UI pencapaian pengebilan.
