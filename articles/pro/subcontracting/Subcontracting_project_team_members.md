---
title: Subkontrak ahli pasukan projek
description: Topik ini menerangkan cara subkontrak ahli pasukan projek dalam Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 846de9afab5bf9ebc13670abd6ce735801796f0e
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903068"
---
# <a name="subcontracting-project-team-members"></a>Subkontrak ahli pasukan projek

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Dalam Dynamics 365 Project Operations Microsoft, anda boleh memilih untuk subkontrak ahli pasukan projek yang tidak terjejas atau kakitangan.

- Ahli pasukan projek yang tidak terjejas mempunyai sumber generik yang diberikan.
- Ahli pasukan yang dikendalikan mempunyai sumber bernama yang ditugaskan.

Apabila anda memautkan ahli pasukan projek ke talian subkontrak, sebarang tugasan kepada tugas yang ahli pasukan akan dicas semula berdasarkan senarai harga pembelian yang dilampirkan pada subkontrak.  Pada **tab Anggaran** pada halaman Butiran **Projek**, pilih butang Kemas kini harga **untuk melihat harga** dan/atau kos yang dikemas kini hasil daripada keputusan untuk subkontrak. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subkontrak ahli pasukan projek yang tidak terjejas
**Halaman butiran Ahli Pasukan mempunyai medan garis** subkontrak dan subkontrak yang membolehkan pengurus projek menyatakan cara mereka ingin menarik kapasiti yang diperlukan daripada subkontrak. Untuk subkontrak ahli pasukan projek sebagai sumber generik, ikuti langkah-langkah berikut:

1.  Pilih subkontrak pada **halaman butiran ahli** Pasukan.

2.  Anda hanya boleh memilih subkontrak dengan **Draf** atau Status **Disahkan**. **Subkontrak** tertutup atau **Dibatalkan tidak** boleh dipilih. 

3.  **Medan Garis subkontrak** menjadi kelihatan selepas anda memilih subkontrak.

4.  Dalam **medan Garis subkontrak,** anda hanya boleh memilih garis subkontrak yang untuk masa. Anda tidak boleh memilih garis subkontrak untuk perbelanjaan atau bahan.

5.  Peranan untuk rekod ahli pasukan projek perlu sepadan dengan peranan pada garis subkontrak. Ini memastikan bahawa masa untuk peranan yang dianggarkan pada projek adalah peranan yang sama yang dibeli pada garis subkontrak. 

Apabila ahli pasukan generik dikaitkan dengan garis subkontrak dan subkontrak, **medan jenis Pekerja pada baris ahli pasukan generik akan dikemas kini kepada Pekerja Kontrak dan** **·** **Kesahan Subkontrak** akan ditetapkan kepada **Sah**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subkontrak ahli pasukan projek kakitangan
Seperti ahli pasukan generik atau tidak terjejas, kapasiti ahli pasukan kakitangan yang diperlukan dalam projek juga boleh dikaitkan dengan subkontrak. Untuk subkontrak ahli pasukan projek yang dinamakan, ikut langkah ini:

1.  Pastikan sumber yang dinamakan disediakan sebagai jenis pekerja kontrak sumber boleh ditempah. Selain itu, pastikan **medan Vendor pada sumber boleh ditempah sepadan dengan vendor pada** subkontrak yang anda pilih. 

2.  Anda hanya boleh memilih subkontrak dalam **Draf** atau Status **Disahkan**. **Subkontrak** tertutup atau **Dibatalkan tidak** boleh dipilih. 

3.  **Medan Garis subkontrak** menjadi kelihatan selepas anda memilih subkontrak.

4.  Dalam **medan Garis subkontrak,** anda hanya boleh memilih garis subkontrak yang untuk masa. Anda tidak boleh memilih garis subkontrak untuk perbelanjaan atau bahan.

5.  Peranan untuk rekod ahli pasukan projek perlu sepadan dengan peranan pada garis subkontrak. Ini memastikan bahawa masa untuk peranan yang dianggarkan pada projek adalah peranan yang sama yang dibeli pada garis subkontrak. 

Ahli pasukan projek bernama yang ditubuhkan sebagai pekerja kontrak jenis **sumber boleh ditempah akan ditunjukkan dengan status** kesahan subkontrak **Tidak sah jika mereka tidak** dikaitkan dengan subkontrak. Apabila ahli pasukan projek yang dinamakan dikaitkan dengan garis subkontrak dan subkontrak, **medan jenis Pekerja dalam baris ahli pasukan akan dikemas kini kepada Pekerja Kontrak dan** **·** **Kesahan Subkontrak** akan ditetapkan kepada **Sah**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
