---
title: Parameter Pengurusan perbelanjaan
description: Parameter berikut mengawal tingkah laku dalam Pengurusan perbelanjaan.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 41d78726f6d0aa6b5e647dbb359824950cb6ca72
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993741"
---
# <a name="expense-management-parameters"></a>Parameter Pengurusan perbelanjaan


Parameter berikut mengawal tingkah laku am dalam Pengurusan perbelanjaan.

### <a name="general"></a>Umum

| **Medan**                                                | **Penerangan**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Kadar standard perbatuan**                             | Masukkan kadar bayaran balik untuk perbelanjaan perbatuan. Kadar ini akan didarabkan dengan perbatuan yang dimasukkan pada perbelanjaan untuk mengira jumlah yang dibayar balik untuk perbelanjaan perjalanan.                       |
|**Perbelanjaan peribadi yang dibayar oleh**                             | Pilih orang yang bertanggungjawab untuk membayar mana-mana amaun transaksi kad kredit yang dikategorikan sebagai peribadi.                                                                                                     |
|**Paparkan keseluruhan laporan perbelanjaan pada drillback**               | Pilih pilihan ini untuk memaparkan semua perbelanjaan untuk laporan perbelanjaan apabila melihat butiran dokumen asal untuk baucar tertentu yang dijana apabila laporan perbelanjaan disiarkan.              |
|**Prakebenaran perjalanan adalah mandatori**                 | Pilih pilihan ini untuk menghendaki permintaan perjalanan diserahkan dan diluluskan sebelum pekerja boleh menyerahkan laporan perbelanjaan.                                                                    |
|**Membenarkan pengeditan pengagihan sebelum diterbitkan**            | Pilih sama ada pengagihan laporan perbelanjaan boleh diedit sebelum disiarkan.                                                                                                                 |
|**Menilai dasar pengurusan perbelanjaan**                     | Pilih apabila perbelanjaan dinilai untuk menentukan sama ada dasar perbelanjaan telah dilanggar. Perbelanjaan boleh disemak untuk pelanggaran apabila entri perbelanjaan dimasukkan dan disimpan, atau apabila perbelanjaan tersebut diserahkan untuk kelulusan. Peraturan dasar untuk resit yang diperlukan akan disemak apabila baris perbelanjaan disimpan.                   |
|**Benarkan baris perbelanjaan antara syarikat**                         | Pilih sama ada membenarkan entri perbelanjaan untuk entiti sah lain dalam laporan perbelanjaan.                                                                                                          |
|**Benarkan mengedit kadar pertukaran untuk perbelanjaan kad kredit** | Pilih pilihan ini untuk membolehkan pengguna mengedit kadar pertukaran untuk perbelanjaan kad kredit yang diimport.                                                                        |
|**Medan hierarki berbilang peringkat untuk dipaparkan**                  | Pilih medan pelulus untuk dipaparkan apabila jenis penugaskan aliran kerja laporan perbelanjaan ditetapkan kepada hierarki dan pemilihan hierarki ditetapkan untuk menggunakan hierarki kelulusan berbilang tahap Perbelanjaan. Apabila hierarki kelulusan berbilang tahap digunakan untuk aliran kerja, medan yang dipilih akan dipaparkan dan boleh diedit dalam laporan Perbelanjaan. |
|**Masukkan nombor kad kredit pekerja (kemas kini Julai 2017)**     | Pilih sama ada nombor 15 atau 16 aksara boleh dimasukkan dan disimpan dalam medan **ID Kad** dalam halaman **Kad kredit** untuk pekerja.                                                                          |

### <a name="financial"></a>Kewangan

