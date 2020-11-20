---
title: Anggarkan baris kontrak berdasarkan projek
description: Topik ini menyediakan maklumat mengenai anggaran pada baris kontrak berdasarkan projek.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24299d997074efcff3776168652809d490c81b17
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180473"
---
# <a name="estimate-a-projectbased-contract-line"></a>Anggarkan baris kontrak berdasarkan projek

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_ 

Dalam Dynamics 365 Project Operations, suatu baris kontrak berdasarkan projek mempunyai butiran yang membantu menganggarkan kos dan potensi pendapatan kerja yang terlibat untuk menyampaikan baris kontrak.

Untuk menganggarkan baris kontrak berdasarkan projek, pergi ke tab **Butiran Baris Kontrak** pada **Baris Kontrak** berdasarkan projek.  Terdapat dua cara untuk mencipta anggaran pada baris kontrak berdasarkan projek:

   - Cipta anggaran secara langsung pada baris kontrak dengan menambah butiran baris kontrak secara manual.
   - Cipta projek dan pelan projek dan kemudian kaitkan projek dan tugas kepada baris kontrak projek. Ini membolehkan proses yang anda boleh mengimport anggaran pelan projek ke baris kontrak berdasarkan komponen yang disertakan dalam baris kontrak.

## <a name="create-an-estimate-directly-on-a-projectbased-contract-line"></a>Cipta anggar secara langsung pada baris kontrak berdasarkan projek

1. Pergi ke baris kontrak dan pilih tab **Butiran Baris Kontrak**. Baris yang anda cipta pada tab ini diringkaskan dan dipaparkan sebagai **Nilai Kontrak** untuk **Baris Kontrak** ini. 
2. Dalam subgrid **Butiran Baris Kontrak**, pilih **+ Butiran Baris Kontrak Baharu**. Gelangsar cipta pantas dibuka. Medan berikut tersedia pada borang **Butiran baris kontrak**:

| Medan | Lokasi | Penerangan  | Kesan hiliran |
| --- | --- | --- | --- |
| **Perihalan** | **Cipta Cepat** | Perihalan mengenai anggaran tertentu. | Medan ini lalai kepada butiran baris kontrak berkaitan untuk kos yang dicipta secara automatik. |
| **Kelas Transaksi** | **Cipta Cepat** | Senarai juntai bawah ini ialah senarai kelas transaksi yang disertakan dalam tab **Umum** bagi baris kontrak berdasarkan projek. | Medan ini lalai kepada butiran baris kontrak berkaitan untuk kos yang dicipta secara automatik. |
| **Peranan** | **Cipta Cepat** | Peranan orang yang melaksanakan kerja ini atau menanggung perbelanjaan ini. | Medan ini lalai kepada butiran baris kontrak berkaitan untuk kos yang dicipta secara automatik. |
| **Kategori** | **Cipta Cepat** | Kategori bagi kerja atau perbelanjaan. | Medan ini lalai kepada butiran baris kontrak berkaitan untuk kos yang dicipta secara automatik. |
| **Tarikh Mula** | **Cipta Cepat** | Tarikh mula kerja. | Medan ini lalai kepada butiran baris kontrak berkaitan untuk kos yang dicipta secara automatik. |
| **Tarikh Tamat** | **Cipta Cepat** | Tarikh akhir kerja. | Medan ini lalai kepada butiran baris kontrak berkaitan untuk kos yang dicipta secara automatik. |
| **Syarikat Penyumberan** | **Cipta Cepat** | Syarikat pensumberan semula atau entiti sah yang menanggung kos ini dan menyediakan sumber untuk bekerja ke atasnya. | Medan ini lalai kepada butiran baris kontrak berkaitan untuk kos yang dicipta secara automatik. Medan ini juga digunakan dalam mendapatkan kembali harga kos. |
| **Unit Sumber** | **Cipta Cepat** | Unit persumberan semula yang menyebabkan kos ini dan menyediakan sumber untuk bekerja di atasnya. | Medan ini lalai kepada butiran baris kontrak berkaitan untuk kos yang dicipta secara automatik. Medan ini juga digunakan dalam mendapatkan kembali harga kos. |
| **Jadual unit** | **Cipta cepat** | Kumpulan unit bagi kerja atau perbelanjaan tersebut. Unit yang tergolong dalam jadual seunit atau kumpulan unit. Contohnya, *batu* dan *kilometers (Kms)* ialah unit yang tergolong dalam kumpulan unit yang menggambarkan jarak. | Medan ini lalai kepada butiran baris kontrak berkaitan untuk kos yang dicipta secara automatik. |
| **Unit** | **Cipta Cepat** | Unit bagi kerja atau perbelanjaan. | Medan ini lalai kepada butiran baris kontrak berkaitan untuk kos yang dicipta secara automatik. |
| **Kuantiti** | **Cipta Cepat** | Kuantiti bagi kerja atau perbelanjaan. | Medan ini lalai kepada butiran baris kontrak berkaitan untuk kos yang dicipta secara automatik. |
| **Harga unit** | **Cipta Cepat** | Kadar bil peranan yang menjalankan kerja atau harga jualan kategori belanja. Medan ini lalai untuk **Masa** berdasarkan kombinasi peranan dan unit pesumberan semula pada senarai harga projek yang berkesan untuk tarikh mula. Untuk perbelanjaan, lalai medan ini ialah daripada persediaan harga untuk kategori transaksi dalam senarai harga projek yang berkesan untuk tarikh mula. Jika kaedah penetapan harga untuk kategori urus niaga tidak **harga setiap unit**, tidak ada lalai, medan ini dibiarkan kosong. | Kadar kos peranan yang menjalankan kerja atau kos setiap unit kategori belanja. Lapangan ini lalai untuk **Masa berdasarkan peranan** dan kombinasi unit persumberan semula pada baris harga peranan senarai harga kos yang dilampirkan kepada unit kontrak yang berkuatkuasa untuk tarikh mula. Untuk perbelanjaan, lalai medan ini berdasarkan pada garis harga kategori senarai harga kos yang dilampirkan pada unit kontrak yang berkuat kuasa pada tarikh mula. Jika kaedah penetapan harga untuk kategori transaksi bukan harga per unit, tidak ada default dan medan ini dibiarkan kosong. |
| **Anggaran Cukai** | **Cipta Cepat** | Anggaran cukai untuk kerja atau perbelanjaan ini sebagai input oleh pengguna. | Anggaran cukai untuk kerja atau perbelanjaan ini sebagai input oleh pengguna. |
| **Amaun** | **Cipta Cepat** | Ini nilai dalam medan ini boleh ditambah oleh pengguna jika medan **Kuantiti** dan **Harga** dibiarkan kosong. Jika **Kuantiti** dan **Harga** diisi, medan **Jumlah** adalah baca sahaja dan dikira sebagai **(Kuantiti \* Harga unit) + Cukai**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Kemas kini harga untuk butiran baris kontrak

