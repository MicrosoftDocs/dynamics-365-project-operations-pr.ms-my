---
title: Sahkan invois vendor projek
description: Artikel ini menerangkan cara mengesahkan invois vendor projek dalam Microsoft Dynamics 365 Project Operations dan kesan kewangan untuk mengesahkan invois vendor projek.
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

Selepas anda mengesahkan semua baris pada invois vendor dalam Microsoft Dynamics 365 Project Operations, anda boleh menggunakan tindakan Sahkan untuk mengesahkan invois vendor.

Apabila anda memilih **Sahkan** pada invois vendor, kelakuan berikut berlaku:

1. Keadaan invois vendor dikemas kini kepada **Disahkan**.
2. Invois vendor yang disahkan dan rekod berkaitan menjadi baca sahaja dan tidak boleh diedit atau dipadamkan.
3. Jika sebarang kos sebenarnya merujuk talian invois vendor sebagai sebahagian daripada proses pemadanan, semua kos sebenar yang berkaitan dengan baris invois vendor yang dirujuk diterbalikkan.
4. Kos sebenar baharu dicipta dengan menggunakan maklumat pada baris invois vendor.
5. Selepas invois vendor disahkan, anda tidak lagi boleh membuat jurnal pembetulan, memproses penarikan balik entri atau membatalkan kelulusan masa, perbelanjaan atau bahan sebenar yang telah diterbalikkan.

> [!NOTE]
> Jika mana-mana baris pada invois vendor mempunyai status pengesahan selain **Daripada Selesai**, invois vendor tidak dapat disahkan.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
