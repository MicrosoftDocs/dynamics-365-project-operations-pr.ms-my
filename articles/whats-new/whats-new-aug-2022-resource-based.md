---
title: Ciri baharu Ogos 2022 - Project Operations untuk senario berdasarkan sumber/bukan stok
description: Artikel ini menyediakan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran Ogos 2022 Microsoft Dynamics 365 Project Operations untuk senario berasaskan sumber/bukan stok.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 4042dca72a33f48e04e51af2a3cfd2da83146afd
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403868"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Ciri baharu Ogos 2022 - Project Operations untuk senario berdasarkan sumber/bukan stok

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Artikel ini digunakan pada komponen dan versi Microsoft Dynamics 365 Project Operations berikut :

- Operasi Projek dalam Dataverse versi persekitaran 4.45.0.53
- Pengurusan projek dan perakaunan dalam persekitaran Dynamics 365 Finance versi 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Kemas kini peta dwi tulis Project Operations

Tiada kemas kini untuk peta dwi tulis Project Operations dalam keluaran ini. Untuk senarai semasa dan versi peta dwi tulis Project Operations, lihat [Versi peta dwi tulis Project Operations](../environment/resource-dual-write-maps.md).

Sentiasa jalankan versi terkini peta dalam persekitaran anda dan dayakan semua peta jadual yang berkaitan semasa anda mengemas kini penyelesaian Operasi Dataverse Projek dan versi penyelesaian Kewangan anda. Sesetengah ciri dan keupayaan mungkin tidak berfungsi dengan betul jika versi terkini peta tidak diaktifkan. Anda boleh melihat versi aktif peta dalam lajur **Versi** pada halaman **Dwi tulis**. Untuk mengaktifkan versi baharu peta dengan, pilih **Versi peta jadual**, pilih versi terkini dan kemudian simpan versi yang dipilih. Jika anda telah menyesuaikan peta jadual luar kotak, gunakan semula perubahan. Untuk maklumat lanjut, lihat [Pengurusan kitaran hayat Aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika anda menghadapi isu apabila anda memulakan peta, ikuti arahan dalam [seksyen Isu lajur jadual hilang pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) pada panduan Penyelesaian Masalah dwi-tulis.

## <a name="quality-updates"></a>Kemas kini kualiti

### <a name="project-operations-on-dataverse"></a>Project Operations pada Dataverse

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Pengurusan peluang | 2762089 | Pengendalian ralat semasa menutup kontrak sebagai hilang jika simpanan automatik dinyahdayakan dalam organisasi.|
|Perancangan dan Penjejakan Projek | 2767841 | Telemetri mengemas kini entiti Project Mencipta atau Mengemas Kini senario.|
|Pengebilan dan Penentuan Harga | 2771072 | Pengendalian pengecualian rujukan nol semasa memenangi sebut harga.|
|Pengebilan dan Penentuan Harga | 2844181 |Kegagalan mendapatkan id korelasi dan menyekat penciptaan invois.|
|Pengebilan dan Penentuan Harga | 2852836 | Intercompany sebenarnya hilang untuk Perbelanjaan Intercompany dicipta dan diluluskan dalam CE.|


### <a name="project-management-and-accounting-in-finance"></a>Pengurusan projek dan perakaunan dalam Kewangan

Untuk maklumat tentang pembetulan pepijat yang disertakan dalam kemas kini ini, log masuk ke Microsoft Dynamics Perkhidmatan Kitaran Hayat (LCS) dan lihat [artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438) KB.
