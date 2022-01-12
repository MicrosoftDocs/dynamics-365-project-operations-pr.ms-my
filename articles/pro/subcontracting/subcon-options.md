---
title: Opsyen subkontrak untuk ahli pasukan projek
description: Topik ini menerangkan pilihan subkontrak untuk ahli pasukan projek dalam Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 4db283db728b50ccf76eafabfd643313620bbce2
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903737"
---
# <a name="subcontracting-options-for-project-team-members"></a>Opsyen subkontrak untuk ahli pasukan projek

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Dalam Dynamics 365 Project Operations Microsoft, anda boleh menilai pilihan subkontrak yang tersedia untuk satu atau lebih ahli pasukan projek. Pilihan subkontrak yang ada membolehkan anda:

- Cipta subkontrak baru dan/atau cipta baris baru pada subkontrak sedia ada untuk ahli pasukan projek yang dipilih. 
- Rizab terhadap garis subkontrak dan subkontrak yang sedia ada. 

Anda boleh memilih daripada pilihan subkontrak yang ada untuk ahli pasukan projek generik atau memilih daripada ahli pasukan projek yang telah dikendalikan dengan sumber bernama yang merupakan pekerja kontrak. 

Tiada opsyen subkontrak tersedia untuk yang berikut:

- Ahli pasukan projek yang telah dikendalikan dengan pekerja. 
- Ahli pasukan projek yang telah dikaitkan dengan garis subkontrak dan subkontrak. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subkontrak ahli pasukan projek yang tidak terjejas

Untuk menyemak dan memilih daripada pilihan subkontrak yang tersedia untuk ahli pasukan projek generik atau tidak terjejas, ikuti langkah-langkah ini:

1. Pilih satu atau lebih rekod ahli pasukan projek di mana sumber adalah sumber generik.
2. Pastikan tiada rekod ahli pasukan projek yang dipilih telah dikontrak. 
3. Pilih **Opsyen Subkontrak** pada sub grid ahli pasukan projek. Dialog **Opsyen Subkontrak** dibuka. 
4. Jika anda hanya memilih satu rekod ahli pasukan projek dalam langkah 1, maka pilihan berikut akan tersedia:
    - Cipta garis subkontrak baru. 
    - Rizab terhadap subkontrak sedia ada Jika anda memilih berbilang rekod ahli pasukan projek dalam langkah 1, maka satu-satunya pilihan yang tersedia adalah untuk mencipta garis subkontrak baru.
5. Pilihan untuk membuat rizab terhadap garis subkontrak sedia ada membolehkan anda memilih garis subkontrak dan subkontrak yang anda ingin simpan. Apabila memilih garis subkontrak untuk menyimpan kapasiti, anda harus memastikan bahawa garis subkontrak yang dipilih adalah untuk masa dan peranan yang diperlukan pada ahli pasukan projek sepadan dengan peranan yang dibeli pada garis subkontrak.
6. Apabila anda memilih untuk mencipta garis subkontrak baru untuk ahli pasukan projek, sistem akan membolehkan anda memilih subkontrak yang anda ingin cipta baris ini. Subkontrak yang anda pilih untuk mencipta baris baru hendaklah dalam **status** Draf. Dengan pilihan ini untuk mencipta garis subkontrak baru untuk ahli pasukan projek yang dipilih, sistem akan mencipta satu garis subkontrak untuk masa untuk setiap ahli pasukan projek. Peranan, jam dan tarikh akan disalin daripada ahli pasukan projek kepada setiap baris subkontrak yang dicipta. 
7. Apabila ahli pasukan generik dikaitkan dengan garis subkontrak dan subkontrak, **medan jenis Pekerja pada baris ahli pasukan generik akan dikemas kini kepada Pekerja Kontrak dan** nilai **·** **Kesahan Subkontrak** akan ditetapkan kepada **Sah**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subkontrak ahli pasukan projek kakitangan

Seperti ahli pasukan generik atau tidak terjejas, anda juga boleh melihat pilihan subkontrak untuk ahli pasukan projek kakitangan selagi ahli pasukan kakitangan adalah pekerja kontrak. Untuk menyemak dan memilih daripada pilihan subkontrak yang tersedia untuk ahli pasukan projek yang dikendalikan atau dinamakan, ikut langkah ini:

1. Pilih satu atau lebih rekod ahli pasukan projek di mana sumber adalah pekerja kontrak bernama.
2. Pastikan tiada rekod ahli pasukan projek yang dipilih telah dikontrak. 
3. Pilih **Opsyen Subkontrak** pada sub grid ahli pasukan projek. Dialog **Opsyen Subkontrak** dibuka. 
4. Jika anda hanya memilih satu rekod ahli pasukan projek dalam langkah 1, maka pilihan berikut akan tersedia:
      - Cipta garis subkontrak baru.
      - Rizab terhadap subkontrak yang sedia ada.
  Jika anda memilih berbilang rekod ahli pasukan projek dalam langkah 1, maka satu-satunya pilihan yang tersedia adalah untuk membuat garis subkontrak baru.
5. Pilihan untuk membuat rizab terhadap garis subkontrak sedia ada membolehkan anda memilih garis subkontrak dan subkontrak yang anda ingin simpan. Apabila memilih garis subkontrak untuk menyimpan kapasiti, anda harus memastikan perkara berikut:
      - Garis subkontrak yang dipilih adalah untuk masa. 
      - Peranan yang diperlukan pada ahli pasukan projek sepadan dengan peranan yang dibeli pada garis subkontrak. 
      - Vendor yang pekerja kontrak dikaitkan adalah sama dengan vendor di subkontrak.
6. Apabila anda memilih untuk mencipta garis subkontrak baru untuk ahli pasukan projek, sistem akan membolehkan anda memilih subkontrak yang anda ingin cipta baris ini. Dengan pilihan ini, anda harus memastikan bahawa vendor yang dimiliki oleh pekerja kontrak adalah sama dengan vendor di subkontrak. 
7. Subkontrak yang anda pilih untuk mencipta baris baru hendaklah dalam **status** Draf. Dengan pilihan ini untuk mencipta garis subkontrak baru untuk ahli pasukan projek yang dipilih, sistem akan mencipta satu garis subkontrak untuk masa untuk setiap ahli pasukan projek. Peranan, jam dan tarikh akan disalin daripada ahli pasukan projek kepada setiap baris subkontrak yang dicipta.  
8. Apabila ahli pasukan bernama dikaitkan dengan garis subkontrak dan subkontrak, **medan jenis Pekerja pada baris ahli pasukan yang** dinamakan akan dikemas kini kepada Pekerja **Kontrak dan nilai** **Kesahan Subkontrak** akan ditetapkan kepada **Sah**.

## <a name="re-costing-subcontractor-assignments"></a>Kos semula tugasan subkontraktor

Apabila ahli pasukan projek (generik atau dinamakan) dipautkan ke garis subkontrak menggunakan **dialog Opsyen Subkontrak,** sebarang tugasan kepada tugas yang ahli pasukan akan ditimbang semula berdasarkan senarai harga pembelian yang dilampirkan pada subkontrak. Pada **tab Anggaran** pada halaman Butiran **Projek**, pilih butang Kemas kini harga **untuk melihat harga** dan/atau kos yang dikemas kini hasil daripada keputusan untuk subkontrak.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
