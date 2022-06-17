---
title: Kakitangan projek dengan pekerja kontrak dan kapasiti yang disubkontrak
description: Artikel ini menerangkan bagaimana keperluan projek boleh dikendalikan menggunakan pekerja kontrak atau kapasiti subkontrak dalam Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 173e1c20d2d046ee2120ec178e51d4868b70847d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922095"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Kakitangan projek dengan pekerja kontrak dan kapasiti yang disubkontrak

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Ahli pasukan projek generik boleh dikendalikan dengan pekerja atau pekerja kontrak. Apabila kakitangan projek dengan pekerja kontrak, anda boleh mengehadkan pilihan kakitangan anda kepada pekerja kontrak tertentu yang ditugaskan kepada garis subkontrak. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Cari keperluan sumber kakitangan dengan pekerja kontrak yang tergolong dalam garis subkontrak tertentu

Untuk mencari dan keperluan sumber kakitangan dengan pekerja kontrak yang tergolong dalam garis subkontrak tertentu, ikuti langkah-langkah berikut:

1. Cipta ahli pasukan projek generik yang merujuk garis subkontrak dan subkontrak.
2. Menjana keperluan sumber untuk ahli pasukan projek generik ini dengan **menggunakan butang Jana keperluan** pada sub grid ahli pasukan projek.
3. Pilih baris ahli pasukan dan kemudian pilih butang **Tempah** pada sub grid. 
4. Ini membuka Papan Jadual dengan konteks keperluan. Bersama-sama dengan atribut lain seperti tarikh, peranan dan medan unit organisasi, penapis Papan Jadual juga diisi secara automatik dengan medan baris vendor, subkontrak dan subkontrak daripada keperluan sumber.
5. Sistem mencari sumber yang memenuhi kriteria penapis dan menyenaraikannya. 
6. Pilih salah satu sumber yang ditapis dan tempah sumber untuk keperluan. 
7. Ahli pasukan projek dicipta dan dikemas kini dengan rujukan baris subkontrak dan subkontrak. Pergi ke **Anggaran** Projek dan pilih **Kemas kini harga** untuk melihat kos tugasan sumber yang dikemas kini. 

> [!NOTE]
> Mengemas kini ahli pasukan projek dengan rujukan subkontrak dan subkontrak mungkin tidak selalu dapat dilakukan semasa tempahan jika sumber diberikan kepada berbilang baris subkontrak. Jika sistem tidak dapat mengemas kini ahli pasukan projek dengan garis subkontrak dan subkontrak, kemudian buka rekod ahli pasukan projek dan kemas kini medan ini secara manual supaya anggaran kos kewangan dengan tepat mencerminkan kos subkontraktor.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Cari dan keperluan sumber kakitangan dengan mana-mana pekerja kontrak

Untuk mencari dan keperluan sumber kakitangan dengan mana-mana pekerja kontrak, ikuti langkah-langkah berikut:

1. Buat ahli pasukan projek generik.
2. Menjana keperluan sumber untuk ahli pasukan projek generik ini dengan **menggunakan butang Jana keperluan** pada sub grid ahli pasukan projek.
3. Pilih baris ahli pasukan dan kemudian pilih butang **Tempah** pada sub grid. 
4. Ini membuka Papan Jadual dengan konteks keperluan. Bersama-sama dengan atribut lain seperti tarikh, peranan dan medan unit organisasi, penapis Papan Jadual juga diisi secara automatik dengan medan baris vendor, subkontrak dan subkontrak daripada keperluan sumber. Oleh kerana keperluan tidak mempunyai sebarang nilai garis subkontrak atau subkontrak yang diisi, atribut ini akan kosong pada anak tetingkap penapis.
5. Sistem mencari sumber yang memenuhi kriteria penapis dan menyenaraikannya.
6. **Kemas kini medan jenis** Pekerja pada anak tetingkap penapis kepada **Pekerja** Kontrak untuk mengehadkan carian kepada pekerja kontrak. Kemas kini **Vendor** pada anak tetingkap penapis untuk memilih vendor untuk mengehadkan carian untuk hanya menunjukkan pekerja kontrak yang dimiliki oleh syarikat vendor tertentu.
7. Pilih pekerja kontrak dari senarai dan tempah sumber untuk keperluan tersebut.
8. Ahli pasukan projek dicipta. Walau bagaimanapun, ahli pasukan projek tidak dikemas kini dengan mana-mana subkontrak atau subkontrak dan oleh itu tugasan sumber tidak akan dikenakan kos menggunakan harga subkontrak. Kemas kini ahli pasukan projek secara manual dengan baris subkontrak dan pergi ke **Anggaran** Projek dan pilih **Kemas kini harga** untuk melihat kos tugasan sumber yang dikemas kini.

> [!NOTE]
> Ahli pasukan projek yang mempunyai **jenis** Pekerja sebagai **pekerja** kontrak tetapi tidak mempunyai rujukan subkontrak dibenderakan sebagai **Tidak Sah** pada **grid ahli** pasukan Projek. Jika terdapat mana-mana ahli pasukan projek dengan status ini, buka rekod ahli pasukan projek dan kemas kini medan baris subkontrak dan subkontrak secara manual supaya anggaran kos kewangan mencerminkan kos subkontraktor dengan tepat pada **tab Anggaran**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
