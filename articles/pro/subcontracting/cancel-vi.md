---
title: Batal invois vendor projek
description: Artikel ini menerangkan cara membatalkan invois vendor projek dalam Microsoft Dynamics 365 Project Operations dan kesan kewangan tindakan membatalkan invois vendor projek.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 79d00a91f9ab2d66eab2f80349d6f1fba1934f94
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261102"
---
# <a name="cancel-a-project-vendor-invoice"></a>Batal invois vendor projek

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Selepas invois vendor disahkan, ia tidak boleh diedit atau dipadam. Jika terdapat ralat pada invois vendor yang telah disahkan, anda boleh menggunakan tindakan Batal untuk membalikkan kesan invois vendor dan mencipta invois vendor baharu.

Apabila anda memilih **Batal** pada invois vendor, tingkah laku berikut berlaku:

1. Keadaan invois vendor dikemas kini kepada **Dibatalkan**.
2. Invois vendor yang dibatalkan dan rekod berkaitan dengannya menjadi baca sahaja dan tidak boleh diedit atau dipadamkan.
3. Apa-apa aktual kos yang dicipta berdasarkan baris invois vendor sebagai sebahagian daripada pengesahan invois vendor dibalikkan.
4. Jika mana-mana aktual kos dipautkan dengan baris invois vendor sebagai sebahagian daripada proses pemadanan, pengesahan invois vendor asal membalikkannya. Semasa pembatalan invois vendor, aktual kos tersebut dicipta semula. Asal menunjukkan entri masa, perbelanjaan atau penggunaan bahan.
5. Selepas invois vendor dibatalkan, anda boleh mencipta jurnal pembetulan, memproses panggilan balik entri masa dan membatalkan kelulusan bagi aktual masa, perbelanjaan atau bahan asal sekali lagi.

> [!NOTE]
> Hanya invois vendor projek yang disahkan boleh dibatalkan. Invois vendor dalam keadaan lain tidak boleh dibatalkan.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
