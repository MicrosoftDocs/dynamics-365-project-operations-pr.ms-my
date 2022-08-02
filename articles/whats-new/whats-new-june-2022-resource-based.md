---
title: Ciri baharu Jun 2022 - Project Operations untuk senario berdasarkan sumber/tidak distok
description: Artikel ini menyediakan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran Jun 2022 Microsoft Dynamics 365 Project Operations untuk senario berasaskan sumber/bukan stok.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32bc7793c5a0ee8c04272d3ffcbd290b39fce4cc
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031342"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Ciri baharu Jun 2022 - Project Operations untuk senario berdasarkan sumber/tidak distok

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Artikel ini terpakai kepada komponen dan versi Microsoft Dynamics 365 Project Operations berikut :

- Operasi Projek dalam versi persekitaran yang Dataverse 4.43.0.77 atau 4.43.0.119
- Pengurusan projek dan perakaunan dalam persekitaran Dynamics 365 Finance versi 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Kemas kini peta dwi tulis Project Operations

Jadual berikut menunjukkan peta dwi-tulis yang telah diubah suai atau ditambah dalam keluaran Operasi Projek Jun 2022.

| Peta entiti | Versi dikemas kini | Komen |
| --- | --- | --- |
| Entiti eksport invois projek integrasi Project Operations (msdyn_projectvendorinvoices) | 1.0.0.1 | Tamat medan legasi dan dipetakan ke medan baharu untuk penjejakan keadaan invois vendor. |

Sentiasa jalankan versi terkini peta dalam persekitaran anda dan dayakan semua peta jadual yang berkaitan semasa anda mengemas kini penyelesaian Operasi Dataverse Projek dan versi penyelesaian Kewangan anda. Sesetengah ciri dan keupayaan mungkin tidak berfungsi dengan betul jika versi terkini peta tidak diaktifkan. Anda boleh melihat versi aktif peta dalam lajur **Versi** pada halaman **Dwi tulis**. Untuk mengaktifkan versi baharu peta dengan, pilih **Versi peta jadual**, pilih versi terkini dan kemudian simpan versi yang dipilih. Jika anda telah menyesuaikan peta jadual di luar kotak, gunakan semula perubahan. Untuk maklumat lanjut, lihat [Pengurusan kitaran hayat Aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika anda menghadapi isu apabila anda memulakan peta, ikut arahan dalam [isu lajur jadual hilang pada bahagian peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) panduan penyelesaian masalah Dwi-tulis.

## <a name="quality-updates"></a>Kemas kini kualiti

### <a name="project-operations-on-dataverse"></a>Project Operations pada Dataverse

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Subkontrak | 2708885 | Membaiki mesej ralat yang muncul apabila pengguna mencipta rekod pengepala tempahan sumber boleh ditempah di mana tiada sumber boleh ditempah diisi. |
| Perancangan dan penjejakan projek | 2629441 | Membetulkan aliran kerja yang mencetuskan logik untuk membantu menghalang gelung tak terhingga apabila tugas projek dikemas kini. |
| Masa dan perbelanjaan | 2641209 | Import kemasukan masa daripada tugasan/tempahan mesti mengekalkan rujukan sumber yang boleh ditempah. |
| Perancangan dan penjejakan projek | 2651148 | Pengepala dokumen projek mesti dijaga.|
| Perancangan dan penjejakan projek | 2653145 | Pengesahan tambahan untuk memastikan rekod projek tidak dapat dicipta yang mempunyai aksara tidak sah dalam namanya. |
| Masa dan perbelanjaan | 2654710 | Membetulkan penapisan pada **halaman Kelulusan**. |
| Pengebilan dan harga | 2667805 | Pengesahan tambahan untuk membantu mengelakkan sebenar jualan yang dibilkan daripada dicipta jika menyokong sebenar jualan yang tidak dibilkan tidak wujud. |
| Pengebilan dan harga | 2668378 | Pengesahan tambahan untuk membantu mengelakkan dimensi harga tersuai daripada ditambah melainkan nama logik dan nama medan diisi. |
| Subkontrak | 2677485 | Mengemas kini versi sasaran peta dwi-tulis baris invois vendor. |
| Masa dan perbelanjaan | 2700428 | Meningkatkan logik kelulusan untuk memastikan bahawa set kelulusan lain untuk projek dapat diproses walaupun salah satu set kelulusan tersekat dalam pekerjaan sistem. |

### <a name="project-management-and-accounting-in-finance"></a>Pengurusan projek dan perakaunan dalam Kewangan

Untuk maklumat tentang pembetulan pepijat yang disertakan dalam kemas kini ini, log masuk ke Microsoft Dynamics Perkhidmatan Kitaran Hayat (LCS) dan lihat [artikel KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
