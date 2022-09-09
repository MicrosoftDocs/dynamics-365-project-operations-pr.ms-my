---
title: Mengaktifkan dan menyemak semula sebut harga projek
description: Artikel ini menyediakan maklumat tentang mengaktifkan dan menyemak semula petikan dalam Microsoft Dynamics 365 Project Operations.
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
# <a name="activate-and-revise-a-project-quote"></a>Mengaktifkan dan menyemak semula sebut harga projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Keupayaan pengaktifan dan semakan membantu anda menjejaki versi untuk sebut harga berasaskan projek semasa fasa anggaran dan rundingan. Apabila draf sebut harga diaktifkan, ia menjadi baca sahaja.

Keupayaan pengaktifan dan semakan membolehkan anda melaksanakan tugas berikut:

- Menang atau kehilangan sebut harga hanya selepas pengaktifan.
- Menyemak semula sebut harga untuk sama ada membuat perubahan pada sebut harga sedia ada atau mencipta versi baru.

> [!NOTE]
> Selepas ciri untuk pengaktifan dan semakan sebut harga didayakan, ia tidak boleh dinyahdayakan.

Untuk menghidupkan keupayaan untuk mengaktifkan dan menyemak semula sebut harga berasaskan projek, ikuti langkah-langkah ini.

1. Pergi ke **Parameter Tetapan** \> **·**.
1. **Buka rekod Parameter**.
1. Pada Anak Tetingkap Tindakan, pada tab **Kawalan** Ciri, pilih **Dayakan pengaktifan dan semakan sebut harga**.
1. Dalam kotak dialog pengesahan, pilih **OK**.
1. Selepas beberapa saat, muat semula penyemak imbas anda. Keupayaan pengaktifan dan semakan kini harus tersedia. Anda akan tahu bahawa keupayaan ini telah didayakan jika **butang Dayakan pengaktifan dan semakan sebut harga** tidak lagi muncul pada Anak Tetingkap Tindakan.

## <a name="activating-a-quote"></a>Mengaktifkan sebut harga

Selepas ciri untuk pengaktifan dan semakan sebut harga didayakan, **tutup sebut harga sebagai won** dan **Tutup sebut harga sebagai butang hilang** pada Anak Tetingkap Tindakan tidak tersedia untuk draf sebut harga projek. Mereka hanya boleh didapati selepas sebut harga diaktifkan.

Pengaktifan mewakili peringkat dalam proses sebut harga apabila anda ingin menghalang lebih banyak perubahan pada sebut harga. Pada peringkat ini, sebut harga dihantar untuk semakan dalaman atau kepada pelanggan.

Tutup **sebut harga sebagai menang** dan **Tutup sebut harga sebagai hilang** butang pada Anak Tetingkap Tindakan tersedia untuk sebut harga yang diaktifkan. Bergantung pada hasil semakan dalaman atau pelanggan, anda boleh menggunakan salah satu butang ini untuk menutup sebut harga yang diaktifkan. Anda boleh membuat rundingan dan perubahan pada sebut harga yang diaktifkan dengan **memilih Sebut harga** Semak semula.

## <a name="revising-a-quote"></a>Menyemak sebut harga

Jika anda mesti membuat perubahan pada sebut harga yang diaktifkan, pilih **Semak semula sebut harga**. Sebut harga ditutup, dan **kod sebab yang disemak** semula digunakan. Sebut harga baru kemudiannya dicipta yang mempunyai ID yang sama dan nombor semakan tambahan. Semua butiran dari sebut harga asal disalin ke sebut harga baru. Sebut harga baru berada dalam status draf dan boleh diedit mengikut keperluan.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
