---
title: Urus sumber
description: Topik ini memberikan maklumat tentang cara anda boleh mengurus sumber.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 548595e3951f824e1c79a641d3f336e381fcaaf9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132344"
---
# <a name="manage-resources"></a>Urus sumber

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation memasukkan papan pemuka pengurus sumber yang memberikan gambaran keseluruhan visual bagi permintaan dan penggunaan sumber di seluruh organisasi. Anda boleh menggunaan carta pada papan pemuka ini untuk visualisasikan maklumat berikut:

- **Permintaan sumber** – Carta **Permintaan Sumber Aktif** menunjukkan sumber yang telah diserahkan. Sumber diagregatkan sama ada melalui peranan atau projek.
- **Permintaan sumber belum diserahkan** – Carta **Permintaan Sumber Belum Ditugaskan** menunjukkan semua keperluan sumber yang belum diserahkan. Ia membantu pengurus sumber melihat permintaan yang tidak tegas dan mungkin menyerahkan melalui permintaan sumber.
- **Penggunaan boleh bil untuk minggu lepas** – Carta **Penggunaan mengikut Peranan** menunjukkan peratusan penggunaan boleh bil aktual organisasi oleh peranan dengan penggunaan boleh bil sasaran mengikut peranannya.

    > [!NOTE]
    > Untuk menjadikan carta **Penggunaan mengikut Peranan** tersedia, cipta kerja yang menjalankan aliran kerja UpdateRoleUtilization. Peranan berulang ini berjalan setiap tujuh hari untuk mengira penggunaan boleh bil untuk tujuh hari sebelumnya. Keputusan diagregatkan mengikut peranan.

## <a name="manage-project-team-members"></a>Urus ahli pasukan projek

Pengurus projek boleh menggunakan papan pemuka pengurus sumber untuk mengurus sumber pada projek. Contohnya, mereka boleh menambah ahli pasukan secara terus untuk projek dan menempah ahli pasukan untuk mengisi keperluan sumber yang direkod oleh sumber generik.

### <a name="add-a-team-member-directly-to-a-project"></a>Tambah ahli pasukan secara terus kepada projek

Untuk menambah ahli pasukan secara terus kepada projek, pada halaman **Projek**, pada tab **Pasukan**, pilih **Baharu**. Kotak dialog **Cipta Pantas: Ahli Pasukan Projek** muncul. Dalam kotak dialog ini, anda boleh menjalankan tugas ini:

- **Tempah sumber bernama** – Dalam medan **Sumber Boleh Tempah**, pilih nama sumber. Kemudian pilih sumber, tetapkan tempoh, kemudian pilih kaedah peruntukan. Sumber bernama yang anda pilih ditambah pada projek menggunakan kaedah peruntukan dipilih dan kalendar sumber.
- **Tambah sumber generik** – Biarkan medan **Sumber boleh tempah** kosong, kemudian pilih peranan, tetapkan period, dan pilih kaedah peruntukkan pilihan. Sumber generik ditambah pada pasukan sebagai pemegang ruang untuk memegang corak permintaan yang digunakan untuk menempah sumber bernama pada pasukan. Keperluan dibuat mengikut kalendar projek.
- **Tambah sumber bernama pada pasukan tanpa menggunakan kapasiti sumber** – Dalam medan **Sumber Boleh Tempah**, pilih sumber. Kemudian pilih tempoh, dan pilih **Tiada** sebagai kaedah peruntukan. Sumber ditambah pada pasukan, tetapi kapasiti sumber tidak digunakan melalui tempahan.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Tempah ahli pasukan untuk mengisi keperluan sumber untuk sumber generik

Dalam PSA, anda boleh menempah sumber generik pada pasukan projek, dan boleh menyatakan peranan, kapasiti diperlukan, dan cara kapasiti tersebut diagihkan. Anda boleh menempah sumber bernama untuk menggantikan sumber generik yang mempunyai keperluan sumber. Atirbut ini termasuklah kemahiran yang diperlukan, unit organisasi pilihan, dan sumber pilihan.

