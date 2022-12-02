---
title: Melanjutkan entri masa
description: Artikel ini memberikan maklumat tentang cara pemaju dapat melanjutkan kawalan entri masa.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 7ed501af3fb2059ab3c3ab6f6c957fe518595d55
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914781"
---
# <a name="extending-time-entries"></a>Melanjutkan entri masa

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Dynamics 365 Project Operations termasuk kawalan tersuai entri masa yang boleh dilanjutkan. Kawalan ini termasuk ciri-ciri berikut:

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
Setiap kali penyertaan adalah berkaitan dengan rekod sumber masa. Rekod ini menentukan aplikasi yang perlu memproses entri masa dan caranya.

Penyertaan masa sentiasa satu blok masa bersama dengan permulaan, akhir, dan tempoh yang berkaitan.

Logik akan secara automatik mengemas kini rekod kemasukan dalam situasi berikut:

- Jika dua daripada tiga medan berikut disediakan, medan ketiga dikira secara automatik: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Medan **msdyn_start** dan **msdyn_end** adalah peka zon waktu.
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

1. Tambah medan tersuai ke kotak dialog **Cipta pantas**.
2. Konfigurasikan grid untuk menunjukkan medan tersuai.
3. Tambah medan tersuai kepada halaman **Edit baris** atau **Edit entri masa**, mengikut kesesuaian.

Pastikan bahawa medan baharu mempunyai pengesahan yang diperlukan pada halaman **Edit baris** atau **Edit entri masa**. Sebagai sebahagian daripada tugas ini, kunci medan, berdasarkan status entri masa.

Apabila anda menambahkan medan tersuai pada grid **Entri masa** dan kemudian mencipta entri masa secara langsung dalam grid, medan tersuai untuk entri tersebut ditetapkan secara automatik supaya ia sepadan dengan baris. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Tambah medan tersuai ke kotak dialog Cipta pantas
Tambah medan tersuai ke kotak dialog **Cipta pantas: Cipta Entri Masa**. Pengguna kemudian boleh memasukkan nilai apabila mereka menambahkan penyertaan masa dengan memilih **Baharu**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurasikan grid untuk menunjukkan medan tersuai
Terdapat dua langkah untuk menambah medan tersuai ke grid **Entri masa mingguan**.

- Sesuaikan pandangan **Entri Masa Mingguan Saya** dan tambah medan tersuai padanya. Anda boleh menentukan kedudukan dan saiz medan tersuai dalam grid dengan mengedit sifat tersebut dalam pandangan.
- Cipta pandangan entri masa tersuai baharu dan tetapkan sebagai pandangan lalai. Pandangan ini harus mengandungi medan **Perihalan** dan **Komen luaran**, sebagai tambahan kepada lajur yang anda mahu ada dalam grid. Anda boleh menentukan kedudukan, saiz dan isih pesanan lalai grid dengan mengedit sifat tersebut dalam pandangan. Seterusnya, konfigurasikan kawalan tersuai untuk pandangan ini supaya ia adalah kawalan **Grid Entri Masa**. Tambah kawalan kepada pandangan dan pilih kawalan untuk **Web**, **Telefon** dan **Tablet**. Seterusnya, konfigurasikan parameter untuk grid **Entri masa mingguan**. Tetapkan medan **Tarikh mula** kepada **msdyn\_date**, tetapkan medan **Tempoh** kepada **msdyn\_duration** dan tetapkan medan **Status** kepada **msdyn\_entrystatus**. Medan **Senarai Status Baca Sahaja** ditetapkan kepada **192350002 (Diluluskan)**, **192350003 (Diserahkan)**, atau **192350004 (Panggilan Balik Diminta)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Tambah medan tersuai kepada halaman edit yang sesuai
Halaman yang digunakan untuk mengedit entri masa atau baris entri masa boleh didapati di bawah **Borang**. Butang **Edit entri** dalam grid membuka halaman **Edit entri** dan butang **Edit baris** membuka halaman **Edit baris**. Anda boleh mengedit halaman ini supaya merangkumi medan tersuai.

Kedua-dua pilihan mengeluarkan beberapa penapisan keluar kotak pada entiti **Projek** dan **Tugas Projek** supaya semua pandangan carian untuk entiti boleh dilihat. Keluar dari kotak, hanya pandangan carian yang berkaitan boleh dilihat.

