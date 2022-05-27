---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 32, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Kemas kini Project Service Automation Keluaran 32, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 3ad87eceb90a48997aadf00803b8d14c5108eb83
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580099"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 32, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami amat berbesar hati mengumumkan kemas kini terbaharu untuk apl Microsoft Dynamics 365 Project Service Automation. Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan. Kemas kini serasi dengan Dynamics 365 9.x. Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian dalam talian Pusat Pentadbir untuk Dynamics 365 dan pasang kemas kini. Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](/power-platform/admin/install-remove-preferred-solution).

Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 32. Versi ini mempunyai nombor binaan V3.10.53.108 dan secara amnya boleh didapati melalui kemas kini sendiri pada bulan Jun 2021.

## <a name="update-release-32"></a>Keluaran Kemas kini 32

### <a name="bug-fixes"></a>Pembetulan pepijat

#### <a name="general"></a>Umum

- Apabila naik taraf utama gagal, hanya titik masuk aplikasi utama harus disekat, untuk memastikan entiti yang dikongsi masih boleh diakses.

#### <a name="time-and-expense"></a>Masa dan Perbelanjaan

Isu berikut telah dibaiki:

- **TimeEntriesImportFromResourceAssignment** tidak mengekalkan masa mula dan akhir pada hirisan kontur tugasan sumber.
- Apabila anda memilih **Emtri Terbuka** pada gris **Entri Masa**, anda mungkin akan dihalang daripada memilih borang lain.
- Semasa anda mengimport tugasan ke entri masa, pertanyaan kod pelanggan boleh menjana URL panjang yang gagal pertanyaan.
- Dalam grid **Entri Masa**, selepas nilai dipadamkan daripada sel, fokus tidak kekal dalam grid.
- Butang **Tolak** telah dialih keluar daripada pandangan **Kelulusan pemprosesan** untuk kelulusan moden.
- Kestabilan dan prestasi kelulusan pukal entri masa akan dipengaruhi oleh kunci mati dan kegagalan untuk mengendalikan penyesuaian dengan sewajarnya yang berkaitan dengan entiti **Entri Masa**.

#### <a name="project-planning"></a>Perancangan Projek

- Pengecualian rujukan nol akan dijana apabila anda mengemas kini projek yang mempunyai nilai nol dalam medan **Unit Berkontrak**.
- **Segar Semula Jumlah Projek** mengira baki kos dan baki jualan pada projek secara salah.
- Pengiraan penetapan harga yang berlebihan mempengaruhi prestasi yang berkaitan dengan kemas kini pada kontur peruntukan sumber.

#### <a name="resource-management"></a>Pengurusan Sumber

Isu berikut telah dibetulkan:

- Apabila keupayaan kalendar sumber boleh ditempah lebih daripada 1, Project Service Automation mengenal pasti kapasiti sebagai 0 (sifar) secara salah. Oleh itu, gelung tak terhingga berlaku dalam pandangan jadual.

#### <a name="sales"></a>Jualan

Isu berikut telah dibaiki:

- Apabila garisan jurnal dicipta yang mempunyai jenis transaksi tersuai, pengecualian rujukan nol berikut berlaku: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- Peranan dan kategori yang tidak diaktifkan sebelum sebut harga disalin tidak boleh ditambah ke peranan dan kategori sebut harga yang baru disalin.
- Tarikh dokumen dan tarikh perakaunan tidak sejajar dengan tarikh mula yang disediakan pada butiran baris invois yang dicipta secara langsung pada invois draf.
- Pengecualian rujukan nol dijana dalam senario yang berkaitan dengan ketidakaktifan peranan dan kategori sebelum sebut harga disalin.
- Tindakan **Kemas Kini Harga** pada halaman **Projek** tidak mengemas kini perbelanjaan dan anggaran penting.
