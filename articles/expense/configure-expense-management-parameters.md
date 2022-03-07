---
title: Konfigurasikan parameter pengurusan Perbelanjaan
description: Topik ini menghuraikan parameter yang mengawal tingkah laku umum dalam pengurusan Perbelanjaan.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 1cabb0be624f7f6c12761e4fb6d5a095396a5940a37616bb3a304798e1f97808
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007787"
---
# <a name="configure-expense-management-parameters"></a>Konfigurasikan parameter pengurusan Perbelanjaan

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Topik ini menghuraikan parameter mengawal tingkah laku umum dalam pengurusan Perbelanjaan.

## <a name="general"></a>Umum

| Medan                                                    | Penerangan |
|----------------------------------------------------------|-------------|
| Kadar standard perbatuan                                 | Masukkan kadar bayaran balik untuk perbelanjaan perbatuan. Kadar ini didarabkan dengan perbatuan yang dimasukkan untuk perbelanjaan untuk mengira jumlah yang dibayar balik untuk perbelanjaan perjalanan. |
| Sahkan tujuan perbelanjaan                                 | Hidupkan pilihan ini untuk mengehadkan pengguna kepada set nilai sedia ada yang dikonfigurasikan dalam medan **Tujuan laporan perbelanjaan** apabila mereka mencipta laporan perbelanjaan. |
| Perbelanjaan peribadi yang dibayar oleh                                | Pilih siapa yang bertanggungjawab untuk membayar sebarang jumlah transaksi kad kredit yang dikategorikan sebagai peribadi. |
| Paparkan keseluruhan laporan perbelanjaan pada drillback               | Pilih pilihan ini untuk menunjukkan semua perbelanjaan untuk laporan perbelanjaan apabila butiran dokumen asal dilihat untuk baucar tertentu yang dijana apabila laporan perbelanjaan telah diterbitkan. |
| Prakebenaran perjalanan adalah mandatori                 | Pilih pilihan ini untuk menghendaki permintaan perjalanan diserahkan dan diluluskan sebelum pekerja boleh menyerahkan laporan perbelanjaan. |
| Membenarkan pengeditan pengagihan sebelum diterbitkan            | Pilih sama ada pengagihan laporan perbelanjaan boleh diedit sebelum diterbitkan. |
| Menilai dasar pengurusan perbelanjaan                     | Pilih apabila perbelanjaan dinilai untuk menentukan sama ada dasar perbelanjaan telah dilanggar. Perbelanjaan boleh dinilai untuk pelanggaran apabila kemasukan perbelanjaan dimasukkan dan disimpan, atau apabila perbelanjaan tersebut diserahkan untuk kelulusan. Peraturan dasar untuk resit yang diperlukan akan dinilai apabila baris perbelanjaan disimpan. |
| Benarkan baris perbelanjaan antara syarikat                         | Pilih sama ada perbelanjaan untuk entiti sah lain boleh dimasukkan pada laporan perbelanjaan. |
| Benarkan mengedit kadar pertukaran untuk perbelanjaan kad kredit | Pilih pilihan ini untuk membolehkan pengguna mengedit kadar pertukaran untuk perbelanjaan kad kredit yang diimport. |
| Medan hierarki berbilang peringkat untuk dipaparkan                  | Pilih medan pelulus yang ditunjukkan apabila jenis tugasan aliran kerja ditetapkan untuk menjadi hierarki dan pemilihan **Hierarki** ditetapkan untuk menggunakan hierarki kelulusan, kelulusan berbilang peringkat. Apabila hierarki kelulusan berbilang peringkat digunakan untuk aliran kerja, medan yang dipilih akan ditunjukkan pada laporan perbelanjaan dan boleh diedit. |
| Masukkan nombor kad kredit pekerja                        | Pilih sama ada nombor 15 atau aksara 16 boleh dimasukkan dan disimpan dalam medan **ID Kad** pada halaman **Kad kredit** untuk pekerja. |
| Mengesahkan tujuan permintaan perjalanan                      | Hidupkan pilihan ini untuk mengehadkan pengguna kepada set nilai sedia ada yang dikonfigurasikan dalam medan **Tujuan laporan perbelanjaan** apabila mereka mencipta keperluan perjalanan. |

## <a name="financial"></a>Kewangan

