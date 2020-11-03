---
title: Mata wang
description: Topik ini menyediakan maklumat tentang cara menambah dan mengalih keluar jenis mata wang dalam Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 1db7e76dbb220954b9f9088b2168eed1a1902abc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081260"
---
# <a name="currency"></a>Mata wang

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Mata wang menentukan harga produk dalam katalog produk dan kos transaksi, seperti pesanan jualan. Jika pelanggan anda tersebar di seluruh dunia, tambah mata wang mereka untuk mengurus transaksi anda. Tambah mata wang yang paling sesuai dengan mata wang dan keperluan perniagaan akan datang anda.  

> [!NOTE]
> Jika persekitaran anda adalah persekitaran Common Data Service, anda berada dalam pusat pentadbir Power Platform dan anda memilih halaman **Mata Wang** ( **Persekitaran** > [pilih persekitaran] > **Tetapan** > **Perniagaan** > **Mata Wang** ), halaman akan menjadi kosong. Ini ialah kerana tetapan mata wang tidak disokong dalam persekitaran Common Data Service.

## <a name="add-a-currency"></a>Tambah matawang  
Sebelum anda memulakan prosedur ini, sahkan bahawa peranan keselamatan anda mengandungi keizinan pentadbir sistem. 

1. Dalam pusat pentadbir Power Platform, pilih persekitaran. 
2. Pilih **Tetapan** > **Perniagaan**.
3. Pilih **Mata wang**.  
4. Pilih **Baharu**.  
5. Isikan maklumat, seperti yang diperlukan.  


   |          Medan          |                                                                                                                                                                                                                                                                                                                                                                            Perihalan                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Jenis Mata Wang**    | - **Sistem** - Pilih pilihan ini jika anda mahu menggunakan mata wang yang tersedia dalam aplikasi dipacu model dalam Dynamics 365. Untuk carian mata wang, pilih **Carian**. Apabila anda memilih kod mata wang, **Nama Mata Wang** dan **Simbol Mata Wang** ditambah secara automatik untuk mata wang yang dipilih.<br />- **Tersuai** - Pilih pilihan ini jika anda mahu menambah mata wang yang tidak tersedia dalam aplikasi dipacu model dalam Dynamics 365. Dalam kes ini, anda secara manual mesti masukkan nilai bagi **Kod Mata Wang** , **Kejituan Mata Wang** , **Nama Mata Wang** , **Simbol Mata Wang** dan **Pertukaran Mata Wang**. |
   |    **Kod Mata Wang**    |                                                                                                                                                                                                                                                                                                                                            Singkatan untuk mata wang. Sebagai contoh, **USD** untuk Dolar Amerika Syarikat.                                                                                                                                                                                                                                                                                                                                            |
   | **Kejituan Mata Wang**  |                                                                                                                                                                                  Taipkan nombor perpuluhan yang anda mahu gunakan untuk mata wang.  Anda boleh menambah nilai antara 0 dan 4. **Nota:**  Jika anda telah menetapkan nilai kejituan dalam kotak dialog **Tetapan Sistem** , nilai tersebut akan muncul di sini.                                                                                                                                                                                  |
   |    **Nama Mata Wang**    |                                                                                                                                                                                                                                         Jika anda memilih kod mata wang daripada senarai mata wang yang tersedia dalam aplikasi dipacu model dalam Dynamics 365, nama mata wang untuk kod yang terpilih akan dipaparkan di sini. Jika anda memilih **Tersuai** sebagai jenis mata wang, taipkan nama mata wang.                                                                                                                                                                                                                                          |
   |   **Simbol Mata Wang**   |                                                                                                                                                                                                                                                                      Jika anda memilih kod mata wang daripada senarai mata wang yang tersedia, simbol untuk mata wang yang terpilih akan dipaparkan di sini. Jika anda memilih **Tersuai** sebagai jenis mata wang, masukkan simbol untuk mata wang baharu.                                                                                                                                                                                                                                                                       |
   | **Pertukaran Mata Wang** |                                                                                                                                                                                                                                     Taipkan nilai mata wang yang dipilih dari segi satu dolar AS. Ini adalah amaun di mana mata wang yang dipilih ditukar kepada mata wang asas. **Penting:**  Pastikan anda mengemas kini nilai ini sekerap yang diperlukan untuk mengelakkan sebarang pengiraan yang tidak tepat dalam transaksi anda.                                                                                                                                                                                                                                      |


6. Apabila anda sudah selesai, pada bar perintah, pilih **Simpan** atau **Simpan dan Tutup**.  

   > [!TIP]
   >  Untuk mengedit mata wang, pilih mata wang dan kemudian masukkan atau pilih nilai baharu.  

## <a name="delete-a-currency"></a>Padam mata wang  

1. Dalam pusat pentadbir Power Platform, pilih persekitaran. 
2. Pilih **Tetapan** > **Perniagaan**.
3. Pilih **Mata wang**.  
4. Dari senarai mata wang yang dipaparkan, pilih mata wang untuk dipadamkan.  
5. Pilih **Padam**.  
6. Sahkan pemadaman.  

> [!IMPORTANT]
>  Anda tidak boleh memadamkan mata wang yang sedang digunakan oleh rekod lain; anda hanya boleh menyahaktifkannya. Menyahaktifkan rekod mata wang tidak mengalih keluar maklumat mata wang yang disimpan dalam rekod sedia ada, seperti peluang atau pesanan. Bagaimanapun, anda tidak akan dapat memilih mata wang yang dinyahaktifkan untuk transaksi baharu.  
