---
title: Penetapan harga projek
description: Topik ini menyediakan maklumat mengenai cara penetapan harga berfungsi dalam Dynamics 365 Project Service Automation.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
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
ms.openlocfilehash: dfbfb59547f295e5fb275264b9222bfa20517f6278144ca013e14a99454b6840
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000587"
---
# <a name="project-pricing"></a>Penetapan harga projek 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation melanjutkan entiti Senarai harga dalam Dynamics 365 Sales. 

## <a name="key-entities"></a>Entiti utama

Senarai harga termasuk maklumat yang disediakan oleh empat entiti yang berbeza:

- **Senarai Harga** - Entiti ini menyimpan maklumat mengenai konteks, mata wang, tarikh keberkesanan dan unit masa untuk masa penetapan harga. Konteks menunjukkan sama ada senarai harga menyatakan kadar kos atau kadar jualan. 
- **Mata wang** - Entiti ini menyimpan mata wang harga pada senarai harga. 
- **Tarikh** - Entiti ini digunakan apabila sistem cuba memasukkan harga lalai pada transaksi. Penetapan harga PSA memilih senarai harga yang mengandungi tarikh keberkesanan yang termasuk tarikh transaksi. Jika penetapan harga PSA mendapati lebih daripada satu senarai harga yang berkesan untuk tarikh transaksi dilampirkan kepada unit sebut harga, kontrak atau organisasi yang berkaitan, maka tiada harga yang ditetapkan. 
- **Masa** - Entiti ini menyimpan unit masa yang harga dinyatakan, seperti kadar harian atau jam. 

Entiti Senarai harga mempunyai tiga jadual berkaitan yang menyimpan harga:

  - **Harga Peranan** - Jadual ini menyimpan kadar untuk gabungan nilai unit peranan dan organisasi dan digunakan untuk menyediakan harga berasaskan peranan untuk sumber manusia.
  - **Harga Kategori Transaksi** - Jadual ini menyimpan harga mengikut kategori transaksi dan digunakan untuk menyediakan harga kategori perbelanjaan.
  - **Item Senarai Harga** - Jadual ini menyimpan harga untuk produk katalog.

> ![Mengkonfigurasi harga menggunakan senarai harga.](media/basic-guide-12.png)
 
Senarai harga ialah kad kadar. Kad kadar ialah kombinasi entiti Senarai Harga dan baris berkaitan dalam jadual Harga Peranan, Harga Kategori Transaksi dan Item Senarai Harga.

## <a name="resource-roles"></a>Peranan sumber

Istilah *peranan sumber* merujuk kepada set kemahiran, kecekapan dan pensijilan yang seseorang mesti ada untuk melakukan satu set tugas tertentu pada projek.

Masa sumber manusia biasanya dipetik berdasarkan peranan bahawa sumber mengisi projek tertentu. Untuk masa sumber manusia, PSA menyokong kos dan pengebilan berdasarkan peranan sumber. Masa boleh ditetapkan harga dalam mana-mana unit dalam kumpulan unit **Masa**.

Kumpulan unit **Masa** dicipta apabila PSA dipasang. Ia mempunyai unit **Jam** lalai. Anda tidak boleh memadamkan, menamakan semula atau mengedit atribut dalam unit kumpulan **Masa** atau unit **Jam**. Walau bagaimanapun, anda boleh menambah unit lain kepada kumpulan unit **Masa**. Jika anda cuba untuk memadam sama ada kumpulan unit **Masa** atau unit **Jam**, anda mungkin menyebabkan kegagalan dalam logik perniagaan PSA.

> ![Mengkonfigurasi harga mengikut peranan.](media/basic-guide-13.png)
 
## <a name="transaction-categories-and-expense-categories"></a>Kategori transaksi dan kategori perbelanjaan

