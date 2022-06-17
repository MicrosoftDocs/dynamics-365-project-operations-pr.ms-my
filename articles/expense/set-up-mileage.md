---
title: Sediakan perbatuan menggunakan peringkat kadar perbatuan
description: Artikel ini memberikan maklumat mengenai kadar perbatuan dan kadar perbatuan.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 03ca18c8fef6228f2ba553ebe50447beda5a857c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930145"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>Sediakan perbatuan menggunakan peringkat kadar perbatuan

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Apabila perbelanjaan dilaporkan dan kategori perbelanjaan dipilih ialah **Perbatuan**, jumlah untuk baris perbelanjaan dikira mengikut jumlah *kadar setiap perbatuan*. Jumlah ini ditentukan dengan menggunakan peringkat perbatuan yang ditakrifkan atau jika tiada peringkat kadar perbatuan disediakan, dengan mengikut kadar standard perbatuan. 

Peringkat kadar perbatuan boleh ditetapkan dengan pergi ke **Pengurusan Perbelanjaan** > **Persediaan** > **Umum** > **Kategori perbelanjaan** > **Perbatuan** > **Persediaan kategori**.

Selepas anda menaik taraf kepada 10.0.18, jika organisasi anda menggunakan kategori perbelanjaan perbatuan, pertimbangkan mendayakan ciri perbatuan selepas menyemak perubahan reka bentuk di bawah. 

Reka bentuk baharu peringkat kadar perbatuan memberi kesan kepada cara nilai dalam medan **Kuantiti** diproses. Sebelum keluaran 10.0.18, nilai dalam medan **Kuantiti** dianggap sebagai had yang lebih rendah. Apabila pengumpulan melepasi nilai tersebut, kadar yang berkaitan digunakan.  Mengikut10.0.18, nilai dalam medan **Kuantiti** dianggap had lebih atas. Kadar yang sepadan digunakan apabila pengumpulan perbatuan kurang daripada nilai dalam medan **Kuantiti**.  Model baharu untuk peringkat perbatuan membantu dengan konsistensi merentasi peringkat perbatuan dan kebolehgunaan yang lebih baik.   

Semua laporan perbelanjaan yang diluluskan akan dikira semula semasa penyiaran mengikut reka bentuk baharu.

## <a name="example"></a>Contoh
 
### <a name="before-version-10018"></a>Sebelum versi 10.0.18
Dengan dua peringkat kadar perbatuan, medan **Kuantiti** dalam setiap peringkat mewakili had perbatuan yang lebih rendah. Pada masa ini, peringkat satu mempunyai nilai sifar (0) dan kadar 0.45 dan periingkat dua mempunyai nilai 1000 dan kadar 0.25. Jika perbatuan atau kilometer yang terkumpul melepasi nilai dalam medan, kadar berkaitan digunakan. Jika tiada baris dengan kuantiti sifar, sistem menggunakan kadar perbatuan yang ditakrifkan dalam pengurusan Perbelanjaan. 
 
Jika pekerja menyerahkan laporan perbelanjaan dengan 1,500 batu, dua baris perbatuan pada laporan perbelanjaan yang disiarkan akan menjadi: 1000 (kadar 0.45) + 500 (kadar 0.25) = 575.00.

### <a name="after-version-10018"></a>Selepas versi 10.0.18
Dalam 10.0.18, medan **Kuantiti** dalam setiap peringkat mewakili had lebih atas peringkat. Pada masa ini, peringkat satu mempunyai nilai sifar 999 dan kadar 0.45 dan periingkat dua mempunyai nilai 999,999,999.00 dan kadar 0.25. Jika perbatuan atau kilometer yang terkumpul melepasi nilai dalam medan **Kuantiti**, kadar berkaitan digunakan. Jika melebihi semua had lebih atas, sistem menggunakan kadar perbatuan yang ditakrifkan dalam pengurusan Perbelanjaan. 
 
Untuk mengira dengan betul senario yang sama, peringkat yang ditetapkan mesti ditukar. Medan **Kuantiti** dalam peringkat satu mempunyai nilai 999.00 dan nilai 999,999,999.00 dalam peringkat dua. Jika pekerja melebihi jumlah kuantiti batu atau kilometer dalam satu peringkat, sistem menggunakan kadar Perbatuan yang ditakrifkan dalam pengurusan perbelanjaan. 
  
Jika pekerja menyerahkan laporan perbelanjaan dengan 1,500 batu, dua baris perbatuan pada laporan perbelanjaan yang disiarkan akan menjadi: 1000 (kadar 0.45) + 500 (kadar 0.25) = 575

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>Dayakan pengiraan jumlah Perbatuan untuk berbilang peringkat perbatuan dengan ciri kadar yang sama

Ciri **Pengiraan jumlah Perbatuan untuk berbilang peringkat perbatuan dengan kadar yang sama** menambah baik pengiraan kadar perbatuan. Lengkapkan langkah berikut untuk mendayakan ciri ini.

1. Pergi ke **Tetapan** > **Pengurusan Ciri**. 
2. Dalam senarai, cari dan pilih **Pengiraan jumlah perbatuan untuk berbilang peringkat perbatuan dengan kadar yang sama** dan kemudian pilih **dayakan sekarang**.

Selepas anda mendayakan ciri tersebut, tetapkan semula peringkat perbatuan untuk menunjukkan nilai medan kuantiti medan **Kuantiti**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
