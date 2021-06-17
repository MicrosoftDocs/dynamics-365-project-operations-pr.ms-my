---
title: Urus senarai harga projek pada sebut harga
description: Topik ini menyediakan maklumat tentang entiti senarai harga Projek.
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
ms.openlocfilehash: da349924488fb62dc0b0bd8eaf4c48b02aa16d09
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996262"
---
# <a name="manage-project-price-lists-on-a-quote"></a>Urus senarai harga projek pada sebut harga

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Dynamics 365 Project Operations melanjutkan entiti Senarai harga dalam Dynamics 365 Sales. 

## <a name="key-entities"></a>Entiti utama

Senarai harga termasuk maklumat yang disediakan oleh empat entiti yang berbeza:

- **Senarai Harga**: Entiti ini menyimpan maklumat tentang konteks, mata wang, tarikh kuat kuasa dan unit masa untuk masa penetapan harga. Konteks menunjukkan sama ada senarai harga menunjukkan kadar kos atau kadar jualan. 
- **Mata wang**: Entiti ini menyimpan mata wang harga pada senarai harga. 
- **Tarikh**: Entiti ini digunakan apabila sistem cuba memasukkan harga lalai pada transaksi. Penetapan harga yang mengandungi tarikh kuat kuasa termasuk tarikh transaksi dipilih. Jika lebih daripada satu senarai harga ditemui efektif untuk tarikh transaksi dan dilampirkan ke sebut harga, kontrak atau unit organisasi berkaitan maka tiada harga dilalaikan. 
- **Masa**: Entiti ini menyimpan unit masa yang ditunjukkan oleh harga untuk seperti kadar harian atau jam. 

Entiti Senarai harga mempunyai tiga jadual berkaitan yang menyimpan harga:

  - **Harga Peranan**: Jadual ini menyimpan kadar untuk gabungan nilai unit peranan dan organisasi dan digunakan untuk menyediakan harga berasaskan peranan untuk sumber manusia.
  - **Harga Kategori Transaksi**: Jadual ini menyimpan harga mengikut kategori transaksi dan digunakan untuk menyediakan harga kategori perbelanjaan.
  - **Item Senarai Harga**: Jadual ini menyimpan harga untuk produk katalog.
 
Senarai harga ialah kad kadar. Kad kadar ialah kombinasi entiti Senarai Harga dan baris berkaitan dalam jadual Harga Peranan, Harga Kategori Transaksi dan Item Senarai Harga.

## <a name="resource-roles"></a>Peranan sumber

Istilah *peranan sumber* merujuk kepada set kemahiran, kecekapan dan pensijilan yang seseorang mesti ada untuk melakukan satu set tugas tertentu pada projek.

Masa sumber manusia biasanya diberi sebut harga berasaskan peranan yang sumber isi pada projek tertentu. Untuk masa sumber manusia, pengekosan dan pengebilan adalah berasaskan pada peranan sumber. Masa boleh ditetapkan harga dalam mana-mana unit dalam kumpulan unit **Masa**.

Kumpulan unit **Masa** dicipta apabila anda memasang Project Operations. Ia mempunyai unit **Jam** lalai. Anda tidak boleh memadam, menamakan semula atau mengedit atribut dalam unit kumpulan **Masa** atau unit **Jam**. Walau bagaimanapun, anda boleh menambah unit lain kepada kumpulan unit **Masa**. Jika anda cuba memadam sama ada kumpulan unit **Masa** atau unit **Jam**, anda mungkin menyebabkan kegagalan dalam logik perniagaan.
 
## <a name="transaction-categories-and-expense-categories"></a>Kategori transaksi dan kategori perbelanjaan

Perbelanjaan perjalanan dan lain-lain yang ditanggung oleh perunding projek dibilkan kepada pelanggan. Penetapan harga kategori perbelanjaan dilengkapkan menggunakan senarai harga. Tambang kapal terbang, hotel dan sewa kereta ialah contoh kategori perbelanjaan. Setiap baris senarai harga untuk perbelanjaan menentukan penetapan harga untuk kategori perbelanjaan tertentu. Tiga kaedah berikut digunakan untuk kategori perbelanjaan harga:

- **Pada kos**: Kos perbelanjaan dibilkan kepada pelanggan dan tiada tokokan digunakan.
- **Peratusan tokokan**: Peratusan yang melebihi kos sebenar akan dibilkan kepada pelanggan. 
- **Harga setiap unit**: Harga pengebilan ditetapkan untuk setiap unit kategori perbelanjaan. Jumlah yang dibilkan kepada pelanggan dikira berdasarkan bilangan unit perbelanjaan yang perunding laporkan. Perbatuan menggunakan kaedah penetapan harga setiap unit. Sebagai contoh, kategori perbelanjaan perbatuan boleh dikonfigurasikan kepada 30 dolar AS (USD) setiap hari atau 2 USD setiap batu. Apabila perunding melaporkan perbatuan ke atas projek, jumlah kepada bil dikira berdasarkan bilangan batu yang dilaporkan oleh perunding.
 
## <a name="project-sales-pricing-and-overrides"></a>Penetapan harga jualan projek dan ganti

Untuk sebut harga projek dan kontrak, senarai harga projek mempunyai corak ganti harga yang berbeza berbanding senarai harga produk. Pada baris sebut harga berdasarkan katalog produk, anda boleh menulis ganti harga kepada peranan dan kategori secara langsung pada baris sebut harga, kerana setiap mata baris sebut harga kepada betul-betul satu item katalog. Walau bagaimanapun, pada baris sebut harga berasaskan projek, anda tidak boleh mengganti harga kepada peranan dan kategori secara langsung pada baris sebut harga. Gunakan senarai harga projek untuk menyokong dua corak gantian yang berbeza.

