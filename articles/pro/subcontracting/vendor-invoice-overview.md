---
title: Penginvoisan vendor - Konsep dan penciptaan
description: Artikel ini menerangkan konsep invois vendor, senario untuk digunakan dan cara membuat invois vendor dalam Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b57ec8cdb6097e6f2207056667aadfb43ee8acfc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261955"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Penginvoisan vendor - Konsep dan penciptaan

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Invois vendor dalam Microsoft Dynamics 365 Project Operations boleh digunakan untuk merekodkan kos daripada penghantaran perkhidmatan dan/atau bahan pada projek oleh vendor.

Apabila perkhidmatan dan/atau bahan disubkontrak kepada vendor, subkontrak mewakili perjanjian kontrak dengan vendor tersebut. Oleh kerana vendor menyampaikan perkhidmatan, atau bahan-bahan yang diterima dan digunakan pada tugas projek, kos direkodkan pada projek. Secara berkala, vendor menghantar invois yang disahkan dan dipadankan dengan kos yang direkodkan pada projek. Selepas proses pengesahan selesai, invois vendor disahkan dan dikeluarkan untuk pembayaran.

## <a name="scenarios-for-use"></a>Senario untuk digunakan

Invois vendor dalam Operasi Projek boleh digunakan untuk menyokong dua senario berbeza.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Pelanggan menggunakan pengalaman subkontrak penuh

Pengalaman invois vendor menyediakan cara untuk mengesahkan dan memadankan entri masa, penggunaan bahan dan entri perbelanjaan yang merujuk komponen subkontrak dengan baris invois vendor. Proses ini boleh digunakan untuk mengesahkan ketepatan talian invois vendor. Selepas proses pengesahan selesai dan invois vendor disahkan, permohonan akan membalikkan sebenar yang telah direkodkan oleh masa, perbelanjaan dan log penggunaan bahan yang diluluskan, dan membuat kos sebenar baharu dengan menggunakan baris invois vendor.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Pelanggan tidak menggunakan pengalaman subkontrak penuh tetapi ingin mempunyai pandangan kos yang bersatu pada projek dalam Operasi Projek

Jika anda menjejaki proses subkontrak dalam sistem pihak ketiga, anda boleh merekodkan kos daripada sistem pihak ketiga tersebut kepada Operasi Projek dengan mencipta invois vendor yang tidak merujuk subkontrak. Dengan cara ini, pengurus projek anda boleh mempunyai pandangan tunggal dan bersatu mengenai semua kos pada projek tertentu.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Penciptaan invois vendor dalam Operasi Projek

Invois vendor boleh dibuat dalam dua cara:

- Daripada halaman senarai invois vendor atau halaman butiran untuk invois vendor tunggal
- Daripada halaman senarai subkontrak atau halaman butiran untuk subkontrak tunggal

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Penciptaan daripada halaman senarai invois vendor atau halaman butiran

1. Pergi ke **Invois Vendor Pembelian** \> **·**.
2. Pada halaman senarai invois vendor atau halaman butiran untuk invois vendor tunggal, pilih **Baharu** untuk mencipta invois vendor baharu.

Invois vendor yang dicipta dengan cara ini juga boleh merujuk subkontrak.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Penciptaan daripada halaman senarai subkontrak atau halaman butiran

1. Pergi ke **Subkontrak Pembelian** \> **·**.
2. Pilih satu atau lebih subkontrak.
3. Pada halaman senarai subkontrak atau halaman butiran untuk satu subkontrak, pilih **Buat invois** vendor untuk mencipta invois vendor baharu.

Invois vendor baharu dalam **status Draf** dicipta untuk setiap subkontrak yang anda pilih.

Invois vendor yang anda cipta dengan cara ini sentiasa merujuk subkontrak pada pengepala invois vendor. Setiap baris pada subkontrak yang mempunyai kaedah pengebilan Masa dan bahan akan menyebabkan baris dibuat pada invois vendor. Setiap baris pada subkontrak yang mempunyai kaedah pengebilan harga tetap akan menyebabkan baris dicipta pada invois vendor untuk setiap pencapaian subkontrak yang mempunyai status **Sedia untuk invois**.

Medan berikut dan rekod berkaitan akan disalin daripada subkontrak kepada pengepala invois vendor:

- Penjual.
- Senarai harga berkaitan akan disalin ke invois vendor sebagai senarai harga.
- Mata wang.
- Unit kontrak.
- Terma pembayaran.

Untuk garis subkontrak masa dan bahan, medan berikut dan rekod berkaitan akan disalin dari garis subkontrak ke baris invois vendor:

- Rujukan garis subkontrak dan subkontrak
- Kelas transaksi
- Peranan
- Kategori transaksi
- Bidang produk
- Project
- Tugas
- Sumber boleh ditempah

Untuk garis subkontrak harga tetap, medan berikut akan disalin daripada garis subkontrak dan pencapaian garis subkontrak ke baris invois vendor:

- Rujukan baris subkontrak dan subkontrak.
- Kelas transaksi. Secara lalai, nilai akan menjadi **Milestone**.
- Nama dan jumlah pencapaian akan disalin daripada tonggak garis subkontrak yang berkaitan.
- Pengguna akan dapat memilih projek dan tugas pada talian invois vendor.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
