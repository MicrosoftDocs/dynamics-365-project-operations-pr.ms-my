---
title: Aktual
description: Topik ini memberikan maklumat tentang cara bekerja dengan aktual dalam Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 13c429763fa805fae5324e4dcf1bf7669e842281
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126322"
---
# <a name="actuals"></a>Aktual 

_**Gunakan pada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Aktual ialah jumlah kerja yang telah disiapkan pada sebuah projek. Ia dicipta sebagai hasil daripada entri masa dan perbelanjaan, serta entri jurnal dan invois.

## <a name="journal-lines-and-time-submission"></a>Garisan jurnal dan serahan masa

Untuk mendapatkan maklumat lanjut tentang entri masa, lihat [Gambaran keseluruhan entri masa](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Masa dan bahan

Apabila entri masa yang diserahkan telah dipautkan dengan projek yang dipetakan dengan baris kontrak masa dan bahan, sistem mencipta dua garisan jurnal, satu untuk kos dan satu untuk jualan yang tidak dibilkan.

### <a name="fixed-price"></a>Harga tetap

Apabila entri masa yang telah diserahkan dipautkan kepada projek yang dipetakan kepada baris kontrak harga tetap, sistem mencipta satu garisan jurnal untuk kos.

### <a name="default-pricing"></a>Penetapan harga lalai

Logik untuk mencipta harga lalai terletak pada garisan jurnal. Nilai medan daripada entri masa disalin kepada garisan jurnal. Nilai-nilai ini termasuk tarikh transaksi, baris kontrak yang projek dipetakan padanya, dan mata wang yang menghasilkan senarai harga yang sesuai.

Medan-medan yang mempengaruhi penetapan harga lalai, seperti **Peranan** dan **Unit Organisasi**, digunakan untuk menentukan harga yang sesuai pada garisan jurnal. Anda boleh menambah medan tersuai pada entri masa. Jika anda mahu nilai medan disebarkan kepada aktual, cipta medan pada entiti Aktual dan gunakan pemetaan medan untuk menyalin medan daripada entri masa kepada aktual.

## <a name="journal-lines-and-basic-expense-submission"></a>Serahan garisan jurnal dan perbelanjaan asas

Untuk mendapatkan maklumat lanjut tentang entri perbelanjaan, lihat [Gambaran keseluruhan perbelanjaan](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Masa dan bahan

Apabila entri perbelanjaan asas yang diserahkan telah dipautkan kepada projek yang dipetakan kepada baris kontrak masa dan bahan, sistem mencipta dua garisan jurnal, satu untuk kos dan satu untuk jualan yang tidak dibilkan.

### <a name="fixed-price"></a>Harga tetap

Apabila entri perbelanjaan asas yang telah diserahkan dipautkan kepada projek yang dipetakan kepada baris kontrak harga tetap, sistem mencipta satu garisan jurnal untuk kos.

### <a name="default-pricing"></a>Penetapan harga lalai

Logik untuk memasukkan harga lalai bagi perbelanjaan adalah berdasarkan kategori perbelanjaan. Tarikh transaksi, baris kontrak yang projek dipetakan dan mata wang semuanya digunakan untuk menentukan senarai harga bersesuaian. Walau bagaimanapun, secara lalai, jumlah yang dimasukkan untuk harga itu sendiri ditetapkan secara langsung pada garisan jurnal perbelanjaan bagi kos dan jualan.

Entri berasaskan kategori bagi setiap unit harga lalai pada entri perbelanjaan tidak tersedia.

## <a name="use-entry-journals-to-record-costs"></a>Gunakan jurnal entri untuk merekodkan kos

Anda boleh menggunakan jurnal entri untuk merekodkan kos atau hasil dalam kelas bahan, yuran, masa, perbelanjaan, atau transaksi cukai. Jurnal boleh digunakan untuk tujuan berikut:

- Rekodkan kos aktual bahan dan jualan pada projek.
- Alihkan transaksi aktual daripada sistem lain kepada Microsoft Dynamics 365 Project Operations..
- Rekodkan kos yang berlaku dalam sistem yang lain. Kos ini boleh merangkumi kos perolehan atau subkontrak.

> [!IMPORTANT]
> Aplikasi ini tidak mengesahkan jenis garisan jurnal atau penetapan harga yang berkaitan yang dimasukkan pada garisan jurnal. Oleh itu, hanya pengguna yang menyedari sepenuhnya kesan perakaunan yang aktual ada pada projek itu, harus menggunakan jurnal entri untuk mencipta aktual. Disebabkan oleh kesan jenis Jurnal ini, anda perlu memilih dengan teliti orang yang mempunyai akses untuk mencipta jurnal entri.
## <a name="record-actuals-based-on-project-events"></a>Rekodkan aktual berdasarkan peristiwa projek

Project Operations merekodkan transaksi kewangan yang berlaku semasa projek. Transaksi ini direkodkan sebagai aktual. Jadual berikut menunjukkan jenis aktual berbeza yang dicipta, bergantung pada sama ada projek itu adalah projek masa dan bahan atau projek harga tetap, dalam peringkat prajualan, atau merupakan projek dalaman.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>Sumber tersebut tergolong dalam unit organisasi yang sama seperti unit kontrak projek

<table>
<thead>
<tr>
<th rowspan="3">Peristiwa</th>
<th colspan="4">Projek boleh dibilkan atau dijual</th>
<th rowspan="3">Projek dalam peringkat prajualan</th>
<th rowspan="3">Projek dalaman</th>
</tr>
<tr>
<th colspan="2">Masa dan bahan</th>
<th colspan="2">Harga tetap</th>
</tr>
<tr>
<th>Sebenar</th>
<th>Mata wang transaksi</th>
<th>Harga tetap</th>
<th>Mata wang transaksi</th>
</tr>
</thead>
<tbody>
<tr>
<td>Entri masa dicipta.</td>
<td colspan="6">Tiada aktiviti dalam entiti Aktual</td>
</tr>
<tr>
<td>Entri masa diserahkan.</td>
<td colspan="6">Tiada aktiviti dalam entiti Aktual</td>
</tr>
<tr>
<td rowspan="2">Masa telah diluluskan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku semasa kelulusan.</td>
<td>Kos sebenar</td>
<td>Mata wang unit pengkontrakan</td>
<td rowspan="2">Kos sebenar</td>
<td rowspan="2">Mata wang unit pengkontrakan
<td rowspan="2">Kos sebenar</td>
<td rowspan="2">Kos sebenar</td>
</tr>
<tr>
<td>Jualan belum dibilkan sebenar – Boleh dituntut</td>
<td>Mata wang kontrak projek</td>
</tr>
<tr>
<td rowspan="3">Masa telah diluluskan dan tiada pengurangan dalam masa boleh dibilkan berlaku semasa kelulusan.</td>
<td>Kos sebenar</td>
<td>Mata wang unit pengkontrakan</td>
<td rowspan="3">Kos sebenar</td>
<td rowspan="3">Mata wang unit pengkontrakan</td>
<td rowspan="3">Kos sebenar</td>
<td rowspan="3">Kos sebenar</td>
</tr>
<tr>
<td>Jualan belum dibilkan sebenar – Boleh dituntut untuk kuantiti baharu</td>
<td>Mata wang kontrak projek</td>
</tr>
<tr>
<td>Jualan belum dibilkan sebenar – Tidak boleh dituntut untuk perbezaan</td>
<td>Mata wang kontrak projek</td>
</tr>
<tr>
<td rowspan="2">Invois disahkan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku.</td>
<td>Pengunduran jualan belum dibilkan</td>
<td>Mata wang kontrak projek</td>
<td rowspan="2">Jualan dibilkan untuk pencapaian</td>
<td rowspan="2">Mata wang kontrak projek</td>
<td rowspan="2">Tidak berkenaan</td>
<td rowspan="2">Tidak berkenaan</td>
</tr>
<tr>
<td>Jualan dibilkan</td>
<td>Mata wang kontrak projek</td>
</tr>
<tr>
<td rowspan="3">Invois disahkan dan pengurangan dalam masa boleh dibilkan berlaku.</td>
<td>Pengunduran jualan belum dibilkan</td>
<td>Mata wang kontrak projek</td>
<td rowspan="3">Tidak berkenaan</td>
<td rowspan="3">Tidak berkenaan</td>
<td rowspan="3">Tidak berkenaan</td>
<td rowspan="3">Tidak berkenaan</td>
</tr>
<tr>
<td>Jualan dibilkan – Boleh dituntut untuk kuantiti baharu</td>
<td>Mata wang kontrak projek</td>
</tr>
<tr>
<td>Jualan dibilkan – Tidak boleh dituntut untuk perbezaan</td>
<td>Mata wang kontrak projek</td>
</tr>
<tr>
<td rowspan="2">Invois dibetulkan untuk menambah kuantiti yang boleh dituntut.</td>
<td>Julana dibilkan – Pengunduran</td>
<td>Mata wang kontrak projek</td>
<td rowspan="5">
<ul>
<li>Pengunduran jualan dibilkan untuk pencapaian</li>
<li>Penukarang status pencapaian daripada <strong>Diinvoiskan</strong> kepada <strong>Sedia untuk invois</strong></li>
</ul>
</td>
<td rowspan="5">Mata wang kontrak projek</td>
<td rowspan="5">Tidak berkenaan</td>
<td rowspan="5">Tidak berkenaan</td>
</tr>
<tr>
<td>Jualan dibilkan</td>
<td>Mata wang kontrak projek</td>
</tr>
<tr>
<td rowspan="3">Invois dibetulkan untuk mengurangkan kuantiti yang boleh dituntut.</td>
<td>Julana dibilkan – Pengunduran</td>
<td>Mata wang kontrak projek</td>
</tr>
<tr>
<td>Jualan dibilkan untuk kuantiti baharu</td>
<td>Mata wang kontrak projek</td>
</tr>
<tr>
<td>Jualan tidak dibilkan – Boleh dituntut untuk perbezaan</td>
<td>Mata wang kontrak projek</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>Sumber tersebut tergolong dalam unit organisasi yang berbeza daripada unit kontrak projek

<table>
<thead>
<tr>
<th rowspan="3">Peristiwa</th>
<th colspan="4">Projek boleh dibilkan atau dijual</th>
<th rowspan="3">Projek dalam peringkat prajualan</th>
<th rowspan="3">Projek dalaman</th>
</tr>
<tr>
<th colspan="2">Masa dan bahan</th>
<th colspan="2">Harga tetap</th>
</tr>
<tr>
<th>Sebenar</th>
<th>Mata wang transaksi</th>
<th>Harga tetap</th>
<th>Mata wang transaksi</th>
</tr>
</thead>
<tbody>
<tr>
<td>Entri masa dicipta.</td>
<td colspan="6">Tiada aktiviti dalam entiti Aktual</td>
</tr>
<tr>
<td>Entri masa diserahkan.</td>
<td colspan="6">Tiada aktiviti dalam entiti Aktual</td>
</tr>
<tr>
<td rowspan="4">Masa telah diluluskan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku semasa kelulusan.</td>
<td>Kos sebenar</td>
<td>Mata wang unit pengkontrakan</td>
<td rowspan="4">Kos sebenar</td>
<td rowspan="4">Mata wang unit pengkontrakan</td>
<td rowspan="4">Kos sebenar</td>
<td rowspan="4">Kos sebenar</td>
</tr>
<tr>
<td>Jualan belum dibilkan sebenar – Boleh dituntut</td>
<td>Mata wang kontrak projek</td>
</tr>
<tr>
<td>Kos unit persumberan</td>
<td>Mata wang unit persumberan</td>
</tr>
<tr>
<td>Jualan antara organisasi</td>
<td>Mata wang unit pengkontrakan</td>
</tr>
<tr>
<td rowspan="5">Masa telah diluluskan dan tiada pengurangan dalam masa boleh dibilkan berlaku semasa kelulusan.</td>
<td>Kos sebenar</td>
<td>Mata wang unit pengkontrakan</td>
<td rowspan="5">Kos sebenar</td>
<td rowspan="5">Mata wang unit pengkontrakan</td>
<td rowspan="5">Kos sebenar</td>
<td rowspan="5">Kos sebenar</td>
</tr>
<tr>
<td>Kos unit persumberan</td>
<td>Mata wang unit persumberan</td>
</tr>
<tr>
<td>Jualan antara organisasi</td>
<td>Mata wang unit pengkontrakan</td>
</tr>
<tr>
<td>Jualan belum dibilkan sebenar – Boleh dituntut untuk kuantiti baharu</td>
<td>Mata wang kontrak projek</td>
</tr>
<tr>
<td>Jualan belum dibilkan sebenar – Tidak boleh dituntut untuk perbezaan</td>
<td>Mata wang kontrak projek</td>
</tr>
<tr>
<td rowspan="2">Invois disahkan dan tiada perubahan kepada atau peningkatan dalam masa boleh dibilkan berlaku.</td>
<td>Pengunduran jualan belum dibilkan</td>
<td>Mata wang kontrak projek</td>
<td rowspan="2">Jualan dibilkan untuk pencapaian</td>
<td rowspan="2">Mata wang kontrak projek</td>
<td rowspan="2">Tidak berkenaan</td>
<td rowspan="2">Tidak berkenaan</td>
</tr>
<tr>
<td>Jualan dibilkan</td>
<td>Mata wang kontrak projek</td>
</tr>
<tr>
<td rowspan="3">Invois disahkan dan pengurangan dalam masa boleh dibilkan berlaku.</td>
<td>Pengunduran jualan belum dibilkan</td>
<td>Mata wang kontrak projek</td>
<td rowspan="3">Tidak berkenaan</td>
<td rowspan="3">Tidak berkenaan</td>
<td rowspan="3">Tidak berkenaan</td>
<td rowspan="3">Tidak berkenaan</td>
</tr>
<tr>
<td>Jualan dibilkan – Boleh dituntut untuk kuantiti baharu</td>
<td>Mata wang kontrak projek</td>
</tr>
<tr>
<td>Jualan dibilkan – Tidak boleh dituntut untuk perbezaan</td>
<td>Mata wang kontrak projek</td>
</tr>
<tr>
<td rowspan="2">Invois dibetulkan untuk menambah kuantiti yang boleh dituntut.</td>
<td>Julana dibilkan – Pengunduran</td>
<td>Mata wang kontrak projek</td>
<td rowspan="5">
<ul>
<li>Pengunduran jualan dibilkan untuk pencapaian</li>
<li>Penukarang status pencapaian daripada <strong>Diinvoiskan</strong> kepada <strong>Sedia untuk invois</strong></li>
</ul>
</td>
<td rowspan="5">Mata wang kontrak projek</td>
<td rowspan="5">Tidak berkenaan</td>
<td rowspan="5">Tidak berkenaan</td>
</tr>
<tr>
<td>Jualan dibilkan</td>
<td>Mata wang kontrak projek</td>
</tr>
<tr>
<td rowspan="3">Invois dibetulkan untuk mengurangkan kuantiti yang boleh dituntut.</td>
<td>Julana dibilkan – Pengunduran</td>
<td>Mata wang kontrak projek</td>
</tr>
<tr>
<td>Jualan dibilkan untuk kuantiti baharu</td>
<td>Mata wang kontrak projek</td>
</tr>
<tr>
<td>Jualan tidak dibilkan – Boleh dituntut untuk perbezaan</td>
<td>Mata wang kontrak projek</td>
</tr>
</tbody>
</table>
