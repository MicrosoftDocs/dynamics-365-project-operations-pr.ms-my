---
title: Pemasangan data sampel
description: Topik ini menyediakan maklumat tentang cara memasang data sampel dalam Project Service Automation.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.service: project-operations
ms.reviewer: kfend
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 3c9cca7aa9d85bb38e48820b361ba07923ceddbd
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132434"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Pemasangan data sampel untuk aplikasi Project Service

Untuk membantu anda membina persekitaran demo anda sendiri, Microsoft memberikan sampel pakej data yang boleh dimuat turun yang menunjukkan keupayaan aplikasi anda. Terdapat dua jenis pakej data sampel:
- data rujukan/persediaan
- data demo (data rujukan/persediaan dan transaksi seperti pesanan kerja dan projek)

Pakej data **rujukan** sampel boleh dimuat turun dalam tiga pakej berbeza, jadi anda boleh memasang data hanya untuk Project Service atau hanya untuk Field Service atau anda boleh memasang data sampel untuk kedua-dua aplikasi sekaligus.

Pakej data persediaan/rujukan sampel ialah:

- [**V902PSMasterData** - Project Service versi 3.x sahaja](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** - Field Service versi 8.x sahaja](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** - Field Service 8.x dan Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

Pakej data **demo** terakhir ialah:

 - [**FPSDemoData** - Field Service 8.x dan Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   Arahan pemasangan berbeza sedikit dalam pengguna untuk mencipta dan mengkonfigurasi bahagian tetapi yang lain adalah sama seperti dalam [**siaran blog**](https://aka.ms/fpsdemodatablog) sebelumnya. Pakej ini mempunyai set data demo yang dikurangkan dan mengambil masa kira-kira 3 jam untuk dipasang.

Pakej data sampel ini ini hanya boleh didapati dalam Bahasa Inggeris.

> [!IMPORTANT]
> **Data sampel tidak boleh dinyahpasang dengan apa cara sekali pun.** Anda hendaklah hanya memasang pakej ini pada sistem demonstrasi, penilaian, latihan atau ujian. Juga, sila ambil perhatian bahawa memasang pakej individu dan kemudian memasang dalam pakej lain individu, tidak disokong. (Dengan kata lain, anda tidak boleh memasang **FSMasterData** diikuti dengan **PSMasterData**, atau sebaliknya.) Jika anda merasakan diri anda memerlukan data sampel untuk kedua-dua aplikasi pada bila-bila pada masa hadapan, anda perlu memasang pakej **v902FPSMasterData**.

Apabila anda memasang mana-mana pakej data sampel, proses pemasangan menjalankan tindakan berikut:

- Mencipta atau menetapkan parameter lalai untuk menggunakan Project Service, Field Service, atau kedua-dua aplikasi (jika berkenaan).

- Mengimport sampel data untuk aplikasi, seperti sumber boleh tempah, peranan khusus aplikasi, jualan dan senarai harga kos, unit organisasi, rekod proses jualan dan entiti-entiti lain untuk menunjukkan keupayaan utama.  

Dengan pakej **data demo**, anda mendapat yang di atas dan data transaksi tambahan seperti pesanan kerja dan projek.

Tertanya-tanya apakah keupayaan yang anda boleh tunjukkan dengan data sampel? Lihat senario rekaan Fabrikam Robotics dalam [Nota teknikal](#technical-notes).

Jika anda mempunyai soalan tentang memasang pakej data sampel ini, [hantarkan e-mel kepada kami di fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).

## <a name="requirements"></a>Keperluan

Protokol pemasangan menjangkakan perkara berikut mengenai tika sasaran (organisasi) anda:

- Bahasa asas ialah Bahasa Inggeris dan mata wang asas ialah dolar AS (USD,$).

- Organisasi belum mempunyai data Project Service atau Field Service atau hanya mempunyai data lalai paling asas yang dilengkapi dengan mana-mana organisasi baharu

- Versi aplikasi perniagaan yang betul telah dipasang:
       
    - **Untuk FPSDemoData atau v902FPSMasterData:** Organisasi telah memasang Field Service versi 8.x dan Project Service versi 3.x.

    - **Untuk v902PSMasterData:** Organisasi telah memasang Project Service versi 3.x.

    - **For v902FSMasterData:** Organisasi telah memasang Field Service versi 8.x.

> [!NOTE]
> Jika anda perlu memasang data sampel selain daripada persekitaran percubaan atau demo Project Service dan Field Service sedia ada yang telah mempunyai data (tidak disyorkan), anda perlu menggantung prasemakan keselamatan yang dilakukan oleh pemasang. Untuk mendapatkan maklumat lanjut, lihat nota teknikal di bawah.

## <a name="prepare-for-installation"></a>Sedia untuk memasang

Anda perlu menjalankan pemasang pada komputer dengan versi Windows terkini (Windows 10 diutamakan).

Anda perlu merancang supaya komputer tetap bersambung ke rangkaian dan pemasangannya berjalan sehingga **1 jam** untuk **data persediaan/rujukan**. (Biasanya pemasangan mengambil masa kira-kira 30 minit untuk **FPSMasterData**, yang merangkumi data sampel bagi kedua-dua aplikasi.) Bagi **FPSDemoData**, pemasangan akan mengambil masa kira-kira **3 jam**.

Komputer hendaklah mematikan fungsi penyelamat skrin. Sebaliknya, kelayakan sesi untuk pemasangan mungkin hilang apabila penyelamat skrin terlibat sama (melainkan anda mengekalkan sesi anda kepada aktif sepanjang masa).

> [!div class="mx-imgBorder"]
> ![Tangkap layar tetapan penyelamat skrin, dengan penyelamat skrin dimatikan](media/sample-data-1.png)

## <a name="download-and-unpack"></a>Muat turun dan buka

Pemasangan data sampel Project Service dan Field Service diagihkan sebagai pengekstrakan sendiri boleh laksana. Nama fail mungkin berbeza-beza bergantung pada pakej data sampel, tetapi sebaliknya langkah-langkah adalah sama tidak kira jenis pakej yang anda pasang.

Selepas memuat turun pakej, jalankan fail .exe dan kemudian terima terma dan syarat untuk buka pakej fail zip yang dimampatkan. Kemudian anda perlu mengekstrak kandungan fail tersebut ke folder komputer anda.

Bergantung pada sistem operasi dan tetapan keselamatan, anda mungkin perlu melakukan langkah berikut selepas membuka fail zip:

1. Cari dan klik kanan fail **FPSDemoData.dll** dalam folder **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.

2. Pilih **Nyahsekat**.

3. Pilih **Guna**.

4. Pilih **OK**.


## <a name="create-or-configure-users"></a>Cipta atau konfigurasikan pengguna

Pakej **FPSDemoData** memerlukan enam pengguna sementara pakej **FPSMasterData** memerlukan seorang pengguna. Rujuk kepada pakej yang betul untuk pakej data sampel anda.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Cipta atau konfigurasikan pengguna - pakej data persediaan/rujukan

Pakej **FPSMasterData** direka untuk dipasang dengan seorang pengguna bernama Spencer Low dengan tetapan yang digambarkan di sini. Untuk memasang pakej dengan betul, anda perlu mencipta (atau menamakan semula buat sementara) pengguna dalam persekitaran anda untuk dipadankan dengan konfigurasi data sampel masuk.

Untuk mencipta atau mengkonfigurasi pengguna, pergi ke **Tetapan** > **Keselamatan** > **Pengguna**, dan lakukan perkara berikut:

1. Tetapkan UserFullname="Spencer Low" dengan nama pengguna "spencerl" (**huruf kecil**) kepada peranan Pengurus Projek dan Pengurus Latihan.

2. Pilih pengguna **Spencer Low**, kemudian pilih **Urus Peranan**. Cari dan pilih peranan **Pentadbir Sistem**, dan kemudian pilih **OK** untuk memberi hak pentadbir penuh kepada Spencer Low. Langkah ini perlu untuk memastikan rekod sampel dicipta dengan pemilikan pengguna yang betul dan oleh itu mengisi pandangan dengan betul.

3. Daripada pakej boleh dimuat turun, anda perlu mengemas kini fail pemetaan data dengan alamat e-mel konteks pengguna lalai. Untuk melakukan ini, buka **PkgFolder** dan kemudian cari dan buka fail **ImportUserMapFile.xml** dalam Notepad (atau Visual Studio atau editor XML lain). Tetapkan medan **DefaultUserToMapTo=** kepada alamat e-mel pengguna Spencer Low.

4. Jika anda tidak menggunakan Spencer Low dengan nama pengguna **spencerl**, anda perlu mengemas kini satu fail tambahan. Buka fail **DemoDataPreImportConfig.xml**, dan kemudian cari tag **userstocreateandconfigure**. Kemas kini tag **\<login\>** dengan nama pengguna bagi pengguna Spencer Low. Untuk maklumat tambahan, lihat [Nota teknikal](#technical-notes).

## <a name="create-or-configure-users---demo-data-package"></a>Cipta atau konfigurasikan pengguna - pakej data demo

Pakej data demo memerlukan enam pengguna. Untuk pakej memasang dengan betul, lakukan perkara berikut:

 1. Cipta atau tukar nama pengguna sedia ada buat sementara waktu untuk dipadankan dengan konfigurasi data sampel yang masuk dengan pergi ke **Tetapan** > **Keselamatan** > **Pengguna**.
 
    Peranan ini hanya diperlukan untuk demo berasaskan persona.  
    - Nama penuh Pengguna="David So" sebagai Juruteknik Perkhidmatan Lapangan   
    - Nama penuh Pengguna="Jamie Reding" sebagai Penghantar Khidmat Pelanggan & Perkhidmatan Lapangan   
    - Nama penuh Pengguna="Molly Clark" sebagai Pengurus Akaun   
    - Nama penuh Pengguna="Spencer Low" sebagai Pengurus Amalan dan Projek  
    - Nama penuh Pengguna="Veronica Quek" sebagai Ahli Pasukan   
    - Nama penuh Pengguna="William Contoso"
  
2. Untuk tujuan import data demo, tugaskan enam pengguna di atas peranan Pentadbir supaya rekod sampel diimport dengan betul. 

3. Buka **PkgFolder** dan kemudian cari dan buka **ImportUserMapFile.xml**. Kemas kini medan **Baharu=** kepada alamat e-mel pengguna yang sepadan dalam sistem anda.

   > [!div class="mx-imgBorder"]
   > ![Tangkap skrin UserMapFile](media/sample-data-7.png)

4. Jika pengguna nama penuh "Spencer Low" anda mempunyai ID pengguna yang berbeza daripada **"spencerl"**, maka anda perlu mengemas kini satu fail tambahan. Buka **DemoDataPreImportConfig.xml** dan kemudian cari tag **userstocreateandconfigure**. Kemas kini tag **\<login\>** dengan loginId (sensitif huruf). 

5. Kalendar pengguna pertama (dalam tag **userstocreateandconfigure**) digunakan untuk mengisi waktu bekerja untuk semua sumber yang boleh ditempah pada import data demo. Navigasi ke **Tetapan** > **Keselamatan** > **Pengguna**, cari pengguna "Spencer Low" anda dan buka pilihan "Waktu Bekerja". Edit waktu bekerja sedia ada, pilih pilihan **Seluruh jadual mingguan berulang dari awal hingga akhir**. Pastikan yang **waktu bekerja ditetapkan kepada 8 PG - 5 PTG (9 jam), Isnin hingga Jumaat dan dengan Zon Waktu ditetapkan kepada Waktu Pasifik (AS & Kanada)**. Ini diperlukan untuk memastikan yang papan Projek dan Jadual menunjukkan seperti yang dijangkakan.

**Pengesyoran:** Pertimbangkan mencipta sandaran organisasi anda sekarang, jika anda perlu kembali ke titik permulaan anda jika sesuatu yang tidak kena berlaku semasa pemasangan data sampel. Untuk maklumat lanjut, lihat [Sandarkan dan pulihkan tika](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).

## <a name="run-the-package-deployer"></a>Jalankan Package Deployer

1. Cari dan jalankan **PackageDeployer.exe** dalam folder **v902FPSMasterData** ATAU **PackageDeployer_FPSDemoData**.

2. Terima terma dan syarat.

3. Pada tetingkap seterusnya:

   a. Pilih jenis pelaksanaan **Office 365**.

   b. Gunakan pengguna dan kata laluan pengguna pentadbir sistem yang dikonfigurasikan dalam "Cipta atau konfigurasikan pengguna" ("Spencer Low" dengan nama pengguna "spencerl").

   c. Pastikan **Paparkan senarai organisasi yang tersedia** dipilih.

      > [!div class="mx-imgBorder"]
      > ![Syot skrin bagi tetingkap Package Deployer dengan " Paparkan senarai organisasi tersedia" dipilih](media/sample-data-2.png)

4. Pilih organisasi di mana anda mahu memasang data sampel.

5. Pilih **Seterusnya** sehingga anda melihat dialog **Persediaan Data Demo**.

   > [!div class="mx-imgBorder"]
   > ![Tangkap layar tetingkap status pemasang data demo](media/sample-data-3.png)

6. Sebelum meneruskan, ambil perhatian bahawa memasang data sampel boleh mengambil masa sehingga satu jam (selalunya ~ 10 minit). Anda perlu pastikan komputer kekal hidup dan disambungkan ke rangkaian sepanjang proses pemasangan, dan sesi anda kekal aktif.   

7. Apabila anda bersedia, klik **Seterusnya** untuk memulakan proses pemasangan data sampel. Selepas data sampel dimuatkan, klik **Selesai**.

## <a name="verify-the-sample-data-installation"></a>Sahkan pemasangan data sampel

Untuk semakan kewarasan, sahkan bilangan rekod dan jenis entiti yang disenaraikan dalam senario rekaan Fabrikam Robotic yang muncul seperti yang dijangkakan.

Selepas data sampel dimuatkan sepenuhnya, daftar masuk masuk sebagai pengguna Spencer Low dan sahkan yang berikut:

- Jika aplikasi Project Service dipasang, pergi ke **Project Service** > **Tetapan** > **Senarai Harga**. Sahkan bahawa kadar bil dan kadar kos wujud dengan mata wang yang betul untuk setiap negara/rantau dalam set data.

- Jika aplikasi Project Service dipasang, pergi ke **Universal Resource Scheduling** > **Tetapan** > **Unit Organisasi**. Sahkan bahawa senarai harga kos dengan mata wang yang betul telah dikaitkan dengan setiap unit organisasi (tidak termasuk kemasukan bandar). Jika ada yang hilang, cari dan kaitkan senarai harga kos yang betul.

- Jika aplikasi Field Service dipasang, pergi ke **Project Service** > **Tetapan** > **Senarai Harga**. Sahkan bahawa kadar bil dan kadar kos wujud. Pergi ke **Field Service** > **Tetapan** > **Senarai Harga** dan pastikan bahawa kadar bil dan kadar kos wujud, dengan wang yang betul untuk setiap negara/rantau dalam set data.

  > [!div class="mx-imgBorder"]
  > ![Tangkap layar senarai harga aktif](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Tangkap layar unit organisasi aktif](media/sample-data-5.png)

## <a name="technical-notes"></a>Nota teknikal

Lihat di bawah untuk maklumat teknikal lebih lanjut mengenai pemasangan data ini.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Memasang data sampel selain daripada data sedia ada (tidak disyorkan)

Nota: jika anda perlu memasang data sampel selain daripada percubaan atau persekitaran demo Project Service dan Field Service sedia ada yang sudah mempunyai data, anda perlu menggantung pra-semakan keselamatan yang dilakukan oleh pemasang.

Untuk melakukan ini, pergi ke folder **PkgFolder** untuk mencari dan membuka fail **DemoDataPreImportConfig.xml** dengan Notepad (atau XML editor lain).

Cari nilai berikut, dan kemudian tukar tetapan daripada benar kepada palsu:

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Perubahan ini menyebabkan pemasang memintas beberapa semakan keselamatan yang penting termasuk:

- Mengesahkan bahawa tidak lebih daripada satu rekod **Unit Organisasi** aktif dan kemudian menamakannya semula kepada **Fabrikam AS**.

- Mengesahkan bahawa tidak lebih daripada satu rekod **Templat Kerja** aktif.

- Mengesahkan bahawa tidak lebih daripada satu rekod **Parameter Projek** aktif, dan kemudian menamakan semula kemasukan tersebut kepada **Parameter**.

### <a name="configuration-components"></a>Komponen konfigurasi

Terdapat beberapa komponen konfigurasi lain dalam fail konfigurasi pra-import ini. Untuk pengguna teknikal, sebahagian daripada ini termasuk:

- **\<RequiredSolutions\>** menentukan pemasangan penyelesaian prasyarat dan nombor versi.

- **\<InstallSampleData\>** mengawal data sampel luar kotak untuk aplikasi yang dipasang.

    - palsu - melangkau pemasangan data terbina dalam ini (yang boleh dialih keluar)

    - benar - memasang data terbina dalam serentak dengan pemasangan data sampel FS dan PSA

- **\<PreImportDataCollection\>** menentukan Peta Data fail rata dan Rekod yang berkaitan untuk diimport lebih awal sebelum pemasangan data sampel utama.

- **\<EntitiesToEnableScheduling\>** menentukan entiti yang sepatutnya didayakan untuk Tempahan dalam Microsoft Dynamics Scheduling (juga dikenali sebagai Universal Resource Scheduling).

- **\<UsersToCreateAndConfigure\>** menentukan Sumber Boleh Tempah yang akan dicipta (jika ia belum wujud) sebelum import data sampel dilaksanakan. Ambil perhatian bahawa Sumber Boleh Ditempah data sampel sistem sumber sepadan dengan rekod Sumber Boleh Ditempah sistem sasaran pada FullName dan log masuk bagi setiap sumber. Oleh itu, MUSTAHIL untuk menukar nama dalam fail prakonfigurasi ini melainkan anda terlebih dahulu mengimport data sampel ke dalam sistem sasaran yang menggunakan nama ini, kemudian menamakan semula Sumber Boleh Tempah kepada set nama yang diingini bersama dengan rekod Pengguna Didayakan, dan kemudian mengeksport data sekali lagi untuk diimport ke dalam sistem destinasi akhir anda (mengemas kini kemasukan **ImportUserMapFile.xml** Lama dan Baharu dengan wajar).

- **\<PluginsToDisable\>** menentukan pasang masuk item baris yang sangat berhati-hati yang mesti dinyahdayakan semasa import data sampel dan kemudian didayakan semula selepas itu.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Senario rekaan Fabrikam Robotics

Pakej data rujukan sampel Field Service dan Project Service memasang **penyelesaian Fabrikam Manufacturing Master Data (v3.0.0.0)**, bersama dengan kira-kira 4,000 rekod dan kira-kira 40 entiti yang berbeza. Pakej data sampel berasingan untuk Field Service atau Project Service mengandungi sebahagian daripada data sampel **v902FPSMasterData** untuk aplikasi tersebut. Pakej **Data Demo** memasang **penyelesaian Fabrikam Manufacturing Demo Data (v3.0.0.7)** dengan kira-kira 22,000 rekod merentasi 148 entiti.

Syarikat rekaan, Fabrikam Robotics, adalah pengeluar robot talian pemasangan peranti elektronik dan dikenali dengan kualiti produk, inovasi dan perkhidmatan pelanggan mereka yang kukuh, termasuk perancangan pemasangan, pelaksanaan dan perkhidmatan penyelenggaraan yang berterusan. Fabrikam beribu pejabat di Amerika Syarikat (Fabrikam AS), dan mempunyai operasi perkhidmatan berasaskan projek di Perancis, India, United Kingdom dan Switzerland.

Operasi perkhidmatan lapangan berpusat di Amerika Syarikat, kebanyakannya di bahagian Seattle yang lebih besar. Syarikat tertumpu kepada memanfaatkan ketersambungan Internet Perkara (IoT) untuk memantau prestasi aset pelanggan dan memberikan perkhidmatan di tapak yang proaktif.

Gambaran keseluruhan peringkat tinggi data sampel adalah seperti berikut:

- Elemen data sampel biasa (termasuk kedua-dua aplikasi)

    - 1 pengguna

    - 71 akaun

    - 137 kenalan

    - Pelbagai jenis transaksi dan kategori

    - 50 produk dengan 1 senarai harga produk

    - 14 senarai harga/kos

    - 31 ciri-ciri (kemahiran sumber) dalam 2 model perkadaran dengan 3 peringkat (nilai perkadaran)

- Project Service

    - 8 unit organisasi

    - 6 peringkat penggunaan peranan khusus

    - 2.8k+ spesifikasi harga peranan

- Field Service

    - 4 wilayah

    - 5 jenis pesanan kerja

    - 22 aset pelanggan

    - 9 jenis insiden dengan pelbagai ciri sumber berkaitan (9), perkhidmatan (13) dan tugas perkhidmatan (13)
   
Pakej **Data Demo** memasang kira-kira 179 pesanan kerja, 12 projek dan data transaksi yang berkaitan. 

### <a name="change-the-work-hours-for-sample-resources"></a>Ubah waktu bekerja untuk sumber sampel

Secara lalai, semua sumber yang boleh ditempah mempunyai kalendar waktu bekerja 24 jam.

Jika anda perlu mengubah waktu bekerja untuk sumber boleh tempah sampel, pergi ke **Universal Resource Scheduling** > **Penjadualan** > **Sumber**.

Pilih pengguna (contohnya, Spencer Low) dan ubah waktu bekerja Spencer kepada jam yang anda mahu gunakan pada berbilang pengguna. Pergi ke **Universal Resource Scheduling** > **Tetapan** > **Templat Waktu Bekerja** dan edit rekod **Templat Kerja Lalai**. Dalam medan **Sumber Templat**, pilih pengguna dengan waktu bekerja yang anda mahu gunakan pada sumber lain. Pergi ke **Universal Resource Scheduling** > **Penjadualan** > **Sumber** > **Sumber Boleh Ditempah Sktif**. Pilih sumber yang anda mahu ubah, dan kemudian pilih **Tetapkan Kalendar**. Pada senarai juntai ke bawah **Templat Kerja**, pilih templat **Waktu Bekerja Lalai** atau templat lain dengan sumber templat yang betul. Apabila anda pergi ke papan Jadual, anda akan dapat melihat sumber sekarang telah mengemas kini waktu bekerja.

> [!div class="mx-imgBorder"]
> ![Tangkap layar sumber boleh tempah aktif](media/sample-data-6.png)
