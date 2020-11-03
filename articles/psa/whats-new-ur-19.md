---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 19, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas kini Project Service Automation 19, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: ecc923cccfad21985025ab9d8006aaff16afc25f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081181"
---
# <a name="project-service-automation-update-release-19-v3"></a>Project Service Automation, Keluaran Kemas kini 19, V3

Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365. Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan. Keluaran ini serasi dengan Dynamics 365 9.x. Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini. Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk PSA V3, Keluaran Kemas kini 19. Versi ini mempunyai nombor binaan V3.10.30.41 dan secara amnya boleh didapati melalui kemas kini sendiri pada Mei 2020.

## <a name="update-release-19"></a>Keluaran Kemas kini 19

### <a name="bug-fixes"></a>Pembetulan pepijat

**Masa dan Perbelanjaan**

Isu berikut telah dibaiki: 

- Ralat yang diperolehi daripada import kemasukan masa tidak timbul dengan betul.
- Grid Entri Masa tidak menyokong tingkah laku medan **Tarikh Sahaja**.
- Sumber projek tidak dapat mencipta perbelanjaan dengan projek.

**Pengurusan Projek**

Isu berikut telah dibaiki: 

-  Tugas cucu menyebabkan anggaran yang salah tidak betul semasa Pengiraan Siap (EAC).

**Sales**

Isu berikut telah dibaiki: 

- **Tindakan mengira semula** tidak berfungsi dengan butiran baris kontrak perbelanjaan atau butiran baris sebut harga.
- **Harga Kemas kini** hilang untuk anggaran perbelanjaan.
-  Pelanggan tidak boleh memilih sebab status kontrak tersuai daripada halaman **Kontrak Projek**.
- Pelanggan mengalami prestasi yang diturun taraf apabila mencipta senarai harga tersuai daripada sebut harga.
- Pelanggan mengalami ketidakselarasan dengan **unit** lalai pada **Butiran Baris Sebut Harga** dan halaman **Butiran Baris Kontrak**.
- Menambah butiran kategori transaksi tidak boleh dikenakan ke baris kontrak bercukai tidak akan menghormati jenis **Pengebilan tidak boleh dituntut** pada kategori transaksi.
- Pelanggan tidak boleh menggunakan peranan dan kategori baru yang ditambah pada kontrak yang dicipta sebelumnya.
- Pelanggan mengalami prestasi yang diturun taraf yang tidak perlu untuk mendapatkan dalam Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs
- Peranan yang ditetapkan sebagai tidak boleh digunakan dalam senarai **Kategori Sumber** harus ditambah ke tab **Peranan boleh dituntut** sebagai **Tidak tidak boleh dituntut** pada baris kontrak untuk projek.
- Pelanggan mungkin mengalami prestasi yang diturun taraf apabila mencipta projek kerana **GetBookableResourceIdFromUser** mendapatkan semua kolum sumber boleh ditempah bukan sekadar ID utama.
- Entiti **TransactionType** kehilangan pasang masuk kemas kini pra pengesahan untuk mengelakkan pengguna daripada memasuki **Unit** dan **UnitGroups** yang tidak sah untuk jenis transaksi.
- Langkah **Keluarkan** tidak berfungsi untuk import kemasukan masa.
