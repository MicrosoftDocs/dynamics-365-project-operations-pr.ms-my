---
title: Aliran kerja Pengurusan perbelanjaan
description: Topik ini menerangkan cara anda boleh menggunakan sistem aliran kerja dalam Microsoft Dynamics 365 Finance, untuk menyediakan proses semakan untuk laporan perbelanjaan dalam Pengurusan perbelanjaan.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5207be92cb58d8ab2658096b3e0f3fc81d73d91e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081383"
---
# <a name="expense-management-workflow"></a>Aliran kerja Pengurusan perbelanjaan

[!include [banner](../includes/banner.md)]

Anda boleh menggunakan sistem aliran kerja untuk menyediakan proses semakan untuk laporan perbelanjaan dalam Pengurusan perbelanjaan. Anda boleh menyediakan aliran kerja yang menggunakan kriteria berikut untuk menentukan orang yang meluluskan laporan perbelanjaan:

- Hierarki pelaporan pekerja dan had kelulusan yang dipratetapkan
- Kelulusan berbilang tahap yang menyokong pelulus interim dan pelulus akhir
- Dimensi kewangan dan tanggungjawab projek
- Penugasan kepada pengguna atau kumpulan pengguna tertentu

Kelulusan aliran kerja boleh dicipta untuk laporan perbelanjaan, permintaan perjalanan, pendahuluan tunai dan pemulihan cukai nilai tambah (VAT).

**Contoh**

Proses berikut ialah contoh aliran kerja pengurusan perbelanjaan untuk laporan perbelanjaan.

1. Pekerja mencipta dan menyimpan laporan perbelanjaan.
2. Pekerja menyerahkan laporan perbelanjaan untuk kelulusan. Pelulus dikenal pasti berdasarkan peraturan yang ditakrifkan apabila aliran kerja disediakan.
3. Pelulus menerima pemberitahuan bahawa laporan perbelanjaan sedia untuk kelulusan. Pelulus menyemak laporan perbelanjaan dan mengesahkan bahawa syarat berikut dipenuhi:

    - Perbelanjaan tidak melanggar apa-apa dasar perbelanjaan. Jika perbelanjaan melanggar dasar, pelulus mengesahkan bahawa laporan perbelanjaan termasuk justifikasi perniagaan yang sah.
    - Resit elektronik dilampirkan pada laporan perbelanjaan.

4. Pelulus meluluskan laporan perbelanjaan.
5. Laporan perbelanjaan ditugaskan kepada penyelaras Akaun belum bayar untuk penyiaran.
6. Salah satu langkah berikut berlaku, bergantung pada sama ada penyiaran automatik dikonfigurasikan:

    - Jika penyiaran automatik dikonfigurasikan, laporan perbelanjaan diproses untuk pembayaran, dan status laporan perbelanjaan dikemas kini.
    - Jika penyiaran automatik tidak dikonfigurasikan, penyelaras Akaun belum bayar mengesahkan bahawa semua resit asal telah diserahkan, dan bahawa resit adalah selaras dengan perbelanjaan pada laporan perbelanjaan. Semua kod cukai yang dimasukkan pada laporan perbelanjaan juga mesti disahkan sebagai betul.

Selepas keperluan ini disahkan, laporan perbelanjaan akan disiarkan.

Selepas laporan perbelanjaan disiarkan, pembayaran dibenarkan untuk laporan perbelanjaan, dan pekerja akan dibayar balik.