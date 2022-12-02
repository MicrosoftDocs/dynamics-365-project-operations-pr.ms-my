---
title: Tempah lembut sumber
description: Artikel ini memberikan maklumat tentang cara menjadualkan secara sementara atau membuat tempahan sementara ahli pasukan projek.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 6c666e5c0a83a3d1b440144a62cbd58a58c5db81
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929133"
---
# <a name="soft-book-a-resource"></a>Tempah lembut sumber

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Anda boleh jadualkan secara sementara atau "menempah sementara" satu sumber kepada pasukan projek untuk menunjukkan yang anda merancang untuk menugaskan sumber itu kepada projek. Menempah sementara tidak menggunakan kapasiti tersedia sumber dan anda boleh menugaskan ahli pasukan yang ditempah sementara kepada tugas projek. Walau bagaimanapun, disebabkan menempah sementara tidak menggunakan kapasiti sumber, anda masih boleh "menempah tetap" sumber itu untuk tugas lain dalam tempoh yang sama. Sumber generik tidak boleh ditempah lembut, tempahan lembut juga tidak boleh memenuhi permintaan untuk sumber generik.

Ahli pasukan projek yang ditempah lembut disenaraikan pada tab **Pasukan** dalam halaman **Projek**, dengan jam ditempah lembut mereka ditunjukkan dalam lajur **Jam Ditempah Lembut** dalam pandangan **Ahli Pasukan Bernama**. Ahli pasukan ditempah lembut juga tersenarai pada papan Jadual. Disebabkan mereka ditempah lembut, papan Jadual tidak menunjukkan sebarang penggunaan kapasiti untuk sumber ini. Masa ditempah lembut tidak muncul pada tab **Penyesuaian**, tidak juga muncul dalam medan **Lanjutkan Tempahan** dalam tab **Penyesuaian** bagi papan Jadual. 

Terdapat dua cara untuk tempah lembut ahli pasukan ke dalam projek: terus dari papan Jadual, atau dengan menambah ahli pasukan pada tab **Pasukan**. 

## <a name="soft-book-from-the-schedule-board"></a>Tempah lembut dari papan Jadual
Lengkapkan langkah-langkah berikut untuk tempah lembut sumber dari papan Jadual. 

1. Buka papan Jadual, kemudian dalam panel **Syarat Tempahan**, pilih tab **Projek**.
2. Cari projek yang anda mahu tempah lembut sumber. Jika terdapat sebilangan besar projek dalam senarai, pilih pengepala lajur **Projek**, kemudian guna penapis untuk mencari satau atau lebih projek.
3. Pilih projek, kemudian seret dan jatuhkannya pada grid masa sumber.
5. Dalam panel **Cipta Tempahan Sumber**, selaraskan tarikh mula dan tamat, tetapakn **Status Tempahan** kepada **Lembut**, kemudian tetapkan jam. 
6. Klik **Tempah**. Sumber sekarang ditunjukkan pada tab **Pasukan** sebagai sumber untuk projek. Pada pandangan **Ahli Pasukan Bernama**, anda akan melihat jam ditempah lembut dalam lajur **Jam Ditempah Lembut**.

> [!NOTE]
> Anda kini boleh menugaskan ditempah lembut kepada tugas pada tab **Jadual**. Pada tab **Penyesuaian**, sumber menunjukkan defisit tempahan berkaitan dengan tugasan tugas kerana tab **Penyesuaian** hanya mempertimbangkan tempahan keras. Anda boleh menggunakan ciri **Lanjutkan Tempahan** untuk tempah keras sumber bagi menyingkirkan defisit tempahan keras terhadap tugasan sumber. Anda perlu membatalkan tempahan lembut secara manual untuk sumber dengan menggunakan **Kekalkan Tempahan**.

## <a name="soft-book-on-the-team-tab"></a>Tempah sementara pada tab Pasukan

Anda boleh menambah ahli pasukan secara terus pada tab **Pasukan**, kemudian mengubah status tempahan mereka daripada **Keras** kepada **Lembut** dengan **Kekalkan Tempahan**. Apabila anda menambah ahli pasukan dengan cara ini, ia sentiasa akan menghasilkan tempahan keras kecuali anda memilih kaedah peruntukan sebagai **Tiada**.

Untuk menggunakan kaedah ini, lengkapkan langkah-langkah berikut.

1. Pada halaman **Projek**, pada tab **Pasuka**, klik **Baharu**.
2. Pilih sumber boleh tempah, peranan, dan tarikh dari dan sehingga.
3. Pilih kaedah peruntukan selain daripada **Tiada**.
4. Pilih **Simpan**. Anda akan melihat sumber pada grid dan jam mereka dalam lajur **Jam Ditempah Keras**.
5. Kekalkan tempahan sumber dengan memilih **Kekalkan Tempahan**.
6. Apabila papan Jadual dibuka, kembangkan sumber untuk menunjukkan tempahan mereka. Anda akan melihat tempahan ditunjukkan sebagai **Keras**.
7. Klik kanan tempahan, dan di bawah **Ubah Status**, pilih **Tempah Lembut** \> **Lembut**. Status tempahan kini adalah **Lembut**.
8. Selepas anda menutup papan Jadual, anda akan mendapati bahawa sumber telah dialih keluar daripada lajur **Jam Ditempah Keras** kepada **Jam Ditempah Lembut** pada grid tab **Pasukan**, apabila melihat pada pandangan **Ahli Pasukan Bernama**.

> [!NOTE]
> Apabila anda menggunakan **Kekalkan Tempahan** untuk menukar status daripada **Keras** kepad **Lembut**, jka anda tempah keras sumber ke dalam pasukan dan kemudian menugaskan tugas ekpada sumber, tugasan tugas untuk sumber dikekalkan. Namun, pada tab **Penyesuaian**, sumber akan mengalami kekurangan tempahan kerana hanya tempahan keras dipertimbangkan apabila menyesuaikan tempahan dengan tugasan. Anda boleh menggunakan ciri **Lanjutkan Tempahan** pada tab **Penyesuaian** untuk tempah keras sumber bagi menyingkirkan defisit tempahan keras terhadap tugasan sumber. Anda perlu membatalkan tempahan lembut untuk sumber dengan menggunakan **Kekalkan Tempahan**.

Apabila anda bersedia untuk menukar sumber ahli pasukan yang ditempah sementara kepada ahli pasukan ditempah tetap, lakukan yang berikut:

1. Pada papan Jadual, kembangkan sumber untuk menunjukkan tempahan mereka. Anda akan melihat tempahan ditunjukkan sebagai **Lembut**.
2. Klik kanan tempahan, dan di bawah **Ubah Status**, pilih **Tempah Keras** \> **Keras**. Status tempahan kini adalah **Keras**.
3. Selepas anda menutup papan Jadual, kembalik ke projek, dan buka tab **Pasukan**, anda akan mendapati bahawa jam untuk sumber telah dialih keluar daripada lajur **Jam Ditempah Lembut** kepada lajur **Jam Ditempah Keras** pada tab **Pasukan** apabila dalam pandangan **Ahli Pasukan Bernama**. Jika sumber ditugaskan kepada tugas, ia tidak lagi ditunjukkan sebagai defisit tempahan pada tab **Penyesuaian** kerana tempahannya kini adalah keras.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
