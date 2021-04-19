---
title: Anggarkan baris sebut harga projek
description: Topik ini menyediakan maklumat tentang cara mencipta anggaran pada baris sebut harga projek.
author: rumant
manager: Annbe
ms.date: 04/01/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b941511f842a81764ddd1c05a437578b9fd902ce
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858799"
---
# <a name="estimate-a-project-quote-line"></a>Anggarkan baris sebut harga projek

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Baris sebut harga berasaskan projek mempunyai butiran yang membantu menganggarkan kos dan potensi hasil kerja yang terlibat untuk menyampaikan baris sebut harga.

Untuk menganggarkan baris sebut harga berdasarkan projek, pada baris sebut harga, pilih tab **Butiran Baris Sebut Harga**. Terdapat dua cara untuk mencipta anggaran pada baris sebut harga berdasarkan projek:

   - Buat secara manual anggaran secara langsung pada baris sebut harga menggunakan butiran baris sebut harga. 
   - Cipta projek dan pelan projek, dan kemudian kaitkan projek dan tugas pada projek ke baris sebut harga. Proses untuk mengimport anggaran ke atas pelan projek ke dalam garis sebut harga berdasarkan maklumat yang anda berikan akan didayakan.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Buat anggaran secara langsung pada baris sebut harga berasaskan projek

Untuk mencipta anggaran secara terus pada baris sebut harga berdasarkan projek, ikut langkah ini:

1. Untuk mencipta anggaran pada baris sebut harga berasaskan projek, pilih tab **Butiran Baris Sebut Harga**. Item baris yang anda cipta pada tab ini akan merumuskan nilai sebut harga untuk baris sebut harga ini. 
2. Untuk mencipta butiran baris sebut harga, pilih **Butiran baris sebut harga baharu** pada subgrid **Butiran Baris Sebut Harga**. Gelangsar cipta pantas akan dibuka. Medan berikut pada halaman **Baris Sebut Harga**.

| **Medan** | **Lokasi** | **Perihalan** | **Kesan hiliran** |
| --- | --- | --- | --- |
| Penerangan | Cipta cepat | Perihalan mengenai anggaran tertentu. | Nilai ini lalai kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Kelas Transaksi | Cipta cepat | Senarai juntai bawah ini menyediakan kelas transaksi yang dimasukkan pada tab **Umum** baris sebut harga berasaskan projek.  | Nilai ini lalai kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Pilih Produk | Cipta cepat | Digunakan apabila kelas transaksi ialah **Bahan**. Anda boleh memilih untuk menentukan bahawa baris anggaran ini bagi produk (katalog) **Sedia ada** atau produk **Masukan manual**. | Nilai ini lalai kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Produk | Cipta cepat | ID produk daripada katalog produk. Medan ini hanya didayakan apabila anda memilih **Sedia ada** dalam medan **Pilih Produk**. ID digunakan untuk mendapatkan kembali harga jualan daripada senarai harga projek pada sebut harga. | Nilai ini lalai kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Produk Masukan Manual | Cipta cepat | Kotak teks untuk masukan manual nama produk. Medan ini hanya didayakan apabila anda memilih **Masukan Manual** dalam medan **Pilih Produk**.| Nilai ini lalai kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Peranan | Cipta cepat | Peranan orang yang akan melaksanakan kerja ini atau menanggung perbelanjaan ini. | Nilai ini lalai kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Kategori | Cipta cepat | Kategori bagi kerja atau perbelanjaan. | Nilai ini lalai kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Tarikh Mula | Cipta cepat | Tarikh mula kerja. | Medan ini lalai untuk butiran baris sebut harga bagi kos yang dicipta secara automatik. |
| Tarikh Tamat | Cipta cepat | Tarikh akhir kerja. | Medan ini lalai untuk butiran baris sebut harga bagi kos yang dicipta secara automatik. |
| Syarikat Penyumberan | Cipta Cepat | Syarikat atau entiti sah penyumberan yang menanggung kos ini dan menyediakan sumber untuk mengusahakannya. | Nilai ini lalai untuk butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik dan digunakan dalam pengambilan semula harga kos. |
| Unit Sumber | Cipta cepat | Unit penyumberan yang menanggung kos ini dan menyediakan sumber untuk mengusahakannya. | Nilai ini lalai untuk butiran baris sebut harga yang berkaitan bagi kos yang dicipta secara automatik dan digunakan dalam pengambilan semula harga kos. |
| Jadual unit | Cipta cepat | Kumpulan unit kerja, produk atau perbelanjaan. Unit yang tergolong dalam jadual seunit atau kumpulan unit. Contohnya, batu dan kilometers ialah unit yang tergolong dalam kumpulan unit yang menggambarkan jarak. | Nilai ini lalai kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Unit | Cipta cepat | Unit kerja, produk atau perbelanjaan. | Nilai ini lalai kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Kuantiti | Cipta cepat | Kuantiti kerja, produk atau perbelanjaan. | Nilai ini lalai kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Harga unit | Cipta Cepat |Kadar bil peranan yang melaksanakan kerja, harga unit produk atau harga jualan kategori produk atau perbelanjaan. Lalai untuk **Masa** berdasarkan gabungan nilai dimensi penetapan harga pada baris harga peranan bagi senarai harga projek yang berkuat kuasa untuk tarikh mula. Untuk **Perbelanjaan**, lalai adalah daripada persediaan harga untuk kategori transaksi dalam senarai harga projek yang berkuat kuasa untuk tarikh mula. Jika kaedah penetapan harga untuk kategori urus niaga tidak harga setiap unit, tidak ada lalai, medan ini dibiarkan kosong. Untuk produk, lalai medan ini adalah berdasarkan baris **Item senarai harga** dalam senarai harga kos yang berkuat kuasa untuk tarikh mula.| Kadar kos peranan yang melaksanakan kerja, atau kos setiap unit kategori perbelanjaan atau kos unit produk. Lalai untuk **Masa** berdasarkan gabungan nilai dimensi penetapan harga pada baris harga peranan bagi senarai harga kos yang dilampirkan pada unit kontrak yang berkuat kuasa untuk tarikh mula. Untuk perbelanjaan, lalai adalah berdasarkan baris harga kategori bagi senarai harga kos yang dilampirkan pada unit kontrak yang berkuat kuasa untuk tarikh mula. Jika kaedah penetapan harga untuk kategori transaksi bukan harga setiap unit, tiada tetapan lalai dan medan ini dibiarkan kosong. Untuk produk, lalai medan ini adalah berdasarkan baris **Item senarai harga** bagi senarai harga kos yang dilampirkan pada unit kontrak yang berkuat kuasa untuk tarikh mula.|
| Anggaran Cukai | Cipta cepat | Anda boleh memasukkan cukai anggaran secara manual untuk kerja atau perbelanjaan ini. | Tiada kesan hiliran untuk medan ini. |
| Amaun | Cipta cepat | Anda boleh memasukkan maklumat input secara manual ke medan ini jika medan **Kuantiti** dan **Harga** dibiarkan kosong. Jika medan ini tidak kosong, medan ini menjadi baca sahaja dan dikira sebagai (Kuantiti \* Harga unit) + Cukai. | Tiada kesan hiliran untuk medan ini. |

