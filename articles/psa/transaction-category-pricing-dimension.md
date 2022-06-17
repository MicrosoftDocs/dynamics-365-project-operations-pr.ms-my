---
title: Gunakan kategori urus niaga sebagai dimensi penetapan harga
description: Artikel ini memberikan maklumat tentang menggunakan kategori transaksi sebagai dimensi harga.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 1a1c2dc17c2092e5364d90e7efc1f13aee80703e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915747"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Gunakan kategori urus niaga sebagai dimensi penetapan harga

[!include [banner](../includes/psa-now-project-operations.md)]

Artikel ini menunjukkan cara menggunakan kategori transaksi sebagai dimensi harga. Sebelum anda mulakan, jika anda belum mencipta penyelesaian dimensi penetapan harga, anda akan perlu mencipta yang baharu. Jika anda sudah mempunyai penyelesaian dimensi penetapan harga, anda boleh membuat perubahan anda dalam penyelesaian tersebut. Jika anda belum mencipta penyelesaian dimensi harga baharu untuk organisasi anda, lengkapkan prosedur dalam [artikel Cipta medan dan entiti](create-custom-fields-entities.md) tersuai.

## <a name="add-transaction-category-to-forms-and-views"></a>Tambah kategori urus niaga ke borang dan pandangan
Untuk membuat kategori transaksi boleh dilihat dalam UI dalam penyelesaian dimensi penetapan harga, anda akan perlu berjalan melalui semua borang dan pandangan entiti utama dan menambah medan ini kepada borang dan pandangan entiti tersebut.
Jadual berikut ialah senarai komprehensif bagi borang dan pandangan kotak yang lengkap, yang disenaraikan oleh entiti, yang akan perlu dikemas kini dengan medan baharu. Jika terdapat pandangan tambahan atau borang dalam penyesuaian anda pada entiti ini, tambah medan baharu kepada yang juga.

|  Entiti        | Borang     |Pandangan        |
| ------------------------------|---------------------------------|----------------------------------|
|  Harga Peranan|•Maklumat |•Harga Kategori Sumber Aktif<br> •Pandangan Berkaitan Harga Kategori Sumber|
|  Tokokan Harga Peranan|• Maklumat|• Tokokan Harga Peranan aktif<br>• Pandangan Berkaitan Tokokan Harga Peranan|
|  Butiran baris sebut harga|• Maklumat Projek<br>• Cipta Cepat Projek|• Butiran Baris Sebut Harga Aktif<br>• Butiran Baris Sebut Harga Digabungkan<br>• Pandangan Berkaitan Butiran Baris Sebut Harga|
|  Butiran baris Kontrak Projek|• Maklumat Projek<br>• Cipta Cepat Projek|• Butiran Baris Kontrak Digabungkan<br>• Butiran Baris Kontrak Aktif<br>• Pandangan Butiran Baris Kontrak Berkaitan|
|  Tugas Projek|•Maklumat<br>• Borang Baharu||
|  Ahli Pasukan Projek|•Maklumat<br>• Borang Baharu|• Ahli Pasukan Projek Aktif<br>• Ahli Pasukan Projek<br>• Pandangan Berkaitan Ahli Pasukan Projek|
|  Entri Masa|• Maklumat<br>• Cipta Entri Masa|• Entri Masa Saya Mengikut Tarikh<br>• Entri Masa Saya untuk minggu ini<br>• Entri masa untuk kelulusan|
|  Garisan Jurnal|• Maklumat<br>• Cipta pantas|• Baris jurnal aktif<br>• Pandangan Berkaitan Barisan Jurnal|
|  Butiran Baris Invois|• Maklumat<br>• Cipta pantas|• Butiran Baris Invois Aktif<br>• Transaksi Invois Boleh Dituntut<br>• Transaksi Invois Percuma<br>• Pandangan Berkaitan Butiran Baris Invois<br>• Transaksi Invois Tidak Boleh Dituntut|
|  Sebenar|• Maklumat<br>• Aktif Sebenar|• Pandangan Berkaitan Aktual|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Sediakan kategori urus niaga sebagai dimensi penetapan harga

1. Dalam antara muka web, pergi ke **Project Service** > **Tetapan** > **Parameter**. 
2. Pada halaman **Parameters**, pada tab **Dimensi Penetapan Harga Berdasarkan Jumlah** perhatikan grid pada tab menunjukkan rekod dalam entiti **Dimensi Penetapan Harga**.
3. Tambah **Kategori Transaksi** ke senarai ini dan tetapkan medan **Digunakan pada Kos** dan **Digunakan pada Jualan** ditetapkan kepada **Ya**.
4. Dalam medan **Jenis Dimensi** pilih **Berdasarkan jumlah** dan kemudian pilih keutamaan untuk **Kategori Transaksi** yang berkaitan dengan kos dan jualan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