| **Medan**                                                            | **Perihalan**     |
|----------------------------------------------------------------------|------------------------------------|
|**Nama jurnal harian lejar**                                         | Pilih nama jurnal lejar yang diluluskan oleh laporan perbelanjaan.            |
|**Bolehkan pemulihan cukai daripada perbelanjaan**                                  | Pilih pilihan ini untuk mendayakan pemulihan cukai perbelanjaan untuk perbelanjaan yang layak. Pilihan ini tidak boleh didayakan jika cukai jualan AS dan menggunakan peraturan cukai didayakan.      |
|**Post pendahuluan tunai dengan serta-merta**                                     | Pilih pilihan ini untuk menyiarkan pendahuluan tunai yang diluluskan apabila proses untuk Pembayaran dan pemindahan selesai. Jika pilihan ini tidak dipilih, proses Pembayaran dan pemindahan akan menjana jurnal umum yang belum disiarkan. |
|**Tarikh perakaunan yang betul semasa menyiarkan**                             | Pilih pilihan ini untuk mengemas kini tarikh perakaunan apabila menyiarkan perbelanjaan, jika tempoh semasa sedang ditahan atau tertutup. Tarikh perakaunan akan ditetapkan kepada tempoh terbuka akan datang.   |
|**Membenarkan pengumpulan urus niaga berdasarkan akaun yang diimbangi seperti yang dinyatakan dalam kaedah pembayaran**      | Pilih pilihan ini untuk merumuskan transaksi perbelanjaan untuk laporan perbelanjaan, berdasarkan akaun ofset yang ditentukan dalam kaedah pembayaran untuk perbelanjaan.   
|**Cukai termasuk**                                                   | Pilih pilihan ini untuk memasukkan cukai jualan dalam jumlah perbelanjaan secara lalai.             |
|**Mengeluarkan bebanan pada penutupan perjalanan**            | Pilih pilihan ini untuk mengeluarkan dana terbeban apabila permintaan perjalanan yang diluluskan ditutup.                                                                                   |
|**Membenarkan permintaan perjalanan menyerahkan lebihan had bajet untuk daftar bajet dan bajet projek** | Pilih pilihan ini untuk membolehkan pekerja menyerahkan permintaan perjalanan untuk kelulusan yang melebihi sama ada belanjawan dibenarkan yang ditetapkan dalam daftar belanjawan atau belanjawan yang dibenarkan untuk projek.            |
|**Membenarkan laporan perbelanjaan menyerahkan lebihan had bajet untuk daftar bajet dan bajet projek**    | Pilih pilihan ini untuk membolehkan pekerja menyerahkan laporan perbelanjaan untuk kelulusan yang melebihi sama ada belanjawan dibenarkan yang ditetapkan dalam daftar belanjawan atau belanjawan yang dibenarkan untuk projek.                |
|**Membenarkan kelulusan laporan perbelanjaan lebihan had bajet untuk daftar bajet sahaja**                | Pilih pilihan ini untuk membenarkan approvers meluluskan laporan perbelanjaan yang melebihi bajet dibenarkan yang ditetapkan dalam daftar bajet.                                                                       |

### <a name="per-diem"></a>Bagi sehari

| **Medan**                             | **Penerangan**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Minimum untuk setiap diem**           | Masukkan bilangan jam lalai yang mana pekerja mesti bekerja dalam sehari untuk layak menerima perbelanjaan bagi setiap diem untuk perjalanan yang berkaitan dengan perjalanan.  Nilai ini hanya digunakan sebagai nilai lalai untuk medan Jam minimum pada peringkat kadar saraan harian.                                                                                      |
|**Peratus hidangan**                          | Masukkan peratus lalai bagi setiap diem untuk hidangan yang digunakan pada hari pertama dan terakhir bagi perbelanjaan berkaitan perjalanan apabila medan **Kira pengurangan hidangan mengikut** ditetapkan sama ada **Jenis hidangan setiap hari** atau **Bilangan hidangan setiap hari**. Hari kerja pada hari pertama dan terakhir mungkin lebih pendek daripada hari kerja standard. Oleh itu, amaun saraan harian pada hari-hari tersebut mungkin berbeza daripada amaun standard. Jika peratusan ditetapkan kepada 0, maka potongan hari pertama dan terakhir akan menjadi 0.00. |
|**Peratus hotel**                        | Masukkan peratusan lalai bagi setiap diem untuk hotel yang digunakan pada hari pertama dan terakhir bagi perbelanjaan yang berkaitan dengan perjalanan. Hari kerja pada hari pertama dan terakhir mungkin lebih pendek daripada hari kerja standard. Oleh itu, amaun saraan harian pada hari-hari tersebut mungkin berbeza daripada amaun standard. Jika peratusan ditetapkan kepada 0, maka potongan hari pertama dan terakhir akan menjadi 0.00.                                              |
|**Peratus lain**                        | Masukkan peratusan lalai bagi setiap diem untuk perbelanjaan lain-lain yang digunakan pada hari pertama dan terakhir bagi perbelanjaan yang berkaitan dengan perjalanan. Hari kerja pada hari pertama dan terakhir mungkin lebih pendek daripada hari kerja standard. Oleh itu, amaun saraan harian pada hari-hari tersebut mungkin berbeza daripada amaun standard. Jika peratusan ditetapkan kepada 0, maka potongan hari pertama dan terakhir akan menjadi 0.00.                                                                                                     |
|**Pengurangan peratusan untuk sarapan pagi** | Masukkan amaun saraan harian yang dikurangkan untuk sarapan. Sebagai contoh, jika pekerja mendapat sarapan percuma, anda mungkin mahu mengurangkan amaun saraan harian sebanyak 10 peratus.                               |
|**Pengurangan peratusan untuk makan tengah hari**    | Masukkan amaun saraan harian yang dikurangkan untuk makan tengah hari. Sebagai contoh, jika pekerja mendapat makan tengah hari percuma, anda mungkin mahu mengurangkan amaun saraan harian sebanyak 15 peratus.                                       |
|**Pengurangan peratusan untuk makan malam**   | Masukkan amaun saraan harian yang dikurangkan untuk makan malam. Sebagai contoh, jika pekerja mendapat makan malam, anda mungkin mahu mengurangkan amaun saraan harian sebanyak 25 peratus.                                     |
|**Hitung pengurangan hidangan mengikut**         | Pilih cara sistem harus mengira pengurangan makanan saraan harian, dengan memilih sama ada pengurangan berdasarkan jenis makanan bagi setiap perjalanan atau setiap hari, atau sama ada pengurangan adalah berdasarkan bilangan hidangan yang dibenarkan setiap hari.|
|**Setiap pemgenapan diem**                  | Pilih jenis penggenapan yang digunakan untuk perbelanjaan setiap diem. Jika anda memilih pembundaran biasa, sebarang perbelanjaan setiap Diem yang mempunyai jumlah sebanyak 0.50 dibulatkan ke 1.00 dan sebarang perbelanjaan setiap diem yang mempunyai jumlah yang kurang daripada 0.50 dibundarkan ke bawah untuk 0.00.                                                                                              |
|**Pengiraan asas bagi setiap diem pada**         | Pilih sama ada jumlah setiap diem adalah berdasarkan hari kalendar atau tempoh 24 jam.       |

