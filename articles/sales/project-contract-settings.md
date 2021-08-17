---
title: Tetapan kontrak projek
description: Topik ini memberikan maklumat tentang medan yang memberi kesan kepada baris kontrak dan maklumat tentang kontrak yang diringkaskan untuk merentasi semua item baris.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f34d6c6b92f164cc95405147356c34bb03eb127284aba7a92712b8eec42d792f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996312"
---
# <a name="header-details-for-project-based-contracts"></a>Butiran pengepala untuk kontrak berdasarkan projek

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Topik ini menyediakan maklumat mengenai medan yang digunakan untuk seluruh kontrak projek termasuk tetapan yang memberi kesan kepada semua baris kontrak. Maklumat mengenai kontrak yang diringkaskan merentasi semua item baris untuk mendorong KPI kontrak projek juga disertakan.

Jadual berikut menyenaraikan medan paada kontrak projek yang unik kepada Dynamics 365 Project Operations atau mempunyai beberapa perubahan penting dalam tingkah laku daripada pesanan jualan dalam Dynamics 365 Sales.

| Medan | Lokasi | Penerangan | Kesan hiliran |
| --- | --- | --- | --- |
| Jenis | Tab **Ringkasan** (tersembunyi) | Ini adalah medan set pilihan dengan pilihan berikut:</br>- **Berasaskan kerja** (Tersedia hanya apabila Operasi Projek dipasang)</br>- **Berasaskan item** (Tersedia hanya apabila Operasi Projek and Jualan dipasang)</br>- **Perkhidmatan berasaskan Penyelenggaraan** (Tersedia apabila Dynamics 365 Field Service dipasang) | Dalam Operasi Projek, nilai medan ini lalai untuk **Berasaskan kerja** dan mengklasifikasikan kontrak sebagai kontrak berasaskan projek. Kontrak sepatutnya berasaskan projek untuk mendayakan semua sambungan dan fungsi khusus projek. |
| Syarikat Pemilikan | Tab **Ringkasan** | Entiti sah yang akaun untuk kos dan hasil yang terakru daripada projek yang berkaitan dengan kontrak projek ini. Apabila kontrak dicipta daripada sebut harga, medan ini disalin daripada medan yang sepadan pada rekod sebut harga. | Syarikat pemilikan menyamai konsep entiti yang sah dalam modul Project Operations **Pengurusan projek dan perakaunan**. Semua kos dan hasil yang terakru daripada projek ini akan diambil kira dalam Lejar Umum syarikat pemilikan. |
| Pelanggan | Tab **Ringkasan** | Rujukan kepada syarikat atau rekod akaun pelanggan. Apabila kontrak dicipta daripada sebut harga, medan ini disalin daripada medan yang sepadan pada rekod sebut harga. | Mata wang pada lalai kontrak projek berdasarkan mata wang pelanggan. Mata wang boleh diubah sebelum kontrak disimpan. |
| Pengurus Akaun | Tab **Ringkasan** | Nama Pengurus Akaun untuk urusan ini. Apabila kontrak dicipta daripada sebut harga, medan ini disalin daripada medan yang sepadan pada rekod sebut harga. | Pengurus Akaun bertanggungjawab untuk menguruskan perhubungan dengan pelanggan melalui penyelesaian projek ini. Berdasarkan rekod sumber boleh ditempah yang terikat dengan Pengurus Akaun, lalai unit kontrak pada kontrak projek. |
| Unit Pengkontrakan | Tab **Ringkasan** | Unit organisasi yang bertanggungjawab untuk penghantaran projek yang berkaitan dengan kontrak ini. Apabila kontrak dicipta daripada sebut harga, medan ini disalin daripada medan yang sepadan pada rekod sebut harga. | Unit kontrak adalah divisyen syarikat yang akan melaksanakan projek. Setiap unit pengkontrakan mempunyai mata wang dan mata wang ini digunakan untuk melaporkan kos anggaran dan sebenar yang berlaku semasa projek. |
| Senarai Harga Produk | Tab **Ringkasan** | Senarai harga ini digunakan untuk harga lalai pada baris kontrak berasaskan produk. Senarai pilihan juntai bawah untuk medan ini menunjukkan senarai harga yang mana mata wang senarai harga sepadan dengan mata wang pada kontrak. Apabila kontrak dicipta daripada sebut harga, medan ini disalin daripada medan yang sepadan pada rekod sebut harga. Pada kontrak projek, medan ini dilalaikan daripada rekod akaun tetapi boleh ditukar. | Tiada keterkaitan hiliran untuk medan ini. |
| Mata wang | Tab **Ringkasan** | Mata wang yang digunakan untuk melaporkan nilai urusan ini dan mata wang yang pelanggan akan diinvois. Apabila kontrak dicipta daripada sebut harga, medan ini disalin daripada medan yang sepadan pada rekod sebut harga. Pada kontrak projek, medan ini dilalaikan daripada rekod akaun tetapi boleh ditukar. | Selepas kontrak disimpan, medan ini tidak lagi boleh diedit. Medan ini digunakan untuk melalaikan senarai harga produk dan projek pada kontrak. Mata wang pada kontrak digunakan untuk dipadankan dengan mata wang pada senarai harga. |
| Had yang tidak boleh Melebihi | Tab **Ringkasan** | Medan ini menunjukkan atas rundingan pada nilai akhir yang pelanggan bersetuju untuk urusan ini. | Atas dinilai semasa pelaksanaan dan diguna pakai merentasi semua item baris dan projek berkaitan dengan urusan ini. |
| Tarikh Penghantaran Diminta | Tab **Ringkasan** | Apabila kontrak dicipta daripada sebut harga projek, medan ini disalin daripada medan yang sepadan pada sebut harga projek. | Tarikh ini digunakan sebagai tarikh akhir untuk menjana jadual invois. |

