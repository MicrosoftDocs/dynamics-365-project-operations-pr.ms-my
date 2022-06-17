---
title: Perkara baharu Februari 2022 - Project Operations untuk senario berasaskan sumber/bukan stok
description: Artikel ini memberikan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran Februari 2022 Operasi Projek untuk senario berasaskan sumber/tidak berstok.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932997"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Perkara baharu Februari 2022 - Project Operations untuk senario berasaskan sumber/bukan stok

*Digunakan Pada: Project Operations untuk senario berdasarkan sumber/tidak distok*

Artikel ini terpakai kepada komponen dan versi Microsoft Dynamics 365 Project Operations berikut :

- Operasi Projek dalam versi persekitaran 4.28.0.120 Dataverse
- Pengurusan projek dan perakaunan dalam persekitaran Dynamics 365 Finance versi 10.0.24

## <a name="features-included-in-this-release"></a>Ciri yang disertakan dalam keluaran ini

- Setakat keluaran ini, anda boleh menambah sehingga 300 ahli pasukan kepada satu projek. Sebelum ini, had bilangan ahli pasukan adalah 150. Untuk maklumat lanjut, lihat [Had projek](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Kemas kini peta dwi-tulis Project Operations

Senarai berikut menunjukkan peta dwi-tulis yang telah diubah suai atau ditambah dalam keluaran Operasi Projek Februari 2022.

| Peta entiti | Versi dikemas kini | Komen |
| --- | --- | --- |
| Entiti eksport perbelanjaan projek integrasi Project Operations (perbelanjaan msdyn\_) | 1.0.0.3 | Dilanjutkan untuk penyegerakan aktiviti projek kepada Dataverse. |

Untuk senarai semasa dan versi peta dwi-tulis Project Operations, lihat [Versi peta dwi-tulis Project Operations](../environment/resource-dual-write-maps.md).

Sentiasa jalankan versi terkini peta dalam persekitaran anda dan dayakan semua peta jadual yang berkaitan semasa anda mengemas kini penyelesaian Operasi Dataverse Projek dan versi penyelesaian Kewangan anda. Sesetengah ciri dan keupayaan mungkin tidak berfungsi dengan betul jika versi terkini peta tidak diaktifkan. Anda boleh melihat versi aktif peta dalam lajur **Versi** pada halaman **Dwi tulis**. Untuk mengaktifkan versi baharu peta dengan, pilih **Versi peta jadual**, pilih versi terkini dan kemudian simpan versi yang dipilih. Jika anda telah menyesuaikan peta jadual di luar kotak, gunakan semula perubahan. Untuk maklumat lanjut, lihat [Pengurusan kitaran hayat Aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika anda menghadapi isu apabila anda memulakan peta, ikut arahan dalam [isu lajur jadual hilang pada bahagian peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) panduan penyelesaian masalah Dual Write.

## <a name="quality-updates"></a>Kemas kini kualiti

### <a name="project-operations-on-dataverse"></a>Project Operations pada Dataverse

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Pengebilan dan harga | 2415109 | Nilai lalai dalam **medan terma** pembayaran Operasi mestilah rekod pelanggan kontrak projek dan rekod invois proforma. |
| Pengebilan dan harga | 2497369 | Pembetulan bahan mesti mengikut nilai tarikh dalam **parameter Pembetulan**. |
| Pengebilan dan harga | 2498697 | Meningkatkan konfigurasi keselamatan untuk ingatan **masukan masa**. |
| Pengebilan dan harga | 2513824 | Untuk senario berasaskan sumber, ID kategori transaksi tidak boleh melebihi 28 aksara dalam Operasi Projek. |
| Pengebilan dan harga | 2517455 | Tindakan **urus niaga** baris invois Segar Semula tidak boleh dibenarkan dicetuskan beberapa kali serentak untuk invois yang sama. |
| Pengebilan dan harga | 2517465 | Tindakan **Nyahaktifkan butiran** baris invois disekat kerana ia tidak disokong. |
| Pengebilan dan harga | 2556660 | Tetapkan semakan kesan tarikh yang dilakukan pada senarai harga yang dilampirkan pada rekod parameter projek. |
| Pengurusan peluang | 2369202 | Membetulkan logik perniagaan yang mengesahkan bahawa senarai harga yang mempunyai tarikh kesan bertindih boleh dilampirkan pada kontrak projek yang sama. |
| Pengurusan peluang | 2385965 | Membetulkan tingkah laku pada **tab** Pelanggan **halaman kontrak** Projek apabila anda memilih **Simpan dan tutup**. |
| Masa dan perbelanjaan | 2538503 | Tugas projek mesti tersedia dalam **entiti sebenar** Projek selepas laporan perbelanjaan disiarkan. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Pengurusan projek dan perakaunan pada Dynamics 365 Finance

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Pengurusan projek dan perakaunan | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Semasa import nota kredit vendor, ralat berlaku. Mesej ralat menyatakan, "Jumlah penahan tidak boleh melebihi jumlah bersih yang tinggal." |
| Pengurusan projek dan perakaunan | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Jika cadangan invois termasuk sebarang transaksi yuran jumlah sifar yang merupakan aktual jualan yang tidak dibilkan, invois tidak boleh berlaku. |
| Pengurusan projek dan perakaunan | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Kos yang disiarkan tidak betul selepas harga pembelian dikemas kini dan **Aktifkan pengurusan** perubahan didayakan.|
| Pengurusan projek dan perakaunan | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Anggaran pengeposan untuk projek harga tetap menggunakan mata wang dan jumlah yang salah dalam baucar anggaran, walaupun **apabila ciri Dayakan mata wang kontrak projek untuk pengiraan** anggaran didayakan. |
| Pengurusan projek dan perakaunan | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **Sambungan\_ ProjDMFDataPopulation** tidak boleh membuat panggilan untuk mendayakan penjejakan perubahan tanpa menangkap pengecualian untuk entiti yang mempunyai kekunci konfigurasi yang tidak didayakan. |
| Pengurusan projek dan perakaunan | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Kerja batch diperbaiki apabila berbilang jurnal lanjutan disiarkan dan ralat berlaku. |
| Perjalanan dan Perbelanjaan | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Kerana isu penyelesaian yang berkaitan dengan pendahuluan tunai atas laporan perbelanjaan, jumlah cukai tidak dilindungi sebagai sebahagian daripada pendahuluan tunai. |
| Perjalanan dan Perbelanjaan | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Maklumat cukai jualan tidak termasuk dalam **laporan Perbelanjaan - Transaksi** yang disiarkan. |
| Perjalanan dan Perbelanjaan | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | Pelanggaran **dasar perbelanjaan Yang Diperlukan** Resit salah menunjukkan amaran mengenai laporan perbelanjaan. |
| Perjalanan dan Perbelanjaan | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Transaksi projek tidak termasuk cukai jualan yang tidak boleh diperolehi semula dalam jumlah jualan apabila transaksi adalah hasil daripada perbelanjaan perbatuan. |
| Perjalanan dan Perbelanjaan | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Apabila baris terperinci mempunyai cukai, anda tidak boleh mengubah tarikh baris item dan ralat keadaan dokumen sumber berlaku. |

## <a name="removed-and-deprecated-features"></a>Ciri yang dialih keluar dan ditamatkan

Ciri [yang dialih keluar atau ditamatkan dalam artikel Operasi](removed-depreciated-features-project.md) Projek menerangkan ciri yang telah dialih keluar atau ditamatkan untuk Dynamics 365 Project Operations.

- Ciri dialih keluar tidak lagi tersedia dalam produk.
- Ciri yang telah lapuk tidak berada dalam pembangunan aktif dan mungkin dialih keluar dalam kemas kini akan datang.

Pengumuman penamatan akan muncul dalam [ciri Dialih keluar atau ditamatkan dalam artikel Operasi](removed-depreciated-features-project.md) Projek 12 bulan sebelum sebarang ciri dialih keluar daripada produk.

Untuk memecahkan perubahan yang hanya menjejaskan masa kompilasi, tetapi binari serasi dengan persekitaran kotak pasir dan pengeluaran, masa penamatan akan kurang daripada 12 bulan. Biasanya, perubahan ini adalah kemas kini berfungsi yang mesti dibuat kepada pengkompil.
