---
title: Menggunakan baris kontrak berasaskan projek - lite
description: Topik ini menyediakan maklumat tentang menggunakan baris kontrak berdasarkan projek.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7ec8973df1def3f707603019cdd45147423c1ae3
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180653"
---
# <a name="work-with-projectbased-contract-lines---lite"></a>Menggunakan baris kontrak berasaskan projek - lite

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Baris kontrak berasaskan projek dalam Dynamics 365 Project Operations direka untuk memegang anggaran dan perjanjian pengebilan untuk komponen khusus kerja projek yang terlibat. Struktur baris kontrak berasaskan projek diperluaskan untuk anggaran projek dan senario pengebilan dengan konsep berikut:

- Kaedah pengebilan
- Pemetaan projek dan tugas
- Kelas transaksi yang disertakan
- Had yang tidak boleh melebihi
- Persediaan boleh dikenakan caj
- Anggaran menggunakan butiran baris kontrak
- Pelanggan baris kontrak

Jadual berikut termasuk medan pada tab **Jadual** untuk baris kontrak berasaskan projek yang membantu menyediakan asas bagi penhaturan pengebilan dan anggaran yang terperinci dan berasas untuk kerja berasaskan projek.

| Medan | Penerangan  | Kesan hiliran |
| --- | --- | --- |
| **Nama** | Nama baris kontrak. Ini mengenal pasti komponen berasingan untuk kontrak yang sedang dianggarkan. Untuk kontrak projek yang dicipta daripada sebut harga, nilai ini akan disalin daripada nilai yang sepadan dengan baris sebut harga berasaskan projek. | Nama disalin kepada baris invois projek yang dicipta daripada baris kontrak ini apabila invois dicipta. |
| **Kaedah Pengebilan** | Pada kontrak projek yang dicipta daripada sebut harga, nilai ini akan disalin daripada medan yang sepadan pada baris sebut harga. Ini ialah set pilihan yang mewakili dua model kontrak utama yang disokong oleh Project Operations:</br>- **Harga Tetap**</br>- **Masa dan Bahan** | Berdasarkan kaedah pengebilan bagi baris kontrak rujukan, transaksi sebenar akan diproses. Jika baris kontrak yang dirujuk oleh aktual mempunyai kaedah pengebilan masa dan material, rekod aktual kos dan jualan yang tidak dibilkan dicipta. Jika baris kontrak yang dirujuk oleh aktual mempunyai kaedah pengebilan harga tetap, hanya aktual kos dicipta. |
| **Project** | Gunakan medan ini untuk mengenal pasti projek yang akan digunakan untuk menyampaikan kerja pada penglibatan ini. | Nilai ini akan digunakan bersempena dengan **Tugas yang Disertakan** dan **Kelas Transaksi yang Disertakan** untuk menyelesaikan rujukan baris kontrak pada rekod baris aktual atau anggaran. |
| **Tugas yang Disertakan** | Menunjukkan sama ada baris kontrak ini termasuk semua tugas projek untuk projek yang dipilih atau hanya subset tugas. Ia ialah set pilihan yang mempunyai nilai mungkin berikut:</br>- **Semua Tugas Projek**</br>- **Tugas Projek Terpilih Sahaja**. Nilai kosong dalam medan ini adalah sama dengan memilih **Semua Tugas Projek**. | Jika **Tugas yang Dipilih Sahaja** dipilih, anda boleh memilih tugas khusus dan dikaitkan kepada baris kontrak ini pada tab **Persediaan Pengebilan Tugas** pada halaman **Projek**. Nilai ini akan digunakan bersempena dengan **Projek** dan kelas **Transaksi yang Disertakan** untuk menyelesaikan rujukan baris kontrak pada rekod baris aktual atau anggaran. |
| **Termasuk Masa** | Bendera menunjukkan sama ada transaksi masa atau kos buruh pada projek yang dipilih akan dimasukkan dalam baris kontrak ini. Nilai **Tiada** menunjukkan bahawa transaksi masa atau kos buruh tidak akan dimasukkan ke dalam baris kontrak ini. Nilai **Ya** menunjukkan bahawa transaksi masa atau kos buruh akan dimasukkan. | Nilai ini digunakan bersempena dengan projek untuk menyelesaikan rujukan baris kontrak pada rekod baris aktual atau anggaran. |
| **Termasuk Perbelanjaan** | Bendera menunjukkan sama ada kos perbelanjaan pada projek yang dipilih akan dimasukkan dalam baris kontrak ini. Nilai **Tiada** menunjukkan bahawa kos perbelanjaan tidak akan dimasukkan ke dalam baris kontrak ini. Nilai **Ya** menunjukkan bahawa kos perbelanjaan akan dimasukkan. | Nilai ini digunakan bersempena dengan projek untuk menyelesaikan rujukan baris kontrak pada rekod baris aktual atau anggaran. |
| **Termasuk Yuran** | Bendera menunjukkan sama ada yuran pada projek yang dipilih akan dimasukkan dalam baris kontrak ini. Nilai **Tiada** menunjukkan bahawa yuran tidak akan dimasukkan ke dalam baris kontrak ini. Nilai **Ya** menunjukkan bahawa transaksi masa atau kos buruh akan dimasukkan. | Nilai ini digunakan bersempena dengan projek untuk menyelesaikan rujukan baris kontrak pada rekod baris aktual atau anggaran. |
| **Amaun Dikontrakkan** | Pada baris kontrak harga tetap, amaun ini yang dipersetujui yang akan diinvoiskan kepada pelanggan untuk semua komponen kerja yang berkaitan dengan baris kontrak ini. Pada baris kontrak masa dan bahan, amaun ini ialah nilai anggaran yang akan diinvoiskan kepada pelanggan untuk semua komponen kerja yang berkaitan dengan baris kontrak ini. Pada kontrak projek yang dicipta daripada sebut harga, nilai ini akan disalin daripada medan yang sepadan pada baris sebut harga. Apabila baris kontrak berasaskan projek mempunyai butiran baris, medan ini dikunci untuk pengeditan dan diringkaskan daripada jumlah pada butiran baris kontrak. | Apabila baris kontrak mempunyai butiran baris, nilai ini boleh diubah suai dengan mengubah jumlah pada butiran baris. Pada baris kontrak harga tetap, nilai ini digunakan untuk menjana amaun sebelum cukai pada pencapaian pengebilan berkala. |
| **Anggaran Cukai** | Pengguna boleh mengedit medan ini untuk memasukkan anggaran jumlah cukai pada baris kontrak. Apabila baris kontrak berasaskan projek mempunyai butiran baris, medan ini dikunci untuk pengeditan dan diringkaskan daripada jumlah cukai pada butiran baris kontrak. | Apabila baris kontrak mempunyai butiran baris, nilai ini boleh diubah suai dengan mengubah jumlah cukai pada butiran baris. Pada baris kontrak harga tetap, nilai ini digunakan untuk menjana cukai pada pencapaian pengebilan berkala. |
| **Amaun Kontrak selepas Cukai** | Amaun baris kontrak selepas cukai. Medan ini adalah baca sahaja dan dikira sebagai **Amaun kontrak + Cukai**. | Pada baris kontrak harga tetap, nilai ini digunakan untuk menjana pencapaian pengebilan berkala. |
| **Had Tidak Boleh Dilebihi** | Pengguna boleh mengedit medan ini dan ia hanya tersedia untuk baris kontrak berdasarkan projek yang menetapkan kaedah pengebilan kepada masa dan bahan. | Pengguna boleh mengedit medan ini. Apabila aktual untuk masa dan bahan merujuk kepada baris kontrak ini untuk masa dan bahan, jumlah bagi aktual dinilai dengan had tidak melebihi pada baris kontrak ini selepas mengira jumlah yang sudah dibelanjakan dan dilakukan. Penilaian ini diselesaikan selepas amaun yang telah dibelanjakan dan dilakukan diambil kira. |
| **Belanjawan Pelanggan** | Medan ini boleh diedit dan disalin daripada medan sepadan pada baris sebut harga jika kontrak dicipta daripada sebut harga. | Medan ini hanya digunakan untuk maklumat dan tidak mempunyai sebarang kepentingan hiliran. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Peraturan pengesahan untuk pilihan pada tab Umum baris kontrak berasaskan projek

