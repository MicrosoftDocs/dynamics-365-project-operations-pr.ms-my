---
title: Semak sumber yang dicadangkan
description: Topik ini memberikan maklumat tentang cara untuk mencadang sumber projek.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
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
ms.openlocfilehash: 54a0924da17eac86e2fa400540e629f6d803aa35
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401184"
---
# <a name="review-proposed-resources"></a>Semak sumber yang dicadangkan

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Pengurus sumber boleh mencadangkan sumber kepada pengurus projek menggunakan permintaan sumber.

1. Daripada grid permintaan atau permintaan itu sendiri, pilih **Cari sumber.**
2. Pada halaman **Pembantu Jadual** , pilih sumber dan kemudian, dalam anak tetingkap **Cipta Tempahan Sumber** dalam medan status **Status Tempahan**, pilih **Tempah.**

Kemas kini status berikut berlaku:

- Pada halaman **Pembantu Jadual**, penunjuk status dikemas kini untuk menunjukkan bahawa penempahan dicadangkan, tidak ditempah cetak.
- Pada permintaan sumber, status ditukar kepada **Keperluan Semakan Semula.**
- Pada tab **Pasukan** projek, permintaan ahli pasukan generik **Status Permintaan** ditukar kepada **Keperluan Semakan Semula.**

Pengurus projek boleh sama ada menerima atau menolak cadangan itu.

Apabila pengurus sumber memproses permintaan sumber, mereka boleh menggunakan sebarang pendekatan berikut:

- Mencadangkan berbilang sumber untuk memenuhi permintaan jika tiada sumber tunggal tersedia untuk memenuhi jam yang diperlukan. Waktu yang dicadangkan kemudian berpecah antara sumber yang boleh memenuhi jam yang diperlukan. Dalam senario ini, jam tidak boleh bertindan.
- Mencadangkan lebih sedikit sumber daripada keperluan. Dalam senario ini, kapasiti sumber yang dicadangkan adalah kurang daripada jam yang diperlukan yang ditentukan oleh peminta. Oleh itu, apabila peminta menerima sumber yang dicadangkan, keperluan sumber yang tidak dipatuhi dicipta untuk menawan permintaan yang berbaki.
- Tempah berbilang sumber untuk memenuhi permintaan jika tiada sumber tunggal tersedia untuk menyelesaikan kerja.
- Menempah lebih sedikit sumber daripada keperluan. Dalam senario ini, masa yang ditempah adalah lebih sedikit daripada jam yang diperlukan. Sistem ini memberi panduan kepada anda untuk mencadangkan sumber dan bukannya penempahan, supaya peminta boleh mengesahkan dan menjejaki permintaan yang berbaki.

## <a name="resource-availability"></a>Ketersediaan sumber

Adalah penting bahawa pengurus sumber boleh melihat ketersediaan sumber dan kemas kini tempahan. Dalam sesetengah kes, tidak ada permintaan formal (permintaan sumber), tetapi pengurus sumber mesti bertindak balas kepada permintaan yang tidak dirancang yang datang melalui saluran seperti e-mel, panggilan telefon atau mesej segera. Pengurus sumber menggunakan Papan Jadual untuk mengemas kini sumber dan penempahan.

Waktu kerja sumber digunakan sebagai asas untuk mengira ketersediaan sumber. Tempahan sumber mengambil kapasiti sumber.

Papan Jadual menggunakan warna dan pembayangan untuk menunjukkan penempahan, ketersediaan dan pilihan berlebihan dan juga status tempahan. Tetapan dalam tetapan Papan Jadual membolehkan anda menunjukkan petunjuk.

Jika anak panah tunjuk sebelah kanan muncul di sebelah sumber boleh ditempah individu pada Papan Jadual, sumber itu dapat dikembangkan untuk menunjukkan butiran kerja yang digunakan oleh sumber tersebut.

Oleh kerana Dynamics 365 Project Operations menggunakan enjin Universal Resource Scheduling, jika anda juga dipasang dengan Dynamics 365 Field Service, anda boleh melihat butiran tempahan sumber untuk projek, pesanan kerja dan sebarang entiti lain yang anda telah lanjutkan penjadualannya.

Untuk melihat lebih banyak butiran mengenai sumber individu, klik kanan padanya untuk membuka kad sumber.

