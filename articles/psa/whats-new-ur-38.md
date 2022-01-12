---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 38, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas kini Microsoft Dynamics 365 Project Service Automation 38, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
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
ms.openlocfilehash: 1e5175b12c9e06962888bf09c8e07119b9505dda
ms.sourcegitcommit: 2aba2082d50b20b596ee86735045644cd647c2b0
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 12/08/2021
ms.locfileid: "7901515"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 38, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami amat berbesar hati mengumumkan kemas kini terbaharu untuk apl Microsoft Dynamics 365 Project Service Automation. Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan. Kemas kini serasi dengan Dynamics 365 9.x. Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian dalam talian Pusat Pentadbir untuk Dynamics 365 dan pasang kemas kini. Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](/power-platform/admin/install-remove-preferred-solution).

Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Keluaran Kemas kini Project Service Automation 38, V3. Versi ini mempunyai nombor binaan V3.10.59.117 dan secara amnya tersedia melalui kemas kini dengan sendiri pada Disember 2021.

## <a name="update-release-38"></a>Keluaran Kemas kini 38

### <a name="bug-fixes"></a>Pembetulan pepijat

Isu berikut telah dibaiki.

**Masa dan Perbelanjaan**

- Pengecualian berlaku apabila panjang log set kelulusan melebihi 100,000 rekod.
- Pengguna tidak boleh mengakses **grid Entri Masa daripada halaman utama Entri** **Masa**.
- **Kotak dialog Import Entri Masa tidak menunjukkan sebarang teks apabila tiada item yang layak** diimport.
- Pengguna boleh mencipta set kelulusan di mana **medan Status Sasaran** disetkan kepada **Tidak Diketahui**.

**Pengurusan Projek**

- Kontur tidak ditunjukkan dengan betul dalam tugasan sumber untuk UTC(+09:30) dan UTC(+10:00) apabila waktu penjimatan siang bermula.
- Medan **Lajur Tambahan untuk struktur pecahan kerja disembunyikan dalam sesetengah** tempat.
- Pemilih tarikh untuk kawalan kalendar dalam **grid Tugas Projek tidak** disetempatkan dengan betul untuk bahasa Cina.

**Jualan**

- **Prestasi Kontrak** dan nilai Kos Sebenar Projek tidak sepadan apabila sumber boleh ditempah yang mempunyai unit kontrak dan mata **wang yang berbeza menyerahkan entri** masa.
- Aliran kerja tersuai untuk mengesahkan invois secara automatik gagal apabila invois diimport sebagai penyelesaian terurus. Mesej berikut ditunjukkan: "Mesej Microsoft.Xrm.Sdk.InvalidPluginExecutionException: Status invois tidak sah."
- Apabila **Root dipilih sebagai pilihan** ringkasan, dan projek itu mempunyai anggaran dari campuran kelas transaksi (contohnya, gabungan masa, perbelanjaan, dan anggaran bahan), sistem meringkaskan merentas kelas transaksi sebagai garis yuran tunggal.
- Dalam senario di mana garis perbelanjaan ditambahkan sebelum garis kontrak dikaitkan dengan projek, harga yang betul tidak dimasukkan sebagai nilai lalai dalam **medan Harga Kemas** Kini.
- Amaun jualan negatif tidak dibenarkan pada **entiti Projek** dan **Tugas**.
