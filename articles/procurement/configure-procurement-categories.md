---
title: Gunakan kategori perolehan dengan pesanan pembelian projek dan invois vendor yang belum selesai
description: Artikel ini menerangkan cara mengkonfigurasi kategori perolehan yang boleh digunakan dengan pesanan pembelian projek dan invois vendor yang belum selesai.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7d774631a4712de9b29ddedfee2ea3fc4a2d436f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927431"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Gunakan kategori perolehan dengan pesanan pembelian projek dan invois vendor yang belum selesai

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Profesional pembelian boleh membuat dan mengekalkan katalog item dan perkhidmatan yang boleh digunakan dalam pesanan pembelian projek dan invois vendor yang belum selesai. [Katalog perolehan](/dynamics365/supply-chain/procurement/procurement-catalogs) memberi anda cara mudah untuk mengkategorikan pembelian tanpa perlu mengkonfigurasi dan menggunakan katalog produk yang dikeluarkan. Setiap kategori perolehan boleh dipetakan ke kategori projek untuk masa, perbelanjaan atau transaksi item. Selepas invois vendor yang belum selesai yang menggunakan kategori perolehan disiarkan, sistem akan mencipta masa, perbelanjaan atau sebenar projek bahan, transaksi projek dan entri subledger.

## <a name="minimum-version-requirements"></a>Keperluan versi minimum

Versi berikut diperlukan untuk menggunakan kategori perolehan dengan pesanan pembelian projek untuk senario bukan stok/berasaskan sumber Microsoft Dynamics 365 Project Operations:

- Versi penyelesaian Project Operations Dataverse 4.41.0.45 atau lebih baru
- Persekitaran Kewangan dan Operasi versi 10.0.26 atau lebih baru

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Jalankan peta dwi-tulis untuk sokongan kategori perolehan

Pastikan pemetaan untuk **projek integrasi Project Operations vendor invois talian invois entiti eksport msdyn\_ projectvendorinvoicelines** menggunakan versi 1.0.0.4 atau lebih baru.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Mendayakan kekunci ciri untuk kategori perolehan

Ikuti langkah ini untuk mendayakan kefungsian untuk menggunakan kategori perolehan dengan pesanan pembelian projek.

1. Dalam Dynamics 365 Finance, buka **ruang kerja pengurusan** Ciri.
1. Dalam senarai ciri, cari **ciri Gunakan kategori perolehan dalam Operasi Projek untuk senario berasaskan sumber/tidak berstok**, kemudian pilih **Dayakan**.

> [!IMPORTANT]
> Sebagai prasyarat, anda juga mesti mendayakan **ciri Dayakan invois vendor yang belum selesai pada Operasi Projek untuk ciri senario berasaskan sumber/tidak berstok**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Petakan kategori projek dalam hierarki kategori Perolehan

Ikuti langkah ini untuk memetakan kategori projek kepada kategori perolehan dalam **hierarki kategori** Perolehan:

1. Pergi ke **kategori \> Perolehan dan Penyumberan** Perolehan.
1. Pilih **Edit hierarki** kategori.
1. Pilih nod hierarki kategori yang dikehendaki, kemudian, pada **tab Peruntukkan kategori** projek, kaitkan nod dengan kategori projek daripada **kategori Masa**, **Perbelanjaan** atau, **Projek** Item (iaitu kategori **Masa-Masa atau** Perbelanjaan **Lalai**).
1. Pilih **Simpan**.
1. Tutup halaman.

> [!NOTE]
> Pemetaan kategori perolehan ke kategori projek adalah pilihan. Jika kategori perolehan tidak dipetakan, sistem akan menggunakan nilai yang disetkan dalam **medan Item** dalam **seksyen lalai** kategori Projek pada **tab Operasi Projek pada Dynamics 365 Penglibatan pelanggan** halaman **pengurusan Projek dan parameter** perakaunan.
