---
title: Kesan aktual semasa peringkat prajualan sesebuah penglibatan
description: Artikel ini memberikan maklumat tentang kesan ke atas jadual Aktual pada pelbagai peristiwa semasa penglibatan berada dalam peringkat prajualan dalam Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: d03d6ac2154806189d0d9d0b232bb317f51071ba
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922371"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Kesan aktual semasa peringkat prajualan sesebuah penglibatan

_**Gunakan pada:** Project Operations untuk senario berdasarkan sumber/bukan stok, Pelaksanaan ringan - urusan untuk penginvoisan proforma_

Jadual berikut menyenaraikan aktual jenis transaksi berbeza yang dicipta pada pelbagai peristiwa semasa peringkat prajualan penglibatan projek.

| Peristiwa | Kos sebenar | Contoh |
|---|---|---|
| Masa dicipta. | Tidak berkenaan | <p>Bob Kozack dari unit organisasi Fabrikam AS yang mempunyai kadar kos 100 Dolar AS (USD100) sejam, sedang mengusahakan projek yang dinamakan "Pemasangan Lengan di Adatum". Projek ini dipetakan kepada kaedah pengebilan harga tetap pada garisan kontrak. Berikut ialah sampel entri masa daripada Bob Kozak:</p><p>Bob Kozack - 8 jam</p> |
| Masa diserahkan. | Tidak berkenaan | Garisan jurnal kos untuk entri masa dicipta. Kadar kos lalai dimasukkan dalam entri jurnal. |
| Entri masa dipanggil semula sebelum diluluskan. | Tidak berkenaan | |
| Masa diluluskan. | Aktual kos dicipta. | <p>Aktual baharu yang dicipta:</p><ul><li>**Aktual kos:** Bob Kozack, 8 jam, USD800</li></ul> |
| Kelulusan masa dibatalkan. | <p>Status pelarasan aktual kos asal telah dikemas kini kepada **Dilaraskan**.</p><p>Aktual kos pembalikan yang mempunyai status pelarasan **Tidak boleh dilaraskan** dicipta.</p> | <p>Aktual sedia ada yang dikemas kini:</p><ul><li>**Aktual kos:** Bob Kozack, 8 jam, USD800, *Dilaraskan*</li></ul><p>Aktual baharu yang dicipta untuk membalikkan kesan kewangan sebelumnya:</p><ul><li>**Aktual kos:** Bob Kozack, (8 jam), (USD800), *Tidak boleh dilaraskan*</li></ul> |
| Entri masa dipanggil semula selepas diluluskan. | <p>Status pelarasan aktual kos asal telah dikemas kini kepada **Dilaraskan**.</p><p>Aktual kos pembalikan yang mempunyai status pelarasan **Tidak boleh dilaraskan** dicipta.</p> | <p>Aktual sedia ada yang dikemas kini:</p><ul><li>**Aktual kos:** Bob Kozack, 8 jam, USD800, *Dilaraskan*</li></ul><p>Aktual baharu yang dicipta untuk membalikkan kesan kewangan sebelumnya:</p><ul><li>**Aktual kos:** Bob Kozack, (8 jam), (USD800), *Tidak boleh dilaraskan*</li></ul> |
| Sebut harga dimenangi dan kontrak dicipta. | <p>Status pelarasan aktual kos lama telah dikemas kini kepada **Dilaraskan**.</p><p>Aktual kos pembalikan yang mempunyai status pelarasan **Tidak boleh dilaraskan** telah dicipta.</p><p>Aktual kos baharu dicipta selepas peraturan kontrak dinilai semula.</p> | <p>Aktual sedia ada yang dikemas kini:</p><ul><li>**Aktual kos:** Bob Kozack, 8 jam, USD800, *Dilaraskan*</li></ul><p>Aktual baharu yang dicipta untuk membalikkan kesan kewangan sebelumnya:</p><ul><li>**Aktual kos:** Bob Kozack, (8 jam), (USD800), *Tidak boleh dilaraskan*</li></ul><p>Aktual baharu yang dicipta untuk kesan kewangan yang dinilai semula apabila sebut harga dimenangi dan kontrak dicipta:</p><ul><li>**Aktual kos:** Bob Kozack, 8 jam, USD800</li><li>**Aktual jualan yang tidak dibilkan:** Bob Kozack, 8 jam, USD1,600</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
