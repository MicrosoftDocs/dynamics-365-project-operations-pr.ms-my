---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 33, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas kini Project Service Automation 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 063290526c25e7073137fc88408be6a61d2d20ac
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601489"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 33, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami amat berbesar hati mengumumkan kemas kini terbaharu untuk apl Microsoft Dynamics 365 Project Service Automation. Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan. Kemas kini serasi dengan Dynamics 365 9.x. Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian dalam talian Pusat Pentadbir untuk Dynamics 365 dan pasang kemas kini. Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](/power-platform/admin/install-remove-preferred-solution).

Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 33. Versi ini mempunyai nombor binaan V3.10.54.98 dan secara umumnya tersedia melalui kemas kini kendiri pada Julai 2021.

## <a name="update-release-33"></a>Keluaran Kemas kini 33

### <a name="bug-fixes"></a>Pembetulan pepijat

**Masa dan Perbelanjaan**

Isu berikut telah dibaiki:

- Dua medan terkunci, **msdyn_description** dan **msdyn_externaldescription** boleh diedit selepas penyerahan.
- Mesej ralat berlaku jika perbelanjaan dicipta yang tidak berkaitan dengan projek.
- Apabila entri masa dicipta, peranan sumber ditetapkan secara lalai kepada peranti tidak aktif.
- Baris jurnal yang berkaitan dengan perbelanjaan yang ditarik balik dan dipadamkan tidak dipadamkan.
- Pada **Borang Cipta Cepat Entri masa**, kemas kini pandangan **Senarai Tugas Projek** untuk mengubah tarikh yang dipaparkan secara lalai kepada tarikh mula tugas.
- Apabila anda mencipta entri masa daripada tab **Berkaitan** sumber boleh ditempah, entri masa tidak dicipta dengan betul untuk pengguna didaftar masuk dan bukannya sumber boleh ditempah induk.
- Medan baharu ditambahkan pada kotak dialog **Kelulusan pukal MDD**.

**Perancangan projek**

Isu berikut telah dibaiki:
- Prestasi penciptaan projek perlahan apabila templat waktu kerja projek digunakan dengan kalendar yang kompleks.
- Apabila tarikh mula lebih besar daripada tarikh tamat, ralat dipaparkan pada templat projek salinan disebabkan perbezaan dalam komponen masa setiap medan.

**Pengurusan sumber**

Isu berikut telah dibaiki:
- Parameter yang tidak betul digunakan dalam pertanyaan penggunaan sumber dan XML membawa kepada hasil penapis yang tidak betul pada grid **Penggunaan Sumber**.
- Pengesahan **Tempahan Lanjut** memaparkan tarikh tamat yang tidak betul untuk tempahan.

**Jualan**

Isu berikut telah dibaiki:
- Mesej ralat berlaku jika harga kategori dicipta dengan nilai yang tidak ditemui.
- Mesej ralat berlaku jika pencapaian baris kontrak dicipta tanpa baris pesanan.
