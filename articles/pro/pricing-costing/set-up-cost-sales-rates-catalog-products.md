---
title: Sediakan kadar kos dan jualan untuk produk katalog - ringan
description: Topik ini memberikan maklumat tentang cara menetapkan kadar kos dan jualan untuk item dalam katalog produk.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e851193df8151821e112e01a9f33df5afee7df7
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764568"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Sediakan kadar kos dan jualan untuk produk katalog - ringan

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_


Menyediakan harga untuk item katalog produk dalam Dynamics 365 Project Operations adalah sama seperti dalam Dynamics 365 Sales.

Dalam Project Operations, produk tidak boleh dianggarkan atau digunakan pada projek, maka harga katalog produk tidak perlu ditetapkan pada senarai harga projek untuk sebut harga dan kontrak.

Gunakan medan **Harga Produk** bagi sebut harga, kontrak atau akaun untuk menyediakan harga katalog produk. Jangan sediakan harga katalog produk dalam senarai harga projek. Senarai harga projek adalah eksklusif untuk Operasi Projek. Logik perniagaan khusus aplikasi menyalin senarai harga daripada sebut harga kepada kontrak. Hasilnya ialah senarai harga projek khusus kontrak. Operasi salinan boleh melambatkan proses memenangi sebut harga jika senarai harga projek pada sebut harga terlalu besar. Senarai harga produk tidak disalin untuk mencipta senarai harga tersuai pada kontrak. Disebabkan tiada salinan yang terlibat, prestasi proses sebut harga tidak terjejas.
