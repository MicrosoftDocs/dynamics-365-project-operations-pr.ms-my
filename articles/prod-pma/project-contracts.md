---
title: Kontrak projek
description: Topik ini menyediakan contoh kontrak projek yang boleh anda cipta untuk pelbagai jenis produk dan sumber pembiayaan serta cara anda boleh mengurus kontrak dan menginvois pelanggan projek.
author: Yowelle
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7d15523f1b22bb8813a47f9f822f12bc4162104
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081359"
---
# <a name="project-contracts"></a>Kontrak projek

[!include [banner](../includes/banner.md)]

Artikel ini menyediakan contoh kontrak projek yang boleh anda cipta untuk pelbagai jenis produk dan sumber pembiayaan serta cara anda boleh mengurus kontrak dan menginvois pelanggan projek.

Jenis projek yang anda cipta untuk kontrak projek menentukan kaedah yang digunakan untuk menginvois pelanggan projek. Anda boleh mengubah kontrak projek dan projek yang berkaitan tetapi anda tidak boleh mengubah jenis projek. 

Dengan menggunakan kontrak projek, anda boleh menginvois satu atau lebih projek pada masa yang sama. Kontrak projek juga membantu menjamin prosedur penginvoisan yang konsisten untuk setiap subprojek dalam struktur projek. 

Setiap projek yang akan diinvoiskan mesti berkaitan dengan kontrak projek. Tetapan untuk kontrak projek terpakai kepada semua projek dan subprojek yang berkaitan dengan kontrak projek tersebut. 

Kontrak projek boleh menentukan satu atau lebih sumber pembiayaan. Oleh itu, anda boleh memisahkan pengebilan antara berbilang pembiaya, menyediakan had pembiayaan supaya sumber pembiayaan tidak dibilkan lebih daripada amaun yang ditentukan dan mengkonfigurasikan peraturan pembiayaan untuk mengecaj perbelanjaan.

## <a name="funding-for-project-contracts"></a>Pembiayaan untuk kontrak projek
Beberapa kontrak projek menentukan bahawa berbilang pihak mempunyai tanggungjawab bersama untuk membiayai kos projek. Berikut adalah beberapa contoh:

-   Pelanggan besar yang mempunyai berbilang bahagian meminta agar pembiayaan projek dipisahkan mengikut bahagian.
-   Syarikat anda berkongsi kod projek besar dengan organisasi luar.
-   Projek jalan dibiayai bersama oleh dua majlis perbandaran.
-   Projek jambatan dibiayai oleh geran kerajaan dan syarikat swasta.

Dalam Dynamics 365 Finance, anda boleh memisahkan pengebilan untuk transaksi tunggal atau keseluruhan projek antara berbilang pelanggan, geran atau organisasi. 

Dalam projek yang mempunyai berbilang pembiaya, semua pihak yang menyumbang kepada pembiayaan projek pembiayaan awal dipanggil sumber pembiayaan. Selepas pelanggan, organisasi atau pelan ditakrifkan sebagai sumber pembiayaan, ia boleh diperuntukkan kepada satu atau lebih peraturan pembiayaan. Peraturan pembiayaan mengandungi kriteria yang menentukan cara caj diperuntukkan kepada pelbagai sumber pembiayaan untuk projek. 

Disebabkan item stok, seperti yang muncul pada pemerolehan pembelian dan pesanan pembelian, tidak boleh dipisahkan, amaun kos tidak boleh dipisahkan antara berbilang sumber pembiayaan pada waktu pengagihan. Oleh itu, nilai sumber pembiayaan kekal 0 (sifar) sehingga isu inventori disiarkan. Apabila isu inventori disiarkan, amaun kos diagihkan mengikut peraturan pengagihan akaun untuk projek tersebut.

Berikut beberapa langkah yang boleh anda ambil untuk menjadikannya lebih mudah untuk memisahkan pengebilan antara berbilang sumber pembiayaan:

