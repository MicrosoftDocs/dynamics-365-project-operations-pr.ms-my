---
title: Pilihan subkontrak untuk ahli pasukan projek
description: Artikel ini menerangkan pilihan subkontrak untuk ahli pasukan projek dalam Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 046b5d38ef7e433d02e3eac2e858a3333e941c45
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522290"
---
# <a name="subcontracting-options-for-project-team-members"></a>Pilihan subkontrak untuk ahli pasukan projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Dalam Microsoft Dynamics 365 Project Operations, anda boleh menilai pilihan subkontrak yang tersedia untuk satu atau lebih ahli pasukan projek. Pilihan subkontrak yang tersedia membolehkan anda untuk:

- Mencipta subkontrak baharu dan/atau mencipta baris baharu pada subkontrak sedia ada untuk ahli pasukan projek yang dipilih. 
- Menempah terhadap subkontrak sedia ada dan baris subkontrak. 

Anda boleh memilih daripada pilihan subkontrak yang tersedia untuk ahli pasukan projek generik atau memilih daripada ahli pasukan projek yang telah dianggotai dengan sumber bernama yang merupakan pekerja kontrak. 

Tiada pilihan subkontrak tersedia untuk yang berikut:

- Ahli pasukan projek yang telah dianggotai dengan pekerja. 
- Ahli pasukan projek yang sudah dikaitkan dengan subkontrak dan baris subkontrak. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Membuat subkontrak bagi ahli pasukan projek tanpa kakitangan

Untuk menyemak dan memilih daripada pilihan subkontrak yang tersedia untuk ahli pasukan projek generik atau tanpa kakitangan, ikut langkah ini:

1. Pilih satu atau lebih rekod ahli pasukan projek yang sumber merupakan sumber generik.
2. Memastikan tiada rekod ahli pasukan projek yang terpilih sudah dikontrak. 
3. Pilih **Pilihan subkontrak** pada subgrid ahli pasukan projek. Dialog **Pilihan subkontrak** terbuka. 
4. Jika anda hanya memilih satu rekod ahli pasukan projek dalam langkah 1, maka pilihan berikut akan tersedia:
    - Cipta baris subkontrak baharu. 
    - Tempah terhadap subkontrak sedia ada jika anda memilih berbilang rekod ahli pasukan projek dalam langkah 1, maka satu-satunya pilihan tersedia untuk mencipta baris subkontrak baharu.
5. Pilihan untuk menempah terhadap baris subkontrak sedia ada membolehkan anda untuk memilih subkontrak dan baris subkontrak yang anda mahu tempah. Apabila memilih baris subkontrak untuk menempah kapasiti, anda perlu memastikan bahawa baris subkontrak dipilih adalah untuk masa dan bahawa peranan yang diperlukan pada ahli pasukan projek sepadan dengan peranan yang dibeli pada baris subkontrak.
6. Apabila anda memilih untuk mencipta baris subkontrak baharu untuk ahli pasukan projek, sistem akan membolehkan anda memilih subkontrak yang anda mahu cipta baris ini. Subkontrak yang anda pilih untuk mencipta baris baharu hendaklah dalam status **Draf**. Dengan pilihan ini untuk mencipta baris subkontrak baharu bagi ahli pasukan projek yang dipilih, sistem akan mencipta satu baris subkontrak masa untuk setiap ahli pasukan projek. Peranan, jam dan tarikh akan disalin daripada ahli pasukan projek ke setiap baris subkontrak yang dicipta. 
7. Apabila ahli pasukan generik dikaitkan dengan baris subkontrak dan subkontrak, medan **Jenis pekerja** pada baris ahli pasukan generik akan dikemas kini kepada **Pekerja Kontrak** dan nilai **Kesahan subkontrak** akan ditetapkan kepada **Sah**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Membuat subkontrak bagi ahli pasukan projek dengan kakitangan

Seperti ahli pasukan generik atau tanpa kakitangan, anda juga boleh melihat pilihan subkontrak untuk ahli pasukan projek kakitangan selagi ahli pasukan kakitangan ialah pekerja kontrak. Untuk menyemak dan memilih daripada pilihan subkontrak yang tersedia untuk ahli pasukan projek kakitangan atau nama, ikut langkah ini:

1. Pilih satu atau lebih rekod ahli pasukan projek yang sumber merupakan sumber kontrak bernama.
2. Memastikan tiada rekod ahli pasukan projek yang dipilih sudah dikontrak. 
3. Pilih **Pilihan subkontrak** pada subgrid ahli pasukan projek. Dialog **Pilihan subkontrak** terbuka. 
4. Jika anda hanya memilih satu rekod ahli pasukan projek dalam langkah 1, maka pilihan berikut akan tersedia:
      - Cipta baris subkontrak baharu.
      - Tempah pada subkontrak yang sedia ada
  Jika anda memilih berbilang rekod ahli pasukan projek dalam langkah 1, maka satu-satunya pilihan tersedia untuk mencipta baris subkontrak baharu.
5. Pilihan untuk menempah terhadap baris subkontrak sedia ada membolehkan anda untuk memilih subkontrak dan baris subkontrak yang anda mahu tempah. Apabila memilih baris subkontrak untuk menempah kapasiti, anda perlu memastikan perkara berikut:
      - Baris subkontrak yang dipilih adalah untuk masa. 
      - Peranan yang diperlukan pada ahli pasukan projek sepadan dengan peranan yang telah dibeli pada baris subkontrak. 
      - Vendor yang berkaitan dengan pekerja kontrak adalah sama dengan vendor pada subkontrak.
6. Apabila anda memilih untuk mencipta baris subkontrak baharu untuk ahli pasukan projek, sistem akan membolehkan anda memilih subkontrak yang anda mahu cipta baris ini. Dengan pilihan ini, anda hendaklah memastikan bahawa pekerja kontrak yang dimiliki vendor adalah sama dengan vendor pada subkontrak. 
7. Subkontrak yang anda pilih untuk mencipta baris baharu hendaklah dalam status **Draf**. Dengan pilihan ini untuk mencipta baris subkontrak baharu bagi ahli pasukan projek yang dipilih, sistem akan mencipta satu baris subkontrak masa untuk setiap ahli pasukan projek. Peranan, jam dan tarikh akan disalin daripada ahli pasukan projek ke setiap baris subkontrak yang dicipta.  
8. Apabila ahli pasukan bernama dikaitkan dengan baris subkontrak dan subkontrak, medan **Jenis pekerja** pada baris ahli pasukan bernama akan dikemas kini kepada **Pekerja Kontrak** dan nilai **Kesahan subkontrak** akan ditetapkan kepada **Sah**.

## <a name="re-costing-subcontractor-assignments"></a>Membuat kos semula pada tugas subkontraktor

Apabila ahli pasukan projek (generik atau bernama) dikaitkan dengan baris subkontrak menggunakan dialog **Pilihan subkontrak**, sebarang peruntukan untuk tugas yang dimiliki oleh ahli pasukan tersebut akan dikira semula kos berdasarkan senarai harga pembelian yang dilampirkan pada subkontrak. Pada tab **Anggarkan** pada halaman **Butiran Projek**, pilih butang **Kemas kini harga** untuk melihat harga yang dikemas kini dan/atau kos yang terhasil daripada keputusan untuk membuat subkontrak.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
