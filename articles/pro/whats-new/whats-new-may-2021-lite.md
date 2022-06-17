---
title: Perkara baharu Mei 2021 - Pelaksanaan ringan Project Operations
description: Artikel ini memberikan maklumat tentang kemas kini kualiti yang tersedia dalam siaran Mei 2021 penggunaan Project Operations lite.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: a5d67159b732e0309e03c64fb6dadcc7b8cbff51
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934193"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>Perkara baharu Mei 2021 - Pelaksanaan ringan Project Operations

_Gunakan Pada: Pelaksanaan lite - urusan dengan invois proforma_

Artikel ini terpakai kepada komponen dan versi berikut Dynamics 365 Project Operations:

   - Project Operations pada persekitaran Dataverse versi 4.10.0.186.

## <a name="features-included-in-this-release"></a>Ciri yang disertakan dalam keluaran ini

Ciri berikut disertakan dalam keluaran ini:

- [Mod penjadualan](../../project-management/scheduling-modes.md): Pengurus projek kini boleh mentakrifkan jika projek harus diuruskan menggunakan tempoh tetap, kerja tetap atau unit penjadualan tetap.

## <a name="quality-updates"></a>Kemas kini kualiti

| **Bahagian ciri** | **Nombor rujukan** | **Kemas kini kualiti** |
| --- | --- | --- |
| Pengebilan dan harga | 2224568 | Logik ditambahkan untuk mendayakan penyesuaian yang melibatkan permohonan pasang masuk pengesahan invois. |
| Pengebilan dan harga | 2101098 | Memperbaiki logik medan lalai untuk invois proforma. Medan ini termasuk, **Alamat bil kepada**, **Nama bil kepada** dan **Terma pembayaran**. Medan kini lalai daripada rekod pelanggan kontrak projek yang berkaitan. |
| Pengebilan dan harga | 2021413 | Kemas kini medan **Kos aktual** dan **Jualan** pada entiti **Tugas** untuk menyertakan nilai jualan daripada perbelanjaan yang belum dibilkan dan dibilkan pada tugas. |
| Pengebilan dan harga | 2182110 | Apabila menyalin kontrak projek, ID baris kontrak dijana semula dalam kontrak projek destinasi untuk memastikan ia unik. |
| Pengurusan Peluang | 2186741 | Pengesahan ditambah untuk memastikan medan **Asal** dan jenis transaksi tidak boleh dikemas kini pada butiran baris sebut harga yang sedia ada. |
| Pengurusan Peluang | 2191353 | Penciptaan pencapaian tidak boleh dibenarkan pada masa dan baris kontrak bahan. |
| Pengurusan Peluang | 2216956 | Betulkan isu dengan **Kemas kini harga**. |
| Perancangan dan Penjejakan | 2182979 | Fungsi salinan projek ditambah baik untuk memastikan bahawa baris anggaran perbelanjaan disalin daripada projek asal. |
| Perancangan dan Penjejakan | 2184144 | Fungsi salinan projek ditambah baik untuk memastikan nama posisi sumber disalin daripada projek asal. |
| Perancangan dan Penjejakan | 2184799 | Kawalan diketatkan apabila menyalin projek untuk memastikan tarikh mula yang dianggarkan tidak boleh ditukar semasa salinan sedang berjalan. |
| Perancangan dan Penjejakan | 2185134 | Semasa salinan projek, tarikh mula yang dianggarkan bagi projek destinasi ditetapkan kepada tarikh hari ini. |
| Perancangan dan Penjejakan | 2196373 | Memastikan pengurus projek dan rekod ahli pasukan tidak diduplikasi dalam pasukan projek semasa menyalin projek. |
| Perancangan dan Penjejakan | 2211833 | Tugasan sumber disalin daripada tugas projek sumber ke projek destinasi. |
| Perancangan dan Penjejakan | 2186541 | Betulkan isu dalam grid **Anggaran** apabila pengumpulan oleh **Sumber**. |
| Perancangan dan Penjejakan | 2166906 | Kategori transaksi daripada tugas mesti disalin ke entiti **Tugasan sumber**. |
| Pengurusan Sumber | 2125362 | Betulkan isu dengan mencipta ahli pasukan generik menggunakan kaedah peruntukan berdasarkan jam. |
| Masa dan Perbelanjaan | 2113603 | Betulkan isu berkaitan penyesuaian dengan mengalih keluar atribut daripada halaman **Entri masa**. Sistem menyemak jika atribut wujud pada halaman sebelum mengakses atribut dengan menggunakan skrip. |
| Masa dan Perbelanjaan | 2204377 | Lembaran masa yang disalin mesti ditunjukkan secara automatik apabila anda memilih **Salin Minggu**. |
| Masa dan Perbelanjaan | 2209059 | Medan **Status** boleh diedit untuk entri masa Dynamics 365 Field Service. |
