---
title: Kemajuan projek dan penggunaan kos
description: Topik ini memberikan maklumat tentang penjejakan kemajuan projek dan penggunaan kos.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
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
ms.openlocfilehash: 73b23aad2976c8ccbb542fc2dda1d96dd9f5714b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283649"
---
# <a name="project-progress-and-cost-consumption"></a>Kemajuan projek dan penggunaan kos

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Keperluan untuk menjejaki kemajuan terhadap jadual berbeza-beza mengikut industri. Sesetengah industri menjejaki pada tahap butiran, manakala industri lain menjejaki pada tahap yang lebih tinggi. Topik ini menunjukkan cara untuk menjadualkan bagi memenuhi keperluan organisasi anda.

## <a name="effort-tracking-view"></a>Pandangan penjejakan usaha

Pandangan **Penjejakan usaha** menjejaki kemajuan tugas dalam jadual. Ia membandingkan jam usaha sebenar yang dihabiskan pada satu tugas dengan jam usaha yang dirancang bagi tugas tersebut. Project Service Automation menggunakan formula berikut untuk mengira metrik penjejakan:

Di awal penciptaan tugas: Kos yang dirancang akan ditetapkan kepada Anggaran kos yang lengkap. Sebaik sahaja Sebenar direkodkan pada tugas, perkara berikut akan menjadi pengiraan pada pandangan Penjejakan untuk Usaha

- Peratusan kemajuan = Usaha sebenar yang dihabiskan sehingga kini ÷ Anggaran yang lengkap (EAC) 
- Anggaran untuk lengkap (ETC) = Anggaran yang lengkap (EAC) – Usaha sebenar dihabiskan sehingga kini 
- EAC = Usaha selebihnya + Usaha sebenar dihabiskan sehingga kini 
- Varians usaha yang diunjurkan = Usaha yang dirancang - EAC

Project Service Automation menunjukkan unjuran bagi varians usaha pada tugas. Jika EAC adalah lebih daripada usaha yang dirancang, tugas itu diunjurkan mengambil lebih banyak masa daripada yang dirancang pada asalnya. Oleh itu, ia lebih lewat daripada yang dijadualkan. Jika EAC kurang daripada usaha yang dirancang, tugas itu diunjurkan mengambil sedikit masa daripada yang dirancang pada asalnya. Oleh itu, ia lebih awal daripada yang dijadualkan.

## <a name="reprojecting-effort"></a>Usaha mengunjurkan semula

Ia adalah perkara biasa bagi pengurus projek untuk menyemak semula anggaran asal pada tugas. Unjuran semula projek ialah persepsi pengurus projek berkenaan anggaran, memandangkan keadaan projek semasa. Walau bagaimanapun, kami tidak mengesyorkan agar pengurus projek mengubah nombor garis dasar, kerana garis dasar projek mewakili sumber kebenaran yang sudah mantap bagi jadual dan anggaran kos projek, dan semua pemegang amanah projek telah bersetuju dengannya.

Terdapat dua cara pengurus projek boleh mengunjurkan semula usaha pada tugas:

- Ganti ETC lalai dengan anggaran baharu bagi usaha sebenar yang masih tinggal pada tugas. 
- Ganti peratusan kemajuan lalai dengan anggaran baharu bagi kemajuan sebenar tugas.

Setiap pendekatan ini menyebabkan pengiraan semula ETC, EAC dan peratusan kemajuan tugas, serta varians usaha yang diunjurkan pada tugas. EAC, ETC dan peratusan kemajuan pada tugas ringkasan juga dikira semula, dan menghasilkan unjuran baharu varians usaha.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Unjuran semula usaha pada tugas ringkasan

Usaha pada tugas ringkasan atau tugas bekas boleh diunjurkan semula. Tidak kira sama ada pengguna mengunjurkan semula dengan menggunakan usaha yang masih tinggal atau peratusan kemajuan pada tugas ringkasan, set pengiraan berikut bermula:

