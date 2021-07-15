---
title: Penjejakan usaha projek
description: Topik ini menyediakan maklumat tentang cara menjejaki usaha projek dan kemajuan kerja.
author: ruhercul
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: 6fe381470326fc4000a9ed096b91fde56c045c38
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369207"
---
# <a name="project-effort-tracking"></a>Penjejakan usaha projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Keperluan untuk menjejaki kemajuan terhadap jadual berbeza-beza mengikut industri. Sesetengah industri menjejaki pada tahap berbutir, sedangkan industri yang lain menjejaki pada tahap yang lebih tinggi. Topik ini menunjukkan cara untuk menjadualkan bagi memenuhi keperluan organisasi anda.

## <a name="effort-tracking-view"></a>Pandangan penjejakan usaha

Pandangan **Penjejakan usaha** menjejaki kemajuan tugas dalam jadual dengan membandingkan jam usaha sebenar yang diluangkan pada tugas dengan jam usaha tugas yang dirancang. Dynamics 365 Project Operations menggunakan formula berikut untuk mengira metrik penjejakan:

- **Peratusan kemajuan**: Usaha sebenar diluangkan sehingga kini ÷ Anggaran ketika selesai (EAC) 
- **Baki Usaha**: Anggaran usaha ketika selesai – Usaha aktual dihabiskan sehingga kini 
- **EAC**: Usaha selebihnya + Usaha sebenar diluangkan sehingga kini 
- **Varians usaha yang diunjurkan**: Usaha dirancang – EAC

Project Operations menunjukkan unjuran varians usaha pada tugas. Jika EAC adalah lebih daripada usaha yang dirancang, tugas itu diunjurkan untuk mengambil masa yang lebih lama daripada yang dirancang pada asalnya dan di belakang jadual. Jika EAC adalah kurang daripada usaha yang dirancang, tugas itu diunjurkan untuk mengambil masa yang lebih pendek daripada yang dirancang pada asalnya dan mendahului jadual.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Usaha pengunjuran semula pada tugas nod daun

Pengurus projek sering meminda anggaran asal pada tugas. Unjuran semula projek ialah persepsi pengurus projek berkenaan anggaran, memandangkan keadaan projek semasa. Walau bagaimanapun, kami tidak mengesyorkan agar pengurus projek menukar nombor usaha yang dirancang. Ini kerana usaha yang dirancang projek itu mewakili sumber kebenaran yang mantap untuk jadual projek dan anggaran kos serta semua pemegang amanah projek telah bersetuju dengannya.

Pengurus projek boleh mengunjurkan semula usaha pada tugas dengan mengemas kini nilai lalai **Baki Usaha** dengan anggaran baharu pada tugas. Pengemaskinian ini menyebabkan pengiraan semula anggaran tugas ketika selesai (EAC), peratusan kemajuan dan varians usaha yang diunjurkan pada tugas. EAC, ETC dan peratusan kemajuan pada tugas ringkasan juga dikira semula dan menghasilkan unjuran varians usaha baharu.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Unjuran semula usaha pada tugas ringkasan

Usaha pada tugas ringkasan atau tugas bekas boleh diunjurkan semula. Pengurus projek boleh mengemas kini baki usaha pada tugas ringkasan. Mengemaskini baki usaha mencetuskan set pengiraan berikut dalam aplikasi:

- EAC dan peratusan kemajuan pada tugas dikira.
- EAC yang baharu diagihkan sehingga ke tugas anak dalam perkadaran yang sama dengan EAC asal pada tugas tersebut.
- EAC baharu pada setiap tugas individu sehingga ke tugas nod daun dikira. 
- Tugas anak yang terjejas sehingga nod daun, mempunyai baki usaha dan peratusan kemajuan dikira semula berdasarkan pada nilai EAC. Ini menghasilkan unjuran baharu bagi varians usaha tugas tersebut. 
- EAC tugas ringkasan sehingga ke nod akar dikira semula.


## <a name="project-status-summary"></a>Ringkasan status projek

Data penjejakan dalam pandangan **Penjejakan usaha** dan **Penjejakan kos** menunjukkan kemajuan dan penggunaan kos pada nod akar projek, tugas ringkasan dan tahap tugas nod daun. Bahagian **Status** pada halaman **Entiti projek** menunjukkan ringkasan status peringkat projek.

## <a name="status-summary-fields"></a>Medan ringkasan status

Medan **Status keseluruhan projek** ialah medan boleh diedit yang menunjukkan status keseluruhan projek. Ia menggunakan pengekodan warna, seperti hijau, kuning dan merah untuk menunjukkan peningkatan risiko. Medan **Komen** membolehkan pengurus projek memasukkan komen khusus tentang status. Medan **Status dikemas kini pada** tidak boleh diedit dan nilainya ialah cap masa yang menunjukkan masa status tersebut dikemas kini kali terakhir.

Medan **Prestasi jadual** dan **Prestasi kos** ditetapkan dari tarikh penjejakan. Apabila jadual dan varians kos untuk nod akar dalam pandangan **Penjejakan usaha** adalah positif, anda boleh menetapkan medan ini kepada **Di Hadapan.** Apabila jadual dan varians kos untuk nod akar adalah negatif, anda boleh menetapkan ia kepada **Di Belakang**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
