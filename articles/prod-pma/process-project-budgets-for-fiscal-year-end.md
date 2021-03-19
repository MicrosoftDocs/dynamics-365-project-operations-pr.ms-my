---
title: Pindahkan projek belanjawan pada akhir tahun fiskal
description: Artikel ini memberikan maklumat tentang cara untuk memindahkan amaun belanjawan yang tinggal ke tahun hadapan dan mencipta butiran daftar belanjawan.
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1f601be072e84fc04246cd55a260c8004f6fb3e5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289740"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Pindahkan projek belanjawan pada akhir tahun fiskal

[!include [banner](../includes/banner.md)]

Apabila bekerja pada projek berbilang tahun, anda mungkin mempunyai belanjawan yang tinggal pada akhir tahun fiskal. Anda boleh memindahkan amaun belanjawan yang tinggal ke tahun hadapan, dan mencipta butiran daftar belanjawan untuk amaun dalam akaun lejar umum berkaitan. Sebelum anda membawa ke hadapan amaun yang tinggal, semak dan analisis amaun belanjawan yang tinggal.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Semak dan analisis amaun belanjawan yang tinggal

Lengkapkan langkah berikut untuk menyemak amaun belanjawan akhir tahun untuk projek, tetapi tidak membawa amaun ke hadapan.

1. Pergi ke **Pengurusan projek dan perakaunan** > **Berkala** > **Belanjawan** > **Belanjawan dibawa ke hadapan**. 
2. Pada halaman **Proses dibawa ke hadapan belanjawan projek**, pada tab **Pilihan akhir tahun**, sahkan yang **Amaun belanjawan projek yang tinggal dibawa ke hadapan** tidak didayakan.
3. Pada tab **Parameter**, dalam medan **Tahun belanjawan projek**, pilih tahun fiskal yang anda mahu lihat amaun belanjawan yang tinggal. 
4. Pada medan **Pembukaan tahun fiskal**, pilih tahun fiskal yang anda mahu lihat amaun belanjawan yang tinggal. 
5. Dalam medan **Daripada model ramalan**, pilih **Belanjawan yang tinggal**. 
6. Untuk memasukkan projek yang memenuhi kriteria pilihan anda dan tidak mempunyai belanjawan yang tinggal, pilih **Tunjukkan baki sifar**.  
7. Pada tab **Pilih Belanjawan**, pilih **Dapatkan semula semua belanjawan** untuk memuatkan semua belanjawan yang sepadan dengan kriteria pilihan anda, dan kemudian pilih **Proses**. 
8. Untuk mereka bentuk pangkalan data pertanyaan yang memuatkan set belanjawan tertentu ke dalam anak tetingkap, pilih **Dapatkan semula belanjawan dipilih**.

Untuk mendapatkan maklumat lanjut tentang baris tertentu dalam anak tetingkap, pilih baris, dan kemudian pilih **Lihat butiran belanjawan** atau **Lihat akaun**.

## <a name="carry-forward-remaining-budget-amounts"></a>Bawa ke hadapan amaun belanjawan yang tinggal 

