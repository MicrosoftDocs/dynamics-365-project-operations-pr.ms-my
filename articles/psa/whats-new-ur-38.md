---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 38, V3
description: Artikel ini menyenaraikan ciri dan pembetulan yang tersedia dalam Microsoft Dynamics 365 Project Service Automation Kemas Kini Keluaran 38, V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: ccc08cd0bc365bd4761424a4c0ceac91985e7c89
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915196"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 38, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami amat berbesar hati mengumumkan kemas kini terbaharu untuk apl Microsoft Dynamics 365 Project Service Automation. Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan. Kemas kini serasi dengan Dynamics 365 9.x. Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian dalam talian Pusat Pentadbir untuk Dynamics 365 dan pasang kemas kini. Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](/power-platform/admin/install-remove-preferred-solution).

Artikel ini menyenaraikan ciri dan pembetulan yang baru atau diubah untuk Keluaran Kemas Kini Automasi Project Service 38, V3. Versi ini mempunyai nombor binaan V3.10.59.117 dan secara amnya tersedia melalui kemas kini dengan sendiri pada Disember 2021.

## <a name="update-release-38"></a>Keluaran Kemas kini 38

### <a name="bug-fixes"></a>Pembetulan pepijat

Isu berikut telah dibaiki.

**Masa dan Perbelanjaan**

- Pengecualian berlaku apabila panjang log set kelulusan melebihi 100,000 rekod.
- Pengguna tidak boleh mengakses **grid Kemasukan** Masa daripada **halaman utama Entri** Masa.
- Kotak **dialog Import** Entri Masa tidak menunjukkan sebarang teks apabila tiada item layak untuk diimport.
- Pengguna boleh mencipta set kelulusan di mana medan Status **Sasaran disetkan** kepada **Tidak Diketahui**.

**Pengurusan Projek**

- Kontur tidak ditunjukkan dengan betul dalam tugasan sumber untuk UTC(+09:30) dan UTC(+10:00) apabila masa penjimatan siang bermula.
- Medan **Lajur** Tambahan untuk struktur pecahan kerja tersembunyi di sesetengah tempat.
- Pemilih tarikh untuk kawalan kalendar dalam **grid Tugas** Projek tidak disetempatkan dengan betul untuk bahasa Cina.

**Jualan**

- **Prestasi** Kontrak dan **nilai Kos** Sebenar Projek tidak sepadan apabila sumber yang boleh ditempah yang mempunyai unit kontrak dan mata wang yang berbeza menyerahkan entri masa.
- Aliran kerja tersuai untuk mengesahkan invois secara automatik gagal apabila invois diimport sebagai penyelesaian terurus. Mesej berikut ditunjukkan: "Microsoft.Xrm.Sdk.invalidPluginExecutionExceptionException Message: Status invois tidak sah."
- Apabila **Root** dipilih sebagai pilihan ringkasan, dan projek itu mempunyai anggaran dari campuran kelas transaksi (contohnya, gabungan masa, perbelanjaan, dan anggaran material), sistem meringkaskan merentasi kelas transaksi sebagai garis yuran tunggal.
- Dalam senario di mana garis perbelanjaan ditambahkan sebelum garis kontrak dikaitkan dengan projek, harga yang betul tidak dimasukkan sebagai nilai lalai dalam **medan Harga** Kemas Kini.
- Jumlah jualan negatif tidak dibenarkan pada **entiti Project** dan **Tugas**.
