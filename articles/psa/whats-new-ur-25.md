---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 25, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Kemas kini Project Service Automation Keluaran 25, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: aabee3fe755e33d2c0f01a96b6f53a68957bc041
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143774"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 25, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365. Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan. Keluaran ini serasi dengan Dynamics 365 9.x. Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini. Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Topik ini menyenaraikan ciri dan pembetulan yang baharu atau ditukar untuk Project Service Automation V3, Kemas Kini Keluaran 25. Versi ini mempunyai nombor binaan V 3.10.43.76 dan secara umumnya tersedia melalui kemas kini dengan sendiri pada Oktober 2020.

## <a name="update-release-25"></a>Keluaran Kemas kini 25

### <a name="bug-fixes"></a>Pembetulan pepijat

**Masa dan Perbelanjaan**

Isu berikut telah dibetulkan:

- Carta entri masa menunjukkan data tambahan berdasarkan terlalu besar tempoh masa yang diambil.

**Pengurusan Sumber**

Isu berikut telah dibetulkan:

- Menambahkan kod Package Deployer untuk melangkau import tampalan Universal Resource Scheduling jika tampalan versi lebih tinggi telah wujud.

**Pengurusan Projek**

Isu berikut telah dibaiki:

- Percanggahan pembundaran dan kadar pertukaran yang dibetulkan menyebabkan kos dirancang tidak betul dalam grid penjejakan projek.
- Sokong keupayaan untuk memaparkan dua atau beberapa grid yang bertindak balas pada borang **Projek**.
- Berikan pengesahan bagi menyelesaikan keupayaan untuk menugaskan tugas melepasi tarikh tamat kalendar, yang menyebabkan penugasan sumber gagal.
- Pengendalian ralat yang ditambah baik untuk menangani Pengecualian Rujukan Nol yang dijana daripada berikut:

    - Pasang masuk **PreValidateProjectTeamMemberCreate**
    - **PreValidateProjectTaskCreate** apabila tugas projek dicipta tanpa projek berkaitan
    - Pasang masuk **PreValidateProjectTeamMemberCreate**
    - Pasang masuk **PreValidateProjectTeamMemberCreate**
    - Pasang masuk **PreValidateProjectTaskDelete**

**Sales**

Isu berikut telah dibaiki:

- Pengendalian ralat yang ditambah baik untuk menangani Pengecualian Rujukan Nol yang dijana daripada **Projek Salinan: Anggaran Pengurusan HelperResource**.
- **Tidak bersedia diinvois** pada **Tunggakan Pengebilan Masa dan Bahan** tidak menjelaskan status pengebilan.
- Membetulkan butang **Harga** yang tersalah label pada tab **Harga Peranan** dan **Item Katalog**.