### <a name="fax-cover-pages"></a>Laman web perlindungan faks

| **Medan**                      | **Penerangan**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Arahan**                   | Masukkan arahan yang pekerja mesti ikuti apabila mereka mencipta halaman perlindungan untuk Faks yang digunakan untuk menghantar resit yang berkaitan dengan laporan perbelanjaan. Klik butang **Terjemahan** untuk memasukkan teks khusus bahasa yang akan dipaparkan berdasarkan bahasa pengguna. |
|**ID pengguna (maklumat Kod Bar)** | Pilih pilihan ini untuk menyimpan pengecam unik pekerja dalam kod bar yang digunakan pada halaman kulit faks.                 |
|**Kod bar**                      | Pilih kod bar yang digunakan pada halaman perlindungan bagi faks. Kod bar 39 dan 128 disokong dengan Pengurusan perbelanjaan.               |

### <a name="anti-corruption"></a>Antirasuah

|                 <strong>Medan</strong>                 |                                                                                                                                                                                            <strong>Perihalan</strong>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <strong>Mempamerkan serangan antirasuah</strong>  | Pilih pilihan ini untuk memaparkan teks antirasuah apabila mencipta laporan perbelanjaan baharu. Kategori perbelanjaan tertentu kemudian boleh didayakan yang akan memerlukan pengakuan antirasuah dipilih pada laporan perbelanjaan. Contohnya, kategori hadiah yang berkaitan dengan perbelanjaan pegawai kerajaan mungkin menghendaki pekerja mengesahkan bahawa perbelanjaan tersebut memenuhi dasar syarikat yang berkaitan dengan pegawai kerajaan. |
| <strong>Mesej antirasuah untuk penghantar</strong> |                                                                                             Masukkan teks yang akan dipaparkan kepada pekerja apabila mencipta laporan perbelanjaan baharu. Klik butang <strong>Terjemahan</strong> untuk memasukkan teks khusus bahasa yang akan dipaparkan berdasarkan bahasa pengguna.                                                                                             |
| <strong>Mesej antirasuah untuk pelulus</strong>  |                                                                                             Masukkan teks yang akan dipaparkan kepada pelulus apabila mencipta laporan perbelanjaan baharu. Klik butang <strong>Terjemahan</strong> untuk memasukkan teks khusus bahasa yang akan dipaparkan berdasarkan bahasa pengguna.                                                                                             |



[!INCLUDE[footer-include](../includes/footer-banner.md)]