---
title: Ahli pasukan projek subkontrak
description: Artikel ini menerangkan cara untuk membuat subkontrak bagi ahli pasukan projek dalam Microsoft Dynamics 365 Project Operations.
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

Dalam Microsoft Dynamics 365 Project Operations, anda boleh memilih untuk subkontrak tanpa kakitangan atau ahli pasukan projek.

- Ahli pasukan projek tanpa kakitangan mempunyai sumber generik yang diuntukkan.
- Ahli pasukan dengan kakitangan mempunyai sumber bernama yang diuntukkan.

Apabila anda memautkan ahli pasukan projek pada baris subkontrak, sebarang tugasan kepada tugas yang ahli pasukan tersebut akan dikira kos semula berdasarkan senarai harga pembelian yang dilampirkan pada subkontrak.  Pada tab **Anggarkan** pada halaman **Butiran Projek**, pilih butang **Kemas kini harga** untuk melihat harga yang dikemas kini dan/atau kos yang terhasil daripada keputusan untuk membuat subkontrak. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Membuat subkontrak bagi ahli pasukan projek tanpa kakitangan
Halaman **Butiran Ahli Pasukan** mempunyai medan subkontrak dan baris subkontrak yang membenarkan pengurus projek untuk menyatakan cara mereka mahu menarik kapasiti yang diperlukan daripada subkontrak. Untuk membuat subkontrak bagi ahli pasukan projek sebagai sumber generik, ikut langkah ini:

1.  Pilih subkontrak pada halaman **Butiran ahli pasukan**.

2.  Anda hanya boleh memilih subkontrak dengan status **Draf** atau **Disahkan**. Subkontrak **Ditutup** atau **Dibatalkan** tidak boleh dipilih. 

3.  Medan **Baris subkontrak** menjadi boleh dilihat selepas anda memilih subkontrak.

4.  Dalam medan **Baris subkontrak**, anda hanya boleh memilih baris subkontrak yang ada untuk masa. Anda tidak boleh memilih baris subkontrak untuk perbelanjaan atau bahan.

5.  Peranan untuk rekod ahli pasukan projek perlu sepadan dengan peranan pada baris subkontrak. Ini memastikan bahawa masa untuk peranan yang dianggarkan pada projek ialah peranan sama yang dibeli pada baris subkontrak. 

Apabila ahli pasukan generik dikaitkan dengan baris subkontrak dan subkontrak, medan **Jenis pekerja** pada baris ahli pasukan generik akan dikemas kini kepada **Pekerja Kontrak** dan **Kesahan subkontrak** akan ditetapkan kepada **Sah**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Membuat subkontrak bagi ahli pasukan projek dengan kakitangan
Seperti ahli pasukan generik atau tanpa kakitangan, kapasiti ahli pasukan dengan kakitangan yang diperlukan pada projek juga boleh dikaitkan dengan subkontrak. Untuk membuat subkontrak bagi ahli pasukan projek bernama, ikut langkah ini:

1.  Pastikan sumber bernama ditetapkan sebagai jenis pekerja kontrak sumber boleh ditempah. Selain itu, pastikan medan **Vendor** pada sumber boleh ditempah sepadan dengan vendor pada subkontrak yang anda pilih. 

2.  Anda hanya boleh memilih subkontrak dengan status dalam **Draf** atau **Disahkan**. Subkontrak **Ditutup** atau **Dibatalkan** tidak boleh dipilih. 

3.  Medan **Baris subkontrak** menjadi boleh dilihat selepas anda memilih subkontrak.

4.  Dalam medan **Baris subkontrak**, anda hanya boleh memilih baris subkontrak yang ada untuk masa. Anda tidak boleh memilih baris subkontrak untuk perbelanjaan atau bahan.

5.  Peranan untuk rekod ahli pasukan projek perlu sepadan dengan peranan pada baris subkontrak. Ini memastikan bahawa masa untuk peranan yang dianggarkan pada projek ialah peranan sama yang dibeli pada baris subkontrak. 

Ahli pasukan projek bernama yang ditetapkan sebagai jenis pekerja kontrak **Sumber boleh ditempah** akan ditunjukkan dengan status kesahan subkontrak **Tidak sah** jika tidak dikaitkan dengan subkontrak. Apabila ahli pasukan projek bernama dikaitkan dengan baris subkontrak dan subkontrak, medan **Jenis pekerja** dalam baris ahli pasukan akan dikemas kini kepada **Pekerja Kontrak** dan **Kesahan subkontrak** akan ditetapkan kepada **Sah**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
