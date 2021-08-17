---
title: Semak sumber yang dicadangkan
description: Topik ini memberikan maklumat tentang cara untuk mencadang sumber projek.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a9d3f7b9194b29859ee1479fea8158067e22e819e8f190ef1659e14b7c0cd6b5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998022"
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

Kerana Dynamics 365 Project Operations menggunakan enjin Universal Resource Scheduling, jika anda juga telah Dynamics 365 Field Service dipasang, anda boleh melihat butiran daripada penempahan sumber untuk projek, pesanan kerja dan sebarang entiti lain yang anda telah melanjutkan penjadualan.

Untuk melihat lebih banyak butiran mengenai sumber individu, klik kanan padanya untuk membuka kad sumber.



[!INCLUDE[footer-include](../includes/footer-banner.md)]