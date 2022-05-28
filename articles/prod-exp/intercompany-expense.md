---
title: Perbelanjaan antara syarikat
description: Topik ini menyediakan maklumat tentang cara untuk menggunakan perbelanjaan antara syarikat untuk menguntukkan perbelanjaan pekerja kepada entiti undang-undang yang mana kerja tersebut dilaksanakan.
author: suvaidya
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6788a590879bd839ebb9dedc45895dc047cc9f15
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684245"
---
# <a name="intercompany-expenses"></a>Perbelanjaan antara syarikat

Pekerja yang diupah oleh satu entiti sah dalam organisasi mungkin melaksanakan kerja untuk entiti sah yang lain dalam organisasi yang sama. Anda boleh menggunakan perbelanjaan antara syarikat untuk menguntukkan perbelanjaan pekerja kepada entiti undang-undang yang mana kerja tersebut dilaksanakan. Entiti sah yang mengupah pekerja dipanggil sebagai entiti sah peminjaman. Entiti sah yang pekerja menanggung perbelanjaan dipanggil entiti sah pinjaman. 

Sebelum pekerja boleh mencipta dan menyerahkan perbelanjaan antara syarikat, anda mestilah mendayakan baris perbelanjaan antara syarikat. Dalam entiti undang-undang peminjaman, pada halaman **Parameter pengurusan perbelanjaan**, pilih **Benarkan baris perbelanjaan antara syarikat**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Penyiaran cukai untuk perbelanjaan antara syarikat

[!include [banner](../includes/banner.md)]

Sebelum anda boleh menggunakan kumpulan cukai yang dikaitkan dengan entiti undang-undang (sumber) peminjaman dan bukannya entiti undang-undang (destinasi) pinjaman dalam laporan perbelanjaan anda, anda mestilah mendayakan kefungsian dalam persediaan cukai jualan lejar Am. Apabila parameter **Entiti undang-undang untuk penyiaran cukai antara syarikat** ditetapkan kepada **Sumber** dan **Gunakan peraturan pencukaian cukai jualan** ditetapkan kepada **Tidak**, gabungan cukai untuk entiti undang-undang peminjaman digunakan. Apabila parameter yang sama ditetapkan kepada **Destinasi**, gabungan cukai untuk entiti sah pinjaman akan digunakan. Untuk entiti sah di Amerika Syarikat, apabila parameter ditetapkan kepada **Sumber**, medan **Cukai jualan boleh diterima** juga mesti dikonfigurasikan pada halaman  **Kumpulan penyiaran lejar**. Enjin perakaunan akan menggunakan maklumat daripada medan ini untuk entri perakaunan berkaitan cukai.   
Tingkah laku ini konsisten untuk baris perbelanjaan yang disiarkan dengan atau tanpa projek.  

## <a name="new-expense-expression-builder"></a>Pembina ungkapan perbelanjaan baru

Pembina ungkapan perbelanjaan baru menangani masalah dengan senario perbelanjaan antara syarikat yang menggunakan projek. Ciri ini memastikan bahawa, apabila anda mencipta perbelanjaan antara syarikat, dasar perbelanjaan disahkan dengan betul terhadap projek yang dipilih pada baris perbelanjaan, dan bahawa laporan perbelanjaan boleh berjaya diserahkan.

Untuk ciri pembina ungkapan perbelanjaan berfungsi, ia mesti dihidupkan. Selain itu, dasar perbelanjaan yang mempunyai ID projek perlu disediakan.

Jika anda sudah mengkonfigurasi dasar yang mengesahkan ID projek pada baris perbelanjaan, dasar tersebut mesti dihentikan. Anda kemudian boleh menghidupkan ciri dan mengkonfigurasi semula dasar tersebut.

Untuk menghidupkan ciri tersebut, ikuti langkah ini.

1. Pergi ke **Ruang kerja** \> **Pengurusan Ciri**.
2. Dalam senarai, pilih **Pembangun ungkapan perbelanjaan baru untuk menangani masalah dengan senario perbelanjaan antara syarikat yang menggunakan projek**. Kemudian pilih **Dayakan sekarang**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
