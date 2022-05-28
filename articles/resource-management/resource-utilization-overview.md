---
title: Gambaran keseluruhan penggunaan sumber
description: Topik ini memberikan maklumat tentang penggunaan sumber dalam Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e24bbb33cdf34426d4e7fff21b68fcaea2fcef5e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587137"
---
# <a name="resource-utilization-overview"></a>Gambaran keseluruhan penggunaan sumber

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Sumber boleh mempunyai sasaran penggunaan boleh dibilkan. Penggunaan sasaran ini ditakrifkan sebagai atribut pada peranan lalai sumber atau ditetapkan pada rekod sumber boleh ditempah individu. Pengiraan penggunaan adalah berdasarkan masa sebenar bahawa sumber telah dilaporkan dengan menggunakan kemasukan penyertaan yang diluluskan.

Formula berikut digunakan untuk mengira penggunaan:

  - Penggunaan boleh dibilkan = Jam sebenar ÷ Kapasiti sumber boleh dituntut.
  - Penggunaan tidak boleh dibilkan = Masa sebenar dengan ID jenis bil = Tidak dikenakan caj, Pelengkap atau Tidak tersedia yang boleh ÷ Kapasiti sumber
  - Dalaman = Masa sebenar dengan tiada kontrak jualan ÷ Kapasiti sumber
  - Kapasiti sumber = Waktu kerja sumber – Keluar dari pejabat – Hari tidak bekerja

Anda boleh mencari pandangan **Penggunaan Sumber** dalam anak tetingkap **Sumber**.

Setiap sel dalam grid mewakili peratusan penggunaan boleh dibilkan bagi sumber dalam tempoh, seperti hari, minggu atau bulan. Formula berikut digunakan untuk mewarnakan sel:

  - **Hijau**: Penggunaan boleh dibilkan >= Penggunaan sasaran sumber
  - **Kuning**: Penggunaan sasaran – 20 <= Penggunaan boleh dibilkan < Penggunaan sasaran
  - **Merah**: Penggunaan boleh dibilkan < Penggunaan sasaran – 20

Oleh kerana pandangan **Penggunaan Sumber** adalah berdasarkan Papan Jadual, anda boleh menggunakan keupayaan penapisan Papan Jadual untuk menapis hasil anda.

Grid memerlukan anda menetapkan penggunaan sasaran pada sama ada peranan atau sumber individu. Untuk melakukan persediaan ini, pergi ke **Sumber** > **Peranan sumber**.

Selain itu, peranan lalai mesti ditugaskan kepada setiap sumber boleh ditempah. Pergi ke **Sumber** > **Sumber**. Pada tab **Perkhidmatan Projek**, sahkan peranan sumber yang ditakrifkan dan medan **Ialah Lalai** ditetapkan kepada **Ya**. Anda boleh menambah peranan tambahan iaitu **Ialah Lalai** = **Tidak**. Peranan iaitu **Ialah Lalai** = **Ya** digunakan untuk menilai penggunaan sumber terhadap sasaran untuk peranan tersebut.

Pada tab **Project Service**, anda juga boleh menetapkan penggunaan sasaran individu untuk sumber. Pengiraan penggunaan ini kemudian menggunakan penggunaan sasaran yang akan menilai sasaran sumber bukan sasaran peranan lalai sumber.

Penggunaan ditunjukkan untuk sumber sahaja jika sumber tersebut telah diluluskan dan masa boleh dituntut dalam tempoh yang ditunjukkan dalam grid.


[!INCLUDE[footer-include](../includes/footer-banner.md)]