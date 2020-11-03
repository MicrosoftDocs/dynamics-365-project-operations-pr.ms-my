---
title: Anggaran sumber
description: Topik ini menyediakan maklumat tentang cara anggaran sumber dikira dalam Operasi Projek.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081148"
---
# <a name="resource-estimates"></a>Anggaran sumber

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Anggaran sumber datang dari usaha jangka masa yang ditakrifkan dalam struktur pecahan kerja berserta dengan dimensi harga yang berkenaan. Lazimnya, pengiraan adalah **kadar/jam untuk setiap peranan x jam.** Usaha berfasa masa untuk setiap sumber disimpan dalam rekod tugas sumber. Harga disimpan dalam senarai harga pratakrif. Unit penukaran digunakan berdasarkan senarai harga yang berkenaan.

![Anggaran Sumber](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Harga kos dan mata wang kos lalai

Harga kos dilalaikan daripada Unit Organisasi.

## <a name="default-bill-rate-and-sales-currency"></a>Kadar bil dan mata wang jualan lalai

Harga jualan digunakan sekali setiap urusan. Hierarki untuk senarai harga jualan yang ingkar adalah seperti berikut:

1. Organisasi
2. Pelanggan
3. Sebut harga/kontrak