Ikuti langkah-langkah ini untuk menyatakan kemahiran yang diperlukan pada sumber generik untuk pembangun.

1. Pada halaman **Projek**, pada tab **Pasukan**, pilih **Baharu** untuk menempah sumber generik.

    ![Sumber generik ditempah pada pasukan](media/Resource-Management-image9.png)

2. Dalam pandangan **Semua Ahli Pasukan**, dalam lajur **Keperluan Sumber**, pilih pautan untuk menambah kemahiran diperlukan untuk sumber generik.

    ![Pautan keperluan](media/Resource-Management-image10.png)

3. Pada halaman **Keperluan Sumber** yang muncul, dalam grid **Kemahiran**, pilih elipsis (**...**) kemudian pilih **Tambah Sifat Keperluan Baharu** untuk menambah kemahiran yang diperlukan untuk pembangun anda.

    ![Tambah perintah Sifat Keperluan Baharu](media/Resource-Management-image11.png)

4. Dalam kotak dialog **Cipta Pantas: Sifat Keperluan** yang muncul, dalam medan **Sifat**, pilih kemahiran diperlukan. Kemudian dalam medan **Nilai Penarafan**, pilih tahap kecekapan untuk kemahiran tersebut. Akhir sekali, dalam medan **Keperluan Sumber**, tetapkan keperluan untuk sumber sumber daripada unit organiasi atau bahkan sumber bernama. Apabila anda telah selesai, pilih **Simpan**.

    ![Cari Cepat: kotak dialog Sifat Keperluan](media/Resource-Management-image12.png)

5. Pada halaman **Keperluan Sumber**, pilih **Tempah** untuk memenuhi keperluan sumber.

    ![Butang tempah pada halaman Keperluan Sumber](media/Resource-Management-image13.png)

    Anda juga boleh memilih sumber generik dalam grid **Semua Ahli Pasukan** dan kemudian pilih **Tempah**.

    ![Butang tempah di atas grid Semua Ahli Pasukan](media/Resource-Management-image14.png)

    > [!NOTE]
    > Dalam contoh ini, terdapat 40 jam diperlukan tetapi tiada jam ditempah aktual, kerana sumber generik tidak mempunyai tempahan. Selain itu, tiada jam ditugaskan, kerana sumber generik ditambah terus kepada pasukan. Ia tidak ditambah menggunakan tugasan tugas.

    Pada halaman **Menjadualkan Pembantu**, anda boleh menapis sumber tersedia melalui keperluan yang dinyatakan dalam keperluan sumber. Sumber diisih mengikut parameter pengisihan yang dinyatakan dalam papan Jadual.

    ![Halaman Menjadualkan Pembantu](media/Resource-Management-image15.png)

    Berikut adalah beberapa penapis yang sering digunakan:

    - **Ciri berserta dengan penarafan** – Tapis mengikut kemahiran, pensijilan, kualiti sumber lain, selain daripada penarafan kecekapan.
    - **Peranan** – Tapis mengikut peranan lalai yang ditugaskan untuk sumber boleh tempah.
    - **Unit organisasi** – Tapis sumber boleh tempah mengikut unit organisasi yang ditugaskan mereka.

6. Jika anda tidak berpuas hati dengan kepurusan carian keperluan awal, anda boleh mengubah kriteria penapis. Kembangkan anak tetingkap **Pandangan Penapis** di sebelah kiri, kemudian pilih **Cari** untuk mencari sumber tambahan.

    ![Anak tetingkap Pandangan Penapis](media/Resource-Management-image16.png)

7. Untuk mengubah cara hasil diisih, pilih **Isih**.

    ![Isih perintah](media/Resource-Management-image17.png)

8. Pilih sumber mengikut permintaan yang dinyatakan dalam keperluan, seperti dinyakan di bahagian atas grid. Anda boleh mengosongkan pilihan sel dalam grid dan membiarkan kapasiti sumber terbuka. Hanya satu sumber pada satu masa boleh dipilih sebagai ditempah.

