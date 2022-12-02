---
title: Pembelian bahan bukan stok atau kategori perolehan menggunakan invois vendor yang belum selesai
description: Artikel ini menerangkan cara untuk merekodkan invois vendor yang belum selesai.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1c05755f6759e90e031a11261f15a2c4b6b716e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922003"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Pembelian bahan bukan stok atau kategori perolehan menggunakan invois vendor yang belum selesai

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Apabila syarikat memperoleh bahan bukan stok atau kategori perolehan untuk projek, kos boleh direkod dengan segera terhadap projek itu. 

Contohnya, Contoso Robotics US sedang melakukan projek pembaharuan peralatan dan memerlukan lesen perisian. Lesen ini diperoleh daripada vendor pihak ketiga.  Dengan menggunakan Dynamics 365 Finance, kerani Akaun belum bayar merekodkan dokumen invois yang belum selesai dan mengatributkan kos lesen secara langsung terhadap projek pembaharuan peralatan. 

> [!IMPORTANT]
> Sebelum anda menggunakan kefungsian yang diterangkan dalam artikel ini, semak dan gunakan konfigurasi yang diperlukan. Untuk mendapatkan maklumat lanjut, lihat [Dayakan bahan bukan stok dan invois vendor yang belum selesai](configure-materials-nonstocked.md) dan [Gunakan kategori perolehan dengan pesanan pembelian projek dan invois penjual yang belum selesai](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Siarkan invois vendor berkaitan projek yang belum selesai 

Invois vendor yang belum selesai boleh direkodkan pada halaman **Invois vendor yang belum selesai** (**Akaun belum bayar** > **Invois** > **Invois vendor yang belum selesai**). Lengkapkan langkah berikut untuk menyiarkan invois vendor yang berkaitan dengan projek:

1. Pergi ke **Akaun belum bayar** > **Invois** dan pilih **Baharu**. 
1. Dalam medan **Akaun invois**, pilih vendor dan kemudian dalam medan **Nombor**, masukkan pengenalan invois vendor.
1. Tambahkan baris kepada invois vendor dan kemudian dalam medan **Nombor item**, pilih item bukan stok yang telah dibeli daripada vendor. Sebagai alternatif, dalam medan **Kategori perolehan**, pilih kategori perolehan yang dibeli daripada vendor.   
1. Tambahkan kuantiti yang telah dibeli. Sistem mengisi harga unit berdasarkan pada konfigurasi harga item bukan stok. 
1. Sahkan jumlah amaun dan butiran lain yang diperlukan pada baris.
1. Dalam butiran baris, pada tab **Projek**, pilih ID projek yang akan merekodkan item ini.
1. Pilihan: Pilih nombor aktiviti dan kemas kini kategori projek dan sifat baris.
1. Siarkan invois vendor yang belum selesai. Apabila invois disiarkan, sistem merekodkan maklumat berikut:
    
    - Amaun baki vendor.
    - Amaun cukai jualan.
    - Kos daripada projek itu direkodkan dalam akaun integrasi perolehan.
    - Transaksi kos aktual projek dalam Dataverse.  Transaksi ini akan diproses lebih lanjut menggunakan [Jurnal Integrasi Project Operations](../project-accounting/project-operations-integration-journal.md). Penyiaran jurnal ini memindahkan amaun daripada akaun integrasi perolehan ke akaun kos projek. 
    - Pembelian yang dibilkan kepada pelanggan projek yang menggunakan kaedah pengebilan masa dan bahan. Selain itu, transaksi jualan yang tidak dibilkan dicipta untuk pembelian dalam Dataverse. Senarai harga produk dalam Dataverse digunakan untuk harga dan jumlah jualan bagi transaksi jualan yang tidak dibilkan.
