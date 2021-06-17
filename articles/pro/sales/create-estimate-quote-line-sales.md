---
title: Menganggarkan baris sebut harga berdasarkan projek
description: Topik ini menyediakan maklumat tentang cara mencipta anggaran pada baris sebut harga berasaskan projek.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 20a318c9f288b08a0984f9c29dced05997622f47
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003417"
---
# <a name="estimating-a-project-based-quote-line"></a>Menganggarkan baris sebut harga berdasarkan projek

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Baris sebut harga berasaskan projek mempunyai butiran yang membantu menganggarkan kos dan potensi hasil kerja yang terlibat untuk menyampaikan baris sebut harga.

Untuk menganggarkan baris sebut harga berdasarkan projek, pada baris sebut harga berasaskan projek, pilih tab **Butiran Baris Sebut Harga**. Terdapat dua cara untuk mencipta anggaran pada baris sebut harga berasaskan projek:

- Buat secara manual anggaran secara langsung pada baris sebut harga menggunakan butiran baris sebut harga. 
- Cipta projek dan pelan projek, dan kemudian kaitkan projek dan tugas pada projek ke baris sebut harga. Proses untuk mengimport anggaran ke atas pelan projek ke dalam garis sebut harga berdasarkan maklumat yang anda berikan akan didayakan.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Buat anggaran secara langsung pada baris sebut harga berasaskan projek

Untuk mencipta anggaran pada baris sebut harga berasaskan projek, pilih tab **Butiran Baris Sebut Harga**. Item baris yang anda cipta pada tab ini akan merumuskan nilai sebut harga untuk baris sebut harga ini. 

Untuk mencipta butiran baris sebut harga, pilih **Butiran baris sebut harga baharu** pada subgrid **Butiran Baris Sebut Harga**. Gelangsar cipta pantas akan dibuka. Jadual berikut menyediakan butiran tentang medan pada halaman **Butiran Baris Sebut Harga** dan cara nilai memberikan kesan kepada kefungsian.

| **Medan** | **Lokasi** | **Perihalan** | **Kesan hiliran** |
| --- | --- | --- | --- |
| Penerangan | Cipta cepat | Perihalan mengenai anggaran tertentu. | Nilai ini lalai kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Kelas Transaksi | Cipta cepat | Senarai juntai bawah ini menyediakan kelas transaksi yang disertakan pada tab **Umum** bagi baris sebut harga berdasarkan projek.  | Nilai ini lalai kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Pilih Produk | Cipta cepat | Digunakan apabila kelas transaksi ialah **Bahan**. Anda boleh memilih untuk menentukan bahawa baris anggaran ini bagi produk (katalog) **Sedia ada** atau produk **Masukan Manual**. | Nilai ini lalai kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Produk | Cipta cepat | ID produk daripada katalog produk. Medan ini hanya didayakan jika anda memilih **Sedia ada** dalam medan **Pilih Produk**. ID digunakan untuk mendapatkan kembali harga jualan daripada senarai harga projek pada sebut harga. | Nilai ini lalai kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Produk Masukan Manual | Cipta cepat | Kotak teks untuk masukan manual nama produk. Medan ini hanya didayakan jika anda memilih **Masukan Manual** dalam medan **Pilih Produk**.| Nilai ini lalai kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Peranan | Cipta cepat | Peranan orang yang akan melaksanakan kerja ini atau menanggung perbelanjaan ini. | Nilai ini lalai kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Kategori | Cipta cepat | Kategori bagi kerja atau perbelanjaan. | Nilai ini lalai kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Tarikh Mula | Cipta cepat | Tarikh mula kerja. | Medan ini lalai untuk butiran baris sebut harga bagi kos yang dicipta secara automatik. |
| Tarikh Tamat | Cipta cepat | Tarikh akhir kerja. | Medan ini lalai untuk butiran baris sebut harga bagi kos yang dicipta secara automatik. |
| Unit Sumber | Cipta cepat | Unit penyumberan yang akan menanggung kos ini dan menyediakan sumber untuk mengusahakannya. | Nilai ini lalai untuk butiran baris sebut harga yang berkaitan bagi kos yang dicipta secara automatik dan digunakan dalam pengambilan semula harga kos. |
| Jadual unit | Cipta cepat | Kumpulan unit kerja, produk atau perbelanjaan. Unit yang tergolong dalam jadual seunit atau kumpulan unit. Contohnya, batu dan kilometers ialah unit yang tergolong dalam kumpulan unit yang menggambarkan jarak. | Nilai ini lalai kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Unit | Cipta cepat | Unit kerja, produk atau perbelanjaan. | Nilai ini lalai kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Kuantiti | Cipta cepat | Kuantiti kerja, produk atau perbelanjaan. | Nilai ini lalai kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Harga unit | Cipta Cepat |Kadar bil peranan yang melaksanakan kerja, harga unit produk atau harga jualan kategori produk atau perbelanjaan. Tetapan lalai untuk medan ini ialah **Masa** berdasarkan gabungan nilai dimensi penetapan harga pada baris harga peranan bagi senarai harga projek yang berkuat kuasa untuk tarikh mula. Untuk **Perbelanjaan**, lalai adalah daripada persediaan harga untuk kategori transaksi dalam senarai harga projek yang berkuat kuasa untuk tarikh mula. Jika kaedah penetapan harga untuk kategori transaksi bukan harga setiap unit, tiada tetapan lalai dan medan ini dibiarkan kosong. Untuk produk, tetapan lalai adalah berdasarkan baris **Item senarai harga** dalam senarai harga kos yang berkuat kuasa untuk tarikh mula.| Kadar kos peranan yang melaksanakan kerja, atau kos setiap unit kategori perbelanjaan atau kos unit produk. Tetapan lalai untuk medan ini ialah **Masa** berdasarkan gabungan nilai dimensi penetapan harga pada baris harga peranan bagi senarai harga projek yang berkuat kuasa untuk tarikh mula. Untuk **Perbelanjaan**, lalai adalah daripada persediaan harga untuk kategori transaksi dalam senarai harga projek yang berkuat kuasa untuk tarikh mula. Jika kaedah penetapan harga untuk kategori transaksi bukan harga setiap unit, tiada tetapan lalai dan medan ini dibiarkan kosong. Untuk produk, tetapan lalai adalah berdasarkan baris **Item senarai harga** dalam senarai harga kos yang berkuat kuasa untuk tarikh mula.|
| Anggaran Cukai | Cipta cepat | Anda boleh memasukkan cukai anggaran secara manual untuk kerja atau perbelanjaan ini. | Tiada kesan hiliran untuk medan ini. |
| Amaun | Cipta cepat | Anda boleh memasukkan maklumat input secara manual ke medan ini jika medan **Kuantiti** dan **Harga** dibiarkan kosong. Jika medan ini tidak kosong, medan ini menjadi baca sahaja dan dikira sebagai (Kuantiti \* Harga unit) + Cukai. | Tiada kesan hiliran untuk medan ini. |


