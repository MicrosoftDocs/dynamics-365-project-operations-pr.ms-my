---
title: Gambaran keseluruhan penjejakan projek
description: Topik ini memberikan maklumat tentang cara untuk menjejaki kemajuan projek dan penggunaan kos.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f159ecac53b824ef208221bb14958923fb5da63b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127371"
---
# <a name="project-tracking-overview"></a>Gambaran keseluruhan penjejakan projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Keperluan untuk menjejaki kemajuan terhadap jadual berbeza-beza mengikut industri. Sesetengah industri menjejaki pada tahap berbutir, sedangkan industri yang lain menjejaki pada tahap yang lebih tinggi. Topik ini menunjukkan cara untuk menjadualkan bagi memenuhi keperluan organisasi anda.

## <a name="effort-tracking-view"></a>Pandangan penjejakan usaha

Pandangan **Penjejakan usaha** menjejaki kemajuan tugas dalam jadual dengan membandingkan jam usaha sebenar yang diluangkan pada tugas dengan jam usaha tugas yang dirancang. Dynamics 365 Project Operations menggunakan formula yang berikut untuk mengira metrik penjejakan:

- **Peratusan kemajuan**:  Usaha sebenar diluangkan sehingga kini ÷ Anggaran ketika selesai (EAC) 
- **Anggaran untuk selesai (ETC)**: Usaha dirancang – Usaha sebenar diluangkan sehingga kini 
- **EAC**: Usaha selebihnya + Usaha sebenar diluangkan sehingga kini 
- **Varians usaha yang diunjurkan**: Usaha dirancang – EAC

Project Operations menunjukkan unjuran varians usaha pada tugas. Jika EAC adalah lebih daripada usaha yang dirancang, tugas itu diunjurkan untuk mengambil masa yang lebih lama daripada yang dirancang pada asalnya dan di belakang jadual. Jika EAC adalah kurang daripada usaha yang dirancang, tugas itu diunjurkan untuk mengambil masa yang lebih pendek daripada yang dirancang pada asalnya dan mendahului jadual.

## <a name="reprojecting-effort"></a>Usaha mengunjurkan semula

Pengurus projek sering meminda anggaran asal pada tugas. Unjuran semula projek ialah persepsi pengurus projek berkenaan anggaran, memandangkan keadaan projek semasa. Walau bagaimanapun, kami tidak mengesyorkan pengurus projek mengubah nombor garis dasar. Ini adalah kerana garis dasar projek mewakili sumber kebenaran yang diwujudkan untuk jadual projek dan anggaran kos, dan semua pemegang saham projek telah bersetuju dengannya.

Terdapat dua cara pengurus projek boleh mengunjurkan semula usaha pada tugas:

- Ganti ETC lalai dengan anggaran baharu bagi usaha sebenar yang masih tinggal pada tugas. 
- Ganti peratusan kemajuan lalai dengan anggaran baharu bagi kemajuan sebenar tugas.

Setiap pendekatan menyebabkan pengiraan semula ETC, EAC, peratusan kemajuan tugas dan varians usaha yang diunjurkan pada tugas. EAC, ETC dan peratusan kemajuan pada tugas ringkasan juga dikira semula dan menghasilkan unjuran varians usaha baharu.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Unjuran semula usaha pada tugas ringkasan

Usaha pada tugas ringkasan atau tugas bekas boleh diunjurkan semula. Tidak kira sama ada pengguna mengunjurkan semula dengan menggunakan usaha yang masih tinggal atau peratusan kemajuan pada tugas ringkasan, set pengiraan berikut bermula:

- EAC, ETC dan peratusan kemajuan pada tugas dikira.
- EAC yang baharu diagihkan sehingga ke tugas anak dalam perkadaran yang sama dengan EAC asal pada tugas tersebut.
- EAC baharu pada setiap tugas individu sehingga ke tugas nod daun dikira. 
- Tugas anak yang terjejas sehingga ke nod daun, ETC dan peratusan kemajuan ia dikira semula berdasarkan pada nilai EAC. Ini menghasilkan unjuran baharu bagi varians usaha tugas tersebut. 
- EAC tugas ringkasan sehingga ke nod akar dikira semula.

### <a name="cost-tracking-view"></a>Pandangan penjejakan kos 

Pandangan **Penjejakan kos** membandingkan kos sebenar yang dibelanjakan pada tugas dengan kos yang dirancang pada tugas. 

> [!NOTE]
> Pandangan ini hanya menunjukkan kos buruh dan tidak termasuk kos daripada anggaran perbelanjaan. Project Operations menggunakan formula yang berikut untuk mengira metrik penjejakan:

- **Peratusan kos yang digunakan**: Kos sebenar dibelanjakan sehingga kini ÷ Anggaran kos ketika selesai
- **Kos untuk selesai (CTC)**: Kos dirancang – Kos sebenar dibelanjakan sehingga kini
- **EAC**: Kos selebihnya + Kos sebenar dibelanjakan sehingga kini
- **Varians kos yang diunjurkan**: Kos dirancang – EAC

Unjuran varians kos ditunjukkan pada tugas. Jika EAC adalah lebih daripada kos yang dirancang, tugas itu diunjurkan menelan belanja lebih daripada yang dirancang pada asalnya. Oleh itu, ia akan berkembang melebihi belanjawan. Jika EAC adalah kurang daripada kos yang dirancang, tugas itu diunjurkan menelan belanja kurang daripada yang dirancang pada asalnya. Oleh itu, ia berkembang di bawah belanjawan.

## <a name="project-managers-reprojection-of-cost"></a>Unjuran semula kos pengurus projek

Apabila usaha diunjurkan semula, CTC, EAC, peratusan kos yang digunakan dan varians kos unjuran semuanya dikira semula dalam pandangan **Penjejakan kos**.

## <a name="project-status-summary"></a>Ringkasan status projek

Data penjejakan dalam pandangan **Penjejakan usaha** dan **Penjejakan kos** menunjukkan kemajuan dan penggunaan kos pada nod akar projek, tugas ringkasan dan tahap tugas nod daun. Bahagian **Status** pada halaman **Entiti projek** menunjukkan ringkasan status peringkat projek.

## <a name="status-summary-fields"></a>Medan ringkasan status

Medan **Status keseluruhan projek** ialah medan boleh diedit yang menunjukkan status keseluruhan projek. Ia menggunakan pengekodan warna, seperti hijau, kuning dan merah untuk menunjukkan peningkatan risiko. Medan **Komen** membolehkan pengurus projek memasukkan komen khusus tentang status. Medan **Status dikemas kini pada** tidak boleh diedit dan nilainya ialah cap masa yang menunjukkan masa status tersebut dikemas kini kali terakhir.

Medan **Prestasi jadual** dan **Prestasi kos** ditetapkan dari tarikh penjejakan. Apabila jadual dan varians kos untuk nod akar dalam pandangan **Penjejakan usaha** adalah positif, anda boleh menetapkan medan ini kepada **Di Hadapan.** Apabila jadual dan varians kos untuk nod akar adalah negatif, anda boleh menetapkan ia kepada **Di Belakang**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]