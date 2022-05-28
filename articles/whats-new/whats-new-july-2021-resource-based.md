---
title: Ciri baharu Julai 2021 - Project Operations untuk senario berdasarkan sumber/tidak distok
description: Topik ini menyediakan maklumat mengenai kemas kini berkualiti yang tersedia dalam keluaran Julai 2021 Project Operations untuk senario berdasarkan sumber/tidak distok.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1c88f3b4747005bee0d68d0e8a4314c01ffdaf34
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600891"
---
# <a name="whats-new-july-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Ciri baharu Julai 2021 - Project Operations untuk senario berdasarkan sumber/tidak distok

*Digunakan Pada: Project Operations untuk senario berdasarkan sumber/tidak distok*

Topik ini digunakan pada komponen dan versi Dynamics 365 Project Operations berikut:

   - Project Operations dalam persekitaran Microsoft Dataverse versi 4.12.0.148 atau 4.12.0.152.
   - Pengurusan projek dan perakaunan dalam persekitaran Dynamics 365 Finance versi 10.0.20.

## <a name="features-included-in-this-release"></a>Ciri yang disertakan dalam keluaran ini

Ciri berikut disertakan dalam keluaran ini:

- Keupayaan pentadbir untuk melihat log PSS dan log Operations Set yang ditetapkan daripada menu tetapan. Log disimpan selama 90 hari.

## <a name="project-operations-dual-write-maps-updates"></a>Kemas kini peta dwi tulis Project Operations

Tiada kemas kini untuk peta dwi tulis Project Operations dalam keluaran ini.

Untuk senarai semasa dan versi peta dwi tulis Project Operations, lihat [Versi peta dwi tulis Project Operations](../environment/resource-dual-write-maps.md).

