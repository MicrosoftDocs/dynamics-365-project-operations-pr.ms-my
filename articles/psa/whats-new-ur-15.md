---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 15, V3
description: Topik ini memberikan maklumat tentang perkara baharu dalam Keluaran Kemas kini Project Service Automation 15, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 26b9ee0a6ff1ad81d6c77a6a7091733667c493ff
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585159"
---
# <a name="project-service-automation-update-release-15-v3"></a>Project Service Automation, Keluaran Kemas kini 15, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami gembira untuk mengumumkan kemas kini terbaharu untuk aplikasi Dynamics 365 Project Service Automation (PSA). Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan. Keluaran ini serasi dengan Dynamics 365 9.x. Untuk mengemas kini kepada keluaran ini, lawati Pusat Pentadbir untuk Dynamics 365 online dan pergi ke halaman penyelesaian untuk memasang kemas kini. Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](/power-platform/admin/install-remove-preferred-solution).

Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk PSA V3, Keluaran Kemas kini 15. Versi ini mempunyai nombor binaan V3.10.5.28 dan secara amnya boleh didapati melalui kemas kini kendiri pada Januari 2020.

## <a name="update-release-15"></a>Keluaran Kemas kini 15 

### <a name="enhancements"></a>Peningkatan

- Pengurusan Projek

### <a name="bug-fixes"></a>Pembetulan pepijat

- Masa dan Perbelanjaan

  - Dibetulkan: Tambah pengendalian ralat ketika memuat dalam pandangan penyesuaian.
  - Dibetulkan: Hab Sumber Projek: Namakan semula **Jumlah** untuk mengurangkan kekaburan.
  - Dibetulkan: Laraskan pandangan **Salin Lajur Entri Masa** untuk memasukkan jenis.
  - Dibetulkan: Pengeditan tempoh entri masa dalam pandangan grid menggunakan nombor perpuluhan menyebabkan ralat tidak diketahui bagi beberapa nombor.

- Pengurusan Projek

  - Dibetulkan: Menu ke bawah untuk **Gunakan dalam Pandangan Penjejakan** kini mengembang berdasarkan lebar pilihan.
  - Dibetulkan: Apabila menguruskan projek dalam zon masa +13, pengiraan tugas boleh memaparkan keputusan yang tidak tepat.
  - Dibetulkan: **Masa Tamat Ahli Pasukan** telah dibetulkan apabila menggunakan kalendar 24 jam.
  - Dibetulkan: Aktifkan semula **BPF** dalam borang utama **msdyn_project**.
  - Dibetulkan: Pengiraan tugasan tidak lagi mengabaikan satu hari.
  - Dibetulkan: Sepanduk pemberitahuan baharu telah ditambah kepada borang projek apabila zon waktu berbeza antara pengguna dan projek.

- Sales

  - Dibetulkan: Carian kategori anggaran perbelanjaan boleh digunakan untuk menapis pendua.
  - Dibetulkan: Kod dalam **PluginDomain. ExecuteInTryCatchBlock (..)** tidak lagi menyembunyikan asal pengecualian.
  - Dibetulkan: Tidak lagi mendapat mesej ralat dalam **Carian projek** dalam borang **Baris Sebut Harga** apabila terdapat lebih daripada 1000 projek.
  - Dibetulkan: Grid **Anggaran** untuk anggaran pekerja dan anggaran perbelanjaan kini memaparkan simbol mata wang yang betul.
  - Dibetulkan: Selepas organisasi mengemas kini PSA daripada Keluaran Kemas kini 14 kepada Keluaran Kemas kini 15, tab **Jadual** tidak lagi muncul sebagai kosong pada borang **Projek**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
