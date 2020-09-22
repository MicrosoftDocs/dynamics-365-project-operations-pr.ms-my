---
title: Keperluan tempah lembut
description: Topik ini memberikan maklumat tentang cara untuk memenuhi keperluan tempahan lembut.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 97323b73-c6de-4a7f-b889-19d4c42cf17a
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 08a8b46ee03fb93b30d178756e38c3086880f774
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753983"
---
# <a name="soft-book-requirements"></a>Keperluan tempah lembut

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
