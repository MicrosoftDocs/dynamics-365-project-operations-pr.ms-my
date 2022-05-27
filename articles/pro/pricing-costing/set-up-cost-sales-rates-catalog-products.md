---
title: Sediakan kadar kos dan jualan untuk produk katalog - ringan
description: Topik ini memberikan maklumat tentang cara menetapkan kadar kos dan jualan untuk item dalam katalog produk.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 12e09d99e9832c93c3aea34ec0d4488cdf6b02fa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576833"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Sediakan kadar kos dan jualan untuk produk katalog - ringan

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_


Menyediakan harga untuk item katalog produk dalam Dynamics 365 Project Operations adalah sama seperti dalam Dynamics 365 Sales.

Dalam Project Operations, produk tidak boleh dianggarkan atau digunakan pada projek, maka harga katalog produk tidak perlu ditetapkan pada senarai harga projek untuk sebut harga dan kontrak.

Gunakan medan **Harga Produk** bagi sebut harga, kontrak atau akaun untuk menyediakan harga katalog produk. Jangan sediakan harga katalog produk dalam senarai harga projek. Senarai harga projek adalah eksklusif untuk Operasi Projek. Logik perniagaan khusus aplikasi menyalin senarai harga daripada sebut harga kepada kontrak. Hasilnya ialah senarai harga projek khusus kontrak. Operasi salinan boleh melambatkan proses memenangi sebut harga jika senarai harga projek pada sebut harga terlalu besar. Senarai harga produk tidak disalin untuk mencipta senarai harga tersuai pada kontrak. Disebabkan tiada salinan yang terlibat, prestasi proses sebut harga tidak terjejas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]