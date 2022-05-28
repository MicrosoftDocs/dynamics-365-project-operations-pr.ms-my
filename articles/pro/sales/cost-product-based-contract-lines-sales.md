---
title: Kos baris kontrak berasaskan produk - ringan
description: Topik ini menyediakan maklumat tentang penciptaan
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3def4c330dc9aadbf5ff806ef7682fbfd1072e4b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599281"
---
# <a name="cost-product-based-contract-lines---lite"></a>Kos baris kontrak berasaskan produk - ringan

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_


Baris kontrak berdasarkan produk dalam Dynamics 365 Project Operations termasuk medan **Harga Kos**, yang menyimpan harga kos bagi produk untuk pengiraan keuntungan hiliran.

Apabila baris kontrak berdasarkan produk dicipta untuk produk katalog, kos baris lalai daripada medan **Kos Standard** dalam katalog produk. Medan **Kos Standard** dalam katalog produk ditetapkan dalam mata wang asas Organisasi. Apabila unit kos lalai pada baris kontrak, ia ditukar ke dalam mata wang jualan pada kontrak.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Kos unit pada barisan kontrak berasaskan produk

Mempunyai kos unit pada baris kontrak berasaskan produk membenarkan untuk kos produk yang berbeza bagi setiap jualan. Walaupun tidak semestinya perlu, terdapat senario tertentu yang kos produk mungkin didiskaunkan kepada pelanggan oleh pembekal. Pertimbangkan senario yang berikut:

Fabrikam Robotics sedang memasang lengan robotik pada barisan pemasangan Adatum Corporation. Fabrikam menyediakan perkhidmatan pemasangan tetapi lengan robot adalah daripada Trey Reserarch. Jika pemasangan lengan robotik di Adatum Corporation membuka industri menegak baharu bagi Trey Research, ia boleh menawarkan diskaun istimewa untuk urusan ini kepada Fabrikam. Dalam hal ini, Fabrikam mencipta baris kontrak berdasarkan produk untuk Lengan Robot. Kos seunit dimasukkan untuk kontrak ini. Kos adalah berbeza daripada kos lengan robot daripada Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]