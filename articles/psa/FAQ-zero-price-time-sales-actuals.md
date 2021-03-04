---
title: Mengapakah harga itu ditetapkan lalai kepada sifar pada masa jualan sebenar?
description: Penyelesaian masalah sebab harga ditetapkan lalai kepada 0 pada masa jualan sebenar.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 5f72e0db94392a35fee9fdcf2c4adb8a08feef13
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146224"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Mengapakah harga ditetapkan lalai kepada sifar pada masa jualan sebenar?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Soalan lazim (FAQ) ini digunakan untuk kelas transaksi sebenar yang ditetapkan pada Masa dan jenis transaksi adalah Jualan Belum Dibilkan. Tiga semakan berikut akan membantu anda menyelesaikan masalah sebab harga (kadar bil) ditetapkan lalai kepada 0 pada masa jualan sebenar.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>Semak 1: Kenal pasti senarai harga jualan untuk projek itu

Cari projek dari medan projek sebenar dan pergi ke halaman projek. Kemudian pergi ke tab Jualan dan pada grid baris Kontrak Projek, klik pada pautan dalam medan Kontrak Projek. Halaman Kontrak projek akan dibuka. Pada halaman Kontrak Projek, pergi ke tab Senarai Harga Projek. Semak jika terdapat sekurang-kurangnya satu senarai harga yang dilampirkan di sini. Jika tiada senarai harga yang dilampirkan dalam grid Senarai Harga Projek daripada Kontrak Projek yang anda telah asingkan masalah tersebut. Lampirkan senarai harga pada grid senarai Harga Projek. Senarai harga yang dibenarkan untuk dilampirkan di sini perlu mempunyai medan konteks yang ditetapkan kepada Jualan dan medan mata wang pada senarai harga perlu sepadan dengan medan mata wang pada Kontrak Projek. Setelah anda selesai membuat pembetulan yang diperlukan, cipta semula entri masa, luluskannya dan sahkan bahawa jualan belum dibilkan sebenarnya menunjukkan harga sah. 

Jika anda mempunyai satu atau lebih senarai harga yang dilampirkan dalam grid Senarai Harga Projek daripada Kontrak Projek, terus ke semakan seterusnya dalam dokumen.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>Semak 2: Adakah mana-mana senarai harga yang dikenal pasti di atas sah untuk tarikh bagi masa jualan sebenar?

Untuk Project Service mempertimbangkan senarai harga untuk menetapkan harga lalai, senarai harga itu seharusnya boleh digunakan untuk tarikh pada masa jualan sebenar. Semak perkara berikut untuk melihat jika senarai harga yang dikenal pasti di atas boleh digunakan:
- Semak jika tarikh mula dan akhir pada tab umum untuk senarai harga yang dilampirkan tidak kosong. Jika tarikh mula dan akhir pada senarai harga yang dikenal pasti di atas adalah kosong, anda telah mengasingkan masalah tersebut. 
- Buat catatan medan tarikh mula pada masa jualan sebenar dan semak jika mana-mana senarai harga yang dikenal pasti boleh digunakan untuk tarikh itu. Sebagai contoh, tarikh masa jualan sebenar seharusnya jatuh pada tarikh mula dan tarikh akhir pada senarai harga. 
    - Jika tiada senarai harga yang meliputi tarikh itu pada masa jualan sebenar, anda telah mengasingkan masalah tersebut. Ubah suai tarikh mula dan akhir bagi senarai harga untuk memastikan senarai harga meliputi tarikh masa jualan sebenar. 
    - Jika terdapat lebih daripada satu senarai harga yang meliputi tarikh pada masa jualan sebenar, anda telah mengasingkan masalah tersebut. Anda boleh membetulkan ini dengan mengedit tarikh mula dan akhir senarai harga supaya terdapat hanya satu senarai harga yang meliputi tarikh masa jualan sebenar. 
    - Jika terdapat hanya satu senarai harga yang meliputi tarikh masa jualan sebenar, pergi ke Semak 3.
Setelah anda selesai membuat pembetulan yang diperlukan, cipta semula entri masa, luluskannya dan sahkan bahawa masa jualan sebenarnya menunjukkan harga sah.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>Semak 3: Adakah terdapat harga sah dalam senarai harga untuk dimensi penentuan harga pada masa jualan sebenar?

Jika anda telah berjaya melengkapkan Semak 1 dan Semak 2, anda kini hanya mempunyai satu senarai harga projek yang boleh digunakan untuk tarikh masa jualan sebenar. Buka Senarai Harga Projek ini dan navigasi ke tab Harga Peranan. Pastikan terdapat baris dalam grid untuk dimensi penentuan harga pada Masa jualan sebenar.

Jika tiada baris dalam grid harga peranan untuk dimensi penentuan harga pada masa jualan sebenar, maka anda telah mengasingkan masalah tersebut. Cipta baris dalam grid harga Peranan untuk dimensi penentuan harga pada masa jualan sebenar. Setelah ini selesai, cipta semula entri masa, luluskannya dan sahkan bahawa masa jualan sebenarnya menunjukkan harga sah.

Jika anda masih tidak melihat harga sah pada masa jualan sebenar anda selepas mengikuti tiga semakan di atas, sila log tiket sokongan. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]