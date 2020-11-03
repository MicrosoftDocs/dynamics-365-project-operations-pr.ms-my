---
title: Hapuskan anggaran projek
description: Topik ini menyediakan maklumat tentang cara menghapuskan anggaran projek selepas ia selesai.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 8bda8a7357e883b948449b2a19bea476996dde3c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081281"
---
# <a name="eliminate-a-project-estimate"></a>Hapuskan anggaran projek

[!include [banner](../includes/banner.md)]

Anggaran projek memberikan pandangan kewangan untuk kerja yang dianggarkan dan dijadualkan untuk projek. Untuk menggunakan anggaran untuk projek, anda mesti melampirkan projek kepada projek anggaran. Projek anggaran sentiasa berdasarkan projek yang sedia ada, namun berbilang projek boleh merujuk kepada satu projek anggaran. Hanya projek harga tetap dan pelaburan boleh dilampirkan kepada projek anggaran, dan projek tersebut mesti tergolong dalam kumpulan projek yang sama dengan projek anggaran.

Untuk menghapuskan projek anggaran, ia mesti dilengkapkan. Langkah berikut menerangkan cara untuk menghapuskan anggaran.

1. Pergi **Pengurusan dan perakaunan projek** > **Semua Projek** dan buka projek. 
2. Pada tab **Uruskan** , pilih **Anggaran** , dan pada halaman **Anggaran** , pilih **Hapuskan**.
3. Pada halaman **Hapuskan anggaran** pada tab **Umum** , tetapan pilihan berikut:

   - **Kod tempoh** : Pilih kod tempoh untuk memilih projek anggaran yang sewajarnya. 
   - **Tarikh anggaran** : Pilih tarikh anggaran yang sewajarnya untuk penghapusan.
   - **Hapuskan dengan amaran WIP** : Dayakan pilihan ini untuk memberikan pemberitahuan apabila anggaran yang dikaitkan dengan kerja yang sedang dijalankan (WIP) akan dihapuskan. Apabila pilihan ini tidak didayakan, penghapusan tidak dapat diteruskan jika mana-mana transaksi bukan anggaran wujud. 
   > [!NOTE]
   > Pilihan ini hanya tersedia apabila penghapusan digunakan pada projek anggaran. Ia tidak tersedia jika anda menggunakan penyiaran berkala. Tetapan ini berfungsi dengan tetapan pada tab **Anggaran** pada halaman **Parameter projek** , dalam kumpulan medan **Benarkan penghapusan apabila transaksi bukan anggaran wujud**.
   - **Tetapkan peringkat kepada Selesai** : Dayakan pilihan ini untuk menetapkan peringkat projek anggaran kepada **Selesai** selepas anda menjalankan penghapusan.
   - **Cetak senarai anggaran** : Pilih maklumat yang akan disertakan apabila senarai anggaran dicetak.
   - **Tunjukkan Log Maklumat** : Dayakan pilihan ini untuk memaparkan Log Maklumat.
   - **Tarikh penyiaran** : Pilih tarikh penyiaran lejar anggaran.

4.  Pilih **OK**.
5. Selepas proses penghapusan selesai, projek anggaran yang dihapuskan akan dipaparkan dengan nilai negatif. 

Jika anda tidak berniat untuk menghapuskan anggaran, anda boleh memilih anggaran yang dihapuskan dan pilih **Buat balik penghapusan**.   
