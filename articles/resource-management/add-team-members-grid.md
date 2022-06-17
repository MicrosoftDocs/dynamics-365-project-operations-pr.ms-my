---
title: Tambah ahli pasukan daripada grid ahli Pasukan
description: Artikel ini memberikan maklumat tentang cara anda boleh menguruskan sumber ahli pasukan.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3c0c277ca1fe2b709a6ff1c626f5ea7ec63705d6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928581"
---
# <a name="add-team-members-from-the-team-member-grid"></a>Tambah ahli pasukan daripada grid ahli Pasukan

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Dynamics 365 Project Operations memasukkan papan pemuka pengurus Sumber yang memberikan gambaran keseluruhan visual bagi permintaan dan penggunaan sumber di seluruh organisasi. Anda boleh menggunaan carta pada papan pemuka ini untuk visualisasikan maklumat berikut:

- **Permintaan sumber**: Carta **Permintaan Sumber Aktif** menunjukkan sumber yang telah diserahkan. Sumber diagregatkan sama ada melalui peranan atau projek.
- **Permintaan sumber belum diserahkan** – Carta **Permintaan Sumber Belum Ditugaskan** menunjukkan semua keperluan sumber yang belum diserahkan. Carta ini membantu Pengurus sumber melihat permintaan yang tidak tetap dan mungkin dihantar melalui permintaan sumber.
- **Penggunaan boleh dibilkan untuk minggu lepas**: Carta **Penggunaan mengikut Peranan** menunjukkan peratusan penggunaan boleh dibilkan aktual organisasi oleh peranan dengan penggunaan boleh dibilkan sasaran mengikut peranan.

    > [!NOTE]
    > Untuk menjadikan carta **Penggunaan mengikut Peranan** tersedia, cipta kerja yang menjalankan aliran kerja **UpdateRoleUtilization**. Peranan berulang ini berjalan setiap tujuh hari untuk mengira penggunaan boleh bil untuk tujuh hari sebelumnya. Keputusan diagregatkan mengikut peranan.

## <a name="manage-project-team-members"></a>Urus ahli pasukan projek

Pengurus projek boleh menggunakan papan pemuka Pengurus sumber untuk mengurus sumber pada projek. Contohnya, mereka boleh menambah ahli pasukan secara terus untuk projek dan menempah ahli pasukan untuk mengisi keperluan sumber yang direkod oleh sumber generik.

### <a name="add-a-team-member-directly-to-a-project"></a>Tambah ahli pasukan secara terus kepada projek

Untuk menambah ahli pasukan secara terus kepada projek, pada borang **Projek**, pada tab **Pasukan**, pilih **Baharu**. Kotak dialog **Cipta Pantas: Ahli Pasukan Projek** muncul. Dalam kotak dialog ini, anda boleh menjalankan tugas ini:

- **Tempah sumber bernama**: Dalam medan **Sumber Boleh Ditempah**, pilih nama sumber. Kemudian pilih sumber, tetapkan tempoh, kemudian pilih kaedah peruntukan. Sumber bernama yang anda pilih ditambah pada projek menggunakan kaedah peruntukan dipilih dan kalendar sumber.
- **Tambah sumber generik**: Biarkan medan **Sumber boleh ditempah** kosong, kemudian pilih peranan, tetapkan tempoh dan pilih kaedah peruntukan pilihan. Sumber generik ditambah kepada pasukan sebagai ruang letak. Ruang letak menyimpan corak permintaan yang digunakan untuk menempah sumber bernama pada pasukan. Keperluan dibuat mengikut kalendar projek.
- **Tambah sumber bernama pada pasukan tanpa menggunakan kapasiti sumber**: Dalam medan **Sumber Boleh Ditempah**, pilih sumber. Pilih tempoh, dan kemudian pilih **Tiada** sebagai kaedah peruntukan. Sumber ditambah pada pasukan, tetapi kapasiti sumber tidak digunakan melalui tempahan.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Tempah ahli pasukan untuk mengisi keperluan sumber untuk sumber generik

