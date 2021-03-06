---
title: Sediakan medan tersuai sebagai dimensi penetapan harga
description: Topik ini menyediakan maklumat tentang penyediaan dimensi penetapan harga menggunakan medan tersuai.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3a2a3b48df02853e519a45dc1d37052c8ba2529d
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896607"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Sediakan medan tersuai sebagai dimensi penetapan harga

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Sebelum anda bermula, topik ini mengandaikan bahawa anda telah melengkapkan prosedur dalam topik, [Cipta medan dan entiti tersuai](create-custom-fields-entities-pricing-dimensions.md) dan [Tambah medan tersuai kepada persediaan harga dan entiti transaksi yang diperlukan](add-custom-fields-price-setup-transactional-entities.md). Jika anda belum menyelesaikan prosedur tersebut, kembali dan lengkapkan mereka dan kemudian kembali ke topik ini. 

Topik ini memberikan maklumat tentang penyediaan dimensi penetapan harga tersuai. Pada halaman **Parameter**, tab **Dimensi Penetapan Harga Berasaskan Amaun** menunjukkan rekod dalam entiti dimensi penetapan harga. Secara lalai, terdapat dua baris dalam grid pada tab ini:

- **msdyn_resourcecategory** (Peranan)
- **msdyn_OrganizationalUnit** (Unit Organisasi)

> [!IMPORTANT]
> Jangan padamkan baris ini. Walau bagaimanapun, jika anda tidak memerlukannya, anda boleh menjadikan mereka tidak diguna pakai dalam konteks tertentu dengan menetapkan **Terpakai untuk Kos**yang **Terpakai untuk Jualan**, dan **Terpakai untuk Membeli** semua kepada **Tidak.** Penetapan nilai atribut ini kepada **Tidak** mempunyai kesan yang sama tidak mempunyai medan sebagai dimensi penetapan harga.

Untuk medan untuk menjadi dimensi penetapan harga, ia mesti:

- Dicipta sebagai medan dalam **Peranan Harga** dan entiti **Tokokan Peranan Harga**. Untuk mendapatkan maklumat lanjut tentang cara untuk melakukannya, lihat [Tambah medan tersuai kepada persediaan harga dan entiti transaksi](add-custom-fields-price-setup-transactional-entities.md).
- Dicipta sebagai baris dalam jadual **Dimensi Penetapan harga**. Contohnya, tambah baris dimensi penetapan seperti yang ditunjukkan dalam grafik yang berikut. 

Jam Kerja Sumber (**msdyn_resourceworkhours**) ditambah sebagai dimensi berasaskan tokokan dan telah ditambah ke grid pada tab **Dimensi Penetapan Harga Berasaskan Tokokan**.

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