Sentiasa menjalankan versi terkini peta dalam persekitaran anda dan mendayakan semua peta jadual berkaitan ketika anda mengemas kini versi penyelesaian Project Operations Dataverse dan penyelesaian Finance anda. Ciri dan keupayaan tertentu mungkin tidak berfungsi dengan betul jika versi terkini peta tidak diaktifkan. Anda boleh melihat versi aktif peta pada halaman **dwi tulis** dalam lajur **Versi**. Aktifkan versi baharu peta dengan memilih **Versi peta jadual**, memilih versi terkini dan kemudian menyimpan versi yang dipilih. Jika anda mempunyai peta jadual luar kotak tersuai, mohon semula perubahan. Untuk maklumat lanjut, lihat [Pengurusan kitaran hayat Aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika anda menghadapi isu memulakan peta, ikuti arahan dalam bahagian [Isu lajur jadual yang tidak ditemui pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) dalam Panduan penyelesaian masalah dwi tulis

## <a name="quality-updates"></a>Kemas kini kualiti

### <a name="project-operations-on-dataverse"></a>Project Operations pada Dataverse

| **Bahagian ciri**              | **Nombor rujukan** | **Kemas kini kualiti**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pengebilan dan Penentuan Harga           | 2224046              | Medan **Kelas Transaksi** boleh diedit pada tab **Butiran Baris Sebut Harga** tetapi dikunci jika anda bekerja daripada halaman **Butiran Baris Sebut Harga**.                                                                     |
| Pengebilan dan Penentuan Harga           | 2224400              | Tindakan **Tutup Sebut Harga Sebagai Menang** gagal apabila sebut harga tidak mempunyai pencapaian tarikh.                                                                                                                                    |
| Pengebilan dan Penentuan Harga           | 2234089              | Apabila anda memasukkan perihalan produk secara manual, ia dikosongkan selepas anda memasukkan kuantiti untuk anggaran material.                                                                                                                         |
| Pengebilan dan Penentuan Harga           | 2234100              | Grid **Persediaan Pengebilan Tugas** tidak termasuk lajur **Material** dan nilainya pada tab **Pengebilan Tugas** projek.                                                                                                       |
| Pengebilan dan Penentuan Harga           | 2277409              | ID produk tidak tersedia pada butiran baris kontrak untuk baris jenis bahan.                                                                                                                                        |
| Pengebilan dan Penentuan Harga           | 2281728              | Mencipta baris kontrak tidak semestinya menilai semula aktual yang menyebabkan peningkatan ketara dalam volum data, yang memberi kesan kepada prestasi.                                                                                |
| Pengebilan dan Penentuan Harga           | 2298668              | Baris jurnal yang berkaitan dengan perbelanjaan yang ditarik balik dan dipadamkan tidak dialih keluar.                                                                                                                                     |
| Pengebilan dan Penentuan Harga           | 2300192              | Apabila berbilang pengguna mengedit invois, butiran baris invois baharu boleh dicipta pada invois yang disahkan.                                                                                   |
| Pengebilan dan Penentuan Harga           | 2301569              | Invois tidak boleh dibetulkan jika penahan amaun \$0 telah dikenakan.                                                                                                                                        |
| Pengebilan dan Penentuan Harga           | 2307965              | Ralat berlaku jika harga kategori dicipta dengan nilai yang tidak ditemui.                                                                                                                           |
| Pengebilan dan Penentuan Harga           | 2326870              | Ralat berlaku dalam **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** jika **producttypecode** adalah nol.                                                                            |
| Pengebilan dan Penentuan Harga           | 2332732              | Ralat berlaku jika pencapaian baris kontrak dicipta tanpa baris pesanan.                                                                                                                |
| Perancangan dan Penjejakan Projek | 2181094              | API Penjadualan Projek kini menyokong Log PSS dan Log Operation Set yang disimpan selama 90 hari.                                                                                                                  |
| Perancangan dan Penjejakan Projek | 2254201              | Label **Mod Jadual** dikemas kini dengan butiran yang menghuraikan penetapan logik lalai.                                                                                                                                      |
| Perancangan dan Penjejakan Projek | 2300252              | Cache respons **openProject** dikemas kini dan memasukkan pemilik token dalam kunci cache, **Url asas** dan **Url Segmen** supaya **Url Permintaan** boleh sentiasa dikira semula jika **Url asas** berubah. |
| Perancangan dan Penjejakan Projek | 2301312              | **msdyn_membershipstatus** telah dialih keluar daripada pandangan **Ahli Pasukan Projek**.                                                                                                                                        |
| Perancangan dan Penjejakan Projek | 2302759              | Produk tidak semestinya diambil pada tab **Tugasan Sumber**, **Anggaran** dan **Anggaran Perbelanjaan**.                                                                                                        |
| Perancangan dan Penjejakan Projek | 2308050              | **CopyProject** gagal dengan ralat, “Gagal mendapatkan token untuk berbual dengan perkhidmatan jauh”.                                                                                                                           |
| Perancangan dan Penjejakan Projek | 2322650              | Pandangan **Senarai Tugas Projek** telah dikemas kini untuk memaparkan tarikh tugas secara lalai.                                                                                                            |
| Perancangan dan Penjejakan Projek | 2327266              | **CopyProject** menjana ralat, "Kunci tidak ditemui dalam kamus" ketika menyalin anggaran.                                                                                                      |
| Perancangan dan Penjejakan Projek | 2328123              | **CopyProject** menjana ralat, "Gagal mendapatkan token untuk berbual dengan perkhidmatan jauh".                                                                                                                          |
| Perancangan dan Penjejakan Projek | 2336258              | **CopyProject** menyalin secara tidak betul nama kedudukan sumber.                                                                                                                                                 |
| Pengebilan dan Penentuan Harga           | 2224476              | Medan **Sumber Boleh Ditempah** tidak ditetapkan kepada pengguna dilog masuk secara lalai pada halaman **Penggunaan Bahan**.                                                                                                            |
| Pengurusan Sumber           | 2277249              | Ralat berlaku apabila keperluan sumber bukan berdasarkan projek dikemas kini.                                                                                                            |
| Pengurusan Sumber           | 2323869              | Penggunaan sumber tidak mengenal pasti sumber yang ditapis dengan betul.                                                                                                                                             |
| Masa dan Perbelanjaan              | 2176538              | Operator penapis yang tidak betul dikenakan kepada kawalan **Entri Masa**.                                                                                                                                                   |
| Masa dan Perbelanjaan              | 2177462              | Pemadaman entri masa dalam grid tidak mengemas kini status butang **Serah**, **Tarik Balik**, **Padam** dan **Entri Edit** seperti dijangka.                                                                                        |
| Masa dan Perbelanjaan              | 2299985              | **TimeEntriesImportFromResourceAssignment** tidak mengekalkan masa mula/tamat daripada kontur tugasan.                                                                                                  |
| Masa dan Perbelanjaan              | 2318426              | Selepas entri masa diserahkan, medan dikunci masih boleh diedit.                                                                                                                                   |
| Masa dan Perbelanjaan              | 2323749              | Ralat berlaku apabila perbelanjaan dicipta daripada tab **Berkaitan** bagi sumber boleh ditempah.                                                                                                      |
| Masa dan Perbelanjaan              | 2327678              | Apabila anda mencipta entri masa daripada tab **Berkaitan** bagi sumber boleh ditempah tidak dihantar ke kawalan entri masa.                                                                            |
| Umum                       | 2296857              | Penjejakan kemajuan untuk kerja yang memakan masa lama.                                                                                                                                                                        |
| Umum                       | 2253682              | Penyelesaian dwi tulis Project Operations tidak boleh dipasang apabila teras dwi tulis dipasang dalam persekitaran tanpa penyelesaian pengorkestraan dwi tulis.                                                |
| Umum                       | 2316420              | Peruntukan teras Project Service gagal jika unit perniagaan pengguna aplikasi berubah.                                                                                                                     |
| Umum                       | 2376405              | Masalah kemas kini berpandukan penerbit tetap (Kemas kini kualiti tersedia dalam versi 4.12.0.152)                                                                                                                     |
### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Pengurusan projek dan perakaunan pada Dynamics 365 Finance

| Bahagian ciri                      | Nombor rujukan | Kemas kini kualiti                                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pengurusan projek dan perakaunan | 4620267          | Tidak boleh memperibadikan borang untuk menambahkan medan **Tujuan** pada halaman **Transaksi disiarkan projek**, **Penciptaan cadangan invois** dan **Cadangan invois**.                                                                                                                                                                                         |
| Pengurusan projek dan perakaunan | 4613449          | Apabila anda memilih ID kontrak Project dalam Finance, persekitaran bersepadu Project Operations membuka halaman untuk mencipta rekod baharu, dan bukannya halaman untuk kontrak projek yang sudah dicipta.                                                                                                                                           |
| Pengurusan projek dan perakaunan | 4614445          | Dalam pelaksanaan disepadukan Project Operations, anda tidak boleh mengedit medan **Kumpulan cukai jualan item** pada cadangan invois yang diimport daripada pemeringkatan. Kumpulan cukai jualan item harus boleh diedit untuk cadangan invois terbuka bagi semua jenis transaksi termasuk akaun, jam, perbelanjaan, yuran dan item. |
| Pengurusan projek dan perakaunan |                  | Tidak boleh menyiarkan cadangan invois yang terhasil daripada pembetulan transaksi masa negatif.                                                                                                                                                                                                                                              |
| Pengurusan projek dan perakaunan |                  | Baris cadangan invois diduplikasi disebabkan berbilang proses berkala **Import daripada pemeringkatan** yang berjalan pada masa yang sama.                                                                                                                                                                                                                |

