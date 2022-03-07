---
title: Baris subkontrak untuk produk
description: Topik ini menerangkan cara merekodkan baris subkontrak untuk produk dan menggunakan pelbagai medan untuk merekodkan pembelian produk daripada vendor.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323697"
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

| Medan | Penerangan |
| ----- | ----------- |
| Nama | Nama baris subkontrak. |
| Penerangan | Penerangan ringkas tentang produk yang dipesan pada baris subkontrak. |
| Jenis Baris | Nilai medan ini terlalai kepada **Berasaskan kuantiti**. |
| Kaedah Pengebilan |  Kaedah pengebilan baris subkontrak. Jadual invois berasaskan pencapaian tersedia untuk kaedah pengebilan harga tetap. |
| Kelas Transaksi | Nilai medan ini terlalai kepada **Masa**. Untuk mencipta baris subkontrak untuk pembelian produk, dalam medan **Kelas Transaksi**, pilih **Bahan**. Pemilihan ini menunjukkan bahawa baris subkontrak digunakan untuk merekodkan pembelian produk yang akan digunakan pada projek. |
| Pilih Produk | Pilih sama ada produk yang dibeli disimpan dalam katalog produk atau merupakan produk masukan manual. |
| Produk | Pilih produk yang aktif daripada katalog. Medan ini hanya tersedia apabila **Pilih Produk** ditetapkan kepada **Sedia ada**. |
| Produk Masukan Manual | Masukkan nama produk masukan manual. Medan ini hanya tersedia apabila **Pilih Produk** ditetapkan kepada **Masukan Manual**.  |
| Tarikh Penyampaian Diminta | Pilih tarikh penghantaran yang diperlukan untuk produk tersebut. Tarikh ini juga digunakan untuk memilih senarai harga projek daripada senarai harga projek yang dilampirkan kepada subkontrak. Kos produk pada baris subkontrak kemudian terlalai daripada senarai harga tersebut. |
| Tarikh penghantaran mengikut kontrak | Pilih tarikh apabila produk akan dihantar mengikut persetujuan pada kontrak.  |
| Kuantiti Dipesan | Masukkan kuantiti produk yang dibeli daripada vendor. Jika Pengurus Projek menarik lebih daripada kuantiti ini, amaran akan berlaku. |
| Kumpulan Unit | Nilai ini terlalai untuk produk katalog sahaja. Apabila **Produk** dan **Tarikh penghantaran yang diminta** dipilih, sistem akan memilih senarai harga yang terpakai berdasarkan tarikh penghantaran. Item senarai harga yang berkaitan ditanya untuk produk yang sepadan. Nilai unit dan kumpulan unit terlalai daripada persediaan pada rekod item senarai harga. |
| Unit | Nilai ini terlalai kepada persediaan unit pada rekod item senarai harga. Anda boleh mengubah ini kepada unit lain jika perlu. Gabungan produk dan unit digunakan untuk melalaikan harga unit pada baris subkontrak untuk produk katalog yang sedia ada. |
| Harga Unit | Harga unit terlalai menggunakan gabungan produk dan unit daripada item senarai harga yang berkaitan dengan senarai harga projek yang terpakai untuk tarikh penghantaran yang diminta pada baris subkontrak.  |
| Jumlah kecil | Medan baca sahaja dikira sebagai Kuantiti x Harga unit jika kedua-dua medan mempunyai nilai yang dimasukkan. Jika sama ada medan **Kuantiti**, **Harga unit** atau kedua-duanya kosong, anda boleh memasukkan nilai secara manual.  |
| Cukai Jualan | Masukkan nilai cukai jualan. |
| Jumlah Amaun | Medan dikira ini menunjukkan jumlah amaun baris subkontrak selepas termasuk cukai. Nilai dalam medan ini dikira sebagai jumlah kecil + cukai. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
