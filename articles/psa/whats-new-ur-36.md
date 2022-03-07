---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 36, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas kini Microsoft Dynamics 365 Project Service Automation 36, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.openlocfilehash: 9b85aed79acb7e7784a23f54a2e9af1cc83f5f4d
ms.sourcegitcommit: 6d9fc4dc851814664bf71729904ab4bedd85fe70
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/06/2021
ms.locfileid: "7606794"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 36, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami amat berbesar hati mengumumkan kemas kini terbaharu untuk apl Microsoft Dynamics 365 Project Service Automation. Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan. Kemas kini serasi dengan Dynamics 365 9.x. Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian dalam talian Pusat Pentadbir untuk Dynamics 365 dan pasang kemas kini. Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](/power-platform/admin/install-remove-preferred-solution).

Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Keluaran Kemas kini Project Service Automation 36, V3. Versi ini mempunyai nombor binaan V3.10.57.152 dan secara amnya boleh didapati melalui kemas kini kendiri pada Oktober 2021.

## <a name="update-release-36"></a>Keluaran Kemas kini 36

### <a name="bug-fixes"></a>Pembetulan pepijat

Isu berikut telah dibaiki.

**Umum**
- Nama medan **Templat Jam Kerja Lalai** diterjemahkan dengan salah pada halaman **Parameter Projek**.
- Pasang masuk tak segerak menangani pengecualian yang berkaitan dengan **SharedVariableService** secara salah.

**Masa dan Perbelanjaan**
- Apabila baris jurnal hilang atau pengguna tidak mempunyai kelayakan yang betul untuk membaca baris jurnal, ralat yang salah berlaku apabila kelulusan projek dibatalkan.
- Pengguna tidak boleh membatalkan kelulusan apabila perbelanjaan atau entri masa mempunyai lebih daripada satu kelulusan projek yang berkaitan.
- **Ketidakhadiran** dan **Percutian** tidak diterjemahkan dengan betul untuk Bahasa Cina dalam pencarian pada halaman cipta pantas **Entri Masa**.

**Pengurusan sumber**
- Pengguna tidak boleh mencari sumber dalam **Pembantu Jadual** apabila mod pandangan ditetapkan ke **Hari**, **Minggu** atau **Bulan**.
- Sumber generik tidak dibenarkan untuk mempunyai nama kedudukan kosong. 
- Menutup kontrak kerana kehilangan tidak membatalkan tempahan masa hadapan.

**Jualan**
- Apabila persekitaran mempunyai volum yang besar bagi produk, prestasi menurun dalam grid **Anggaran Bahan**.
- Apabila mencipta projek daripada templat, mata wang projek tidak akan menjadi lalai ke unit kontrak Pengurus Projek masing-masing.
- Jumlah sebenar tidak selalu sesuai dengan yang ditunjukkan pada projek yang perlu dibayar atau jumlahnya menjadi negatif dalam senario penarikan balik tertentu.
- Ralat berlaku apabila anda mengaitkan projek yang dicipta daripada templat projek ke baris kontrak.
- Pengguna boleh memadam baris kontrak dengan pencapaian, **Bersedia untuk diinvois** dan **Invois Dicipta**. Ini sepatutnya tidak dibenarkan.
- Apabila anggaran diimport daripada projek, kebolehtuntutan butiran baris sebut harga tidak ditetapkan dengan betul semasa pengebilan berasaskan tugas didayakan untuk baris sebut harga.
- Apabila anda menambahkan pencapaian pengebilan harga tetap, pencapaian tidak ditunjukkan dalam subgrid pencapaian sehingga halaman disegar semula.
- Pengecualian rujukan nol dijana apabila anda mencipta kontrak projek dengan nama sebut harga yang nol.
- Tugas mod manual bagi mata wang projek yang berbeza daripada hasil mata wang sumber dalam anggaran harga yang tidak betul.
- Pengguna tidak boleh menarik balik transaksi yang telah berjaya dibetulkan oleh invois pembetulan.
- Kategori transaksi dinyahaktifkan dipaparkan dalam grid **Anggaran Perbelanjaan**.



