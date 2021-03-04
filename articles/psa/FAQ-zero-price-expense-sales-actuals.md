---
title: Mengapakah harga ditetapkan lalai kepada sifar pada jualan perbelanjaan sebenar?
description: Tiga semakan berikut akan membantu anda menyelesaikan masalah sebab harga ditetapkan lalai kepada 0 pada jualan perbelanjaan sebenar.
author: rumant
manager: kfend
ms.prod: ''
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
ms.openlocfilehash: d4910d3727085a45036f3b438ecd69abc3e99836
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146314"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>Mengapakah harga ditetapkan lalai kepada sifar pada jualan perbelanjaan sebenar?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Soalan lazim (FAQ) ini digunakan untuk perbelanjaan sebenar yang mana kelas transaksi ditetapkan kepada Perbelanjaan dan jenis transaksi ialah Jualan Belum Dibilkan. Tiga semakan berikut akan membantu anda menyelesaikan masalah sebab harga (kadar bil) ditetapkan lalai kepada 0 pada jualan perbelanjaan sebenar.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>Semak 1: Kenal pasti senarai harga jualan untuk projek

Cari projek dari medan projek sebenar dan pergi ke halaman projek. Kemudian pergi ke tab Jualan. Pada grid baris Kontrak Projek, klik pada pautan dalam medan Kontrak Projek. Halaman Kontrak Projek akan dibuka. Pada halaman Kontrak Projek, pergi ke tab Senarai Harga Projek. Semak jika terdapat sekurang-kurangnya satu senarai harga yang dilampirkan di sini.

Jika tiada senarai harga yang dilampirkan dalam grid Senarai Harga Projek daripada Kontrak Projek:

- Lampirkan senarai harga pada grid senarai Harga Projek. Senarai harga yang dibenarkan untuk dilampirkan di sini perlu mempunyai medan konteks yang ditetapkan kepada Jualan dan medan mata wang pada senarai harga perlu sepadan dengan medan mata wang pada Kontrak Projek. Setelah anda membuat pembetulan yang diperlukan, cipta semula entri perbelanjaan, luluskannya dan sahkan bahawa jualan belum dibilkan sebenarnya menunjukkan harga sah.
- Jika anda mempunyai satu atau lebih senarai harga yang dilampirkan dalam grid Senarai Harga Projek daripada Kontrak Projek, pergi ke Semak 2.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>Semak 2: Adakah mana-mana senarai harga yang dikenal pasti di atas sah untuk tarikh tertentu bagi perbelanjaan sebenar?

Untuk Project Service mempertimbangkan senarai harga untuk menetapkan harga lalai, senarai harga itu perlulah boleh digunakan bagi tarikh pada jualan perbelanjaan sebenar. Semak perkara berikut untuk melihat jika senarai harga yang dikenal pasti di atas boleh digunakan:

- Mulakan dengan menyemak jika tarikh mula dan akhir pada tab umum untuk senarai harga yang dilampirkan tidak kosong. Jika tarikh mula dan akhir pada senarai harga yang dikenal pasti di atas adalah kosong, anda telah mengasingkan masalah tersebut. 
- Buat catatan medan tarikh mula pada jualan perbelanjaan sebenar dan semak jika mana-mana senarai harga yang dikenal pasti boleh digunakan untuk tarikh itu. Sebagai contoh, tarikh perbelanjaan sebenar akan jatuh pada tarikh mula dan tarikh akhir pada senarai harga. 
    - Jika tiada senarai harga yang meliputi tarikh itu pada jualan perbelanjaan sebenar, anda telah mengasingkan masalah tersebut. Ubah suai tarikh mula dan akhir bagi senarai harga untuk memastikan senarai harga meliputi tarikh perbelanjaan sebenar. 
    - Jika terdapat lebih daripada satu senarai harga yang meliputi tarikh jualan perbelanjaan sebenar, anda telah mengasingkan masalah tersebut. Edit tarikh mula dan akhir senarai harga supaya terdapat hanya satu senarai harga yang meliputi tarikh perbelanjaan sebenar. 
    - Jika terdapat hanya satu senarai harga yang meliputi tarikh perbelanjaan sebenar, beralih ke Semak 3.
Setelah anda selesai membuat pembetulan yang diperlukan, cipta semula entri perbelanjaan, luluskannya dan sahkan bahawa jualan belum dibilkan sebenarnya menunjukkan harga sah.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>Semak 3: Adakah terdapat harga sah bagi kategori perbelanjaan dalam senarai harga projek boleh digunakan? 

Jika anda telah berjaya melengkapkan Semak 1 dan Semak 2, anda kini hanya mempunyai satu senarai harga projek boleh digunakan untuk tarikh jualan perbelanjaan sebenar. Buka Senarai Harga Projek ini dan pergi ke tab Harga Kategori. Pastikan terdapat baris dalam grid untuk kategori perbelanjaan tertentu pada Perbelanjaan sebenar.
 
- Jika tiada baris, maka anda telah mengasingkan masalah tersebut. Cipta baris dalam grid harga Kategori untuk kategori pada perbelanjaan sebenar anda. Kemudian, cipta semula entri perbelanjaan, luluskannya dan sahkan bahawa jualan belum dibilkan sebenarnya menunjukkan harga sah. 
- Jika terdapat baris untuk kategori perbelanjaan dalam grid harga kategori, semak jika ia mempunyai harga sah.

Untuk memahami tentang harga sah, gunakan kaedah ini:

- Jika medan Kaedah Penentuan Harga pada baris harga Kategori ditetapkan pada Kos, maka kadar unit pada jualan Perbelanjaan anda sebenarnya akan dilalaikan kepada nilai dalam entri Perbelanjaan.
- Jika medan Kaedah Penentuan Harga pada baris harga Kategori ditetapkan kepada Peratusan Tokokan, kemudian semak jika medan Peratus ditetapkan pada nilai sah. Kadar unit pada jualan Perbelanjaan sebenar anda dilalaikan dengan menggunakan peratus tokokan kepada harga dalam entri Perbelanjaan.
- Jika medan Kaedah Penentuan Harga pada baris harga Kategori ditetapkan kepada Harga setiap Unit, kemudian semak jika medan Harga ditetapkan pada nilai sah. Kadar unit pada jualan Perbelanjaan sebenar anda akan dilalaikan kepada jumlah mata wang yang ditentukan dalam medan Harga.

Jika persediaan harga untuk kategori perbelanjaan tidak sah, maka anda telah mengasingkan masalah tersebut. Penyelesaiannya adalah dengan mengedit baris harga kategori dengan harga sah untuk kategori perbelanjaan mengikut peraturan di atas. Setelah anda selesai, cipta semula entri perbelanjaan, luluskannya dan kemudian semak bahawa jualan belum dibilkan sebenarnya mendapat harga sah.

Jika anda masih tidak melihat harga sah pada jualan perbelanjaan sebenar anda selepas melakukan tiga semakan di atas, log tiket sokongan.




[!INCLUDE[footer-include](../includes/footer-banner.md)]