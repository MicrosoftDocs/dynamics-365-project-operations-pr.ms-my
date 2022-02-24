---
title: Gambaran keseluruhan penyelarasan sumber
description: Topik ini menyediakan maklumat yang akan membantu anda memastikan bahawa tempahan dan tugasan sumber untuk projek disejajarkan.
author: ruhercul
manager: AnnBe
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 8723cfad1e7cd07774e37023c5427b0a5833a554
ms.sourcegitcommit: cffc84187007b34211c90babef8af5152d4d92ea
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 01/12/2021
ms.locfileid: "4849635"
---
# <a name="resource-reconciliation-overview"></a>Gambaran keseluruhan penyelarasan sumber

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Untuk ahli pasukan, tempahan dan tugasan tidak begitu digandingkan. Dengan kata lain, sumber boleh mempunyai tugasan dan tidak tempahan, atau mereka boleh ada tempahan dan tidak tugasan. Tempahan dan tugasan hendaklah sejajar, agar sumber ada kapasiti komited untuk melaksanakan tugasan tugas. Namun, tempahan mungkin berdasarkan ketersediaan, dan pemasaan tugas mungkin berubah seiring projek diteruskan. Makan, gandingan longgar tempahan dan tugasan memberikan kefleksibelan.

Tab **Pelarasan** pada halaman **Projek** membolehkan pengurus projek menyesuaikan tempahan dan tugasan ahli pasukan mereka untuk pasukan projek.

Tab **Penyelarasan** menunjukkan tempahan dan tugasan sehingga ke tahap tugasan tugas individu untuk setiap ahli pasukan. Jam ditunjukkan dalam sel yang mewakili tempoh dari bulan hingga hari. Tab juga menunjukkan gambaran keseluruhan jumlah bersih bagi projek, bersama-sama dengan lajur **Jumlah**.

Untuk setiap sumber, tab **Pelarasan** mengira perbezaan antara tempahan dan gulung atas ahli pasukan bagi tugasan tugas ahli pasukan. Perbezaan ini hendaklah 0 (sifar). Dengan kata lain, tiada perbezaan antara tempahan dan tugasan. Perbezaan diwarnai dan dibayangi untuk menarik perhatian kepada dua keadaan:

- **Kekurangan tempahan** – Kekurangan tempahan berlaku apabila sumber ada lebih tugasan berbanding tempahan. Disebabkan kapasiti ini telah disimpan, pengurus projek mungkin mahu membetulkan keadaan ini dengan melanjutkan tempahan sumber untuk menampung desifit.
- **Tempahan berlebihan** – Tempahan berlebihan berlaku apabila sumber telah ditempah kepada projek tetapi belum ditugaskan kepada tugas. Keadaan ini mungkin boleh diterima dalam situasi di mana sumber ditempah untuk projek sebelum tugasan tugas berlaku. Namun, dalam situasi lain yang mana tiada rancangan untuk menugaskan sumber kepada tugas, pengurus projek harus mempertimbangkan untuk membatalkan tempahan sumber. Dengan cara itu, kapasiti boleh digunakan untuk projek lain.

Dalam situasi tertentu, apabila anda melihat masa pada tahap lebih tingi daripada tahap hari (contohnya, tahap bulan), anda mungkin melihat perbezaan bersih sifar untuk sumber (dengan kata lain, tempahan sama dengan tugasan). Namun, jika anda melihat masa pada tahap minggu, anda mungkin melihat tugasan sifat jam dan tempahan 40 jam dalam minggu pertama, tetapi tugasan 40 jam dan tempahan sifar jam dalam minggu kedua. Keseluruhannya, tempahan dan tugasan diselaraskan, tetapi berbeza dari satu minggu ke minggu seterusnya.

Apabila anda melihat masa pada tahap lebih tinggi, sel pada tab **Penyelarasan** mempunyai penunjuk untuk memaklumkan anda terdapat perbezaan pada tahap lebih rendah. Dengan mengetik atau mengklik dua kali dalam sel, anda boleh zum dekat untuk melihat perbezaan. Anda kemudian boleh pilih dan tahan (atau klik kanan) untuk zum jauh. Dengan memilih sumber dan menggunakan kawalan **Perbezaan seterusnya** pada bar alat grid, anda boleh pergi ke perbezaan seterusnya antara tempahan dan tugasan untuk sumber tersebut. Anda kemudian boleh menggunakan kawalan **Perbezaan sebelumnya** untuk kembali. Anda juga boleh mematikan penunjuk perbezaan dan tingkah laku navigasi di bawah **Tetapan**.

Jika anda ada tugasan tugas untuk sumber tetapi tiada tempahan, pilih kekurangan tempahan pada tab **Pelarasan** pada halaman **Projek**, kemudian pilih **Lanjutkan Tempahan**. Kotak dialog **Lanjutkan Tempahan** yang muncul menunjukkan tempahan yang diperlukan untuk menyelesaikan kekurangan sumber. Kotak dialog juga menunjukkan tempahan sumber yang sedia ada di semua projek atau entiti lain yang boleh dijadualkan. Jika anda pilih **OK** untuk mencipta tempahan untuk sumber, tanpa mengira ketersediaan sumber tersebut, anda mungkin menyebabkan tempahan berlebihan.

Tempahan yang dicipta melalui tindakan **Lanjutkan Tempahan** dikaitkan dengan keperluan projek utama. Apabila lanjutan dimulakan, keperluan khusus yang mesti dilanjutkan tidak boleh ditentukan, kerana sumber mungkin dikaitkan dengan lebih daripada satu keperluan untuk projek.

Pengurus projek atau pengurus sumber kemudian boleh menggunakan Papan Jadual untuk mengurus sebarang situasi di mana sumber ditempah berlebihan di luar kapasitinya.
