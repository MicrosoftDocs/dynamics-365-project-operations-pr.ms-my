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
ms.openlocfilehash: 029d2aa4fd20fc036a34ae6136fe12454f3b7703
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273344"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Urus unit kompleks untuk baris kontrak berdasarkan produk - lite

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Dynamics 365 Project Operations menggunakan faktor kuantiti untuk menyokong jualan produk berdasarkan langganan. Untuk produk berdasarkan langganan, kuantiti pada kontrak atau baris kontrak projek dinyatakan sebagai bilangan bulan pengguna.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]