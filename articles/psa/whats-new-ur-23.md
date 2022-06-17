---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 23, V3
description: Artikel ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas Kini Automasi Project Service 23, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 968626c7b2097a9b85178cb000b3633a766f54c9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913040"
---
# <a name="project-service-automation-update-release-23-v3"></a>Project Service Automation, Keluaran Kemas kini 23, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365. Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan. Keluaran ini serasi dengan Dynamics 365 9.x. Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini. Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](/power-platform/admin/install-remove-preferred-solution).

Artikel ini menyenaraikan ciri dan pembetulan yang baru atau diubah untuk Project Service Automation V3, Kemas Kini Keluaran 23. Versi ini mempunyai nombor bina V 3.10.34.30 dan secara amnya boleh didapati melalui kemas kini kendiri pada Ogos 2020.

## <a name="update-release-23"></a>Keluaran Kemas kini 23

### <a name="bug-fixes"></a>Pembetulan pepijat

**Masa dan Perbelanjaan**

Isu berikut telah dibaiki:
- Kendalikan kes pinggir dalam **Padam Ahli Pasukan Projek** untuk memberikan pengecualian bermakna.
- Import tugasan menyebabkan skrin alih keluar kosong.

**Pengurusan Sumber**

Isu berikut telah dibaiki:

- **Kad sumber grid penggunaan sumber** menunjukkan data yang salah apabila skala masa lebih daripada lima hari.
- Apabila pelanggan mencipta sumber boleh ditempah, pasang masuk sekejap-sekejap gagal menambah sumber secara automatik pada kumpulan Microsoft Office 365.
- Pandangan **penyesuaian** memaparkan kontur manual yang salah dalam pandangan **Minggu** atau **Bulan**.

**Pengurusan Projek**

Isu berikut telah dibaiki:

- Bilangan berlebihan entiti **RetrieveMultiple for usersettings** telah menyebabkan prestasi diturun taraf untuk kelulusan projek dan operasi lain.
- Carian sumber grid **Perancangan Tugas** hanya terhad kepada lima ahli pasukan daripada pasukan projek. 
- Carian sumber grid **Perancangan Tugas** tidak menapis sumber yang tidak aktif.
- Mod manual tidak berfungsi seperti yang dijangkakan dalam struktur pecahan kerja perancangan projek.
- Grid **Perancangan Tugas** menunjukkan **Kategori Transaksi Tidak Aktif**.
- Grid **Tugasan Sumber** dibundarkan dengan tidak betul apabila tugas mempunyai berbilang tugas.
- Nilai pembundaran adalah berbeza antara kos yang dirancang dan kos sebenar untuk satu tugas.

**Sales**

Isu berikut telah dibaiki:

- Klik dua kali **Kutip Semua Kategori Transaksi** mencipta berbilang baris.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
