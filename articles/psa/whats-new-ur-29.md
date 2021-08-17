---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 29, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas Kini Project Service Automation 29, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 87f10d793f9edc055444a3cecea9ea709c1fd7ff7213d6cfaf6b3cbe83a6a5a6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985107"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 29, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365. Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan. Keluaran ini serasi dengan Dynamics 365 9.x. Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini. Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](/power-platform/admin/install-remove-preferred-solution).

Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 29. Versi ini mempunyai nombor binaan V3.10.47.7 dan secara amnya tersedia melalui kemas kini dengan sendiri pada Februari 2021.

## <a name="update-release-29"></a>Keluaran Kemas kini 29

### <a name="bug-fixes"></a>Pembetulan pepijat

**Masa dan Perbelanjaan**

Isu berikut telah dibaiki:

- Pengguna tidak dapat melihat waktu bekerja yang dilog pada hari tidak bekerja dalam grid entri masa.
- Entri perbelanjaan yang diluluskan boleh diedit pada grid.

**Pengurusan Projek**

Isu berikut telah dibaiki:

- Logik pengesahan tiada untuk memastikan waktu usaha tugasan sumber tidak boleh negatif.
- Tindakan tersuai, **AssignResourcesForTask** mengemas kini semua medan dan bukannya hanya medan yang berubah.
- Apabila menyalin projek dalam persekitaran dengan pasang masuk atau aliran kerja yang didaftarkan pada peristiwa **CreateProject**, atribut **msdyn_bulkgenerationstatus** tidak dikemas kini jika **CopyWBSToProject** gagal.
- Apabila anda mengembangkan kalendar projek, hari bekerja tidak diisih dalam susunan naik menyebabkan beberapa kemas kini tugas projek gagal.
- Mengubah Pengurus Projek pada projek sedia ada mencetuskan logik lalai unit organisasi.

**Jualan**

Isu berikut telah dibaiki:

- Tab **Prestasi Kontrak** pada halaman **Kontrak** gagal secara senyap semasa pengawalan apabila tiada baris kontrak wujud.