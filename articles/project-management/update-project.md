---
title: Cipta dan kemas kini projek
description: Topik ini menyediakan maklumat tentang mengemas kini projek dalam Project Operations.
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d0847b5343cf3e353b91eae04c94509f14213ba5
ms.sourcegitcommit: 51224cb3bf7cdeae6614d39fc8d899c83dbad5f2
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/23/2021
ms.locfileid: "7678360"
---
# <a name="create-and-update-a-project"></a>Cipta dan kemas kini projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Berikut adalah ringkasan medan yang boleh dikemas kini pada projek selepas ia telah dicipta. Ini juga termasuk sebarang implikasi yang berkaitan berdasarkan kemas kini ini.

## <a name="project-detail-fields"></a>Medan butiran projek

- **Nama**: Tajuk projek.
- **Perihalan** : Gambaran keseluruhan projek.
- **Pelanggan**: Syarikat projek itu akan dihantar kepada.
- **Templat kalendar**: Waktu kerja projek. Apabila medan ditukar, keseluruhan jadual dikira semula.
- **Mata Wang**: Mata wang untuk projek. Nilai lalai bagi medan ini adalah berdasarkan mata wang yang ditakrifkan dalam unit kontrak. Apabila unit kontrak dikemas kini, medan juga dikemas kini.
- **Unit Kontrak**: Unit organisasi yang mewakili kumpulan atau bahagian syarikat yang bertanggungjawab terutamanya untuk memenangi jualan dan menguruskan penyampaian kerja dan perkhidmatan kepada pelanggan.  Apabila unit organisasi Pengurus projek tidak ditakrifkan, medan ini ditetapkan lalai kepada nilai yang ditakrifkan dalam parameter projek.
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



[!INCLUDE[footer-include](../includes/footer-banner.md)]
