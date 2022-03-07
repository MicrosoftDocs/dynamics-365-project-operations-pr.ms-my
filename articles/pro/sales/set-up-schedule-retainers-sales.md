---
title: Sediakan jadual retainer
description: Topik ini memberikan maklumat tentang cara menyediakan jadual retainer dalam Project Operations.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a1cfd83837a91a8d1b3db6df688da6e216a90ada4735e5909a7e8cb26b87247d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994377"
---
# <a name="set-up-a-retainer-schedule"></a>Sediakan jadual retainer

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Jadual retainer disediakan pada halaman **Kontrak Projek** dalam Dynamics 365 Project Operations.

1. Pada halaman **Kontrak Projek**, pada tab **Pendahuluan dan Retainer**, pilih **Sediakan jadual retainer**.
2. Pada halaman dialog yang dibuka, medan yang disenaraikan dalam jadual berikut ditunjukkan. Jadual memberikan idea tentang cara memasukkan nilai yang memberikan kesan atau mempengaruhi jadual retainer yang akan dicipta.

| Medan | Penerangan | Kesan hiliran |
| --- | --- | --- |
| Pelanggan Kontrak Projek | Pelanggan dalam kontrak yang akan diinvois untuk retainer atau pendahuluan ini. | Jika anda mempunyai berbilang pelanggan dalam kontrak dan jika anda perlu menginvois setiap daripada mereka untuk jumlah retainer atau pendahuluan tertentu, cipta satu invois untuk setiap pelanggan secara manual. |
| Tarikh Mula Jadual Retainer | Masukkan tarikh mula jadual retainer. | Tarikh ini mungkin bukan tarikh yang retainer atau pendahuluan pertama dicipta. Tarikh yang retainer atau pendahuluan pertama dicipta turut dipengaruhi oleh kekerapan invois. |
| Tarikh Tamat Jadual Retainer | Masukkan tarikh tamat jadual retainer. | Tarikh ini mungkin bukan tarikh yang retainer atau pendahuluan terakhir dicipta. Tarikh yang retainer atau pendahuluan terakhir dicipta turut dipengaruhi oleh kekerapan invois. |
| Bilangan Retainer untuk Dicipta | Apabila anda memasukkan bilangan retainer untuk dicipta, sistem menggunakan tarikh mula dan kekerapan untuk mencipta nombor dalam medan ini. | Apabila medan ini dikemas kini secara manual, sistem mengabaikan nilai dalam medan **Akhir Jadual Retainer** dan sebaliknya mencipta bilangan khusus retainer atau pendahuluan. |
| Kekerapan Invois | Berapa kerapkah aplikasi akan mencipta retainer dan pendahuluan. | Nilai ini secara langsung mempengaruhi bilangan retainer dan pendahuluan serta tarikh yang telah dicipta. |
| Jumlah Amaun | Jumlah amaun yang dibahagikan kepada retainer individu atau bayaran pendahuluan yang akan dicipta. | Tiada kesan hiliran untuk medan ini. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]