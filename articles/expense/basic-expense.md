---
title: Entri perbelanjaan (ringan)
description: Topik ini memberikan maklumat tentang cara untuk bekerja dengan entri perbelanjaan dalam pelaksanaan ringan.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081112"
---
# <a name="expense-entry-lite"></a>Entri perbelanjaan (ringan)

_**Gunakan pada:** Pelaksanaan ringan - urusan dengan invois proforma_

Asas, atau ringan, pengurusan perbelanjaan ialah keupayaan untuk merekodkan perbelanjaan mudah. Anda boleh merekodkan perbelanjaan terhadap projek, dan kemudian pelulus projek akan menyemak dan meluluskannya.

Untuk mendapatkan maklumat lanjut tentang keupayaan perbelanjaan dalam Dynamics 365 Project Operations, lihat [Gambaran keseluruhan perbelanjaan](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Merekodkan perbelanjaan asas

Anda boleh merekodkan perbelanjaan anda supaya anda boleh menyerahkannya kepada pelulus.

1. Pergi ke **Perbelanjaan** dan pilih **Baharu**.
2. Pada halaman **Perbelanjaan Baharu** , masukkan maklumat perbelanjaan yang diperlukan dan kemudian pilih **Simpan**.

## <a name="submit-a-basic-expense"></a>Menyerahkan perbelanjaan asas

Selepas anda selesai merekodkan semua perbelanjaan anda, dan anda bersedia untuk mendapatkan kelulusan untuknya, anda mesti menyerahkannya.

1. Pergi ke **Perbelanjaan** dan pilih perbelanjaan. Atau, pilih semua perbelanjaan dengan menggunakan kotak semak pada pengepala.
2. Pilih **Serahkan**. Sistem memproses entri yang dipilih dan kemudian mencipta permintaan kelulusan perbelanjaan.

## <a name="recall-a-basic-expense"></a>Tarik balik perbelanjaan asas

Apabila anda menyerahkan perbelanjaan dengan tidak sengaja, anda boleh menariknya balik. Masa yang diperlukan untuk menarik balik entri perbelanjaan bergantung pada peringkat kelulusannya.  Jika pelulus belum meluluskan entri itu, tarik balik boleh berlaku dengan serta-merta. Walau bagaimanapun, jika entri telah diluluskan, pelulus diminta untuk meluluskan tarik balik dan membalikkan transaksi tersebut.

1. Pergi ke **Perbelanjaan** , dan kemudian, dalam senarai perbelanjaan, pilih perbelanjaan untuk ditarik balik.
2. Pilih **Tarik balik**. Jika entri perbelanjaan belum lagi diluluskan, sistem menarik balik ia dengan segera. Jika entri perbelanjaan telah diluluskan, permintaan tarik balik dibuat untuk memberitahu pelulus yang anda mahu membalikkan perbelanjaan itu. Pelulus akan mengesahkan yang pembalikan boleh dilakukan dan entri akan dikembalikan.

## <a name="delete-a-basic-expense"></a>Padamkan perbelanjaan asas

Perbelanjaan yang belum diserahkan boleh dipadamkan. Untuk memadamkan perbelanjaan yang telah diserahkan, anda mesti menarik balik perbelanjaan itu terlebih dahulu.

## <a name="see-also"></a>Lihat juga

- [Gambaran keseluruhan kelulusan](../approvals/approvals-overview.md)
