---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 18, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas kini Project Service Automation 18, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: d6e0bb669513185ca266858ea9b8a89ed6dd4408
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147214"
---
# <a name="project-service-automation-update-release-18-v3"></a>Project Service Automation, Keluaran Kemas kini 18, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365. Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan. Keluaran ini serasi dengan Dynamics 365 9.x. Untuk mengemas kini kepada keluaran ini, lawati Pusat Pentadbir untuk Dynamics 365 online, halaman penyelesaian untuk memasang kemas kini. Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 18. Versi ini mempunyai nombor binaan V3.10.8.12 dan secara amnya boleh didapati melalui kemas kini sendiri pada April 2020.

## <a name="update-release-18"></a>Keluaran Kemas kini 18

### <a name="bug-fixes"></a>Pembetulan pepijat

**Masa dan Perbelanjaan**

- Dibaiki: Aliran **Ingat semula**, **Minta** dan **Batalkan Kelulusan** menghasilkan pengecualian dengan mesej ralat tidak jelas.
- Dibaiki: Apabila **Batal Kelulusan** gagal untuk perbelanjaan, ralat pengecualian yang berkaitan tidak dibuang.
- Dibaiki: Grid Entri Masa secara salah mengendalikan hari tidak bekerja di Australia selepas pertukaran waktu penjimatan siang (DST) pada bulan Oktober.
- Dibaiki: Logik lalai yang salah menghalang penghantaran perbelanjaan.
- Dibaiki: Apabila kelulusan entri masa gagal, kelulusan masih dalam keadaan **Belum Selesai**.
- Dibaiki: Ralat SQL ke atas kelulusan pukal (kunci mati/tamat tempoh).
- Dibaiki: Isu prestasi penting dalam pengalaman pengguna yang disebabkan oleh mengemas kini ahli pasukan sambil meluluskan entri masa.

**Pengurusan Projek**

- Dibaiki: Pemberitahuan zon masa dipindahkan daripada pandangan **Penyesuaian** ke borang utama **Projek**.
- Dibaiki: Templat kalendar tidak lalai secara betul apabila borang projek baru dibuka.
- Dibaiki: Untuk pelayar berasaskan chromium, pengguna tidak dapat memilih tugas terdahulu untuk dipadamkan dengan mudah.
- Dibaiki: Mencipta atau menyalin **Projek daripada templat Kosong** menarik tugasan yang tidak berkaitan.
- Dibaiki: Dalam kes-kes edge tertentu, mencipta tugasan baharu daripada keputusan grid tugas dalam rekod pendua yang dicipta.
- Dibaiki: Dalam mod manual, pengguna tidak dapat mengemas kini tarikh mula tugas lebih lewat daripada tarikh semasa yang disimpan.

**Pengurusan Sumber**

- Dibaiki: Baris subjumlah pandangan **Penyesuaian** salah mengira penempahan varians selepas melanjutkan penempahan.
- Dibaiki: Pandangan **Penyesuaian** yang salah memaparkan tugasan sumber apabila sumber boleh ditempah mempunyai kalendar yang tidak sepadan dengan kalendar projek.

**Sales**

- Dibaiki: Apabila entri masa telah diluluskan semula (**Lulus > Batal >** lulus semula), pendua sebenar tidak boleh dikenakan bayaran dibuat.
