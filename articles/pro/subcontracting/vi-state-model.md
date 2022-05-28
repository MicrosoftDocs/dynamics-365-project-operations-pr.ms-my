---
title: Peralihan negeri pada invois vendor
description: Topik ini menerangkan peralihan negeri pada invois vendor dalam Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7efb52621ee325d5025dfad0b45218d1fe20a063
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584699"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Peralihan negeri pada invois vendor

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Topik ini menerangkan peralihan negeri pada invois vendor dalam Microsoft Dynamics 365 Project Operations. Negeri-negeri berikut digunakan: **Draf**, **Dalam semakan**, **Disahkan**, **Ditahan** dan **Dibatalkan**.

Ilustrasi berikut menunjukkan peralihan negeri.

![Model peralihan keadaan subkontrak.](../media/VI_State_Model.jpg)

Jadual berikut menerangkan perkara yang diwakili oleh setiap negeri dalam kitaran hayat invois vendor dalam Operasi Projek.

| Negeri | Description | Peralihan yang dibenarkan |
| --- | --- | --- |
| Draf | Keadaan ini ialah keadaan awal invois vendor. Garisan dan harga tertakluk kepada pengubahsuaian. Invois vendor dalam keadaan ini boleh diedit dan dipadamkan. | Dalam proses |
| Dalam semakan | Keadaan ini mewakili keadaan pemprosesan invois vendor. Sekurang-kurangnya satu baris invois vendor mempunyai status **pengesahan Sedang berjalan**. | Disahkan, Ditahan |
| Disahkan | Negeri ini mewakili peringkat invois vendor di mana aplikasi telah mencipta sebenar kos untuk setiap baris invois vendor. Sebarang sebenar kos terpaut yang dipadankan dengan baris invois vendor telah diterbalikkan dan digantikan dengan sebenar kos daripada baris invois vendor tersebut. Invois vendor dalam keadaan ini tidak boleh diedit atau dipadamkan. Anda boleh menggunakan butang **Batal** untuk membatalkan invois vendor yang disahkan. Tindakan Batal membalikkan kesan tindakan Sahkan. | Dibatalkan |
| Ditahan | <p>Keadaan ini mewakili peringkat invois vendor di mana invois vendor tidak boleh bergerak kerana isu dengan invois atau status vendor. Invois vendor dalam keadaan ini tidak boleh disahkan, dibatalkan, diedit atau dipadamkan.</p><p>Anda boleh menggunakan tindakan Buka semula untuk mengalihkan invois vendor ke keadaan **Draf** atau **Dalam semakan**. Jika sekurang-kurangnya satu baris pada invois vendor mempunyai status **pengesahan Sedang berjalan** atau **Selesai**, invois vendor akan dibuka semula dalam keadaan **Dalam semakan**. Jika semua baris pada invois vendor mempunyai status **pengesahan Tidak bermula**, invois vendor akan dibuka semula dalam keadaan **Draf**.</p> | Draf, Dalam semakan |
| Dibatalkan | Keadaan ini mewakili peringkat subkontrak di mana penghantaran sebenar bahan dan/atau kerja oleh sumber subkontrak tidak lagi diperlukan. Subkontrak di negeri ini tidak dapat digunakan untuk menganggarkan dan keperluan projek kakitangan untuk sumber dan bahan, dan juga tidak dapat dirujuk tepat pada waktunya, perbelanjaan, dan penggunaan bahan pada projek. Subkontrak dalam keadaan ini tidak boleh diedit atau dipadamkan. | Tiada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
