---
title: Anggarkan gambaran keseluruhan projek
description: Topik ini menyediakan maklumat tentang anggaran dalam Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8e7ee4888a907b9d8c3ce06c1597f6b05be84477
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081117"
---
# <a name="estimate-projects-overview"></a>Anggarkan gambaran keseluruhan projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Pada sebut harga berasaskan projek, anda boleh menggunakan entiti **Butiran baris sebut harga** untuk menganggarkan kerja yang diperlukan bagi menghantar projek. Kemudian, anda boleh berkongsi anggaran tersebut dengan pelanggan.

Baris sebut harga berasaskan projek boleh mempunyai sifar hingga banyak butiran baris sebut harga. Butiran baris sebut harga digunakan untuk menganggarkan masa, perbelanjaan atau yuran. Microsoft Dynamics 365 Project Operations tidak membenarkan anggaran bahan pada butiran baris sebut harga. Ini dipanggil kelas transaksi. Anggaran amaun cukai boleh juga dimasukkan dalam kelas transaksi.

Selain daripada kelas transaksi, butiran baris sebut harga mempunyai jenis transaksi. Dua jenis transaksi disokong untuk butiran baris sebut harga, **Kos** dan **Kontrak Projek**.

## <a name="estimate-by-using-a-contract"></a>Anggaran menggunakan kontrak

Jika anda menggunakan sebut harga apabila anda mencipta kontrak berasaskan projek, anggaran yang anda lakukan untuk setiap baris sebut harga ke atas sebut harga disalin pada kontrak projek. Struktur kontrak projek adalah seperti struktur sebut harga projek yang ada baris, butiran baris, dan jadual invois.

Anggaran boleh dilakukan secara terus dalam kontrak projek seperti dalam sebut harga projek. Untuk sebut harga projek, anggaran dilakukan menggunakan baris kontrak, dan butiran baris kontrak. Butiran baris kontrak juga boleh dijana daripada rancangan projek yang dicipta menggunakan pendekatan anggaran bawah-atas.

Butiran baris kontrak boleh digunakan untuk menganggarkan masa, perbelanjaan atau yuran. Anggaran amaun cukai boleh juga dimasukkan dalam butiran baris kontrak.

Anggaran bahan tidak dibenarkan pada butiran baris kontrak.

Proses yang disokong pada kontrak projek adalah penciptaan dan pengesahan invois. Penciptaan invois mencipta draf untuk invois berasaskan projek yang termasuk semua aktual jualan belum dibilkan sehingga tarikh semasa.

Pengesahan menjadikan kontrak baca sahaja dan mengubah statusnya daripada **Draf** kepada **Disahkan**. Selepas anda mengambil tindakan ini, anda tidak boleh buat asal. Disebabkan tindakan ini adalah kekal, menjadi amalan terbaik untuk mengekalkan kontrak dalam status **Draf**.

Satu-satunya perbezaan antara kontrak draf dan kontrak disahkan ialah statusnya dan hakikat bahawa kontrak draf boleh diedit, manakala kontrak disahkan tidak boleh. Penciptaan invois dan aktual penjejakan boleh dilakukan pada kontrak draf dan kontrak disahkan.

Project operations tidak menyokong pesanan perubahan pada kontrak atau projek.

## <a name="estimating-projects"></a>Menganggarkan projek

Anda boleh menganggarkan masa dan perbelanjaan ke atas projek Project operations tidak membenarkan anggaran bahan atau yuran ke atas projek.

Anggaran masa dijana apabila anda mencipta tugas dan mengenal pasti atribut sumber generik yang diperlukan untuk menjalankan tugas. Anggaran masa dijana daripada tugas jadual. Anggaran masa tidak dicipta jika anda mencipta ahli pasukan generik di luar konteks jadual.

Anggaran perbelanjaan dimasukkan dalam grid pada halaman **Anggaran**.

## <a name="understanding-estimation"></a>Memahami anggaran

Gunakan jadual berikut sebagai panduan untuk memahami logik perniagaan dalam fasa anggaran.

