---
title: Kesan aktual dalam penglibatan harga tetap
description: Artikel ini memberikan maklumat tentang kesan ke atas jadual Aktual pada pelbagai peristiwa semasa kitaran hayat penglibatan harga tetap dalam Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 50819d77d56935bfe5438d7d9dae99562bcc0b49
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918139"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Kesan aktual dalam penglibatan harga tetap

_**Gunakan pada:** Project Operations untuk senario berdasarkan sumber/bukan stok, Pelaksanaan ringan - urusan untuk penginvoisan proforma_

Jadual berikut menyenaraikan aktual jenis transaksi berbeza yang dicipta pada pelbagai peristiwa dalam penglibatan harga tetap.

| Peristiwa | Kos sebenar | Jualan sebenar belum dibilkan | Aktual jualan belum dibilkan | Contoh |
|---|---|---|---|---|
| Masa dicipta. | Tidak berkenaan | Tidak berkenaan | Tidak berkenaan | <p>Bob Kozack dari unit organisasi Fabrikam AS yang mempunyai kadar kos 100 Dolar AS (USD100) sejam, sedang mengusahakan projek yang dinamakan "Pemasangan Lengan di Adatum". Projek ini dipetakan kepada kaedah pengebilan harga tetap pada garisan kontrak. Berikut ialah sampel entri masa daripada Bob Kozak:</p><p>Bob Kozack - 8 jam</p> |
| Masa diserahkan. | Tidak berkenaan | Tidak berkenaan | Tidak berkenaan | Garisan jurnal kos untuk entri masa dicipta. Kadar kos lalai dimasukkan dalam entri jurnal. |
| Entri masa dipanggil semula sebelum diluluskan. | Tidak berkenaan | Tidak berkenaan | Tidak berkenaan | |
| Masa diluluskan. | Aktual kos dicipta. | Tidak berkenaan | Tidak berkenaan | <p>Aktual baharu yang dicipta:</p><ul><li>**Aktual kos:** Bob Kozack, 8 jam, USD800</li></ul> |
| Kelulusan masa dibatalkan. | <p>Status pelarasan aktual kos asal telah dikemas kini kepada **Dilaraskan**.</p><p>Aktual kos pembalikan yang mempunyai status pelarasan **Tidak boleh dilaraskan** dicipta.</p> | Tidak berkenaan | Tidak berkenaan | <p>Aktual sedia ada yang dikemas kini:</p><ul><li>**Aktual kos:** Bob Kozack, 8 jam, USD800, *Dilaraskan*</li></ul><p>Aktual baharu yang dicipta untuk membalikkan kesan kewangan sebelumnya:</p><ul><li>**Aktual kos:** Bob Kozack, (8 jam), (USD800), *Tidak boleh dilaraskan*</li></ul> |
| Entri masa dipanggil semula selepas diluluskan. | <p>Status pelarasan aktual kos asal telah dikemas kini kepada **Dilaraskan**.</p><p>Aktual kos pembalikan yang mempunyai status pelarasan **Tidak boleh dilaraskan** dicipta.</p> | Tidak berkenaan | Tidak berkenaan | <p>Aktual sedia ada yang dikemas kini:</p><ul><li>**Aktual kos:** Bob Kozack, 8 jam, USD800, *Dilaraskan*</li></ul><p>Aktual baharu yang dicipta untuk membalikkan kesan kewangan sebelumnya:</p><ul><li>**Aktual kos:** Bob Kozack, (8 jam), (USD800), *Tidak boleh dilaraskan*</li></ul> |
| Kontrak disahkan. | <p>Status pelarasan aktual kos lama telah dikemas kini kepada **Dilaraskan**.</p><p>Aktual kos pembalikan yang mempunyai status pelarasan **Tidak boleh dilaraskan** telah dicipta.</p><p>Aktual kos baharu dicipta selepas peraturan kontrak dinilai semula.</p> | Tidak berkenaan | Tidak berkenaan | <p>Aktual sedia ada yang dikemas kini:</p><ul><li>**Aktual kos:** Bob Kozack, 8 jam, USD800, *Dilaraskan*</li></ul><p>Aktual baharu yang dicipta untuk membalikkan kesan kewangan sebelumnya:</p><ul><li>**Aktual kos:** Bob Kozack, (8 jam), (USD800), *Tidak boleh dilaraskan*</li></ul><p>Aktual baharu yang dicipta untuk kesan kewangan yang dinilai semula:</p><ul><li>**Aktual kos:** Bob Kozack, 8 jam, USD800</li></ul> |
| Invois dicipta. | Tidak berkenaan | Tidak berkenaan | Tidak berkenaan | |
| Invois disahkan dengan pencapaian. | Tidak berkenaan | Tidak berkenaan | Aktual jualan dibilkan berdasarkan pencapaian baharu dicipta. | <p>Aktual sedia ada yang masih tidak berubah:</p><ul><li>**Aktual kos:** Bob Kozack, 8 jam, USD800</li></ul><p>Aktual baharu yang dicipta untuk merekodkan nilai jualan dibilkan:</p><ul><li>**Aktual jualan dibilkan:** Pencapaian, USD 5,000</li></ul> |
| Invois diperbetulkan untuk mengkreditkan pencapaian. | Tidak berkenaan | Tidak berkenaan | Aktual jualan dibilkan pembalikan dicipta. | <p>Aktual sedia ada yang masih tidak berubah:</p><ul><li>**Aktual kos:** Bob Kozack, 8 jam, 800 USD</li></ul><p>Aktual sedia ada yang dikemas kini:</p><ul><li>**Aktual jualan dibilkan:** Pencapaian, USD 5,000, *Dilaraskan*</li></ul><p>Aktual baharu yang dicipta untuk membalikkan nilai jualan dibilkan sebelumnya:</p><ul><li>**Aktual jualan dibilkan:** Pencapaian, (USD 5,000),*Tidak boleh dilaras*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
