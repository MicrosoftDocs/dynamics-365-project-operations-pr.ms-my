---
title: Aktifkan dan semak sebut harga projek
description: Artikel ini memberikan maklumat tentang pengaktifan dan penyemakan sebut harga dalam Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410378"
---
# <a name="activate-and-revise-a-project-quote"></a>Aktifkan dan semak sebut harga projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Keupayaan pengaktifan dan semakan membantu anda menjejaki versi sebut harga berdasarkan projek semasa fasa anggaran dan rundingan. Apabila draf sebut harga diaktifkan, ia menjadi baca sahaja.

Keupayaan pengaktifan dan semakan membolehkan anda melakukan tugas berikut:

- Menang atau kalah sebut harga hanya selepas pengaktifan.
- Semak sebut harga sama ada untuk membuat perubahan pada sebut harga sedia ada atau mencipta sebut harga versi baharu.

> [!NOTE]
> Selepas ciri untuk pengaktifan dan semakan sebut harga didayakan, ia tidak boleh dinyahdayakan.

Untuk menghidupkan keupayaan mengaktifkan dan menyemak sebut harga berdasarkan projek, ikut langkah ini.

1. Pergi ke **Tetapan** \> **Parameter**.
1. Buka rekod **Parameter**.
1. Pada anak tetingkap Tindakan, pada tab **Kawalan Ciri**, pilih **Dayakan pengaktifan dan semakan sebut harga**.
1. Dalam kotak dialog pengesahan, pilih **OK**.
1. Selepas beberapa ketika, segarkan semula pelayar anda. Keupayaan pengaktifan dan semakan kini patut tersedia. Anda akan tahu bahawa keupayaan ini telah didayakan jika butang **Dayakan pengaktifan dan semakan untuk sebut harga** tidak lagi muncul pada Anak Tetingkap Tindakan.

## <a name="activating-a-quote"></a>Mengaktifkan sebut harga

Selepas ciri untuk pengaktifan dan semakan sebut harga didayakan, butang **Tutup sebut harga sebagai menang** dan **Tutup sebut harga sebagai kalah** pada Anak Tetingkap Tindakan tidak tersedia untuk draf sebut harga projek. Butang ini hanya tersedia selepas sebut harga diaktifkan.

Pengaktifan mewakili peringkat dalam proses sebut harga apabila anda mahu menghalang lebih banyak perubahan pada sebut harga. Pada peringkat ini, sebut harga dihantar untuk semakan dalaman atau kepada pelanggan.

Butang **Tutup sebut harga sebagai menang** dan **Tutup sebut harga sebagai kalah** pada Anak Tetingkap Tindakan tersedia untuk sebut harga yang diaktifkan. Bergantung pada hasil semakan dalaman atau pelanggan, anda boleh menggunakan salah satu daripada butang ini untuk menutup sebut harga yang diaktifkan. Anda boleh membuat rundingan dan perubahan pada sebut harga yang diaktifkan dengan memilih **Semak sebut harga**.

## <a name="revising-a-quote"></a>Menyemak sebut harga

Jika anda mesti membuat perubahan pada sebut harga yang diaktifkan, pilih **Semak sebut harga**. Sebut harga ditutup dan kod sebab yang **disemak** digunakan. Sebut harga baharu yang mempunyai ID dan nombor semakan tambahan yang sama dicipta kemudiannya. Semua butiran daripada sebut harga asal disalin ke sebut harga baharu. Sebut harga baharu ialah dalam status draf dan boleh diedit seperti yang diperlukan.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
