---
title: Salin projek
description: Topik ini menyediakan maklumat tentang menyalin projek dalam Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479530"
---
# <a name="copy-a-project"></a>Salin projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Dengan Dynamics 365 Project Operations, anda boleh dengan cepat membina projek baru dengan memilih **Salin Projek** pada borang **Projek**. Untuk menyalin projek, buka projek yang anda mahu salin dan kemudian pilih **Salin projek**. Tindakan akan disalin:

- Sifat projek (Anggaran tarikh mula disalin daripada projek sumber)
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
