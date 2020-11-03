---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 20, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas kini Project Service Automation 20, V3
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 12edae76dbc6de63d3e2d36058c4092f80ede77d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081177"
---
# <a name="project-service-automation-update-release-20-v3"></a>Project Service Automation Keluaran Kemas kini 20, V3

Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365. Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan. Keluaran ini serasi dengan Dynamics 365 9.x. Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini. Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 20. Versi ini mempunyai nombor binaan V 3.10.31.37 dan secara amnya boleh didapati melalui kemas kini sendiri pada Jun 2020.

## <a name="update-release-20"></a>Keluaran Kemas kini 20

### <a name="bug-fixes"></a>Pembetulan pepijat

**Pengurusan Projek**

Isu berikut telah dibaiki:

- Mengimport ahli pasukan projek dengan kaedah peruntukan yang memerlukan masa untuk mendapatkan mesej ralat yang tidak jelas apabila masa yang ditentukan adalah sifar.
- Pengguna menerima ralat yang salah apabila bilangan maksimum aksara telah dimasukkan ke dalam medan **Perihalan** untuk tugas projek.
- **Muat turun pasang masuk Microsoft Dynamics 365 Project Service Automation** diarahkan semula ke halaman muat turun Bahasa Inggeris apabila tetapan bahasa pengguna ditetapkan kepada Bahasa Jepun.
- Apabila ralat pelayan berlaku, label penyegerakan pada tab **Jadual** bagi borang **Projek** kadangkala kekal.
- Kemas kini tugas berlebihan dihantar kepada pelayan apabila tugas diubah suai.

**Sales**

Isu berikut telah dibaiki:

- Pada borang **Kontrak** , klik dua kali  **Cipta invois** mencipta dua invois untuk rekod aktual tunggal.
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
- Apabila cuba untuk menavigasi dari borang **Butiran Baris Sebut Harga** , kembali ke tab **Sebut Harga** , borang menyegar semula dan memaparkan tab **Ringkasan**.