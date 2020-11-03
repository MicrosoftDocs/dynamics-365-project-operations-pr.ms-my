---
title: Pembetulan pukal aktual yang dicipta oleh entri masa dan perbelanjaan yang diluluskan
description: Topik ini menerangkan cara pentadbir boleh membuat pembetulan tunggal atau pukal kepada entri masa atau perbelanjaan yang telah diluluskan jika pengebilan tidak lengkap.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 6d6c03cc74d47ca3ae7c2bd7d0aa0720bb2f3c01
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081404"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a>Pembetulan pukal aktual yang dicipta oleh entri masa dan perbelanjaan yang diluluskan

Kadangkala entri masa atau perbelanjaan boleh dimasukkan dengan salah. Sebagai contoh, seorang perunding mungkin memilih tarikh yang salah apabila mencipta entri masa atau mereka mungkin mengubah nombor apabila memasukkan perbelanjaan. Jika perunding tidak boleh membuat kemas kini kepada entri yang diserahkan, pentadbir boleh secara langsung membetulkan entri untuk projek.

Untuk melengkapkan prosedur dalam topik ini, anda akan memerlukan keizinan Pentadbir.

## <a name="correct-approved-time-entries"></a>Entri masa yang diluluskan yang betul     

Lengkapkan langkah berikut untuk membetulkan entri masa tunggal atau berbilang bagi projek.

1. Dalam kawasan **Jualan** , pilih **Urus niaga** dan kemudian pilih **Masa yang Diluluskan**. 

2. Dalam senarai **Masa yang Diluluskan** , cari dan pilih satu atau lebih entri masa yang diluluskan untuk dibetulkan. Anda boleh menggunakan penapis untuk mengesan entri yang berkaitan. Contohnya, anda boleh menapis ID Projek dan memilih semua entri masa yang diluluskan dengan ID Projek tersebut.

3. Pilih **Entri yang betul**. Jurnal pembetulan baharu dicipta secara automatik, dengan jenis ditugaskan **Pembetulan masa**. Entri yang anda pilih ditambah kepada jurnal tersebut. 

4. Pada halaman **Jurnal Baharu** , masukkan **Perihalan** untuk jurnal pembetulan anda dan kemudian pilih tab **Pembetulan Entri Masa**.  
5. Dalam bahagian **Nilai Baharu untuk Entri Masa** , kemas kini medan dengan maklumat yang betul mengikut keperluan. Contohnya, anda boleh mengubah projek yang ditugaskan atau sumber boleh ditempah.

6. Pilih **Pratonton**. Dalam kotak dialog, pilih **OK**. Pada tab **Garisan jurnal** , anda boleh melihat senarai aktual asal yang berkaitan dengan entri masa terpilih yang telah diterbalikkan dan baris sepadan yang dibetulkan yang telah dicipta. Jika pembetulan tambahan perlu dibuat, ulangi langkah 5 dan 6. 

> [!NOTE]
> Semua aktual yang dibetulkan akan mempunyai nilai yang sama yang anda pilih dalam bahagian **Nilai Baharu untuk Entri Masa**.

7. Jika pembetulan muncul seperti yang dijangka, pilih **Sahkan**. Dalam kotak dialog, pilih **OK**.

8. Kembali ke kawasan **Jualan** , pilih **Projek** , dan kemudian buka projek yang anda baru sahaja kemas kini entri masanya. 

9. Pada halaman **Projek** , pada tab **Aktual** , lihat perubahan yang anda lakukan. 

> [!NOTE]
> Jika tab **Aktual** tidak kelihatan, pilih **Berkaitan** > **Aktual**.  

10. Dalam senarai **Pandangan Berkaitan Aktual** , anda boleh melihat bahawa entri masa asal yang telah diterbalikkan masih disenaraikan, seperti entri masa dibetulkan yang sepadan. 

Sebagai contoh, dalam grafik berikut, terdapat dua baris item dengan kuantiti 8.00 yang mempunyai debit disenaraikan dalam lajur Amaun. Selain itu, terdapat dua baris item dengan kuantiti -8.00 yang menunjukkan amaun yang dikreditkan dalam lajur Amaun. Pembetulan ini membawa kuantiti kepada sifar.

![Senarai pandangan berkaitan aktual](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a>Entri perbelanjaan yang diluluskan yang betul

Lengkapkan langkah berikut untuk membetulkan satu atau lebih entri perbelanjaan. 

1. Dalam kawasan **Jualan** , dalam anak tetingkap navigasi kiri, di bawah **Urus niaga** , pilih **Perbelanjaan Diluluskan**.

2. Dalam senarai **Perbelanjaan Diluluskan** , pilih projek yang anda mahu betulkan dan kemudian pilih **Entri yang betul**. Jurnal pembetulan akan dicipta secara automatik dengan jenis ditugaskan **Pembetulan perbelanjaan**. 

3. Pada halaman **Jurnal Baharu** , masukkan **Perihalan** untuk pembetulan dan pada tab **Pembetulan Perbelanjaan** , dalam bahagian **Nilai Baharu untuk Perbelanjaan** , pilih medan data yang anda mahu betulkan untuk baris perbelanjaan yang dipilih. Contohnya, anda boleh menugaskan perbelanjaan ke **Projek** lain atau membetulkan **Kategori Perbelanjaan** , **Tarikh Perbelanjaan** atau **Sumber Boleh Ditempah**.

4. Pilih **Pratonton**. Dalam kotak dialog, pilih **OK**. 

5. Sahkan pembetulan pada tab **Garisan jurnal**. Anda boleh melihat senarai aktual asal yang berkaitan dengan entri perbelanjaan terpilih yang telah diterbalikkan dan baris sepadan yang dibetulkan yang telah dicipta.

6. Jika nilai yang dibetulkan adalah seperti yang dijangka, pilih **Sahkan**. Dalam kotak dialog, pilih **OK.** Jika nilai tidak ditunjukkan seperti yang dijangkakan, pilih **Batalkan** untuk kembali ke senarai **Perbelanjaan yang Diluluskan**. Ulangi langkah 2 hingga 5. 

> [!NOTE]
> Aktual yang dibetulkan akan mempunyai nilai yang sama yang anda pilih dalam bahagian **Nilai Baharu untuk Perbelanjaan**.

7. Selepas anda mengesahkan jurnal pembetulan, navigasi kembali ke projek atau projek yang anda kemas kini, untuk melihat perubahan anda.  

8. Dalam halaman projek, pada tab **Aktual** , semak **Pandangan Berkaitan Aktual**. Entri asal dan entri yang diperbetulkan disenaraikan. Grafik berikut menunjukkan jumlah entri perbelanjaan asal dan jumlah entri perbelanjaan dibetulkan yang sepadan. 

![Aktual perbelanjaan](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)
