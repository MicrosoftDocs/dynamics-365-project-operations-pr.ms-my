---
title: Gambaran keseluruhan pengekalan vendor
description: Topik ini memberikan gambaran keseluruhan keupayaan pengekalan vendor.
author: sigitac
ms.date: 10/01/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f9e4a1e63e47524bb622771f645c04e61c279496
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588471"
---
# <a name="vendor-retention-overview"></a>Gambaran keseluruhan pengekalan vendor

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Organisasi anda mungkin mahu mengekalkan sebahagian daripada pembayaran kepada vendor yang bekerja pada projek untuk organisasi anda. Contohnya, sebelum anda membayar vendor anda, anda mungkin mahu memastikan item dan perkhidmatan yang diberikan memenuhi jangkaan anda.

Semasa anda merundingkan pembelian untuk projek dengan vendor, anda boleh menentukan terma pengekalan vendor yang merangkumi peratusan atau jumlah yang akan dikekalkan. Apabila vendor menghantar item dan perkhidmatan, anda memotong peratusan pengekalan yang ditentukan atau jumlah daripada pembayaran anda kepada vendor. Apabila projek selesai atau mencapai peringkat interim seperti yang ditetapkan dalam kontrak vendor, anda mengeluarkan jumlah yang dikekalkan dan mencipta pembayaran kepada vendor.

## <a name="vendor-retention-example"></a>Contoh pengekalan vendor

Contoh berikut menunjukkan cara peratusan jumlah invois vendor dikekalkan berdasarkan pada peratusan yang telah dilengkapkan untuk projek.

Contoso Robotics USA mempunyai kontrak dengan vendor Fabrikam untuk memberikan latihan selama 100 jam bagi projek pembaharuan peralatan. Jumlah nilai kontrak ialah USD 30,000 dengan harga pembelian yang dipersetujui bagi USD 300 sejam.

Latihan akan diberikan dalam tiga fasa dengan jadual berikut:

- Fasa 1: 50 jam atau 50 peratus daripada projek
- Fasa 2: 30 jam atau jumlah 80 peratus daripada projek
- Fasa 3: 20 jam atau 100 peratus daripada projek

Jadual berikut menyenaraikan terma pengekalan.

| **Peratusan unit dihantar** | **Peratusan untuk dikekalkan** | **Peratusan untuk dilepaskan** |
| --- | --- | --- |
| 50% | 20% | 0% |
| 80% | 10% | 10% |
| 100% | 0% | 100% |

Hasil transaksi dalam jumlah berikut:

- Fasa 1:
  - Jumlah perlu dibayar ialah 50 x 300 atau 15,000.
  - 20 peratus daripada jumlah atau 3,000, dikekalkan dan akan dilepaskan pada peringkat kemudian.
  - Jumlah yang dibayar kepada vendor ialah 12,000.
- Fasa 2:
  - Jumlah perlu dibayar ialah 30 x 300 atau 9,000.
  - 10 peratus daripada jumlah atau 900, dikekalkan.
  - 10 peratus daripada 3,000 yang dikekalkan dalam Fasa 1 atau 300, dilepaskan.
  - Jumlah yang dibayar kepada vendor ialah 8,400. Jumlah ini ialah 9,000 kurang daripada pengekalan 900 ditambah dengan 300 yang dilepaskan daripada pengekalan Fasa 1.
- Fasa 3:
  - Jumlah perlu dibayar ialah 20 x 300 atau 6,000.
  - Tiada jumlah dikekalkan.
  - Jumlah yang dilepaskan ialah 3,600. Jumlah ini terdiri daripada 3,000 yang dikekalkan dalam Fasa 1, ditolak 300 daripada Fasa 1 yang dilepaskan dalam Fasa 2, ditambah dengan 900 yang dikekalkan dalam Fasa 2.
  - Jumlah yang dibayar kepada vendor ialah 9,600. Jumlah ini terdiri daripada jumlah 3,600 yang dikekalkan ditambah dengan 6,000 untuk pelengkapan Fasa 3.

Jumlah amaun yang dibayar kepada vendor selepas tiga fasa lengkap adalah 30,000 yang merupakan jumlah pesanan pembelian (15,000 + 9,000 + 6,000).