9. Pilih **Tempah** untuk menempah sumber dipilih dan biarkan Papan Jadual dibuka, agar anda boleh memilih sumber tambahan. Secara alternatif, pilih **Tempah & Keluar** untuk menampah sumber dipilih dan tutup Papan Jadual.

    ![Sumber untuk ditempah](media/Resource-Management-image19.png)

    Anda terima pemberitahuan tentang jam ditempah. Penunjuk permintaan menunjukkan bilangan keperluan tempahan dipenuhi dan bilangan yang dikekalkan. Anda juga boleh melihat berapa banyak kapasiti sumber dipilih telah digunakan. Pilih **Kembangkan** untuk melihat lebih lanjut tentang tempahan sumber.

9. Kembali ke pandangan **Semua Ahli Pasukan**. Dalam grid, sila maklum bahawa sumber generik telah digantikan oleh sumber bernama dan 40 jam disenaraikan sebagai ditempah untuk sumber tersebut.

    ![Gris Semua Ahli Pasukan yang Dikemas Kini](media/Resource-Management-image20.png)

    > [!NOTE]
    > Tiada jam ditugaskan ditunjukkan kerana ia telah ditempah secara terus pada pasukan. Ia tidak ditempah menggunakan tugasan tugas.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Tugaskan sumber generik untuk tugas dan jana tugasan sumber.

Dalam PSA, anda boleh mencipta tugas, kemudian tugaskan sumber generik kepada mereka. Dengan cara ini, permintaan sumber boleh diwakili oleh pemegang ruang sementara anda menganggarkan jadual dan angka kewangan anda. Anda kemudian boleh menjana keperluan sumber untuk sumber generik dan memenuhinya.

1. Pada halaman **Projek**, pada tab **Jadual**, pilih **Tambah** untuk mencipta tugas.

    ![Tugas baharu dicipta](media/Resource-Management-image21.png)

2. Dalam medan **Sumber**, pilih simbol **Pemilih Sumber**. Pemilih Sumber muncul dan menunjukkan ahli pasukan sedia ada untuk projek.

    ![Pemilih Sumber](media/Resource-Management-image22.png)

3. Masukkan nama sumber generik baharu dan pilih **Cipta**.

    ![Nama sumber generik baharu dimasukkan](media/Resource-Management-image23.png)

4. Dalam kotak dialog **Cipta Pantas: Ahli Pasukan Projek** yang muncul, dalam medan **Peranan**, pilih peranan untuk sumber generik. Dalam medan **Unit Penyumberan**, pilih unit organisasi untuk sumber generik. Kemudian pilih **Simpan**.

    ![Kotak dialog Cipta Pantas: Ahli Pasukan Projek](media/Resource-Management-image24.png)

    Ahli pasukan generik kini ditugaskan kepada tugas.

    ![Ahli pasukan generik ditugaskan kepada tugas](media/Resource-Management-image25.png)

    Pada tab **Pasukan**, anda akan melihat ahli pasukan generik baharu. Sila maklum bahawa ia hanya mempunyai jam ditugaskan. Jam ini adalah jumlah semua tugas yang ditugaskan kepada ahli pasukan generik. Ahli pasukan generik belum lagi mempunyai jam diperlukan atau keperluan sumber.

    ![Ahli pasukan generik pada tab Pasukan](media/Resource-Management-image26.png)

5. Anda kini boleh menugaskan ahli pasukan generik kepada tugas lain dengan menggunakan Pemilih Sumber.

    ![Ahli pasukan generik dalam Pemilih Sumber](media/Resource-Management-image27.png)

    Apabila anda selesai menugaskan sumber generik kepada tugas, anda boleh menjana keperluan sumber untuk sumber generik.

