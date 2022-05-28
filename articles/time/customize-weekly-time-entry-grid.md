---
title: Melanjutkan entri masa
description: Topik ini memberikan maklumat mengenai cara pemaju dapat melanjutkan kawalan kemasukan masa.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 6b91aecd76950d2bd37192d634c80ea98d08034e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582997"
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
Setiap kali penyertaan adalah berkaitan dengan rekod sumber masa. Rekod ini menentukan aplikasi mana yang harus memproses entri masa dan bagaimana.

Penyertaan masa sentiasa satu blok masa bersama dengan permulaan, akhir, dan tempoh yang berkaitan.

Logik akan secara automatik mengemas kini rekod kemasukan dalam situasi berikut:

- Jika dua daripada tiga medan berikut disediakan, medan ketiga dikira secara automatik: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Medan **msdyn_start** dan **msdyn_end** adalah zon waktu yang sedar.
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

1. Tambah medan tersuai pada **kotak dialog Cipta cepat**.
2. Konfigurasikan grid untuk menunjukkan medan tersuai.
3. Tambah medan tersuai pada **halaman edit** **baris atau** Masa edit entri, mengikut kesesuaian.

Pastikan medan baru mempunyai pengesahan yang diperlukan pada **halaman edit** **baris atau** Entri masa. Sebagai sebahagian daripada tugas ini, kunci medan, berdasarkan status entri masa.

Apabila anda menambah medan tersuai pada **grid entri** Masa dan kemudian mencipta entri masa secara langsung dalam grid, medan tersuai untuk entri tersebut disetkan secara automatik supaya ia sepadan dengan baris. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Tambah medan tersuai pada kotak dialog Cipta cepat
Tambah medan tersuai pada **kotak dialog Cipta Cepat: Cipta Entri Masa**. Pengguna kemudian boleh memasukkan nilai apabila mereka menambahkan penyertaan masa dengan memilih **Baharu**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurasikan grid untuk menunjukkan medan tersuai
Terdapat dua cara menambah medan tersuai pada **grid entri** masa Mingguan.

- **Sesuaikan pandangan Penyertaan** Masa Mingguan Saya dan tambahkan medan tersuai padanya. Anda boleh menentukan kedudukan dan saiz medan tersuai dalam grid dengan mengedit sifat dalam paparan.
- Cipta pandangan entri masa tersuai baru dan setkannya sebagai pandangan lalai. Pandangan ini harus mengandungi **medan Perihalan** dan **Komen** luaran sebagai tambahan kepada lajur yang anda ingin sertakan grid. Anda boleh menentukan kedudukan, saiz dan tertib isihan lalai grid dengan mengedit sifat dalam paparan. Seterusnya, konfigurasikan kawalan tersuai untuk pandangan ini supaya ia adalah kawalan **Grid Entri Masa**. Tambah kawalan pada pandangan dan pilihnya untuk **Web**, **Telefon** dan **Tablet**. Seterusnya, konfigurasikan parameter untuk **grid kemasukan** masa Mingguan. **Tetapkan medan Tarikh** mula kepada **tarikh\_ msdyn**, tetapkan **medan Tempoh** kepada **tempoh\_ msdyn** dan tetapkan **medan Status** kepada **msdyn\_ entrystatus**. Medan **Senarai** Status Baca sahaja disetkan kepada **192350002 (Diluluskan)**, **192350003 (Dihantar)**, atau **192350004 (Ingat Diminta)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Tambah medan tersuai pada halaman edit yang sesuai
Halaman yang digunakan untuk mengedit entri masa atau baris entri masa boleh didapati di bawah **Borang**. Butang **Edit entri** dalam grid membuka **halaman entri** Edit, dan **butang Edit baris baris** membuka **halaman edit** Baris. Anda boleh mengedit halaman ini supaya ia termasuk medan tersuai.

Kedua-dua opsyen mengalih keluar beberapa penapisan di luar kotak pada **entiti Project** dan **Project Task**, supaya semua pandangan carian untuk entiti kelihatan. Keluar dari kotak, hanya pandangan carian yang berkaitan boleh dilihat.

