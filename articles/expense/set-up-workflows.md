---
title: Sediakan aliran kerja untuk pengurusan Perbelanjaan
description: Anda boleh menyediakan proses aliran kerja yang digunakan untuk menyemak dan meluluskan dokumen perjalanan dan perbelanjaan.
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
ms.openlocfilehash: dfc5945f32bb8d4073fc31499979ba279fef66a4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896562"
---
# <a name="set-up-workflows-for-expense-management"></a>Sediakan aliran kerja untuk pengurusan Perbelanjaan

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Anda boleh menyediakan proses aliran kerja untuk menyemak dan meluluskan dokumen perjalanan dan perbelanjaan. Anda boleh menakrifkan aliran kerja untuk laporan perbelanjaan, permintaan perjalanan dan permintaan pendahuluan tunai.

Aliran kerja mewakili proses perniagaan dan mentakrifkan cara aliran dokumen melalui sistem. Aliran kerja juga menunjukkan siapa yang mesti melengkapkan tugas atau meluluskan dokumen. Terdapat beberapa faedah menggunakan sistem aliran kerja dalam organisasi anda:

- **Proses konsisten**: Anda boleh menakrifkan proses kelulusan untuk dokumen tertentu seperti permintaan pembelian dan laporan perbelanjaan. Menggunakan sistem aliran kerja membantu memastikan dokumen diproses dan diluluskan dengan cara yang konsisten dan berkesan.
- **Keterlihatan proses**: Anda boleh menjejak status, sejarah dan metrik prestasi tika aliran kerja tertentu. Ini membantu anda menentukan sama ada perubahan harus dibuat pada aliran kerja untuk meningkatkan kecekapan.
- **Senarai kerja berpusat**: Pengguna boleh melihat senarai kerja berpusat untuk melihat tugas aliran kerja dan kelulusan yang ditugaskan kepada mereka. 

## <a name="workflow-types"></a>Jenis aliran kerja

Jadual berikut menyenaraikan jenis aliran kerja yang anda boleh cipta dalam **Pengurusan perbelanjaan**.


|              <strong>Jenis</strong>              |                   <strong>Gunakan jenis ini untuk</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Kelulusan automatik laporan perbelanjaan</strong> |            Cipta aliran kerja kelulusan untuk laporan perbelanjaan.             |
|  <strong>siaran automatik laporan perbelanjaan</strong>   |        Cipta aliran kerja siaran automatik untuk laporan perbelanjaan.        |
|       <strong>Item bari perbelanjaan</strong>        |     Cipta aliran kerja kelulusan untuk item baris pada laporan perbelanjaan.      |
| <strong>Siaran automatik item baris perbelanjaan</strong> | Cipta aliran kerja Siaran untuk item baris pada laporan perbelanjaan. |
|       <strong>Permintaan perjalanan</strong>       |          Cipta aliran kelulusan untuk permintaan perjalanan.           |
|      <strong>Permintaan pendahuluan tunai</strong>      |         Cipta aliran kerja kelulusan untuk permintaan pendahuluan tunai.          |
|        <strong>Pemulihan cukai VAT</strong>        | Cipta aliran kerja kelulusan untuk mendapatkan kembali cukai nilai ditambah (VAT).  |
