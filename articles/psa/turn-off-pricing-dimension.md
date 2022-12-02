---
title: Padamkan dimensi penetapan harga
description: Artikel ini menunjukkan cara menyediakan dimensi penetapan harga dalam penyelesaian Project Service.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 81c3cfaad8dc8d057985b509f20c3ba31de45e3b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913171"
---
# <a name="turn-off-a-pricing-dimension"></a>Padamkan dimensi penetapan harga

[!include [banner](../includes/psa-now-project-operations.md)]

Anda mungkin perlu menyemak semula dan mengemas kini strategi penetapan harga setiap beberapa tahun. Sebarang kemas kini yang anda lakukan mungkin memerlukan anda memadamkan dimensi penetapan harga yang sedia ada dan mencipta satu yang baharu. Sebagai contoh, anda mungkin telah memilih lebih banyak **Peranan** tetapi kini anda telah memutuskan harga mengikut **Pengalaman Kerja**. Ini mungkin memerlukan anda **Peranan** sebagai dimensi penetapan harga dan mencipta **Pengalaman Kerja** sebagai dimensi penetapan harga baharu. 

Mematikan dimensi penetapan harga, tanpa mengira jika ia di luar kotak atau tersuai, boleh dilakukan dengan menetapkan medan **Digunakan pada Kos** dan **Diguna pada Jualan** Dimensi Penetapan Harga ke **Tidak**.

Walau bagaimanapun, apabila anda lakukan ini, anda mungkin menerima mesej ralat berikut.

![Ralat Proses Perniagaan mungkin berlaku apabila memadamkan dimensi penentuan harga.](media/Business-Process-Error.png)


Mesej ralat ini menunjukkan bahawa terdapat rekod harga yang ditetapkan sebelum ini untuk dimensi yang sedang dipadamkan. Semua **Harga Peranan** dan **Tokokan Harga Peranan** yang merujuk kepada dimensi mesti dipadamkan sebelum kebolehgunaan dimensi boleh ditetapkan ke **Tidak**. Peraturan ini diguna pakai untuk kedua-dua dimensi penetapan harga luar kotak dan sebarang dimensi penetapan harga tersuai yang anda telah cipta. Sebab untuk pengesahan ini adalah kerana Project Service mempunyai kekangan bahawa setiap rekod **Harga Peranan** mesti mempunyai kombinasi unik dimensi. Sebagai contoh, pada senarai harga yang dipanggil **Kadar Kos 2018 AS**, anda mempunyai baris harga **Peranan harga**. 

| Tajuk Standard         | Unit Organisasi    |Unit   |Harga  |Mata Wang  |
| -----------------------|-------------|-------|-------|----------|
| Jurutera sistem|Contoso AS|Hour| 100|USD|
| Jurutera Sistem Senior|Contoso AS|Hour| 150| USD|


Apabila anda memadamkan **Tajuk Standard** sebagai dimensi penetapan harga dan enjin penetapan harga Project Service mencari untuk harga, ia hanya akan menggunakan nilai **Unit Harga** daripada konteks input. Jika **Unit Organisasi** konteks input ialah "Contoso US", hasilnya tidak akan ditentukan kerana kedua-dua baris akan dipadankan. Untuk mengelakkan senario ini, apabila anda mencipta **Harga Peranan** Project Service mengesahkan bahawa kombinasi dimensi adalah unik. Jika dimensi telah dimatikan selepas rekod **Peranan Harga** dicipta, kekangan ini boleh dilanggar. Oleh itu, ia adalah diperlukan bahawa sebelum anda mematikan dimensi, anda memadamkan **Peranan Harga** dan **Tokokan Harga Peranan** yang mempunyai nilai dimensi yang diisi.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
