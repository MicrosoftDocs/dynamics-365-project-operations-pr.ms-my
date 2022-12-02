---
title: Peralihan keadaan pada invois vendor
description: Artikel ini menerangkan tentang peralihan keadaan pada invois vendor dalam Microsoft Dynamics 365 Project Operations.
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

Artikel ini menerangkan tentang peralihan keadaan pada invois vendor dalam Microsoft Dynamics 365 Project Operations. Keadaan berikut digunakan: **Draf**, **Sedang disemak**, **Disahkan**, **Ditahan**, dan **Dibatalkan**.

Ilustrasi berikut menunjukkan peralihan keadaan.

![Model peralihan keadaan subkontrak.](../media/VI_State_Model.jpg)

Jadual berikut menerangkan cara setiap keadaan mewakili kitaran hayat invois vendor dalam Project Operations.

| Negeri | Description | Peralihan dibenarkan |
| --- | --- | --- |
| Draf | Keadaan ini ialah keadaan awal invois vendor. Baris dan harga tertakluk pada perubahan. Invois vendor dalam keadaan ini boleh diedit dan dipadamkan. | Sedang berjalan |
| Dalam semakan | Keadaan ini mewakili keadaan pemprosesan invois vendor. Sekurang-kurangnya satu baris invois vendor mempunyai status pengesahan **Sedang berjalan**. | Disahkan, Ditahan |
| Disahkan | Keadaan ini mewakili peringkat invois vendor yang aplikasi telah mencipta aktual kos untuk setiap baris invois vendor. Sebarang aktual kos berkaitan dengan aktual yang dipadankan dengan baris invois vendor telah diterbalikkan dan digantikan dengan aktual kos daripada baris invois vendor tersebut. Invois vendor dalam keadaan ini tidak boleh diedit atau dipadamkan. Anda boleh menggunakan butang **Batal** untuk membatalkan invois vendor yang disahkan. Tindakan Batal membalikkan kesan tindakan Sahkan. | Dibatalkan |
| Ditahan | <p>Keadaan ini mewakili peringkat invois vendor yang invois vendor tidak boleh beralih kerana isu dengan invois atau status vendor. Invois vendor dalam keadaan ini tidak boleh disahkan, dibatalkan, diedit atau dipadamkan.</p><p>Anda boleh menggunakan tindakan Buka semula untuk mengalihkan invois vendor kepada keadaan **Draf** atau **Sedang disemak**. Jika sekurang-kurangnya satu baris pada invois vendor mempunyai status pengesahan **Sedang berjalan** atau **Selesai**, invois vendor akan dibuka semula dalam keadaan **Sedang disemak**. Jika semua baris pada invois vendor mempunyai status pengesahan **Belum bermula**, invois vendor akan dibuka semula dalam keadaan **Draf**.</p> | Draf, Sedang disemak |
| Dibatalkan | Keadaan ini mewakili peringkat subkontrak yang penghantaran sebenar bahan dan/atau kerja oleh sumber subkontrak tidak diperlukan lagi. Satu subkontrak dalam keadaan ini tidak boleh digunakan untuk anggaran dan keperluan projek kakitangan bagi sumber dan bahan, dan juga tidak boleh dirujuk pada masa, perbelanjaan, dan penggunaan bahan pada projek. Subkontrak dalam keadaan ini tidak boleh diedit atau dipadamkan. | Tiada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
