---
title: Gambaran keseluruhan struktur pecahan kerja
description: Struktur pecahan kerja (WBS) ialah penerangan tentang kerja yang akan dilakukan untuk projek. Ia ialah hierarki tugas yang mewakili pemahaman pasukan projek tentang komposisi kerja dan saiz, kos serta tempoh setiap komponen atau tugas.
author: Yowelle
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23861
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9dc4575f5b4b80e257e34e21980b0516e7c546e6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287969"
---
# <a name="work-breakdown-structures-overview"></a>Gambaran keseluruhan struktur pecahan kerja

[!include [banner](../includes/banner.md)]

Struktur pecahan kerja (WBS) ialah penerangan tentang kerja yang akan dilakukan untuk projek. Ia ialah hierarki tugas yang mewakili pemahaman pasukan projek tentang komposisi kerja dan saiz, kos serta tempoh setiap komponen atau tugas. WBS mempunyai tiga tujuan utama:

-   Terangkan pecahan atau komposisi kerja dalam tugas.
-   Menjadualkan kerja projek.
-   Anggarkan kos setiap tugas.

Tahap perincian dalam WBS bergantung pada tahap ketepatan yang diperlukan dalam anggaran dan tahap penjejakan yang diperlukan terhadap anggaran tersebut. Projek yang mempunyai had terima yang sangat rendah untuk slippages dalam jadual atau kos biasanya memerlukan WBS yang lebih terperinci, dan penjejakan kemajuan kerja dan kos terhadap WBS dengan tekun. Projek jenis ini biasa dalam industri pembinaan dan kejuruteraan. 

Sebaliknya, projek dalam industri seperti media dan pengiklanan, perisian dan infrastruktur IT biasanya menjadi salah satu jenis, dan produktiviti berkaitan dengan pengalaman dan kompetensi individu yang menjalankan tugas. Oleh itu, industri ini menggunakan WBS untuk mendapatkan anggaran saiz projek, bukan untuk menjejaki kemajuan projek tersebut secara terperinci. 

Membina WBS adalah proses intensif yang biasanya dilakukan dalam tempoh yang panjang, dan ia memerlukan kerjasama dan maklumat daripada pelbagai orang. Topik ini menerangkan bagaimana anda boleh menggunakan penambahbaikan WBS untuk memenuhi keperluan anda untuk anggaran dan penjejakan.

## <a name="prerequisites-for-creating-a-wbs"></a>Prasyarat untuk penciptaan WBS
Untuk mencipta WBS, anda mesti dapat mencipta jadual kerja dan anggaran kos kerja.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Prasyarat untuk mencipta jadual kerja

Untuk menggunakan penjadualan perkhidmatan penuh ciri WBS, lengkapkan persediaan berikut:

1.  Sediakan kalendar lalai dan kalendar projek:
    1.  Klik **Pengurusan projek dan perakaunan** &gt; **Persediaan** &gt; **Pengurusan projek dan parameter perakaunan** &gt; **Penjadualan**. Dalam **Medan kalendar kerja lalai**, tentukan kalendar lalai. Ini akan menjadi kalendar kerja lalai untuk apa-apa projek baru yang dicipta.
    2.  Anda boleh menukar kalendar lalai untuk projek tertentu. Klik halaman butiran projek, dan kemudian, pada **pasukan projek dan penjadualan** FastTab, kemas kini **Medan kalendar penjadualan** dengan memilih kalendar lain.

2.  Sediakan hari kerja dan waktu kerja standard. Kalendar yang anda tetapkan sebagai kalendar kerja untuk projek anda akan digunakan dalam WBS untuk menentukan maklumat berikut:

-   Hari bekerja dan cuti
-   Bilangan jam kerja dalam sehari

Untuk menyediakan hari kerja dan waktu kerja untuk kalendar, atau untuk mencipta kalendar baharu, klik **Pentadbiran organisasi** &gt; **Umum** &gt; **Kalendar**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Prasyarat untuk menganggarkan kos kerja

Untuk menggunakan keupayaan anggaran kos penuh WBS, anda perlu menetapkan kos dan harga jualan untuk pekerja, kategori pekerja, perbelanjaan dan yuran, dan item.

