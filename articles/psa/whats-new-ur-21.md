---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 21, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas kini Project Service Automation 21, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: b1194c1cf1997b68030fe88360c6ebb756c715fd
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147034"
---
# <a name="project-service-automation-update-release-21-v3"></a>Project Service Automation, Keluaran Kemas kini 21, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365. Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan. Keluaran ini serasi dengan Dynamics 365 9.x. Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini. Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 21. Versi ini mempunyai nombor binaan V 3.10.32.50 dan secara amnya boleh didapati melalui kemas kini sendiri pada Jun 2020.

## <a name="update-release-21"></a>Keluaran Kemas kini 21

### <a name="bug-fixes"></a>Pembetulan pepijat

**Masa dan Perbelanjaan**

Isu berikut telah dibaiki:

- Apabila mengehoskan **Kawalan Grid Entri Masa** dalam Papan Pemuka, grid tidak menggunakan lebar penuh bekas grid papan pemuka.
- Untuk zon masa tertentu, kawalan grid **Entri Masa** tidak memaparkan rekod.
- Entri masa yang selepas 9:00 MLM muncul pada hari yang salah.
- Pengguna tidak dapat menyerahkan perbelanjaan jika kategori perbelanjaan, **Resit perbelanjaan yang diperlukan** tidak mempunyai nilai.

**Pengurusan Sumber**

Isu berikut telah dibaiki:

- Penempahan tidak aktif dipaparkan dalam pandangan **Penyelarasan**.
- Pencapaian sumber generik tiada pengesahan untuk memastikan status penempahan yang sah wujud.

**Pengurusan Projek**

Isu berikut telah dibaiki:

- Grid borang **Projek** ( **Tugasan Sumber**, **Tugas**, pandangan **Penyelarasan**, **Anggaran Perbelanjaan**) tetap boleh diedit walaupun semasa projek tidak aktif.
- Pelanggan duplikasi tidak boleh digabungkan dengan pelanggan yang dipautkan kepada kontrak projek yang telah disahkan.
- Apabila sumber yang tidak mempunyai kalendar yang sah ditambah, sistem tidak akan mengembalikan mesej ralat mesra pengguna.
- Butang **Tambah Tugas** pada grid tugas didayakan apabila projek dipautkan kepada **Tambahan Projek Microsoft**.
- Usaha bertambah tidak terkawal apabila tugas dengan kategori ditugaskan kepada sumber dengan peranan yang terdapat harga kos yang ditentukan.

**Sales**

Peningkatan berikut telah dibuat:

- **Kekerapan Invois** dan **Permulaan Pengebilan** telah dipindahkan ke tab **Jadual invois**.

Isu berikut telah dibaiki:

- **Jumlah Harga Jualan** ialah sifar (0) bagi **Kategori** walaupun **Peranan** mempunyai jumlah harga jualan yang bukan sifar.
- Pelanggan tidak boleh mengubah nilai medan **Status Invois** untuk **Bersedia untuk penginvoisan** apabila proses tersuai lain mengemas kini medan tambahan.
- Butang **Segar Semula Baris Invois** boleh mencipta beberapa baris pendua jika ia dipilih berulang kali.
- Butang **Kemas Kini Harga** tidak berfungsi pada subgrid **Harga Peranan** dalam borang **Pandangan Cepat**.
- Logik **Ketetapan Senarai Harga Jualan** tidak mengendalikan zon masa dengan betul, menyebabkan pemilihan senarai harga yang salah.
- **Jumlah Kos Sebenar** projek boleh dimatikan oleh jumlah pecahan selepas entri masa tunggal diluluskan.
- Logik **Ketetapan Harga** tidak memberikan mesej ralat mesra pengguna jika **RolePrice yang didapatkan semula** tidak mempunyai nilai dalam medan **'Unit utama'** dan **'Harga Dalam Unit Utama**.
