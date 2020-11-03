---
title: Perkara baharu atau diubah dalam Project Service Automation versi 3.x gelombang 1 2020
description: Topik ini menyediakan maklumat tentang perkara baharu dan diubah dalam Project Service Automation versi 3 gelombang 1 2020.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 16b51995f863d9ee54172625dacbf081c51c8556
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081174"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Perkara baharu atau diubah dalam Project Service Automation versi 3 gelombang 1 2020
Topik ini menyerlahkan pertimbangan naik taraf utama apabila beralih ke keluaran terkini Project Service Automation (PSA) versi 3.x gelombang 1 2020.

## <a name="time-entry"></a>Entri masa
Pengalaman entri masa telah dilanjutkan untuk menyampaikan keupayaan bagi melanjutkan entri masa ke dalam lebih banyak senario pelanggan. Ini termasuk keupayaan untuk menambah jenis entri yang kini mendorong tingkah laku khusus berdasarkan nama skema medan **Tetapan Entri Masa** , dipaparkan sebagai **Sumber Masa**. Penyelesaian baharu, yang dipanggil Masa, Perbelanjaan, Penstatusan dan Kelulusan (TESA) telah ditambah untuk menyokong fungsi ini.

### <a name="upgrade-consideration"></a>Pertimbangan naik taraf
Untuk menyokong fungsi ini, peranan dalam PSA telah dikemas kini untuk menyertakan kelayakan baharu. Kelayakan ini memberikan akses baca kepada entiti baharu, **Tetapan Entri Masa**.

Pengguna yang memerlukan keupayaan untuk log masa harus diberikan peranan pengguna **Pengguna Entri Masa** selain peranan yang sedia ada. Peranan ini termasuk fungsi baharu dan memastikan entri masa akan terus berfungsi.

Selain itu, jika anda mempunyai sebarang modul aplikasi tersuai yang termasuk semua borang untuk entiti kemasukan masa, anda akan dikehendaki untuk mengalih keluar **Borang Cipta Cepat Entri TESA** dari modul.

### <a name="currently-extended-time-entry-changes"></a>Perubahan entri masa yang dilanjutkan buat masa ini
Untuk meminimumkan kesan kepada pengguna semasa entri masa, perubahan peranan ini adalah satu-satunya keperluan teras yang diperlukan untuk terus menggunakan entri masa. Jika anda telah mencipta pandangan tersuai atau pengalaman entri masa yang berasingan, anda mesti menetapkan medan **Tetapan Entri Masa** kepada nilai PSA yang betul.