Anda mesti menentukan halaman yang sesuai untuk medan tersuai. Kemungkinan besar, jika anda menambah medan ke grid, ia perlu berada pada halaman **Edit baris** yang digunakan untuk medan yang diguna pakai pada seluruh baris entri masa. Jika medan tersuai mempunyai nilai unik dalam baris setiap hari, (contohnya, jika ia merupakan medan tersuai untuk masa tamat), ia harus berada pada halaman **Edit entri masa**.

Untuk menambah medan tersuai kepada halaman, seret elemen **Medan** ke kedudukan yang sesuai pada halaman dan kemudian tetapkan sifatnya.

### <a name="add-new-option-set-values"></a>Tambah nilai set pilihan baharu
Untuk menambah nilai set pilihan kepada medan luar kotak, ikut langkah ini.

1. Buka halaman pengeditan untuk medan dan kemudian, di bawah **Jenis**, pilih **Edit** di sebelah set pilihan.
2. Tambah pilihan baharu yang mempunyai label tersuai dan warna. Jika anda mahu menambah status kemasukan masa baharu, medan di luar kotak dinamakan **Status Entri**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Tetapkan status kemasukan masa baharu sebagai baca sahaja
Untuk memilih status entri masa baharu sebagai baca sahaja, tambah nilai masukan masa baharu ke sifat senarai **Senarai Status Baca Sahaja** sahaja. Pastikan untuk menambahkan nombor, bukan label. Bahagian yang boleh diedit bagi grid entri masa kini akan dikunci untuk baris yang mempunyai status baharu. Untuk menetapkan sifat **Senarai Status Baca Sahaja** yang berbeza untuk pandangan **Entri Masa** yang berbeza, tambahkan grid **Entri masa** dalam bahagian **Kawalan tersuai** dan konfigurasikan parameter mengikut kesesuaian.

Seterusnya, tambahkan peraturan perniagaan untuk mengunci semua medan pada halaman **Edit baris** dan **Edit entri masa**. Untuk mengakses peraturan perniagaan untuk halaman ini, buka editor borang untuk setiap halaman dan kemudian pilih **Peraturan perniagaan**. Anda boleh menambahkan status baharu pada keadaan dalam peraturan perniagaan sedia ada atau anda boleh menambah peraturan perniagaan baharu untuk status baharu.

### <a name="add-custom-validation-rules"></a>Tambah peraturan pengesahan tersuai
Anda boleh menambah dua jenis peraturan pengesahan untuk pengalaman grid **Entri masa mingguan**:

- Peraturan perniagaan pihak klien yang berfungsi pada halaman
- Pengesahan pasang masuk bahagian pelayan yang diguna pakai untuk semua kemas kini entri masa

#### <a name="client-side-business-rules"></a>Peraturan perniagaan pihak klien
Gunakan peraturan perniagaan untuk mengunci dan membuka kunci medan, masukkan nilai lalai dalam medan dan takrifkan pengesahan yang memerlukan maklumat hanya dari rekod kemasukan masa semasa. Untuk mengakses peraturan perniagaan untuk satu halaman, buka editor borang dan kemudian pilih **Peraturan perniagaan**. Anda kemudian boleh mengedit peraturan perniagaan sedia ada atau menambah peraturan perniagaan baharu.

#### <a name="server-side-plug-in-validations"></a>Pengesahan pasang masuk bahagian pelayan
Anda harus menggunakan pengesahan pasang masuk untuk apa-apa pengesahan yang memerlukan lebih banyak konteks daripada yang tersedia dalam rekod entri masa tunggal. Anda juga harus menggunakannya untuk apa-apa pengesahan yang anda mahu jalankan pada kemas kini dalam baris dalam grid. Untuk melengkapkan pengesahan, cipta pasang masuk tersuai pada entiti **Entri Masa**.

### <a name="limits"></a>Had
Pada masa ini, grid **Entri masa** mempunyai had saiz 500 baris. Jika terdapat lebih daripada 500 baris, baris lebihan tidak akan ditunjukkan. Tidak ada cara untuk menambah had saiz ini.

### <a name="copying-time-entries"></a>Menyalin entri masa
Gunakan pandangan **Salin Lajur Entri Masa** untuk mentakrifkan senarai medan untuk disalin semasa entri masa. **Tarikh** dan **Tempoh** adalah medan yang diperlukan dan tidak boleh dialih keluar daripada pandangan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
