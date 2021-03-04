---
title: Gunakan Kategori Transaksi sebagai dimensi penentuan harga
description: Topik ini memberikan maklumat tentang cara menggunakan medan Kategori Transaksi sebagai dimensi penentuan harga.
author: rumant
manager: tfehr
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bace11455d34fdda95e08be1a7cc37850a0cf589
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514008"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Gunakan Kategori Transaksi sebagai dimensi penentuan harga


_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_


Topik ini menerangkan cara menggunakan medan **Kategori Transaksi** sebagai dimensi penentuan harga. 

## <a name="prerequisites"></a>Prasyarat
Sebelum anda melengkapkan prosedur dalam topik ini, anda mesti mempunyai penyelesaian dimensi penentuan harga baharu untuk organisasi anda. Jika anda belum menciptanya, lihat [Cipta medan dan entiti tersuai sebagai dimensi penentuan harga](create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>Tambahkan medan Kategori Transaksi pada borang dan pandangan
Untuk menjadikan medan **Kategori Transaksi** boleh dilihat dalam penyelesaian dimensi penentuan harga, anda perlu menambah medan kepada semua borang dan pandangan sebagai entiti.

Jadual berikut menyenaraikan semua borang dan pandangan siap guna, mengikut entiti. Anda juga perlu menambah medan baharu pada sebarang borang atau pandangan tambahan dalam entiti tersuai anda.

|  EntitI        | Borang     |Pandangan        |
| ------------------------------|---------------------------------|----------------------------------|
|  Harga Peranan| Maklumat |- Harga Kategori Sumber Aktif<br> - Harga Kategori Sumber Berkaitan |
|  Tokokan Harga Peranan| Maklumat|- Tokokan Harga Peranan aktif<br>- Tokokan Harga Peranan Berkaitan |
|  Butiran Baris Sebut Harga|- Maklumat Projek<br>- Cipta Cepat Projek| - Butiran Baris Sebut Harga Aktif<br>- Butiran Baris Sebut Harga Digabungkan<br>- Butiran Baris Sebut Harga Berkaitan |
|  Butiran Baris Kontrak Projek|- Maklumat Projek<br>- Cipta Cepat Projek|- Butiran Baris Kontrak Digabungkan<br>- Butiran Baris Kontrak Aktif<br>- Butiran Baris Kontrak Berkaitan |
|  Tugas Projek|- Maklumat<br>- Borang Baharu| &nbsp; |
|  Ahli Pasukan Projek|- Maklumat<br>- Borang Baharu|- Ahli Pasukan Projek Aktif<br>- Ahli Pasukan Projek<br>- Ahli Pasukan Projek Berkaitan |
|  Entri Masa|- Maklumat<br>- Cipta Entri Masa|- Entri Masa Saya Mengikut Tarikh<br>- Entri Masa Saya untuk Minggu ini<br>- Entri Masa untuk Kelulusan|
|  Garisan Jurnal|- Maklumat<br>- Cipta Cepat|- Garisan Jurnal Aktif<br>- Garisan Jurnal Berkaitan|
|  Butiran Baris Invois|- Maklumat<br>- Cipta Cepat|- Butiran Baris Invois Aktif<br>- Transaksi Invois Boleh Dituntut<br>- Transaksi Invois Percuma<br>- Butiran Baris Invois Berkaitan <br>- Transaksi Invois Tidak Boleh Dituntut|
|  Sebenar|- Maklumat<br>- Aktual Aktif| Berkaitan Sebenar |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>Sediakan medan Kategori Transaksi sebagai dimensi penentuan harga

1. Pergi ke **Tetapan** > **Parameter**. 
2. Pada halaman **Parameter**, pada tab **Dimensi Penentuan Harga Berdasarkan Jumlah** sahkan bahawa grid menunjukkan rekod dalam entiti **Dimensi Penentuan Harga**.
3. Tambah **Kategori Transaksi** pada senarai ini dan tetapkan medan **Digunakan pada Kos** dan **Digunakan pada Jualan** kepada **Ya**.
4. Dalam medan **Jenis Dimensi** pilih **Berdasarkan jumlah** dan kemudian pilih keutamaan untuk **Kategori Transaksi** kerana ia berkaitan dengan kos dan jualan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]