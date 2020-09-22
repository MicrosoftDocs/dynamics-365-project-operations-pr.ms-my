---
title: Tempah sumber nama daripada keperluan sumber.
description: Topik ini memberikan maklumat tentang menempah sumber bernama untuk keperluan sumber generik.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 83ac2056-313e-4f90-8297-238fd4d25ef9
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: eab280cd1a670cc2a6ed0ae02cde7ba9bf7d601d
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753867"
---
# <a name="book-named-resources-from-resource-requirements"></a>Tempah sumber nama daripada keperluan sumber.

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Anda boleh menempah sumber bernama untuk menggantikan sumber generik yang mempunyai keperluan sumber.

1. Dalam Project Service Automation (PSA), pada halaman **Projek**, klik tab **Pasukan**.
2. Pilih sumber generik yang mempunyai keperluan sumber daripada senarai dan kemudian klik **Tempah**. Atau, buka keperluan sumber dan kemudian klik **Tempah**.


![Menempah ahli pasukan generik](media/RM-how-to-14.png)


3. Pada halaman **Pembantu Jadual**, pilih sumber bernama untuk menempah ke dalam pasukan projek anda dan kemudian klik**Tempah**.

![Menempah ahli pasukan generik menggunakan pembantu jadual](media/RM-how-to-15.png)

Apabila tempahan selesai dan diisi dengan sumber bernama, sumber generik digantikan dengan sumber bernama.

![Ahli pasukan bernama menggantikan ahli pasukan generik](media/RM-how-to-16.png)

Tugasan ke atas jadual dikemas kini dengan sumber bernama juga.

![Ahli pasukan bernama ditugaskan kepada tugas projek](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Isi sumber generik dengan berbilang sumber bernama
Mengisi keperluan untuk sumber generik dengan berbilang sumber bernama adalah serupa dengan menugaskan sumber bernama tunggal. Contohnya, terdapat tugas yang mempunyai tempoh lima hari dan 120 jam usaha. Tugas ini tidak boleh diselesaikan oleh satu sumber yang bekerja 8 jam sehari selama lima hari seminggu yang biasa. 

![Tugas yang memerlukan 120 jam usaha selama lima hari](media/RM-how-to-21.png)

Keperluan adalah untuk 120 jam bagi kejuruteraan robotik selama lima hari, yang mana 24 jam sehari.

![Keperluan setiap hari](media/RM-how-to-22.png)

Ini adalah contoh ketika sumber berbilang diperlukan untuk mengisi permintaan sumber generik. Anda perlu menempah berbilang sumber untuk mengisi keperluan.

![Menempah berbilang sumber untuk mengisi keperluan](media/RM-how-to-23.png)

Perbezaan utama dalam senario ini ialah bahawa sumber generik kekal dalam pasukan yang ditugaskan kepada tugas, dan ahli pasukan sumber bernama yang ditempah tidak ditugaskan sebagai sebahagian daripada kedudukan tersebut. Pengurus projek boleh menugaskan kerja sebagai sesuai kepada sumber bernama. Pandangan **Penyesuaian** boleh membantu pengurus projek dalam memecahkan tempahan di semua berbilang sumber untuk menugaskan tugasan. Ini tidak dilakukan secara automatik kerana dalam mana-mana senario yang lebih rumit daripada contoh mudah di atas, seperti di mana anda mempunyai tugas yang memenuhi keperluan, niat tentang cara pengurus projek mahu menugaskan, perlu disangka oleh sistem. Disebabkan sistem tidak boleh memahami niat, peluang adalah bahawa sangkaan akan berbeza daripada yang diniatkan, dan hasil yang tidak betul atau tidak dijangka akan berlaku. Hasil yang boleh dijangka ialah sumber generik kekal ditugaskan sehingga pengurus projek secara sengaja mencipta tugasan, dengan bantuan pandangan **Penyesuaian**.


