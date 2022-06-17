---
title: Perkara baharu Mac 2022 - Project Operations untuk senario berasaskan sumber/bukan stok
description: Artikel ini memberikan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran Mac 2022 Operasi Projek untuk senario berasaskan sumber/tidak berstok.
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

Artikel ini terpakai kepada komponen dan versi Microsoft Dynamics 365 Project Operations berikut :

- Operasi Projek dalam versi persekitaran 4.30.0.99 Dataverse
- Pengurusan projek dan perakaunan dalam persekitaran Dynamics 365 Finance versi 10.0.25

## <a name="features-included-in-this-release"></a>Ciri yang disertakan dalam keluaran ini

Setiap diem kini disokong dalam ruang kerja perbelanjaan moden yang baru dan dibayangkan semula. Syarikat yang menggunakan setiap diem boleh membolehkan ciri ini memberi pengguna cara mudah untuk menghantar dan dibayar balik untuk perbelanjaan per diem mereka. Untuk maklumat lanjut, lihat [Setiap perbelanjaan diem](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Kemas kini peta dwi tulis Project Operations

Senarai berikut menunjukkan peta dwi-tulis yang telah diubah suai atau ditambah dalam keluaran Operasi Projek Mac 2022.

| **Peta entiti** | **Versi dikemas kini** | **Komen** |
| --- | --- | --- |
| Project Operations integrasi projek vendor invois talian export entity msdyn\_ projectvendorinvoicelines | 1.0.0.3 | Pemetaan dikemas kini untuk diselaraskan dengan entiti baris invois vendor dalam Dataverse. <br>Jangan aktifkan versi pemetaan 1.0.0.4. Ia akan sedia untuk digunakan dalam kombinasi dengan persekitaran Kewangan versi 10.0.26 dalam kemas kini bulanan seterusnya. |

Sentiasa jalankan versi terkini peta dalam persekitaran anda dan dayakan semua peta jadual yang berkaitan semasa anda mengemas kini penyelesaian Operasi Dataverse Projek dan versi penyelesaian Kewangan anda. Sesetengah ciri dan keupayaan mungkin tidak berfungsi dengan betul jika versi terkini peta tidak diaktifkan. Anda boleh melihat versi aktif peta dalam lajur **Versi** pada halaman **Dwi tulis**. Untuk mengaktifkan versi baharu peta dengan, pilih **Versi peta jadual**, pilih versi terkini dan kemudian simpan versi yang dipilih. Jika anda telah menyesuaikan peta jadual di luar kotak, gunakan semula perubahan. Untuk maklumat lanjut, lihat [Pengurusan kitaran hayat Aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika anda menghadapi isu apabila anda memulakan peta, ikut arahan dalam [isu lajur jadual hilang pada bahagian peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) panduan penyelesaian masalah Dwi-tulis.

## <a name="quality-updates"></a>Kemas kini kualiti

### <a name="project-operations-on-dataverse"></a>Project Operations pada Dataverse

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Masa dan perbelanjaan | 2388011 | Tunjukkan komen penolakan kepada penyerah kemasukan masa semasa kelulusan pukal. |
| Perancangan dan penjejakan projek | 2495294 | Butiran projek tidak boleh diedit pada **halaman Butiran** tugas. |
| Pengebilan dan harga | 2499605 | Tonggak kontrak yang dicipta daripada peristiwa penting sebut harga ditandakan dengan salah sebagai baca sahaja. |
| Perancangan dan penjejakan projek | 2506050 | Set operasi kekal belum selesai selama satu jam jika tiada perubahan untuk disimpan. Set itu kemudiannya ditandakan secara salah sebagai **Gagal**, sedangkan ia perlu dilengkapkan dengan serta-merta. |
| Pengebilan dan harga | 2507401 | Unit kontrak lalai salah dimasukkan pada projek kerana caching yang salah. |
| Pengebilan dan harga | 2541660 | **Pengesahan** Penciptaan Pesanan Jualan dalam dwi-tulis hendaklah untuk pesanan berasaskan projek sahaja. |
| Pengebilan dan harga | 2552745 | Cukai tidak dibahagikan antara pelanggan yang telah menetapkan peraturan pengebilan berpecah. |
| Pengebilan dan harga | 2558859 | Mesej ralat yang lebih baik apabila dimensi harga disediakan. |
| Pengebilan dan harga | 2558933 | **Import dari Anggaran** Projek gagal apabila **projek\_ msdyn** ditambahkan sebagai dimensi harga. |
| Pengebilan dan harga | 2559101 | Penghapusan parameter projek tidak disekat dan menyebabkan isu. |
| Pengurusan peluang | 2570390 | Pemalam dwi-tulis memaksa jenis akaun pada sebut harga, pesanan dan peluang untuk menjadi **Pelanggan**, walaupun jenis akaun itu tidak betul. |
| Pengebilan dan harga | 2586097 | Sebenar kos terbelah yang dibilkan tidak diterbalikkan apabila projek dialih keluar daripada baris kontrak projek. |
| Pengebilan dan harga | 2589619 | Cukai ke atas bahan tulis disebarkan kepada sebenar jualan yang tidak dibilkan dan invois. |
| Pengurusan peluang | 2594015 | Sebut harga tidak boleh ditutup seperti yang dimenangi untuk pelanggan yang mempunyai **terma pembayaran Net60**. |
| Perancangan dan penjejakan projek | 2595841 | Dalam Project for the Web, pengguna menerima mesej ralat tentang permulaan **sebenar msdyn\_ yang hilang** apabila mereka mencipta permintaan sumber baru. |
| Masa dan Perbelanjaan | 2602511 | Medan **Ditolak oleh** untuk entri masa menunjukkan **Sistem** dan bukannya pengguna bernama sebagai penolak. |
| Masa dan Perbelanjaan | 2602528 | Pelulus projek boleh meluluskan masa pada projek di mana ia tidak disenaraikan sebagai pelulus. |
| Pengebilan dan harga | 2608550 | Invois pembetulan boleh disahkan walaupun tiada perubahan pada yang asal. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Pengurusan projek dan perakaunan pada Dynamics 365 Finance

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Pengurusan projek dan perakaunan | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Terdapat ketidakpadanan antara Kewangan dan Operasi Projek dalam panjang medan Kategori ID **yang** dibenarkan. |
| Pengurusan projek dan perakaunan | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Projek harga tetap tidak boleh dihapuskan apabila **medan Penginvoisan** Pada Akaun ditetapkan kepada **Keuntungan dan Kerugian** dan **prinsip Peratusan** selesai digunakan. |
| Pengurusan projek dan perakaunan | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Kumpulan cukai jualan lalai yang salah dimasukkan daripada persediaan projek pada baris perbelanjaan dalam jurnal integrasi Operasi Projek. |
| Pengurusan projek dan perakaunan | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Anda tidak boleh mengedit dimensi pengepala cadangan invois projek dalam penggunaan bersepadu dengan Operasi Projek. |
| Pengurusan projek dan perakaunan | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Invois vendor antara syarikat tidak boleh disepadukan dengan Dataverse. |
| Pengurusan projek dan perakaunan | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Terdapat ketidakpadanan dalam mata wang baki pelanggan dan mata wang pelaporan. |
| Pengurusan projek dan perakaunan | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Anda boleh menyiarkan invois projek walaupun pelanggan ditahan untuk semua invois. |
| Pengurusan projek dan perakaunan | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Butang **Padam semua baris** hilang daripada cadangan invois projek yang mempunyai **pandangan Pengepala** dan **Baris**. |
| Pengurusan projek dan perakaunan | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Apabila anda menyiarkan invois vendor, ralat berikut berlaku: "Tarikh perakaunan untuk invois mestilah dalam tahun perakaunan yang sama dengan pesanan yang dibeli yang berkaitan. Jalankan proses akhir tahun pesanan pembelian atau ubah tarikh kepada tahun perakaunan semasa." |
| Perjalanan dan Perbelanjaan | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Kos yang komited untuk projek tidak dikeluarkan setelah kos komitmen permintaan perjalanan dikeluarkan. |
| Perjalanan dan Perbelanjaan | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Kesalahan berikut berlaku apabila anda menyerahkan laporan perbelanjaan: "Stack Trace: Syarikat tidak wujud." |
| Perjalanan dan Perbelanjaan | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | ID Projek lalai **tidak dimasukkan pada laporan perbelanjaan apabila** parameter Memerlukan aktiviti untuk jurnal **dipilih pada** projek. |
| Perjalanan dan Perbelanjaan | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Butang **Post Expenses** tidak berfungsi dengan betul dalam Operasi Projek untuk senario sumber/bukan stok. |
| Perjalanan dan Perbelanjaan | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Terdapat isu dengan **Kadar per batu** untuk laporan perbelanjaan perbatuan yang merangkumi penumpang. |
| Perjalanan dan Perbelanjaan | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Kadar perbatuan perbelanjaan untuk pekerja tidak dikira dengan betul apabila dua jenis kenderaan yang berbeza digunakan dalam **kategori perbelanjaan peringkat** kadar Mileage. |
| Perjalanan dan Perbelanjaan | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Carian untuk **medan Projek** pada baris permintaan perjalanan tidak mengembalikan senarai projek yang betul. |
| Perjalanan dan Perbelanjaan | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Perbatuan dalam ulasan** menunjukkan amaran mengenai laporan perbelanjaan. |
| Perjalanan dan Perbelanjaan | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Perkhidmatan pengecaman aksara optik resit (OCR) tidak berfungsi kerana masalah dengan URL perkhidmatan OCR perbelanjaan. |
| Perjalanan dan Perbelanjaan | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | **Apabila Ciri Keupayaan untuk memperincikan perbelanjaan berulang dengan cepat** didayakan, amaun pada baris butiran pada laporan perbelanjaan mengubah jumlah setiap kali **halaman Butiran** dibuka. |
| Perjalanan dan Perbelanjaan | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Anda tidak boleh memadamkan laporan perbelanjaan apabila senarai interim mempunyai lebih daripada satu pelulus. |

## <a name="removed-and-deprecated-features"></a>Ciri yang dialih keluar dan ditamatkan

Ciri [yang dialih keluar atau ditamatkan dalam artikel Operasi](removed-depreciated-features-project.md) Projek menerangkan ciri yang telah dialih keluar atau ditamatkan untuk Dynamics 365 Project Operations.

- Ciri dialih keluar tidak lagi tersedia dalam produk.
- Ciri yang telah lapuk tidak berada dalam pembangunan aktif dan mungkin dialih keluar dalam kemas kini akan datang.

Pengumuman penamatan akan muncul dalam [ciri Dialih keluar atau ditamatkan dalam artikel Operasi](removed-depreciated-features-project.md) Projek 12 bulan sebelum sebarang ciri dialih keluar daripada produk.

Untuk memecahkan perubahan yang hanya menjejaskan masa kompilasi, tetapi binari serasi dengan persekitaran kotak pasir dan pengeluaran, masa penamatan akan kurang daripada 12 bulan. Biasanya, perubahan ini adalah kemas kini berfungsi yang mesti dibuat kepada pengkompil.