Peraturan 1: Jika medan **Tugas yang Disertakan** kosong atau ditetapkan kepada **Semua Tugas Projek**, semua tugas projek akan dimasukkan ke dalam baris kontrak.

Peraturan 2: Apabila medan **Tugas yang Disertakan** kosong atau secara jelas ditetapkan kepada **Semua Tugas Projek**, projek dan kelas transaksi tertentu hanya boleh dimasukkan ke dalam satu baris kontrak berasaskan projek kontrak.

Peraturan 3: Apabila medan **Tugas yang Disertakan** ditetapkan kepada **Tugas Projek Terpilih Sahaja**, projek dan kelas transaksi tertentu boleh dimasukkan ke dalam berbilang baris kontrak berasaskan projek kontrak.

| Kontrak | Baris kontrak | Project | Tugas yang disertakan      | Termasuk masa | Termasuk perbelanjaan | Termasuk yuran | Sah/tidak sah | Sebab                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------|---------------|---------|---------------------|--------------|-----------------|-------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | P1      | Kosong               | Ya          | Ya             | Ya         | Tidak sah       | Pelanggaran Peraturan #2. Masa, perbelanjaan dan yuran pada projek P1 termasuk dalam kedua-dua baris kontrak, CL1 dan CL2.                                                                                                                                                                                                                                                                                                              |
| C1       | CL2           | P1      | Kosong               | Ya          | Ya             | Ya         | Tidak sah       | Pelanggaran Peraturan #2. Masa, perbelanjaan dan yuran pada projek P1 termasuk dalam kedua-dua baris kontrak, CL1 dan CL2.                                                                                                                                                                                                                                                                                                              |
| C1       | CL1           | P1      | Kosong               | Ya          | Tidak              | Ya         | Tidak sah       | Pelanggaran Peraturan #2. Masa dan yuran pada projek P1 termasuk dalam kedua-dua baris kontrak, CL1 dan CL2.                                                                                                                                                                                                                                                                                                                          |
| C1       | CL2           | P1      | Kosong               | Ya          | Ya             | Ya         | Tidak sah       | Pelanggaran Peraturan #2. Masa dan yuran pada projek P1 termasuk dalam kedua-dua baris kontrak, CL1 dan CL2.                                                                                                                                                                                                                                                                                                                          |
| C1       | CL1           | P1      | Kosong               | Ya          | Tidak              | Ya         | Sah           | Masa dan yuran projek P1 termasuk dalam CL1. Perbelanjaan pada projek P1 termasuk dalam CL2. </br>   Tidak terdapat pertindihan dalam apa yang dimasukkan pada setiap baris kontrak dan oleh itu sah.                                                                                                                                                                                                                         |
| C1       | CL2           | P1      | Kosong               | Tidak           | Ya             | Tidak          | Sah           | Masa dan yuran projek P1 termasuk dalam CL1. Perbelanjaan pada projek P1 termasuk dalam CL2. </br>   Tidak terdapat pertindihan dalam apa yang dimasukkan pada setiap baris kontrak dan oleh itu sah.                                                                                                                                                                                                                         |
| C1       | CL1           | P1      | Tugas terpilih sahaja | Ya          | Ya             | Ya         | Tidak sah       | Pelanggaran Peraturan #2.   </br>- C1 termasuk masa, perbelanjaan dan yuran pada subset tugas pada projek P1. </br>- CL2 termasuk masa, perbelanjaan dan yuran untuk seluruh projek P1 dan oleh itu bertindih dengan apa yang dimasukkan ke dalam C1.                                                                                                                                                                                          |
| C1       | CL2           | P1      | Kosong               | Ya          | Ya             | Ya         | Tidak sah       | Pelanggaran Peraturan #2.   </br>- C1 termasuk masa, perbelanjaan dan yuran pada subset tugas pada projek P1. </br>- CL2 termasuk masa, perbelanjaan dan yuran untuk seluruh projek P1 dan oleh itu bertindih dengan apa yang dimasukkan ke dalam C1.                                                                                                                                                                                          |
| C1       | CL1           | P1      | Tugas terpilih sahaja | Ya          | Ya             | Ya         | Sah           | Setiap Peraturan #3</br>- C1 termasuk masa, perbelanjaan dan yuran pada subset tugas pada projek P1. </br> - CL2 termasuk masa, perbelanjaan dan yuran untuk subset tugas pada projek P1. </br> Satu-satunya pengesahan tambahan ialah subset tugas pada CL1, yang berbeza daripada subset tugas pada CL2 untuk memastikan tiada pertindihan. Pengesahan ini dilengkapkan oleh sistem apabila tugas dikaitkan. |
| C1       | CL2           | P1      | Tugas terpilih sahaja | Ya          | Ya             | Ya         | Sah           | Setiap Peraturan #3</br>- C1 termasuk masa, perbelanjaan dan yuran pada subset tugas pada projek P1. </br> - CL2 termasuk masa, perbelanjaan dan yuran untuk subset tugas pada projek P1. </br> Satu-satunya pengesahan tambahan ialah subset tugas pada CL1, yang berbeza daripada subset tugas pada CL2 untuk memastikan tiada pertindihan. Pengesahan ini dilengkapkan oleh sistem apabila tugas dikaitkan. |