---
title: Guna sumber boleh tempah sebagai dimensi penentuan harga
description: Topik ini memberikan maklumat tentang menggunakan sumber boleh tempat sebagai dimensi penentuan harga.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
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
ms.openlocfilehash: d9b25a768f892d83c09d37ce76291d6c8e75b1be
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145009"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Guna sumber boleh tempah sebagai dimensi penentuan harga

[!include [banner](../includes/psa-now-project-operations.md)]

Topik ini memberikan maklumat tentang menggunakan sumber boleh tempat sebagai dimensi penentuan harga. Sebelum anda mulakan, jika anda belum mencipta penyelesaian dimensi penetapan harga, anda akan perlu mencipta yang baharu. Jika anda sudah mempunyai penyelesaian dimensi penetapan harga, anda boleh membuat perubahan anda dalam penyelesaian tersebut. Jika anda belum mencipta penyelesaian dimensi penetapan harga baharu untuk organisasi anda, lengkapkan prosedur [Cipta medan tersuai dan topik entiti](create-custom-fields-entities.md).

## <a name="add-bookable-resource-to-forms-and-views"></a>Tambah sumber boleh tempah pada borang dan pandangan
Untuk membolehkan medan boleh dilihat dalam UI dalam penyelesaian dimensi penentuan harga, anda perlu meneliti semua borang dan pandangan entiti Project Service utama dan menambah medan pada borang dan pandangan entiti tersebut.
Jadual berikut ialah senarai borang dan pandangan luar kota yang menyeluruh, disenaraikan mengikut entiti, yang perlu dikemas kini nanti. Jika terdapat pandangan atau borang tambahan dalam penyesuaian anda ke atas entiti ini, tambah medan baharu ke atasnya juga.
Buka Solution Explorer untuk mengetahui penyelesaian dimensi penentuan harga dan kemudian klik **Terbitkan Semua Penyesuaian**.


|   Entiti        | Borang   |Pandangan        |
| ------------------------------|---------------------------------|----------------------------------|
|  Harga Peranan|• Maklumat |•Harga Kategori Sumber Aktif<br> •Pandangan Berkaitan Harga Kategori Sumber|
|  Tokokan Harga Peranan|• Maklumat|• Tokokan Harga Peranan aktif<br>• Pandangan Berkaitan Tokokan Harga Peranan|
|  Butiran baris sebut harga|• Maklumat Projek<br>• Cipta Cepat Projek|• Butiran Baris Sebut Harga Aktif<br>• Butiran Baris Sebut Harga Digabungkan<br>• Pandangan Berkaitan Butiran Baris Sebut Harga|
|  Butiran baris Kontrak Projek|• Maklumat Projek<br>• Cipta Cepat Projek|• Butiran Baris Kontrak Digabungkan<br>• Butiran Baris Kontrak Aktif<br>• Pandangan Butiran Baris Kontrak Berkaitan|
|  Tugas Projek|•Maklumat<br>• Borang Baharu||
|  Ahli Pasukan Projek|•Maklumat<br>• Borang Baharu|• Ahli Pasukan Projek Aktif<br>• Ahli Pasukan Projek<br>• Pandangan Berkaitan Ahli Pasukan Projek|
|  Entri Masa|• Maklumat<br>• Cipta Entri Masa|• Entri Masa Saya Mengikut Tarikh<br>• Entri Masa Saya untuk minggu ini<br>• Entri masa untuk kelulusan|
|  Garisan Jurnal|• Maklumat<br>• Cipta pantas|• Baris jurnal aktif<br>• Pandangan Berkaitan Barisan Jurnal|
|  Butiran Baris Invois|• Maklumat<br>• Cipta pantas|• Butiran Baris Invois Aktif<br>• Transaksi Invois Boleh Dituntut<br>• Transaksi Invois Percuma<br>• Pandangan Berkaitan Butiran Baris Invois<br>• Transaksi Invois Tidak Boleh Dituntut|
|  Sebenar|• Maklumat<br>• Aktif Sebenar|• Pandangan Berkaitan Aktual|

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Sediakan sumber boleh tempah sebagai dimensi penentuan harga

1. Dalam antara muka web, pergi ke **Project Service** > **Tetapan** > **Parameter**. Pada halaman **Parameter**, pada tab **Dimensi Penentuan Harga Berasaskan Amaun**, sila maklum bahawa grid pada tab menunjukkan rekod dalam entiti dimensi penentuan harga. 
2. Tambah **Sumber Boleh Tempah** pada senarai dimensi penentuan harga ini sebagai **msdyn_bookableresource**. 
3. Nyatakan konteks yang mana sumber boleh tempah berfungsi sebagai dimensi penentuan harga dan tetapkan nilai **Berkenaan dengan kos** dan **Berkenaan dengan jualan**.
4. Dalam medan **Jenis Dimensi**, pilih **berasaskan Amaun**. 
5. Pilih keutamaan kos dan jualan untuk sumber boleh tempah. Lazimnya, apabila dimasukkan sebagai dimensi penentuan harga, sumber boleh tempah mempunyai keutamaan tertinggi, jadi menetapkan ini pada **1** (atau **0** bergantung pada cara anda mengira keutamaan) akan memastikan tingkah laku tersebut.

## <a name="set-up-pricing-dimension-field-names"></a>Tetapkan nama medan dimensi penentuan harga

Apabila nama medan dimensi penentuan harga dalam jadual **Harga Peranan** berbeza daripada nama medan dalam mana-mana entiti lain di mana melalaikan harga perlu berfungsi, rekod dimensi penentuan harga mestilah maklum dengan nama yang berbeza.    
Untuk sumber boleh tempah, entiti **Ahli Pasukan Projek** mempunyai nama medan yang sedikit berbeza (**msdyn_bookableresourceid**) daripada apa yang dipanggil pada entiti **Harga peranan** (**msdyn_bookableresource**). Rekod dimensi penentuan harga untuk **msydn_bookableresource** mestilah maklum tentang perkara ini. 
1. Untuk melakukan ini, klik dua kali pada baris dalam grid **Dimensi Penentuan Harga** untuk membuka halaman dimensi **msdyn_bookableresource**.
2. Pada halaman dimensi, pada tab **Berkaitan**, klik **Nama Medan Dimensi Penentuan Harga**.

 ![Tab nama medan dimensi penentuan harga](media/PD-fieldname.png)

4. Pada padangan berkaitan yang dibuka, klik **Tanbah Nama Medan Dimensi Penentuan Harga Baharu**.

 ![Tambah Nama Medan Dimensi Penentuan Harga Baharu](media/Add-NewPD-fieldname.png)


Ini membuka halaman **nama medan dimensi Penentuan Harga baharu** untuk **msdyn_bookableresource**. 

5. Tambah **msdyn_projectteam** pada medan **Nama Logik Entiti** dan **msdyn_bookableresourceid** pada medan **Nama Medan**. Simpan rekod.

 ![Borang nama medan dimensi Penentuan Harga baharu](media/PD-fieldname-Added.png)
