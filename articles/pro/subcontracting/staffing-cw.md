---
title: Kakitangan projek dengan pekerja kontrak dan kapasiti yang disubkontrak
description: Artikel ini menerangkan cara keperluan projek boleh dikendalikan menggunakan pekerja kontrak atau keupayaan subkontrak dalam Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 30e16efeed93ab4568eac57fb3ed46067a08524d
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522447"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Kakitangan projek dengan pekerja kontrak dan kapasiti yang disubkontrak

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Ahli pasukan projek generik boleh dikendalikan dengan pekerja atau pekerja kontrak. Apabila mengendalikan projek dengan pekerja kontrak, anda boleh mengehadkan pilihan kakitangan anda kepada pekerja kontrak khusus yang diuntukkan kepada baris subkontrak. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Cari keperluan sumber pekerja dengan pekerja kontrak yang tergolong dalam baris subkontrak tertentu

Untuk mencari keperluan sumber kakitangan dengan pekerja kontrak yang tergolong dalam baris subkontrak tertentu, ikut langkah ini:

1. Cipta ahli pasukan projek generik yang merujuk subkontrak dan baris subkontrak.
2. Jana keperluan sumber untuk ahli pasukan projek generik ini menggunakan butang **Jana keperluan** pada subgrid ahli pasukan projek.
3. Pilih baris ahli pasukan, kemudian pilih butang **Tempah** pada subgrid. 
4. Ini membuka Papan Jadual dengan konteks keperluan. Bersama dengan atribut lain seperti medan tarikh, peranan dan unit organisasi, penapis Papan Jadual juga diisi secara automatik dengan medan vendor, subkontrak dan baris subkontrak daripada keperluan sumber.
5. Sistem mencari sumber yang memenuhi kriteria penapis dan menyenaraikan sumber tersebut. 
6. Pilih salah satu sumber yang ditapis dan tempah sumber untuk keperluan. 
7. Ahli pasukan projek dicipta dan dikemas kini dengan rujukan subkontrak dan baris subkontrak. Pergi ke **Anggaran Projek** dan pilih **Kemas kini harga** untuk melihat kos yang dikemas kini bagi tugas sumber. 

> [!NOTE]
> Mengemas kini ahli pasukan projek dengan satu rujukan subkontrak dan baris subkontrak mungkin tidak dapat dilakukan dengan kerap semasa penempahan jika sumber diuntukkan untuk berbilang baris subkontrak. Jika sistem tidak dapat mengemas kini ahli pasukan projek dengan subkontrak dan baris subkontrak, kemudian buka rekod ahli pasukan projek dan kemas kini medan ini secara manual supaya anggaran kos kewangan menggambarkan kos subkontraktor dengan tepat.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Cari keperluan sumber kakitangan dengan mana-mana pekerja kontrak

Untuk mencari keperluan sumber kakitangan dengan mana-mana pekerja kontrak, ikut langkah ini:

1. Cipta ahli pasukan projek generik.
2. Jana keperluan sumber untuk ahli pasukan projek generik ini menggunakan butang **Jana keperluan** pada subgrid ahli pasukan projek.
3. Pilih baris ahli pasukan, kemudian pilih butang **Tempah** pada subgrid. 
4. Ini membuka Papan Jadual dengan konteks keperluan. Bersama dengan atribut lain seperti medan tarikh, peranan dan unit organisasi, penapis Papan Jadual juga diisi secara automatik dengan medan vendor, subkontrak dan baris subkontrak daripada keperluan sumber. Oleh sebab keperluan tidak mempunyai sebarang nilai subkontrak atau baris subkontrak yang diisi, atribut ini akan dibiarkan kosong pada anak tetingkap penapis.
5. Sistem mencari sumber yang memenuhi kriteria penapis dan menyenaraikan sumber tersebut.
6. Kemas kini medan **Jenis pekerja** pada anak tetingkap penapis kepada **Pekerja Kontrak** untuk mengehadkan carian kepada pekerja kontrak. Kemas kini **Vendor** pada anak tetingkap penapis untuk memilih vendor untuk mengehadkan carian agar menunjukkan pekerja kontrak yang dimiliki oleh syarikat vendor tertentu sahaja.
7. Pilih pekerja kontrak daripada senarai dan tempah sumber untuk keperluan.
8. Ahli pasukan projek generik dicipta. Walau bagaimanapun, ahli pasukan projek tidak dikemas kini dengan mana-mana subkontrak atau baris subkontrak dan oleh itu, tugas sumber tidak akan dikira kos menggunakan harga subkontrak. Kemas kini ahli pasukan projek secara manual dengan baris subkontrak dan pergi ke **Anggaran Projek** dan pilih **Kemas kini harga** untuk melihat kos yang dikemas kini bagi tugas sumber.

> [!NOTE]
> Ahli pasukan projek yang mempunyai **Jenis pekerja** sebagai **Pekerja kontrak** tetapi tidak mempunyai rujukan subkontrak ditandakan sebagai **Tidak Sah** pada grid **Ahli pasukan projek**. Jika terdapat mana-mana ahli pasukan projek dengan status ini, buka rekod ahli pasukan projek dan kemas kini medan subkontrak dan baris subkontrak secara manual supaya anggaran kos kewangan menggambarkan kos subkontraktor dengan tepat pada tab **Anggarkan**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