-   Untuk menetapkan kos dan harga jualan pekerja, perbelanjaan dan kategori bayaran, klik **Pengurusan projek dan perakaunan** &gt; **Persediaan** &gt; **Harga**.
-   Untuk menetapkan kos dan harga jualan item, gunakan halaman **Perjanjian perdagangan** untuk setiap item pada halaman senarai **Produk keluaran** dalam pengurusan maklumat Produk.

## <a name="creating-a-wbs"></a>Mencipta WBS
Mencipta WBS melibatkan tiga aktiviti:

1.  **Penguraian kerja** – Cipta pecahan kerja ke dalam potongan atau tugas boleh diuruskan.
2.  **Jadual kerja** – Anggarkan masa yang diperlukan untuk melengkapkan tugas, menetapkan saling kebergantungan tugas dan pilih tarikh mula dan tamat untuk tugas.
3.  **Anggaran kos** – Anggarkan kos untuk setiap tugas.

Bahagian berikut membincangkan cara keupayaan WBS boleh membantu setiap aktiviti tersebut.

### <a name="work-decomposition"></a>Penguraian kerja

Mencipta pecahan atau penguraian kerja biasanya merupakan langkah pertama dalam proses mencipta WBS. Fungsi WBS menyokong membina asas yang berikut untuk pecahan dan penguraian kerja. 

**Tugas akar projek** Tugas akar projek ialah tugas ringkasan peringkat atas untuk projek. Semua tugas projek lain dicipta di bawahnya. Nama tugas akar selalunya ditetapkan pada nama projek. Usaha, tarikh, dan tempoh nod akar merumuskan nilai untuk tugas di bawah tugas akar. Anda tidak boleh mengubahsuai sifat nod akar atau memadamnya.

**Tugas ringkas atau bekas** Tugas ringkasan adalah tugas yang mempunyai sub tugas atau tugas konstituen di bawahnya. Tugas ringkas tidak mempunyai sebarang usaha kerja atau kosnya sendiri. Sebaliknya, usaha kerja dan kos tugas ringkas ialah jumlah usaha kerja dan kos tugas konstituen. Tarikh mula paling awal tugas konstituen digunakan sebagai tarikh mula tugas ringkas, dan tarikh tamat terkini tugas konstituen digunakan sebagai tarikh tamat. Anda boleh mengubah nama tugas ringkas, tetapi anda tidak boleh mengubah suai sifat penjadualan untuk usaha, tarikh dan tempoh. Jika anda memadamkan tugas ringkas, anda juga akan memadamkan semua tugas konstituen. 

**Tugas nod daun** Tugas nod daun mewakili pakej kerja yang paling terperinci pada projek. Nod daun mengandungi usaha anggaran, bilangan sumber yang dirancang, tarikh mula dan tarikh tamat, dan tempoh yang dirancang. 

Anda boleh melengkapkan operasi hierarki berikut untuk mendayakan penciptaan hierarki atau penguraian kerja untuk projek. 

**Tugas baru** Sebarang tugas baru yang anda cipta akan ditambah secara automatik di bawah nod akar dan nombor WBS ditugaskan secara automatik ke tugas tersebut. Bilangan WBS mewakili tahap tugas dalam hierarki. Untuk tugas dalam peringkat pertama di bawah tugas akar projek, skema penomboran 1, 2, 3 dan seterusnya digunakan. Untuk tugas yang di bawah peringkat pertama, skema penomboran 1.1, 1.2, 1.3 dan seterusnya digunakan. Untuk setiap peringkat yang ditambah di bawah peringkat sebelumnya, siri nombor bertitik baharu ditambah. 

Buat masa ini, anda tidak boleh menyesuaikan penomboran WBS. 

**Engsot masuk tugas** apabila anda mengengsot masuk tugas, ia menjadi anak kepada tugas yang mendahuluinya. Bilangan WBS bagi tugas anak baharu telah dikira secara automatik berdasarkan bilangan WBS induk baharunya. Tugas induk kini ialah ringkasan atau tugas bekas dan oleh itu menjadi gulung tugas konstituen tersebut. 

> [!NOTE] 
> Apabila anda mengengsot masuk tugas di bawah tugas yang merupakan nod daun sebelum mengengsot masuk operasi, tugas ringkas yang baru diwujudkan kehilangan tarikh, usaha dan bilangan sumber. Ia kini menggunakan ringkasan nilai tugas konstituen baharunya. 

