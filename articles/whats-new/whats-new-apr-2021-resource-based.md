---
title: Perkara baharu April 2021 - Project Operations untuk senario berdasarkan sumber/bukan stok
description: Topik ini menyediakan maklumat tentang kemas kini kualiti yang tersedia pada bulan April 2021 keluaran Project Operations untuk senario berdasarkan sumber/bukan stok.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 518d795cf7fd2e172a1ce54e2483881d35cea1da
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012687"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Perkara baharu April 2021 - Project Operations untuk senario berdasarkan sumber/bukan stok

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Topik ini digunakan pada komponen dan versi Dynamics 365 Project Operations berikut:

- Project Operations pada persekitaran Dataverse versi 4.9.0.221
- Pengurusan projek dan perakaunan dalam persekitaran Dynamics 365 Finance versi 10.0.17

## <a name="features-included-in-this-release"></a>Ciri yang disertakan dalam keluaran ini

Ciri berikut disertakan dalam keluaran ini:

- Bahan yang tidak dipenuhi untuk projek. Keupayaan utama termasuk:
  - Menganggarkan dan penetapan harga bahan bukan stok semasa kitaran jualan untuk projek. Untuk mendapatkan maklumat lanjut, lihat [Sediakan kadar kos dan jualan untuk produk katalog - ringan](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Menjejaki penggunaan bahan bukan stok semasa penghantaran projek. Untuk mendapatkan maklumat lanjut, lihat [Penggunaan bahan rekod pada projek dan tugas projek](../material/material-usage-log.md).
  - Penginvoisan menggunakan kos bahan bukan stok. Untuk mendapatkan maklumat lanjut, lihat [Urus tunggakan pengebilan](../proforma-invoicing/manage-billing-backlog.md).
  - Untuk maklumat tentang cara mengkonfigurasikan ciri ini, lihat [Konfigurasi bahan bukan stok dan invois vendor yang belum selesai](../procurement/configure-materials-nonstocked.md)
- Pengebilan berdasarkan tugas: Keupayaan ditambahkan untuk mengaitkan tugas projek dengan baris kontrak projek, dengan itu tertakluk pada kaedah pengebilan, frekuensi invois dan pelanggan yang sama seperti yang terdapat pada baris kontrak. Perkaitan ini memastikan invois, perakaunan, anggaran hasil dan pengiktirafan yang tepat untuk berfungsi selaras dengan persediaan ini pada tugas projek.
- Api baharu dalam Dynamics 365 Dataverse membenarkan operasi mencipta, mengemas kini dan memadam dengan **Entiti penjadualan**. Untuk mendapatkan maklumat lanjut, lihat [Gunakan API Jadual untuk melaksanakan operasi dengan Entiti penjadualan](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Kemas kini peta dwi tulis Project Operations

Senarai berikut menunjukkan peta dwi tulis yang telah diubah suai atau ditambah dalam Project Operations keluaran April 2021.

| **Peta entiti** | **Versi dikemas kini** | **Komen** |
| --- | --- | --- |
| Aktual integrasi Project Operations (msdyn\_actuals) | 1.0.0.14 | Peta diubah suai untuk menyegerakkan aktual projek bahan. |
| Entiti integrasi Project Operations untuk anggaran perbelanjaan (msdyn\_estimateslines) | 1.0.0.2 | Baris kontrak projek ditambah ke aplikasi Finance and Operations untuk sokongan pengebilan berdasarkan tugas. |
| Entiti integrasi Project Operations untuk anggaran jam (msdyn\_resourceassignments) | 1.0.0.5 | Baris kontrak projek ditambah ke aplikasi Finance and Operations untuk sokongan pengebilan berdasarkan tugas. |
| Jadual integrasi Project Operations untuk anggaran bahan (msdyn\_estimatelines) | 1.0.0.0 | Peta jadual baharu untuk menyegerakkan anggaran bahan daripada Dataverse ke aplikasi Finance and Operations. |
| Entiti eksport invois projek integrasi Project Operations (msdyn\_projectvendorinvoices) | 1.0.0.0 | Peta jadual baharu untuk menyegerakkan pengepala invois vendor daripada Finance and Operations aplikasi ke Dataverse. |
| Entiti eksport baris invois vendor projek integrasi Project Operations (msdyn\_projectvendorinvoicelines) | 1.0.0.0 | Peta jadual baharu untuk menyegerakkan baris invois vendor daripada Finance and Operations aplikasi ke Dataverse. |

Anda hendaklah sentiasa menjalankan versi terkini peta dalam persekitaran anda dan mendayakan semua peta jadual yang berkaitan apabila anda mengemas kini penyelesaian Project Operations Dataverse dan versi penyelesaian Finance and Operations. Ciri dan keupayaan tertentu mungkin tidak berfungsi dengan betul jika versi terkini peta tidak diaktifkan. Anda boleh melihat versi aktif peta dalam lajur **Versi** pada halaman **Dwi tulis**. Anda boleh mengaktifkan versi baharu peta dengan memilih **Versi peta jadual**, memilih versi terkini dan kemudian menyimpan versi yang dipilih. Jika anda mempunyai peta jadual luar kotak tersuai, mohon semula perubahan. Untuk maklumat lanjut, lihat [Pengurusan kitaran hayat Aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika anda mengalami isu dengan memulakan peta, ikuti arahan dalam bahagian [Isu lajur jadual yang hilang pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) bagi garis panduan penyelesaian masalah Dwi Tulis.

## <a name="quality-updates"></a>Kemas kini kualiti

### <a name="project-operations-in-dynamics-365-dataverse"></a>Project Operations dalam Dynamics 365 Dataverse

| **Bahagian ciri** | **Nombor rujukan** | **Kemas kini kualiti** |
| --- | --- | --- |
| Pengebilan dan harga | 2124532 | Butang **Invois yang betul** dipaparkan pada invois proforma apabila amaun retainer atau amaun retainer yang digunakan wujud pada invois asal. Butang dipaparkan hanya untuk persekitaran dengan Kewangan versi 10.0.19 atau lebih tinggi. |
| Pengebilan dan harga | 2224568 | Logik ditambahkan untuk mendayakan penyesuaian yang melibatkan permohonan pasang masuk pengesahan invois. |
| Pengebilan dan harga | 2101098 | Menambah baik logik medan lalai untuk invois proforma: **Alamat bil kepada**, **Nama Bil kepada** dan **Syarat pembayaran** kini ditetapkan lalai daripada rekod pelanggan kontrak projek yang berkenaan. |
| Pengebilan dan harga | 2021413 | Kemas kini medan **Kos Aktual** dan **Jualan** pada entiti **Tugas** untuk menyertakan nilai jualan daripada perbelanjaan yang belum dibilkan dan dibilkan pada tugas. |
| Pengebilan dan harga | 2182110 | Apabila menyalin kontrak projek, ID baris kontrak dijana semula dalam kontrak projek destinasi untuk memastikan ia unik. |
| Pengurusan Peluang | 2186741 | Pengesahan ditambah untuk memastikan medan **Asal** dan **Jenis Transaksi** tidak boleh dikemas kini pada butiran baris sebut harga yang sedia ada. |
| Pengurusan Peluang | 2191353 | Pencapaian tidak boleh dicipta pada masa dan baris kontrak bahan. |
| Pengurusan Peluang | 2216956 | Betulkan isu dengan **Kemas kini harga**. |
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

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Pengurusan projek dan perakaunan dalam Dynamics 365 Finance

| **Bahagian ciri** | **Nombor rujukan** | **Kemas kini kualiti** |
| --- | --- | --- |
| Pengurusan projek dan perakaunan | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Penyingkiran anggaran pembalikan tidak berfungsi dalam bahagian **Berkala**.  |
| Pengurusan projek dan perakaunan | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | Ciri **Pelarasan perakaunan** mencipta isu dengan akaun lejar yang mempunyai **Tidak membenarkan entri manual** dipilih. |
| Pengurusan projek dan perakaunan | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | Logik perniagaan ditambahkan untuk memproses invois pembetulan termasuk amaun retainer atau amaun retainer yang digunakan. |
| Pengurusan projek dan perakaunan | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | WIP-penyiaran nilai jualan dalam penginvoisan projek antara syarikat memilih akaun yang tidak dijangka. |
| Pengurusan projek dan perakaunan | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Apabila bekerja dengan retainer dalam Project Operations, menukar projek lalai pada kontrak selepas prapembayaran diinvois mengakibatkan isu dengan potongan baharu. |
| Pengurusan projek dan perakaunan | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Dalam Project Operations, mengalih keluar projek daripada kontrak perlu menetapkan semula projek lalai kontrak itu, jika perlu. |
| Pengurusan projek dan perakaunan | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | Dalam Project Operations, baris perbelanjaan yang salah ditunjukkan dalam senarai **Tambahkan baris** pada invois antara syarikat. |
| Pengurusan projek dan perakaunan | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | Dalam Project Operations, halaman **Perjanjian Pembelian** tidak kelihatan dalam entiti sah Kewangan yang berintegrasi dengan Project Operations. |
| Pengurusan projek dan perakaunan | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Disebabkan ralat integrasi Dataverse, anda tidak boleh menukar sebut harga untuk dimenangi dalam Project Operations. |
| Pengurusan projek dan perakaunan | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** boleh menetapkan alamat invois sumber pembiayaan daripada pelanggan yang berbeza.  |
| Pengurusan projek dan perakaunan | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | Dalam Project Operations, tiada dimensi dipilih apabila anda mencipta invois penyiaran untuk transaksi. |
| Perjalanan dan Perbelanjaan | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Baki pendahuluan tunai tidak dikemas kini untuk laporan perbelanjaan jika ia diluluskan dan disiarkan baris demi baris. |
| Perjalanan dan Perbelanjaan | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | Cukai untuk laporan perbelanjaan antara syarikat yang disenaraikan tidak dikira dengan betul. |
| Perjalanan dan Perbelanjaan | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | Medan tambahan yang berkaitan dengan projek dipaparkan pada halaman **Laporan perbelanjaan antara syarikat** yang digambarkan semula. |
| Perjalanan dan Perbelanjaan | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | Mesej ralat yang salah berlaku pada resit pengepala laporan perbelanjaan. |
| Perjalanan dan Perbelanjaan | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | Laporan perbelanjaan tidak disiarkan dengan betul dalam senario antara syarikat jika cukai jualan disiarkan ke entiti sah destinasi. |
| Perjalanan dan Perbelanjaan | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | Tarikh penyerahan laporan tidak dicetak pada laporan perbelanjaan yang diluluskan. |
| Perjalanan dan Perbelanjaan | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | Medan **Tarikh Diluluskan** dan **Tarikh Ditolak** tidak diisi selepas perbelanjaan diluluskan. |
| Perjalanan dan Perbelanjaan | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | Permintaan perjalanan yang dicipta untuk seorang pekerja boleh digunakan untuk laporan perbelanjaan pekerja lain. |
| Perjalanan dan Perbelanjaan | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Kategori perbelanjaan dikunci apabila menambah baris perbelanjaan baharu. |
| Perjalanan dan Perbelanjaan | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Menyenaraikan baris laporan perbelanjaan yang sudah dipisahkan akan mengakibatkan penyiaran baucar Lejar Akaun Belum Bayar\Am yang tidak lengkap dan memecahkan Peneroka Sumber Perakaunan kerana **TRVEXPTRANS.SOURCEDOCUMENTLINE** diduplikasikan. |
| Perjalanan dan Perbelanjaan | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | Dasar permintaan perjalanan tidak berfungsi seperti yang dijangkakan. |
| Perjalanan dan Perbelanjaan | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | Nama akaun vendor tidak ditunjukkan pada transaksi projek yang disiarkan untuk laporan perbelanjaan. |
| Perjalanan dan Perbelanjaan | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | Dalam Project Operations, anda tidak boleh meluluskan masa dengan tugas untuk projek antara syarikat. |
| Perjalanan dan Perbelanjaan | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | Kategori pulangan pendahuluan tunai tidak akan mengemas kini baki pendahuluan tunai apabila disiarkan. |
| Perjalanan dan Perbelanjaan | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | Harga jualan dikira dengan salah pada laporan perbelanjaan yang telah dicipta dalam mata wang asing menggunakan transaksi kad kredit yang diimport dan dikaitkan dengan projek. |
| Perjalanan dan Perbelanjaan | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Melancarkan semula entiti data **TrvRequisitionLine** dan indeks unik yang berkaitan. |
| Perjalanan dan Perbelanjaan | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Instrumentasi ditambahkan untuk generasi **SOURCEDOCUMENTLINE**. |
| Perjalanan dan Perbelanjaan | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Jurnal sublejar yang salah ditunjukkan dalam senario antara syarikat jika cukai jualan disiarkan ke entiti sah destinasi. |
| Perjalanan dan Perbelanjaan | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Dalam Project Operations, anggaran perbelanjaan tidak dipadamkan daripada Kewangan apabila ia dipadamkan daripada Dataverse. |
| Perjalanan dan Perbelanjaan | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Apabila kategori perbelanjaan ialah kategori bukan projek, dimensi kewangan yang dipilih pada halaman **Perbelanjaan** tidak disalin ke laporan perbelanjaan. |
