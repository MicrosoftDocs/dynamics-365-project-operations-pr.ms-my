---
title: Penginvoisan vendor - Konsep dan penciptaan
description: Topik ini menerangkan konsep invois vendor, senario untuk digunakan dan cara membuat invois vendor dalam Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: dc9b3954b237294f52aa0bb74f8008a5dfdf78fd
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580559"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Penginvoisan vendor - Konsep dan penciptaan

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Penginvoisan vendor dalam Microsoft Dynamics 365 Project Operations boleh digunakan untuk merekodkan kos daripada penghantaran perkhidmatan dan/atau bahan pada projek oleh vendor.

Apabila perkhidmatan dan/atau bahan disubkontrakkan kepada vendor, subkontrak mewakili perjanjian kontrak dengan vendor tersebut. Oleh kerana vendor menyampaikan perkhidmatan, atau bahan diterima dan digunakan pada tugas projek, kos direkodkan pada projek. Secara berkala, vendor menghantar invois yang disahkan dan dipadankan dengan kos yang direkodkan pada projek. Selepas proses pengesahan selesai, invois vendor disahkan dan dikeluarkan untuk pembayaran.

## <a name="scenarios-for-use"></a>Senario untuk digunakan

Invois vendor dalam Operasi Projek boleh digunakan untuk menyokong dua senario yang berbeza.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Pelanggan menggunakan pengalaman subkontrak penuh

Pengalaman invois vendor menyediakan cara untuk mengesahkan dan memadankan entri masa, penggunaan bahan dan entri perbelanjaan yang merujuk komponen subkontrak dengan baris invois vendor. Proses ini boleh digunakan untuk mengesahkan ketepatan baris invois vendor. Selepas proses pengesahan selesai dan invois vendor disahkan, aplikasi akan membalikkan sebenar yang direkodkan oleh masa yang diluluskan, perbelanjaan dan log penggunaan bahan, dan mencipta sebenar kos baharu dengan menggunakan baris invois vendor.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Pelanggan tidak menggunakan pengalaman subkontrak penuh tetapi ingin mempunyai pandangan yang bersatu mengenai kos projek dalam Operasi Projek

Jika anda menjejaki proses subkontrak dalam sistem pihak ketiga, anda boleh merekodkan kos daripada sistem pihak ketiga tersebut kepada Project Operations dengan mencipta invois vendor yang tidak merujuk subkontrak. Dengan cara ini, pengurus projek anda boleh mempunyai pandangan tunggal dan bersatu mengenai semua kos pada projek tertentu.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Penciptaan invois vendor dalam Operasi Projek

Invois vendor boleh dibuat dalam dua cara:

- Daripada halaman senarai invois vendor atau halaman butiran untuk satu invois vendor
- Dari halaman senarai subkontrak atau halaman butiran untuk satu subkontrak

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Penciptaan daripada halaman senarai invois vendor atau halaman butiran

1. Pergi ke **Invois Vendor Pembelian** \> **·**.
2. Pada halaman senarai invois vendor atau halaman butiran untuk satu invois vendor, pilih **Baru** untuk mencipta invois vendor baharu.

Invois vendor yang dibuat dengan cara ini juga boleh merujuk subkontrak.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Penciptaan daripada halaman senarai subkontrak atau halaman butiran

1. Pergi ke **Subkontrak** Pembelian \>**·**.
2. Pilih satu atau lebih subkontrak.
3. Pada halaman senarai subkontrak atau halaman butiran untuk satu subkontrak, pilih **Cipta invois** vendor untuk mencipta invois vendor baharu.

Invois vendor baharu dalam **status Draf** dicipta untuk setiap subkontrak yang anda pilih.

Invois vendor yang anda buat dengan cara ini sentiasa merujuk subkontrak pada pengepala invois vendor. Setiap baris pada subkontrak yang mempunyai kaedah pengebilan Masa dan bahan akan menyebabkan talian dibuat pada invois vendor. Setiap baris pada subkontrak yang mempunyai kaedah pengebilan harga tetap akan menyebabkan talian dibuat pada invois vendor untuk setiap tonggak baris subkontrak yang mempunyai status **Sedia untuk invois**.

Medan berikut dan rekod yang berkaitan akan disalin daripada subkontrak kepada pengepala invois vendor:

- Penjual.
- Senarai harga yang berkaitan akan disalin ke invois vendor sebagai senarai harga.
- Mata wang.
- Unit kontrak.
- Terma pembayaran.

Untuk baris subkontrak Masa dan bahan, medan berikut dan rekod yang berkaitan akan disalin dari baris subkontrak ke baris invois vendor:

- Rujukan baris subkontrak dan subkontrak
- Kelas transaksi
- Peranan
- Kategori transaksi
- Medan produk
- Project
- Tugas
- Sumber boleh ditempah

Untuk baris subkontrak harga tetap, medan berikut akan disalin dari baris subkontrak dan tonggak baris subkontrak ke baris invois vendor:

- Rujukan subkontrak dan subkontrak.
- Kelas transaksi. Secara lalai, nilai akan menjadi **Milestone**.
- Nama dan amaun milestone akan disalin daripada peristiwa penting baris subkontrak yang berkaitan.
- Pengguna akan dapat memilih projek dan tugas pada baris invois vendor.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
