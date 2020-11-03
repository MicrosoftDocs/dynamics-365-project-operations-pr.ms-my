---
title: Naik taraf laman utama
description: Topik ini menunjukkan di mana untuk mencari maklumat penting mengenai ciri baharu dan diubah dalam Dynamics 365 Project Service Automation dan proses untuk menaik taraf kepada versi terbaharu.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
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
ms.openlocfilehash: 29e7b519b61e8709c025e9906d04aed0156f65eb
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081309"
---
# <a name="upgrade-home-page"></a>Naik taraf laman utama

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Naik taraf daripada versi PSA 2.x atau 1.x kepada versi 3.x

### <a name="new-instances"></a>Tika baharu

Pada 17 Mei 2019, apabila Project Service Automation dipilih semasa peruntukan tika baharu, versi 3.x dipasang secara lalai.

### <a name="existing-instances"></a>Tika sedia ada

Sebelum ini, pelanggan yang mempunyai tika PSA versi 2. x dan perlu menaik taraf kepada versi 3.x, yang merupakan versi Berasaskan antara muka klien disatukan (UCI) bagi PSA, mesti menghubungi Sokongan Microsoft dan menyediakan butiran tika mereka, supaya sokongan boleh mendayakan tika bagi naik taraf kepada versi 3.x. Pada 1 Mac 2020, pelanggan yang mempunyai tika PSA versi 2.x dan perlu menaik taraf kepada versi 3.x, akan dapat menaik taraf tika mereka secara terus daripada portal Pentadbir tanpa perlu menghubungi Sokongan Microsoft.  

> [!NOTE]
> PSA versi 3.x termasuk perubahan ketara. Ia telah dibina pada rangka kerja Antara Muka Disatukan untuk membantu menyediakan pengalaman pengguna yang lebih baik. Aplikasi direka bentuk semula menghantar yang konsisten dan seragam (UI) dan ia mengikut prinsip reka bentuk responsif untuk pandangan optimum pada sebarang saiz skrin atau peranti. Telah ada perubahan lain di seluruh aplikasi. Antara kawasan yang telah ditukar termasuk penetapan harga, penempahan dan pemberian sumber, masa, perbelanjaan dan kelulusan.

Sebelum anda memulakan proses peningkatan, kami mengesyorkan anda melengkapkan tugas berikut:

- Tentu sahkan sama Dynamics 365 Field Service dan Project Service Automation telah dipasang pada tika yang dikenal pasti. Jika kedua-dua penyelesaian dipasang, anda perlu merancang untuk menaik taraf sebelum anda menyambung semula kegunaan biasa tika.
- Semak semula dengan teliti topik berikut. Kesedaran dan pemahaman tentang perubahan antara versi akan membantu anda dengan proses peningkatan. Topik ini memberikan maklumat tentang perubahan besar dalam PSA, bersama dengan pertimbangan dan pengesyoran untuk merancang naik taraf anda kepada versi 3.x.

    - [Perkara baharu atau berubah dalam Project Service Automation versi 3](whats-new-changed-v3.md)
    - [Pertimbangan naik taraf - Project Service Automation versi 2.x atau 1.x kepada versi 3](upgrade-v3.md)

- Naik taraf tika kotak pasir anda untuk menilai perubahan dalam pelaksanaan anda sebelum anda menaik taraf tika pengeluaran anda.

Selepas anda menyemak topik yang disebutkan sebelum ini dan bersedia untuk menaik taraf kepada PSA versi 3.x atau versi UCI, serahkan permintaan kepada sokongan Microsoft untuk membuat peningkatan tersedia daripada Pusat pentadbir. Dalam permintaan anda, berikan butiran tika anda.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Versi lebih lama PSA (PSA versi 2.x) dalam tika yang baharu dicipta

Pada 17 Mei, 2019, semua tika baru akan mempunyai UCI sebagai klien lalai. Untuk penjajaran dengan perubahan ini, PSA versi 3.x dan Field Service Version 8.x akan diperuntukkan secara lalai, kerana versi ini direka untuk berfungsi dengan klien UCI.

Mulai 1 Mac 2020, pelanggan Dynamics PSA tidak lagi akan dapat mencipta persekitaran baharu dengan versi PSA yang lebih lama, contohnya PSA versi 2.x atau lebih rendah. Sebarang persekitaran baharu akan hanya mendapat versi 3.x PSA.

> [!NOTE]
> Untuk pengalaman terbaik apabila anda menggunakan versi lebih lama daripada Field Service dan aplikasi PSA, pergi ke halaman **Tetapan sistem** dan untuk medan **Gunakan medan baru Antara Muka Disatukan hanya (disyorkan)** , pilih **Tidak** sebagai versi ini tidak direka untuk dimuatkan dengan betul dalam UCI. Selepas anda memadamkan UCI, anda boleh buka dan jalankan versi Field Service ini dan PSA dengan menggunakan klien web lama. 