**Engsot keluar tugas** Apabila anda engsot keluar tugas, ia tidak lagi tugas konstituen induknya. Nombor WBS tugas ini secara automatik mengira semula untuk menunjukkan tahap baharu tugas dalam hierarki. Usaha, kos dan tarikh tugas induk sebelumnya dikira semula untuk mengecualikan tugas tersebut. 

**Gerak ke atas dan Gerak ke bawah** Apabila anda klik **Gerak ke atas** dan **Gerak ke bawah**, anda mengubah kedudukan tugas dalam hierarki induk. Kedudukan tugas tidak menjejaskan usaha, kos, tarikh atau tempoh tugas. Walau bagaimanapun, nombor WBS tugas dikira semula secara automatik untuk menggambarkan kedudukan baharu tugas.

### <a name="schedule-estimation"></a>Anggaran jadual

Anggaran jadual biasanya langkah kedua dalam mencipta WBS. Sebagai amalan terbaik, anda harus melengkapkan anggaran jadual selepas anda mencipta tugas. Halaman **Struktur pecahan kerja** dalam Finance mempunyai dua bahagian. Anak tetingkap atas ditujukan untuk anggaran jadual dan anak tetingkap yang lebih rendah merangkumi **Kos dan hasil anggaran** tab yang anda boleh gunakan untuk anggaran kos. 
**Kebergantungan tugas** Dalam WBS, anda boleh mencipta perhubungan terdahulu antara tugas. Apabila anda tugaskan tugas pendahulu pada satu tugas, tugasan tersebut boleh bermula hanya selepas semua tugas pendahulu telah selesai. Tarikh mula yang dirancang untuk tugas ditetapkan secara automatik ke tarikh paling terkini semua terdahulu. 

**Penjadualan tugas** Faktor berikut menentukan penjadualan tugas nod daun:

-   Pendahulu
-   Usaha
-   Bilangan sumber
-   Tarikh mula dan tamat

Tarikh mula tugas nod daun yang tidak mempunyai pendahuluan yang ditetapkan secara automatik kepada tarikh mula penjadualan projek. Tempoh tugas nod daun sentiasa dikira sebagai bilangan hari bekerja antara tarikh mula dan tamatnya. 

*<strong><em>Peraturan penjadualan</em></strong>* Apabila bantuan penjadualan automatik dihidupkan, peraturan berikut diguna pakai pada penjadualan tugas untuk tugas nod daun:

-   Tarikh mula dan tamat tugas mesti hari bekerja, mengikut kalendar penjadualan projek.
-   Tarikh mula tugas yang mempunyai pendahuluan ditetapkan secara automatik kepada tarikh tamat terkini pendahuluannya.
-   Usaha untuk tugas dikira secara automatik seperti berikut:

Bilangan orang × Tempoh × Bilangan jam dalam hari kerja standard dalam kalendar projek. 

Dalam sesetengah kes, anda mungkin mahu menyimpang daripada peraturan ini. Anda boleh mematikan penjadualan automatik untuk mengelakkan Finance daripada menetapkan atau membetulkan sebarang sifat tugas nod daun secara automatik. Apabila anda memasukkan maklumat untuk tugas yang menyebabkan pelanggaran sebarang peraturan penjadualan, ikon ralat penjadualan ditunjukkan untuk tugas tersebut. Jika anda tidak mahu ralat penjadualan dipaparkan, klik **Ralat penjadualan ditunjukkan** untuk mematikan ciri. 

> [!NOTE] 
> Nilai untuk tugas ringkasan atau bekas terus dikira sebagai jumlah nilai tugas konstituen, tanpa mengira sama ada bantuan penjadualan automatik dihidupkan atau dimatikan. 

**Membetulkan ralat penjadualan** Apabila bantuan penjadualan automatik dihidupkan, ralat penjadualan tidak mungkin berlaku. Walau bagaimanapun, jika anda mematikan bantuan penjadualan automatik dan kemudian menghidupkan kembali, ikon ralat penjadualan mungkin muncul dalam WBS. 

**Membetulkan ralat penjadualan dengan tugas** Apabila anda klik dua kali ikon ralat jadual untuk tugas khusus, kotak dialog memaparkan semua ralat penjadualan untuk tugas tersebut. Anda boleh memutuskan jenis ralat penjadualan untuk membetulkan tugas tersebut. 