-   Tentukan bahawa semua transaksi yang dimasukkan untuk projek menggunakan mata wang jualan yang sama seperti kontrak projek.
-   Sediakan had pembiayaan, supaya sumber pembiayaan tidak diinvoiskan lebih daripada amaun yang ditentukan terhadap projek.
-   Konfigurasikan peraturan pembiayaan dan had pembiayaan untuk setiap pekerja, item, kategori, kumpulan kategori dan jenis transaksi (atau untuk semua jenis transaksi).
-   Pilih tarikh mula dan tamat pilihan untuk mentakrifkan tempoh apabila setiap peraturan pembiayaan adalah sah.
-   Tentukan peratusan yang menjadi tanggungjawab setiap sumber pembiayaan.
-   Tentukan sumber pembiayaan yang bertanggungjawab terhadap perbezaan pembundaran yang disebabkan oleh pengiraan peruntukan pembiayaan.
-   Sediakan peraturan yang menentukan cara kos projek diinvoiskan kepada pelanggan luar dan dicaj kepada organisasi luar.
-   Rekodkan transaksi dalam akaun pembiayaan yang ditahan sehingga pembiayaan tambahan boleh diperoleh atau sehingga anda memutuskan untuk menanggung kos secara dalaman.

Untuk menentukan kumpulan cukai yang akan dikaitkan dengan transaksi, projek dicari untuk tugasan kumpulan cukai. Jika tiada tugasan kumpulan cukai telah dibuat pada peringkat projek, kontrak projek dicari.

### <a name="example-multiple-funding-sources-simple"></a>Contoh: Berbilang sumber pembiayaan (ringkas)

Jadual yang berikut memberikan senario untuk menguruskan peruntukan pembiayaan antara berbilang sumber pembiayaan. Senario ini berdasarkan anggapan yang berikut:

-   Tetapan keutamaan difaktorkan ke dalam peruntukan dana sebelum kriteria peraturan pembiayaan lain dikenakan.
-   Tiada julat tarikh telah ditentukan untuk mentakrifkan tempoh d apabila peraturan pembiayaan adalah sah.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Senario</strong></td>
<td><strong>Sumber pembiayaan</strong></td>
<td><strong>Peratusan peruntukan</strong></td>
<td><strong>Keutamaan peruntukan</strong></td>
</tr>
<tr class="even">
<td>Anda mahu menguntukkan kos kepada sumber pembiayaan pertama sehingga dananya habis, menguntukkan kos kepada sumber pembiayaan kedua sehingga dananya habis dan akhir sekali menguntukkan kos yang tinggal kepada sumber pembiayaan ketiga.</td>
<td><ul>
<li>Sumber pembiayaan 1</li>
<li>Sumber pembiayaan 2</li>
<li>Sumber pembiayaan 3</li>
</ul></td>
<td><ul>
<li>100%</li>
<li>100%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Anda mahu menguntukkan 75 peratus kos kepada sumber pembiayaan pertama dan 25 peratus kepada sumber pembiayaan kedua. Apabila sama ada sumber pembiayaan tersebut habis, anda mahu membayar kos yang tinggal daripada sumber pembiayaan ketiga.</td>
<td><ul>
<li>Sumber pembiayaan 1</li>
<li>Sumber pembiayaan 2</li>
<li>Sumber pembiayaan 3</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Anda mahu menguntukkan 75 peratus kos kepada sumber pembiayaan pertama dan 25 peratus kepada sumber pembiayaan kedua. Apabila sama ada sumber pembiayaan tersebut habis, anda mahu memisahkan kos yang tinggal antara sumber pembiayaan ketiga dan sumber pembiayaan keempat.</td>
<td><ul>
<li>Sumber pembiayaan 1</li>
<li>Sumber pembiayaan 2</li>
<li>Sumber pembiayaan 3</li>
<li>Sumber pembiayaan 4</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>50%</li>
<li>50%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Anda mahu menguntukkan 25 peratus kos pertama kepada sumber pembiayaan pertama dan selebihnya kepada sumber pembiayaan kedua.</td>
<td><ul>
<li>Sumber pembiayaan 1</li>
<li>Sumber pembiayaan 2</li>
</ul></td>
<td><ul>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Contoh: Berbilang sumber pembiayaan (rumit)

