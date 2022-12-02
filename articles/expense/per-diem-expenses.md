---
title: Perbelanjaan saraan harian
description: Artikel ini memberikan maklumat tentang cara untuk bekerja dengan perbelanjaan saraan harian.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0d2f95b677720726049d7d010e9738ad8c513802
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923199"
---
# <a name="per-diem-expenses"></a>Perbelanjaan saraan harian

> [!IMPORTANT] 
> Fungsi yang diterangkan dalam artikel ini tersedia untuk pengguna yang disasarkan sebagai sebahagian daripada keluaran pratonton.

Bayaran saraan harian ialah elaun harian tetap yang ditentukan terlebih dahulu dan dibayar oleh syarikat kepada pekerja untuk penginapan (hotel), hidangan dan perbelanjaan sampingan yang ditanggung oleh pekerja semasa mereka membuat perjalanan untuk kerja. Syarikat membayar elaun ini kepada pekerja dan bukannya membayar perbelanjaan perjalanan sebenar. Pekerja boleh menggunakan elaun saraan harian **Sampingan/Lain-lain** mereka untuk meliputi tip, perkhidmatan bilik, dobi atau perkhidmatan cucian kering untuk mesyuarat perniagaan penting. Kadar saraan harian boleh berubah-ubah, bergantung pada sama ada majikan memilih untuk membayar balik kos gabungan penginapan dan hidangan, atau hanya untuk kos makan dan sampingan.

Kadar harian boleh berdasarkan masa dalam tahun, lokasi perjalanan atau kedua-duanya. Apabila anda mencipta peraturan saraan harian, anda boleh menentukan bahawa peratusan kadar saraan harian akan ditahan jika pekerja menerima hidangan atau perkhidmatan percuma. Anda juga boleh menetapkan bilangan jam minimum dan maksimum yang kadar saraan harian boleh digunakan pada perjalanan pekerja.

Saraan harian dikira sebagai jumlah elaun yang ditawarkan setiap hari ditolak pengurangan hidangan (kos hidangan percuma) yang disediakan kepada pekerja.

## <a name="configure-per-diems"></a>Konfigurasikan saraan harian

Untuk mengkonfigurasi perbelanjaan saraan harian, ikut langkah ini.

1. Pergi ke **Pengurusan perbelanjaan** \> **Persediaan** \> **Umum** \> **Parameter pengurusan perbelanjaan**.
2. Pada tab **Saraan harian**, dalam medan **Kira pengurangan hidangan mengikut**, pilih cara saraan harian patut dikira:

    - **Jenis hidangan setiap perjalanan** – Kira saraan harian berdasarkan jenis hidangan yang dimasukkan (sarapan pagi, makan tengah hari atau makan malam) dan pengurangan hidangan yang ditetapkan untuk setiap jenis hidangan bagi elaun saraan harian untuk tempoh perjalanan.
    - **Jenis hidangan setiap hari** – Kira saraan harian berdasarkan jenis hidangan yang dimasukkan dan pengurangan hidangan yang ditetapkan untuk setiap jenis hidangan bagi elaun saraan harian setiap hari.
    - **Bilangan hidangan sehari** – Kira saraan harian berdasarkan bilangan hidangan yang dimasukkan setiap hari dan pengurangan hidangan untuk bilangan hidangan yang disediakan setiap hari.

3. Pergi ke **Pengurusan perbelanjaan** \> **Persediaan** \> **Pengiraan dan kod** \> **Lokasi saraan harian**.
4. Tambah lokasi saraan harian boleh digunakan.
5. Untuk setiap lokasi yang anda tambahkan, pada tab **Saraan harian**, pilih kadar saraan harian dan mata wang yang sah antara tarikh mula dan tamat tertentu untuk penginapan, hidangan dan perbelanjaan lain. Untuk mengkonfigurasi kadar saraan harian dan mata wang, pergi ke **Pengurusan perbelanjaan** \> **Persediaan** \> **Pengiraan dan kod** \> **Saraan harian**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Saraan harian dalam antara muka perbelanjaan gambaran semula

Ciri saraan harian disokong dalam ruang kerja **Pengurusan Perbelanjaan** gambaran semula dalam Microsoft Dynamics 365 Finance versi 10.0.25 dan lebih tinggi.

