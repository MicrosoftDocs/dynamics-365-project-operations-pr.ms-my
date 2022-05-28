---
title: Cipta dan sahkan jurnal Kemasukan
description: Topik ini memberikan maklumat tentang cara membuat dan mengesahkan jurnal Kemasukan dalam Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8cb768337bc197895a837670f93b99b132c97437
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584239"
---
# <a name="create-and-confirm-entry-journals"></a>Cipta dan sahkan jurnal Kemasukan

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Anda menggunakan jurnal Entri untuk merakam sebenar secara langsung dalam Microsoft Dynamics 365 Project Operations. Apabila anda menggunakan jurnal Kemasukan, anda tidak perlu memasukkan log Masa, Perbelanjaan dan Penggunaan Bahan dalam Operasi Projek.

Jurnal Kemasukan tunggal membolehkan anda mencipta berbilang baris jurnal. Apabila jurnal disahkan, baris jurnal Entri merekodkan sebenar untuk butiran berikut:

- Kos atau hasil, bergantung pada jenis transaksi yang dipilih.
- Kelas transaksi yang dipilih. Kelas yang ada ialah **Masa**, **Perbelanjaan**, **Bahan**, **Penahan**, **Milestone**, dan **Cukai**.
- Projek dan/atau tugas yang dipilih pada baris jurnal.

Ikuti langkah ini untuk mencipta jurnal Entri dalam Operasi Projek.

