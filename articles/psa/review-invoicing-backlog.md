---
title: Semak invois yang tertunggak pada projek dan kontrak projek
description: Topik ini memberikan maklumat mengenai cara untuk mengkaji masa, perbelanjaan dan tunggakan produk, dan cara menandanya sebagai bersedia untuk penginvoisan.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 51a7ecfefcc20544f5be378a347e3568285cafb3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600569"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Semak invois yang tertunggak pada projek dan kontrak projek

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Apabila transaksi bersedia untuk mempunyai invois yang dicipta dan diproses, transaksi sepatutnya ditanda **Bersedia untuk dinvois**. Topik ini menghuraikan jenis transaksi yang boleh dicipta.

## <a name="review-the-time-and-material-billing-backlog"></a>Semak semula tunggakan pengebilan masa dan bahan

Apabila masa kemasukan atau perbelanjaan diserahkan dan diluluskan untuk projek, PSA mewujudkan projek sebenar. Jika kombinasi projek dan kelas transaksi dipetakan ke satu baris kontrak untuk projek masa dan bahan, dua aktual dicipta apabila kemasukan diluluskan:

- Kos sebenar 
- Jualan sebenar belum dibilkan

Jualan sebenar yang belum dibilkan mewakili log pengebilan dan status pengebilan mereka mesti ditetapkan kepada **Bersedia untuk Diinvois**. Apabila invois projek dicipta, jualan sebenar yang tidak dibilkan yang ditandakan **Bersedia untuk Diinvois** disalin sebagai butiran baris invois.

Untuk menyemak tunggakan pengebilan untuk masa dan bahan, pergi ke **Jualan** \> **Pengebilan** \> **Tunggakan Pengebilan Masa dan Bahan**. Pilih semua aplikasi jualan yang tidak dibilkan yang bersedia untuk diinvois dan kemudian pilih **Bersedia untuk Diinvois.** Status pengebilan bagi aktual ini ditukar kepada **Bersedia untuk Diinvois**.

![Tunggakan pengebilan masa dan bahan.](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Semak semula tunggakan pengebilan produk

Dalam PSA, apabila kontrak projek mempunyai talian kontrak berasaskan produk, baris tersebut dipertimbangkan untuk penginvoisan apabila invois dicipta untuk kontrak projek. Sebarang produk yang mempunyai baris kontrak yang ditanda **Bersedia untuk Diinvois** disalin ke invois projek sebagai baris invois projek.

Untuk menyemak tunggakan pengebilan untuk produk, pergi ke **Jualan** \> **Pengebilan** \> **Tunggakan Pengebilan Produk**. Pilih semua baris kontrak berdasarkan produk yang bersedia untuk diinvois dan kemudian pilih **Bersedia untuk Diinvois.** Status pengebilan baris ini ditukar kepada **Bersedia untuk Diinvois**.

![Tunggakan pengebilan produk.](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Tinjauan pencapaian pengebilan pada kontrak harga tetap

Setiap baris kontrak projek yang mempunyai kaedah pengebilan harga tetap mesti mentakrifkan pencapaian kontrak. Pencapaian kontrak ini hanya boleh diinvois hanya jika ia ditandakan **Bersedia untuk Diinvois**. 

Untuk menyemak semula pencapaian pengebilan, pergi ke **Jualan** \> **Pengebilan** \> **Pencapaian Harga Tetap**. Pilih semua pencapaian yang bersedia untuk diinvois dan kemudian pilih **Bersedia untuk diinvois.** Status pengebilan pencapaian ini ditukar kepada **Bersedia untuk Diinvois**.

![Pencapaian harga tetap.](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