| Senario                                                                                                                                                                                                                                                                                                                                          | Rekod entiti                                                                                                                                                                                                       | Jenis Transaksi | Kelas Transaksi | Maklumat tambahan                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Apabila anda perlu menganggarkan nilai jualan bagi masa atas sebut harga                                                                                                                                                                                                                                                                                    | Rekod butiran baris sebut harga (QLD) dicipta                                                                                                                                                                               | Kontrak projek | Time        | Medan asal transaksi pada baris QLD bahagian sasaran merujuk kepada QLD bahagian Kos |
|                                                                                                                                                                                                                                                                                     | Rekod QLD kedua dicipta oleh sistem untuk menyimpan nilai kos serupa. Semua medan bukan wang disalin daripada QLD jualan kepada QLD Kos oleh sistem.                                                                                                                                                                               | Kos | Time        | Medan asal transaksi pada baris butiran baris sebut harga (QLD) bahagian sasaran merujuk kepada QLD bahagian Kos |
| Apabila anda perlu menganggarkan nilai jualan bagi masa atas kontrak                                                                                                                                                                                                                                                                                 | Rekod butiran baris kontrak projek (CLD) dicipta                                                                                                                                                                    | Kontrak Projek | Time        | Medan asal transaksi pada baris CLD bahagian sasaran merujuk kepada CLD kos      |
|                                                                                                                                                                                                                                                                                  | Rekod CLD kedua dicipta oleh sistem untuk menyimpan nilai kos serupa. Semua medan bukan wang disalin daripada CLD jualan kepada CLD kos oleh sistem.                                                                                                                                                                    | Kos | Time        | Medan asal transaksi pada baris CLD bahagian sasaran merujuk kepada CLD kos      |
| Apabila mengguna melanggan sumber pada tugas projek                                                                                                                                                                                                                                                                                            | Anggaran rekod baris untuk menunjukkan nilai jualan tugas dicipta apabila tugas dicipta dengan semua dimensi penentuan harga yang diperlukan. Peranan dan unit organisasi adalah dimensi penetapan harga | Kontrak Projek | Waktu        |                                                                                   |
|     | Anggaran rekod baris untuk menunjukkan nilai kos tugas dicipta apabila tugas dicipta dengan semua dimensi penentuan harga yang diperlukan. Semua medan bukan wang disalin daripada baris anggaran jualan kepada baris anggaran kos oleh sistem. Peranan dan unit organisasi adalah dimensi penetapan harga untuk kedua-dua kod dan kadar bil.                                                                                                                                                                                                                | Kos             | Waktu           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Sesuaikan butiran baris Sebut Harga dan entiti butiran baris Kontrak

Jika anda menambah medan tersuai pada butiran baris sebut harga dan mahu sistem memasukkan nilai medan sebagai nilai lalai pada baris kos berkaitan yang dicipta, gunakan alat pendaftaran pasang masuk **PreOperationContractLineDetailUpdate** dan **PreOperationQuoteLineDetailUpdate**. Pasang masuk ini mestilah didaftarkan selepas butiran baris sebut harga atau butiran baris kontrak diubah. Ikuti langkah-langkah ini untuk menyelesaikan proses.

1. Buka Alat Pendaftaran Pasang Masuk, dan sambungkan ke tika dalam talian anda.
2. Pilih **Cari**, dan cari pasang masuk untuk kemas kini.
3. Pilih pasang masuk dan kemudian pada halaman utama, klik **Pilih**.
4. Pilih langkah pasang masuk untuk kemas kini, klik kanan, kemudian pilih **Kemas Kini**.
5. Dalam kotak dialog **Kemas Kini Langkah Sedia Ada**, dalam medan **Menapis Atribut**, pilih butang elipsis (**...**):
6. Dalam kotak dialog **Pilih Atribut**, pilih kotak semak untuk atribut tersuai.
7. Pilih **OK** untuk menutup kotak dialog, kemudian pilih **Kemas Kini Langkah**.
8. Ulangan langkah 1 hingga 7 untuk pasang masuk kedua.
9. Tutup **PluginRegistrationTool**.
