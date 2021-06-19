---
title: Salin projek
description: Topik ini menyediakan maklumat tentang menyalin projek dalam Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091265"
---
# <a name="copy-a-project"></a>Salin projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Dengan Dynamics 365 Project Operations, anda boleh dengan cepat membina projek baru dengan memilih **Salin Projek** pada borang **Projek**. Untuk menyalin projek, buka projek yang anda mahu salin dan kemudian pilih **Salin projek**. Tindakan akan menyalin yang berikut:

- Sifat projek 
- Struktur pecahan kerja
- Ahli pasukan projek
- Anggaran projek
- Anggaran perbelanjaan projek
- Anggaran bahan projek

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
- Anggaran Tarikh Mula: Ini ialah tarikh projek yang dicipta daripada salinan.
- Anggaran Tarikh Tamat: Tarikh ini dilaraskan berdasarkan tarikh mula projek baharu yang telah dibuat daripada salinan.
- Usaha (Jam)
- Kos Buruh yang Dianggarkan
- Kos Perbelanjaan yang Dianggarkan
- Kos Bahan yang Dianggarkan

> [!NOTE]
> Salin projek adalah operasi yang panjang berjalan. Rekod projek, atribut yang berkaitan dan banyak entiti berkaitan juga boleh disalin. Disebabkan oleh sifat jangka panjang operasi, selepas salinan dimulakan, halaman projek sasaran dikunci untuk pengeditan sehingga operasi salinan selesai.

## <a name="work-breakdown-structure"></a>Struktur pecahan kerja

Apabila projek disalin, keseluruhan struktur pecahan kerja yang dimuatkan oleh sumber akan disalin. Sumber yang dinamakan digantikan dengan sumber yang generik. Jika sumber yang dinamakan tidak mempunyai masa kerja yang sama dengan sumber generik, jadual akan dikira semula dan tempoh tugas mungkin berubah.

## <a name="project-team-members"></a>Ahli pasukan projek

Apabila pasukan projek disalin daripada projek sumber, sumber generik akan disalin. Tugasan sumber generik juga dikekalkan sebagai mana ia di dalam projek sumber. Sumber yang dinamakan akan ditukar kepada ahli pasukan generik.

## <a name="estimates"></a>Anggaran

Apabila projek disalin, sumber, perbelanjaan dan baris anggaran bahan akan disalin daripada projek sumber. 

Untuk maklumat tentang cara mengakses Salin Projek secara programatik, lihat [Membangun templat projek dengan Salin Projek](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
