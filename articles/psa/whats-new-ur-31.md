---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 31, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Kemas kini Project Service Automation Keluaran 31, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 70a8bd381c27c9a3dd3b33c582e5616fad280e95
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586769"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 31, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365. Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan. Keluaran ini serasi dengan Dynamics 365 9.x. Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini. Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](/power-platform/admin/install-remove-preferred-solution).

Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 31. Versi ini mempunyai nombor binaan V3.10.52.77 dan secara amnya boleh didapati melalui kemas kini sendiri pada Mei 2021.

## <a name="update-release-31"></a>Keluaran Kemas kini 31

### <a name="bug-fixes"></a>Pembetulan pepijat

**Masa dan Perbelanjaan**

Isu berikut telah dibaiki:

- Butang arahan kawalan entri masa pada halaman **Sumber Boleh Ditempah** adalah mengelirukan.
- Pengecualian rujukan nol dijana dalam **Project.SetTrackingFields** apabila meluluskan entri masa.

**Pengurusan Sumber**

Isu berikut telah dibaiki:

- **Cipta Ahli Pasukan** tidak memaparkan tetapan metadata persediaan penempahan untuk **Status Penempahan Terikat Lalai** dengan betul.
- Apabila menaik taraf daripada PSA 1.X ke 3.X, proses naik taraf gagal pada **UpgradeResourceRequirements**.


**Jualan**

Isu berikut telah dibaiki:

- Hasil sebenar menukar jumlah ke mata wang projek dalam grid penjejakan.
- Lalai mata wang lalai tidak jelas apabila mencipta baris jurnal, baris sebut harga dan baris kontrak dalam senario yang mata wang asas organisasi berbeza daripada mata wang projek.
- Pertanyaan **Pengesahan jurnal pembetulan belum selesai** tidak ditapis oleh projek.
- Baki jualan tidak dikira dengan betul pada projek.
- Sebut harga berdasarkan pada kenalan gagal apabila sebut harga dicipta tanpa senarai harga.
- Tiada spinner pemprosesan ditunjukkan apabila anda memilih **Sahkan Invois**.
- Tiada spinner pemprosesan ditunjukkan apabila anda memilih **Cipta Invois**.
- Menutup sebut harga sebagai kehilangan tidak membatalkan tempahan.







