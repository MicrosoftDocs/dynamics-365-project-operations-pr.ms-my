---
title: Entri masa tingkah laku UI
description: Topik ini memberikan maklumat tentang tingkah laku UI untuk Entri Masa.
author: stsporen
ms.date: 03/03/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: fd62fb1d8e0b2d859cb7da8b99cb725af587ff2f
ms.sourcegitcommit: 639ec8a41fda15dedfd6918702d33ea406999ba6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304312"
---
# <a name="time-entry-ui-behavior"></a>Entri masa tingkah laku UI

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_


Grid **Entri masa mingguan** adalah kawalan tersuai yang mempunyai dua bahagian utama, **Dimensi** dan **Tempoh**.

## <a name="keyboard-shortcuts"></a>Pintasan papan kekunci
| Tindakan        | Pintasan                  |
|------------   |------------------------   |
| Baru           | Alt + Shift + n           |
| Salin baris      | Alt + Shift + c           |
| Edit entri    | Alt + Shift + e           |
| Edit baris      | Alt + Shift + Ctrl + e    |
| Buka entri    | Alt + Shift + o           |
| Serah        | Alt + Shift + s           |
| Panggil Balik        | Alt + Shift + r           |
| Delete        | Alt + Shift + d           |
| Salin minggu     | Alt + Shift + w           |

## <a name="dimensions"></a>Dimensi
Bahagian **Dimensi** menunjukkan dimensi yang boleh dimasuki masa. Dimensi berikut adalah disokong di luar kotak:

  - Project
  - Tugas Projek
  - Peranan
  - Jenis
  - Status Entri

Bahagian **Dimensi** tidak membenarkan pengeditan sebaris. Bahagian ini disokong oleh pandangan yang mendayakan medan tersuai untuk ditambah ke grid kemasukan masa mingguan.

## <a name="duration"></a>Tempoh
Bahagian Tempoh menunjukkan hari minggu sebagai pengepala lajur. Bahagian ini membenarkan pengeditan sebaris. Selepas baris entri masa dicipta dengan dimensi yang sesuai, pengguna dengan pantasnya boleh memasukkan jumlah masa yang mereka belanjakan pada dimensi tersebut.

## <a name="create-a-new-time-entry"></a>Cipta entri masa baharu

1. Dalam grid entri masa, pilih **Baharu**. 
2. Dalam kotak dialog **Cipta Pantas Entri Masa**, pilih tarikh entri masa.
3. Masukkan data untuk **Projek**, **Tugas Projek**, **Peranan**, dan dimensi **Tempoh**. Maklumat ini sepatutnya ditambah dalam minit, jam, atau hari dengan menaip **h**, **m**, atau **d**, bersama dengan nombor. 
4. Masukkan perihalan untuk entri dan sebarang komen yang boleh dikongsi secara luaran berkenaan entri masa. 

Apabila anda menyimpan entri, nilai yang dimasukkan muncul dalam bahagian **Dimensi**. Maklumat yang dimasukkan dalam medan **Tempoh** muncul pada tarikh entri masa diciptakan.

Medan carian disokong oleh pandangan sistem. Sebagai contoh, selepas pengguna memasuki projek, medan **Tugas Projek** ditetapkan kepada pandangan **Salinan** secara lalai. Bagi mencipta entri masa untuk tugas yang tidak ditugaskan kepada pengguna, pilih **Ubah pandangan** pada kotak dialog carian dan kemudian pilih pandangan **Semua Tugas Projek Aktif**.

## <a name="edit-a-time-entry"></a>Edit entri masa 
Butiran daripada beberapa medan pada halaman entri masa, seperti **Perihalan** dan **Komen Luaran** tidak ditunjukkan dalam grid entri masa mingguan. Sebaliknya, penunjuk segi tiga yang kecil muncul dalam sel **Tempoh** yang mempunyai butiran tambahan ini. 

1. Untuk mengedit entri masa, pilih sel yang anda mahu kemas kini dalam entri masa.
2. Pilih **Edit Butiran** untuk mengemas kini data dalam anak tetingkap **BorangUtama Entri Masa**. 

