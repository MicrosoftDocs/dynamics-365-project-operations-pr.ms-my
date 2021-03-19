---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 20, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas kini Project Service Automation 20, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: db416343ac9ac2591007e83be80493a48f9ae904
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280679"
---
# <a name="project-service-automation-update-release-20-v3"></a>Project Service Automation Keluaran Kemas kini 20, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365. Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan. Keluaran ini serasi dengan Dynamics 365 9.x. Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini. Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 20. Versi ini mempunyai nombor binaan V 3.10.31.37 dan secara amnya boleh didapati melalui kemas kini sendiri pada Jun 2020.

## <a name="update-release-20"></a>Keluaran Kemas kini 20

### <a name="bug-fixes"></a>Pembetulan pepijat

**Pengurusan Projek**

Isu berikut telah dibaiki:

- Mengimport ahli pasukan projek dengan kaedah peruntukan yang memerlukan masa untuk mendapatkan mesej ralat yang tidak jelas apabila masa yang ditentukan adalah sifar.
- Pengguna menerima ralat yang salah apabila bilangan maksimum aksara telah dimasukkan ke dalam medan **Perihalan** untuk tugas projek.
- Halaman **muat turun tambahan Microsoft Dynamics 365 Project Service Automation** dilencongkan ke halaman muat turun Bahasa Inggeris apabila tetapan bahasa pengguna ditetapkan kepada bahasa Jepun.
- Apabila ralat pelayan berlaku, label penyegerakan pada tab **Jadual** bagi borang **Projek** kadangkala kekal.
- Kemas kini tugas berlebihan dihantar kepada pelayan apabila tugas diubah suai.

**Sales**

Isu berikut telah dibaiki:

- Pada borang **Kontrak**, klik dua kali  **Cipta invois** mencipta dua invois untuk rekod aktual tunggal.
- Dalam Internet Explorer 11, pengguna tidak dapat mencipta entri perbelanjaan.
- Pembalikan Kos dan pembalikan Jualan yang Tidak Dibilkan adalah tidak berkaitan.
- Butang **Segar semula Aktual** pada borang **Projek** tidak menyegarkan semula **Tugas Masa Sebenar**.
- Pasang masuk **Plug-in PreValidateProjectTeamMemberCreate** boleh mencipta sumber boleh ditempah generik pendua apabila atribut **msdyn_isgenericresourceprojectscoped** ditetapkan kepada **Palsu**.
- **Mengira semula** kos boleh dituntut butiran baris sebut harga berdasarkan produk dan butiran baris kontrak.
- Dalam senario tertentu, pasang masuk **PostEstimateLineUpdate** memaparkan ralat teferi pengecualian yang tidak sah.
- Tempoh masa fasa pada **Carta Analisis Keuntungan** tidak padan dengan tempoh kos dalam garis sebut harga tetap baris butiran sebut harga.
- Unit dan unit nilai kumpulan tidak lalai dengan betul untuk kategori perbelanjaan pada **Butiran Baris Kontrak** dan borang **Butiran Baris Sebut Harga**.
- Senarai permit **Harga Kos Organisasi Unit** bertindih pada tarikh penguatkuasaan.
- Pengguna tidak dibenarkan untuk mengubah **OrgUnit** apabila jenis pesanan tidak berasaskan kerja kerana ia akan membawa kepada ralat pengecualian rujukan yang tidak sah.
- Apabila cuba untuk menavigasi dari borang **Butiran Baris Sebut Harga**, kembali ke tab **Sebut Harga**, borang menyegar semula dan memaparkan tab **Ringkasan**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]