---
title: Petakan projek dan tugas kepada baris sebut harga berasaskan projek
description: Topik ini memberikan maklumat mengenai cara untuk memetakan projek dan tugas kepada baris tugas berasaskan projek.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 871d323136cd982bd48ed9aa2b9c34017951d2d8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130724"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a>Petakan projek dan tugas kepada baris sebut harga berasaskan projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Pada baris sebut harga berasaskan projek, anda boleh memetakan tugas khusus projek yang sudah dikaitkan kepada baris sebut harga.

Apabila anda memetakan tugas kepada baris sebut harga, item berikut yang anda takrifkan pada baris sebut harga hanya akan digunakan pada tugas tersebut:

- Kaedah pengebilan
- Pilihan boleh dikenakan caj
- Had yang tidak melebihi
- Pelanggan

Contohnya, anda mungkin mempunyai projek yang satu fasa adalah harga tetap dan semua fasa lain adalah masa dan bahan. Dalam kes ini, anda boleh mengaitkan fasa pertama dan semua tugas anak kepada baris sebut harga untuk fasa tersebut dengan kaedah pengebilan harga tetap. Anda kemudian boleh mengaitkan semua fasa lain kepada masa dan baris sebut harga berasaskan bahan.

## <a name="associate-tasks-to-project-based-quote-lines"></a>Kaitkan tugas kepada baris sebut harga berasaskan projek

Anda boleh mengaitkan tugas dengan baris sebut harga daripada lokasi berikut:

- Halaman **Projek** > tab **Pengebilan tugas** (optimum)
- Halaman **Baris Sebut Harga** > tab **Tugas boleh dicaj** 

### <a name="from-the-project-page"></a>Daripada halaman Projek

Halaman **Projek** menyediakan pengalaman optimum untuk mengaitkan tugas kepada baris sebut harga. Anda boleh menggunakan halaman ini untuk memilih berbilang tugas dan mengaitkan semuanya, ditambah dengan tugas anaknya kepada baris sebut harga terpilih.

1. Pada tab **Umum** bagi baris sebut harga berasaskan projek, sahkan medan **Projek** telah diisi.
2. Dalam medan **Tugas yang disertakan**, pilih **Tugas terpilih sahaja**.
3. Simpan baris sebut harga berasaskan projek. Apabila borang disegar semula, tab **Tugas boleh dicaj** dipaparkan.
4. Pada tab **Umum**, pilih pautan untuk projek daripada medan **Projek**.
5. Pada halaman **Projek**, pilih tab **Pengebilan tugas**.
6. Dalam grid kedua, yang digunakan kepada persediaan pengebilan berkhususkan tugas, pilih satu atau lebih tugas dan kemudian pilih **Kaitkan baris sebut harga**.
7. Dalam halaman dialog yang muncul, pilih baris sebut harga yang memaparkan baris sebut harga berasaskan projek pada sebut harga.
8. Dalam medan **Jenis pengebilan**, menunjukkan jika tugas ini boleh dikenakan caj atau tidak boleh dikenakan caj.
9. Pilih kotak semak untuk menunjukkan jika perkaitan harus memasukkan tugas anak bagi tugas terpilih. Menyemak kotak akan mengaitkan tugas anak bagi tugas terpilih kepada baris sebut harga.
10. Pilih **OK** untuk menutup dialog.

### <a name="from-the-quote-line-page"></a>Daripada halaman baris sebut harga

Anda boleh mengaitkan tugas projek kepada baris sebut harga daripada tab **Tugas boleh dicaj** pada halaman **Baris sebut harga**.

>[!NOTE]
>Tempat yang optimum untuk mengaitkan tugas projek kepada baris sebut harga pada tab **Pengebilan tugas** pada halaman **Projek**. Jika anda mengaitkan tugas daripada tab **Tugas boleh dicaj** pada halaman **Baris sebut harga**, anda mesti mengaitkan setiap projek secara manual.

1. Pada tab **Umum** bagi baris sebut harga berasaskan projek, sahkan terdapat projek terpilih di dalam medan **Projek**.
2. Dalam medan **Tugas yang disertakan**, pilih **Tugas terpilih sahaja**.
3. Simpan baris sebut harga berasaskan projek. Apabila borang disegar semula, tab **Tugas boleh dicaj** dipaparkan.
4. Pada tab **Tugas boleh dicaj**, pilih **Tambah tugas baris sebut harga**.
5. Pada halaman **Tugas baris sebut harga**, di dalam medan **Tugas**, pilih tugas dan di dalam medan **Jenis pengebilan**, pilih **Simpan**. 
6. Tutup halaman. Tugas terpilih kini dikaitkan kepada baris sebut harga.

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a>Pisahkan tugas kepada baris sebut harga berasaskan projek

### <a name="from-the-project-page"></a>Daripada halaman Projek

Kaedah ini menyediakan pengalaman paling optimum untuk memisahkan tugas daripada baris sebut harga. Anda boleh memilih berbilang tugas dan memisahkan semuanya, ditambah dengan tugas anaknya daripada baris sebut harga terpilih.

1. Pada tab **Umum** bagi baris sebut harga berasaskan projek, di dalam medan **Projek**, pilih pautan projek.
2. Pada halaman **Projek**, pilih tab **Pengebilan tugas**.
3. Dalam grid kedua, yang digunakan kepada persediaan pengebilan berkhususkan tugas, pilih satu atau lebih tugas dan kemudian pilih **Pisahkan baris sebut harga**.
4. Dalam halaman dialog yang muncul, pilih baris sebut harga.
5. Pilih kotak semak untuk menunjukkan sama ada hubungan juga harus dialih keluar daripada tugas anak bagi tugas terpilih. Menyemak kotak juga akan memisahkan tugas anak bagi tugas terpilih kepada baris sebut harga.
6. Pilih **OK**. Mesej amaran memberitahu anda bahawa jika anda telah mengalih keluar perkaitan ini, sebarang rekod pada tugas sebelum ini boleh diterbalikkan. 
7. Pilih **OK** untuk meneruskan dan mengalih keluar perkaitan antara tugas dan baris sebut harga berasaskan projek.

### <a name="from-the-quote-line-page"></a>Daripada halaman baris sebut harga

Anda juga boleh memisahkan tugas projek kepada baris sebut harga daripada tab **Tugas boleh dicaj** pada halaman **Baris sebut harga**.

1. Pada tab **Tugas boleh dicaj**, pilih **Padam tugas baris sebut harga**.
2. Pilih **OK**. Mesej amaran memberitahu anda bahawa jika anda telah mengalih keluar perkaitan ini, sebarang rekod pada tugas sebelum ini boleh diterbalikkan. 
3. Pilih **OK** untuk meneruskan dan mengalih keluar perkaitan antara tugas dan baris sebut harga berasaskan projek.

>[!NOTE]
> Prosedur ini tidak memadam tugas daripada projek tersebut. Ia hanya mengalih keluar perkaitan tugas daripada baris sebut harga berasaskan projek.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]