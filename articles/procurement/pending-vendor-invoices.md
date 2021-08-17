---
title: Pembelian bahan bukan stok menggunakan invois vendor yang belum selesai
description: Topik ini menerangkan cara untuk merekodkan invois vendor yang belum selesai.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ce9f244eaa549742aeb55024ca9ef4d82cde1bd4a5b9c7f8c762cf72e0da83f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009047"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Pembelian bahan bukan stok menggunakan invois vendor yang belum selesai

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Oleh kerana syarikat memperoleh bahan bukan ada stok untuk projek, kos boleh direkod dengan segera berbanding projek itu. 

Contohnya, Contoso Robotics US melaksanakan projek pembaharuan peralatan dan memerlukan lesen perisian. Lesen ini diperoleh daripada vendor pihak ketiga.  Menggunakan Dynamics 365 Finance, kerani Akaun belum bayar merekodkan dokumen invois yang belum selesai dan mengatributkan kos lesen secara langsung terhadap projek pembaharuan peralatan. 

> [!IMPORTANT]
> Sebelum anda menggunakan kefungsian yang diterangkan dalam topik ini, semak dan gunakan konfigurasi yang diperlukan. Untuk maklumat lanjut, lihat [Dayakan bahan bukan stok dan invois vendor yang belum selesai](configure-materials-nonstocked.md). 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Siarkan invois vendor berkaitan projek yang belum selesai 

Invois vendor yang belum selesai boleh direkodkan pada halaman **Invois vendor yang belum selesai** (**Akaun belum bayar** > **Invois** > **Invois vendor yang belum selesai**). Lengkapkan langkah berikut untuk menyiarkan invois vendor yang berkaitan dengan projek:

1. Pergi ke **Akaun belum bayar** > **Invois** dan pilih **Baharu**. 
2. Dalam medan **Akaun invois**, pilih vendor dan dalam medan **Nombor**, masukkan pengenalan invois vendor.
3. Tambah baris ke invois vendor dan dalam medan **Nombor item**, pilih item bukan stok yang dibeli daripada vendor. 

    > [!NOTE]
    > Baris invois vendor yang berdasarkan pada kategori perolehan tidak boleh direkodkan terhadap projek. 
    
5. Tambah kuantiti yang dibeli. Sistem akan mengisi harga unit berdasarkan pada konfigurasi harga item bukan stok. 
6. Sahkan jumlah amaun dan butiran lain yang diperlukan pada baris.
7. Pada butiran baris, pada tab **Projek**, pilih ID projek yang akan merekodkan item.
8. Secara pilihan, pilih nombor aktiviti dan kemas kini kategori projek dan sifat baris.
9. Siarkan invois vendor yang belum selesai. Apabila invois disiarkan, sistem merekodkan:
    
    - Amaun baki vendor.
    - Amaun cukai jualan.
    - Kos daripada projek itu direkodkan dalam akaun integrasi perolehan.
    - Transaksi sebenar projek dalam Dataverse. Transaksi ini akan diproses lebih lanjut menggunakan [Jurnal Integrasi Project Operations](../project-accounting/project-operations-integration-journal.md). Penyiaran jurnal ini memindahkan amaun daripada akaun integrasi perolehan ke akaun kos projek.
