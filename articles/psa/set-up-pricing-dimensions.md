---
title: Sediakan medan tersuai sebagai dimensi penetapan harga
description: Topik ini memberikan maklumat tentang penyediaan dimensi penetapan harga tersuai.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: fed8d1d478dfcceb7a1e848b6432563e3b94dcf8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081443"
---
# <a name="setting-up-custom-fields-as-pricing-dimensions"></a>Sediakan medan tersuai sebagai dimensi penetapan harga 

Sebelum anda mulakan, topik ini menganggap bahawa anda telah melengkapkan prosedur dalam topik, [Cipta medan dan entiti tersuai](create-custom-fields-entities.md) dan [Tambah medan tersuai kepada persediaan harga dan entiti transaksi](field-references.md). Jika anda belum menyelesaikan prosedur tersebut, kembali dan lengkapkan mereka dan kemudian kembali ke topik ini. 

Topik ini memberikan maklumat tentang penyediaan dimensi penetapan harga tersuai. Dalam antara muka web Project Service, pada halaman **Parameter** , tab **Dimensi Penetapan Harga Berdasarkan Jumlah** menunjukkan rekod dalam entiti dimensi penetapan harga. Secara lalai, pemasangan Project Service mencipta 2 baris dalam grid pada tab ini:

- **msdyn_resourcecategory** (Peranan)
- **msdyn_OrganizationalUnit** (Unit Organisasi)

> [!IMPORTANT]
> Jangan padamkan baris ini. Walau bagaimanapun, jika anda tidak memerlukannya, anda boleh menjadikan mereka tidak diguna pakai dalam konteks tertentu dengan menetapkan **Terpakai untuk Kos** yang **Terpakai untuk Jualan** , dan **Terpakai untuk Membeli** semua kepada **Tidak.** Penetapan nilai atribut ini kepada **Tidak** mempunyai kesan yang sama tidak mempunyai medan sebagai dimensi penetapan harga.

Untuk medan untuk menjadi dimensi penetapan harga, ia mesti:

- Dicipta sebagai medan dalam **Peranan Harga** dan entiti **Tokokan Peranan Harga**. Untuk mendapatkan maklumat lanjut tentang cara untuk melakukannya, lihat [Tambah medan tersuai kepada persediaan harga dan entiti transaksi](field-references.md).
- Dicipta sebagai baris dalam jadual **Dimensi Penetapan harga**. Contohnya, tambah baris dimensi penetapan seperti yang ditunjukkan dalam grafik yang berikut. 

![Baris Dimensi Penentuan Harga Berasaskan Jumlah](media/Amt-based-PD.png)

Perhatikan bahawa masa Kerja sumber ( **msdyn_resourceworkhours** ) telah ditambah sebagai dimensi berasaskan tokokan dan telah ditambah ke grid pada tab **Dimensi Penetapan Harga Berdasarkan Tokokan**.

![Tokokan - berdasarkan Baris Dimensi Penentuan Harga Berasaskan](media/Markup-based-PD.png)

> [!IMPORTANT]
> Sebarang perubahan kepada data dimensi penetapan harga dalam jadual ini, sedia ada atau baharu, disebarkan kepada pemacu perniagaan penetapan harga Project Service hanya selepas cache disegar semula. Masa menyegar semula cache mungkin mengambil masa sehingga 10 minit. Benarkan tempoh masa untuk melihat perubahan dalam logik harga yang ditetapkan yang mesti disebabkan oleh perubahan pada data Dimensi Penetapan Harga.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Atribut jadual Dimensi Penetapan Harga
Bahagian berikut memberikan maklumat mengenai atribut yang berbeza dalam jadual **Dimensi Penetapan Harga**.

### <a name="pricing-dimension-name"></a>Nama Dimensi Penentuan Harga
Nilai ini sepatutnya sama dengan nama skema medan yang ditambah pada jadual **Harga Peranan** untuk dimensi penetapan harga tersuai. Untuk mendapatkan maklumat lanjut tentang menambah medan kepada **Jadual harga** peranan, lihat [Tambah medan tersuai kepada persediaan harga dan entiti transaksi](field-references.md).

