---
title: Perkara baharu Oktober 2022 - Project Operations untuk senario berasaskan sumber/bukan stok
description: Artikel ini menyediakan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran Microsoft Dynamics 365 Project Operations pada Oktober 2022 untuk senario berasaskan sumber/bukan stok.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806756"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Perkara baharu Oktober 2022 - Project Operations untuk senario berasaskan sumber/bukan stok

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Artikel ini digunakan pada komponen dan versi Microsoft Dynamics 365 Project Operations berikut:

- Project Operations dalam persekitaran Dataverse versi 4.57.0.176
- Pengurusan projek dan perakaunan dalam persekitaran Dynamics 365 Finance versi 10.0.30

## <a name="features-included-in-this-release"></a>Ciri yang disertakan dalam keluaran ini

| Bahagian ciri | Nama ciri | Maklumat lanjut |
| --- | --- | --- |
| Perancangan dan Penjejakan Projek | **Penjadualan Luaran Operasi Projek**<br>Mod penjadualan luaran membolehkan pelanggan mencipta, mengemas kini dan memadam entiti yang berkaitan dengan struktur pecahan kerja (WBS) secara asli dengan menggunakan API asli Dataverse , tanpa had semasa yang dikuatkuasakan oleh Project for the Web. | [Penjadualan luaran](/dynamics365/project-operations/project-management/external-scheduling) |
| Pelaksanaan dan Konfigurasi | <p>**Benarkan pelanggan memilih jenis penggunaan**<br>Kemas kini dipacu produk (PDU) Operasi Projek digunakan untuk memasang penyelesaian dwi-tulis Operasi Projek secara automatik apabila penyelesaian teras dan orkestra dwi-tulis dipasang di persekitaran.</p><p>Ciri ini memperkenalkan parameter kelakuan **naik taraf Penyelesaian baru** dalam parameter Projek. Apabila parameter ini disetkan kepada **Lite sahaja**, PUD tidak lagi akan memasang penyelesaian dwi-tulis Operasi Projek secara automatik, walaupun penyelesaian teras dan orkestra dwi-tulis dipasang di persekitaran. Tingkah laku ini akan memberi manfaat kepada pelanggan yang merancang untuk menggunakan penyelesaian Dwi-tulis untuk mengintegrasikan pesanan jualan ke dalam aplikasi kewangan dan operasi, tetapi ingin menggunakan Operasi Projek dalam mod Lite (iaitu, tanpa penyepaduan ke dalam aplikasi kewangan dan operasi).</p> | |
| Pengebilan dan Penentuan Harga | <p>**Penukaran mata wang untuk transaksi jualan tanpa bil perbelanjaan dalam persekitaran bersepadu**<br>Bagi pelanggan yang menggunakan Operasi Projek yang disepadukan dengan aplikasi kewangan dan operasi (iaitu, dalam jenis penggunaan sumber/bukan stok), kadar pertukaran biasanya dikuasai dalam aplikasi kewangan dan operasi. Walau bagaimanapun, jika kategori perbelanjaan harus berharga dengan menggunakan kaedah pengiraan harga "pada kos" atau "markup over cost" apabila pelanggan dibilkan, kadar pertukaran yang digunakan untuk mengira jumlah jualan menggunakan kadar pertukaran, bukan kadar Dataverse pertukaran dari aplikasi kewangan dan operasi.</p><p>Ciri ini memperkenalkan parameter kelakuan **penukaran Mata Wang baru** dalam parameter Projek. Apabila parameter ini disetkan kepada **Dilanjutkan dengan pengecilan**, jumlah jualan yang belum dibil pada transaksi perbelanjaan dikira dengan menggunakan kadar pertukaran daripada aplikasi kewangan dan operasi.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Kemas kini peta dwi tulis Project Operations

Tiada kemas kini untuk peta dwi tulis Project Operations dalam keluaran ini. Untuk senarai semasa dan versi peta dwi tulis Project Operations, lihat [Versi peta dwi tulis Project Operations](../environment/resource-dual-write-maps.md).

