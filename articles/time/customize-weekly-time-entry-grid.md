---
title: Melanjutkan entri masa
description: Topik ini memberikan maklumat mengenai cara pemaju dapat melanjutkan kawalan kemasukan masa.
author: stsporen
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d9c14f0550d4429ac794607a3fb61717566207e4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124649"
---
# <a name="extending-time-entries"></a>Melanjutkan entri masa

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Operasi Projek Dynamics 365 termasuk kawalan tersuai kemasukan masa yang boleh dipanjangkan. Kawalan ini termasuk ciri-ciri berikut:

- Masukkan masa secara mendatar selama seminggu
- Jumlah mengikut hari, baris atau minggu
- Salin baris atau minggu
- Masa penyertaan melalui HH:mm atau HH.hh (secara automatik memeluk HH.hh)
- Import daripada tugasan, tempahan atau janji temu

Memanjangkan penyertaan masa kini mungkin dalam dua bahagian:
- [Tambah entri masa tersuai untuk kegunaan anda sendiri](#add)
- [Sesuaikan grid Entri Masa mingguan](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Tambah entri masa tersuai untuk kegunaan anda sendiri

Entri masa ialah entiti teras yang digunakan dalam berbilang senario. Dalam Gelombang April 1 2020, penyelesaian teras TESA telah diperkenalkan. TESA menyediakan entiti **Tetapan** dan peranan keselamatan **Pengguna Entri Masa** baharu. Medan baharu, **msdyn_start** dan **msdyn_end**, yang mempunyai hubungan langsung dengan **msdyn_duration** juga disertakan. Entiti, peranan keselamatan dan medan baharu membenarkan pendekatan yang lebih bersepadu untuk masa yang merentasi berbilang produk.


### <a name="time-source-entity"></a>Entiti sumber masa
| Medan | Penerangan | 
|-------|------------|
| Nama  | Nama entri Sumber masa yang digunakan sebagai nilai pemilihan apabila mencipta entri masa. |
| Sumber Masa Lalai [Sumber Masa: isdefault] | Secara lalai, hanya satu Sumber Masa boleh ditandakan pada lalai. Ini membolehkan entri untuk lalai kepada sumber masa jika nilai tidak ditentukan. |
|Jenis Sumber Masa [Sumber Masa: sourcetype] | Jenis sumber ialah pilihan (Jenis Sumber Entri Masa) yang membolehkan perkaitan sumber masa untuk aplikasi. Microsoft mempunyai nilai yang lebih besar daripada 190,000,000.|


### <a name="time-entries-and-the-time-source-entity"></a>Entri masa dan Entiti sumber masa
Setiap kali penyertaan adalah berkaitan dengan rekod sumber masa. Rekod ini menentukan cara dan aplikasi perlu memproses penyertaan masa.

Penyertaan masa sentiasa satu blok masa bersama dengan permulaan, akhir, dan tempoh yang berkaitan.

Logik akan secara automatik mengemas kini rekod kemasukan dalam situasi berikut:

- Jika dua daripada tiga medan berikut disediakan, medan ketiga dikira secara automatik: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Medan, **msdyn_start** dan **msdyn_end** adalah peka zon masa.
- Entri masa yang dicipta dengan hanya **msdyn_date** dan **msdyn_duration** ditetapkan akan bermula pada waktu tengah malam. Medan **msdyn_start** dan **msdyn_end** akan dikemas kini dengan sewajarnya.

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



## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Sesuaikan kawalan Entri masa mingguan
Pembangun boleh menambah medan dan carian tambahan kepada entiti lain dan melaksanakan peraturan perniagaan tersuai untuk menyokong senario perniagaan mereka.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Tambah medan tersuai dengan carian ke entiti lain
Terdapat tiga langkah utama untuk menambah medan tersuai ke grid kemasukan masa mingguan.

1. Tambah medan tersuai ke kotak dialog cipta pantas.
2. Konfigurasikan grid untuk menunjukkan medan tersuai.
3. Tambah medan tersuai pada baris edit aliran tugas atau sel edit aliran tugas.

Pastikan bahawa medan baharu mempunyai pengesahan yang diperlukan dalam baris atau sel edit aliran tugas. Sebagai sebahagian daripada langkah ini, kunci medan berdasarkan status entri masa.

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Tambah medan tersuai ke kotak dialog cipta pantas
Tambah medan tersuai kepada kotak dialog **Cipta Cipta Pantas Entri Masa**. Kemudian, apabila entri masa ditambahkan, nilai boleh dimasukkan dengan memilih **Baharu**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurasikan grid untuk menunjukkan medan tersuai
Terdapat dua langkah utama untuk menambah medan tersuai ke grid kemasukan masa mingguan:

  - Sesuaikan pandangan dan tambah medan tersuai
  - Cipta entri masa tersuai lalai baharu 


#### <a name="customize-a-view-and-add-a-custom-field"></a>Sesuaikan pandangan dan tambah medan tersuai

Sesuaikan pandangan **Entri Masa Mingguan Saya** dan tambah medan tersuai padanya. Anda boleh memilih kedudukan dan saiz medan tersuai dalam grid dengan mengedit sifat tersebut dalam pandangan.

#### <a name="create-a-new-default-custom-time-entry"></a>Cipta entri masa tersuai lalai baharu

Pandangan ini harus mengandungi **Perihalan** dan **Komen Luaran**, sebagai tambahan kepada lajur yang anda mahu ada dalam grid. 

1. Pilih kedudukan, saiz dan isih pesanan lalai grid dengan mengedit sifat tersebut dalam pandangan. 
2. Konfigurasikan kawalan tersuai untuk pandangan ini supaya ia adalah kawalan **Grid Entri Masa**. 
3. Tambah kawalan ini ke pandangan, dan pilih ia untuk web, telefon dan tablet. 
4. Konfigurasikan parameter untuk grid entri masa mingguan. 
5. Tetapkan medan **Tarikh Mula** ke **msdyn_date**, tetapkan medan **Tempoh** untuk **msdyn_duration** dan tetapkan medan **Status** kepada **msdyn_entrystatus**. 
6. Untuk pandangan lalai, medan **Senarai Status Baca Sahaja** ditetapkan kepada **192350002,192350003,192350004**. Medan **Aliran Tugas Edit Baris** ditetapkan kepada **msdyn_timeentryrowedit**. Medan **Aliran Tugas Edit Sel** ditetapkan kepada **msdyn_timeentryedit**. 
7. Anda boleh menyesuaikan medan ini untuk menambah atau mengeluarkan status baca sahaja atau untuk menggunakan pengalaman berasaskan tugas berbeza (TBX) untuk pengeditan baris atau sel. Medan ini kini terikat dengan nilai statik.


> [!NOTE] 
> Kedua-dua pilihan akan mengalih keluar beberapa penapisan siap guna pada entiti **Projek** dan **Tugas Projek** supaya semua pandangan carian untuk entiti tersebut akan boleh dilihat. Keluar dari kotak, hanya pandangan carian yang berkaitan boleh dilihat.

Tentukan aliran tugas yang sesuai untuk medan tersuai. Jika anda menambah medan kepada grid, ia perlu ditambah dalam aliran tugas edit baris yang digunakan untuk medan yang digunakan pada seluruh baris entri masa. Jika medan tersuai mempunyai nilai unik setiap hari, seperti medan tersuai untuk **Masa akhir**, ia harus pergi dalam edit aliran tugas sel.

Untuk menambah medan tersuai kepada aliran tugas, seret elemen **Medan** ke kedudukan yang sesuai pada halaman dan kemudian tetapkan sifat medan. Tetapkan sifat **Sumber** ke **Entri Masa** dan set sifat **Medan Data** ke medan tersuai. Sifat **Medan** menentukan nama paparan pada halaman TBX. Pilih **Gunakan** untuk menyimpan perubahan anda pada medan dan kemudian pilih **Kemas kini** untuk menyimpan perubahan anda pada halaman.

Untuk menggunakan halaman TBX tersuai baharu sebagai ganti, cipta proses baharu. Tetapkan kategori untuk **Aliran Proses Perniagaan**, tetapkan entiti ke **Entri Masa** dan tetapkan jenis proses perniagaan untuk **Menjalankan proses sebagai aliran tugas**. Di bawah **Sifat**, sifat **Nama halaman** patut ditetapkan ke nama paparan untuk halaman. Tambah semua medan yang berkaitan dengan halaman TBX. Simpan dan aktifkan proses. Kemas kini sifat kawalan tersuai untuk aliran tugas yang relevan kepada nilai **Nama** pada proses.

### <a name="add-new-option-set-values"></a>Tambah nilai set pilihan baharu
Untuk menambah nilai set pilihan kepada medan siap guna, buka halaman pengeditan untuk medan tersebut dan di bawah **Jenis**, pilih **Edit** di sebelah set pilihan. Tambah pilihan baharu yang mempunyai label tersuai dan warna. Jika anda mahu menambah status entri masa baharu, medan siap guna dinamakan **Status Entri** bukan **Status**.

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
Gunakan pengesahan pasang masuk untuk sebarang pengesahan yang memerlukan lebih banyak konteks daripada yang tersedia dalam rekod entri tunggal atau untuk sebarang pengesahan yang anda mahu jalankan pada kemas kini sebaris dalam grid. Untuk melengkapkan pengesahan, cipta pasang masuk tersuai pada **Entiti Masa**.

### <a name="copying-time-entries"></a>Menyalin entri masa
Gunakan pandangan **Salin Lajur Entri Masa** untuk mentakrifkan senarai medan untuk disalin semasa entri masa. **Tarikh** dan **Tempoh** adalah medan yang diperlukan dan tidak boleh dialih keluar daripada pandangan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]