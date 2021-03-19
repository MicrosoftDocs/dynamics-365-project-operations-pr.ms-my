---
title: Keperluan tempah lembut
description: Topik ini memberikan maklumat tentang cara untuk memenuhi keperluan tempahan lembut.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 736d59976ad0f456a694cedbb28b516c90632fe6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282929"
---
# <a name="soft-book-requirements"></a>Keperluan tempah lembut

[!include [banner](../includes/psa-now-project-operations.md)]

Keperluan sumber boleh ditempah cetak. Penempahan cetak mencipta cadangan yang menggunakan kapasiti sumber. Cadangan kemudiannya dihantar kembali ke peminta untuk kelulusan. Penempahan lembut secara tentatif menambah sumber kepada pasukan projek dan mempunyai status berbeza pada Papan Jadual tetapi ia tidak mengambil kapasiti sumber. Untuk membuat pilihan lembut sumber daripada Papan Jadual, tetapkan medan **Status Tempahan** kepada **Lembut**.

![Status Penempahan ditetapkan kepada Lembut](media/Resource-Management-image77.png)

Apabila tab **Pasukan** berada dalam pandangan **Ahli Pasukan Dinamakan**, sumber muncul di sana. Waktu yang ditempah lembut dilaporkan dalam lajur **Jam yang Ditempah Lembut**.

![Jam yang ditempah lembut dalam pandangan Ahli Pasukan Dinamakan](media/Resource-Management-image78.png)

Ahli pasukan ditempah lembut boleh ditugaskan kepada tugas.

![Ahli pasukan ditempah lembut boleh ditugaskan kepada satu tugas.](media/Resource-Management-image79.png)

Pada tab **Penyesuaian**, tiada tempahan ditunjukkan untuk sumber tempahan lembut, kerana tab **Penyesuaian** yang menganggap hanya tempahan cetak.

![Sumber tempahan lembut tanpa sebarang tempahan pada tab Penyesuaian](media/Resource-Management-image80.png)

> [!NOTE]
> Anda tidak boleh menempah lembut sumber daripada keperluan yang telah dijana daripada ahli pasukan generik.

Pada Papan Jadual, pewarna yang berbeza digunakan untuk tempahan lembut untuk sumber.

![Tempah lembut pada Papan Jadual](media/Resource-Management-image81.png)

Untuk menukar Tempahan lembut kepada penempahan keras, pada papan Jadual, klik kanan dengan tempahan lembut dan kemudian pilih **Ubah status** \> **Tempahan Cetak** \> **Cetak**.

![Mengubah status penempahan kepada Cetak](media/Resource-Management-image82.png)

Penempahan ditukar dan status ditukar pada Papan Jadual. Oleh kerana status penempahan kini **Cetak**, sumber ditunjukkan sebagai telah ditempah dan keupayaan dan ketersediaan akan dilaraskan.

Anda boleh menggunakan kaedah yang sama untuk membatalkan tempahan cetak atau membuat tempahan lembut daripada Papan Jadual.

Untuk menukar sumber yang lembut ditempah untuk ditempah keras pada tab **Pasukan** projek, pilih sumber dan kemudian pilih **Sahkan**.

![Sahkan perintah](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]