## <a name="update-prices-on-quote-line-details"></a>Kemas kini harga untuk butiran baris sebut harga

Jika anda telah mengubah harga pada senarai harga projek yang dilampirkan pada sebut harga, atau pada senarai harga kos unit kontrak, anda boleh memilih **Mengira semula** pada halaman **Sebut harga** untuk menyegarkan semula harga pada butiran baris sebut harga individu untuk mencerminkan perubahan ini. Apabila anda memilih **Mengira semula**, amaran muncul yang memaklumkan kepada anda bahawa harga pada butiran baris sebut harga untuk semua baris sebut harga pada sebut harga ini akan ditetapkan semula. Pilih **Ya** untuk menyegarkan semula harga untuk jualan dan butiran baris sebut harga.

## <a name="access-quote-line-details-for-cost"></a>Akses butiran baris sebut harga untuk kos

Pada tab **Butiran baris sebut harga**, pilih baris dalam grid untuk mendayakan sesetengah tindakan pada bar alat subgrid. Tindakan pertama pada bar alat subgrid apabila butiran baris sebut harga dipilih adalah **Buka Butiran Kos**. Pilih **Buka Butiran Kos** untuk melihat kadar kos dan jumlah yang berkaitan untuk baris sebut harga ini.

> [!NOTE]
> Mengubah unit sumber, kuantiti, tarikh, peranan atau nilai kategori pada baris sebut harga butiran untuk kos akan mengubah nilai yang sesuai pada butiran baris sebut harga untuk jualan.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Mata wang untuk butiran baris sebut harga kos dan jualan

Mata wang pada baris sebut harga butiran untuk jualan lalai dari senarai harga projek yang berkesan untuk tarikh mula butiran baris sebut harga.

Mata wang pada butiran baris sebut harga untuk kos lalai dari senarai harga unit kontrak sebut harga yang berkuat kuasa pada tarikh mula butiran sebut harga untuk kos.

Pengiraan keuntungan menukar jumlah pada butiran baris sebut harga untuk kos dan jualan ke asas mata wang persekitaran untuk melaporkan jumlah margin yang dianggarkan pada sebut harga tersebut.

> [!NOTA
> > Ralat pembundaran mata wang dan margin yang ditukar boleh berlaku kerana kurangnya kadar pertukaran berkesan tarikh. Gunakan pengiraan ini hanya pada kontrak projek kerana ini ialah anggaran dan bukan untuk statutori aktual atau pelaporan lain yang memerlukan ketepatan pembundaran dan kesedaran yang lebih tinggi tentang penguatkuasaan tarikh untuk kadar pertukaran.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