Dalam Project Operations, anda boleh menempah sumber generik pada pasukan projek. Anda juga boleh menentukan peranan, kapasiti yang diperlukan dan cara kapasiti tersebut diagihkan. Untuk keperluan sumber, anda boleh menentukan atribut yang berkaitan dengan sumber generik. Atirbut ini termasuklah kemahiran yang diperlukan, unit organisasi pilihan, dan sumber pilihan.

Lengkapkan langkah berikut untuk menentukan kemahiran yang diperlukan pada sumber generik untuk pembangun.

1. Pada borang **Projek**, pada tab **Pasukan**, pilih **Baharu** untuk menempah sumber generik.
2. Dalam pandangan **Semua Ahli Pasukan**, dalam lajur **Keperluan Sumber**, pilih pautan untuk menambah kemahiran diperlukan untuk sumber generik.
3. Pada borang **Keperluan Sumber**, dalam grid **Kemahiran**, pilih elipsis (**...**) dan kemudian pilih **Tambah Sifat Keperluan Baharu** untuk menambah kemahiran yang diperlukan untuk pembangun anda.
4. Dalam borang dialog **Cipta Pantas: Sifat Keperluan**, dalam medan **Sifat**, pilih kemahiran diperlukan.
5. Dalam medan **Nilai Penarafan**, pilih tahap kecekapan untuk kemahiran tersebut. 
6. Dalam medan **Keperluan Sumber**, tetapkan keperluan untuk sumber sumber daripada unit organisasi atau bahkan sumber bernama. Apabila anda telah selesai, pilih **Simpan**.
7. Pada borang **Keperluan Sumber**, pilih **Tempah** untuk memenuhi keperluan sumber. Anda juga boleh memilih sumber generik dalam grid **Semua Ahli Pasukan** dan kemudian pilih **Tempah**.

    > [!NOTE]
    > Dalam contoh ini, terdapat 40 jam diperlukan tetapi tiada jam ditempah aktual, kerana sumber generik tidak mempunyai tempahan. Selain itu, tiada jam yang ditugaskan, kerana sumber generik ditambah terus kepada pasukan dan bukannya ditambah dengan menggunakan tugasan tugas.

    Pada borang **Menjadualkan Pembantu**, anda boleh menapis sumber tersedia mengikut keperluan yang dinyatakan dalam keperluan sumber. Sumber diisih mengikut parameter pengisihan yang dinyatakan dalam papan Jadual.

   Beberapa penapis yang paling biasa digunakan ialah:

    - **Ciri berserta dengan penarafan**: Tapis mengikut kemahiran, pensijilan, kualiti sumber lain, selain daripada penarafan kecekapan.
    - **Peranan**: Tapis mengikut peranan lalai yang ditugaskan pada sumber boleh ditempah.
    - **Unit organisasi**: Tapis sumber boleh ditempah mengikut unit organisasi yang ditugaskan kepada mereka.

8. Jika anda tidak berpuas hati dengan kepurusan carian keperluan awal, anda boleh mengubah kriteria penapis. Kembangkan anak tetingkap **Pandangan Penapis** di sebelah kiri, kemudian pilih **Cari** untuk mencari sumber tambahan. Untuk mengubah cara hasil diisih, pilih **Isih**.
9. Pilih sumber mengikut permintaan yang dinyatakan dalam keperluan, seperti dinyakan di bahagian atas grid. Anda boleh mengosongkan pilihan sel dalam grid dan membiarkan kapasiti sumber terbuka. Hanya satu sumber pada satu masa boleh dipilih sebagai ditempah.
10. Pilih **Tempah** untuk menempah sumber dipilih dan biarkan Papan Jadual dibuka, agar anda boleh memilih sumber tambahan. Secara alternatif, pilih **Tempah & Keluar** untuk menampah sumber dipilih dan tutup Papan Jadual.
11. Kembali ke pandangan **Semua Ahli Pasukan**. Dalam grid, sila maklum bahawa sumber generik telah digantikan oleh sumber bernama dan 40 jam disenaraikan sebagai ditempah untuk sumber tersebut.

    > [!NOTE]
    > Tiada jam ditugaskan ditunjukkan kerana ia telah ditempah secara terus pada pasukan. Ia tidak ditempah menggunakan tugasan tugas.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Tugaskan sumber generik untuk tugas dan jana tugasan sumber.

