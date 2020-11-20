---
title: Batalkan entri masa dan perbelanjaan yang diluluskan sebelumnya
description: Topik ini memberikan maklumat tentang cara membatalkan masa projek diluluskan dan transaksi perbelanjaan.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
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
ms.openlocfilehash: 84fc057599dd98162320d6104ed4a7612e894ecb
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123344"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Batalkan entri masa atau perbelanjaan yang diluluskan sebelumnya

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dalam versi terkini Dynamics 365 Project Service Automation, pelulus boleh membatalkan entri masa atau perbelanjaan yang mereka luluskan sebelum ini.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Batalkan entri masa atau perbelanjaan yang diluluskan sebelumnya

Ikuti langkah-langkah ini untuk membatalkan entri masa atau perbelanjaan yang anda luluskan sebelumnya.

1. Pergi ke **Projek** \> **Kerja Saya** \> **Kelulusan**.
2. Pada halaman senarai **Kelulusan**, ubah pandangan kepada **Kelulusan lalu saya**. Senarai entri masa dan perbelanjaan yang anda luluskan sebelum ini ditunjukkan.
3. Pilih satu atau lebih entri, kemudian pilih **Batalkan kelulusan**. Anda menerima satu mesej amaran.
4. Pilih **OK** untuk membatalkan kelulusan.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Fahami impak pembatalan kelulusan entri masa atau perbelanjaan

Apabila kelulusan dibatalkan, terdapat impak operasi dan impak kewangan.

### <a name="operational-impact"></a>Impak operasi

Pada bahagian operasi, apabila kelulusan dibatalkan, status rekod ditetapkan kepada **Draf**, dan kelulusan tidak lagi muncul dalam pandangan **Kelulusan lalu saya**. Sebaliknya, kelulusan yang dibatalkan muncul dalam sama ada pandangan **Entri masa untuk kelulusan** atau pandangan **Entri perbelanjaan untuk kelulusan**, bergantung pada sama ada ia adalah entri masa atau entri perbelanjaan. Selain itu, status entri masa atau perbelanjaan berkaitan diubah kepada **Diserahkan**, agar entri berkaitan konsisten dengan kelulusan yang mempunyai status **Draf**.

Sebagai pelulus, anda boleh mengedit beberapa medan kelulusan yang mempunyai status **Draf**. Medan ini termasuk **Jenis Pengebilan** dan **Jam Boleh Dibilkan untuk Entri Masa**. Selepas anda membuat perubahan, anda boleh meluluskan rekod semula. Secara alternatif, anda boleh menolak entri. Jika anda menolak kelulusan entri masa, status entri diubah kepada **Dipulangkan**. Jika anda menolak kelulusan entri perbelanjaan, status entri diubah kepada **Ditolak**. Dari segi fungsi, entri yang dipulangkan dan ditolak bertindak sama seperti entri yang mempunyai status **Draf**. Ahli pasukan projek boleh sama ada membuat sebarang perubahan yang diperlukan ke atas entri, dan kemudian menyerahkan semula untuk kelulusan, atau memadam entri secara keseluruhannya.

### <a name="financial-impact"></a>Impak kewangan

Projek juga terjejas dari segi kewangan apabila kelulusan dibatalkan. Pertama, aktual serupa untuk kos dan jualan dikemas kini dalam cara berikut:

- Status pelarasan ditetapkan kepada **Dilaraskan**.
- Status pengebilan ditetapkan kepada **Dibatalkan**.

Seterusnya, entri balikan dicipta dalam jadual Aktual. Untuk mencipta entri balikan, sistem menyalin nilai medan daripada aktual sebenar. Satu-satunya nilai yang tidak disalin adalah nilai kuantiti. Sebaliknya, nilai ini dibalikkan. Aktual balikan dicipta untuk **Kos** dan aktual **Jualan Tidak Dibilkan**. Medan **Status Pelarasan** pada aktual balikan ditetapkan kepada **Tidak dilaraskan**, dan status pengebilan ditetapkan kepada **Dibatalkan**.

Selepas semua perubahan ini dibuat, amaun yang direkod sebagai dibelanja ke atas projek dan tunggakan hasil ke atas projek tidak lagi dikira untuk amaun yang diwakili aktual ini.
