---
title: Penetapan kos baris sebut harga berdasarkan produk
description: Topik ini memberikan maklumat tentang penerapan harga kos pada sebut harga berdasarkan produk.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d21ab159294cac66ffeb8abcf0943b4babd7b360
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118935"
---
# <a name="costing-product-based-quote-lines"></a>Penetapan kos baris sebut harga berdasarkan produk

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_


Baris sebut harga berasaskan produk dalam Operasi Projek Dynamics 365 juga mempunyai medan **Harga Kos**. Medan ini digunakan untuk menjejaki harga kos untuk produk pada baris sebut harga dan untuk pengiraan keuntungan hiliran.

Apabila baris sebut harga berdasarkan produk dicipta untuk produk katalog, kos baris sebut harga berdasarkan produk ditetapkan daripada medan **Kos Standard** dalam katalog produk. Medan kos standard dalam katalog produk ditetapkan dalam mata wang asas Organisasi. Kos unit lalai pada baris sebut harga berasaskan produk ditukar kepada mata wang jualan pada sebut harga.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Kos unit pada barisan sebut harga berasaskan produk

Tujuan mempunyai kos unit pada baris sebut harga berasaskan produk ialah untuk membolehkan kos yang berbeza untuk produk untuk setiap jualan. Ini bukan senario biasa, tetapi kadangkala kos produk mungkin didiskaunkan oleh pembekal bergantung pada pelanggan jualan akhir.

Contohnya:

Fabrikam Robotics sedang memasang lengan robot pada barisan pemasangan Datum Corporation. Fabrikam menyediakan perkhidmatan pemasangan tetapi lengan robot diperolehi daripada Trey robotics. Jika pemasangan senjata robot di sebuah Datum Corporation membuka industri baru menegak untuk lengan robot Trey, Trey boleh memberikan diskaun khas untuk urusan ini ke Fabrikam.

Dalam kes ini, Fabrikam akan mencipta talian sebut harga berdasarkan produk untuk Senjata Robot dan masukkan kos khas bagi setiap unit untuk sebut harga ini. Kos ini berbeza daripada kos Standard Lengan Robot Trey.
