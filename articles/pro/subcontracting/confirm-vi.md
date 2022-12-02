---
title: Sahkan invois vendor projek
description: Artikel ini menerangkan cara mengesahkan invois vendor projek dalam Microsoft Dynamics 365 Project Operations dan kesan kewangan tindakan mengesahkan invois vendor projek.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4dafbe64e0727957068d68f510202a12871b62aa
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261523"
---
# <a name="confirm-a-project-vendor-invoice"></a>Sahkan invois vendor projek

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Selepas anda mengesahkan semua baris pada invois vendor dalam Microsoft Dynamics 365 Project Operations, anda boleh menggunakan tindakan Sah untuk mengesahkan invois vendor.

Apabila anda memilih **Sah** pada invois vendor, tingkah laku berikut berlaku:

1. Keadaan invois vendor dikemas kini kepada **Disahkan**.
2. Invois vendor yang disahkan dan rekod berkaitan dengannya menjadi baca sahaja dan tidak boleh diedit atau dipadamkan.
3. Jika mana-mana aktual kos merujuk kepada baris invois vendor sebagai sebahagian daripada proses pemadanan, semua aktual kos yang berkaitan dengan baris invois vendor yang dirujuk akan dibalikkan.
4. Aktual kos baharu dicipta dengan menggunakan maklumat pada baris invois vendor.
5. Selepas invois vendor disahkan, anda tidak boleh lagi mencipta jurnal pembetulan, memproses panggilan balik entri masa atau membatalkan kelulusan bagi aktual masa, perbelanjaan atau bahan asal yang dibalikkan.

> [!NOTE]
> Jika mana-mana baris pada invois vendor mempunyai status pengesahan selain daripada **Lengkap**, invois vendor tidak boleh disahkan.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
