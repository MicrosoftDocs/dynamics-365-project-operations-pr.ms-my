---
title: Peringkat projek
description: Topik ini memberikan maklumat tentang peringkat projek.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753880"
---
# <a name="project-stages"></a>Peringkat projek 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Peringkat projek dikemas kini untuk menggambarkan keadaan projek tersebut apabila ia berjalan. Aliran proses perniagaan lalai mengemas kini secara automatik beberapa peringkat projek sementara yang lain dikemas kini secara manual oleh pengurus projek. 

Peringkat berikut ditakrifkan dalam BPF lalai:

- Baharu
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
