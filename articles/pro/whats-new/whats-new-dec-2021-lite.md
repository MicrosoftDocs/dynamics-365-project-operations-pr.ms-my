---
title: Perkara baharu Disember 2021 - Pelaksanaan Project Operations lite
description: Artikel ini memberikan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran Disember 2021 bagi pelaksanaan Project Operations lite.
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
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Perkara baharu Disember 2021 - Pelaksanaan Project Operations lite

_Gunakan Pada: Pelaksanaan lite - urusan dengan invois proforma_

Artikel ini digunakan pada komponen dan versi Microsoft Dynamics 365 Project Operations berikut:

- Project Operations dalam persekitaran Dataverse versi 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Ciri yang disertakan dalam keluaran ini

### <a name="subcontract-management"></a>Pengurusan subkontrak 

- [Membuat subkontrak bagi ahli pasukan projek](../subcontracting/subcontracting-project-team-members.md): Pengurus projek boleh mencipta ahli pasukan bernama atau generik dengan subkontrak dan baris subkontrak baris untuk memberikan kesan pada pengambilan kakitangan dan anggaran.
- [Pilihan membuat subkontrak bagi ahli pasukan projek](../subcontracting/subcon-options.md): Apabila membuat pilihan pengambilan kakitangan untuk ahli pasukan bernama atau generik, pengurus projek boleh menyemak subkontrak sedia ada atau mencipta subkontrak baharu untuk satu atau lebih ahli pasukan projek. 
- [Anggaran kos tugas sumber subkontrak](../subcontracting/costing-subcon-ra.md): Anggaran kos projek akan mengambil kira tugas sumber subkontrak dan akan dikira kosnya menggunakan senarai harga pembelian yang berkaitan dengan subkontrak. 
- [Konfigurasi Papan Jadual untuk menunjukkan kapasiti pekerja kontrak dan subkontrak](../subcontracting/configure-sb-subcon.md): Papan jadual dalam Project Operations kini boleh dikonfigurasikan untuk mencari dan mencadangkan jenis pekerja kontrak kapasiti sumber boleh ditempah dan subkontrak bersama dengan pekerja. Konfigurasi ini boleh digunakan apabila mencari sumber dalam konteks pengambilan kakitangan untuk keperluan projek tertentu atau semasa mencari di luar konteks keperluan projek.
- [Pengambilan kakitangan projek dengan kapasiti pekerja kontrak dan subkontrak](../subcontracting/staffing-cw.md): Pekerja kontrak kini boleh ditempah untuk projek yang memanfaatkan pengalaman papan jadual.
- [Merekod masa, perbelanjaan dan penggunaan bahan ke atas projek untuk komponen subkontrak](../subcontracting/recording-subcon-actuals.md): Pekerja kontrak boleh merekodkan masa dan perbelanjaan dan ahli pasukan projek juga boleh merekodkan penggunaan bahan yang dibeli menggunakan subkontrak pada projek. Ini akan menyebabkan rekod kos yang tepat ke atas projek yang menggunakan kapasiti atau bahan yang dibeli.
- [Peralihan keadaan pada subkontrak](../subcontracting/subcon-states.md) : Subkontrak boleh disahkan untuk melengkapkan rundingan dengan vendor, ditutup untuk menunjukkan penyelesaian penghantaran, atau dibatalkan untuk menunjukkan penamatan kontrak dengan vendor sebelum penyelesaian penghantaran.

### <a name="task-planning"></a>Perancangan Tugas
- Penyelesaian masalah ditambah baik untuk pentadbir sistem. Apabila pengguna tidak dapat membuka projek, pentadbir boleh menyemak ralat yang tidak berkaitan dengan lesen yang dijana daripada Project for the web dalam [Log penjadualan projek](../../project-management/schedule-api-logs.md).
- [Gunakan senarai semak tugas dalam Microsoft Project for the web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). Dalam Microsoft Project for the web, anda boleh menambahkan senarai semak pada tugas untuk menjejaki item khusus.

## <a name="quality-updates"></a>Kemas kini kualiti

| **Bahagian ciri** | **Nombor rujukan** | **Kemas kini kualiti** |
| --- | --- | --- |
| Perancangan dan Penjejakan | 2392596 | Jadualkan API sekarang akan membolehkan kemas kini untuk medan **Baki usaha**, **Usaha selesai**, dan **% Selesai**. |
| Perancangan dan Penjejakan | 2478497 | Medan **Nombor aktiviti** dan **ID Tugas** API Jadual boleh dibiarkan kosong pada input kerana sistem akan mengisi maklumat itu menggunakan penomboran automatik.|
| Masa dan Perbelanjaan | 2468135 | Bilangan cubaan semula kelulusan telah dikurangkan daripada lima kepada tiga. |
| Masa dan Perbelanjaan | 2468188 | Memperbaiki isu dengan teks log yang melebihi panjang maksimum dalam atribut **notetext** **anotasi**. |