Anda mempunyai tiga sumber pembiayaan yang anda mahu gunakan dalam terbit yang berikut:

1.  Gunakan sumber pembiayaan 2 dan sumber pembiayaan 3 secara sama rata sehingga sumber pembiayaan 2 habis.
2.  Terus menggunakan sumber pembiayaan 3 sehingga ia habis.
3.  Gunakan sumber pembiayaan 1 selepas sumber pembiayaan 3 habis.

Untuk mencapai matlamat ini, anda mesti melakukan perkara berikut:

-   Sediakan had pembiayaan untuk sumber pembiayaan 2 dan sumber pembiayaan 3 bagi amaun mereka masing-masing.
-   Cipta peraturan pembiayaan yang berikut:
    -   Peraturan 1 (Keutamaan 1): Peruntukkan 50 peratus transaksi kepada sumber pembiayaan 2 dan 50 peratus kepada sumber pembiayaan 3.
    -   Peraturan 2 (Keutamaan 2): Peruntukkan 100 peratus transaksi kepada sumber pembiayaan 3.
    -   Peraturan 3 (Keutamaan 3): Peruntukkan 100 peratus transaksi kepada sumber pembiayaan 1.

Persediaan ini berfungsi kerana transaksi disemak terhadap peraturan dan had untuk menentukan sama ada mana-mana daripadanya dikenakan kepada transaksi. Jika tiada peraturan atau had khusus dikenakan kepada transaksi, Semua peraturan transaksi dikenakan. Semua peraturan transaksi sepadan dengan semua transaksi. 

Jika peraturan didapati sepadan dengan transaksi, peratusan yang telah diperuntukkan dalam peraturan tersebut dikenakan dahulu tetapi hanya selepas padanan disemak terhadap sebarang had yang telah disediakan. Jika had telah dicapai dan dana sumber pembiayaan habis, peraturan pembiayaan yang berkaitan dengan had pembiayaan tersebut diabaikan dan semakan program untuk peraturan seterusnya dikenakan. 

Dalam sesetengah kes, hanya sebahagian transaksi boleh diperuntukkan di bawah peraturan. Ini mungkin berlaku disebabkan had dicapai apabila transaksi diperuntukkan. Dalam kes ini, hanya amaun tertentu diperuntukkan mengikut peraturan tersebut, seperti 50 peratus untuk setiap sumber pembiayaan. Ini ialah kes dalam peraturan 1, yang dihuraikan lebih awal dalam bahagian ini. Selebihnya diperuntukkan mengikut peraturan seterusnya dalam jujukan. 

