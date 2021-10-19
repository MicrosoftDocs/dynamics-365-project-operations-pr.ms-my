---
title: Pesanan bahan bukan stok untuk projek menggunakan pesanan pembelian projek
description: Topik ini menerangkan cara anda boleh memesan bahan bukan stok untuk projek menggunakan pesanan pembelian projek.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6e0307ad6474feef96fc8080877eccbbbc7259db
ms.sourcegitcommit: 2d96345fb3afc3b174530285f95271b5ccbdea03
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/29/2021
ms.locfileid: "7563033"
---
# <a name="order-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Pesanan bahan bukan stok untuk projek menggunakan pesanan pembelian projek

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Jabatan perolehan dalam organisasi anda mungkin menggunakan [pesanan pembelian](/dynamics365/supply-chain/procurement/purchase-order-overview) untuk menjejak pesanan barangan dan perkhidmatan. Pesanan pembelian untuk bahan bukan stok boleh diatributkan ke projek. Penginvoisan pesanan pembelian ini merekodkan kos projek itu.

## <a name="prerequisites"></a>Prasyarat
Lengkapkan langkah berikut untuk mendayakan kefungsian pesanan pembelian projek.

1. Dalam Dynamics 365 Finance, pergi ke ruang kerja **Pengurusan Ciri**.
2. Dalam senarai ciri, cari dan pilih ciri, **Dayakan pesanan pembelian projek pada Project Operations untuk senario berasaskan sumber/bukan stok**.
3. Pilih **Dayakan**.
4. Konfigurasikan bahan bukan stok dan invois vendor yang belum selesai seperti yang diterangkan dalam [Konfigurasikan bahan bukan stok dan invois vendor yang belum selesai](configure-materials-nonstocked.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Cipta pesanan pembelian projek daripada senarai pesanan pembelian projek

1. Dalam kewangan, pergi ke **Pengurusan projek dan perakaunan** > **Projek** > **Semua Projek** dan pilih projek.
2. Pada Anak Tetingkap Tindakan, pada tab **Uruskan**, dalam kumpulan **Baharu**, pilih **Tugas item** > **Pesanan pembelian**.
3. Pada halaman **Cipta pesanan pembelian**, pilih vendor yang anda ingin membuat pesanan pembelian, masukkan maklumat lain sewajarnya dan kemudian pilih **OK**.
4. Pada halaman **Pesanan pembelian**, dalam grid **Baris pesanan pembelian**, pilih **Tambah baris**.
5. Masukkan nombor item, kuantiti, unit, harga unit dan maklumat lain sewajarnya.

    > [!NOTE]
    > Hanya item dan perkhidmatan bukan stok boleh digunakan dengan pesanan pembelian projek. Item stok dan kategori perolehan tidak disokong.

6. Teruskan menambah item yang diperlukan dan sahkan pesanan pembelian.

    Resit barangan dan perkhidmatan boleh direkodkan dengan mencipta dan menyiarkan resit produk.

    > [!NOTE]
    > Resit produk tidak direkodkan ke aktual projek dalam Microsoft Dataverse dan tidak mempengaruhi sublejar projek.

    Selepas vendor menghantar invois untuk item dan perkhidmatan pada pesanan pembelian, jabatan perolehan boleh menjana invois untuk pesanan pembelian dengan pergi ke **Invois** > **Janakan** > **Invois** pada Anak Tetingkap Tindakan. Untuk maklumat lanjut tentang invois vendor belum selesai, lihat [Pembelian bahan bukan stok menggunakan invois vendor belum selesai](pending-vendor-invoices.md).
