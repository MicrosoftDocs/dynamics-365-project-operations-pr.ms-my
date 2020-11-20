---
title: Mengapakah harga ditetapkan lalai kepada sifar pada masa kos sebenar?
description: Penyelesaian masalah sebab harga ditetapkan lalai kepada 0 pada masa kos sebenar.
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
ms.openlocfilehash: 124719410f89dea506d43a1b64cb91c85d4f3968
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131385"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>Mengapakah harga ditetapkan lalai kepada sifar pada masa kos sebenar?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Soalan lazim (FAQ) ini digunakan untuk kelas transaksi sebenar ditetapkan kepada Masa dan jenis transaksi adalah Kos. Tiga semakan berikut akan membantu anda menyelesaikan masalah sebab harga ditetapkan lalai kepada 0 pada masa kos sebenar.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>Semak 1: Kenal pasti senarai harga kos untuk projek

Cari projek dari medan projek sebenar dan kemudian pergi ke halaman projek. Klik pada pautan unit kontrak dalam medan. Pada halaman Unit Kontrak, semak jika unit kontrak mempunyai senarai harga dalam grid Senarai Harga Kos.

Jika terdapat lebih daripada satu senarai harga, anda telah mengasingkan masalah tersebut. Project Service hanya menyokong satu senarai harga setiap unit organisasi. Keluarkan semua senarai harga daripada entiti ini sehingga terdapat hanya satu senarai harga yang dilampirkan dalam grid Senarai Harga Kos Unit Organisasi.

Jika tiada senarai harga yang dilampirkan pada Unit Organisasi, buat catatan mata wang unit Organisasi. Pergi ke Project Service dan kemudian Parameter dan buka tab Senarai Harga. Semak jika terdapat mana-mana senarai harga dengan konteks ditetapkan kepada Kos dan mata wang yang sepadan dengan mata wang Unit Organisasi.
 
Jika tiada senarai harga yang sepadan dengan kriteria itu, anda telah mengasingkan masalah tersebut. Pastikan anda mempunyai sekurang-kurangnya satu senarai harga yang konteksnya ditetapkan kepada Kos dan mata wangnya sepadan dengan mata wang Unit Organisasi.

Jika terdapat lebih daripada satu senarai harga yang sepadan dengan kriteria itu, teruskan membaca dokumen ini untuk membuat lebih banyak semakan.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>Semak 2: Adakah mana-mana senarai harga yang dikenal pasti di atas sah untuk tarikh tertentu bagi masa kos sebenar?

Untuk Project Service mempertimbangkan senarai harga untuk menetapkan harga lalai, senarai harga itu seharusnya boleh digunakan untuk tarikh pada masa kos sebenar. Semak perkara berikut untuk melihat jika senarai harga yang dikenal pasti di atas boleh digunakan:

- Semak jika tarikh mula dan akhir pada tab umum untuk senarai harga yang dilampirkan tidak kosong. Jika tarikh mula dan akhir pada senarai harga yang dikenal pasti di atas adalah kosong, anda telah mengasingkan masalah tersebut. 
- Buat catatan medan tarikh mula pada masa kos sebenar dan semak jika mana-mana senarai harga yang dikenal pasti boleh digunakan untuk tarikh itu. Sebagai contoh, tarikh masa kos sebenar seharusnya jatuh pada tarikh mula dan tarikh akhir pada senarai harga. 
    - Jika tiada senarai harga yang meliputi tarikh itu pada masa kos sebenar, anda telah mengasingkan masalah tersebut. Ubah suai tarikh mula dan akhir bagi senarai harga untuk memastikan senarai harga meliputi tarikh masa kos sebenar. 
    - Jika terdapat lebih daripada satu senarai harga yang meliputi tarikh masa kos sebenar, anda telah mengasingkan masalah tersebut. Anda boleh membetulkan ini dengan mengedit tarikh mula dan akhir senarai harga supaya terdapat hanya satu senarai harga yang meliputi tarikh masa kos sebenar. 
    - Jika terdapat hanya satu senarai harga yang meliputi tarikh masa kos sebenar, beralih ke semakan seterusnya dalam dokumen.
Setelah anda selesai membuat pembetulan yang diperlukan, cipta semula entri masa, luluskannya dan sahkan bahawa masa kos sebenarnya menunjukkan harga sah.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>Semak 3: Adakah terdapat harga sah dalam senarai harga untuk dimensi penentuan harga pada masa kos sebenar?

Jika anda telah berjaya melengkapkan Semak 1 dan Semak 2, anda kini hanya mempunyai satu senarai harga projek yang boleh digunakan untuk tarikh masa kos sebenar. Buka Senarai Harga Projek ini dan pergi ke tab Harga Peranan. Pastikan terdapat baris dalam grid untuk dimensi penentuan harga pada masa kos sebenar.

Jika tiada baris dalam grid harga peranan untuk dimensi penentuan harga pada masa kos sebenar, maka anda telah mengasingkan masalah tersebut. Cipta baris dalam grid harga Peranan untuk dimensi penentuan harga pada masa kos sebenar. Setelah ini selesai, cipta semula entri masa, luluskannya dan sahkan bahawa masa kos sebenarnya menunjukkan harga sah.
 
Jika anda masih tidak melihat harga sah pada masa kos sebenar anda selepas anda melakukan tiga semakan di atas, sila log tiket sokongan.



