---
title: Perkara baharu September 2021 - Project Operations untuk senario berasaskan sumber/bukan stok
description: Artikel ini memberikan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran September 2021 Operasi Projek untuk senario berasaskan sumber/tidak berstok.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: c7f764b3e8ee3775167ee57b4f034e383899aea3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923383"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Perkara baharu September 2021 - Project Operations untuk senario berasaskan sumber/bukan stok

*Digunakan Pada: Project Operations untuk senario berdasarkan sumber/tidak distok*

Artikel ini terpakai kepada komponen dan versi berikut Dynamics 365 Project Operations:

   - Project Operations dalam persekitaran Microsoft Dataverse versi 4.14.0.99.
   - Pengurusan projek dan perakaunan dalam persekitaran Dynamics 365 Finance versi 10.0.20.

## <a name="project-operations-dual-write-maps-updates"></a>Kemas kini peta dwi tulis Project Operations

Tiada kemas kini untuk peta dwi tulis Project Operations dalam keluaran ini. Untuk senarai semasa dan versi peta dwi tulis Project Operations, lihat [Versi peta dwi tulis Project Operations](../environment/resource-dual-write-maps.md).

Sentiasa menjalankan versi terkini peta dalam persekitaran anda dan mendayakan semua peta jadual berkaitan ketika anda mengemas kini versi penyelesaian Project Operations Dataverse dan penyelesaian Finance anda. Ciri dan keupayaan tertentu mungkin tidak berfungsi dengan betul jika versi terkini peta tidak diaktifkan. Anda boleh melihat versi aktif peta pada halaman **dwi tulis** dalam lajur **Versi**. Untuk mengaktifkan versi baharu peta, pilih **Versi peta jadual**, pilih versi terkini dan kemudian simpan versi yang dipilih. Jika anda mempunyai peta jadual luar kotak tersuai, mohon semula perubahan. Untuk maklumat lanjut, lihat [Pengurusan kitaran hayat Aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika anda menghadapi isu memulakan peta, ikuti arahan dalam bahagian [Isu kehilangan lajur jadual pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) bagi panduan penyelesaian masalah Dwi Tulis.

## <a name="quality-updates"></a>Kemas kini kualiti

### <a name="project-operations-on-dataverse"></a>Project Operations pada Dataverse

| **Bahagian ciri** | **Nombor rujukan** | **Kemas kini kualiti** |
| --- | --- | --- |
| Masa dan perbelanjaan | 1811407 | Mengubahsuai peranan keselamatan Pelulus Projek untuk kelulusan entri perbelanjaan. |
| Masa dan perbelanjaan | 1811438 | Mengubahsuai peranan keselamatan Pelulus Projek untuk pembatalan kelulusan entri masa. |
| Masa dan perbelanjaan | 2370126 | Kemas kini ikon **Tugas Projek** dan **Peranan** dalam entiti **Entri Masa**. |
| Masa dan perbelanjaan | 2379879 | Betulkan fungsi **Salin Minggu** dalam entri masa apabila menggunakan Dynamics 365 untuk telefon. |
| Pengebilan dan Penentuan Harga | 2371906 | Jumlah proforma invois tidak boleh dilaraskan dalam Project Operations untuk pelaksanaan berasaskan sumber. |
| Pengebilan dan Penentuan Harga | 2385802 | Perbetulkan ralat yang berlaku dengan jam aktual negatif semasa jumlah projek disegar semula. |
| Pengebilan dan Penentuan Harga | 2389675 | Tingkah laku pengesahan invois proforma dipertingkatkan. Entiti kerja jangka panjang mesti mengambil kira aktiviti yang diperlukan untuk menulis hasil pengesahan bagi perakaunan. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Pengurusan projek dan perakaunan di Dynamics 365 Finance

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Perjalanan dan perbelanjaan | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Jumlah pada transaksi vendor dan cukai jualan yang disiarkan daripada perbelanjaan yang dicipta daripada transaksi kad kredit adalah tidak betul. |
| Perjalanan dan perbelanjaan | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Baris penyelesaian yang salah dicipta apabila jurnal pembayaran dijana. |
| Perjalanan dan perbelanjaan | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Jumlah pada transaksi cukai jualan yang disiarkan daripada perbelanjaan yang dicipta daripada transaksi kad kredit adalah tidak betul. |
| Perjalanan dan perbelanjaan | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Memadamkan baris perbelanjaan mungkin mengambil masa yang lama. |
| Perakaunan projek | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Selepas anda menggunakan KB 4619395, mengubah nombor jujukan ke **Berterusan** tidak disokong dan apabila anda menyiarkan anggaran, ralat berikut berlaku, "Persediaan sistem tidak menyokong nombor jujukan Proj_X 'berterusan'." |
| Perakaunan projek | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Menyiarkan invois vendor mungkin gagal dengan mesej ralat berikut, "Transaksi pada baucar tidak seimbang mengikut 5/17/2021. (mata wang perakaunan: 0.00 - mata wang pelaporan: 0.01)." |
