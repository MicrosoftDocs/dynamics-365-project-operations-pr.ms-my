---
title: Semak invois yang tertunggak pada projek dan kontrak projek
description: Topik ini memberikan maklumat mengenai cara untuk mengkaji masa, perbelanjaan dan tunggakan produk, dan cara menandanya sebagai bersedia untuk penginvoisan.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: eb6d942d61bf8b5d20afb75c88716132a596bcbd
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081437"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Semak invois yang tertunggak pada projek dan kontrak projek

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Apabila transaksi bersedia untuk mempunyai invois yang dicipta dan diproses, transaksi sepatutnya ditanda **Bersedia untuk dinvois**. Topik ini menghuraikan jenis transaksi yang boleh dicipta.

## <a name="review-the-time-and-material-billing-backlog"></a>Semak semula tunggakan pengebilan masa dan bahan

Apabila masa kemasukan atau perbelanjaan diserahkan dan diluluskan untuk projek, PSA mewujudkan projek sebenar. Jika kombinasi projek dan kelas transaksi dipetakan ke satu baris kontrak untuk projek masa dan bahan, dua aktual dicipta apabila kemasukan diluluskan:

- Kos sebenar 
- Jualan sebenar belum dibilkan

Jualan sebenar yang belum dibilkan mewakili log pengebilan dan status pengebilan mereka mesti ditetapkan kepada **Bersedia untuk Diinvois**. Apabila invois projek dicipta, jualan sebenar yang tidak dibilkan yang ditandakan **Bersedia untuk Diinvois** disalin sebagai butiran baris invois.

Untuk menyemak tunggakan pengebilan untuk masa dan bahan, pergi ke **Jualan** \> **Pengebilan** \> **Tunggakan Pengebilan Masa dan Bahan**. Pilih semua aplikasi jualan yang tidak dibilkan yang bersedia untuk diinvois dan kemudian pilih **Bersedia untuk Diinvois.** Status pengebilan bagi aktual ini ditukar kepada **Bersedia untuk Diinvois**.

![Tunggakan pengebilan masa dan bahan](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Semak semula tunggakan pengebilan produk

Dalam PSA, apabila kontrak projek mempunyai talian kontrak berasaskan produk, baris tersebut dipertimbangkan untuk penginvoisan apabila invois dicipta untuk kontrak projek. Sebarang produk yang mempunyai baris kontrak yang ditanda **Bersedia untuk Diinvois** disalin ke invois projek sebagai baris invois projek.

Untuk menyemak tunggakan pengebilan untuk produk, pergi ke **Jualan** \> **Pengebilan** \> **Tunggakan Pengebilan Produk**. Pilih semua baris kontrak berdasarkan produk yang bersedia untuk diinvois dan kemudian pilih **Bersedia untuk Diinvois.** Status pengebilan baris ini ditukar kepada **Bersedia untuk Diinvois**.

![Tunggakan pengebilan produk](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Tinjauan pencapaian pengebilan pada kontrak harga tetap

Setiap baris kontrak projek yang mempunyai kaedah pengebilan harga tetap mesti mentakrifkan pencapaian kontrak. Pencapaian kontrak ini hanya boleh diinvois hanya jika ia ditandakan **Bersedia untuk Diinvois**. 

Untuk menyemak semula pencapaian pengebilan, pergi ke **Jualan** \> **Pengebilan** \> **Pencapaian Harga Tetap**. Pilih semua pencapaian yang bersedia untuk diinvois dan kemudian pilih **Bersedia untuk diinvois.** Status pengebilan pencapaian ini ditukar kepada **Bersedia untuk Diinvois**.

![Pencapaian harga tetap](media/FPBacklog.png)
