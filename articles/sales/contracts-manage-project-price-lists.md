---
title: Urus senarai harga projek pada kontrak projek
description: Topik ini menyediakan maklumat tentang pengurusan sebut harga projek pada kontrak projek.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2cfac6eda64d1d8e578115bba07942a7d786328f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278609"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Urus senarai harga projek pada kontrak projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Kontrak projek dalam Dynamics 365 Project Operations direka bentuk untuk menyokong berbilang tarikh senarai harga yang berkesan pada kontrak. Dalam Project Operations, terdapat satu entiti berkaitan baharu yang dipanggil **Senarai Harga Projek**. Entiti ini mempunyai perhubungan satu kepada banyak ke kontrak projek.

Senarai Harga projek digunakan untuk mengira masa dan transaksi perbelanjaan pada projek. Apabila kontrak mempunyai satu atau lebih senarai harga projek, senarai harga yang digunakan ke harga untuk masa dan anggaran perbelanjaan dan aktual ke atas projek yang berkaitan dengan kontrak melalui baris kontrak.

Apabila tiada senarai harga projek pada kontrak projek, anda akan melihat mesej amaran bahawa tiada senarai harga projek dan anggaran anda, kerja projek aktual dan perbelanjaan tidak akan diberikan harga. Nilai jualan tidak akan diberikan.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Kaitkan atau tidak kaitkan senarai harga projek pada kontrak projek

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-and-expenses"></a>Cipta atau kaitkan senarai harga khusus untuk menganggarkan kerja dan perbelanjaan berdasarkan projek

1. Pada kontrak projek, pilih tab **Senarai Harga Projek**.
2. Dalam subgrid, pilih **+ Tambah Senarai Harga Projek Baharu**.
3. Pada gelangsar **Cipta Pantas**, pilih senarai harga. 

  Senarai juntai bawah menunjukkan semua senarai harga yang mempunyai konteks ditetapkan kepada **Jualan**, di mana mata wang pada senarai harga sepadan dengan mata wang pada kontrak.
  
4. Masukkan perihalan untuk perkaitan senarai harga projek, pilih **Simpan** dan kemudian tutup gelangsar **Cipta Pantas**.

   Perkaitan senarai harga projek dicipta.
   
5. Ulangi langkah 1-4 untuk mengaitkan lebih daripada satu senarai harga projek ke kontrak projek. Hanya membuat beberapa senarai harga projek jika anda mempunyai tarikh berkuatkuasa yang berbeza pada setiap senarai harga projek yang berkaitan.

> [!NOTE]
> Project Operations tidak menyokong pertindihan tarikh berkuatkuasa senarai harga projek. Jika terdapat beberapa senarai harga projek untuk transaksi dengan tarikh yang diberikan, harga pada transaksi tersebut akan ditetapkan secara lalai kepada sifar.

### <a name="remove-a-project-price-list-association"></a>Alih keluar perkaitan senarai harga projek

- Pilih senarai harga projek dan kemudian pilih **Padamkan Senarai Harga Projek Kontrak** pada subgrid. 

  Senarai harga dialih keluar daripada senarai harga projek dalam kontrak. Senarai harga itu sendiri tidak akan dipadamkan. Hanya perkaitan pada kontrak akan dipadam.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>Sediakan salinan automatik secara lalai senarai harga projek pada kontrak

Senarai harga projek boleh ditetapkan sebagai senarai lalai pada kontrak projek. Persediaan ini boleh membantu memastikan bahawa semua kontrak dalam organisasi anda sentiasa bermula dengan senarai harga standard untuk tempoh harga tersebut.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>Sediakan organisasi lalai untuk senarai harga projek

1. Pergi ke **Tetapan** > **Umum** dan kemudian pilih **Parameter**.
2. Dalam halaman **Senarai parameter aktif**, pilih dan klik dua kali pada rekod untuk membukanya. Semasa klikan dua kali, pastikan anda tidak klik pada nilai medan yang merupaan pautan hiper. 
3. Pada halaman **Parameter Aktif**, pilih tab **Senarai Harga**. Subgrid menunjukkan senarai senarai harga lalai. Ini ialah kos standard dan senarai harga jualan. Mempunyai senarai harga **Jualan** yang berkaitan di sini untuk setiap mata wang yang anda jual dalam memastikan senarai harga jualan adalah lalai pada sebarang kontrak yang anda cipta untuk pelanggan yang berurus niaga dalam mata wang ini.

### <a name="set-up-a-customer-specific-project-price-list"></a>Sediakan senarai harga projek khusus pelanggan

Anda juga boleh menyediakan senarai harga projek tertentu apabila anda telah berunding dengan perjanjian penetapan harga induk dengan pelanggan anda.

1. Pergi ke **Jualan** > **Pelanggan**.
2. Daripada senarai akaun aktif, pilih pelanggan yang mempunyai senarai harga khas.
3. Pilih rekod pelanggan untuk membukanya dan kemudian pilih tab **Senarai Harga Projek**. Subgrid menunjukkan senarai harga projek khusus untuk pelanggan ini. 
4. Cipta perkaitan senarai harga baharu di sini untuk mempunyai senarai harga projek khusus untuk pelanggan ini.

## <a name="custom-pricing-on-a-project-contract"></a>Penetapan harga tersuai pada kontrak projek

Selepas anda mempunyai senarai harga projek lalai organisasi dan khusus pelanggan, kontrak projek anda akan dicipta dengan perkaitan senarai harga projek ini secara automatik. Walau bagaimanapun, senarai harga projek pada kontrak projek sentiasa disalin dengan nama tarikh dan kontrak dilampirkan kepada mereka. Pengurus akaun dan projek kemudian boleh mula membuat suntingan kepada harga pada salinan ini. Harga yang diubah ini akan digunakan untuk kontrak projek ini sahaja.


[!INCLUDE[footer-include](../includes/footer-banner.md)]