---
title: Per diem perbelanjaan
description: Topik ini memberikan maklumat tentang cara bekerja dengan perbelanjaan setiap diem.
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
ms.openlocfilehash: fe72f066a6819c3b43e3977d5e7afb01ba95338c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596061"
---
# <a name="per-diem-expenses"></a>Per diem perbelanjaan

> [!IMPORTANT] 
> Fungsi yang diterangkan dalam topik ini tersedia untuk pengguna yang disasarkan sebagai sebahagian daripada keluaran pratonton.

Bayaran per diem adalah elaun harian tetap yang telah ditetapkan dan telah ditetapkan yang dibayar oleh syarikat kepada pekerjanya untuk penginapan (hotel), makanan, dan perbelanjaan sampingan yang ditanggung oleh pekerja tersebut semasa mereka melakukan perjalanan untuk bekerja. Syarikat membayar elaun ini kepada pekerja dan bukannya membayar perbelanjaan perjalanan sebenar. Pekerja boleh menggunakan Elaun Sampingan / Lain-lain **setiap diem mereka** untuk merangkumi petua, perkhidmatan bilik, dobi, atau perkhidmatan cucian kering untuk mesyuarat perniagaan penting. Kadar per diem boleh berbeza-beza, bergantung kepada sama ada majikan memilih untuk membayar balik kos gabungan penginapan dan makanan, atau hanya untuk kos makanan dan sampingan.

Kadar harian boleh berdasarkan masa dalam tahun, lokasi perjalanan atau kedua-duanya. Apabila anda membuat peraturan per diem, anda boleh menentukan bahawa peratusan kadar per diem akan ditahan jika pekerja menerima makanan atau perkhidmatan percuma. Anda juga boleh menetapkan bilangan jam minimum dan bilangan maksimum jam yang kadar per diem boleh digunakan untuk perjalanan pekerja.

Per diem dikira sebagai jumlah elaun yang ditawarkan setiap hari tolak pengurangan makanan (kos makanan percuma) yang diberikan kepada pekerja.

## <a name="configure-per-diems"></a>Configure per diems

Untuk mengkonfigurasi setiap perbelanjaan diem, ikuti langkah ini.

1. Pergi ke **Pengurusan Perbelanjaan** \> **Persediaan** \> **parameter** pengurusan Perbelanjaan Am.\>**·**
2. **Pada tab Per diem**, dalam **medan Kira pengurangan makanan mengikut**, pilih cara setiap diem harus dikira:

    - **Jenis makanan setiap perjalanan** - Kira per diem berdasarkan jenis makanan yang dimasukkan (sarapan, makan tengah hari, atau makan malam) dan pengurangan makanan yang ditentukan untuk setiap jenis hidangan untuk elaun per diem untuk tempoh perjalanan.
    - **Jenis makanan setiap hari** – Kira per diem berdasarkan jenis makanan yang dimasukkan dan pengurangan makanan yang ditentukan untuk setiap jenis hidangan untuk elaun per diem setiap hari.
    - **Bilangan makanan setiap hari** – Kira per diem berdasarkan bilangan makanan yang dimasukkan setiap hari dan pengurangan makanan untuk bilangan makanan yang disediakan setiap hari.

3. Pergi ke **Pengurusan Perbelanjaan** \> **Persediaan** \> **Pengiraan dan kod** \> **Setiap lokasi** diem.
4. Tambah lokasi di mana setiap diem boleh digunakan.
5. Untuk setiap lokasi yang anda tambah, pada **tab Per diems**, pilih kadar per diem dan mata wang yang sah antara tarikh mula dan akhir tertentu untuk penginapan, makanan dan perbelanjaan lain. Untuk mengkonfigurasi setiap kadar diem dan mata wang, pergi ke **Pengiraan Persediaan** \> **pengurusan** \> **Perbelanjaan dan kod** \> **Per diems.**

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Setiap diem dalam antara muka perbelanjaan yang dibayangkan semula

Ciri per diem disokong dalam ruang kerja Pengurusan **Perbelanjaan yang dibayangkan semula** dalam Microsoft Dynamics 365 Kewangan versi 10.0.25 dan lebih baru.