Sentiasa menjalankan versi terkini peta dalam persekitaran anda, dan mendayakan semua peta jadual berkaitan ketika anda mengemas kini versi penyelesaian Project Operations Dataverse dan penyelesaian Kewangan anda. Sesetengah ciri dan keupayaan mungkin tidak berfungsi dengan betul jika versi terkini peta tidak diaktifkan. Anda boleh melihat versi aktif peta dalam lajur **Versi** pada halaman **Dwi tulis**. Untuk mengaktifkan versi baharu peta dengan, pilih **Versi peta jadual**, pilih versi terkini dan kemudian simpan versi yang dipilih. Jika anda sudah mempunyai peta jadual luar kotak tersuai, mohon semula perubahan. Untuk maklumat lanjut, lihat [Pengurusan kitaran hayat Aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika anda mengalami isu semasa anda memulakan peta, ikut arahan dalam bahagian [Isu lajur jadual yang hilang pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) bagi panduan penyelesaian masalah Dwi tulis.

## <a name="quality-updates"></a>Kemas kini kualiti

### <a name="project-operations-on-dataverse"></a>Project Operations pada Dataverse

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Pengebilan dan Penentuan Harga | 2316317 | Sistem ini membolehkan invois dibuat yang tidak mempunyai transaksi yang boleh dikenakan bayaran. |
| Pengebilan dan Penentuan Harga | 2737300 | Sahkan ketersediaan **medan Pelanggan** sebelum borang diakses. |
| Pengebilan dan Penentuan Harga | 2744948 | Tambah semakan nol untuk kaedah Pengebilan. |
| Pengebilan dan Penentuan Harga | 2763515 | Ralat rujukan nol mengendalikan apabila kontrak jualan invois hilang. |
| Pengebilan dan Penentuan Harga | 2844301 | Penciptaan invois kumpulan gagal kerana ralat. |
| Pengebilan dan Penentuan Harga | 2845869 | Penyimpanan Perkhidmatan Organisasi yang tidak betul. |
| Pengebilan dan Penentuan Harga | 2853729 | Butiran peranan dan harga dikemas kini apabila jenis Pengebilan diubah suai. |
| Pengebilan dan Penentuan Harga | 2940350 | Apabila harga sebenar ditetapkan, hanya senarai harga aktif yang perlu dimasukkan secara automatik. |
| Pelaksanaan dan Konfigurasi | 3001206 | Entiti replaylogheader msdyn\_ menghalang peningkatan Organisasi Pelanggan. |
| Pengurusan Peluang | 2755582 | Pemegang pengecualian rujukan nol dalam Pembantu Peraturan Pengebilan Pisah. |
| Pengurusan Peluang | 2761477 | Apabila pengebilan berpecah digunakan, pemadaman peristiwa penting (header) meninggalkan tonggak anak yatim. |
| Pengurusan Peluang | 2767595 | Apabila rekod penggunaan bahan dibuka dalam bentuk utama, sumber Boleh Ditempah untuk rekod diubah kepada pengguna yang didaftar masuk pada masa ini. |
| Perancangan dan Penjejakan Projek | 2790384 | Masa keluar Pending OperationSet terlalu pendek. |
| Perancangan dan Penjejakan Projek | 2957840 | Tugas tidak boleh disimpan dan lajur tidak boleh ditambahkan pada **halaman Tugas** dalam Operasi Projek Bersepadu. |
| Pengurusan Sumber | 2751560 | Unit Organisasi Pilihan yang Tidak Konsisten dalam Keperluan Sumber. |
| Pemberian subkontrak | 2853245 | Pemadanan untuk Talian Invois Vendor sebenarnya tidak mengemas kini status pengesahan jika talian kontrak telah dipautkan ke baris invois vendor. |
| Pemberian subkontrak | 2907231 | Peringkat proses invois vendor tidak boleh maju. |
| Masa dan Perbelanjaan | 2867363 | Rekod tidak termasuk dalam pandangan Ketidakhadiran/Percutian untuk Kelulusan apabila mereka beratur untuk kelulusan. |
| Masa dan Perbelanjaan | 2894405 | TESA: Direktori POC yang tidak digunakan menyebabkan isu pematuhan. |

### <a name="project-management-and-accounting-in-finance"></a>Pengurusan projek dan perakaunan dalam Kewangan

Untuk maklumat tentang pembetulan pepijat yang termasuk dalam kemas kini ini, daftar masuk ke Microsoft Dynamics Lifecycle Services, dan lihat [artikel KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
