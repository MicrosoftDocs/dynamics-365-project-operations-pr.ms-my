---
title: Anggaran kos tugasan sumber yang disubkontrak
description: Artikel ini menerangkan tentang beberapa cara Microsoft Dynamics 365 Project Operations mengira anggaran kos bagi penugasan sumber subkontrak.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9fded1baa63d2defc134994c858dfc6c09f75082
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522667"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Anggaran kos tugasan sumber yang disubkontrak

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Penugasan tugas ahli pasukan projek subkontrak dikoskan menggunakan senarai harga **Pembelian** yang dilampirkan kepada subkontrak pada rekod ahli pasukan berkaitan. Ini berbeza daripada cara penugasan sumber pekerja dikoskan apabila penugasan tugas sumber pekerja dikoskan menggunakan senarai harga **Kos** yang dilampirkan kepada unit kontrak projek. 

Untuk ahli pasukan projek generik yang disubkontrak, penugasan dikoskan menggunakan persediaan harga berdasarkan peranan dalam senarai harga pembelian yang dilampirkan kepada subkontrak. Harga pembelian juga boleh ditetapkan khusus untuk setiap sumber. Harga yang khusus sumber ini akan diberi keutamaan apabila penugasan tugas pengekosan ahli pasukan projek yang dinamakan ialah pekerja kontrak. 

Keutamaan menggunakan harga pembelian khusus peranan berbanding khusus sumber didorong oleh persediaan keutamaan dimensi penetapan harga dalam **Parameter > Dimensi penentuan harga berdasarkan amaun.**.

Fungsi penentuan harga secara dinamik berdasarkan persediaan dimensi untuk pembelian harga subkontraktor adalah sama dengan cara kadar kos dan bil yang diperolehi untuk pekerja sepenuh masa. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Mencipta penugasan tugas untuk mendapatkan anggaran kos sumber subkontraktor

Penugasan tugas untuk subkontraktor boleh dicipta dalam dua cara: 
- Menggunakan tab **Tugas**.
- Menggunakan tab **Pasukan**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Mencipta penugasan sumber menggunakan tab Tugas
Dengan menggunakan senarai **Sumber** dalam tab **Tugas** untuk tugas khusus, anda boleh mencipta penugasan tugas untuk sumber yang dinamakan atau sumber generik. Jika anda memilih sumber yang dinamakan daripada juntai bawah **Sumber Ditugaskan** pada tugas dan sumber ini adalah pekerja kontrak, sumber yang dinamakan ditugaskan kepada tugas dan rekod ahli pasukan projek berkenaan dicipta dengan jenis pekerja ditetapkan kepada **Pekerja Kontrak** dan **Kesahihan** ditetapkan kepada **Tidak Sah**. Sebagai langkah seterusnya, anda perlu membuka rekod ahli pasukan projek dan memilih subkontrak dan baris subkontrak. Ini akan mengemas kini penugasan tugas untuk mempunyai rujukan kepada subkontrak dan baris subkontrak dan juga akan mengemas kini status ahli pasukan kepada **Sah**.

Jika anda memilih untuk mencipta ahli pasukan generik daripada juntai bawah **Sumber Ditugaskan** pada tugas, dialog **Penciptaan ahli pasukan generik** akan membolehkan anda memilih subkontrak dan baris subkontrak. Apabila sumber generik ditugaskan kepada tugas dan rekod ahli pasukan projek yang sepadan dicipta, anda akan dapati bahawa rekod ahli pasukan projek dicipta dengan jenis pekerja ditetapkan kepada **Pekerja Kontrak** dan **Kesahihan** ditetapkan kepada **Sah**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Mencipta ahli pasukan projek menggunakan tab Pasukan
Menggunakan tab Pasukan pada projek, anda boleh mencipta generik atau ahli pasukan yang dinamakan. Apabila mencipta ahli pasukan, anda boleh memilih subkontrak dan baris subkontrak. Selepas ahli pasukan dicipta, anda perlu menugaskan ahli pasukan kepada tugas menggunakan juntai bawah **Sumber Ditugaskan** pada tugas. 

## <a name="updating-estimates"></a>Mengemas kini anggaran
Selepas anda telah menugaskan ahli pasukan projek kepada tugas, anda perlu menavigasi ke tab **Anggaran** pada projek dan memilih **Kemas kini harga** untuk memastikan bahawa kadar kos bagi penugasan sumber subkontraktor dikemas kini berdasarkan senarai harga pembelian yang dilampirkan pada subkontrak. Anggaran tidak dijana untuk tugas yang tidak ditugaskan dalam Microsoft Dynamics 365 Project Operations. Oleh itu, anda perlu mencipta penugasan tugas kepada harga dan kos pelbagai tugas pada projek anda. 

> [NOTA!] Ahli pasukan projek yang mempunyai **Jenis pekerja** sebagai **Pekerja kontrak** tetapi tidak mempunyai rujukan subkontrak ditandakan sebagai **Tidak Sah** pada grid **Ahli pasukan projek**. Jika terdapat mana-mana ahli pasukan projek dengan status ini, buka rekod ahli pasukan projek dan kemas kini medan subkontrak dan baris subkontrak secara manual supaya anggaran kos kewangan menggambarkan kos subkontraktor dengan tepat pada tab **Anggarkan**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
