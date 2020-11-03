---
title: Tugaskan sumber boleh ditempah generik kepada tugas dan pasukan projek
description: Topik ini memberikan maklumat tentang tempahan sumber generik kepada tugasan dan pasukan projek.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: ca0999ae5413d824dd1384fe2262e5226695a5f8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081243"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Tugaskan sumber boleh ditempah generik kepada tugas dan menjana keperluan sumber 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Selain membuat tempahan dan menugaskan sumber yang dinamakan atau sebenar kepada projek anda, anda boleh menugaskan sumber generik kepada tugas projek. Sumber ini boleh menjadi pemilik tempat untuk sumber yang dinamakan sehingga anda bersedia untuk menyediakan kakitangan projek anda dengan sumber yang dinamakan. 

1. Dalam Project Service Automation (PSA), buka halaman **Projek** dan pada tab **Jadual** , masukkan nama kedudukan sumber generik dalam sel **Sumber** jadual. Atau, klik ikon **Sumber** dalam sel untuk membuka pemilih sumber dan kemudian masukkan nama sumber generik yang anda ingin cipta.

![Mencipta dan menugaskan ahli pasukan generik](media/RM-how-to-9.png)

Ini akan membuka panel **Cipta Pantas: Ahli Pasukan Projek**. 

2. Masukkan peranan dan unit organisasi bagi ahli pasukan sumber generik dan kemudian klik **Simpan**.

![Cipta pantas ahli pasukan generik](media/RM-how-to-10.png)

3. Selepas anda telah mencipta ahli pasukan sumber generik yang baharu, ia ditugaskan kepada tugas. Anda boleh terus menugaskan sumber generik itu kepada tugas lain dalam jadual tugas.

![Menugaskan ahli pasukan generik sedia ada kepada tugasan](media/RM-how-to-11.png)

4. Selepas anda telah menugaskan sumber generik, anda boleh menjana keperluan sumber dan melaksanakannya dengan menempah secara langsung atau menyerahkan permintaan sumber kepada pengurus sumber.

![Menjana keperluan untuk ahli pasukan generik](media/RM-how-to-12.png)

Pada grid ahli pasukan, selain daripada boleh menggunakan pemilih sumber seperti yang dinyatakan di atas, anda boleh menambah sumber generik secara langsung. Sumber ditambah dengan keperluan sumber yang berdasarkan pada tarikh mula/tamat dan kaedah peruntukan yang ditetapkan dalam panel **Cipta Pantas: Ahli Pasukan**.

Anda boleh melihat perbezaan jika anda menambah ahli pasukan generik secara langsung dan kemudian menugaskan lebih banyak tugas kepada sumber generik berbanding mereka memerlukan waktu untuk meliputi. Klik **Jana Keperluan** untuk menjana semula keperluan untuk mengimbangkan jam yang diperlukan terhadap tugasan.

Anda juga boleh mengklik pautan **Keperluan sumber** dalam grid pasukan untuk membuka keperluan dan menambah kemahiran, sumber pilihan dll.

![Keperluan sumber](media/RM-how-to-13.png)