## <a name="update-prices-on-quote-line-details"></a>Kemas kini harga untuk butiran baris sebut harga

Jika anda telah mengubah harga pada senarai harga projek yang dilampirkan dengan sebut harga, atau pada senarai harga kos unit kontrak, anda boleh memilih **Mengira semula** pada halaman **Sebut harga**, untuk menyegarkan harganya pada butiran baris sebut harga individu untuk mencerminkan perubahan ini. Apabila anda memilih **Mengira semula**, amaran muncul yang memaklumkan kepada anda bahawa harga pada butiran baris sebut harga untuk semua baris sebut harga pada sebut harga ini akan ditetapkan semula. Pilih **Ya** untuk menyegarkan semula harga untuk jualan dan butiran baris sebut harga.

## <a name="access-quote-line-details-for-cost"></a>Akses butiran baris sebut harga untuk kos

Bagi mengakses butiran baris sebut harga untuk kos, ikuti langkah ini:

1. Pada tab **Butiran Baris Sebut Harga**, pilih baris dalam grid untuk mendayakan tindakan pada bar alat subgrid. 
2. Pilih **Buka Butiran Kos** untuk melihat kadar kos dan jumlah yang berkaitan untuk baris sebut harga ini.

> [!NOTE]
> Mengubah unit sumber, kuantiti, tarikh, peranan atau nilai kategori pada baris sebut harga butiran untuk kos akan mengubah nilai yang sesuai pada butiran baris sebut harga untuk jualan.

## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Mata wang untuk butiran baris sebut harga kos dan jualan

Mata wang pada butiran baris sebut harga untuk jualan lalai daripada senarai harga projek yang berkuat kuasa untuk tarikh mula bagi butiran baris sebut harga.

Mata wang pada butiran baris sebut harga untuk kos lalai daripada senarai harga unit kontrak bagi sebut harga yang berkuat kuasa untuk tarikh mula bagi butiran baris sebut harga untuk kos.

> [!NOTE]
> Pengiraan keuntungan menukar jumlah pada butiran baris sebut harga untuk kos dan jualan ke asas mata wang persekitaran untuk melaporkan jumlah margin yang dianggarkan pada sebut harga tersebut. Ralat pembundaran mata wang dan margin yang ditukar boleh berlaku kerana kurangnya kadar pertukaran berkesan tarikh. Gunakan pengiraan ini hanya pada sebut harga projek kerana ini ialah anggaran dan bukan untuk statutori aktual atau pelaporan lain yang memerlukan ketepatan pembundaran dan kesedaran yang lebih tinggi tentang penguatkuasaan tarikh untuk kadar pertukaran.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
