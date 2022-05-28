---
title: Semak sumber yang dicadangkan
description: Topik ini memberikan maklumat tentang cara untuk mencadang sumber projek.
author: ruhercul
ms.date: 08/18/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3d2ab3ba9e5b18a2b42acaa2dc51ad94b8189274
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584975"
---
# <a name="review-proposed-resources"></a>Semak sumber yang dicadangkan

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Pengurus sumber boleh mencadangkan sumber kepada pengurus projek menggunakan permintaan sumber.

Untuk menyemak sumber yang dicadangkan, ikut langkah berikut:

1. Daripada grid **Permintaan** atau permintaan itu sendiri, pilih **Cari Sumber**.
2. Pada halaman **Pembantu Jadual**, pilih sumber dan kemudian sahkan bahawa semua jam yang dicadangkan akan disertakan dalam tempahan yang dicadangkan.
3. Dalam anak tetingkap **Cipta Tempahan Sumber**, tetapkan medan **Status Tempahan** kepada **Dicadangkan** dan kemudian pilih **Tempah**.

    > [!NOTE]
    > Menetapkan **Status Tempahan** kepada **Dicadangkan** tidak akan menempah sumber secara terjamin dan tidak menggantikan sumber generik dengan ahli pasukan yang dinamakan.

    Kemas kini status berikut berlaku:

    - Pada halaman **Pembantu Jadual**, penunjuk status dikemas kini untuk menunjukkan bahawa tempahan telah dicadangkan, bukan ditempah secara terjamin.
    - Pada permintaan sumber, status ditukar kepada **Keperluan Semakan Semula.**
    - Pada tab **Pasukan** projek, permintaan ahli pasukan generik **Status Permintaan** ditukar kepada **Keperluan Semakan Semula.**

Pengurus projek boleh menerima atau menolak cadangan itu.

Apabila pengurus sumber memproses permintaan sumber, mereka boleh menggunakan sebarang pendekatan berikut:

- Mencadangkan berbilang sumber untuk memenuhi permintaan jika tiada sumber tunggal tersedia untuk memenuhi jam yang diperlukan. Waktu yang dicadangkan kemudian berpecah antara sumber yang boleh memenuhi jam yang diperlukan. Dalam senario ini, jam tidak boleh bertindan.
- Mencadangkan lebih sedikit sumber daripada keperluan. Dalam senario ini, kapasiti sumber yang dicadangkan adalah kurang daripada jam yang diperlukan yang ditentukan oleh peminta. Apabila peminta menerima sumber yang dicadangkan, keperluan sumber yang tidak dipatuhi dicipta untuk mencatatkan permintaan yang selebihnya.
- Tempah berbilang sumber untuk memenuhi permintaan jika tiada sumber tunggal tersedia untuk menyelesaikan kerja.
- Tempah kurang sumber daripada yang diperlukan. Dalam senario ini, masa yang ditempah adalah lebih sedikit daripada jam yang diperlukan. Sistem akan membimbing anda untuk mencadangkan sumber dan bukannya tempahan supaya peminta boleh mengesahkan dan menjejak permintaan yang selebihnya.

## <a name="resource-availability"></a>Ketersediaan sumber

Pengurus sumber mesti dapat melihat ketersediaan sumber dan mengemas kini tempahan. Dalam sesetengah kes, tidak ada permintaan formal (permintaan sumber). Walau bagaimanapun, pengurus sumber mesti bertindak balas terhadap permintaan yang tidak dirancang yang datang melalui saluran lain seperti e-mel, panggilan telefon atau mesej segera. Pengurus sumber menggunakan **Papan Jadual** untuk mengemas kini sumber dan tempahan.

Jam kerja sumber digunakan sebagai asas untuk mengira ketersediaan sumber. Tempahan sumber mengambil kapasiti sumber.

**Papan Jadual** menggunakan warna dan pembayangan untuk menunjukkan tempahan, ketersediaan dan tempahan berlebihan dan juga status tempahan. Tetapan pada **Papan Jadual** membolehkan anda memaparkan petunjuk.

Jika anak panah yang menunjuk ke sebelah kanan muncul di sebelah sumber boleh ditempah individu pada **Papan Jadual**, sumber itu boleh dikembangkan untuk menunjukkan butiran kerja yang sumber tersebut ditempahkan.

Kerana Dynamics 365 Project Operations menggunakan enjin Universal Resource Scheduling, jika anda juga telah Dynamics 365 Field Service dipasang, anda boleh melihat butiran daripada penempahan sumber untuk projek, pesanan kerja dan sebarang entiti lain yang anda telah melanjutkan penjadualan.

Untuk melihat butiran tambahan tentang sumber individu, klik kanan padanya untuk membuka kad sumber.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
