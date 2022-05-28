---
title: Ahli pasukan projek subkontrak
description: Topik ini menerangkan cara subkontrak ahli pasukan projek dalam Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f43f817e59ef83fbf4dda6267327080f7c56e0f7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587857"
---
# <a name="subcontracting-project-team-members"></a>Ahli pasukan projek subkontrak

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Dalam Microsoft Dynamics 365 Project Operations, anda boleh memilih untuk subkontrak ahli pasukan projek tanpa kakitangan atau kakitangan.

- Ahli pasukan projek yang tidak mempunyai kakitangan mempunyai sumber generik yang diberikan.
- Ahli pasukan kakitangan mempunyai sumber bernama yang ditugaskan.

Apabila anda memautkan ahli pasukan projek kepada baris subkontrak, sebarang tugasan kepada tugas yang dimiliki oleh ahli pasukan akan dijejaskan semula berdasarkan senarai harga pembelian yang dilampirkan pada subkontrak.  **Pada tab Anggaran** pada **halaman Butiran** Projek, pilih **butang Kemas Kini harga** untuk melihat harga yang dikemas kini dan/atau kos yang terhasil daripada keputusan untuk subkontrak. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subkontrak ahli pasukan projek yang tidak mempunyai kakitangan
Halaman **butiran** Ahli Pasukan mempunyai medan subkontrak dan subkontrak yang membolehkan pengurus projek menyatakan bagaimana mereka ingin menarik kapasiti yang diperlukan daripada subkontrak. Untuk subkontrak ahli pasukan projek sebagai sumber generik, ikuti langkah berikut:

1.  Pilih subkontrak pada **halaman butiran** ahli Pasukan.

2.  Anda hanya boleh memilih subkontrak dengan **status Draf** atau **Disahkan**. **Subkontrak tertutup** atau **dibatalkan** tidak boleh dipilih. 

3.  Medan **baris** Subkontrak menjadi kelihatan selepas anda memilih subkontrak.

4.  **Dalam medan Baris** Subkontrak, anda hanya boleh memilih baris subkontrak yang sesuai untuk masa. Anda tidak boleh memilih baris subkontrak untuk perbelanjaan atau bahan.

5.  Peranan untuk rekod ahli pasukan projek perlu sepadan dengan peranan pada baris subkontrak. Ini memastikan bahawa masa untuk peranan yang dianggarkan pada projek adalah peranan yang sama yang dibeli pada garis subkontrak. 

Apabila ahli pasukan generik dikaitkan dengan subkontrak dan subkontrak, **medan jenis** Pekerja pada baris ahli pasukan generik akan dikemas kini kepada **Pekerja** Kontrak dan **Kesahan** Subkontrak akan ditetapkan kepada **Sah**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subkontrak ahli pasukan projek kakitangan
Seperti ahli pasukan generik atau tanpa kakitangan, kapasiti ahli pasukan kakitangan yang diperlukan pada projek juga boleh dikaitkan dengan subkontrak. Untuk subkontrak ahli pasukan projek yang dinamakan, ikuti langkah berikut:

1.  Pastikan sumber yang dinamakan disediakan sebagai jenis sumber yang boleh ditempah oleh pekerja kontrak. Juga, pastikan **medan Vendor** pada sumber yang boleh ditempah sepadan dengan vendor pada subkontrak yang anda pilih. 

2.  Anda hanya boleh memilih subkontrak dalam **status Draf** atau **Disahkan**. **Subkontrak tertutup** atau **dibatalkan** tidak boleh dipilih. 

3.  Medan **baris** Subkontrak menjadi kelihatan selepas anda memilih subkontrak.

4.  **Dalam medan Baris** Subkontrak, anda hanya boleh memilih baris subkontrak yang sesuai untuk masa. Anda tidak boleh memilih baris subkontrak untuk perbelanjaan atau bahan.

5.  Peranan untuk rekod ahli pasukan projek perlu sepadan dengan peranan pada baris subkontrak. Ini memastikan bahawa masa untuk peranan yang dianggarkan pada projek adalah peranan yang sama yang dibeli pada garis subkontrak. 

Ahli pasukan projek yang dinamakan yang ditubuhkan sebagai jenis **pekerja kontrak sumber** Boleh Ditempah akan ditunjukkan dengan status **kesahan subkontrak Tidak sah** jika mereka tidak dikaitkan dengan subkontrak. Apabila ahli pasukan projek yang dinamakan dikaitkan dengan subkontrak dan subkontrak, **medan jenis** Pekerja dalam baris ahli pasukan akan dikemas kini kepada **Pekerja** Kontrak dan **Kesahan** Subkontrak akan ditetapkan kepada **Sah**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
