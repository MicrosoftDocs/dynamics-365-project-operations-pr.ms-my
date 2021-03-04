---
title: Tempahan sumber dan kaitannya dengan tugasan tugas
description: Topik ini memberikan maklumat tentang cara mengurus sumber bernama, tempahan sumber dan tugasan tugas dan kaitannya antara satu sama lain.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 0e4eea87bfb059a3c0be8ccbd2914a4d6c3cf46b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149959"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>Tempahan sumber dan kaitannya dengan tugasan tugas

[!include [banner](../includes/psa-now-project-operations.md)]

Terdapat dua cara sumber bernama boleh ditempah pada pasukan projek dan tugas projek yang ditugaskan:

- Sumber boleh ditempah secara terus ke dalam projek, kemudian ditugaskan kepada tugas projek.
- Tugas boleh ditugaskan kepada sumber generika yang kemudiannya digunakan untuk mencari dan menggantikan generik dengan sumber bernama. 

Dalam kedua-dua kes, tindakan menempah sumber itu menyimpan kapasiti sumber tersebut.

Pengurus projek yang merancang projek memiliki rancangan projek dan jadual. Dengan menggunakan sumber generik untuk tugasan dan kemudian menjana permintaan sumber daripadanya, pengurus projek boleh menempah sumber ke dalam projek dengan kontur dikhususkan dalam rancangan projek. Mereka boleh menempah sumber kepada projek dan kemudian menugaskannya kepada tugas, tiada cara untuk selarikan kontur tempahan dengan kontur tugas. Tempahan tidak menjejaskan jadual projek.

Pertimbangkan sebuah projek kompleks dengan berbilang tugas bertindih yang berbilang sumber daripada jenis yang sama perlu bekerja pada masa yang sama. Jika satu sumber diberikan kontur yang berbeza daripada agregat tugasan mereka, sukar untuk mengubah suai tugas agar sesuai dengan kontur tempahan untuk tugas yang berasingan dan kontur asalnya.

Dalam contoh di bawah, jumlah usaha yang diperlukan oleh sumber yang sama daripada satu set empat tugas ialah 62 jam dalam tempoh dua minggu dan terdapat kontur tertentu. Jika sumber Bob ditempah untuk 62 jam semasa dua minggu yang sama tetapi dengan kontur berbeza, keperluan dan penempahan adalah sejajar.

| **Kontur tugas**    | **Jumlah jam** | Is 4/6 | Se 5/6 | Ra 6//6 | Kh 7/6 | Ju 8/6 | Sa 9/6 | Ah 10/6 | Is 11/6 | Se 12/6 | Ra 13/6 | Kh 14/6 | Ju 15/6 |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Tugas 1               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| Tugas 2               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| Tugas 3               | 10              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| Tugas 4               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Jumlah**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Ketersediaan Bob
| **Penempahan sumber** | **Jumlah jam** | Is 4/6 | Se 5/6 | Ra 6/6 | Kh 7/6 | Ju 8/6 | Sa 9/6 | Ah 10/6 | Is 11/6 | Se 12/6 | Ra 13/6 | Kh 14/6 | Ju 15/6 |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Bob                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

Walau bagaimanapun, tidak ada cara yang sistematik untuk menugaskan kontur jam yang ditempah kepada tugas setiap hari. Jika pengurus projek bersedia untuk mengubah jadual projek untuk memenuhi ketersediaan sumber, maka mereka perlu mengeluarkan tugasan dan menyemak semua tugas untuk dipadankan dengan kontur tempahan.

Dalam kes apabila organisasi telah memberi tugas perancangan projek kepada pengurus projek dan pengurus sumber, pengurus projek menetapkan jadual dan ini termasuk pengkonturan kerja yang diperlukan. Pengurus sumber tidak dapat menjejaskan jadual tanpa pengetahuan pengurus projek dengan mengubah kontur usaha semasa menempah sumber sebenar. Jika pengurus sumber memenuhi sesuatu yang berbeza daripada yang diminta oleh pengurus projek, mereka perlu membuat persetujuan tentang perubahan yang diperlukan dalam jadual projek.

Memandangkan tempahan dan tugasan tidak terlalu digandingkan, anda boleh menempah kontur yang berbeza daripada kontur tugas atau menukar tugasan untuk menghasilkan keadaan di mana tempahan dan tugasan adalah di luar penjajaran.

**Pandangan Penyesuaian** membolehkan pengurus projek melihat tempahan dan tugasan untuk setiap ahli pasukan projek. Pandangan tersebut menggunakan warna dan pembayangan untuk menunjukkan tempat terdapat ketaksesuaian antara tempahan dan tugasan ahli pasukan. Berdasarkan maklumat ini, pengurus projek boleh mengambil tindakan pembetulan sama ada untuk melanjutkan tempahan sumber untuk kes-kes apabila terdapat tugasan dan tiada tempahan atau membatalkan tempahan apabila sumber ditempah tetapi tiada tugasan.

> [!NOTE]
> Jika anda mengalihkan tugas yang anda telah kontur sendiri, kontur ini tidak dikekalkan. Kontur dijanakan semula mengikut kalendar projek untuk menjelaskan perubahan dalam jam kerja dan cuti. Ini adalah mengikut rancangan kerana sistem tidak mengetahui niat kontur asal dan tidak boleh menentukan sama ada logik untuk mengekalkan kontur tersebut dalam tempoh masa baharu. Disebabkan tempahan dan tugasan dinyahsambungkan, tempahan mengekalkan kontur tempahan asal. Dalam kes ini, anda perlu membatalkan dan menempah semula kepada kontur tugasan yang baharu.



[!INCLUDE[footer-include](../includes/footer-banner.md)]