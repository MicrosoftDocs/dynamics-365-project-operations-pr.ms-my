---
title: Sesuaikan kemasukan masa mingguan
description: Topik ini memberikan maklumat mengenai cara untuk melaksanakan peraturan perniagaan tersuai yang menyokong amalan organisasi.
author: stsporen
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 3c4a508f2a67f87302f8b81640d2031fd5d2627b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127934"
---
# <a name="customize-weekly-time-entry"></a>Sesuaikan kemasukan masa mingguan 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dalam Microsoft Dynamics 365 Project Service Automation versi 3.3, Microsoft memperkenalkan grid moden yang membolehkan sumber projek dengan pantas memasuki masa sehingga seminggu pada satu masa. Grid kemasukan masa mingguan baharu boleh menunjukkan jumlah untuk penyertaan mengikut tarikh, mengikut baris atau mengikut minggu. Sumber boleh membuat salinan masa penyertaan dalam minggu dan juga salinan besar dari minggu sebelumnya. Penyesuai sistem boleh menyesuaikan pandangan dengan menambah medan, menambah carian ke entiti lain dan melaksanakan peraturan perniagaan tersuai untuk menyokong amalan organisasi mereka.

Entri masa dan grid masa mingguan baharu dicapai melalui peta tapak. Pengalaman kemasukan tersuai tidak boleh diperluas yang merupakan sebahagian daripada versi PSA awal telah digantikan oleh grid kemasukan masa mingguan yang boleh diperluas, dan juga oleh pengalaman alternatif dalam grid baca sahaja dan kalendar. Oleh kerana perubahan ini, pengguna boleh memasukkan masa dalam jumlah mingguan.

## <a name="page-layout"></a>Tataletak halaman
Grid masuk masa mingguan baharu adalah kawalan tersuai yang mempunyai bar alat dan dua bahagian utama **Dimensi** dan **Tempoh.** Bar alat termasuk butang yang digunakan hanya untuk kawalan tersuai ini untuk grid kemasukan masa. Sebaliknya, butang pada tetingkap tindakan di bahagian atas halaman diguna pakai pada tiga jenis kawalan yang disokong untuk masukan masa: kawalan kemasukan masa mingguan, kawalan baca sahaja, dan kawalan kalendar.

### <a name="dimensions"></a>Dimensi
Bahagian **Dimensi** menunjukkan, sebagai tajuk lajur, semua dimensi masa boleh masuki. Dimensi berikut disokong di luar kotak:

- Projek
- Tugas Projek
- Peranan
- Taip
- Status Entri

Bahagian **Dimensi** tidak membenarkan pengeditan sebaris. Bahagian ini disokong oleh pandangan yang mendayakan medan tersuai untuk ditambah ke grid kemasukan masa mingguan. Untuk maklumat mengenai cara untuk menambah medan tersuai, lihat bahagian "Kebolehsuian" kemudian dalam topik ini.

### <a name="duration"></a>Tempoh
Bahagian Tempoh menunjukkan hari minggu sebagai pengepala lajur. Bahagian ini membenarkan pengeditan dalam baris. Selepas baris entri masa ialah dicipta yang mempunyai dimensi yang sesuai, pengguna boleh memasukkan dengan cepat, mengikut baris, jumlah masa yang mereka belanjakan pada dimensi tersebut.

## <a name="create-a-new-time-entry"></a>Cipta entri masa baharu
Untuk mencipta entri masa baharu dalam grid kemasukan masa, pilih **Baharu.** Kotak dialog **Cipta Pantas Entri Masa** akan muncul. Dalam kotak dialog pengguna boleh memilih tarikh kemasukan masa dan kemudian memasukkan data untuk **Projek**, **Tugas Projek**, dan, **Peranan** dan **Tempoh** dalam minit, jam atau hari dengan menaip **h**, **m** atau **d** bersama dengan nombor. Pengguna juga boleh memasukkan perihalan dan komen yang boleh dikongsi secara luaran untuk masa kemasukan. Apabila pengguna menyimpan perubahan mereka, nilai yang telah mereka masukkan terhadap dimensi muncul dalam bahagian **Dimensi**. Tempoh maklumat yang mereka masukkan dalam medan **Tempoh** muncul pada tarikh kemasukan telah dicipta.

Medan carian disokong oleh pandangan sistem. Sebagai contoh, selepas pengguna memasuki projek, medan **Tugas Projek** ditetapkan kepada pandangan **Salinan** secara lalai. Bagi mencipta entri masa untuk tugas yang tidak ditugaskan kepada pengguna, pilih **Ubah pandangan** pada kotak dialog carian dan kemudian pilih pandangan **Semua Tugas Projek Aktif**.

