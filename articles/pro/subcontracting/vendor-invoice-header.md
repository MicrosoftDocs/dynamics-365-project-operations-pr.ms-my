---
title: Butiran pengepala untuk invois vendor
description: Artikel ini menerangkan fungsi yang disediakan pada pengepala invois vendor dalam Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 95f84f2d2a357abbd8d507705412a0434b44f658
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929869"
---
# <a name="header-details-for-vendor-invoices"></a>Butiran pengepala untuk invois vendor

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Artikel ini menerangkan fungsi yang disediakan pada pengepala invois vendor dalam Microsoft Dynamics 365 Project Operations.

Apabila pengurus projek merancang dan melaksanakan projek, mereka mungkin menggunakan subkontraktor dan membeli produk dan perkhidmatan daripada vendor. Semasa pelaksanaan projek, kos ditanggung daripada kategori perkhidmatan, bahan, dan perbelanjaan yang diperoleh pada subkontrak dengan vendor. Vendor menginvois kos ini kepada projek dengan membuat invois vendor.

Jadual berikut memberikan maklumat tentang medan pada pengepala invois vendor dalam Operasi Projek.

| Medan | Description | Kesan kefungsian |
| --- | --- | --- |
| Nama | Nama invois vendor. | Dalam semua senarai juntai bawah invois vendor, nama invois vendor disenaraikan dalam lajur pertama untuk membantu anda mengenal pasti invois vendor. Secara lalai, apabila invois vendor dicipta daripada subkontrak, **medan Nama** invois vendor ditetapkan kepada nilai yang terdiri daripada nama subkontrak ditambah tarikh semasa. |
| Description | Penerangan ringkas tentang perkhidmatan dan produk yang diinvois pada invois vendor. | Tiada |
| Vendor | Nama syarikat yang menginvois untuk produk dan perkhidmatan. Syarikat ini harus menjadi rekod akaun yang mempunyai jenis **hubungan Vendor** atau **Pembekal**. | <p>Berdasarkan vendor yang dipilih, nilai lalai dimasukkan secara automatik dalam medan berikut:</p><ul><li>Mata Wang</li><li>Senarai harga</li><li>Terma pembayaran</li><li>Alamat pembayaran</li></ul> |
| Subkontrak | Rujukan kepada subkontrak untuk invois vendor. | <p>Berdasarkan subkontrak yang dipilih, nilai lalai dimasukkan secara automatik dalam medan berikut:</p><ul><li>Mata Wang</li><li>Senarai harga</li><li>Terma pembayaran</li><li>Alamat pembayaran</li></ul><p>Subkontrak yang dipilih pada pengepala invois vendor dimasukkan secara lalai pada baris invois vendor dan tidak boleh diubah di sana.</p> |
| Tarikh invois | Tarikh untuk sebenar kos yang akan dibuat apabila invois vendor disahkan. | Tarikh invois juga digunakan untuk memilih senarai harga pembelian yang betul sama ada daripada senarai harga yang dilampirkan pada vendor berkaitan atau daripada parameter projek. |
| Sebab status | Status invois vendor. | <p>Status menentukan di mana invois vendor berada dalam proses perniagaan dan sama ada ia boleh diedit. Berikut adalah beberapa nilai yang ada:</p><ul><li>**Draf** - Invois vendor boleh diedit.</li><li>**Disahkan** - Invois vendor telah disahkan dan disahkan. Invois vendor dalam status ini tidak boleh diedit atau dipadamkan.</li><li>**Dalam proses** - Invois vendor sedang disemak. Invois vendor dalam status ini boleh diedit, tetapi invois tersebut tidak boleh dipadamkan.</li><li>**Dibatalkan** - Invois vendor dibatalkan. Invois vendor dalam status ini tidak boleh diedit atau dipadamkan.</li></ul> |
| Mata Wang | Mata wang yang digunakan oleh vendor untuk produk dan perkhidmatan pada invois vendor. | Pada invois vendor yang merujuk subkontrak, mata wang subkontrak dimasukkan secara lalai sebagai mata wang invois vendor. Pada invois vendor yang tidak merujuk subkontrak, nilai lalai dimasukkan daripada rekod akaun vendor dan boleh diubah. Selepas invois vendor disimpan, mata wang tidak lagi boleh diedit. |
| Unit pengkontrakan | Bahagian syarikat yang bertanggungjawab untuk menerima perkhidmatan dan / atau produk dari vendor. | Tiada |
| Terma pembayaran | Syarat pembayaran pada invois vendor yang dikeluarkan. Nilai lalai akan dimasukkan secara automatik daripada rekod akaun vendor. | Terma pembayaran daripada subkontrak disalin kepada semua invois vendor yang berkaitan dengan subkontrak. Terma pembayaran boleh dikemas kini jika invois vendor mempunyai status **Draf**. |
| Alamat pembayaran | Alamat vendor untuk penghantaran pembayaran. Nilai lalai akan dimasukkan secara automatik daripada rekod akaun vendor. | Alamat pembayaran dari subkontrak disalin sebagai alamat pembayaran kepada semua invois vendor yang dibuat untuk subkontrak tersebut. Alamat pembayaran boleh dikemas kini jika invois vendor mempunyai status **Draf**. |
| Jumlah kecil | Jika invois vendor tidak mempunyai baris, masukkan subjumlah invois sebelum cukai. Jika invois vendor mempunyai baris, medan ini hanya dibaca. Dalam kes ini, jumlah yang ditunjukkan adalah jumlah subjumlah dari semua baris pada invois vendor. | Tiada |
| Jumlah cukai | Jika invois vendor tidak mempunyai baris, masukkan jumlah cukai pada subkontrak. Jika invois vendor mempunyai baris, medan ini hanya dibaca. Dalam kes ini, jumlah yang ditunjukkan adalah jumlah cukai dari semua baris pada invois vendor. | Tiada |
| Jumlah | Medan yang dikira ini menunjukkan jumlah invois vendor selepas cukai dimasukkan. | Tiada |

> [!NOTE]
> Medan berikut pada invois vendor tidak boleh diubah selepas invois vendor disimpan: **Vendor**, Subkontrak **,** **Mata Wang**, **Unit** Kontrak dan **Terma** Pembayaran. Jika sebarang perubahan diperlukan pada medan ini pada invois vendor, anda mesti memadamkan invois vendor dan mencipta invois vendor baharu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
