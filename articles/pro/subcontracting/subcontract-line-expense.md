---
title: Baris subkontrak untuk kategori perbelanjaan
description: Topik ini menerangkan cara merekodkan baris subkontrak untuk perbelanjaan dan menggunakan medan untuk merekodkan pembelian masa daripada vendor.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0c32bf2ac54de98a921d338e436ecd089e68a759
ms.sourcegitcommit: cd4e81f129681a12f2efe63ec2bb14e611cf88ba
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/20/2021
ms.locfileid: "7506110"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Baris subkontrak untuk kategori perbelanjaan

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Subkontrak dalam Dynamics 365 Project Operations boleh mempunyai baris untuk kategori perbelanjaan. Baris subkontrak untuk kategori perbelanjaan membolehkan Pengurus Projek membeli kategori perkhidmatan atau produk daripada vendor yang boleh dikenakan bayaran pada projek.

Untuk mencipta baris subkontrak untuk kategori perbelanjaan dalam Project Operations, lengkapkan langkah berikut.

1. Dalam anak tetingkap navigasi, pilih **Subkontrak** dan buka subkontrak yang ingin anda usahakan.
2. Pada tab **Baris Subkontrak**, pilih **Baharu** untuk mencipta baris baharu.
3. Pada halaman **Cipta Pantas**, dalam medan **Kelas Transaksi**, pilih **Perbelanjaan** dan masukkan atau pilih apa-apa maklumat medan lain yang diperlukan.

Jadual berikut memberikan maklumat tentang medan pada halaman butiran **Baris subkontrak** dan halaman **Cipta Pantas**.

| **Medan** | **Perihalan** | **Kesan kefungsian** |
| --- | --- | --- |
| Nama | Nama baris subkontrak untuk membantu pengenalpastian. | Ini akan ditunjukkan sebagai lajur pertama dalam semua carian berdasarkan pada baris subkontrak. |
| Penerangan | Perihalan ringkas tentang kategori perbelanjaan yang sedang dibeli pada baris subkontrak. | Tiada |
|Jenis Baris | Medan ini mempunyai nilai lalai bagi **Berasaskan kuantiti**. |Tiada |
| Kaedah Pengebilan | Ini adalah set pilihan yang mewakili dua model kontrak utama disokong oleh Project Operations: **Harga Tetap** dan **Masa dan Bahan**. | Jadual invois berasaskan pencapaian tersedia untuk baris subkontrak jika kaedah pengebilan Harga Tetap dipilih. |
| Kelas Transaksi | Medan ini mempunyai nilai lalai bagi **Masa**. Untuk mencipta baris subkontrak bagi pembelian produk, tetapkan medan **Kelas Transaksi** ke **Perbelanjaan**.  | Ini menunjukkan bahawa baris subkontrak sedang digunakan untuk merekodkan pembelian kategori perbelanjaan yang akan digunakan pada projek. |
| Kategori Transaksi | Menunjukkan senarai kategori transaksi yang aktif dalam sistem. |Tiada |
| Permulaan Diminta | Masukkan tarikh apabila kategori pembelian mesti tersedia daripada vendor. | Permulaan yang diminta digunakan untuk memilih senarai harga projek daripada senarai harga projek yang dilampirkan ke subkontrak. Kos kategori pada baris subkontrak datang daripada senarai harga. |
| Penamatan Diminta | Masukkan tarikh apabila kategori pembelian tidak lagi diperlukan. | Ini akan digunakan untuk menunjukkan amaran apabila pengurus projek mengaitkan subkontrak ini untuk anggaran perbelanjaan tertentu pada projek yang diperlukan selepas tarikh ini. |
| Kuantiti Dipesan | Kuantiti kategori sedang dibeli daripada vendor. | Ini akan digunakan untuk menunjukkan amaran apabila pengurus projek lebih daripada kuantiti ini.|
| Kumpulan Unit | Nilai lalai adalah berdasarkan pada kumpulan unit lalai yang disediakan untuk kategori yang dipilih. |Tiada |
| Unit | Nilai lalai adalah berdasarkan pada unit lalai yang disediakan untuk kategori yang dipilih.  | Gabungan **Kategori** dan **Unit** akan digunakan sebagai lalai atau dikira untuk harga unit bagi baris subkontrak.  |
| Harga Unit | Nilai lalai menggunakan gabungan **Kategori** dan **Unit** daripada kategori harga yang berkaitan dengan senarai harga projek yang tidak berkenaan untuk permulaan baris subkontrak yang diminta. |Tiada |
| Jumlah kecil | Ini ialah medan baca sahaja yang dikira sebagai Kuantiti X harga Unit, jika kedua-dua kuantiti dan nilai harga unit dimasukkan. Jika salah satu atau kedua-dua medan adalah kosong, anda boleh memasukkan nilai dalam medan ini. |Tiada |
| Cukai Jualan | Masukkan amaun cukai jualan. |Tiada |
| Jumlah Amaun | Jumlah amaun baris subkontrak termasuk cukai. Medan ini dikira sebagai Subjumlah + cukai Jualan. |Tiada |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
