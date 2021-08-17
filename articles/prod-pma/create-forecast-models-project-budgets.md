---
title: Cipta model ramalan untuk belanjawan projek
description: Topik ini menerangkan cara untuk mencipta model ramalan untuk belanjawan selebihnya.
author: Yowelle
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: c4467bc1c687b028f1cce8280c3cf0b5ef492b6fd1a024d49f001ce5ff8a34cb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986007"
---
# <a name="create-forecast-models-for-project-budgets"></a>Cipta model ramalan untuk belanjawan projek 

[!include [banner](../includes/banner.md)]

Topik ini menerangkan cara untuk mencipta model ramalan untuk belanjawan selebihnya. Projek yang tertakluk kepada kawalan belanjawan menggunakan dua jenis belanjawan: asal dan selebihnya. Apabila anda mencipta belanjawan projek, anda mesti menentukan model ramalan belanjawan asal dan selebihnya yang dicipta dalam halaman **Model ramalan**. Belanjawan projek berdasarkan model yang ditentukan dicipta apabila anda melaksanakan belanjawan projek.

> [!NOTE]
> Model ramalan yang digunakan untuk kawalan belanjawan tidak boleh mempunyai submodel atau digunakan sebagai submodel.

1. Pilih **Pengurusan dan perakaunan projek** > **Penyediaan** > **Ramalan**  > **Model ramalan**.
2. Pilih **Baharu** untuk mencipta model ramalan baharu dan kemudian masukkan nombor ID model dan nama untuk model baharu itu. 
3. Tetapkan pilihan **Berhenti** kepada **Ya** untuk mengelakkan sebarang perubahan pada baris ramalan untuk model ramalan. 
4. Jika baris ramalan yang dikaitkan dengan model tersebut sepatutnya menjana ramalan aliran tunai dalam lejar umum, tetapkan **Sertakan dalam Ramalan aliran tunai** kepada **Ya.** 
5. Untuk menggunakan tarikh projek sebagai tarikh invois, tetapkan **Tarikh Invoice Ramalan** kepada **Ya**. 
6. Dalam medan **Jenis belanjawan**, pilih salah satu daripada jenis model berikut:

   - **Belanjawan asal**: Gunakan jumlah belanjawan asal yang dilaksanakan apabila belanjawan awal dicipta dan diluluskan.
   - **Belanjawan selebihnya**: Gunakan jumlah belanjawan selebihnya semasa hayat projek. Baki dalam model ramalan ini dikurangkan dengan transaksi sebenar dan ditambah atau dikurangkan mengikut semakan belanjawan.
   - **Bawa ke hadapan**: Gunakan jumlah belanjawan dibawa ke hadapan untuk projek. Bawa ke hadapan ialah satu proses pilihan yang boleh dijalankan untuk memindahkan jumlah belanjawan yang tidak digunakan daripada satu tahun fiskal kepada tahun fiskal yang lain.

7. Tetapkan pilihan berikut mengikut keperluan:

   - Dayakan **Tarikh invois ramalan** untuk menggunakan tarikh projek sebagai tarikh invois.
   - Dayakan **Ramalan dengan WIP** untuk meramal berdasarkan kerja yang sedang berjalan (WIP) dan kemudian, pilih jenis WIP. 
   - Anda boleh mengekalkan **Jenis belanjawan** lalai sebagai **Tiada** atau masukkan jenis baharu. Jenis belanjawan tidak boleh ditukar selepas anda menukar rekod.     
    > [!NOTE]
    > Jika anda menukar jenis belanjawan lalai, semua pilihan lain tidak akan tersedia untuk kemas kini dan anda tidak boleh menggunakan semula model ramalan ini. 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]