1. Pergi ke **Jurnal** Transaksi \>**Jualan**.\>**·**
2. **Pada halaman Senarai entri jurnal**, pada Anak Tetingkap Tindakan, pilih **Baru** untuk mencipta jurnal.
3. **Pada halaman Jurnal** baru, dalam **medan Perihalan**, masukkan perihalan jurnal.
4. Pastikan medan jenis Jurnal disetkan **kepada** Kemasukan **, kemudian pilih** Simpan **.** Selepas jurnal Entri baru disimpan, **tab Baris** Jurnal akan muncul pada halaman jurnal.
5. **Pada tab Baris** jurnal, pada bar alat di atas grid, pilih **Baru** untuk mencipta baris jurnal Entri.
6. **Dalam kotak dialog Cipta cepat** untuk mencipta baris Jurnal entri, setkan medan seperti yang diterangkan dalam jadual berikut.

    | Medan | Description | Kesan kefungsian |
    | --- | --- | --- |
    | Kelas Transaksi | Baris jurnal boleh dikelaskan kepada salah satu daripada enam kelas transaksi: **Masa**, Perbelanjaan **,** Bahan **,** **Retainer**, **Milestone**, atau **Cukai**. | Kelas **transaksi Cukai** telah ditamatkan dalam Operasi Projek. <br> Jika anda mencipta **kelas transaksi Cukai**, ia tidak akan diproses dengan invois atau dalam pengiraan kos atau hasil. **Milestone** adalah kelas transaksi pendapatan sahaja. <br>Kelas **transaksi Retainer** mewakili pendahuluan yang diterima daripada pelanggan. Ia harus sentiasa dibuat sebagai sepasang jualan yang dibilkan dan barisan jurnal jualan yang tidak dibilkan. |
    | Jenis Transaksi | **Jenis transaksi kos** unit Kos **,** Interorg **, dan** Penyumberan Semula harus digunakan untuk merekodkan kos.<br> Jenis **transaksi Jualan** Tidak Dibilkan dan **Jualan** Dibilkan hendaklah digunakan untuk merekodkan hasil. | Kelas **transaksi Retainer** hanya berfungsi dengan **jenis transaksi Jualan** Tidak Dibilkan dan **Jualan** Dibilkan.<br> Kelas **transaksi Milestone** hanya berfungsi dengan **jenis transaksi Billed Sales**. <br>Jenis **transaksi kos** unit Interorg Sales **and** Resourcing hanya boleh digunakan untuk **kelas transaksi Masa** dan ini hanya boleh didapati di jurnal Kemasukan dalam scneario penggunaan Lite dan bukan semasa menggunakan Operasi Projek dalam senario Sumber / Tidak Berstok. |
    | Pilih Produk | **Apabila kelas transaksi Bahan** dipilih, medan ini membolehkan anda menentukan sama ada transaksi material yang anda cipta baris jurnal ialah produk sedia ada atau produk tulis. | Jika anda memilih **Produk** tulis masuk, anda boleh memasukkan nama untuk produk tersebut. |
    | Produk | Rujukan kepada produk dari katalog. | |
    | Description | Penerangan mengenai baris jurnal untuk membantu memudahkan untuk mengenal pasti. | Untuk baris jurnal jualan yang tidak dibilkan, nilai akan digunakan sebagai perihalan apabila butiran baris invois dibuat. |
    | Penerangan luaran | Penerangan mengenai garis jurnal yang boleh digunakan untuk berkongsi dengan pihak berkepentingan luaran. | Untuk baris jurnal jualan yang tidak dibilkan, nilai akan digunakan sebagai perihalan luaran apabila butiran baris invois dibuat. Ia juga boleh muncul pada invois yang dihantar kepada pelanggan. |
    | Jenis Pengebilan | Nilai yang menunjukkan sama ada baris jurnal akan dikira sebagai komponen yang boleh dikenakan bayaran, percuma, atau tidak boleh dikenakan bayaran pada projek. | Dalam aliran biasa, jenis pengebilan diperolehi daripada terma yang dipersetujui yang ditetapkan pada kontrak. Walau bagaimanapun, apabila anda merakam baris jurnal, anda boleh memasukkan nilai dalam medan ini. |
    | Tarikh dokumen | Gunakan tarikh apabila transaksi berlaku. | |
    | Tarikh Mula | Gunakan tarikh apabila transaksi berlaku. | Medan ini digunakan untuk perbandingan dengan tarikh penciptaan invois untuk transaksi **jenis Jualan** Belum Dibilkan. Perbandingan ini akan membantu anda memutuskan sama ada transaksi itu adalah tarikh masa depan atau tarikh lalu. Hanya transaksi tarikh lalu akan ditambahkan pada invois. |
    | Tarikh Tamat | Gunakan tarikh apabila transaksi berlaku. | |
    | Tarikh Perakaunan | Gunakan tarikh apabila kesan perakaunan akan direkodkan. | |
    | Pelanggan talian kontrak | Secara lalai, jika baris kontrak hanya mempunyai satu pelanggan, medan ini ditetapkan kepada pelanggan pada baris kontrak apabila baris jurnal disimpan. Jika talian kontrak mempunyai berbilang pelanggan, pilih pelanggan yang betul pada baris kontrak. | Jika sistem tidak dapat menentukan pelanggan baris kontrak pada baris jurnal, dan jika ia kosong pada sebenar **jenis Jualan** Tidak Dibilkan yang dicipta daripada baris jurnal, yang sebenar tidak akan diinvois. |
    | Project | Pilih projek untuk merakam yang sebenarnya. | Berdasarkan projek, kelas transaksi, dan tugas yang dipilih, sistem akan cuba menentukan kontrak, garis kontrak, dan pelanggan talian kontrak. |
    | Tugas | Pilih tugas untuk merakam yang sebenar. | Jika anda mengaitkan tugas dengan baris kontrak semasa persediaan kontrak, sistem akan menggunakan tugas yang dipilih, bersama-sama dengan kelas projek dan transaksi, untuk menentukan kontrak, garis kontrak, dan pelanggan talian kontrak. |
    | Kategori Transaksi | Pilih kategori transaksi untuk merakam yang sebenar. | Untuk perbelanjaan, kategori transaksi yang dipilih menentukan harga lalai yang akan dimasukkan pada baris jurnal apabila ia disimpan. |
    | Peranan | Medan ini berkaitan dengan baris jurnal Masa. Pilih peranan sumber yang menghabiskan masa untuk projek dan/atau tugas. | Untuk baris jurnal Time, jika anda menggunakan konfigurasi luar kotak untuk kemasukan kos sumber lalai dan kadar bil, peranan yang dipilih digunakan bersama-sama dengan unit sumber semula untuk menentukan harga lalai yang akan dimasukkan pada baris jurnal apabila ia disimpan. Jika anda menggunakan konfigurasi tersuai untuk kemasukan harga lalai, anda harus menyemak semula konfigurasi tersebut **untuk menentukan sama ada medan Peranan** digunakan untuk memasukkan nilai harga lalai. |
    | Subkontrak | Jika baris jurnal mewakili kapasiti subkontrak, atau perbelanjaan atau bahan subkontrak, pilih subkontrak yang berkaitan. | Apabila baris jurnal Kos direkodkan, subkontrak yang dipilih akan menentukan senarai harga yang digunakan untuk memasukkan kos unit lalai. |
    | Garis subkontrak | Jika baris jurnal mewakili kapasiti subkontrak, atau perbelanjaan atau bahan subkontrak, pilih garis subkontrak yang berkaitan. | Apabila baris jurnal Kos direkodkan, garis subkontrak yang dipilih akan memastikan bahawa pengiraan kapasiti yang tersedia pada baris subkontrak dikira dengan betul. |
    | Kaedah Amaun | Secara lalai, medan ini disetkan kepada **Mendarabkan Kuantiti Mengikut Harga**. Apabila kaedah ini digunakan, amaun akan dikira sebagai *Kuantiti* × *Harga*. Kaedah lain yang disokong ialah **Harga** Tetap. Apabila kaedah ini digunakan, harga akan ditetapkan kepada jumlah, dan kuantiti tidak akan digunakan dalam pengiraan. | |
    | Jadual Unit dan Unit | Bersama-sama, jadual unit dan unit mengenal pasti unit kuantiti. | Gabungan unit dan kategori transaksi digunakan untuk memasukkan harga lalai untuk perbelanjaan. Dalam konfigurasi lalai Operasi Projek, gabungan unit, peranan dan unit sumber semula digunakan untuk memasukkan harga lalai untuk masa. Jika anda mempunyai konfigurasi tersuai untuk kemasukan harga lalai, ia akan digunakan bersama-sama dengan unit. Gabungan produk dan unit digunakan untuk memasukkan harga lalai untuk bahan. |
    | Kuantiti | Masukkan kuantiti. | |
    | Harga | Jika harga dibiarkan kosong apabila baris jurnal dicipta, nilai yang berkaitan akan digunakan untuk memasukkan harga lalai, bergantung pada kelas transaksi. Jika harga dimasukkan apabila baris jurnal dicipta, harga itu akan digunakan. | |
    | Cukai | Masukkan sebarang amaun cukai. | Bergantung kepada jumlah cukai yang dimasukkan, jumlah lanjutan akan dikira sebagai *Jumlah* + *Cukai*. |

