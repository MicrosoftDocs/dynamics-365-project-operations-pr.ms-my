---
title: Salin projek
description: Topik ini memberikan maklumat tentang menyalin projek dalam Operasi Projek Dynamics 365.
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 53c72e5fd680eb28128644788752368705440445
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131804"
---
# <a name="copy-a-project"></a>Salin projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Dengan Dynamics 365 Project Operations, anda boleh membina projek baharu secara pantas dengan memilih **Salin Projek** pada borang **Projek**. Untuk menyalin projek, buka projek yang anda mahu salin dan kemudian pilih **Salin projek**. Tindakan akan disalin:

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

Untuk maklumat tentang cara mengakses Salin Projek secara programatik, lihat [Membangun templat projek dengan Salin Projek](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]