---
title: Sahkan invois vendor projek
description: Artikel ini menerangkan cara mengesahkan invois vendor projek dalam Microsoft Dynamics 365 Project Operations dan menerangkan kesan kewangan mengesahkan invois vendor projek.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475475"
---
# <a name="confirm-project-vendor-invoices"></a>Sahkan invois vendor projek

_ **Gunakan Pada:** Operasi Projek untuk senario berasaskan sumber/bukan stok

**Apabila manual pengesahan oleh PM diperlukan** parameter didayakan, invois vendor yang dicipta mempunyai Microsoft Dataverse **status Draf**. Invois vendor yang dicipta dengan cara ini mesti disemak dan disahkan secara manual. **Apabila manual pengesahan oleh PM diperlukan** parameter dinyahdayakan, invois vendor yang dicipta dalam Dataverse disahkan secara automatik. Tiada tindakan lanjut diperlukan. 

Selepas anda mengesahkan semua baris pada invois vendor, Dynamics 365 Project Operations pilih **Sahkan** untuk mengesahkan invois vendor.

Apabila anda memilih **Sahkan** pada invois vendor, kelakuan berikut berlaku:

1. Status invois vendor dikemas kini kepada **Disahkan**.
1. Invois vendor yang disahkan dan rekod berkaitan menjadi baca sahaja dan tidak boleh diedit atau dipadamkan.
1. Jika sebarang kos sebenarnya merujuk talian invois vendor sebagai sebahagian daripada proses pemadanan, semua kos sebenar yang berkaitan dengan baris invois vendor yang dirujuk diterbalikkan.
1. Kos sebenar baharu dicipta dengan menggunakan maklumat pada baris invois vendor.
1. Anda tidak lagi boleh membuat jurnal pembetulan, memproses penarikan balik entri masa, atau membatalkan kelulusan masa asal, perbelanjaan, atau bahan sebenar yang telah diterbalikkan.
1. Dalam Dynamics 365 Finance, **nilai kos** Projek dikemas kini dengan menggunakan jurnal integrasi Projek, dan akaun *integrasi Perolehan diterbalikkan* selepas jurnal integrasi Projek disiarkan.

> [!NOTE]
> Jika mana-mana baris pada invois vendor mempunyai status pengesahan selain **Daripada Selesai**, invois vendor tidak dapat disahkan.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
