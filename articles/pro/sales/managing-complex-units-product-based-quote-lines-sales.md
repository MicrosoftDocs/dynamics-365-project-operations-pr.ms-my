---
title: Mengurus unit kompleks seperti setiap pengguna, setiap bulan untuk baris sebut harga berasaskan produk
description: Topik ini menyediakan maklumat tentang mengurus unit kompleks untuk baris sebut harga berasaskan projek.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 741230e69302138cce8f7379f520f7178e1c80af
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081160"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines"></a>Mengurus unit kompleks seperti setiap pengguna, setiap bulan untuk baris sebut harga berasaskan produk

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Dynamics 365 Project Operations menggunakan faktor kuantiti untuk menyokong jualan produk berasaskan langganan. Untuk produk berasaskan langganan, kuantiti pada sebut harga atau baris kontrak projek dinyatakan sebagai bilangan bulan pengguna.

Biasanya, harga perisian langganan disimpan dalam katalog sebagai harga bagi setiap pengguna setiap bulan. Semasa proses jualan, harga pada baris sebut harga biasanya adalah harga bagi setiap pengguna, setiap bulan yang telah dirundingkan dan terdiskaun oleh ejen jualan IT. Setiap urusan mempunyai bilangan pengguna yang berbeza dan bilangan bulan langganan yang berbeza. Kuantiti yang digunakan untuk mengira baris sebut harga adalah produk bilangan pengguna dan bilangan bulan langganan.

Untuk menyokong jenis jualan ini, Project Operations memperkenalkan konsep faktor kuantiti. Faktor kuantiti bergantung pada atribut produk dalam Dynamics 365. Apabila anda mengkonfigurasi sifat khusus untuk produk, Project Operations membolehkan anda menandakan subset atau semua sifat tersebut, sebagai faktor kuantiti.

Project Operations mengesahkan bahawa hanya sifat angka atau sifat produk yang mempunyai jenis data berangka ditandakan sebagai faktor kuantiti. Apabila anda menambah produk dengan faktor kuantiti pada baris sebut harga, medan **Kuantiti** menjadi baca sahaja. Selepas anda memasukkan nilai untuk sifat produk yang merupakan faktor kuantiti, Project Operations mengira kuantiti baris sebut harga.

Contohnya, Dynamics 365 Sales mungkin mempunyai sifat berikut:

- **Bilangan pengguna** : Bilangan pengguna
- **Bilangan bulan** : Bilangan bulan langganan
- **SKU Produk**

Anda boleh menandakan sifat **Bilangan Pengguna** dan **Bilangan Bulan** sebagai faktor kuantiti dengan mengedit sifat baris produk.

Untuk mencipta faktor Kuantiti daripada sifat Produk, ikuti langkah berikut:

1. Pada tetingkap navigasi kiri Project Operations, pergi ke **Jualan** > **Produk**.
2. Buka produk yang anda perlukan untuk mengkonfigurasi faktor kuantiti. Pastikan produk mempunyai sifat yang telah pun dikonfigurasi.
3. Pada halaman **Maklumat Projek** untuk Produk, pilih tab **Faktor Kuantiti**.
4. Dalam subgrid, pilih **+ Pengiraan medan baharu**.
5. Masukkan nama faktor Kuantiti dan pilih nilai sifat yang dipetakan kepada pengiraan medan.
6. Simpan dan tutup borang. Ulangi langkah ini untuk semua sifat yang digunakan untuk pengkomputeran kuantiti untuk baris sebut harga berasaskan produk.

Apabila anda mencipta baris sebut harga berasaskan produk untuk produk, kuantiti baris sebut harga akan dikunci. Kuantiti akan dikira sebagai produk nilai sifat yang anda masukkan untuk baris sebut harga tersebut.
