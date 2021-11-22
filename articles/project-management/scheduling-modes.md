---
title: Mod penjadualan
description: Topik ini memberikan maklumat tentang mod penjadualan.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 41e56d01c3cfa62558b10e178085a4408a0aadb023f3f7347a61d121f542bb08
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987762"
---
# <a name="scheduling-modes"></a>Mod penjadualan

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_


Dynamics 365 Project Operations menyediakan keupayaan untuk organisasi mentakrifkan cara mereka mengurus perubahan ke pemboleh ubah utama dalam tugas dalam struktur pecahan kerja. Berdasarkan pada keperluan khusus organisasi, Pengurus Projek boleh membuat perubahan pada mod penjadualan apabila projek dicipta.

Terdapat tiga mod penjadualan yang tersedia dalam Project Operations:

  - Tempoh tetap (ini adalah mod lalai)
  - Usaha ditetapkan (*Kerja*)
  - Unit ditetapkan

Nilai yang terjejas dengan definisi mod penjadualan tertentu ditentukan oleh formula berikut:

  Usaha = Tempoh x Unit

Apabila anda mentakrifkan mod penjadualan projek, anda menetapkan salah satu daripada nilai ini yang kemudian tidak boleh ditukar. Memegang nilai ini sebagai pemalar meletakkan keutamaan pada nilai itu yang memberitahu sistem untuk tidak mengubahnya apabila dua nilai lain berubah. Jadual berikut memberikan maklumat tentang kesan pemilihan mod tertentu.

| **Dalam tugas ini**             | **Jika anda menyemak semula unit**   | **Jika anda menyemak semula tempoh** | **Jika anda menyemak semula usaha**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Tugas unit tetap     | Tempoh dikira semula. | Usaha dikira semula.    | Tempoh dikira semula. |
| Tugas usaha tetap    | Tempoh dikira semula. | Unit dikira semula.    | Tempoh dikira semula. |
| Tugas tempoh tetap  | Usaha dikira semula.   | Usaha dikira semula.    | Unit dikira semula.   |

Untuk maklumat lanjut tentang implikasi mod diberikan, lihat [Tukar jenis tugas untuk penjadualan yang lebih tepat](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72). Dalam topik, istilah **Kerja** digunakan berbanding **Usaha**.

## <a name="change-the-organizations-scheduling-mode"></a>Tukar mod penjadualan organisasi

Lengkapkan langkah berikut untuk mentakrifkan mod penjadualan organisasi.

1. Pergi ke **Tetapan** \> **Umum** \> **Parameter** dan kemudian pilih parameter projek. 
2. Pada halaman **Parameter Projek**, pilih mod penjadualan lalai untuk organisasi dan kemudian takrifkan keupayaan untuk pengurus Projek mengganti tetapan apabila mencipta projek baharu.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>Tukar tetapan mod penjadualan pada projek

Jika organisasi membenarkan pengurus Projek mengganti mod penjadualan lalai, pengurus Projek boleh membuat perubahan itu apabila mereka mencipta projek baharu. Walau bagaimanapun selepas projek telah disimpan, mod penjadualan tidak boleh ditukar.

## <a name="copied-projects"></a>Projek disalin

Oleh kerana projek dicipta apabila salinan tindakan projek diambil, pengurus Projek tidak boleh menetapkan mod penjadualan. Projek destinasi akan sentiasa lalai dengan mod yang ditakrifkan pada peringkat organisasi.

## <a name="copied-tasks"></a>Tugas yang disalin

Apabila tugas disalin daripada satu projek ke yang lain, tugas mewarisi mod penjadualan projek destinasi.