---
title: Semak sumber yang dicadangkan
description: Topik ini memberikan maklumat tentang cara untuk mencadang sumber projek.
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
ms.openlocfilehash: ad5cbdeb5fe05e6115eb024833a8d58b626ea4c9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081195"
---
# <a name="review-proposed-resources"></a>Semak sumber yang dicadangkan

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Pengurus sumber boleh mencadangkan sumber kepada pengurus projek menggunakan permintaan sumber.

1. Daripada grid permintaan atau permintaan itu sendiri, pilih **Cari sumber.**
2. Pada halaman **Pembantu Jadual** , pilih sumber dan kemudian, dalam anak tetingkap **Cipta Tempahan Sumber** dalam medan status **Status Tempahan** , pilih **Tempah.**

Kemas kini status berikut berlaku:

- Pada halaman **Pembantu Jadual** , penunjuk status dikemas kini untuk menunjukkan bahawa penempahan dicadangkan, tidak ditempah cetak.
- Pada permintaan sumber, status ditukar kepada **Keperluan Semakan Semula.**
- Pada tab **Pasukan** projek, permintaan ahli pasukan generik **Status Permintaan** ditukar kepada **Keperluan Semakan Semula.**

Pengurus projek boleh sama ada menerima atau menolak cadangan itu.

Apabila pengurus sumber memproses permintaan sumber, mereka boleh menggunakan sebarang pendekatan berikut:

- Mencadangkan berbilang sumber untuk memenuhi permintaan jika tiada sumber tunggal tersedia untuk memenuhi jam yang diperlukan. Waktu yang dicadangkan kemudian berpecah antara sumber yang boleh memenuhi jam yang diperlukan. Dalam senario ini, jam tidak boleh bertindan.
- Mencadangkan lebih sedikit sumber daripada keperluan. Dalam senario ini, kapasiti sumber yang dicadangkan adalah kurang daripada jam yang diperlukan yang ditentukan oleh peminta. Oleh itu, apabila peminta menerima sumber yang dicadangkan, keperluan sumber yang tidak dipatuhi dicipta untuk menawan permintaan yang berbaki.
- Tempah berbilang sumber untuk memenuhi permintaan jika tiada sumber tunggal tersedia untuk menyelesaikan kerja.
- Menempah lebih sedikit sumber daripada keperluan. Dalam senario ini, masa yang ditempah adalah lebih sedikit daripada jam yang diperlukan. Sistem ini memberi panduan kepada anda untuk mencadangkan sumber dan bukannya penempahan, supaya peminta boleh mengesahkan dan menjejaki permintaan yang berbaki.

## <a name="billable-utilization"></a>Penggunaan boleh dibilkan

Sumber boleh mempunyai sasaran penggunaan boleh dibilkan. Penggunaan sasaran ini sama ada ditakrifkan sebagai atribut pada peranan lalai sumber atau ditetapkan pada rekod sumber boleh ditempah individu. Pengiraan penggunaan adalah berdasarkan masa sebenar bahawa sumber telah dilaporkan dengan menggunakan kemasukan penyertaan yang diluluskan.

Formula berikut digunakan untuk mengira penggunaan:

- Penggunaan boleh dibilkan = Jam sebenar ÷ Kapasiti sumber boleh dituntut.
- Penggunaan tidak boleh dibilkan = Masa sebenar dengan ID jenis bil = Tidak dikenakan caj, Pelengkap atau Tidak tersedia yang boleh ÷ Kapasiti sumber
- Dalaman = Masa sebenar dengan tiada kontrak jualan ÷ Kapasiti sumber
- Kapasiti sumber = Waktu kerja sumber – Keluar dari pejabat – Hari tidak bekerja

Anda boleh mencari pandangan **Penggunaan Sumber** dalam anak tetingkap **Sumber**.

Setiap sel dalam grid mewakili peratusan penggunaan boleh dibilkan bagi sumber dalam tempoh, seperti hari, minggu atau bulan. Formula berikut digunakan untuk mewarnakan sel:

- **Hijau:** Penggunaan boleh dibilkan \>= Penggunaan sasaran sumber
- **Kuning:** Penggunaan sasaran – 20 \<= Penggunaan boleh dibilkan \< Penggunaan sasaran
- **Merah:** Penggunaan boleh dibilkan \< Penggunaan sasaran – 20

Oleh kerana pandangan **Penggunaan Sumber** adalah berdasarkan Papan Jadual, anda boleh menggunakan keupayaan penapisan Papan Jadual untuk menapis hasil anda.

Grid memerlukan anda menetapkan penggunaan sasaran pada sama ada peranan atau sumber individu. Untuk melakukan persediaan ini, pergi ke **Peranan** \> **Peranan sumber**.

Selain itu, peranan lalai mesti ditugaskan kepada setiap sumber boleh ditempah. Pergi ke **Sumber** \> **Sumber**. Pada tab **Project Service** sahkan peranan sumber ditakrifkan dan medan **Adalah Lalai** untuk ia disetkan kepada **Ya.** Anda boleh menambah peranan tambahan di mana **Adalah Lalai = No**. Peranan di mana **Adalah Lalai = Ya** digunakan untuk menilai penggunaan sumber terhadap sasaran untuk peranan tersebut.

Pada tab **Project Service** , anda juga boleh menetapkan penggunaan sasaran individu untuk sumber. Pengiraan penggunaan ini kemudian menggunakan penggunaan sasaran yang akan menilai sasaran sumber bukan sasaran peranan lalai sumber.

Penggunaan ditunjukkan untuk sumber hanya jika sumber tersebut telah diluluskan dan masa boleh dikenakan dalam tempoh yang ditunjukkan dalam grid.

## <a name="resource-availability"></a>Ketersediaan sumber

Adalah penting bahawa pengurus sumber boleh melihat ketersediaan sumber dan kemas kini tempahan. Dalam sesetengah kes, tidak ada permintaan formal (permintaan sumber), tetapi pengurus sumber mesti bertindak balas kepada permintaan yang tidak dirancang yang datang melalui saluran seperti e-mel, panggilan telefon atau mesej segera. Pengurus sumber menggunakan Papan Jadual untuk mengemas kini sumber dan penempahan.

Waktu kerja sumber digunakan sebagai asas untuk mengira ketersediaan sumber. Tempahan sumber mengambil kapasiti sumber.

Papan Jadual menggunakan warna dan pembayangan untuk menunjukkan penempahan, ketersediaan dan pilihan berlebihan dan juga status tempahan. Tetapan dalam tetapan Papan Jadual membolehkan anda menunjukkan petunjuk.

Jika anak panah tunjuk sebelah kanan muncul di sebelah sumber boleh ditempah individu pada Papan Jadual, sumber itu dapat dikembangkan untuk menunjukkan butiran kerja yang digunakan oleh sumber tersebut.

Oleh kerana Dynamics 365 Project Operations menggunakan enjin Universal Resource Scheduling, jika anda juga dipasang dengan Dynamics 365 Field Service, anda boleh melihat butiran tempahan sumber untuk projek, pesanan kerja dan sebarang entiti lain yang anda telah lanjutkan penjadualannya.

Untuk melihat lebih banyak butiran mengenai sumber individu, klik kanan padanya untuk membuka kad sumber.

