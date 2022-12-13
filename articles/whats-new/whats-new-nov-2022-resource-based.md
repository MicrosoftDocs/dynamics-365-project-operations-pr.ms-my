---
title: Perkara baharu November 2022 - Project Operations untuk senario berasaskan sumber/bukan stok
description: Artikel ini menyediakan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran Microsoft Dynamics 365 Project Operations pada November 2022 untuk senario berasaskan sumber/bukan stok.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831137"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Perkara baharu November 2022 - Project Operations untuk senario berasaskan sumber/bukan stok

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Artikel ini digunakan pada komponen dan versi Microsoft Dynamics 365 Project Operations berikut:

- Project Operations dalam persekitaran Dataverse versi 4.58.0.119
- Pengurusan projek dan perakaunan dalam persekitaran Dynamics 365 Finance versi 10.0.30

## <a name="project-operations-dual-write-maps-updates"></a>Kemas kini peta dwi tulis Project Operations

Tiada kemas kini untuk peta dwi tulis Project Operations dalam keluaran ini. Untuk senarai semasa dan versi peta dwi tulis Project Operations, lihat [Versi peta dwi tulis Project Operations](../environment/resource-dual-write-maps.md).

Sentiasa menjalankan versi terkini peta dalam persekitaran anda dan mendayakan semua peta jadual berkaitan ketika anda mengemas kini versi penyelesaian Project Operations Dataverse dan penyelesaian Finance anda. Sesetengah ciri dan keupayaan mungkin tidak berfungsi dengan betul jika versi terkini peta tidak diaktifkan. Anda boleh melihat versi aktif peta dalam lajur **Versi** pada halaman **Dwi tulis**. Untuk mengaktifkan versi baharu peta dengan, pilih **Versi peta jadual**, pilih versi terkini dan kemudian simpan versi yang dipilih. Jika anda sudah mempunyai peta jadual luar kotak tersuai, mohon semula perubahan. Untuk maklumat lanjut, lihat [Pengurusan kitaran hayat Aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika anda mengalami isu semasa anda memulakan peta, ikut arahan dalam bahagian [Isu lajur jadual yang hilang pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) bagi panduan penyelesaian masalah Dwi tulis.

## <a name="quality-updates"></a>Kemas kini kualiti

### <a name="project-operations-on-dataverse"></a>Project Operations pada Dataverse

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Pengebilan dan Penentuan Harga | 2781818 | Kunci tidak menemui ralat semasa lalai harga untuk log penggunaan bahan. |
| Pengebilan dan Penentuan Harga | 2922373 | Tidak dapat memautkan baris sebut harga ke projek yang telah ditutup sebagai sebut harga yang hilang. |
| Pengebilan dan Penentuan Harga | 2943206 | **Bidang Talian** Kontrak dalam Entiti Projek Harus Pilihan. |
| Pengebilan dan Penentuan Harga | 2953182 | Tingkatkan mesej ralat untuk invois pembetulan.|
| Pengebilan dan Penentuan Harga | 2959500 | Tidak dapat memautkan baris sebut harga ke tugas projek yang telah dikaitkan dengan sebut harga yang hilang.|
| Pengebilan dan Penentuan Harga | 2959560 | Mesej "Pelanggan ini sudah berada dalam Kontrak Projek" yang diterima semasa menutup sebut harga seperti yang dimenangi di kawasan tertentu. |
| Pengebilan dan Penentuan Harga | 3031727 | Tugasan sumber gagal dengan medan Diperlukan 'msdyn_Company' hilang ralat. |
| Pengebilan dan Penentuan Harga | 3036905 | Memiliki Syarikat tidak pernah dimulakan pada ProjectTeamMember. |
| Pengurusan Peluang | 2763519 | Ralat Rujukan Nol dalam EnsureProjectContractAllowsUpdates. |
| Pengurusan Peluang | 2783798 | Apabila mengimport anggaran projek pada baris sebut harga, perihalan tugas hilang untuk anggaran perbelanjaan dan bahan.|
| Pengurusan Peluang | 2988635 | Meningkatkan ralat msg penerangan apabila memadam Pelanggan pada Sebut Harga. |
| Pengurusan Peluang | 3001191 | Tidak dapat mencipta sebut harga daripada Peluang di mana kaedah pengebilan ditentukan sebagai batal. |
| Naik taraf | 3012324 | Penukaran projek gagal pada projek dengan aksara kawalan seperti Tab dalam namanya. || Perancangan dan Penjejakan Projek | 2790384 | Masa keluar Pending OperationSet terlalu pendek. |
| Perancangan dan Penjejakan Projek | 3044275 | Penyetempatan yang hilang untuk: missingProjectSchedulerErrorMessage. |
| Perancangan dan Penjejakan Projek | 3044277 | Project Recon grid tidak dimuatkan apabila penjadual tidak ditetapkan.|
| Pengurusan Sumber | 2943153 | Kemas kini tab Penjejakan untuk menunjukkan dua tempat perpuluhan untuk Tempoh.|
| Pemberian subkontrak | 2932774 | Talian Invois Vendor Baca Hanya membuang ralat dengan tidak betul. |
| Pemberian subkontrak | 2939556 | Status Pengepala Invois Vendor tidak boleh ditetapkan kepada Draf pemadaman dalam talian jika tidak aktif. |
| Masa dan Perbelanjaan | 2939998 | Ambil versi TESA baru dalam ProjOps. |


### <a name="project-management-and-accounting-in-finance"></a>Pengurusan projek dan perakaunan dalam Kewangan

Untuk maklumat tentang pembetulan pepijat yang termasuk dalam kemas kini ini, daftar masuk ke Microsoft Dynamics Lifecycle Services, dan lihat [artikel KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).