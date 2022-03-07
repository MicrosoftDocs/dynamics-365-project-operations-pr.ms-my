---
title: Baris subkontrak untuk kategori perbelanjaan
description: Topik ini menerangkan cara merekodkan baris subkontrak untuk perbelanjaan dan menggunakan medan untuk merekodkan pembelian masa daripada vendor.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323832"
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

| **Medan** |  **Perihalan** |
| ----------| ---------------- |
| Nama | Nama baris subkontrak. |
| Penerangan | Perihalan ringkas tentang perkhidmatan dan kategori produk yang dibeli pada baris subkontrak. |
| Jenis Baris | Nilai medan ini mempunyai nilai lalai daripada **Berasaskan kuantiti**.  |
| Kaedah Pengebilan | Kaedah pengebilan baris subkontrak. Berdasarkan kaedah pengebilan baris, jadual invois berasaskan pencapaian disediakan untuk kaedah pengebilan harga tetap.  |
| Kelas Transaksi | Nilai medan ini mempunyai nilai lalai daripada **Masa**. Untuk mencipta baris subkontrak untuk pembelian produk, tetapkan medan **Kelas Transaksi** kepada **Perbelanjaan**. Nilai medan ini menunjukkan bahawa baris subkontrak sedang digunakan untuk merekodkan pembelian kategori produk atau perkhidmatan untuk digunakan pada projek. |
| Kategori Transaksi | Pilih kategori transaksi. |
| Permulaan Diminta | Tarikh apabila kategori pembelian mesti tersedia daripada penjual. Permulaan diminta juga digunakan untuk memilih senarai harga projek daripada senarai harga projek yang dilampirkan kepada subkontrak. Kos kategori pada baris subkontrak yang terlalai daripada senarai harga tersebut. |
| Penamatan diminta | Tarikh apabila kategori pembelian tidak lagi diperlukan. Tarikh ini memanggil amaran apabila pengurus projek mengaitkan baris subkontrak ini dengan anggaran perbelanjaan tertentu pada projek yang bertarikh selepas tarikh ini. |
| Kuantiti Dipesan | Kuantiti kategori yang dibeli daripada vendor. Jika pengurus projek menarik lebih daripada kuantiti dibeli, amaran akan berlaku.  |
| Kumpulan Unit | Nilai medan ini terlalai berdasarkan kumpulan unit lalai yang disediakan untuk kategori yang dipilih. |
| Unit | Nilai medan ini terlalai berdasarkan unit lalai yang disediakan untuk kategori yang dipilih. Gabungan kategori dan unit digunakan untuk melalaikan harga unit pada baris subkontrak. |
| Harga Unit | Nilai medan harga unit terlalai daripada gabungan kategori dan unit daripada harga kategori yang berkaitan dengan senarai harga projek yang terpakai untuk permulaan diminta pada baris subkontrak.  |
| Jumlah kecil | Ini merupakan medan baca sahaja yang dikira secara automatik sebagai harga unit kuantiti jika kuantiti dan nilai harga unit dimasukkan. Jika satu atau kedua-dua medan adalah kosong, anda boleh memasukkan nilai secara manual dalam medan ini.  |
| Cukai Jualan | Masukkan amaun cukai jualan.  |
| Jumlah Amaun | Jumlah amaun baris subkontrak termasuk cukai. Medan ini dikira sebagai jumlah kecil + cukai jualan.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
