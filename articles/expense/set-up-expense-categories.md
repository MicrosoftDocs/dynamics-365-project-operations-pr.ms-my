---
title: Sediakan kategori perbelanjaan
description: Topik ini memberikan maklumat tentang cara menyediakan kategori perbelanjaan dan kategori dikongsi untuk laporan perbelanjaan.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896697"
---
# <a name="set-up-expense-categories"></a>Sediakan kategori perbelanjaan

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Apabila pekerja cipta laporan perbelanjaan, setiap perbelanjaan yang mereka rekod mesti dikaitkan dengan kategori perbelanjaan. Kategori perbelanjaan diperoleh daripada kategori dikongsi yang boleh dikongsi merentasi entiti yang sah dalam organisasi anda. Bergantung pada cara organisasi anda ditakrifkan, kategori perbelanjaan ini juga boleh dikongsi di kawasan lain. Berdasarkan definisi organisasi dan panduan anda daripada pasukan pelaksanaan, anda mesti menentukan sama ada kategori yang digunakan dalam Pengurusan perbelanjaan akan digunakan hanya dalam Pengurusan perbelanjaan atau harus dikongsi di kawasan lain.

> [!NOTE]
> Kategori ini boleh dikongsi di antara Pengurusan projek dan perakaunan dan Pengurusan perbelanjaan, atau antara Pengurusan projek dan perakaunan dan Pengeluaran. Walau bagaimanapun, ia tidak boleh dikongsi antara Pengurusan perbelanjaan dan Pengeluaran.

Sebelum anda boleh memulakan proses persediaan, keputusan berikut mesti dibuat untuk setiap kategori perbelanjaan:

- Apakah itu kategori perbelanjaan? Contohnya termasuk kategori untuk penerbangan, hotel, atau perbatuan.
- Bolehkah kategori perbelanjaan juga digunakan dalam Pengurusan projek dan perakaunan? Jika ia boleh, anda juga mesti membuat keputusan berikut:

    - Akaun kos manakah akan digunakan untuk perbelanjaan yang berikut?

        - Kos
        - Peruntukan gaji
        - WIP-nilai kos
        - Kos-item
        - WIP-nilai kos-item
        - Kerugian terakru
        - WIP-kerugian terakru

    - Akaun hasil manakah yang akan digunakan untuk sumber hasil berikut?

        - Hasil diinvois
        - Hasil terakru-nilai jualan
        - WIP-nilai jualan
        - Hasil terakru-pengeluaran
        - WIP-pengeluaran
        - Hasil terakru-keuntungan
        - WIP-keuntungan
        - Hasil terakru-langganan
        - WIP-langganan

- Apakah itu jenis perbelanjaan?
- Apakah itu kaedah pembayaran lalai untuk kategori perbelanjaan?
- Adakah perbelanjaan dalam kategori perbelanjaan perlu diperincikan?
- Apakah itu akaun lalai utama untuk kategori perbelanjaan?
- Apakah itu kumpulan cukai jualan item lalai untuk kategori perbelanjaan?
- Adakah kaedah pembayaran tambahan dibenarkan untuk kategori perbelanjaan? Jika ya, apakah itu?
- Adakah terdapat subkategori dalam kategori perbelanjaan ini? Jika terdapat subkategori, anda juga mesti membuat keputusan berikut:

    - Adakah sebarang subkategori dikecualikan daripada pemulihan cukai?
    - Apakah itu kumpulan cukai jualan item subkategori?