Dalam Project Operations, anda boleh mencipta tugas, dan kemudian menugaskan sumber generik kepada mereka. Permintaan sumber kemudiannya boleh diwakili oleh ruang letak sementara anda menganggarkan jadual dan angka kewangan anda. Anda kemudian boleh menjana keperluan sumber untuk sumber generik dan memenuhinya.

1. Pada borang **Projek**, pada tab **Jadual**, pilih **Tambah** untuk mencipta tugas.
2. Dalam medan **Sumber**, pilih simbol **Pemilih Sumber**. Pemilih Sumber muncul dan menunjukkan ahli pasukan sedia ada untuk projek.
3. Masukkan nama sumber generik baharu dan pilih **Cipta**.
4. Dalam kotak dialog **Cipta Pantas: Ahli Pasukan Projek** yang muncul, dalam medan **Peranan**, pilih peranan untuk sumber generik. 
5. Dalam medan **Unit Penyumberan**, pilih unit organisasi untuk sumber generik. Kemudian pilih **Simpan**. Ahli pasukan generik kini ditugaskan kepada tugas.

   Pada tab **Pasukan**, anda akan melihat ahli pasukan generik baharu. Sila maklum bahawa ia hanya mempunyai jam ditugaskan. Jam ini adalah jumlah semua tugas yang ditugaskan kepada ahli pasukan generik. Ahli pasukan generik tidak mempunyai jam yang diperlukan atau keperluan sumber.

6. Anda kini boleh menugaskan ahli pasukan generik kepada tugas lain dengan menggunakan Pemilih Sumber.

   Apabila anda selesai menugaskan sumber generik kepada tugas, anda boleh menjana keperluan sumber untuk sumber generik.

7. Pada tab **Pasukan**, pilih sumber generik dan kemudian pilih **Jana Keperluan**. Apabila keperluan dijana, ahli pasukan generik akan mempunyai jam diperlukan dan pautan untuk keperluan sumber.

  Selepas anda menempah sumber bernama, sumber generik dialih keluardaripada pasukan dan digantikan oleh sumber bernama. Pada tab **Jadual**, tugasan sumber generik dialih keluar dan digantikan dengan sumber bernama.

  > [!NOTE]
  > Tingkah laku ini berlaku hanya apabila sumber bernama ditempah penuh untuk keperluan sumber generik. Apabila sama ada sumber bernama menggantikan separuh keperluan sumber generik atau berbilang sumber bernama menggantikan keperluan sumber generik, sumber generik kekal ditugaskan kepada tugas.

Project Operations tidak menugaskan kedua-dua sumber kepada tugas, kerana tingkah laku tersebut akan menghasilkan jadual yang kurang dapat diramalkan. Dalam contoh mudah ini, mudah untuk membahagian jam sama rata antara dua sumber. Nmaun, dalam senario lebih rumit yang melibatkan berbilang tugas dan berbilang sumber, PSA perlu membuat anggapan tentang cara ia perlu memperuntukkan tempahan yang diterima untuk berbilang sumber pada semua berbilang tugas.

Maka, dalam senario ini, Pengurus projek bertanggungjawab menghuraikan berbilang tempahan dan menugaskannya mengikut keperluan. Untuk memperuntukkan tempahan, Pengurus projek menugaskan tugasan daripada sumber generik kepada sumber bernama dan menggunakan pandangan **Penyelarasan** untuk memastikan peruntukan berfungsi dengan tempahan.