| Medan                                                                                    | Penerangan |
|------------------------------------------------------------------------------------------|-------------|
| Nama jurnal harian lejar                                                                | Pilih nama jurnal lejar yang diluluskan oleh laporan perbelanjaan. |
| Bolehkan pemulihan cukai daripada perbelanjaan                                                        | Pilih pilihan ini untuk mendayakan pemulihan cukai perbelanjaan untuk perbelanjaan yang layak. Pilihan ini tidak boleh dipilih jika cukai jualan AS dan menggunakan peraturan cukai didayakan. |
| Post pendahuluan tunai dengan serta-merta                                                           | Pilih pilihan ini untuk menyiarkan pendahuluan tunai yang diluluskan apabila proses Pembayaran dan pemindahan selesai. Jika pilihan ini tidak dipilih, proses Pembayaran dan pemindahan menjana jurnal umum yang belum diterbitkan. |
| Tarikh perakaunan yang betul semasa menyiarkan                                                   | Pilih pilihan ini untuk mengemas kini tarikh perakaunan apabila perbelanjaan disiarkan, jika tempoh semasa sedang ditahan atau tertutup. Tarikh perakaunan akan ditetapkan kepada tempoh terbuka akan datang. |
| Membenarkan pengumpulan urus niaga berdasarkan akaun yang diimbangi seperti yang dinyatakan dalam kaedah pembayaran       | Pilih pilihan ini untuk merumuskan transaksi perbelanjaan untuk laporan perbelanjaan, berdasarkan akaun ofset yang ditentukan dalam kaedah pembayaran untuk perbelanjaan. |
| Cukai termasuk                                                                             | Pilih pilihan ini untuk memasukkan cukai jualan dalam jumlah perbelanjaan secara lalai. |
| Mengeluarkan bebanan pada penutupan perjalanan                                      | Pilih pilihan ini untuk mengeluarkan dana terbeban apabila permintaan perjalanan yang diluluskan ditutup. |
| Membenarkan permintaan perjalanan menyerahkan lebihan had bajet untuk daftar bajet dan bajet projek | Pilih pilihan ini untuk membolehkan kakitangan menyerahkan pengesahan perjalanan untuk kelulusan, walaupun mereka melebihi sama ada bajet dibenarkan yang ditetapkan dalam senarai bajet atau bajet yang dibenarkan untuk projek. |
| Membenarkan laporan perbelanjaan menyerahkan lebihan had bajet untuk daftar bajet dan bajet projek     | Pilih pilihan ini untuk membolehkan kakitangan menyerahkan laporan perbelanjaan untuk kelulusan, walaupun mereka melebihi sama ada bajet dibenarkan yang ditetapkan dalam senarai bajet atau bajet yang dibenarkan untuk projek. |
| Membenarkan kelulusan laporan perbelanjaan lebihan had bajet untuk daftar bajet sahaja                 | Pilih pilihan ini untuk membenarkan approvers meluluskan laporan perbelanjaan yang melebihi bajet dibenarkan yang ditetapkan dalam daftar bajet. |

## <a name="per-diem"></a>Bagi sehari

