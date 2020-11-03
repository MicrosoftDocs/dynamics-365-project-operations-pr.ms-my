---
title: Anggarkan jualan dan kos projek apabila sumber boleh ditempah mengisi berbilang peranan pada projek
description: Topik ini memberikan maklumat tentang cara dimensi penetapan harga yang boleh digunakan untuk menyokong penetapan harga dan kos bagi sumber yang memenuhi berbilang peranan pada projek.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081280"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a>Anggarkan jualan dan kos projek apabila sumber boleh ditempah mengisi berbilang peranan pada projek 

Syarikat berasaskan projek selalunya memerlukan satu sumber untuk melaksanakan berbilang peranan pada projek. Setiap peranan ini mungkin berharga dan berkos berbeza yang bermaksud masa sumber yang sama pada projek boleh mendapatkan anggaran kewangan yang berbeza bergantung kepada kadar bil dan kos bagi setiap peranan. Project Service Automation membolehkan penyediaan nilai pada rekod ahli pasukan untuk sumber yang bernama dan membolehkan untuk digantikan pada setiap tugas yang diberikan kepada ahli pasukan.

Contoh berikut menerangkan bagaimana penggantian mudah bagi nilai ini membenarkan sumber mempunyai berbilang peranan pada projek dengan kadar kos dan bil yang berbeza.

## <a name="create-tasks"></a>Cipta tugas
Cipta dua tugas projek untuk 40 jam setiap satunya, Tugas A dan Tugas B. Pilih Tugas A sebagai yang terdahulu kepada Tugas B.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Sediakan Unit Peranan dan Organisasi untuk ahli pasukan projek generik

1. Pada halaman **Jadual** , pilih baris **Tugas** untuk Tugas A. 
2. Dalam medan **Sumber** , pilih **Cipta** dalam senarai juntai bawah.
3. Pada halaman **Cipta Pantas Ahli Pasukan** , tentukan atribut ahli pasukan generik yang boleh melaksanakan tugas ini.
4. Pilih unit peranan dan organisasi yang sesuai dan kemudian pilih **Simpan dan Tutup**. Ahli pasukan generik dicipta dan ditugaskan untuk tugas ini. 

Ulangi langkah ini untuk Tugas B dan pastikan bahawa peranan dan unit organisasi pada ahli pasukan generik dicipta untuk Tugas B adalah berbeza daripada Tugas A. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Sediakan unit peranan dan organisasi untuk tugas projek

1. Selepas anda mencipta Tugas A, pilih tugas dan kemudian pilih **Edit tugas**.
2. Pada halaman **Butiran Tugas** , cari medan **Peranan** dan **Unit Organisasi** , tambah nilai yang memerlukan sumber yang akan melaksanakan tugas ini. 

  > [!NOTE]
  > Jika anda melengkapkan senario ini menggunakan data demo Project Service Automation, pilih **Berunding dengan Bakal Pelanggan** untuk peranan dan **Fabrikam US** sebagai unit organisasi.

3. Pilih Tugas B dan kemudian pilih **Edit tugas**.
4. Pada halaman **Butiran Tugas** , cari medan **Peranan** dan **Unit Organisasi** , tambah nilai yang memerlukan sumber yang akan melaksanakan tugas ini. Pastikan bahawa nilai dalam medan **Peranan** dan **Unit Organisasi** adalah berbeza untuk Tugas B daripada nilai untuk Tugas A. 

  > [!NOTE]
  > Jika anda melengkapkan senario ini menggunakan data demo Project Service Automation, pilih **Juruteknik Rangkaian** untuk peranan dan **Fabrikam US** sebagai unit organisasi.

5. Simpan dan tutup halaman **Butiran Tugas**. 

## <a name="team-member-and-estimates-behaviour"></a>Ahli pasukan dan anggaran tingkah laku 

1. Pada halaman **Butiran Tugas** , pada **Ahli Pasukan** , pilih dua ahli pasukan generik dan kemudian pilih **Jana Keperluan**. Ini akan menjana keperluan sumber. 
2. Pilih baris ahli pasukan untuk **Berunding dengan Bakal Pelanggan** dan kemudian pilih **Tempah**. Papan jadual membuka dan menempah sumber mengikut keperluan tersebut.
3. Pilih baris ahli pasukan untuk **Juruteknik Rangkaian** dan kemudian pilih **Tempah**. Papan jadual membuka dan menempah sumber yang sama mengikut keperluan tersebut.

### <a name="team-member-grid"></a>Grid Ahli Pasukan 
Pada grid **Ahli Pasukan** , perhatikan bahawa kedua-dua rekod ahli pasukan generik telah dipadamkan dan telah digantikan dengan satu sumber. Terdapat satu set nilai untuk sumber itu yang menunjukkan set nilai lalai untuk **Peranan** dan **Unit Organisasi**.
Apabila anda mengembangkan baris rekod Ahli Pasukan tersebut, anda boleh melihat tugasan berbeza pada rekod ahli pasukan bagi kedua-dua tugas tersebut. Setiap baris tugasan mempunyai peranan yang khusus untuk **Peranan** dan **Unit Organisasi**. 

### <a name="estimates-grid"></a>Grid anggaran 
Apabila anda menavigasi ke grid **Anggaran** , anda akan dapati bahawa kedua-dua tugasan untuk sumber yang sama berharga berbeza.
Tugasan untuk sumber pada Tugas A adalah berharga menggunakan nilai atribut **Peranan** bagi **Berunding dengan Bakal Pelanggan**. Tugasan untuk sumber sama pada Tugas B adalah berharga menggunakan nilai atribut **Peranan** bagi **Juruteknik Rangkaian**.




