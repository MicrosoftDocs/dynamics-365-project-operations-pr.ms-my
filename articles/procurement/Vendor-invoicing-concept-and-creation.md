---
title: Buat invois vendor
description: Artikel ini menerangkan konsep invois vendor dan menerangkan cara menciptanya dalam Microsoft Dynamics 365 Project Operations.
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
# <a name="create-vendor-invoices"></a>Buat invois vendor

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Untuk menggunakan kefungsian yang diterangkan dalam artikel ini, anda mesti mendayakan **ciri Dayakan subkontrak pemprosesan sebenar dengan Operasi Projek untuk senario** berasaskan sumber dalam **ruang kerja Pengurusan** ciri.

Invois vendor dalam Microsoft Dynamics 365 Project Operations boleh digunakan untuk merekodkan kos daripada penghantaran perkhidmatan dan/atau bahan pada projek yang disiapkan oleh vendor.

Apabila perkhidmatan dan/atau bahan disubkontrak kepada vendor, subkontrak mewakili perjanjian kontrak dengan vendor tersebut. Oleh kerana vendor menyampaikan perkhidmatan, atau sebagai bahan yang diterima dan digunakan pada tugas projek, kos direkodkan pada projek. Penjual kemudian menghantar invois secara berkala. Invois tersebut disahkan dan dipadankan dengan kos yang direkodkan pada projek. Selepas proses pengesahan selesai, invois vendor disahkan dan dikeluarkan untuk pembayaran.

## <a name="scenarios-for-use"></a>Senario untuk digunakan

Invois vendor dalam Operasi Projek boleh digunakan untuk menyokong dua senario berbeza:

- Pelanggan menggunakan pengalaman subkontrak penuh.
- Pelanggan tidak menggunakan pengalaman subkontrak penuh tetapi ingin mempunyai pandangan kos yang bersatu mengenai projek dalam Operasi Projek.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Pelanggan menggunakan pengalaman subkontrak penuh

Pengalaman invois vendor menyediakan cara untuk mengesahkan entri masa, penggunaan bahan dan entri perbelanjaan yang merujuk komponen subkontrak dan memadankannya dengan baris invois vendor. Proses ini boleh digunakan untuk mengesahkan ketepatan talian invois vendor. Selepas proses pengesahan selesai dan invois vendor disahkan, sistem membalikkan sebenar yang direkodkan oleh masa, perbelanjaan dan log penggunaan bahan yang diluluskan, dan kemudian mencipta kos sebenar baharu dengan menggunakan baris invois vendor.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Pelanggan tidak menggunakan pengalaman subkontrak penuh tetapi ingin mempunyai pandangan kos yang bersatu pada projek dalam Operasi Projek

Jika anda menjejaki proses subkontrak dalam sistem pihak ketiga, anda boleh merekodkan kos daripada sistem pihak ketiga tersebut kepada Operasi Projek dengan mencipta invois vendor yang tidak merujuk subkontrak. Dengan cara ini, pengurus projek anda boleh mempunyai pandangan tunggal yang bersatu mengenai semua kos pada projek tertentu.

## <a name="create-vendor-invoices-in-project-operations"></a>Cipta invois vendor dalam Operasi Projek

Invois vendor dibuat dalam Dynamics 365 Finance, dengan **menggunakan modul Akaun yang perlu dibayar**. Anda tidak boleh membuat invois vendor terus dalam Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Sediakan pengesahan invois vendor

Jika invois vendor dimaksudkan untuk subkontrak, Dataverse anda mesti mendayakan **pengesahan Manual oleh PM parameter diperlukan**. Tetapan pilihan menentukan sama ada invois vendor harus disahkan secara automatik dalam Dataverse, atau sama ada ia memerlukan pengesahan manual. Tajuk setiap invois vendor projek termasuk pilihan nama yang sama. Secara lalai, opsyen pada pengepala semua invois vendor projek disetkan kepada nilai yang anda setkan di sini. Walau bagaimanapun, anda boleh mengemas kini nilai seperti yang diperlukan pada tajuk invois vendor individu.

Jika pilihan disetkan kepada **Ya**, invois vendor yang dicipta dalam Kewangan dan disegerakkan untuk Dataverse mempunyai **status Draf**. Invois kemudiannya mesti disahkan dan disahkan oleh pengurus projek, dan disahkan, sebelum diproses dan diposkan ke akaun projek dan lejar tertentu dalam Kewangan.

Jika opsyen disetkan kepada **Tidak**, invois vendor disahkan secara automatik. Tiada tindakan lanjut diperlukan.

Untuk menyediakan pengesahan invois vendor, ikut langkah ini.