## <a name="confirm-an-entry-journal"></a>Sahkan jurnal Kemasukan

Selepas anda memasukkan semua baris jurnal dalam jurnal Entri, anda boleh mengesahkan jurnal. Proses ini akan merekodkan setiap baris jurnal sebagai sebenar pada projek yang sesuai.

Selepas jurnal disahkan, anda tidak lagi boleh mengeditnya atau mana-mana barisnya.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Sebenar yang dicipta oleh pengesahan jurnal Kemasukan

Terdapat beberapa perbezaan utama antara sebenar yang dicipta oleh Pengesahan jurnal kemasukan dan sebenar yang dicipta semasa kelulusan Masa, Perbelanjaan, dan log penggunaan Bahan dan pengesahan invois dalam Operasi Projek:

- Jurnal kemasukan tidak menggunakan sambungan transaksi untuk memautkan kos sebenar kepada sebenar jualan yang belum dibilkan. Sebenar yang dicipta apabila log penggunaan Masa, Perbelanjaan dan Bahan diluluskan sentiasa menggunakan sambungan transaksi untuk memautkan kos dan sebenar jualan yang belum dibilkan.
- Jurnal kemasukan tidak menggunakan asal transaksi untuk memautkan kos sebenar dan sebenar jualan yang tidak dibilkan kepada mana-mana rekod asal. Sebenar yang dicipta apabila log penggunaan Masa, Perbelanjaan dan Bahan diluluskan sentiasa menggunakan asal-usul transaksi untuk menghubungkan kos dan sebenar jualan yang tidak dibilkan kepada entri masa asal.
- Apabila sebenar jualan yang tidak dibilkan yang dicipta oleh pengesahan jurnal kemasukan diinvois, sebenar jualan yang dibilkan yang dicipta semasa pengesahan invois dipautkan kepada aktual jualan yang belum dibilkan, dengan cara yang sama dengan sebenar jualan yang tidak dibilkan yang dicipta apabila log penggunaan Masa, Perbelanjaan dan Bahan diluluskan.
- Baris jurnal kemasukan yang dicipta untuk masa yang dimasukkan oleh sumber antara organisasi tidak menyebabkan sebenar **kos** unit Sumber Semula dan **jenis Jualan** Interorg dicipta secara automatik. Sebenar ini mesti dibuat secara manual. Tingkah laku ini berbeza dari tingkah laku untuk entri masa yang direkodkan oleh sumber antara organisasi. Dalam kes itu, apabila masa diluluskan, aplikasi secara automatik mencipta sebenar **jenis Kos** pada projek dan sebenar **kos** unit Sumber Semula dan **jenis Jualan** Interorg pada bahagian pemilikan pekerja. Ia kemudian menggunakan sambungan transaksi untuk menghubungkan sebenar tersebut bersama-sama dan asal-usul transaksi untuk menghubungkannya ke entri masa asal.
- Apabila jurnal Kemasukan disahkan, mereka mencipta sebenar. Walau bagaimanapun, jurnal Pembetulan tidak boleh digunakan untuk membetulkan sebenar tersebut. Tingkah laku ini berbeza daripada tingkah laku untuk sebenar yang dicipta apabila log penggunaan Masa, Perbelanjaan dan Bahan diluluskan. Sekiranya demikian, aplikasi ini membolehkan anda menggunakan jurnal Pembetulan untuk membetulkan sebenar untuk membetulkan sebarang ralat, dengan syarat bahawa aktual tersebut belum diinvois. Sekiranya mereka telah diinvois, anda masih boleh membetulkan yang sebenarnya jika anda memproses kredit penuh yang sebenarnya kepada pelanggan.

> [!NOTE]
> Jurnal kemasukan tidak menguatkuasakan peraturan lalai yang ketat. Oleh itu, gunakan Jurnal Kemasukan ini sesedikit mungkin, dan berhati-hati dan berhati-hati untuk memastikan bahawa anda tidak membuat data kewangan yang rosak dalam sistem anda. Bila-bila masa anda boleh, gunakan log penggunaan Masa, Perbelanjaan dan Bahan, persediaan tonggak dan penahan pada kontrak projek, dan proses pengesahan invois projek dan bukannya Jurnal kemasukan untuk mencipta sebenar.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