**Membetulkan semua ralat penjadualan** Jika anda mahu Finance membetulkan semua ralat penjadualan dalam WBS, pada Tetingkap Tindakan, klik **Betulkan semua percanggahan penjadualan**. 

> [!NOTE] 
> Ciri ini boleh menyebabkan pengubahsuaian ketara pada WBS. Ralat dibetulkan dalam tertib yang berikut:

1.  Anggaran usaha tentang semua tugas telah diubah suai supaya ia sama dengan kapasiti yang telah ditetapkan dalam kalendar projek.
2.  Tarikh mula setiap tugas diubah suai supaya tugas bermula selepas semua tugas terdahulu selesai.
3.  Tarikh mula setiap tugas diubah suai untuk mengeluarkan jurang dalam tarikh mula tugas terdahulu.

### <a name="cost-estimation"></a>Anggaran kos

Seperti yang dinyatakan sebelum ini dalam dokumen ini, anda memasukkan anggaran kos untuk setiap tugas nod daun dengan menggunakan **Anggaran kos dan hasil** tab dalam anak tetingkap bawah **Halaman struktur pecahan kerja** . 

> [!NOTE] 
> Anda tidak boleh mengubah suai anggaran kos untuk tugas ringkas atau bekas. Anggaran kos untuk tugas ringkas adalah sama dengan jumlah anggaran kos tugas nod daun. Anggaran jumlah kos untuk setiap tugas dikira sebagai jumlah anggaran jumlah kos untuk jenis transaksi berikut:

-   Buruh
-   Item atau bahan
-   Perbelanjaan

Jenis transaksi **Yuran** digunakan untuk menganggarkan pendapatan berasaskan yuran. Jenis transaksi ini tidak mempunyai komponen kos dan oleh itu tidak dipertimbangkan apabila kos dianggarkan. 

Jenis transaksi **Pada akaun** digunakan untuk merekodkan nilai jualan berkontrak dalam jenis projek nilai tetap. Jenis transaksi ini juga tidak dipertimbangkan apabila kos dianggarkan. 

Apabila anda menganggarkan kos untuk buruh, bahan dan perbelanjaan untuk setiap tugas, anda mesti tugaskan kategori projek ke kos anggaran. 

**Menganggarkan kos buruh** Untuk setiap tugas nod daun, anda tugaskan usaha kerja dalam jam dan kategori lalai. Oleh itu, apabila anda menyediakan jadual untuk tugas, anggaran kos buruh untuk tugas tersebut secara automatik ditambah dalam kategori lalai untuk buruh. Anggaran kos ini dipaparkan pada **Kos dan hasil anggaran** tab dalam **grid butiran baris** untuk tugas tersebut. Jika anda memerlukan lebih banyak anggaran kos buruh, anda boleh menambahnya pada tab ini. Jika anda menambah atau mengurangkan jam pada anggaran kos buruh, jadual untuk tugas itu dikira semula secara automatik. 

**Menganggarkan perbelanjaan dan kos bahan**  **Anggaran kos dan hasil** tab juga membolehkan anda menganggarkan perbelanjaan dan kos bahan untuk tugas, jika anda memerlukan anggaran. 

Harga kos dan jualan untuk setiap buruh atau baris anggaran perbelanjaan adalah berdasarkan persediaan yang ditetapkan untuk setiap kategori dalam jadual penetapan harga di dalam **Pengurusan projek dan perakaunan** &gt; **Persediaan** &gt; **Penetapan harga**. Untuk item, kos dan harga jualan ditambah secara lalai dari item atau perjanjian perdagangan pada **Produk keluaran** halaman senarai dalam pengurusan maklumat Produk.

## <a name="tracking-progress-on-the-wbs"></a>Perkembangan penjejakan pada WBS
Sesetengah industri jejak kemajuan projek terhadap WBS pada peringkat butiran, manakala yang lain jejak kemajuan pada peringkat yang lebih tinggi dalam WBS. Bahagian ini menerangkan cara anda boleh menggunakan penjejakan WBS untuk keperluan projek anda. 

Finance mempunyai tiga pandangan untuk projek WBS: pandangan Perancangan, pandangan penjejakan Usaha, dan pandangan penjejakan Kos.

