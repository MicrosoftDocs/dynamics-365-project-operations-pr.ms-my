---
title: Batal invois vendor projek
description: Artikel ini menerangkan cara membatalkan invois vendor projek dalam Microsoft Dynamics 365 Project Operations dan kesan kewangan membatalkan invois vendor projek.
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

Selepas invois vendor disahkan, invois vendor tidak boleh diedit atau dipadamkan. Jika terdapat ralat pada invois vendor yang telah disahkan, anda boleh menggunakan tindakan Batal untuk membalikkan kesan invois vendor dan mencipta invois vendor baharu.

Apabila anda memilih **Batal** pada invois vendor, kelakuan berikut berlaku:

1. Keadaan invois vendor dikemas kini kepada **Dibatalkan**.
2. Invois vendor yang dibatalkan dan rekod berkaitan menjadi baca sahaja dan tidak boleh diedit atau dipadamkan.
3. Sebarang kos sebenar yang dibuat berdasarkan baris invois vendor sebagai sebahagian daripada pengesahan invois vendor diterbalikkan.
4. Jika sebarang kos sebenar dikaitkan dengan talian invois vendor sebagai sebahagian daripada proses pemadanan, pengesahan invois vendor asal membalikkannya. Semasa pembatalan invois vendor, kos sebenar dibuat semula. Asal-usul menunjuk kepada entri masa, perbelanjaan, atau penggunaan bahan.
5. Selepas invois vendor dibatalkan, anda boleh sekali lagi membuat jurnal pembetulan, memproses penarikan balik entri dan membatalkan kelulusan masa, perbelanjaan atau bahan sebenar.

> [!NOTE]
> Hanya invois vendor projek yang disahkan boleh dibatalkan. Invois vendor di negeri lain tidak boleh dibatalkan.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
