---
title: Perkara baharu Mei 2021 - Project Operations untuk senario berdasarkan sumber/bukan stok
description: Artikel ini memberikan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran Mei 2021 Operasi Projek untuk senario berasaskan sumber/bukan stok.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 425b0eb78b5f03d4b0da9a792d6e33fc96adf060
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930421"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Perkara baharu Mei 2021 - Project Operations untuk senario berdasarkan sumber/bukan stok

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Artikel ini terpakai kepada komponen dan versi berikut Dynamics 365 Project Operations:

- Project Operations pada Dynamics 365 Dataverse persekitaran versi 4.10.0.186
- Pengurusan projek dan perakaunan dalam persekitaran aplikasi Kewangan dan Operasi versi 10.0.18

## <a name="features-included-in-this-release"></a>Ciri yang disertakan dalam keluaran ini

Ciri berikut disertakan dalam keluaran ini:

- [Mod penjadualan](../project-management/scheduling-modes.md): Pengurus projek boleh mentakrifkan sama ada projek perlu diuruskan menggunakan tempoh tetap, kerja tetap atau mod penjadualan unit tetap.
- [Sediakan perbatuan menggunakan peringkat tahap perbatuan](../expense/set-up-mileage.md): Kemas kini peringkat perbatuan untuk laporan perbelanjaan pekerja.

## <a name="project-operations-dual-write-maps-updates"></a>Kemas kini peta dwi tulis Project Operations

Senarai berikut menunjukkan peta dwi tulis yang telah diubah suai atau ditambah dalam Project Operations keluaran Mei 2021.

