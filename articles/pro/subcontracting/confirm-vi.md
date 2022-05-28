---
title: Sahkan invois vendor projek
description: Topik ini menerangkan cara mengesahkan invois vendor projek dalam Microsoft Dynamics 365 Project Operations dan kesan kewangan mengesahkan invois vendor projek.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c248b3baec6d3f14a020e4fa93f3dad50c65b263
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595739"
---
# <a name="confirm-a-project-vendor-invoice"></a>Sahkan invois vendor projek

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Selepas anda mengesahkan semua baris pada invois vendor dalam Microsoft Dynamics 365 Project Operations, anda boleh menggunakan tindakan Sahkan untuk mengesahkan invois vendor.

Apabila anda memilih **Sahkan** pada invois vendor, tingkah laku berikut berlaku:

1. Keadaan invois vendor dikemas kini kepada **Disahkan**.
2. Invois vendor yang disahkan dan rekod berkaitannya menjadi baca sahaja dan tidak boleh diedit atau dipadamkan.
3. Jika mana-mana actual kos merujuk baris invois vendor sebagai sebahagian daripada proses pemadanan, semua sebenar kos yang dikaitkan dengan baris invois vendor yang dirujuk akan diterbalikkan.
4. Sebenar kos baharu dicipta dengan menggunakan maklumat pada baris invois vendor.
5. Selepas invois vendor disahkan, anda tidak lagi boleh mencipta jurnal pembetulan, memproses pengingatan semula kemasukan masa atau membatalkan kelulusan masa asal, perbelanjaan atau sebenar bahan yang telah diterbalikkan.

> [!NOTE]
> Jika mana-mana baris pada invois vendor mempunyai status pengesahan selain daripada **Selesai**, invois vendor tidak boleh disahkan.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
