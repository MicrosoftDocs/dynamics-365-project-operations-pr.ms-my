---
title: Aktual
description: Topik ini memberikan maklumat tentang cara untuk bekerja dengan aktual dalam Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9e046602a3005930c41ab8c50472d5b1a72303c6
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368622"
---
# <a name="actuals"></a>Aktual 

_**Gunakan pada:** Project Operations untuk senario berdasarkan sumber/bukan stok, Pelaksanaan ringan - urusan untuk penginvoisan proforma_

Aktual mewakili kemajuan kewangan dan jadual yang disemak dan diluluskan untuk sesuatu projek. Ia dicipta hasil daripada kelulusan masa, perbelanjaan, entri penggunaan bahan serta entri jurnal dan invois.

## <a name="journal-lines-and-time-submission"></a>Garisan jurnal dan serahan masa

Untuk mendapatkan maklumat lanjut tentang entri masa, lihat [Gambaran keseluruhan entri masa](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Masa dan bahan

Apabila entri masa yang diserahkan telah dipautkan dengan projek yang dipetakan dengan baris kontrak masa dan bahan, sistem mencipta dua garisan jurnal, satu untuk kos dan satu untuk jualan yang tidak dibilkan.

### <a name="fixed-price"></a>Harga tetap

Apabila entri masa yang telah diserahkan dipautkan kepada projek yang dipetakan kepada baris kontrak harga tetap, sistem mencipta satu garisan jurnal untuk kos.

### <a name="default-pricing"></a>Penetapan harga lalai

Logik untuk mencipta harga lalai terletak pada garisan jurnal. Nilai medan daripada entri masa disalin kepada garisan jurnal. Nilai-nilai ini termasuk tarikh transaksi, baris kontrak yang projek dipetakan padanya, dan mata wang yang menghasilkan senarai harga yang sesuai.

Medan yang menjejaskan penetapan harga lalai, seperti **Peranan** dan **Unit Penyumberan**, digunakan untuk menentukan harga bersesuaian pada garisan jurnal. Anda boleh menambah medan tersuai pada entri masa. Jika anda mahu nilai medan disebarluaskan pada aktual, cipta medan dalam jadual **Aktual** dan **Garisan Jurnal**. Gunakan kod tersuai untuk menyebarluaskan nilai medan yang dipilih daripada Entri Masa kepada Aktual melalui baris jurnal menggunakan asal transaksi. Untuk mendapatkan maklumat lanjut tentang asal transaksi dan sambungan, lihat [Memautkan aktual pada rekod asal](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-basic-expense-submission"></a>Serahan garisan jurnal dan perbelanjaan asas

Untuk mendapatkan maklumat lanjut tentang entri perbelanjaan, lihat [Gambaran keseluruhan perbelanjaan](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Masa dan bahan

Apabila entri perbelanjaan asas yang diserahkan telah dipautkan kepada projek yang dipetakan kepada baris kontrak masa dan bahan, sistem mencipta dua garisan jurnal, satu untuk kos dan satu untuk jualan yang tidak dibilkan.

### <a name="fixed-price"></a>Harga tetap

Apabila entri perbelanjaan asas yang diserahkan dipautkan pada projek yang dipetakan kepada baris kontrak harga tetap, sistem mencipta satu garisan jurnal untuk kos.

### <a name="default-pricing"></a>Penetapan harga lalai

Logik untuk memasukkan harga lalai bagi perbelanjaan adalah berdasarkan kategori perbelanjaan. Tarikh transaksi, baris kontrak yang projek dipetakan dan mata wang, semuanya digunakan untuk menentukan senarai harga bersesuaian. Medan yang menjejaskan penetapan harga lalai, seperti **Kategori Transaksi** dan **Unit**, digunakan untuk menentukan harga bersesuaian pada garisan jurnal. Walau bagaimanapun, ini hanya berfungsi apabila kaedah penetapan harga dalam senarai harga ialah **Harga setiap unit**. Jika kaedah penetapan harga ialah **Pada kos** atau **Tokokan ke atas kos**, harga yang dimasukkan apabila entri perbelanjaan dicipta akan digunakan untuk kos dan harga pada garisan jurnal jualan dikira berdasarkan kaedah penetapan harga. 

Anda boleh menambahkan medan tersuai pada entri perbelanjaan. Jika anda mahu nilai medan disebarluaskan pada aktual, cipta medan dalam jadual **Aktual** dan **Garisan Jurnal**. Gunakan kod tersuai untuk menyebarluaskan nilai medan yang dipilih daripada Entri Masa kepada Aktual melalui baris jurnal menggunakan asal transaksi. Untuk mendapatkan maklumat lanjut tentang asal transaksi dan sambungan, lihat [Memautkan aktual pada rekod asal](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-material-usage-log-submission"></a>Penyerahan log garisan jurnal dan penggunaan bahan

Untuk mendapatkan maklumat lanjut tentang entri perbelanjaan, lihat [Log Penggunaan Bahan](../material/material-usage-log.md).

### <a name="time-and-materials"></a>Masa dan bahan

Apabila entri log penggunaan bahan yang diserahkan dikaitkan dengan projek yang dipetakan kepada baris kontrak masa dan bahan, sistem mencipta dua garisan jurnal, satu untuk kos dan satu untuk jualan yang belum dibilkan.

### <a name="fixed-price"></a>Harga tetap

Apabila entri log penggunaan bahan yang diserahkan dipautkan pada projek yang dipetakan kepada baris kontrak harga tetap, sistem mencipta satu garisan jurnal untuk kos.

### <a name="default-pricing"></a>Penetapan harga lalai

Logik untuk memasukkan harga lalai bagi bahan adalah berdasarkan gabungan produk dan unit. Tarikh transaksi, baris kontrak yang projek dipetakan dan mata wang, semuanya digunakan untuk menentukan senarai harga bersesuaian. Medan yang menjejaskan penetapan harga lalai, seperti **ID Produk** dan **Unit**, digunakan untuk menentukan harga bersesuaian pada garisan jurnal. Walau bagaimanapun, ini hanya berfungsi untuk produk katalog. Untuk produk masukan manual, harga yang dimasukkan apabila entri log penggunaan bahan dicipta digunakan untuk kos dan harga jualan pada garisan jurnal. 

Anda boleh menambahkan medan tersuai pada entri **Log Penggunaan Bahan**. Jika anda mahu nilai medan disebarluaskan pada aktual, cipta medan dalam jadual **Aktual** dan **Garisan Jurnal**. Gunakan kod tersuai untuk menyebarluaskan nilai medan yang dipilih daripada Entri Masa kepada Aktual melalui baris jurnal menggunakan asal transaksi. Untuk mendapatkan maklumat lanjut tentang asal transaksi dan sambungan, lihat [Memautkan aktual pada rekod asal](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="use-entry-journals-to-record-costs"></a>Gunakan jurnal entri untuk merekodkan kos

Anda boleh menggunakan jurnal entri untuk merekodkan kos atau hasil dalam kelas bahan, yuran, masa, perbelanjaan, atau transaksi cukai. Jurnal boleh digunakan untuk tujuan berikut:

- Alihkan aktual transaksi daripada sistem lain kepada Microsoft Dynamics 365 Project Operations.
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
