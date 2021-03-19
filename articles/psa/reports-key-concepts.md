---
title: Konsep utama
description: Topik ini memberikan maklumat tentang konsep utama bagi pengurusan sumber dalam Project Service Automation.
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
ms.openlocfilehash: 704aadab3dd1b8b3e22ecdb15cf97cc7cbba1a23
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283334"
---
# <a name="key-concepts"></a>Konsep utama

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Jadual berikut mentakrifkan konsep utama yang digunakan dalam aplikasi Dynamics 365 Project Service Automation.

| Konsep                    | Definisi |
|----------------------------|------------|
| Ahli pasukan projek        | Sebagai sebahagian daripada pasukan projek, ahli pasukan projek boleh menjadi sumber yang dinamakan yang mempunyai tempahan, sumber yang dinamakan yang tidak mempunyai tempahan atau sumber generik. Sumber generik tidak mempunyai tempahan, adalah tempatan kepada projek dan tidak mempunyai kekangan kapasiti merentasi projek. |
| Sumber generik projek   | Ruang letak sumber yang membolehkan anda membentuk pasukan dan menyediakan kakitangan pelan projek tanpa perlu mengetahui sumber yang dinamakan. Kalendar projek digunakan sebagai kalendar sumber generik. Sumber generik boleh ditambah kepada pasukan projek dan ditugaskan kepada tugas. |
| Jam yang ditempah               | Jam sumber yang ditempah keras terhadap projek untuk membantu menjamin bahawa kerja projek itu selesai. Jam yang ditempah digunakan daripada kapasiti keseluruhan sumber. Penempahan adalah terhadap sumber yang dinamakan sahaja, bukan terhadap sumber generik. |
| Jam diperuntukkan             | Jam sumber ditugaskan kepada tugas dalam jadual projek. Tugasan boleh jadi terhadap sama ada sumber yang dinamakan atau sumber generik. Tugasan boleh bebas daripada tempahan. |
| Jam diperlukan             | Kapasiti yang diperlukan, tetapi tidak lagi dipenuhi oleh sumber yang dinamakan. Jam yang diperlukan hanya relevan bagi ahli pasukan generik yang telah menjana keperluan sumber. |
| Permintaan                     | Beban kerja semasa dan akan datang. Dalam Project Service Automation, permintaan ditunjukkan sebagai keperluan sumber atau permintaan sumber. |
| Keperluan sumber       | Entiti yang digunakan untuk merekodkan jam yang diperlukan, tarikh mula dan tamat, kemahiran, geografi dan dimensi penetapan harga yang lain untuk sumber yang diperlukan. Keperluan sumber sama ada dijana daripada ahli pasukan projek atau dicipta secara individu. |
| Permintaan sumber           | Entiti yang digunakan sebagai "sampul surat" untuk membawa keperluan sumber yang mesti dipenuhi oleh pengurus sumber. |
| Peranan lalai sumber      | Peranan yang sumber dikumpulkan di bawahnya untuk pengiraan penggunaan. Sumber tersebut dianggap mempunyai kemahiran yang diperlukan untuk peranan dan untuk memenuhi penggunaan sasaran bagi peranan tersebut. |
| Unit organisasi sumber | Unit organisasi yang sumber ditugaskan padanya. |
| Kontur                    | Tugas, keperluan atau jam tugasan apabila ia dipecahkan menjadi pengagihan harian. Contohnya, tugas selama lima hari, 40 jam boleh dikonturkan menjadi lapan jam sehari selama lima hari. |
| Pandangan penyesuaian        | Pandangan yang menunjukkan tempahan dan tugasan untuk setiap ahli pasukan projek. Pandangan ini membolehkan pengurus projek mencari sebarang ketakpadanan antara penempahan dan tugasan dan untuk mengambil tindakan pembetulan jika sebarang ketakpadanan berlaku. |
| Jam kerja                 | Entiti yang digunakan untuk mengenal pasti kapasiti sumber serta jam bekerja dan tidak bekerja. Entiti ini juga dirujuk sebagai kalendar sumber. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]