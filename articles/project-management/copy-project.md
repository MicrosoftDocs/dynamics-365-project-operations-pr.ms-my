---
title: Salin projek
description: Topik ini menyediakan maklumat tentang menyalin projek dalam Dynamics 365 Project Operations.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e9b637d2d282d123dfacb8a295292ea06549aa1e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574441"
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
- Senarai semak projek
- Baldi projek

## <a name="project-properties"></a>Sifat projek

Apabila projek disalin, nilai dalam medan berikut disalin.

| Medan | Operasi Projek Bahan Tidak Berstok | Operasi Projek Lite | Projek untuk Web |
|-------|------------------------------------------|-------------------------|---------------------|
| Nama | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Description | :heavy_check_mark: | :heavy_check_mark: | |
| Dihormati | :heavy_check_mark: | :heavy_check_mark: | |
| Templat Kalendar | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Mata Wang | :heavy_check_mark: | :heavy_check_mark: | |
| Unit Pengkontrakan | :heavy_check_mark: | :heavy_check_mark: | |
| Syarikat Pemilikan | :heavy_check_mark: | | |
| Pengurus Projek | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Status | :heavy_check_mark: | :heavy_check_mark: | |
| Keseluruhan Status Projek | :heavy_check_mark: | :heavy_check_mark: | |
| Komen | :heavy_check_mark: | :heavy_check_mark: | |
| Anggaran | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Anggaran Tarikh Mula</p><p><strong>Nota:</strong> Medan ini menentukan tarikh projek dicipta daripada salinan. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Anggaran Tarikh Selesai</p><p><strong>Nota:</strong> Tarikh dalam medan ini dilaraskan berdasarkan tarikh mula projek baru yang dibuat daripada salinan.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| Usaha (Jam) | :heavy_check_mark: | :heavy_check_mark: | |
| Kos Buruh yang Dianggarkan | :heavy_check_mark: | :heavy_check_mark: | |
| Kos Perbelanjaan yang Dianggarkan | :heavy_check_mark: | :heavy_check_mark: | |
| Kos Bahan yang Dianggarkan | | :heavy_check_mark: | |

> [!NOTE]
> Salin projek adalah operasi yang panjang berjalan. Rekod projek, atribut yang berkaitan dan banyak entiti berkaitan juga boleh disalin. Disebabkan oleh sifat jangka panjang operasi, selepas salinan dimulakan, halaman projek sasaran dikunci untuk pengeditan sehingga operasi salinan selesai.

## <a name="work-breakdown-structure"></a>Struktur pecahan kerja

Apabila projek disalin, keseluruhan struktur pecahan kerja yang dimuatkan oleh sumber akan disalin. Sumber yang dinamakan digantikan dengan sumber yang generik. Jika sumber yang dinamakan tidak mempunyai waktu kerja yang sama dengan sumber generik, jadual akan dikira semula dan tempoh tugas mungkin berubah.

## <a name="project-team-members"></a>Ahli pasukan projek

Apabila pasukan projek disalin daripada projek sumber, sumber generik akan disalin. Tugasan sumber generik juga dikekalkan sebagai mana ia di dalam projek sumber. Sumber yang dinamakan akan ditukar kepada ahli pasukan generik.

> [!NOTE]
> Ahli pasukan dan tugasan tidak disalin dalam Project untuk Web.

## <a name="estimates"></a>Anggaran

Apabila projek disalin, sumber, perbelanjaan dan baris anggaran bahan akan disalin daripada projek sumber. 

Untuk maklumat tentang cara mengakses Salin Projek secara programatik, lihat [Membangun templat projek dengan Salin Projek](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Sebut harga dan kontrak

Sebut harga dan kontrak tidak dikaitkan dengan projek destinasi.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