5. Pada tab **Pasukan**, pilih sumber generik dan kemudian pilih **Jana Keperluan**.

    ![Jana perintah Keperluan](media/Resource-Management-image28.png)

    Apabila keperluan dijana, ahli pasukan generik akan mempunyai jam diperlukan dan pautan untuk keperluan sumber.

    ![Pautan keperluan sumber](media/Resource-Management-image29.png)

    Selepas anda menempah sumber bernama, sumber generik dialih keluardaripada pasukan dan digantikan oleh sumber bernama.

    ![Sumber generik digantikan oleh sumber bernama](media/Resource-Management-image30.png)

    Pada tab **Jadual**, tugasan sumber generik dialih keluar dan digantikan dengan sumber bernama.

    ![Tugasan sumber generik digantikan dengan sumber bernama pada tab Jadual](media/Resource-Management-image31.png)

    > [!NOTE]
    > Tingkah laku ini berlaku hanya apabila sumber bernama ditempah penuh untuk keperluan sumber generik. Apabila sama ada sumber bernama menggantikan separuh keperluan sumber generik atau berbilang sumber bernama menggantikan keperluan sumber generik, sumber generik kekal ditugaskan kepada tugas.

    Dalam ilustrasi berikut, 80 jam tugas telah dirancang selama tempoh limat hari (16 jam setiap hari selama lima hari) dan ditugaskan kepada sumber generi bernama **Fungsi**.

    ![Tugas 80 jam, lima hari ditugaskan kepada sumber generi Fungsi](media/Resource-Management-image32.png)

    Apabila anda menjana keperluan, ia untuk 80 jam selama lima hari.

    ![Keperluan dijana untuk 80 jam selama lima hari](media/Resource-Management-image33.png)

    Disebabkan sumber tersedia hanya bekerja lapan jam setiap hari, dua sumber diperlukan untuk memenuhi keperluan ini.

    ![Sumber kedua](media/Resource-Management-image35.png)

    Pada tab **Pasukan**, anda kini boleh melihat sumber generik tiada jam diperlukan, tetapi jam ditugaskan masih muncul bersama dengan dua sumber bernama yang mengisi keperluan.

    ![Dua sumber bernama pada tab Pasukan](media/Resource-Management-image36.png)

    Pada tab **Jadual**, sumber generik kekal ditugaskan kepada tugas.

    ![Sumber generik pada tab Jadual](media/Resource-Management-image37.png)

PSA tidak menyokong kedua-dua sumber kepada tugas, kerana tingkah laku tersebut akan kurang menghasilkan jadual boleh diramalkan. Dalam contoh mudah ini, mudah untuk membahagian jam sama rata antara dua sumber. Nmaun, dalam senario lebih rumit yang melibatkan berbilang tugas dan berbilang sumber, PSA perlu membuat anggapan tentang cara ia perlu memperuntukkan tempahan yang diterima untuk berbilang sumber pada semua berbilang tugas.

Maka, dalam senario ini, pengurus projek bertanggungjawab menghuraikan berbilang tempahan dan menugaskan sebagaimana perlu. Untuk memperuntukkan tempahan, pengurus projek menugaskan tugasan daripada sumber generik kepada sumber bernama dan menggunakan pandangan **Pelarasan** untuk memastikan peruntukan berfungsi dengan tempahan.

### <a name="edit-a-resource-requirement"></a>Edit keperluan sumber

Selepas keperluan sumber dicipta, pengurus projek atau pengurus sumber mungkin mahu mengedit butiran untuk menghalusi kriteria carian apabila Papan Jadual digunakan. Untuk mengedit keperluan sumber, ikut langkah ini.

1. Pada halaman **Projek**, pada tab **Pasukan**, pilih pautan ke mana-mana keperluan pada sumber generik.
2. Pada halaman **Keperluan Sumber** yang muncul, anda boleh mengemas kini beberapa atribut. Berikut adalah beberapa contoh:

    - Nama
    - Tarikh Dari
    - Tarikh Sehingga
    - Tempoh
    - Jenis Sumber

Pada halaman **Keperluan Sumber**, pengurus projek atau pengurus sumber boleh juga mentakrifkan maklumat berikut:

- Kemahiran
- Peranan
- Keutamaan sumber
- Unit organisasi diutamakan

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Kemas kini tempahan sumber selepas ia ditempah pada projek

