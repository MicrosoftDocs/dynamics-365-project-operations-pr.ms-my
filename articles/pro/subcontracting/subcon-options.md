---
title: Pilihan subkontrak untuk ahli pasukan projek
description: Artikel ini menerangkan opsyen subkontrak untuk ahli pasukan projek dalam Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 88a76ccf73a4b6cfa13a67b50130b007f244d831
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919795"
---
# <a name="subcontracting-options-for-project-team-members"></a>Pilihan subkontrak untuk ahli pasukan projek

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Dalam Microsoft Dynamics 365 Project Operations, anda boleh menilai pilihan subkontrak yang tersedia untuk satu atau lebih ahli pasukan projek. Pilihan subkontrak yang tersedia membolehkan anda:

- Cipta subkontrak baru dan/atau cipta baris baru pada subkontrak sedia ada untuk ahli pasukan projek yang dipilih. 
- Rizab terhadap garis subkontrak dan subkontrak yang sedia ada. 

Anda boleh memilih daripada pilihan subkontrak yang tersedia untuk ahli pasukan projek generik atau memilih daripada ahli pasukan projek yang telah dikendalikan dengan sumber bernama yang merupakan pekerja kontrak. 

Tiada opsyen subkontrak tersedia untuk yang berikut:

- Ahli pasukan projek yang telah dikendalikan dengan pekerja. 
- Ahli pasukan projek yang telah dikaitkan dengan garis subkontrak dan subkontrak. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subkontrak ahli pasukan projek yang tidak mempunyai kakitangan

Untuk menyemak dan memilih daripada opsyen subkontrak yang tersedia untuk ahli pasukan projek generik atau tidak kakitangan, ikuti langkah berikut:

1. Pilih satu atau lebih rekod ahli pasukan projek di mana sumber adalah sumber generik.
2. Pastikan tiada rekod ahli pasukan projek yang dipilih telah disubkontrakkan. 
3. Pilih **Opsyen subkontrak** pada sub grid ahli pasukan projek. Dialog **opsyen** Subkontrak dibuka. 
4. Jika anda hanya memilih satu rekod ahli pasukan projek dalam langkah 1, maka pilihan berikut akan tersedia:
    - Buat baris subkontrak baru. 
    - Rizab terhadap subkontrak sedia ada Jika anda memilih berbilang rekod ahli pasukan projek dalam langkah 1, maka satu-satunya pilihan yang tersedia ialah mencipta baris subkontrak baru.
5. Pilihan untuk menempah terhadap garis subkontrak sedia ada membolehkan anda memilih garis subkontrak dan subkontrak yang anda ingin simpan. Apabila memilih garis subkontrak untuk menyimpan kapasiti, anda harus memastikan bahawa garis subkontrak yang dipilih adalah untuk masa dan peranan yang diperlukan pada ahli pasukan projek sepadan dengan peranan yang dibeli pada baris subkontrak.
6. Apabila anda memilih untuk mencipta baris subkontrak baru untuk ahli pasukan projek, sistem akan membolehkan anda memilih subkontrak yang anda ingin cipta baris ini. Subkontrak yang anda pilih untuk mencipta baris baru hendaklah dalam **status Draf**. Dengan pilihan ini untuk mencipta baris subkontrak baru untuk ahli pasukan projek yang dipilih, sistem akan mencipta satu baris subkontrak untuk masa untuk setiap ahli pasukan projek. Peranan, jam dan tarikh akan disalin dari ahli pasukan projek ke setiap baris subkontrak yang dibuat. 
7. Apabila ahli pasukan generik dikaitkan dengan subkontrak dan subkontrak, **medan jenis** Pekerja pada baris ahli pasukan generik akan dikemas kini kepada **Pekerja** Kontrak dan **nilai Kesahan** Subkontrak akan ditetapkan kepada **Sah**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subkontrak ahli pasukan projek kakitangan

Seperti ahli pasukan generik atau tanpa kakitangan, anda juga boleh melihat pilihan subkontrak untuk ahli pasukan projek kakitangan selagi ahli pasukan kakitangan adalah pekerja kontrak. Untuk menyemak dan memilih daripada opsyen subkontrak yang tersedia untuk kakitangan atau ahli pasukan projek yang dinamakan, ikuti langkah berikut:

1. Pilih satu atau lebih rekod ahli pasukan projek di mana sumber adalah pekerja kontrak yang dinamakan.
2. Pastikan tiada rekod ahli pasukan projek yang dipilih telah disubkontrakkan. 
3. Pilih **Opsyen subkontrak** pada sub grid ahli pasukan projek. Dialog **opsyen** Subkontrak dibuka. 
4. Jika anda hanya memilih satu rekod ahli pasukan projek dalam langkah 1, maka pilihan berikut akan tersedia:
      - Buat baris subkontrak baru.
      - Rizab terhadap subkontrak sedia ada.
  Jika anda memilih berbilang rekod ahli pasukan projek dalam langkah 1, maka satu-satunya pilihan yang tersedia ialah mencipta baris subkontrak baru.
5. Pilihan untuk menempah terhadap garis subkontrak sedia ada membolehkan anda memilih garis subkontrak dan subkontrak yang anda ingin simpan. Apabila memilih garis subkontrak untuk menyimpan kapasiti, anda harus memastikan perkara berikut:
      - Garis subkontrak yang dipilih adalah untuk masa. 
      - Peranan yang diperlukan pada ahli pasukan projek sepadan dengan peranan yang dibeli pada baris subkontrak. 
      - Penjual yang dikaitkan dengan pekerja kontrak adalah sama dengan vendor pada subkontrak.
6. Apabila anda memilih untuk mencipta baris subkontrak baru untuk ahli pasukan projek, sistem akan membolehkan anda memilih subkontrak yang anda ingin cipta baris ini. Dengan pilihan ini, anda harus memastikan bahawa vendor yang dimiliki oleh pekerja kontrak adalah sama dengan vendor pada subkontrak. 
7. Subkontrak yang anda pilih untuk mencipta baris baru hendaklah dalam **status Draf**. Dengan pilihan ini untuk mencipta baris subkontrak baru untuk ahli pasukan projek yang dipilih, sistem akan mencipta satu baris subkontrak untuk masa untuk setiap ahli pasukan projek. Peranan, jam dan tarikh akan disalin dari ahli pasukan projek ke setiap baris subkontrak yang dibuat.  
8. Apabila ahli pasukan yang dinamakan dikaitkan dengan subkontrak dan subkontrak, **medan jenis** Pekerja pada baris ahli pasukan yang dinamakan akan dikemas kini kepada **Pekerja** Kontrak dan **nilai Kesahan** Subkontrak akan ditetapkan kepada **Sah**.

## <a name="re-costing-subcontractor-assignments"></a>Tugasan subkontraktor kos semula

Apabila ahli pasukan projek (generik atau bernama) dipautkan kepada baris subkontrak menggunakan **dialog opsyen** Subkontrak, sebarang tugasan kepada tugas yang dimiliki oleh ahli pasukan akan dikoskan semula berdasarkan senarai harga pembelian yang dilampirkan pada subkontrak. **Pada tab Anggaran** pada **halaman Butiran** Projek, pilih **butang Kemas Kini harga** untuk melihat harga yang dikemas kini dan/atau kos yang terhasil daripada keputusan untuk subkontrak.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
