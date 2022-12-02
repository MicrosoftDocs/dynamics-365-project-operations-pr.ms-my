---
title: Perkara baharu November 2021 - Project Operations untuk senario berasaskan sumber/bukan stok
description: Artikel ini memberikan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran November 2021 bagi Project Operations untuk senario berasaskan sumber/bukan stok.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d5b58965f728321cc30d4e476b0dacf621fdec71
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932905"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Perkara baharu November 2021 - Project Operations untuk senario berasaskan sumber/bukan stok

*Digunakan Pada: Project Operations untuk senario berdasarkan sumber/tidak distok*

Artikel ini digunakan pada komponen dan versi Microsoft Dynamics 365 Project Operations berikut:

- Project Operations dalam persekitaran Dataverse versi 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
- Pengurusan projek dan perakaunan dalam persekitaran Dynamics 365 Finance versi 10.0.22

## <a name="features-included-in-this-release"></a>Ciri yang disertakan dalam keluaran ini

Ciri berikut disertakan dalam keluaran ini:

- Antara muka pengaturcaraan (API) Projek Penjadualan kini menyokong keupayaan untuk mencipta dan memadamkan baldi Projek.

## <a name="project-operations-dual-write-maps-updates"></a>Kemas kini peta dwi tulis Project Operations

Tiada kemas kini untuk peta dwi tulis Project Operations dalam keluaran ini. Untuk senarai semasa dan versi peta dwi tulis Project Operations, lihat [Versi peta dwi tulis Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Sentiasa menjalankan versi terkini peta dalam persekitaran anda, dan mendayakan semua peta jadual berkaitan ketika anda mengemas kini versi penyelesaian Project Operations Dataverse dan penyelesaian Kewangan anda. Sesetengah ciri dan keupayaan mungkin tidak berfungsi dengan betul jika versi terkini peta tidak diaktifkan. Anda boleh melihat versi aktif peta dalam lajur **Versi** pada halaman **Dwi tulis**. Untuk mengaktifkan versi baharu peta dengan, pilih **Versi peta jadual**, pilih versi terkini dan kemudian simpan versi yang dipilih. Jika anda sudah mempunyai peta jadual luar kotak tersuai, mohon semula perubahan. Untuk maklumat lanjut, lihat [Pengurusan kitaran hayat Aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika anda mengalami isu semasa anda memulakan peta, ikut arahan dalam bahagian [Isu lajur jadual yang hilang pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) bagi panduan penyelesaian masalah Dwi tulis.

## <a name="quality-updates"></a>Kemas kini kualiti

### <a name="project-operations-in-dataverse"></a>Project Operations dalam Dataverse

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Pengebilan dan Penentuan Harga | 2240080 | Medan **Terma pembayaran** tidak boleh diulang pada invois pro forma. |
| Pengebilan dan Penentuan Harga | 2358236 | Pembetulan invois mesti membenarkan pembetulan yang mempunyai baris sifar harga. |
| Pengurusan Sumber | 2410072 | Benarkan persediaan sumber yang diuntukkan kepada tugas sebagai pengurus projek. |
| Pengebilan dan Penentuan Harga | 2430234 | Betulkan isu pengiraan prestasi kos. |
| Masa dan Perbelanjaan | 2436978 | Benarkan masa untuk dimasukkan dalam format jj: mm. |
| Pengebilan dan Penentuan Harga | 2448623 | Benarkan senarai harga yang akan dikemas kini selepas dikaitkan dengan unit organisasi. |
| Masa dan Perbelanjaan | 2460396 | Benarkan entri masa dipadamkan dengan mengosongkan sel. |
| Pengebilan dan Penentuan Harga | 2467386 | Benarkan projek yang mempunyai tugas untuk dipadamkan, walaupun tugas berkaitan dengan sebut harga yang dimenangi. |
| Masa dan Perbelanjaan | 2461744 | Pandangan **Kelulusan gagal saya** hanya mengandungi kelulusan projek di peringkat **Diserahkan**. |
| Masa dan Perbelanjaan | 2464082 | Keluarkan pautan daripada kelulusan projek kepada set kelulusan apabila status sasaran dipadankan. |
| Masa dan Perbelanjaan | 2468108 | Kerja Jadual tidak sepatutnya menetapkan status **Pemprosesan** untuk set kelulusan. |
| Masa dan Perbelanjaan | 2471503 | Padamkan set kelulusan yang berusia tujuh hari. |
| Pengebilan dan Penentuan Harga | 2480687 | Rujukan baris sebut harga tidak boleh dialih keluar apabila pencapaian baris sebut harga dicipta. |

### <a name="project-management-and-accounting-in-finance"></a>Pengurusan projek dan perakaunan dalam Kewangan

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Pengurusan projek dan perakaunan | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Jumlah vendor yang dikekalkan dalam urus niaga perbelanjaan projek tidak ditunjukkan dalam senarai transaksi. |
| Pengurusan projek dan perakaunan | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Invois vendor antara syarikat rosak apabila penyepaduan invois vendor dihidupkan. |
| Pengurusan projek dan perakaunan | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Terma pembayaran pada invois projek tidak berfungsi seperti yang dijangkakan. |
| Pengurusan projek dan perakaunan | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Apabila pengekalan vendor dikeluarkan, penyiaran baucar mempunyai baris tambahan yang salah. |
| Pengurusan projek dan perakaunan | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Apabila jurnal penyepaduan Project Operations disiarkan, jurnal tersebut gagal kerana tiada dimensi akaun yang tidak disiarkan. |
| Pengurusan projek dan perakaunan | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Tab **Projek** tidak boleh diedit pada invois vendor yang belum selesai apabila kategori perolehan diuntukkan untuk item. |
| Pengurusan projek dan perakaunan | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Tiada anak tetingkap navigasi jika anda tidak didaftar masuk ke Project Operations Dataverse. |
| Pengurusan projek dan perakaunan | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Apabila anda menyiarkan hasil daripada invois projek dalam kes retainer yang digunakan, isu berlaku kerana urus niaga pada baucar tidak seimbang. |
| Pengurusan projek dan perakaunan | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Penciptaan anggaran selepas anda menyiarkan cadangan invois menyekat baris pembetulan daripada import. |
| Pengurusan projek dan perakaunan | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Pengubahsuaian rekod pencapaian invois penuh tidak boleh dilakukan. |
| Perjalanan dan Perbelanjaan | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Semua laporan perbelanjaan boleh dilihat apabila anda mencari kategori dalam aplikasi mudah alih Perbelanjaan. |
| Perjalanan dan Perbelanjaan | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Jumlah salah pada urus niaga vendor dan urus niaga cukai jualan disiarkan daripada perbelanjaan yang dicipta daripada urus niaga kad kredit. |
| Perjalanan dan Perbelanjaan | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Mesej amaran yang tidak relevan berlaku apabila anda menyegar semula halaman **Laporan perbelanjaan**. |
| Perjalanan dan Perbelanjaan | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Pelulus interim yang salah digunakan apabila anda memadamkan pelulus interim, kemudian menyerahkan semula laporan perbelanjaan melalui aliran kerja. |
| Perjalanan dan Perbelanjaan | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Ralat penyiaran yang berkaitan dengan persediaan perbatuan berlaku. |
