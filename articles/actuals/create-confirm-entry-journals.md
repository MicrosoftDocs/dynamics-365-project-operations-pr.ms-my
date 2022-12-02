---
title: Cipta dan sahkan jurnal Entri
description: Artikel ini menyediakan maklumat tentang cara mencipta dan mengesahkan jurnal Entri dalam Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 138dccd72607d6515eeeffb066fa485f83eabbec
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912343"
---
# <a name="create-and-confirm-entry-journals"></a>Cipta dan sahkan jurnal Entri

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Anda menggunakan Jurnal entri untuk merekod aktual secara langsung dalam Microsoft Dynamics 365 Project Operations. Apabila anda menggunakan Jurnal entri, anda tidak perlu memasukkan Masa, Perbelanjaan dan log kegunaan Bahan dalam Project Operations.

Satu Jurnal entri membolehkan anda mencipta berbilang garisan jurnal. Apabila jurnal itu disahkan, garisan Jurnal entri merekodkan aktual untuk butiran berikut:

- Kos atau hasil, bergantung pada jenis transaksi yang dipilih.
- Kelas transaksi yang dipilih. Kelas yang tersedia ialah **Masa**, **Perbelanjaan**, **Bahan**, **Retainer**, **Pencapaian** dan **Cukai**.
- Projek dan/atau tugas yang dipilih pada garisan jurnal.

Ikut langkah ini untuk mencipta Jurnal entri dalam Project Operations.

