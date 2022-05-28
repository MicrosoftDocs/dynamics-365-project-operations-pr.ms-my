---
title: Menggunakan baris kontrak berasaskan projek
description: Topik ini menyediakan maklumat tentang baris kontrak berasaskan projek.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f67c0447c0b2a23d6f7d03dfc5ac7800943bbf36
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595187"
---
# <a name="work-with-projectbased-contract-lines"></a>Menggunakan baris kontrak berasaskan projek

Baris kontrak berasaskan projek dalam Dynamics 365 Project Operations direka untuk memegang anggaran dan perjanjian pengebilan untuk komponen khusus kerja projek yang terlibat. Struktur baris kontrak berasaskan projek diperluaskan untuk anggaran projek dan senario pengebilan dengan konsep berikut:

- Kaedah pengebilan
- Pemetaan projek dan tugas
- Kelas transaksi yang disertakan
- Had yang tidak boleh melebihi
- Persediaan boleh dikenakan caj
- Anggaran menggunakan butiran baris kontrak
- Pelanggan baris kontrak

Medan berikut disertakan dalam tab **Umum** untuk baris kontrak berasaskan projek. Medan ini membantu menyediakan asas untuk anggaran yang terperinci dan berasas dan penyusunan pengebilan untuk kerja berasaskan projek.

| Medan | Penerangan | Kesan hiliran |
| --- | --- | --- |
| **Nama** | Nama baris kontrak yang mengenal pasti komponen berasingan untuk kontrak yang sedang dianggarkan. Untuk kontrak projek yang dicipta daripada sebut harga, nilai ini akan disalin daripada nilai yang sepadan dengan baris sebut harga berasaskan projek. | Nilai medan ini disalin kepada baris invois projek yang dicipta daripada baris kontrak ini apabila invois dicipta. |
| **Kaedah Pengebilan** | Pada kontrak projek yang dicipta daripada sebut harga, nilai ini akan disalin daripada medan yang sepadan pada baris sebut harga. Ini ialah set pilihan yang mewakili dua model kontrak utama yang disokong oleh Project Operations:</br>- **Harga Tetap**</br>- **Masa dan Bahan** | Berdasarkan kaedah pengebilan bagi baris kontrak rujukan, transaksi sebenar akan diproses. Jika baris kontrak yang dirujuk oleh aktual mempunyai kaedah pengebilan masa dan material, rekod aktual kos dan jualan yang tidak dibilkan dicipta. Jika baris kontrak yang dirujuk oleh aktual mempunyai kaedah pengebilan harga tetap, hanya aktual kos dicipta. |
| **Project** | Gunakan medan ini untuk mengenal pasti projek yang akan digunakan untuk menyampaikan kerja pada penglibatan ini. | Nilai dalam medan ini digunakan bersempena dengan **Tugas yang Disertakan** dan **Kelas Transaksi yang Disertakan** untuk menyelesaikan rujukan baris kontrak pada rekod baris aktual atau anggaran. |
| **Termasuk Masa** | Bendera menunjukkan sama ada transaksi masa atau kos buruh pada projek yang dipilih akan dimasukkan dalam baris kontrak ini. Nilai **Tiada** menunjukkan bahawa transaksi masa atau kos buruh tidak akan dimasukkan ke dalam baris kontrak ini. Nilai **Ya** menunjukkan bahawa transaksi masa atau kos buruh akan dimasukkan. | Nilai medan ini digunakan bersempena dengan projek untuk menyelesaikan rujukan baris kontrak pada rekod baris aktual atau anggaran. |
| **Termasuk Perbelanjaan** | Bendera menunjukkan sama ada kos perbelanjaan pada projek yang dipilih akan dimasukkan dalam baris kontrak ini. Nilai **Tiada** menunjukkan bahawa kos perbelanjaan tidak akan dimasukkan ke dalam baris kontrak ini. Nilai **Ya** menunjukkan bahawa kos perbelanjaan akan dimasukkan. | Nilai medan ini digunakan bersempena dengan projek untuk menyelesaikan rujukan baris kontrak pada rekod baris aktual atau anggaran. |
| **Termasuk Yuran** | Bendera menunjukkan sama ada yuran pada projek yang dipilih akan dimasukkan dalam baris kontrak ini. Nilai **Tiada** menunjukkan bahawa yuran tidak akan dimasukkan ke dalam baris kontrak ini. Nilai **Ya** menunjukkan bahawa transaksi masa atau kos buruh akan dimasukkan. | Nilai medan ini digunakan bersempena dengan projek untuk menyelesaikan rujukan baris kontrak pada rekod baris aktual atau anggaran. |
| **Amaun Dikontrakkan** | Pada barisan kontrak harga tetap, ini ialah nilai yang dipersetujui yang akan diinvoiskan kepada pelanggan untuk semua komponen kerja yang berkaitan dengan baris kontrak ini. Pada baris kontrak masa dan bahan, amaun ini ialah nilai anggaran yang akan diinvoiskan kepada pelanggan untuk semua komponen kerja yang berkaitan dengan baris kontrak ini. Pada kontrak projek yang dicipta daripada sebut harga, nilai ini akan disalin daripada medan yang sepadan pada baris sebut harga. Apabila baris kontrak berasaskan projek mempunyai butiran baris, medan ini dikunci untuk pengeditan dan diringkaskan daripada jumlah pada butiran baris kontrak. | Apabila baris kontrak mempunyai butiran baris, nilai ini boleh diubah suai dengan mengubah jumlah pada butiran baris. Pada baris kontrak harga tetap, nilai ini digunakan untuk menjana amaun sebelum cukai pada pencapaian pengebilan berkala. |
| **Anggaran Cukai** | Pengguna boleh mengedit medan ini untuk memasukkan anggaran jumlah cukai pada baris kontrak. Apabila baris kontrak berasaskan projek mempunyai butiran baris, medan ini dikunci untuk pengeditan dan diringkaskan daripada jumlah cukai pada butiran baris kontrak. | Apabila baris kontrak mempunyai butiran baris, nilai ini boleh diubah suai dengan mengubah jumlah cukai pada butiran baris. Pada baris kontrak harga tetap, nilai ini digunakan untuk menjana cukai pada pencapaian pengebilan berkala. |
| **Amaun Kontrak selepas Cukai** | Amaun baris kontrak selepas cukai. Medan ini adalah baca sahaja dan dikira sebagai **Amaun kontrak + Cukai**. | Pada baris kontrak harga tetap, nilai ini digunakan untuk menjana pencapaian pengebilan berkala. |
| **Had Tidak Boleh Dilebihi** | Pengguna boleh mengedit medan ini dan ia hanya tersedia untuk baris kontrak berdasarkan projek yang mempunyai kaedah pengebilan masa dan bahan. | Pengguna boleh mengedit medan ini. Apabila masa atau aktual perbelanjaan merujuk kepada baris kontrak ini untuk masa dan bahan, jumlah bagi aktual dinilai dengan had tidak melebihi pada baris kontrak ini selepas mengira jumlah yang sudah dibelanjakan dan dilakukan. |
| **Belanjawan Pelanggan** | Medan ini boleh diedit dan disalin daripada medan sepadan pada baris sebut harga, jika kontrak dicipta daripada sebut harga. | Medan ini hanya digunakan untuk maklumat dan tidak mempunyai sebarang kepentingan hiliran. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Peraturan pengesahan untuk pilihan pada tab Umum baris kontrak berasaskan projek