Jika anda mengubah harga pada senarai harga projek yang dilampirkan kepada kontrak atau senarai harga kos unit kontrak, anda boleh menyegarkan semula harga pada butiran baris kontrak individu untuk menggambarkan perubahan tersebut. Pada halaman **Kontrak**, pilih **Pengiraan semula**. Amaran dibuka untuk memaklumkan kepada anda bahawa harga untuk semua baris kontrak dalam kontrak ini akan ditetapkan semula. Pilih **Ya** untuk menyegarkan semula harga untuk kedua-dua butiran baris jualan dan kos kontrak.

## <a name="access-contract-line-details-for-cost"></a>Mengakses butiran baris kontrak untuk kos

Pada tab **Butiran Baris Sebut harga**, pilih baris dalam grid untuk memaparkan tindakan pada bar alat subgrid. Tindakan pertama pada bar alat subgrid adalah **Buka Butiran Kos**. Untuk melihat kadar kos dan jumlah yang berkaitan untuk butiran baris kontrak ini, pilih **Buka Butiran Kos**. 

> [!NOTE]
> Mengubah syarikat persumberan semula, unit persumberan semula, kuantiti, tarikh, peranan atau nilai kategori pada baris kontrak butiran untuk **Kos** juga mengubah nilai yang sesuai pada baris kontrak butiran untuk **Jualan**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Mata wang dengan butiran baris kontrak untuk kos dan jualan

Baris kontrak butiran untuk **Jualan** menetapkan mata wang lalai daripada senarai harga projek yang berkesan untuk tarikh mula butiran baris kontrak.

Baris kontrak butiran untuk **Kos** menetapkan mata wang lalai daripada senarai harga projek yang berkuatkuasa untuk tarikh mula butiran baris kontrak untuk **Kos**.

Pengiraan keuntungan menukar jumlah untuk butiran baris kontrak untuk **Kos** dan **Jualan** ke mata wang asas persekitaran untuk melaporkan keseluruhan margin sebenar dan anggaran pada kontrak.

> [!NOTE]
> Ralat pembundaran mata wang dan margin yang ditukar boleh berlaku kerana kurangnya kadar pertukaran berkesan tarikh. Gunakan pengiraan ini pada kontrak projek hanya sebagai anggaran dan bukan untuk laporan statutori yang sebenar atau lain yang memerlukan kejituan yang lebih tinggi untuk pembundaran dan kesedaran tarikh effectivity untuk kadar pertukaran.