### <a name="planning-view"></a>Pandangan perancangan

Pandangan perancangan memaparkan anggaran yang dirancang atau asas bagi maklumat jadual dan kos. Walaupun tiada ciri untuk versi dan asas penjejakan untuk projek WBS, nilai dalam pandangan ini ditujukan untuk mewakili versi asas. Bahagian anggaran Jadual dan anggaran kos untuk topik ini menerangkan pandangan ini dan cara ia digunakan untuk mencipta WBS.

### <a name="effort-tracking-view"></a>Pandangan penjejakan usaha

Pandangan penjejakan Usaha memaparkan penjejakan kemajuan untuk tugas dalam WBS. Ia membandingkan jam usaha sebenar yang terkumpul untuk tugas ke jam usaha yang dirancang. Formula berikut memberikan nilai dalam pandangan penjejakan Usaha:

-   Peratusan kemajuan = Usaha sebenar sehingga kini ÷ Usaha yang dirancang untuk tugas tersebut
-   Usaha selebihnya (juga dikenali sebagai Anggaran-untuk-lengkap \[ETC\]) = Usaha yang dirancang – Usaha sebenar sehingga kini
-   Anggaran ketika selesai (EAC) = Usaha selebihnya + Usaha sebenar sehingga kini
-   Varians usaha yang diunjurkan = Usaha yang dirancang - EAC

Pandangan penjejakan Usaha memaparkan unjuran varians usaha untuk tugas, berdasarkan sama ada EAC lebih atau kurang daripada usaha yang dirancang:

-   Jika EAC adalah lebih daripada usaha yang dirancang, tugas itu diunjurkan mengambil lebih banyak masa daripada yang dirancang pada asalnya dan lebih lewat daripada jadual.
-   Jika EAC kurang daripada usaha yang dirancang, tugas itu diunjurkan mengambil kurang masa daripada yang dirancang pada asalnya dan lebih awal daripada yang dijadualkan.

**Pengurus projek unjuran semula usaha** Sekali-sekala, pengurus projek atau persona lain yang menjejaki kemajuan projek perlu meminda anggaran asal dalam tugas. Tugas itu mungkin bergerak lebih cepat atau lebih perlahan daripada yang dijangkakan pada asalnya kerana pelbagai sebab. Sebagai contoh, skop telah dikurangkan, atau pekerja kurang berpengalaman daripada yang dirancang pada asalnya. Unjuran ialah persepsi pengurus projek mengenai anggaran, berdasarkan status semasa projek. Secara umumnya, anda tidak seharusnya mengubah nombor garis dasar, kerana garis dasar projek mewakili dokumen telaga diterbitkan untuk jadual projek dan anggaran kos yang dipersetujui oleh semua pemegang amanah dalam projek tersebut. 

Terdapat dua cara pengurus projek boleh ubah suai usaha pada tugas:

-   Ubah suai usaha selebihnya yang ditetapkan secara automatik untuk mengemas kini usaha selebihnya yang sebenar pada tugas.
-   Ubah suai peratusan kemajuan yang ditetapkan secara automatik untuk mengemas kini kemajuan sebenar pada tugas.

Kedua-dua pendekatan ini menyebabkan pengiraan semula tugas ETC, EAC dan peratusan kemajuan, serta varians usaha yang diunjurkan pada tugas. EAC, ETC dan peratusan kemajuan pada tugas ringkasan juga dikira semula, dan varians usaha dijangka dikemas kini. 

**Usaha diubah suai pada tugas ringkasan** Anda boleh mengubah suai usaha dalam tugas ringkas atau bekas. Tanpa mengira sama ada anda mengubah suai nilai ini dengan menggunakan usaha selebihnya atau peratusan kemajuan dalam tugas ringkasan, pengiraan berlaku secara automatik dalam pesanan yang berikut:

1.  EAC, ETC dan peratusan kemajuan pada tugas dikira.
2.  EAC baharu diagihkan kepada tugas anak dalam perkadaran yang sama dengan jumlah EAC asal.
3.  EAC baharu pada setiap tugas nod daun dikira.
4.  Usaha selebihnya dan peratusan kemajuan dikira semula untuk semua tugas anak yang terjejas, berdasarkan nilai EAC baharu. Varians usaha kerja juga telah dikira semula.
5.  EAC tugas ringkasan juga telah dikira semula daripada nod daun.

