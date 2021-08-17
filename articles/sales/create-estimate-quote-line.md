---
title: Cipta anggaran pada baris sebut harga
description: Topik ini menyediakan maklumat tentang cara mencipta anggaran pada baris sebut harga untuk projek.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8d7e7df4830612f5a7c43adf37f75bdb623959ffe00fe219441d8e394ddecac3
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996447"
---
# <a name="create-estimates-on-a-quote-line"></a>Cipta anggaran pada baris sebut harga

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Pada sebut harga berasaskan projek, anda boleh menggunakan entiti butiran baris Sebut Harga untuk menganggarkan kerja yang diperlukan untuk menghantar projek. Kemudian, anda boleh berkongsi anggaran tersebut dengan pelanggan.

Baris sebut harga berasaskan projek tidak perlu mempunyai butiran baris sebut harga. Secara alternatif, ia boleh mempunyai banyak butiran baris sebut harga. Butiran baris sebut harga digunakan untuk menganggarkan masa, perbelanjaan atau yuran. Dynamics 365 Project Operations tidak membenarkan anggaran bahan ke atas butiran baris sebut harga. Ini dipanggil kelas transaksi. Anggaran amaun cukai boleh juga dimasukkan dalam kelas transaksi.

Selain daripada kelas transaksi, butiran baris sebut harga mempunyai jenis transaksi. Terdapat dua jenis transaksi untuk butiran baris sebut harga, **Kos** dan **Kontrak Projek**.

## <a name="estimate-by-using-a-contract"></a>Anggaran menggunakan kontrak

Jika anda menggunakan sebut harga Project Operations apabila anda mencipta kontrak berasaskan projek, anggaran yang anda lakukan untuk setiap baris sebut harga pada sebut harga disalin ke kontrak projek. Struktur kontrak projek adalah seperti struktur sebut harga projek yang ada baris, butiran baris, dan jadual invois.

Anggaran boleh dilakukan secara terus dalam kontrak projek seperti dalam sebut harga projek. Untuk sebut harga projek, anggaran dilakukan menggunakan baris kontrak, dan butiran baris kontrak. Butiran baris kontrak juga boleh dijana daripada rancangan projek yang dicipta menggunakan pendekatan anggaran bawah-atas.

Butiran baris kontrak boleh digunakan untuk menganggarkan masa, perbelanjaan atau yuran. Anggaran amaun cukai boleh juga dimasukkan dalam butiran baris kontrak.

Anggaran bahan tidak dibenarkan pada butiran baris kontrak.

Proses yang disokong pada kontrak projek adalah penciptaan dan pengesahan invois. Penciptaan invois mencipta draf untuk invois berasaskan projek yang termasuk semua aktual jualan belum dibilkan sehingga tarikh semasa.

Pengesahan menjadikan kontrak baca sahaja dan mengubah statusnya daripada **Draf** kepada **Disahkan**. Selepas anda mengambil tindakan ini, anda tidak boleh buat asal. Disebabkan tindakan ini adalah kekal, menjadi amalan terbaik untuk mengekalkan kontrak dalam status **Draf**.

Satu-satunya perbezaan antara kontrak draf dan kontrak disahkan ialah statusnya dan hakikat bahawa kontrak draf boleh diedit, manakala kontrak disahkan tidak boleh. Penciptaan invois dan aktual penjejakan boleh dilakukan pada kontrak draf dan kontrak disahkan.

Pesanan perubahan tidak disokong pada kontrak atau projek.

## <a name="estimating-projects"></a>Menganggarkan projek

Anda boleh menganggarkan masa dan perbelanjaan projek tetapi bukan bahan atau yuran.

Anggaran masa dijana apabila anda mencipta tugas dan mengenal pasti atribut sumber generik yang diperlukan untuk menjalankan tugas. Anggaran masa dijana daripada tugas jadual. Anggaran masa tidak dicipta jika anda mencipta ahli pasukan generik di luar konteks jadual.

Anggaran perbelanjaan dimasukkan dalam grid pada halaman **Anggaran**.

## <a name="understand-estimation"></a>Fahami anggaran

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

Jika anda menambah medan tersuai pada butiran baris sebut harga dan mahu sistem memasukkan nilai medan sebagai nilai lalai pada baris kos berkaitan yang dicipta, gunakan alat pendaftaran pasang masuk PreOperationContractLineDetailUpdate dan PreOperationQuoteLineDetailUpdate. Pasang masuk ini mestilah didaftarkan selepas butiran baris sebut harga atau butiran baris kontrak diubah. Ikuti langkah-langkah ini untuk menyelesaikan proses.

1. Buka Alat Pendaftaran Pasang Masuk, dan sambungkan ke tika dalam talian anda.
2. Pilih **Cari**, dan cari pasang masuk untuk kemas kini.
3. Pilih pasang masuk, kemudian pada halaman utama, pilih **Pilih**.
4. Pilih langkah pasang masuk untuk kemas kini, klik kanan, kemudian pilih **Kemas Kini**.
5. Dalam kotak dialog **Kemas Kini Langkah Sedia Ada**, dalam medan **Menapis Atribut**, pilih butang elipsis (**...**):
6. Dalam kotak dialog **Pilih Atribut**, pilih kotak semak untuk atribut tersuai.
7. Pilih **OK** untuk menutup kotak dialog, kemudian pilih **Kemas Kini Langkah**.
8. Ulangan langkah 1 hingga 7 untuk pasang masuk kedua.
9. Tutup Alat Pendaftaran Pasang Masuk.


[!INCLUDE[footer-include](../includes/footer-banner.md)]