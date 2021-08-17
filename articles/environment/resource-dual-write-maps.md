---
title: Versi peta dwi tulis Project Operations
description: Topik ini menyediakan senarai peta dwi tulis yang diperlukan untuk Dynamics 365 Project Operations.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c8bc389c83eaf2a7720ef3fa969c677eed11e7959199b5f0083df5bf3b43ea43
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003827"
---
# <a name="project-operations-dual-write-map-versions"></a>Versi peta dwi tulis Project Operations

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Penggunaan Dynamics 365 Project Operations untuk senario sumber/distok memerlukan set peta dwi tulis untuk berjalan dalam persekitaran. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Peta prasyarat: Penyelesaian pengorkestraan dwi tulis

Peta berikut memerlukan prasyarat untuk penyelesaian Project Operations. Pastikan untuk menjalankan peta yang disenaraikan dalam jadual berikut dan sebarang peta jadual yang berkaitan dalam persekitaran anda.

| Peta jadual | Penyegerakan awal |
| --- | --- |
| Lejar (msdyn_ledgers) | Memerlukan penyegerakan awal untuk peta jadual dan semua prasyarat. Induk untuk penyegerakan awal adalah aplikasi Finance and Operations. |
| Entiti sah (cdm_companies) | Tidak diperlukan. Sistem ini mengisi entiti secara automatik apabila persekitaran dipautkan menggunakan dwi tulis. |
| Pelanggan V3 (akaun) | Tidak diperlukan untuk peruntukan. |
| Vendor V2 (msdyn_vendors) | Tidak diperlukan untuk peruntukan. |

1. Daripada senarai peta, pilih peta Lejar **(msdyn\_ledgers)** dengan semua prasyarat dan pilih kotak semak **Initial sync**. Dalam medan **Induk untuk penyegerakan awal**, pilih aplikasi **Finance and Operations** untuk kedua-dua peta lejar dan semua peta prasyarat. Pilih **Jalankan**.

![Penyegerakan peta lejar.](media/DW6.png)

2. Ikuti langkah yang sama untuk semua baki peta jadual yang disenaraikan dalam jadual di atas. Jangan pilih kotak semak **Penyegerakan awal** apabila menjalankan peta itu.

## <a name="project-operations-dual-write-maps"></a>Peta dwi tulis Project Operations

Peta berikut diperlukan untuk penyelesaian Project Operations. Versi peta dwitulis berdaftar bermula dengan Project Operations kemas kini Mei 2021, versi 4.10.0.186.

| **Peta entiti** | **Versi terkini** | **Penyegerakan awal** |
| --- | --- | --- |
| Entiti integrasi untuk perhubungan transaksi projek (msdyn\_transactionconnections) | 1.0.0.0 | Tidak diperlukan untuk peruntukan. |
| Pengepala kontrak projek (pesanan jualan) | 1.0.0.1 | Tidak diperlukan untuk peruntukan. |
| Baris kontrak projek (salesorderdetails) | 1.0.0.0 | Tidak diperlukan untuk peruntukan. |
| Sumber pembiayaan projek (msdyn_projectcontractsplitbillingrules) | 1.0.0.2 | Tidak diperlukan untuk peruntukan. |
| Jadual integrasi Project Operations untuk anggaran bahan (msdyn\_estimatelines) | 1.0.0.0 | Tidak diperlukan untuk peruntukan. |
| Cadangan invois projek V2 (invois) | 1.0.0.3 | Tidak diperlukan untuk peruntukan. |
| Aktual integrasi Project Operations (msdyn_actuals) | 1.0.0.14 | Tidak diperlukan untuk peruntukan. |
| Pencapaian baris kontrak integrasi Project Operations (msdyn_contractlinesscheduleofvalues) | 1.0.0.4 | Tidak diperlukan untuk peruntukan. |
| Entiti integrasi Project Operations untuk anggaran perbelanjaan (msdyn_estimateslines) | 1.0.0.2 | Tidak diperlukan untuk peruntukan. |
| Entiti integrasi Project Operations untuk anggaran jam (msdyn_resourceassignments) | 1.0.0.5 | Tidak diperlukan untuk peruntukan. |
| Entiti eksport kategori perbelanjaan projek integrasi Project Operations (msdyn_expensecategories) | 1.0.0.1 | Tidak diperlukan untuk peruntukan. |
| Entiti eksport perbelanjaan projek integrasi Project Operations (msdyn_expenses) | 1.0.0.2 | Tidak diperlukan untuk peruntukan. |
| Entiti eksport invois projek integrasi Project Operations (msdyn_projectvendorinvoices) | 1.0.0.0 | Tidak diperlukan untuk peruntukan. |
| Entiti eksport baris invois vendor projek integrasi Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.1 | Tidak diperlukan untuk peruntukan. |
| Peranan sumber projek untuk semua syarikat (bookableresourcecategories) | 1.0.0.1 | Memerlukan penyegerakan awal untuk peta jadual menyegerakkan peranan Pengurus Projek dan sumber ahli Pasukan yang diisi dalam persekitaran Dynamics 365 Dataverse semasa peruntukan. Dataverse ialah sumber utama untuk penyegerakan awal. |
| Tugas projek (msdyn_projecttasks) | 1.0.0.4 | Tidak diperlukan untuk peruntukan. |
| Kategori transaksi projek (msdyn_transactioncategories) | 1.0.0.0 | Tidak diperlukan untuk peruntukan. |
| Projek V2 (msdyn_projects) | 1.0.0.2 | Tidak diperlukan untuk peruntukan. |

Lengkapkan langkah berikut untuk menjalankan peta yang disenaraikan.

1. Dayakan peranan sumber Projek untuk peta jadual **semua syarikat (bookableresourcecategories)** kerana peta ini memerlukan penyegerakan awal. Dalam medan **Induk untuk penyegerakan awal**, pilih **Common Data Service**. 

 ![Penyegerakan peta jadual peranan sumber.](media/6ResourceInitialSync.jpg)

 Tunggu sehingga status peta adalah **Berjalan** sebelum anda berpindah ke langkah seterusnya.

2. Pilih semua baki peta yang diperlukan. Anda boleh menapis mereka dalam senarai peta dwi tulis menggunakan kata kunci, **Projek** dalam carian di sudut kanan atas. Anda boleh berbilang pilih semua peta dan kemudian jalankan. Untuk maklumat lanjut, lihat [Urus berbilang peta jadual](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Pastikan juga untuk mendaya dan menjalankan peta entiti yang berkaitan.

### <a name="project-operations-dual-write-map-versions"></a>Versi peta dwi tulis Project Operations

Sentiasa jalankan versi terkini peta dalam persekitaran anda. Ciri dan keupayaan tertentu mungkin tidak berfungsi dengan betul jika mana-mana syarat berikut wujud:

- Peta tidak diaktifkan.
- Peta versi terkini tidak diaktifkan. 
- Peta jadual yang berkaitan tidak diaktifkan.

Anda boleh melihat versi aktif peta dalam lajur **Versi** pada halaman **Dwi tulis**. Anda boleh mengaktifkan versi baharu peta dengan memilih **Versi peta jadual**, memilih versi terkini dan kemudian menyimpan versi yang dipilih. Jika anda telah menyesuaikan peta jadual di luar kotak, anda akan perlu memohon semula perubahan. Untuk maklumat lanjut, lihat [Pengurusan kitaran hayat Aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).
