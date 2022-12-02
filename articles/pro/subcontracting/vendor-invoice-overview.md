---
title: Penginvoisan vendor - Konsep dan penciptaan
description: Artikel ini menghuraikan konsep invois vendor, senario penggunaan dan cara untuk mencipta invois vendor dalam Microsoft Dynamics 365 Project Operations.
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

Penginvoisan vendor dalam Microsoft Dynamics 365 Project Operations boleh digunakan untuk merekodkan kos daripada penghantaran perkhidmatan dan/atau bahan pada projek oleh vendor.

Apabila perkhidmatan dan/atau bahan merupakan subkontrak kepada vendor, subkontrak mewakili perjanjian kontrak dengan vendor tersebut. Apabila vendor menyampaikan perkhidmatan, atau bahan yang diterima dan digunakan pada tugas projek, kos direkodkan pada projek. Secara berkala, vendor menghantar invois yang disahkan dan dipadankan dengan kos yang direkodkan pada projek. Selepas proses pengesahan selesai, invois vendor disahkan dan dikeluarkan untuk pembayaran.

## <a name="scenarios-for-use"></a>Senario penggunaan

Invois vendor dalam Project Operations boleh digunakan untuk menyokong dua senario yang berbeza.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Pelanggan menggunakan pengalaman subkontrak penuh

Pengalaman invois vendor menyediakan cara untuk mengesahkan dan memadankan entri masa, penggunaan bahan dan entri perbelanjaan yang merujuk komponen subkontrak, dan dipadankan dengan baris invois vendor. Proses ini boleh digunakan untuk mengesahkan ketepatan baris invois vendor. Selepas proses pengesahan dilengkapkan dan invois vendor disahkan, aplikasi akan membalikkan aktual yang dirakam dengan masa yang diluluskan, perbelanjaan dan log penggunaan bahan, dan mencipta aktual kos baharu menggunakan baris invois vendor.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Pelanggan tidak menggunakan pengalaman subkontrak penuh tetapi mahu mempunyai pandangan disatukan kos pada projek dalam Project Operations

Jika anda menjejaki proses subkontrak dalam sistem pihak ketiga, anda boleh merekodkan kos daripada sistem pihak ketiga tersebut kepada Project Operations dengan mencipta invois vendor yang tidak merujuk subkontrak. Dengan cara ini, pengurus projek anda boleh mempunyai pandangan tunggal yang disatukan bagi semua kos projek yang diberikan.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Penciptaan invois vendor dalam Project Operations

Invois vendor boleh dicipta dalam dua cara:

- Daripada halaman senarai invois vendor atau halaman butiran untuk invois vendor tunggal
- Daripada halaman senarai subkontrak atau halaman butiran untuk subkontrak tunggal

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Penciptaan daripada halaman senarai invois vendor atau halaman butiran

1. Pergi ke **Pembelian** \> **Invois vendor**.
2. Pada halaman senarai invois vendor atau halaman butiran untuk invois vendor tunggal, pilih **Baharu** untuk mencipta invois vendor baharu.

Invois vendor yang dicipta dengan cara ini juga boleh merujuk subkontrak.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Penciptaan daripada halaman senarai subkontrak atau halaman butiran

1. Pergi ke **Pembelian** \> **Subkontrak**.
2. Pilih satu atau lebih subkontrak.
3. Pada halaman senarai subkontrak atau halaman butiran untuk subkontrak tunggal, pilih **Cipta invois vendor** untuk mencipta invois vendor baharu.

Invois vendor baharu dalam status **Draf** dicipta untuk setiap subkontrak yang anda pilih.

Invois vendor yang anda cipta dengan cara ini sentiasa merujuk subkontrak pada pengepala invois vendor. Setiap baris pada subkontrak yang mempunyai Masa dan kaedah pengebilan bahan yang akan menyebabkan baris tercipta pada invois vendor. Setiap baris pada subkontrak yang mempunyai kaedah pengebilan harga Tetap yang akan menyebabkan baris tercipta pada invois vendor untuk setiap pencapaian baris subkontrak yang mempunyai status **Tersedia untuk diinvois**.

Medan berikut dan rekod yang berkaitan akan disalin daripada subkontrak kepada pengepala invois vendor:

- Vendor.
- Senarai harga berkaitan akan disalin ke invois vendor sebagai senarai harga.
- Mata wang.
- Unit kontrak.
- Terma pembayaran

Untuk baris subkontrak Masa dan bahan, medan berikut dan rekod yang berkaitan akan disalin daripada baris subkontrak kepada baris invois vendor:

- Rujukan subkontrak dan baris subkontrak
- Kelas transaksi
- Peranan
- Kategori transaksi
- Medan produk
- Project
- Tugas
- Sumber boleh ditempah

Untuk baris subkontrak harga Tetap, medan berikut akan disalin daripada baris subkontrak dan pencapaian baris subkontrak kepada baris invois vendor:

- Rujukan subkontrak dan baris subkontrak.
- Kelas urus niaga. Secara lalai, nilai akan menjadi **Pencapaian**.
- Nama pencapaian dan jumlah akan disalin daripada pencapaian baris subkontrak yang berkaitan.
- Pengguna akan dapat memilih projek dan tugas pada baris invois vendor.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
