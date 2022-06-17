---
title: Anggarkan baris kontrak berasaskan projek - ringan
description: Artikel ini memberikan maklumat tentang menganggarkan garis kontrak berasaskan projek.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8b4379cc5822d08b55623f0f3d4d49791af90927
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914413"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Anggarkan baris kontrak berasaskan projek - ringan

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Dalam Dynamics 365 Project Operations, baris kontrak berdasarkan projek mempunyai butiran yang membantu menganggarkan kos dan potensi pendapatan kerja yang terlibat untuk menyampaikan baris kontrak.

Untuk menganggarkan baris kontrak berdasarkan projek, pergi ke tab **Butiran Baris Kontrak** pada **Baris Kontrak** berdasarkan projek.  Terdapat dua cara untuk mencipta anggaran pada baris kontrak berdasarkan projek:

   - Cipta anggaran secara langsung pada baris kontrak dengan menambah butiran baris kontrak secara manual.
   - Cipta projek dan pelan projek dan kemudian kaitkan projek dan tugas kepada baris kontrak projek. Ini membolehkan proses yang anda boleh mengimport anggaran pelan projek ke baris kontrak berdasarkan komponen yang disertakan dalam baris kontrak.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Cipta anggaran secara langsung pada baris kontrak berdasarkan projek

Untuk mencipta anggaran secara terus pada baris kontrak berdasarkan projek, ikut langkah ini:

1. Pergi ke baris kontrak dan pilih tab **Butiran Baris Kontrak**. Baris yang anda cipta pada tab ini diringkaskan dan dipaparkan sebagai **Nilai Kontrak** untuk **Baris Kontrak** ini. 
2. Dalam subgrid **Butiran Baris Kontrak**, pilih **Butiran Baris Kontrak Baharu**. Gelangsar cipta pantas dibuka. Medan berikut tersedia pada halaman **Butiran Baris Kontrak**.

| Medan | Lokasi | Penerangan | Kesan hiliran |
| --- | --- | --- | --- |
| **Perihalan** | **Cipta Cepat** | Perihalan mengenai anggaran tertentu. | Nilai ini lalai kepada butiran baris kontrak yang berkaitan untuk kos yang dicipta secara automatik. |
| **Kelas Transaksi** | **Cipta Cepat** | Ini merupakan senarai kelas transaksi yang disertakan dalam tab **Umum** baris kontrak berdasarkan projek. | Nilai ini lalai kepada butiran baris kontrak yang berkaitan untuk kos yang dicipta secara automatik. |
| **Pilih Produk** | **Cipta cepat** | Digunakan apabila kelas transaksi ialah **Bahan**. Anda boleh menentukan jika baris anggaran ini untuk produk (katalog) **Sedia ada** atau produk **Masukan manual**. | Nilai ini lalai kepada butiran baris kontrak yang berkaitan untuk kos yang dicipta secara automatik. |
| **Produk** | **Cipta cepat** | ID produk daripada katalog produk. Medan ini hanya didayakan apabila anda memilih **Produk sedia ada** dalam medan **Pilih Produk**. ID digunakan untuk mendapatkan kembali harga jualan daripada senarai harga projek pada kontrak. | Nilai ini lalai kepada butiran baris kontrak yang berkaitan untuk kos yang dicipta secara automatik. |
| **Produk Masukan Manual** | **Cipta cepat** | Medan teks untuk memasukkan nama produk. Medan ini hanya didayakan apabila anda memilih **Masukan Manual** dalam medan **Pilih Produk**.| Nilai ini lalai kepada butiran baris kontrak yang berkaitan untuk kos yang dicipta secara automatik. |
| **Peranan** | **Cipta Cepat** | Peranan orang yang melaksanakan kerja ini atau menanggung perbelanjaan ini. | Nilai ini lalai kepada butiran baris kontrak yang berkaitan untuk kos yang dicipta secara automatik.|
| **Kategori** | **Cipta Cepat** | Kategori bagi kerja atau perbelanjaan. |Nilai ini lalai kepada butiran baris kontrak yang berkaitan untuk kos yang dicipta secara automatik.|
| **Tarikh Mula** | **Cipta Cepat** | Tarikh mula kerja. | Nilai ini lalai kepada butiran baris kontrak yang berkaitan untuk kos yang dicipta secara automatik. |
| **Tarikh Tamat** | **Cipta Cepat** | Tarikh akhir kerja. | Nilai ini lalai kepada butiran baris kontrak yang berkaitan untuk kos yang dicipta secara automatik. |
| **Unit Sumber** | **Cipta Cepat** | Unit penyumberan yang menanggung kos ini dan menyediakan sumber untuk mengusahakannya. |Nilai ini lalai kepada butiran baris kontrak yang berkaitan untuk kos yang dicipta secara automatik dan digunakan dalam pengambilan semula harga kos. |
| **Jadual unit** | **Cipta cepat** | Kumpulan unit kerja, produk atau perbelanjaan. Unit yang tergolong dalam jadual seunit atau kumpulan unit. Contohnya, *batu* dan *kilometers (kms)* ialah unit yang tergolong dalam kumpulan unit yang menggambarkan jarak. | Nilai ini lalai kepada butiran baris kontrak yang berkaitan untuk kos yang dicipta secara automatik. |
| **Unit** | **Cipta Cepat** | Unit kerja, produk atau perbelanjaan. | Nilai ini lalai kepada butiran baris kontrak yang berkaitan untuk kos yang dicipta secara automatik. |
| **Kuantiti** | **Cipta Cepat** | Kuantiti kerja, produk atau perbelanjaan. | Nilai ini lalai kepada butiran baris kontrak yang berkaitan untuk kos yang dicipta secara automatik. |
| **Harga unit** | **Cipta Cepat** | Kadar bil peranan yang melaksanakan kerja, harga unit produk atau harga jualan kategori produk atau perbelanjaan. Medan ini lalai untuk **Masa** berdasarkan gabungan nilai dimensi penetapan harga pada baris harga peranan bagi senarai harga projek yang berkuat kuasa untuk tarikh mula. Untuk **Perbelanjaan**, lalai medan ini adalah daripada persediaan harga untuk kategori transaksi dalam senarai harga projek yang berkuat kuasa untuk tarikh mula. Jika kaedah penetapan harga untuk kategori urus niaga tidak **harga setiap unit**, tidak ada lalai, medan ini dibiarkan kosong. Untuk produk, lalai medan ini adalah berdasarkan baris **Item senarai harga** dalam senarai harga kos yang berkuat kuasa untuk tarikh mula.| Kadar kos peranan yang melaksanakan kerja, atau kos setiap unit kategori perbelanjaan atau kos unit produk. Medan ini lalai untuk **Masa** berdasarkan gabungan nilai dimensi penetapan harga pada baris harga peranan bagi senarai harga kos yang dilampirkan pada unit kontrak yang berkuat kuasa untuk tarikh mula. Untuk perbelanjaan, lalai medan ini berdasarkan pada garis harga kategori senarai harga kos yang dilampirkan pada unit kontrak yang berkuat kuasa pada tarikh mula. Jika kaedah penetapan harga untuk kategori transaksi bukan harga per unit, tidak ada default dan medan ini dibiarkan kosong. Untuk produk, lalai medan ini adalah berdasarkan baris **Item senarai harga** bagi senarai harga kos yang dilampirkan pada unit kontrak yang berkuat kuasa untuk tarikh mula.|
| **Anggaran Cukai** | **Cipta Cepat** | Cukai yang dianggarkan untuk kerja atau perbelanjaan ini. | Cukai yang dianggarkan untuk kerja atau perbelanjaan ini. |
| **Amaun** | **Cipta Cepat** | Anda boleh menambahkan nilai dalam medan ini jika medan **Kuantiti** dan **Harga** dibiarkan kosong. Jika **Kuantiti** dan **Harga** diisi, medan **Jumlah** ialah baca sahaja dan dikira sebagai **(Kuantiti \* Harga unit) + Cukai**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Kemas kini harga untuk butiran baris kontrak