- EAC, ETC dan peratusan kemajuan pada tugas dikira.
- EAC yang baharu diagihkan sehingga ke tugas anak dalam perkadaran yang sama dengan EAC asal pada tugas tersebut.
- EAC baharu pada setiap tugas individu sehingga ke tugas nod daun dikira. 
- Tugas anak yang terjejas sehingga ke nod daun, ETC dan peratusan kemajuan ia dikira semula berdasarkan pada nilai EAC. Ini menghasilkan unjuran baharu bagi varians usaha tugas tersebut. 
- EAC tugas ringkasan sehingga ke nod akar dikira semula.

### <a name="cost-tracking-view"></a>Pandangan penjejakan kos 

Pandangan **Penjejakan kos** membandingkan kos sebenar yang dibelanjakan pada tugas dengan kos yang dirancang. 

> [!NOTE]
> Pandangan ini hanya menunjukkan kos buruh dan tidak termasuk kos daripada anggaran perbelanjaan. 

Project Service Automation menggunakan formula berikut untuk mengira metrik penjejakan:

Apabila tugas dicipta, kos yang dirancang sama dengan anggaran kos yang lengkap. Selepas sebenar direkodkan pada tugas, perkara berikut dikira pada pandangan **Penjejakan** untuk kos:

 - Peratusan kos yang digunakan = Kos sebenar yang dibelanjakan sehingga kini ÷ Anggaran kos yang lengkap untuk tugas
 - Kos untuk lengkap (CTC) = Anggaran kos yang lengkap – Kos sebenar yang dibelanjakan sehingga kini
 - Anggaran kos yang lengkap = Anggaran kos yang lengkap CTC + Kos sebenar yang dibelanjakan sehingga kini
 - Varians kos yang unjuran = Kos yang dirancang – Anggaran kos yang lengkap

Unjuran varians kos ditunjukkan pada tugas. Jika anggaran kos yang lengkap adalah lebih daripada kos yang dirancang, tugas itu diunjurkan menelan belanja lebih daripada yang dirancang pada asalnya. Oleh itu, ia akan berkembang melebihi belanjawan. Jika Anggaran kos yang lengkap adalah kurang daripada kos yang dirancang, tugas itu diunjurkan menelan belanja kurang daripada yang dirancang pada asalnya dan mengalir di bawah belanjawan.

## <a name="project-managers-reprojection-of-cost"></a>Unjuran semula kos pengurus projek

Apabila usaha diunjurkan semula, CTC, Anggaran kos yang lengkap, peratusan kos yang digunakan dan varians kos unjuran semuanya dikira semula dalam pandangan **Penjejakan kos**.

## <a name="project-status-summary"></a>Ringkasan status projek

Data penjejakan dalam pandangan **Penjejakan usaha** dan **Penjejakan kos** menunjukkan kemajuan dan penggunaan kos pada nod akar projek, tugas ringkasan dan tahap tugas nod daun. Bahagian **Status** pada halaman **Entiti projek** menunjukkan ringkasan status peringkat projek.

## <a name="status-summary-fields"></a>Medan ringkasan status

Medan **Status keseluruhan projek** ialah medan boleh diedit yang menunjukkan status keseluruhan projek. Ia menggunakan pengekodan warna, seperti hijau, kuning dan merah untuk menunjukkan peningkatan risiko. Medan **Komen** membolehkan pengurus projek memasukkan komen khusus tentang status. Medan **Status dikemas kini pada** tidak boleh diedit dan nilainya ialah cap masa yang menunjukkan masa status tersebut dikemas kini kali terakhir.

Medan **Prestasi jadual** dan **Prestasi kos** ditetapkan dari tarikh penjejakan. Apabila jadual dan varians kos untuk nod akar dalam pandangan **Penjejakan usaha** adalah positif, anda boleh menetapkan medan ini kepada **Di Hadapan.** Apabila jadual dan varians kos untuk nod akar adalah negatif, anda boleh menetapkan ia kepada **Di Belakang**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]