---
title: Urus zon waktu
description: Apabila projek dicipta, zon masa adalah berdasarkan zon waktu yang ditakrifkan dalam templat jam kerja yang digunakan.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c3feb05e1b2e81add1b0df886a5a69ced229eb72
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578535"
---
# <a name="manage-time-zones"></a>Urus zon waktu

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_


## <a name="projects"></a>Projek

Apabila projek dicipta, zon masa adalah berdasarkan pada zon waktu yang ditakrifkan dalam templat jam kerja yang digunakan. Pada **Projek** itu, tarikh sentiasa relatif kepada zon masa pengguna yang dilog masuk pada setiap tab, kecuali tab **Tugas**. Apabila anda melihat struktur pecahan kerja, tarikh akan sentiasa dipaparkan dalam zon waktu projek.

## <a name="tasks"></a>Tugas

Apabila tugas dicipta, masa mula, masa tamat dan jam/hari dikawal oleh waktu kerja projek. Contohnya, jika tugas dicipta dengan projek yang zon masa adalah -8 PST dan mempunyai waktu kerja berikut: 9:00 PAGI hingga 5:00 PETANG Isnin hingga Jumaat, sebarang tugas yang dicipta tanpa sebarang penugasan akan mengikut masa mula dan masa akhir kalendar projek.

## <a name="manage-resources-with-time-zones"></a>Urus sumber dengan zon masa

Untuk keputusan yang tepat dan boleh diramal apabila menggunakan **Penempahan Lanjutan**, terdapat dua syarat utama yang mesti dipatuhi:  

- Pengguna mesti mengkonfigurasi zon masa peranti mereka untuk dipadankan dengan zon waktu yang ditakrifkan dalam **Tetapan Peribadi** sistem.
 
  ![Tetapan zon waktu dalam Windows 10.](media/reconcile-assignments-03.png)

  ![Tetapan zon waktu dalam tetapan pemperibadian.](media/reconcile-assignments-04.png)
 
- Sumber boleh ditempah mesti mempunyai sekurang-kurangnya satu minit daripada masa kerja yang bertindih dengan kontur yang digunakan untuk mentakrifkan sambungan yang diminta. Contohnya, sumber yang berikut dengan waktu bekerja yang jatuh antara 9:00 PAGI dan 7:00 MALAM. 

  ![Perbandingan kontur sumber.](media/reconcile-assignments-05.png)

Jadual berikut menunjukkan:

- Templat kalendar projek
- Sumber A: Sumber ini mempunyai kalendar yang sama dan berada dalam zon waktu yang sama seperti projek. Masa mula tempahan ialah 9:00 PG.
- Sumber B: Sumber ini terletak dalam zon waktu yang berbeza daripada projek dan bermula pada 7:00 PAGI dalam zon waktu mereka. Walau bagaimanapun, tempahan akan bermula pada 9:00 PG kerana itu adalah masa mula paling awal kontur tugasan.
- Sumber C dan D: Sumber yang terletak dalam zon masa berbeza, kedua-duanya berbeza antara satu sama lain dan projek, dan penempahan mereka bermula tidak lebih awal daripada masa tersedia mereka.

|EntitI  |Kalendar  |
|-|-|
|Templat kalendar projek   | ![kalendar projek.](media/reconcile-assignments-06.png) |
|Sumber A  | ![Kalendar Sumber A.](media/reconcile-assignments-06.png) |
|Sumber B  |  ![Kalendar Sumber B.](media/reconcile-assignments-07.png) |
|Sumber C  |  ![Kalendar Sumber C.](media/reconcile-assignments-08.png) |
|Sumber D  | ![Kalendar Sumber D.](media/reconcile-assignments-09.png)  |
 
Apabila anda menavigasi ke pandangan **Penyelarasan**, tugasan sumber dan kekurangan penempahan yang berkaitan dipaparkan.

![Pandangan penyelarasan sebelum lanjutan.](media/reconcile-assignments-10.png)

Selepas fungsi penempahan lanjutan telah digunakan untuk setiap sumber, penempahan berjaya dilanjutkan untuk setiap sumber kerana setiap jam kerja yang bertindih dengan kekurangan kontur.

![Pandangan penyelarasan selepas lanjutan tempahan.](media/reconcile-assignments-11.png) 

Perhatikan bahawa pandangan lebih dekat pada butiran daripada penempahan Tempahan menunjukkan perbezaan dalam masa mula penempahan. Penempahan mula tidak lebih awal daripada masa mula penugasan kontur dan tidak akan lebih awal daripada masa mula sumber yang tersedia.

![Tempahan baharu sumber dalam papan jadual.](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]