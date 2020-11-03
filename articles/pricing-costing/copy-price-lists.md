---
title: Salin senarai harga
description: Topik ini menyediakan maklumat tentang cara menyalin senarai harga dalam Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 91ee798a206ea5200780c8ebafc8f99cd9a3e219
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081267"
---
# <a name="copy-price-lists"></a>Salin senarai harga

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Anda boleh mencipta salinan senarai harga dalam Dynamics 365 Project Operations. Contohnya, anda boleh mencipta senarai harga untuk tahun akan datang menggunakan senarai harga daripada tahun semasa.  Atau anda mungkin menyalin senarai harga untuk kadar bil dan harga jualan daripada senarai harga untuk kos. 

Untuk membuat salinan senarai harga, lengkapkan langkah berikut.

1. Buka senarai harga yang anda mahu membuat salinan dan pilih **Salin**.
2. Masukkan sebarang maklumat yang diperlukan untuk menyalin senarai harga. Jadual berikut menunjukkan pertimbangan yang perlu diingat apabila memasukkan maklumat.

| Medan | Keterkaitan, tujuan dan panduan | Kesan hiliran |
| --- | --- | --- |
| Nama | Nama senarai harga sumber dengan **-salin** ditambah. | Senarai harga termasuk nilai ini pada semua halaman senarai dan pilihan juntai bawah. |
| Konteks | Masukkan konteks yang anda mahu untuk senarai harga sasaran. | Senarai harga mempunyai set konteks ke **Kos** digunakan untuk mencari harga bagi kos anggaran dan kos aktual. Senarai harga mempunyai set konteks ke **Jualan** digunakan untuk mencari jualan bagi jualan anggaran dan jualan aktual. Hanya senarai harga yang mempunyai set konteks ke **Jualan** boleh dilampirkan ke senarai harga projek untuk pelanggan, sebut harga atau kontrak. |
| Tarikh Mula | Tarikh mula tempoh senarai harga berkuat kuasa. | Bersama dengan **Tarikh Akhir** , medan ini digunakan untuk menentukan senarai harga yang berkenaan untuk anggaran tertentu atau baris aktual. |
| Tarikh Tamat | Tarikh akhir tempoh senarai harga berkuat kuasa. | Bersama dengan **Tarikh Mula** , medan ini digunakan untuk menentukan senarai harga yang berkenaan untuk anggaran tertentu atau baris aktual. |
| Mata wang | Mata wang senarai harga sumber. Ini boleh diubah. | Apabila ini diubah, semua baris harga untuk buruh, perbelanjaan dan katalog produk yang terhasil ditukar kepada mata wang senarai harga sasaran semasa salinan. |
| Unit Masa | Mata wang senarai harga sumber. Ini boleh diubah. | Apabila ini diubah, semua baris harga untuk item buruh yang terhasil ditukar kepada unit senarai harga sasaran semasa salinan. Penukaran daripada persediaan unit untuk unit senarai harga sumber dan unit masa senarai harga sasaran digunakan. |
| Penerangan  | Perihalan senarai harga sumber dengan **-salin** ditambah. Ini adalah medan teks dan membenarkan anda mempunyai perihalan berbilang baris pada senarai harga. | Medan ini ditunjukkan dalam pandangan **Berkaitan** pada senarai harga dalam pelbagai entiti yang mempunyai senarai harga berkaitan.. |

3. Simpan senarai harga. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Kemas kini senarai harga dengan menggunakan tokokan untuk semua harga

1. Pada tab **Peranan** , **Kategori** dan **Item Senarai Harga** pada senarai harga, anda boleh memilih **Kemas Kini Harga** untuk menggunakan tokokan bagi semua harga dalam sub grid. 
2. Pada halaman dialog yang terbuka, masukkan tokokan. Anda juga boleh memasukkan peratus tokokan negatif untuk menurunkan harga mengikut peratusan tertentu. 
3. Pilih **OK** pada halaman dialog dan kemudian sahkan harga dalam sub grid menunjukkan perubahan yang anda lakukan.
