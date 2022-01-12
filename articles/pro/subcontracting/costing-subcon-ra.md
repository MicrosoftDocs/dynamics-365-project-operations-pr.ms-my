---
title: Anggaran kos tugasan sumber subkontrak
description: Topik ini menerangkan beberapa cara Microsoft Dynamics 365 Project Operations mengira anggaran kos tugasan sumber subkontrak.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 09a2a86ea0e97376939d5bff6df9177747818ebb
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903730"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Anggaran kos tugasan sumber subkontrak

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Tugasan tugas ahli pasukan projek subkontrak dikenakan bayaran menggunakan **senarai** harga Belian yang dilampirkan pada subkontrak pada rekod ahli pasukan yang berkaitan. Ini berbeza dengan bagaimana tugasan sumber pekerja dikenakan di mana tugasan tugas sumber pekerja dikenakan biaya menggunakan **senarai harga Kos yang dilampirkan pada unit kontrak** projek. 

Untuk ahli pasukan projek generik yang subkontrak, tugasan dikenakan kos menggunakan persediaan harga berasaskan peranan dalam senarai harga belian yang dilampirkan pada subkontrak. Harga pembelian juga boleh disediakan khusus untuk setiap sumber. Harga khusus sumber ini akan diberi keutamaan apabila kos tugasan tugas ahli pasukan projek yang dinamakan adalah pekerja kontrak. 

Keutamaan menggunakan harga pembelian khusus peranan berbanding khusus sumber didorong oleh penetapan keutamaan dimensi harga dalam **Parameter > dimensi harga berasaskan amaun**.

Fungsi harga yang diperoleh secara dinamik berdasarkan persediaan dimensi untuk harga pembelian subkontraktor adalah sama dengan bagaimana kos dan kadar bil diperolehi untuk pekerja sepenuh masa. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Mencipta tugasan tugas untuk mendapatkan anggaran kos sumber subkontraktor

Tugasan tugas untuk subkontraktor boleh dicipta dalam dua cara: 
- Menggunakan **tab** Tugas.
- Menggunakan **tab** Pasukan.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Mencipta tugasan sumber menggunakan tab Tugas
Menggunakan **senarai Sumber** dalam tab Tugas untuk tugas **tertentu**, anda boleh mencipta tugasan tugas untuk sumber bernama atau sumber generik. Jika anda memilih sumber bernama daripada **juntai bawah Sumber Diuntukkan** pada tugas dan sumber ini ialah pekerja kontrak, sumber yang dinamakan diperuntukkan kepada tugas dan rekod ahli pasukan projek yang sepadan dicipta dengan jenis pekerja yang disetkan kepada Pekerja Kontrak **dan** **Kesahan** disetkan kepada **Tidak Sah**. Sebagai langkah seterusnya, anda perlu membuka rekod ahli pasukan projek dan memilih garis subkontrak dan subkontrak. Ini akan mengemas kini tugasan tugas untuk mempunyai rujukan kepada garis subkontrak dan subkontrak dan juga akan mengemas kini status ahli pasukan kepada **Sah**.

Jika anda memilih untuk mencipta ahli pasukan generik daripada **juntai bawah Sumber Diuntukkan** pada tugas, **dialog Penciptaan ahli pasukan generik akan membolehkan anda memilih garis** subkontrak dan subkontrak. Apabila sumber generik diberikan kepada tugas dan rekod ahli pasukan projek yang sepadan dicipta, anda akan melihat bahawa rekod ahli pasukan projek dicipta dengan jenis pekerja yang ditetapkan kepada **Pekerja Kontrak** dan **Kesahan yang ditetapkan kepada Sah** **·**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Mencipta ahli pasukan projek menggunakan tab Pasukan
Menggunakan tab Pasukan pada projek, anda boleh mencipta ahli pasukan generik atau bernama. Apabila mencipta ahli pasukan, anda boleh memilih garis subkontrak dan subkontrak. Selepas ahli pasukan dicipta, anda perlu menugaskan ahli pasukan kepada tugas menggunakan **menugaskan sumber yang** diuntukkan pada tugas. 

## <a name="updating-estimates"></a>Mengemas kini anggaran
Selepas anda menugaskan ahli pasukan projek kepada tugas, anda perlu menavigasi ke **tab Anggaran projek dan pilih Kemas kini harga untuk memastikan kadar kos tugasan sumber** **subkontraktor** dikemas kini berdasarkan senarai harga pembelian yang dilampirkan pada subkontrak. Anggaran tidak dijana untuk tugas yang tidak ditugaskan dalam Microsoft Dynamics 365 Project Operations. Akibatnya, anda perlu membuat tugasan tugas untuk harga dan kos pelbagai tugas pada projek anda. 

> [NOTA!] Ahli pasukan projek yang mempunyai **jenis Pekerja sebagai pekerja Kontrak tetapi tidak mempunyai rujukan** **subkontrak** dibenderakan sebagai **Tidak Sah pada grid ahli pasukan** **Projek**. Jika terdapat mana-mana ahli pasukan projek dengan status ini, buka rekod ahli pasukan projek dan kemas kini medan garis subkontrak dan subkontrak secara manual supaya anggaran kos kewangan mencerminkan kos subkontraktor dengan tepat pada **tab** Anggaran. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
