---
title: Perkara baharu September 2022 - Pelaksanaan Project Operations lite
description: Artikel ini menyediakan maklumat tentang kemas kini kualiti yang tersedia pada bulan September 2022 keluaran pelaksanaan Microsoft Dynamics 365 Project Operations lite.
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

- Project Operations dalam persekitaran Dataverse versi 4.46.0.60

## <a name="features-included-in-this-release"></a>Ciri yang disertakan dalam keluaran ini

| Bahagian ciri | Nama ciri | Maklumat lanjut |
| --- | --- | --- |
| Pengurusan Peluang | **Semakan dan Pengaktifan Sebut Harga**<br>Project Operations membawa sokongan penuh proses jualan. Sebut harga projek boleh diaktifkan untuk mewakili keadaan yang sebut harga adalah dalam format baca sahaja dan sedang disemak. Sebut harga aktif boleh disemak semula untuk mencipta sebut harga baharu yang mempunyai nombor semakan ditambah. Sebut harga projek aktif atau semakan sebut harga boleh ditutup sebagai menang atau hilang. | [Aktifkan dan semak sebut harga projek](/dynamics365/project-operations/sales/activation-and-revision) |
| Pengebilan dan Penentuan Harga | **Penetapan nilai lalai harga agnostik zon waktu**<br>Project Operations telah memperkenalkan konsep tarikh agnostik zon waktu pada semua projek aktual. Medan baharu, **Tarikh transaksi**, kini tersedia pada garisan jurnal dan aktual, dan akan digunakan untuk menyimpan tarikh apabila transaksi berlaku, tetapi tanpa menukar tarikh tersebut kepada Waktu Sejagat Selaras. Tarikh ini akan digunakan untuk proses hiliran seperti penetapan nilai lalai harga dan penciptaan invois. | <p>[Tentukan kadar kos untuk anggaran berdasarkan projek dan aktual](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Tentukan harga jualan untuk anggaran berdasarkan dan aktual](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Pengebilan dan Penentuan Harga | **Harga tarikh kuat kuasa mengganti dalam Project Operations**<br>Membatalkan harga tarikh kuat kuasa memberikan cara untuk menganti atau mengubah harga tertentu dalam senarai harga. | [Penggantian harga tarikh kuat kuasa](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Masa dan Perbelanjaan | **Pelulus Global**<br>Ciri ini mendayakan vendor perisian bebas (ISV) dan kelulusan berpusat, tanpa mengira status projek atau ahli pasukan dalam projek. | [Keselamatan dan kelulusan](/dynamics365/project-operations/approvals/approvals-security) |
|Perancangan dan Penjejakan Projek|**Gunakan API jadual Projek untuk melaksanakan operasi dengan entiti Penjadualan** </br> </br>API pengeditan kontur tugas sumber membolehkan pembangun menyatakan usaha penerima tugas secara programatik merentasi mana-mana julat tarikh yang disokong untuk lebih banyak butiran fasa masa perancangan usaha.|[Gunakan API jadual Projek untuk melaksanakan operasi dengan entiti Penjadualan](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Kemas kini kualiti

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Pengebilan dan Penentuan Harga | 2754422 | Anggaran Bahan dan Perbelanjaan tidak mengalir ke Dynamics 365 Finance apabila projek disalin dalam Dataverse. |
| Masa dan Perbelanjaan | 2787409 | Pelulus yang tidak sah boleh meluluskan entri masa bukan projek. |
| Pengurusan Peluang | 2788907 | Mesej ralat yang dikemas kini pada pensahihan keunikan untuk baris pesanan yang termasuk bendera. |
| Masa dan Perbelanjaan | 2842253 | Pengecualian pengendalian tidak sah untuk kelulusan masa. |
| Pengebilan dan Penentuan Harga | 2844181 | Kegagalan untuk mendapatkan ID korelasi menyekat penciptaan invois. |
| Pengebilan dan Penentuan Harga | 2876628 | QLD, CLD - Anggaran resolusi senarai harga harus menggunakan medan julat tarikh legasi senarai harga. |
| Pemberian subkontrak | 2893222 | Jika tiada peranan ditetapkan untuk baris subkontrak, jadi baris tersebut boleh dipilih pada ahli pasukan untuk sebarang peranan. |
