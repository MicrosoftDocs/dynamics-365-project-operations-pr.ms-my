---
title: Perkara baharu Mei 2022 - Project Operations untuk senario berdasarkan sumber/bukan stok
description: Artikel ini menyediakan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran Mei 2022 Microsoft Dynamics 365 Project Operations untuk senario berasaskan sumber/bukan stok.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: beb75fc4b721d52cddbdaf2d20194218cefced5e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921405"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Perkara baharu Mei 2022 - Project Operations untuk senario berdasarkan sumber/bukan stok

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Artikel ini terpakai kepada komponen dan versi Microsoft Dynamics 365 Project Operations berikut :

- Operasi Projek dalam versi persekitaran 4.42.0.70 Dataverse
- Pengurusan projek dan perakaunan dalam persekitaran Dynamics 365 Finance versi 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>Kemas kini peta dwi tulis Project Operations

Tiada kemas kini untuk peta dwi tulis Project Operations dalam keluaran ini. Untuk senarai semasa dan versi peta dwi tulis Project Operations, lihat [Versi peta dwi tulis Project Operations](../environment/resource-dual-write-maps.md).

Sentiasa jalankan versi terkini peta dalam persekitaran anda dan dayakan semua peta jadual yang berkaitan semasa anda mengemas kini penyelesaian Operasi Dataverse Projek dan versi penyelesaian Kewangan anda. Sesetengah ciri dan keupayaan mungkin tidak berfungsi dengan betul jika versi terkini peta tidak diaktifkan. Anda boleh melihat versi aktif peta dalam lajur **Versi** pada halaman **Dwi tulis**. Untuk mengaktifkan versi baharu peta dengan, pilih **Versi peta jadual**, pilih versi terkini dan kemudian simpan versi yang dipilih. Jika anda telah menyesuaikan peta jadual di luar kotak, gunakan semula perubahan. Untuk maklumat lanjut, lihat [Pengurusan kitaran hayat Aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika anda menghadapi isu apabila anda memulakan peta, ikut arahan dalam [isu lajur jadual hilang pada bahagian peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) panduan penyelesaian masalah Dwi-tulis.

## <a name="quality-updates"></a>Kemas kini kualiti
### <a name="project-operations-on-dataverse"></a>Project Operations pada Dataverse

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Pengurusan sumber | 2634019 | Mesej ralat yang dipertingkatkan untuk pengesahan perniagaan apabila menambah ahli pasukan generik sebagai sumber. |
| Perancangan dan penjejakan projek | 2648515 | Kemas kini **terhad id pemilik**, **keadaan**, dan **status** dalam entiti penjadualan. |
| Pengebilan dan harga | 2653167 | Pemisah **perpuluhan grid Anggaran** mesti mengikut seting format dalam **Opsyen** Peribadi. |
| Pengebilan dan harga| 2662251 | Nilai dalam **unit** yang diperbetulkan dan **medan kumpulan** Unit lalai apabila mencipta rekod dalam anggaran bahan. |
| Pengebilan dan harga| 2571408 | Sebenar jualan yang tidak dibilkan dicop dengan ID invois proforma semasa membuat invois draf. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Pengurusan projek dan perakaunan di Dynamics 365 Finance

Untuk maklumat tentang pembetulan pepijat yang disertakan dalam kemas kini ini, log masuk ke Microsoft Dynamics Perkhidmatan Kitaran Hayat (LCS) dan lihat [artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864) KB.
