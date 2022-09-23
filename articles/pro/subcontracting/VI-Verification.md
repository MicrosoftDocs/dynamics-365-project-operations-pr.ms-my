---
title: Pengesahan invois vendor dengan aktual yang diluluskan
description: Artikel ini menerangkan cara Microsoft Dynamics 365 Project Operations let's pengurus projek mengesahkan invois vendor dengan sebenar yang telah diluluskan sebagai kontraktor melaksanakan kerja dan masa yang direkodkan serta perbelanjaan dan bahan yang digunakan oleh ahli pasukan projek.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 67e0a0143fa354ca9a87bfac5fbbd6306a97811c
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522945"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Pengesahan invois vendor dengan aktual yang diluluskan

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Microsoft Dynamics 365 Project Operations mari pengurus projek mengesahkan baris invois vendor dengan cara berikut:

- Gunakan medan **status** Pengesahan pada baris invois vendor.
- Jika baris invois vendor merujuk garis subkontrak, paut kos sebenar daripada aktiviti subkontraktor kepada baris invois vendor tersebut. Pautan dibuat dengan memadankan kos sebenar kepada baris invois vendor.

    > [!NOTE]
    > Walaupun status pengesahan boleh dijejaki untuk baris invois vendor yang tidak merujuk subkontrak, kos sebenar tidak boleh dipautkan kepada baris invois vendor tersebut.

## <a name="verification-status"></a>Status pengesahan

Medan **status** Pengesahan pada baris invois vendor menunjukkan status pengesahan tersebut. Status berikut disokong:

1. Belum dimulakan
2. Sedang dijalankan
3. Dilengkapkan

Baris invois vendor yang mempunyai status **pengesahan Tidak bermula** boleh diedit.

Baris invois vendor yang mempunyai status **pengesahan Sedang berjalan** tidak lagi boleh diedit. Untuk baris invois vendor yang merujuk subkontrak, status pengesahan disetkan secara automatik kepada **Dalam kemajuan** sebaik sahaja kos pertama sebenar dipadankan dengan baris invois vendor.

Talian invois vendor yang mempunyai status **pengesahan Selesai** tidak lagi boleh diedit. Apabila semua baris pada invois vendor mempunyai status pengesahan ini, invois vendor boleh disahkan.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Kos perlawanan sebenar kepada talian invois vendor

Pemadanan kos sebenar membantu proses pengesahan pada baris invois vendor. Untuk memadankan kos sebenar kepada talian invois vendor, ikut langkah ini.

1. Buka baris invois vendor dan pilih tab **sebenar** kos tidak dapat ditandingi. Grid menunjukkan senarai kos sebenar yang merujuk garis subkontrak yang sama seperti baris invois vendor.
2. Pilih satu atau lebih daripada kos sebenar, kemudian pilih **Padanan** pada bar alat di atas grid. Sistem ini mengesahkan bahawa kos sebenar yang dipilih boleh dipadankan. Selepas pengesahan diluluskan, kos sebenar dihubungkan dengan talian invois vendor.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Kriteria pengesahan yang digunakan untuk memautkan kos sebenar ke talian invois vendor

Semasa proses pemadanan, pautan antara kos sebenar dan talian invois vendor boleh diwujudkan hanya jika kedua-dua syarat berikut dipenuhi:

- Medan **status** Pelarasan bagi setiap kos sebenar yang dipilih mestilah kosong. Dalam erti kata lain, kos sebenar tidak boleh digantikan dengan kos sebenar lain semasa proses jurnal penarikan balik, pembatalan kelulusan, atau pembetulan.
- Nilai medan berikut dipadankan antara baris invois vendor dan kos sebenar yang dipilih. Jika mana-mana medan tidak disetkan pada baris invois vendor, ia tidak dianggap sepadan.

    - Kontrak projek
    - Baris kontrak projek
    - Kelas transaksi
    - Project
    - Tugas
    - Kategori sumber
    - Kategori transaksi
    - Produk
    - Garis subkontrak
    - Sumber boleh ditempah

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Kos tidak sepadan sebenarnya dari talian invois vendor

Kos sebenar yang tidak sepadan juga boleh membantu proses pengesahan pada invois vendor dengan membolehkan pautan yang telah ditetapkan sebelum ini dialih keluar. Kos sebenar tidak dapat ditandingi hanya dari talian invois vendor yang mempunyai status **pengesahan Sedang berjalan**. Untuk mengurangkan kos sebenar daripada talian invois vendor, ikut langkah ini.

1. Buka baris invois vendor dan pilih tab **sebenar** kos dipadankan. Grid menunjukkan senarai kos sebenar yang merujuk kepada baris invois vendor.
2. Pilih satu atau lebih kos sebenar, kemudian pilih **Tiada pada bar** alat di atas grid.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