Klik **Kembangkan ke peringkat** dalam pandangan penjejakan Usaha untuk menetapkan peringkat untuk menjejaki dan mengekalkan WBS anda. WBS secara automatik dikembangkan ke peringkat itu dalam pandangan penjejakan Usaha pada bila-bila masa anda membukanya.

### <a name="cost-tracking-view"></a>Pandangan penjejakan kos

Pandangan penjejakan Kos memaparkan penjejakan penggunaan kos untuk tugas. Dalam pandangan ini, kos sebenar yang telah dibelanjakan berbanding tugas sehingga kini dibandingkan dengan kos yang dirancang untuk tugas tersebut. Formula berikut memberikan nilai dalam pandangan penjejakan Kos:

-   Peratusan kos yang digunakan = Kos sebenar sehingga kini ÷ Kos yang dirancang untuk tugas tersebut
-   Kos untuk selesai (CTC) = Kos yang dirancang – Kos sebenar sehingga kini
-   Anggaran selesai (EAC) = CTC + kos sebenar sehingga kini
-   Varians kos unjuran = Kos dirancang – EAC

Pandangan penjejakan Kos memaparkan unjuran varians kos untuk tugas, berdasarkan sama ada EAC lebih atau kurang daripada kos yang dirancang:

-   Jika EAC lebih daripada kos yang dirancang, tugas itu diunjurkan untuk menggunakan lebih banyak wang daripada asalnya dan melebihi belanjawan.
-   Jika EAC kurang daripada kos yang dirancang, tugas itu diunjurkan untuk menggunakan lebih kurang wang daripada asalnya dan di bawah belanjawan.

**Pengurus Projek unjuran semula kos** Pengurus projek mesti menggunakan CTC untuk meminda anggaran kos asal pada tugas. Pengurus Projek boleh boleh mengubah suai nilai CTC kepada kos yang diperlukan untuk melengkapkan tugas. Jika anda mengubah suai nilai CTC, tugas CTC, EAC dan peratusan kos yang digunakan dan varians kos dijangka pada tugas, telah dikira semula. EAC, ETC dan peratusan kos digunakan pada tugas ringkasan juga dikira semula, dan varians usaha dijangka dikemas kini. 

> [!NOTE] 
> Apabila anda meminda usaha untuk tugas WBS dalam pandangan penjejakan Usaha, tugas CTC, EAC, peratusan kos yang digunakan dan varians kos dijangka semua dikira semula dalam pandangan penjejakan Kos. Walau bagaimanapun, semakan kos tidak menjejaskan nilai dalam pandangan penjejakan Usaha, kerana kos mengikut jenis transaksi (buruh, bahan atau perbelanjaan) atau kategori projek tidak dipinda. 

**Semakan unjuran untuk kos tugas ringkasan** Anda boleh menyemak kos pada tugas ringkasan dan pengiraan berlaku secara automatik dalam susunan berikut:

1.  EAC, CTC dan peratusan kos yang digunakan pada tugas akan dikira semula.
2.  EAC baharu diagihkan kepada tugas anak dalam perkadaran yang sama dengan EAC asal pada tugas tersebut.
3.  EAC baharu untuk setiap tugas dikira.
4.  CTS dan peratusan kos yang digunakan dikira semula untuk tugas kanak yang terjejas, berdasarkan nilai EAC. Varians kos kerja juga telah dikira semula.
5.  EAC untuk semua tugas ringkas telah dikira semula berdasarkan perubahan ini.

Klik **Kembangkan ke peringkat** dalam pandangan penjejakan kos untuk menetapkan tahap untuk menjejaki dan mengekalkan WBS anda. WBS secara automatik dikembangkan ke peringkat itu dalam pandangan penjejakan kos apabila anda membukanya.

### <a name="earned-value-management"></a>Pengurusan nilai terperoleh

Anda boleh menggunakan kaedah nilai terperoleh (EVM) untuk menjejaki kemajuan projek. Anda boleh pandangan metrik nilai terperoleh pada Pusat Peranan pengurus projek. Komponen carta nilai terperoleh menunjukkan nilai berfasa masa nilai yang dirancang dan kos sebenar. Nilai terperoleh pada tarikh semasa ditunjukkan sebagai titik. Data berfasa masa untuk nilai terperoleh tidak tersedia buat masa ini. 

