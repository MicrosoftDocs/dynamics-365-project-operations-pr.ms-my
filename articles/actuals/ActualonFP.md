---
title: Kesan sebenar dalam penglibatan harga tetap
description: Topik ini memberikan maklumat tentang kesan pada jadual Sebenar pada pelbagai acara semasa kitaran hayat penglibatan harga tetap dalam Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 222e7c5eefd7c619e4d7389cdaff2f96176ff275
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579239"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Kesan sebenar dalam penglibatan harga tetap

_**Gunakan pada:** Project Operations untuk senario berdasarkan sumber/bukan stok, Pelaksanaan ringan - urusan untuk penginvoisan proforma_

Jadual berikut menyenaraikan sebenar jenis transaksi yang berbeza yang dibuat pada pelbagai acara dalam penglibatan harga tetap.

| Peristiwa | Kos sebenar | Jualan sebenar belum dibilkan | Jualan yang dibilkan sebenar | Contoh |
|---|---|---|---|---|
| Masa dicipta. | Tidak berkenaan | Tidak berkenaan | Tidak berkenaan | <p>Bob Kozack, dari unit organisasi Fabrikam AS yang mempunyai kadar kos 100 dolar AS (USD 100) sejam, sedang mengusahakan projek yang dinamakan "Pemasangan Senjata di Adatum." Projek ini dipetakan kepada kaedah pengebilan harga tetap pada baris kontrak. Berikut adalah contoh catatan waktu dari Bob Kozak:</p><p>Bob Kozack - 8 jam</p> |
| Masa dihantar. | Tidak berkenaan | Tidak berkenaan | Tidak berkenaan | Barisan jurnal kos dicipta untuk entri masa. Kadar kos lalai dimasukkan dalam entri jurnal. |
| Entri masa ditarik balik sebelum ia diluluskan. | Tidak berkenaan | Tidak berkenaan | Tidak berkenaan | |
| Masa diluluskan. | Kos sebenar dicipta. | Tidak berkenaan | Tidak berkenaan | <p>Sebenar baru yang dicipta:</p><ul><li>**Kos sebenar:** Bob Kozack, 8 jam, USD 800</li></ul> |
| Kelulusan masa dibatalkan. | <p>Status pelarasan kos asal sebenar dikemas kini kepada **Dilaraskan**.</p><p>Kos pembalikan sebenar dicipta yang mempunyai status **pelarasan Tidak boleh disesuaikan**.</p> | Tidak berkenaan | Tidak berkenaan | <p>Sebenar sedia ada yang dikemas kini:</p><ul><li>**Kos sebenar:** Bob Kozack, 8 jam, USD 800, *Dilaraskan*</li></ul><p>Sebenar baru yang dicipta untuk membalikkan kesan kewangan sebelumnya:</p><ul><li>**Kos sebenar:** Bob Kozack, (8 jam), (USD 800), *Tidak Boleh Disesuaikan*</li></ul> |
| Entri masa ditarik balik selepas ia diluluskan. | <p>Status pelarasan kos asal sebenar dikemas kini kepada **Dilaraskan**.</p><p>Kos pembalikan sebenar dicipta yang mempunyai status **pelarasan Tidak boleh disesuaikan**.</p> | Tidak berkenaan | Tidak berkenaan | <p>Sebenar sedia ada yang dikemas kini:</p><ul><li>**Kos sebenar:** Bob Kozack, 8 jam, USD 800, *Dilaraskan*</li></ul><p>Sebenar baru yang dicipta untuk membalikkan kesan kewangan sebelumnya:</p><ul><li>**Kos sebenar:** Bob Kozack, (8 jam), (USD 800), *Tidak Boleh Disesuaikan*</li></ul> |
| Kontrak itu disahkan. | <p>Status pelarasan sebenar kos lama dikemas kini kepada **Dilaraskan**.</p><p>Sebenar kos pembalikan dicipta yang mempunyai status **pelarasan Tidak boleh disesuaikan**.</p><p>Sebenar kos baru dicipta selepas peraturan kontrak dinilai semula.</p> | Tidak berkenaan | Tidak berkenaan | <p>Sebenar sedia ada yang dikemas kini:</p><ul><li>**Kos sebenar:** Bob Kozack, 8 jam, USD 800, *Dilaraskan*</li></ul><p>Sebenar baru yang dicipta untuk membalikkan kesan kewangan sebelumnya:</p><ul><li>**Kos sebenar:** Bob Kozack, (8 jam), (USD 800), *Tidak Boleh Disesuaikan*</li></ul><p>Sebenar baru yang dicipta untuk kesan kewangan yang dinilai semula:</p><ul><li>**Kos sebenar:** Bob Kozack, 8 jam, USD 800</li></ul> |
| Invois dicipta. | Tidak berkenaan | Tidak berkenaan | Tidak berkenaan | |
| Invois disahkan dengan tonggak. | Tidak berkenaan | Tidak berkenaan | Sebenar jualan bil berasaskan tonggak baru dicipta. | <p>Sebenar sedia ada yang kekal tidak berubah:</p><ul><li>**Kos sebenar:** Bob Kozack, 8 jam, USD 800</li></ul><p>Sebenar baru yang dicipta untuk merekodkan nilai jualan yang dibilkan:</p><ul><li>**Jualan yang dibilkan sebenar:** Milestone, USD 5,000</li></ul> |
| Invois diperbetulkan untuk mengkreditkan peristiwa penting. | Tidak berkenaan | Tidak berkenaan | Sebenar jualan yang dibilkan terbalik dicipta. | <p>Sebenar sedia ada yang kekal tidak berubah:</p><ul><li>**Kos sebenar:** Bob Kozack, 8 jam, 800 USD</li></ul><p>Sebenar sedia ada yang dikemas kini:</p><ul><li>**Jualan yang dibilkan sebenar:** Milestone, USD 5,000, *Dilaraskan*</li></ul><p>Sebenar baru yang dicipta untuk membalikkan nilai jualan yang dibilkan sebelumnya:</p><ul><li>**Jualan yang dibilkan sebenar:** Milestone, (USD 5,000), *Tidak boleh disesuaikan*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
