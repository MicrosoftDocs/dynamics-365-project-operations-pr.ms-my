---
title: Kemas kini projek
description: Topik ini menyediakan maklumat tentang mengemas kini projek dalam Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897823"
---
# <a name="update-a-project"></a>Kemas kini projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Di bawah adalah ringkasan medan yang boleh dikemas kini pada projek selepas ia telah dicipta dan sebarang implikasi yang berkenaan dengan kemas kini.

## <a name="project-detail-fields"></a>Medan butiran projek

- **Nama**: Tajuk projek.
- **Perihalan** : Gambaran keseluruhan projek.
- **Pelanggan**: Syarikat projek itu akan dihantar kepada.
- **Templat kalendar**: Waktu kerja projek. Apabila medan ditukar, keseluruhan jadual dikira semula.
- **Mata Wang**: Mata wang untuk projek. Medan lalai ini adalah berdasarkan pada mata wang yang ditakrifkan dalam unit kontrak. Apabila unit kontrak dikemas kini, medan juga dikemas kini.
- **Unit Kontrak**: Unit organisasi yang mewakili kumpulan atau bahagian syarikat yang bertanggungjawab terutamanya untuk memenangi jualan dan menguruskan penyampaian kerja dan perkhidmatan kepada pelanggan. 
- **Pengurus Projek**: Ahli pasukan projek yang mempunyai kuasa untuk menyemak dan meluluskan entri masa dan perbelanjaan.

## <a name="estimate-fields"></a>Anggaran medan

- **Anggaran Tarikh Mula**: Tarikh projek akan bermula. Apabila medan ini dikemas kini, sebarang tugas pada projek akan mengalih secara berkadaran dengan tarikh mula yang baharu.
- **Tarikh Selesai**: Tarikh projek itu dijadualkan untuk berakhir.
- **Usaha**: Anggaran usaha projek. Apabila tugas ditambahkan kepada projek, medan ini tidak boleh diedit lagi.
- **Anggaran Kos Buruh**: Anggaran kos buruh projek. Apabila kos buruh ditambahkan kepada projek, medan ini tidak boleh diedit lagi.
- **Anggaran Perbelanjaan**: Anggaran perbelanjaan projek. Apabila perbelanjaan ditambahkan kepada projek, medan ini tidak boleh diedit lagi.

## <a name="project-actual-fields"></a>Medan sebenar projek
- **Mula Sebenar**: Tarikh projek dimulakan.
- **Selesai Sebenar**: Untuk dikemas kini apabila projek telah selesai.

## <a name="project-status-fields"></a>Medan status projek

- **Status Projek Keseluruhan**: Kesihatan projek secara keseluruhan yang disediakan oleh Pengurus projek.
- **Komen**: Naratif mengenai kesihatan semasa projek yang disediakan oleh Pengurus projek.

