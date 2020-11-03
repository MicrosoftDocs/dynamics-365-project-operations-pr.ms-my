---
title: Sebut harga - Konsep utama
description: Topik ini menyediakan maklumat tentang sebut harga projek dan jualan yang tersedia dalam Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 42ea1eb71b3285159b3fdf79ba34a562f948fd6e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081394"
---
# <a name="quotes---key-concepts"></a>Sebut harga - Konsep utama

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Dalam Dynamics 365 Project Operations, terdapat dua jenis sebut harga, projek dan jualan. Dua jenis sebut harga berbeza mengikut cara berikut:

- **Grid untuk item baris** : Pada sebut harga jualan, terdapat hanya satu grid untuk item baris. Pada sebut harga projek, terdapat dua grid untuk item baris. Satu grid adalah untuk baris projek dan yang lain untuk baris produk.
- **Pengaktifan dan semakan** : Sebut harga jualan menyokong pengaktifan dan semakan. Proses ini tidak disokong pada sebut harga projek.
- **Pesanan dilampirkan** : Anda boleh melampirkan berbilang pesanan kepada sebut harga jualan. Hanya satu kontrak projek boleh dilampirkan ke sebut harga projek.
- **Memenangi sebut harga** : Apabila anda memenangi sebut harga jualan, peluang yang berkaitan boleh kekal dibuka. Selepas sebut harga projek dimenangi, peluang yang berkaitan akan ditutup.
- **Medan dan konsep** : Sebut harga jualan tidak termasuk beberapa medan dan konsep yang disertakan pada sebut harga projek. Medan termasuk **Unit Kontrak** , **Pengurus Akaun** dan **Bil kepada Nama Kenalan**.  
- **Jenis** : Sebut harga jualan dan projek juga dikenal pasti oleh medan berasaskan set pilihan, **Jenis**. Untuk sebut harga jualan, medan ini mempunyai nilai **Berasaskan item**. Untuk sebut harga projek, ia mempunyai nilai **Berasaskan kerjas**.

Topik ini menumpu kepada butiran sebut harga projek.

Sebut harga projek dalam Project Operations boleh mempunyai berbilang baris item atau baris sebut harga. Malah, sebut harga projek mempunyai dua grid untuk item baris. Salah satu grid untuk projek berasaskan baris yang membolehkan anggaran terperinci. Grid lain ialah untuk talian berasaskan produk yang menggunakan harga unit ringkas dan pendekatan berasaskan kuantiti.

- **Berasaskan projek** : Nilai disebut harga ditentukan selepas anda menganggarkan jumlah kerja yang diperlukan. Anda boleh menganggarkan kerja pada peringkat tinggi, secara langsung sebagai butiran baris di bawah setiap baris sebut harga atau berasaskan anggaran asas dengan menggunakan projek dan pelan projek. Baris sebut harga berasaskan projek ditemui hanya dalam sebut harga berasaskan projek yang dicipta menggunakan Project Operations. Baris sebut harga jenis ini ialah borang disesuaikan bagi baris sebut harga tulis yang tersedia dalam Microsoft Dynamics 365 Sales.

- **Berasaskan produk** : Nilai disebut harga ditentukan berasaskan kuantiti unit yang dijual dan harga jualan unit. Produk pada baris berasaskan produk boleh datang dari katalog produk dalam Jualan, atau ia boleh menjadi produk yang anda takrifkan. Jenis baris sebut harga ini juga tersedia pada sebut harga berasaskan projek yang dicipta dengan menggunakan Project Operations.

Jumlah pada sebut harga ialah jumlah merentas baris berdasarkan produk dan baris berasaskan projek.

> [!NOTE]
> Sebut harga dan baris sebut harga tidak diperlukan dalam Project Operations. Anda boleh memulakan proses projek dengan kontrak projek (projek yang dijual). Walau bagaimanapun, peluang sentiasa diperlukan, tanpa mengira sama ada anda bermula dengan sebut harga atau kontrak projek.

## <a name="project-based-quote-lines"></a>Baris sebut harga berdasarkan projek

Baris sebut harga berasaskan projek dalam Project Operations mempunyai kaedah pengebilan berikut:

- Masa dan bahan
- Harga tetap

### <a name="time-and-material"></a>Masa dan bahan