## <a name="edit-a-time-entry"></a>Edit entri masa
Butiran daripada beberapa medan pada halaman entri masa, seperti **Perihalan** dan **Komen Luaran** tidak ditunjukkan dalam grid entri masa mingguan. Sebaliknya, penunjuk segi tiga yang kecil muncul dalam sel tempoh yang mempunyai butiran tambahan ini. Pilih sel dan kemudian pilih **Edit butiran** untuk melihat data dalam anak tetingkap **Edit Pantas**. Untuk mengedit atau mengemas kini butiran untuk masukan masa tertentu yang bukan sebahagian daripada grid kemasukan masa mingguan, pengguna mesti membuka anak tetingkap **Edit Pantas**.

## <a name="copy-a-time-entry-row"></a>Salin baris entri masa
Selepas baris entri masa pertama telah dicipta, pengguna boleh memilih **Salin Baris** untuk menyalin keseluruhan baris ke baris baharu. Apabila baris disalin dengan cara ini, dimensi dan tempoh juga disalin. Pengguna juga boleh memilih **Edit baris** untuk mengemas kini nilai dimensi dan talian tempoh dalam bahagian **Tempoh**.

## <a name="open-a-time-entry"></a>Buka entri masa
Untuk menyokong entri yang optimum dan pantas dalam medan paling terkemuka, grid kemasukan masa mingguan menunjukkan subset dimensi yang dipilih dan tempoh masa. Untuk melihat semua butiran kemasukan satu masa, di bawah **Edit Entri**, pilih **Buka.**

## <a name="submit-a-time-entry"></a>Serahkan entri masa
Pengguna boleh menyerahkan satu kali entri atau kumpulan penyertaan masa dengan memilih satu blok sel atau baris entri keseluruhan masa dan kemudian memilih **Serahkan**. Penyertaan masa yang dihantar akan muncul sebagai entri yang menunggu kelulusan pada halaman **Kelulusan**. Selepas penyertaan masa berjaya diserahkan, ia tidak boleh diedit.

## <a name="recall-a-time-entry"></a>Tarik balik entri masa
Anda boleh mengingati entri masa yang telah anda serahkan. Anda boleh mengingati kemasukan satu kali, blok baris masa atau keseluruhan entri masa. Ingat entri masa yang sedia untuk sumber untuk diedit.

## <a name="time-entry-status"></a>Status entri masa
Entri masa baharu ditugaskan status **Draf** secara automatik. Apabila kemasukan telah diserahkan, status dikemas kini kepada **Diserahkan**. Apabila entri masa diserahkan telah diluluskan, status dikemas kini kepada **Diluluskan**. Jika kemasukan masa ditolak, status dikemas kini untuk **Dikembalikan** dan kemasukan menjadi tersedia untuk pembetulan dan diserahkan semula. Hanya entri masa yang mempunyai status **Draf** boleh dipadamkan.

## <a name="view-rejection-comments"></a>Lihat komen penolakan
Apabila kemasukan masa telah ditolak oleh pelulus, pelulus mungkin menambah komen penolakan untuk membantu sumber memahami sebab penolakan. Untuk melihat komen penolakan untuk kemasukan masa, pilih **Buka entri.** Komen penolakan akan ditunjukkan dalam garis masa. Pada masa itu, sumber boleh bertindak balas kepada komen penolakan sebelum dia menyerahkan semula entri.

## <a name="copy-week"></a>Salin minggu
Selepas beberapa kali entri telah dicipta, pengguna boleh memilih **Salin Masa** untuk mencipta entri masa tambahan secara pukal. Kotak dialog **Salin** muncul. Dalam bahagian **Dari Tempoh** gunakan medan **Tarikh Mula** dan **Tarikh Akhir** untuk menentukan julat tarikh untuk menyalin entri masa. Dalam bahagian **Ke Tempoh** dalam medan **Tarikh Mula** tentukan tarikh untuk mencipta entri masa. Kemudian pilih **Salin**. Untuk tarikh yang ditetapkan dalam tempoh "kepada", salinan masa penyertaan untuk hari yang sama dalam minggu dalam tempoh "dari" dicipta. Sebagai contoh, entri masa untuk Isnin dari minggu lepas disalin ke hari Isnin minggu yang ditetapkan sebagai tempoh "kepada".

