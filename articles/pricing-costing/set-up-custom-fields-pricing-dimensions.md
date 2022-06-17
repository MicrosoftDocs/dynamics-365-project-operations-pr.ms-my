---
title: Sediakan medan tersuai sebagai dimensi penentuan harga
description: Artikel ini memberikan maklumat tentang cara menyediakan dimensi harga menggunakan medan tersuai.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0c0c43e483ebcb016747e533d685f13fd5dd8700
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917587"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Sediakan medan tersuai sebagai dimensi penentuan harga

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Sebelum anda memulakan, artikel ini menganggap bahawa anda telah melengkapkan prosedur dalam artikel, [Cipta medan dan entiti](create-custom-fields-entities-pricing-dimensions.md) tersuai dan [Tambah medan tersuai yang diperlukan untuk persediaan harga dan entiti transaksi](add-custom-fields-price-setup-transactional-entities.md). Sekiranya anda belum menyelesaikan prosedur tersebut, kembali dan lengkapkannya dan kemudian kembali ke artikel ini. 

Artikel ini memberikan maklumat mengenai penyediaan dimensi harga tersuai. Pada halaman **Parameter**, tab **Dimensi Penetapan Harga Berasaskan Amaun** menunjukkan rekod dalam entiti dimensi penetapan harga. Secara lalai, terdapat dua baris dalam grid pada tab ini:

- **msdyn_resourcecategory** (Peranan)
- **msdyn_OrganizationalUnit** (Unit Organisasi)

> [!IMPORTANT]
> Jangan padamkan baris ini. Walau bagaimanapun, jika anda tidak memerlukannya, anda boleh menjadikan mereka tidak diguna pakai dalam konteks tertentu dengan menetapkan **Terpakai untuk Kos** yang **Terpakai untuk Jualan**, dan **Terpakai untuk Membeli** semua kepada **Tidak.** Penetapan nilai atribut ini kepada **Tidak** mempunyai kesan yang sama tidak mempunyai medan sebagai dimensi penetapan harga.

Untuk medan untuk menjadi dimensi penetapan harga, ia mesti:

- Dicipta sebagai medan dalam **Peranan Harga** dan entiti **Tokokan Peranan Harga**. Untuk mendapatkan maklumat lanjut tentang cara untuk melakukannya, lihat [Tambah medan tersuai kepada persediaan harga dan entiti transaksi](add-custom-fields-price-setup-transactional-entities.md).

- Dicipta sebagai baris dalam jadual **Dimensi Penetapan harga**. Contohnya, tambah baris dimensi penetapan seperti yang ditunjukkan dalam grafik yang berikut. 

![Baris Dimensi Penentuan Harga Berasaskan Amaun.](media/Amt-based-PD.png)

Jam Kerja Sumber (**msdyn_resourceworkhours**) ditambah sebagai dimensi berasaskan tokokan dan telah ditambah ke grid pada tab **Dimensi Penetapan Harga Berasaskan Tokokan**.

![Baris Dimensi Penentuan Harga Berasaskan Tokokan.](media/Markup-based-PD.png)


> [!IMPORTANT]
> Sebarang perubahan kepada data dimensi penetapan harga dalam jadual ini, sedia ada atau baharu, disebarkan ke logik perniagaan penetapan harga hanya selepas cache disegar semula. Masa menyegar semula cache mungkin mengambil masa sehingga 10 minit. Benarkan tempoh masa untuk melihat perubahan dalam logik harga yang ditetapkan yang mesti disebabkan oleh perubahan pada data Dimensi Penetapan Harga.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Atribut jadual Dimensi Penetapan Harga
Bahagian berikut memberikan maklumat mengenai atribut yang berbeza dalam jadual **Dimensi Penetapan Harga**.

### <a name="pricing-dimension-name"></a>Nama Dimensi Penentuan Harga
Nilai ini sepatutnya sama dengan nama skema medan yang ditambah pada jadual **Harga Peranan** untuk dimensi penetapan harga tersuai. Untuk mendapatkan maklumat lanjut tentang menambah medan kepada **Jadual harga** peranan, lihat [Tambah medan tersuai kepada persediaan harga dan entiti transaksi](add-custom-fields-price-setup-transactional-entities.md).

