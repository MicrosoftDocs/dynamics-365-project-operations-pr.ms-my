---
title: Penetapan kos baris kontrak berdasarkan produk
description: Topik ini menyediakan maklumat tentang penciptaan
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/20/2020
ms.locfileid: "4081459"
---
# <a name="costing-product-based-contract-lines"></a>Penetapan kos baris kontrak berdasarkan produk

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_


Baris kontrak berasaskan produk dalam Dynamics 365 Project Operations termasuk medan **Harga Kos** yang menyimpan harga kos produk untuk pengiraan keberuntungan hiliran.

Apabila baris kontrak berasaskan produk dicipta untuk produk katalog, kos baris kontrak berasaskan produk lalai daripada medan **Kos Standard** dalam katalog produk. Medan **Kos Standard** dalam katalog produk ditetapkan dalam mata wang asas Organisasi. Apabila unit kos lalai pada baris kontrak, ia ditukar ke dalam mata wang jualan pada kontrak.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Kos unit pada barisan kontrak berasaskan produk

Mempunyai kos unit pada baris kontrak berasaskan produk membenarkan untuk kos produk yang berbeza bagi setiap jualan. Walaupun tidak semestinya perlu, terdapat senario tertentu yang kos produk mungkin didiskaunkan kepada pelanggan oleh pembekal. Pertimbangkan senario yang berikut:

Fabrikam Robotics sedang memasang lengan robotik pada barisan pemasangan Adatum Corporation. Fabrikam menyediakan perkhidmatan pemasangan tetapi lengan robotik diperoleh daripada Trey Research. Jika pemasangan lengan robotik di Adatum Corporation membuka industri menegak baharu bagi Trey Research, ia boleh menawarkan diskaun istimewa untuk urusan ini kepada Fabrikam. Dalam kes ini, Fabrikam mencipta baris kontrak berasaskan produk untuk Lengan Robotik dan menginput kos mengikut unit untuk kontrak ini yang berbeza daripada kos standard lengan robotik daripada Trey Research.