### <a name="edit-a-resource-requirement"></a>Edit keperluan sumber

Selepas keperluan sumber dicipta, Pengurus projek atau Pengurus sumber mungkin mahu mengedit butiran untuk menghalusi kriteria carian apabila Papan Jadual digunakan. Untuk mengedit keperluan sumber, ikut langkah ini.

1. Pada borang **Projek**, pada tab **Pasukan**, pilih pautan kepada mana-mana keperluan pada sumber generik.
2. Pada borang **Keperluan Sumber** yang muncul, masukkan maklumat lapangan yang perlu

   Pada borang **Keperluan Sumber**, Pengurus projek atau Pengurus sumber juga boleh mentakrifkan kemahiran, peranan, keutamaan sumber dan unit organisasi pilihan.

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Kemas kini tempahan sumber selepas ia ditempah pada projek

Selepas anda menambah sumber generik atau bernama kepada pasukan projek, anda boleh mengubah tempahan sumber.

1. Pada borang **Projek**, pada tab **Pasukan**, pilih ahli pasukan, dan kemudian pilih **Kekalkan Tempahan**.
 
   Papan Jadual muncul dan menunjukkan tempahan ahli pasukan projek. Kembangkan rekod ahli pasukan untuk melihat jam yang telah ditempah terhadap projek ini dan projek lain yang menggunakan kapasiti ahli pasukan.

2. Pilih dan seret tempahan untuk melanjutkan atau memendekkannya. Kotak dialog **Cipta Tempaham Sumber** muncul yang membolehkan anda melaraskan tempahan.
3. Klik kanan tempahan. Anda kemudian boleh menggunakan menu pintasan untuk melengkapkan tindakan berikut:

    - Ubah status tempahan
    - Edit tempahan
    - Gantikan sumber pada pasukan projek

### <a name="change-the-booking-status"></a>Ubah status tempahan

Anda boleh mengubah status tempahan lalai atau tersuai.

Status berikut termasuk dalam Project Operations:

- **Dibatalkan**: Membatalkan tempahan sumber dan mengosongkan kapasiti sumber.
- **Tempahan Tetap**: Menggunakan kapasiti sumber. Tempahan lazimnya mempunyai status ini apabila anda membuka **Kekalkan Tempahan** daripada grid **Semua Ahli Pasukan** pada borang **Projek**.
- **Tempahan Sementara**: Menambah sumber kepada pasukan tetapi tidak menggunakan kapasiti sumber. Status Ini menunjukkan yang sumber telah disimpan untuk kerja yang berpotensi tetapi masih mempunyai kapasiti jika diperlukan untuk kerja lain. Dalam pandangan keseluruhan ketersediaan sumber, tempahan lembut mempunyai status berbeza daripada tempahan keras.
- **Dicadangkan**: Mewakili cadangan Pengurus projek atau Pengurus sumber untuk sumber. Cadangan tidak menggunakan kapasiti sumber dan sumber tidak ditambah pada pasukan projek. Untuk membuat tempahan tetap sumber dalam pasukan, Pengurus projek mestilah menerima cadangan tersebut.

### <a name="submit-resource-requests"></a>Serahkan permintaan sumber

Permintaan sumber digunakan untuk melaksanakan permintaan atau keperluan sumber yang mesti dipenuhi oleh pengurus sumber. Untuk sumber generik yang telah ada dalam pasukan, anda boleh menyerahkan permintaan sumber secara terus. Permintaan sumber boleh diisi dalam dua cara:

- Pengurus sumber memenuhi permintaan itu secara langsung. Dalam situasi ini, sumber generik digantikan oleh tempahan keras yang ada sumber bernama.
- Pengurus sumber mencadangkan sumber kepada Pengurus projek, dan Pengurus projek meluluskan atau menolak sumber yang dicadangkan itu.

#### <a name="direct-fulfillment-of-resource-requests"></a>Memenuhi keperluan sumber secara terus

