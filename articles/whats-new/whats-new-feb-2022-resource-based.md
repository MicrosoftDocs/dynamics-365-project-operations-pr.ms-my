---
title: Perkara baharu Februari 2022 - Project Operations untuk senario berasaskan sumber/bukan stok
description: Artikel ini memberikan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran Februari 2022 bagi Project Operations untuk senario berasaskan sumber/bukan stok.
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

Artikel ini digunakan pada komponen dan versi Microsoft Dynamics 365 Project Operations berikut:

- Project Operations dalam persekitaran Dataverse versi 4.28.0.120
- Pengurusan projek dan perakaunan dalam persekitaran Dynamics 365 Finance versi 10.0.24

## <a name="features-included-in-this-release"></a>Ciri yang disertakan dalam keluaran ini

- Mulai daripada keluaran ini, anda boleh menambah sehingga 300 ahli pasukan untuk satu projek. Sebelum ini, had bilangan ahli pasukan ialah 150. Untuk maklumat lanjut, lihat [Had projek](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Kemas kini peta dwi tulis Project Operations

Senarai berikut menunjukkan peta dwi tulis yang telah diubah suai atau ditambahkan dalam Project Operations keluaran Februari 2022.

| Peta entiti | Versi dikemas kini | Komen |
| --- | --- | --- |
| Entiti eksport perbelanjaan projek penyepaduan Project Operations (msdyn\_expenses) | 1.0.0.3 | Lanjutan untuk penyegerakan aktiviti projek kepada Dataverse. |

Untuk senarai semasa dan versi peta dwi tulis Project Operations, lihat [Versi peta dwi tulis Project Operations](../environment/resource-dual-write-maps.md).

Sentiasa menjalankan versi terkini peta dalam persekitaran anda, dan mendayakan semua peta jadual berkaitan ketika anda mengemas kini versi penyelesaian Project Operations Dataverse dan penyelesaian Kewangan anda. Sesetengah ciri dan keupayaan mungkin tidak berfungsi dengan betul jika versi terkini peta tidak diaktifkan. Anda boleh melihat versi aktif peta dalam lajur **Versi** pada halaman **Dwi tulis**. Untuk mengaktifkan versi baharu peta dengan, pilih **Versi peta jadual**, pilih versi terkini dan kemudian simpan versi yang dipilih. Jika anda sudah mempunyai peta jadual luar kotak tersuai, mohon semula perubahan. Untuk maklumat lanjut, lihat [Pengurusan kitaran hayat Aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika anda mengalami isu semasa anda memulakan peta, ikut arahan dalam bahagian [Isu lajur jadual yang hilang pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) bagi panduan penyelesaian masalah Dwi Tulis.

## <a name="quality-updates"></a>Kemas kini kualiti

### <a name="project-operations-on-dataverse"></a>Project Operations pada Dataverse

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Pengebilan dan harga | 2415109 | Nilai lalai dalam medan **Terma pembayaran operasi** mestilah rekod pelanggan kontrak projek dan rekod invois proforma. |
| Pengebilan dan harga | 2497369 | Pembetulan bahan mestilah mengikut nilai tarikh dalam parameter **Pembetulan**. |
| Pengebilan dan harga | 2498697 | Peningkatan konfigurasi keselamatan untuk **Ingat semula entri masa**. |
| Pengebilan dan harga | 2513824 | Untuk senario berasaskan sumber, ID kategori urus niaga tidak boleh melebihi 28 aksara dalam Project Operations. |
| Pengebilan dan harga | 2517455 | Tindakan **Segar semula urus niaga baris invois** tidak boleh dibenarkan untuk dicetuskan sebanyak berbilang kali secara serentak untuk invois yang sama. |
| Pengebilan dan harga | 2517465 | Tindakan **Nyahaktifkan butiran baris invois** disekat kerana tidak disokong. |
| Pengebilan dan harga | 2556660 | Memperbaiki semakan kuat kuasa tarikh yang dilakukan pada senarai harga yang dilampirkan pada rekod parameter projek. |
| Pengurusan peluang | 2369202 | Membetulkan logik perniagaan yang mengesahkan bahawa senarai harga yang mempunyai tarikh kuat kuasa bertindan boleh dilampirkan dengan kontrak projek yang sama. |
| Pengurusan peluang | 2385965 | Membetulkan tingkah laku pada tab **Pelanggan** halaman **Kontrak projek** apabila anda memilih **Simpan dan tutup**. |
| Masa dan perbelanjaan | 2538503 | Satu tugas projek mesti tersedia dalam entiti **Aktual projek** selepas laporan perbelanjaan disiarkan. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Pengurusan projek dan perakaunan pada Dynamics 365 Finance

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Pengurusan projek dan perakaunan | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Semasa mengimport nota kredit vendor, ralat berlaku. Mesej ralat menyatakan, "Jumlah pengekalan tidak boleh melebihi baki jumlah bersih." |
| Pengurusan projek dan perakaunan | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Jika cadangan invois termasuk sebarang urus niaga yuran jumlah sifar merupakan aktual jualan tidak dibilkan, penginvoisan tidak boleh berlaku. |
| Pengurusan projek dan perakaunan | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Kos yang disiarkan adalah salah selepas harga belian dikemas kini dan **Aktifkan pengurusan perubahan** didayakan.|
| Pengurusan projek dan perakaunan | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Anggaran penyiaran untuk projek harga tetap menggunakan mata wang yang salah dan jumlah dalam baucar anggaran, walaupun apabila ciri **Dayakan mata wang kontrak projek untuk pengiraan anggaran** telah didayakan. |
| Pengurusan projek dan perakaunan | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_Extension** tidak sepatutnya membuat keputusan untuk mendayakan penjejakan perubahan tanpa menangkap pengecualian untuk entiti yang mempunyai kekunci konfigurasi yang tidak didayakan. |
| Pengurusan projek dan perakaunan | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Kerja pukal ditetapkan apabila berbilang jurnal lanjutan disiarkan dan ralat berlaku. |
| Perjalanan dan Perbelanjaan | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Disebabkan isu penyelesaian yang berkaitan dengan pendahuluan tunai ke atas laporan perbelanjaan, jumlah cukai tidak diliputi sebagai sebahagian daripada pendahuluan tunai. |
| Perjalanan dan Perbelanjaan | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Maklumat cukai jualan tidak termasuk dalam laporan **Perbelanjaan - Urus niaga yang disiarkan**. |
| Perjalanan dan Perbelanjaan | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | Pelanggaran dasar perbelanjaan **Penerimaan Diperlukan** menunjukkan amaran pada laporan perbelanjaan. |
| Perjalanan dan Perbelanjaan | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Urus niaga projek tidak termasuk cukai jualan tidak boleh dipulihkan dalam jumlah amaun jualan apabila urus niaga tersebut merupakan hasil daripada perbelanjaan perbatuan. |
| Perjalanan dan Perbelanjaan | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Apabila baris yang diperincikan mempunyai cukai, anda tidak boleh mengubah tarikh baris perincian dan ralat keadaan dokumen sumber berlaku. |

## <a name="removed-and-deprecated-features"></a>Ciri dialih keluar dan ditamatkan

Artikel [Ciri dialih keluar atau ditamatkan dalam Project Operations](removed-depreciated-features-project.md) menghuraikan ciri yang telah dialih keluar atau ditamatkan untuk Dynamics 365 Project Operations.

- Ciri dialih keluar tidak lagi tersedia dalam produk.
- Ciri ditamatkan bukan dalam pembangunan aktif dan mungkin akan dialih keluar dalam kemas kini yang akan datang.

Pengumuman penamatan akan muncul dalam artikel [Ciri dialih keluar atau ditamatkan dalam Project Operations](removed-depreciated-features-project.md) 12 bulan sebelum sebarang ciri dialih keluar daripada produk.

Untuk memecahkan perubahan yang hanya mempengaruhi masa kompilasi, tetapi serasi binari dengan kotak pasir dan persekitaran pengeluaran, masa penamatan akan kurang dari 12 bulan. Biasanya, perubahan ini merupakan kemas kini fungsi yang mesti dibuat pada pengkompil.
