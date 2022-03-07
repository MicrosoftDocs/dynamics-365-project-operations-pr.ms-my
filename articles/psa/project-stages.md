---
title: Jenis peringkat projek
description: Topik ini memberikan maklumat tentang peringkat projek.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e4f50d12b4f0bf1586d0a5702bcd38b891590bffe0d3f9661d7f5d170877b54e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996897"
---
# <a name="project-stage-types"></a>Jenis peringkat projek 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Peringkat projek direka bentuk untuk menggambarkan keadaan projek semasa ia berjalan. Penyesuaian boleh digunakan untuk mengemas kini peringkat secara automatik dengan aliran proses perniagaan, Power Automate atau sambungan pasang masuk.

Peringkat berikut ditakrifkan dalam BPF lalai:

- Baru
- Sebut Harga
- Pelan
- Hantar
- Selesai
- Tutup 

## <a name="new"></a>Baharu

Apabila anda mencipta projek, peringkat projek ditetapkan kepada **Baharu**. Jika projek dicipta daripada templat, ia mungkin mempunyai jadual, anggaran dan data pasukan. Jika tidak, ia hanya satu garis panduan projek dan komponen yang selebihnya mesti dimasukkan.

## <a name="quote"></a>Sebut Harga

Apabila anda mengaitkan projek dengan sebut harga atau apabila anda mencipta projek daripada sebut harga, peringkat projek ditetapkan kepada **Sebut Harga** dan anggaran tarikh mula dan tamat dikemas kini. Semasa projek berada dalam peringkat **Sebut harga**, tab **Jualan** pada halaman **Entiti Projek** menunjukkan butiran sebut harga tersebut.

## <a name="plan"></a>Pelan

Apabila anda menang sebut harga yang dikaitkan dengan sesuatu projek dan projek tersebut beralih ke peringkat **Kontrak**, peringkat projek dikemas kini kepada **Pelan**. Semasa projek berada dalam peringkat **Pelan**, halaman **Entiti Projek** menunjukkan butiran kontrak tersebut.

## <a name="deliver"></a>Hantar

Apabila pelan projek selesai dan anda bersedia untuk memulakan projek, pengurus projek harus mengemas kini peringkat projek kepada **Hantar** untuk menunjukkan yang projek telah dimulakan.

## <a name="complete"></a>Selesai 

Apabila kerja untuk projek selesai, pengurus projek boleh mengemas kini peringkat kepada **Selesai**. Dengan mengemas kini peringkat projek kepada **Selesai**, pengurus projek menunjukkan bahawa kerja tersebut telah 100 peratus selesai, tetapi projek itu dibiarkan terbuka supaya sebarang masa atau perbelanjaan yang tertangguh boleh direkodkan.

## <a name="close"></a>Tutup

Apabila semua transaksi direkodkan untuk projek, pengurus projek boleh mengemas kini peringkat kepada **Tutup**. Pada ketika itu, tiada transaksi boleh direkodkan dan projek itu ditetapkan kepada baca sahaja.


[!INCLUDE[footer-include](../includes/footer-banner.md)]