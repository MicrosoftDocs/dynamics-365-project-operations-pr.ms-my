---
title: Matikan dimensi penetapan harga
description: Topik ini menyediakan maklumat tentang cara mematikan dimensi penetapan harga.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3d9f0cb2a054941b07809b61ca14a3145c6d6d06acd6ca40255d5ec9de92be22
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994512"
---
# <a name="turning-off-a-pricing-dimension"></a>Matikan dimensi penetapan harga

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Anda mungkin perlu menyemak semula dan mengemas kini strategi penetapan harga setiap beberapa tahun. Sebarang kemas kini yang anda lakukan mungkin memerlukan anda memadamkan dimensi penetapan harga yang sedia ada dan mencipta satu yang baharu. Sebagai contoh, anda mungkin telah memilih lebih banyak **Peranan** tetapi kini anda telah memutuskan harga mengikut **Pengalaman Kerja**. Ini mungkin memerlukan anda mematikan **Peranan** sebagai dimensi penetapan harga dan mencipta **Pengalaman Kerja** sebagai dimensi penetapan harga baharu. 

Mematikan dimensi penetapan harga, tanpa mengira jika ia di luar kotak atau tersuai, boleh dilakukan dengan menetapkan medan **Digunakan pada Kos** dan **Diguna pada Jualan** Dimensi Penetapan Harga ke **Tidak**.

Walau bagaimanapun, apabila anda melakukannya, anda mungkin menerima message ralat, **Dimensi penetapan harga tidak boleh dikemas kini atau dipadam jika terdapat rekod harga yang berkaitan.**

![Ralat Proses Perniagaan mungkin berlaku apabila memadamkan dimensi penentuan harga.](media/Business-Process-Error.png)

Mesej ralat ini menunjukkan bahawa terdapat rekod harga yang ditetapkan sebelum ini untuk dimensi yang sedang dipadamkan. Semua **Harga Peranan** dan **Tokokan Harga Peranan** yang merujuk kepada dimensi mesti dipadamkan sebelum kebolehgunaan dimensi boleh ditetapkan ke **Tidak**. Peraturan ini diguna pakai untuk kedua-dua dimensi penetapan harga luar kotak dan sebarang dimensi penetapan harga tersuai yang anda telah cipta. Sebab pengesahan ini adalah kerana rekod **Harga Peranan** masing-masing mesti mempunyai kombinasi dimensi yang unik. Sebagai contoh, pada senarai harga yang dipanggil **Kadar Kos 2018 AS**, anda mempunyai baris harga **Peranan harga**. 

| Tajuk Standard         | Unit Organisasi    |Unit   |Harga  |Mata wang  |
| -----------------------|-------------|-------|-------|----------|
| Jurutera sistem|Contoso AS|Jam| 100|USD|
| Jurutera Sistem Senior|Contoso AS|Jam| 150| USD|


Apabila anda mematikan **Tajuk Standard** sebagai dimensi penetapan harga dan enjin penetapan harga mencari harga, ianya akan hanya menggunakan nilai **Unit Organisasi** daripada konteks input. Jika **Unit Organisasi** konteks input ialah "Contoso AS", hasilnya tidak akan ditentukan kerana kedua-dua baris akan sepadan. Untuk mengelakkan senario ini, apabila anda mencipta rekod **Harga Peranan**, sistem mengesahkan bahawa kombinasi dimensi adalah unik. Jika dimensi telah dimatikan selepas rekod **Peranan Harga** dicipta, kekangan ini boleh dilanggar. Oleh itu, ia adalah diperlukan bahawa sebelum anda mematikan dimensi, anda memadamkan **Peranan Harga** dan **Tokokan Harga Peranan** yang mempunyai nilai dimensi yang diisi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]