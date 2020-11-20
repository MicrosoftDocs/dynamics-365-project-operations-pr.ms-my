---
title: Urus unit kompleks untuk baris kontrak berdasarkan produk - lite
description: Topik ini memberikan maklumat mengenai menyokong jualan produk berasaskan langganan.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a58a13c8186f36e6031fe3c6f3c3a57ea920ac9e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177387"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Urus unit kompleks untuk baris kontrak berdasarkan produk - lite

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Dynamics 365 Project Operations menggunakan faktor kuantiti untuk menyokong jualan produk berasaskan langganan. Untuk produk berdasarkan langganan, kuantiti pada kontrak atau baris kontrak projek dinyatakan sebagai bilangan bulan pengguna.

Harga perisian langganan disimpan dalam katalog sebagai harga bagi setiap pengguna setiap bulan. Semasa proses jualan, harga pada baris kontrak biasanya adalah harga bagi setiap pengguna, setiap bulan yang telah dirundingkan dan terdiskaun oleh ejen jualan. Setiap urusan mempunyai bilangan pengguna yang berbeza dan bilangan bulan langganan yang berbeza. Kuantiti yang digunakan untuk mengira jumlah baris kontrak adalah produk bilangan pengguna dan bilangan bulan langganan.

Untuk menyokong jenis jualan ini, Project Operations menyokong konsep *faktor kuantiti*. Faktor kuantiti bergantung pada atribut produk. Apabila anda mengkonfigurasikan sifat khusus untuk produk, anda boleh menandakan subset sifat itu atau semua sifat itu, sebagai faktor kuantiti.

Project Operations mengesahkan bahawa hanya sifat angka atau sifat produk yang mempunyai jenis data berangka ditandakan sebagai faktor kuantiti. Apabila produk yang mempunyai faktor kuantiti yang dikonfigurasikan ditambah pada baris kontrak, medan **Kuantiti** menjadi baca sahaja. Selepas anda memasukkan nilai untuk sifat produk yang merupakan faktor kuantiti, Project Operations mengira kuantiti baris kontrak.

Contohnya, Dynamics 365 Sales mungkin mempunyai sifat berikut:

- **Bilangan pengguna**: Bilangan pengguna.
- **Bilangan Bulan**: Bilangan bulan langganan.
- **Produk SKU**: Unit penyimpanan stok (SKU) untuk produk tersebut.

Sifat **Bilangan Pengguna** dan **Bilangan Bulan** boleh ditanda sebagai faktor kuantiti dengan mengedit sifat baris produk.

Untuk mencipta faktor kuantiti daripada sifat produk, lengkapkan langkah berikut.

1. Pada **Project Operations**, pilih **Produk Jualan**.
2. Buka produk yang anda perlukan untuk menetapkan faktor kuantiti. Pastikan produk mempunyai sifat yang sudah ditetapkan.
3. Pada halaman **Maklumat Projek**, pilih tab **Faktor Kuantiti**.
4. Dalam subgrid, pilih **+ Pengiraan medan baharu**.
5. Masukkan nama **Faktor Kuantiti** dan pilih nilai sifat yang dipetakan kepada pengiraan medan.
6. Simpan dan tutup borang.
7. Ulangi langkah 2-6 untuk semua sifat yang bersama akan membentuk kuantiti untuk baris kontrak berasaskan produk.

Dengan faktor kuantiti yang disediakan, apabila pengguna mencipta baris kontrak untuk produk ini, kuantiti baris kontrak dikunci. Kuantiti kemudian dikira sebagai produk nilai sifat untuk baris kontrak tersebut.
