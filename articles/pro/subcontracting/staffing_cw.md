---
title: Kakitangan projek dengan pekerja kontrak dan kapasiti subkontrak
description: Topik ini menerangkan bagaimana keperluan projek boleh dikendalikan menggunakan pekerja kontrak atau kapasiti subkontrak dalam Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 7e9a0ca08f472999138589f31ca820b733b6303e
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903070"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Kakitangan projek dengan pekerja kontrak dan kapasiti subkontrak

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Ahli pasukan projek generik boleh dikendalikan dengan pekerja atau pekerja kontrak. Apabila kakitangan projek dengan pekerja kontrak, anda boleh mengehadkan pilihan kakitangan anda kepada pekerja kontrak tertentu yang ditugaskan ke garis subkontrak. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Cari keperluan sumber kakitangan dengan pekerja kontrak yang tergolong dalam garis subkontrak tertentu

Untuk mencari dan keperluan sumber kakitangan dengan pekerja kontrak yang tergolong dalam garis subkontrak tertentu, ikuti langkah-langkah berikut:

1. Cipta ahli pasukan projek generik yang merujuk garis subkontrak dan subkontrak.
2. Menjana keperluan sumber untuk ahli pasukan projek generik ini dengan menggunakan **butang Jana keperluan** pada sub grid ahli pasukan projek.
3. Pilih baris ahli pasukan kemudian pilih **butang Tempah pada sub** grid. 
4. Ini membuka Lembaga Jadual dengan konteks keperluan. Bersama-sama dengan atribut lain seperti medan tarikh, peranan dan unit organisasi, penapis Papan Jadual juga diisi secara automatik dengan medan garis vendor, subkontrak dan subkontrak daripada keperluan sumber.
5. Sistem mencari sumber yang memenuhi kriteria penapis dan menyenaraikannya. 
6. Pilih salah satu sumber yang ditapis dan tempah sumber untuk keperluan. 
7. Ahli pasukan projek dicipta dan dikemas kini dengan rujukan garis subkontrak dan subkontrak. Pergi ke **Anggaran Projek dan pilih Kemas kini harga untuk melihat kos tugasan sumber yang dikemas** **kini**. 

> [!NOTE]
> Mengemas kini ahli pasukan projek dengan rujukan garis subkontrak dan subkontrak mungkin tidak selalu mungkin semasa tempahan jika sumber diberikan kepada pelbagai baris subkontrak. Jika sistem tidak dapat mengemas kini ahli pasukan projek dengan garis subkontrak dan subkontrak, kemudian buka rekod ahli pasukan projek dan kemas kini medan ini secara manual supaya anggaran kos kewangan mencerminkan kos subkontraktor dengan tepat.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Mencari dan keperluan sumber kakitangan dengan mana-mana pekerja kontrak

Untuk mencari dan keperluan sumber kakitangan dengan mana-mana pekerja kontrak, ikuti langkah-langkah berikut:

1. Cipta ahli pasukan projek generik.
2. Menjana keperluan sumber untuk ahli pasukan projek generik ini dengan menggunakan **butang Jana keperluan** pada sub grid ahli pasukan projek.
3. Pilih baris ahli pasukan kemudian pilih **butang Tempah pada sub** grid. 
4. Ini membuka Lembaga Jadual dengan konteks keperluan. Bersama-sama dengan atribut lain seperti medan tarikh, peranan dan unit organisasi, penapis Papan Jadual juga diisi secara automatik dengan medan garis vendor, subkontrak dan subkontrak daripada keperluan sumber. Oleh kerana keperluan tidak mempunyai sebarang nilai garis subkontrak atau subkontrak yang diisi, atribut ini akan kosong pada anak tetingkap penapis.
5. Sistem mencari sumber yang memenuhi kriteria penapis dan menyenaraikannya.
6. Kemas kini **medan jenis Pekerja pada anak tetingkap penapis kepada Pekerja Kontrak untuk mengehadkan carian kepada pekerja** **kontrak**. Kemas kini **Vendor pada anak tetingkap penapis untuk memilih vendor untuk mengehadkan carian untuk hanya menunjukkan pekerja kontrak yang** tergolong dalam syarikat vendor tertentu.
7. Pilih pekerja kontrak daripada senarai dan tempah sumber untuk keperluan tersebut.
8. Ahli pasukan projek dicipta. Walau bagaimanapun, ahli pasukan projek tidak dikemas kini dengan mana-mana subkontrak atau garis subkontrak dan oleh itu tugasan sumber tidak akan dikenakan biaya menggunakan harga subkontrak. Kemas kini ahli pasukan projek secara manual dengan garis subkontrak dan pergi ke **Anggaran Projek dan pilih Kemas kini harga untuk melihat kos tugasan sumber yang dikemas** **kini**.

> [!NOTE]
> Ahli pasukan projek yang mempunyai **jenis Pekerja sebagai pekerja Kontrak tetapi tidak mempunyai rujukan** **subkontrak** dibenderakan sebagai **Tidak Sah pada grid ahli pasukan** **Projek**. Jika terdapat mana-mana ahli pasukan projek dengan status ini, buka rekod ahli pasukan projek dan kemas kini medan garis subkontrak dan subkontrak secara manual supaya anggaran kos kewangan mencerminkan kos subkontraktor dengan tepat pada **tab** Anggaran. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