Apabila anda memproses amaun belanjawan yang tinggal, anda boleh mencipta transaksi dalam lejar umum untuk amaun yang anda dibawa ke hadapan. Untuk mencipta transaksi lejar umum, lengkapkan langkah dalam bahagian, [Bawa ke hadapan amaun belanjawan dan cipta transaksi lejar umum](#carry-forward). 

> [!NOTE]
> Amaun belanjawan yang dibawa ke hadapan dipindahkan ke model ramalan yang dipilih dalam halaman **Model ramalan** sebagai model ramalan dibawa ke hadapan.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Bawa ke hadapan amaun belanjawan dan cipta transaksi lejar umum

1.  Pilih **Pengurusan projek dan perakaunan** > **Berkala** > **Belanjawan** > **Belanjawan dibawa ke hadapan**. 
2. Pada halaman **Proses dibawa ke hadapan belanjawan projek**, pilih **Akhir tahun**, dan kemudian dayakan **Amaun belanjawan projek yang tinggal dibawa ke hadapan** dan **Cipta entri daftar belanjawan dalam lejar umum**. 
3. Pada tab **Parameter**, dalam kumpulan medan **Parameter projek**, pilih yang berikut:

   - **Projek tahun belanjawan**: Pilih permulaan tahun fiskal yang anda mahu lihat amaun belanjawan yang tinggal. 
   - **Untung dan rugi**: Cipta transaksi untung dan rugi dalam lejar umum. 
   -  **WIP**: Cipta transaksi Kerja dalam Proses (WIP) dalam lejar umum.
   -  **Gaji**: Cipta transaksi peruntukan gaji dalam lejar umum. 

5. Dalam kumpulan medan **Lejer umum**, berikan maklumat berikut: 

   - Pada medan **Pembukaan tahun fiskal**, pilih tahun fiskal yang anda mahu pindahkan amaun belanjawan yang tinggal untuk projek. Nilai lalai ialah setahun selepas nilai dalam medan **Projek tahun belanjawan**.
   -  Dalam medan **Tempoh dibawa ke hadapan**, pilih tempoh yang anda mahu cipta butiran daftar belanjawan di dalam lejar umum. Ini biasanya merupakan tempoh pertama dalam pembukaan tahun fiskal.

6. Dalam kumpulan medan **Salin daripada/kepada**, berikan maklumat berikut:

   - Dalam medan **Daripada model ramalan**, pilih model ramalan belanjawan projek berkaitan dengan amaun belanjawan yang tinggal anda mahu pindahkan untuk projek. 
   - Dalam medan **Ke model ramalan lejer**, pilih model belanjawan lejer berkaitan dengan amaun belanjawan yang anda mahu pindahkan ke lejer umum. 
   -  Pilih **Pindahkan mata wang jualan** untuk menggunakan mata wang jualan projek untuk transaksi lejar umum yang dicipta apabila anda memindahkan amaun belanjawan untuk projek. Apabila pilihan tidak dipilih, transaksi menggunakan mata wang perakaunan. 
   -  Pilih **Tunjukkan baki sifar** untuk memasukkan projek yang tidak mempunyai amaun belanjawan yang tinggal, tetapi memenuhi kriteria lain yang anda pilih dalam projek yang dipaparkan dalam anak tetingkap bahagian bawah.

7. Pada tab **Pilih Belanjawan**, pilih **Dapatkan semula semua belanjawan** untuk memuatkan semua belanjawan yang sepadan dengan kriteria pilihan anda. Jika anda suka untuk mereka bentuk pangkalan data pertanyaan yang memuatkan set belanjawan projek tertentu ke dalam anak tetingkap, pilih **Dapatkan semula belanjawan dipilih**.
8. Bagi setiap projek yang anda mahu proses, pilih pilihan pada permulaan baris untuk projek.

    > [!TIP]
    > Untuk memilih semua atau sebahagian besar projek, pilih tanda semak dalam penjuru kiri paling atas. Untuk mengecualikan pemprosesan sebarang projek, kosongkan tanda semak untuk projek tersebut.

9. Untuk memindahkan amaun belanjawan yang tinggal untuk projek yang dipilih ke tahun fiskal yang dipilih dan mencipta butiran daftar belanjawan dalam lejar umum, pilih **Proses**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Amaun belanjawan dibawa ke hadapan tanpa mencipta transaksi lejar umum

1. Pergi ke **Pengurusan projek dan perakaunan** > **Berkala** > **Belanjawan** > **Belanjawan dibawa ke hadapan**.
2. Pada halaman **Proses dibawa ke hadapan belanjawan projek**, dalam medan **Pilihan akhir tahun**, pilih **Amaun belanjawan projek yang tinggal dibawa ke hadapan**.
3. Pada kumpulan **Parameter**, dalam medan **Tahun belanjawan projek**, pilih tahun fiskal yang anda mahu lihat amaun belanjawan yang tinggal.
4. Dalam kumpulan **Salin daripada/kepada**, berikan maklumat berikut:

   - Dalam medan **Daripada model ramalan**, pilih model ramalan belanjawan projek yang berkaitan dengan amaun belanjawan yang tinggal yang anda mahu pindahkan untuk projek. 
   - Pilih **Tunjukkan baki sifar** untuk memasukkan projek yang tidak mempunyai amaun belanjawan yang tinggal, tetapi yang memenuhi kriteria lain pilihan anda.
   - Pada kumpulan **Pilih Belanjawan**, pilih **Dapatkan semula semua belanjawan** untuk memuatkan semua belanjawan yang sepadan dengan kriteria yang anda telah pilih. Untuk mereka bentuk pangkalan data pertanyaan yang memuatkan set belanjawan projek ke dalam anak tetingkap, pilih **Dapatkan semula belanjawan dipilih**.

5. Bagi setiap projek yang anda mahu proses, pilih pilihan pada permulaan baris untuk projek. 
6. Pilih **Proses** untuk memindahkan amaun belanjawan yang tinggal untuk projek yang dipilih kepada tahun fiskal yang dipilih.



[!INCLUDE[footer-include](../includes/footer-banner.md)]