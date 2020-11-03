---
title: Analisis sebut harga projek
description: Topik ini memberikan maklumat mengenai analisis sebut harga projek.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 0d9cefafcce33297146cae81d9ba7e68ab79aeb6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081344"
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
