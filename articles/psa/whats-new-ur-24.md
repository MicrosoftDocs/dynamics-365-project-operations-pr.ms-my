---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 24, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas kini Project Service Automation 24, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 51d08dd147b7804cb5c9255159aeab2ecd94f4597d6e99c5fa92efe1246c44d0
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998067"
---
# <a name="project-service-automation-update-release-24-v3"></a>Project Service Automation, Keluaran Kemas kini 24, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365. Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan. Keluaran ini serasi dengan Dynamics 365 9.x. Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini. Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](/power-platform/admin/install-remove-preferred-solution).

Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 24. Versi ini mempunyai nombor bina V 3.10.42.43 dan secara amnya boleh didapati melalui kemas kini kendiri pada Oktober 2020.

## <a name="update-release-24"></a>Keluaran Kemas kini 24

### <a name="bug-fixes"></a>Pembetulan pepijat

**Sales**

Isu berikut telah dibaiki:

- Masalah semasa menetapkan senarai harga lalai produk.
- Prestasi menang Sebut Harga perlahan disebabkan senarai harga terbenam dan salinan rekod harga peranan.
- **Kontrak Projek/Hab Jualan** > **Item Baris Produk/Kuantiti Baris Pesanan** dibundarkan secara automatik kepada integer terdekat.
- Tingkatkan kepada kelayakan sistem apabila membaca senarai harga.
- Salin medan alamat pelanggan **address1_freighttermscode** dan **address1_shippingmethodcode** kepada Sebut Harga/Pesanan. 


**Masa dan Perbelanjaan**

Isu berikut telah dibaiki:

- **Grid Entri Masa** tidak menyokong tingkah laku masa **Tarikh Sahaja**.
- **Entri Masa** tidak disegarkan semula secara automatik. Segar semula manual diperlukan.
- Tidak dapat mengimport entri masa daripada tugasan apabila terdapat rehat (0 jam) dalam tugasan sumber.
- Apabila mencipta entri masa, tetapkan mula sama seperti **msdyn_date**.
- Dayakan semula edit pukal untuk entri masa.

**Pengurusan Sumber**

Isu berikut telah dibaiki:

- Mencuba untuk mengemas kini status tempahan antara hari tanpa keperluan akan membuang pengecualian rujukan yang tidak sah.
- Ralat memuatkan **Pandangan Penyesuaian**.


**Pengurusan Projek**

Isu berikut telah dibaiki:

- Dalam **Jadual Projek**, apabila mengubah daripada **Manual** kepada **Auto**, simpan auto tidak selesai.
- Kos perbelanjaan tidak sepatutnya dikira ke atas varians pada **Grid Penjejakan Projek**.
- Tingkah laku yang tidak konsisten untuk lajur **Tag anggaran** semasa beban berbanding mengubah jenis **Fasa Masa**.
- Kos sebenar ke atas projek mungkin tidak menggambarkan jumlah daripada **Sebenar**.
- **Anggaran Tarikh Tamat** pada tab **Ringkasan** tidak sepadan dengan **Jadual WBS**.
- **Kemas Kini Masa Sebenar** di luar tidak berfungsi dengan betul.
- Pengurus Projek di luar akar **BU** tidak boleh mencipta projek.
- Perubahan kepada tugas atau kategori tentang **Anggaran Perbelanjaan** tidak diteruskan.
- **Salinan kontrak** menyalin jadual invois dan status jalanan.
- Butang **Segar Semula Sebenar** mengira tugasan ringkasan dengan salah.
- Tambahan Projek Microsoft: Betulkan ralat rujukan tidak sah jika mana-mana ahli pasukan mempunyai unit penyumberan kosong.



[!INCLUDE[footer-include](../includes/footer-banner.md)]