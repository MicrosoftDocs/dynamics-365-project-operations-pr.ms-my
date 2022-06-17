---
title: Buat jadual invois pada baris kontrak berdasarkan projek
description: Artikel ini memberikan maklumat tentang cara membuat jadual invois dan peristiwa penting pada baris kontrak.
author: rumant
ms.date: 10/17/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 490a61b67f54bdad95ecfce905191c381dddc85b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915011"
---
# <a name="create-an-invoice-schedule-on-a-project-based-contract-line"></a>Buat jadual invois pada baris kontrak berdasarkan projek 

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Anda boleh menjadualkan invois kepada baris kontrak berdasarkan projek. Invois hanya dibenarkan selepas kontrak dimenangi dan anda sedang mencipta kontrak projek. Jadual invois membolehkan draf invois untuk baris kontrak berasaskan projek untuk dicipta secara automatik. Jika bagaimanapun, anda hanya membuat invois secara manual, anda boleh melangkau penciptaan jadual invois pada baris kontrak.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Cipta masa dan bahan jadula invois untuk baris kontrak

Apabila baris kontrak berasaskan projek mempunyai kaedah pengebilan masa dan bahan, anda boleh membuat jadual invois berdasarkan tarikh. Untuk menjana jadual invois berdasarkan tarikh secara automatik, lengkapkan langkah berikut.

1. Pergi ke **Tetapan** > **Kekerapan invois** dan sediakan kekerapan invois.
2. Pergi ke rekod kontrak projek, dan pada tab **Ringkasan** dalam medan **Tarikh Penghantaran yang Diminta**, pilih tarikh.
3. Buka baris kontrak **Masa dan Bahan** yang anda ciptakan jadual invois berasaskan tarikh. 
4. Pada tab **Jadual Invois** , pilih tarikh mula pengebilan dan kekerapan invois.
5. Pada subgrid, pilih **Jana Jadual Invois**. Jadual invois dijana dengan **Tarikh Jalanan Invois**, **Tarikh Tamat Urus Niaga** dan **Status Jalanan** ditetapkan seperti berikut:

    - **Tarikh Jalanan Invois**: Tarikh ini yang ditentukan oleh kekerapan invois.
    - **Tarikh Tamat Urus Niaga**: Hari sebelum tarikh jalanan invois.
    - **Status Jalanan**: Secara automatik ditetapkan kepada **Jangan Jalankan**. Apabila kerja penciptaan invois automatik berjalan untuk tarikh jalanan invois tertentu, medan ini akan dikemas kini kepada **Jalanan Berjaya** atau **Jalanan Gagal**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Cipta jadual invois harga tetap untuk baris kontrak

Apabila baris kontrak mempunyai kaedah pengebilan tetap, anda boleh mencipta jadual invois berasaskan pencapaian. 

> [!NOTE]
> Pencapaian tidak boleh dibuat pada baris kontrak jika tiada projek dipetakan ke baris kontrak.

Lengkapkan langkah berikut untuk menjana jadual jadual invois berasaskan pencapaian untuk set pencapaian tetap yang diagihkan sama rata untuk tempoh kalendar.

1. Pergi ke **Tetapan** > **Kekerapan invois** dan sediakan kekerapan invois.
2. Pergi ke rekod kontrak projek, dan pada tab **Ringkasan** dalam medan **Tarikh Penghantaran yang Diminta**, pilih tarikh.
3. Buka baris kontrak **Harga Tetap** yang anda ciptakan jadual pencapaian. Pada tab **Pencapaian Pengebilan** , pilih tarikh mula pengebilan dan kekerapan invois. 
4. Pada subgrid, pilih **Jana Pencapaian Berkala**. Jadual invois dijana dengan **Nama Pencapaian**, **Tarikh Pencapaian** dan medan **Jumlah Pencapaian** ditetapkan seperti berikut:

    - **Nama Pencapaian**: Nama ini ditentukan oleh kekerapan invois.
    - **Tarikh Pencapaian**: Tarikh ini yang ditentukan oleh kekerapan invois.
    - **Jumah Pencapaian**: Jumlah ini dikira dengan membahagikan jumlah kontrak pada baris kontrak dengan bilangan pencapaian yang ditentukan oleh kekerapan dan tarikh mula pengebilan dan tarikh penghantaran yang diminta.

    Jika baris kontrak mempunyai nilai dalam medan **Anggaran jumlah Cukai**, maka medan ini juga didiagihkan kepada setiap pencapaian yang sama apabila menjana pencapaian berkala.

Pencapaian pengebilan sepatutnya sama dengan nilai berkontrak baris kontrak. Jika tidak, anda akan menerima ralat pada halaman **Baris Kontrak**. Anda boleh membetulkan ralat dengan mengesahkan bahawa kontrak telah mencapai jumlah nilai kontrak baris dengan mencipta, mengedit atau memadamkan pencapaian. Selepas perubahan dibuat, segar semula halaman untuk mengalih keluar ralat.

### <a name="manually-create-milestones"></a>Cipta pencapaian secara manual

Anda boleh menjana pencapaian harga tetap apabila tidak berpecah secara berkala. Lengkapkan langkah berikut untuk mencipta pencapaian secara manual.

1. Buka baris kontrak harga tetap yang anda akan mencipta pencapaian dan pada tab **Jadual Invois**, pada subgrid, pilih **+Cipta pencapaian Baris kontrak baharu**. 
2. Pada halaman **Penciptaan pencapaian**, masukkan maklumat yang diperlukan berdasarkan jadual berikut.

| Medan | Lokasi | Penerangan | Kesan hiliran |
| --- | --- | --- | --- |
| Nama Pencapaian | Cipta Cepat | Medan teks untuk nama pencapaian. | Ini telah dibawa kepada pencapaian baris kontrak pencapaian dan invois. |
| Tugas Projek | Cipta Cepat | Jika pencapaian tersebut terikat dengan tugas projek, gunakan rujukan ini untuk menambah logik tersuai untuk menetapkan status pencapaian berdasarkan status tugas. | Aplikasi ini tidak mempunyai sebarang kesan hiliran bagi rujukan ini kepada tugas. |
| Tarikh Pencapaian | Cipta Cepat | Tetapkan tarikh yang mana proses penciptaan invois automatik sepatutnya mencari status pencapaian ini untuk dipertimbangkan untuk penginvoisan. | Ini telah dibawa kepada pencapaian baris kontrak pencapaian dan invois. |
| Status Invois | Cipta Cepat | Apabila pencapaian dicipta, status ini sentiasa ditetapkan kepada **Tidak Bersedia untuk Penginvoisan** atau **Tidak Bermula**. | Ini telah dibawa kepada pencapaian baris kontrak pencapaian dan invois. |
| Amaun Baris | Cipta Cepat | Jumlah atau nilai pencapaian yang akan diinvoiskan kepada pelanggan. | Ini telah dibawa kepada pencapaian baris kontrak pencapaian dan invois. |
| Cukai | Cipta Cepat | Jumlah cukai yang dikenakan ke atas pencapaian tersebut. | Ini telah dibawa kepada pencapaian baris kontrak pencapaian dan invois. |

3. Pilih **Simpan dan Tutup**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]