---
title: Pengesahan invois vendor dengan aktual yang diluluskan
description: Artikel ini menerangkan cara Microsoft Dynamics 365 Project Operations membolehkan pengurus projek mengesahkan invois vendor dengan aktual yang diluluskan sebagai kontraktor yang menjalankan kerja dan masa dirakam, dan perbelanjaan serta bahan yang digunakan oleh ahli pasukan projek.
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

Microsoft Dynamics 365 Project Operations membolehkan pengurus projek mengesahkan baris invois vendor dalam cara berikut:

- Gunakan medan **Status pengesahan** pada baris invois vendor.
- Jika baris invois vendor merujuk baris subkontrak, pautkan aktual kos daripada aktiviti subkontraktor kepada baris invois vendor tersebut. Pautan dicipta dengan memadankan aktual kos dengan baris invois vendor.

    > [!NOTE]
    > Walaupun status pengesahan boleh dijejak untuk baris invois vendor yang tidak merujuk subkontrak, aktual kos tidak boleh dipautkan kepada baris invois vendor tersebut.

## <a name="verification-status"></a>Status pengesahan

Medan **Status pengesahan** pada baris invois vendor menunjukkan status pengesahan. Status berikut disokong:

1. Belum dimulakan
2. Sedang dijalankan
3. Dilengkapkan

Baris invois vendor hanya mempunyai status pengesahan **Belum bermula** boleh diedit.

Baris invois vendor yang mempunyai status pengesahan **Sedang diproses** tidak boleh diedit lagi. Untuk baris invois vendor yang merujuk subkontrak, status pengesahan ditetapkan secara automatik kepada **Sedang diproses** sebaik sahaja aktual kos pertama dipadankan dengan baris invois vendor.

Baris invois vendor yang mempunyai status pengesahan **Selesai** tidak boleh diedit lagi. Apabila semua baris pada invois vendor mempunyai status pengesahan ini, invois vendor boleh disahkan.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Padankan aktual kos dengan baris invois vendor

Pemadanan aktual kos membantu proses pengesahan pada baris invois vendor. Untuk memadankan aktual kos dengan baris invois vendor, ikut langkah ini.

1. Buka baris invois vendor dan pilih tab **Nyahpadan aktual kos**. Grid menunjukkan senarai aktual kos yang merujuk kepada baris subkontrak yang sama dengan baris invois vendor.
2. Pilih satu atau lebih daripada aktual kos, kemudian pilih **Padankan** pada bar alat di atas grid. Sistem mengesahkan bahawa aktual kos yang dipilih boleh dipadankan. Selepas pengesahan diluluskan, aktual kos dihubungkan dengan baris invois vendor.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Kriteria pengesahan yang digunakan untuk memautkan aktual kos pada baris invois vendor

Semasa proses pemadanan, pautan antara aktual kos dengan baris invois vendor boleh diwujudkan hanya jika kedua-dua syarat berikut dipenuhi:

- Medan **Status pelarasan** untuk setiap aktual kos yang dipilih mestilah kosong. Dalam erti kata lain, aktual kos tidak boleh digantikan dengan aktual kos lain semasa sesi ingat semula, pembatalan kelulusan atau proses pembetulan.
- Nilai medan berikut dipadankan antara baris invois vendor dengan aktual kos yang dipilih. Jika sebarang medan tidak ditetapkan pada baris invois vendor, maka medan itu tidak dikira sebagai pemadanan.

    - Kontrak projek
    - Baris kontrak projek
    - Kelas transaksi
    - Project
    - Tugas
    - Kategori sumber
    - Kategori transaksi
    - Produk
    - Baris subkontrak
    - Sumber boleh ditempah

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Nyahpadan aktual kos daripada baris invois vendor

Penyahpadanan aktual kos boleh juga membantu dengan proses pengesahan pada invois vendor dengan mendayakan pautan yang ditetapkan sebelum ini untuk dialih keluar. Aktual kos boleh dinyahpadan hanya daripada baris invois vendor yang mempunyai status pengesahan **Sedang diproses**. Untuk menyahpadankan aktual kos daripada baris invois vendor, ikut langkah ini.

1. Buka baris invois vendor dan pilih tab **Memadankan aktual kos**. Grid menunjukkan senarai aktual kos yang merujuk kepada baris invois vendor.
2. Pilih satu atau lebih daripada aktual kos, kemudian pilih **Nyahpadankan** pada bar alat di atas grid.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
