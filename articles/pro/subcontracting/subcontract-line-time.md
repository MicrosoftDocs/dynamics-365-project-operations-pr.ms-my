---
title: Baris subkontrak untuk masa
description: Topik ini menerangkan cara merekodkan baris subkontrak untuk masa dan merekodkan pembelian masa daripada vendor.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c1adc1e88369e9f60548ed69b5950070d5f10c57
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595693"
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

| **Medan** | **Perihalan** | **Kesan kefungsian** |
| --- | --- | --- |
| Nama | Nama baris subkontrak untuk membantu pengenalpastian. | Ini akan ditunjukkan sebagai lajur pertama dalam semua carian berdasarkan pada baris subkontrak. |
| Penerangan | Penerangan ringkas tentang perkhidmatan yang dibeli pada baris subkontrak. |Tiada |
| Jenis Baris |   Nilai medan ini mempunyai nilai lalai daripada **Berasaskan kuantiti**.| Tiada |
| Kaedah Pengebilan | Ini adalah set pilihan yang mewakili dua model kontrak utama disokong oleh Project Operations: **Harga Tetap** dan **Masa dan Bahan**. | Berdasarkan pada kaedah pengebilan yang dipilih, jadual invois berasaskan pencapaian tersedia untuk baris subkontrak dengan kaedah pengebilan Harga Tetap. |
| Kelas Transaksi | Nilai lalai ialah **Masa**. | Ini menunjukkan bahawa baris subkontrak sedang digunakan untuk merekod pembelian masa subkontraktor. |
| Peranan | Pilih peranan sumber subkontrak untuk masa yang sedang dibeli. | Peranan yang dilakukan oleh sumber subkontrak menentukan kos pembelian. |
| Permulaan Diminta | Peranan yang dilakukan oleh sumber subkontrak menentukan kos pembelian. | Ini digunakan untuk memilih senarai harga projek daripada senarai harga projek yang dilampirkan ke subkontrak. Kos peranan pada baris subkontrak datang daripada senarai harga. |
| Penamatan Diminta | Masukkan tarikh apabila penugasan sumber subkontraktor tamat. | Ini akan digunakan untuk menunjukkan amaran apabila pengurus projek menarik diri daripada keupayaan untuk keperluan sumber yang berlaku selepas tarikh ini. |
| Kuantiti Dipesan | Masukkan bilangan jam peranan yang dibeli daripada vendor. | Ini akan digunakan untuk menunjukkan amaran apabila pengurus projek menarik diri secara berlebihan daripada keupayaan ini untuk keperluan sumber. |
| Kumpulan Unit | Nilai lalai ialah **Kumpulan unit masa** yang tidak boleh diubah. | Tiada|
| Unit | Lalai untuk medan ini ialah unit asas jam daripada **Kumpulan unit masa**. Anda boleh mengubah nilai ini untuk membeli apa-apa unit bagi **Kumpulan unit masa** seperti hari atau minggu. | Gabungan **Peranan** dan **Unit** akan digunakan sebagai lalai atau dikira untuk harga unit bagi baris subkontrak. |
| Harga Unit | Harga unit lalai menggunakan gabungan **Peranan** dan **Unit** daripada senarai harga projek yang berkenaan dengan untuk tarikh **Tarikh Mula Diminta** bagi baris subkontrak. | Apabila senarai harga projek terpakai mempunyai harga yang ditetapkan dalam unit yang berbeza daripada unit pada baris subkontrak, sistem menggunakan penukaran unit untuk mengira harga seunit. |
| Jumlah kecil |    Ini ialah medan baca sahaja yang dikira sebagai Kuantiti x harga Unit, jika kedua-dua kuantiti dan nilai harga unit dimasukkan. Jika sama ada kuantiti, harga unit atau kedua-duanya kosong, anda boleh memasukkan nilai dalam medan. | Tiada|
| Cukai Jualan |   Masukkan amaun cukai jualan. |Tiada |
| Jumlah Amaun | Jumlah amaun baris subkontrak termasuk cukai. Medan ini dikira sebagai Subjumlah + cukai Jualan.|Tiada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
