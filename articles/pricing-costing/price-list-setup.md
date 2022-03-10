---
title: Sediakan senarai harga
description: Topik ini memberikan maklumat tentang cara untuk sediakan senarai harga jualan dan kos.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 227e9a6f0ce6fd3fa1c2b0bd9afa014a3ec4f9758ead0dfb408156535692575c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009497"
---
# <a name="set-up-price-lists"></a>Sediakan senarai harga

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Senarai harga dalam Dynamics 365 Project Operations mewakili katalog kadar. Kadar menyatakan kos, jualan, dan kadar bil. Bergantung pada sama ada senarai harga menyatakan kadar kos atau jualan dan kadar bil, konteks senarai harga adalah **Jualan** atau **Kos**.

Sambungan berikut adalah khusus untuk Project Operations dan digunakan pada senarai harga daripada Dynamics 365 Sales.

- **Konteks**: Medan ini mempunyai nilai yang disokong, **Kos** dan **Jualan**. Nilai, **Belian** adalah tidak disokong. Tetapkan konteks kepada **Kos** untuk membuat senarai harga kos atau tetapkan konteks kepada **Jualan** untuk senarai harga jualan. Senarai harga kos selesaikan harga bagi jenis kos pada anggaran dan rekod sebenar. Senarai harga jualan selesaikan harga pada anggaran dan rekod sebenar jenis jualan yang belum dibilkan dan dibilkan.
- **Unit Masa**: Ini adalah unit lalai masa yang harga ditetapkan dalam jadual **Harga Peranan** yang berkaitan untuk senarai harga ini.
- **Entiti Senarai Harga**: Medan tersembunyi ini adalah oleh Project Operations untuk membezakan senarai harga yang sebut harga atau khusus kontrak daripada digunakan yang standard dan peringkat global.

## <a name="price-list-header"></a>Pengepala senarai harga

Jadual berikut termasuk medan pada tab senarai harga **Umum** yang unik pada Project Operations atau mempunyai perubahan ketara dalam tingkah laku daripada senarai harga dalam Jualan.

| Medan | Lokasi | Penerangan | Kesan hiliran |
| --- | --- | --- | --- |
| Nama | Tab **Umum** dan borang **Cipta Pantas** | Identiti senarai harga. | Senarai harga ditunjukkan dengan nilai ini pada semua halaman senarai dan pilihan juntai bawah.|
| Konteks | Tab **Umum** dan borang **Cipta Pantas** | Medan ini boleh ditetapkan kepada **Kos** atau **Jualan**. | Senarai harga ditetapkan kepada **Kos** adalah digunakan untuk mencari harga untuk anggaran kos dan kos sebenar. Senarai harga ditetapkan kepada **Jualan** adalah digunakan untuk mencari harga untuk anggaran jualan dan jualan sebenar. Hanya senarai harga yang mempunyai konteks ditetapkan kepada **Jualan** boleh dilampirkan ke senarai harga projek untuk pelanggan, sebut harga projek, dan kontrak projek. |
| Tarikh Mula | Tab **Umum** dan borang **Cipta Pantas** | Tarikh mula tempoh senarai harga berkuat kuasa. | Dengan medan **Tarikh Akhir**, medan ini digunakan untuk menentukan senarai harga yang berkenaan digunakan untuk anggaran tertentu atau baris sebenar. |
| Tarikh Tamat | Tab **Umum** dan borang **Cipta Pantas** | Tarikh akhir tempoh senarai harga berkuat kuasa. | Dengan medan **Tarikh Mula**, medan ini digunakan untuk menentukan senarai harga yang berkenaan digunakan untuk anggaran tertentu atau baris sebenar. |
| Mata wang | Tab **Umum** dan borang **Cipta Pantas** | Medan ini digunakan untuk melalaikan mata wang pada setiap peranan, kategori, atau baris item senarai harga yang berkaitan dengan senarai harga ini. | Pada senarai harga, peranan, kategori, atau baris item senarai harga **Jualan** tidak boleh dicipta dalam sebarang mata wang selain daripada mata wang ini. Pada senarai harga **Kos**, anda boleh mencipta baris harga peranan dalam sebarang mata wang. Mata wang yang ditakrifkan di sini digunakan sebagai lalai. Persediaan pengguna yang berkaitan dengan harga peranan boleh ganti nilai ini untuk mendayakan persediaan kadar kos buruh dalam sebarang mata wang. Kategori kadar kos dan kos item senarai harga boleh ditetapkan hanya dalam mata wang yang ditakrifkan di sini. |
| Unit Masa | Tab **Umum** dan borang **Cipta Pantas** | Medan ini digunakan untuk melalaikan unit masa pada setiap baris peranan yang berkaitan dengan senarai harga ini. | Nilai medan ini hanya digunakan pada persediaan harga peranan yang berkaitan. Pada senarai harga **Kos** dan **Jualan**, anda boleh mencipta baris harga peranan dalam sebarang unit masa. Unit masa yang ditakrifkan di sini digunakan sebagai lalai. Persediaan pengguna yang berkaitan dengan harga peranan boleh ganti nilai ini untuk mendayakan persediaan kadar kos buruh dan kadar bil dalam sebarang unit masa. |
| Penerangan | Tab **Umum** dan borang **Cipta Pantas** | Medan teks ini membenarkan anda untuk memberikan perihalan berbilang baris senarai harga. | Medan ini ditunjukkan dalam pandangan **Berkaitan** pada senarai harga dalam pelbagai entiti yang mempunyai senarai harga berkaitan.. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]