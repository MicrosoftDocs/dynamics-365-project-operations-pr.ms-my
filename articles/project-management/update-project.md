---
title: Cipta dan kemas kini projek
description: Artikel ini memberikan maklumat tentang mengemas kini projek Operasi Projek.
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dcb822a726f94a7e8e8621dc7a04f9051168d361
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911101"
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
