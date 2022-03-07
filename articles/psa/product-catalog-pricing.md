---
title: Tetapan harga katalog produk
description: Topik ini memberikan maklumat tentang cara penetapan harga produk berfungsi dalam Dynamics 365 Project Service Automation (PSA).
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
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
ms.openlocfilehash: 59e05a55d41573b96785a2f41a7d5d822f6b515fb55edddea5ef1862b7694a1b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000182"
---
# <a name="product-catalog-pricing"></a>Tetapan harga katalog produk 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Senarai harga dan entiti item senarai harga menyokong penetapan harga katalog produk. Bagi sebahagian besar, fungsi ini digunakan untuk baris berdasarkan katalog pada sebut harga projek dan kontrak projek.

Bagi baris berdasarkan projek, kontrak mewakili urusan selepas ia dimenangi. Oleh sebab proses rundingan biasanya mendahului kemenangan tersebut, harga yang dilampirkan pada sebut harga sentiasa disalin seadanya pada senarai harga baharu dan dilampirkan pada kontrak. Senarai harga baharu ini tidak boleh ditukar di luar skop kontrak. Pengehadan ini membantu melindungi kad kadar yang telah dirunding daripada sebarang perubahan harga yang berlaku dalam senarai harga induk.

Produk perlu disediakan supaya ia mempunyai kos lalai dan senarai harga dalam katalog produk. Anda mesti menggunakan senarai harga, kos standard dan kos semasa untuk mengkonfigurasi kos lalai dan harga senarai. Harga senarai lalai digunakan pada baris sebut harga atau baris kontrak projek hanya apabila sistem tidak dapat mencari baris senarai harga untuk produk tersebut dalam senarai harga produk untuk sebut harga atau kontrak projek.

Harga kos baris katalog produk boleh ditukar antara sebut harga. Keupayaan ini penting kerana jika anda tidak menjejak kos dengan tepat, anda tidak boleh menentukan keuntungan operasi pada penglibatan projek. Secara lalai, kos standard produk digunakan sebagai harga kos. Walau bagaimanapun, harga kos lalai boleh dikemas kini pada baris sebut harga jika terdapat harga kos yang berbeza untuk sebut harga itu.

## <a name="price-list-items"></a>Item senarai harga

Anda boleh menambah produk daripada katalog produk kepada senarai harga yang berbeza. Baris senarai harga untuk produk sentiasa merujuk kepada unit tertentu. Penetapan harga untuk produk pada item senarai harga boleh dikonfigurasikan sebagai jumlah mata wang. Sebagai alternatif, ia boleh dikonfigurasikan sebagai fungsi harga senarai, kos semasa, atau kos standard.

PSA menyokong pelbagai pilihan pembundaran apabila harga dikonfigurasikan sebagai fungsi harga senarai, kos standard atau kos semasa. Selain mengambil kesempatan daripada pelbagai kaedah penetapan harga dan pilihan pembundaran, anda boleh mengaitkan senarai diskaun dengan item senarai harga. 

> ![Menambah produk dari katalog kepada senarai harga yang berbeza.](media/basic-guide-16.png)

Apabila anda mencipta senarai harga tersuai baharu untuk sebut harga dengan memilih **Cipta Penetapan Harga Tersuai** pada halaman **Sebut Harga Projek**, PSA membuat salinan senarai harga dan medan **Entiti** pada pengepala senarai harga baharu ditetapkan kepada **Entiti Jualan**. Nama senarai harga baharu akan ditambah dengan nama sebut harga dan cap masa. Anda juga boleh menggunakan nama senarai harga baharu dan nama sebut harga dalam aliran kerja tersuai untuk mencetuskan semakan tambahan dan kelulusan untuk sebut harga yang menggunakan penetapan harga tersuai.

 
## <a name="default-product-price-list"></a>Senarai harga produk lalai
Setiap rekod pelanggan mempunyai medan **Senarai Harga Lalai**, tempat anda boleh tentukan senarai harga yang sepadan dengan mata wang pelanggan. Dalam PSA, nilai lalai tidak dimasukkan secara automatik dalam medan ini. Apabila perjanjian penetapan harga tersuai dengan pelanggan tertentu wujud, anda boleh menggunakan medan ini untuk mengaitkan senarai harga dengan pelanggan tersebut.

Entiti Peluang, Sebut Harga dan Kontrak Projek menggunakan pesanan berikut untuk memasukkan senarai harga produk lalai. Pesanan yang sama digunakan untuk senarai harga projek.

1.  Sebut Harga
2.  Peluang
3.  Pelanggan
4.  Tetapan global untuk PSA

Secara lalai, medan **Produk** pada baris sebut harga menyenaraikan semua produk aktif dalam senarai harga produk sebut harga. Jika produk telah dinyahaktifkan atau jika ia merupakan produk draf, ia tidak disenaraikan, walaupun ia ada dalam senarai harga. 

Baris katalog produk ditambahkan sebagai baris invois pada invois pertama yang dicipta untuk kontrak projek. Pada invois draf, baris invois tersebut boleh dipadamkan. Dalam kes tersebut, baris akan muncul pada invois berikutnya sehingga ia diinvoiskan atau sehingga invois dihantar kepada pelanggan. Dalam PSA, anda tidak boleh menginvoiskan kuantiti separa baris invois produk. Apabila baris produk daripada kontrak projek diinvoiskan, aktual dicipta. Walau bagaimanapun, aktual tersebut tidak dipautkan kepada entiti projek berkaitan. Dalam erti kata lain, baris kontrak projek berdasarkan produk adalah bebas daripada sebarang penggunaan berdasarkan projek. PSA tidak menjejaki penggunaan bahan pada projek.


[!INCLUDE[footer-include](../includes/footer-banner.md)]