Masa dan kaedah pengebilan bahan adalah berdasarkan penggunaan. Apabila anda memilih kaedah pengebilan ini, pelanggan ialah diinvois sebagai kos berlaku projek. Invois dicipta berdasarkan kekerapan berkala berasaskan tarikh. Semasa proses jualan, nilai yang disebut harga bagi komponen masa dan bahan hanya memberikan anggaran kos terakhir kepada pelanggan. Vendor tidak akan melakukannya sendiri untuk melengkapkan projek pada nilai sebut harga yang disebut dengan betul. Komponen masa dan bahan meningkatkan risiko pelanggan. Pelanggan mungkin mahu berunding tambahan kepada klausa tidak melebihi untuk meminimumkan risiko mereka. Project Operations tidak menyokong tetapan tidak melebihi.

### <a name="fixed-price"></a>Harga tetap

Dalam kaedah pengebilan Harga tetap, vendor melakukan sendiri untuk menyampaikan projek dengan kos tetap kepada pelanggan. Pelanggan dibilkan nilai yang disebut bagi talian sebut harga tetap, tanpa mengira kos yang menyebabkan vendor untuk menyampaikan baris sebut harga tersebut. Nilai baris sebut harga tetap dibilkan dalam salah satu cara berikut: 

- Sebagai jumlah sekaligus pada permulaan atau akhir projek, atau apabila pencapaian projek dicapai. 
- Pada kekerapan berasaskan tarikh ansuran yang sama nilai tetap pada baris sebut harga. Ansuran ini dikenali sebagai pencapaian berkala.
- Pada ansuran yang mempunyai nilai kewangan yang sejajar dengan kemajuan kerja atau pencapaian khusus yang dicapai pada projek. Dalam kes ini, nilai setiap ansuran boleh berbeza, tetapi ia mesti menambah sehingga nilai tetap pada baris sebut harga.

Project Operations menyokong kesemua tiga jenis jadual invois untuk baris sebut harga tetap.

## <a name="transaction-classification"></a>Pengelasan transaksi

Organisasi perkhidmatan profesional biasanya sebut harga dan invois pelanggan mereka dengan pengelasan kos. Kos akan diwakili oleh pengelasan transaksi berikut:

- **Masa** : Klasifikasi ini mewakili kos buruh atau masa sumber manusia pada projek.
- **Perbelanjaan** : Pengelasan ini mewakili semua jenis perbelanjaan lain pada projek. Kerana perbelanjaan boleh secara umum dikelaskan, kebanyakan organisasi mencipta subkategori, seperti perjalanan, sewa kereta, hotel atau bekalan pejabat.
- **Yuran** : Pengelasan ini mewakili pelbagai overhead, penalti dan item lain yang dikenakan kepada pelanggan. 
- **Cukai** : Pengelasan ini mewakili amaun cukai yang ditambah oleh pengguna apabila mereka memasukkan perbelanjaan.
- **Transaksi bahan** : Pengelasan ini mewakili aktual daripada barisan produk pada invois projek yang telah disahkan.
- **Pencapaian** : Pengelasan ini digunakan oleh logik pengebilan harga tetap.

Satu atae lebih pengeleasan transaksi boleh dikaitkan dengan setiap baris sebut harga. Selepas sebut harga dimenangi, pemetaan antara klasifikasi transaksi dan baris sebut harga dipindahkan ke baris kontrak.
  
Sebagai contoh, sebut harga mungkin mengandungi dua baris sebut harga berikut: 

- Kerja perundingan yang menggunakan kaedah pengebilan masa dan bahan di mana pengelasan transaksi masa dan yuran dikenakan. Contohnya, semua transaksi masa dan yuran untuk projek contoh **Pelaksanaan Dynamics AX** ialah invois kepada pelanggan berdasarkan masa dan bahan yang digunakan. 
- Perbelanjaan perjalanan berkaitan yang menggunakan kaedah pengebilan harga tetap. Contohnya, semua perbelanjaan perjalanan untuk projek contoh **Pelaksanaan Dynamiscs AX** ialah invois pada nilai wang tetap.

> [!NOTE]
> Gabungan klasifikasi projek dan transaksi **Masa** , **Perbelanjaan** dan **Yuran** yang dikaitkan dengan baris sebut harga atau baris kontrak mesti unik. Jika gabungan projek dan transaksi yang sama kelas dikaitkan dengan lebih daripada satu baris kontrak atau baris sebut harga, Project Operations tidak akan berfungsi dengan betul.

## <a name="billing-types"></a>Jenis pengebilan

Medan **Jenis Pengebilan** mentakrifkan konsep kebolehtuntutan. Ia ialah set pilihan yang mempunyai nilai mungkin berikut:

