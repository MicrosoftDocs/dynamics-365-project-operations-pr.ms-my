---
title: Sediakan kadar kos dan jualan untuk produk katalog - ringan
description: Topik ini memberikan maklumat tentang cara menetapkan kadar kos dan jualan untuk item dalam katalog produk.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176712"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Sediakan kadar kos dan jualan untuk produk katalog - ringan

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_


Menyediakan penetapan harga untuk item katalog produk dalam Dynamics 365 Project Operations adalah sama seperti dalam Dynamics 365 Sales.

Oleh kerana produk tidak dapat dianggarkan atau digunakan pada projek dalam Operasi Projek, jadi tidak perlu menetapkan harga katalog produk pada senarai harga projek untuk sebut harga dan kontrak.

Harga katalog produk perlu disediakan dalam medan **Harga Produk** bagi sebut harga, kontrak atau akaun. Jangan sediakan harga katalog produk dalam senarai harga projek untuk entiti ini. Senarai harga projek adalah eksklusif untuk Operasi Projek. Terdapat logik perniagaan khusus aplikasi yang menyalin senarai harga daripada sebut harga kepada kontrak. Hasilnya ialah senarai harga projek khusus kontrak. Operasi salinan boleh melambatkan proses memenangi sebut harga jika senarai harga projek pada sebut harga terlalu besar. Senarai harga produk tidak disalin untuk mencipta senarai harga tersuai pada kontrak. Ini bermaksud bahawa senarai harga produk tidak akan memberi kesan pada prestasi proses memenangi sebut harga.
