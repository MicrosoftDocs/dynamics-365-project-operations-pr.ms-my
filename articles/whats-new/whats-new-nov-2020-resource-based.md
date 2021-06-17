---
title: Perkara baharu November 2020 - Project Operations untuk senario berasaskan sumber/bukan stok
description: Topik ini memberikan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran November 2020 bagi Project Operations untuk senario berasaskan sumber/bukan stok.
author: sigitac
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f6b14a1cbe7f3d41c86aedaf863434214f911eaa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995632"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Perkara baharu November 2020 - Project Operations untuk senario berasaskan sumber/bukan stok

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Topik ini digunakan pada komponen dan versi Dynamics 365 Project Operations berikut:

- Project Operations pada persekitaran CDS versi 4.4.0.70
- Pengurusan projek dan perakaunan dalam persekitaran Dynamics 365 Finance versi 10.0.14

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Kemas kini untuk Project Operations bagi senario berasaskan sumber bukan stok

### <a name="project-operations-on-cds"></a>Project Operations pada CDS

| Bahagian ciri                 | Nombor rujukan | Kemas kini kualiti                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Pengurusan peluang       | 2036993          | Anggaran penugasan baris dan sumber untuk baris kontrak dikemas kini pada sebut harga yang dimenangi apabila jenis baris sebut harga ialah **Semua tugas**.                                                 |
| Pengebilan dan harga          | 2070392          | Baris kontrak projek pada peningkatan invois setiap kali **Transaksi invois segar semula** dipilih.                                                                         |
| Perancangan projek             | 2043336          | Tidak dapat memadamkan rekod ahli pasukan projek.                                                                                                                                  |
| Perancangan projek             | 2046013          | Tingkah laku yang tidak konsisten untuk Anggaran lajur tag semasa beban berbanding penukaran jenis fasa masa.                                                                                   |
| Perancangan projek             | 2046647          | Masa mula dan tamat dimatikan sejam apabila keperluan sumber dijanakan daripada ahli pasukan projek.                                                                      |
| Perancangan projek             | 2053879          | (Setiap pengeluaran CDS akan datang) PublishUnassignedAssignments mematahkan percubaan untuk menyimpan tugas apabila ralat, "Nilai yang diluluskan untuk ConditionOperator.In ialah kosong".                       |
| Perancangan projek             | 2055501          | Membiarkan medan **Tarikh Mula Projek** kosong menyebabkan kegagalan dalam jadual.                                                                                                      |
| Perancangan projek             | 2066817          | Tidak dapat mencipta sumber generik menggunakan pemilih orang pada tab **Tugas**.                                                                                                   |
| Perancangan projek             | 2067034          | Butang **Lihat Butiran** tidak tersedia pada halaman **Butiran Tugas**.                                                                                                       |
| Pengurusan sumber          | 2046667          | Ahli pasukan generik tidak akan dipadamkan walaupun setelah semua sumber dipenuhi.                                                                                                    |
| Masa dan entri perbelanjaan pantas | 2047499          | Butang **Baharu** pada halaman Entri Masa membuka halaman **Pengenalan E-mel Baharu**.                                                                                               |
| Masa dan entri perbelanjaan pantas | 2059859          | Tetingkap timbul tidak dijangka terbuka apabila mencipta entri perbelanjaan.                                                                                                                         |
| Lain-lain                        | 2044181          | (Penyahpasangan pesanan pembelian) Apabila cuba untuk menyahpasang msdyn_ProjectServiceCore_Patch dan penyelesaian teras msdyn Project Service, berlaku ralat "Rekod tidak tersedia".  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Pengurusan projek dan perakaunan dalam Dynamics 365 Finance

| Bahagian ciri        | Nombor rujukan | Kemas kini kualiti                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pengiktirafan hasil | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | Peratusan anggaran projek selesai salah apabila kontrak menggunakan mata wang asing dan peratusan kemajuan kerja untuk kaedah lengkap.                     |
| Pengiktirafan hasil | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | Tidak dapat menyiarkan anggaran dengan kaedah penyelesaian **Kos sebenar**.                                                                                                    |
| Pengiktirafan hasil | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | Penghapusan gagal kerana ralat ketidakseimbangan baucar apabila mata wang syarikat dan mata wang transaksi berbeza.                                              |
| Pengurusan perbelanjaan  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | Untuk pengguna bukan pentadbir, nilai carian untuk lajur baris perbelanjaan seperti **ID Projek** dan **Kategori Perbelanjaan** tidak ditunjukkan dengan betul dalam bingkai penyambung data. |
| Pengurusan perbelanjaan  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | Sifat baris lalai tidak dipaparkan untuk kategori Perbelanjaan.                                                                                                         |
| Pengurusan perbelanjaan  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | Integrasi perbelanjaan mesti merangkumi sifat baris daripada laporan perbelanjaan.                                                                                             |
| Penginvoisan           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | Tidak dapat menyiarkan cadangan invois projek kerana mesej ralat yang menyatakan gabungan FD tidak disahkan.                                                    |
| Penginvoisan           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | Tidak dapat melihat transaksi daripada halaman butiran **invois**.                                                                                                              |
| Penginvoisan           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | Baris cadangan invois boleh dipadamkan.                                                                                                                                  |
| Perakaunan projek  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Item menu **Ramalan** tidak boleh dilihat pada halaman senarai **Projek**.                                                                                                   |
| Perakaunan projek  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | Tidak dapat membuka **Pernyataan projek**   > **Transaksi dan ramalan**.                                                                                                       |
| Perakaunan projek  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | **Selaraskan perakaunan** tidak didayakan untuk transaksi projek yang diinvois.                                                                                                  |
| Perakaunan projek  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | Butiran perakaunan tidak termasuk dalam jadual **ProjCDSActualsImport** apabila jurnal **Integrasi** disiarkan.                                                  |
| Perakaunan projek  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | Entri ramalan Projek dua kali ganda apabila anda mengalih keluar, kemudian menambah semula penugasan sumber.                                                                            |
| Perakaunan projek  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | Memilih pautan ID Projek tidak membuka URL pautan dalam CDS.                                                                                                         |
| Perakaunan projek  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Tidak dapat mengemas kini tarikh mula pada tugas dalam CDS.                                                                                                                           |
| Perakaunan projek  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Mendayakan ciri, Berbilang baris kontrak tidak mungkin tanpa integrasi CDS.                                                                                   |

### <a name="regulatory-updates"></a>Kemas kini kawal selia
Untuk mendapatkan maklumat tentang kemas kini kawal selia untuk aplikasi Finance and Operations, lihat [Kemas kini kawal selia](/dynamics365/finance/localizations/regulatory-updates). Anda juga boleh mendaftar masuk ke LCS dan melihat kemas kini kawal selia yang dirancang dengan menggunakan alat carian isu. Carian isu membolehkan anda membuat carian mengikut negara, jenis ciri dan keluaran.


[!INCLUDE[footer-include](../includes/footer-banner.md)]