Perbelanjaan perjalanan dan lain-lain yang perunding projek tanggung biasanya dibilkan kepada pelanggan. PSA menyokong penetapan harga kategori perbelanjaan dengan menggunakan senarai harga. Tambang kapal terbang, hotel dan sewa kereta ialah contoh kategori perbelanjaan. Setiap baris senarai harga untuk perbelanjaan menentukan penetapan harga untuk kategori perbelanjaan tertentu. Untuk penetapan harga kategori perbelanjaan, PSA menyokong tiga kaedah penetapan berikut:

- **Pada kos** - Kos perbelanjaan dibilkan kepada pelanggan dan tiada tokokan digunakan.
- **Peratusan tokokan** - Peratusan yang melebihi kos sebenar akan dibilkan kepada pelanggan. 
- **Harga setiap unit** - Harga bil ditetapkan untuk setiap unit kategori perbelanjaan. Jumlah yang dibilkan kepada pelanggan dikira berdasarkan bilangan unit perbelanjaan yang perunding laporkan. Perbatuan menggunakan kaedah penetapan harga setiap unit. Sebagai contoh, kategori perbelanjaan perbatuan boleh dikonfigurasikan kepada 30 dolar AS (USD) setiap hari atau 2 USD setiap batu. Apabila perunding melaporkan perbatuan ke atas projek, jumlah kepada bil dikira berdasarkan bilangan batu yang dilaporkan oleh perunding.

> ![Mengkonfigurasi penetapan harga untuk kategori perbelanjaan.](media/basic-guide-14.png)
 
## <a name="project-sales-pricing-and-overrides"></a>Penetapan harga jualan projek dan ganti

Untuk sebut harga projek dan kontrak, senarai harga projek mempunyai corak ganti harga yang berbeza berbanding senarai harga produk. Pada baris sebut harga berdasarkan katalog produk, anda boleh menulis ganti harga kepada peranan dan kategori secara langsung pada baris sebut harga, kerana setiap mata baris sebut harga kepada betul-betul satu item katalog. Walau bagaimanapun, pada baris sebut harga berasaskan projek, anda tidak boleh mengganti harga kepada peranan dan kategori secara langsung pada baris sebut harga. Untuk menyokong dua corak ganti yang berbeza, PSA telah memperkenalkan persatuan senarai harga baharu, senarai harga projek.

> [!NOTE]
> Kami mengesyorkan anda mempunyai senarai harga berasingan untuk sumber projek dan item katalog anda, disebabkan perbezaan tingkah laku antara kedua-dua apabila anda mengganti penetapan harga.

Setiap entiti berikut boleh mempunyai senarai harga jualan yang berkaitan untuk penetapan harga projek:

- Pelanggan (akaun) 
- Peluang 
- Sebut Harga 
- Kontrak Projek

Persatuan entiti ini dengan senarai harga ditunjukkan oleh senarai harga projek. Anda boleh mengaitkan satu atau lebih senarai harga dengan entiti Pelanggan, Peluang, Sebut Harga dan Jualan Kontrak Projek.

Senarai harga projek lalai tidak dimasukkan secara automatik pada rekod pelanggan. Walau bagaimanapun, anda boleh melampirkan senarai harga projek kepada rekod pelanggan secara manual. Walau bagaimanapun, anda akan melampirkan senarai harga projek secara manual hanya apabila anda mempunyai perjanjian penetapan harga tersuai dengan pelanggan. 

Apabila senarai harga projek dilampirkan kepada entiti jualan, PSA mengesahkan maklumat berikut:

- Senarai harga untuk konteks **Jualan**. 
- Mata wang senarai harga sepadan dengan mata wang pelanggan. 

Pada kontrak projek, PSA menggunakan perintah keutamaan berikut untuk menetapkan senarai harga projek yang berkaitan secara automatik:

1. Sebut Harga
2. Peluang
3. Pelanggan 
4. Tetapan global untuk PSA

Apabila senarai harga projek dimasukkan secara lalai, PSA mengesahkan bahawa mata wang sepadan dengan mata wang pelanggan dan senarai harga lalai yang telah dimasukkan mempunyai konteks **Jualan**.