KPI berikut tersedia pada tab **Prestasi Kontrak** kontrak projek.

| Medan | Lokasi | Penerangan |
| --- | --- | --- |
| Nilai Kontrak | Keseluruhan kontrak | Jumlah nilai kontrak Projek. |
| Amaun Dibilkan | Keseluruhan kontrak | Jumlah amaun ke atas semua invois terhadap kontrak ini. |
| Kos Dikenakan | Keseluruhan kontrak | Jumlah semua kos aktual log masuk ke semua projek yang dipetakan ke kontrak. |
| Margin Kasar | Keseluruhan kontrak | Amaun dibilkan - Kos dikenakan sehingga kini / Amaun dibilkan |
| Margin Jangkaan | Keseluruhan kontrak | (Nilai kontrak - Kos anggaran) / Nilai kontrakKos anggaran = Jumlah semua kos anggaran pada semua projek yang dipetakan ke kontrak.|
| Nilai Kontrak | Baris berdasarkan projek | Nilai baris kontrak. |
| Amaun dibilkan | Baris berdasarkan projek | Untuk baris kontrak harga tetap: Jumlah amaun pada semua pencapaian sebenar jualan dibilkan terhadap baris kontrak ini pada pelbagai invois yang dicipta untuk kontrak ini. Untuk baris kontrak masa dan bahan: Jumlah amaun pada semua jualan sebenar dibilkan boleh dituntut terhadap baris kontrak ini pada pelbagai invois yang dicipta untuk kontrak ini. |
| Kos Dikenakan | Baris berdasarkan projek | Jumlah semua kos sebenar dilogkan ke semua projek yang dipetakan ke baris kontrak. |
| Margin Kasar | Baris berdasarkan projek | (Amaun dibilkan - Kos Dikenakan sehingga kini) / Amaun dibilkan |
| Margin Jangkaan | Baris berdasarkan projek | (Amaun baris kontrak dalam mata wang asas - Kos anggaran untuk baris kontrak dalam mata wang asas) / Amaun baris kontrak dalam mata wang asas |
| Kos Dikenakan | Butiran baris berasaskan projek | Masa: Jumlah amaun pada kos masa sebenar yang telah dilogkan untuk peranan ini pada projek dipetakan ke baris kontrak. Perbelanjaan: Jumlah amaun pada semua kos perbelanjaan sebenar yang telah dilogkan untuk kategori ini pada projek dipetakan ke baris kontrak. |
| Kuantiti Didaftar | Butiran baris berasaskan projek | Masa: Semua kuantiti masa pada kos masa sebenar untuk peranan pada projek yang dipetakan ke baris kontrak ini. Perbelanjaan: Semua kuantiti untuk kategori perbelanjaan ini pada kos perbelanjaan sebenar pada projek yang dipetakan ke baris kontrak ini. |
| Amaun Dibilkan | Butiran baris berasaskan projek | Untuk baris kontrak harga tetap, medan ini dibiarkan kosong pada tahap butiran dan hanya ditunjukkan pada peringkat baris kontrak. Untuk baris kontrak masa dan bahan, pengiraan diselesaikan pada tahap butiran. Butiran menunjukkan jumlah amaun pada semua baris hasil yang dibilkan terhadap baris kontrak ini yang boleh dituntut. |
| Kuantiti Dibilkan | Butiran baris berasaskan projek | Untuk baris kontrak harga tetap, medan ini dibiarkan kosong pada tahap butiran dan hanya ditunjukkan pada peringkat baris kontrak. Untuk baris kontrak masa dan bahan, pengiraan diselesaikan pada tahap butiran untuk masa dan perbelanjaan. Masa: Jumlah jam pada semua baris hasil yang dibilkan untuk peranan ini terhadap baris kontrak ini yang boleh dituntut. Perbelanjaan: Semua kuantiti untuk kategori perbelanjaan ini pada kos perbelanjaan sebenar pada projek yang dipetakan ke baris kontrak ini. |
| Nilai Kontrak | Baris berdasarkan produk | Nilai baris kontrak bagi baris kontrak berasaskan produk ini. |
| Amaun Dibilkan | Baris berdasarkan produk | Jumlah amaun pada semua baris invois terhadap baris kontrak berasaskan produk ini pada pelbagai invois yang dicipta untuk kontrak ini. |
| Kos Dikenakan | Baris berdasarkan produk | Jumlah semua kos sebenar dilogkan untuk baris kontrak berasaskan produk. |
| Margin Kasar | Baris berdasarkan projek | Amaun dibilkan - Kos dikenakan sehingga kini / Amaun dibilkan |
| Margin Jangkaan | Baris berdasarkan produk | (Nilai baris kontrak - Kos anggaran untuk baris kontrak) / Nilai baris kontrak |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
