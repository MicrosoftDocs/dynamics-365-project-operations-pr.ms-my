---
title: Peralihan keadaan pada invois vendor
description: Artikel ini menerangkan peralihan keadaan pada invois vendor dalam Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e25e4d63d4c9098112a7f40abe60c7184018d582
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261028"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Peralihan keadaan pada invois vendor

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Artikel ini menerangkan peralihan keadaan pada invois vendor dalam Microsoft Dynamics 365 Project Operations. Negeri-negeri berikut digunakan: **Draf**, **Dalam semakan**, **Disahkan**, **Ditahan** dan **Dibatalkan**.

Ilustrasi berikut menunjukkan peralihan negeri.

![Model peralihan negeri subkontrak.](../media/VI_State_Model.jpg)

Jadual berikut menerangkan perkara yang diwakili oleh setiap negeri dalam kitaran hayat invois vendor dalam Operasi Projek.

| Negeri | Description | Peralihan yang dibenarkan |
| --- | --- | --- |
| Draf | Keadaan ini adalah keadaan awal invois vendor. Garis dan harga tertakluk kepada pengubahsuaian. Invois vendor di negeri ini boleh diedit dan dipadamkan. | Dalam proses |
| Dalam semakan | Keadaan ini mewakili keadaan pemprosesan invois vendor. Sekurang-kurangnya satu baris invois vendor mempunyai status **pengesahan Sedang berjalan**. | Disahkan, Ditahan |
| Disahkan | Keadaan ini mewakili peringkat invois vendor di mana aplikasi telah mencipta kos sebenar untuk setiap baris invois vendor. Sebarang kos sebenar yang dikaitkan yang dipadankan dengan talian invois vendor telah diterbalikkan dan digantikan dengan kos sebenar daripada talian invois vendor tersebut. Invois vendor di negeri ini tidak boleh diedit atau dipadamkan. Anda boleh menggunakan butang **Batal** untuk membatalkan invois vendor yang disahkan. Tindakan Batal membalikkan kesan tindakan Sahkan. | Dibatalkan |
| Ditahan | <p>Keadaan ini mewakili peringkat invois vendor di mana invois vendor tidak dapat dipindahkan kerana masalah dengan invois atau status vendor. Invois vendor di negeri ini tidak boleh disahkan, dibatalkan, diedit atau dipadamkan.</p><p>Anda boleh menggunakan tindakan Buka semula untuk mengalihkan invois vendor ke **Draf** atau **Dalam keadaan semakan**. Jika sekurang-kurangnya satu baris pada invois vendor mempunyai status **pengesahan Dalam kemajuan** atau **Selesai**, invois vendor akan dibuka semula dalam **keadaan Semakan**. Jika semua baris pada invois vendor mempunyai status **pengesahan Tidak bermula**, invois vendor akan dibuka semula dalam **keadaan Draf**.</p> | Draf, Dalam semakan |
| Dibatalkan | Keadaan ini mewakili peringkat subkontrak di mana penghantaran sebenar bahan dan / atau kerja oleh sumber subkontrak tidak lagi diperlukan. Subkontrak di negeri ini tidak boleh digunakan untuk menganggarkan dan keperluan projek kakitangan untuk sumber dan bahan, dan juga tidak boleh dirujuk mengenai masa, perbelanjaan, dan penggunaan bahan pada projek. Subkontrak dalam keadaan ini tidak boleh diedit atau dipadamkan. | Tiada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
