---
title: Kesan sebenar untuk projek dalaman
description: Artikel ini memberikan maklumat mengenai kesan pada jadual Sebenar di pelbagai acara untuk projek dalaman di Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: de05714c079fe121ef68e28b1acb82c24bce095e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921359"
---
# <a name="actuals-impact-for-an-internal-project"></a>Kesan sebenar untuk projek dalaman

_**Gunakan pada:** Project Operations untuk senario berdasarkan sumber/bukan stok, Pelaksanaan ringan - urusan untuk penginvoisan proforma_

Jadual berikut menyenaraikan sebenar jenis transaksi yang berbeza yang dibuat pada pelbagai acara dalam penglibatan projek dalaman.

| Peristiwa | Kos sebenar | Contoh |
|---|---|---|
| Masa dicipta. | Tidak berkenaan | <p>Bob Kozack, dari unit organisasi Fabrikam AS yang mempunyai kadar kos 100 dolar AS (USD 100) sejam, sedang mengusahakan projek yang dinamakan "Pemasangan Senjata di Adatum." Projek ini dipetakan kepada kaedah pengebilan harga tetap pada baris kontrak. Berikut adalah contoh catatan waktu dari Bob Kozak:</p><p>Bob Kozack - 8 jam</p> |
| Masa dihantar. | Tidak berkenaan | Barisan jurnal kos dicipta untuk entri masa. Kadar kos lalai dimasukkan dalam entri jurnal. |
| Entri masa ditarik balik sebelum ia diluluskan. | Tidak berkenaan | |
| Masa diluluskan. | Kos sebenar dicipta. | <p>Sebenar baru yang dicipta:</p><ul><li>**Kos sebenar:** Bob Kozack, 8 jam, USD 800</li></ul> |
| Kelulusan masa dibatalkan. | <p>Status pelarasan kos asal sebenar dikemas kini kepada **Dilaraskan**.</p><p>Kos pembalikan sebenar dicipta yang mempunyai status **pelarasan Tidak boleh disesuaikan**.</p> | <p>Sebenar sedia ada yang dikemas kini:</p><ul><li>**Kos sebenar:** Bob Kozack, 8 jam, USD 800, *Dilaraskan*</li></ul><p>Sebenar baru yang dicipta untuk membalikkan kesan kewangan sebelumnya:</p><ul><li>**Kos sebenar:** Bob Kozack, (8 jam), (USD 800), *Tidak Boleh Disesuaikan*</li></ul> |
| Entri masa ditarik balik selepas ia diluluskan. | <p>Status pelarasan kos asal sebenar dikemas kini kepada **Dilaraskan**.</p><p>Kos pembalikan sebenar dicipta yang mempunyai status **pelarasan Tidak boleh disesuaikan**.</p> | <p>Sebenar sedia ada yang dikemas kini:</p><ul><li>**Kos sebenar:** Bob Kozack, 8 jam, USD 800, *Dilaraskan*</li></ul><p>Sebenar baru yang dicipta untuk membalikkan kesan kewangan sebelumnya:</p><ul><li>**Kos sebenar:** Bob Kozack, (8 jam), (USD 800), *Tidak Boleh Disesuaikan*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