## <a name="import"></a>Import
Proses asas yang sama digunakan untuk mengimport daripada tempahan, tugas dan pertukaran. Pengguna boleh menentukan julat tarikh bagi tempahan yang diimport. Mereka mesti memilih tempahan secara jelas yang harus disalin ke dalam entri masa draf. Dalam keluaran sebelumnya, entri masa yang dicadangkan muncul dalam grid dan kalendar, dan telah hilang apabila sesi itu disegar semula.

## <a name="extensibility"></a>Dapat diperluas
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Tambah medan tersuai yang mempunyai carian ke entiti lain
Terdapat tiga langkah utama untuk menambah medan tersuai ke grid kemasukan masa mingguan.

1.  Tambah medan tersuai ke kotak dialog cipta pantas.
2.  Konfigurasikan grid untuk menunjukkan medan tersuai.
3.  Tambah medan tersuai kepada sama ada baris edit aliran tugas atau sel edit aliran tugas, mengikut kesesuaian.

Anda juga mesti memastikan bahawa medan baharu mempunyai pengesahan yang diperlukan dalam baris atau edit aliran tugas. Sebagai sebahagian daripada langkah ini, anda mesti mengunci medan, berdasarkan status entri masa.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Tambah medan tersuai ke kotak dialog cipta pantas
Anda mesti menambah medan tersuai kepada kotak dialog Cipta Pantas Entri Masa. supaya pengguna boleh memasukkan nilai untuknya apabila mereka menambahkan penyertaan masa dengan menggunakan butang **Baharu**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurasikan grid untuk menunjukkan medan tersuai
Terdapat dua langkah utama untuk menambah medan tersuai ke grid kemasukan masa mingguan. Pilihan pertama ialah sesuaikan pandangan **Entri Masa Mingguan Saya** dan tambah medan tersuai kepadanya. Anda boleh memilih kedudukan dan saiz medan tersuai dalam grid dengan mengedit sifat tersebut dalam pandangan.

Pilihan kedua ialah cipta pandangan entri masa tersuai baharu dan setkan sebagai pandangan lalai. Pandangan ini harus mengandungi **Perihalan** dan **Komen Luaran**, sebagai tambahan kepada lajur yang anda mahu ada dalam grid. Anda boleh memilih kedudukan, saiz dan isih pesanan lalai grid dengan mengedit sifat tersebut dalam pandangan. Seterusnya, konfigurasikan kawalan tersuai untuk pandangan ini supaya ia adalah kawalan **Grid Entri Masa**. Tambah kawalan ini ke pandangan, dan pilih ia untuk web, telefon dan tablet. Seterusnya, konfigurasikan parameter untuk grid entri masa mingguan. Tetapkan medan **Tarikh Mula** ke **msdyn_date**, tetapkan medan **Tempoh** untuk **msdyn_duration** dan tetapkan medan **Status** kepada **msdyn_entrystatus**. Untuk pandangan lalai, medan **Senarai Status Baca Sahaja** ditetapkan kepada **192350002, 192350003, 192350004**, medan **Baris Edit Aliran Tugas** ditetapkan kepada **msdyn_timeentryrowedit** dan **Sel Edit Aliran Tugas** ditetapkan kepada **msdyn_timeentryedit.** Anda boleh menyesuaikan medan ini untuk menambah atau mengeluarkan status baca sahaja atau untuk menggunakan pengalaman berasaskan tugas berbeza (TBX) untuk pengeditan baris atau sel. Medan ini sepatutnya terikat dengan nilai statik.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Tambah medan tersuai kepada edit aliran tugas yang sesuai
Laman TBX yang digunakan untuk mengedit boleh didapati di bawah **Proses**. Halaman lalai adalah **Project Service-Edit Baris Entri Masa** dan **Project Service-Edit Entri Masa**. Anda boleh sama ada mengedit halaman lalai ini atau mencipta halaman TBX tersuai yang baharu.

> [!NOTE] 
> Kedua-dua pilihan akan mengeluarkan beberapa penapisan keluar kotak **Projek** dan entiti **Tugas Projek** supaya semua pandangan carian untuk entiti akan boleh dilihat. Keluar dari kotak, hanya pandangan carian yang berkaitan boleh dilihat.

Anda mesti menentukan aliran tugas yang sesuai untuk medan tersuai. Kemungkinan besar, jika anda menambah medan ke grid, ia perlu pergi dalam baris edit aliran tugas yang digunakan untuk medan yang diguna pakai pada seluruh baris entri masa. Jika medan tersuai mempunyai nilai unik setiap hari, seperti medan tersuai untuk **Masa akhir**, ia harus pergi dalam edit aliran tugas sel.