Untuk mendayakan saraan harian, ikut langkah berikut.

1. Dalam ruang kerja **Pengurusan Ciri**, cari dan pilih ciri **Laporan Perbelanjaan Gambaran Semula** dalam senarai dan kemudian pilih **Dayakan sekarang**.
2. Cari dan pilih ciri **Antara muka saraan harian untuk laporan perbelanjaan gambaran semula** dalam senarai dan kemudian pilih **Dayakan sekarang**.

## <a name="how-the-feature-works"></a>Cara ciri berfungsi

Bahagian ini menyediakan contoh untuk tiga senario konfigurasi. Untuk setiap contoh, medan **Kira pengurangan hidangan mengikut** ditetapkan pada nilai yang berbeza. Bagi ketiga-tiga contoh, jumlah amaun yang perlu dibayar adalah sama sehingga pengurangan hidangan dikenakan. Selepas peringkat itu, jumlah amaun yang perlu dibayar berbeza untuk setiap contoh.

Untuk mencipta perbelanjaan saraan harian yang digunakan untuk ketiga-tiga contoh, ikut langkah ini.

1. Pergi ke **Ruang kerja** \> **Pengurusan Perbelanjaan**.
2. Pilih **Laporan perbelanjaan baharu** atau pilih laporan perbelanjaan sedia ada.
3. Tambah perbelanjaan baharu. Dalam medan **Kategori**, pilih **Saraan harian**. Pilih lokasi, tarikh mula dan tamat perjalanan anda. Saraan harian bagi penginapan, hidangan dan sampingan (perbelanjaan lain) dikira berdasarkan elaun harian yang ditetapkan untuk lokasi yang dipilih.

    Contohnya, anda pilih **Redmond (AS)** sebagai lokasi. Elaun harian untuk lokasi tersebut ialah 150 US Dolar (USD150) untuk penginapan, USD75 untuk hidangan dan USD5 untuk sampingan. Tarikh mula ialah 10 Januari dan tarikh tamat ialah 14 Januari. Oleh itu, tempoh yang dipilih ialah lima hari apabila konfigurasi yang dipilih ialah hari kalendar dengan masa dan masa yang dipilih bermula dan berakhir pada 12:00 am pada tarikh mula dan tamat. Berikut ialah pengiraan:

    - Jumlah amaun perlu dibayar = 5 × (150 + 75 + 5) = 5 × 230 = USD1,150
    - Bilangan hidangan dan sampingan daripada jumlah keseluruhan = 5 × (75 + 5) = USD400

Jika sarapan pagi, makan tengah hari dan makan malam disediakan semasa perjalanan, hidangan tersebut mesti diambil kira sebagai pengurangan hidangan.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Contoh 1: Saraan harian yang pengurangan hidangan adalah berdasarkan jenis hidangan setiap perjalanan

Dalam contoh ini, pengurangan hidangan ialah 30 peratus untuk sarapan pagi, 30 peratus untuk makan tengah hari dan 40 peratus untuk makan malam. Pada halaman **Parameter pengurusan perbelanjaan**, medan **Kira pengurangan hidangan mengikut** ditetapkan kepada **Jenis hidangan setiap perjalanan**. Berikut ialah pengiraan jika tiga sarapan pagi, dua makan tengah hari dan tiada makan malam disediakan kepada pekerja:

- Pengurangan hidangan = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22.50) + (2 × 22.50) + 0 = 67.50 + 45 + 0 = USD112.50
- Hidangan dan sampingan = 400 – 112.50 = USD287.50
- Jumlah amaun perlu dibayar = Jumlah elaun – Pengurangan hidangan = 1,150 – 112.50 = USD1,037.50

