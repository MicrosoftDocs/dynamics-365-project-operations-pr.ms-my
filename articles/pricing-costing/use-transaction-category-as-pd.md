---
title: Gunakan Kategori Transaksi sebagai dimensi penentuan harga
description: Artikel ini memberikan maklumat tentang cara menggunakan medan Kategori Transaksi sebagai dimensi harga.
author: rumant
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 648933299616a683b19bbe2f1231caac779bd1f8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911705"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Gunakan Kategori Transaksi sebagai dimensi penentuan harga


_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_


Artikel ini menerangkan cara menggunakan medan **Kategori** Transaksi sebagai dimensi harga. 

## <a name="prerequisites"></a>Prasyarat
Sebelum anda melengkapkan prosedur dalam artikel ini, anda mesti mempunyai penyelesaian dimensi harga baru untuk organisasi anda. Jika anda belum menciptanya, lihat [Cipta medan dan entiti tersuai sebagai dimensi penentuan harga](create-custom-fields-entities-pricing-dimensions.md).

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