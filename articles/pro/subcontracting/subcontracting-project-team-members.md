---
title: Ahli pasukan projek subkontrak
description: Artikel ini menerangkan cara subkontrak ahli pasukan projek dalam Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 9/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a2f17d6f270029e3a517e99c7bb518cdb19b8d23
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522807"
---
# <a name="subcontracting-project-team-members"></a>Ahli pasukan projek subkontrak

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Dalam Microsoft Dynamics 365 Project Operations, anda boleh memilih untuk subkontrak ahli pasukan projek yang tidak ditapis atau dikendalikan.

- Ahli pasukan projek yang tidak terjejas mempunyai sumber generik yang diberikan.
- Ahli pasukan kakitangan mempunyai sumber yang dinamakan yang diberikan.

Apabila anda memautkan ahli pasukan projek ke baris subkontrak, sebarang tugasan kepada tugas yang ahli pasukan telah akan dipulihkan berdasarkan senarai harga belian yang dilampirkan pada subkontrak.  Pada tab **Anggaran** pada **halaman Butiran** Projek, pilih butang **Kemas kini harga** untuk melihat harga dan/atau kos yang dikemas kini hasil daripada keputusan untuk subkontrak. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subkontrak ahli pasukan projek yang tidak terjejas
Halaman **butiran** Ahli Pasukan mempunyai medan garis subkontrak dan subkontrak yang membolehkan pengurus projek menyatakan cara mereka ingin menarik kapasiti yang diperlukan daripada subkontrak. Untuk subkontrak ahli pasukan projek sebagai sumber generik, ikuti langkah berikut:

1.  Pilih subkontrak pada **halaman Butiran** ahli pasukan.

2.  Anda hanya boleh memilih subkontrak dengan **Draf** atau **status disahkan**. **Subkontrak tertutup** atau **Dibatalkan** tidak boleh dipilih. 

3.  Medan **garis** Subkontrak boleh dilihat selepas anda memilih subkontrak.

4.  Dalam medan **garis** Subkontrak, anda hanya boleh memilih garis subkontrak yang sesuai untuk masa. Anda tidak boleh memilih garis subkontrak untuk perbelanjaan atau bahan.

5.  Peranan untuk rekod ahli pasukan projek perlu sepadan dengan peranan pada garis subkontrak. Ini memastikan bahawa masa untuk peranan yang dianggarkan pada projek adalah peranan yang sama yang dibeli di garis subkontrak. 

Apabila ahli pasukan generik dikaitkan dengan garis subkontrak dan subkontrak, **medan jenis** Pekerja pada baris ahli pasukan generik akan dikemas kini kepada **Pekerja** Kontrak dan **Kesahan** Subkontrak akan ditetapkan kepada **Sah**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subkontrak ahli pasukan projek kakitangan
Seperti ahli pasukan generik atau tidak terjejas, kapasiti ahli pasukan kakitangan yang diperlukan pada projek juga boleh dikaitkan dengan subkontrak. Untuk subkontrak ahli pasukan projek yang dinamakan, ikuti langkah berikut:

1.  Pastikan sumber yang dinamakan disediakan sebagai jenis sumber boleh ditempah pekerja kontrak. Selain itu **, pastikan medan Vendor** pada sumber boleh ditempah sepadan dengan vendor pada subkontrak yang anda pilih. 

2.  Anda hanya boleh memilih subkontrak dalam **Draf** atau **status disahkan**. **Subkontrak tertutup** atau **Dibatalkan** tidak boleh dipilih. 

3.  Medan **garis** Subkontrak boleh dilihat selepas anda memilih subkontrak.

4.  Dalam medan **garis** Subkontrak, anda hanya boleh memilih garis subkontrak yang sesuai untuk masa. Anda tidak boleh memilih garis subkontrak untuk perbelanjaan atau bahan.

5.  Peranan untuk rekod ahli pasukan projek perlu sepadan dengan peranan pada garis subkontrak. Ini memastikan bahawa masa untuk peranan yang dianggarkan pada projek adalah peranan yang sama yang dibeli di garis subkontrak. 

Ahli pasukan projek yang dinamakan yang ditubuhkan sebagai jenis **pekerja kontrak sumber** Boleh Ditempah akan ditunjukkan dengan status **kesahan subkontrak tidak sah** jika mereka tidak dikaitkan dengan subkontrak. Apabila ahli pasukan projek yang dinamakan dikaitkan dengan garis subkontrak dan subkontrak, **medan Jenis** Pekerja dalam baris ahli pasukan akan dikemas kini kepada **Pekerja** Kontrak dan **Kesahan** Subkontrak akan ditetapkan kepada **Sah**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