Untuk mendayakan setiap diem, ikuti langkah ini.

1. **Dalam ruang kerja Pengurusan** Ciri, cari dan pilih **ciri Laporan Perbelanjaan Yang Dibayangkan Semula** dalam senarai, kemudian pilih **Dayakan sekarang**.
2. Cari dan pilih **ciri Antara muka** yang dibayangkan semula oleh laporan per-diem untuk perbelanjaan dalam senarai, kemudian pilih **Dayakan sekarang**.

## <a name="how-the-feature-works"></a>Bagaimana ciri berfungsi

Bahagian ini memberikan contoh untuk tiga senario konfigurasi. Untuk setiap contoh, **kira pengurangan makanan mengikut** medan disetkan kepada nilai yang berbeza. Bagi ketiga-tiga contoh, jumlah yang perlu dibayar adalah sama sehingga pengurangan makanan dikenakan. Selepas itu, jumlah amaun yang perlu dibayar berbeza untuk setiap contoh.

Untuk mencipta perbelanjaan per diem yang digunakan untuk ketiga-tiga contoh, ikuti langkah ini.

1. Pergi ke **Pengurusan Perbelanjaan Ruang Kerja** \> **.**
2. Pilih **Laporan perbelanjaan baharu** atau pilih laporan perbelanjaan sedia ada.
3. Tambah perbelanjaan baru. **Dalam medan Kategori**, pilih **Setiap diem**. Pilih lokasi, dan tarikh mula dan tamat perjalanan anda. Per diem untuk penginapan, makanan, dan sampingan (perbelanjaan lain) dikira berdasarkan elaun harian yang ditetapkan untuk lokasi yang dipilih.

    Sebagai contoh, anda memilih **Redmond (AS)** sebagai lokasi. Elaun harian untuk lokasi itu ialah 150 dolar AS (USD 150) untuk penginapan, USD 75 untuk makan, dan USD 5 untuk sampingan. Tarikh mula ialah 10 Januari, dan tarikh akhir ialah 14 Januari. Oleh itu, tempoh yang dipilih adalah lima hari apabila konfigurasi yang dipilih adalah hari kalendar dengan masa, dan masa yang dipilih bermula dan berakhir pada jam 12:00 pagi pada tarikh mula dan akhir. Berikut adalah pengiraan:

    - Jumlah amaun yang perlu dibayar = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
    - Bahagian makan dan sampingan jumlah keseluruhan = 5 × (75 + 5) = USD 400

Sekiranya sarapan pagi, makan tengah hari, dan makan malam disediakan semasa perjalanan, makanan tersebut mesti diambil kira sebagai pengurangan makanan.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Contoh 1: Per diem di mana pengurangan makanan adalah berdasarkan jenis makanan setiap perjalanan

Dalam contoh ini, pengurangan makanan adalah 30 peratus untuk sarapan pagi, 30 peratus untuk makan tengah hari, dan 40 peratus untuk makan malam. **Pada halaman Parameter** pengurusan Perbelanjaan, **medan Kira pengurangan makanan mengikut** medan disetkan kepada **Jenis makanan bagi setiap perjalanan**. Berikut adalah pengiraan jika tiga sarapan pagi, dua makan tengah hari, dan makan malam sifar disediakan kepada pekerja:

- Pengurangan makanan = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22.50) + (2 × 22.50) + 0 = 67.50 + 45 + 0 = USD 112.50
- Makanan dan sampingan = 400 - 112.50 = USD 287.50
- Jumlah amaun yang perlu dibayar = Jumlah elaun – Pengurangan makanan = 1,150 – 112.50 = USD 1,037.50

