---
title: Perkara baharu November 2021 - Project Operations untuk senario berasaskan sumber/bukan stok
description: Artikel ini memberikan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran November 2021 Operasi Projek untuk senario berasaskan sumber/tidak berstok.
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

Artikel ini terpakai kepada komponen dan versi Microsoft Dynamics 365 Project Operations berikut :

- Operasi Projek dalam versi persekitaran 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155 Dataverse
- Pengurusan projek dan perakaunan dalam persekitaran yang Dynamics 365 Finance versi 10.0.22

## <a name="features-included-in-this-release"></a>Ciri yang disertakan dalam keluaran ini

Ciri berikut disertakan dalam keluaran ini:

- Antara muka pengaturcaraan aplikasi Penjadualan Projek (API) kini menyokong keupayaan untuk mencipta dan memadam baldi Projek.

## <a name="project-operations-dual-write-maps-updates"></a>Kemas kini peta dwi tulis Project Operations

Tiada kemas kini untuk peta dwi tulis Project Operations dalam keluaran ini. Untuk senarai semasa dan versi peta dwi tulis Project Operations, lihat [Versi peta dwi tulis Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Sentiasa jalankan versi terkini peta dalam persekitaran anda dan dayakan semua peta jadual yang berkaitan semasa anda mengemas kini penyelesaian Operasi Dataverse Projek dan versi penyelesaian Kewangan anda. Sesetengah ciri dan keupayaan mungkin tidak berfungsi dengan betul jika versi terkini peta tidak diaktifkan. Anda boleh melihat versi aktif peta dalam lajur **Versi** pada halaman **Dwi tulis**. Untuk mengaktifkan versi baharu peta dengan, pilih **Versi peta jadual**, pilih versi terkini dan kemudian simpan versi yang dipilih. Jika anda telah menyesuaikan peta jadual di luar kotak, gunakan semula perubahan. Untuk maklumat lanjut, lihat [Pengurusan kitaran hayat Aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika anda menghadapi isu apabila anda memulakan peta, ikut arahan dalam [isu lajur jadual hilang pada bahagian peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) panduan penyelesaian masalah Dwi-tulis.

## <a name="quality-updates"></a>Kemas kini kualiti

### <a name="project-operations-in-dataverse"></a>Operasi Projek di Dataverse

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Pengebilan dan Penentuan Harga | 2240080 | Medan **Terma** pembayaran tidak boleh diduplikasi pada invois pro forma. |
| Pengebilan dan Penentuan Harga | 2358236 | Pembetulan invois mesti membenarkan pembetulan yang mempunyai garis harga sifar. |
| Pengurusan Sumber | 2410072 | Benarkan persediaan sumber yang diperuntukkan kepada tugas sebagai pengurus projek. |
| Pengebilan dan Penentuan Harga | 2430234 | Betulkan isu pengiraan prestasi kos. |
| Masa dan Perbelanjaan | 2436978 | Benarkan masa dimasukkan dalam format hh:mm. |
| Pengebilan dan Penentuan Harga | 2448623 | Benarkan senarai harga dikemas kini selepas ia dikaitkan dengan unit organisasi. |
| Masa dan Perbelanjaan | 2460396 | Benarkan entri masa dihapuskan dengan mengosongkan sel. |
| Pengebilan dan Penentuan Harga | 2467386 | Benarkan projek yang mempunyai tugas untuk dipadamkan, walaupun tugas itu dikaitkan dengan petikan yang dimenangi. |
| Masa dan Perbelanjaan | 2461744 | Pandangan **kelulusan Saya yang gagal** hanya mengandungi kelulusan projek dalam **peringkat Dihantar**. |
| Masa dan Perbelanjaan | 2464082 | Alih keluar pautan daripada kelulusan projek kepada set kelulusan kelulusan apabila status sasaran dipadankan. |
| Masa dan Perbelanjaan | 2468108 | Kerja Jadual tidak boleh menetapkan **status Pemprosesan** untuk set kelulusan. |
| Masa dan Perbelanjaan | 2471503 | Padamkan set kelulusan yang berusia tujuh hari. |
| Pengebilan dan Penentuan Harga | 2480687 | Rujukan baris petikan tidak boleh dialih keluar apabila peristiwa penting baris sebut harga dicipta. |

### <a name="project-management-and-accounting-in-finance"></a>Pengurusan projek dan perakaunan dalam Kewangan

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Pengurusan projek dan perakaunan | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Jumlah vendor tertahan dalam transaksi perbelanjaan projek tidak ditunjukkan dalam senarai transaksi. |
| Pengurusan projek dan perakaunan | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Invois vendor antara syarikat rosak apabila penyepaduan invois vendor dihidupkan. |
| Pengurusan projek dan perakaunan | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Syarat pembayaran pada invois projek tidak berfungsi seperti yang diharapkan. |
| Pengurusan projek dan perakaunan | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Apabila pengekalan vendor dikeluarkan, pengeposan baucar mempunyai baris tambahan yang tidak betul. |
| Pengurusan projek dan perakaunan | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Apabila jurnal integrasi Project Operations disiarkan, ia gagal kerana dimensi yang hilang untuk akaun yang tidak disiarkan. |
| Pengurusan projek dan perakaunan | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Tab **Projek** tidak boleh diedit pada invois vendor yang belum selesai apabila kategori perolehan diuntukkan kepada item. |
| Pengurusan projek dan perakaunan | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Anak tetingkap navigasi hilang jika anda tidak log masuk ke Project Operations Dataverse. |
| Pengurusan projek dan perakaunan | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Apabila anda menyiarkan hasil daripada invois projek dalam kes penahan yang digunakan, isu berlaku kerana transaksi pada baucar tidak seimbang. |
| Pengurusan projek dan perakaunan | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Penciptaan anggaran selepas anda menyiarkan cadangan invois menyekat garisan pembetulan daripada import. |
| Pengurusan projek dan perakaunan | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Pengubahsuaian rekod pencapaian invois sepenuhnya tidak boleh dilakukan. |
| Perjalanan dan Perbelanjaan | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Semua laporan perbelanjaan boleh dilihat apabila anda mencari kategori dalam aplikasi mudah alih Perbelanjaan. |
| Perjalanan dan Perbelanjaan | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Jumlah yang tidak betul pada transaksi vendor dan transaksi cukai jualan disiarkan dari perbelanjaan yang dibuat dari transaksi kad kredit. |
| Perjalanan dan Perbelanjaan | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Amaran yang tidak berkaitan berlaku apabila anda menyegar semula **halaman laporan** Perbelanjaan. |
| Perjalanan dan Perbelanjaan | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Pelulus interim yang salah digunakan apabila anda memadamkan pelulus interim dan kemudian menghantar semula laporan perbelanjaan melalui aliran kerja. |
| Perjalanan dan Perbelanjaan | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Ralat pengeposan yang berkaitan dengan persediaan perbatuan berlaku. |
