---
title: Anggaran kos tugasan sumber yang disubkontrak
description: Artikel ini menerangkan beberapa cara Microsoft Dynamics 365 Project Operations mengira anggaran kos tugasan sumber subkontrak.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 40603c1d2dfdd49909d9a4bf5085f43201e8f6bd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932353"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Anggaran kos tugasan sumber yang disubkontrak

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Tugasan tugas ahli pasukan projek subkontrak adalah kos menggunakan **senarai harga Pembelian** yang dilampirkan pada subkontrak pada rekod ahli pasukan yang berkaitan. Ini berbeza dengan cara tugasan sumber pekerja dikenakan biaya di mana tugasan tugas sumber pekerja dikenakan biaya menggunakan **senarai harga Kos** yang dilampirkan pada unit kontrak projek. 

Untuk ahli pasukan projek generik yang disubkontrak, tugasan dikenakan kos menggunakan persediaan harga berasaskan peranan dalam senarai harga pembelian yang dilampirkan pada subkontrak. Harga pembelian juga boleh disediakan khusus untuk setiap sumber. Harga khusus sumber ini akan diberi keutamaan apabila kos tugasan tugas ahli pasukan projek yang dinamakan adalah pekerja kontrak. 

Keutamaan menggunakan harga pembelian khusus peranan berbanding khusus sumber didorong oleh penyediaan keutamaan dimensi harga dalam **Parameter > dimensi harga berasaskan Jumlah**.

Fungsi harga yang diperolehi secara dinamik berdasarkan persediaan dimensi untuk harga belian subkontraktor adalah serupa dengan bagaimana kos dan kadar bil diperolehi untuk pekerja sepenuh masa. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Mencipta tugasan tugas untuk mendapatkan anggaran kos sumber subkontraktor

Tugasan tugas untuk subkontraktor boleh dibuat dalam dua cara: 
- Menggunakan tab **Tugas**.
- **Menggunakan tab Pasukan**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Mencipta tugasan sumber menggunakan tab Tugas
**Menggunakan senarai Sumber** dalam **tab Tugas** untuk tugas tertentu, anda boleh mencipta tugasan tugas untuk sumber bernama atau sumber generik. Jika anda memilih sumber bernama daripada **juntai bawah Sumber** ditugaskan pada tugas dan sumber ini ialah pekerja kontrak, sumber yang dinamakan ditugaskan kepada tugas dan rekod ahli pasukan projek yang sepadan dicipta dengan jenis pekerja yang ditetapkan kepada **Pekerja** Kontrak dan **Kesahan** ditetapkan kepada **Tidak Sah**. Sebagai langkah seterusnya, anda perlu membuka rekod ahli pasukan projek dan memilih garis subkontrak dan subkontrak. Ini akan mengemas kini tugasan tugas untuk mempunyai rujukan kepada baris subkontrak dan subkontrak dan juga akan mengemas kini status ahli pasukan kepada **Sah**.

Jika anda memilih untuk mencipta ahli pasukan generik daripada **juntai bawah Sumber** yang Ditugaskan pada tugas, **dialog penciptaan** ahli pasukan generik akan membolehkan anda memilih garis subkontrak dan subkontrak. Apabila sumber generik diberikan kepada tugas dan rekod ahli pasukan projek yang sepadan dicipta, anda akan melihat bahawa rekod ahli pasukan projek dicipta dengan jenis pekerja ditetapkan kepada **Pekerja Kontrak dan** Kesahan **ditetapkan kepada** Sah **·**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Mencipta ahli pasukan projek menggunakan tab Pasukan
Menggunakan tab Pasukan pada projek, anda boleh mencipta generik atau ahli pasukan yang dinamakan. Apabila mencipta ahli pasukan, anda boleh memilih garis subkontrak dan subkontrak. Selepas ahli pasukan dicipta, anda perlu menugaskan ahli pasukan kepada tugas menggunakan **juntai bawah Sumber** yang Ditugaskan pada tugas. 

## <a name="updating-estimates"></a>Mengemas kini anggaran
Selepas anda menugaskan ahli pasukan projek kepada tugas, anda perlu menavigasi ke **tab Anggaran** pada projek dan pilih **Kemas kini harga** untuk memastikan bahawa kadar kos tugasan sumber subkontraktor dikemas kini berdasarkan senarai harga pembelian yang dilampirkan pada subkontrak. Anggaran tidak dijana untuk tugas yang tidak ditugaskan dalam Microsoft Dynamics 365 Project Operations. Akibatnya, anda perlu membuat tugasan tugas untuk harga dan kos pelbagai tugas pada projek anda. 

> [NOTA!] Ahli pasukan projek yang mempunyai **jenis** Pekerja sebagai **pekerja** kontrak tetapi tidak mempunyai rujukan subkontrak dibenderakan sebagai **Tidak Sah** pada **grid ahli** pasukan Projek. Jika terdapat mana-mana ahli pasukan projek dengan status ini, buka rekod ahli pasukan projek dan kemas kini medan baris subkontrak dan subkontrak secara manual supaya anggaran kos kewangan mencerminkan kos subkontraktor dengan tepat pada **tab Anggaran**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
