---
title: Perbelanjaan antara syarikat
description: Pekerja yang diupah oleh satu entiti sah dalam organisasi mungkin melaksanakan kerja untuk entiti sah yang lain dalam organisasi yang sama. Dalam situasi ini, anda boleh menggunakan ciri perbelanjaan antara syarikat untuk menugaskan perbelanjaan pekerja kepada entiti sah yang dilaksanakan kerja oleh pekerja tersebut.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081379"
---
# <a name="intercompany-expenses"></a>Perbelanjaan antara syarikat

[!include [banner](../includes/banner.md)]

Pekerja yang diupah oleh satu entiti sah dalam organisasi mungkin melaksanakan kerja untuk entiti sah yang lain dalam organisasi yang sama. Dalam situasi ini, anda boleh menggunakan ciri perbelanjaan antara syarikat untuk menugaskan perbelanjaan pekerja kepada entiti sah yang dilaksanakan kerja oleh pekerja tersebut. Entiti sah yang mengupah pekerja dipanggil sebagai entiti sah peminjaman. Entiti sah yang pekerja menanggung perbelanjaan dipanggil entiti sah pinjaman. 

Sebelum pekerja boleh mencipta dan menyerahkan perbelanjaan untuk kerja dilaksanakan untuk entiti sah yang berbeza, dalam entiti sah peminjaman, pada halaman **Parameter pengurusan perbelanjaan** , pilih pilihan **Benarkan baris perbelanjaan antara syarikat**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Penyiaran cukai untuk perbelanjaan antara syarikat

[!include [banner](../includes/banner.md)]

Jika anda mahu menggunakan kumpulan cukai yang dikaitkan dengan entiti sah peminjaman (sumber) dan bukannya entiti sah pinjaman (destinasi) dalam laporan perbelanjaan anda, anda akan perlu mengkonfigurasikan ciri ini dalam persediaan cukai jualan Lejar am. Apabila parameter Lejar am, **Entiti sah untuk penyiaran cukai antara syarikat** ditetapkan kepada **Sumber** dan **Gunakan peraturan pencukaian cukai jualan** ditetapkan kepada **Tidak** , gabungan cukai untuk entiti sah peminjaman akan digunakan. Apabila parameter yang sama ditetapkan kepada **Destinasi** , gabungan cukai untuk entiti sah pinjaman akan digunakan. Untuk entiti sah di Amerika Syarikat, apabila parameter ditetapkan kepada **Sumber** , medan **Cukai jualan boleh diterima** juga mesti dikonfigurasikan pada halaman  **Kumpulan penyiaran lejar**. Enjin perakaunan akan menggunakan maklumat daripada medan ini untuk entri perakaunan berkaitan cukai.   
Tingkah laku ini konsisten untuk baris perbelanjaan yang disiarkan dengan atau tanpa projek.  
