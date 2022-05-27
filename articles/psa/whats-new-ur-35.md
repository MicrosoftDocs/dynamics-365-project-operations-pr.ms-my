---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 35, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas kini Microsoft Dynamics 365 Project Service Automation 35, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: e210777f1e4d149b700721ac7fb9bd129b1166fe
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574039"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 35, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami amat berbesar hati mengumumkan kemas kini terbaharu untuk apl Microsoft Dynamics 365 Project Service Automation. Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan. Kemas kini serasi dengan Dynamics 365 9.x. Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian dalam talian Pusat Pentadbir untuk Dynamics 365 dan pasang kemas kini. Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](/power-platform/admin/install-remove-preferred-solution).

Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Keluaran Kemas kini Project Service Automation 35, V3. Versi ini mempunyai nombor binaan V3.10.56.110 dan secara umumnya tersedia melalui kemas kini kendiri pada September 2021.

## <a name="update-release-35"></a>Keluaran Kemas kini 35

### <a name="bug-fixes"></a>Pembetulan pepijat

Isu berikut telah dibaiki.

**Masa dan Perbelanjaan**

- Pelulus projek menerima ralat kelayakan baca apabila mereka meluluskan entri perbelanjaan dengan peranan **Pelulus Projek**.
- Pelulus projek menerima ralat kelayakan tulis pada **msdyn_projectapproval** apabila mereka membatalkan entri masa yang diluluskan dengan peranan **Pelulus Projek**.
- Apabila anda memilih **Salin minggu** dalam entri masa dalam Dynamics 365 untuk telefon - modul aplikasi Hab Sumber Projek, ralat berikut berlaku: "...\OfficeProductivity_RibbonRules.js.map: HTTP error: status code 404, net::ERR_HTTP_RESPONSE_CODE_FAILURE."
- Dasar **Cuba semula** meluluskan entri yang telah ditolak sebelumnya secara automatik.
- Subgrid **Set Kelulusan** menunjukkan tindakan reben yang tidak terpakai.
- Ikon hilang untuk **Tugas Projek** dan **Peranan Sumber** pada entiti **Entri Masa**.
- Apabila anda mengimport tugasan sumber, entri masa yang diimport tidak mempunyai tempoh yang betul untuk tugasan yang dicipta melalui tugas mod manual.
- **Padam** hilang daripada halaman **Carian Lanjutan untuk rekod Entri Masa**.
- **Simpan** hilang daripada halaman **maklumat Entri Masa**. Isu ini mengelakkan perubahan daripada disimpan apabila halaman ditutup.

**Perancangan projek**

- Grid **Tugasan Sumber** dan **Penyesuaian Sumber** tidak mengisih atribut yang dikelompokkan mengikut abjad.
- Tugas tidak boleh dicipta jika tingkah laku tarikh disesuaikan kepada **Tarikh Sahaja**.

**Pengurusan sumber**

- Jika Dynamics 365 Field Service dan Project Service Automation dipasang, isu lapisan terlebih tindih berlaku apabila **Pandangan Berkaitan Keperluan Sumber** dikaitkan dengan halaman utama.
- Klik dua kali **Simpan** dalam kotak dialog **Cipta Pantas Ahli Pasukan** mengelakkan keperluan sumber daripada dicipta.

**Jualan**

- Pengecualian akan dibuang jika anda memadamkan tugas yang dikaitkan dengan sebut harga yang mempunyai status **Dimenangi**.
