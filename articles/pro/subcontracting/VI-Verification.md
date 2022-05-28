---
title: Pengesahan invois vendor dengan sebenar yang diluluskan
description: Topik ini menerangkan cara pengurus projek Microsoft Dynamics 365 Project Operations membenarkan mengesahkan invois vendor dengan sebenar yang diluluskan apabila kontraktor melakukan kerja dan masa yang direkodkan, dan perbelanjaan dan bahan yang digunakan oleh ahli pasukan projek.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3350a51bde2872036b79a789fae23ea6790fb21a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585481"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Pengesahan invois vendor dengan sebenar yang diluluskan

[!include [banner](../../includes/dataverse-preview.md)]

_ **Applies To:** Lite deployment - deal to proforma invoicing

Pengurus projek Microsoft Dynamics 365 Project Operations mari mengesahkan baris invois vendor dengan cara berikut:

- **Gunakan medan status** Pengesahan pada baris invois vendor.
- Jika baris invois vendor merujuk baris subkontrak, pautkan kos sebenar daripada aktiviti subkontraktor kepada baris invois vendor tersebut. Pautan ini dibuat dengan memadankan sebenarnya kos dengan baris invois vendor.

    > [!NOTE]
    > Walaupun status pengesahan boleh dijejaki untuk baris invois vendor yang tidak merujuk subkontrak, actual kos tidak boleh dipautkan kepada baris invois vendor tersebut.

## <a name="verification-status"></a>Status pengesahan

Medan **status** Pengesahan pada baris invois vendor menunjukkan status pengesahan tersebut. Status berikut disokong:

1. Belum dimulakan
2. Sedang dijalankan
3. Dilengkapkan

Baris invois vendor yang mempunyai status **pengesahan Tidak dimulakan** boleh diedit.

Baris invois vendor yang mempunyai status **pengesahan sedang berjalan** tidak lagi boleh diedit. Untuk baris invois vendor yang merujuk subkontrak, status pengesahan ditetapkan secara automatik kepada **Sedang berjalan** sebaik sahaja kos sebenar pertama dipadankan dengan baris invois vendor.

Baris invois vendor yang mempunyai status **pengesahan Lengkap** tidak lagi boleh diedit. Apabila semua baris pada invois vendor mempunyai status pengesahan ini, invois vendor boleh disahkan.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Padankan sebenar kos dengan baris invois vendor

Pemadanan sebenar kos membantu dengan proses pengesahan pada baris invois vendor. Untuk memadankan sebenar kos dengan baris invois vendor, ikuti langkah ini.

1. Buka baris invois vendor dan pilih **tab Sebenar** kos tidak sepadan. Grid menunjukkan senarai sebenar kos yang merujuk garis subkontrak yang sama seperti baris invois vendor.
2. Pilih satu atau lebih daripada sebenar kos, kemudian pilih **Padankan** pada bar alat di atas grid. Sistem ini mengesahkan bahawa sebenar kos yang dipilih boleh dipadankan. Selepas pengesahan diluluskan, sebenar kos dipautkan kepada baris invois vendor.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Kriteria pengesahan yang digunakan untuk memautkan sebenar kos kepada baris invois vendor

Semasa proses pemadanan, pautan antara kos sebenar dan garis invois vendor boleh diwujudkan hanya jika kedua-dua syarat berikut dipenuhi:

- Medan **status** Pelarasan untuk setiap kos sebenar yang dipilih mestilah kosong. Dengan kata lain, sebenar kos tidak boleh digantikan dengan sebenar kos lain semasa proses jurnal penarikan balik, pembatalan kelulusan, atau pembetulan.
- Nilai medan berikut dipadankan antara baris invois vendor dan kos sebenar yang dipilih. Jika mana-mana medan tidak ditetapkan pada baris invois vendor, ia tidak dianggap untuk dipadankan.

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

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Sebenar kos yang tidak sepadan daripada baris invois vendor

Ketidakpadanan sebenar kos juga boleh membantu proses pengesahan pada invois vendor dengan membolehkan pautan yang telah ditetapkan sebelum ini dialih keluar. Sebenar kos tidak dapat ditandingi hanya dari baris invois vendor yang mempunyai status **pengesahan Sedang berjalan**. Untuk menyahpadanankan kos sebenar daripada baris invois vendor, ikut langkah ini.

1. Buka baris invois vendor dan pilih **tab Padanan kos sebenar** . Grid menunjukkan senarai sebenar kos yang merujuk baris invois vendor.
2. Pilih satu atau lebih daripada sebenar kos, kemudian pilih **Tidak dapat ditandingi** pada bar alat di atas grid.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
