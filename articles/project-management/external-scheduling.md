---
title: Penjadualan luaran
description: Artikel ini memberikan maklumat tentang penjadualan luaran.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736991"
---
# <a name="external-scheduling"></a>Penjadualan luaran

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Mod penjadualan luaran membolehkan anda mencipta, mengemas kini dan memadam entiti yang berkaitan dengan struktur pecahan kerja (WBS) secara asli tetapi tanpa had semasa yang dikuatkuasakan oleh Microsoft Project for the Web. Ia juga menyediakan pensahihan terhad. Mod ini hanya boleh digunakan oleh pelanggan berikut:

- Pelanggan yang mempunyai alat yang diperlukan untuk mentakrifkan WBS di luar logik penjadualan yang disediakan oleh Project Operations
- Pelanggan yang perlu menguruskan jadual hierarki, kebergantungan atau tempoh tugas

> [!IMPORTANT]
> Data yang tidak dimasukkan dengan betul dalam entiti yang berkaitan WBS mungkin tidak akan ditunjukkan dalam grid penyesuaian sumber, grid anggaran, grid penjejakan atau grid penugasan sumber.

## <a name="configuration"></a>Konfigurasi

Ciri ini didayakan secara lalai. Walau bagaimanapun, pada halaman utama luar kotak untuk projek, medan berkaitan tidak boleh dilihat secara lalai. Untuk mendayakan medan, dalam Maker portal, buka halaman utama untuk entiti projek, pilih medan **Enjin Penjadualan** dan kemudian tukar medan kepada **Boleh Dilihat secara Lalai**. Jika anda tidak menggunakan halaman utama projek luar kotak, edit halaman sedia ada anda dan tambah medan **Enjin Penjadualan** kepadanya.

## <a name="settings"></a>Seting

Untuk menggunakan mod penjadualan luaran, anda mesti terlebih dahulu mencipta projek baharu dan memilih enjin penjadualan yang **Dijadualkan Secara Luaran** dalam senarai juntai bawah pada halaman utama projek. Selepas mod ini telah disediakan untuk projek, ia tidak boleh ditukar.

## <a name="viewing-the-wbs"></a>Melihat WBS

Jika projek dijadualkan secara luaran, akses kepada Project for the Web dihadkan untuk projek tersebut. Untuk melihat WBS, anda mesti pergi ke grid penjejakan, tempat WBS penuh ditunjukkan.

## <a name="creating-and-editing-the-wbs"></a>Mencipta dan mengedit WBS

Jika penjadualan luaran didayakan untuk projek, anda mesti mentakrifkan data untuk semua entiti yang berkaitan dengan WBS, termasuk tugas, ahli pasukan, penugasan sumber dan kebergantungan.

Ilustrasi berikut menunjukkan model data untuk perancangan projek.

![Model data perancangan projek.](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>Had fungsian

Operasi berikut tidak dibenarkan pada projek yang dijadualkan secara luaran.

### <a name="project-planning"></a>Perancangan projek

- **Salin projek** – Operasi ini tidak disokong pada projek yang dijadualkan secara luaran.
- **Pindah projek** – Perubahan pada tarikh mula projek tidak akan mengalih permulaan tugas atau penugasan sumber dalam WBS.
- **Mengemas kini Pengurus Projek** – Perubahan kepada pengurus projek pada halaman utama projek tidak akan mencipta ahli pasukan projek baharu secara automatik sehinggalah projek telah ditukar.
- **Mengemas kini templat jam kerja projek** – Perubahan pada templat jam kerja projek tidak akan mengira semula jadual projek.
- **Kontur Penugasan Sumber** – Penciptaan penugasan sumber tidak akan mengemas kini medan **mdyn\_PlannedWork** secara automatik. Medan ini digunakan untuk menyimpan kontur untuk usaha penugasan sumber. Jika anda menunjukkan usaha berfasa masa dalam grid penugasan sumber atau grid penyelarasan sumber, anda mesti mentakrifkan kontur penugasan sumber yang sah. Kontur ini mesti diformat dengan betul supaya ia mencetuskan pengiraan kedua-dua kontur kos dan kontur harga jualan. Kami mengesyorkan anda mencipta projek ujian yang dijadualkan oleh Project for the Web dan kemudian menyemak data yang berkaitan untuk mengesahkan keperluan dan pemformatan.

### <a name="resource-management"></a>Pengurusan sumber

- **Pemenuhan sumber generik** – Pemenuhan sumber generik tidak disokong untuk projek yang dijadualkan secara luaran. Percubaan untuk memenuhi keperluan terbuka aktif akan mewujudkan ahli pasukan projek baharu, tetapi ia tidak akan memadamkan ahli pasukan generik atau menggantikan ahli pasukan generik pada mana-mana penugasan sumber sedia ada.
- **Padam Ahli Pasukan** – Pemadaman ahli pasukan tidak akan memadamkan penugasan sumber secara automatik.

### <a name="quoting-and-contracting"></a>Sebut harga dan kontrak

- **Mengimport butiran Baris Sebut Harga dan Baris Kontrak** – Apabila butiran sebut harga atau baris kontrak diimport daripada projek, aplikasi telah diuji untuk menyokong maksimum hanya 500 tugas dalam WBA, berdasarkan had 20 penugasan bagi setiap tugas.

### <a name="actuals-and-invoicing"></a>Aktual dan penginvoisan

- Walaupun tiada perubahan pada pensahihan sedia ada antara WBS dan transaksi kewangan, anda perlu mematuhi model data luar kotak untuk memastikan semua transaksi hiliran berjalan seperti yang dijangkakan.
