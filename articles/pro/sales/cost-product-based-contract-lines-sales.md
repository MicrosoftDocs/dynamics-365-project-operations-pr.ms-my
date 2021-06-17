---
title: Kos baris kontrak berasaskan produk - ringan
description: Topik ini menyediakan maklumat tentang penciptaan
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9458a57863244a68359f57185325c03a46bd6569
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003552"
---
# <a name="cost-product-based-contract-lines---lite"></a>Kos baris kontrak berasaskan produk - ringan

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_


Baris kontrak berdasarkan produk dalam Dynamics 365 Project Operations termasuk medan **Harga Kos**, yang menyimpan harga kos bagi produk untuk pengiraan keuntungan hiliran.

Apabila baris kontrak berdasarkan produk dicipta untuk produk katalog, kos baris lalai daripada medan **Kos Standard** dalam katalog produk. Medan **Kos Standard** dalam katalog produk ditetapkan dalam mata wang asas Organisasi. Apabila unit kos lalai pada baris kontrak, ia ditukar ke dalam mata wang jualan pada kontrak.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Kos unit pada barisan kontrak berasaskan produk

Mempunyai kos unit pada baris kontrak berasaskan produk membenarkan untuk kos produk yang berbeza bagi setiap jualan. Walaupun tidak semestinya perlu, terdapat senario tertentu yang kos produk mungkin didiskaunkan kepada pelanggan oleh pembekal. Pertimbangkan senario yang berikut:

Fabrikam Robotics sedang memasang lengan robotik pada barisan pemasangan Adatum Corporation. Fabrikam menyediakan perkhidmatan pemasangan tetapi lengan robot adalah daripada Trey Reserarch. Jika pemasangan lengan robotik di Adatum Corporation membuka industri menegak baharu bagi Trey Research, ia boleh menawarkan diskaun istimewa untuk urusan ini kepada Fabrikam. Dalam hal ini, Fabrikam mencipta baris kontrak berdasarkan produk untuk Lengan Robot. Kos seunit dimasukkan untuk kontrak ini. Kos adalah berbeza daripada kos lengan robot daripada Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]