---
title: Peringkat projek
description: Topik ini memberikan maklumat tentang peringkat projek yang tersedia dalam Microsoft Dynamics Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: aa3d692a46165b01eafbd7619578cead8dd912d6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127484"
---
# <a name="project-stages"></a>Peringkat projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Peringkat projek direka bentuk untuk menggambarkan keadaan projek semasa ia berjalan. Penyesuaian boleh digunakan untuk mengemas kini peringkat secara automatik dengan aliran proses perniagaan, Power Automate atau sambungan pasang masuk.

Peringkat berikut ditakrifkan dalam aliran proses perniagaan lalai:

- Baru
- Sebut Harga
- Pelan
- Hantar
- Dilengkapkan
- Tutup 

## <a name="new"></a>Baru

Apabila anda mencipta projek, peringkat projek ditetapkan kepada **Baharu**. Jika projek dicipta daripada templat, ia mungkin mempunyai jadual, anggaran dan data pasukan. Sebaliknya, ia adalah satu garis panduan projek dan komponen yang tinggal mesti dimasukkan.

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