![Setiap perbelanjaan diem di mana pengurangan makanan adalah berdasarkan jenis makanan setiap perjalanan.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Contoh 2: Setiap diem di mana pengurangan makanan adalah berdasarkan jenis makanan setiap hari

Dalam contoh ini, pengurangan makanan adalah 30 peratus untuk sarapan pagi, 30 peratus untuk makan tengah hari, dan 40 peratus untuk makan malam. **Pada halaman Parameter** pengurusan perbelanjaan, **medan Kira pengurangan makanan mengikut** medan disetkan kepada **jenis Makanan setiap hari**. Dalam kes ini, dalam **grid Makanan** dalam **kotak dialog Edit perbelanjaan**, anda mengosongkan kotak semak untuk menunjukkan makanan yang diberikan kepada anda semasa perjalanan anda.

Sebagai contoh, berikut adalah pengiraan jika sarapan disediakan untuk tiga hari pertama perjalanan:

- Pengurangan makanan harian untuk setiap tiga hari pertama = 75 × 30% = USD 22.50
- Jumlah pengurangan makanan = 3 × 22.50 = USD 67.50
- Makanan dan sampingan untuk hari 1 hingga 3 = 75 - 22.50 = USD 57.50
- Jumlah makanan dan sampingan = Jumlah makanan dan sampingan sepanjang lima hari = 400 – 67.50 = USD 332.50
- Jumlah amaun yang perlu dibayar = Jumlah amaun – Pengurangan makanan = 1,150 – 67.50 = USD 1,082.50

![Setiap perbelanjaan diem di mana pengurangan makanan adalah berdasarkan jenis makanan setiap hari.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Contoh 3: Setiap diem di mana pengurangan makanan adalah berdasarkan bilangan makanan setiap hari

Dalam contoh ini, pengurangan makanan dikira berdasarkan bilangan makanan yang disediakan setiap hari (iaitu, **pengiraan pengurangan makanan mengikut** medan pada **halaman parameter** pengurusan Perbelanjaan ditetapkan kepada **Bilangan makanan setiap hari**). **Dalam grid Makanan** dalam **kotak dialog Edit perbelanjaan**, anda mengosongkan kotak semak untuk menunjukkan makanan yang disediakan.
Dalam kes ini, pengurangan makanan hanya berdasarkan # makanan yang disediakan, dan bukan pada jenis makanan (Sarapan / makan tengah hari / makan malam) yang disediakan.

Berikut adalah pengiraan untuk setiap diem apabila elaun harian USD 150 untuk penginapan, USD 75 untuk makan, dan USD 5 untuk sampingan:

- **Jumlah amaun yang perlu dibayar** = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
- **Satu hidangan:** Pengurangan makanan = 20% = USD 15
- **Dua kali makan:** Pengurangan makanan = 50% = USD 37.50
- **Tiga kali makan:** Pengurangan makanan = 100% = USD 75

Berikut adalah pengiraan untuk **elaun makanan dan sampingan**, yang termasuk USD 5 untuk sampingan:

- Hari 1 - Dua hidangan disediakan = (75 - 37.50) + 5 = 37.50 + 5 = USD 42.50
- Hari 2 - Dua hidangan disediakan = (75 - 37.50) + 5 = 37.50 + 5 = USD 42.50
- Hari 3 - Satu hidangan disediakan = (75 - 15) + 5 = 60 + 5 = USD 65
- Hari 4 - Makanan sifar disediakan = (75-0) + 5 = 75 + 5 = USD 80
- Hari 5 - Tiga hidangan disediakan = (75 - 75) + 5 = 0 + 5 = USD 5

- Jumlah makanan dan sampingan = Makanan dan Sampingan untuk Hari 1+ Hari 2 +Hari 3+Hari 4+ Hari 5 = USD 235
- Jumlah pengurangan makanan = Pengurangan makanan untuk Hari 1+ Hari 2 +Hari 3+Hari 4+ Hari 4+ Hari 5= 37.5+ 37.5+ 15 + 0+ 75 = USD 165
- Jumlah amaun yang perlu dibayar = Jumlah elaun - Jumlah pengurangan makanan = USD 1,150 - USD 165 = USD 985

![Setiap perbelanjaan diem di mana pengurangan makanan adalah berdasarkan bilangan makanan setiap hari.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Pada versi Kewangan 10.0.23, jika anda menggunakan antara muka perbelanjaan yang dibayangkan semula, anda tidak boleh membuat perbelanjaan per diem yang mempunyai tarikh bertindih. Jika anda cuba, anda akan menerima mesej ralat.