Jadual yang berikut memeriksa senario ini dengan lebih terperinci.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Fokus</strong></td>
<td><strong>Butiran</strong></td>
</tr>
<tr class="even">
<td>Peraturan pembiayaan</td>
<td><ul>
<li>Peraturan 1 (Keutamaan 1): Semua transaksi. Peruntukkan sumber pembiayaan 2 pada 50% dan sumber pembiayaan 3 pada 50%.</li>
<li>Peraturan 2 (Keutamaan 2): Semua transaksi. Peruntukkan sumber pembiayaan 3 pada 100%.</li>
<li>Peraturan 3 (Keutamaan 2): Semua transaksi. Peruntukkan sumber pembiayaan 1 pada 100%.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Had pembiayaan</td>
<td><ul>
<li>Had sumber pembiayaan 1 = 10,000.00</li>
<li>Had sumber pembiayaan 2 = 500.00</li>
<li>Had sumber pembiayaan 3 = 750.00</li>
</ul></td>
</tr>
<tr class="even">
<td>Transaksi 1</td>
<td><strong>Amaun transaksi:</strong> Pembiayaan<strong>100.00:</strong> Transaksi dibayar mengikut peraturan 1 sahaja, kerana transaksi dibayar penuh selepas peraturan 1 dikenakan. Transaksi dibiayai sama rata antara sumber pembiayaan 2 dan sumber pembiayaan 3.
<ul>
<li>Sumber pembiayaan 2: 50.00</li>
<li>Sumber pembiayaan 3: 50.00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Transaksi 2</td>
<td><strong>Amaun transaksi:</strong> Pembiayaan<strong>5,000.00:</strong> Transaksi dibayar mengikut kesemua tiga peraturan. <strong>Peraturan 1</strong>
<ul>
<li>Sumber pembiayaan 2: 450.00</li>
<li>Sumber pembiayaan 3: 450.00</li>
</ul>
<strong>Peraturan 2</strong>
<ul>
<li>Sumber pembiayaan 3: 250.00 (= 750.00 – 50.00 – 450.00)</li>
</ul>
<strong>Peraturan 3</strong>
<ul>
<li>Sumber pembiayaan 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Jumlah dana yang diagihkan untuk setiap sumber pembiayaan</td>
<td><ul>
<li>Sumber pembiayaan 1: 3,850.00</li>
<li>Sumber pembiayaan 2: 500.00</li>
<li>Sumber pembiayaan 3: 750.00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Peraturan pengebilan
Apabila anda berunding tentang kontrak projek dengan pelanggan, anda mentakrifkan cara dan masa anda boleh menginvois pelanggan untuk kerja bagi satu projek. Selepas anda menyediakan kontrak projek dan projek, anda boleh menyediakan peraturan pengebilan untuk projek tersebut. Peraturan pengebilan adalah berdasarkan terma projek yang ditentukan dalam kontrak projek. Peraturan pengebilan yang boleh anda cipta bergantung pada terma kontrak projek dan jenis projek, seperti Masa dan bahan atau Harga Tetap, yang anda kaitkan dengan peraturan pengebilan. Anda boleh mencipta lebih daripada satu peraturan pengebilan untuk kontrak projek. Anda juga boleh menetapkan peraturan pengebilan kepada berbilang projek yang dikaitkan dengan kontrak projek yang sama dan mempunyai terma pengebilan yang serupa. 

Anda boleh menyediakan jenis peraturan pengebilan yang berikut:

-   **Unit penghantaran** – Invois pelanggan apabila anda melengkapkan unit penghantaran. Anda mentakrifkan unit penghantaran dalam kontrak.
-   **Kemajuan** – Invois pelanggan apabila anda melengkapkan peraturan projek yang ditentukan. Anda boleh menyediakan peraturan pengebilan untuk mengira secara automatik peratusan kerja yang dilengkapkan atau anda boleh mengira secara manual peratusan kerja yang dilengkapkan dan amaun untuk menginvois pelanggan.
-   **Pencapaian** – Invois pelanggan untuk amaun penuh pencapaian projek apabila pencapaian dicapai.
-   **Yuran** – Invois pelanggan untuk perkhidmatan anda serta yuran pengurusan, yang pada lazimnya peratusan kos perkhidmatan.
-   **Masa dan bahan** – Invois pelanggan untuk nilai masa dan bahan yang digunakan dalam projek.

Untuk semua jenis peraturan pengebilan, anda boleh menentukan peratusan penahanan yang dipotong daripada invois pelanggan sehingga projek mencapai peringkat yang telah dipersetujui. Peratusan penahanan bayaran ditentukan dalam kontrak projek. Amaun dikira berdasarkan dan ditolak daripada, jumlah nilai barisan dalam invois pelanggan. 

Untuk peraturan pengebilan **Masa dan bahan** dan **Kemajuan**, anda boleh menetapkan kategori boleh dituntut. Kategori boleh dituntut menunjukkan transaksi yang perlu disertakan dalam invois pelanggan. 

Apabila anda bersedia untuk menginvois pelanggan, amaun untuk menginvois bagi projek dikira berdasarkan peraturan pengebilan dan cadangan invois projek dijanakan. 

Bahagian berikut memberikan contoh yang menunjukkan cara menyediakan dan menguruskan peraturan pengebilan untuk projek.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Contoh: Cipta peraturan pengebilan yang berdasarkan bilangan unit yang dihantar

Organisasi anda membuat perjanjian untuk menyediakan sejumlah lima sesi latihan kepada pekerja pelanggan pada kos 10,000 setiap sesi latihan. Anda menginvois pelanggan selepas setiap sesi latihan. 

Apabila anda menyediakan peraturan pengebilan untuk kontrak tersebut, anda menggunakan nilai yang berikut:

