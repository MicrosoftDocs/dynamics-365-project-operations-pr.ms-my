---
title: Perkara baharu atau diubah dalam Project Service Automation versi 3.x gelombang 1 2020
description: Topik ini menyediakan maklumat tentang perkara baharu dan diubah dalam Project Service Automation versi 3 gelombang 1 2020.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753901"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Perkara baharu atau diubah dalam Project Service Automation versi 3 gelombang 1 2020
Topik ini menyerlahkan pertimbangan naik taraf utama apabila beralih ke keluaran terkini Project Service Automation (PSA) versi 3.x gelombang 1 2020.

## <a name="time-entry"></a>Entri masa
Pengalaman entri masa telah dilanjutkan untuk menyampaikan keupayaan bagi melanjutkan entri masa ke dalam lebih banyak senario pelanggan. Ini termasuk keupayaan untuk menambah jenis entri yang kini mendorong tingkah laku khusus berdasarkan nama skema medan **Tetapan Entri Masa**, dipaparkan sebagai **Sumber Masa**.

### <a name="upgrade-consideration"></a>Pertimbangan naik taraf
Untuk menyokong fungsi ini, peranan dalam PSA telah dikemas kini untuk menyertakan kelayakan baharu. Kelayakan ini memberikan akses baca kepada entiti baharu, **Tetapan Entri Masa**.

Pengguna yang memerlukan keupayaan untuk log masa harus diberikan peranan pengguna **Pengguna Entri Masa** selain peranan yang sedia ada. Peranan ini termasuk fungsi baharu dan memastikan entri masa akan terus berfungsi.

### <a name="currently-extended-time-entry-changes"></a>Perubahan entri masa yang dilanjutkan buat masa ini
Untuk meminimumkan kesan kepada pengguna semasa entri masa, perubahan peranan ini adalah satu-satunya keperluan teras yang diperlukan untuk terus menggunakan entri masa. Jika anda telah mencipta pandangan tersuai atau pengalaman entri masa yang berasingan, anda mesti menetapkan medan **Tetapan Entri Masa** kepada nilai PSA yang betul.
