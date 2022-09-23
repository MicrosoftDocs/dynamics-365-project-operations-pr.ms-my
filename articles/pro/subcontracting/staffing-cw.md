---
title: Kakitangan projek dengan pekerja kontrak dan kapasiti yang disubkontrak
description: Artikel ini menerangkan cara keperluan projek boleh dikendalikan menggunakan pekerja kontrak atau kapasiti subkontrak dalam Microsoft Dynamics 365 Project Operations.
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

Ahli pasukan projek generik boleh dikendalikan dengan pekerja atau pekerja kontrak. Apabila mengendalikan projek dengan pekerja kontrak, anda boleh mengehadkan opsyen kakitangan anda kepada pekerja kontrak tertentu yang ditugaskan ke garis subkontrak. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Cari keperluan sumber kakitangan dengan pekerja kontrak yang tergolong dalam garis subkontrak tertentu

Untuk mencari dan keperluan sumber kakitangan dengan pekerja kontrak yang tergolong dalam garis subkontrak tertentu, ikuti langkah-langkah berikut:

1. Cipta ahli pasukan projek generik yang merujuk kepada garis subkontrak dan subkontrak.
2. Menjana keperluan sumber untuk ahli pasukan projek generik ini dengan menggunakan butang **Jana keperluan** pada sub grid ahli pasukan projek.
3. Pilih baris ahli pasukan dan kemudian pilih butang **Buku** pada sub grid. 
4. Ini membuka Lembaga Jadual dengan konteks keperluan. Bersama-sama dengan atribut lain seperti tarikh, peranan, dan medan unit organisasi, penapis Lembaga Jadual juga diisi secara automatik dengan medan vendor, subkontrak dan garis subkontrak daripada keperluan sumber.
5. Sistem ini mencari sumber yang memenuhi kriteria penapis dan menyenaraikannya. 
6. Pilih salah satu sumber yang ditapis dan tempah sumber untuk keperluan. 
7. Ahli pasukan projek dicipta dan dikemas kini dengan rujukan garis subkontrak dan subkontrak. Pergi ke **Anggaran** Projek dan pilih **Kemas kini harga** untuk melihat kos tugasan sumber yang dikemas kini. 

> [!NOTE]
> Mengemas kini ahli pasukan projek dengan rujukan garis subkontrak dan subkontrak mungkin tidak selalu dapat dilakukan semasa tempahan jika sumber ditugaskan kepada berbilang baris subkontrak. Sekiranya sistem tidak dapat mengemas kini ahli pasukan projek dengan garis subkontrak dan subkontrak, buka rekod ahli pasukan projek dan kemas kini medan ini secara manual supaya anggaran kos kewangan mencerminkan kos subkontraktor dengan tepat.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Mencari dan keperluan sumber kakitangan dengan mana-mana pekerja kontrak

Untuk mencari dan keperluan sumber kakitangan dengan mana-mana pekerja kontrak, ikuti langkah-langkah berikut:

1. Buat ahli pasukan projek generik.
2. Menjana keperluan sumber untuk ahli pasukan projek generik ini dengan menggunakan butang **Jana keperluan** pada sub grid ahli pasukan projek.
3. Pilih baris ahli pasukan dan kemudian pilih butang **Buku** pada sub grid. 
4. Ini membuka Lembaga Jadual dengan konteks keperluan. Bersama-sama dengan atribut lain seperti tarikh, peranan, dan medan unit organisasi, penapis Lembaga Jadual juga diisi secara automatik dengan medan vendor, subkontrak dan garis subkontrak daripada keperluan sumber. Oleh kerana keperluan tidak mempunyai sebarang subkontrak atau nilai garis subkontrak yang diisi, atribut ini akan kosong pada anak tetingkap penapis.
5. Sistem ini mencari sumber yang memenuhi kriteria penapis dan menyenaraikannya.
6. **Kemas kini medan Jenis** Pekerja pada anak tetingkap penapis kepada **Pekerja** Kontrak untuk mengehadkan carian kepada pekerja kontrak. Kemas kini **Vendor** pada anak tetingkap penapis untuk memilih vendor untuk mengehadkan carian untuk hanya menunjukkan pekerja kontrak yang dimiliki oleh syarikat vendor tertentu.
7. Pilih pekerja kontrak daripada senarai dan tempah sumber untuk keperluan.
8. Ahli pasukan projek dicipta. Walau bagaimanapun, ahli pasukan projek tidak dikemas kini dengan mana-mana subkontrak atau subkontrak talian dan oleh itu tugasan sumber tidak akan dikenakan biaya menggunakan harga subkontrak. Kemas kini secara manual ahli pasukan projek dengan garis subkontrak dan pergi ke **Anggaran** Projek dan pilih **Kemas kini harga** untuk melihat kos tugasan sumber yang dikemas kini.

> [!NOTE]
> Ahli pasukan projek yang mempunyai **jenis** Pekerja sebagai **pekerja** Kontrak tetapi tidak mempunyai rujukan subkontrak dibenderakan sebagai **Tidak Sah** pada **grid ahli** pasukan Projek. Jika terdapat mana-mana ahli pasukan projek dengan status ini, buka rekod ahli pasukan projek dan kemas kini medan subkontrak dan subkontrak secara manual supaya anggaran kos kewangan mencerminkan kos subkontraktor pada **tab Anggaran**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