Selepas anda menambah sumber generik atau bernama kepada pasukan projek, anda boleh mengubah tempahan sumber.

1. Pada halaman **Projek**, pada tab **Pasukan**, pilih ahli pasukan kemudian pilih **Kekalkan Tempahan**.

    ![Papan Jadual dibuka untuk ahli pasukan terpilih](media/Resource-Management-image40.png)

    Papan Jadual muncul dan menunjukkan tempahan ahli pasukan projek. Kembangkan rekod ahli pasukan untuk melihat jam yang telah ditempah terhadap projek ini dan projek lain yang menggunakan kapasiti ahli pasukan.

2. Pilih dan seret tempahan untuk melanjutkan atau memendekkannya. Kotak dialog **Cipta Tempaham Sumber** muncul yang membolehkan anda melaraskan tempahan.

    ![Kotak dialog Cipta Tempahan Sumber](media/Resource-Management-image41.png)

3. Klik kanan tempahan. Anda kemudian boleh menggunakan menu pintasan untuk melengkapkan tindakan berikut:

    - Ubah status tempahan.
    - Edit tempahan.
    - Gantikan sumber pada pasukan projek.

### <a name="change-the-booking-status"></a>Ubah status tempahan

Anda boleh mengubah status tempahan lalai atau tersuai.

![Ubah Perintah Status](media/Resource-Management-image42.png)

Status berikut dimasukkan dalam PSA:

- **Dibatalkan** – Status ini membatalkan tempahan sumber dan mengosongkan kapasiti sumber.
- **Tempah Keras** – Status ini menggunakan kapasiti sumber. Tempahan lazimnya mempunyai status ini apabila anda membuka **Kekalkan Tempahan** dari grid **Semua Ahli Pasukan** pada halaman **Projek**.
- **Tempah Lembut** – Status ini menambah sumber kepada pasukan tetapi tidak menggunakan kapasiti sumber. Ini menunjukkan sumber telah disimpan untuk potensi kerja tetapi masih mempunyai kapasiti jika diperlukan untuk kerja lain. Dalam pandangan keseluruhan ketersediaan sumber, tempahan lembut mempunyai status berbeza daripada tempahan keras.
- **Dicadangkan** – Status ini mewakili cadangan pengurus projek atau pengurus sumber untuk sumber. Cadangan tidak menggunakan kapasiti sumber dan sumber tidak ditambah pada pasukan projek. Untuk tempah keras sumber dalam pasukan, pengurus projek mestilah menerima cadangan.

### <a name="submit-resource-requests"></a>Serahkan permintaan sumber

Permintaan sumber digunakan untuk menjalankan permintaan (keperluan sumber) yang mesti diisi oleh pengurus sumber. Untuk sumber generik yang telah ada dalam pasukan, anda boleh menyerahkan permintaan sumber secara terus. Permintaan sumber boleh diisi dalam dua cara:

- Pengurus sumber mengisi permintaan secara terus. Dalam situasi ini, sumber generik digantikan oleh tempahan keras yang ada sumber bernama.
- Sumber pengurus mencadangkan sumber kepada pengurus projek, dan pengurus projek meluluskan atau menolak cadangan sumber.

#### <a name="direct-fulfillment-of-resource-requests"></a>Memenuhi keperluan sumber secara terus

Apabila keperluan sumber dijana, pengurus projek boleh menyerahkan permintaan sumber untuk sumber generik dengan memilih sumber dan kemudian memilih **Serah Permintaan**.

![Butang Serah Permintaan](media/Resource-Management-image45.png)

Komen tentang sumber boleh diberikan kepada pengurus sumber yang mengisi permintaan tersebut. Selepas permintaan diserahkan, medan **Status** untuk ahli pasukan diubah kepada **Diserahkan**.

![Memasukkan komen pilihan](media/Resource-Management-image46.png)

Apabila pengurus sumber mengisi keperluan, ahli pasukan generik digantikan dengan sumber bernama dalam grid **Semua Ahli Pasukan**.