1. Pergi ke **Jualan** \> **Transaksi** \> **Jurnal**.
2. Pada halaman senarai **Jurnal entri**, pada Anak Tetingkap Tindakan, pilih **Baharu** untuk mencipta jurnal.
3. Pada halaman **Jurnal baharu**, dalam medan **Perihalan**, masukkan perihalan jurnal.
4. Pastikan medan **Jenis jurnal** ditetapkan kepada **Entri** dan kemudian pilih **Simpan**. Selepas Jurnal entri baharu disimpan, tab **Garisan jurnal** seharusnya muncul pada halaman jurnal.
5. Pada tab **Garisan jurnal**, pada nar alat di atas grid, pilih **Baharu** untuk mencipta garisan Jurnal entri.
6. Dalam dialog **Cipta pantas** untuk mencipta garisan Jurnal entri, tetapkan medan seperti yang diterangkan dalam jadual berikut.

    | Medan | Description | Kesan kefungsian |
    | --- | --- | --- |
    | Kelas Transaksi | Garisan jurnal boleh diklasifikasikan dalam salah satu daripada enam kelas transaksi: **Masa**, **Perbelanjaan**, **Bahan**, **Retainer**, **Pencapaian** atau **Cukai**. | Kelas transaksi **Cukai** telah ditamatkan dalam Project Operations. <br> Jika anda mencipta kelas transaksi **Cukai**, ia tidak akan diproses oleh penginvoisan atau pengiraan kos atau hasil. **Pencapaian** ialah kelas transaksi hasil sahaja. <br>Kelas transaksi **Retainer** mewakili pendahuluan yang diterima daripada pelanggan. Ia harus sentiasa dicipta sebagai sepasang garisan jurnal jualan dibilkan dan belum dibilkan. |
    | Jenis Transaksi | Jenis transaksi **Kos**, **Jualan Antara Organisasi** dan **Kos unit persumberan** harus digunakan untuk merekodkan kos.<br> Jenis transaksi **Jualan Belum Dibilkan** dan **Jualan Dibilkan** dibilkan harus digunakan untuk merekodkan hasil. | Kelas transaksi **Retainer** hanya berfungsi dengan **Jualan Belum Dibilkan** dan **Jualan Dibilkan**.<br> Kelas transaksi **Pencapaian** hanya berfungsi dengan jenis transaksi **Jualan Dibilkan**. <br>Jenis transaksi **Jualan Antara Organisasi** dan **Kos unti persumberan** hanya diguna pakai untuk kelas transaksi **Masa** dan ini hanya tersedia pada Jurnal entri dalam senario Pelaksanaan ringan dan tidak semasa melaksanakan Project Operations dalam senario Sumber/Bukan stok. |
    | Pilih Produk | Apabila kelas transaksi **Bahan** dipilih, medan ini membolehkan anda menentukan sama ada transaksi bahan yang anda ciptakan garisan jurnal untuknya ialah produk sedia ada atau produk masukan manual. | Jika anda memilih **Produk masukan manual**, anda boleh memasukkan nama untuk produk. |
    | Produk | Rujukan kepada produk daripada katalog. | |
    | Description | Perihalan garisan jurnal untuk membantu menjadikan ia mudah untuk dikenal pasti. | Untuk garisan jurnal jualan belum dibilkan, nilai akan digunakan sebagai perihalan apabila butiran baris invois dicipta. |
    | Perihalan luaran | Perihalan garisan jurnal yang boleh digunakan untuk perkongsian dengan pihak pemegang amanah. | Untuk garisan jurnal jualan belum dibilkan, nilai akan digunakan sebagai perihalan luaran apabila butiran baris invois dicipta. Ia juga boleh muncul pada invois yang dihantar kepada pelanggan. |
    | Jenis Pengebilan | Nilai yang menunjukkan sama ada garisan jurnal akan dikira sebagai komponen boleh dituntut, percuma atau tidak boleh dituntut pada projek. | Dalam aliran biasa, jenis pengebilan diperolehi daripada terma dipersetujui yang ditetapkan pada kontrak. Walau bagaimanapun, apabila anda merekodkan garisan jurnal, anda boleh memasukkan nilai dalam medan ini. |
    | Tarikh dokumen | Gunakan tarikh transaksi berlaku. | |
    | Tarikh Mula | Gunakan tarikh transaksi berlaku. | Medan ini digunakan untuk perbandingan dengan tarikh penciptaan invois untuk transaksi jenis **Jualan Belum Dibilkan**. Perbandingan ini akan membantu anda membuat keputusan sama ada transaksi tersebut adalah bertarikh masa depan atau bertarikh masa lalu. Hanya transaksi bertarikh masa lalu akan ditambahkan pada invois. |
    | Tarikh Tamat | Gunakan tarikh transaksi berlaku. | |
    | Tarikh Perakaunan | Gunakan tarikh kesan perakaunan akan direkodkan. | |
    | Pelanggan baris kontrak | Secara lalai, jika baris kontrak hanya mempunyai satu pelanggan, medan ini ditetapkan kepada pelanggan pada baris kontrak apabila garisan jurnal disimpan. Jika garisan kontrak mempunyai berbilang pelanggan, pilih pelanggan yang betul pada garisan kontrak. | Jika sistem tidak boleh menentukan pelanggan baris kontrak pada garisan jurnal dan jika ia kosong pada aktual jenis **Jualan Belum Dibilkan** yang dicipta daripada garisan jurnal, aktual tidak akan diinvoiskan. |
    | Project | Pilih projek untuk merekod aktual. | Berdasarkan projek yang dipilih, kelas transaksi dan tugas, sistem akan cuba untuk menentukan kontrak, baris kontrak dan pelanggan baris kontrak. |
    | Tugas | Pilih tugas untuk merekod aktual. | Jika anda mengaitkan tugas dengan baris kontrak semasa persediaan kontrak, sistem akan menggunakan tugas yang dipilih, bersama dengan projek dan kelas transaksi, untuk menentukan kontrak, baris kontrak dan pelanggan baris kontrak. |
    | Kategori Transaksi | Pilih kategori transaksi untuk merekod aktual. | Untuk perbelanjaan, kategori transaksi yang dipilih menentukan harga lalai yang akan dimasukkan pada garisan jurnal apabila ia disimpan. |
    | Peranan | Medan ini berkaitan dengan garisan jurnal Masa. Pilih peranan sumber yang meluangkan masa pada projek dan/atau tugas. | Untuk garisan jurnal Masa, jika anda menggunakan konfigurasi di luar kotak untuk entri kos sumber lalai dan kadar bil, peranan yang dipilih digunakan bersama dengan unit persumberan untuk menentukan harga lalai yang akan dimasukkan ke dalam garisan jurnal apabila ia disimpan. Jika anda menggunakan konfigurasi tersuai untuk entri harga lalai, anda perlu menyemak konfigurasi untuk menentukan sama ada medan **Peranan** digunakan untuk memasukkan nilai harga lalai. |
    | Subkontrak | Jika garisan jurnal mewakili kapasiti subkontrak, atau perbelanjaan atau bahan subkontrak, pilih subkontrak yang berkaitan. | Apabila garisan jurnal Kos direkodkan, subkontrak yang dipilih akan menentukan senarai harga yang digunakan untuk memasukkan kos unit lalai. |
    | Baris subkontrak | Jika garisan jurnal mewakili kapasiti subkontrak, atau perbelanjaan atau bahan subkontrak, pilih baris subkontrak yang berkaitan. | Apabila baris jurnal Kos direkodkan, barisan subkontrak yang dipilih akan memastikan bahawa pengiraan kapasiti yang tersedia pada baris subkontrak dikira dengan betul. |
    | Kaedah Amaun | Medan ini ditetapkan kepada **Darab Kuantiti Dengan Harga** secara lalai. Apabila kaedah ini digunakan, amaun tersebut akan dikira sebagai *Kuantiti* × *Harga*. Kaedah lain yang disokong ialah **Harga Tetap**. Apabila kaedah ini digunakan, harga akan ditetapkan kepada amaun dan kuantiti tidak akan digunakan dalam pengiraan. | |
    | Jadual Unit dan Unit | Bersama-sama, jadual unit dan unit mengenal pasti unit kuantiti. | Gabungan unit dan kategori transaksi digunakan untuk memasukkan harga lalai untuk perbelanjaan. Dalam konfigurasi lalai bagi Project Operations, kombinasi unit, peranan dan unit persumberan digunakan untuk memasukkan harga lalai untuk masa. Jika anda mempunyai konfigurasi tersuai untuk entri harga lalai, ia akan digunakan bersama dengan unit tersebut. Kombinasi produk dan unit digunakan untuk memasukkan harga lalai untuk bahan. |
    | Kuantiti | Masukkan kuantiti. | |
    | Harga | Jika harga dibiarkan kosong apabila garisan jurnal dicipta, nilai yang berkaitan akan digunakan untuk memasukkan harga lalai, bergantung pada kelas transaksi. Jika harga dimasukkan apabila garisan jurnal dicipta, harga tersebut akan digunakan. | |
    | Cukai | Masukkan apa-apa amaun cukai. | Bergantung pada amaun cukai yang dimasukkan, amaun dilanjutkan akan dikira sebagai *Amaun* + *Cukai*. |

