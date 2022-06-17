---
title: Sahkan invois vendor projek
description: Artikel ini menerangkan cara mengesahkan invois vendor projek dalam Microsoft Dynamics 365 Project Operations dan kesan kewangan mengesahkan invois vendor projek.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 092b3cd5981f7d9bb8767c7a2acb2f4952801d06
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932445"
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