Untuk menambah medan tersuai kepada aliran tugas, seret elemen **Medan** ke kedudukan yang sesuai pada halaman dan kemudian tetapkan sifatnya. Tetapkan sifat **Sumber** ke **Entri Masa** dan set sifat **Medan Data** ke medan tersuai. Sifat **Medan** menentukan nama paparan pada halaman TBX. Pilih **Gunakan** untuk menyimpan perubahan ke medan. Kemudia pilih **Kemas Kini** untuk menyimpan perubahan ke halaman.

Untuk menggunakan halaman TBX tersuai baharu sebagai ganti, cipta proses baharu. Tetapkan kategori untuk **Aliran Proses Perniagaan**, tetapkan entiti ke **Entri Masa** dan tetapkan jenis proses perniagaan untuk **Menjalankan proses sebagai aliran tugas**. Di bawah **Sifat**, sifat **Nama halaman** patut ditetapkan ke nama paparan untuk halaman. Tambah semua medan yang berkaitan dengan halaman TBX. Simpan dan aktifkan proses, dan kemudian kemas kini sifat kawalan tersuai untuk aliran tugas yang relevan kepada nilai **Nama** pada proses.

### <a name="add-new-option-set-values"></a>Tambah nilai set pilihan baharu
Untuk menambah nilai set pilihan ke medan luar, buka halaman pengeditan untuk medan dan kemudian, di bawah **Jenis**, pilih **Edit** di sebelah set pilihan. Seterusnya, tambah pilihan baru yang mempunyai label tersuai dan warna. Jika anda mahu menambah status kemasukan masa baharu, medan di luar kotak dinamakan **Status Entri** bukan **Status**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Tetapkan status kemasukan masa baharu sebagai baca sahaja
Untuk memilih status entri masa baharu sebagai baca sahaja, tambah nilai masukan masa baharu (nombor tersebut, bukan label) ke sifat senarai **Senarai Status Baca Sahaja** sahaja. Bahagian yang boleh diedit bagi grid kemasukan masa akan dikunci untuk baris yang mempunyai status baharu.
Seterusnya, tambah peraturan perniagaan untuk mengunci semua medan **Edit Baris Entri Masa** dan **Edit Entri Masa** halaman TBX. Anda boleh mengakses peraturan perniagaan untuk halaman ini dengan membuka editor aliran proses perniagaan untuk halaman dan kemudian memilih **Peraturan Perniagaan**. Anda boleh menambahkan status baharu pada keadaan dalam peraturan perniagaan sedia ada atau anda boleh menambah peraturan perniagaan baharu untuk status baharu.

### <a name="add-custom-validation-rules"></a>Tambah peraturan pengesahan tersuai
Terdapat dua jenis peraturan pengesahan yang anda boleh tambah untuk pengalaman grid kemasukan masa mingguan: •    Peraturan perniagaan pihak klien yang berfungsi dalam kotak dialog cipta pantas dan pada halaman TBX •   Pengesahan pasang masuk bahagian pelayan yang diguna pakai untuk semua kemas kini kemasukan masa

#### <a name="business-rules"></a>Peraturan perniagaan
Gunakan peraturan perniagaan untuk mengunci dan membuka kunci medan, masukkan nilai lalai dalam medan dan takrifkan pengesahan yang memerlukan maklumat hanya dari rekod kemasukan masa semasa. Anda boleh mengakses peraturan perniagaan untuk halaman TBX dengan membuka editor aliran proses perniagaan untuk halaman dan kemudian memilih **Peraturan Perniagaan**. Anda kemudian boleh mengedit peraturan perniagaan sedia ada atau menambah peraturan perniagaan baharu. Untuk pengesahan yang lebih tersuai malah, anda boleh menggunakan peraturan perniagaan untuk menjalankan JavaScript.

#### <a name="plug-in-validations"></a>Pengesahan pasang masuk
Anda patut menggunakan pengesahan pasang masuk untuk sebarang pengesahan yang memerlukan lebih banyak konteks daripada tersedia dalam rekod kemasukan tunggal atau sebarang pengesahan yang anda mahu jalankan pada kemas kini dalam baris dalam grid. Untuk melengkapkan pengesahan, cipta pasang masuk tersuai pada **Entiti Masa**.

> [!IMPORTANT] 
> Pada masa ini, isu yang diketahui pada halaman TBX menghalang pengguna daripada membetulkan maklumat dan memilih semula Selesai yang dilakukan apabila kemas kini gagal pengesahan pasang masuk. Sebagai penyelesaian, sediakan pengesahan peraturan perniagaan untuk mengelakkan situasi ini sebanyak mungkin.
