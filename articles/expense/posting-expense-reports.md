---
title: Siarkan laporan perbelanjaan
description: Artikel ini menerangkan cara menyiarkan laporan perbelanjaan.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524881"
---
# <a name="post-expense-reports"></a>Siarkan laporan perbelanjaan

Selepas laporan perbelanjaan diluluskan dan dipindahkan kepada jurnal umum, laporan ini boleh disiarkan. Apabila anda menyiarkan laporan perbelanjaan, perbelanjaan yang layak untuk pemulihan cukai ditambahkan nilai (VAT) dikenal pasti. Tugas penentusahan dan pemulihan bayaran VAT diperuntukkan kepada pekerja yang bertanggungjawab untuk menentusahkan laporan perbelanjaan tersebut.

Jika perbelanjaan pada laporan perbelanjaan dikenakan kepada syarikat selain syarikat yang merupakan majikan pekerja tersebut, anda mesti menentusahkan perbelanjaan yang dipinjamkan kepada syarikat dan perbelanjaan yang dipinjamkan daripada syarikat. Contohnya, pekerja yang menyerahkan laporan perbelanjaan bekerja untuk syarikat DAT tetapi mengenakan perbelanjaan kepada syarikat DIR. Dalam kes ini, perbelanjaan dipinjamkan kepada syarikat DAT dan perbelanjaan tersebut dipinjamkan daripada syarikat DIR. Selepas anda menentusahkan baris jurnal ini, anda boleh menyiarkan baris perbelanjaan pada lejar umum.

Untuk menyiarkan laporan perbelanjaan, pada halaman **Laporan perbelanjaan yang diluluskan**, pilih laporan perbelanjaan dan kemudian, pada Anak Tetingkap Tindakan, pilih **Siarkan**.

Anda juga boleh menyiarkan semua laporan perbelanjaan dalam senarai pada masa yang sama. Pilih semua laporan perbelanjaan dan kemudian pilih **Siarkan**.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>Membolehkan Keupayaan untuk menyiarkan liabiliti perbelanjaan dalam mata wang vendor untuk ciri kaedah pembayaran tunai

Keupayaan **untuk menyiarkan liabiliti perbelanjaan dalam mata wang vendor untuk ciri kaedah** pembayaran tunai membolehkan laporan perbelanjaan diposkan dalam mata wang vendor untuk kaedah pembayaran tunai.

Pada masa ini, apabila anda menyerahkan perbelanjaan tunai, laporan perbelanjaan dipaparkan dalam mata wang perakaunan. Kerana penukaran amaun di kalangan mata wang transaksi, mata wang perakaunan, dan mata wang vendor, jumlah yang salah dibayar kepada vendor jika tarikh transaksi perbelanjaan dan tarikh pembayaran sebenar mempunyai kadar pertukaran yang berbeza.

Ciri ini akan memastikan baki vendor direkodkan dalam mata wang vendor apabila laporan perbelanjaan disiarkan.

1. Pergi ke **Ruang kerja** \> **Pengurusan Ciri**.
2. Dalam senarai, cari dan pilih **Keupayaan untuk menyiarkan liabiliti perbelanjaan dalam mata wang vendor untuk kaedah** pembayaran tunai, dan kemudian pilih **Dayakan sekarang**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
