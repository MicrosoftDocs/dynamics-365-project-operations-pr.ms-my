---
title: Jadual invois pada baris sebut harga berasaskan projek
description: Artikel ini menyediakan maklumat tentang penciptaan jadual invois dan pencapaian untuk baris sebut harga.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b1e431bc3586f9fef7a01348555e4ee4e06cc66c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918323"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a>Jadual invois pada baris sebut harga berasaskan projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Baris sebut harga berasaskan projek memberikan keupayaan untuk menyatakan jadual invois. Ini adalah pilihan semasa fasa sebut harga kerana aplikasi tidak menyokong penginvoisan projek apabila invois terikat dengan baris sebut harga. Penginvoisan hanya dibenarkan selepas sebut harga dimenangi. Satu-satunya kesan hiliran kerana mencipta jadual invois semasa fasa sebut harga adalah bahawa jadual invois ini disalin pada baris kontrak berasaskan projek. Jika anda tidak mencipta jadual invois semasa fasa sebut harga, anda akan dapat berbuat demikian pada baris kontrak berasaskan projek.

Pada keseluruhannya, tujuan jadual invois adalah untuk membenarkan penciptaan automatik invois draf untuk baris kontrak berasaskan projek. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a>Cipta jadual invois Masa dan bahan untuk baris sebut harga projek

Apabila kaedah pengebilan untuk baris sebut harga berdasarkan projek ialah Masa dan bahan, sistem menjana jadual invois berdasarkan tarikh. Untuk menjana jadual invois berdasarkan tarikh secara automatik, lengkapkan langkah berikut.

1. Pergi ke **Tetapan** > **kekerapan invois** dan sediakan kekerapan invois.
2. Pada halaman **Sebut harga**, buka sebut harga Project dan pada tab **Ringkasan**, tetapkan tarikh penghantaran yang diminta.
3. Buka baris sebut harga masa dan bahan yang anda perlukan untuk mencipta jadual invois berasaskan tarikh. 
4. Pada tab **Jadual Invois**, pilih nilai dalam medan **Mula pengebilan** dan **Kekerapan Invois**. 
5. Pada subgrid, pilih **Jana Jadual Invois**.
6. Aplikasi ini menjana jadual invois dengan medan **Tarikh Jalanan Invois**, **Tarikh Tamat Urus Niaga** dan **Status Jalanan** ditetapkan mengikut cara berikut:

    - **Tarikh Jalanan Invois** ditetapkan kepada tarikh yang ditentukan berdasarkan kekerapan invois.
    - **Tarikh tamat urus niaga** ditetapkan pada hari sebelum **Tarikh Jalanan Invois**.
    - **Status Jalanan** ditetapkan secara automatik kepada **Jangan Jalankan**. Apabila kerja penciptaan invois automatik berjalan untuk tarikh jalanan invois tertentu, ia akan mengemas kini medan ini kepada sama ada **Jalanan Berjaya** atau **Jalanan Gagal**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a>Cipta jadual invois harga Tetap untuk baris sebut harga projek

Apabila baris sebut harga berasaskan projek mempunyai kaedah pengebilan **Tetap**, sistem mencipta jadual invois berasaskan pencapaian. Lengkapkan langkah berikut untuk menjana jadual ini secara automatik untuk set pencapaian tetap yang diagihkan sama rata untuk tempoh kalendar.

1. Pergi ke **Tetapan** > **kekerapan invois** dan sediakan kekerapan invois.
2. Pada halaman **Sebut harga**, buka sebut harga Project dan pada tab **Ringkasan**, tetapkan tarikh penghantaran yang diminta.
3. Buka baris sebut harga tetap yang anda perlukan untuk mencipta jadual pencapaian. 
4. Pada tab **Jadual Invois**, pilih nilai dalam medan **Mula pengebilan** dan **Kekerapan Invois**. 
5. Pada subgrid, pilih **Jana Pencapaian Berkala**.
6. Aplikasi ini menjana jadual invois dengan nama, tarikh dan jumlah pencapaian.

    - Nama pencapaian ditetapkan kepada tarikh yang ditentukan berasaskan kekerapan invois.
    - Tarikh pencapaian ditetapkan kepada tarikh yang ditentukan berasaskan kekerapan invois.
    - Jumlah pencapaian dikira dengan membahagikan jumlah sebut harga pada baris sebut harga projek dengan bilangan pencapaian yang ditentukan oleh kekerapan dan tarikh mula pengebilan dan tarikh penghantaran yang diminta.
    - Jika baris Sebut Harga juga mempunyai anggaran jumlah cukai, nilai ini akan dibahagikan antara setiap pencapaian secara sama rata apabila menjana pencapaian berkala.

### <a name="manually-create-milestones"></a>Cipta pencapaian secara manual

Pencapaian harga tetap juga boleh dijana secara manual apabila tidak berpecah secara berkala. Untuk mencipta pencapaian secara manual:

Buka baris sebut harga Tetap yang anda perlukan untuk mencipta pencapaian. Pada tab **Jadual Invois**, dalam subgrid, pilih **+ Cipta pencapaian baris sebut harga baharu** dan masukkan maklumat yang diperlukan berdasarkan jadual berikut.

| **Medan** | **Lokasi** | **Perihalan** | **Kesan hiliran** |
| --- | --- | --- | --- |
| Nama pencapaian | Cipta cepat | Nama pencapaian. | Ini telah disebarkan kepada pencapaian baris kontrak projek dan kepada invois |
| Tugas Projek | Cipta cepat | Jika pencapaian tersebut terikat dengan tugas projek, anda boleh menggunakan rujukan ini untuk menambah logik tersuai dan menetapkan status pencapaian berdasarkan status tugas. | Aplikasi ini tidak mempunyai sebarang kesan hiliran bagi rujukan ini kepada tugas. |
| Tarikh pencapaian | Cipta cepat | Tetapkan tarikh yang mana proses penciptaan invois automatik sepatutnya mencari status pencapaian ini untuk dipertimbangkan untuk penginvoisan. | Ini telah disebarkan kepada pencapaian baris kontrak projek dan kepada invois. |
| Status invois | Cipta cepat | Apabila pencapaian dicipta, status ini sentiasa ditetapkan kepada **Tidak bersedia untuk penginvoisan**. | Ini telah disebarkan kepada pencapaian baris kontrak projek dan kepada invois. |
| Amaun Baris | Cipta cepat | Jumlah atau nilai pencapaian yang akan diinvoiskan kepada pelanggan. | Ini telah disebarkan kepada pencapaian baris kontrak projek dan kepada invois. |
| Cukai | Cipta cepat | Jumlah cukai yang akan dikenakan kepada pencapaian. | Ini telah disebarkan kepada pencapaian baris kontrak projek dan kepada invois. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]