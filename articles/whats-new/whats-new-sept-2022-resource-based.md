---
title: Perkara baharu September 2022 - Project Operations untuk senario berasaskan sumber/bukan stok
description: Artikel ini memberikan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran September 2022 bagi Microsoft Dynamics 365 Project Operations untuk senario berasaskan sumber/bukan stok.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634817"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Perkara baharu September 2022 - Project Operations untuk senario berasaskan sumber/bukan stok

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Artikel ini digunakan pada komponen dan versi Microsoft Dynamics 365 Project Operations berikut:

- Project Operations dalam persekitaran Dataverse versi 4.46.0.60
- Pengurusan projek dan perakaunan dalam persekitaran Dynamics 365 Finance versi 10.0.29

## <a name="features-included-in-this-release"></a>Ciri yang disertakan dalam keluaran ini

| Bahagian ciri | Nama ciri | Maklumat lanjut |
| --- | --- | --- |
| Pengurusan Peluang | **Semakan dan Pengaktifan Sebut Harga**<br>Project Operations membawa sokongan penuh proses jualan. Sebut harga projek boleh diaktifkan untuk mewakili keadaan yang sebut harga adalah dalam format baca sahaja dan sedang disemak. Sebut harga aktif boleh disemak semula untuk mencipta sebut harga baharu yang mempunyai nombor semakan ditambah. Sebut harga projek aktif atau semakan sebut harga boleh ditutup sebagai menang atau hilang. | [Aktifkan dan semak sebut harga projek](/dynamics365/project-operations/sales/activation-and-revision) |
| Pengebilan dan Penentuan Harga | **Penetapan nilai lalai harga agnostik zon waktu**<br>Project Operations telah memperkenalkan konsep tarikh agnostik zon waktu pada semua projek aktual. Medan baharu, **Tarikh transaksi**, kini tersedia pada garisan jurnal dan aktual, dan akan digunakan untuk menyimpan tarikh apabila transaksi berlaku, tetapi tanpa menukar tarikh tersebut kepada Waktu Sejagat Selaras. Tarikh ini akan digunakan untuk proses hiliran seperti penetapan nilai lalai harga dan penciptaan invois. | <p>[Tentukan kadar kos untuk anggaran berdasarkan projek dan aktual](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Tentukan harga jualan untuk anggaran berdasarkan dan aktual](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Pengebilan dan Penentuan Harga | **Harga tarikh kuat kuasa mengganti dalam Project Operations**<br>Membatalkan harga tarikh kuat kuasa memberikan cara untuk menganti atau mengubah harga tertentu dalam senarai harga. | [Penggantian harga tarikh kuat kuasa](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Pemberian subkontrak | **Pemberian subkontrak dan penyelarasan invois vendor**<br>Ciri ini membolehkan pelanggan mencipta subkontrak untuk membeli masa sumber, kategori perbelanjaan dan bahan yang digunakan untuk kerja projek. Ciri ini juga membolehkan pelanggan merakam, dalam aplikasi kewangan dan operasi, invois vendor yang akan tersedia kepada pengurus projek dalam Dataverse untuk pengesahan. | <p>[Pengurusan subkontrak](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Cipta invois vendor](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Masa dan Perbelanjaan | **Pelulus Global**<br>Ciri ini mendayakan vendor perisian bebas (ISV) dan kelulusan berpusat, tanpa mengira status projek atau ahli pasukan dalam projek. | [Keselamatan dan kelulusan](/dynamics365/project-operations/approvals/approvals-security) |
| Pengurusan perbelanjaan | **Keupayaan untuk menyiarkan liabiliti perbelanjaan dalam mata wang vendor**<br>Ciri ini mendayakan laporan perbelanjaan untuk disiarkan dalam mata wang vendor untuk kaedah pembayaran tunai. | [Keupayaan untuk menyiarkan liabiliti perbelanjaan dalam mata wang vendor](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Perolehan Projek | **Bayar apabila pembayaran vendor dibayar**<br>Ciri ini mendayakan ciri Bayar apabila dibayar (PWP) digunakan dengan persekitaran bukan stok Project Operations. Ciri ini mendayakan pembayaran vendor yang akan disekat/dikekalkan, berdasarkan terma pengekalan, sehinggalah pembayaran diterima daripada pelanggan. | [Bayar apabila pembayaran vendor dibayar](/dynamics365/project-operations/procurement/pay-when-paid) |
| Perolehan Projek | **Permintaan pembelian projek**<br>Ciri ini mendayakan pengguna untuk mencipta pesanan belian berkaitan projek dalam entiti sah yang penyepaduan Project Operations pada Dynamics 365 Customer Engagement didayakan. Pesanan belian projek boleh digunakan untuk merekodkan Perolehan bahan bukan stok dengan projek oleh Persona jabatan perolehan. Pesanan belian projek tidak akan disegerakkan dengan Dataverse. Walau bagaimanapun, anda boleh menggunakan entiti maya untuk mewujudkan baris pesanan belian projek dalam Dataverse untuk maklumat pengurus projek. Kos invois vendor berkaitan projek disepadukan dengan entiti Aktual Projek dalam Dataverse. Kos projek direkodkan dalam sublejar Projek menggunakan jurnal Penyepaduan Project Operations. | |
|Perancangan dan Penjejakan Projek|**Gunakan API jadual Projek untuk melaksanakan operasi dengan entiti Penjadualan** </br> </br>API pengeditan kontur tugas sumber membolehkan pembangun menyatakan usaha penerima tugas secara programatik merentasi mana-mana julat tarikh yang disokong untuk lebih banyak butiran fasa masa perancangan usaha.|[Gunakan API jadual Projek untuk melaksanakan operasi dengan entiti Penjadualan](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Kemas kini peta dwi tulis Project Operations

Jadual berikut menunjukkan peta dwi tulis yang telah diubah suai atau ditambahkan dalam keluaran September 2022 Project Operations.

| Peta entiti | Versi dikemas kini | Komen |
| -------------- | ------------------- | ------------|
| Aktual integrasi Project Operations (msdyn_actuals) | 1.0.0.15 | Peta ini menyokong pemprosesan subkontrak dengan Project Operations untuk senario berasaskan sumber. |
| Entiti eksport invois projek integrasi Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Peta ini menyokong pemprosesan subkontrak dengan Project Operations untuk senario berasaskan sumber. |
| Entiti eksport baris invois vendor projek integrasi Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Peta ini menyokong pemprosesan subkontrak dengan Project Operations untuk senario berasaskan sumber. |

Sentiasa menjalankan versi terkini peta dalam persekitaran anda, dan mendayakan semua peta jadual berkaitan ketika anda mengemas kini versi penyelesaian Project Operations Dataverse dan penyelesaian Kewangan anda. Sesetengah ciri dan keupayaan mungkin tidak berfungsi dengan betul jika versi terkini peta tidak diaktifkan. Anda boleh melihat versi aktif peta dalam lajur **Versi** pada halaman **Dwi tulis**. Untuk mengaktifkan versi baharu peta dengan, pilih **Versi peta jadual**, pilih versi terkini dan kemudian simpan versi yang dipilih. Jika anda sudah mempunyai peta jadual luar kotak tersuai, mohon semula perubahan. Untuk maklumat lanjut, lihat [Pengurusan kitaran hayat Aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika anda mengalami isu semasa anda memulakan peta, ikut arahan dalam bahagian [Isu lajur jadual yang hilang pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) bagi panduan penyelesaian masalah Dwi tulis.

## <a name="quality-updates"></a>Kemas kini kualiti

### <a name="project-operations-on-dataverse"></a>Project Operations pada Dataverse

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Pengebilan dan Penentuan Harga | 2754422 | Anggaran Bahan dan Perbelanjaan tidak mengalir ke Kewangan apabila projek disalin dalam Dataverse. |
| Masa dan Perbelanjaan | 2787409 | Pelulus yang tidak sah boleh meluluskan entri masa bukan projek. |
| Pengurusan Peluang | 2788907 | Mesej ralat yang dikemas kini pada pensahihan keunikan untuk baris pesanan yang termasuk bendera. |
| Masa dan Perbelanjaan | 2842253 | Pengecualian pengendalian tidak sah untuk kelulusan masa. |
| Pengebilan dan Penentuan Harga | 2844181 | Kegagalan untuk mendapatkan ID korelasi menyekat penciptaan invois. |
| Pengebilan dan Penentuan Harga | 2876628 | QLD, CLD - Anggaran resolusi senarai harga harus menggunakan medan julat tarikh legasi senarai harga. |
| Pemberian subkontrak | 2893222 | Jika tiada peranan ditetapkan untuk baris subkontrak, jadi baris tersebut boleh dipilih pada ahli pasukan untuk sebarang peranan. |

### <a name="project-management-and-accounting-in-finance"></a>Pengurusan projek dan perakaunan dalam Kewangan

Untuk maklumat tentang pembetulan pepijat yang termasuk dalam kemas kini ini, daftar masuk ke Microsoft Dynamics Lifecycle Services, dan lihat [artikel KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Ciri dihidupkan secara lalai dalam keluaran yang akan datang

Jadual berikut menyenaraikan ciri yang dihidupkan secara lalai dalam versi 10.0.30. Kebanyakan ciri yang dihidupkan secara automatik boleh dimatikan dalam [Pengurusan ciri](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Pada masa hadapan, sesetengah ciri yang dihidupkan secara automatik mungkin akan dialih keluar daripada pengurusan Ciri dan menjadi mandatori. Perubahan ini memastikan bahawa pelanggan menggunakan kefungsian semasa, supaya peningkatan boleh dibina pada kefungsian semasa apabila ditambahkan. Ciri tidak akan didayakan secara automatik dalam masa kurang dari satu tahun, melainkan ciri tersebut dianggap penting.

| Nama ciri | Dayakan tarikh | Ciri ditambahkan | Keadaan ciri | Modul |
| --- | --- | --- |--- |--- |
| Dayakan operasi tak segerak apabila pengguna perlu bertukar antara operasi segerak dan tak segerak | 21 Oktober 2022 | 9 April 2021 | Dihidupkan secara lalai | Pengurusan perbelanjaan |
| Penilaian dasar perbelanjaan untuk penerimaan diperlukan | 21 Oktober 2022 | 20 Disember 2021 | Dihidupkan secara lalai | Pengurusan perbelanjaan |
| Senarai pandangan laporan perbelanjaan yang dicipta oleh delegasi pekerja | 21 Oktober 2022 | 19 Februari 2020 | Dihidupkan secara lalai | Pengurusan perbelanjaan |
| Pengiraan jumlah perbatuan mengikut tahun fiskal | 21 Oktober 2022 | 10 Mei 2022 | Dihidupkan secara lalai | Pengurusan perbelanjaan |
