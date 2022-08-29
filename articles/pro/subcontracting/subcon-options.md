---
title: Pilihan subkontrak untuk ahli pasukan projek
description: Artikel ini menerangkan opsyen subkontrak untuk ahli pasukan projek dalam Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5e0955d58365a4ecbe1c053882736f196758816e
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261618"
---
# <a name="subcontracting-options-for-project-team-members"></a>Pilihan subkontrak untuk ahli pasukan projek

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Dalam Microsoft Dynamics 365 Project Operations, anda boleh menilai opsyen subkontrak yang tersedia untuk satu atau lebih ahli pasukan projek. Opsyen subkontrak yang tersedia membolehkan anda:

- Cipta subkontrak baru dan/atau cipta baris baru pada subkontrak sedia ada untuk ahli pasukan projek yang dipilih. 
- Rizab terhadap garis subkontrak dan subkontrak yang sedia ada. 

Anda boleh memilih daripada opsyen subkontrak yang tersedia untuk ahli pasukan projek generik atau memilih daripada ahli pasukan projek yang telah dikendalikan dengan sumber bernama yang merupakan pekerja kontrak. 

Tiada opsyen subkontrak tersedia untuk yang berikut:

- Ahli pasukan projek yang telah dianggotai oleh pekerja. 
- Ahli pasukan projek yang telah dikaitkan dengan subkontrak dan garis subkontrak. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subkontrak ahli pasukan projek yang tidak terjejas

Untuk menyemak semula dan memilih daripada opsyen subkontrak yang tersedia untuk ahli pasukan projek umum atau tidak ditapis, ikuti langkah berikut:

1. Pilih satu atau lebih rekod ahli pasukan projek di mana sumber adalah sumber generik.
2. Memastikan tiada rekod ahli pasukan projek yang dipilih telah disubkontrak. 
3. Pilih **Opsyen subkontrak** pada sub grid ahli pasukan projek. Dialog **opsyen** Subkontrak terbuka. 
4. Jika anda hanya memilih satu rekod ahli pasukan projek dalam langkah 1, maka opsyen berikut akan tersedia:
    - Buat baris subkontrak baru. 
    - Tempah terhadap subkontrak sedia ada Jika anda memilih berbilang rekod ahli pasukan projek dalam langkah 1, maka satu-satunya pilihan yang tersedia ialah mencipta garis subkontrak baharu.
5. Pilihan untuk menempah terhadap garis subkontrak sedia ada membolehkan anda memilih garis subkontrak dan subkontrak yang ingin anda simpan. Apabila memilih garis subkontrak untuk kapasiti rizab, anda harus memastikan bahawa garis subkontrak yang dipilih adalah untuk masa dan peranan yang diperlukan pada ahli pasukan projek sepadan dengan peranan yang dibeli pada garis subkontrak.
6. Apabila anda memilih untuk mencipta baris subkontrak baru untuk ahli pasukan projek, sistem akan membolehkan anda memilih subkontrak yang anda ingin cipta baris ini. Subkontrak yang anda pilih untuk mencipta baris baru hendaklah dalam **status Draf**. Dengan pilihan ini untuk mencipta baris subkontrak baru untuk ahli pasukan projek yang dipilih, sistem akan mencipta satu garis subkontrak untuk masa untuk setiap ahli pasukan projek. Peranan, jam dan tarikh akan disalin daripada ahli pasukan projek kepada setiap baris subkontrak yang dicipta. 
7. Apabila ahli pasukan generik dikaitkan dengan garis subkontrak dan subkontrak, **medan jenis** Pekerja pada baris ahli pasukan generik akan dikemas kini kepada **Pekerja** Kontrak dan **nilai Kesahan** Subkontrak akan ditetapkan kepada **Sah**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subkontrak ahli pasukan projek kakitangan

Seperti ahli pasukan generik atau tidak terjejas, anda juga boleh melihat pilihan subkontrak untuk ahli pasukan projek kakitangan selagi ahli pasukan kakitangan adalah pekerja kontrak. Untuk menyemak semula dan memilih opsyen subkontrak yang tersedia untuk kakitangan atau ahli pasukan projek bernama, ikuti langkah berikut:

1. Pilih satu atau lebih rekod ahli pasukan projek di mana sumber adalah pekerja kontrak yang dinamakan.
2. Memastikan tiada rekod ahli pasukan projek yang dipilih telah disubkontrak. 
3. Pilih **Opsyen subkontrak** pada sub grid ahli pasukan projek. Dialog **opsyen** Subkontrak terbuka. 
4. Jika anda hanya memilih satu rekod ahli pasukan projek dalam langkah 1, maka opsyen berikut akan tersedia:
      - Buat baris subkontrak baru.
      - Rizab terhadap subkontrak sedia ada.
  Jika anda memilih berbilang rekod ahli pasukan projek dalam langkah 1, maka satu-satunya opsyen yang tersedia ialah mencipta garis subkontrak baru.
5. Pilihan untuk menempah terhadap garis subkontrak sedia ada membolehkan anda memilih garis subkontrak dan subkontrak yang ingin anda simpan. Apabila memilih garis subkontrak untuk kapasiti rizab, anda harus memastikan perkara berikut:
      - Garis subkontrak yang dipilih adalah untuk masa. 
      - Peranan yang diperlukan pada ahli pasukan projek sepadan dengan peranan yang dibeli di garisan subkontrak. 
      - Vendor yang dikaitkan dengan pekerja kontrak adalah sama dengan vendor di subkontrak.
6. Apabila anda memilih untuk mencipta baris subkontrak baru untuk ahli pasukan projek, sistem akan membolehkan anda memilih subkontrak yang anda ingin cipta baris ini. Dengan pilihan ini, anda harus memastikan bahawa vendor yang dimiliki oleh pekerja kontrak adalah sama dengan vendor di subkontrak. 
7. Subkontrak yang anda pilih untuk mencipta baris baru hendaklah dalam **status Draf**. Dengan pilihan ini untuk mencipta baris subkontrak baru untuk ahli pasukan projek yang dipilih, sistem akan mencipta satu garis subkontrak untuk masa untuk setiap ahli pasukan projek. Peranan, jam dan tarikh akan disalin daripada ahli pasukan projek kepada setiap baris subkontrak yang dicipta.  
8. Apabila ahli pasukan yang dinamakan dikaitkan dengan garis subkontrak dan subkontrak, **medan Jenis** Pekerja pada baris ahli pasukan yang dinamakan akan dikemas kini kepada **Pekerja** Kontrak dan **nilai Kesahan** Subkontrak akan ditetapkan kepada **Sah**.

## <a name="re-costing-subcontractor-assignments"></a>Kos semula tugasan subkontraktor

Apabila ahli pasukan projek (generik atau dinamakan) dipautkan kepada baris subkontrak menggunakan **dialog Opsyen** Subkontrak, sebarang tugasan kepada tugas yang ahli pasukan telah akan dikenakan biaya semula berdasarkan senarai harga belian yang dilampirkan pada subkontrak. Pada tab **Anggaran** pada **halaman Butiran** Projek, pilih butang **Kemas kini harga** untuk melihat harga dan/atau kos yang dikemas kini hasil daripada keputusan untuk subkontrak.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
