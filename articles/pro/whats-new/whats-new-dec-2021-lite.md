---
title: Apa yang baru Disember 2021 - Operasi Projek lite deployment
description: Topik ini menyediakan maklumat mengenai kemas kini kualiti yang tersedia dalam keluaran Disember 2021 Pelaksanaan Projek lite deployment.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0432e2d4970c352e91cca589987bbdace57c6eaf
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942988"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Apa yang baru Disember 2021 - Operasi Projek lite deployment

_Gunakan Pada: Pelaksanaan lite - urusan dengan invois proforma_

Topik ini digunakan pada komponen dan versi Microsoft Dynamics 365 Project Operations berikut:

- Operasi Projek dalam Dataverse versi persekitaran 4.27.0.195, 4.27.0.242


## <a name="features-included-in-this-release"></a>Ciri yang disertakan dalam keluaran ini

### <a name="subcontract-management"></a>Pengurusan subkontrak 

- [Ahli pasukan projek subkontrak](../subcontracting/subcontracting-project-team-members.md) : Pengurus projek boleh mencipta ahli pasukan yang dinamakan atau generik dengan subkontrak dan garis subkontrak untuk memberi kesan kepada kakitangan dan anggaran.
- [Pilihan subkontrak untuk ahli pasukan projek](../subcontracting/subcon-options.md) : Apabila membuat pilihan kakitangan untuk ahli pasukan projek yang dinamakan atau generik, pengurus projek boleh menyemak subkontrak sedia ada atau mencipta subkontrak baru untuk satu atau lebih ahli pasukan projek. 
- [Anggaran kos tugasan sumber subkontrak](../subcontracting/costing-subcon-ra.md) : Anggaran kos projek akan mengambil kira tugasan sumber subkontrak dan akan membebankan mereka menggunakan senarai harga pembelian yang berkaitan dengan subkontrak. 
- [Konfigurasikan Lembaga Jadual untuk menunjukkan pekerja kontrak dan kapasiti subkontrak](../subcontracting/configure-sb-subcon.md) : Papan jadual dalam Operasi Projek kini boleh dikonfigurasikan untuk mencari dan mencadangkan jenis pekerja kontrak sumber boleh ditempah dan kapasiti subkontrak bersama-sama dengan pekerja. Konfigurasi ini boleh digunakan semasa mencari sumber dalam konteks kakitangan untuk keperluan projek tertentu atau semasa mencari di luar konteks keperluan projek.
- [Kakitangan projek dengan pekerja kontrak dan kapasiti subkontrak:](../subcontracting/staffing-cw.md) Pekerja kontrak kini boleh ditempah pada projek yang memanfaatkan pengalaman lembaga jadual.
- [Masa rakaman, perbelanjaan, dan penggunaan bahan pada projek untuk komponen subkontrak:](../subcontracting/recording-subcon-actuals.md) Pekerja kontrak boleh merekodkan masa dan perbelanjaan, dan ahli pasukan projek juga boleh merekodkan penggunaan bahan yang dibeli menggunakan subkontrak pada projek. Ini akan menyebabkan merekodkan kos yang tepat pada projek yang menggunakan kapasiti atau bahan yang dibeli.
- [Peralihan negeri pada](../subcontracting/subcon-states.md) subkontrak : Subkontrak boleh disahkan untuk menyelesaikan rundingan dengan vendor, ditutup untuk menunjukkan penyelesaian penghantaran, atau dibatalkan untuk menunjukkan penamatan kontrak dengan vendor sebelum selesai penghantaran.

### <a name="task-planning"></a>Perancangan Tugas
- Penyelesaian masalah yang lebih baik untuk pentadbir sistem. Apabila pengguna tidak dapat membuka projek, pentadbir boleh menyemak semula ralat berkaitan bukan lesen yang dijana daripada Project for web dalam [log penjadualan Projek](../../project-management/schedule-api-logs.md).
- [Gunakan senarai semak tugas dalam Microsoft Project untuk web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). Dalam Microsoft Project untuk web, anda boleh menambah senarai semak pada tugas untuk menjejaki item tertentu.

## <a name="quality-updates"></a>Kemas kini kualiti

| **Bahagian ciri** | **Nombor rujukan** | **Kemas kini kualiti** |
| --- | --- | --- |
| Perancangan dan Penjejakan | 2392596 | Jadualkan API kini membenarkan pengemaskinian kepada **medan Usaha yang** tinggal, usaha **selesai**, dan % **Lengkap**. |
| Perancangan dan Penjejakan | 2478497 | Jadualkan **API Nombor aktiviti** dan medan ID Tugas boleh menjadi kosong pada input kerana sistem akan **mengisinya** menggunakan penomboran automatik.|
| Masa dan Perbelanjaan | 2468135 | Bilangan kelulusan dikurangkan daripada lima kepada tiga. |
| Masa dan Perbelanjaan | 2468188 | Tetapkan isu dengan teks log melebihi panjang maksimum dalam **atribut notetext** entiti **anotasi.** |
