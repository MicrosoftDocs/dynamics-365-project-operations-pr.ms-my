---
title: Cipta jadual invois tentang baris kontrak berasaskan projek - lite
description: Artikel ini memberikan maklumat tentang penciptaan jadual invois dan pencapaian.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 403b993c3f61ca5f0fb1bac45331aa0613d16439
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921129"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a>Cipta jadual invois tentang baris kontrak berasaskan projek - lite

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Anda boleh melampirkan jadual invois tentang baris kontrak berasaskan projek. Invois hanya dibenarkan selepas kontrak itu dimenangi untuk mencipta kontrak Projek. Jadual invois membenarkan draf invois untuk baris kontrak berasaskan projek dicipta secara automatik. Jika anda merancang untuk sentiasa mencipta invois secara manual, anda boleh melangkau penciptaan jadual invois pada baris kontrak berasaskan projek atau baris kontrak.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Cipta jadual invois masa dan bahan untuk baris kontrak berasaskan projek

Apabila baris kontrak berasaskan projek mempunyai kaedah pengebilan masa dan bahan, anda boleh membuat jadual invois berdasarkan tarikh. Untuk menjana jadual invois berdasarkan tarikh secara automatik, lengkapkan langkah berikut.

1. Pergi ke **Tetapan** > **Kekerapan Invois** untuk menyediakan kekerapan invois.
2. Buka kontrak projek dan pada tab **Ringkasan**, tetapkan tarikh penghantaran yang diminta.
3. Buka baris kontrak masa dan bahan yang anda mahu cipta jadual invois berdasarkan tarikh. 
4. Pada tab **Jadual Invois**, pilih tarikh mula pengebilan dan kekerapan invois. 
5. Pada subgrid, pilih **Jana Jadual Invois**.

    Sistem menjana jadual invois dengan maklumat medan berikut:

    - **Tarikh Jalanan Invois** ditetapkan kepada tarikh berdasarkan kekerapan invois.
    - **Tarikh Tamat Urus Niaga** ditetapkan kepada hari sebelum **Tarikh Jalanan Invois**.
    - **Status Jalanan** ditetapkan secara automatik kepada **Jangan Jalankan**. Apabila kerja penciptaan invois automatik berjalan untuk **Tarikh Jalanan Invois** tertentu, medan ini akan dikemas kini kepada **Jalanan Berjaya** atau **Jalanan Gagal**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Cipta jadual invois harga tetap untuk baris kontrak berasaskan projek

Apabila baris kontrak berasaskan projek mempunyai kaedah pengebilan harga tetap, anda boleh membuat jadual invois berdasarkan pencapaian. Lengkapkan langkah berikut untuk menjana jadual invois berasaskan pencapaian secara automatik untuk set tetap pencapaian yang diagihkan sama rata untuk tempoh kalendar.

1. Pergi ke **Tetapan** > **Kekerapan Invois** untuk menyediakan kekerapan invois.
2. Buka kontrak projek dan pada tab **Ringkasan**, tetapkan tarikh penghantaran yang diminta.
3. Buka baris kontrak harga tetap yang anda perlu membuat jadual pencapaian. 
4. Pada tab **Jadual Invois (Pencapaian Pengebilan)**, pilih tarikh mula pengebilan dan kekerapan invois. 
5. Pada subgrid, pilih **Jana Pencapaian Berkala**.

    Sistem menjana jadual invois dengan maklumat pencapaian berikut.

    - **Nama Pencapaian** ditetapkan kepada tarikh yang ditentukan berdasarkan kekerapan invois.
    - **Tarikh Pencapaian** ditetapkan kepada tarikh yang ditentukan berdasarkan kekerapan invois.
    - **Jumlah Pencapaian** dikira dengan membahagikan jumlah kontrak pada baris kontrak berasaskan projek mengikut bilangan pencapaian seperti yang ditentukan oleh kekerapan, mula pengebilan dan tarikh penghantaran yang diminta.
    - Jika baris kontrak mempunyai nilai dalam medan **Anggaran Amaun Cukai**, medan ini juga diuntukkan kepada setiap pencapaian yang sama apabila menjana pencapaian berkala.

Pencapaian pengebilan haruslah sama dengan nilai kontrak baris kontrak berasaskan projek. Jika ia tidak sama, ralat berlaku. Anda boleh membetulkan ralat tersebut dengan mengesahkan bahawa kontrak telah mencapai jumlah nilai kontrak baris dengan sama ada mencipta, mengedit atau memadamkan pencapaian. Selepas perubahan dibuat, segar semula halaman.

### <a name="manually-create-milestones"></a>Cipta pencapaian secara manual

Pencapaian harga tetap boleh dijana secara manual apabila ia tidak berpecah secara berkala. Untuk mencipta pencapaian secara manual, lengkapkan langkah berikut.

1. Buka baris kontrak harga tetap yang anda mahu membuat pencapaian. 
2. Pada tab **Jadual Invois**, pada subgrid, pilih **+ Cipta pencapaian Baris Kontrak baharu**.
3. Pada borang **Cipta Pencapaian**, masukkan maklumat yang diperlukan berdasarkan jadual berikut. 

| Medan | Lokasi | Penerangan | Kesan hiliran |
| --- | --- | --- | --- |
| Nama Pencapaian | Cipta Cepat | Medan teks untuk nama pencapaian. | Medan ini disertakan pada pencapaian baris kontrak projek dan invois. |
| Tugas Projek | Cipta Cepat | Jika pencapaian tersebut terikat dengan tugas projek, gunakan rujukan ini untuk menambah logik tersuai dan menetapkan status pencapaian berdasarkan status tugas. | Tiada kesan hiliran bagi rujukan ini kepada tugas. |
| Tarikh Pencapaian | Cipta Cepat | Tarikh yang mana proses penciptaan invois automatik sepatutnya mencari status pencapaian ini untuk dipertimbangkan sebagai invois. | Ini disertakan pada pencapaian baris kontrak projek dan invois. |
| Status Invois | Cipta Cepat | Apabila pencapaian dicipta, status ini sentiasa ditetapkan kepada **Tidak bersedia untuk penginvoisan** atau **Tidak dimulakan**. | Ini disertakan pada pencapaian baris kontrak projek dan invois. |
| Amaun Baris | Cipta Cepat | Jumlah atau nilai pencapaian yang akan diinvoiskan kepada pelanggan. | Medan ini disertakan pada pencapaian baris kontrak projek dan invois. |
| Cukai | Cipta Cepat | Jumlah cukai yang dikenakan ke atas pencapaian tersebut. | Ini disertakan pada pencapaian baris kontrak projek dan invois. |

4. Pilih **Simpan dan Tutup**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]