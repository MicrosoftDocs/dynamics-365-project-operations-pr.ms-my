---
title: Cipta dan sahkan jurnal Pembetulan
description: Topik ini menyediakan maklumat tentang cara mencipta dan mengesahkan jurnal pembetulan.
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
ms.openlocfilehash: 9d242741b2070f086bf8d3f1d40a5380c2a0f518
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996667"
---
# <a name="create-and-confirm-correction-journals"></a>Cipta dan sahkan jurnal Pembetulan

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Kadangkala entri masa atau perbelanjaan boleh dimasukkan dengan salah. Sebagai contoh, seorang perunding mungkin memilih tarikh yang salah apabila mencipta entri masa atau mereka mungkin mengubah nombor apabila memasukkan perbelanjaan. Jika perunding tidak boleh membuat kemas kini kepada entri yang diserahkan, pentadbir boleh secara langsung membetulkan entri untuk projek.

Untuk melengkapkan prosedur dalam topik ini, anda akan memerlukan keizinan Pentadbir.

## <a name="correct-approved-time-entries"></a>Entri masa yang diluluskan yang betul     

Lengkapkan langkah berikut untuk membetulkan entri masa tunggal atau berbilang bagi projek.

1. Dalam kawasan **Jualan**, pilih **Urus niaga** dan kemudian pilih **Masa yang Diluluskan**. 

2. Dalam senarai **Masa yang Diluluskan**, cari dan pilih satu atau lebih entri masa yang diluluskan untuk dibetulkan. Anda boleh menggunakan penapis untuk mengesan entri yang berkaitan. Contohnya, anda boleh menapis ID Projek dan memilih semua entri masa yang diluluskan dengan ID Projek tersebut.

3. Pilih **Entri yang betul**. Jurnal pembetulan baharu dicipta secara automatik, dengan jenis ditugaskan **Pembetulan masa**. Entri yang anda pilih ditambah kepada jurnal tersebut. 

4. Pada halaman **Jurnal Baharu**, masukkan **Perihalan** untuk jurnal pembetulan anda dan kemudian pilih tab **Pembetulan Entri Masa**.  

5. Dalam bahagian **Nilai Baharu untuk Entri Masa**, kemas kini medan dengan maklumat yang betul mengikut keperluan. Contohnya, anda boleh mengubah projek yang ditugaskan atau sumber boleh ditempah.

6. Pilih **Pratonton**. Dalam kotak dialog, pilih **OK**. Pada tab **Garisan jurnal**, anda boleh melihat senarai aktual asal yang berkaitan dengan entri masa terpilih yang telah diterbalikkan dan baris sepadan yang dibetulkan yang telah dicipta. Jika pembetulan tambahan perlu dibuat, ulangi langkah 5 dan 6. 

> [!NOTE]
> Semua aktual yang dibetulkan akan mempunyai nilai yang sama yang anda pilih dalam bahagian **Nilai Baharu untuk Entri Masa**.

7. Jika pembetulan muncul seperti yang dijangka, pilih **Sahkan**. Dalam kotak dialog, pilih **OK**.

8. Kembali ke kawasan **Jualan**, pilih **Projek**, dan kemudian buka projek yang anda baru sahaja kemas kini entri masanya. 

9. Pada halaman **Projek**, pada tab **Aktual**, lihat perubahan yang anda lakukan. 

> [!NOTE]
> Jika tab **Aktual** tidak kelihatan, pilih **Berkaitan** > **Aktual**.  

10. Dalam senarai **Pandangan Berkaitan Aktual**, anda boleh melihat bahawa entri masa asal yang telah diterbalikkan masih disenaraikan, seperti entri masa dibetulkan yang sepadan. 

Sebagai contoh, dalam grafik berikut, terdapat dua baris item dengan kuantiti 8.00 yang mempunyai debit disenaraikan dalam lajur Amaun. Selain itu, terdapat dua baris item dengan kuantiti -8.00 yang menunjukkan amaun yang dikreditkan dalam lajur Amaun. Pembetulan ini membawa kuantiti kepada sifar.

 
## <a name="correct-approved-expense-entries"></a>Entri perbelanjaan yang diluluskan yang betul

Lengkapkan langkah berikut untuk membetulkan satu atau lebih entri perbelanjaan. 

1. Dalam kawasan **Jualan**, dalam anak tetingkap navigasi kiri, di bawah **Urus niaga**, pilih **Perbelanjaan Diluluskan**.

2. Dalam senarai **Perbelanjaan Diluluskan**, pilih projek yang anda mahu betulkan dan kemudian pilih **Entri yang betul**. Jurnal pembetulan akan dicipta secara automatik dengan jenis ditugaskan **Pembetulan perbelanjaan**. 

3. Pada halaman **Jurnal Baharu**, masukkan **Perihalan** untuk pembetulan dan pada tab **Pembetulan Perbelanjaan**, dalam bahagian **Nilai Baharu untuk Perbelanjaan**, pilih medan data yang anda mahu betulkan untuk baris perbelanjaan yang dipilih. Contohnya, anda boleh menugaskan perbelanjaan ke **Projek** lain atau membetulkan **Kategori Perbelanjaan**, **Tarikh Perbelanjaan** atau **Sumber Boleh Ditempah**.

4. Pilih **Pratonton**. Dalam kotak dialog, pilih **OK**. 

5. Sahkan pembetulan pada tab **Garisan jurnal**. Anda boleh melihat senarai aktual asal yang berkaitan dengan entri perbelanjaan terpilih yang telah diterbalikkan dan baris sepadan yang dibetulkan yang telah dicipta.

6. Jika nilai yang dibetulkan adalah seperti yang dijangka, pilih **Sahkan**. Dalam kotak dialog, pilih **OK.** Jika nilai tidak ditunjukkan seperti yang dijangkakan, pilih **Batalkan** untuk kembali ke senarai **Perbelanjaan yang Diluluskan**. Ulangi langkah 2 hingga 5. 

> [!NOTE]
> Aktual yang dibetulkan akan mempunyai nilai yang sama yang anda pilih dalam bahagian **Nilai Baharu untuk Perbelanjaan**.

7. Selepas anda mengesahkan jurnal pembetulan, navigasi kembali ke projek atau projek yang anda kemas kini, untuk melihat perubahan anda.  

8. Dalam halaman projek, pada tab **Aktual**, semak **Pandangan Berkaitan Aktual**. Entri asal dan entri yang diperbetulkan disenaraikan. Grafik berikut menunjukkan jumlah entri perbelanjaan asal dan jumlah entri perbelanjaan dibetulkan yang sepadan. 




[!INCLUDE[footer-include](../includes/footer-banner.md)]