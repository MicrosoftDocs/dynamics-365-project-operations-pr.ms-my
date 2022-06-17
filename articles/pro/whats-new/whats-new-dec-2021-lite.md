---
title: Apa yang baru Disember 2021 - Operasi Projek lite penggunaan
description: Artikel ini memberikan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran Disember 2021 pelaksanaan Project Operations lite.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 301acc5be76fb0318d6298820b62ae5bb05efac3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914091"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Apa yang baru Disember 2021 - Operasi Projek lite penggunaan

_Gunakan Pada: Pelaksanaan lite - urusan dengan invois proforma_

Artikel ini terpakai kepada komponen dan versi Microsoft Dynamics 365 Project Operations berikut :

- Operasi Projek dalam versi persekitaran 4.27.0.195, 4.27.0.242, 4.27.0.244 Dataverse


## <a name="features-included-in-this-release"></a>Ciri yang disertakan dalam keluaran ini

### <a name="subcontract-management"></a>Pengurusan subkontrak 

- [Ahli](../subcontracting/subcontracting-project-team-members.md) pasukan projek subkontrak: Pengurus projek boleh mencipta ahli pasukan bernama atau generik dengan subkontrak dan garis subkontrak untuk memberi kesan kepada kakitangan dan anggaran.
- [Pilihan subkontrak untuk ahli](../subcontracting/subcon-options.md) pasukan projek: Apabila membuat pilihan kakitangan untuk ahli pasukan projek bernama atau generik, pengurus projek boleh menyemak subkontrak sedia ada atau mencipta subkontrak baharu untuk satu atau lebih ahli pasukan projek. 
- [Anggaran kos tugasan](../subcontracting/costing-subcon-ra.md) sumber subkontrak: Anggaran kos projek akan mengambil kira tugasan sumber subkontrak dan akan membebankan mereka menggunakan senarai harga belian yang berkaitan dengan subkontrak. 
- [Konfigurasikan Papan Jadual untuk menunjukkan pekerja kontrak dan kapasiti](../subcontracting/configure-sb-subcon.md) subkontrak: Papan jadual dalam Operasi Projek kini boleh dikonfigurasikan untuk mencari dan mencadangkan pekerja kontrak jenis sumber yang boleh ditempah dan kapasiti subkontrak bersama dengan pekerja. Konfigurasi ini boleh digunakan apabila mencari sumber dalam konteks kakitangan untuk keperluan projek tertentu atau apabila mencari di luar konteks keperluan projek.
- [Kakitangan projek dengan pekerja kontrak dan kapasiti](../subcontracting/staffing-cw.md) subkontrak: Pekerja kontrak kini boleh ditempah pada projek yang memanfaatkan pengalaman papan jadual.
- [Merakam masa, perbelanjaan, dan penggunaan bahan pada projek untuk komponen](../subcontracting/recording-subcon-actuals.md) subkontrak: Pekerja kontrak boleh merekodkan masa dan perbelanjaan, dan ahli pasukan projek juga boleh merekodkan penggunaan bahan yang dibeli menggunakan subkontrak pada projek. Ini akan menghasilkan rakaman kos yang tepat pada projek yang menggunakan kapasiti atau bahan yang dibeli.
- [Peralihan negeri pada subkontrak](../subcontracting/subcon-states.md): Subkontrak boleh disahkan untuk menyelesaikan rundingan dengan vendor, ditutup untuk menunjukkan penyelesaian penghantaran, atau dibatalkan untuk menunjukkan penamatan kontrak dengan vendor sebelum selesai penghantaran.

### <a name="task-planning"></a>Perancangan Tugas
- Penyelesaian masalah yang lebih baik untuk pentadbir sistem. Apabila pengguna tidak dapat membuka projek, pentadbir boleh menyemak ralat berkaitan bukan lesen yang dijana daripada Project for the web dalam [log](../../project-management/schedule-api-logs.md) penjadualan Projek.
- [Gunakan senarai semak tugas dalam Microsoft Project untuk web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). Dalam Microsoft Project untuk web, anda boleh menambah senarai semak pada tugas untuk menjejaki item tertentu.

## <a name="quality-updates"></a>Kemas kini kualiti

| **Bahagian ciri** | **Nombor rujukan** | **Kemas kini kualiti** |
| --- | --- | --- |
| Perancangan dan Penjejakan | 2392596 | Jadualkan API kini kini kepada medan Usaha yang **tinggal**, **Usaha selesai** dan **% Lengkap**. |
| Perancangan dan Penjejakan | 2478497 | Jadualkan API **Nombor** aktiviti dan **medan ID** Tugas boleh kosong pada input kerana sistem akan mengisinya menggunakan penomboran automatik.|
| Masa dan Perbelanjaan | 2468135 | Bilangan percubaan kelulusan dikurangkan daripada lima kepada tiga. |
| Masa dan Perbelanjaan | 2468188 | Betulkan isu dengan teks log melebihi panjang maksimum dalam **atribut** teks **nota entiti anotasi**. |
