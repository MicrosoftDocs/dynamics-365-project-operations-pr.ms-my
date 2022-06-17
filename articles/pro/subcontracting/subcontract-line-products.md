---
title: Baris subkontrak untuk produk
description: Artikel ini menerangkan cara merakam baris subkontrak untuk produk dan menggunakan pelbagai bidang untuk merakam pembelian produk dari vendor.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ff9636f86102fa671a443d7646614070b3e2ee79
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934377"
---
# <a name="subcontract-lines-for-products"></a>Baris subkontrak untuk produk

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Subkontrak dalam Dynamics 365 Project Operations boleh mempunyai baris subkontrak untuk produk. Baris ini membenarkan Pengurus Projek untuk membeli produk daripada vendor yang kemudian boleh digunakan oleh mereka pada tugas projek.

Lengkapkan langkah berikut untuk mencipta baris subkontrak untuk produk dalam Project Operations.

1. Pada halaman navigasi, pilih **Subkontrak** dan kemudian buka subkontrak yang ingin anda usahakan. 
2. Pada tab **Baris Subkontrak**, pilih **+ Baharu** untuk mencipta baris subkontrak baharu.
3. Pada halaman **Cipta Pantas**, dalam medan **Kelas Transaksi**, pilih **Bahan** dan masukkan atau pilih maklumat medan yang diperlukan. 
4. Pilih **Simpan**.

Jadual berikut memberikan maklumat tentang medan pada halaman **Butiran baris subkontrak** dan halaman **Cipta pantas** kerana halaman berkaitan dengan pembelian produk.

| Medan | Penerangan | Kesan kefungsian|
| ----- | ----------- | ----------- |
| Nama | Nama baris subkontrak untuk membantu pengenalpastian. |Ini akan ditunjukkan sebagai lajur pertama dalam semua carian berdasarkan pada baris subkontrak.
| Penerangan | Penerangan ringkas tentang produk yang dipesan pada baris subkontrak. | Tiada |
| Jenis Baris | Nilai medan ini mempunyai nilai lalai daripada **Berasaskan kuantiti**. |Tiada |
| Kaedah Pengebilan | Ini adalah set pilihan yang mewakili dua model kontrak utama disokong oleh Project Operations: **Harga Tetap** dan **Masa dan Bahan**. | Berdasarkan pada kaedah pengebilan yang dipilih, jadual invois berasaskan pencapaian tersedia untuk baris subkontrak dengan kaedah pengebilan Harga Tetap. |
| Kelas Transaksi |Medan ini mempunyai nilai lalai bagi **Masa**. Untuk mencipta baris subkontrak bagi pembelian produk, tetapkan medan  **Kelas Transaksi** ke **Bahan**.  | Ini menunjukkan bahawa baris subkontrak sedang digunakan untuk merekodkan pembelian produk yang akan digunakan pada projek. |
| Pilih Produk | Pilih sama ada produk yang dibeli disimpan dalam katalog produk atau merupakan produk masukan manual. |Tiada |
| Produk | Pilih produk yang aktif daripada katalog. Medan ini hanya tersedia apabila **Pilih Produk** ditetapkan kepada **Sedia ada**. |Gabungan **Produk** dan **Unit** akan digunakan sebagai lalai atau dikira untuk harga unit bagi baris subkontrak.
| Produk Masukan Manual | Masukkan nama produk masukan manual. Medan ini hanya tersedia apabila **Pilih Produk** ditetapkan kepada **Masukan Manual**.  |Harga belian tidak akan diisi secara automatik untuk produk masukan manual.|
| Tarikh Penyampaian Diminta | Masukkan tarikh penghantaran yang diperlukan untuk produk.| Tarikh ini juga digunakan untuk memilih senarai harga projek daripada senarai harga projek yang dilampirkan kepada subkontrak. Kos produk pada baris subkontrak kemudian terlalai daripada senarai harga tersebut. |
| Tarikh penghantaran mengikut kontrak | Masukkan tarikh produk yang digunakan oleh Syarikat bersetuju untuk dihantar.  |Tiada|
| Kuantiti Dipesan | Masukkan kuantiti produk yang dibeli daripada vendor.| Ini akan digunakan untuk menunjukkan amaran apabila pengurus projek lebih daripada kuantiti ini.|
| Kumpulan Unit | Nilai ini terlalai untuk produk katalog sahaja. |Apabila **Produk** dan **Tarikh penghantaran yang diminta** dipilih, sistem akan memilih senarai harga yang terpakai berdasarkan tarikh penghantaran. Item senarai harga yang berkaitan ditanya untuk produk yang sepadan. Nilai unit dan kumpulan unit terlalai daripada persediaan pada rekod item senarai harga. |
| Unit | Nilai ini lalai untuk unit yang disediakan pada rekod item senarai harga. Anda boleh mengubah ini kepada unit lain jika perlu.| Gabungan produk dan unit digunakan untuk melalaikan harga unit pada baris subkontrak untuk produk katalog yang sedia ada. |
| Harga Unit | Harga unit terlalai menggunakan gabungan produk dan unit daripada item senarai harga yang berkaitan dengan senarai harga projek yang terpakai untuk tarikh penghantaran yang diminta pada baris subkontrak.  |Tiada |
| Jumlah kecil | Medan baca sahaja dikira sebagai Kuantiti x Harga unit jika kedua-dua medan mempunyai nilai yang dimasukkan. Jika sama ada medan **Kuantiti**, **Harga unit** atau kedua-duanya kosong, anda boleh memasukkan nilai secara manual.  |Tiada |
| Cukai Jualan | Masukkan nilai cukai jualan. |Tiada |
| Jumlah Amaun | Medan dikira ini menunjukkan jumlah amaun baris subkontrak selepas termasuk cukai. Nilai dalam medan ini dikira sebagai Subjumlah + Cukai. |Tiada |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
