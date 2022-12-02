---
title: Gunakan kategori perolehan dengan pesanan pembelian projek dan invois vendor yang belum selesai
description: Artikel ini menerangkan cara mengkonfigurasi kategori perolehan yang boleh digunakan dengan pesanan pembelian projek dan invois vendor yang belum selesai.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f71c6bfcd183613471a4cc10e16a5a54571fac31
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028621"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Gunakan kategori perolehan dengan pesanan pembelian projek dan invois vendor yang belum selesai

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Profesional pembelian boleh mencipta dan menyelenggara katalog item dan perkhidmatan yang boleh digunakan dalam pesanan pembelian projek dan invois vendor yang belum selesai. [Katalog perolehan](/dynamics365/supply-chain/procurement/procurement-catalogs) memberikan anda cara mudah untuk mengkategorikan pembelian tanpa perlu mengkonfigurasi dan menggunakan katalog keluaran keluaran. Setiap kategori perolehan boleh dipetakan kepada kategori projek untuk masa, perbelanjaan atau transaksi item. Selepas invois vendor yang belum selesai yang menggunakan kategori perolehan disiarkan, sistem akan mencipta aktual projek masa, perbelanjaan atau material, transaksi projek dan entri sublejar.

## <a name="minimum-version-requirements"></a>Keperluan versi minimum

Versi berikut diperlukan untuk menggunakan kategori perolehan dengan pesanan pembelian projek untuk senario bukan stok/berasaskan sumber Microsoft Dynamics 365 Project Operations:

- Penyelesaian Project Operations Dataverse versi 4.41.0.45 atau lebih terkini
- Persekitaran kewangan dan operasi versi 10.0.26 atau lebih terkini

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Jalankan peta dwitulis untuk sokongan kategori perolehan

Pastikan bahawa pemetaan untuk **Entiti eksport baris vendor projek integrasi Project Operations msdyn\_projectvendorinvoicelines** menggunakan versi 1.0.0.4 atau lebih terkini.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Dayakan kunci ciri untuk kategori perolehan

Ikut langkah ini untuk mendayakan fungsi untuk menggunakan kategori perolehan dengan pesanan pembelian projek.

1. Dalam Dynamics 365 Finance, buka ruang kerja **Pengurusan ciri**.
1. Dalam senarai ciri, cari ciri **Gunakan kategori perolehan dalam Project Operations untuk senario berdasarkan sumber/bukan stok** dan kemudian pilih **Dayakan**.

> [!IMPORTANT]
> Sebagai prasyarat, anda juga mesti mendayakan ciri **Dayakan invois vendor yang belum selesai pada Project Operations untuk senario berdasarkan sumber/bukan stok**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Petakan kategori projek dalam hierarki kategori Perolehan

Ikut langkah ini untuk memetakan kategori projek kepada kategori perolehan dalam hierarki **Kategori perolehan**:

1. Pergi ke **Perolehan dan penyumberan \> Kategori perolehan**.
1. Pilih **Edit hierarki kategori**.
1. Pilih nod hierarki kategori yang dikehendaki dan kemudian, pada tab **Untukkan kategori projek**, kaitkan nod dengan kategori projek daripada kategori **Masa**, **Perbelanjaan** atau **Projek Item** (iaitu kategori **Masa Lalai** atau **Perbelanjaan Lalai**).
1. Pilih **Simpan**.
1. Tutup halaman.

> [!NOTE]
> Pemetaan kategori perolehan kepada kategori projek adalah pilihan. Jika kategori perolehan tidak dipetakan, sistem akan menggunakan nilai yang ditetapkan dalam medan **Item** dalam bahagian **Lalai kategori projek** pada tab **Project Operations pada Dynamics 365 Customer Engagement** bagi halaman **Parameter pengurusan projek dan perakaunan**.
