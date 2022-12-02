---
title: Cipta invois vendor
description: Artikel ini menghuraikan konsep invois vendor dan menerangkan cara untuk menciptanya dalam Microsoft Dynamics 365 Project Operations.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475472"
---
# <a name="create-vendor-invoices"></a>Cipta invois vendor

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Untuk menggunakan fungsi yang diterangkan dalam artikel ini, anda mesti mendayakan ciri **Dayakan pemprosesan aktual subkontrak dengan Project Operations untuk senario berasaskan sumber** dalam ruang kerja **Pengurusan ciri**.

Penginvoisan vendor dalam Microsoft Dynamics 365 Project Operations boleh digunakan untuk merekodkan kos daripada penghantaran perkhidmatan dan/atau bahan pada projek yang diselesaikan oleh vendor.

Apabila perkhidmatan dan/atau bahan merupakan subkontrak kepada vendor, subkontrak mewakili perjanjian kontrak dengan vendor tersebut. Apabila vendor menyampaikan Perkhidmatan, atau sebagai bahan yang diterima dan digunakan pada tugas projek, kos direkodkan pada projek. Vendor akan menghantar invois secara berkala. Invois tersebut disahkan dan dipadankan dengan kos yang direkodkan pada projek. Selepas proses pengesahan selesai, invois vendor disahkan dan dikeluarkan untuk pembayaran.

## <a name="scenarios-for-use"></a>Senario penggunaan

Invois vendor dalam Project Operations boleh digunakan untuk menyokong dua senario yang berbeza:

- Pelanggan menggunakan pengalaman subkontrak penuh.
- Pelanggan tidak menggunakan pengalaman subkontrak penuh tetapi mahu mempunyai pandangan disatukan kos pada projek dalam Project Operations.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Pelanggan menggunakan pengalaman subkontrak penuh

Pengalaman invois vendor menyediakan cara untuk mengesahkan entri masa, penggunaan bahan dan entri perbelanjaan yang merujuk komponen subkontrak, dan dipadankan dengan baris invois vendor. Proses ini boleh digunakan untuk mengesahkan ketepatan baris invois vendor. Selepas proses pengesahan dilengkapkan dan invois vendor disahkan, sistem membalikkan aktual yang dirakam dengan masa yang diluluskan, perbelanjaan dan log penggunaan bahan, kemudian mencipta aktual kos baharu menggunakan baris invois vendor.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Pelanggan tidak menggunakan pengalaman subkontrak penuh tetapi mahu mempunyai pandangan disatukan kos pada projek dalam Project Operations

Jika anda menjejaki proses subkontrak dalam sistem pihak ketiga, anda boleh merekodkan kos daripada sistem pihak ketiga tersebut kepada Project Operations dengan mencipta invois vendor yang tidak merujuk subkontrak. Dengan cara ini, pengurus projek anda boleh mempunyai pandangan tunggal yang disatukan bagi semua kos projek yang diberikan.

## <a name="create-vendor-invoices-in-project-operations"></a>Cipta invois vendor dalam Project Operations

Invois vendor dicipta dalam Dynamics 365 Finance, menggunakan modul **Akaun belum bayar**. Anda tidak boleh mencipta invois vendor secara langsung dalam Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Sediakan pengesahan invois vendor

Jika invois vendor dimaksudkan untuk subkontrak dalam Dataverse, anda mesti mendayakan parameter **Pengesahan manual oleh PM diperlukan**. Tetapan pilihan untuk menentukan sama ada invois vendor seharusnya disahkan dalam Dataverse secara automatik atau sama ada invois vendor tersebut memerlukan pengesahan manual. Pengepala setiap invois vendor projek termasuk pilihan nama yang sama. Secara lalai, pilihan pada pengepala semua invois vendor projek ditetapkan kepada nilai yang anda tetapkan di sini. Walau bagaimanapun, anda boleh mengemas kini nilai seperti yang diperlukan pada pengepala invois vendor individu.

Jika pilihan ditetapkan kepada **Ya**, invois vendor yang dicipta dalam Kewangan dan disegerakkan dengan Dataverse mempunyai status **Draf**. Kemudian invois mestilah disahkan dan ditentusahkan oleh pengurus projek, dan disahkan, sebelum diproses dan disiarkan ke akaun projek dan lejar tertentu dalam Kewangan.

Jika pilihan ditetapkan kepada **Tidak**, invois vendor disahkan secara automatik. Tiada tindakan lanjut diperlukan.

Untuk menyediakan pengesahan invois vendor, ikut langkah ini.