Anda boleh mengaitkan senarai harga berbilang projek dengan entiti Pelanggan, Peluang, Sebut Harga dan Jualan Kontrak Projek. Keupayaan ini menyokong harga lalai khusus masa untuk kontrak projek panjang, yang anda mungkin memerlukan lebih daripada satu senarai harga untuk akaun bagi kemas kini harga yang berlaku kerana inflasi. Bagaimanapun, jika senarai harga yang anda kaitkan dengan entiti Pelanggan, Peluang, Sebut Harga atau Kontrak Projek mempunyai keberkesanan tarikh bertindan, harga lalai mungkin salah. Oleh itu, anda perlu memastikan senarai harga projek yang mempunyai keberkesanan tarikh bertindan tidak dikaitkan dengan entiti tersebut.

### <a name="deal-specific-price-overrides"></a>Harga khusus urusan ganti

Dalam PSA, anda boleh membuat menggantikan urusan khusus untuk harga terpilih pada senarai harga projek yang dimasukkan secara lalai pada sebut harga atau kontrak projek.

Secara lalai, kontrak projek sentiasa mendapat salinan senarai harga jualan indukr dan bukannya pautan langsung kepadanya. Tingkah laku ini membantu menjamin bahawa perjanjian harga yang dibuat dengan pelanggan untuk pernyataan kerja (SOW) tidak berubah jika senarai harga induk ditukar.

Walau bagaimanapun, pada sebut harga, anda boleh menggunakan senarai harga induk. Sebagai alternatif, anda boleh menyalin senarai harga induk dan mengeditnya untuk mencipta senarai harga tersuai yang digunakan hanya untuk sebut harga tersebut. Untuk mencipta senarai harga baharu yang khusus untuk sebut harga, pada halaman **Sebut Harga**, pilih **Cipta penetapan harga tersuai**. Anda boleh mengakses senarai harga projek khusus urusan hanya daripada sebut harga. 

Apabila anda mencipta senarai harga projek tersuai, hanya komponen projek senarai harga yang disalin. Dalam erti kata lain, senarai harga baharu yang dicipta sebagai salinan senarai harga projek sedia ada yang dilampirkan pada sebut harga, dan senarai harga baru ini hanya mengandungi harga peranan dan harga kategori transaksi yang berkaitan.

> ![Melihat dan mengkonfigurasi penetapan harga tersuai untuk kontrak projek.](media/basic-guide-15.png)
  
## <a name="tracking-costs"></a>Menjejak kos

PSA menjejaki kos untuk penggunaan masa sumber manusia pada projek. Ia juga menjejaki kos untuk perbelanjaan lain yang berlaku semasa semasa projek, seperti perbelanjaan perjalanan.

Seperti kadar bil, kadar kos untuk sumber manusia juga disediakan menggunakan senarai harga. Berikut adalah perbezaan utama dalam tingkah laku senarai harga kos dan senarai harga jualan:

- Kadar kos sumber tidak boleh diganti dengan projek, kontrak atau sebut harga tertentu. Walau bagaimanapun, kadar bil boleh diganti secara setiap urusan jika perubahan dibuat khusus untuk keadaan urusan tersebut. 

- Arahan berikut digunakan untuk menyelesaikan senarai harga kos:

    1. Senarai harga kos yang dilampirkan kepada unit organisasi.
    2. Senarai harga kos yang dilampirkan kepada parameter perkhidmatan projek. Oleh kerana senarai harga kos dalam banyak mata wang boleh dilampirkan untuk parameter perkhidmatan projek, PSA melakukan padanan mata wang antara mata wang unit organisasi kontak bagi projek, kontrak atau sebut harga, dan mata wang bagi senarai harga kos.
    3. Untuk perbelanjaan, kaedah penetapan harga pada kos dan tokokan melebihi kos tidak dikenakan pada senarai harga kos. Walaupun kaedah penetapan harga digunakan pada baris senarai harga kos untuk menyediakan kos kategori transaksi, sistem menolaknya dan tiada harga kos lalai dimasukkan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]