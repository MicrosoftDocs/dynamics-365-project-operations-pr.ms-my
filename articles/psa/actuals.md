---
title: Gambaran keseluruhan aktual
description: Topik ini memberikan maklumat tentang aktual projek.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 63ad6544f0ec0a893aebd8d81f3ee895e51c294e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146134"
---
# <a name="actuals-overview"></a>Gambaran keseluruhan aktual

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Aktual ialah jumlah kerja yang telah disiapkan pada sebuah projek. Aktual projek boleh dikesan kembali kepada dokumen sumber mereka. Dokumen sumber tersebut termasuk entri masa, perbelanjaan dan jurnal dan serta invois.

![Cara aktual projek dikesan untuk mendapatkan dokumen sumber](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Menyerahkan entri masa

Dalam PSA, apabila entri masa telah diserahkan untuk projek yang dipetakan kepada garis kontrak masa dan bahan, dua garisan jurnal dicipta. Satu garis ialah untuk kos, dan garis lain ialah untuk jualan yang tidak dibilkan. Apabila entri masa telah diserahkan untuk projek yang dipetakan kepada garis kontrak harga tetap, satu garis jurnal dicipta hanya untuk kos. 

Logik untuk memasukkan harga lalai pada garisan jurnal. Semua nilai medan daripada entri masa disalin ke garisan jurnal. Medan-medan ini termasuk tarikh transaksi, baris kontrak yang projek dipetakan dan keputusan mata wang dalam senarai harga bersesuaian. 

Medan-medan yang menjejaskan harga lalai, seperti **Peranan** dan **Unit Organisasi**, menyebabkan harga bersesuaian akan dimasukkan secara lalai pada garisan jurnal. Jika anda menambah medan tersuai pada entri masa dan anda mahu nilai medan disebarkan kepada aktual, cipta medan pada entiti Aktual dan gunakan pemetaan medan untuk menyalin medan daripada entri masa kepada aktual.

## <a name="submitting-an-expense-entry"></a>Menyerahkan entri perbelanjaan

Dalam PSA, apabila entri perbelanjaan telah diserahkan untuk projek yang dipetakan kepada garis kontrak masa dan bahan, dua garisan jurnal dicipta. Satu garis ialah untuk kos, dan garis lain ialah untuk jualan yang tidak dibilkan. Apabila entri perbelanjaan telah diserahkan untuk projek yang dipetakan kepada garis kontrak harga tetap, satu garis jurnal dicipta hanya untuk kos.

Logik untuk memasukkan harga lalai bagi perbelanjaan adalah berdasarkan pada kategori perbelanjaan yang dipilih pada halaman **Entri perbelanjaan**. Tarikh transaksi, baris kontrak yang projek dipetakan dan mata wang semuanya digunakan untuk menentukan senarai harga bersesuaian. Walau bagaimanapun, untuk harga itu sendiri, jumlah yang pengguna masukkan ditetapkan secara langsung pada garisan jurnal perbelanjaan berkaitan untuk kos dan jualan secara lalai.

Dalam versi terkini PSA, entri berasaskan kategori setiap unit harga lalai pada entri perbelanjaan tidak tersedia.

## <a name="using-entry-journals-to-record-costs"></a>Menggunakan jurnal Entri untuk merekodkan kos

Di PSA, jurnal entri membolehkan anda merekodkan kos atau hasil dalam kelas transaksi bahan, yuran, masa, perbelanjaan, atau cukai. Jurnal mempunyai pengepala, baris dan tindakan **Sahkan**. Berikut ialah beberapa senario di mana anda mungkin menggunakan jurnal:

- Anda mesti merakam kos aktual bahan dan jualan pada projek.
- Anda mesti mengalihkan transaksi aktual daripada sistem lain ke PSA.
- Anda mesti merekodkan kos yang berlaku dalam sistem lain, seperti kos perolehan atau subkontrak.

> [!IMPORTANT]
> Menggunakan jurnal Entri untuk mewujudkan aktual hanya boleh dilakukan oleh pengguna yang menyedari sepenuhnya kesan perakaunan yang terdapat pada aktual terhadap projek tersebut. Ini kerana aplikasi tidak mengesahkan jenis garisan jurnal, atau penentuan harga berkaitan yang dimasukkan pada garisan jurnal. Disebabkan oleh kesan jenis jurnal ini, beri perhatian yang mencukupi kepada orang yang diberikan akses untuk mencipta jurnal Entri.     


## <a name="recording-actuals-based-on-project-events"></a>Merekod aktual berdasarkan peristiwa projek

PSA merekod transaksi kewangan yang berlaku semasa projek. Transaksi ini direkodkan sebagai **aktual**. Jadual berikut menunjukkan jenis aktual berbeza yang dicipta, bergantung pada sama ada projek itu adalah projek masa dan bahan atau projek harga tetap, dalam peringkat prajualan, atau merupakan projek dalaman.

**Sumber tersebut tergolong dalam unit organisasi yang sama seperti unit kontrak projek**

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

**Sumber tersebut tergolong dalam unit organisasi yang berbeza daripada unit kontrak projek**

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