1. Dalam Kewangan, pergi ke **Pengurusan projek dan perakaunan** \> **Persediaan** \> **Parameter pengurusan projek dan perakaunan**.
1. Pada tab **Kewangan**, tetapkan pilihan **Pengesahan manual oleh PM diperlukan** kepada **Ya** jika dasar Syarikat memerlukan pengesahan dalam invois vendor. Jika pengesahan oleh pengurus projek tidak diperlukan dalam Dataverse, biarkan set pilihan kepada **Tidak**. Secara lalai, tetapan akan digunakan pada halaman **Invois vendor belum selesai**.

> [!NOTE]
> Invois vendor yang dicipta untuk subkontrak dalam Dataverse boleh diproses dengan betul hanya jika pilihan **Pengesahan manual oleh PM diperlukan** ditetapkan kepada **Ya**. Kos masa, bahan dan perbelanjaan aktual yang dicipta oleh subkontraktor boleh dipadankan secara manual dengan baris invois vendor oleh pengurus projek hanya jika pilihan ini ditetapkan kepada **Ya**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Sediakan akaun penyepaduan perolehan untuk invois vendor

Apabila invois vendor disiarkan dalam Kewangan untuk Project Operations – Persekitaran bersepadu (bukan saham), kewangan akan disiarkan ke dalam akaun penyepaduan Perolehan. Sistem ini menjana aktual dalam Dataverse untuk invois yang disiarkan. Aktual ini disiarkan dalam Kewangan menggunakan jurnal penyepaduan Projek. Penyiaran jurnal penyepaduan Projek ini menyiarkan kos aktual dan membalikkan akaun penyepaduan Perolehan.

Untuk menyediakan akaun penyepaduan Perolehan untuk invois vendor, ikut langkah ini.

1. Dalam Kewangan, pergi ke **Pengurusan projek dan perakaunan** \> **Persediaan** \> **Parameter pengurusan projek dan perakaunan**.
1. Pada tab **Project Operations pada Dynamics 365 Customer Engagement**, pilih **Bahan** \> **Akaun penyepaduan perolehan**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Cipta dan siarkan invois vendor subkontrak

Apabila kerani Akaun belum bayar menerima invois daripada subkontraktor, invois baharu dicipta dalam Kewangan.

1. Dalam Kewangan, pergi ke **Akaun belum bayar** \> **Invois** \> **Invois vendor belum selesai**.
1. Pada **Anak Tetingkap Tindakan**, pilih **Baharu** untuk mencipta invois vendor.
1. Pada pengepala invois, dalam medan **Akaun invois**, pilih **Subkontraktor**.
1. Pilih tarikh invois.
1. Pada tab **Pengepala**, tetapkan pilihan **Pengesahan manual oleh PM diperlukan** kepada **Ya**. Tetapan lalai bagi pilihan ini datang daripada halaman **Parameter pengurusan projek dan perakaunan**. Walau bagaimanapun, ini boleh ditukar pada peringkat invois vendor.
1. Pada FastTab **Baris invois**, pilih **Tambah baris** untuk mencipta baris invois vendor.
1. Pilih kategori perolehan yang dicipta untuk baris subkontrak, dan masukkan harga unit, unit ukuran dan kuantiti.
1. Dalam bahagian baris invois vendor, pada tab **Projek**, pilih projek yang subkontraktor berkongsi invois subkontrak.
1. Pilih kategori projek. Boleh menjadi sebarang jenis **Item**, **Perbelanjaan**, **Bahan** atau **Jam**.
1. Pilih peranan hanya jika kategori projek yang dipilih merupakan jenis **Jam**.
1. Pilih **Siaran** untuk menyiarkan invois vendor.

Sebagai alternatif, anda boleh mencipta invois vendor dengan pergi ke **Akaun belum bayar** \> **Invois** \> **Buka invois vendor** dan memilih **Baharu**.

Apabila invois vendor disiarkan, invois vendor menjadi tersedia dalam Dataverse untuk pengesahan dan pemprosesan pengurus projek.

## <a name="vendor-invoice-processing-in-dataverse"></a>Pemprosesan invois vendor dalam Dataverse

Dalam invois vendor yang dicipta dalam Dataverse, beberapa nilai medan datang daripada invois vendor yang direkodkan dalam Kewangan. Nilai lain ialah nilai lalai yang datang daripada subkontrak.

Medan berikut dan rekod yang berkaitan akan disalin daripada subkontrak kepada pengepala invois vendor:

- Mata Wang
- Unit pengkontrakan
- Terma pembayaran

Pada baris invois vendor, Project Operations menggunakan nilai medan berikut untuk memasuki subkontrak lalai dan rujukan baris subkontrak:

- Kelas transaksi
- Peranan
- Kategori transaksi
- Medan produk
- Project
- Tugas

> [!NOTE]
> Baris subkontrak harga tetap tidak disokong dalam Project Operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
