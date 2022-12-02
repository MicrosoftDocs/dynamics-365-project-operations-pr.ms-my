---
title: Konsep anggaran kewangan
description: Artikel ini menyediakan maklumat tentang anggaran kewangan projek dalam Project Operations.
author: rumant
ms.date: 03/22/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f8a4c3dd31cf5612c352331891178ac0ab852921
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931019"
---
# <a name="financial-estimation-concepts"></a>Konsep anggaran kewangan

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Dalam Dynamics 365 Project Operations, anda boleh menganggarkan projek anda dari segi kewangan dalam dua peringkat: 
1. Semasa peringkat prajualan sebelum urusan dimenangi. 
2. Semasa peringkat pelaksanaan selepas kontrak projek dicipta. 

Anda boleh mencipta anggaran kewangan untuk kerja berdasarkan projek menggunakan mana-mana 3 halaman berikut:
- Halaman **Baris sebut harga**, menggunakan butiran baris sebut harga.  
- Halaman **Baris kontrak projek**, menggunakan butiran baris kontrak. 
- Halaman **Projek**, menggunakan halaman tab **Tugas** atau **Anggaran Perbelanjaan**.

## <a name="use-a-project-quote-to-create-an-estimate"></a>Gunakan sebut harga projek untuk mencipta anggaran
Pada sebut harga berasaskan projek, anda boleh menggunakan entiti **Butiran baris sebut harga** untuk menganggarkan kerja yang diperlukan bagi menghantar projek. Kemudian, anda boleh berkongsi anggaran tersebut dengan pelanggan.

Baris sebut harga berasaskan projek boleh mempunyai sifar hingga banyak butiran baris sebut harga. Butiran baris sebut harga digunakan untuk menganggarkan masa, perbelanjaan atau yuran. Microsoft Dynamics 365 Project Operations tidak membenarkan anggaran bahan ke atas butiran baris sebut harga. Ini dipanggil kelas transaksi. Anggaran amaun cukai boleh juga dimasukkan dalam kelas transaksi.

Selain daripada kelas transaksi, butiran baris sebut harga mempunyai jenis transaksi. Dua jenis transaksi disokong untuk butiran baris sebut harga, **Kos** dan **Kontrak Projek**.

## <a name="use-a-project-contract-to-create-an-estimate"></a>Gunakan kontrak projek untuk mencipta anggaran

Jika anda menggunakan sebut harga apabila anda mencipta kontrak berasaskan projek, anggaran yang anda lakukan untuk setiap baris sebut harga ke atas sebut harga disalin pada kontrak projek. Struktur kontrak projek adalah seperti struktur sebut harga projek yang ada baris, butiran baris, dan jadual invois.

Anggaran boleh dilakukan secara terus dalam kontrak projek seperti dalam sebut harga projek. Untuk sebut harga projek, anggaran dilakukan menggunakan baris kontrak, dan butiran baris kontrak. Butiran baris kontrak juga boleh dijana daripada rancangan projek yang dicipta menggunakan pendekatan anggaran bawah-atas.

Butiran baris kontrak boleh digunakan untuk menganggarkan masa, perbelanjaan atau yuran. Anggaran amaun cukai boleh juga dimasukkan dalam butiran baris kontrak.

Anggaran bahan tidak dibenarkan pada butiran baris kontrak.

## <a name="use-a-project-to-create-an-estimate"></a>Gunakan projek untuk mencipta anggaran 

Anda boleh menganggarkan masa dan perbelanjaan ke atas projek Project Operations tidak menyokong anggaran bahan atau yuran pada projek.

Anggaran masa dijana apabila anda mencipta tugas dan mengenal pasti atribut sumber generik yang diperlukan untuk menjalankan tugas. Anggaran masa dijana daripada tugas jadual. Anggaran masa tidak dicipta jika anda mencipta ahli pasukan generik di luar konteks jadual.

Anggaran perbelanjaan dimasukkan dalam grid pada halaman **Anggaran Perbelanjaan**.

Mencipta anggaran untuk projek dianggap sebagai amalan terbaik kerana anda boleh membina anggaran terperinci bawah ke atas untuk buruh atau masa dan perbelanjaan pada setiap tugas dalam pelan projek. Kemudian anda boleh menggunakan anggaran terperinci ini untuk mencipta anggaran bagi setiap baris sebut harga dan membina sebut harga yang lebih dipercayai untuk pelanggan. Apabila anda mengimport atau mencipta anggaran terperinci pada baris sebut harga menggunakan pelan projek, Project Operations mengimport nilai jualan dan nilai kos anggaran ini. Selepas mengimport, anda boleh melihat metrik keuntungan, margin dan kebolehlaksanaan pada sebut harga projek.

## <a name="understanding-estimates"></a>Memahami anggaran

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