-   Unit penghantaran ialah satu sesi latihan.
-   Harga unit ialah 10,000 setiap sesi latihan.
-   Jumlah bilangan unit ialah lima sesi latihan.

Apabila anda telah melengkapkan satu sesi latihan, anda boleh mencipta invois untuk 10,000 bagi unit pertama yang telah dihantar dan menghantar invois kepada pelanggan.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Contoh: Cipta peraturan pengebilan yang berdasarkan peratusan pelengkapan projek yang ditentukan (pengiraan manual)

Organisasi anda, sebuah firma perunding perisian, membuat perjanjian dengan pelanggan untuk membangunkan sebahagian produk yang sedang dibangunkan oleh pelanggan. Organisasi anda bersetuju untuk menghantar kod perisian dalam tempoh enam bulan. Pelanggan bersetuju untuk membayar organisasi anda sejumlah 100,000 untuk kerja tersebut. Anda mencipta peraturan pengebilan untuk menginvois pelanggan berdasarkan peratusan kerja yang dilengkapkan bagi projek tersebut, seperti yang ditentukan dalam kontrak.

-   Pada penghujung bulan pertama, anda bertemu dengan pelanggan untuk menentukan peratusan kerja dilengkapkan. Selepas anda dan pelanggan menyemak semula projek, anda membuat keputusan bahawa projek tersebut 15 peratusan dilengkapkan.
-   Anda mencipta invois untuk 15,000 (15 peratus daripada 100,000) dan menghantarnya kepada pelanggan.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Contoh: Cipta peraturan pengebilan yang berdasarkan peratusan pelengkapan projek yang ditentukan (pengiraan automatik)

Organisasi anda, sebuah firma pembangunan perisian, bersetuju untuk membangunkan pakej perakaunan gaji untuk pelanggan pada harga 30,000. Pelanggan bersetuju untuk membayar organisasi anda berdasarkan peratusan kerja dilengkapkan. Anda menganggarkan bahawa kos projek ialah 20,000. Kontrak projek menentukan kategori kerja yang anda gunakan dalam proses pengebilan. Anda menyediakan peraturan pengebilan yang mengira secara automatik amaun invois untuk peratusan kerja yang dilengkapkan untuk setiap kategori. Anda menyediakan belanjawan untuk setiap kategori:

-   **Pembangunan** – Kos 15,000 dan hasil 20,000
-   **Pemasangan** – Kos 5,000 dan hasil 10,000

Apabila anda mencipta invois pelanggan buat pertama kali, amaun invois tersebut dikira secara automatik berdasarkan maklumat yang berikut:

-   Selepas sebulan, pekerja bagi projek tersebut menyerahkan lembaran masa untuk projek tersebut. Kos jam pekerja ialah 5,000 untuk pembangunan dan 1,000 untuk pemasangan. Kerja pembangunan adalah 33 peratus dilengkapkan (5,000 kos sebenar/15,000 kos belanjawan) dan kerja pemasangan adalah 20 peratus dilengkapkan (1,000 kos sebenar/5,000 kos belanjawan).
-   Amaun invois 8,667 dikira secara automatik (33 peratus daripada 20,000 + 20 peratus daripada 10,000).
-   Anda mencipta invois untuk 8,667 dan menghantarnya kepada pelanggan.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Contoh: Cipta peraturan pengebilan yang berdasarkan pencapaian yang telah dipersetujui

Organisasi anda, sebuah firma perunding pengurusan, bersetuju untuk melakukan penyelidikan pasaran untuk produk pelanggan yang dirancang oleh pelanggan untuk dijual. Pelanggan bersetuju untuk menggunakan perkhidmatan anda untuk tempoh tiga bulan, bermula pada bulan Mac dan bersetuju untuk membayar organisasi anda sebanyak 50,000. Projek ini mempunyai tiga pencapaian:

-   Pencapaian 1: Kumpul data pelanggan – 31 Mac
-   Pencapaian 2: Analisis data pelanggan – 30 April
-   Pencapaian 3: Bentangkan cadangan kebolehjayaan produk – 31 Mei