> [!NOTE]
> Kami mengesyorkan anda mempunyai senarai harga berasingan untuk sumber projek dan item katalog anda, disebabkan perbezaan tingkah laku antara kedua-dua apabila anda mengganti penetapan harga.

Setiap entiti berikut boleh mempunyai senarai harga jualan yang berkaitan untuk penetapan harga projek:

- Pelanggan (akaun) 
- Peluang 
- Sebut Harga 
- Kontrak Projek

Persatuan entiti ini dengan senarai harga ditunjukkan oleh senarai harga projek. Anda boleh mengaitkan satu atau lebih senarai harga dengan entiti Pelanggan, Peluang, Sebut Harga dan Jualan Kontrak Projek.

Senarai harga projek lalai tidak dimasukkan secara automatik pada rekod pelanggan. Walau bagaimanapun, anda boleh melampirkan senarai harga projek kepada rekod pelanggan secara manual. Walau bagaimanapun, anda akan melampirkan senarai harga projek secara manual hanya apabila anda mempunyai perjanjian penetapan harga tersuai dengan pelanggan. 

Apabila senarai harga projek dilampirkan ke entiti jualan, maklumat berikut disahkan:

- Senarai harga mempunyai konteks **Jualan**. 
- Mata wang senarai harga sepadan dengan mata wang pelanggan. 

Pada kontrak projek, perintah keutamaan berikut untuk menetapkan senarai harga projek yang berkaitan secara automatik:

1. Sebut Harga
2. Peluang
3. Pelanggan 
4. Tetapan global 

Apabila senarai harga projek dimasukkan secara lalai, sistem mengesahkan bahawa mata wang sepadan dengan mata wang pelanggan dan senarai harga lalai yang telah dimasukkan mempunyai konteks **Jualan**.

Anda boleh mengaitkan senarai harga berbilang projek dengan entiti Pelanggan, Peluang, Sebut Harga dan Jualan Kontrak Projek. Keupayaan ini menyokong harga lalai khusus masa untuk kontrak projek panjang, yang anda mungkin memerlukan lebih daripada satu senarai harga untuk akaun bagi kemas kini harga yang berlaku kerana inflasi. Bagaimanapun, jika senarai harga yang anda kaitkan dengan entiti Pelanggan, Peluang, Sebut Harga atau Kontrak Projek mempunyai keberkesanan tarikh bertindan, harga lalai mungkin salah. Oleh itu, anda perlu memastikan senarai harga projek yang mempunyai keberkesanan tarikh bertindan tidak dikaitkan dengan entiti tersebut.

### <a name="deal-specific-price-overrides"></a>Harga khusus urusan ganti

Anda boleh mencipta gantian urusan khusus untuk harga terpilih pada senarai harga projek yang dimasukkan secara lalai pada sebut harga atau kontrak projek.

Secara lalai, kontrak projek sentiasa mendapat salinan senarai harga jualan indukr dan bukannya pautan langsung kepadanya. Tingkah laku ini membantu menjamin perjanjian harga yang dibuat dengan pelanggan untuk pernyataan kerja (SOW) tidak berubah jika senarai harga induk ditukar.

Walau bagaimanapun, pada sebut harga, anda boleh menggunakan senarai harga induk. Sebagai alternatif, anda boleh menyalin senarai harga induk dan mengeditnya untuk mencipta senarai harga tersuai yang digunakan hanya untuk sebut harga tersebut. Untuk mencipta senarai harga baharu yang khusus untuk sebut harga, pada halaman **Sebut Harga**, pilih **Cipta penetapan harga tersuai**. Anda boleh mengakses senarai harga projek khusus urusan hanya daripada sebut harga. 

Apabila anda mencipta senarai harga projek tersuai, hanya komponen projek senarai harga yang disalin. Dalam erti kata lain, senarai harga baharu yang dicipta sebagai salinan senarai harga projek sedia ada yang dilampirkan pada sebut harga, dan senarai harga baru ini hanya mengandungi harga peranan dan harga kategori transaksi yang berkaitan.
  
## <a name="tracking-costs"></a>Menjejak kos

Project Operations menjejak kos untuk penggunaan masa sumber manusia pada projek. Ia juga menjejak kos untuk perbelanjaan lain yang berlaku semasa semasa projek seperti perbelanjaan perjalanan.

Seperti kadar bil, kadar kos untuk sumber manusia juga disediakan menggunakan senarai harga. Berikut adalah perbezaan utama dalam tingkah laku senarai harga kos dan senarai harga jualan:

- Kadar kos sumber tidak boleh diganti dengan projek, kontrak atau sebut harga tertentu. Walau bagaimanapun, kadar bil boleh diganti secara setiap urusan jika perubahan dibuat khusus untuk keadaan urusan tersebut. 

- Arahan berikut digunakan untuk menyelesaikan senarai harga kos:

    1. Senarai harga kos yang dilampirkan kepada unit organisasi.
    2. Senarai harga kos yang dilampirkan kepada parameter Project Operations. Oleh kerana senarai harga kos dalam banyak mata wang yang berbeza boleh dilampirkan ke parameter, padanan mata wang dilengkapkan antara mata wang unit organisasi kontrak bagi projek, kontrak atau sebut harga dan mata wang bagi senarai harga kos.
    3. Untuk perbelanjaan, kaedah penetapan harga pada kos dan tokokan melebihi kos tidak dikenakan pada senarai harga kos. Walaupun kaedah penetapan harga digunakan pada baris senarai harga kos untuk menyediakan kos kategori transaksi, sistem menolaknya dan tiada harga kos lalai dimasukkan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]