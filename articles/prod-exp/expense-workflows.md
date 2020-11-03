---
title: Sediakan aliran kerja Pengurusan perbelanjaan
description: Anda boleh menyediakan proses aliran kerja untuk menyemak dan meluluskan dokumen perjalanan dan perbelanjaan.
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
ms.openlocfilehash: 0af23ed2cf172e4c90de72f5db389c349303c039
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081382"
---
# <a name="set-up-expense-management-workflows"></a>Sediakan aliran kerja Pengurusan perbelanjaan

[!include [banner](../includes/banner.md)]

Anda boleh menyediakan proses aliran kerja yang digunakan untuk menyemak dan meluluskan dokumen perjalanan dan perbelanjaan. Dokumen yang aliran kerja boleh ditakrifkan termasuk laporan perbelanjaan, permintaan perjalanan dan permintaan pendahuluan tunai.

Aliran kerja mewakili proses perniagaan. Ia menentukan cara dokumen dialirkan melalui sistem dan menandakan orang yang harus melengkapkan tugas atau meluluskan dokumen. Terdapat beberapa faedah menggunakan sistem aliran kerja dalam organisasi anda:

-   **Proses konsisten** : — Anda boleh menentukan proses kelulusan untuk dokumen tertentu seperti permintaan pembelian dan laporan perbelanjaan. Menggunakan sistem aliran kerja membantu anda memastikan dokumen diproses dan diluluskan dengan cara yang konsisten dan berkesan.

-   Keterlihatan proses: — Anda boleh menjejak status, sejarah dan metrik prestasi tika aliran kerja tertentu. Ini membantu anda menentukan sama ada perubahan harus dibuat pada aliran kerja untuk meningkatkan kecekapan.

-   Senarai kerja terpusat: — Pengguna boleh melihat senarai kerja terpusat untuk melihat tugas aliran kerja dan kelulusan yang ditugaskan kepada mereka. 

**Jenis aliran kerja yang boleh anda cipta**

Jadual berikut menyenaraikan jenis aliran kerja yang boleh anda cipta dalam **Perbelanjaan**.


|              <strong>Jenis</strong>              |                   <strong>Gunakan jenis ini untuk</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <strong>Laporan perbelanjaan</strong>         |            Cipta aliran kerja kelulusan untuk laporan perbelanjaan.             |
|  <strong>siaran automatik laporan perbelanjaan</strong>   |        Cipta aliran kerja siaran automatik untuk laporan perbelanjaan.        |
|       <strong>Item bari perbelanjaan</strong>        |     Cipta aliran kerja kelulusan untuk item baris pada laporan perbelanjaan.      |
| <strong>Siaran automatik item baris perbelanjaan</strong> | Cipta aliran kerja Siaran untuk item baris pada laporan perbelanjaan. |
|       <strong>Permintaan perjalanan</strong>       |          Cipta aliran kelulusan untuk permintaan perjalanan.           |
|      <strong>Permintaan pendahuluan tunai</strong>      |         Cipta aliran kerja kelulusan untuk permintaan pendahuluan tunai.          |
|        <strong>Pemulihan cukai VAT</strong>        | Cipta aliran kerja kelulusan untuk mendapatkan kembali cukai nilai ditambah (VAT).  |