Peraturan: Projek dan kelas transaksi tertentu hanya boleh dimasukkan pada satu baris kontrak berasaskan projek dalam kontrak.

| Kontrak | Baris kontrak | Project | Termasuk masa | Termasuk perbelanjaan | Termasuk yuran | Sah/tidak sah | Sebab                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | P1      | Ya          | Ya             | Ya         | Tidak sah       | Mencabuli peraturan. Masa, perbelanjaan dan yuran pada projek P1 termasuk dalam kedua-dua baris kontrak, CL1 dan CL2.                                                                                       |
| C1       | CL2           | P1      | Ya          | Ya             | Ya         | Tidak sah       | Mencabuli peraturan. Masa, perbelanjaan dan yuran pada projek P1 termasuk dalam kedua-dua baris kontrak, CL1 dan CL2.                                                                                       |
| C1       | CL1           | P1      | Ya          | Tidak              | Ya         | Tidak sah       | Mencabuli peraturan. Masa dan yuran pada projek P1 termasuk dalam kedua-dua baris kontrak, CL1 dan CL2.                                                                                                   |
| C1       | CL2           | P1      | Ya          | Ya             | Ya         | Tidak sah       | Mencabuli peraturan. Masa dan yuran pada projek P1 termasuk dalam kedua-dua baris kontrak, CL1 dan CL2.                                                                                                   |
| C1       | CL1           | P1      | Ya          | Tidak              | Ya         | Sah           | Masa dan yuran projek P1 termasuk dalam CL1. Perbelanjaan pada projek P1 termasuk dalam CL2. </br>   Tidak terdapat pertindihan dalam apa yang dimasukkan pada setiap baris kontrak dan oleh itu sah.  |
| C1       | CL2           | P1      | Tidak           | Ya             | Tidak          | Sah           | Masa dan yuran projek P1 termasuk dalam CL1. Perbelanjaan pada projek P1 termasuk dalam CL2. </br>   Tidak terdapat pertindihan dalam apa yang dimasukkan pada setiap baris kontrak dan oleh itu sah.  |
| C1       | CL1           | P1      | Ya          | Ya             | Ya         | Tidak sah       | Mencabuli peraturan. Masa, perbelanjaan dan yuran pada projek P1 termasuk dalam baris dua kontrak.                                                                                               |
| CL2      | CL2           | P1      | Ya          | Ya             | Ya         | Tidak sah       | Mencabuli peraturan. Masa, perbelanjaan dan yuran pada projek P1 termasuk dalam baris dua kontrak.                                                                                               |


[!INCLUDE[footer-include](../includes/footer-banner.md)]