| Peta entiti | Versi dikemas kini | Komen |
| --- | --- | --- |
| Sumber pembiayaan projek (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Menyegerakkan terma pembayaran pelanggan kontrak projek. |
| Cadangan invois projek V2 (invois) | 1.0.0.3 | Menyegerakkan terma pembayaran invois proforma. |
| Entiti eksport baris invois vendor projek integrasi Project Operations (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | Kemas kini kualiti |
| Projeck V2 (msdyn\_projects) | 1.0.0.2 | Kemas kini kualiti |

Sentiasa jalankan versi terkini peta dalam persekitaran anda dan dayakan semua peta jadual yang berkaitan semasa anda mengemas kini penyelesaian Operasi Dataverse Projek anda dan versi penyelesaian aplikasi Kewangan dan Operasi. Ciri dan keupayaan tertentu mungkin tidak berfungsi dengan betul jika versi terkini peta tidak diaktifkan. Anda boleh melihat versi aktif peta dalam lajur  **Versi**  pada halaman  **Dwi tulis**. Untuk mengaktifkan versi baharu peta dengan, pilih **Versi peta jadual**, pilih versi terkini dan kemudian simpan versi yang dipilih. Jika anda mempunyai peta jadual luar kotak tersuai, mohon semula perubahan. Untuk maklumat lanjut, lihat [Pengurusan kitaran hayat Aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika anda mengalami isu dengan memulakan peta, ikuti arahan dalam bahagian [Isu lajur jadual yang hilang pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) bagi garis panduan penyelesaian masalah Dwi-Tulis.

## <a name="quality-updates"></a>Kemas kini kualiti

### <a name="project-operations-on-dataverse"></a>Project Operations pada Dataverse

| **Bahagian ciri** | **Nombor rujukan** | **Kemas kini kualiti** |
| --- | --- | --- |
| Pengebilan dan Penentuan Harga | 2227635 | Nilai dalam medan **Kumpulan unit** dan **Unit** lalai daripada produk dalam grid **Anggaran Bahan**. |
| Pengebilan dan Penentuan Harga | 2234127 | Medan **ID Tugas** kini dengan mengintegrasikan kepada aktual projek Dataverse dengan betul apabila invois vendor disiarkan. |
| Pengebilan dan Penentuan Harga | 2235564 | Menyimpan garisan jurnal memastikan mata wang yang dipaparkan dalam masukan garisan jurnal padan dengan mata wang lalai ke baris selepas menyimpan. |
| Pengebilan dan Penentuan Harga | 2246671 | Membuat transaksi tidak boleh dikenakan caj semasa pengivoisan membalikkan rekod jualan yang belum dibilkan asal dan mencipta rekod jualan yang belum dibilkan yang baharu sebagai tidak boleh dikenakan caj. |
| Pengebilan dan Penentuan Harga | 2264042 | Pembetulan invois yang sah mesti tidak disekat jika terdapat butiran pembetulan invois yang tidak sah dalam persekitaran. |
| Pengebilan dan Penentuan Harga | 2146367 | Pemetaan dwi-tulis pengepala invois diperluaskan untuk memasukkan terma pembayaran. |
| Pengurusan peluang | 2086888 | Jangan tambah peranan dan kategori yang dinyahaktifkan sebelum anda menyalin sebut harga kepada peranan serta kategori sebut harga yang baharu yang disalin. |
| Pengurusan peluang | 2234376 | Medan baca sahaja dikelabukan dalam grid **Anggaran Bahan**. |
| Pengurusan peluang | 2238337 | Sebut harga berdasarkan kenalan boleh disimpan walaupun ia tidak berkaitan dengan senarai harga projek. |
| Pengurusan peluang | 2239810 | Menutup sebut harga sebagai rugi juga menutup projek berkaitan dan membatalkan sebarang tempahan. |
| Perancangan dan Penjejakan Projek | 2099559 | Pengesahan tambahan ditambah untuk kesihatan sistem sebelum grid **Tugas projek** dibuka. |
| Perancangan dan Penjejakan Projek | 2178987 | Baiki ralat sementara yang berlaku apabila memilih **Peringkat Seterusnya** pada halaman **Projek**. |
| Pengurusan Sumber | 2224817 | Fungsi untuk melanjutkan penempahan lalai ke status tempahan yang betul. |
| Entri masa | 2202476 | Halaman **Entri Masa** kini menggunakan kawalan grid bertindak balas dan membaiki isu seperti salah jajaran grid. |
| Entri masa | 2223377 | Kemasukan masa tersembunyi dari bahagian **Berkaitan** pada halaman **Sumber Boleh Ditempah** untuk mengelakkan kekeliruan dengan kebolehgunaan. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Pengurusan projek dan perakaunan di Dynamics 365 Finance

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Pengurusan projek dan perakaunan | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Dalam Project Operations untuk senario berdasarkan Sumber: Anda tidak boleh menukar sebut harga untuk dimenangi kerana ralat integrasi. |
| Pengurusan projek dan perakaunan | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations: Ralat berlaku apabila anda cuba mengaitkan baris kontrak kepada ID Projek kerana semakan untuk pertindihan baris kontrak dan jenis transaksi. |
| Pengurusan projek dan perakaunan | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** menetapkan menetapkan alamat invois sumber pembiayaan daripada pelanggan yang berbeza. |
| Perjalanan dan Perbelanjaan | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Ralat penyiaran yang berkaitan dengan persediaan perbatuan boleh berlaku. |
| Perjalanan dan Perbelanjaan | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | Fungsi **Pisahkan ke peribadi** tidak berfungsi untuk transaksi perbelanjaan mata wang asing. |
| Perjalanan dan Perbelanjaan | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | Nilai juntai bawah kategori perbelanjaan menunjukkan kategori yang salah untuk perwakilan tanpa mengira jika mereka adalah sumber. |
| Perjalanan dan Perbelanjaan | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | Anda tidak boleh menyimpan laporan perbelanjaan antara syarikat disebabkan oleh ralat **Pengesahan Sumber/Kategori**. |
| Perjalanan dan Perbelanjaan | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | Pengiraan kadar perbatuan yang salah dalam penyiaran laporan perbelanjaan mempunyai baris pecahan. |
| Perjalanan dan Perbelanjaan | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | Anda tidak boleh menyiarkan laporan perbelanjaan antara syarikat apabila cukai jualan disertakan dan jenis akaun ofset pada kaedah pembayaran ialah **Pekerja**. |
| Perjalanan dan Perbelanjaan | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Lancarkan semula entiti data **TrvRequisitionLine** dan indeks unik berkaitan. |
| Perjalanan dan Perbelanjaan | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Laporan perbelanjaan menyokong baris dokumen sumber yang mencipta dan mengemas kini. |
| Perjalanan dan Perbelanjaan | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Jurnal sublejar yang salah ditunjukkan dalam senario antara syarikat jika cukai jualan disiarkan ke entiti sah destinasi. |
| Perjalanan dan Perbelanjaan | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations: Anggaran perbelanjaan tidak dipadamkan daripada Kewangan apabila ia dipadamkan daripada Dataverse. |
| Perjalanan dan Perbelanjaan | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Apabila kategori perbelanjaan adalah kategori bukan projek, dimensi kewangan yang dipilih pada halaman **Perbelanjaan** tidak disalin ke laporan perbelanjaan. |
