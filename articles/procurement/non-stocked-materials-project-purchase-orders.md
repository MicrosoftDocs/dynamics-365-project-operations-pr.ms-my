---
title: Pesanan bahan bukan stok untuk projek menggunakan pesanan pembelian projek
description: Artikel ini menerangkan cara anda boleh memesan bahan bukan stok untuk projek menggunakan pesanan pembelian projek.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fe24faa143869af2396f3b0f28aae31417cadda7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929823"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Perintahkan kategori perolehan atau bahan bukan stok untuk projek menggunakan pesanan pembelian projek

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Jabatan perolehan dalam organisasi anda mungkin menggunakan [pesanan pembelian](/dynamics365/supply-chain/procurement/purchase-order-overview) untuk menjejak pesanan barangan dan perkhidmatan. Pesanan pembelian untuk kategori perolehan atau bahan bukan stok boleh dikaitkan dengan projek. Penginvoisan pesanan pembelian ini merekodkan kos projek itu.

## <a name="prerequisites"></a>Prasyarat
Lengkapkan langkah berikut untuk mendayakan kefungsian pesanan pembelian projek.

1. Dalam Dynamics 365 Finance, pergi ke **ruang kerja Pengurusan** Ciri.
2. Dalam senarai ciri, cari dan pilih ciri, **Dayakan pesanan pembelian projek pada Project Operations untuk senario berasaskan sumber/bukan stok**.
3. Pilih **Dayakan**.
4. Konfigurasikan bahan bukan stok dan invois vendor yang belum selesai seperti yang diterangkan dalam [Konfigurasikan bahan bukan stok dan invois vendor yang belum selesai](configure-materials-nonstocked.md).
5. Konfigurasikan kategori perolehan seperti yang diterangkan dalam [Gunakan kategori perolehan dengan pesanan pembelian projek dan invois vendor yang belum selesai](configure-procurement-categories.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Cipta pesanan pembelian projek daripada senarai pesanan pembelian projek

1. Dalam kewangan, pergi ke **Pengurusan projek dan perakaunan** > **Projek** > **Semua Projek** dan pilih projek.
2. Pada Anak Tetingkap Tindakan, pada tab **Uruskan**, dalam kumpulan **Baharu**, pilih **Tugas item** > **Pesanan pembelian**.
3. Pada halaman **Cipta pesanan pembelian**, pilih vendor yang anda ingin membuat pesanan pembelian, masukkan maklumat lain sewajarnya dan kemudian pilih **OK**.
4. Pada halaman **Pesanan pembelian**, dalam grid **Baris pesanan pembelian**, pilih **Tambah baris**.
5. Masukkan nombor item atau kategori perolehan, kuantiti, unit, harga unit, dan maklumat lain yang sesuai.

    > [!NOTE]
    > Hanya kategori perolehan, item tidak berstok, dan perkhidmatan boleh digunakan dengan pesanan pembelian projek. Item stok tidak disokong.

6. Teruskan menambah item atau kategori perolehan seperti yang diperlukan, dan sahkan pesanan pembelian.

    Resit barangan dan perkhidmatan boleh direkodkan dengan mencipta dan menyiarkan resit produk.

    > [!NOTE]
    > Resit produk tidak direkodkan ke aktual projek dalam Microsoft Dataverse dan tidak mempengaruhi sublejar projek.

    Selepas vendor menghantar invois untuk item dan perkhidmatan pada pesanan pembelian, jabatan perolehan boleh menjana invois untuk pesanan pembelian dengan pergi ke **Invois** > **Janakan** > **Invois** pada Anak Tetingkap Tindakan. Untuk maklumat lanjut tentang invois vendor belum selesai, lihat [Pembelian bahan bukan stok menggunakan invois vendor belum selesai](pending-vendor-invoices.md).
