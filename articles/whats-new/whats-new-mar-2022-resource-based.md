---
title: Perkara baharu Mac 2022 - Project Operations untuk senario berasaskan sumber/bukan stok
description: Artikel ini memberikan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran Mac 2022 bagi Project Operations untuk senario berasaskan sumber/bukan stok.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910917"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Perkara baharu Mac 2022 - Project Operations untuk senario berasaskan sumber/bukan stok

*Digunakan Pada: Project Operations untuk senario berdasarkan sumber/tidak distok*

Artikel ini digunakan pada komponen dan versi Microsoft Dynamics 365 Project Operations berikut:

- Project Operations dalam persekitaran Dataverse versi 4.30.0.99
- Pengurusan projek dan perakaunan dalam persekitaran Dynamics 365 Finance versi 10.0.25

## <a name="features-included-in-this-release"></a>Ciri yang disertakan dalam keluaran ini

Harian kini disokong dalam ruang kerja perbelanjaan moden baharu dan digambarkan semula. Syarikat yang menggunakan harian boleh mendayakan ciri ini untuk memberi pengguna cara mudah untuk menyerahkan dan dibayar balik untuk perbelanjaan harian mereka. Untuk mendapatkan maklumat lanjut, lihat [Perbelanjaan harian](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Kemas kini peta dwi tulis Project Operations

Senarai berikut menunjukkan peta dwi tulis yang telah diubah suai atau ditambahkan dalam Project Operations keluaran Mac 2022.

| **Peta entiti** | **Versi dikemas kini** | **Komen** |
| --- | --- | --- |
| Entiti eksport baris invois vendor projek penyepaduan Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.3 | Pemetaan dikemas kini untuk menjajarkan dengan entiti baris invois vendor dalam Dataverse. <br>Jangan aktifkan pemetaan versi 1.0.0.4. Ciri ini akan tersedia untuk digunakan dalam kombinasi dengan persekitaran Kewangan versi 10.0.26 dalam kemas kini bulanan yang akan datang. |

Sentiasa menjalankan versi terkini peta dalam persekitaran anda, dan mendayakan semua peta jadual berkaitan ketika anda mengemas kini versi penyelesaian Project Operations Dataverse dan penyelesaian Kewangan anda. Sesetengah ciri dan keupayaan mungkin tidak berfungsi dengan betul jika versi terkini peta tidak diaktifkan. Anda boleh melihat versi aktif peta dalam lajur **Versi** pada halaman **Dwi tulis**. Untuk mengaktifkan versi baharu peta dengan, pilih **Versi peta jadual**, pilih versi terkini dan kemudian simpan versi yang dipilih. Jika anda sudah mempunyai peta jadual luar kotak tersuai, mohon semula perubahan. Untuk maklumat lanjut, lihat [Pengurusan kitaran hayat Aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika anda mengalami isu semasa anda memulakan peta, ikut arahan dalam bahagian [Isu lajur jadual yang hilang pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) bagi panduan penyelesaian masalah Dwi tulis.

## <a name="quality-updates"></a>Kemas kini kualiti

### <a name="project-operations-on-dataverse"></a>Project Operations pada Dataverse

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Masa dan perbelanjaan | 2388011 | Tunjuk komen penolakan untuk penyerah entri masa semasa kelulusan pukal. |
| Perancangan dan penjejakan projek | 2495294 | Butiran projek tidak boleh diedit pada halaman **Butiran tugas**. |
| Pengebilan dan harga | 2499605 | Pencapaian kontrak yang dicipta daripada pencapaian sebut harga tidak ditandakan sebagai baca sahaja dengan betul. |
| Perancangan dan penjejakan projek | 2506050 | Set operasi ini akan kekal pada belum selesai selama satu jam jika tiada perubahan untuk disimpan. Set itu kemudian ditandakan secara palsu sebagai **Gagal**, sedangkan set itu sepatutnya dilengkapkan dengan serta-merta. |
| Pengebilan dan harga | 2507401 | Unit kontrak lalai tidak dimasukkan ke dalam projek dengan betul kerana caching yang salah. |
| Pengebilan dan harga | 2541660 | **Pengesahan Penciptaan Pesanan Jualan** dalam dwi tulis sepatutnya untuk pesanan berasaskan projek sahaja. |
| Pengebilan dan harga | 2552745 | Cukai tidak dibahagikan antara pelanggan yang telah menyediakan peraturan pembahagian pengebilan. |
| Pengebilan dan harga | 2558859 | Mesej ralat ditambah baik apabila dimensi penetapan harga disediakan. |
| Pengebilan dan harga | 2558933 | **Import daripada Anggaran Projek** gagal apabila **msdyn\_project** ditambahkan sebagai dimensi harga. |
| Pengebilan dan harga | 2559101 | Pemadaman parameter projek tidak disekat dan menyebabkan isu. |
| Pengurusan peluang | 2570390 | Pasang masuk dwi tulis memaksa jenis akaun pada sebut harga, pesanan dan peluang menjadi **Pelanggan**, walaupun jenis akaun tersebut salah. |
| Pengebilan dan harga | 2586097 | Pembahagian aktual kos yang dibilkan tidak boleh dibalikkan apabila projek dialih keluar daripada baris kontrak projek. |
| Pengebilan dan harga | 2589619 | Cukai pada bahan masukan manual akan disebarkan kepada aktual jualan yang belum dibilkan dan invois. |
| Pengurusan peluang | 2594015 | Sebut harga tidak boleh ditutup sebagai menang untuk pelanggan yang mempunyai terma pembayaran **Net60**. |
| Perancangan dan penjejakan projek | 2595841 | Dalam Project for the Web, pengguna menerima mesej ralat mengenai **msdyn\_actualstart** yang hilang apabila mereka mencipta permintaan sumber baharu. |
| Masa dan Perbelanjaan | 2602511 | Medan **Ditolak oleh** untuk entri masa menunjukkan **Sistem** dan bukannya pengguna bernama sebagai penolak. |
| Masa dan Perbelanjaan | 2602528 | Sebuah pelulus projek boleh meluluskan masa projek pada projek yang mereka tidak disenaraikan sebagai pelulus. |
| Pengebilan dan harga | 2608550 | Invois pembetulan boleh disahkan walaupun jika tiada perubahan pada asal. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Pengurusan projek dan perakaunan pada Dynamics 365 Finance

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Pengurusan projek dan perakaunan | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Terdapat padanan salah antara Kewangan dengan Project Operations dalam panjang medan **ID Kategori** yang dibenarkan. |
| Pengurusan projek dan perakaunan | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Projek harga tetap tidak boleh disingkirkan apabila medan **Pada penginvoisan akaun** ditetapkan kepada **Keuntungan dan Kerugian** dan prinsip **Peratusan selesai** digunakan. |
| Pengurusan projek dan perakaunan | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Kumpulan cukai jualan lalai yang salah dimasukkan daripada persediaan projek pada baris perbelanjaan dalam jurnal penyepaduan Project Operations. |
| Pengurusan projek dan perakaunan | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Anda tidak boleh mengedit dimensi pengepala cadangan invois projek dalam pelaksanaan bersepadu dengan Project Operations. |
| Pengurusan projek dan perakaunan | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Invois vendor antara syarikat tidak boleh disepadukan dengan Dataverse. |
| Pengurusan projek dan perakaunan | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Terdapat padanan salah dengan mata wang baki pelanggan dan mata wang pelaporan. |
| Pengurusan projek dan perakaunan | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Anda boleh menyiarkan invois projek walaupun pelanggan memegang semua invois. |
| Pengurusan projek dan perakaunan | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Butang **Padam semua baris** hilang daripada cadangan invois projek yang mempunyai pandangan **Pengepala** dan **Baris**. |
| Pengurusan projek dan perakaunan | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Apabila anda menyiarkan invois vendor, ralat berikut berlaku: "Tarikh perakaunan untuk invois mesti pada tahun perakaunan yang sama seperti pesanan belian yang berkaitan. Jalankan proses akhir tahun pesanan belian atau ubah tarikh kepada tahun perakaunan semasa." |
| Perjalanan dan Perbelanjaan | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Kos komited untuk projek tidak dikeluarkan selepas kos komited permintaan perjalanan dikeluarkan. |
| Perjalanan dan Perbelanjaan | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Ralat berikut berlaku apabila anda menyerahkan laporan perbelanjaan: "Jejak Timbunan: Syarikat tidak wujud." |
| Perjalanan dan Perbelanjaan | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | **ID Projek** tidak dimasukkan pada laporan perbelanjaan apabila parameter **Memerlukan aktiviti untuk jurnal** dipilih pada projek. |
| Perjalanan dan Perbelanjaan | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Butang **Siarkan Perbelanjaan** tidak berfungsi dengan betul dalam Project Operations untuk senario sumber/bukan stok. |
| Perjalanan dan Perbelanjaan | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Terdapat isu dengan **Kadar setiap batu** untuk laporan perbelanjaan perbatuan yang termasuk penumpang. |
| Perjalanan dan Perbelanjaan | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Kadar perbatuan perbelanjaan untuk pekerja tidak dijumlahkan dengan betul apabila dua jenis kenderaan berbeza digunakan dalam kategori perbelanjaan **Peringkat kadar perbatuan**. |
| Perjalanan dan Perbelanjaan | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Cari medan **Projek** pada baris permintaan perjalanan tidak mengembalikan senarai projek yang betul. |
| Perjalanan dan Perbelanjaan | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Perbatuan sedang disemak** menunjukkan amaran mengenai laporan perbelanjaan. |
| Perjalanan dan Perbelanjaan | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Perkhidmatan pengecaman aksara optik (OCR) tidak berfungsi kerana isu dengan URL Perkhidmatan OCR perbelanjaan. |
| Perjalanan dan Perbelanjaan | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Apabila ciri **Keupayaan untuk memperincikan perbelanjaan berulang dengan cepat** didayakan, jumlah pada baris perincian pada laporan perbelanjaan mengubah jumlah setiap kali halaman **Perincikan** dibuka. |
| Perjalanan dan Perbelanjaan | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Anda tidak boleh memadamkan laporan perbelanjaan apabila senarai interim mempunyai lebih daripada satu pelulus. |

## <a name="removed-and-deprecated-features"></a>Ciri dialih keluar dan ditamatkan

Artikel [Ciri dialih keluar atau ditamatkan dalam Project Operations](removed-depreciated-features-project.md) menghuraikan ciri yang telah dialih keluar atau ditamatkan untuk Dynamics 365 Project Operations.

- Ciri dialih keluar tidak lagi tersedia dalam produk.
- Ciri ditamatkan bukan dalam pembangunan aktif dan mungkin akan dialih keluar dalam kemas kini yang akan datang.

Pengumuman penamatan akan muncul dalam artikel [Ciri dialih keluar atau ditamatkan dalam Project Operations](removed-depreciated-features-project.md) 12 bulan sebelum sebarang ciri dialih keluar daripada produk.

Untuk memecahkan perubahan yang hanya mempengaruhi masa kompilasi, tetapi serasi binari dengan kotak pasir dan persekitaran pengeluaran, masa penamatan akan kurang dari 12 bulan. Biasanya, perubahan ini merupakan kemas kini fungsi yang mesti dibuat pada pengkompil.
