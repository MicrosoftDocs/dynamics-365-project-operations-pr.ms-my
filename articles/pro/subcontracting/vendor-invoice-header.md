---
title: Butiran pengepala untuk invois vendor
description: Artikel ini menerangkan fungsi yang disediakan pada pengepala invois vendor dalam Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d575ebe44e45411e1009c64e9b575777b741322f
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261674"
---
# <a name="header-details-for-vendor-invoices"></a>Butiran pengepala untuk invois vendor

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Artikel ini menerangkan fungsi yang disediakan pada pengepala invois vendor dalam Microsoft Dynamics 365 Project Operations.

Apabila pengurus projek merancang dan melaksanakan projek, mereka boleh menggunakan subkontraktor dan membeli produk dan perkhidmatan daripada vendor. Semasa pelaksanaan projek, kos ditanggung daripada perkhidmatan, bahan dan kategori perbelanjaan yang diperoleh melalui subkontrak dengan vendor. Vendor menginvois kos ini kepada projek dengan mencipta invois vendor.

Jadual berikut menyediakan maklumat mengenai medan pada pengepala invois vendor dalam Project Operations.

| Medan | Description | Kesan kefungsian |
| --- | --- | --- |
| Nama | Nama invois vendor. | Dalam semua senarai juntai bawah invois vendor, nama invois vendor disenaraikan dalam lajur pertama untuk membantu anda mengenal pasti invois vendor. Secara lalai, apabila invois vendor dicipta daripada subkontrak, medan **Nama** invois vendor ditetapkan kepada nilai yang terdiri daripada nama subkontrak ditambah dengan tarikh semasa. |
| Description | Penerangan ringkas tentang perkhidmatan dan produk yang sedang diinvois pada invois vendor. | Tiada |
| Vendor | Nama syarikat yang menginvois untuk produk dan perkhidmatan. Syarikat ini hendaklah menjadi rekod akaun yang mempunyai jenis perhubungan **Vendor** atau **Pembekal**. | <p>Berdasarkan pada vendor yang dipilih, nilai lalai akan dimasukkan secara automatik dalam medan berikut:</p><ul><li>Mata Wang</li><li>Senarai harga</li><li>Terma pembayaran</li><li>Alamat pembayaran</li></ul> |
| Subkontrak | Rujukan kepada subkontrak untuk invois vendor. | <p>Berdasarkan subkontrak yang dipilih, nilai lalai akan dimasukkan secara automatik dalam medan berikut:</p><ul><li>Mata Wang</li><li>Senarai harga</li><li>Terma pembayaran</li><li>Alamat pembayaran</li></ul><p>Subkontrak yang dipilih pada pengepala invois vendor dimasukkan secara lalai pada baris invois vendor dan tidak boleh ditukar di sana.</p> |
| Tarikh invois | Tarikh untuk aktual kos yang akan dicipta apabila invois vendor disahkan. | Tarikh invois juga digunakan untuk memilih senarai harga pembelian yang betul sama ada daripada senarai harga yang dilampirkan ke vendor berkaitan atau daripada parameter projek. |
| Sebab status | Status invois vendor. | <p>Status menentukan tempat invois vendor dalam proses perniagaan dan sama ada invois vendor boleh diedit. Berikut merupakan beberapa nilai yang tersedia:</p><ul><li>**Draf** – Invois vendor boleh diedit.</li><li>**Disahkan** – Invois vendor telah ditentusahkan dan disahkan. Invois vendor dalam status ini tidak boleh diedit atau dipadamkan.</li><li>**Dalam proses** – Invois vendor sedang disemak. Invois vendor dalam status ini boleh diedit, tetapi tidak boleh dipadamkan.</li><li>**Dibatalkan** – Invois vendor telah dibatalkan. Invois vendor dalam status ini tidak boleh diedit atau dipadamkan.</li></ul> |
| Mata Wang | Mata wang yang diinvois oleh vendor untuk produk dan perkhidmatan pada invois vendor. | Pada invois vendor yang merujuk subkontrak, mata wang subkontrak dimasukkan secara lalai sebagai mata wang invois vendor. Pada invois vendor yang tidak merujuk subkontrak, nilai lalai yang dimasukkan daripada rekod akaun vendor dan boleh ditukar. Selepas invois vendor disimpan, mata wang tidak boleh diedit lagi. |
| Unit pengkontrakan | Bahagian syarikat yang bertanggungjawab untuk menerima perkhidmatan dan/atau produk daripada vendor. | Tiada |
| Terma pembayaran | Terma pembayaran invois vendor yang dikeluarkan. Nilai lalai akan dimasukkan secara automatik daripada rekod akaun vendor. | Terma pembayaran daripada subkontrak akan disalin ke semua invois vendor yang berkaitan dengan subkontrak. Terma pembayaran boleh dikemas kini jika invois vendor mempunyai status **Draf**. |
| Alamat pembayaran | Alamat vendor untuk penghantaran pembayaran. Nilai lalai akan dimasukkan secara automatik daripada rekod akaun vendor. | Alamat pembayaran daripada subkontrak disalin sebagai alamat pembayaran ke semua invois vendor yang dicipta untuk subkontrak tersebut. Alamat pembayaran boleh dikemas kini jika invois vendor mempunyai status **Draf**. |
| Jumlah kecil | Jika invois vendor tidak mempunyai baris, masukkan subjumlah invois sebelum cukai. Jika invois vendor mempunyai baris, medan ini merupakan baca sahaja. Dalam kes ini, jumlah yang ditunjukkan ialah amaun subjumlah daripada semua baris pada invois vendor. | Tiada |
| Jumlah cukai | Jika invois vendor tidak mempunyai baris, masukkan cukai pada subkontrak. Jika invois vendor mempunyai baris, medan ini merupakan baca sahaja. Dalam kes ini, jumlah yang ditunjukkan ialah jumlah amaun cukai daripada semua baris pada invois vendor. | Tiada |
| Jumlah amaun | Medan dikira ini menunjukkan jumlah amaun invois vendor selepas cukai dimasukkan. | Tiada |

> [!NOTE]
> Medan pada invois vendor tidak boleh ditukar selepas invois vendor disimpan: **Vendor**, **Subkontrak**, **Mata wang**, **Unit kontrak**, dan **Terma pembayaran**. Jika sebarang perubahan diperlukan untuk medan ini pada invois vendor, anda mesti memadamkan invois vendor dan mencipta invois vendor baharu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
