---
title: Mengurus unit kompleks seperti mengikut setiap pengguna, setiap bulan untuk baris sebut harga berasaskan produk - lite
description: Topik ini menyediakan maklumat tentang mengurus unit kompleks untuk baris sebut harga berasaskan projek.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2ee46da2f663ef4f5f8fc7f9f89b6fcfd09a1798
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175587"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a>Mengurus unit kompleks seperti mengikut setiap pengguna, setiap bulan untuk baris sebut harga berasaskan produk - lite

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Dynamics 365 Project Operations menggunakan faktor kuantiti untuk menyokong jualan produk berasaskan langganan. Untuk produk berasaskan langganan, kuantiti pada sebut harga atau baris kontrak projek dinyatakan sebagai bilangan bulan pengguna.

Biasanya, harga perisian langganan disimpan dalam katalog sebagai harga bagi setiap pengguna setiap bulan. Semasa proses jualan, harga pada baris sebut harga biasanya adalah harga bagi setiap pengguna, setiap bulan yang telah dirundingkan dan terdiskaun oleh ejen jualan IT. Setiap urusan mempunyai bilangan pengguna yang berbeza dan bilangan bulan langganan yang berbeza. Kuantiti yang digunakan untuk mengira baris sebut harga adalah produk bilangan pengguna dan bilangan bulan langganan.

Untuk menyokong jenis jualan ini, Project Operations memperkenalkan konsep faktor kuantiti. Faktor kuantiti bergantung pada atribut produk dalam Dynamics 365. Apabila anda mengkonfigurasi sifat khusus untuk produk, Project Operations membolehkan anda menandakan subset atau semua sifat tersebut, sebagai faktor kuantiti.

Project Operations mengesahkan bahawa hanya sifat angka atau sifat produk yang mempunyai jenis data berangka ditandakan sebagai faktor kuantiti. Apabila anda menambah produk dengan faktor kuantiti pada baris sebut harga, medan **Kuantiti** menjadi baca sahaja. Selepas anda memasukkan nilai untuk sifat produk yang merupakan faktor kuantiti, Project Operations mengira kuantiti baris sebut harga.

Contohnya, Dynamics 365 Sales mungkin mempunyai sifat berikut:

- **Bilangan pengguna**: Bilangan pengguna
- **Bilangan bulan**: Bilangan bulan langganan
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]