---
title: Berbilang pelulus pada laporan perbelanjaan
description: Topik ini menyediakan maklumat tentang laporan perbelanjaan yang memerlukan kelulusan oleh berbilang orang.
author: saraschi2
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c745dda957fab5acc464b9d1c774fcdc783cde40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005262"
---
# <a name="multiple-approvers-on-an-expense-report"></a>Berbilang pelulus pada laporan perbelanjaan

Bergantung pada dasar kelulusan perbelanjaan organisasi anda, lebih daripada satu orang mungkin perlu meluluskan laporan perbelanjaan yang diserahkan oleh pekerja. Apabila anda menyediakan proses aliran kerja untuk kelulusan laporan perbelanjaan, anda boleh menambah elemen aliran kerja yang termasuk tugas atau langkah untuk satu atau lebih laporan pelulus. Contohnya, anda mungkin mengkehendaki semua laporan perbelanjaan diluluskan dahulu oleh pengurus pekerja yang menyerahkan laporan dan kemudian diluluskan oleh Penyelaras akaun belum bayar.

Jika anda memutuskan untuk memerlukan berbilang pelulus laporan perbelanjaan, anda boleh menambah elemen aliran kerja dalam mana-mana cara berikut:

- Tambah satu elemen kelulusan yang mempunyai satu langkah. Contohnya, langkah mungkin memerlukan laporan perbelanjaan ditugaskan kepada kumpulan pengguna dan ia akan diluluskan oleh 50 peratus daripada ahli kumpulan pengguna.
- Tambah satu elemen kelulusan yang mempunyai berbilang langkah. Contohnya, elemen kelulusan mungkin mempunyai langkah berikut:

    1. Pengurus pekerja yang menyerahkan laporan perbelanjaan meluluskannya.
    2. Kerani akaun belum bayar mengesahkan resit dan item laporan perbelanjaan.
    3. Pemilik bajet meluluskan laporan perbelanjaan.

- Tambah berbilang elemen kelulusan, setiap satunya mempunyai satu langkah. Contohnya, anda mungkin menambahkan elemen kelulusan berasingan bagi setiap langkah berikut:

    1. Pengurus pekerja akan meluluskan laporan perbelanjaan.
    2. Pemilik bajet meluluskan laporan perbelanjaan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]