Apabila keperluan sumber dijana, Pengurus projek boleh menyerahkan permintaan sumber untuk sumber generik dengan memilih sumber dan kemudian memilih **Serah Permintaan**. Komen tentang sumber boleh diberikan kepada Pengurus sumber yang memenuhi permintaan tersebut. Selepas permintaan diserahkan, medan **Status** untuk ahli pasukan diubah kepada **Diserahkan**. Apabila Pengurus sumber memenuhi permintaan tersebut, ahli pasukan generik digantikan dengan sumber bernama dalam grid **Semua Ahli Pasukan**.

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Gunakan cadangan sumber untuk permintaan sumber

Daripada menempah secara terus sumber dalam permintaan sumber, Pengurus sumber boleh mencadangkan sumber kepada Pengurus projek. Pengurus projek mungkin menggunakan pilihan ini apabila padanan yang tepat untuk keperluan tidak tersedia. Apabila Pengurus sumber mencadangkan sumber, Pengurus projek melihat yang medan **Status** untuk ahli pasukan generik diubah kepada **Memerlukan Semakan**.

Anda boleh melihat sumber yang dicadangkan bersama-sama dengan visualisasi untuk kesan daripada tempahan cadangan. 

1. Klik dua kali ahli pasukan yang mempunyai status **Memerlukan Semakan**. 
2. Pilih tab **Sumber Dicadangkan**.
3. Pilih **Terima Semua Cadangan** untuk menerima semua sumber dicadangkan atau **Tolak Semua Cadangan** untuk menolaknya. Jika anda menerima sumber dicadangkan, ia ditempah keras dalam projek sebagai ahli pasukan dan menggantikan sumber generik.

> [!NOTE]
> Anda mesti sama ada menerima atau menolak semua sumber dicadangkan. Anda boleh terima atau menolak separuh.

### <a name="substitute-a-resource-on-the-project-team"></a>Gantikan sumber pada pasukan projek

Kadangkala, Pengurus projek mesti menggantikan ahli pasukan yang ditempah dalam projek.

1. Pada borang **Projek**, pada tab **Pasukan**, pilih sumber yang perlu diganti, kemudian pilih **Kekalkan Tempahan**.
2. Kembangkan sumber untuk melihat projek yang ditugaskan.
3. Klik kanan projek, kemudian pilih **Gantikan Sumber**.
4. Jika anda tahu sumber yang anda mahu gantikan bagi sumber semasa, pilih atau taip nama, dan kemudian pilih **Tugaskan semula**.

Atau. jika anda perlu mencari sumber, lengkapkan langkah berikut.

1. Pilih **Cari Penggantian**.

   Pembantu Jadual mengembalikan senarai gantian tersedia. Dalam Pembantu Jadual, anda boleh menapis sumber tersedia untuk mencari gantian sesuai.

2. Untuk menggantikan sumber, pilih sumber yang anda mahu, dan pilih **Gantikan**.   

   Tempahan dan tugasan digantikan dengan sumber baharu.

## <a name="reconcile-team-member-bookings-and-assignments"></a>Sesuaikan tempahan dan tugasan ahli pasukan

Untuk ahli pasukan, tempahan dan tugasan tidak begitu digandingkan. Dengan kata lain, sumber boleh mempunyai tugasan tapi tidak tempahan, atau mereka boleh ada tempahan tetapi tidak tugasan. Tempahan dan tugasan hendaklah sejajar, agar sumber ada kapasiti komited untuk melaksanakan tugasan tugas. Namun, tempahan mungkin berdasarkan ketersediaan, dan pemasaan tugas mungkin berubah seiring projek diteruskan. Makan, gandingan longgar tempahan dan tugasan memberikan kefleksibelan.

Project Operations mempunyai tab **Penyelarasan** yang membolehkan Pengurus projek menyelaraskan tempahan ahli pasukan dan tugasan mereka untuk pasukan projek.

