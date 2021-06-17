---
title: Urus senarai harga projek pada sebut harga projek
description: Topik ini menyediakan maklumat tentang bekerja dengan senarai harga projek pada sebut harga.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 926581f877f91e3a351d51cac9c2b1daba035126
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994912"
---
# <a name="manage-project-price-lists-on-project-quotes"></a>Urus senarai harga projek pada sebut harga projek 

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Sebut harga projek direka untuk menyokong berbilang tarikh kuat kuasa senarai harga jualan. Dengan Dynamics 365 Project Operations, entiti baru yang berkaitan yang dipanggil **Senarai harga projek**. Entiti ini mempunyai perhubungan 1 hingga banyak kepada sebut harga projek.

Senarai harga projek digunakan untuk menentukan harga masa, bahan dan perbelanjaan transaksi bagi projek. Apabila sebut harga mempunyai satu atau lebih senarai harga projek, senarai harga ini digunakan untuk menentukan harga masa, bahan, anggaran dan aktual bagi projek yang berkaitan dengan sebut harga melalui baris sebut harga.

Apabila tiada senarai harga projek pada sebut harga projek, anda akan menerima mesej amaran. Mesej menyatakan bahawa kerana tiada senarai harga projek, anggaran dan kiraan sebenar kerja projek dan perbelanjaan anda tidak akan dikira. Sebaliknya, ia akan mempunyai harga sifar (0) untuk nilai jualan.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Kaitkan dan pisahkan senarai harga projek pada sebut harga projek

Untuk mencipta atau memilih senarai harga khusus untuk menganggarkan kerja berasaskan projek dan perbelanjaan, lengkapkan langkah berikut.

1. Pada sebut harga, pilih tab **Harga projek** dan dalam subgrid, pilih **+ Tambah Senarai Harga Projek Baharu**.
2. Pada halaman Cipta Pantas, pilih senarai harga. Senarai juntai bawah menunjukkan semua senarai harga yang mempunyai konteks ditetapkan kepada **Jualan** dan mata wang sepadan dengan mata wang pada sebut harga.
4. Masukkan perihalan untuk perkaitan senarai harga projek dan pilih **Simpan dan Tutup**.

Perkaitan senarai harga projek dicipta.

Anda boleh mengulangi proses ini jika anda perlu untuk mengaitkan lebih daripada satu senarai harga projek kepada sebut harga projek. Hanya mencipta berbilang senarai harga projek jika anda mempunyai tarikh efektif yang berbeza pada setiap senarai harga projek yang berkaitan.

> [!NOTE]
> Project Operations tidak menyokong tarikh kuat kuasa pertindihan senarai harga projek. Jika terdapat berbilang senarai harga projek untuk transaksi dengan tarikh yang diberikan, harga pada transaksi tersebut akan dilalaikan kepada sifar (0).
Untuk mengalih keluar perkaitan senarai harga projek, pilih senarai harga projek dan kemudian pilih **Padam Sebut Harga Senarai Harga Projek**. Senarai harga dialih keluar daripada senarai harga projek bagi sebut harga, tetapi senarai harga itu sendiri tidak dipadam. Hanya perkaitan dengan sebut harga dipadam.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Sediakan senarai harga projek lalai pada sebut harga

Senarai harga projek boleh ditetapkan secara lalai pada sebut harga projek. Persediaan ini memastikan semua sebut harga dalam organisasi anda sentiasa bermula dengan senarai harga standard untuk tempoh harga tersebut.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Sediakan organisasi lalai untuk senarai harga projek

1. Pergi ke **Tetapan** > **Umum** > **Parameter**.
2. Pada halaman senarai **Parameter Aktif**, cari rekod dan klik dua kali untuk membukanya. 
3. Pada halaman **Parameter**, pilih tab **Senarai Harga**. Anda boleh melihat senarai bagi senarai harga lalai ditunjukkan. Ini ialah senarai kos standard dan senarai harga jualan. Mempunyai senarai harga jualan yang berkaitan di sini untuk setiap mata wang yang anda jual, akan memastikan bahawa senarai harga jualan ini telah dilalaikan pada sebarang sebut harga yang anda cipta untuk pelanggan yang melakukan transaksi dalam mata wang ini.

### <a name="set-up-customer-specific-project-price-lists"></a>Sediakan senarai harga projek berkhususkan pelanggan

Senarai harga projek berkhususkan pelanggan juga boleh ditetapkan apabila anda telah berunding perjanjian penetapan harga induk dengan pelanggan anda.

Untuk menetapkan senarai harga projek berkhususkan pelanggan, lengkapkan langkah berikut.

1. Dalam kawasan **Jualan**, pilih **Pelanggan**.
2. Dalam senarai akaun aktif anda, pilih dan buka rekod pelanggan yang anda mempunyai senarai harga istimewa untuknya.
3. Pada tab **Senarai Harga Projek**, anda boleh mencipta mengaitkan senarai harga baharu untuk mempunyai senarai harga projek yang khusus untuk pelanggan ini.

## <a name="create-custom-pricing-on-a-project-quote"></a>Cipta penetapan harga tersuai pada sebut harga projek

Selepas anda mempunyai senarai harga projek lalai organisasi berkhususkan organisasi dan pelanggan, sebut harga projek anda akan dicipta secara automatik dengan perkaitan senarai harga projek ini. Walau bagaimanapun, dalam kes tertentu, anda mungkin perlu mencipta penetapan harga tersuai untuk sebut harga projek tertentu. 

1. Pada **Sebut Harga Projek**, pada tab **Senarai Harga Projek**, sahkan di dalam subgrid bahawa tiada rekod senarai harga tertentu dipilih.
2. Pilih **Cipta Penetapan Harga Tersuai**. Ini akan membuat salinan semua senarai harga standard pada masa ini yang berkaitan dengan sebut harga dan mengaitkan salinan ini kepada sebut harga. Perkaitan sedia ada kepada senarai harga standard akan dialih keluar. Jurujual kemudian boleh mula membuat edit kepada harga pada salinan ini. Harga yang ditukar ini akan digunakan untuk sebut harga projek ini sahaja.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
