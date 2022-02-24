---
title: Petakan projek dan tugas ke baris kontrak berasaskan projek - lite
description: Topik ini menyediakan maklumat tentang menambah dan mengalih keluar projek dan tugas ke baris kontrak.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4737f9870904bfc7adac11b8e2aa13bb8c610ca3
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858108"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line"></a>Petakan projek dan tugas pada baris kontrak berdasarkan projek 

_**Gunakan Pada:** Pelaksanaan ringan - urusan untuk penginvoisan proforma, Project Operations untuk senario berdasarkan sumber/bukan stok_

Pada baris kontrak berasaskan projek, anda boleh memetakan tugas tertentu dalam projek ke baris kontrak.

Apabila anda memetakan tugas tertentu ke baris kontrak, kaedah pengebilan, pilihan kebolehtuntutan, had tidak boleh dilebihi dan pelanggan ditakrifkan pada baris kontrak akan digunakan ke tugas tertentu itu sahaja.

Jika anda mempunyai senario satu fasa projek, contohnya Fasa Prototaip adalah harga tetap dan semua fasa yang lain adalah masa dan bahan, anda akan dapat mengaitkan fasa Prototaip dan semua tugas anak yang berkaitan dengan baris kontrak untuk fasa dengan kaedah pengebilan harga tetap.

Semua fasa lain dalam struktur pecahan kerja projek (WBS) anda boleh dikaitkan dengan masa dan baris kontrak berasaskan bahan.

## <a name="associate-tasks-to-project-based-contract-lines"></a>Kaitkan tugas ke baris kontrak berasaskan projek

Tugas boleh dikaitkan ke baris kontrak daripada tab **Tugas Boleh Dicaj** pada halaman **Baris Kontrak** atau daripada tab **Pengebilan Tugas** pada halaman **Projek**.

### <a name="from-the-contract-line-page"></a>Daripada halaman baris Kontrak

Lengkapkan langkah berikut untuk mengaitkan tugas projek ke baris kontrak daripada tab **Tugas boleh Dicaj** bagi halaman **Baris Kontrak**.

1. Pada tab **Umum** baris kontrak berasaskan projek, sahkan bahawa medan **Projek** telah diisi.
2. Dalam medan **Tugas Yang Disertakan**, pilih **Tugas Yang Dipilih Sahaja**.
3. Simpan perubahan anda. Borang akan disegar semula dan tab **Tugas Boleh Dituntut** akan kelihatan.
4. Pilih tab **Tugas Boleh Dituntut** dan dalam sub grid, pilih **Tambah Tugas Baris Kontrak**.
5. Pada halaman **Tugas Baris Kontrak**, dalam juntai bawah **Tugas**, pilih tugas. 
6. Masukkan maklumat dalam medan **Jenis Pengebilan** dan kemudian pilih **Simpan dan Tutup**. Tugas yang dipilih adalah berkaitan dengan baris kontrak.

> [!NOTE]
> Ini bukan pengalaman yang paling optimum untuk mengaitkan tugas projek ke baris kontrak. Setiap projek perlu dikaitkan secara manual dalam pengalaman ini. Cara yang paling disukai ialah daripada tab **Pengebilan Tugas** pada halaman **Projek**.

### <a name="from-the-project-page"></a>Daripada halaman projek

Ini adalah kaedah optimum untuk mengaitkan tugas ke baris kontrak. Anda boleh memilih pelbagai tugas dan mengaitkan semua tugas itu dan tugas anaknya ke baris kontrak yang dipilih. Lengkapkan langkah berikut untuk mengaitkan tugas ke baris kontrak daripada halaman **Projek**.