Jika anda mengubah harga pada senarai harga projek yang dilampirkan kepada kontrak atau senarai harga kos unit kontrak, anda boleh menyegarkan semula harga pada butiran baris kontrak individu untuk menggambarkan perubahan tersebut. Pada halaman **Kontrak**, pilih **Pengiraan semula**. Amaran kelihatan untuk memaklumkan kepada anda bahawa harga untuk semua baris kontrak pada kontrak ini telah ditetapkan semula. Pilih **Ya** untuk menyegarkan semula harga untuk kedua-dua butiran baris jualan dan kos kontrak.

## <a name="access-contract-line-details-for-cost"></a>Mengakses butiran baris kontrak untuk kos

Pada tab **Butiran Baris Sebut harga**, pilih baris dalam grid untuk memaparkan tindakan pada bar alat subgrid. Tindakan pertama pada bar alat subgrid adalah **Buka Butiran Kos**. Untuk melihat kadar kos dan jumlah yang berkaitan untuk butiran baris kontrak ini, pilih **Buka Butiran Kos**. 

> [!NOTE]
> Mengubah syarikat persumberan semula, unit persumberan semula, kuantiti, tarikh, peranan atau nilai kategori pada baris kontrak butiran untuk **Kos** juga mengubah nilai yang sesuai pada baris kontrak butiran untuk **Jualan**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Mata wang dengan butiran baris kontrak untuk kos dan jualan

Baris kontrak butiran untuk **Jualan** menetapkan mata wang lalai daripada senarai harga projek yang berkesan untuk tarikh mula butiran baris kontrak.

Baris kontrak butiran untuk **Kos** menetapkan mata wang lalai daripada senarai harga projek yang berkuatkuasa untuk tarikh mula butiran baris kontrak untuk **Kos**.

Pengiraan keuntungan menukar jumlah untuk butiran baris kontrak untuk **Kos** dan **Jualan** ke mata wang asas persekitaran untuk melaporkan keseluruhan margin sebenar dan anggaran pada kontrak.

> [!NOTE]
> Ralat pembundaran mata wang dan margin yang ditukar boleh berlaku kerana kurangnya kadar pertukaran berkesan tarikh. Gunakan pengiraan ini hanya pada kontrak projek kerana ini ialah anggaran dan bukan untuk statutori aktual atau pelaporan lain yang memerlukan ketepatan pembundaran dan kesedaran yang lebih tinggi tentang penguatkuasaan tarikh untuk kadar pertukaran.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
