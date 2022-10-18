---
title: Perkara baharu September 2022 - Pelaksanaan Project Operations lite
description: Artikel ini menyediakan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran penggunaan Microsoft lite keluaran Dynamics 365 Project Operations September 2022.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: a02ac7a69489bc7974eb0e63c11fa5de74795b78
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634864"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Perkara baharu September 2022 - Pelaksanaan Project Operations lite

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Artikel ini digunakan pada komponen dan versi Microsoft Dynamics 365 Project Operations berikut:

- Operasi Projek dalam versi persekitaran 4.46.0.60 Dataverse

## <a name="features-included-in-this-release"></a>Ciri yang disertakan dalam keluaran ini

| Bahagian ciri | Nama ciri | Maklumat lanjut |
| --- | --- | --- |
| Pengurusan Peluang | **Semakan dan Pengaktifan Sebut Harga**<br>Operasi Projek membawa sokongan penuh proses jualan. Petikan projek boleh diaktifkan untuk mewakili keadaan di mana sebut harga dibaca sahaja dan sedang disemak. Sebut harga yang diaktifkan boleh disemak semula untuk membuat sebut harga baru yang mempunyai nombor semakan tambahan. Sebut harga projek yang diaktifkan atau semakan sebut harga boleh ditutup sebagai menang atau hilang. | [Aktifkan dan semak sebut harga projek](/dynamics365/project-operations/sales/activation-and-revision) |
| Pengebilan dan Penentuan Harga | **Lalai harga agnostik zon masa**<br>Operasi Projek telah memperkenalkan konsep tarikh agnostik zon waktu pada semua projek sebenar. Satu bidang baru, Tarikh **transaksi, kini boleh didapati di baris jurnal dan sebenar, dan akan digunakan untuk menyimpan tarikh apabila transaksi berlaku,** tetapi tanpa menukar tarikh itu kepada Masa Universal yang Diselaraskan. Tarikh ini akan digunakan untuk proses hiliran seperti lalai harga dan penciptaan invois. | <p>[Tentukan kadar kos untuk anggaran dan realiti berasaskan projek](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Menentukan harga jualan untuk anggaran dan realiti berasaskan projek](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Pengebilan dan Penentuan Harga | **Penggantian harga tarikh efektif dalam Operasi Projek**<br>Penggantian harga tarikh efektif menyediakan cara untuk mengatasi atau menukar harga tertentu dalam senarai harga. | [Penggantian harga efektif tarikh](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Masa dan Perbelanjaan | **Pelulus Global**<br>Ciri ini membolehkan vendor perisian bebas (ISV) dan kelulusan berpusat, tanpa mengira projek atau status ahli pasukan dalam projek. | [Keselamatan dan kelulusan](/dynamics365/project-operations/approvals/approvals-security) |
|Perancangan dan Penjejakan Projek|**Gunakan API jadual Projek untuk melaksanakan operasi dengan entiti Penjadualan** </br> </br>Kontur penugasan sumber mengedit API mari pembangun secara programatik menentukan usaha penerima serah tugas merentasi sebarang julat tarikh yang disokong untuk perancangan usaha berperingkat masa yang lebih terperinci.|[Gunakan API jadual Projek untuk melaksanakan operasi dengan entiti Penjadualan](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Kemas kini kualiti

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Pengebilan dan Penentuan Harga | 2754422 | Anggaran Bahan dan Perbelanjaan tidak mengalir ke Dynamics 365 Finance apabila projek disalin Dataverse. |
| Masa dan Perbelanjaan | 2787409 | Pelulus yang tidak sah boleh meluluskan kemasukan masa bukan projek. |
| Pengurusan Peluang | 2788907 | Mesej ralat yang dikemas kini pada pengesahan keunikan untuk baris pesanan yang termasuk bendera. |
| Masa dan Perbelanjaan | 2842253 | Pengendalian pengecualian nol untuk kelulusan masa. |
| Pengebilan dan Penentuan Harga | 2844181 | Kegagalan untuk mendapatkan penciptaan invois blok ID korelasi. |
| Pengebilan dan Penentuan Harga | 2876628 | QLD, CLD - Anggaran resolusi senarai harga harus menggunakan medan julat tarikh warisan senarai harga. |
| Subkontrak | 2893222 | Jika tiada peranan ditentukan untuk baris subkontrak, adalah mungkin untuk memilih baris itu pada ahli pasukan untuk sebarang peranan. |