| Medan                                 | Penerangan |
|---------------------------------------|-------------|
| Minimum untuk setiap diem            | Masukkan bilangan jam lalai yang mana pekerja mesti bekerja dalam sehari untuk layak menerima perbelanjaan bagi setiap diem untuk perjalanan yang berkaitan dengan perjalanan. Nilai ini digunakan sebagai nilai lalai hanya untuk medan **Tempoh minimum** bagi setiap peringkat kadar masa. |
| Peratus hidangan                          | Masukkan peratus lalai bagi setiap diem untuk hidangan yang digunakan pada hari pertama dan terakhir bagi perbelanjaan berkaitan perjalanan apabila medan **Kira pengurangan hidangan mengikut** ditetapkan sama ada **Jenis hidangan setiap hari** atau **Bilangan hidangan setiap hari**. Hari kerja pada hari pertama dan terakhir mungkin lebih pendek daripada hari kerja standard. Oleh itu, jumlah setiap diem pada hari tersebut mungkin berbeza daripada jumlah yang standard. Jika peratusan ditetapkan kepada **0** (sifar), potongan untuk hari pertama dan terakhir akan 0.00. |
| Peratus hotel                         | Masukkan peratusan lalai bagi setiap diem untuk hotel yang digunakan pada hari pertama dan terakhir bagi perbelanjaan yang berkaitan dengan perjalanan. Hari kerja pada hari pertama dan terakhir mungkin lebih pendek daripada hari kerja standard. Oleh itu, jumlah setiap diem pada hari tersebut mungkin berbeza daripada jumlah yang standard. Jika peratusan ditetapkan kepada **0** (sifar), potongan untuk hari pertama dan terakhir akan 0.00. |
| Peratus lain                         | Masukkan peratusan lalai bagi setiap diem untuk perbelanjaan lain-lain yang digunakan pada hari pertama dan terakhir bagi perbelanjaan yang berkaitan dengan perjalanan. Hari kerja pada hari pertama dan terakhir mungkin lebih pendek daripada hari kerja standard. Oleh itu, jumlah setiap diem pada hari tersebut mungkin berbeza daripada jumlah yang standard. Jika peratusan ditetapkan kepada **0** (sifar), potongan untuk hari pertama dan terakhir akan 0.00. |
| Pengurangan peratusan untuk sarapan pagi | Masukkan jumlah yang akan dikurangkan untuk sarapan pagi. Sebagai contoh, jika pekerja menerima sarapan percuma, anda mungkin mahu mengurangkan jumlah setiap diem sebanyak 10 peratus. |
| Pengurangan peratusan untuk makan tengah hari     | Masukkan jumlah yang akan dikurangkan untuk makan tengah hari. Sebagai contoh, jika pekerja menerima makan tengah hari percuma, anda mungkin mahu mengurangkan jumlah setiap diem sebanyak 15 peratus. |
| Pengurangan peratusan untuk makan malam    | Masukkan jumlah yang akan dikurangkan untuk makan malam. Sebagai contoh, jika pekerja menerima makan malam percuma, anda mungkin mahu mengurangkan jumlah setiap diem sebanyak 25 peratus. |
| Hitung pengurangan hidangan mengikut           | Tentukan bagaimana sistem perlu mengira pengurangan hidangan setiap diem, dengan memilih sama ada pengurangan berdasarkan jenis makanan setiap kali perjalanan atau setiap hari, atau sama ada ia berdasarkan bilangan hidangan yang dibenarkan setiap hari. |
| Setiap pemgenapan diem                     | Pilih jenis penggenapan yang digunakan untuk perbelanjaan setiap diem. Jika anda memilih pembundaran biasa, sebarang perbelanjaan setiap Diem yang mempunyai jumlah sebanyak 0.50 dibulatkan ke 1.00 dan sebarang perbelanjaan setiap diem yang mempunyai jumlah yang kurang daripada 0.50 dibundarkan ke bawah untuk 0.00. |
| Pengiraan asas bagi setiap diem pada          | Pilih sama ada jumlah setiap diem adalah berdasarkan hari kalendar atau tempoh 24 jam. |

## <a name="fax-cover-pages"></a>Laman web perlindungan faks

| Medan                          | Penerangan |
|--------------------------------|-------------|
| Arahan                   | Masukkan arahan yang pekerja mesti ikuti apabila mereka mencipta halaman perlindungan untuk Faks yang digunakan untuk menghantar resit yang berkaitan dengan laporan perbelanjaan. Untuk memasukkan teks khusus bahasa yang akan ditunjukkan, berdasarkan bahasa pengguna, pilih **Terjemahan**. |
| ID pengguna (maklumat Kod Bar) | Pilih pilihan ini untuk menyimpan pengecam unik pekerja dalam kod bar yang digunakan pada halaman perlindungan bagi faks. |
| Kod bar                       | Pilih kod bar yang digunakan pada halaman perlindungan bagi faks. Bar kod 39 dan 128 disokong dalam pengurusan Perbelanjaan. |

## <a name="anti-corruption"></a>Antirasuah

| Medan                                 | Penerangan |
|---------------------------------------|-------------|
| Mempamerkan serangan antirasuah   | Pilih pilihan ini untuk menunjukkan teks anti rasuah apabila laporan perbelanjaan dicipta. Kategori belanja khusus boleh kemudian didayakan yang akan memerlukan bahawa penkategorasi antirasuah dipilih dalam laporan perbelanjaan. Contohnya, kategori hadiah yang berkaitan dengan perbelanjaan rasmi kerajaan mungkin menghendaki pekerja mengesahkan bahawa perbelanjaan tersebut memenuhi dasar syarikat yang berkaitan dengan pegawai kerajaan. |
| Mesej antirasuah untuk penghantar | Masukkan teks yang sepatutnya ditunjukkan kepada pekerja yang mencipta laporan perbelanjaan. Untuk memasukkan teks khusus bahasa yang akan ditunjukkan, berdasarkan bahasa pengguna, pilih **Terjemahan**. |
| Mesej antirasuah untuk pelulus  | Masukkan teks yang sepatutnya ditunjukkan kepada kepada pelulus semasa laporan perbelanjaan dibuat. Untuk memasukkan teks khusus bahasa yang akan ditunjukkan, berdasarkan bahasa pengguna, pilih **Terjemahan**. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]