Anda mesti menentukan halaman yang sesuai untuk medan tersuai. Kemungkinan besar, jika anda menambah medan pada grid, ia harus pergi pada halaman edit **Baris yang digunakan untuk medan yang digunakan pada** keseluruhan baris entri masa. Jika medan tersuai mempunyai nilai unik dalam baris setiap hari (contohnya, jika ia adalah medan tersuai untuk masa tamat), ia harus pergi pada **halaman Edit** entri masa.

Untuk menambah medan tersuai pada halaman, seret **elemen Medan** ke dalam kedudukan yang sesuai pada halaman, kemudian setkan sifatnya.

### <a name="add-new-option-set-values"></a>Tambah nilai set pilihan baharu
Untuk menambah nilai set pilihan pada medan luar kotak, ikuti langkah ini.

1. Buka halaman pengeditan untuk medan, kemudian, di bawah **Jenis**, pilih **Edit** di sebelah set pilihan.
2. Tambah pilihan baharu yang mempunyai label tersuai dan warna. Jika anda ingin menambah status entri masa baru, medan luar kotak dinamakan **Status** Kemasukan.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Tetapkan status kemasukan masa baharu sebagai baca sahaja
Untuk memilih status entri masa baharu sebagai baca sahaja, tambah nilai masukan masa baharu ke sifat senarai **Senarai Status Baca Sahaja** sahaja. Pastikan anda menambah nombor, bukan label. Bahagian yang boleh diedit bagi grid masukan masa kini akan dikunci untuk baris yang mempunyai status baru. Untuk mengesetkan **sifat Senarai** Status Baca Sahaja secara berbeza untuk pandangan Entri Masa yang **berbeza**, tambah **grid entri** Masa dalam seksyen kawalan **Tersuai pandangan** dan konfigurasikan parameter yang sesuai.

Seterusnya, tambahkan peraturan perniagaan untuk mengunci semua medan pada **halaman edit baris** dan **Entri masa.** Untuk mengakses peraturan perniagaan bagi halaman ini, buka editor borang bagi setiap halaman, kemudian pilih **Peraturan perniagaan**. Anda boleh menambahkan status baharu pada keadaan dalam peraturan perniagaan sedia ada atau anda boleh menambah peraturan perniagaan baharu untuk status baharu.

### <a name="add-custom-validation-rules"></a>Tambah peraturan pengesahan tersuai
Anda boleh menambah dua jenis peraturan pengesahan untuk **pengalaman grid kemasukan** masa Mingguan:

- Peraturan perniagaan bahagian pelanggan yang berfungsi pada halaman
- Pengesahan pemalam bahagian pelayan yang digunakan pada semua kemas kini masukan masa

#### <a name="client-side-business-rules"></a>Peraturan perniagaan sebelah pelanggan
Gunakan peraturan perniagaan untuk mengunci dan membuka kunci medan, masukkan nilai lalai dalam medan dan takrifkan pengesahan yang memerlukan maklumat hanya dari rekod kemasukan masa semasa. Untuk mengakses peraturan perniagaan bagi halaman, buka editor borang, kemudian pilih **Peraturan perniagaan**. Anda kemudian boleh mengedit peraturan perniagaan sedia ada atau menambah peraturan perniagaan baharu.

#### <a name="server-side-plug-in-validations"></a>Pengesahihan pemalam bahagian pelayan
Anda harus menggunakan pengesahihan pemalam untuk sebarang pengesahan yang memerlukan lebih banyak konteks daripada yang tersedia dalam rekod entri sekali sahaja. Anda juga harus menggunakannya untuk sebarang pengesahan yang anda ingin jalankan pada kemas kini sebaris dalam grid. Untuk melengkapkan pengesahihan, cipta pemalam tersuai pada **entiti Kemasukan** Masa.

### <a name="limits"></a>Had
Pada masa ini, **grid entri** Masa mempunyai had saiz 500 baris. Jika terdapat lebih daripada 500 baris, baris yang berlebihan tidak akan dipaparkan. Tidak ada cara untuk meningkatkan had saiz ini.

### <a name="copying-time-entries"></a>Menyalin entri masa
Gunakan pandangan **Salin Lajur Entri Masa** untuk mentakrifkan senarai medan untuk disalin semasa entri masa. **Tarikh** dan **Tempoh** adalah medan yang diperlukan dan tidak boleh dialih keluar daripada pandangan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
