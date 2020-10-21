---
title: Salin projek
description: Topik ini memberikan maklumat tentang menyalin projek dalam Operasi Projek Dynamics 365.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908407"
---
# <a name="copy-a-project"></a>Salin projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Dengan operasi Projek Dynamics 365, anda boleh dengan cepat membina projek baru dengan menggunakan tindakan **Salin Projek** pada **Projek**. Untuk menyalin projek, pilih projek dan kemudian pilih **Salin**. Tindakan akan disalin:

- Sifat projek
- Struktur pecahan kerja
- Ahli pasukan projek
- Anggaran projek
- Anggaran perbelanjaan projek

## <a name="project-properties"></a>Sifat projek

Apabila projek disalin, nilai dalam medan berikut disalin:

- Nama
- Penerangan 
- Pelanggan
- Templat Kalendar
- Mata wang
- Unit Pengkontrakan
- Pengurus Projek
- Status
- Keseluruhan Status Projek
- Komen
- Anggaran
- Anggaran Tarikh Mula
- Tarikh Siap
- Usaha (Jam)
- Anggaran Kos Buruh
- Anggaran Kos Perbelanjaan

## <a name="work-breakdown-structure"></a>Struktur pecahan kerja

Apabila projek disalin, keseluruhan struktur pecahan kerja yang dimuatkan oleh sumber akan disalin. Sumber yang dinamakan digantikan dengan sumber yang generik. Jika sumber yang dinamakan tidak mempunyai masa kerja yang sama dengan sumber generik, jadual akan dikira semula dan tempoh tugas mungkin berubah.

## <a name="project-team-members"></a>Ahli pasukan projek

Apabila pasukan projek disalin daripada projek sumber, sumber generik akan disalin. Tugasan sumber generik juga dikekalkan sebagai mana ia di dalam projek sumber. Sumber yang dinamakan akan ditukar kepada ahli pasukan generik.

## <a name="estimates"></a>Anggaran

Apabila projek disalin, kedua-dua sumber dan anggaran had baris disalin daripada projek sumber.