1. Pada tab **Umum** baris kontrak berasaskan projek, sahkan bahawa medan **Projek** telah diisi.
2. Pada medan **Tugas Yang Disertakan**, pilih **Tugas Yang Dipilih Sahaja**.
3. Simpan baris kontrak berasaskan projek. Borang akan disegar semula dan tab **Tugas Boleh Dituntut** akan kelihatan. Ini hanya untuk tujuan pengesahan sahaja.
4. Pada tab **Umum** baris kontrak berasaskan projek, dalam medan **Projek**, pilih pautan projek.
5. Pada halaman **Projek**, pilih tab **Sediakan Pengebilan Tugas**.
6. Terdapat dua grid. Salah satu grid adalah untuk baris kontrak yang digunakan untuk seluruh projek. Grid kedua digunakan untuk persediaan pengebilan khusus tugas. Dalam grid kedua, pilih satu atau lebih tugas dan kemudian pilih **Kaitkan Baris Kontrak**.
7. Dalam halaman dialog yang terbuka, pilih baris kontrak daripada juntai bawah.
8. Gunakan juntai bawah **Jenis Pengebilan** untuk menanda tugas sebagai boleh dicaj atau tidak boleh dicaj.
9. Pilih kotak semak untuk menunjukkan sama ada perkaitan juga perlu menyertakan tugas anak bagi tugas yang dipilih. Semakan kotak juga akan mengaitkan tugas anak bagi tugas yang dipilih ke baris kontrak.
10. Pilih **OK** untuk menutup dialog.

## <a name="unassociate-tasks-from-project-based-contract-lines"></a>Nyahkaitkan tugas daripada baris kontrak berasaskan projek

### <a name="from-the-contract-line-page"></a>Daripada halaman baris kontrak

Lengkapkan langkah berikut untuk menyahkaitkan tugas projek daripada baris kontrak pada tab **Tugas boleh Dicaj** bagi halaman **Baris Kontrak**.

1. Pada tab **Tugas Boleh Dicaj**, pilih **Padam Tugas Baris Kontrak**.
2. Mesej amaran menunjukkan bahawa mengalih keluar perkaitan ini boleh menyebabkan pembalikan semula sebarang aktual yang dirakamkan sebelum ini pada tugas. Pilih **OK** pada dialog untuk mengalih keluar perkaitan antara tugas dan baris kontrak berasaskan projek. 

> [!NOTE]
> Ini tidak memadamkan tugas daripada projek. Sebaliknya, ia mengalih keluar perkaitan tugas daripada baris kontrak berasaskan projek.

### <a name="from-the-project-page"></a>Daripada halaman projek

Ini adalah pengalaman yang lebih optimum untuk menyahkaitkan tugas daripada baris kontrak. Anda boleh memilih pelbagai tugas dan menyahkaitkan semua tugas itu dan tugas anaknya daripada baris kontrak yang dipilih. Lengkapkan langkah berikut untuk menyahkaitkan tugas daripada baris kontrak.

1. Daripada tab **Umum** baris kontrak berasaskan projek, dalam medan **Projek**, klik pada pautan untuk projek.
2. Pada halaman **Projek**, pilih tab **Sediakan Pengebilan Tugas**.
3. Terdapat dua grid pada halaman. Satu grid adalah untuk baris kontrak yang digunakan ke seluruh projek dan yang kedua digunakan untuk persediaan pengebilan khusus tugas. Dalam grid kedua, pilih satu atau lebih tugas dan kemudian pilih **Nyahkaitkan Baris Kontrak**.
4. Dalam halaman dialog yang terbuka, pilih baris kontrak daripada juntai bawah.
5. Pilih kotak semak untuk menunjukkan sama ada perkaitan juga perlu dialih keluar daripada tugas anak bagi tugas yang dipilih. Semakan kotak juga akan menyahkaitkan tugas anak bagi tugas yang dipilih daripada baris kontrak.
6. Pilih **OK**. Mesej amaran menunjukkan bahawa mengalih keluar perkaitan ini boleh menyebabkan pembalikan semula sebarang aktual yang dirakamkan sebelum ini pada tugas. Pilih **OK** pada dialog amaran untuk mengalih keluar perkaitan antara tugas dan baris kontrak berasaskan projek.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
