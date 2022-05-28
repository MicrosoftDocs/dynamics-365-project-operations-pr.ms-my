---
title: Perkara baharu April 2021 - pelaksanaan ringan Project Operations
description: Topik ini menyediakan maklumat tentang kemas kini kualiti yang tersedia pada bulan April 2021 keluaran pelaksanaan ringan Project Operations.
author: sigitac
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 10d9498636d8c5f72b7544be4ec30f399d5e0311
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598131"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>Perkara baharu April 2021 - pelaksanaan ringan Project Operations

_Gunakan Pada: Pelaksanaan lite - urusan dengan invois proforma_

Topik ini digunakan pada komponen dan versi Dynamics 365 Project Operations berikut:

  - Project Operations pada persekitaran Dataverse versi 4.9.0.221 

## <a name="features-included-in-this-release"></a>Ciri yang disertakan dalam keluaran ini

Ciri berikut disertakan dalam keluaran ini:

- Bahan yang tidak dipenuhi untuk projek. Keupayaan utama termasuk:
  - Menganggarkan dan penetapan harga bahan bukan stok semasa kitaran jualan untuk projek. Untuk mendapatkan maklumat lanjut, lihat [Sediakan kadar kos dan jualan untuk produk katalog - ringan](../pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Menjejaki penggunaan bahan bukan stok semasa penghantaran projek. Untuk mendapatkan maklumat lanjut, lihat [Penggunaan bahan rekod pada projek dan tugas projek](../../material/material-usage-log.md).
  - Penginvoisan menggunakan kos bahan bukan stok. Untuk mendapatkan maklumat lanjut, lihat [Urus tunggakan pengebilan - ringan](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog).
  - Api baharu dalam Dynamics 365 Dataverse membenarkan operasi mencipta, mengemas kini dan memadam dengan **Entiti penjadualan**. Untuk mendapatkan maklumat lanjut, lihat [Gunakan API jadual untuk melaksanakan operasi dengan Entiti penjadualan](../../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Kemas kini kualiti

| **Bahagian ciri** | **Nombor rujukan** | **Kemas kini kualiti** |
| --- | --- | --- |
| Pengebilan dan harga | 2224568 | Logik ditambahkan untuk mendayakan penyesuaian yang melibatkan permohonan pasang masuk pengesahan invois. |
| Pengebilan dan harga | 2101098 | Menambah baik logik medan lalai untuk invois proforma: **Alamat bil kepada**, **Nama Bil kepada** dan **Syarat pembayaran** kini ditetapkan lalai daripada rekod pelanggan kontrak projek yang berkenaan. |
| Pengebilan dan harga | 2021413 | Kemas kini medan **Kos Aktual** dan **Jualan** pada entiti **Tugas** untuk menyertakan nilai jualan daripada perbelanjaan yang belum dibilkan dan dibilkan pada tugas. |
| Pengebilan dan harga | 2182110 | Apabila menyalin kontrak projek, ID baris kontrak dijana semula dalam kontrak projek destinasi untuk memastikan ia unik. |
| Pengurusan Peluang | 2186741 | Pengesahan ditambah untuk memastikan medan **Asal** dan **Jenis Transaksi** tidak boleh dikemas kini pada butiran baris sebut harga yang sedia ada. |
| Pengurusan Peluang | 2191353 | Pencapaian tidak boleh dicipta pada masa dan baris kontrak bahan. |
| Pengurusan Peluang | 2216956 | Betulkan isu dengan **Kemas Kini Harga**. |
| Perancangan dan Penjejakan | 2182979 | Fungsi salinan projek ditambah baik untuk memastikan baris anggaran perbelanjaan disalin daripada projek asal. |
| Perancangan dan Penjejakan | 2184144 | Fungsi salinan projek ditambah baik untuk memastikan nama posisi sumber disalin daripada projek asal. |
| Perancangan dan Penjejakan | 2184799 | Salinan projek: Kawalan diketatkan untuk memastikan tarikh mula yang dianggarkan tidak boleh ditukar semasa penyalinan sedang berjalan. |
| Perancangan dan Penjejakan | 2185134 | Salinan projek: Tarik mula yang dianggarkan bagi projek destinasi ditetapkan kepada tarikh hari ini. |
| Perancangan dan Penjejakan | 2196373 | Salinan projek: Memastikan pengurus projek dan rekod ahli pasukan tidak diduplikasi dalam pasukan projek. |
| Perancangan dan Penjejakan | 2211833 | Salinan projek: Tugasan sumber disalin daripada tugas projek sumber ke projek destinasi. |
| Perancangan dan Penjejakan | 2186541 | Betulkan isu dalam grid **Anggaran** apabila pengumpulan oleh sumber. |
| Perancangan dan Penjejakan | 2166906 | Kategori transaksi daripada tugas mesti disalin ke entiti **Tugasan Sumber**. |
| Pengurusan Sumber | 2125362 | Betulkan isu dengan mencipta ahli pasukan generik menggunakan kaedah peruntukan berdasarkan jam. |
| Masa dan Perbelanjaan | 2113603 | Betulkan isu berkaitan penyesuaian dengan mengalih keluar atribut daripada halaman **Entri Masa**. Sistem kini menyemak jika atribut wujud pada halaman sebelum mengaksesnya dengan menggunakan skrip. |
| Masa dan Perbelanjaan | 2204377 | Lembaran masa yang disalin mesti ditunjukkan secara automatik apabila anda memilih **Salin Minggu** semasa entri masa. |
| Masa dan Perbelanjaan | 2209059 | Medan **status** boleh diedit untuk entri masa Dynamics 365 Field Service. |
