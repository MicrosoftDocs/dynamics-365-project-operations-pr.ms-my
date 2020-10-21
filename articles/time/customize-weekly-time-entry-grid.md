---
title: Melanjutkan entri masa
description: Topik ini memberikan maklumat mengenai cara pemaju dapat melanjutkan kawalan kemasukan masa.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 93f411ad7c86beefcc35e7799a03987dacdcd62b
ms.sourcegitcommit: 5a29adce48133e09f051929e8544d6c2c93c025d
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930891"
---
# <a name="extending-time-entries"></a>Melanjutkan entri masa

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Operasi Projek Dynamics 365 termasuk kawalan tersuai kemasukan masa yang boleh dipanjangkan. Kawalan ini termasuk ciri-ciri berikut:

- Masukkan masa secara mendatar selama seminggu
- Jumlah mengikut hari, baris atau minggu
- Salin baris atau minggu
- Masa penyertaan melalui HH:mm atau HH.hh (secara automatik memeluk HH.hh)
- Import daripada tugasan, penempahan atau janji temu

Memanjangkan penyertaan masa kini mungkin dalam dua bahagian:
- [Tambah entri masa tersuai untuk kegunaan anda sendiri](#add)
- [Sesuaikan grid Entri Masa mingguan](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Tambah entri masa tersuai untuk kegunaan anda sendiri.

Penyertaan masa ialah entiti teras yang direka untuk digunakan untuk berbilang senario. Dalam April Wave 1 2020, penyelesaian teras TESA telah diperkenalkan, yang menyediakan entiti **Tetapan** dan peranan keselamatan **Pengguna entri kali baharu**. Medan baharu, **msdyn_start** dan **msdyn_end** yang mempunyai hubungan langsung dengan **msdyn_duration** juga disertakan. Entiti, peranan keselamatan dan medan baharu membenarkan pendekatan yang lebih bersepadu untuk masa yang merentasi berbilang produk.


### <a name="time-source-entity"></a>Entiti Sumber Masa
| Medan | Penerangan  | 
|-------|------------|
| Nama  | Nama entri Sumber Masa yang digunakan sebagai nilai pemilihan semasa penciptaan entri masa. |
| Sumber Masa Lalai [Sumber Masa: isdefault] | Secara lalai, hanya satu Sumber Masa mungkin ditandakan pada sumber masa lalai. Keupayaan ini membenarkan penyertaan untuk lalai kepada sumber masa jika seseorang tidak ditentukan. |
|Jenis Sumber Masa [Sumber Masa: sourcetype] | Jenis sumber ialah pilihan (Jenis Sumber Entri Masa) yang membolehkan perkaitan sumber masa untuk aplikasi. Nilai tambahan akan ditambah ke set pilihan ini kerana aplikasi tambahan ditambah. Ambil perhatian bahawa Microsoft mempunyai nilai yang lebih besar daripada 190,000,000.|


### <a name="time-entries-and-the-time-source-entity"></a>Entri masa dan Entiti Sumber Masa
Setiap kali penyertaan adalah berkaitan dengan rekod sumber masa. Rekod ini menentukan cara dan aplikasi perlu memproses penyertaan masa.

Penyertaan masa sentiasa satu blok masa bersama dengan permulaan, akhir, dan tempoh yang berkaitan.

Logik akan secara automatik mengemas kini rekod kemasukan dalam situasi berikut:

- Jika dua daripada tiga medan berikut disediakan, ketiga dikira secara automatik 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Medan, **msdyn_start** dan **msdyn_end** adalah peka zon masa.
- Entri masa dicipta dengan hanya **msdyn_date** dan **msdyn_duration** ditetapkan akan bermula pada waktu tengah malam dan **msdyn_start** dan **msdyn_end** akan dikemas kini dengan sewajarnya.

#### <a name="time-entry-types"></a>Jenis entri masa

Rekod entri masa mempunyai jenis berkaitan yang mentakrifkan tingkah laku dalam aliran penyerahan untuk permohonan yang berkaitan.

|Label | Nilai|
|-----|-----|
|Sedang rehat   |192,355,000|
|Pelancongan | 192,355,001|
|Kerja Lebih Masa   | 192,354,320|
|Kerja   | 192,350,000|
|Ketidakhadiran    | 192,350,001|
|Percutian   | 192,350,002|



## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Sesuaikan kawalan Entri Masa mingguan
Pembangun boleh menambah medan dan carian tambahan kepada entiti lain dan melaksanakan peraturan perniagaan tersuai untuk menyokong senario perniagaan mereka.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Tambah medan tersuai dengan carian ke entiti lain
Terdapat tiga langkah utama untuk menambah medan tersuai ke grid kemasukan masa mingguan.

- Tambah medan tersuai ke kotak dialog cipta pantas.
- Konfigurasikan grid untuk menunjukkan medan tersuai.
- Tambah medan tersuai kepada sama ada baris edit aliran tugas atau sel edit aliran tugas.

Anda juga mesti memastikan bahawa medan baharu mempunyai pengesahan yang diperlukan dalam baris atau edit aliran tugas. Sebagai sebahagian daripada langkah ini anda mesti mengunci medan, berdasarkan status entri masa.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Tambah medan tersuai ke kotak dialog cipta pantas
Anda mesti menambah medan tersuai kepada kotak dialog **Cipta Pantas Entri Masa**. Pengguna kemudian boleh memasukkan nilai apabila mereka menambahkan penyertaan masa dengan memilih **Baharu**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurasikan grid untuk menunjukkan medan tersuai
Terdapat dua langkah utama untuk menambah medan tersuai ke grid kemasukan masa mingguan:

  - Sesuaikan pandangan dan tambah medan tersuai
  - Cipta entri masa tersuai lalai baharu 


**Sesuaikan pandangan dan tambah medan tersuai**

Anda boleh menyesuaikan pandangan **Entri Masa Mingguan Saya** dan tambah medan tersuai kepadanya. Anda boleh memilih kedudukan dan saiz medan tersuai dalam grid dengan mengedit sifat tersebut dalam pandangan.

**Cipta entri masa tersuai lalai baharu** 

Pandangan ini harus mengandungi **Perihalan** dan **Komen Luaran**, sebagai tambahan kepada lajur yang anda mahu ada dalam grid. 

1. Pilih kedudukan, saiz dan isih pesanan lalai grid dengan mengedit sifat tersebut dalam pandangan. 
2. Konfigurasikan kawalan tersuai untuk pandangan ini supaya ia adalah kawalan **Grid Entri Masa**. 
3. Tambah kawalan ini ke pandangan, dan pilih ia untuk web, telefon dan tablet. 
4. Konfigurasikan parameter untuk grid entri masa mingguan. Tetapkan medan **Tarikh Mula** ke **msdyn_date**, tetapkan medan **Tempoh** untuk **msdyn_duration** dan tetapkan medan **Status** kepada **msdyn_entrystatus**. 
5. Untuk pandangan lalai, medan **Senarai Status Baca Sahaja** ditetapkan kepada **192350002, 192350003, 192350004**, medan **Baris Edit Aliran Tugas** ditetapkan kepada **msdyn_timeentryrowedit** dan **Sel Edit Aliran Tugas** ditetapkan kepada **msdyn_timeentryedit.** 
6. Anda boleh menyesuaikan medan ini untuk menambah atau mengeluarkan status baca sahaja atau untuk menggunakan pengalaman berasaskan tugas berbeza (TBX) untuk pengeditan baris atau sel. Medan ini sepatutnya terikat dengan nilai statik.


> [!NOTE] 
> Kedua-dua pilihan akan mengeluarkan beberapa penapisan keluar kotak **Projek** dan entiti **Tugas Projek** supaya semua pandangan carian untuk entiti akan boleh dilihat. Keluar dari kotak, hanya pandangan carian yang berkaitan boleh dilihat.
Anda mesti menentukan aliran tugas yang sesuai untuk medan tersuai. Kemungkinan besar, jika anda menambah medan ke grid, ia perlu pergi dalam baris edit aliran tugas yang digunakan untuk medan yang diguna pakai pada seluruh baris entri masa. Jika medan tersuai mempunyai nilai unik setiap hari, seperti medan tersuai untuk **Masa akhir**, ia harus pergi dalam edit aliran tugas sel.

Untuk menambah medan tersuai kepada aliran tugas, seret elemen **Medan** ke kedudukan yang sesuai pada halaman dan kemudian tetapkan sifat medan. Tetapkan sifat **Sumber** ke **Entri Masa** dan set sifat **Medan Data** ke medan tersuai. Sifat **Medan** menentukan nama paparan pada halaman TBX. Pilih **Gunakan** untuk menyimpan perubahan anda pada medan dan kemudian pilih **Kemas kini** untuk menyimpan perubahan anda pada halaman.

Untuk menggunakan halaman TBX tersuai baharu sebagai ganti, cipta proses baharu. Tetapkan kategori untuk **Aliran Proses Perniagaan**, tetapkan entiti ke **Entri Masa** dan tetapkan jenis proses perniagaan untuk **Menjalankan proses sebagai aliran tugas**. Di bawah **Sifat**, sifat **Nama halaman** patut ditetapkan ke nama paparan untuk halaman. Tambah semua medan yang berkaitan dengan halaman TBX. Simpan dan aktifkan proses, dan kemudian kemas kini sifat kawalan tersuai untuk aliran tugas yang relevan kepada nilai **Nama** pada proses.

### <a name="add-new-option-set-values"></a>Tambah nilai set pilihan baharu
Untuk menambah nilai set pilihan ke medan luar, buka halaman pengeditan untuk medan dan kemudian, di bawah **Jenis**, pilih **Edit** di sebelah set pilihan. Seterusnya, tambah pilihan baru yang mempunyai label tersuai dan warna. Jika anda mahu menambah status kemasukan masa baharu, medan di luar kotak dinamakan **Status Entri** bukan **Status**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Tetapkan status kemasukan masa baharu sebagai baca sahaja
Untuk memilih status entri masa baharu sebagai baca sahaja, tambah nilai masukan masa baharu ke sifat senarai **Senarai Status Baca Sahaja** sahaja. Bahagian yang boleh diedit bagi grid kemasukan masa akan dikunci untuk baris yang mempunyai status baharu.
Seterusnya, tambah peraturan perniagaan untuk mengunci semua medan **Edit Baris Entri Masa** dan **Edit Entri Masa** halaman TBX. Anda boleh mengakses peraturan perniagaan untuk halaman ini dengan membuka editor aliran proses perniagaan untuk halaman dan kemudian memilih **Peraturan Perniagaan**. Anda boleh menambahkan status baharu pada keadaan dalam peraturan perniagaan sedia ada atau anda boleh menambah peraturan perniagaan baharu untuk status baharu.

### <a name="add-custom-validation-rules"></a>Tambah peraturan pengesahan tersuai
Terdapat dua jenis peraturan pengesahan yang anda boleh tambah untuk pengalaman grid kemasukan masa mingguan:

- Peraturan perniagaan pihak klien yang berfungsi dalam kotak dialog cipta pantas dan pada halaman TBX.
- Pengesahan pasang masuk bahagian pelayan yang diguna pakai untuk semua kemas kini kemasukan.

#### <a name="business-rules"></a>Peraturan perniagaan
Gunakan peraturan perniagaan untuk mengunci dan membuka kunci medan, masukkan nilai lalai dalam medan dan takrifkan pengesahan yang memerlukan maklumat hanya dari rekod kemasukan masa semasa. Anda boleh mengakses peraturan perniagaan untuk halaman TBX dengan membuka editor aliran proses perniagaan untuk halaman dan kemudian memilih **Peraturan Perniagaan**. Anda kemudian boleh mengedit peraturan perniagaan sedia ada atau menambah peraturan perniagaan baharu. Untuk pengesahan yang lebih tersuai malah, anda boleh menggunakan peraturan perniagaan untuk menjalankan JavaScript.

#### <a name="plug-in-validations"></a>Pengesahan pasang masuk
Anda patut menggunakan pengesahan pasang masuk untuk sebarang pengesahan yang memerlukan lebih banyak konteks daripada tersedia dalam rekod kemasukan tunggal atau sebarang pengesahan yang anda mahu jalankan pada kemas kini dalam baris dalam grid. Untuk melengkapkan pengesahan, cipta pasang masuk tersuai pada **Entiti Masa**.