Fasa masa pada carta nilai terperoleh dipaparkan mengikut minggu atau mengikut bulan. Bahagian ini menerangkan tiga tonggak daripada EVM: nilai yang dirancang, nilai terperoleh dan kos sebenar. 

**Nilai terancang** keadaan teori EVM plot nilai terancang mewakili kadar yang mana pasukan projek sebenarnya merancang untuk memperoleh nilai ke atas projek tersebut. 

Finance menggunakan 0:100 peraturan pendapatan apabila ia plot nilai yang dirancang. Di bawah peraturan ini, nilai tugas akan dihantar kepada tugas sebagai tarikh tamat. Tiada nilai disiarkan sehingga tugas itu 100 peratus selesai. 

Dalam pengurusan Projek dan perakaunan, anda memasukkan tarikh akhir nod daun dan kos yang dirancang untuk itu. Apabila graf nilai yang dirancang dipaparkan mengikut minggu, nilai yang dirancang diringkaskan mengikut minggu untuk semua tugas nod daun untuk tempoh projek. 

**Nilai terperoleh** keadaan teori EVM plot nilai terperoleh mewakili kadar yang mana pasukan projek sebenarnya memperoleh nilai ke atas projek tersebut. 

Finance menggunakan 0:100 peraturan pendapatan apabila ia plot nilai terperoleh. Di bawah peraturan ini, nilai tugas akan dihantar kepada tugas sebagai tarikh tamat. Tiada nilai disiarkan sehingga tugas itu 100 peratus selesai. 

Apabila nilai terperoleh dikira, peratusan kemajuan setiap tugas dipertimbangkan. Di bawah peraturan perolehan 0:100, hanya tugas yang selesai dalam tempoh diberikan dianggap sebagai pengiraan nilai terperoleh pada akhir tempoh tersebut. Nilai terperoleh pada projek dikira untuk semua tugas yang telah diselesaikan apabila graf dicipta. 

> [!NOTE] 
> Buat masa ini, sistem untuk penjejakan WBS tidak mempunyai struktur data untuk menyimpan peratusan kemajuan bersejarah pada setiap tugas. Oleh itu, nilai terperoleh boleh dilaporkan hanya pada masa kiub diproses. Proses kiub secara kerap untuk mengemas kini data nilai terperoleh yang ditunjukkan pada Pusat Peranan. 

**Kos sebenar** teori EVM menyatakan bahawa plot kos sebenar mewakili kadar di mana wang yang dibelanjakan untuk projek. 

Transaksi yang disiarkan untuk projek digunakan untuk plot garis kos sebenar. Kos yang diringkaskan mengikut tarikh. Data ini kemudian digunakan untuk graf kos sebenar mengikut minggu atau mengikut bulan pada carta nilai terperoleh.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Cara menggunakan konsep nilai terancang, nilai terperoleh dan kos sebenar

**Varians Jadual** Semasa merancang, anda mencipta ramalan untuk kerja pada garis masa. Oleh itu, nilai yang dirancang ialah kadar di mana perancang projek fikir kerja akan selesai pada projek tersebut. Selepas projek sedang berjalan, kerja selesai dan projek mendapat nilai. Dengan membandingkan nilai terancang kepada nilai terperoleh, anda boleh pandangan cara kerja projek yang sedang berjalan. Hasil perbandingan ini dipanggil varians jadual. 

Jika nilai yang dirancang untuk tempoh lebih daripada nilai terperoleh, jumlah kerja yang telah dilakukan ke atas projek adalah kurang daripada apa yang dirancang. Oleh itu, projek ini adalah lebih lewat daripada jadual. Oleh kerana nilai yang dirancang dan nilai terperoleh dinyatakan dalam terma kewangan, masa lag pada projek juga diberikan nilai kewangan. 

Jika nilai yang dirancang untuk tempoh kurang daripada nilai terperoleh, jumlah kerja yang telah dilakukan ke atas projek adalah lebih daripada apa yang dirancang. Oleh itu, projek ini adalah ahead daripada jadual. Masa bakal pelanggan ini juga diberi nilai kewangan.

