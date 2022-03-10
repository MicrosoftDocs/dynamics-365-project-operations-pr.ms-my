---
title: Uruskan anggaran pendapatan
description: Topik ini menyediakan maklumat tentang cara bekerja dengan anggaran hasil untuk projek.
author: sigitac
ms.date: 11/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8d118826f8c63b9540435e320924d4562ab191ba126088560f5def1c1ff0b908
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996537"
---
# <a name="manage-revenue-estimates"></a>Uruskan anggaran pendapatan

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Anda boleh mencipta, mengira, menyiarkan, membalikkan atau menghapuskan anggaran hasil. Anda boleh melakukan perkara ini sama ada secara manual atau dengan menggunakan proses berkala. Topik ini menyediakan maklumat tentang cara bekerja dengan anggaran hasil untuk projek.

### <a name="manage-revenue-estimates-manually"></a>Uruskan anggaran hasil secara manual

Pada projek anggaran hasil harga tetap atau halaman **Pertanyaan anggaran** (**Pengurusan projek dan perakaunan** > **Laporan dan pertanyaan** > **Pertanyaan dan laporan anggaran**), pilih **Anggaran**.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Uruskan anggaran hasil menggunakan proses berkala

Pergi ke **Pengurusan projek dan perakaunan** > **Berkala** > **Anggaran** dan pilih proses yang sepadan.

## <a name="create-a-revenue-estimate"></a>Cipta anggaran hasil

Lengkapkan langkah yang berikut untuk mencipta anggaran hasil. 

1. Pergi ke **Pengurusan projek dan anggaran** > **Berkala** > **Anggaran**.
2. Pilih **Baharu**. Pada halaman **Penciptaan anggaran**, pilih parameter berikut:

   - **Kod tempoh**: Kod ini menentukan kekerapan anggaran disiarkan.
   - **Tarikh anggaran**: Tarikh anggaran diproses.
   - **Berterusan**: Pilih kotak semak ini untuk mencipta anggaran hanya jika anggaran disiarkan dalam tempoh sebelumnya, atau jika anggaran adalah anggaran pertama yang telah dicipta. Jika ini tidak dipilih, anggaran dicipta walaupun anggaran tidak disiarkan dalam tempoh sebelumnya.
   - **Kaedah kos untuk melengkapkan**: Tentukan cara untuk menganggarkan baki kerja projek. Untuk maklumat lanjut, lihat [Kaedah kos untuk melengkapkan](cost-complete-methods.md).
   - **Kaedah penyelesaian**: Pilih kaedah penyelesaian daripada pilihan berikut:
     - **Automatik**: Peratusan siap dikira secara automatik dan berdasarkan garisan kos yang dimasukkan dalam pengiraan. Templat kos mentakrifkan garisan kos yang disertakan.
     - **Manual**: Peratusan siap bersamaan dengan peratusan siap bagi anggaran terakhir. Selepas anggaran dicipta, anda boleh menukar **Pengiraan manual** pada halaman **Anggaran**.
     - **Daripada templat kos**: Gabungan kaedah automatik dan manual. Pilihan ini ditetapkan secara automatik atau manual, bergantung kepada nilai lalai dalam templat kos.
   - **Model ramalan**: Pilih model ramalan untuk anggaran.
   - **Cetak senarai anggaran**: Cipta dan tunjukkan senarai anggaran. Senarai tersebut mengandungi status fungsi semasa. Anda boleh mencetak sebarang amaran tentang anggaran pada laporan. Syarat-syarat berikut menyebabkan amaran untuk muncul dalam senarai anggaran:
     - Peratusan siap melebihi 100 peratus.
     - Peratusan siap kurang daripada sifar peratus.
     - Jumlah negatif dalam lajur **Untuk selesai**.
     - Anggaran tanpa amaun kontrak yang sepadan.
     - Anggaran tanpa anggaran kos yang dilampirkan.
   - **Tunjukkan Infolog**: Pilih pilihan ini untuk menerima mesej yang mengandungi maklumat tentang projek anggaran yang diproses semasa kerja dijalankan.


## <a name="post-wip-or-accruals"></a>Siarkan WIP atau akruan

Selepas anggaran dinilai, ia dikekalkan, dikurangkan atau ditingkatkan. Anda kemudiannya boleh menyiarkan WIP apabila anda bekerja dengan prinsip penilaian **Kontrak yang telah dilengkapkan**, atau siarkan akruan apabila anda bekerja dengan prinsip penilaian **Peratusan yang telah dilengkapkan**.
  
Status tempoh anggaran berubah daripada **Dicipta** kepada **Disiarkan**.

## <a name="reverse-wip-or-accruals"></a>Terbalikkan WIP atau akruan

Gunakan pilihan terbalik untuk mengkredit WIP atau akruan yang sudah disiarkan, dan kemudian buat anggaran untuk tempoh tersebut.

> [!NOTE]
> Untuk membalikkan tempoh yang berada di antara tempoh masa lain, balikkan tempoh anggaran yang perlu dan kemudian siarkan semula. Kerana semua tempoh berikut bergantung pada anggaran daripada tempoh sebelumnya, jangan melangkau sebarang tempoh.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>Hapuskan projek anggaran dan tamatkan projek

Langkah terakhir dalam proses anggaran ialah untuk menghapuskan projek anggaran dan menamatkan projek harga tetap apabila peratusan siap mencapai 100 peratus.

Berikut berlaku apabila anda menjalankan penyingkiran:

- Untuk projek harga tetap dengan kontrak yang lengkap, nilai WIP yang jelas daripada akaun baki dan siarkan kepada akaun untung rugi.
- Bagi projek harga tetap dengan peratusan yang lengkap, akruan akan dialih keluar daripada akaun untung rugi.

Anggaran mengubah status kepada **Disingkirkan**.

> [!NOTE]
> Dalam kes khas, peratusan boleh lanjut melebihi 100 peratus. Apabila ini berlaku, mengurangkan peratusan siap dengan menggunakan **Kaedah tetapkan kos untuk melengkapkan kepada sifar** untuk mencapai 100 peratus.

## <a name="reverse-elimination"></a>Balikkan penyingkiran

1. Pergi ke **Pengurusan dan perakaunan projek** > **Berkala** > **Anggaran** > **Balikkan penyingkiran**. 
2. Pada Anak Tetingkap Tindakan, pada tab **Proses**, dalam kumpulan **Kekalkan**, pilih **Anggaran**. 
3. Pilih **Balikkan penyingkiran**.

Gunakan halaman ini untuk membalikkan semua penyingkiran dengan tarikh anggaran yang ditetapkan dan dengan status anggaran **Disingkirkan**. Status transaksi berubah selepas anda memilih medan yang sesuai.

Ini juga secara automatik mengubah status projek kepada **Dalam proses** jika peringkat projek ditetapkan kepada selesai. Status anggaran tempoh projek berubah kembali ke **Disiarkan**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]