---
title: Perkara baharu September 2022 - Pelaksanaan Project Operations lite
description: Artikel ini menyediakan maklumat tentang kemas kinian kualiti yang tersedia dalam keluaran Penggunaan Microsoft Dynamics 365 Project Operations lite keluaran September 2022.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 2cce7ae25f05258e8bf0bab9430324bc9b30e329
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621353"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Perkara baharu September 2022 - Pelaksanaan Project Operations lite

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Artikel ini digunakan pada komponen dan versi Microsoft Dynamics 365 Project Operations berikut :

- Operasi Projek dalam Dataverse versi persekitaran 4.46.0.60

## <a name="features-included-in-this-release"></a>Ciri yang disertakan dalam keluaran ini

| Bahagian ciri | Nama ciri | Maklumat lanjut |
| --- | --- | --- |
| Pengurusan Peluang | **Semakan dan Pengaktifan Sebut Harga**<br>Operasi Projek membawa sokongan penuh proses jualan. Petikan projek boleh diaktifkan untuk mewakili keadaan di mana sebut harga adalah baca sahaja dan sedang disemak. Sebut harga diaktifkan boleh disemak semula untuk mencipta sebut harga baru yang mempunyai nombor semakan tambahan. Sebut harga projek yang diaktifkan atau semakan sebut harga boleh ditutup sebagai menang atau hilang. | [Aktifkan dan semak sebut harga projek](/dynamics365/project-operations/sales/activation-and-revision) |
| Pengebilan dan Penentuan Harga | **Harga agnostik zon masa lalai**<br>Operasi Projek telah memperkenalkan konsep tarikh agnostik zon masa pada semua projek sebenar. Medan baru, **Tarikh** transaksi, kini boleh didapati di baris jurnal dan sebenar, dan akan digunakan untuk menyimpan tarikh apabila transaksi berlaku, tetapi tanpa menukar tarikh itu kepada Masa Universal Yang Diselaraskan. Tarikh ini akan digunakan untuk proses hiliran seperti lalai harga dan penciptaan invois. | <p>[Tentukan kadar kos untuk anggaran berasaskan projek dan sebenar](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Tentukan harga jualan untuk anggaran berasaskan projek dan sebenar](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Pengebilan dan Penentuan Harga | **Penggantian harga efektif tarikh dalam Operasi Projek**<br>Penggantian harga efektif memberikan cara untuk mengatasi atau mengubah harga tertentu dalam senarai harga. | [Penggantian harga efektif tarikh](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Masa dan Perbelanjaan | **Pelulus Global**<br>Ciri ini membolehkan vendor perisian bebas (ISV) dan kelulusan berpusat, tanpa mengira projek atau status ahli pasukan dalam projek. | [Keselamatan dan kelulusan](/dynamics365/project-operations/approvals/approvals-security) |

## <a name="quality-updates"></a>Kemas kini kualiti

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Pengebilan dan Penentuan Harga | 2754422 | Anggaran Bahan dan Perbelanjaan tidak mengalir ke Dynamics 365 Finance apabila projek disalin masuk Dataverse. |
| Masa dan Perbelanjaan | 2787409 | Pelulus yang tidak sah boleh meluluskan kemasukan masa bukan projek. |
| Pengurusan Peluang | 2788907 | Mesej ralat yang dikemas kini mengenai pengesahihan keunikan untuk baris pesanan yang termasuk bendera. |
| Masa dan Perbelanjaan | 2842253 | Pengendalian pengecualian nol untuk kelulusan masa. |
| Pengebilan dan Penentuan Harga | 2844181 | Kegagalan untuk mendapatkan penciptaan invois blok ID korelasi. |
| Pengebilan dan Penentuan Harga | 2876628 | QLD, CLD - Anggar resolusi senarai harga harus menggunakan medan julat tarikh warisan senarai harga. |
| Subkontrak | 2893222 | Jika tiada peranan ditentukan untuk garis subkontrak, anda boleh memilih baris tersebut pada ahli pasukan untuk sebarang peranan. |