![Ahli pasukan generik digantikan dengan sumber bernama dalam grid Semua Ahli Pasukan](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Gunakan cadangan sumber untuk permintaan sumber

Daripada menempah terus sumber dalam permintaan sumber, pengurus sumber boleh mencadangkan sumber kepada pengurus projek. Pengurus projek mungkin menggunakan pilihan ini apabila padanan betul untuk keperluan tidak tersedia. Apabila pengurus sumber mencadangkan sumber, pengurus projek melihat bahawa medan **Status** untuk ahli pasukan generik diubah kepada **Memerlukan Semakan**.

![Status ahli pasukan generik diubah kepada Memerlukan Ulasan](media/Resource-Management-image48.png)

Untuk melihat cadangan sumber berserta dengan visualisasi kesan tempahan cadangan, klik dua kali ahli pasukan yang mempunyai status **Memerlukan Semakan**. Kemudian pilih tab **Sumber Dicadangkan**.

![Tab Sumber Dicadangkan](media/Resource-Management-image49.png)

Pilih **Terima Semua Cadangan** untuk menerima semua sumber dicadangkan atau **Tolak Semua Cadangan** untuk menolaknya. Jika anda menerima sumber dicadangkan, ia ditempah keras dalam projek sebagai ahli pasukan dan menggantikan sumber generik.

> [!NOTE]
> Anda mesti sama ada menerima atau menolak semua sumber dicadangkan. Anda boleh terima atau menolak separuh.

### <a name="substitute-a-resource-on-the-project-team"></a>Gantikan sumber pada pasukan projek

Kadangkala, pengurus projek mestilah menggantikan ahli pasukan ditempah dalam projek.

1. Pada halaman **Projek**, pada tab **Pasukan**, pilih sumber yang perlu diganti, kemudian pilih **Kekalkan Tempahan**.
2. Kembangkan sumber untuk melihat projek yang ditugaskan.

    ![Sumber dikembangkan untuk menunjukkan projek yang ditugaskan](media/Resource-Management-image50.png)

3. Klik kanan projek, kemudian pilih **Gantikan Sumber**.
4. Jika anda tahu sumber yang anda mahu gantikan untuk sumber semasa, pilih atau taip nama, kemudian pilih **Tugaskan semula**.

    ![Menentukan sumber gantian](media/Resource-Management-image51.png)

    Secara alternatif, ikuti langkah-langkah ini untuk mencari sumber:

    1. Pilih **Cari Penggantian**.

        ![Mencari sumber gantian](media/Resource-Management-image52.png)

        Pembantu Jadual mengembalikan senarai gantian tersedia. Dalam Pembantu Jadual, anda boleh menapis sumber tersedia untuk mencari gantian sesuai.

        ![Senarai gantian tersedia](media/Resource-Management-image53.png)

    2. Untuk menggantikan sumber, pilih sumber yang anda mahu, dan pilih **Gantikan**.

        ![Sumber gantian dipilih](media/Resource-Management-image54.png)

    Tempahan dan tugasan digantikan dengan sumber baharu.

    ![Tempahan dan tugasan digantikan dengan sumber baharu](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a>Sesuaikan tempahan dan tugasan ahli pasukan

Untuk ahli pasukan, tempahan dan tugasan tidak begitu digandingkan. Dengan kata lain, sumber boleh mempunyai tugasan tapi tidak tempahan, atau mereka boleh ada tempahan tetapi tidak tugasan. Tempahan dan tugasan hendaklah sejajar, agar sumber ada kapasiti komited untuk melaksanakan tugasan tugas. Namun, tempahan mungkin berdasarkan ketersediaan, dan pemasaan tugas mungkin berubah seiring projek diteruskan. Makan, gandingan longgar tempahan dan tugasan memberikan kefleksibelan.

PSA mempunyai tab **Pelarasan** yang membolehkan pengurus projek menyesuaikan tempahan dan tugasan ahli pasukan mereka untuk pasukan projek.

![Tab Penyelarasan](media/Resource-Management-image56.png)

Tab **Penyelarasan** menunjukkan tempahan dan tugasan sehingga ke tahap tugasan tugas individu untuk setiap ahli pasukan. Ia menunjukkan jam dalam sel yang mewakili tempoh masa dari bulan sehingga hari.

Tab juga menunjukkan keseluruhan jumlah bersih untuk projek, berserta lajur jumlah.

Untuk setiap sumber, tab mengira perbezaan antara tempahan dan gulung atas ahli pasukan bagi tugasan tugas ahli pasukan. Perbezaan ini hendaklah 0 (sifar). Dengan kata lain, tiada perbezaan antara tempahan dan tugasan. Perbezaan diwarnai dan dibayangi untuk menarik perhatian kepada dua keadaan:

- **Kekurangan tempahan** – Kekurangan tempahan berlaku apabila sumber ada lebih tugasan berbanding tempahan. Disebabkan kapasiti ini telah disimpan, pengurus projek mungkin mahu membetulkan keadaan ini dengan melanjutkan tempahan sumber untuk menampung desifit.
- **Tempahan berlebihan** – Tempahan berlebihan berlaku apabila sumber telah ditempah kepada projek tetapi belum ditugaskan kepada tugas. Keadaan ini mungkin boleh diterima dalam situasi di mana sumber ditempah untuk projek sebelum tugasan tugas berlaku. Namun, dalam situasi lain, sumber tidak dirandang ditugaskan kepada tugas. Dalam kes ini, pengurus projek perlu mempertimbangkan untuk membatalkan penempahan sumber, supaya kapasiti boleh digunakan untuk projek lain.

Dalam situasi tertentu, apabila anda melihat masa pada tahap lebih tingi daripada tahap hari (contohnya, tahap bulan), anda mungkin melihat perbezaan bersih sifar untuk sumber (dengan kata lain, tempahan = tugasan). Namun, jika anda melihat masa pada tahap minggu, anda mungkin melihat tugasan sifat jam dan tempahan 40 jam dalam minggu pertama, tetapi tugasan 40 jam dan tempahan sifar jam dalam minggu kedua. Keseluruhannya, tempahan dan tugasan diselaraskan, tetapi berbeza dari satu minggu ke minggu seterusnya.

Apabila anda melihat masa pada tahap lebih tinggi, sel dalam tab **Penyelarasan** mempunyai penunjuk untuk memaklumkan anda terdapat perbezaan pada tahap lebih rendah. Dengan mengklik dua kali dalam sel, anda boleh zum dekat untuk melihat perbezaan. Anda kemudian boleh klik kanan untuk zum jauh. Dengan memilih sumber dan menggunakan kawalan **Perbezaan seterusnya** pada bar alat grid, anda boleh pergi ke perbezaan seterusnya antara tempahan dan tugasan untuk sumber tersebut. Anda kemudian boleh menggunakan kawalan **Perbezaan sebelumnya** untuk kembali. Anda juga boleh mematikan penunjuk perbezaan dan tingkah laku navigasi di bawah **Tetapan**.

![Penunjuk perbezaan](media/Resource-Management-image57.png)

Jika anda ada tugasan tugas untuk sumber tetapi tiada tempahan, pada halaman **Projek**, pada tab **Penyelarasan**, pilih kekurangan tempahan dan kemudian pilih **Lanjutkan Tempahan**. Kotak dialog **Lanjutkan Tempahan** muncul dan menunjukkan tempahan yang diperlukan untuk menyelesaikan kekurangan sumber. Ia juga menunjukkan tempahan sedia ada sumber dalam semua projek atau entiti boleh dijadual lain. Jika anda pilih **OK** untuk mencipta tempahan untuk sumber, tanpa mengira ketersediaan sumber tersebut, anda mungkin menyebabkan tempahan berlebihan.

![Kotak dialog Lanjutkan Tempahan](media/Resource-Management-image58.png)

Pengurus projek atau pengurus sumber kemudian boleh menggunakan Papan Jadual untuk mengurus sebarang situasi di mana sumber ditempah berlebihan di luar kapasitinya.
