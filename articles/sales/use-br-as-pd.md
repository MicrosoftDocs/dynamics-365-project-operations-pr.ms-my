---
title: Gunakan sumber boleh ditempah sebagai dimensi penentuan harga
description: Topik ini memberikan maklumat tentang cara menggunakan sumber boleh ditempah sebagai dimensi penentuan harga.
author: Rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1e8487d3d32acab294bb2de16fb0278f357f774e62b553eb0c1ebd5b6246e332
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996267"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Gunakan sumber boleh ditempah sebagai dimensi penentuan harga

 _**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_ 

Topik ini memberikan maklumat tentang cara menggunakan sumber boleh ditempah sebagai dimensi penentuan harga. Jika strategi penentuan harga anda ditetapkan supaya setiap sumber boleh ditempah mesti mempunyai kadar harga atau kos tertentu, gunakan sumber boleh ditempah sebagai dimensi penentuan harga.

## <a name="prerequisites"></a>Prasyarat
Sebelum anda melengkapkan prosedur dalam topik ini, anda mesti mempunyai penyelesaian dimensi penentuan harga baharu untuk organisasi anda. Jika anda belum menciptanya, lihat [Cipta medan dan entiti tersuai](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Tambahkan medan Sumber Boleh Ditempah pada borang dan pandangan
Untuk menjadikan medan **Sumber Boleh Ditempah** boleh dilihat dalam penyelesaian dimensi penentuan harga, anda perlu menambah medan kepada semua borang dan pandangan sebagai entiti.

Jadual berikut menyenaraikan semua borang dan pandangan siap guna, mengikut entiti. Anda juga perlu menambah medan baharu pada sebarang borang atau pandangan tambahan dalam entiti tersuai anda.

|   EntitI        | Borang   |Pandangan        |
| ------------------------------|---------------------------------|----------------------------------|
|  Harga Peranan| Maklumat | - Harga Kategori Sumber Aktif<br> - Harga Kategori Sumber Berkaitan |
|  Tokokan Harga Peranan| Maklumat| - Tokokan Harga Peranan aktif<br>- Tokokan Harga Peranan Berkaitan |
|  Butiran baris sebut harga| - Maklumat Projek<br>- Cipta Cepat Projek| - Butiran Baris Sebut Harga Aktif<br>- Butiran Baris Sebut Harga Digabungkan<br>- Butiran Baris Sebut Harga Berkaitan |
|  Butiran baris Kontrak Projek| - Maklumat Projek<br>- Cipta Cepat Projek| - Butiran Baris Kontrak Digabungkan<br>- Butiran Baris Kontrak Aktif<br>- Butiran Baris Kontrak Berkaitan |
|  Tugas Projek| - Maklumat<br>- Borang Baharu| &nbsp; |
|  Ahli Pasukan Projek| - Maklumat<br>- Borang Baharu| - Ahli Pasukan Projek Aktif<br>- Ahli Pasukan Projek<br>- Ahli pasukan Projek Berkaitan |
|  Entri Masa| - Maklumat<br>- Cipta Entri Masa| - Entri Masa Saya Mengikut Tarikh<br>- Entri Masa Saya untuk Minggu ini<br>- Entri Masa untuk Kelulusan|
|  Garisan Jurnal| - Maklumat<br>- Cipta Cepat| - Garisan Jurnal Aktif<br>- Garisan Jurnal Berkaitan |
|  Butiran Baris Invois| - Maklumat<br>- Cipta Cepat| - Butiran Baris Invois Aktif<br>- Transaksi Invois Boleh Dituntut<br>- Transaksi Invois Percuma<br>- Butiran Baris Invois Berkaitan <br>- Transaksi Invois Tidak Boleh Dituntut|
|  Sebenar| - Maklumat<br>- Aktual Aktif| Berkaitan Sebenar |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Sediakan sumber boleh ditempah sebagai dimensi penentuan harga
Untuk menyediakan sumber boleh ditempah sebagai dimensi penentuan harga, ikut langkah ini:

1. Pergi ke **Tetapan** > **Parameter**. 
2. Pada halaman **Parameter**, pada tab **Dimensi Penentuan Harga Berdasarkan Jumlah**, sahkan bahawa grid menunjukkan rekod dalam entiti **Dimensi Penentuan Harga**. 
2. Tambah **Sumber Boleh Tempah** pada senarai dimensi penentuan harga ini sebagai **msdyn_bookableresource**. 
3. Dalam **Digunakan pada kos** dan **Digunakan pada jualan**, pilih nilai.
4. Dalam **Jenis Dimensi**, pilih **Berasaskan jumlah**. 
5. Pilih keutamaan kos dan jualan untuk sumber boleh tempah. Lazimnya, sumber boleh ditempah mempunyai keutamaan tertinggi apabila dimasukkan sebagai dimensi penentuan harga. Tetapkan keutamaan kepada **1** (atau **0** bergantung pada cara anda mengira keutamaan) untuk memastikan tingkah laku ini.

## <a name="set-up-pricing-dimension-field-names"></a>Tetapkan nama medan dimensi penentuan harga

Apabila nama medan dimensi penentuan harga dalam jadual **Harga Peranan** berbeza daripada nama medan dalam mana-mana entiti lain yang harga lalai digunakan, rekod dimensi penentuan harga mestilah dimaklumkan tentang nama yang berbeza itu.  

Untuk sumber boleh ditempah, entiti **Ahli Pasukan Projek** mempunyai nama medan yang sedikit berbeza daripada yang dipanggil pada entiti **Harga Peranan**: 

 - Entiti **Ahli Pasukan Projek** = **msdyn_bookableresourceid**
 - Entiti **Harga Peranan** = **msdyn_bookableresource**

Rekod dimensi penentuan harga untuk **msydn_bookableresource** mestilah dimaklumkan tentang perbezaan ini.

1. Klik dua kali pada baris dalam grid **Dimensi Penentuan Harga** untuk membuka halaman dimensi **msdyn_bookableresource**.
2. Pada halaman dimensi, pada tab **Berkaitan**, pilih **Nama Medan Dimensi Penentuan Harga**.

  ![Tab nama medan dimensi penentuan harga.](media/PD-fieldname.png)

3. Dalam pandangan berkaitan yang dibuka, pilih **Tambah Nama Medan Dimensi Penentuan Harga Baharu**.

  ![Tambahkan Nama Medan Dimensi Penentuan Harga Baru.](media/Add-NewPD-fieldname.png)

  Ini membuka halaman **nama medan dimensi Penentuan Harga baharu** untuk **msdyn_bookableresource**. 

4. Pada halaman **Nama Medan Dimensi Penentuan Harga Baharu**, tambahkan **msdyn_projectteam** pada **Nama Logik Entiti**.
5. Tambah **msdyn_bookableresourceid** pada **Nama Medan**.

 ![Borang nama medan dimensi Penentuan Harga Baru.](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]