1. Dalam Kewangan, pergi ke **pengurusan Projek dan perakaunan** \> **Pengurusan** \> **Projek dan parameter** perakaunan.
1. Pada tab **Kewangan**, setkan **pilihan Pengesahan manual oleh PM diperlukan** kepada **Ya** jika dasar syarikat memerlukan pengesahan invois vendor subkontraktor. Jika pengesahan oleh pengurus projek tidak diperlukan Dataverse, serahkan set pilihan kepada **Tidak**. Secara lalai, seting akan digunakan pada halaman Invois **vendor belum** selesai.

> [!NOTE]
> Invois vendor yang dicipta untuk subkontrak boleh Dataverse diproses dengan betul hanya jika **pilihan Pengesahan manual oleh PM diperlukan** disetkan kepada **Ya**. Kos masa, bahan dan perbelanjaan sebenarnya yang dibuat oleh subkontraktor boleh dipadankan secara manual dengan baris invois vendor oleh pengurus projek hanya jika pilihan ini ditetapkan kepada **Ya**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Sediakan akaun integrasi perolehan untuk invois vendor

Apabila invois vendor disiarkan dalam Kewangan untuk Operasi Projek - Persekitaran bersepadu (bukan stok), kewangan diposkan ke akaun integrasi Perolehan. Sistem ini menjana sebenar untuk Dataverse invois yang disiarkan. Sebenarnya ini disiarkan dalam Kewangan dengan menggunakan jurnal integrasi Projek. Penyiaran jurnal integrasi Projek menyiarkan kos sebenar dan membalikkan akaun integrasi Perolehan.

Untuk menyediakan akaun integrasi Perolehan untuk invois vendor, ikuti langkah ini.

1. Dalam Kewangan, pergi ke **pengurusan Projek dan perakaunan** \> **Pengurusan** \> **Projek dan parameter** perakaunan.
1. **Pada operasi Projek pada tab penglibatan** pelanggan Dynamics 365, pilih **akaun** integrasi Perolehan Bahan \>**·**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Mencipta dan menyiarkan invois vendor subkontrak

Apabila kerani akaun belum bayar menerima invois daripada subkontraktor, invois baharu dicipta dalam Kewangan.

1. Dalam Kewangan, pergi ke **Invois pemiutang** \> **Akaun Menunggu** \> **invois vendor**.
1. **Pada Anak Tetingkap** Tindakan, pilih **Baru** untuk mencipta invois vendor.
1. Pada pengepala invois, dalam **medan Akaun invois**, pilih **Subkontraktor**.
1. Pilih tarikh invois.
1. Pada tab **Pengepala**, setkan **opsyen Pengesahan Manual oleh PM diperlukan** kepada **Ya**. Tetapan lalai opsyen ini berasal dari **halaman parameter** pengurusan dan perakaunan Projek. Walau bagaimanapun, ia boleh diubah pada tahap invois vendor.
1. **Pada baris** Invois FastTab, pilih **Tambah baris** untuk mencipta baris invois vendor.
1. Pilih kategori perolehan yang dicipta untuk garis subkontrak, dan masukkan harga unit, unit pengukuran dan kuantiti.
1. Dalam seksyen baris invois vendor, pada tab **Projek**, pilih projek yang subkontraktor berkongsi invois subkontrak.
1. Pilih kategori projek. Ia boleh terdiri daripada sebarang jenis Item, Perbelanjaan, Bahan, atau **Jam**.**·** **·** **·**
1. Pilih peranan hanya jika kategori projek yang dipilih ialah **jenis Jam**.
1. Pilih **Hantar** untuk menyiarkan invois vendor.

Sebagai alternatif, anda boleh membuat invois vendor dengan pergi ke **Invois** \> **belum bayar** \> **Akaun Buka invois vendor** dan memilih **Baharu.**

Apabila invois vendor disiarkan, ia tersedia Dataverse untuk pengesahan dan pemprosesan pengurus projek.

## <a name="vendor-invoice-processing-in-dataverse"></a>Pemprosesan invois vendor dalam Dataverse

Dalam invois vendor yang dicipta dalam Dataverse, beberapa nilai medan datang daripada invois vendor yang direkodkan dalam Kewangan. Nilai lain ialah nilai lalai yang datang daripada subkontrak.

Medan berikut dan rekod berkaitan akan disalin daripada subkontrak kepada pengepala invois vendor:

- Mata Wang
- Unit pengkontrakan
- Terma pembayaran

Pada baris invois vendor, Operasi Projek menggunakan nilai medan berikut untuk memasukkan subkontrak lalai dan rujukan garis subkontrak:

- Kelas transaksi
- Peranan
- Kategori transaksi
- Bidang produk
- Project
- Tugas

> [!NOTE]
> Garis subkontrak harga tetap tidak disokong dalam Operasi Projek.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
