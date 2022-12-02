---
title: Sediakan dan gunakan bayar apabila pembayaran vendor dibayar
description: Artikel ini menjelaskan cara untuk mencipta terma bayar apabila dibayar (PWP) supaya anda boleh mengeluarkan pembayaran vendor separa, berdasarkan pembayaran pelanggan.
author: RadhikaRS
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 10e8e57695caece6c4b6ba4c2ddb52395dad1218
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920761"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Sediakan dan gunakan bayar apabila pembayaran vendor dibayar

[!include [banner](../includes/banner.md)]

Apabila anda meluluskan vendor untuk bekerja sebagai subkontraktor, anda mungkin mahu menangguhkan pembayaran kepada vendor sehingga pelanggan anda membayar anda untuk projek tersebut. Untuk menyokong senario ini, anda boleh menyediakan terma bayar apabila dibayar (PWP) semasa anda menyediakan pesanan pembelian (PO) dengan vendor.

Sebagai contoh, apabila pelanggan membayar jumlah pada invois projek, anda boleh mengeluarkan sebahagian atau semua jumlah invois vendor. Hanya sediakan terma PWP yang menentukan bahawa vendor akan dibayar selepas anda menerima peratusan daripada pembayaran yang berkaitan daripada pelanggan. Jika anda menerima pembayaran separa daripada pelanggan, anda boleh mengeluarkan beberapa invois vendor berkaitan untuk pembayaran secara manual.

Contoh berikut menghuraikan proses apabila terma PWP digunakan.

## <a name="example"></a>Contoh

Organisasi anda bersetuju untuk menyediakan pelanggan dengan 100 komputer yang mempunyai perisian yang dipasang, dengan harga dolar AS (USD) 150.00 bagi setiap komputer. Anda kemudian mengupah vendor untuk menyediakan komputer yang mempunyai perisian yang dipasang kepada anda. Menurut perjanjian, pelanggan mesti meluluskan kualiti komputer sebelum ia membayar organisasi anda. Dasar organisasi anda ialah untuk menahan pembayaran kepada vendor sehingga pelanggan telah membayar anda. Oleh itu, anda menetapkan projek supaya ia mempunyai peratusan PWP 100 peratus.

Vendor menghantar anda 100 komputer yang mempunyai perisian yang dipasang bersama invois sebanyak USD 10,000.00. Oleh sebab terma PWP disediakan untuk projek anda, anda tidak akan membayar vendor apabila menerima komputer. Sebaliknya, anda menghantar komputer kepada pelanggan, bersama dengan invois sebanyak 15,000.00. Pelanggan memeriksa komputer dan meluluskan jumlah penuh invois projek.

Selepas anda menerima bayaran penuh daripada pelanggan, anda membayar 10,000.00 kepada vendor, jumlah penuh invois vendor.

## <a name="set-up-pwp-terms-for-a-project"></a>Sediakan terma PWP untuk projek

Apabila anda menyediakan terma PWP untuk projek, anda mesti menetapkan, sebagai peratusan, jumlah minimum yang pelanggan mesti membayar anda untuk projek sebelum anda akan membayar vendor. Jumlah ambang dikira secara automatik pada invois pelanggan untuk projek. Ikuti langkah ini untuk menetapkan peratusan ambang bagi terma PWP.

1. Pergi ke **Pengurusan dan perakaunan projek** \> **Projek** \> **Semua projek**.
2. Cari dan buka projek yang anda mahu sediakan terma PWP untuknya.
3. Pada FastTab **Perjanjian vendor**, pilih **Tambah baris**.
3. Dalam medan **Kod akaun**, pilih salah satu daripada pilihan berikut:

    - **Jadual** – Terma PWP digunakan pada vendor tunggal.
    - **Kumpulan** – Terma PWP digunakan pada semua vendor dalam kumpulan vendor.
    - **Semua** – Terma PWP digunakan kepada semua vendor.

4. Jika anda memilih **Jadual** atau **Kumpulan** dalam langkah sebelumnya, dalam medan **Vendor/Kumpulan vendor**, pilih vendor atau kumpulan vendor yang digunakan oleh terma PWP. Jika anda memilih **Semua** dalam langkah sebelumnya, medan **Vendor/Kumpulan vendor** tidak boleh diedit.
5. Jika terma pengekalan vendor disediakan untuk vendor dalam projek, dalam medan **Terma pengekalan vendor**, pilih ID peraturan untuk terma pengekalan.
6. Dalam medan **peratusan ambang PWP**, masukkan peratusan ambang untuk projek. Peratusan yang anda masukkan untuk projek ini mentakrifkan jumlah minimum yang pelanggan mesti bayar kepada anda sebelum anda akan membayar vendor.

## <a name="create-a-po-that-has-pwp-terms"></a>Cipta PO yang mempunyai terma PWP

Apabila anda menyiarkan invois daripada vendor, jika vendor tertakluk kepada terma PWP, terma tersebut ditunjukkan pada baris PO. Untuk mencipta PO yang mempunyai terma PWP, ikuti langkah ini.

1. Pergi ke **Perolehan dan penyumberan** \> **Pesanan pembelian** \> **Semua pesanan pembelian**.
2. Pada Anak Tetingkap Tindakan, pilih **Baharu**. Kemudian, dalam kotak dialog **Cipta pesanan pembelian**, masukkan maklumat yang diperlukan dan pilih **OK**.

    Secara alternatif, buka PO sedia ada pada halaman senarai **Semua pesanan pembelian**.

4. Pada halaman **Pesanan pembelian**, pada FastTab **Baris pesanan pembelian**, semak semula butiran baris Po untuk vendor. Pilihan **Bayar apabila dibayar** dipilih secara automatik dan nilai dalam medan **peratusan ambang PWP** akan disalin secara automatik daripada medan **peratusan ambang PWP** pada halaman **Projek**.
6. Jika anda tidak mahu menggunakan terma PWP kepada vendor untuk baris PO, kosongkan pilihan **bayar apabila dibayar**. Dalam kes ini, medan **peratusan ambang PWP** untuk baris PO akan ditetapkan semula kepada 0 (sifar).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Kemas kini pembayaran pelanggan dan bayar vendor tersebut

Apabila vendor melengkapkan kerjanya pada projek dan menghantar invois kepada anda, anda mesti menyemak semula status projek dan invois pelanggan untuk menentukan sama ada terma PWP telah dipenuhi untuk projek tersebut. Jika terma PWP untuk vendor dipenuhi, anda boleh menentukan baris yang ada pada invois vendor perlu dibayar, berdasarkan pembayaran pelanggan untuk projek tersebut. Jika anda memutuskan untuk membayar vendor walaupun terma PWP tidak dipenuhi, anda boleh mengganti terma PWP pada halaman **Invois vendor dengan bayar apabila dibayar**.

1. Pergi ke **Pengurusan projek dan perakaunan** \> **Pertanyaan dan laporan** \> **Pertanyaan pengekalan** \> **Invois vendor dengan bayar apabila dibayar**.
2. Pada halaman **Invois vendor dengan bayar apabila dibayar**, dalam medan carian, masukkan nilai untuk mencari invois vendor yang anda mahu semak semula dan kemudian pilih **Carian**.
3. Pada FastTab **Baris invois vendor**, pilih baris yang anda mahu tukar.
4. Jika syarat **Bayar apabila dibayar** dipenuhi untuk baris invois, pilih **Keluarkan pembayaran vendor**. Pilihan **Bayar apabila dibayar** dikosongkan dan nilai medan **Bersedia untuk pembayaran** ditukar kepada **Ya**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]