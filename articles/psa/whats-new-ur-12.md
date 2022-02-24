---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 12, V3
description: Topik ini memberikan maklumat tentang perkara baharu dalam Keluaran Kemas kini Project Service Automation 12, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: daf0e6c7a4b1b953cb808cfefab74475c47d3996
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143839"
---
# <a name="project-service-automation-update-release-12-v3"></a>Project Service Automation, Keluaran Kemas kini 12, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami gembira untuk mengumumkan kemas kini terbaharu untuk aplikasi Dynamics 365 Project Service Automation (PSA). Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan. Keluaran ini serasi dengan Dynamics 365 9.x. Untuk mengemas kini kepada keluaran ini, lawati Pusat Pentadbir untuk Dynamics 365 online dan pergi ke halaman penyelesaian untuk memasang kemas kini. Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 12. Versi ini mempunyai nombor binaan V3.10.2.34 dan secara amnya boleh didapati melalui kemas kini kendiri pada Oktober 2019.

## <a name="update-release-12"></a>Keluaran Kemas kini 12

### <a name="bug-fixes"></a>Pembetulan pepijat

- Masa dan Perbelanjaan

    - Dibetulkan: Mesej ralat entri masa telah dikemas kini dengan konteks yang lebih berkaitan.
    - Dibetulkan: Grid entri masa dan jadual memaparkan bar skrol menegak dengan betul apabila diperlukan.
    - Dibetulkan: Perbelanjaan dan entri masa yang telah diserahkan boleh diluluskan.
    - Dibetulkan: Mesej dialog batalkan pengesahan kelulusan telah dibetulkan untuk menggambarkan status kelulusan apabila diubah daripada **Diluluskan** kepada **Diserahkan**.
    - Dibetulkan: Medan **Harga**, **Unit** dan **Kuantiti** kini dikunci pada rekod Perbelanjaan selepas ia telah diluluskan.

- Pengurusan Projek

    - Dibetulkan: Tindakan **Baharu** pada borang utama **Ahli pasukan** telah dialih keluar.
    - Dibetulkan: Penugasan sumber telah dikemas kini pada akaun untuk ralat pembundaran tidak tepat, yang membawa kepada anjakan dalam tarikh akhir tugas.
    - Dibetulkan: Dalam grid tugas, ralat bahagian pelayan yang berkaitan akan ditunjukkan kepada pengguna.
    - Dibetulkan: Nama ahli pasukan kini dipaparkan pada pemilih orang tugas dan bukannya nama kedudukan.

- Pengurusan Sumber

    - Dibetulkan: Butiran keperluan sumber untuk projek yang dicipta daripada templat kini menggunakan kalendar projek.
    - Dibetulkan: Kemahiran dan kecekapan kini lalai daripada data induk peranan kepada keperluan sumber yang dicipta untuk peranan tersebut.

- Sales

    - Dibetulkan: ID objek duplikasi ditemui pada borang utama **Kontrak**.
    - Dibetulkan: Logik telah dikemas kini untuk menjadikan tab **Analisis Sebut Harga** boleh dilihat supaya ia memaparkan persediaan metadata tab.
    - Dibetulkan: Tarikh perakaunan pada rekod sebenar kini datang daripada tarikh bagi tarikh entri masa/perbelanjaan dan bukan tarikh kelulusan.
