---
title: Matikan dimensi penetapan harga
description: Topik ini menyediakan maklumat tentang cara mematikan dimensi penetapan harga.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: ffeff2ab465f37b8a4e40f4e64b118e3bb412cb8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119294"
---
# <a name="turning-off-a-pricing-dimension"></a>Matikan dimensi penetapan harga

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Anda mungkin perlu menyemak semula dan mengemas kini strategi penetapan harga setiap beberapa tahun. Sebarang kemas kini yang anda lakukan mungkin memerlukan anda memadamkan dimensi penetapan harga yang sedia ada dan mencipta satu yang baharu. Sebagai contoh, anda mungkin telah memilih lebih banyak **Peranan** tetapi kini anda telah memutuskan harga mengikut **Pengalaman Kerja**. Ini mungkin memerlukan anda mematikan **Peranan** sebagai dimensi penetapan harga dan mencipta **Pengalaman Kerja** sebagai dimensi penetapan harga baharu. 

Mematikan dimensi penetapan harga, tanpa mengira jika ia di luar kotak atau tersuai, boleh dilakukan dengan menetapkan medan **Digunakan pada Kos** dan **Diguna pada Jualan** Dimensi Penetapan Harga ke **Tidak**.

Walau bagaimanapun, apabila anda melakukannya, anda mungkin menerima message ralat, **Dimensi penetapan harga tidak boleh dikemas kini atau dipadam jika terdapat rekod harga yang berkaitan.**

Mesej ralat ini menunjukkan bahawa terdapat rekod harga yang ditetapkan sebelum ini untuk dimensi yang sedang dipadamkan. Semua **Harga Peranan** dan **Tokokan Harga Peranan** yang merujuk kepada dimensi mesti dipadamkan sebelum kebolehgunaan dimensi boleh ditetapkan ke **Tidak**. Peraturan ini diguna pakai untuk kedua-dua dimensi penetapan harga luar kotak dan sebarang dimensi penetapan harga tersuai yang anda telah cipta. Sebab pengesahan ini adalah kerana rekod **Harga Peranan** masing-masing mesti mempunyai kombinasi dimensi yang unik. Sebagai contoh, pada senarai harga yang dipanggil **Kadar Kos 2018 AS**, anda mempunyai baris harga **Peranan harga**. 

| Tajuk Standard         | Unit Organisasi    |Unit   |Harga  |Mata Wang  |
| -----------------------|-------------|-------|-------|----------|
| Jurutera sistem|Contoso AS|Hour| 100|USD|
| Jurutera Sistem Senior|Contoso AS|Hour| 150| USD|


Apabila anda mematikan **Tajuk Standard** sebagai dimensi penetapan harga dan enjin penetapan harga mencari harga, ianya akan hanya menggunakan nilai **Unit Organisasi** daripada konteks input. Jika **Unit Organisasi** konteks input ialah "Contoso US", hasilnya tidak akan ditentukan kerana kedua-dua baris akan dipadankan. Untuk mengelakkan senario ini, apabila anda mencipta rekod **Harga Peranan**, sistem mengesahkan bahawa kombinasi dimensi adalah unik. Jika dimensi telah dimatikan selepas rekod **Peranan Harga** dicipta, kekangan ini boleh dilanggar. Oleh itu, ia adalah diperlukan bahawa sebelum anda mematikan dimensi, anda memadamkan **Peranan Harga** dan **Tokokan Harga Peranan** yang mempunyai nilai dimensi yang diisi.
