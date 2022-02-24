---
title: Anggarkan jualan dan kos projek apabila sumber boleh ditempah mengisi berbilang peranan pada projek
description: Topik ini menerangkan cara menggunakan dimensi penentuan harga untuk menyokong penentuan harga dan kos anggaran untuk sumber yang mengisi berbilang peranan pada projek.
author: rumant
manager: tfehr
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: da17f0f58623128d51fda0f5529182cd37ea41b9
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531505"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>Anggarkan jualan dan kos projek apabila sumber boleh ditempah mengisi berbilang peranan pada projek 

_**Digunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma dan Project Operations untuk senario berasaskan stok/pengeluaran_ 

Syarikat berasaskan projek selalunya mempunyai keperluan bagi satu sumber untuk mengisi berbilang peranan pada projek. Setiap peranan boleh ditetapkan harga dan dikoskan dengan cara yang berbeza. Ini bermakna bahawa masa sumber yang sama pada projek boleh mendapatkan anggaran kewangan yang berbeza bergantung pada kadar bil dan kos untuk setiap peranan. Anda boleh menyediakan nilai pada rekod ahli pasukan untuk sumber yang dinamakan dengan menggantikan salinan yang berbeza pada setiap tugas yang diberikan oleh ahli pasukan.

Contoh berikut membimbing anda melalui cara menggantikan nilai secara mudah membenarkan sumber mempunyai berbilang peranan pada projek dengan kadar kos dan bil yang berbeza.

## <a name="create-tasks"></a>Cipta tugas
Untuk mencipta tugas, anda perlu menambah tugas, serta tugas ringkasan, selepas itu anda perlu menugaskan tugas sebelum anda menambah tempoh tugas. 

### <a name="add-tasks-and-summary-tasks"></a>Tambah tugas dan tugas ringkasan
Untuk menambah tugas, lengkapkan langkah berikut.

1. Pergi ke **Projek** dan buka projek yang anda mahu tambah tugas.
2. Pilih **Tambah tugas baharu**. Namakan tugas dan kemudian tekan **Enter**.
3. Masukkan nama tugas lain dan tekan **Enter**. Ulang langkah ini sehingga anda mempunyai senarai penuh tugas.
3. Untuk mengengsot tugas di bawah tugas **ringkasan**, pilih tiga titik menegak dengan nama tugas dan kemudian pilih **Buat subtugas**. 

  > [!TIP]
  > Untuk memilih lebih daripada satu tugas, pilih tugas, tekan dan tahan **Ctrl** dan kemudian pilih tugas lain.
  >
  > Anda juga boleh memilih **Promosikan subtugas** untuk mengalih keluar tugas dari bawah tugas **ringkasan**.

### <a name="assign-tasks"></a>Tugaskan tugas

Lengkapkan langkah berikut untuk menugaskan tugas.

1. Dalam lajur **Ditugaskan kepada** untuk tugas, pilih ikon orang.
2. Pilih ahli pasukan daripada senarai atau masukkan teks untuk mencari nama.

### <a name="add-task-duration-and-columns"></a>Tambah tempoh tugas dan lajur

Selalunya paling mudah untuk mula membina projek anda dengan tempoh. Lengkapkan langkah berikut untuk menambah tempoh tugas.

1. Dalam lajur **Tempoh** untuk tugas, taipkan bilangan hari yang anda fikir akan diambil untuk menyempurnakan tugas. Jika anda mahu menggunakan unit masa yang berbeza, masukkan nombor ditambah dengan perkataan **jam**, **minggu** atau **bulan**.
2. Jika anda mahu tugas anda muncul sebagai pencapaian berbentuk berlian dalam pandangan **Garis masa**, dalam lajur **Tempoh**, masukkan **0 hari**.
3. Tekan **Enter** untuk pergi ke medan **Tempoh** tugas seterusnya dan terus memasukkan tempoh.

  > [!NOTE]
  > Anda tidak boleh memasukkan tempoh untuk tugas ringkasan.

Anda boleh menambah lajur ke projek anda untuk menyediakan lebih banyak maklumat. Untuk melakukan ini, pilih **Tambah lajur**. 

