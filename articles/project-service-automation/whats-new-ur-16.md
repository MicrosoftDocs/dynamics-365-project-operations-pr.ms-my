---
title: Perkara baharu dalam Keluaran Kemas kini Project Service Automation 16, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas kini Project Service Automation16, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: b890a7b6-1664-4812-8732-fed77653cc05
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 0f4c206fd5b7a36d940e966b28c2437525812a98
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753902"
---
# <a name="project-service-automation-v3-update-release-16"></a>Project Service Automation V3, Keluaran Kemas kini 16
Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365. Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan.

Keluaran ini serasi dengan Dynamics 365 9.x. Untuk mengemas kini kepada keluaran ini, lawati Pusat Pentadbir untuk Dynamics 365 online, halaman penyelesaian untuk memasang kemas kini. Untuk maklumat lanjut, lihat [Pasang, Kemas kini Penyelesaian Pilihan](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page). Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk PSA V3, Keluaran Kemas kini 16. Versi ini mempunyai nombor bina V3.10.6.34 dan secara amnya boleh didapati melalui kemas kini kendiri pada Januari 2020

## <a name="update-release-16"></a>Keluaran Kemas kini 16

### <a name="bug-fixes"></a>Pembetulan pepijat

-   Masa dan Perbelanjaan

    -   Dibetulkan: Pengguna yang cuba menyerahkan entri masa dan perbelanjaan yang dipadamkan untuk kelulusan kini akan menerima mesej ralat yang berkenaan.

-   Pengurusan Projek

    -   Dibetulkan: Unit sumber yang ditakrifkan untuk ahli pasukan dalam templat yang diambil kira dengan templat digunakan untuk projek baharu.

    -   Dibetulkan: Pengendalian yang dipertingkatkan terhadap penyerahan semula pemilikan rekod.

    -   Dibetulkan: Projek yang sedang dalam proses disalin tidak akan dibenarkan untuk disalin sehingga semua operasi salinan selesai.

-   Pengurusan Sumber

    -   Dibetulkan: Melanjutkan tempahan kini mengendalikan jangka masa pendek dengan betul dan tidak lagi menghasilkan jam sifar untuk tempahan yang dilanjutkan.

    -   Dibetulkan: Pandangan penyesuaian kini sedang dipaparkan apabila zon waktu projek ialah +5:30 GMT dan masa pengguna berbeza.

-   Sales

    -   Dibetulkan: Apabila projek dipetakan ke baris kontrak dialih keluar dan projek baru dipetakan, rekod sebenar pada projek baharu tidak dinilai semula berdasarkan peraturan pengebilan dan penetapan harga yang ditakrifkan dalam baris kontrak. Ini telah dibetulkan dalam keluaran ini. Penetapan harga dan rekod sebenar projek yang baru dipetakan akan diterbalikkan dan diciptakan semula dengan betul berdasarkan penetapan harga dan pengebilan baris kontrak. Rekod sebenar projek yang tidak dipetakan juga akan dinilai semula dan dicipta semula sebagai hasilnya.

    -   Dibetulkan: Pengesahan tambahan telah ditambahkan pada medan baris anggaran **Jumlah** untuk memastikan bahawa nilai nol tidak akan diteruskan.

    -   Dibetulkan: Apabila aktual telah dikemas kini pada projek, butang segar semula telah ditambah pada borang utama projek untuk membolehkan pengguna menyegerakkan semula aktual.

    -   Dibetulkan: Apabila pengguna menaik taraf daripada 2.X kepada 3.X, projek dengan nilai NOL untuk nama projek akan dibenarkan.

