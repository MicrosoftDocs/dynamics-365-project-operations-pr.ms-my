---
title: Aliran kerja Pengurusan perbelanjaan
description: Topik ini menerangkan cara anda boleh menggunakan sistem aliran kerja dalam Microsoft Dynamics 365 Finance, untuk menyediakan proses semakan untuk laporan perbelanjaan dalam Pengurusan perbelanjaan.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c2a2cae435342139f32d1bb5d38d68acd920453f5e6f6551e1f6d57967d8053
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001307"
---
# <a name="expense-management-workflow"></a>Aliran kerja Pengurusan perbelanjaan

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]