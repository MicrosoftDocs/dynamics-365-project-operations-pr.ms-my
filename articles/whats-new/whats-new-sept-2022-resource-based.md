---
title: Perkara baharu September 2022 - Project Operations untuk senario berasaskan sumber/bukan stok
description: Artikel ini menyediakan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran September 2022 Microsoft Dynamics 365 Project Operations untuk senario berasaskan sumber/bukan stok.
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

- Operasi Projek dalam versi persekitaran 4.46.0.60 Dataverse
- Pengurusan projek dan perakaunan dalam persekitaran Dynamics 365 Finance versi 10.0.29

## <a name="features-included-in-this-release"></a>Ciri yang disertakan dalam keluaran ini

| Bahagian ciri | Nama ciri | Maklumat lanjut |
| --- | --- | --- |
| Pengurusan Peluang | **Semakan dan Pengaktifan Sebut Harga**<br>Operasi Projek membawa sokongan penuh proses jualan. Petikan projek boleh diaktifkan untuk mewakili keadaan di mana sebut harga dibaca sahaja dan sedang disemak. Sebut harga yang diaktifkan boleh disemak semula untuk membuat sebut harga baru yang mempunyai nombor semakan tambahan. Sebut harga projek yang diaktifkan atau semakan sebut harga boleh ditutup sebagai menang atau hilang. | [Aktifkan dan semak sebut harga projek](/dynamics365/project-operations/sales/activation-and-revision) |
| Pengebilan dan Penentuan Harga | **Lalai harga agnostik zon masa**<br>Operasi Projek telah memperkenalkan konsep tarikh agnostik zon waktu pada semua projek sebenar. Satu bidang baru, Tarikh **transaksi, kini boleh didapati di baris jurnal dan sebenar, dan akan digunakan untuk menyimpan tarikh apabila transaksi berlaku,** tetapi tanpa menukar tarikh itu kepada Masa Universal yang Diselaraskan. Tarikh ini akan digunakan untuk proses hiliran seperti lalai harga dan penciptaan invois. | <p>[Tentukan kadar kos untuk anggaran dan realiti berasaskan projek](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Menentukan harga jualan untuk anggaran dan realiti berasaskan projek](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Pengebilan dan Penentuan Harga | **Penggantian harga tarikh efektif dalam Operasi Projek**<br>Penggantian harga tarikh efektif menyediakan cara untuk mengatasi atau menukar harga tertentu dalam senarai harga. | [Penggantian harga efektif tarikh](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Subkontrak | **Subkontrak dan penyesuaian invois vendor**<br>Ciri ini membolehkan pelanggan membuat subkontrak untuk membeli masa sumber, kategori perbelanjaan dan bahan yang digunakan untuk kerja projek. Ia juga membolehkan pelanggan merakam, dalam aplikasi kewangan dan operasi, invois vendor yang akan tersedia kepada pengurus projek untuk Dataverse pengesahan. | <p>[Pengurusan subkontrak](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Cipta invois vendor](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Masa dan Perbelanjaan | **Pelulus Global**<br>Ciri ini membolehkan vendor perisian bebas (ISV) dan kelulusan berpusat, tanpa mengira status projek atau ahli pasukan dalam projek. | [Keselamatan dan kelulusan](/dynamics365/project-operations/approvals/approvals-security) |
| Pengurusan perbelanjaan | **Keupayaan untuk menyiarkan liabiliti perbelanjaan dalam mata wang vendor**<br>Ciri ini membolehkan laporan perbelanjaan disiarkan dalam mata wang vendor untuk kaedah pembayaran tunai. | [Keupayaan untuk menyiarkan liabiliti perbelanjaan dalam mata wang vendor](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Perolehan Projek | **Bayar apabila pembayaran vendor dibayar**<br>Ciri ini membolehkan ciri Bayar apabila dibayar (PWP) digunakan dengan persekitaran bukan stok Operasi Projek. Ia membolehkan pembayaran vendor disekat/dikekalkan, berdasarkan syarat pengekalan, sehingga pembayaran diterima daripada pelanggan. | [Bayar apabila pembayaran vendor dibayar](/dynamics365/project-operations/procurement/pay-when-paid) |
| Perolehan Projek | **Permintaan pembelian projek**<br>Ciri ini membolehkan pengguna membuat pesanan pembelian berkaitan projek dalam entiti undang-undang di mana Operasi Projek pada penyepaduan Dynamics 365 Customer Engagement didayakan. Pesanan pembelian projek boleh digunakan untuk merekodkan perolehan bahan yang tidak disimpan terhadap projek oleh persona jabatan Perolehan. Pesanan pembelian projek tidak akan disegerakkan ke Dataverse. Walau bagaimanapun, anda boleh menggunakan entiti maya untuk permukaan baris pesanan pembelian Projek untuk Dataverse maklumat pengurus projek. Kos invois vendor berkaitan projek disepadukan dengan entiti Sebenar Projek dalam Dataverse. Kos projek direkodkan dalam subledger Projek dengan menggunakan jurnal Integrasi Operasi Projek. | |
|Perancangan dan Penjejakan Projek|**Gunakan API jadual Projek untuk melaksanakan operasi dengan entiti Penjadualan** </br> </br>Kontur penugasan sumber mengedit API mari pembangun secara programatik menentukan usaha penerima serah tugas merentasi sebarang julat tarikh yang disokong untuk perancangan usaha berperingkat masa yang lebih terperinci.|[Gunakan API jadual Projek untuk melaksanakan operasi dengan entiti Penjadualan](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Kemas kini peta dwi tulis Project Operations

Jadual berikut menunjukkan peta dwi-tulis yang telah diubah suai atau ditambah dalam keluaran Operasi Projek September 2022.

| Peta entiti | Versi dikemas kini | Komen |
| -------------- | ------------------- | ------------|
| Aktual integrasi Project Operations (msdyn_actuals) | 1.0.0.15 | Peta ini menyokong pemprosesan sebenar subkontrak dengan Operasi Projek untuk senario berasaskan sumber. |
| Entiti eksport invois projek integrasi Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Peta ini menyokong pemprosesan sebenar subkontrak dengan Operasi Projek untuk senario berasaskan sumber. |
| Entiti eksport baris invois vendor projek integrasi Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Peta ini menyokong pemprosesan sebenar subkontrak dengan Operasi Projek untuk senario berasaskan sumber. |

Sentiasa jalankan versi terkini peta dalam persekitaran anda dan dayakan semua peta jadual yang berkaitan semasa anda mengemas kini versi penyelesaian Operasi Dataverse Projek dan penyelesaian Kewangan anda. Sesetengah ciri dan keupayaan mungkin tidak berfungsi dengan betul jika versi terkini peta tidak diaktifkan. Anda boleh melihat versi aktif peta dalam lajur **Versi** pada halaman **Dwi tulis**. Untuk mengaktifkan versi baharu peta dengan, pilih **Versi peta jadual**, pilih versi terkini dan kemudian simpan versi yang dipilih. Jika anda telah menyesuaikan peta jadual di luar kotak, gunakan semula perubahan. Untuk maklumat lanjut, lihat [Pengurusan kitaran hayat Aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika anda menghadapi isu semasa anda memulakan peta, ikut arahan dalam [Isu lajur jadual hilang pada bahagian peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) panduan penyelesaian masalah Dwi-tulis.

## <a name="quality-updates"></a>Kemas kini kualiti

### <a name="project-operations-on-dataverse"></a>Project Operations pada Dataverse

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Pengebilan dan Penentuan Harga | 2754422 | Anggaran Bahan dan Perbelanjaan tidak mengalir ke Kewangan apabila projek disalin .Dataverse |
| Masa dan Perbelanjaan | 2787409 | Pelulus yang tidak sah boleh meluluskan kemasukan masa bukan projek. |
| Pengurusan Peluang | 2788907 | Mesej ralat yang dikemas kini pada pengesahan keunikan untuk baris pesanan yang termasuk bendera. |
| Masa dan Perbelanjaan | 2842253 | Pengendalian pengecualian nol untuk kelulusan masa. |
| Pengebilan dan Penentuan Harga | 2844181 | Kegagalan untuk mendapatkan penciptaan invois blok ID korelasi. |
| Pengebilan dan Penentuan Harga | 2876628 | QLD, CLD - Anggaran resolusi senarai harga harus menggunakan medan julat tarikh warisan senarai harga. |
| Subkontrak | 2893222 | Jika tiada peranan ditentukan untuk baris subkontrak, adalah mungkin untuk memilih baris itu pada ahli pasukan untuk sebarang peranan. |

### <a name="project-management-and-accounting-in-finance"></a>Pengurusan projek dan perakaunan dalam Kewangan

Untuk maklumat tentang pembetulan pepijat yang disertakan dalam kemas kini ini, log masuk ke Microsoft Dynamics Perkhidmatan Kitaran Hayat dan lihat [artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559) KB.

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Ciri dihidupkan secara lalai dalam keluaran akan datang

Jadual berikut menyenaraikan ciri yang dihidupkan secara lalai dalam versi 10.0.30. Kebanyakan ciri yang telah dihidupkan secara automatik boleh dimatikan dalam [Pengurusan ciri](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Pada masa hadapan, beberapa ciri yang telah dihidupkan secara automatik mungkin dialih keluar daripada pengurusan Ciri dan menjadi wajib. Perubahan ini memastikan bahawa pelanggan menggunakan fungsi semasa, supaya peningkatan dapat membina fungsi semasa semasa mereka ditambah. Ciri-ciri tidak akan didayakan secara automatik dalam masa kurang dari satu tahun, melainkan ia ditentukan sebagai penting.

| Nama ciri | Dayakan tarikh | Ciri ditambah | Keadaan ciri | Modul |
| --- | --- | --- |--- |--- |
| Mendayakan operasi async apabila pengguna perlu bertukar antara operasi penyegerakan dan async | 21 Oktober 2022 | 9 April 2021 | Dihidupkan secara lalai | Pengurusan perbelanjaan |
| Penilaian dasar perbelanjaan untuk resit yang diperlukan | 21 Oktober 2022 | 20 Disember 2021 | Dihidupkan secara lalai | Pengurusan perbelanjaan |
| Pandangan senarai laporan perbelanjaan yang dicipta oleh wakil pekerja | 21 Oktober 2022 | 19 Februari 2020 | Dihidupkan secara lalai | Pengurusan perbelanjaan |
| Jumlah perbatuan mengikut tahun fiskal | 21 Oktober 2022 | 10 Mei 2022 | Dihidupkan secara lalai | Pengurusan perbelanjaan |