- **Boleh dituntut** : Kos yang terakru oleh peranan/kategori ini adalah kos langsung yang mendorong pelaksanaan projek dan pelanggan akan membayar untuk kerja ini. Pembayaran boleh ditadbir sebagai masa dan bahan atau perkiraan harga tetap. Walau bagaimanapun, pekerja yang menghabiskan masa ini akan menerima kredit yang sesuai untuk penggunaan boleh dibilkan beliau.
- **Tidak boleh dituntut** – Kos yang terakru oleh peranan/kategori ini adalah dianggap kos langsung yang mendorong pelaksanaan projek walaupun pelanggan tidak mengenali fakta ini dan tidak akan membayar untuk kerja ini. Pekerja yang menghabiskan masa ini tidak akan dikreditkan dengan penggunaan yang boleh dibilkan untuk itu.
- **Percuma** : Kos yang terakru oleh peranan/kategori ini adalah dianggap kos langsung yang mendorong pelaksanaan projek dan pelanggan mengenali fakta ini. Pekerja yang menghabiskan masa ini tidak akan dikreditkan untuk penggunaan yang boleh dibilkan untuk itu. Walau bagaimanapun, kos ini tidak dicaj kepada pelanggan.
- **Tidak tersedia** : Kos yang ditanggung ke atas projek dalaman yang tidak memerlukan penjejakan hasil dijejak dengan menggunakan pilihan ini.

## <a name="invoice-schedule"></a>Jadual invois

Jadual invois ialah siri tarikh apabila penginvoisan bagi projek berlaku. Anda secara pilihan boleh mencipta jadual invois pada baris sebut harga. Setiap baris sebut harga boleh mempunyai jadual invois sendiri. Untuk mencipta jadual invois, anda mesti menyediakan nilai atribut berikut:

- Tarikh mula pengebilan 
- Tarikh penghantaran yang mewakili tarikh tamat pengebilan pada projek
- Kekerapan invois

Tiga nilai atribut ini digunakan untuk menjana set tentatif tarikh untuk mewujudkan penginvoisan.

## <a name="invoice-frequency"></a>Kekerapan invois

Kekerapan invois ialah entiti yang menyimpan nilai atribut yang membantu menerangkan kekerapan penciptaan invois. Atribut berikut menyatakan atau mentakrifkan entiti kekerapan Invois:

- **Tempoh** : Tempoh bulanan, dua kali seminggu dan mingguan disokong. 
- **Jalan setiap tempoh** : Untuk tempoh mingguan dan dua kali seminggu, anda boleh mentakrifkan hanya satu jalanan setiap tempoh. Untuk tempoh bulanan, anda boleh mentakrifkan antara satu dan empat jalanan setiap tempoh. 
- **Hari jalanan** : Hari apabila penginvoisan patut dijalankan. Anda boleh mengkonfigurasi atribut ini dalam dua cara yang berbeza:
  - **Hari kerja** : Contohnya, anda boleh menentukan penginvoisan dijalankan setiap Isnin atau Isnin kedua. Pelanggan yang mesti menetapkan penginvoisan untuk dijalankan pada hari kerja mungkin lebih suka konfigurasi jenis ini. 
  - **Hari kalendar** : Contohnya, anda boleh menentukan penginvoisan dijalankan pada hari ketujuh dan dua puluh satu setiap bulan. Sesetengah organisasi mungkin lebih suka konfigurasi jenis ini, kerana ia membantu menjamin penginvoisan yang dijalankan pada jadual tetap setiap bulan.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Jadual invois untuk baris sebut harga tetap

Untuk baris sebut harga tetap, anda boleh menggunakan grid **Jadual Invois** untuk mencipta pencapaian pengebilan yang sama dengan nilai baris sebut harga.

- Untuk mencipta peristiwa pengebilan yang sama dibahagikan, pilih kekerapan invois, masukkan tarikh mula pengebilan pada baris sebut harga dan pilih **Tarikh Penyelesaian Diminta** diminta untuk sebut harga dalam bahagian **Ringkasan** bagi pengepala sebut harga. Kemudian pilih **Jana Pencapaian Berkala** berkala untuk mencipta pencapaian yang sama rata berdasarkan kekerapan invois yang dipilih. 
- Untuk mencipta pencapaian pengebilan sekaligus, cipta pencapaian dan kemudian masukkan nilai baris sebut harga sebagai jumlah pencapaian.
- Untuk mencipta pencapaian pengebilan berdasarkan tugas khusus dalam pelan projek, cipta pencapaian dan petakannya kepada elemen jadual projek dalam UI pencapaian pengebilan.