Tab **Penyelarasan** menunjukkan tempahan dan tugasan sehingga ke tahap tugasan tugas individu untuk setiap ahli pasukan. Ia menunjukkan jam dalam sel yang mewakili tempoh masa dari bulan sehingga hari.

Tab juga menunjukkan keseluruhan jumlah bersih untuk projek, berserta lajur jumlah.

Untuk setiap sumber, tab mengira perbezaan antara tempahan dan gulung atas ahli pasukan bagi tugasan tugas ahli pasukan. Perbezaan ini hendaklah 0 (sifar). Dengan kata lain, tiada perbezaan antara tempahan dan tugasan. Perbezaan diwarnai dan dibayangi untuk menarik perhatian kepada dua keadaan:

- **Kekurangan tempahan**: Berlaku apabila sumber mempunyai lebih banyak tugasan berbanding tempahan. Disebabkan kapasiti ini belum disimpan, Pengurus projek mungkin mahu membetulkan keadaan ini dengan melanjutkan tempahan sumber untuk menampung defisit.
- **Tempahan berlebihan**: Berlaku apabila sumber telah ditempah kepada projek tetapi belum ditugaskan kepada tugas. Keadaan ini mungkin boleh diterima dalam situasi di mana sumber ditempah untuk projek sebelum tugasan tugas berlaku. Namun, dalam situasi lain, sumber tidak dirandang ditugaskan kepada tugas. Dalam kes ini, Pengurus projek perlu mempertimbangkan untuk membatalkan penempahan sumber, supaya kapasiti boleh digunakan untuk projek lain.

Dalam situasi tertentu, apabila anda melihat masa pada tahap lebih tingi daripada tahap hari, contohnya, tahap bulan, anda mungkin melihat perbezaan bersih sifar untuk sumber. dengan kata lain, tempahan = tugasan. Namun, jika anda melihat masa pada tahap minggu, anda mungkin melihat tugasan sifat jam dan tempahan 40 jam dalam minggu pertama, tetapi tugasan 40 jam dan tempahan sifar jam dalam minggu kedua. Keseluruhannya, tempahan dan tugasan diselaraskan, tetapi berbeza dari satu minggu ke minggu seterusnya.

Apabila anda melihat masa pada tahap lebih tinggi, sel dalam tab **Penyelarasan** mempunyai penunjuk untuk memaklumkan anda terdapat perbezaan pada tahap lebih rendah. Klik dua kali dalam sel untuk zum dekat bagi melihat perbezaannya. Anda kemudian boleh klik kanan untuk zum jauh. Dengan memilih sumber dan kemudian memilih **Perbezaan seterusnya** pada bar alat grid, anda boleh pergi ke perbezaan seterusnya antara tempahan dan tugasan untuk sumber tersebut. Pilih **Perbezaan sebelumnya** untuk kembali. Anda juga boleh mematikan penunjuk perbezaan dan tingkah laku navigasi di bawah **Tetapan**.

Jika anda ada penugasan tugas untuk sumber tetapi tiada tempahan, pada borang **Projek**, pada tab **Penyelarasan**, pilih kekurangan tempahan dan kemudian pilih **Lanjutkan Tempahan**. Kotak dialog **Lanjutkan Tempahan** muncul dan menunjukkan tempahan yang diperlukan untuk menyelesaikan kekurangan sumber. Kotak dialog juga menunjukkan tempahan sumber yang sedia ada di semua projek atau entiti lain yang boleh dijadualkan. Jika anda pilih **OK** untuk mencipta tempahan untuk sumber, tanpa mengira ketersediaan sumber tersebut, anda mungkin menyebabkan tempahan berlebihan.

Pengurus projek atau Pengurus sumber kemudiannya boleh menggunakan Papan Jadual untuk menguruskan sebarang keadaan yang sumber ditempah melebihi kapasitinya.


[!INCLUDE[footer-include](../includes/footer-banner.md)]