Untuk mendapatkan maklumat lanjut, lihat [Cipta projek](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>Sediakan peranan dan unit organisasi untuk ahli pasukan projek generik
Lengkapkan langkah berikut untuk menyediakan peranan dan unit organisasi kepada ahli pasukan generik.

1. Pada halaman **Tugas**, pilih baris **Tugas** untuk **Tugas A**. 
2. Dalam **Ditugaskan Kepada**, pilih **Tambah sumber generik**. Ini membuka halaman **Cipta Pantas Ahli Pasukan**.
3. Pada halaman **Cipta Pantas Ahli Pasukan**, tentukan atribut ahli pasukan generik yang boleh melaksanakan tugas ini.
4. Pilih unit peranan dan organisasi yang sesuai dan kemudian pilih **Simpan dan Tutup**. Ahli pasukan generik dicipta dan ditugaskan untuk tugas ini. 
5. Ulangi langkah 1-4 untuk **Tugas B**. Walau bagaimanapun, **Tugas B** mesti mempunyai peranan yang berbeza dan unit organisasi yang ditugaskan untuk ahli pasukan generik daripada **Tugas A**. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>Sediakan peranan dan unit organisasi untuk tugas projek
Lengkapkan langkah berikut untuk menyediakan peranan dan unit organisasi untuk tugas.

1. Selepas anda mencipta **Tugas A**, pilih tugas dan kemudian pilih ikon **i** untuk membuka anak tetingkap **Butiran Tugas**. 
2. Pada anak tetingkap **Butiran Tugas**, tatal ke bawah dan pilih **Lihat Butiran** untuk membuka halaman **Butiran Tugas**.
3. Pada halaman **Butiran Tugas**, dalam **Peranan** dan **Unit Organisasi**, tambah nilai yang diperlukan untuk melaksanakan tugas ini untuk sumber. 

  > [!NOTE]
  > Jika anda melengkapkan senario ini menggunakan data demo Project Operations, pilih **Berunding dengan Bakal Pelanggan** untuk peranan dan **Fabrikam Amerika Syarikat** sebagai unit organisasi.

4. Pilih **Tugas B** dan kemudian pilih tugas.
5. Pilih ikon **i** untuk membuka anak tetingkap **Butiran Tugas**. 
6. Pada anak tetingkap **Butiran Tugas**, tatal ke bawah dan pilih **Lihat butiran** untuk membuka halaman **Butiran Tugas**.
7. Pada halaman **Butiran Tugas**, dalam **Peranan** dan **Unit Organisasi**, tambah nilai yang diperlukan untuk sumber yang akan melaksanakan tugas ini. Nilai dalam **Peranan** dan **Unit Organisasi** untuk **Tugas B** mestilah berbeza berbanding dengan nilai untuk **Tugas A**. 

  > [!NOTE]
  > Jika anda melengkapkan senario ini menggunakan data demo Project Operations, pilih **Juruteknik Rangkaian** untuk peranan dan **Fabrikam Amerika Syarikat** sebagai unit organisasi.

8. Simpan dan tutup halaman **Butiran Tugas**. 

## <a name="team-member-and-estimates-behavior"></a>Ahli pasukan dan anggaran tingkah laku 
Untuk memahami tingkah laku pada grid **Ahli Pasukan** dan anggaran, lengkapkan langkah berikut.

1. Pada grid **Ahli Pasukan**, pilih dua ahli pasukan generik dan kemudian pilih **Jana Keperluan**. Ini akan menjana keperluan sumber. 
2. Pilih baris ahli pasukan untuk **Berunding dengan Bakal Pelanggan** dan kemudian pilih **Tempah**. Papan jadual dibuka dengan senarai sumber. Pilih sumber dan kemudian pilih **Tempah** untuk menempah sumber kepada keperluan tersebut.
3. Pilih baris ahli pasukan untuk **Juruteknik Rangkaian** dan kemudian pilih **Tempah**. Papan jadual dibuka dengan senarai sumber. Pilih sumber yang sama seperti di atas dan kemudian pilih **Tempah** untuk menempah sumber kepada keperluan tersebut.

### <a name="team-member-grid"></a>Grid Ahli Pasukan 

Pada grid **Ahli Pasukan**, dua rekod ahli pasukan generik dipadamkan dan digantikan dengan hanya satu sumber. Terdapat satu set nilai untuk sumber tersebut yang merupakan set nilai lalai untuk **Peranan** dan **Unit Organisasi**.

Apabila anda mengembangkan baris untuk rekod ahli pasukan tersebut, anda boleh melihat penugasan yang berbeza pada rekod ahli pasukan untuk kedua-dua tugas. Setiap baris penugasan mempunyai nilai khusus tugas untuk **Peranan** dan **Unit Organisasi**. 

### <a name="estimates-grid"></a>Grid anggaran 

Pada grid **Anggaran**, kedua-dua penugasan untuk sumber yang sama ditetapkan harga dengan cara yang berbeza. Penugasan untuk sumber pada **Tugas A** ditetapkan harga menggunakan nilai atribut **Peranan** bagi **Berunding dengan Bakal Pelanggan**. Penugasan untuk sumber yang sama pada **Tugas B** ditetapkan harga menggunakan nilai atribut **Peranan** bagi **Juruteknik Rangkaian**.
