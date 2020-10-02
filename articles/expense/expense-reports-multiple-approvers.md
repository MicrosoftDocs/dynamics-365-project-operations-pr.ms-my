---
title: Laporan perbelanjaan dan berbilang pelulus
description: Topik ini menyediakan maklumat tentang laporan perbelanjaan yang memerlukan kelulusan oleh lebih daripada satu orang.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 818092dd631d07cc0a7d63c9eec51eeff4f67ffe
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897102"
---
# <a name="expense-reports-and-multiple-approvers"></a>Laporan perbelanjaan dan berbilang pelulus

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Bergantung pada dasar kelulusan perbelanjaan organisasi anda, lebih daripada satu orang mungkin perlu meluluskan laporan perbelanjaan yang diserahkan. Apabila anda menyediakan proses aliran kerja untuk kelulusan laporan perbelanjaan, anda boleh menambah elemen aliran kerja yang termasuk tugas atau langkah untuk satu atau lebih laporan pelulus. Contohnya, anda mungkin memerlukan semua laporan perbelanjaan yang diluluskan oleh dua orang berasingan, pengurus pekerja yang menyerahkan laporan dan Penyelaras Akaun belum bayar.

Jika anda memutuskan untuk memerlukan berbilang pelulus laporan perbelanjaan, anda boleh menambah elemen aliran kerja dalam mana-mana cara berikut:

- Tambah satu elemen kelulusan yang mempunyai satu langkah. Contohnya, langkah mungkin memerlukan laporan perbelanjaan ditugaskan kepada kumpulan pengguna dan ia akan diluluskan oleh 50 peratus daripada ahli kumpulan pengguna.
- Tambah satu elemen kelulusan yang mempunyai berbilang langkah. Contohnya, elemen kelulusan mungkin mempunyai langkah berikut:

    1. Pengurus pekerja yang menyerahkan laporan perbelanjaan meluluskannya.
    2. Kerani akaun belum bayar mengesahkan resit dan item laporan perbelanjaan.
    3. Pemilik bajet meluluskan laporan perbelanjaan.

- Tambah berbilang elemen kelulusan, setiap satunya mempunyai satu langkah. Contohnya, anda mungkin menambahkan elemen kelulusan berasingan bagi setiap langkah berikut:

    1. Pengurus pekerja akan meluluskan laporan perbelanjaan.
    2. Pemilik bajet meluluskan laporan perbelanjaan.
