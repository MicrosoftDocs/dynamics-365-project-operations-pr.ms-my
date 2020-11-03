---
title: Gambaran keseluruhan penyelarasan sumber
description: Topik ini menyediakan maklumat tentang memastikan penempahan sumber dan tugasan projek disejajarkan.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e2b16a6e1c48769ed4d903e546804ba1c4e1c4fa
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081170"
---
# <a name="resource-reconciliation-overview"></a>Gambaran keseluruhan penyelarasan sumber

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Untuk ahli pasukan, tempahan dan tugasan tidak begitu digandingkan. Dengan kata lain, sumber boleh mempunyai tugasan tapi tidak tempahan, atau mereka boleh ada tempahan tetapi tidak tugasan. Tempahan dan tugasan hendaklah sejajar, agar sumber ada kapasiti komited untuk melaksanakan tugasan tugas. Namun, tempahan mungkin berdasarkan ketersediaan, dan pemasaan tugas mungkin berubah seiring projek diteruskan. Makan, gandingan longgar tempahan dan tugasan memberikan kefleksibelan.

Tab **Penyelarasan** pada borang **Projek** membolehkan pengurus projek menyelaraskan tempahan ahli pasukan dan tugasan mereka untuk pasukan projek.

Tab **Penyelarasan** juga menunjukkan tempahan dan tugasan sehingga ke tahap tugasan tugas individu untuk setiap ahli pasukan. Jam dipaparkan dalam sel yang mewakili tempoh masa daripada bulan hingga hari.

Tab juga menunjukkan gambaran keseluruhan jumlah bersih bagi projek, bersama-sama dengan lajur **Jumlah**.

Untuk setiap sumber, tab mengira perbezaan antara tempahan dan gulung atas ahli pasukan bagi tugasan tugas ahli pasukan. Perbezaan ini hendaklah 0 (sifar). Dengan kata lain, tiada perbezaan antara tempahan dan tugasan. Perbezaan diwarnai dan dibayangi untuk menarik perhatian kepada dua keadaan:

- **Kekurangan tempahan** – Kekurangan tempahan berlaku apabila sumber ada lebih tugasan berbanding tempahan. Disebabkan kapasiti ini telah disimpan, pengurus projek mungkin mahu membetulkan keadaan ini dengan melanjutkan tempahan sumber untuk menampung desifit.
- **Tempahan berlebihan** – Tempahan berlebihan berlaku apabila sumber telah ditempah kepada projek tetapi belum ditugaskan kepada tugas. Keadaan ini mungkin boleh diterima dalam situasi di mana sumber ditempah untuk projek sebelum tugasan tugas berlaku. Namun, dalam situasi lain, sumber tidak dirandang ditugaskan kepada tugas. Dalam kes ini, pengurus projek perlu mempertimbangkan untuk membatalkan penempahan sumber, supaya kapasiti boleh digunakan untuk projek lain.

Dalam situasi tertentu, apabila anda melihat masa pada tahap lebih tingi daripada tahap hari (contohnya, tahap bulan), anda mungkin melihat perbezaan bersih sifar untuk sumber (dengan kata lain, tempahan = tugasan). Namun, jika anda melihat masa pada tahap minggu, anda mungkin melihat tugasan sifat jam dan tempahan 40 jam dalam minggu pertama, tetapi tugasan 40 jam dan tempahan sifar jam dalam minggu kedua. Keseluruhannya, tempahan dan tugasan diselaraskan, tetapi berbeza dari satu minggu ke minggu seterusnya.

Apabila anda melihat masa pada tahap lebih tinggi, sel dalam tab **Penyelarasan** mempunyai penunjuk untuk memaklumkan anda terdapat perbezaan pada tahap lebih rendah. Dengan mengklik dua kali dalam sel, anda boleh zum dekat untuk melihat perbezaan. Anda kemudian boleh klik kanan untuk zum jauh. Dengan memilih sumber dan menggunakan kawalan **Perbezaan seterusnya** pada bar alat grid, anda boleh pergi ke perbezaan seterusnya antara tempahan dan tugasan untuk sumber tersebut. Anda kemudian boleh menggunakan kawalan **Perbezaan sebelumnya** untuk kembali. Anda juga boleh mematikan penunjuk perbezaan dan tingkah laku navigasi di bawah **Tetapan**.


Jika anda ada tugasan tugas untuk sumber tetapi tiada tempahan, pada halaman **Projek** , pada tab **Penyelarasan** , pilih kekurangan tempahan dan kemudian pilih **Lanjutkan Tempahan**. Kotak dialog **Lanjutkan Tempahan** muncul dan menunjukkan tempahan yang diperlukan untuk menyelesaikan kekurangan sumber. Ia juga menunjukkan tempahan sedia ada sumber dalam semua projek atau entiti boleh dijadual lain. Jika anda pilih **OK** untuk mencipta tempahan untuk sumber, tanpa mengira ketersediaan sumber tersebut, anda mungkin menyebabkan tempahan berlebihan.

Pengurus projek atau pengurus sumber kemudian boleh menggunakan Papan Jadual untuk mengurus sebarang situasi di mana sumber ditempah berlebihan di luar kapasitinya.

