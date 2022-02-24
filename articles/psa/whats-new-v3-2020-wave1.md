---
title: Perkara baharu atau diubah dalam Project Service Automation versi 3.x gelombang 1 2020
description: Topik ini menyediakan maklumat tentang perkara baharu dan diubah dalam Project Service Automation versi 3 gelombang 1 2020.
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 5110679038ae7ed1e21a3e7dc80a4657e0752b49
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150949"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Perkara baharu atau diubah dalam Project Service Automation versi 3 gelombang 1 2020

[!include [banner](../includes/psa-now-project-operations.md)]

Topik ini menyerlahkan pertimbangan naik taraf utama apabila beralih ke keluaran terkini Project Service Automation (PSA) versi 3.x gelombang 1 2020.

## <a name="time-entry"></a>Entri masa
Pengalaman entri masa telah dilanjutkan untuk menyampaikan keupayaan bagi melanjutkan entri masa ke dalam lebih banyak senario pelanggan. Ini termasuk keupayaan untuk menambah jenis entri yang kini mendorong tingkah laku khusus berdasarkan nama skema medan **Tetapan Entri Masa**, dipaparkan sebagai **Sumber Masa**. Penyelesaian baharu, yang dipanggil Masa, Perbelanjaan, Penstatusan dan Kelulusan (TESA) telah ditambah untuk menyokong fungsi ini.

### <a name="upgrade-consideration"></a>Pertimbangan naik taraf
Untuk menyokong fungsi ini, peranan dalam PSA telah dikemas kini untuk menyertakan kelayakan baharu. Kelayakan ini memberikan akses baca kepada entiti baharu, **Tetapan Entri Masa**.

Pengguna yang memerlukan keupayaan untuk log masa harus diberikan peranan pengguna **Pengguna Entri Masa** selain peranan yang sedia ada. Peranan ini termasuk fungsi baharu dan memastikan entri masa akan terus berfungsi.

Selain itu, jika anda mempunyai sebarang modul aplikasi tersuai yang termasuk semua borang untuk entiti kemasukan masa, anda akan dikehendaki untuk mengalih keluar **Borang Cipta Cepat Entri TESA** dari modul.

### <a name="currently-extended-time-entry-changes"></a>Perubahan entri masa yang dilanjutkan buat masa ini
Untuk meminimumkan kesan kepada pengguna semasa entri masa, perubahan peranan ini adalah satu-satunya keperluan teras yang diperlukan untuk terus menggunakan entri masa. Jika anda telah mencipta pandangan tersuai atau pengalaman entri masa yang berasingan, anda mesti menetapkan medan **Tetapan Entri Masa** kepada nilai PSA yang betul.