### <a name="type-of-dimension"></a>Jenis dimensi
Terdapat dua jenis dimensi penetapan harga.
  
  - **Dimensi berdasarkan jumlah** : Nilai dimensi daripada konteks input dipadankan dengan nilai dimensi pada baris **Harga Peranan** dan harga/kos ditetapkan secara langsung daripada jadual **Harga Peranan**.
  - **Dimensi Berdasarkan Tokokan** : Ini adalah dimensi di mana Project Service akan menggunakan proses 3 langkah berikut untuk mendapatkan harga/kos
 
    1. Project Service sepadan dengan nilai dimensi bukan tokokan dari konteks input kepada baris Harga Peranan untuk mendapatkan kadar asas.
    2. Project Service sepadan dengan semua nilai dimensi daripada konteks input kepada baris **Tokokan Harga Peranan** untuk mendapatkan peratus tokokan.
    3. Project Service menggunakan peratusan tokokan daripada langkah kedua ke peringkat asas yang diperolehi daripada jadual harga **Harga Peranan** dalam langkah pertama untuk tiba pada harga akhir/kos.
   
   Jadual berikut menunjukkan tokokan harga yang lebih tinggi.
  
| Peranan        | Unit Organisasi    |Lokasi Kerja      |Tajuk Standard      |Waktu Kerja Sumber      |  Tokokan|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|Di Tapak            |                    |Kerja Lebih Masa                 |15     |
|             | Contoso India|Tempatan             |                    |Kerja Lebih Masa                 |10     |
|             | Contoso AS   |Tempatan             |                    |Kerja Lebih Masa                 |20     |


Jika sumber dari Contoso India yang mana kadar asas adalah 100 USD bekerja di tempat kerja, dan mereka log 8 jam masa Tetap dan 2 jam lebih masa kerja pada masa kemasukan, enjin penetapan Project Service akan menggunakan kadar asas 100 untuk 8 jam untuk merakam 800 USD. Untuk kerja lebih masa 2 jam, tokokan sebanyak 15% akan dikenakan ke atas kadar asas 100 untuk mendapatkan harga seunit 115 USD dan akan merekodkan jumlah kos 230 USD.

### <a name="applicable-to-cost"></a>Digunakan pada Kos 
Jika ini ditetapkan kepada **Ya** , ia menunjukkan bahawa nilai dimensi dari konteks input sepatutnya digunakan untuk dipadankan ke **Harga Peranan** dan **Tokokan Harga Peranan** apabila mendapatkan semula kos dan kadar tokokan.

### <a name="applicable-to-sales"></a>Digunakan pada Jualan
Jika ini ditetapkan kepada **Ya** , ia menunjukkan bahawa nilai dimensi dari konteks input sepatutnya digunakan untuk dipadankan ke **Harga Peranan** dan **Tokokan Harga Peranan** apabila mendapatkan semula bil dan kadar tokokan.

### <a name="applicable-to-purchase"></a>Digunakan pada Belian
Jika ini ditetapkan kepada **Ya** , ia menunjukkan bahawa nilai dimensi dari konteks input sepatutnya digunakan untuk dipadankan ke **Harga Peranan** dan **Tokokan Harga Peranan** apabila mendapatkan semula harga belian. Pada masa ini, Project Service tidak menyokong senario sub kontrak, jadi medan ini tidak digunakan. 

### <a name="priority"></a>Keutamaan
Menetapkan keutamaan dimensi membantu penetapan harga Project Service menghasilkan harganya walaupun ia tidak dapat mencari padanan tepat antara nilai dimensi input dan **Harga Peranan** atau jadual **Tokokan Harga Peranan**. Dalam senario ini, Project Service akan menggunakan nilai sifar untuk nilai dimensi yang tidak dapat ditandingi dengan berat dimensi mengikut keutamaan mereka.

- **Keutamaan Kos** : Nilai keutamaan kos dimensi akan menunjukkan berat dimensi tersebut apabila sepadan dengan penyediaan harga kos. Nilai **Keutamaan Kos** mesti unik merentasi dimensi yang **Digunakan pada Kos.**
- **Keutamaan Jualan** : Nilai keutamaan kos dimensi akan menunjukkan berat dimensi tersebut apabila sepadan dengan penyediaan harga jualan atau kadar bil. Nilai **Keutamaan Jualan** mesti unik merentasi dimensi yang **Digunakan pada Jualan.**
