---
title: Pencapaian baris subkontrak
description: Topik ini menerangkan cara mencipta dan menyelenggarkan jadual invois berasaskan pencapaian untuk subkontrak dengan vendor.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3301e5a627e4842009fcd5e352f1b76fd3053ee3
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323787"
---
# <a name="subcontract-line-milestones"></a>Pencapaian baris subkontrak

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Dalam Dynamics 365 Project Operations, baris subkontrak dengan kaedah pengebilan harga tetap boleh menentukan jadual invois berasaskan pencapaian dengan vendor.

Pencapaian untuk penginvoisan vendor boleh dijanakan secara automatik menggunakan kekerapan yang ditetapkan, atau anda boleh menciptanya secara manual.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Cipta jadual invois berasaskan pencapaian secara automatik untuk baris subkontrak

Lengkapkan langkah berikut untuk menjanakan jadual invois berasaskan pencapaian secara automatik untuk set tetap pencapaian yang teragih dengan sekata.

1. Pergi ke **Tetapan** > **Kekerapan Invois** dan sediakan kekerapan invois untuk baris subkontrak.
2. Buka halaman **Subkontrak**, buka subkontrak yang ingin anda usahakan, dan kemudian buka baris subkontrak harga tetap yang akan anda ciptakan jadual pencapaian.
3. Pada tab **Pencapaian Baris Subkontrak**, pilih **Janakan Pencapaian Berkala**.
4. Dalam kotak dialog, masukkan atau pilih julat tarikh, bilangan pencapaian dan kekerapan invois. Anda boleh memilih tarikh mula atau anda boleh memilih bilangan pencapaian dan kekerapan invois atau tarikh mula, atau anda boleh memilih tarikh tamat dan kekerapan invois. Anda tidak boleh memilih tarikh tamat dan bilangan pencapaian.
Dengan menggunakan maklumat ini, sistem menjanakan pencapaian dan rekod yang ditunjukkan dalam grid **Pencapaian**.

   - **Nama Pencapaian** – Nama pencapaian ditetapkan pada tarikh pencapaian berdasarkan kekerapan invois.
   - **Tarikh Pencapaian** – Tarikh berdasarkan kekerapan invois.
   - **Jumlah Pencapaian** - Dikira dengan membahagikan amaun jumlah kecil pada baris subkontrak terhadap bilangan pencapaian.

Jika baris subkontrak mempunyai nilai dalam medan **Amaun Cukai Anggaran**, nilai ini akan ditambah kepada setiap pencapaian secara sekata apabila menjanakan pencapaian berkala.

Jumlah amaun pencapaian baris subkontrak hendaklah sama dengan nilai baris subkontrak. Jika ia tidak sama, ralat berlaku. Anda boleh membetulkan ralat dan mengesahkan bahawa jumlah pencapaian adalah sama dengan nilai baris subkontrak dengan mencipta, mengedit atau memadamkan pencapaian dan amaun cukai. Selepas perubahan dibuat, simpan dan segar semula halaman untuk memastikan tiada lagi ralat.

## <a name="manually-create-subcontract-line-milestones"></a>Cipta pencapaian baris subkobtrak secara manual

Pencapaian harga tetap pada baris subkontrak boleh dijanakan secara manual apabila pencapaian tidak dipisahkan secara berkala. Untuk mencipta pencapaian baris subkontrak secara manual, lengkapkan langkah berikut.

1. Pada anak tetingkap navigasi, pilih **Subkontrak** dan buka subkontrak yang ingin anda usahakan.
2. Buka baris subkontrak harga tetap yang ingin anda ciptakan pencapaian.
3. Pada tab **Pencapaian baris subkontrak**, pada subgrid, pilih **+ Pencapaian Baris Subkontrak Baharu**.
4. Pada halaman **Pencapaian Baris Subkontrak Baharu**, masukkan maklumat yang diperlukan berdasarkan jadual berikut.

    | Medan | Penerangan |
    | --- | --- |
    | Nama Pencapaian | Nama pencapaian. |
    | Penerangan | Perihalan pencapaian.  |
    | Tarikh Pencapaian Penting | Tarikh apabila proses penciptaan invois automatik harus mencari status pencapaian ini untuk menganggapnya sebagai invois. Nilai ini dimasukkan pada baris invois vendor apabila menghantar invois untuk subkontrak ini. |
    | Amaun | Jumlah atau nilai pencapaian yang akan diinvoiskan kepada pelanggan. Nilai ini dimasukkan pada baris invois vendor apabila menghantar invois untuk subkontrak ini. |
    | Cukai | Jumlah cukai yang dikenakan ke atas pencapaian tersebut. Nilai ini dimasukkan pada baris invois vendor apabila menghantar invois untuk subkontrak ini. |
    | Amaun selepas cukai | Medan baca sahaja ini dikira sebagai Amaun + Cukai. Nilai ini dimasukkan pada baris invois vendor apabila menghantar invois untuk subkontrak ini. |
    | Status Invois | Apabila pencapaian dicipta, status ini sentiasa ditetapkan kepada **Tidak sedia untuk penginvoisan**.  Apabila berstatus **Sedia untuk Diinvois**, penciptaan invois vendor termasuk pencapaian ini pada invois vendor. |

5. Pilih **Simpan dan Tutup**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
