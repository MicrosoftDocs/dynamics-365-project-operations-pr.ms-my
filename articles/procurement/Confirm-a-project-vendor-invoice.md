---
title: Sahkan invois vendor projek
description: Artikel ini menerangkan cara mengesahkan invois vendor projek dalam Microsoft Dynamics 365 Project Operations dan menerangkan kesan kewangan tindakan mengesahkan invois vendor projek.
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

Apabila parameter **Pengesahan manual oleh PM diperlukan** didayakan, invois vendor yang dicipta dalam Microsoft Dataverse mempunyai status **Draf**. Invois vendor yang dicipta dengan cara ini mesti disemak dan disahkan secara manual. Apabila parameter **Pengesahan manual oleh PM diperlukan** dinyahdayakan, invois vendor yang dicipta dalam Dataverse disahkan secara automatik. Tiada tindakan lanjut diperlukan. 

Selepas anda mengesahkan semua baris pada invois vendor dalam Dynamics 365 Project Operations, pilih **Sah** untuk mengesahkan invois vendor.

Apabila anda memilih **Sah** pada invois vendor, tingkah laku berikut berlaku:

1. Status invois vendor dikemas kini kepada **Disahkan**.
1. Invois vendor yang disahkan dan rekod berkaitan dengannya menjadi baca sahaja dan tidak boleh diedit atau dipadamkan.
1. Jika mana-mana aktual kos merujuk kepada baris invois vendor sebagai sebahagian daripada proses pemadanan, semua aktual kos yang berkaitan dengan baris invois vendor yang dirujuk akan dibalikkan.
1. Aktual kos baharu dicipta dengan menggunakan maklumat pada baris invois vendor.
1. Anda tidak boleh lagi mencipta jurnal pembetulan, memproses panggilan balik entri masa atau membatalkan kelulusan bagi aktual masa, perbelanjaan atau bahan asal yang dibalikkan.
1. Dalam Dynamics 365 Finance, nilai **Kos projek** dikemas kini dengan menggunakan jurnal integrasi Projek dan akaun integrasi Perolehan *dibalikkan* selepas jurnal integrasi Projek disiarkan.

> [!NOTE]
> Jika mana-mana baris pada invois vendor mempunyai status pengesahan selain daripada **Lengkap**, invois vendor tidak boleh disahkan.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
