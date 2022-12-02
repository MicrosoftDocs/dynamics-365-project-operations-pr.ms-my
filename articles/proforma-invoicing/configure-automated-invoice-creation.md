---
title: Konfigurasi penciptaan invois automatik
description: Artikel ini menyediakan maklumat tentang cara mengkonfigurasi sistem untuk menjana invois secara automatik.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 273e00e7841c8a34e249e54a7d868034bc34a1f7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920623"
---
# <a name="configure-automatic-invoice-creation"></a>Konfigurasi penciptaan invois automatik

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_


Lengkapkan langkah berikut untuk mengkonfigurasi jalanan invois automatik dalam Dynamics 365 Project operations.

1. Pergi ke **Tetapan** > **Kerja kelompok**.
2. Cipta kerja kelompok dan namakannya **Project operations mencipta invois**. Nama kerja kelompok mesti termasuk perkataan perkataan "cipta invois."
3. Dalam medan **Jenis Kerja**, pilih **Tiada**. Secara lalai, **Kekerapan Harian** dan pilihan **Adalah Aktif** ditetapkan kepada **Ya**.
4. Pilih **Jalankan Aliran Kerja**. Dalam kotak dialog **Cari Rekod**, anda akan melihat tiga aliran tugas:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Pilih **ProcessRunCaller**, kemudian pilih **Tambah**.
6. Dalam kotak dialog seterusnya, pilih **OK**. Aliran tugas **Tidur** diikuti dengan aliran tugas **Proses**.

  > [!NOTE]
  > Anda juga boleh memilih **ProcessRunner** dalam langkah 5. Kemudian, apabila anda pilih **OK**, aliran tugas **Proses** diikuti oleh aliran kerja **Tidur**.

Aliran kerja **ProcessRunCaller** dan **ProcessRunner** mencipta invois. **ProcessRunCaller** memanggil **ProcessRunner**. **ProcessRunner** ialah aliran kerja yang sebenarnya mencipta invois. Ia merangkumi semua baris kontrak yang perlu dicipta invois, dan ia mencipta invois untuk baris tersebut. Untuk menentukan baris kontrak yang perlu dicipta invois, kerja dilihat pada tarikh jalanan invois untuk baris kontrak. Jika baris kontrak milik satu kontrak yang mempunyai tarikh jalanan invois sama, transaksi digabungkan ke dalam satu invois yang mempunyai dua baris invois. Jika tiada transaksi untuk dicipta invois, kerja melangkau penciptaan invois.

Selepas **ProcessRunner** selesai berjalan, ia memanggil **ProcessRunCaller**, memberikan masa akhir, dan ditutup. **ProcessRunCaller** kemudian memulakan pemasa yang berjalan 24 jam dari tarikh akhir khusus. Pada penghujung pemasa, **ProcessRunCaller** ditutup.

Kerja proses kelompok untuk mencipta invois adalah kerja berulang. Jika proses kelompok ini berjalan banyak kali, berbilang tika kerja dicipta dan menyebabkan ralat. Maka, anda perlu memulakan proses kelompol hanya satu kali, dan anda hendaklah mulakan semula jika ia berhenti berjalan.

> [!NOTE]
> Penginvoisan kelompok hanya berjalan untuk baris kontrak projek yang dikonfigurasikan oleh jadual invois. Baris kontrak dengan kaedah pengebilan harga tetap mesti mempunyai pencapaian yang dikonfigurasikan. Baris kontrak projek dengan kaedah pengebilan masa dan bahan akan memerlukan persediaan jadual invois berdasarkan tarikh. Perkara yang sama digunakan pada baris kontrak berasaskan projek.     


[!INCLUDE[footer-include](../includes/footer-banner.md)]