---
title: Baris sebut harga berdasarkan produk
description: Topik ini memberikan maklumat tentang baris sebut harga berdasarkan produk.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 3cc2e8788ea699b57ef75903ec3771f2e66fe867a9b8b6328a55b484eb13ede4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008597"
---
# <a name="product-based-quote-lines"></a>Baris sebut harga berdasarkan produk

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Anda boleh mencipta baris sebut harga berdasarkan produk dalam Dynamics 365 Project Service Automation. Baris sebut harga berdasarkan produk boleh menjadi baris "tulis masuk" atau ia boleh menjadi item daripada katalog produk.

## <a name="product-catalog"></a>Katalog produk

Produk dalam katalog produk Dynamics 365 mempunyai unit lalai dan kumpulan unit. Jika beberapa produk berkongsi set atribut yang sama, anda boleh mencipta keluarga produk yang juga mempunyai atribut tersebut. Semua produk dalam satu keluarga produk mewarisi set atribut yang sama.

Sebagai contoh, sebuah syarikat menjual lesen langganan untuk pelbagai perisian. Semua perisian langganan mempunyai dua atribut berikut:

- Bilangan pengguna 
- Tempoh langganan (dalam bulan)

Cara yang baik untuk mengekalkan jenis katalog ini adalah untuk mencipta keluarga produk yang dinamakan **Perisian Langganan** dan yang mempunyai **Bilangan pengguna** dan **Tempoh langganan** sebagai atribut. Anda kemudian boleh menambah produk individu, seperti **Dynamics 365 Sales** atau **Dynamics 365 Field Service** kepada keluarga produk **Perisian Langganan**.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Menambahkan item katalog produk kepada sebut harga projek

Sebut harga projek dan halaman kontrak projek mempunyai bahagian untuk dua jenis baris: Baris berdasarkan projek dan baris berdasarkan produk. Untuk baris berdasarkan produk, Dynamics 365 digunakan untuk menambah item daripada katalog produk kepada sebut harga. Senarai ke bawah pada baris sebut harga atau baris kontrak projek menyertakan semua produk dan unit dalam senarai harga produk yang dilampirkan pada sebut harga atau kontrak projek. Anda juga boleh menambah produk yang bukan sebahagian daripada senarai harga produk sebut harga.

Selain itu, anda boleh memilih produk daripada senarai harga lain atau anda boleh memilih produk secara langsung daripada katalog produk. Apabila anda memilih produk secara langsung daripada katalog produk, senarai harga lalai produk tersebut digunakan untuk mendapatkan harga jualan produk tersebut. Jika senarai harga lalai tidak ditetapkan, harga ditetapkan kepada 0 (sifar).

Jika baris sebut harga adalah berdasarkan katalog produk, anda boleh ganti harga jualan secara langsung pada baris sebut harga. Ambil perhatian bahawa baris sebut harga dalam Dynamics 365 mempunyai medan **Penetapan harga**. Dua nilai tersedia:

- Ganti penetapan harga  
- Gunakan lalai

Jika anda menetapkan medan ini kepada **Ganti penetapan harga**, Dynamics 365 tidak menetapkan harga lalai. Anda mesti masukkan harga untuk produk pada baris sebut harga. Jika anda menetapkan medan ini kepada **Gunakan lalai**, Dynamics 365 menggunakan harga jualan lalai dan mengunci medan tersebut untuk mengelakkan pengeditan.

Selepas anda memasang PSA, harga jualan lalai dimasukkan pada baris berdasarkan produk pada sebut harga. Medan **Penetapan harga** kemudian ditetapkan kepada **Ganti penetapan harga** supaya anda boleh mengedit harga lalai pada baris sebut harga.

> ![Menetapkan penentuan harga ganti.](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>Faktor kuantiti bagi produk

PSA menggunakan faktor kuantiti untuk menyokong jualan produk berdasarkan langganan. Untuk produk berdasarkan langganan, kuantiti pada sebut harga atau baris kontrak projek dinyatakan sebagai bilangan bulan pengguna.

Biasanya, harga perisian langganan disimpan dalam katalog sebagai harga bagi setiap pengguna setiap bulan. Walau bagaimanapun, anda boleh menggunakan perihalan masa lain sebagai ganti. Semasa proses jualan, harga pada baris sebut harga biasanya adalah harga bagi setiap pengguna, setiap bulan yang telah dirundingkan dan terdiskaun oleh ejen jualan IT. Setiap urusan mempunyai bilangan pengguna yang berbeza dan bilangan bulan langganan yang berbeza. Kuantiti yang digunakan untuk mengira jumlah baris sebut harga adalah produk bilangan pengguna dan bilangan bulan langganan.

Untuk menyokong jenis jualan ini, PSA memperkenalkan konsep faktor kuantiti. Faktor kuantiti bergantung pada atribut produk dalam Dynamics 365. Apabila anda mengkonfigurasikan sifat khusus untuk produk, PSA membolehkan anda menandakan subset sifat tersebut atau semua sifat tersebut, sebagai faktor kuantiti.

PSA mengesahkan bahawa hanya sifat angka atau sifat produk yang mempunyai jenis data berangka ditandakan sebagai faktor kuantiti. Apabila produk yang faktor kuantiti dikonfigurasikan ditambah pada baris sebut harga, medan **Kuantiti** pada baris sebut harga akan menjadi medan baca sahaja. Selepas anda memasukkan nilai untuk sifat produk yang merupakan faktor kuantiti, PSA mengira kuantiti baris sebut harga.

Sebagai contoh, Dynamics 365 mungkin mempunyai sifat berikut: 

- **Bilangan pengguna** - Bilangan pengguna 
- **Bilangan bulan** – Bilangan bulan langganan
- **SKU Produk** 

Sifat **Bilangan Pengguna** dan **Bilangan Bulan** boleh ditandakan sebagai faktor kuantiti dengan mengedit sifat baris produk. 

> ![Menandakan Bilangan Pengguna dan Bilangan Bulan sebagai faktor kualiti.](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]