---
title: Baris subkontrak untuk masa
description: Topik ini menerangkan cara merekodkan baris subkontrak untuk masa dan merekodkan pembelian masa daripada vendor.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323877"
---
# <a name="subcontract-lines-for-time"></a>Baris subkontrak untuk masa

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Subkontrak dalam Dynamics 365 Project Operations boleh mempunyai baris subkontrak untuk masa. Baris subkontrak untuk masa membolehkan Pengurus Projek untuk membeli masa vendor untuk menugaskan tugas projek dan keperluan sumber.

Untuk mencipta baris subkontrak untuk masa dalam Project Operations, lengkapkan langkah berikut.

1. Dalam anak tetingkap navigasi, pilih **Subkontrak** dan buka subkontrak.
2. Pada tab **Baris Subkontrak**, pilih **Baharu** untuk mencipta baris subkontrak baharu.
3. Pada halaman **Cipta Pantas**, dalam medan **Kelas Transaksi**, pilih **Masa**.
4. Masukkan maklumat medan yang selebihnya dan kemudian pilih **Simpan**.

  Jadual berikut memberikan maklumat tentang medan pada halaman **Baris subkontrak** dan halaman **Cipta Pantas**.

| **Medan** | **Perihalan** |
| --- | --- |
| Nama | Nama baris subkontrak. |
| Penerangan | Penerangan ringkas tentang perkhidmatan yang dibeli pada baris subkontrak. | 
| Jenis Baris | Medan ini ialah nilai lalai.  |
| Kaedah Pengebilan | Pilih kaedah pengebilan. Berdasarkan kaedah pengebilan baris subkontrak yang dirujuk, jadual invois berasaskan pencapaian disediakan untuk kaedah pengebilan Harga Tetap. |
| Kelas Transaksi | Medan ini ialah nilai lalai yang menunjukkan sama ada baris subkontrak digunakan untuk merekodkan pembelian masa subkontraktor. |
| Peranan | Peranan sumber subkontrak yang masanya dibeli. Peranan ditugaskan kepada sumber subkontrak menentukan kos pembelian. |
| Permulaan Diminta | Tarikh apabila sumber subkontraktor perlu mula bekerja. Permulaan diminta juga digunakan untuk memilih senarai harga projek daripada senarai harga projek yang dilampirkan kepada subkontrak. Kos peranan pada baris subkontrak kemudian terlalai daripada senarai harga tersebut. |
| Penamatan diminta | Tarikh apabila tugasan sumber subkontraktor tamat. Tarikh ini digunakan untuk menunjukkan amaran apabila Pengurus Projek menarik daripada keupayaan ini untuk keperluan sumber yang berlaku selepas tarikh ini. |
| Kuantiti Dipesan | Bilangan jam Peranan yang dibeli daripada vendor. Nilai ini digunakan untuk menunjukkan amaran apabila Pengurus Projek menarik lebih daripada keupayaan ini untuk keperluan sumber. |
| Kumpulan Unit | Nilai medan ini terlalai kepada kumpulan unit Masa dan tidak boleh diubah.  |
| Unit | Medan ini terlalai kepada unit asas jam daripada kumpulan unit Masa. Anda boleh mengubah nilai ini untuk membeli apa-apa unit daripada kumpulan unit Masa, seperti hari atau minggu. Gabungan Peranan dan Unit digunakan untuk mengira harga unit untuk baris subkontrak. |
| Harga Unit | Harga unit terlalai daripada gabungan Peranan dan Unit daripada senarai harga projek yang terpakai untuk tarikh mula yang diminta pada baris subkontrak. Apabila senarai harga projek terpakai mempunyai harga yang ditetapkan dalam unit yang berbeza daripada unit pada baris subkontrak, sistem menggunakan penukaran unit untuk mengira harga seunit. |
| Jumlah kecil | Ini merupakan medan baca sahaja yang dikira secara automatik sebagai **Kuantiti x Harga unit** jika kuantiti dan nilai harga unit dimasukkan. Jika sama ada kuantiti, harga unit atau kedua-duanya kosong, anda boleh memasukkan nilai dalam medan. |
| Cukai Jualan |  Masukkan amaun cukai jualan. |
| Jumlah Amaun | Jumlah amaun baris subkontrak selepas cukai dimasukkan. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
