---
title: Batal invois vendor projek
description: Artikel ini menerangkan cara membatalkan invois vendor projek dalam Microsoft Dynamics 365 Project Operations dan kesan kewangan membatalkan invois vendor projek.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7ddaadc0f6e336a8ba67bb4ad8000f7e894f3eb0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911561"
---
# <a name="cancel-a-project-vendor-invoice"></a>Batal invois vendor projek

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Selepas invois vendor disahkan, invois tersebut tidak boleh diedit atau dipadamkan. Jika terdapat ralat pada invois vendor yang telah disahkan, anda boleh menggunakan tindakan Batal untuk membalikkan kesan invois vendor dan mencipta invois vendor baharu.

Apabila anda memilih **Batalkan** pada invois vendor, tingkah laku berikut berlaku:

1. Keadaan invois vendor dikemas kini kepada **Dibatalkan**.
2. Invois vendor yang dibatalkan dan rekod berkaitannya menjadi baca sahaja dan tidak boleh diedit atau dipadamkan.
3. Sebarang realis kos yang dibuat berdasarkan baris invois vendor sebagai sebahagian daripada pengesahan invois vendor diterbalikkan.
4. Jika sebarang aktual kos dipautkan kepada baris invois vendor sebagai sebahagian daripada proses pemadanan, pengesahan invois vendor asal membalikkannya. Semasa pembatalan invois vendor, sebenar kos tersebut dicipta semula. Asal-usul menunjukkan masa, perbelanjaan, atau entri penggunaan bahan.
5. Selepas invois vendor dibatalkan, anda sekali lagi boleh mencipta jurnal pembetulan, memproses masa kemasukan semula dan membatalkan kelulusan masa asal, perbelanjaan atau sebenar bahan.

> [!NOTE]
> Hanya invois vendor projek yang disahkan boleh dibatalkan. Invois vendor di negeri lain tidak boleh dibatalkan.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
