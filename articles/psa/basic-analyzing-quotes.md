---
title: Analisis sebut harga projek
description: Topik ini memberikan maklumat mengenai analisis sebut harga projek.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
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
ms.openlocfilehash: 6ed900620f92e76d293f6b533b101be94b25cff3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127034"
---
# <a name="analysis-of-project-quotes"></a>Analisis sebut harga projek

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation menganalisa sebut harga projek untuk menganggarkan keuntungan. Ia juga menganalisis seberapa baik sebut harga itu sejajar dengan jangkaan pelanggan mengenai tarikh penghantaran atau tarikh siap dan tentang belanjawan.

## <a name="profitability-analysis"></a>Analisis keuntungan

Project Service Automation menganalisis keuntungan dengan menggunakan margin kasar dan margin kasar yang dilaraskan.

- Margin kasar dikira menggunakan formula berikut:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- Margin kasar yang dilaraskan dikira menggunakan formula berikut:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Jika nilai untuk margin kasar dan margin kasar dilaraskan berbeza mengikut luas margin, kebanyakan kerja dalam sebut harga dikelaskan sebagai tidak boleh dikenakan cukai.

## <a name="analysis-of-customer-expectations"></a>Analisis jangkaan pelanggan

Anda boleh menganalisis sebut harga dan menjana carta untuk jangkaan pelanggan mengenai jadual dan belanjawan jika anda memasukkan nilai untuk medan berikut:

- Medan **Tarikh penghantaran yang diminta** pada pengepala sebut harga.
- Medan **Belanjawan pelanggan** bagi setiap baris sebut harga (untuk baris berasaskan projek dan baris berasaskan produk).

Analisis jangkaan pelanggan mengenai jadual dilakukan dengan membandingkan tarikh akhir baris sebut harga terperinci dengan tarikh penghantaran yang diminta merentasi semua baris sebut harga dalam sebut harga.

Analisis jangkaan pelanggan mengenai belanjawan dilakukan dengan membandingkan jumlah bagi jumlah belanjawan pelanggan dengan amaun disebut merentasi semua baris sebut harga.