![Perbelanjaan saraan harian yang pengurangan hidangan adalah berdasarkan jenis hidangan setiap perjalanan.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Contoh 2: Saraan harian yang pengurangan hidangan adalah berdasarkan jenis hidangan setiap hari

Dalam contoh ini, pengurangan hidangan ialah 30 peratus untuk sarapan pagi, 30 peratus untuk makan tengah hari dan 40 peratus untuk makan malam. Pada halaman **Parameter pengurusan perbelanjaan**, medan **Kira pengurangan hidangan mengikut** ditetapkan kepada **Jenis hidangan setiap hari**. Dalam kes ini, dalam grid **Hidangan** dalam kotak dialog **Edit perbelanjaan**, anda kosongkan kotak semak untuk menunjukkan hidangan yang disediakan kepada anda semasa perjalanan anda.

Sebagai contoh, berikut ialah pengiraan jika sarapan disediakan untuk tiga hari pertama perjalanan:

- Pengurangan hidangan harian untuk setiap satu daripada tiga hari pertama = 75 × 30% = USD22.50
- Jumlah pengurangan hidangan = 3 × 22.50 = USD67.50
- Hidangan dan sampingan untuk hari 1 hingga 3 = 75 – 22.50 = USD57.50
- Jumlah hidangan dan sampingan = Jumlah hidangan dan sampingan sepanjang lima hari = 400 – 67.50 = USD332.50
- Jumlah amaun perlu dibayar = Jumlah amaun – Pengurangan hidangan = 1,150 – 67.50 = USD1,082.50

![Perbelanjaan saraan harian yang pengurangan hidangan adalah berdasarkan jenis hidangan setiap hari.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Contoh 3: Saraan harian yang pengurangan hidangan adalah berdasarkan bilangan hidangan setiap hari

Dalam contoh ini, pengurangan hidangan dikira berdasarkan bilangan hidangan yang disediakan setiap hari (iaitu, medan **Kira pengurangan hidangan mengikut** pada halaman **Parameter pengurusan perbelanjaan** ditetapkan pada **Bilangan hidangan setiap hari**). Dalam grid **Hidangan** dalam kotak dialog **Edit perbelanjaan**, anda kosongkan kotak semak untuk menunjukkan hidangan yang disediakan.
Dalam kes ini, pengurangan hidangan adalah hanya berdasarkan # hidangan yang disediakan dan bukan jenis hidangan (Sarapan/makan tengah hari/makan malam) yang disediakan.

Berikut ialah pengiraan saraan harian apabila elaun harian ialah USD150 untuk penginapan, USD75 untuk hidangan dan USD5 untuk sampingan:

- **Jumlah amaun perlu dibayar** = 5 × (150 + 75 + 5) = 5 × 230 = USD1,150
- **Satu hidangan:** Pengurangan hidangan = 20% = USD15
- **Dua hidangan:** Pengurangan hidangan = 50% = USD37.50
- **Tiga hidangan:** Pengurangan hidangan = 100% = USD75

Berikut ialah pengiraan untuk **elaun hidangan dan sampingan** yang termasuk USD5 untuk sampingan:

- Hari 1 - Dua hidangan disediakan = (75 – 37.50) + 5 = 37.50 + 5 = USD42.50
- Hari 2 - Dua hidangan disediakan = (75 – 37.50) + 5 = 37.50 + 5 = USD42.50
- Hari 3 - Satu hidangan disediakan = (75 – 15) + 5 = 60 + 5 = USD65
- Hari 4 - Tiada hidangan disediakan = (75 – 0) + 5 = 75 + 5 = USD80
- Hari 5 - Tiga hidangan disediakan = (75 – 75) + 5 = 0 + 5 = USD5

- Jumlah hidangan dan sampingan = Hidangan dan Sampingan untuk Hari 1 + Hari 2 + Hari 3 + Hari 4 + Hari 5 = USD235
- Jumlah pengurangan hidangan = Pengurangan hidangan untuk Hari 1 + Hari 2 + Hari 3 + Hari 4 + Hari 5 = 37.5 + 37.5 + 15 + 0 + 75 = USD165
- Jumlah amaun perlu dibayar = Jumlah elaun – Jumlah pengurangan hidangan = USD1,150 – USD165 = USD985

![Perbelanjaan saraan harian yang pengurangan hidangan adalah berdasarkan bilangan hidangan setiap hari.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Setakat Finance versi 10.0.23, jika anda menggunakan antara muka perbelanjaan gambaran semula, anda tidak boleh mencipta perbelanjaan saraan harian yang mempunyai tarikh bertindan. Jika anda mencuba, anda akan menerima mesej ralat.