Pelanggan bersetuju untuk membayar organisasi anda sebanyak 10,000 untuk pencapaian pertama, 20,000 untuk pencapaian kedua dan 20,000 untuk pencapaian ketiga. 

Apabila anda menyediakan kontrak projek, anda bersetuju untuk mengebil pelanggan berdasarkan pencapaian yang telah dilengkapkan. Persediaan peraturan pengebilan termasuk langkah yang berikut:

-   Takrifkan pencapaian projek.
-   Takrifkan amaun untuk menginvois pelanggan apabila setiap pencapaian dilengkapkan.

Apabila pencapaian pertama dilengkapkan pada 31 Mac, anda menandakan pencapaian tersebut sebagai dilengkapkan dan kemudian mencipta invois untuk 10,000 dan menghantarnya kepada pelanggan. Anda tidak boleh mencipta invois untuk satu pencapaian sehingga anda telah menandakan pencapaian tersebut sebagai dilengkapkan.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Contoh: Cipta peraturan pengebilan yang berdasarkan perkhidmatan serta yuran pengurusan

Organisasi anda, sebuah firma perunding pengurusan, bersetuju untuk melakukan penyelidikan pasaran bagi menilai kebolehjayaan produk yang sedang dibangunkan oleh pelanggan, sebuah syarikat runcit. Terma perjanjian menentukan bahawa anda akan menyediakan perkhidmatan bagi tiga perunding pengurusan terbaik anda yang akan melakukan penyelidikan mengikut masa dan bahan. Pelanggan bersetuju untuk membayar sebanyak 100 setiap jam, serta 10 peratus yuran pengurusan untuk waktu perundingan yang dikenakan kepada projek tersebut. 

Apabila anda menyediakan kontrak projek, cipta peraturan pengebilan untuk menambahkan 10 peratus yuran pengurusan untuk waktu perundingan yang dikenakan kepada projek tersebut. 

Apabila anda mencipta invois untuk pelanggan, pelanggan dibilkan 10 peratus yuran pengurusan serta kos jam rundingan. Contohnya, jika tiga perunding telah bekerja sejumlah 200 jam dalam projek, invois untuk 22,000 dicipta berdasarkan pengiraan yang berikut:

-   200 jam dengan bayaran 100 setiap jam = 20,000
-   10 peratus yuran pengurusan = 2,000
-   Jumlah amaun invois = 22,000

Jika yuran boleh dikenakan cukai kepada pelanggan dan anda memilih kumpulan cukai jualan dalam kontrak projek, kumpulan cukai jualan dimasukkan secara automatik dalam peraturan pengebilan untuk yuran.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Contoh: Cipta peraturan pengebilan untuk nilai bagi masa dan bahan

Organisasi anda, sebuah firma perunding perisian, bersetuju untuk menyediakan lima perunding teknikal bagi mengusahakan projek pembangunan perisian untuk pelanggan selama enam bulan berikutnya. Pelanggan bersetuju untuk membayar 150 untuk setiap jam rundingan serta kos bekalan pejabat. Organisasi anda menghantar invois kepada pelanggan pada hujung setiap bulan. 

Apabila anda menyediakan kontrak projek, anda bersetuju untuk mengebil pelanggan setiap bulan untuk masa dan bahan bagi projek tersebut. Anda mencipta peraturan pengebilan yang mengandungi maklumat yang berikut:

-   Tempoh kontrak ialah enam bulan.
-   Masa rundingan dikira pada kadar 150 setiap jam.
-   Bekalan pejabat diinvoiskan pada kos dan jumlah kos untuk projek tidak boleh melebihi 10,000.
-   Anda mencipta invois pelanggan pada hujung setiap bulan kalendar sepanjang projek tersebut.

Sepanjang bulan pertama, sejumlah 800 jam direkodkan oleh perunding bagi projek tersebut. Kos bekalan pejabat. yang dicaj kepada projek ialah 2,000. Oleh itu, pada hujung bulan, anda mencipta invois untuk 122,000, yang dikira sebagai 800 jam pada harga 150 setiap jam, serta 2,000 untuk bekalan pejabat.



