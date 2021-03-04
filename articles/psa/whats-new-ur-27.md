---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 27, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Project Service Automation Keluaran Kemas kini 27, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6b9da3ec54ec10408774945d26db9e702c858d05
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146674"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 27, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365. Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan. Keluaran ini serasi dengan Dynamics 365 9.x. Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini. Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 27. Versi ini mempunyai nombor binaan V3.10.45.98 dan secara amnya boleh didapati melalui kemas kini kendiri pada Januari 2021.

## <a name="update-release-27"></a>Keluaran Kemas kini 27

### <a name="bug-fixes"></a>Pembetulan pepijat

**Umum**

Isu berikut telah dibaiki:

- Log yang dijana oleh pasang masuk dalam Project Service Automation belum ditetapkan ke padam auto.
- Naik taraf automatik gagal kerana penyelesaian Project Service Automation mengandungi nol legasi NavBarArea dan elemen tajuk.

**Masa dan Perbelanjaan**

Isu berikut telah dibaiki:

- Grid **Entri Masa** memaparkan data yang salah untuk tingkah laku tarikh **Bebas Zon Waktu**.
- Grid **Entri Masa** mencipta masa yang salah untuk tingkah laku tarikh **Bebas Zon Waktu**.
- Carian tugas tidak terhad kepada projek terpilih dalam halaman **Edit Entri Masa**.
- Kelulusan masa untuk entri masa bukan projek disekat kerana sistem mencari pelulus projek.
- Entri yang betul pada Aktual memaparkan mesej ralat yang salah.
- Apabila tugas mengandungi nilai nol untuk kos aktual dan jumlah projek disegarkan semula, ralat berikut berlaku, "Kekunci yang diberikan tiada dalam kamus".
- Dalam tika tertentu, **Kumpul Mengikut** yang menapis pada tab **Anggaran Projek** tidak memaparkan anggaran perbelanjaan.
- Selang **Waktu Jimat Siang Hari** tidak betul untuk entri masa.

**Pengurusan Projek**

Isu berikut telah dibaiki:

- Penambahbaikan caching yang meningkatkan prestasi berkaitan dengan memuat halaman **Projek**.
- Peraturan perniagaan yang lapuk menghalang tugas projek daripada disiapkan.
- Kontur Tambahan Microsoft Project tidak menghormati kalendar tambahan menyebabkan keperluan sumber yang tidak betul.
- Mencipta projek daripada templat dengan tidak betul menetapkan tarikh tugasan dan menghalang keupayaan untuk menjana keperluan sumber.
- Pengguna tidak boleh mengakses pilihan **Kategori**, **Perihalan**, **Status** menggunakan papan kekunci.
- Nilai jualan aktual projek tidak termasuk nilai yuran dan jualan bahan.
- Pengagregatan jualan dan kos aktual berlaku secara tidak betul dengan kadar pertukaran yang berbeza.
- Perihalan dalam **Templat Jam Kerja Lalai** adalah mengelirukan.
- Menginden tugas tidak mengalihkeluarkan **Kategori** dalam antara muka pengguna hingga ia disegar semula.
- Tiada pengesahan untuk memastikan memindahkan projek melebihi tarikh akhir tidak dibenarkan.

**Sales**

Isu berikut telah dibaiki:

- Pengecualian rujukan nol dijana pada baris sebut harga projek kerana **Import daripada Anggaran Projek** kelihatan apabila projek belum dipilih.
- Ralat berikut, "Rujukan objek tidak ditetapkan ke tika objek" berlaku apabila menutup sebut harga sebagai **Menang**.
- Status pelarasan tidak ditetapkan semasa pembalikan aktual apabila menyahpautkan projek daripada baris kontrak.
- Apabila kedua-dua Dynamics 365 Field Service dan Project Service Automation dipasang, pilihan **Kunci penetapan harga** dan **Guna Penetapan Harga Semasa** tidak dipaparkan pada masa yang sama dalam halaman **Invois**.
- Untuk bahasa Jepun, terdapat terjemahan yang tidak konsisten dengan halaman berasaskan kalendar lain.
- **Aktifkan** dan **Nyahaktifkan** telah dialih keluar daripada entiti **Perkaitan Senarai Harga** dalam Project Service Automation.


[!INCLUDE[footer-include](../includes/footer-banner.md)]