---
title: Perkara baharu November 2021 - Project Operations untuk senario berasaskan sumber/bukan stok
description: Topik ini menyediakan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran Operasi Projek november 2021 untuk senario berasaskan sumber / tidak lengkap.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 20f277bc9b6f571c0144eaaa867bb97c0cf30ddb
ms.sourcegitcommit: 04ebe764afa22742b3fbf8f12af31e8eea93682e
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/23/2021
ms.locfileid: "7827337"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Perkara baharu November 2021 - Project Operations untuk senario berasaskan sumber/bukan stok

*Digunakan Pada: Project Operations untuk senario berdasarkan sumber/tidak distok*

Topik ini digunakan pada komponen dan versi Microsoft Dynamics 365 Project Operations berikut:

- Operasi Projek dalam 4.26.0.145, 4.26.0.148, versi persekitaran Dataverse atau 4.26.0.150
- Pengurusan projek dan perakaunan dalam persekitaran Dynamics 365 Finance versi 10.0.22

## <a name="features-included-in-this-release"></a>Ciri yang disertakan dalam keluaran ini

Ciri berikut disertakan dalam keluaran ini:

- Antara muka pengaturcaraan aplikasi Penjadualan Projek (API) kini menyokong keupayaan untuk mencipta dan memadam baldi Projek.

## <a name="project-operations-dual-write-maps-updates"></a>Kemas kini peta dwi tulis Project Operations

Tiada kemas kini untuk peta dwi tulis Project Operations dalam keluaran ini. Untuk senarai semasa dan versi peta dwi tulis Project Operations, lihat [Versi peta dwi tulis Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Sentiasa jalankan versi terkini peta dalam persekitaran anda dan dayakan semua peta jadual yang berkaitan semasa anda mengemas kini Operasi Projek Dataverse penyelesaian dan versi penyelesaian Kewangan anda. Sesetengah ciri dan keupayaan mungkin tidak berfungsi dengan betul jika versi peta terkini tidak diaktifkan. Anda boleh melihat versi aktif peta dalam lajur **Versi** pada halaman **Dwi tulis**. Untuk mengaktifkan versi baharu peta dengan, pilih **Versi peta jadual**, pilih versi terkini dan kemudian simpan versi yang dipilih. Jika anda telah menyesuaikan peta jadual di luar kotak, gunakan semula perubahan. Untuk maklumat lanjut, lihat [Pengurusan kitaran hayat Aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika anda menghadapi isu apabila anda memulakan peta, ikut arahan dalam [lajur Jadual hilang isu pada bahagian peta panduan penyelesaian masalah](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) dwi-tulis.

## <a name="quality-updates"></a>Kemas kini kualiti

### <a name="project-operations-in-dataverse"></a>Operasi Projek dalam Dataverse

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Pengebilan dan Penentuan Harga | 2240080 | **Medan Terma pembayaran tidak boleh** diduplikasi pada invois pro forma. |
| Pengebilan dan Penentuan Harga | 2358236 | Pembetulan invois mesti membenarkan pembetulan yang mempunyai garis harga sifar. |
| Pengurusan Sumber | 2410072 | Benarkan persediaan sumber yang diuntukkan kepada tugas sebagai pengurus projek. |
| Pengebilan dan Penentuan Harga | 2430234 | Betulkan isu pengiraan prestasi kos. |
| Masa dan Perbelanjaan | 2436978 | Benarkan masa dimasukkan dalam format hh:mm. |
| Pengebilan dan Penentuan Harga | 2448623 | Benarkan senarai harga dikemas kini selepas ia dikaitkan dengan unit organisasi. |
| Masa dan Perbelanjaan | 2460396 | Benarkan entri masa untuk dihapuskan dengan mengosongkan sel. |
| Pengebilan dan Penentuan Harga | 2467386 | Benarkan projek yang mempunyai tugas dipadamkan, walaupun tugas dikaitkan dengan sebut harga yang dimenangi. |
| Masa dan Perbelanjaan | 2461744 | **Pandangan Kelulusan saya yang gagal hanya mengandungi kelulusan projek dalam peringkat** **Dihantar**. |
| Masa dan Perbelanjaan | 2464082 | Alih keluar pautan daripada kelulusan projek kepada set kelulusan apabila status sasaran dipadankan. |
| Masa dan Perbelanjaan | 2468108 | Kerja Jadual tidak boleh menetapkan **status Pemprosesan untuk set** kelulusan. |
| Masa dan Perbelanjaan | 2471503 | Padamkan set kelulusan yang berumur tujuh hari. |
| Pengebilan dan Penentuan Harga | 2480687 | Rujukan baris sebut harga tidak boleh dialih keluar apabila tonggak baris sebut harga dicipta. |

### <a name="project-management-and-accounting-in-finance"></a>Pengurusan projek dan perakaunan dalam Kewangan

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Pengurusan projek dan perakaunan | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Amaun vendor tertahan dalam urus niaga perbelanjaan projek tidak ditunjukkan dalam senarai transaksi. |
| Pengurusan projek dan perakaunan | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Invois vendor antara syarikat rosak apabila integrasi invois vendor dihidupkan. |
| Pengurusan projek dan perakaunan | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Syarat pembayaran pada invois projek tidak berfungsi seperti yang dijangkakan. |
| Pengurusan projek dan perakaunan | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Apabila pengekalan vendor dikeluarkan, pengeposan baucar mempunyai baris tambahan yang tidak betul. |
| Pengurusan projek dan perakaunan | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Apabila jurnal integrasi Operasi Projek disiarkan, ia gagal kerana dimensi yang hilang untuk akaun yang tidak disiarkan. |
| Pengurusan projek dan perakaunan | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | **Tab Projek tidak boleh** diedit pada invois vendor belum selesai apabila kategori perolehan diberikan kepada item. |
| Pengurusan projek dan perakaunan | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Anak tetingkap navigasi hilang jika anda tidak log masuk ke Dataverse Operasi Projek. |
| Pengurusan projek dan perakaunan | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Apabila anda menyiarkan hasil daripada invois projek dalam kes penahan yang digunakan, isu berlaku kerana transaksi pada baucar tidak seimbang. |
| Pengurusan projek dan perakaunan | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Penciptaan anggaran selepas anda menyiarkan cadangan invois menyekat garisan pembetulan daripada import. |
| Pengurusan projek dan perakaunan | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Pengubahsuaian rekod tonggak yang diinvois sepenuhnya tidak boleh dilakukan. |
| Perjalanan dan Perbelanjaan | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Semua laporan perbelanjaan boleh dilihat apabila anda mencari kategori dalam apl mudah alih Perbelanjaan. |
| Perjalanan dan Perbelanjaan | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Jumlah yang salah pada transaksi vendor dan transaksi cukai jualan dicatatkan daripada perbelanjaan yang dibuat daripada transaksi kad kredit. |
| Perjalanan dan Perbelanjaan | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Amaran yang tidak berkaitan berlaku apabila anda menyegar semula **halaman Laporan** perbelanjaan. |
| Perjalanan dan Perbelanjaan | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Pelulus interim yang salah digunakan apabila anda memadamkan pelulus interim dan kemudian menyerahkan semula laporan perbelanjaan melalui aliran kerja. |
| Perjalanan dan Perbelanjaan | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Ralat pengeposan yang berkaitan dengan persediaan perbatuan berlaku. |
