---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 30, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Kemas kini Project Service Automation Keluaran 30, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 1169ee13c42e982cb30a40d92df660f8933786a9
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852877"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 30, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365. Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan. Keluaran ini serasi dengan Dynamics 365 9.x. Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini. Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 30. Versi ini mempunyai nombor binaan V3.10.51.61 dan secara amnya boleh didapati melalui kemas kini sendiri pada April 2021.

## <a name="update-release-30"></a>Keluaran Kemas kini 30

### <a name="bug-fixes"></a>Pembetulan pepijat

**Masa dan Perbelanjaan**

Isu berikut telah dibaiki:

- Ralat berlaku apabila anda mencipta dan menyimpan entri masa pada halaman **Cipta Pantas** jika medan **Peranan** dialih keluar.
- Penapis Entri Masa menggunakan operator penapis yang salah.
- Lembaran masa yang disalin tidak dipaparkan secara automatik apabila anda memilih **Salin Minggu** pada kawalan entri masa.

**Pengurusan Sumber**

Isu berikut telah dibaiki:

- Apabila anda melanjutkan tempahan, status tempahan ditugaskan kepada tempahan tetap adalah salah. Melanjutkan tempahan berkaitan status tempahan yang ditakrifkan sebagai **Terikat** dalam metadata persediaan tempahan.
- Apabila status tempahan yang sah tidak ditentukan, mesej ralat tidak disetempatkan dengan betul.

**Pengurusan Projek**

Isu berikut telah dibaiki:

- Projek tidak boleh dicipta dalam satu mata wang dan termasuk tugas berkaitan dalam mata wang lain.

**Jualan**

Isu berikut telah dibaiki:

- Apabila senarai harga disalin, harga tidak dikemas kini.
- Menutup sebut harga sebagai gagal dimenangi apabila butiran kos mempunyai nilai untuk asal.
- Pada entiti **Tugas Projek**, **Kos yang Dianggarkan** telah dinamakan semula kepada **Kos yang Dirancang (Asas)**.
- Pengecualian rujukan nol dijana apabila invois dicipta atau dipadamkan.
