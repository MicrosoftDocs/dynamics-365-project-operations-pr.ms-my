---
title: Urus peluang berasaskan projek
description: Topik ini memberikan maklumat tentang cara untuk bekerja dengan peluang yang berkaitan dengan projek.
author: rumant
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: aebff4d3a94735e76bcb9cafd25a058207dae846
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996352"
---
# <a name="manage-project-based-opportunities"></a>Urus peluang berasaskan projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Syarikat berasaskan projek biasanya mempunyai operasi mereka untuk penghantaran tersebar merentasi berbilang negara dan di seluruh dunia. Kos pelaksanaan projek dan penghantaran mungkin berbeza mengikut geografi atau divisyen yang menguruskan penghantaran. Seterusnya, ini boleh memberi kesan pada margin urusan. Penghantaran perkhidmatan berasaskan projek biasanya melibatkan kuantiti masa sumber manusia yang lama, perbelanjaan untuk perjalanan, kos bahan dan perbelanjaan lain yang agak besar.

Peluang berasaskan projek dalam Dynamics 365 Project Operations ialah direka bentuk dengan lanjutan kepada Dynamics 365 Sales. Topik ini memberikan butiran tentang medan dan logik perniagaan yang berbeza termasuk dalam fungsian tambahan yang diperlukan oleh syarikat berasaskan projek untuk menguruskan peluang berasaskan projek.

## <a name="view-all-project-based-opportunities"></a>Lihat semua peluang berasaskan projek

Senarai semua peluang berasaskan projek dapat dilihat daripada halaman senarai **Peluang**. 

1. Pergi ke **Jualan** > **Peluang**.
2. Gunakan **Penukar pandangan** untuk memilih pandangan peluang ditapis yang lain. Anda boleh mencipta pandangan anda sendiri dengan kriteria penapis tersuai untuk mengkonfigurasi pilihan pandangan dan navigasi ini.

Peluang projek boleh dicipta atau dipadamkan daripada halaman senarai ini atau halaman butiran.

## <a name="business-process-flow-for-project-based-deals"></a>Aliran proses perniagaan untuk urusan berasaskan projek

Aliran proses perniagaan berikut disokong untuk urusan berasaskan projek dalam Project Operations:

- Bakal pelanggan ke proses perniagaan Peluang
- Proses jualan Peluang

### <a name="lead-to-opportunity-business-process"></a>Bakal pelanggan kepada proses perniagaan peluang 
Bakal pelanggan kepada proses perniagaan peluang menyokong peringkat berikut:

| Peringkat | Entiti yang dipetakan | Fungsi |
| --- | --- | --- |
| Layakkan | Bakal Pelanggan | Layakkan bakal pelanggan untuk mencipta akaun, kenalan dan peluang. |
| Bangunkan | Peluang | Membangunkan peluang untuk menambah lebih banyak maklumat tentang kerja yang terlibat, pemegang amanah utama dan pertandingan. |
| Cadangkan | Peluang | Membangunkan cadangan dan mendapatkan kelulusan daripada pasukan semakan dalaman. |
| Tutup | Peluang | Memenangi peluang untuk menutup urusan. |

### <a name="opportunity-sales-process"></a>Proses jualan Peluang
Proses jualan Peluang dalam Operasi Projek merupakan tambahan kepada aliran perniagaan proses jualan Peluang dalam aplikasi Jualan. Proses perniagaan ini direka luar kotak untuk menyokong peringkat berikut dalam peluang berasaskan projek.

| Peringkat | Entiti yang dipetakan | Fungsi |
| --- | --- | --- |
| Layakkan | Peluang | Layakkan bakal pelanggan untuk mencipta akaun, kenalan dan peluang. |
| Cadangkan | Sebut Harga | Bangunkan cadangan menggunakan sebut harga projek dan dapatkan kelulusan daripada pasukan semakan dalaman. |
| Kontrak | Kontrak Projek | Menangi sebut harga untuk mencipta kontrak dan mulakan pelaksanaan dan penghantaran projek. |
| Tutup | Kontrak Projek | Selesaikan kerja dengan jayanya dan tutup kontrak projek. |

> [!NOTE]
> Jika urusan berasaskan projek anda bermula dengan Bakal Pelanggan, Bakal Pelanggan kepada proses perniagaan Peluang diberi keutamaan.
>
> Jika urusan berasaskan projek anda bermula dengan Peluang, proses jualan Peluang diberi keutamaan.

Anda boleh mengedit aliran proses perniagaan produk atau mencipta aliran proses perniagaan anda sendiri untuk menjejak proses jualan anda seperti yang diperlukan. Untuk mendapatkan maklumat lanjut tentang aliran proses perniagaan, lihat [Gambaran keseluruhan aliran proses perniagaan](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]