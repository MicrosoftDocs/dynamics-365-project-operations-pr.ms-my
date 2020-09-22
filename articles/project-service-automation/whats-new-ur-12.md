---
title: Perkara baharu dalam Keluaran Kemas kini Project Service Automation 12, V3
description: Topik ini memberikan maklumat tentang perkara baharu dalam Keluaran Kemas kini Project Service Automation 12, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: af8dbfe3-7ce9-4374-9c03-17b2e1d6ac32
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 758717562c12a72848f1a874fa8b1171139ebb0c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753906"
---
# <a name="project-service-automation-v3-update-release-12"></a>Project Service Automation V3, Keluaran Kemas kini 12
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