## <a name="confirm-an-entry-journal"></a>Sahkan Jurnal entri

Selepas anda memasukkan semua garisan jurnal dalam Jurnal entri, anda boleh mengesahkan jurnal. Proses ini akan merekodkan setiap garisan jurnal sebagai aktual pada projek yang sesuai.

Selepas jurnal disahkan, anda tidak boleh lagi mengedit jurnal atau mana-mana garisannya.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Aktual yang dicipta mengikut pengesahan Jurnal entri

Terdapat beberapa perbezaan utama antara aktual yang dicipta oleh pengesahan Jurnal entri dan aktual yang dicipta semasa kelulusan Masa, Perbelanjaan dan log penggunaan Bahan serta pengesahan invois dalam Project Operations:

- Jurnal entri tidak menggunakan sambungan transaksi untuk memautkan aktual kos kepada aktual jualan belum dibilkan. Aktual yang dicipta apabila Masa, Perbelanjaan dan log penggunaan Bahan diluluskan sentiasa menggunakan sambungan transaksi untuk memautkan kos dan aktual jualan belum dibilkan.
- Jurnal entri tidak menggunakan asal transaksi untuk memautkan aktual kos dan aktual jualan belum dibilkan kepada mana-mana rekod asal. Aktual yang dicipta apabila Masa, Perbelanjaan dan log penggunaan Bahan diluluskan sentiasa menggunakan asal transaksi untuk memautkan kos dan aktual jualan belum dibilkan kepada entri masa asal.
- Apabila aktual jualan belum dibilkan yang dicipta oleh pengesahan Jurnal entri diinvoiskan, aktual jualan dibilkan yang dicipta semasa pengesahan invois dipautkan kepada aktual jualan belum dibilkan, dengan cara yang sama dengan aktual jualan belum dibilkan yang dicipta apabila Masa, Perbelanjaan dan log penggunaan Bahan diluluskan.
- Garisan Jurnal entri yang dicipta untuk masa yang dimasukkan oleh sumber antara organisasi tidak menyebabkan aktual daripada jenis **Kos unit persumberan** dan **Jualan Antara Interorganisasi** dicipta secara automatik. Aktual ini mesti dicipta secara manual. Tingkah laku ini berbeza daripada tingkah laku untuk entri masa yang direkodkan oleh sumber antara organisasi. Dalam kes tersebut, apabila masa diluluskan, aplikasi secara automatik mencipta aktual daripada jenis **Kos** pada projek dan aktual jenis **Kos unit persumberan** dan **Jualan Antara Organisasi** pada divisyen pemilikan pekerja. Ia kemudian menggunakan sambungan transaksi untuk memautkan aktual tersebut bersama dan asal transaksi untuk memautkan aktual kepada entri masa asal.
- Apabila Jurnal entri disahkan, ia mencipta aktual. Walau bagaimanapun, Jurnal pembetulan tidak boleh digunakan untuk membetulkan aktual tersebut. Tingkah laku ini berbeza daripada tingkah laku untuk aktual yang dicipta apabila Masa, Perbelanjaan dan log penggunaan Bahan diluluskan. Dalam kes tersebut, aplikasi ini membolehkan anda menggunakan Jurnal pembetulan untuk membetulkan aktual bagi membetulkan apa-apa ralat, dengan syarat aktual belum diinvoiskan. Jika aktual sudah diinvoiskan, anda masih boleh membetulkan aktual jika anda memproses kredit penuh aktual tersebut kepada pelanggan.

> [!NOTE]
> Jurnal entri tidak menguatkuasakan peraturan penetapan nilai lalai yang ketat. Oleh itu, gunakan Jurnal Entri ini sekurang mungkin dan berwaspada serta berhati-hati untuk memastikan bahawa anda tidak mencipta data kewangan yang rosak dalam sistem anda. Bila-bila masa anda boleh, gunakan persediaan Masa, Perbelanjaan dan log penggunaan Bahan, pencapaian dan retainer pada kontrak projek dan proses pengesahan invois projek dan bukannya Jurnal entri untuk mencipta aktual.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
