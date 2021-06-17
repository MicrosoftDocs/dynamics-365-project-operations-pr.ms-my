---
title: Perbelanjaan antara syarikat
description: Topik ini menyediakan maklumat tentang cara untuk menggunakan perbelanjaan antara syarikat untuk menguntukkan perbelanjaan pekerja kepada entiti undang-undang yang mana kerja tersebut dilaksanakan.
author: ShylaThompson
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2cdba8d5368a8b26bf4d98226bda76a58261cf0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005082"
---
# <a name="intercompany-expenses"></a>Perbelanjaan antara syarikat

Pekerja yang diupah oleh satu entiti sah dalam organisasi mungkin melaksanakan kerja untuk entiti sah yang lain dalam organisasi yang sama. Anda boleh menggunakan perbelanjaan antara syarikat untuk menguntukkan perbelanjaan pekerja kepada entiti undang-undang yang mana kerja tersebut dilaksanakan. Entiti sah yang mengupah pekerja dipanggil sebagai entiti sah peminjaman. Entiti sah yang pekerja menanggung perbelanjaan dipanggil entiti sah pinjaman. 

Sebelum pekerja boleh mencipta dan menyerahkan perbelanjaan antara syarikat, anda mestilah mendayakan baris perbelanjaan antara syarikat. Dalam entiti undang-undang peminjaman, pada halaman **Parameter pengurusan perbelanjaan**, pilih **Benarkan baris perbelanjaan antara syarikat**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Penyiaran cukai untuk perbelanjaan antara syarikat

[!include [banner](../includes/banner.md)]

Sebelum anda boleh menggunakan kumpulan cukai yang dikaitkan dengan entiti undang-undang (sumber) peminjaman dan bukannya entiti undang-undang (destinasi) pinjaman dalam laporan perbelanjaan anda, anda mestilah mendayakan kefungsian dalam persediaan cukai jualan lejar Am. Apabila parameter **Entiti undang-undang untuk penyiaran cukai antara syarikat** ditetapkan kepada **Sumber** dan **Gunakan peraturan pencukaian cukai jualan** ditetapkan kepada **Tidak**, gabungan cukai untuk entiti undang-undang peminjaman digunakan. Apabila parameter yang sama ditetapkan kepada **Destinasi**, gabungan cukai untuk entiti sah pinjaman akan digunakan. Untuk entiti sah di Amerika Syarikat, apabila parameter ditetapkan kepada **Sumber**, medan **Cukai jualan boleh diterima** juga mesti dikonfigurasikan pada halaman  **Kumpulan penyiaran lejar**. Enjin perakaunan akan menggunakan maklumat daripada medan ini untuk entri perakaunan berkaitan cukai.   
Tingkah laku ini konsisten untuk baris perbelanjaan yang disiarkan dengan atau tanpa projek.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]