### <a name="type-of-dimension"></a>Jenis dimensi
Terdapat dua jenis dimensi penetapan harga.
  
  - **Dimensi berdasarkan jumlah**: Nilai dimensi daripada konteks input dipadankan dengan nilai dimensi pada baris **Harga Peranan** dan harga/kos ditetapkan secara langsung daripada jadual **Harga Peranan**.
  - **Dimensi Berdasarkan Tokokan**: Ini adalah dimensi tiga langkah berikut untuk mendapatkan harga/kos digunakan:
 
    1. Nilai dimensi berasaskan bukan tokokan daripada konteks input dipadankan ke baris Harga Peranan untuk mendapatkan kadar asas.
    2. Nilai dimensi daripada konteks input dipadankan ke bari **Tokokan Harga Peranan** untuk mendapatkan peratusan tokokan.
    3. Peratusan tokokan daripada langkah kedua digunakan ke kadar asas yang diperoleh daripada jadual **Harga Peranan** dalam langkah pertama untuk sampai ke harga akhir/kos.
   
   Jadual berikut menunjukkan tokokan harga yang lebih tinggi.
  
| Peranan        | Unit Organisasi    |Lokasi Kerja      |Tajuk Standard      |Waktu Kerja Sumber      |  Tokokan|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|Di Tapak            |                    |Kerja Lebih Masa                 |15     |
|             | Contoso India|Tempatan             |                    |Kerja Lebih Masa                 |10     |
|             | Contoso AS   |Tempatan             |                    |Kerja Lebih Masa                 |20     |


Jika sumber dari Contoso India yang kadar asas adalah 100 USD bekerja di tempat kerja dan mereka log 8 jam masa Tetap dan 2 jam lebih masa kerja pada masa entri, enjin penetapan harga menggunakan kadar asas 100 untuk 8 jam bagi merekod 800 USD. Untuk kerja lebih masa 2 jam, tokokan sebanyak 15% akan dikenakan ke atas kadar asas 100 untuk mendapatkan harga seunit 115 USD dan akan merekodkan jumlah kos 230 USD.

### <a name="applicable-to-cost"></a>Digunakan pada Kos 
Jika ini ditetapkan kepada **Ya**, ia menunjukkan bahawa nilai dimensi dari konteks input sepatutnya digunakan untuk dipadankan ke **Harga Peranan** dan **Tokokan Harga Peranan** apabila mendapatkan semula kos dan kadar tokokan.

### <a name="applicable-to-sales"></a>Digunakan pada Jualan
Jika ini ditetapkan kepada **Ya**, ia menunjukkan bahawa nilai dimensi dari konteks input sepatutnya digunakan untuk dipadankan ke **Harga Peranan** dan **Tokokan Harga Peranan** apabila mendapatkan semula bil dan kadar tokokan.

### <a name="applicable-to-purchase"></a>Digunakan pada Belian
Jika ini ditetapkan kepada **Ya**, ia menunjukkan bahawa nilai dimensi dari konteks input sepatutnya digunakan untuk dipadankan ke **Harga Peranan** dan **Tokokan Harga Peranan** apabila mendapatkan semula harga belian. Senario subkontrak tidak disokong, oleh itu medan ini tidak digunakan. 

### <a name="priority"></a>Keutamaan
Menetapkan keutamaan dimensi membantu penetapan harga menghasilkan harga walaupun ianya tidak dapat mencari padanan tepat antara nilai dimensi input dan nilai daripada **Harga Peranan** atau jadual **Tokokan Harga Peranan**. Dalam senario ini, nilai nol digunakan untuk nilai dimensi yang tidak dapat dipadankan dengan mengukur dimensi mengikut keutamaan mereka.

- **Keutamaan Kos**: Nilai keutamaan kos dimensi akan menunjukkan berat dimensi tersebut apabila sepadan dengan penyediaan harga kos. Nilai **Keutamaan Kos** mesti unik merentasi dimensi yang **Digunakan pada Kos.**
- **Keutamaan Jualan**: Nilai keutamaan kos dimensi akan menunjukkan berat dimensi tersebut apabila sepadan dengan penyediaan harga jualan atau kadar bil. Nilai **Keutamaan Jualan** mesti unik merentasi dimensi yang **Digunakan pada Jualan.**


[!INCLUDE[footer-include](../includes/footer-banner.md)]