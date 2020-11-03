---
title: Kumpulan unit dan unit
description: Topik ini menyediakan maklumat mengenai kumpulan unit dan unit.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 78f154856acf796f408491c5873cb29da8ac55bb
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081244"
---
# <a name="unit-groups-and-units"></a>Kumpulan unit dan unit

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Kumpulan unit dan unit adalah entiti asas dalam Microsoft Dynamics 365. Sebuah unit ialah unit ukuran tunggal dan berbilang unit boleh dikumpulkan dalam kumpulan unit. Sebuah kumpulan unit kadangkala dirujuksebagai jadual unit dalam antara muka pengguna Dynamics 365 (UI). 

Berikut adalah beberapa contoh unit dan kumpulan unit:
 
- **Kumpulan unik** : Jarak 
    - **Unit** : Batu, Kiilometer dan sebagainya.
- **Kumpulan unit** : Masa
    - **Unit** : Jam, hari, minggu dan sebagainya. 

Apabila anda menyediakan berbilang unit dalam kumpulan unit, anda juga mesti menyediakan faktor penukaran antara mereka dengan menunjukkan unit pertama yang anda sediakan sebagai unit lalai atau utama bagi kumpulan unit. 

Sebagai contoh, dalam kumpulan unit **Masa** , jika anda meyediakan **Jam** sebagai unit pertama, sistem menetapkan **Jam** sebagai unit lalai. Jika unit seterusnya yang anda sediakan ialah **Hari** , anda mesti menyediakan faktor penukaran untuk **Hari** kepada **Jam**. Jika anda kemudian menambah **Minggu** sebagai unit ketiga, anda mesti menyediakan faktor penukaran untuk **Minggu** dari segi **Hari** atau **Jam**. 

Imej berikut menunjukkan persediaan contoh untuk unit **Hari** , tempat medan **Kuantiti** menunjukkan bilangan jam yang berada dalam sehari dan **Minggu** , di mana medan **Kuantiti** menunjukkan bilangan hari dalam seminggu.

> ![Unit kumpulan: Halaman maklumat](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Menggunakan unit dan kumpulan unit

Dynamics 365 Project Service Automation menggunakan unit dan kumpulan unit untuk memproses anggaran dan entri untuk kedua-dua perbelanjaan dan masa. 

Untuk perbelanjaan, setiap kategori perbelanjaan mempunyai kumpulan unit dan unit lalai. Nilai ini dimasukkan sebagai nilai lalai pada senarai harga entri untuk kategori perbelanjaan. 

Sebagai contoh, anda mempunyai kategori perbelanjaan yang dinamakan **Perbatuan**. Ia mempunyai kumpulan unit yang dinamakan **Jarak** dan unit lalai yang dinamakan **Batu**. Jika anda menyediakan kumpulan unit **Jarak** supaya ia mempunyai dua unit ( **Batu** dan **Kilometer** ), anda boleh menetapkan dua harga untuk kategori **Perbatuan** pada satu senarai harga: harga setiap batu dan harga setiap kilometer.

| Kategori perbelanjaan  | Kumpulan unit  | Unit      | Kaedah penetapan harga  | Harga seunit  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Perbatuan           | Jarak      | Batu      | Harga seunit    | 10 USD            |
| Perbatuan           | Jarak      | Kilometer | Harga seunit    |  6 USD            |

Apabila anda memasukkan perbelanjaan pada projek, sistem menentukan harga melalui gabungan kategori dan unit pada perbelanjaan. 

| Perihalan perbelanjaan        | Kategori perbelanjaan  | Unit  | Kuantiti  | Harga unit   |
|----------------------------|---------------------|-------|-----------|----------------|
| Memandu ke lokasi pelanggan | Perbatuan             | Batu  | 10        | 10 USD         |

Untuk masa, setiap pengepala senarai harga mempunyai medan **Unit Masa Lalai**. Nilai ditetapkan apabila anda mencipta pengepala senarai harga. Unit ini kemudiannya digunakan untuk menetapkan semua harga berasaskan peranan pada senarai harga tersebut.

Baris anggaran untuk medan **Masa pada Sebut Harga** boleh dinyatakan dalam unit masa. Walau bagaimanapun, baris anggaran pada entri masa untuk projek hanya boleh menggunakan unit masa **Jam**. Jika unit pada entri masa atau anggaran baris tidak sepadan dengan unit pada baris senarai harga untuk peranan tersebut, sistem ini akan menukar harga kepada unit yang ditakrifkan dalam anggaran projek atau transaksi projek sebenar.

Contoh berikut menunjukkan cara PSA menggunakan faktor kumpulan unit, unit dan penukaran.
- Unit

   - **Kumpulan unit** : Masa 
   - **Unit** : Jam 
    
    - **Hari** - Faktor penukaran: 8 jam       
    - **Minggu** - Faktor penukaran: 40 jam  
        
- Senarai harga persediaan pada Projek A:

    - **Nama** : Harga jualan UK 2016 
    - **Unit masa lalai** : hari 
    - **Mata wang** : GBP

| Peranan      | Kumpulan unit | Unit | Unit organisasi | Harga   |
|-----------|------------|------|---------------------|---------|
| Pembangun | Time       | Day  | Contoso UK          | 800 GBP |

### <a name="time-entry"></a>Entri masa

Jadual berikut menunjukkan transaksi bahagian jualan hasil yang dicipta oleh PSA untuk projek tiga jam.


| Projek   | Tugas    | Peranan      | Kuantiti | Unit  | Harga unit | Amaun jualan belum dibilkan |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| Projek A | Reka Bentuk  | Pembangun | 3        | Hour  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>Soalan lazim unit masa

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>Adakah PSA ditukar kepada unit yang berbeza dalam kes perbelanjaan?
Tidak. Penukaran unit berfungsi hanya untuk masa. Untuk perbelanjaan, jika sistem tidak dapat mencari harga untuk gabungan kategori perbelanjaan dan unit, harga ditetapkan kepada 0.00 secara lalai.

### <a name="why-does-psa-convert-time-units"></a>Mengapakah PSA menukar unit masa?
Di sesetengah negara atau rantau, terdapat keperluan perundangan yang mana kadar bil ditetapkan dalam masa beberapa hari. Rundingan harga dan diskaun semasa kitaran sebut harga dilakukan dengan menggunakan kadar hari untuk setiap peranan boleh dibilkan. Anggaran jadual dan entri masa dilakukan dalam masa beberapa jam. Untuk menyokong perbezaan ini dalam unit masa, PSA menukar unit masa.

### <a name="can-time-units-be-changed-on-project-estimates"></a>Bolehkah unit masa ditukar pada anggaran projek?
Tidak. Anggaran jadual adalah terhad kepada jam dan tidak boleh ditukar.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>Bolehkan unit dan kumpulan unit diedit, dipadamkan dan ditambah?
Ya. Dengan pengecualian kumpuan unit **Masa** dan unit **Jam** , semua unit boleh dipadamkan atau diedit, dan unit baharu boleh ditambah. Pada PSA, kumpulan unit **Masa** dan unit **Jam** tidak boleh dipadamkan. Walau bagaimanapun, ia boleh dikemas kini dengan teks terjemahan untuk medan **Nama**.
