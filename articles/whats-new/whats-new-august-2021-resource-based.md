---
title: Ciri baharu Ogos 2021 - Project Operations untuk senario berdasarkan sumber/bukan stok
description: Artikel ini memberikan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran Project Operations Ogos 2021 untuk senario berasaskan sumber/bukan stok.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: bd91f7f6b3a6f78161f8900aa06c810a58609b53
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912297"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Ciri baharu Ogos 2021 - Project Operations untuk senario berdasarkan sumber/bukan stok

*Digunakan Pada: Project Operations untuk senario berdasarkan sumber/tidak distok*

Artikel ini digunakan pada komponen dan versi Dynamics 365 Project Operations berikut:

   - Project Operations dalam persekitaran Microsoft Dataverse versi 4.13.0.152.
   - Pengurusan projek dan perakaunan dalam persekitaran Dynamics 365 Finance versi 10.0.20.

## <a name="features-included-in-this-release"></a>Ciri yang disertakan dalam keluaran ini

Ciri berikut disertakan dalam keluaran ini:

- **Set kelulusan**: Set kelulusan mengelompokkan permintaan kelulusan masa, perbelanjaan atau bahan bersama sebagai subset operasi yang lebih kecil. Pengelompokan ini membolehkan kelulusan diproses mengikut tertib tertentu mengikut projek dan membolehkan percubaan semula dan penjujukan. Mengelompokkan permintaan meningkatkan kebolehpercayaan dan kebolehjejakan pemprosesan kelulusan untuk jumlah kelulusan yang besar. Untuk mendapatkan maklumat lanjut, lihat [Set kelulusan](../approvals/approval-sets.md).

## <a name="project-operations-dual-write-maps-updates"></a>Kemas kini peta dwi tulis Project Operations

Tiada kemas kini untuk peta dwi tulis Project Operations dalam keluaran ini.

Untuk senarai semasa dan versi peta dwi tulis Project Operations, lihat [Versi peta dwi tulis Project Operations](../environment/resource-dual-write-maps.md).

Sentiasa menjalankan versi terkini peta dalam persekitaran anda dan mendayakan semua peta jadual berkaitan ketika anda mengemas kini versi penyelesaian Project Operations Dataverse dan penyelesaian Finance anda. Ciri dan keupayaan tertentu mungkin tidak berfungsi dengan betul jika versi terkini peta tidak diaktifkan. Anda boleh melihat versi aktif peta pada halaman **dwi tulis** dalam lajur **Versi**. Aktifkan versi baharu peta dengan memilih **Versi peta jadual**, memilih versi terkini dan kemudian menyimpan versi yang dipilih. Jika anda mempunyai peta jadual luar kotak tersuai, mohon semula perubahan. Untuk maklumat lanjut, lihat [Pengurusan kitaran hayat Aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika anda menghadapi isu memulakan peta, ikuti arahan dalam bahagian [Isu lajur jadual yang tidak ditemui pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) dalam Panduan penyelesaian masalah dwi tulis

## <a name="quality-updates"></a>Kemas kini kualiti

### <a name="project-operations-on-dataverse"></a>Project Operations pada Dataverse

| **Bahagian ciri** | **Nombor rujukan** | **Kemas kini kualiti** |
| --- | --- | --- |
| Pengebilan dan harga | 2295625 | Nama pencapaian mesti disalin daripada jadual invois kepada butiran baris invois. |
| Pengebilan dan harga | 2316323 | Diskaun tidak harus diedit pada invois proforma dalam Project Operations untuk senario berasaskan sumber. |
| Pengurusan peluang | 2338619 | Peraturan perniagaan **Peluang** dan **Sebut harga** mesti hanya dipanggil pada halaman. |
| Pengurusan sumber | 2316523 | Menggunakan **Hantar Permintaan** daripada keperluan sumber yang mempunyai peranan dilampirkan tidak sepatutnya memaparkan ralat. |
| Pengurusan sumber | 2326885 | Mencipta keperluan sumber melalui projek tidak sepatutnya memaparkan ralat. |
| Masa dan perbelanjaan | 2335584 | Aliran tugas ditamatkan dalam entri masa. |
| Masa dan perbelanjaan | 2336884 | Butang entri masa **Salin Minggu** mesti berfungsi untuk lebih daripada hanya pengguna semasa. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Pengurusan projek dan perakaunan pada Dynamics 365 Finance

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Perjalanan dan perbelanjaan | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Transaksi vendor dan amaun transaksi cukai jualan yang salah akan disiarkan apabila perbelanjaan dicipta daripada transaksi kad kredit. |
| Perjalanan dan perbelanjaan | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Penyelesaian yang salah ialah baris yang dicipta apabila jurnal pembayaran dijana. |
| Perjalanan dan perbelanjaan | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Amaun transaksi cukai jualan yang salah akan disiarkan apabila perbelanjaan dicipta daripada transaksi kad kredit. |
| Perjalanan dan perbelanjaan | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Memadamkan baris perbelanjaan mungkin mengambil masa yang lama. |
| Perakaunan projek | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Sistem tidak menyokong persediaan penjujukan nombor berterusan apabila anda menyiarkan anggaran selepas menggunakan KB 4619395. |
| Perakaunan projek | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Penyiaran invois vendor mungkin gagal dengan mesej ralat, "Transaksi pada baucar tidak sama baki seperti pada 17/5/2021. (mata wang perakaunan: 0.00 - mata wang pelaporan: 0.01)" |
