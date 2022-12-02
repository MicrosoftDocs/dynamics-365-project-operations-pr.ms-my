---
title: Pencapaian baris subkontrak
description: Artikel ini menerangkan cara mencipta dan menyelenggara jadual invois berasaskan pencapaian untuk subkontrak dengan vendor.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 431a57adf82c79f72d44886636183d48e0931f53
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522476"
---
# <a name="subcontract-line-milestones"></a>Pencapaian baris subkontrak

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

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

    | Medan | Penerangan |Kesan kefungsian|
    | --- | --- |----------------------|
    | Nama Pencapaian | Nama pencapaian. |Ini akan ditunjukkan sebagai lajur pertama dalam semua carian berdasarkan pada pencapaian baris subkontrak. Baris invois vendor yang dicipta berdasarkan pada pencapaian ini juga akan menggunakan nama pencapaian baris subkontrak sebagai nama lalai bagi baris invois vendor.|
    | Penerangan | Perihalan pencapaian. |Baris invois vendor yang dicipta berdasarkan pada pencapaian ini juga akan menggunakan perihalan pencapaian baris subkontrak sebagai perihalan lalai bagi baris invois vendor.|
    | Tarikh Pencapaian Penting | Tarikh apabila proses penciptaan invois automatik harus mencari status pencapaian ini untuk menganggapnya sebagai invois.| Nilai ini akan digunakan sebagai tarikh lalai bagi baris invois vendor apabila menginvois untuk baris subkontrak ini. |
    | Amaun | Jumlah atau nilai pencapaian yang akan diinvoiskan kepada pelanggan. |Nilai ini digunakan sebagai jumlah lalai pada baris invois vendor apabila menginvois untuk baris subkontrak ini. |
    | Cukai | Jumlah cukai yang dikenakan ke atas pencapaian tersebut.| Nilai ini digunakan sebagai jumlah cukai lalai pada baris invois vendor apabila menginvois untuk baris subkontrak ini. |
    | Amaun selepas cukai | Medan baca sahaja ini dikira sebagai Jumlah + Cukai.|Nilai ini digunakan sebagai lalai pada baris invois vendor apabila menginvois untuk baris subkontrak ini. |
    | Status Invois | Apabila pencapaian dicipta, status ini sentiasa ditetapkan kepada **Tidak sedia untuk penginvoisan**.|  Apabila berstatus **Sedia untuk Diinvois**, penciptaan invois vendor termasuk pencapaian ini pada invois vendor. |

5. Pilih **Simpan dan Tutup**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
