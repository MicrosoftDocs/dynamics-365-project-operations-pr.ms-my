---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 17, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas kini Project Service Automation17, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 7ba685568692dafe117de42a71bb14d391cd7cc4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081184"
---
# <a name="project-service-automation-update-release-17-v3"></a>Project Service Automation, Keluaran Kemas kini 17, V3

Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365. Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan.  Keluaran ini serasi dengan Dynamics 365 9.x. Untuk mengemas kini kepada keluaran ini, lawati Pusat Pentadbir untuk Dynamics 365 online, halaman penyelesaian untuk memasang kemas kini. Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk PSA V3, Keluaran Kemas kini 17. Versi ini mempunyai nombor binaan V3.10.6.34 dan secara amnya tersedia melalui kemas kini kendiri pada Mac 2020.


## <a name="update-release-17"></a>Keluaran Kemas kini 17

### <a name="bug-fixes"></a>Pembetulan pepijat

**Umum**

- Dibetulkan: Kemas kini Project Service Automation untuk kuat kuasakan lesen Ahli Pasukan (Hab Sumber Projek akan menyertakan pelan Perkhidmatan Ahli Pasukan metadata 3.x)
 
**Masa dan Perbelanjaan**

- Dibetulkan: Tidak boleh mengubah anggaran perbelanjaan daripada harga bukan sifar kepada sifar (0). Perubahan diabaikan.

**Pengurusan Projek**

- Dibetulkan: Semakan untuk nilai nol telah ditambah pada nama kedudukan ahli pasukan.
- Dibetulkan: medan **msdyn_userresourceid** pada entiti **msdyn_resourceassignment** telah ditamatkan.
- Dibetulkan: Naik taraf daripada 2.x kepada 3.x kini mengendalikan kontur usaha kosong pada penugasan tugas.

**Sales**

- Dibetulkan: **Invois.PreValidateInvoiceUpdate** kini mengendalikan senario menugaskan semula pemilik rekod dengan betul.
- Dibetulkan: Apabila kelas transaksi ialah **Masa** , **UnitGroup** adalah tidak boleh diedit untuk semua entiti termasuk, **QuoteLineDetails** , **JournalLine** , **InvoiceLineDetail** , dan **ContractLineDetails.** Walau bagaimanapun, **Unit** adalah tidak boleh diedit hanya untuk **JournalLine** dan **InvoiceLineDetails**.