## <a name="copy-a-time-entry-row"></a>Salin baris entri masa
Selepas baris telah dicipta, anda boleh pilih **Salin Baris** untuk menyalin keseluruhan baris ke baris baharu. Apabila baris disalin dengan cara ini, dimensi dan tempoh juga disalin. Anda juga boleh pilih **Edit Baris** untuk mengemas kini nilai dimensi dan tempoh dalam bahagian **Tempoh**.

## <a name="open-a-time-entry-behavior"></a>Buka tingkah laku entri masa
Untuk menyokong entri yang optimum dan pantas dalam medan paling penting, grid entri masa mingguan menunjukkan subset dimensi yang dipilih dan tempoh masa. Untuk melihat semua butiran kemasukan satu masa, di bawah **Edit Entri**, pilih **Buka.**

## <a name="submit-a-time-entry"></a>Serahkan entri masa
Anda boleh menyerahkan entri masa tunggal atau kumpulan entri masa dengan memilih satu blok sel atau baris entri masa keseluruhan, dan kemudian memilih **Serahkan**. Penyertaan masa yang dihantar akan muncul sebagai entri yang menunggu kelulusan pada halaman **Kelulusan**. Selepas penyertaan masa berjaya diserahkan, ia tidak boleh diedit.

## <a name="recall-a-time-entry"></a>Tarik balik entri masa
Anda boleh mengingati entri masa yang telah anda serahkan. Anda boleh mengingati kemasukan satu kali, blok baris masa atau keseluruhan entri masa. Entri masa yang ditarik balik boleh diedit.

## <a name="time-entry-status"></a>Status entri masa

- **Draf**: Entri masa baharu secara automatik ditugaskan status **Draf**. Hanya entri masa yang mempunyai status **Draf** boleh dipadamkan.
- **Diserahkan**: Apabila entri masa diserahkan, status dikemas kini kepada **Diserahkan**. 
- **Diluluskan**: Apabila entri masa yang diserahkan diluluskan, status dikemas kini kepada **Diluluskan**. 
- **Dikembalikan**: Jika entri masa ditolak, status dikemas kini kepada **Dikembalikan**, dan entri menjadi tersedia untuk pembetulan dan diserahkan semula. 

## <a name="view-rejection-comments"></a>Lihat komen penolakan
Apabila entri masa telah ditolak oleh pelulus, pelulus mungkin menambah komen untuk membantu sumber memahami sebab kepada penolakan. Untuk melihat komen penolakan untuk kemasukan masa, pilih **Buka entri.** Komen penolakan akan ditunjukkan dalam garis masa. Pengguna boleh respons kepada komen penolakan sebelum mereka menyerahkan semula entri.

## <a name="copy-week"></a>Salin minggu
Selepas beberapa entri masa telah dicipta, pengguna boleh mencipta berbilang entri masa pada masa yang sama.

1. Dalam borang **Entri Masa**, pilih **Salin Minggu** kepada cipta pukal entri masa tambahan. 
2. Dalam kotak dialog **Salin**, dalam bahagian **Dari tempoh**, gunakan medan **Tarikh Mula** dan **Tarikh Akhir** untuk mentakrif julat tarikh untuk menyalin entri masa. 
3. Dalam bahagian **Ke Tempoh** dalam medan **Tarikh Mula** tentukan tarikh untuk mencipta entri masa. 
4. Pilih **Salin**. Untuk tarikh yang ditentukan dalam **Pada tempoh**, salinan entri masa untuk hari dalam minggu yang berkaitan dalam **Dari tempoh** dicipta. Contohnya, entri masa hari Isnin dari minggu lepas disalin ke hari Isnin minggu yang ditentukan sebagai **Pada tempoh**.

## <a name="import"></a>Import
Proses asas yang sama digunakan untuk mengimport daripada tempahan, tugas dan pertukaran. Anda boleh tentukan julat tarikh bagi penempahan yang diimport daripada dan kemudian secara eksplisit memilih penempahan yang sepatutnya disalin ke dalam draf entiti masa. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