**Varians kos** Kerana nilai terperoleh menggunakan harga kos kerana mendarabkan, nilai terperoleh menunjukkan kos kerja yang dilakukan pada projek. Sebagai kemajuan projek, log transaksi menyediakan rekod wang yang sebenarnya dibelanjakan untuk projek tersebut. Dengan membandingkan nilai terperoleh kepada kos sebenar, anda boleh pandangan jumlah wang yang sedang dibelanjakan berbanding dengan nilai terperoleh. Hasil perbandingan ini dipanggil varians kos. 

Jika kos sebenar yang dibelanjakan untuk tempoh lebih daripada nilai terperoleh, lebih banyak wang telah dibelanjakan daripada terperoleh. Oleh itu, projek itu melebihi belanjawan. 

Jika kos sebenar yang dibelanjakan untuk tempoh kurang daripada nilai terperoleh, lebih banyak wang terperoleh daripada dibelanjakan. Oleh itu, projek itu di bawah belanjawan.

## <a name="wbs-templates"></a>Templat WBS
Anda boleh menggunakan kefungsian templat WBS untuk mencipta templat standard untuk projek. Jika projek yang syarikat anda tawarkan melibatkan banyak kerja berulang, anda perlu pertimbangkan mencipta templat WBS. 

Anda boleh mencipta templat WBS daripada projek yang sedia ada, supaya pengetahuan dan amalan terbaik yang anda kumpul semasa perancangan projek tersebut boleh digunakan semula pada projek yang serupa pada masa hadapan. Walau bagaimanapun, kadangkala, ia mungkin tidak masuk akal untuk menyimpan keseluruhan WBS sebagai templat. Oleh itu, anda juga boleh mencipta templat daripada bahagian WBS untuk projek.

### <a name="saving-a-projects-wbs-as-a-template"></a>Menyimpan WBS projek sebagai templat

Selepas anda mencipta templat, anda boleh mengimportnya ke dalam projek baharu WBS di bawah nod akar, atau di bawah sebarang tugas dalam projek WBS.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Mengimport templat WBS ke dalam WBS projek

Apabila anda mengimport tugas, tugas dalam templat disusun berdasarkan tarikh mula tugas yang diimport. Semasa import, perhubungan terdahulu pada tugas templat digunakan untuk mengira tarikh mula untuk tugas yang diimport. Kalendar kerja standard projek destinasi digunakan untuk mengira tarikh akhir tugas yang diimport, supaya hari kerja dan waktu kerja standard yang ditetapkan dalam kalendar kerja projek semasa dikekalkan. 

Jumlah kos dan harga jualan pada baris anggaran digunakan untuk menjamin bahawa harga tertentu untuk projek atau kontrak projek mempunyai tarikh yang sah.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Perbezaan antara projek WBS dan template WBS

-   Tugas dalam templat WBS tidak mempunyai tarikh mula dan tarikh akhir.

Hari kerja dan bukan kerja tidak ditetapkan untuk templat WBS.

-   Templat WBS sentiasa menggunakan kalendar penjadualan yang disediakan sebagai kalendar lalai untuk semua projek.

Kalendar penjadualan lalai digunakan hanya untuk mengetahui jam dalam hari kerja standard.

-   Perhubungan terdahulu tidak disalin kepada templat WBS.

Oleh kerana templat WBS tidak mempunyai tarikh, logik tarikh mula yang berdasarkan tarikh tamat terdahulu tidak diperlukan.

-   Baris anggaran kos buruh dicipta secara automatik apabila tugas dicipta dalam templat WBS. Harga jualan dan jumlah kos akan disalin daripada pekerja yang terpilih.

Perbelanjaan dan kos item boleh dicipta secara manual, hanya pada projek WBS.

-   Ralat penjadualan dipaparkan apabila terdapat penyelewengan daripada formula berikut:

Usaha = Bilangan sumber × Tempoh × Bilangan jam dalam hari kerja standard 

Anda boleh membetulkan semua ralat penjadualan pada masa yang sama dengan mengklik **Betulkan semua ralat penjadualan**. 

Sebagai alternatif, anda boleh membetulkan ralat penjadualan secara individu dengan mengklik ikon amaran untuk setiap tugas.





[!INCLUDE[footer-include](../includes/footer-banner.md)]