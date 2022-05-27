---
title: Kesan sebenar semasa peringkat pra-jualan penglibatan
description: Topik ini memberikan maklumat tentang kesan pada jadual Sebenar pada pelbagai acara semasa engagment berada di peringkat pra-jualan dalam Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: ad62639b345d5519b103d4bde3fbb033b9a7a519
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577247"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Kesan sebenar semasa peringkat pra-jualan penglibatan

_**Gunakan pada:** Project Operations untuk senario berdasarkan sumber/bukan stok, Pelaksanaan ringan - urusan untuk penginvoisan proforma_

Jadual berikut menyenaraikan sebenar jenis transaksi yang berbeza yang dibuat pada pelbagai acara semasa peringkat pra-jualan penglibatan projek.

| Peristiwa | Kos sebenar | Contoh |
|---|---|---|
| Masa dicipta. | Tidak berkenaan | <p>Bob Kozack, dari unit organisasi Fabrikam AS yang mempunyai kadar kos 100 dolar AS (USD 100) sejam, sedang mengusahakan projek yang dinamakan "Pemasangan Senjata di Adatum." Projek ini dipetakan kepada kaedah pengebilan harga tetap pada baris kontrak. Berikut adalah contoh catatan waktu dari Bob Kozak:</p><p>Bob Kozack - 8 jam</p> |
| Masa dihantar. | Tidak berkenaan | Barisan jurnal kos dicipta untuk entri masa. Kadar kos lalai dimasukkan dalam entri jurnal. |
| Entri masa ditarik balik sebelum ia diluluskan. | Tidak berkenaan | |
| Masa diluluskan. | Kos sebenar dicipta. | <p>Sebenar baru yang dicipta:</p><ul><li>**Kos sebenar:** Bob Kozack, 8 jam, USD 800</li></ul> |
| Kelulusan masa dibatalkan. | <p>Status pelarasan kos asal sebenar dikemas kini kepada **Dilaraskan**.</p><p>Kos pembalikan sebenar dicipta yang mempunyai status **pelarasan Tidak boleh disesuaikan**.</p> | <p>Sebenar sedia ada yang dikemas kini:</p><ul><li>**Kos sebenar:** Bob Kozack, 8 jam, USD 800, *Dilaraskan*</li></ul><p>Sebenar baru yang dicipta untuk membalikkan kesan kewangan sebelumnya:</p><ul><li>**Kos sebenar:** Bob Kozack, (8 jam), (USD 800), *Tidak Boleh Disesuaikan*</li></ul> |
| Entri masa ditarik balik selepas ia diluluskan. | <p>Status pelarasan kos asal sebenar dikemas kini kepada **Dilaraskan**.</p><p>Kos pembalikan sebenar dicipta yang mempunyai status **pelarasan Tidak boleh disesuaikan**.</p> | <p>Sebenar sedia ada yang dikemas kini:</p><ul><li>**Kos sebenar:** Bob Kozack, 8 jam, USD 800, *Dilaraskan*</li></ul><p>Sebenar baru yang dicipta untuk membalikkan kesan kewangan sebelumnya:</p><ul><li>**Kos sebenar:** Bob Kozack, (8 jam), (USD 800), *Tidak Boleh Disesuaikan*</li></ul> |
| Petikan dimenangi, dan kontrak dibuat. | <p>Status pelarasan sebenar kos lama dikemas kini kepada **Dilaraskan**.</p><p>Sebenar kos pembalikan dicipta yang mempunyai status **pelarasan Tidak boleh disesuaikan**.</p><p>Sebenar kos baru dicipta selepas peraturan kontrak dinilai semula.</p> | <p>Sebenar sedia ada yang dikemas kini:</p><ul><li>**Kos sebenar:** Bob Kozack, 8 jam, USD 800, *Dilaraskan*</li></ul><p>Sebenar baru yang dicipta untuk membalikkan kesan kewangan sebelumnya:</p><ul><li>**Kos sebenar:** Bob Kozack, (8 jam), (USD 800), *Tidak Boleh Disesuaikan*</li></ul><p>Sebenar baru yang dicipta untuk kesan kewangan yang dinilai semula apabila sebut harga dimenangi dan kontrak dibuat:</p><ul><li>**Kos sebenar:** Bob Kozack, 8 jam, USD 800</li><li>**Jualan yang tidak dibilkan sebenar:** Bob Kozack, 8 jam, USD 1,600</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
