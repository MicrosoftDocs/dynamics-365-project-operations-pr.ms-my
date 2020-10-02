---
title: Produk
description: Topik ini menyediakan maklumat tentang katalog produk yang boleh anda gunakan untuk memberikan maklumat kepada pelanggan tentang produk dan penetapan harga yang ditawarkan oleh organisasi anda.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 28397fd49ad4cdb2c820ef4b6f198f410995ba0f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898722"
---
# <a name="products"></a>Produk

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Produk adalah teras perniagaan anda. Katalog produk dalam Dynamics 365 Sales Professional ialah koleksi produk dan maklumat penentuan harga. Permudahkan wakil jualan anda untuk meningkatkan jualan mereka dengan mencipta katalog produk secara cepat.

## <a name="add-a-product"></a>Tambah produk

1.  Pastikan anda mempunyai Pengurus Jualan Profesional atau peranan Pentadbir Sistem agar anda boleh menambah produk dalam Dynamics 365 Sales Professional.
2.  Dalam peta tapak, di bawah **Persediaan**, pilih **Produk**.
3.  Pilih **Tambah Produk** dan isi maklumat berikut:

    -  **Nama**
    -  **ID Produk**
    -  **Induk**: Pilih keluarga produk induk untuk produk. Jika anda mencipta produk anak dalam keluarga produk, nama keluarga produk induk dipopulasikan di sini. Ini tidak boleh diubah selepas rekod disimpan.
    -  **Sah Dari**/**Sah Sehingga**: Takrifkan tempoh produk sah dengan memilih tarikh **Sah Dari** dan **Sah Sehingga**.
    -  **Kumpulan Unit**: Pilih kumpulan unit. Kumpulan unit adalah koleksi pelbagai unit yang mana produk dijual dan mendefinisikan bagaimana barang individu dikumpulkan dalam kuantiti lebih besar. Contohnya, jika anda menambah benih sebagai produk, anda mungkin telah mencipta kumpulan unit yang dipanggil "Benih" dan mentakrifkan unit utamanya sebagai "paket."
    -  **Unit Lalai**: Pilih unit paling umum yang mana produk akan dijual. Unit ialah kuantiti atau ukuran bahawa anda menjual produk anda. Contohnya, jika anda menambah benih sebagai produk, anda boleh menjualnya dalam paket, kotak atau palet. Kesemua ini menjadi satu unit produk. Jika benih kebanyakannya dijual di paket, pilih paket sebagai unit.
    -  **Senarai Pilihan Lalai**: Jika ini adalah produk baharu, medan ini adalah baca sahaja. Sebelum anda boleh memilih senarai harga lalai, anda harus melengkapkan semua medan yang diperlukan, kemudian simpan rekod. Walaupun senarai harga lalai tidak diperlukan, selepas anda menyimpan rekod produk, adalah idea yang bagus untuk menetapkan senarai harga lalai untuk setiap produk. Kemudian, jika rekod pelanggan tidak mengandungi senarai harga, Jualan boleh menggunakan senarai harga lalai untuk menjana sebut harga, pesanan dan invois.
    -  **Perpuluhan Disokong**: Masukkan nombor bulat antara 0 dan 5. Jika produk tidak boleh dibahagikan kepada kuantiti pecahan, masukkan 0. Ketepatan medan **Kuantiti** dalam sebut harga, pesanan, atau rekod produk invois disahkan terhadap nilai dalam medan ini jika produk tidak mempunyai senarai harga yang berkaitan.
    -  **SubjeK**: Kaitkan produk ini dengan subjek. Anda boleh menggunakan subjek untuk mengkategorikan produk anda dan untuk menapis laporan.

4.  Pilih **Simpan**.
5.  Pada tab **Butiran Tambahan**, dalam bahagian **Item Senarai Harga**, pilih **Lebih perintah** dan kemudian pilih **Tambah Item Senarai Harga Baharu**.
7.  Pada tab **Butiran Tambahan**, dalam bahagian **Perhubungan Produk**, pilih ikon **Lebih perintah** dan kemudian pilih **Tambah Perhubungan Produk Baharu.**
8.  Dalam borang **Hubungan Produk Baharu**, masukkan butiran berikut, dan pada bar perintah, pilih **Simpan dan Tutup**:

    -   **Produk Berkaitan**: Pilih produk yang anda mahu tambah sebagai produk berkaitan ke rekod produk sedia ada yang sedang anda usahakan.
    -   **Jenis Hubungan Jualan**: Pilih sama ada anda ingin tambah produk sebagai jualan tambahan, jualan silang, aksesori atau produk gantian.
    -   **Arah**:Pilih sama ada hubungan antara produk akan menjadi searah atau dwiarah. Apabila anda memilih searah, produk yang anda pilih dalam **Produk Berkaitan** akan ditunjukkan sebagai pengesyoran untuk produk yang sedia ada tetapi tidak sebaliknya.

9.  Pada borang Produk, pilih **Simpan**.

## <a name="import-products"></a>Produk import

Anda juga boleh menggunakan templat import untuk membawa data produk pukal ke dalam Dynamics 365 Sales.

## <a name="revise-a-product"></a>Ubah suai produk

Pastikan inventori produk dikemas kini dengan menyemak sifat untuk produk secara cepat, seperti yang diperlukan, dan menerbitkan semula maklumat supaya ejen jualan anda dapat melihat perubahan terkini pada inventori.

1.  Pastikan anda mempunyai salah satu daripada peranan keselamatan berikut atau keizinan yang setara: Pentadbir Sistem, Penyesuai Sistem, Pengurus Jualan, Naib Presiden Jualan, Naib Presiden Pemasaran atau CEO-Pengurus Perniagaan.
2.  Dalam peta tapak, pilih **Produk**.
3.  Buka produk aktif yang anda ingin ubah dan pada bar perintah, pilih **Semak**.
4.  Dalam kotak dialog **Sahkan Semak Semula**, pilih **Sahkan**. Ini akan menukar status produk kepada **Dalam Semakan**.
5.  Setelah anda selesai membuat perubahan, pada bar perintah, pilih **Terbit**.

    > [!TIP]
    > Untuk mengembalikan perubahan dan meneruskan dengan versi produk aktif yang terakhir, pilih **Kembali**. Ini menukar status produk kembali kepada **Aktif**.

## <a name="clone-a-product"></a>Klon produk 

Apabila anda mencipta produk baharu, jimatkan masa dengan mengklon yang sedia ada. Ini mencipta satu salinan rekod asal dengan semua butiran kecuali nama dan ID.

1.  Pastikan anda mempunyai salah satu daripada peranan keselamatan berikut atau keizinan yang setara: Pentadbir Sistem, Penyesuai Sistem, Pengurus Jualan, Naib Presiden Jualan, Naib Presiden Pemasaran atau CEO-Pengurus Perniagaan.
2.  Dalam peta tapak, pilih **Produk**.
3.  Pilih rekod produk yang anda ingin klonkan dan pada bar perintah, pilih **Klon**. Kotak dialog pengesahan muncul.
4.  Pilih **Sahkan**.

Rekod produk baharu dibuka dengan butiran sama seperti asal kecuali nama dan ID.

## <a name="retire-a-product"></a>Tamatkan produk 

Jika organisasi anda tidak menjual produk lagi, tamatkannya supaya produk tidak lagi tersedia kepada ejen jualan anda.

1.  Pastikan anda mempunyai peranan Pentadbir Sistem atau Pengurus Sales Professional atau keizinan yang setara.
2.  Dalam peta tapak, pilih **Produk**.
3.  Buka produk aktif yang anda ingin hentikan, dan pada bar perintah, pilih **Henti**.
4.  Dalam kotak dialog **Sahkan Berhenti**, pilih **Sahkan**.


## <a name="delete-a-product"></a>Padamkan produk

Untuk berhenti menjual produk, padamkannya.

> [!IMPORTANT]
> Anda tidak boleh memulihkan rekod yang telah dipadamkan.

1.  Pastikan anda mempunyai peranan Pentadbir Sistem atau Pengurus Sales Professional atau keizinan yang setara.
2.  Dalam peta tapak, pilih **Produk**.
3.  Pilih rekod produk yang anda ingin padamkan dan pada bar perintah, pilih **Padam**.
4.  Dalam kotak dialog **Sahkan Pemadaman**, pilih **Teruskan**.
 
 ## <a name="quantity-factors-for-products"></a>Faktor kuantiti bagi produk

Faktor kuantiti menyokong jualan produk berasaskan langganan. Untuk produk berdasarkan langganan, kuantiti pada sebut harga atau baris kontrak projek dinyatakan sebagai bilangan bulan pengguna.

Biasanya, harga perisian langganan disimpan dalam katalog sebagai harga bagi setiap pengguna setiap bulan. Walau bagaimanapun, anda boleh menggunakan perihalan masa lain sebagai ganti. Semasa proses jualan, harga pada baris sebut harga biasanya adalah harga bagi setiap pengguna, setiap bulan yang telah dirundingkan dan terdiskaun oleh ejen jualan IT. Setiap urusan mempunyai bilangan pengguna yang berbeza dan bilangan bulan langganan yang berbeza. Kuantiti yang digunakan untuk mengira jumlah baris sebut harga adalah produk bilangan pengguna dan bilangan bulan langganan.

Faktor kuantiti bergantung pada atribut produk. Apabila anda mengkonfigurasikan sifat khusus untuk produk, anda boleh menandakan subset sifat itu atau semua sifat itu, sebagai faktor kuantiti.

Sistem mengesahkan bahawa hanya sifat angka atau sifat produk yang mempunyai jenis data berangka ditandakan sebagai faktor kuantiti. Apabila produk yang faktor kuantiti dikonfigurasikan ditambah pada baris sebut harga, medan **Kuantiti** pada baris sebut harga akan menjadi medan baca sahaja. Selepas anda memasukkan nilai untuk sifat produk yang merupakan faktor kuantiti, kuantiti baris sebut harga dikira.

Contohnya, jika terdapat sifat berikut: 

- **Bilangan pengguna**: Bilangan pengguna 
- **Bilangan bulan**: Bilangan bulan langganan
- **SKU Produk** 

Sifat **Bilangan Pengguna** dan **Bilangan Bulan** boleh ditanda sebagai faktor kuantiti dengan mengedit sifat baris produk. 
